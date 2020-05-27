---
title: 在 PowerShell 工作階段之間保存使用者認證
description: 了解如何重覆使用 Azure 認證及多個 PowerShell 工作階段之間的其他資訊。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 946920c22d7f6faeae8d3192e9f37a276a34d11f
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/14/2020
ms.locfileid: "83388018"
---
# <a name="persist-user-credentials-across-powershell-sessions"></a><span data-ttu-id="dcf69-103">在 PowerShell 工作階段之間保存使用者認證</span><span class="sxs-lookup"><span data-stu-id="dcf69-103">Persist user credentials across PowerShell sessions</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="dcf69-104">Azure PowerShell 提供了稱為 **Azure 內容自動儲存**的功能，可提供下列功能：</span><span class="sxs-lookup"><span data-stu-id="dcf69-104">Azure PowerShell offers a feature called **Azure Context Autosave**, which gives the following features:</span></span>

- <span data-ttu-id="dcf69-105">在新的 PowerShell 工作階段中重複使用的登入資訊保留。</span><span class="sxs-lookup"><span data-stu-id="dcf69-105">Retention of sign-in information for reuse in new PowerShell sessions.</span></span>
- <span data-ttu-id="dcf69-106">更易於使用的背景工作，可長時間執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dcf69-106">Easier use of background tasks for executing long-running cmdlets.</span></span>
- <span data-ttu-id="dcf69-107">在帳戶、訂用帳戶及環境之間進行切換，而無須個別登入。</span><span class="sxs-lookup"><span data-stu-id="dcf69-107">Switch between accounts, subscriptions, and environments without a separate sign-in.</span></span>
- <span data-ttu-id="dcf69-108">使用不同的認證和訂用帳戶，同時從相同的 PowerShell 工作階段執行工作。</span><span class="sxs-lookup"><span data-stu-id="dcf69-108">Execution of tasks using different credentials and subscriptions, simultaneously, from the same PowerShell session.</span></span>

## <a name="azure-contexts-defined"></a><span data-ttu-id="dcf69-109">定義的 Azure 內容</span><span class="sxs-lookup"><span data-stu-id="dcf69-109">Azure contexts defined</span></span>

<span data-ttu-id="dcf69-110">Azure 內容是一組資訊，可定義 Azure PowerShell Cmdlet 的目標。</span><span class="sxs-lookup"><span data-stu-id="dcf69-110">An *Azure context* is a set of information that defines the target of Azure PowerShell cmdlets.</span></span> <span data-ttu-id="dcf69-111">內容是由五個部分所組成：</span><span class="sxs-lookup"><span data-stu-id="dcf69-111">The context consists of five parts:</span></span>

- <span data-ttu-id="dcf69-112">帳戶 - 用來驗證與 Azure 通訊的使用者名稱或服務主體</span><span class="sxs-lookup"><span data-stu-id="dcf69-112">An *Account* - the UserName or Service Principal used to authenticate communications with Azure</span></span>
- <span data-ttu-id="dcf69-113">訂用帳戶 - 要進行處理的資源所屬的 Azure 訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="dcf69-113">A *Subscription* - The Azure Subscription with the Resources being acted upon.</span></span>
- <span data-ttu-id="dcf69-114">租用戶 - 包含您訂用帳戶的 Azure Active Directory 租用戶。</span><span class="sxs-lookup"><span data-stu-id="dcf69-114">A *Tenant* - The Azure Active Directory tenant that contains your subscription.</span></span> <span data-ttu-id="dcf69-115">租用戶對於 ServicePrincipal 驗證較為重要。</span><span class="sxs-lookup"><span data-stu-id="dcf69-115">Tenants are more important to ServicePrincipal authentication.</span></span>
- <span data-ttu-id="dcf69-116">環境 - 作為目標的特定 Azure 雲端，通常是 Azure 的全域雲端。</span><span class="sxs-lookup"><span data-stu-id="dcf69-116">An *Environment* - The particular Azure Cloud being targeted, usually the Azure global Cloud.</span></span>
  <span data-ttu-id="dcf69-117">不過，環境設定也可讓您將國家/地區、政府和內部部署 (Azure Stack) 雲端作為目標。</span><span class="sxs-lookup"><span data-stu-id="dcf69-117">However, the environment setting allows you to target National, Government, and on-premises (Azure Stack) clouds as well.</span></span>
- <span data-ttu-id="dcf69-118">認證 - Azure 用來確認您的身分識別，並確定您有權對 Azure 中的資源進行存取的資訊</span><span class="sxs-lookup"><span data-stu-id="dcf69-118">*Credentials* - The information used by Azure to verify your identity and confirm your authorization to access resources in Azure</span></span>

<span data-ttu-id="dcf69-119">在舊版中，您每次開啟新的 PowerShell 工作階段時都必須建立 Azure 內容。</span><span class="sxs-lookup"><span data-stu-id="dcf69-119">In previous releases, an Azure Context had to be created each time you opened a new PowerShell session.</span></span> <span data-ttu-id="dcf69-120">從 Azure PowerShell v4.4.0 開始，已可在每次開啟新的 PowerShell 工作階段時自動儲存 Azure 內容。</span><span class="sxs-lookup"><span data-stu-id="dcf69-120">Beginning with Azure PowerShell v4.4.0, Azure Contexts can automatically be saved whenever opening a new PowerShell session.</span></span>

## <a name="automatically-save-the-context-for-the-next-sign-in"></a><span data-ttu-id="dcf69-121">自動儲存內容以供下一次登入使用</span><span class="sxs-lookup"><span data-stu-id="dcf69-121">Automatically save the context for the next sign-in</span></span>

<span data-ttu-id="dcf69-122">在 6.3.0 版和更新版本中，Azure PowerShell 會自動保留工作階段之間的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="dcf69-122">In versions 6.3.0 and later, Azure PowerShell retains your context information automatically between sessions.</span></span> <span data-ttu-id="dcf69-123">若要將 PowerShell 設定為忘記您的內容和認證，請使用 `Disable-AzureRmContextAutoSave`。</span><span class="sxs-lookup"><span data-stu-id="dcf69-123">To set PowerShell to forget your context and credentials, use `Disable-AzureRmContextAutoSave`.</span></span> <span data-ttu-id="dcf69-124">您每次開啟 PowerShell 工作階段時，都必須登入 Azure。</span><span class="sxs-lookup"><span data-stu-id="dcf69-124">You'll need to sign in to Azure every time you open a PowerShell session.</span></span>

<span data-ttu-id="dcf69-125">若要讓 Azure PowerShell 在 PowerShell 工作階段關閉之後記住您的內容，請使用 `Enable-AzureRmContextAutosave`。</span><span class="sxs-lookup"><span data-stu-id="dcf69-125">To allow Azure PowerShell to remember your context after the PowerShell session is closed, use `Enable-AzureRmContextAutosave`.</span></span> <span data-ttu-id="dcf69-126">內容與認證資訊會自動儲存在您使用者目錄中的特殊隱藏資料夾中 (`%AppData%\Roaming\Windows Azure PowerShell`)。</span><span class="sxs-lookup"><span data-stu-id="dcf69-126">Context and credential information are automatically saved in a special hidden folder in your user directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span>
<span data-ttu-id="dcf69-127">每個新的 PowerShell 工作階段都會將您最後一個工作階段中使用的內容作為目標。</span><span class="sxs-lookup"><span data-stu-id="dcf69-127">Each new PowerShell session targets the context used in your last session.</span></span>

<span data-ttu-id="dcf69-128">可讓您管理 Azure 內容的 Cmdlet 也能讓您進行更細緻的控制。</span><span class="sxs-lookup"><span data-stu-id="dcf69-128">The cmdlets that allow you to manage Azure contexts also allow you fine grained control.</span></span> <span data-ttu-id="dcf69-129">您是否僅需要將變更套用到目前的 PowerShell 工作階段 (`Process` 範圍) 還是要套用到每個 PowerShell 工作階段 (`CurrentUser` 範圍)。</span><span class="sxs-lookup"><span data-stu-id="dcf69-129">If you want changes to apply only to the current PowerShell session (`Process` scope) or every PowerShell session (`CurrentUser` scope).</span></span> <span data-ttu-id="dcf69-130">這些選項將在[使用內容範圍](#using-context-scopes)中深入討論。</span><span class="sxs-lookup"><span data-stu-id="dcf69-130">These options are discussed in mode detail in [Using Context Scopes](#using-context-scopes).</span></span>

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a><span data-ttu-id="dcf69-131">將 Azure PowerShell Cmdlet 作為背景作業執行</span><span class="sxs-lookup"><span data-stu-id="dcf69-131">Running Azure PowerShell cmdlets as background jobs</span></span>

<span data-ttu-id="dcf69-132">**Azure 內容自動儲存**功能也可讓您與 PowerShell 背景作業共用內容。</span><span class="sxs-lookup"><span data-stu-id="dcf69-132">The **Azure Context Autosave** feature also allows you to share you context with PowerShell background jobs.</span></span> <span data-ttu-id="dcf69-133">PowerShell 可讓您以背景作業形式啟動並監視長時間執行的工作，而不必等候工作完成。</span><span class="sxs-lookup"><span data-stu-id="dcf69-133">PowerShell allows you to start and monitor long-executing tasks as background jobs without having to wait for the tasks to complete.</span></span> <span data-ttu-id="dcf69-134">您可以利用兩種不同的方式來與背景作業共用認證：</span><span class="sxs-lookup"><span data-stu-id="dcf69-134">You can share credentials with background jobs in two different ways:</span></span>

- <span data-ttu-id="dcf69-135">傳遞內容作為引數</span><span class="sxs-lookup"><span data-stu-id="dcf69-135">Passing the context as an argument</span></span>

  <span data-ttu-id="dcf69-136">大部分的 AzureRM Cmdlet 可讓您將內容作為參數傳遞至 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dcf69-136">Most AzureRM cmdlets allow you to pass the context as a parameter to the cmdlet.</span></span> <span data-ttu-id="dcf69-137">您可以將內容傳遞至背景作業，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="dcf69-137">You can pass a context to a background job as shown in the following example:</span></span>

  ```powershell-interactive
  PS C:\> $job = Start-Job { param ($ctx) New-AzureRmVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzureRmContext)
  ```

- <span data-ttu-id="dcf69-138">使用預設內容，並啟用自動儲存</span><span class="sxs-lookup"><span data-stu-id="dcf69-138">Using the default context with Autosave enabled</span></span>

  <span data-ttu-id="dcf69-139">如果您已啟用**內容自動儲存**，背景作業就會自動使用預設儲存的內容。</span><span class="sxs-lookup"><span data-stu-id="dcf69-139">If you have enabled **Context Autosave**, background jobs automatically use the default saved context.</span></span>

  ```powershell-interactive
  PS C:\> $job = Start-Job { New-AzureRmVm [... Additional parameters ...]}
  ```

<span data-ttu-id="dcf69-140">當您需要知道背景工作的結果時，請使用 `Get-Job` 來檢查作業狀態，並使用 `Wait-Job` 等候作業完成。</span><span class="sxs-lookup"><span data-stu-id="dcf69-140">When you need to know the outcome of the background task, use `Get-Job` to check the job status and `Wait-Job` to wait for the Job to complete.</span></span> <span data-ttu-id="dcf69-141">使用 `Receive-Job` 可擷取或顯示背景作業的輸出。</span><span class="sxs-lookup"><span data-stu-id="dcf69-141">Use `Receive-Job` to capture or display the output of the background job.</span></span> <span data-ttu-id="dcf69-142">如需詳細資訊，請參閱 [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs)。</span><span class="sxs-lookup"><span data-stu-id="dcf69-142">For more information, see [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>

## <a name="creating-selecting-renaming-and-removing-contexts"></a><span data-ttu-id="dcf69-143">建立、選取、重新命名和移除內容</span><span class="sxs-lookup"><span data-stu-id="dcf69-143">Creating, selecting, renaming, and removing contexts</span></span>

<span data-ttu-id="dcf69-144">若要建立內容，您必須登入 Azure。</span><span class="sxs-lookup"><span data-stu-id="dcf69-144">To create a context, you must be signed in to Azure.</span></span> <span data-ttu-id="dcf69-145">`Connect-AzureRmAccount` Cmdlet (或其別名 `Login-AzureRmAccount`) 會設定 Azure PowerShell Cmdlet 所使用的預設內容，並可讓您存取認證所允許的任何租用戶或訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="dcf69-145">The `Connect-AzureRmAccount` cmdlet (or its alias, `Login-AzureRmAccount`) sets the default context used by Azure PowerShell cmdlets, and allows you to access any tenants or subscriptions allowed by your credentials.</span></span>

<span data-ttu-id="dcf69-146">若要在登入之後新增內容，請使用 `Set-AzureRmContext` (或其別名 `Select-AzureRmSubscription`)。</span><span class="sxs-lookup"><span data-stu-id="dcf69-146">To add a new context after sign-in, use `Set-AzureRmContext` (or its alias, `Select-AzureRmSubscription`).</span></span>

```azurepowershell-interactive
PS C:\> Set-AzureRMContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

<span data-ttu-id="dcf69-147">上一個範例會使用目前的認證來新增目標為 'Contoso Subscription 1' 的新內容。</span><span class="sxs-lookup"><span data-stu-id="dcf69-147">The previous example adds a new context targeting 'Contoso Subscription 1' using your current credentials.</span></span> <span data-ttu-id="dcf69-148">新的內容名為 'Contoso1'。</span><span class="sxs-lookup"><span data-stu-id="dcf69-148">The new context is named 'Contoso1'.</span></span> <span data-ttu-id="dcf69-149">如果您未提供內容的名稱，就會使用使用帳戶識別碼和訂用帳戶識別碼的預設名稱。</span><span class="sxs-lookup"><span data-stu-id="dcf69-149">If you don't provide a name for the context, a default name, using the account ID and subscription ID is used.</span></span>

<span data-ttu-id="dcf69-150">若要將現有的內容重新命名，請使用 `Rename-AzureRmContext` Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dcf69-150">To rename an existing context, use the `Rename-AzureRmContext` cmdlet.</span></span> <span data-ttu-id="dcf69-151">例如：</span><span class="sxs-lookup"><span data-stu-id="dcf69-151">For example:</span></span>

```azurepowershell-interactive
PS C:\> Rename-AzureRmContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

<span data-ttu-id="dcf69-152">這個範例會將包含自動名稱 `[user1@contoso.org; 123456-7890-1234-564321]` 的內容重新命名為簡單名稱 'Contoso2'。</span><span class="sxs-lookup"><span data-stu-id="dcf69-152">This example renames the context with automatic name `[user1@contoso.org; 123456-7890-1234-564321]` to the simple name 'Contoso2'.</span></span> <span data-ttu-id="dcf69-153">管理內容的 Cmdlet 也會使用索引標籤完成，讓您能快速選取內容。</span><span class="sxs-lookup"><span data-stu-id="dcf69-153">Cmdlets that manage contexts also use tab completion, allowing you to quickly select the context.</span></span>

<span data-ttu-id="dcf69-154">最後，若要移除內容，請使用 `Remove-AzureRmContext` Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dcf69-154">Finally, to remove a context, use the `Remove-AzureRmContext` cmdlet.</span></span>  <span data-ttu-id="dcf69-155">例如：</span><span class="sxs-lookup"><span data-stu-id="dcf69-155">For example:</span></span>

```azurepowershell-interactive
PS C:\> Remove-AzureRmContext Contoso2
```

<span data-ttu-id="dcf69-156">忘記名為 'Contoso2' 的內容。</span><span class="sxs-lookup"><span data-stu-id="dcf69-156">Forgets the context that was named 'Contoso2'.</span></span> <span data-ttu-id="dcf69-157">您可以使用 `Set-AzureRmContext` 來重新建立此內容</span><span class="sxs-lookup"><span data-stu-id="dcf69-157">You can recreate this context using `Set-AzureRmContext`</span></span>

## <a name="removing-credentials"></a><span data-ttu-id="dcf69-158">移除認證</span><span class="sxs-lookup"><span data-stu-id="dcf69-158">Removing credentials</span></span>

<span data-ttu-id="dcf69-159">您可以使用 `Disconnect-AzureRmAccount` (也稱為 `Logout-AzureRmAccount`) 來移除使用者或服務主體的所有憑證和相關聯內容。</span><span class="sxs-lookup"><span data-stu-id="dcf69-159">You can remove all credentials and associated contexts for a user or service principal using `Disconnect-AzureRmAccount` (also known as `Logout-AzureRmAccount`).</span></span> <span data-ttu-id="dcf69-160">在無參數的情況下執行時，`Disconnect-AzureRmAccount` Cmdlet 會移除目前內容中與使用者或服務主體相關聯的所有認證和內容。</span><span class="sxs-lookup"><span data-stu-id="dcf69-160">When executed without parameters, the `Disconnect-AzureRmAccount` cmdlet removes all credentials and contexts associated with the User or Service Principal in the current context.</span></span> <span data-ttu-id="dcf69-161">您可以傳入使用者名稱、服務主體名稱或內容，將特定的主體作為目標。</span><span class="sxs-lookup"><span data-stu-id="dcf69-161">You may pass in a Username, Service Principal Name, or context to target a particular principal.</span></span>

```azurepowershell-interactive
Disconnect-AzureRmAccount user1@contoso.org
```

## <a name="using-context-scopes"></a><span data-ttu-id="dcf69-162">使用內容範圍</span><span class="sxs-lookup"><span data-stu-id="dcf69-162">Using context scopes</span></span>

<span data-ttu-id="dcf69-163">有時候，您需要在不影響其他工作階段的情況下，選取、變更或移除 PowerShell 工作階段中的內容。</span><span class="sxs-lookup"><span data-stu-id="dcf69-163">Occasionally, you may want to select, change, or remove a context in a PowerShell session without impacting other sessions.</span></span> <span data-ttu-id="dcf69-164">若要變更內容 Cmdlet 的預設行為，請使用 `Scope` 參數。</span><span class="sxs-lookup"><span data-stu-id="dcf69-164">To change the default behavior of context cmdlets, use the `Scope` parameter.</span></span> <span data-ttu-id="dcf69-165">`Process` 範圍會覆寫預設行為，方法是僅使其套用於目前的工作階段。</span><span class="sxs-lookup"><span data-stu-id="dcf69-165">The `Process` scope overrides the default behavior by making it apply only for the current session.</span></span> <span data-ttu-id="dcf69-166">相反地，`CurrentUser` 範圍會變更所有工作階段，而非只有目前工作階段中的內容。</span><span class="sxs-lookup"><span data-stu-id="dcf69-166">Conversely `CurrentUser` scope changes the context in all sessions, instead of just the current session.</span></span>

<span data-ttu-id="dcf69-167">例如，若要在不影響其他視窗的情況下，變更目前 PowerShell 工作階段中的預設內容，或是下次開啟工作階段時使用的內容，請使用：</span><span class="sxs-lookup"><span data-stu-id="dcf69-167">As an example, to change the default context in the current PowerShell session without impacting other windows, or the context used the next time a session is opened, use:</span></span>

```azurepowershell-interactive
PS C:\> Select-AzureRmContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a><span data-ttu-id="dcf69-168">會記住內容自動儲存設定的方式</span><span class="sxs-lookup"><span data-stu-id="dcf69-168">How the context autosave setting is remembered</span></span>

<span data-ttu-id="dcf69-169">內容自動儲存設定會儲存到使用者 Azure PowerShell 目錄 (`%AppData%\Roaming\Windows Azure PowerShell`)。</span><span class="sxs-lookup"><span data-stu-id="dcf69-169">The context AutoSave setting is saved to the user Azure PowerShell directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span> <span data-ttu-id="dcf69-170">部分類型的電腦帳戶可能無法存取此目錄。</span><span class="sxs-lookup"><span data-stu-id="dcf69-170">Some kinds of computer accounts may not have access to this directory.</span></span> <span data-ttu-id="dcf69-171">如需這類的情節，您可以使用環境變數</span><span class="sxs-lookup"><span data-stu-id="dcf69-171">For such scenarios, you can use the environment variable</span></span>

```azurepowershell-interactive
$env:AzureRmContextAutoSave="true" | "false"
```

<span data-ttu-id="dcf69-172">設為 'true' 時，就會自動儲存內容。</span><span class="sxs-lookup"><span data-stu-id="dcf69-172">When set to 'true', the context is automatically saved.</span></span> <span data-ttu-id="dcf69-173">如果設為 'false'，就不會自動儲存內容。</span><span class="sxs-lookup"><span data-stu-id="dcf69-173">If set to 'false', the context isn't saved.</span></span>

## <a name="changes-to-the-azurermprofile-module"></a><span data-ttu-id="dcf69-174">對 AzureRM.Profile 模組的變更</span><span class="sxs-lookup"><span data-stu-id="dcf69-174">Changes to the AzureRM.Profile module</span></span>

<span data-ttu-id="dcf69-175">新的 Cmdlet，可管理內容</span><span class="sxs-lookup"><span data-stu-id="dcf69-175">New cmdlets for managing context</span></span>

- <span data-ttu-id="dcf69-176">[Enable-AzureRmContextAutosave][enable] - 可在 Powershell 工作階段之間儲存內容。</span><span class="sxs-lookup"><span data-stu-id="dcf69-176">[Enable-AzureRmContextAutosave][enable] - Allow saving the context between powershell sessions.</span></span>
  <span data-ttu-id="dcf69-177">任何變更都會改變全域內容。</span><span class="sxs-lookup"><span data-stu-id="dcf69-177">Any changes alter the global context.</span></span>
- <span data-ttu-id="dcf69-178">[Disable-AzureRmContextAutosave][disable] - 關閉自動儲存內容。</span><span class="sxs-lookup"><span data-stu-id="dcf69-178">[Disable-AzureRmContextAutosave][disable] - Turn off autosaving the context.</span></span> <span data-ttu-id="dcf69-179">需要每個新的 PowerShell 工作階段才能再次登入。</span><span class="sxs-lookup"><span data-stu-id="dcf69-179">Each new PowerShell session is required to sign in again.</span></span>
- <span data-ttu-id="dcf69-180">[Select-AzureRmContext][select] - 選取內容作為預設值。</span><span class="sxs-lookup"><span data-stu-id="dcf69-180">[Select-AzureRmContext][select] - Select a context as the default.</span></span> <span data-ttu-id="dcf69-181">所有 Cmdlet 都會使用此內容中的認證來進行驗證。</span><span class="sxs-lookup"><span data-stu-id="dcf69-181">All cmdlets use the credentials in this context for authentication.</span></span>
- <span data-ttu-id="dcf69-182">[Disconnect-AzureRmAccount][remove-cred] - 移除與帳戶相關聯的所有認證和內容。</span><span class="sxs-lookup"><span data-stu-id="dcf69-182">[Disconnect-AzureRmAccount][remove-cred] - Remove all credentials and contexts associated with an account.</span></span>
- <span data-ttu-id="dcf69-183">[Remove-AzureRmContext][remove-context] - 將已命名的內容移除。</span><span class="sxs-lookup"><span data-stu-id="dcf69-183">[Remove-AzureRmContext][remove-context] - Remove a named context.</span></span>
- <span data-ttu-id="dcf69-184">[Rename-AzureRmContext][rename] - 將現有的內容重新命名。</span><span class="sxs-lookup"><span data-stu-id="dcf69-184">[Rename-AzureRmContext][rename] - Rename an existing context.</span></span>

<span data-ttu-id="dcf69-185">對現有設定檔 Cmdlet 的變更</span><span class="sxs-lookup"><span data-stu-id="dcf69-185">Changes to existing profile cmdlets</span></span>

- <span data-ttu-id="dcf69-186">[Add-AzureRmAccount][login] - 允許登入程序或目前使用者的範圍。</span><span class="sxs-lookup"><span data-stu-id="dcf69-186">[Add-AzureRmAccount][login] - Allow scoping of the sign-in to the process or the current user.</span></span>
  <span data-ttu-id="dcf69-187">允許驗證之後命名預設內容。</span><span class="sxs-lookup"><span data-stu-id="dcf69-187">Allow naming the default context after authentication.</span></span>
- <span data-ttu-id="dcf69-188">[Import-AzureRmContext][import] - 允許登入程序或目前使用者的範圍。</span><span class="sxs-lookup"><span data-stu-id="dcf69-188">[Import-AzureRmContext][import] - Allow scoping of the sign-in to the process or the current user.</span></span>
- <span data-ttu-id="dcf69-189">[Set-AzureRmContext][set-context] - 允許選取現有的已命名內容，以及對程序或目前使用者的範圍變更。</span><span class="sxs-lookup"><span data-stu-id="dcf69-189">[Set-AzureRmContext][set-context] - Allow selection of existing named contexts, and scope changes to the process or current user.</span></span>

<!-- Hyperlinks -->
[enable]: /powershell/module/azurerm.profile/Enable-AzureRmContextAutosave
[disable]: /powershell/module/azurerm.profile/Disable-AzureRmContextAutosave
[select]: /powershell/module/azurerm.profile/Select-AzureRmContext
[remove-cred]: /powershell/module/azurerm.profile/Disconnect-AzureRmAccount
[remove-context]: /powershell/module/azurerm.profile/Remove-AzureRmContext
[rename]: /powershell/module/azurerm.profile/Rename-AzureRmContext

<!-- Updated cmdlets -->
[login]: /powershell/module/azurerm.profile/Connect-AzureRmAccount
[import]:  /powershell/module/azurerm.profile/Import-AzureRmContext
[set-context]: /powershell/module/azurerm.profile/Set-AzureRmContext
