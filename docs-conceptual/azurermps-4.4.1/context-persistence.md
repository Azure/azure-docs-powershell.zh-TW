---
title: 在 PowerShell 工作階段之間保存使用者認證
description: 了解如何重覆使用 Azure 認證及多個 PowerShell 工作階段之間的其他資訊。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/31/2017
ms.openlocfilehash: 85de158cd2a4c3a38f653a530db8e6fae50cb37f
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/08/2018
ms.locfileid: "51275158"
---
# <a name="persisting-user-credentials-across-powershell-sessions"></a><span data-ttu-id="b5a7d-103">在 PowerShell 工作階段之間保存使用者認證</span><span class="sxs-lookup"><span data-stu-id="b5a7d-103">Persisting user credentials across PowerShell sessions</span></span>

<span data-ttu-id="b5a7d-104">Azure PowerShell 提供了稱為 **Azure 內容自動儲存**的功能，可提供下列功能：</span><span class="sxs-lookup"><span data-stu-id="b5a7d-104">Azure PowerShell offers a feature called **Azure Context Autosave**, which gives the following features:</span></span>

- <span data-ttu-id="b5a7d-105">在新的 PowerShell 工作階段中重複使用的登入資訊保留。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-105">Retention of sign in information for reuse in new PowerShell sessions.</span></span>
- <span data-ttu-id="b5a7d-106">更易於使用的背景工作，可長時間執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-106">Easier use of background tasks for executing long-running cmdlets.</span></span>
- <span data-ttu-id="b5a7d-107">在帳戶、訂用帳戶及環境之間進行切換，而無須個別登入。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-107">Switch between accounts, subscriptions, and environments without a separate sign in.</span></span>
- <span data-ttu-id="b5a7d-108">使用不同的認證和訂用帳戶，同時從相同的 PowerShell 工作階段執行工作。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-108">Execution of tasks using different credentials and subscriptions, simultaneously, from the same PowerShell session.</span></span>

## <a name="azure-contexts-defined"></a><span data-ttu-id="b5a7d-109">定義的 Azure 內容</span><span class="sxs-lookup"><span data-stu-id="b5a7d-109">Azure contexts defined</span></span>

<span data-ttu-id="b5a7d-110">Azure 內容是一組資訊，可定義 Azure PowerShell Cmdlet 的目標。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-110">An *Azure context* is a set of information that defines the target of Azure PowerShell cmdlets.</span></span> <span data-ttu-id="b5a7d-111">內容是由五個部分所組成：</span><span class="sxs-lookup"><span data-stu-id="b5a7d-111">The context consists of five parts:</span></span>

- <span data-ttu-id="b5a7d-112">帳戶 - 用來驗證與 Azure 通訊的使用者名稱或服務主體</span><span class="sxs-lookup"><span data-stu-id="b5a7d-112">An *Account* - the UserName or Service Principal used to authenticate communications with Azure</span></span>
- <span data-ttu-id="b5a7d-113">訂用帳戶 - 包含要進行處理之資源的 Azure 訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-113">A *Subscription* - The Azure Subscription containing the Resources being acted upon.</span></span>
- <span data-ttu-id="b5a7d-114">租用戶 - 包含您訂用帳戶的 Azure Active Directory 租用戶。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-114">A *Tenant* - The Azure Active Directory tenant that contains your subscription.</span></span> <span data-ttu-id="b5a7d-115">租用戶對於 ServicePrincipal 驗證較為重要。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-115">Tenants are more important to ServicePrincipal authentication.</span></span>
- <span data-ttu-id="b5a7d-116">環境 - 作為目標的特定 Azure 雲端，通常是 Azure 的全域雲端。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-116">An *Environment* - The particular Azure Cloud being targeted, usually the Azure global Cloud.</span></span>
  <span data-ttu-id="b5a7d-117">不過，環境設定也可讓您將國家/地區、政府和內部部署 (Azure Stack) 雲端作為目標。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-117">However, the environment setting allows you to target National, Government, and on-premises (Azure Stack) clouds as well.</span></span>
- <span data-ttu-id="b5a7d-118">認證 - Azure 用來確認您的身分識別，並確定您在 Azure 中存取資源之授權的資訊</span><span class="sxs-lookup"><span data-stu-id="b5a7d-118">*Credentials* - The information used by Azure to verify your identity and ensure your authorization to access resources in Azure</span></span>

<span data-ttu-id="b5a7d-119">在舊版中，您每次開啟新的 PowerShell 工作階段時都必須建立 Azure 內容。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-119">In previous releases, your Azure Context had to be created each time you opened a new PowerShell session.</span></span> <span data-ttu-id="b5a7d-120">從 Azure PowerShell v4.4.0 開始，您在每次開啟新的 PowerShell 工作階段時，可以啟用自動儲存和重複使用 Azure 內容。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-120">Beginning with Azure PowerShell v4.4.0, you can enable the automatic saving and reuse of Azure Contexts whenever you open a new PowerShell session.</span></span>

## <a name="automatically-saving-the-context-for-the-next-sign-in"></a><span data-ttu-id="b5a7d-121">自動儲存內容以供下一次登入使用</span><span class="sxs-lookup"><span data-stu-id="b5a7d-121">Automatically saving the context for the next sign in</span></span>

<span data-ttu-id="b5a7d-122">根據預設，每當您關閉 PowerShell 工作階段時，Azure PowerShell 就會捨棄內容資訊。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-122">By default, Azure PowerShell discards your context information whenever you close the PowerShell session.</span></span>

<span data-ttu-id="b5a7d-123">若要讓 Azure PowerShell 在 PowerShell 工作階段關閉之後記住您的內容，請使用 `Enable-AzureRmContextAutosave`。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-123">To allow Azure PowerShell to remember your context after the PowerShell session is closed, use `Enable-AzureRmContextAutosave`.</span></span> <span data-ttu-id="b5a7d-124">內容與認證資訊會自動儲存在您使用者目錄中的特殊隱藏資料夾中 (`%AppData%\Roaming\Windows Azure PowerShell`)。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-124">Context and credential information are automatically saved in a special hidden folder in your user directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span>
<span data-ttu-id="b5a7d-125">接下來，每個新的 PowerShell 工作階段都會將您最後一個工作階段中使用的內容作為目標。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-125">Subsequently, each new PowerShell session targets the context used in your last session.</span></span>

<span data-ttu-id="b5a7d-126">若要將 PowerShell 設定為忘記您的內容和認證，請使用 `Disable-AzureRmContextAutoSave`。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-126">To set PowerShell to forget your context and credentials, use `Disable-AzureRmContextAutoSave`.</span></span> <span data-ttu-id="b5a7d-127">您每次開啟 PowerShell 工作階段時，都必須登入 Azure。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-127">You will need to sign in to Azure every time you open a PowerShell session.</span></span>

<span data-ttu-id="b5a7d-128">可讓您管理 Azure 內容的 Cmdlet 也能讓您進行更細緻的控制。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-128">The cmdlets that allow you to manage Azure contexts also allow you fine grained control.</span></span> <span data-ttu-id="b5a7d-129">您是否僅需要將變更套用到目前的 PowerShell 工作階段 (`Process` 範圍) 還是要套用到每個 PowerShell 工作階段 (`CurrentUser` 範圍)。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-129">If you want changes to apply only to the current PowerShell session (`Process` scope) or every PowerShell session (`CurrentUser` scope).</span></span> <span data-ttu-id="b5a7d-130">這些選項將在[使用內容範圍](#Using-Context-Scopes)中深入討論。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-130">These options are discussed in mode detail in [Using Context Scopes](#Using-Context-Scopes).</span></span>

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a><span data-ttu-id="b5a7d-131">將 Azure PowerShell Cmdlet 作為背景作業執行</span><span class="sxs-lookup"><span data-stu-id="b5a7d-131">Running Azure PowerShell cmdlets as background jobs</span></span>

<span data-ttu-id="b5a7d-132">**Azure 內容自動儲存**功能也可讓您與 PowerShell 背景作業共用內容。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-132">The **Azure Context Autosave** feature also allows you to share you context with PowerShell background jobs.</span></span> <span data-ttu-id="b5a7d-133">PowerShell 可讓您以背景作業形式啟動並監視長時間執行的工作，而不必等候工作完成。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-133">PowerShell allows you to start and monitor long-executing tasks as background jobs without having to wait for the tasks to complete.</span></span> <span data-ttu-id="b5a7d-134">您可以利用兩種不同的方式來與背景作業共用認證：</span><span class="sxs-lookup"><span data-stu-id="b5a7d-134">You can share credentials with background jobs in two different ways:</span></span>

- <span data-ttu-id="b5a7d-135">傳遞內容作為引數</span><span class="sxs-lookup"><span data-stu-id="b5a7d-135">Passing the context as an argument</span></span>

  <span data-ttu-id="b5a7d-136">大部分的 AzureRM Cmdlet 可讓您將內容作為參數傳遞至 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-136">Most AzureRM cmdlets allow you to pass the context as a parameter to the cmdlet.</span></span> <span data-ttu-id="b5a7d-137">您可以將內容傳遞至背景作業，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="b5a7d-137">You can pass a context to a background job as shown in the following example:</span></span>

  ```powershell-interactive
  PS C:\> $job = Start-Job { param ($ctx) New-AzureRmVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzureRmContext)
  ```

- <span data-ttu-id="b5a7d-138">使用預設內容，並啟用自動儲存</span><span class="sxs-lookup"><span data-stu-id="b5a7d-138">Using the default context with Autosave enabled</span></span>

  <span data-ttu-id="b5a7d-139">如果您已啟用**內容自動儲存**，背景作業就會自動使用預設儲存的內容。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-139">If you have enabled **Context Autosave**, background jobs automatically use the default saved context.</span></span>

  ```powershell-interactive
  PS C:\> $job = Start-Job { New-AzureRmVm [... Additional parameters ...]}
  ```

<span data-ttu-id="b5a7d-140">當您需要知道背景工作的結果時，請使用 `Get-Job` 來檢查作業狀態，並使用 `Wait-Job` 等候作業完成。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-140">When you need to know the outcome of the background task, use `Get-Job` to check the job status and `Wait-Job` to wait for the Job to complete.</span></span> <span data-ttu-id="b5a7d-141">使用 `Receive-Job` 可擷取或顯示背景作業的輸出。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-141">Use `Receive-Job` to capture or display the output of the background job.</span></span> <span data-ttu-id="b5a7d-142">如需詳細資訊，請參閱 [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs)。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-142">For more information, see [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>

## <a name="creating-selecting-renaming-and-removing-contexts"></a><span data-ttu-id="b5a7d-143">建立、選取、重新命名和移除內容</span><span class="sxs-lookup"><span data-stu-id="b5a7d-143">Creating, selecting, renaming, and removing contexts</span></span>

<span data-ttu-id="b5a7d-144">若要建立內容，您必須登入 Azure。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-144">To create a context, you must be signed in to Azure.</span></span> <span data-ttu-id="b5a7d-145">`Add-AzureRmAccount` Cmdlet (或其別名 `Login-AzureRmAccount`) 會設定後續 Azure PowerShell Cmdlet 所使用的預設內容，並可讓您存取認證所允許的任何租用戶或訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-145">The `Add-AzureRmAccount` cmdlet (or its alias, `Login-AzureRmAccount`) sets the default context used by subsequent Azure PowerShell cmdlets, and allows you to access any tenants or subscriptions allowed by your credentials.</span></span>

<span data-ttu-id="b5a7d-146">若要在登入之後新增內容，請使用 `Set-AzureRmContext` (或其別名 `Select-AzureRmSubscription`)。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-146">To add a new context after sign in, use `Set-AzureRmContext` (or its alias, `Select-AzureRmSubscription`).</span></span>

```azurepowershell-interactive
PS C:\> Set-AzureRMContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

<span data-ttu-id="b5a7d-147">上一個範例會使用目前的認證來新增目標為 'Contoso Subscription 1' 的新內容。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-147">The previous example adds a new context targeting 'Contoso Subscription 1' using your current credentials.</span></span> <span data-ttu-id="b5a7d-148">新的內容名為 'Contoso1'。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-148">The new context is named 'Contoso1'.</span></span> <span data-ttu-id="b5a7d-149">如果您未提供內容的名稱，就會使用使用帳戶識別碼和訂用帳戶識別碼的預設名稱。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-149">If you do not provide a name for the context, a default name, using the account ID and subscription ID is used.</span></span>

<span data-ttu-id="b5a7d-150">若要將現有的內容重新命名，請使用 `Rename-AzureRmContext` Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-150">To rename an existing context, use the `Rename-AzureRmContext` cmdlet.</span></span> <span data-ttu-id="b5a7d-151">例如︰</span><span class="sxs-lookup"><span data-stu-id="b5a7d-151">For example:</span></span>

```azurepowershell-interactive
PS C:\> Rename-AzureRmContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

<span data-ttu-id="b5a7d-152">這個範例會將包含自動名稱 `[user1@contoso.org; 123456-7890-1234-564321]` 的內容重新命名為簡單名稱 'Contoso2'。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-152">This example renames the context with automatic name `[user1@contoso.org; 123456-7890-1234-564321]` to the simple name 'Contoso2'.</span></span> <span data-ttu-id="b5a7d-153">管理內容的 Cmdlet 也會使用索引標籤完成，讓您能快速選取內容。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-153">Cmdlets that manage contexts also use tab completion, allowing you to quickly select the context.</span></span>

<span data-ttu-id="b5a7d-154">最後，若要移除內容，請使用 `Remove-AzureRmContext` Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-154">Finally, to remove a context, use the `Remove-AzureRmContext` cmdlet.</span></span>  <span data-ttu-id="b5a7d-155">例如︰</span><span class="sxs-lookup"><span data-stu-id="b5a7d-155">For example:</span></span>

```azurepowershell-interactive
PS C:\> Remove-AzureRmContext Contoso2
```

<span data-ttu-id="b5a7d-156">忘記名為 'Contoso2' 的內容。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-156">Forgets the context that was named 'Contoso2'.</span></span> <span data-ttu-id="b5a7d-157">您後續可以使用 `Set-AzureRmContext` 來重新建立此內容</span><span class="sxs-lookup"><span data-stu-id="b5a7d-157">You can recreate this context subsequently using `Set-AzureRmContext`</span></span>

## <a name="removing-credentials"></a><span data-ttu-id="b5a7d-158">移除認證</span><span class="sxs-lookup"><span data-stu-id="b5a7d-158">Removing credentials</span></span>

<span data-ttu-id="b5a7d-159">您可以使用 `Remove-AzureRmAccount` (也稱為 `Logout-AzureRmAccount`) 來移除使用者或服務主體的所有憑證和相關聯內容。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-159">You can remove all credentials and associated contexts for a user or service principal using `Remove-AzureRmAccount` (also known as `Logout-AzureRmAccount`).</span></span> <span data-ttu-id="b5a7d-160">在無參數的情況下執行時，`Remove-AzureRmAccount` Cmdlet 會移除目前內容中與使用者或服務主體相關聯的所有認證和內容。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-160">When executed without parameters, the `Remove-AzureRmAccount` cmdlet removes all credentials and contexts associated with the User or Service Principal in the current context.</span></span> <span data-ttu-id="b5a7d-161">您可以傳入使用者名稱、服務主體名稱或內容，將特定的主體作為目標。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-161">You may pass in a Username, Service Principal Name, or context to target a particular principal.</span></span>

```azurepowershell-interactive
Remove-AzureRmAccount user1@contoso.org
```

## <a name="using-context-scopes"></a><span data-ttu-id="b5a7d-162">使用內容範圍</span><span class="sxs-lookup"><span data-stu-id="b5a7d-162">Using context scopes</span></span>

<span data-ttu-id="b5a7d-163">有時候，您需要在不影響其他工作階段的情況下，選取、變更或移除 PowerShell 工作階段中的內容。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-163">Occasionally, you may want to select, change, or remove a context in a PowerShell session without impacting other sessions.</span></span> <span data-ttu-id="b5a7d-164">若要變更內容 Cmdlet 的預設行為，請使用 `Scope` 參數。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-164">To change the default behavior of context cmdlets, use the `Scope` parameter.</span></span> <span data-ttu-id="b5a7d-165">`Process` 範圍會覆寫預設行為，方法是僅使其套用於目前的工作階段。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-165">The `Process` scope overrides the default behavior by making it apply only for the current session.</span></span> <span data-ttu-id="b5a7d-166">相反地，`CurrentUser` 範圍會變更所有工作階段，而非只有目前工作階段中的內容。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-166">Conversely `CurrentUser` scope changes the context in all sessions, instead of just the current session.</span></span>

<span data-ttu-id="b5a7d-167">例如，若要在不影響其他視窗的情況下，變更目前 PowerShell 工作階段中的預設內容，或是下次開啟工作階段時使用的內容，請使用：</span><span class="sxs-lookup"><span data-stu-id="b5a7d-167">As an example, to change the default context in the current PowerShell session without impacting other windows, or the context used the next time a session is opened, use:</span></span>

```azurepowershell-interactive
PS C:\> Select-AzureRmContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a><span data-ttu-id="b5a7d-168">會記住內容自動儲存設定的方式</span><span class="sxs-lookup"><span data-stu-id="b5a7d-168">How the context autosave setting is remembered</span></span>

<span data-ttu-id="b5a7d-169">內容自動儲存設定會儲存到使用者 Azure PowerShell 目錄 (`%AppData%\Roaming\Windows Azure PowerShell`)。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-169">The context AutoSave setting is saved to the user Azure PowerShell directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span> <span data-ttu-id="b5a7d-170">部分類型的電腦帳戶可能無法存取此目錄。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-170">Some kinds of computer accounts may not have access to this directory.</span></span> <span data-ttu-id="b5a7d-171">如需這類的情節，您可以使用環境變數</span><span class="sxs-lookup"><span data-stu-id="b5a7d-171">For such scenarios, you can use the environment variable</span></span>

```azurepowershell-interactive
$env:AzureRmContextAutoSave="true" | "false"
```

<span data-ttu-id="b5a7d-172">如果設為 'true'，就會自動儲存內容。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-172">If set to 'true', the context is automatically saved.</span></span> <span data-ttu-id="b5a7d-173">如果設為 'false'，就不會自動儲存內容。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-173">If set to 'false', the context is not saved.</span></span>

## <a name="changes-to-the-azurermprofile-module"></a><span data-ttu-id="b5a7d-174">對 AzureRM.Profile 模組的變更</span><span class="sxs-lookup"><span data-stu-id="b5a7d-174">Changes to the AzureRM.Profile module</span></span>

<span data-ttu-id="b5a7d-175">新的 Cmdlet，可管理內容</span><span class="sxs-lookup"><span data-stu-id="b5a7d-175">New cmdlets for managing context</span></span>

- <span data-ttu-id="b5a7d-176">[Enable-AzureRmContextAutosave][enable] - 可在 Powershell 工作階段之間儲存內容。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-176">[Enable-AzureRmContextAutosave][enable] - Allow saving the context between powershell sessions.</span></span>
  <span data-ttu-id="b5a7d-177">任何變更都會改變全域內容。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-177">Any changes alter the global context.</span></span>
- <span data-ttu-id="b5a7d-178">[Disable-AzureRmContextAutosave][disable] - 關閉自動儲存內容。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-178">[Disable-AzureRmContextAutosave][disable] - Turn off autosaving the context.</span></span> <span data-ttu-id="b5a7d-179">需要每個新的 PowerShell 工作階段才能再次登入。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-179">Each new PowerShell session is required to sign in again.</span></span>
- <span data-ttu-id="b5a7d-180">[Select-AzureRmContext][select] - 選取內容作為預設值。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-180">[Select-AzureRmContext][select] - Select a context as the default.</span></span> <span data-ttu-id="b5a7d-181">所有後續的 Cmdlet 都會使用此內容中的認證來進行驗證。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-181">All subsequent cmdlets use the credentials in this context for authentication.</span></span>
- <span data-ttu-id="b5a7d-182">[Remove-AzureRmAccount][remove-cred] - 將與帳戶相關聯的所有認證和內容移除。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-182">[Remove-AzureRmAccount][remove-cred] - Remove all credentials and contexts associated with an account.</span></span>
- <span data-ttu-id="b5a7d-183">[Remove-AzureRmContext][remove-context] - 將已命名的內容移除。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-183">[Remove-AzureRmContext][remove-context] - Remove a named context.</span></span>
- <span data-ttu-id="b5a7d-184">[Rename-AzureRmContext][rename] - 將現有的內容重新命名。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-184">[Rename-AzureRmContext][rename] - Rename an existing context.</span></span>

<span data-ttu-id="b5a7d-185">對現有設定檔 Cmdlet 的變更</span><span class="sxs-lookup"><span data-stu-id="b5a7d-185">Changes to existing profile cmdlets</span></span>

- <span data-ttu-id="b5a7d-186">[Add-AzureRmAccount][login] - 允許登入程序或目前使用者的範圍。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-186">[Add-AzureRmAccount][login] - Allow scoping of the sign in to the process or the current user.</span></span>
  <span data-ttu-id="b5a7d-187">允許驗證之後命名預設內容。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-187">Allow naming the default context after authentication.</span></span>
- <span data-ttu-id="b5a7d-188">[Import-AzureRmContext][import] - 允許登入程序或目前使用者的範圍。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-188">[Import-AzureRmContext][import] - Allow scoping of the sign in to the process or the current user.</span></span>
- <span data-ttu-id="b5a7d-189">[Set-AzureRmContext][set-context] - 允許選取現有的已命名內容，以及對程序或目前使用者的範圍變更。</span><span class="sxs-lookup"><span data-stu-id="b5a7d-189">[Set-AzureRmContext][set-context] - Allow selection of existing named contexts, and scope changes to the process or current user.</span></span>

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
