---
title: 在 PowerShell 工作階段之間保存 Azure 認證
description: 了解如何重覆使用 Azure 認證及多個 PowerShell 工作階段之間的其他資訊。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 02b8090aa1868f24445ddff3a95c0d0c376e2cb8
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/15/2019
ms.locfileid: "72370403"
---
# <a name="persist-azure-user-credentials-across-powershell-sessions"></a><span data-ttu-id="15f50-103">在 PowerShell 工作階段之間保存 Azure 使用者認證</span><span class="sxs-lookup"><span data-stu-id="15f50-103">Persist Azure user credentials across PowerShell sessions</span></span>

<span data-ttu-id="15f50-104">Azure PowerShell 提供了稱為 **Azure 內容自動儲存**的功能，可提供下列功能：</span><span class="sxs-lookup"><span data-stu-id="15f50-104">Azure PowerShell offers a feature called **Azure Context Autosave**, which gives the following features:</span></span>

- <span data-ttu-id="15f50-105">在新的 PowerShell 工作階段中重複使用的登入資訊保留。</span><span class="sxs-lookup"><span data-stu-id="15f50-105">Retention of sign-in information for reuse in new PowerShell sessions.</span></span>
- <span data-ttu-id="15f50-106">更易於使用的背景工作，可長時間執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="15f50-106">Easier use of background tasks for executing long-running cmdlets.</span></span>
- <span data-ttu-id="15f50-107">在帳戶、訂用帳戶及環境之間進行切換，而無須個別登入。</span><span class="sxs-lookup"><span data-stu-id="15f50-107">Switch between accounts, subscriptions, and environments without a separate sign-in.</span></span>
- <span data-ttu-id="15f50-108">使用不同的認證和訂用帳戶，同時從相同的 PowerShell 工作階段執行工作。</span><span class="sxs-lookup"><span data-stu-id="15f50-108">Execution of tasks using different credentials and subscriptions, simultaneously, from the same PowerShell session.</span></span>

## <a name="azure-contexts-defined"></a><span data-ttu-id="15f50-109">定義的 Azure 內容</span><span class="sxs-lookup"><span data-stu-id="15f50-109">Azure contexts defined</span></span>

<span data-ttu-id="15f50-110">Azure 內容  是一組資訊，可定義 Azure PowerShell Cmdlet 的目標。</span><span class="sxs-lookup"><span data-stu-id="15f50-110">An *Azure context* is a set of information that defines the target of Azure PowerShell cmdlets.</span></span> <span data-ttu-id="15f50-111">內容是由五個部分所組成：</span><span class="sxs-lookup"><span data-stu-id="15f50-111">The context consists of five parts:</span></span>

- <span data-ttu-id="15f50-112">帳戶  - 用來驗證與 Azure 通訊的使用者名稱或服務主體</span><span class="sxs-lookup"><span data-stu-id="15f50-112">An *Account* - the UserName or Service Principal used to authenticate communications with Azure</span></span>
- <span data-ttu-id="15f50-113">訂用帳戶  - 要進行處理的資源所屬的 Azure 訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="15f50-113">A *Subscription* - The Azure Subscription with the Resources being acted upon.</span></span>
- <span data-ttu-id="15f50-114">租用戶  - 包含您訂用帳戶的 Azure Active Directory 租用戶。</span><span class="sxs-lookup"><span data-stu-id="15f50-114">A *Tenant* - The Azure Active Directory tenant that contains your subscription.</span></span> <span data-ttu-id="15f50-115">租用戶對於 ServicePrincipal 驗證較為重要。</span><span class="sxs-lookup"><span data-stu-id="15f50-115">Tenants are more important to ServicePrincipal authentication.</span></span>
- <span data-ttu-id="15f50-116">環境  - 作為目標的特定 Azure 雲端，通常是 Azure 的全域雲端。</span><span class="sxs-lookup"><span data-stu-id="15f50-116">An *Environment* - The particular Azure Cloud being targeted, usually the Azure global Cloud.</span></span>
  <span data-ttu-id="15f50-117">不過，環境設定也可讓您將國家/地區、政府和內部部署 (Azure Stack) 雲端作為目標。</span><span class="sxs-lookup"><span data-stu-id="15f50-117">However, the environment setting allows you to target National, Government, and on-premises (Azure Stack) clouds as well.</span></span>
- <span data-ttu-id="15f50-118">認證  - Azure 用來確認您的身分識別，並確定您有權對 Azure 中的資源進行存取的資訊</span><span class="sxs-lookup"><span data-stu-id="15f50-118">*Credentials* - The information used by Azure to verify your identity and confirm your authorization to access resources in Azure</span></span>

<span data-ttu-id="15f50-119">若使用最新版的 Azure PowerShell，便可在每次開啟新的 PowerShell 工作階段時自動儲存 Azure 內容。</span><span class="sxs-lookup"><span data-stu-id="15f50-119">With the latest version of Azure PowerShell, Azure Contexts can automatically be saved whenever opening a new PowerShell session.</span></span>

## <a name="automatically-save-the-context-for-the-next-sign-in"></a><span data-ttu-id="15f50-120">自動儲存內容以供下一次登入使用</span><span class="sxs-lookup"><span data-stu-id="15f50-120">Automatically save the context for the next sign-in</span></span>

<span data-ttu-id="15f50-121">Azure PowerShell 會自動保留工作階段之間的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="15f50-121">Azure PowerShell retains your context information automatically between sessions.</span></span> <span data-ttu-id="15f50-122">若要將 PowerShell 設定為忘記您的內容和認證，請使用 `Disable-AzContextAutoSave`。</span><span class="sxs-lookup"><span data-stu-id="15f50-122">To set PowerShell to forget your context and credentials, use `Disable-AzContextAutoSave`.</span></span> <span data-ttu-id="15f50-123">若停用內容儲存功能，您每次開啟 PowerShell 工作階段時，都必須登入 Azure。</span><span class="sxs-lookup"><span data-stu-id="15f50-123">With context saving disabled, you'll need to sign in to Azure every time you open a PowerShell session.</span></span>

<span data-ttu-id="15f50-124">若要讓 Azure PowerShell 在 PowerShell 工作階段關閉之後記住您的內容，請使用 `Enable-AzContextAutosave`。</span><span class="sxs-lookup"><span data-stu-id="15f50-124">To allow Azure PowerShell to remember your context after the PowerShell session is closed, use `Enable-AzContextAutosave`.</span></span> <span data-ttu-id="15f50-125">內容與認證資訊會自動儲存在您使用者目錄中的特殊隱藏資料夾中 (在 Windows 上為 `$env:USERPROFILE\.Azure`，在其他平台上則為 `$HOME/.Azure`)。</span><span class="sxs-lookup"><span data-stu-id="15f50-125">Context and credential information are automatically saved in a special hidden folder in your user directory (`$env:USERPROFILE\.Azure` on Windows, and `$HOME/.Azure` on other platforms).</span></span> <span data-ttu-id="15f50-126">每個新的 PowerShell 工作階段都會將您最後一個工作階段中使用的內容作為目標。</span><span class="sxs-lookup"><span data-stu-id="15f50-126">Each new PowerShell session targets the context used in your last session.</span></span>

<span data-ttu-id="15f50-127">可讓您管理 Azure 內容的 Cmdlet 也能讓您進行更細緻的控制。</span><span class="sxs-lookup"><span data-stu-id="15f50-127">The cmdlets that allow you to manage Azure contexts also allow you fine grained control.</span></span> <span data-ttu-id="15f50-128">您是否僅需要將變更套用到目前的 PowerShell 工作階段 (`Process` 範圍) 還是要套用到每個 PowerShell 工作階段 (`CurrentUser` 範圍)。</span><span class="sxs-lookup"><span data-stu-id="15f50-128">If you want changes to apply only to the current PowerShell session (`Process` scope) or every PowerShell session (`CurrentUser` scope).</span></span> <span data-ttu-id="15f50-129">這些選項將在[使用內容範圍](#using-context-scopes)中深入討論。</span><span class="sxs-lookup"><span data-stu-id="15f50-129">These options are discussed in more detail in [Using Context Scopes](#using-context-scopes).</span></span>

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a><span data-ttu-id="15f50-130">將 Azure PowerShell Cmdlet 作為背景作業執行</span><span class="sxs-lookup"><span data-stu-id="15f50-130">Running Azure PowerShell cmdlets as background jobs</span></span>

<span data-ttu-id="15f50-131">**Azure 內容自動儲存**功能也可讓您與 PowerShell 背景作業共用內容。</span><span class="sxs-lookup"><span data-stu-id="15f50-131">The **Azure Context Autosave** feature also allows you to share you context with PowerShell background jobs.</span></span> <span data-ttu-id="15f50-132">PowerShell 可讓您以背景作業形式啟動並監視長時間執行的工作，而不必等候工作完成。</span><span class="sxs-lookup"><span data-stu-id="15f50-132">PowerShell allows you to start and monitor long-executing tasks as background jobs without having to wait for the tasks to complete.</span></span> <span data-ttu-id="15f50-133">您可以利用兩種不同的方式來與背景作業共用認證：</span><span class="sxs-lookup"><span data-stu-id="15f50-133">You can share credentials with background jobs in two different ways:</span></span>

- <span data-ttu-id="15f50-134">傳遞內容作為引數</span><span class="sxs-lookup"><span data-stu-id="15f50-134">Passing the context as an argument</span></span>

  <span data-ttu-id="15f50-135">大部分的 AzureRM Cmdlet 可讓您將內容作為參數傳遞至 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="15f50-135">Most AzureRM cmdlets allow you to pass the context as a parameter to the cmdlet.</span></span> <span data-ttu-id="15f50-136">您可以將內容傳遞至背景作業，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="15f50-136">You can pass a context to a background job as shown in the following example:</span></span>

  ```powershell-interactive
  PS C:\> $job = Start-Job { param ($ctx) New-AzVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzContext)
  ```

- <span data-ttu-id="15f50-137">使用預設內容，並啟用自動儲存</span><span class="sxs-lookup"><span data-stu-id="15f50-137">Using the default context with Autosave enabled</span></span>

  <span data-ttu-id="15f50-138">如果您已啟用**內容自動儲存**，背景作業就會自動使用預設儲存的內容。</span><span class="sxs-lookup"><span data-stu-id="15f50-138">If you have enabled **Context Autosave**, background jobs automatically use the default saved context.</span></span>

  ```powershell-interactive
  PS C:\> $job = Start-Job { New-AzVm [... Additional parameters ...]}
  ```

<span data-ttu-id="15f50-139">當您需要知道背景工作的結果時，請使用 `Get-Job` 來檢查作業狀態，並使用 `Wait-Job` 等候作業完成。</span><span class="sxs-lookup"><span data-stu-id="15f50-139">When you need to know the outcome of the background task, use `Get-Job` to check the job status and `Wait-Job` to wait for the Job to complete.</span></span> <span data-ttu-id="15f50-140">使用 `Receive-Job` 可擷取或顯示背景作業的輸出。</span><span class="sxs-lookup"><span data-stu-id="15f50-140">Use `Receive-Job` to capture or display the output of the background job.</span></span> <span data-ttu-id="15f50-141">如需詳細資訊，請參閱 [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs)。</span><span class="sxs-lookup"><span data-stu-id="15f50-141">For more information, see [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>

## <a name="creating-selecting-renaming-and-removing-contexts"></a><span data-ttu-id="15f50-142">建立、選取、重新命名和移除內容</span><span class="sxs-lookup"><span data-stu-id="15f50-142">Creating, selecting, renaming, and removing contexts</span></span>

<span data-ttu-id="15f50-143">若要建立內容，您必須登入 Azure。</span><span class="sxs-lookup"><span data-stu-id="15f50-143">To create a context, you must be signed in to Azure.</span></span> <span data-ttu-id="15f50-144">`Connect-AzAccount` Cmdlet (或其別名 `Login-AzAccount`) 會設定 Azure PowerShell Cmdlet 所使用的預設內容，並可讓您存取認證所允許的任何租用戶或訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="15f50-144">The `Connect-AzAccount` cmdlet (or its alias, `Login-AzAccount`) sets the default context used by Azure PowerShell cmdlets, and allows you to access any tenants or subscriptions allowed by your credentials.</span></span>

<span data-ttu-id="15f50-145">若要在登入之後新增內容，請使用 `Set-AzContext` (或其別名 `Select-AzSubscription`)。</span><span class="sxs-lookup"><span data-stu-id="15f50-145">To add a new context after sign-in, use `Set-AzContext` (or its alias, `Select-AzSubscription`).</span></span>

```azurepowershell-interactive
PS C:\> Set-AzContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

<span data-ttu-id="15f50-146">上一個範例會使用目前的認證來新增目標為 'Contoso Subscription 1' 的新內容。</span><span class="sxs-lookup"><span data-stu-id="15f50-146">The previous example adds a new context targeting 'Contoso Subscription 1' using your current credentials.</span></span> <span data-ttu-id="15f50-147">新的內容名為 'Contoso1'。</span><span class="sxs-lookup"><span data-stu-id="15f50-147">The new context is named 'Contoso1'.</span></span> <span data-ttu-id="15f50-148">如果您未提供內容的名稱，就會使用使用帳戶識別碼和訂用帳戶識別碼的預設名稱。</span><span class="sxs-lookup"><span data-stu-id="15f50-148">If you don't provide a name for the context, a default name, using the account ID and subscription ID is used.</span></span>

<span data-ttu-id="15f50-149">若要將現有的內容重新命名，請使用 `Rename-AzContext` Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="15f50-149">To rename an existing context, use the `Rename-AzContext` cmdlet.</span></span> <span data-ttu-id="15f50-150">例如︰</span><span class="sxs-lookup"><span data-stu-id="15f50-150">For example:</span></span>

```azurepowershell-interactive
PS C:\> Rename-AzContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

<span data-ttu-id="15f50-151">這個範例會將包含自動名稱 `[user1@contoso.org; 123456-7890-1234-564321]` 的內容重新命名為簡單名稱 'Contoso2'。</span><span class="sxs-lookup"><span data-stu-id="15f50-151">This example renames the context with automatic name `[user1@contoso.org; 123456-7890-1234-564321]` to the simple name 'Contoso2'.</span></span> <span data-ttu-id="15f50-152">管理內容的 Cmdlet 也會使用索引標籤完成，讓您能快速選取內容。</span><span class="sxs-lookup"><span data-stu-id="15f50-152">Cmdlets that manage contexts also use tab completion, allowing you to quickly select the context.</span></span>

<span data-ttu-id="15f50-153">最後，若要移除內容，請使用 `Remove-AzContext` Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="15f50-153">Finally, to remove a context, use the `Remove-AzContext` cmdlet.</span></span>  <span data-ttu-id="15f50-154">例如︰</span><span class="sxs-lookup"><span data-stu-id="15f50-154">For example:</span></span>

```azurepowershell-interactive
PS C:\> Remove-AzContext Contoso2
```

<span data-ttu-id="15f50-155">忘記名為 'Contoso2' 的內容。</span><span class="sxs-lookup"><span data-stu-id="15f50-155">Forgets the context that was named 'Contoso2'.</span></span> <span data-ttu-id="15f50-156">您可以使用 `Set-AzContext` 來重新建立此內容</span><span class="sxs-lookup"><span data-stu-id="15f50-156">You can recreate this context using `Set-AzContext`</span></span>

## <a name="removing-credentials"></a><span data-ttu-id="15f50-157">移除認證</span><span class="sxs-lookup"><span data-stu-id="15f50-157">Removing credentials</span></span>

<span data-ttu-id="15f50-158">您可以使用 `Disconnect-AzAccount` (也稱為 `Logout-AzAccount`) 來移除使用者或服務主體的所有憑證和相關聯內容。</span><span class="sxs-lookup"><span data-stu-id="15f50-158">You can remove all credentials and associated contexts for a user or service principal using `Disconnect-AzAccount` (also known as `Logout-AzAccount`).</span></span> <span data-ttu-id="15f50-159">在無參數的情況下執行時，`Disconnect-AzAccount` Cmdlet 會移除目前內容中與使用者或服務主體相關聯的所有認證和內容。</span><span class="sxs-lookup"><span data-stu-id="15f50-159">When executed without parameters, the `Disconnect-AzAccount` cmdlet removes all credentials and contexts associated with the User or Service Principal in the current context.</span></span> <span data-ttu-id="15f50-160">您可以傳入使用者名稱、服務主體名稱或內容，將特定的主體作為目標。</span><span class="sxs-lookup"><span data-stu-id="15f50-160">You may pass in a Username, Service Principal Name, or context to target a particular principal.</span></span>

```azurepowershell-interactive
Disconnect-AzAccount user1@contoso.org
```

## <a name="using-context-scopes"></a><span data-ttu-id="15f50-161">使用內容範圍</span><span class="sxs-lookup"><span data-stu-id="15f50-161">Using context scopes</span></span>

<span data-ttu-id="15f50-162">有時候，您需要在不影響其他工作階段的情況下，選取、變更或移除 PowerShell 工作階段中的內容。</span><span class="sxs-lookup"><span data-stu-id="15f50-162">Occasionally, you may want to select, change, or remove a context in a PowerShell session without impacting other sessions.</span></span> <span data-ttu-id="15f50-163">若要變更內容 Cmdlet 的預設行為，請使用 `Scope` 參數。</span><span class="sxs-lookup"><span data-stu-id="15f50-163">To change the default behavior of context cmdlets, use the `Scope` parameter.</span></span> <span data-ttu-id="15f50-164">`Process` 範圍會覆寫預設行為，方法是僅使其套用於目前的工作階段。</span><span class="sxs-lookup"><span data-stu-id="15f50-164">The `Process` scope overrides the default behavior by making it apply only for the current session.</span></span> <span data-ttu-id="15f50-165">相反地，`CurrentUser` 範圍會變更所有工作階段，而非只有目前工作階段中的內容。</span><span class="sxs-lookup"><span data-stu-id="15f50-165">Conversely `CurrentUser` scope changes the context in all sessions, instead of just the current session.</span></span>

<span data-ttu-id="15f50-166">例如，若要在不影響其他視窗的情況下，變更目前 PowerShell 工作階段中的預設內容，或是下次開啟工作階段時使用的內容，請使用：</span><span class="sxs-lookup"><span data-stu-id="15f50-166">As an example, to change the default context in the current PowerShell session without impacting other windows, or the context used the next time a session is opened, use:</span></span>

```azurepowershell-interactive
PS C:\> Select-AzContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a><span data-ttu-id="15f50-167">會記住內容自動儲存設定的方式</span><span class="sxs-lookup"><span data-stu-id="15f50-167">How the context autosave setting is remembered</span></span>

<span data-ttu-id="15f50-168">內容自動儲存設定會儲存到使用者 Azure PowerShell 目錄 (在 Windows 上為 `$env:USERPROFILE\.Azure`，在其他平台上則為 `$HOME/.Azure`)。</span><span class="sxs-lookup"><span data-stu-id="15f50-168">The context AutoSave setting is saved to the user Azure PowerShell directory (`$env:USERPROFILE\.Azure` on Windows, and `$HOME/.Azure` on other platforms).</span></span> <span data-ttu-id="15f50-169">部分類型的電腦帳戶可能無法存取此目錄。</span><span class="sxs-lookup"><span data-stu-id="15f50-169">Some kinds of computer accounts may not have access to this directory.</span></span> <span data-ttu-id="15f50-170">如需這類的情節，您可以使用環境變數</span><span class="sxs-lookup"><span data-stu-id="15f50-170">For such scenarios, you can use the environment variable</span></span>

```azurepowershell-interactive
$env:AzureRmContextAutoSave="true" | "false"
```

<span data-ttu-id="15f50-171">設為 'true' 時，就會自動儲存內容。</span><span class="sxs-lookup"><span data-stu-id="15f50-171">When set to 'true', the context is automatically saved.</span></span> <span data-ttu-id="15f50-172">如果設為 'false'，就不會自動儲存內容。</span><span class="sxs-lookup"><span data-stu-id="15f50-172">If set to 'false', the context isn't saved.</span></span>

## <a name="context-management-cmdlets"></a><span data-ttu-id="15f50-173">內容管理 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="15f50-173">Context management cmdlets</span></span>

- <span data-ttu-id="15f50-174">[Enable-AzContextAutosave][enable] - 可在 Powershell 工作階段之間儲存內容。</span><span class="sxs-lookup"><span data-stu-id="15f50-174">[Enable-AzContextAutosave][enable] - Allow saving the context between powershell sessions.</span></span>
  <span data-ttu-id="15f50-175">任何變更都會改變全域內容。</span><span class="sxs-lookup"><span data-stu-id="15f50-175">Any changes alter the global context.</span></span>
- <span data-ttu-id="15f50-176">[Disable-AzContextAutosave][disable] - 關閉自動儲存內容。</span><span class="sxs-lookup"><span data-stu-id="15f50-176">[Disable-AzContextAutosave][disable] - Turn off autosaving the context.</span></span> <span data-ttu-id="15f50-177">需要每個新的 PowerShell 工作階段才能再次登入。</span><span class="sxs-lookup"><span data-stu-id="15f50-177">Each new PowerShell session is required to sign in again.</span></span>
- <span data-ttu-id="15f50-178">[Select-AzContext][select] - 選取內容作為預設值。</span><span class="sxs-lookup"><span data-stu-id="15f50-178">[Select-AzContext][select] - Select a context as the default.</span></span> <span data-ttu-id="15f50-179">所有 Cmdlet 都會使用此內容中的認證來進行驗證。</span><span class="sxs-lookup"><span data-stu-id="15f50-179">All cmdlets use the credentials in this context for authentication.</span></span>
- <span data-ttu-id="15f50-180">[Disconnect-AzAccount][remove-cred] - 移除與帳戶相關聯的所有認證和內容。</span><span class="sxs-lookup"><span data-stu-id="15f50-180">[Disconnect-AzAccount][remove-cred] - Remove all credentials and contexts associated with an account.</span></span>
- <span data-ttu-id="15f50-181">[Remove-AzContext][remove-context] - 將已命名的內容移除。</span><span class="sxs-lookup"><span data-stu-id="15f50-181">[Remove-AzContext][remove-context] - Remove a named context.</span></span>
- <span data-ttu-id="15f50-182">[Rename-AzContext][rename] - 將現有的內容重新命名。</span><span class="sxs-lookup"><span data-stu-id="15f50-182">[Rename-AzContext][rename] - Rename an existing context.</span></span>
- <span data-ttu-id="15f50-183">[Add-AzAccount][login] - 允許登入程序或目前使用者的範圍。</span><span class="sxs-lookup"><span data-stu-id="15f50-183">[Add-AzAccount][login] - Allow scoping of the sign-in to the process or the current user.</span></span>
  <span data-ttu-id="15f50-184">允許驗證之後命名預設內容。</span><span class="sxs-lookup"><span data-stu-id="15f50-184">Allow naming the default context after authentication.</span></span>
- <span data-ttu-id="15f50-185">[Import-AzContext][import] - 允許登入程序或目前使用者的範圍。</span><span class="sxs-lookup"><span data-stu-id="15f50-185">[Import-AzContext][import] - Allow scoping of the sign-in to the process or the current user.</span></span>
- <span data-ttu-id="15f50-186">[Set-AzContext][set-context] - 允許選取現有的已命名內容，以及對程序或目前使用者的範圍變更。</span><span class="sxs-lookup"><span data-stu-id="15f50-186">[Set-AzContext][set-context] - Allow selection of existing named contexts, and scope changes to the process or current user.</span></span>

<!-- Hyperlinks -->
[enable]: /powershell/module/az.accounts/Enable-AzureRmContextAutosave
[disable]: /powershell/module/az.accounts/Disable-AzContextAutosave
[select]: /powershell/module/az.accounts/Select-AzContext
[remove-cred]: /powershell/module/az.accounts/Disconnect-AzAccount
[remove-context]: /powershell/module/az.accounts/Remove-AzContext
[rename]: /powershell/module/az.accounts/Rename-AzContext

<!-- Updated cmdlets -->
[login]: /powershell/module/az.accounts/Connect-AzAccount
[import]:  /powershell/module/az.accounts/Import-AzContext
[set-context]: /powershell/module/az.accounts/Set-AzContext
