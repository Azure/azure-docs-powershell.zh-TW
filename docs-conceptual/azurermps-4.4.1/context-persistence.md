---
title: 在 PowerShell 工作階段之間保存使用者登入
description: 本文說明 Azure PowerShell 中的新功能，可讓您在多個 PowerShell 工作階段中重複使用認證和其他使用者資訊。
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/31/2017
ms.openlocfilehash: 8ef20796b64b16c78a653e293a57d5e752d89710
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/08/2018
---
# <a name="persisting-user-logins-across-powershell-sessions"></a><span data-ttu-id="34d70-103">在 PowerShell 工作階段之間保存使用者登入</span><span class="sxs-lookup"><span data-stu-id="34d70-103">Persisting user logins across PowerShell sessions</span></span>

<span data-ttu-id="34d70-104">在 Azure PowerShell 的 2017 年 9 月版本中，Azure Resource Manager Cmdlet 推出新的功能，**Azure 內容自動儲存**。</span><span class="sxs-lookup"><span data-stu-id="34d70-104">In the September 2017 release of Azure PowerShell, Azure Resource Manager cmdlets introduce a new feature, **Azure Context Autosave**.</span></span> <span data-ttu-id="34d70-105">這項功能會啟用數個新的使用者情節，包括：</span><span class="sxs-lookup"><span data-stu-id="34d70-105">This feature enables several new user scenarios, including:</span></span>

- <span data-ttu-id="34d70-106">在新的 PowerShell 工作階段中重複使用的登入資訊保留。</span><span class="sxs-lookup"><span data-stu-id="34d70-106">Retention of login information for reuse in new PowerShell sessions.</span></span>
- <span data-ttu-id="34d70-107">更易於使用的背景工作，可長時間執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="34d70-107">Easier use of background tasks for executing long-running cmdlets.</span></span>
- <span data-ttu-id="34d70-108">在帳戶、訂用帳戶及環境之間進行切換，而無須個別登入。</span><span class="sxs-lookup"><span data-stu-id="34d70-108">Switch between accounts, subscriptions, and environments without a separate login.</span></span>
- <span data-ttu-id="34d70-109">使用不同的認證和訂用帳戶，同時從相同的 PowerShell 工作階段執行工作。</span><span class="sxs-lookup"><span data-stu-id="34d70-109">Execution of tasks using different credentials and subscriptions, simultaneously, from the same PowerShell session.</span></span>

## <a name="azure-contexts-defined"></a><span data-ttu-id="34d70-110">定義的 Azure 內容</span><span class="sxs-lookup"><span data-stu-id="34d70-110">Azure contexts defined</span></span>

<span data-ttu-id="34d70-111">Azure 內容是一組資訊，可定義 Azure PowerShell Cmdlet 的目標。</span><span class="sxs-lookup"><span data-stu-id="34d70-111">An *Azure context* is a set of information that defines the target of Azure PowerShell cmdlets.</span></span> <span data-ttu-id="34d70-112">內容是由五個部分所組成：</span><span class="sxs-lookup"><span data-stu-id="34d70-112">The context consists of five parts:</span></span>

- <span data-ttu-id="34d70-113">帳戶 - 用來驗證與 Azure 通訊的使用者名稱或服務主體</span><span class="sxs-lookup"><span data-stu-id="34d70-113">An *Account* - the UserName or Service Principal used to authenticate communications with Azure</span></span>
- <span data-ttu-id="34d70-114">訂用帳戶 - 包含要進行處理之資源的 Azure 訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="34d70-114">A *Subscription* - The Azure Subscription containing the Resources being acted upon.</span></span>
- <span data-ttu-id="34d70-115">租用戶 - 包含您訂用帳戶的 Azure Active Directory 租用戶。</span><span class="sxs-lookup"><span data-stu-id="34d70-115">A *Tenant* - The Azure Active Directory tenant that contains your subscription.</span></span> <span data-ttu-id="34d70-116">租用戶對於 ServicePrincipal 驗證較為重要。</span><span class="sxs-lookup"><span data-stu-id="34d70-116">Tenants are more important to ServicePrincipal authentication.</span></span>
- <span data-ttu-id="34d70-117">環境 - 作為目標的特定 Azure 雲端，通常是 Azure 的全域雲端。</span><span class="sxs-lookup"><span data-stu-id="34d70-117">An *Environment* - The particular Azure Cloud being targeted, usually the Azure global Cloud.</span></span>
  <span data-ttu-id="34d70-118">不過，環境設定也可讓您將國家/地區、政府和內部部署 (Azure Stack) 雲端作為目標。</span><span class="sxs-lookup"><span data-stu-id="34d70-118">However, the environment setting allows you to target National, Government, and on-premises (Azure Stack) clouds as well.</span></span>
- <span data-ttu-id="34d70-119">認證 - Azure 用來確認您的身分識別，並確定您在 Azure 中存取資源之授權的資訊</span><span class="sxs-lookup"><span data-stu-id="34d70-119">*Credentials* - The information used by Azure to verify your identity and ensure your authorization to access resources in Azure</span></span>

<span data-ttu-id="34d70-120">在舊版中，您每次開啟新的 PowerShell 工作階段時都必須建立 Azure 內容。</span><span class="sxs-lookup"><span data-stu-id="34d70-120">In previous releases, your Azure Context had to be created each time you opened a new PowerShell session.</span></span> <span data-ttu-id="34d70-121">從 Azure PowerShell v4.4.0 開始，您在每次開啟新的 PowerShell 工作階段時，可以啟用自動儲存和重複使用 Azure 內容。</span><span class="sxs-lookup"><span data-stu-id="34d70-121">Beginning with Azure PowerShell v4.4.0, you can enable the automatic saving and reuse of Azure Contexts whenever you open a new PowerShell session.</span></span>

## <a name="automatically-saving-the-context-for-the-next-login"></a><span data-ttu-id="34d70-122">自動儲存內容以供下一次登入使用</span><span class="sxs-lookup"><span data-stu-id="34d70-122">Automatically saving the context for the next login</span></span>

<span data-ttu-id="34d70-123">根據預設，每當您關閉 PowerShell 工作階段時，Azure PowerShell 就會捨棄內容資訊。</span><span class="sxs-lookup"><span data-stu-id="34d70-123">By default, Azure PowerShell discards your context information whenever you close the PowerShell session.</span></span>

<span data-ttu-id="34d70-124">若要讓 Azure PowerShell 在 PowerShell 工作階段關閉之後記住您的內容，請使用 `Enable-AzureRmContextAutosave`。</span><span class="sxs-lookup"><span data-stu-id="34d70-124">To allow Azure PowerShell to remember your context after the PowerShell session is closed, use `Enable-AzureRmContextAutosave`.</span></span> <span data-ttu-id="34d70-125">內容與認證資訊會自動儲存在您使用者目錄中的特殊隱藏資料夾中 (`%AppData%\Roaming\Windows Azure PowerShell`)。</span><span class="sxs-lookup"><span data-stu-id="34d70-125">Context and credential information are automatically saved in a special hidden folder in your user directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span>
<span data-ttu-id="34d70-126">接下來，每個新的 PowerShell 工作階段都會將您最後一個工作階段中使用的內容作為目標。</span><span class="sxs-lookup"><span data-stu-id="34d70-126">Subsequently, each new PowerShell session targets the context used in your last session.</span></span>

<span data-ttu-id="34d70-127">若要將 PowerShell 設定為忘記您的內容和認證，請使用 `Disable-AzureRmContextAutoSave`。</span><span class="sxs-lookup"><span data-stu-id="34d70-127">To set PowerShell to forget your context and credentials, use `Disable-AzureRmContextAutoSave`.</span></span> <span data-ttu-id="34d70-128">您每次開啟 PowerShell 工作階段時，都必須登入 Azure。</span><span class="sxs-lookup"><span data-stu-id="34d70-128">You will need to log in to Azure every time you open a PowerShell session.</span></span>

<span data-ttu-id="34d70-129">可讓您管理 Azure 內容的 Cmdlet 也能讓您進行更細緻的控制。</span><span class="sxs-lookup"><span data-stu-id="34d70-129">The cmdlets that allow you to manage Azure contexts also allow you fine grained control.</span></span> <span data-ttu-id="34d70-130">您是否僅需要將變更套用到目前的 PowerShell 工作階段 (`Process` 範圍) 還是要套用到每個 PowerShell 工作階段 (`CurrentUser` 範圍)。</span><span class="sxs-lookup"><span data-stu-id="34d70-130">If you want changes to apply only to the current PowerShell session (`Process` scope) or every PowerShell session (`CurrentUser` scope).</span></span> <span data-ttu-id="34d70-131">這些選項將在[使用內容範圍](#Using-Context-Scopes)中深入討論。</span><span class="sxs-lookup"><span data-stu-id="34d70-131">These options are discussed in mode detail in [Using Context Scopes](#Using-Context-Scopes).</span></span>

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a><span data-ttu-id="34d70-132">將 Azure PowerShell Cmdlet 作為背景作業執行</span><span class="sxs-lookup"><span data-stu-id="34d70-132">Running Azure PowerShell cmdlets as background jobs</span></span>

<span data-ttu-id="34d70-133">**Azure 內容自動儲存**功能也可讓您與 PowerShell 背景作業共用內容。</span><span class="sxs-lookup"><span data-stu-id="34d70-133">The **Azure Context Autosave** feature also allows you to share you context with PowerShell background jobs.</span></span> <span data-ttu-id="34d70-134">PowerShell 可讓您以背景作業形式啟動並監視長時間執行的工作，而不必等候工作完成。</span><span class="sxs-lookup"><span data-stu-id="34d70-134">PowerShell allows you to start and monitor long-executing tasks as background jobs without having to wait for the tasks to complete.</span></span> <span data-ttu-id="34d70-135">您可以利用兩種不同的方式來與背景作業共用認證：</span><span class="sxs-lookup"><span data-stu-id="34d70-135">You can share credentials with background jobs in two different ways:</span></span>

- <span data-ttu-id="34d70-136">傳遞內容作為引數</span><span class="sxs-lookup"><span data-stu-id="34d70-136">Passing the context as an argument</span></span>

  <span data-ttu-id="34d70-137">大部分的 AzureRM Cmdlet 可讓您將內容作為參數傳遞至 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="34d70-137">Most AzureRM cmdlets allow you to pass the context as a parameter to the cmdlet.</span></span> <span data-ttu-id="34d70-138">您可以將內容傳遞至背景作業，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="34d70-138">You can pass a context to a background job as shown in the following example:</span></span>

  ```powershell
  PS C:\> $job = Start-Job { param ($ctx) New-AzureRmVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzureRmContext)
  ```

- <span data-ttu-id="34d70-139">使用預設內容，並啟用自動儲存</span><span class="sxs-lookup"><span data-stu-id="34d70-139">Using the default context with Autosave enabled</span></span>

  <span data-ttu-id="34d70-140">如果您已啟用**內容自動儲存**，背景作業就會自動使用預設儲存的內容。</span><span class="sxs-lookup"><span data-stu-id="34d70-140">If you have enabled **Context Autosave**, background jobs automatically use the default saved context.</span></span>

  ```powershell
  PS C:\> $job = Start-Job { New-AzureRmVm [... Additional parameters ...]}
  ```

<span data-ttu-id="34d70-141">當您需要知道背景工作的結果時，請使用 `Get-Job` 來檢查作業狀態，並使用 `Wait-Job` 等候作業完成。</span><span class="sxs-lookup"><span data-stu-id="34d70-141">When you need to know the outcome of the background task, use `Get-Job` to check the job status and `Wait-Job` to wait for the Job to complete.</span></span> <span data-ttu-id="34d70-142">使用 `Receive-Job` 可擷取或顯示背景作業的輸出。</span><span class="sxs-lookup"><span data-stu-id="34d70-142">Use `Receive-Job` to capture or display the output of the background job.</span></span> <span data-ttu-id="34d70-143">如需詳細資訊，請參閱 [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs)。</span><span class="sxs-lookup"><span data-stu-id="34d70-143">For more information, see [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>

## <a name="creating-selecting-renaming-and-removing-contexts"></a><span data-ttu-id="34d70-144">建立、選取、重新命名和移除內容</span><span class="sxs-lookup"><span data-stu-id="34d70-144">Creating, selecting, renaming, and removing contexts</span></span>

<span data-ttu-id="34d70-145">若要建立內容，您必須登入 Azure。</span><span class="sxs-lookup"><span data-stu-id="34d70-145">To create a context, you must be logged in to Azure.</span></span> <span data-ttu-id="34d70-146">`Add-AzureRmAccount` Cmdlet (或其別名 `Login-AzureRmAccount`) 會設定後續 Azure PowerShell Cmdlet 所使用的預設內容，並可讓您存取登入認證所允許的任何租用戶或訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="34d70-146">The `Add-AzureRmAccount` cmdlet (or its alias, `Login-AzureRmAccount`) sets the default context used by subsequent Azure PowerShell cmdlets, and allows you to access any tenants or subscriptions allowed by your login credentials.</span></span>

<span data-ttu-id="34d70-147">若要在登入之後新增內容，請使用 `Set-AzureRmContext` (或其別名 `Select-AzureRmSubscription`)。</span><span class="sxs-lookup"><span data-stu-id="34d70-147">To add a new context after login, use `Set-AzureRmContext` (or its alias, `Select-AzureRmSubscription`).</span></span>

```powershell
PS C:\> Set-AzureRMContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

<span data-ttu-id="34d70-148">上一個範例會使用目前的認證來新增目標為 'Contoso Subscription 1' 的新內容。</span><span class="sxs-lookup"><span data-stu-id="34d70-148">The previous example adds a new context targeting 'Contoso Subscription 1' using your current credentials.</span></span> <span data-ttu-id="34d70-149">新的內容名為 'Contoso1'。</span><span class="sxs-lookup"><span data-stu-id="34d70-149">The new context is named 'Contoso1'.</span></span> <span data-ttu-id="34d70-150">如果您未提供內容的名稱，就會使用使用帳戶識別碼和訂用帳戶識別碼的預設名稱。</span><span class="sxs-lookup"><span data-stu-id="34d70-150">If you do not provide a name for the context, a default name, using the account ID and subscription ID is used.</span></span>

<span data-ttu-id="34d70-151">若要將現有的內容重新命名，請使用 `Rename-AzureRmContext` Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="34d70-151">To rename an existing context, use the `Rename-AzureRmContext` cmdlet.</span></span> <span data-ttu-id="34d70-152">例如︰</span><span class="sxs-lookup"><span data-stu-id="34d70-152">For example:</span></span>

```powershell
PS C:\> Rename-AzureRmContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

<span data-ttu-id="34d70-153">這個範例會將包含自動名稱 `[user1@contoso.org; 123456-7890-1234-564321]` 的內容重新命名為簡單名稱 'Contoso2'。</span><span class="sxs-lookup"><span data-stu-id="34d70-153">This example renames the context with automatic name `[user1@contoso.org; 123456-7890-1234-564321]` to the simple name 'Contoso2'.</span></span> <span data-ttu-id="34d70-154">管理內容的 Cmdlet 也會使用索引標籤完成，讓您能快速選取內容。</span><span class="sxs-lookup"><span data-stu-id="34d70-154">Cmdlets that manage contexts also use tab completion, allowing you to quickly select the context.</span></span>

<span data-ttu-id="34d70-155">最後，若要移除內容，請使用 `Remove-AzureRmContext` Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="34d70-155">Finally, to remove a context, use the `Remove-AzureRmContext` cmdlet.</span></span>  <span data-ttu-id="34d70-156">例如︰</span><span class="sxs-lookup"><span data-stu-id="34d70-156">For example:</span></span>

```powershell
PS C:\> Remove-AzureRmContext Contoso2
```

<span data-ttu-id="34d70-157">忘記名為 'Contoso2' 的內容。</span><span class="sxs-lookup"><span data-stu-id="34d70-157">Forgets the context that was named 'Contoso2'.</span></span> <span data-ttu-id="34d70-158">您後續可以使用 `Set-AzureRmContext` 來重新建立此內容</span><span class="sxs-lookup"><span data-stu-id="34d70-158">You can recreate this context subsequently using `Set-AzureRmContext`</span></span>

## <a name="removing-credentials"></a><span data-ttu-id="34d70-159">移除認證</span><span class="sxs-lookup"><span data-stu-id="34d70-159">Removing credentials</span></span>

<span data-ttu-id="34d70-160">您可以使用 `Remove-AzureRmAccount` (也稱為 `Logout-AzureRmAccount`) 來移除使用者或服務主體的所有憑證和相關聯內容。</span><span class="sxs-lookup"><span data-stu-id="34d70-160">You can remove all credentials and associated contexts for a user or service principal using `Remove-AzureRmAccount` (also known as `Logout-AzureRmAccount`).</span></span> <span data-ttu-id="34d70-161">在無參數的情況下執行時，`Remove-AzureRmAccount` Cmdlet 會移除目前內容中與使用者或服務主體相關聯的所有認證和內容。</span><span class="sxs-lookup"><span data-stu-id="34d70-161">When executed without parameters, the `Remove-AzureRmAccount` cmdlet removes all credentials and contexts associated with the User or Service Principal in the current context.</span></span> <span data-ttu-id="34d70-162">您可以傳入使用者名稱、服務主體名稱或內容，將特定的主體作為目標。</span><span class="sxs-lookup"><span data-stu-id="34d70-162">You may pass in a Username, Service Principal Name, or context to target a particular principal.</span></span>

```powershell
Remove-AzureRmAccount user1@contoso.org
```

## <a name="using-context-scopes"></a><span data-ttu-id="34d70-163">使用內容範圍</span><span class="sxs-lookup"><span data-stu-id="34d70-163">Using context scopes</span></span>

<span data-ttu-id="34d70-164">有時候，您需要在不影響其他工作階段的情況下，選取、變更或移除 PowerShell 工作階段中的內容。</span><span class="sxs-lookup"><span data-stu-id="34d70-164">Occasionally, you may want to select, change, or remove a context in a PowerShell session without impacting other sessions.</span></span> <span data-ttu-id="34d70-165">若要變更內容 Cmdlet 的預設行為，請使用 `Scope` 參數。</span><span class="sxs-lookup"><span data-stu-id="34d70-165">To change the default behavior of context cmdlets, use the `Scope` parameter.</span></span> <span data-ttu-id="34d70-166">`Process` 範圍會覆寫預設行為，方法是僅使其套用於目前的工作階段。</span><span class="sxs-lookup"><span data-stu-id="34d70-166">The `Process` scope overrides the default behavior by making it apply only for the current session.</span></span> <span data-ttu-id="34d70-167">相反地，`CurrentUser` 範圍會變更所有工作階段，而非只有目前工作階段中的內容。</span><span class="sxs-lookup"><span data-stu-id="34d70-167">Conversely `CurrentUser` scope changes the context in all sessions, instead of just the current session.</span></span>

<span data-ttu-id="34d70-168">例如，若要在不影響其他視窗的情況下，變更目前 PowerShell 工作階段中的預設內容，或是下次開啟工作階段時使用的內容，請使用：</span><span class="sxs-lookup"><span data-stu-id="34d70-168">As an example, to change the default context in the current PowerShell session without impacting other windows, or the context used the next time a session is opened, use:</span></span>

```powershell
PS C:\> Select-AzureRmContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a><span data-ttu-id="34d70-169">會記住內容自動儲存設定的方式</span><span class="sxs-lookup"><span data-stu-id="34d70-169">How the context autosave setting is remembered</span></span>

<span data-ttu-id="34d70-170">內容自動儲存設定會儲存到使用者 Azure PowerShell 目錄 (`%AppData%\Roaming\Windows Azure PowerShell`)。</span><span class="sxs-lookup"><span data-stu-id="34d70-170">The context AutoSave setting is saved to the user Azure PowerShell directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span> <span data-ttu-id="34d70-171">部分類型的電腦帳戶可能無法存取此目錄。</span><span class="sxs-lookup"><span data-stu-id="34d70-171">Some kinds of computer accounts may not have access to this directory.</span></span> <span data-ttu-id="34d70-172">如需這類的情節，您可以使用環境變數</span><span class="sxs-lookup"><span data-stu-id="34d70-172">For such scenarios, you can use the environment variable</span></span>

```powershell
$env:AzureRmContextAutoSave="true" | "false"
```

<span data-ttu-id="34d70-173">如果設為 'true'，就會自動儲存內容。</span><span class="sxs-lookup"><span data-stu-id="34d70-173">If set to 'true', the context is automatically saved.</span></span> <span data-ttu-id="34d70-174">如果設為 'false'，就不會自動儲存內容。</span><span class="sxs-lookup"><span data-stu-id="34d70-174">If set to 'false', the context is not saved.</span></span>

## <a name="changes-to-the-azurermprofile-module"></a><span data-ttu-id="34d70-175">對 AzureRM.Profile 模組的變更</span><span class="sxs-lookup"><span data-stu-id="34d70-175">Changes to the AzureRM.Profile module</span></span>

<span data-ttu-id="34d70-176">新的 Cmdlet，可管理內容</span><span class="sxs-lookup"><span data-stu-id="34d70-176">New cmdlets for managing context</span></span>

- <span data-ttu-id="34d70-177">[Enable-AzureRmContextAutosave][enable] - 可在 Powershell 工作階段之間儲存內容。</span><span class="sxs-lookup"><span data-stu-id="34d70-177">[Enable-AzureRmContextAutosave][enable] - Allow saving the context between powershell sessions.</span></span>
  <span data-ttu-id="34d70-178">任何變更都會改變全域內容。</span><span class="sxs-lookup"><span data-stu-id="34d70-178">Any changes alter the global context.</span></span>
- <span data-ttu-id="34d70-179">[Disable-AzureRmContextAutosave][disable] - 關閉自動儲存內容。</span><span class="sxs-lookup"><span data-stu-id="34d70-179">[Disable-AzureRmContextAutosave][disable] - Turn off autosaving the context.</span></span> <span data-ttu-id="34d70-180">需要每個新的 PowerShell 工作階段才能再次登入。</span><span class="sxs-lookup"><span data-stu-id="34d70-180">Each new PowerShell session is required to log in again.</span></span>
- <span data-ttu-id="34d70-181">[Select-AzureRmContext][select] - 選取內容作為預設值。</span><span class="sxs-lookup"><span data-stu-id="34d70-181">[Select-AzureRmContext][select] - Select a context as the default.</span></span> <span data-ttu-id="34d70-182">所有後續的 Cmdlet 都會使用此內容中的認證來進行驗證。</span><span class="sxs-lookup"><span data-stu-id="34d70-182">All subsequent cmdlets use the credentials in this context for authentication.</span></span>
- <span data-ttu-id="34d70-183">[Remove-AzureRmAccount][remove-cred] - 將與帳戶相關聯的所有認證和內容移除。</span><span class="sxs-lookup"><span data-stu-id="34d70-183">[Remove-AzureRmAccount][remove-cred] - Remove all credentials and contexts associated with an account.</span></span>
- <span data-ttu-id="34d70-184">[Remove-AzureRmContext][remove-context] - 將已命名的內容移除。</span><span class="sxs-lookup"><span data-stu-id="34d70-184">[Remove-AzureRmContext][remove-context] - Remove a named context.</span></span>
- <span data-ttu-id="34d70-185">[Rename-AzureRmContext][rename] - 將現有的內容重新命名。</span><span class="sxs-lookup"><span data-stu-id="34d70-185">[Rename-AzureRmContext][rename] - Rename an existing context.</span></span>

<span data-ttu-id="34d70-186">對現有設定檔 Cmdlet 的變更</span><span class="sxs-lookup"><span data-stu-id="34d70-186">Changes to existing profile cmdlets</span></span>

- <span data-ttu-id="34d70-187">[Add-AzureRmAccount][login] - 允許登入程序或目前使用者的範圍。</span><span class="sxs-lookup"><span data-stu-id="34d70-187">[Add-AzureRmAccount][login] - Allow scoping of the login to the process or the current user.</span></span>
  <span data-ttu-id="34d70-188">允許登入之後命名預設內容。</span><span class="sxs-lookup"><span data-stu-id="34d70-188">Allow naming the default context after login.</span></span>
- <span data-ttu-id="34d70-189">[Import-AzureRmContext][import] - 允許登入程序或目前使用者的範圍。</span><span class="sxs-lookup"><span data-stu-id="34d70-189">[Import-AzureRmContext][import] - Allow scoping of the login to the process or the current user.</span></span>
- <span data-ttu-id="34d70-190">[Set-AzureRmContext][set-context] - 允許選取現有的已命名內容，以及對程序或目前使用者的範圍變更。</span><span class="sxs-lookup"><span data-stu-id="34d70-190">[Set-AzureRmContext][set-context] - Allow selection of existing named contexts, and scope changes to the process or current user.</span></span>

<!-- Hyperlinks -->
[enable]: /powershell/module/azurerm.profile/Enable-AzureRmContextAutosave
[disable]: /powershell/module/azurerm.profile/Disable-AzureRmContextAutosave
[select]: /powershell/module/azurerm.profile/Select-AzureRmContext
[remove-cred]: /powershell/module/azurerm.profile/Remove-AzureRmAccount
[remove-context]: /powershell/module/azurerm.profile/Remove-AzureRmContext
[rename]: /powershell/module/azurerm.profile/Rename-AzureRmContext

<!-- Updated cmdlets -->
[login]: /powershell/module/azurerm.profile/Add-AzureRmAccount
[import]: /powershell/module/azurerm.profile/Import-AzureRmAccount
[set-context]: /powershell/module/azurerm.profile/Import-AzureRmContext
