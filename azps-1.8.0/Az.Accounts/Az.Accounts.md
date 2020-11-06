---
Module Name: Az.Accounts
Module Guid: 342714fc-4009-4863-8afb-a9067e3db04b
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.accounts
Help Version: 4.6.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Az.Accounts.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Az.Accounts.md
ms.openlocfilehash: 134ce4c55d29d5f0dc6c46a1d0495f392694386f
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/23/2019
ms.locfileid: "93611313"
---
# <span data-ttu-id="597f3-101">Az. [帳戶] 模組</span><span class="sxs-lookup"><span data-stu-id="597f3-101">Az.Accounts Module</span></span>
## <span data-ttu-id="597f3-102">說明</span><span class="sxs-lookup"><span data-stu-id="597f3-102">Description</span></span>
<span data-ttu-id="597f3-103">管理所有 Azure 模組的認證與一般設定。</span><span class="sxs-lookup"><span data-stu-id="597f3-103">Manages credentials and common configuration for all Azure modules.</span></span>

## <span data-ttu-id="597f3-104">Az. 帳戶 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="597f3-104">Az.Accounts Cmdlets</span></span>
### [<span data-ttu-id="597f3-105">附加 AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="597f3-105">Add-AzEnvironment</span></span>](Add-AzEnvironment.md)
<span data-ttu-id="597f3-106">新增 Azure 資源管理員實例的端點和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="597f3-106">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

### [<span data-ttu-id="597f3-107">Clear-AzCoNtext</span><span class="sxs-lookup"><span data-stu-id="597f3-107">Clear-AzContext</span></span>](Clear-AzContext.md)
<span data-ttu-id="597f3-108">移除所有 Azure 認證、帳戶及訂閱資訊。</span><span class="sxs-lookup"><span data-stu-id="597f3-108">Remove all Azure credentials, account, and subscription information.</span></span>

### [<span data-ttu-id="597f3-109">Clear-AzDefault</span><span class="sxs-lookup"><span data-stu-id="597f3-109">Clear-AzDefault</span></span>](Clear-AzDefault.md)
<span data-ttu-id="597f3-110">清除目前內容中由使用者設定的預設值。</span><span class="sxs-lookup"><span data-stu-id="597f3-110">Clears the defaults set by the user in the current context.</span></span>

### [<span data-ttu-id="597f3-111">連接-AzAccount</span><span class="sxs-lookup"><span data-stu-id="597f3-111">Connect-AzAccount</span></span>](Connect-AzAccount.md)
<span data-ttu-id="597f3-112">使用已驗證的帳戶連線至 Azure，以與 Azure 資源管理器 Cmdlet 要求搭配使用。</span><span class="sxs-lookup"><span data-stu-id="597f3-112">Connect to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

### [<span data-ttu-id="597f3-113">Disable-AzCoNtextAutosave</span><span class="sxs-lookup"><span data-stu-id="597f3-113">Disable-AzContextAutosave</span></span>](Disable-AzContextAutosave.md)
<span data-ttu-id="597f3-114">關閉 autosaving Azure 認證。</span><span class="sxs-lookup"><span data-stu-id="597f3-114">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="597f3-115">下次開啟 PowerShell 視窗時，系統會忘記您的登入資訊</span><span class="sxs-lookup"><span data-stu-id="597f3-115">Your login information will be forgotten the next time you open a PowerShell window</span></span>

### [<span data-ttu-id="597f3-116">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="597f3-116">Disable-AzDataCollection</span></span>](Disable-AzDataCollection.md)
<span data-ttu-id="597f3-117">在收集資料時，無法改善 AzurePowerShell Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="597f3-117">Opts out of collecting data to improve the AzurePowerShell cmdlets.</span></span> <span data-ttu-id="597f3-118">除非您明確加入宣告，否則不會收集資料。</span><span class="sxs-lookup"><span data-stu-id="597f3-118">Data is not collected unless you explicitly opt in.</span></span>

### [<span data-ttu-id="597f3-119">Disable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="597f3-119">Disable-AzureRmAlias</span></span>](Disable-AzureRmAlias.md)
<span data-ttu-id="597f3-120">針對 Az 模組停用 AzureRm 首碼別名。</span><span class="sxs-lookup"><span data-stu-id="597f3-120">Disables AzureRm prefix aliases for Az modules.</span></span>

### [<span data-ttu-id="597f3-121">中斷連線-AzAccount</span><span class="sxs-lookup"><span data-stu-id="597f3-121">Disconnect-AzAccount</span></span>](Disconnect-AzAccount.md)
<span data-ttu-id="597f3-122">中斷連線的 Azure 帳戶，並移除與該帳戶相關聯的所有認證與內容。</span><span class="sxs-lookup"><span data-stu-id="597f3-122">Disconnects a connected Azure account and removes all credentials and contexts associated with that account.</span></span>

### [<span data-ttu-id="597f3-123">Enable-AzCoNtextAutosave</span><span class="sxs-lookup"><span data-stu-id="597f3-123">Enable-AzContextAutosave</span></span>](Enable-AzContextAutosave.md)
<span data-ttu-id="597f3-124">允許在您開啟 PowerShell 視窗時，儲存 azure 認證、帳戶和訂閱資訊，並自動載入。</span><span class="sxs-lookup"><span data-stu-id="597f3-124">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

### [<span data-ttu-id="597f3-125">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="597f3-125">Enable-AzDataCollection</span></span>](Enable-AzDataCollection.md)
<span data-ttu-id="597f3-126">啟用 Azure PowerShell 以收集資料，以使用 AzurePowerShell Cmdlet 來改善使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="597f3-126">Enables Azure PowerShell to collect data to improve the user experience with AzurePowerShell cmdlets.</span></span>
<span data-ttu-id="597f3-127">執行此 Cmdlet 會將您的目前使用者的資料收集加入到目前的電腦上。</span><span class="sxs-lookup"><span data-stu-id="597f3-127">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span>
<span data-ttu-id="597f3-128">除非您明確加入宣告，否則不會收集任何資料。</span><span class="sxs-lookup"><span data-stu-id="597f3-128">No data is collected unless you explicitly opt in.</span></span>

### [<span data-ttu-id="597f3-129">Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="597f3-129">Enable-AzureRmAlias</span></span>](Enable-AzureRmAlias.md)
<span data-ttu-id="597f3-130">啟用 Az 模組的 AzureRm 首碼別名。</span><span class="sxs-lookup"><span data-stu-id="597f3-130">Enables AzureRm prefix aliases for Az modules.</span></span>

### [<span data-ttu-id="597f3-131">AzCoNtext</span><span class="sxs-lookup"><span data-stu-id="597f3-131">Get-AzContext</span></span>](Get-AzContext.md)
<span data-ttu-id="597f3-132">取得用來驗證 Azure 資源管理器要求的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="597f3-132">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

### [<span data-ttu-id="597f3-133">AzCoNtextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="597f3-133">Get-AzContextAutosaveSetting</span></span>](Get-AzContextAutosaveSetting.md)
<span data-ttu-id="597f3-134">顯示有關內容自動儲存功能的中繼資料，包括是否自動儲存內容，以及可以在何處找到已儲存的內容和認證資訊。</span><span class="sxs-lookup"><span data-stu-id="597f3-134">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

### [<span data-ttu-id="597f3-135">AzDefault</span><span class="sxs-lookup"><span data-stu-id="597f3-135">Get-AzDefault</span></span>](Get-AzDefault.md)
<span data-ttu-id="597f3-136">取得使用者在目前內容中設定的預設值。</span><span class="sxs-lookup"><span data-stu-id="597f3-136">Get the defaults set by the user in the current context.</span></span>

### [<span data-ttu-id="597f3-137">AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="597f3-137">Get-AzEnvironment</span></span>](Get-AzEnvironment.md)
<span data-ttu-id="597f3-138">取得 Azure 服務實例的端點和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="597f3-138">Get endpoints and metadata for an instance of Azure services.</span></span>

### [<span data-ttu-id="597f3-139">AzSubscription</span><span class="sxs-lookup"><span data-stu-id="597f3-139">Get-AzSubscription</span></span>](Get-AzSubscription.md)
<span data-ttu-id="597f3-140">取得目前帳戶可以存取的訂閱。</span><span class="sxs-lookup"><span data-stu-id="597f3-140">Get subscriptions that the current account can access.</span></span>

### [<span data-ttu-id="597f3-141">AzTenant</span><span class="sxs-lookup"><span data-stu-id="597f3-141">Get-AzTenant</span></span>](Get-AzTenant.md)
<span data-ttu-id="597f3-142">取得目前使用者的授權承租人。</span><span class="sxs-lookup"><span data-stu-id="597f3-142">Gets tenants that are authorized for the current user.</span></span>

### [<span data-ttu-id="597f3-143">匯入-AzCoNtext</span><span class="sxs-lookup"><span data-stu-id="597f3-143">Import-AzContext</span></span>](Import-AzContext.md)
<span data-ttu-id="597f3-144">從檔案載入 Azure 驗證資訊。</span><span class="sxs-lookup"><span data-stu-id="597f3-144">Loads Azure authentication information from a file.</span></span>

### [<span data-ttu-id="597f3-145">Register-AzModule</span><span class="sxs-lookup"><span data-stu-id="597f3-145">Register-AzModule</span></span>](Register-AzModule.md)
<span data-ttu-id="597f3-146">提供 AUtoRest 產生的 Cmdlet 之執行時間支援的內部專用 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="597f3-146">Internal-only cmdlet that provides runtime support for AUtoRest generated cmdlets.</span></span>

### [<span data-ttu-id="597f3-147">移除-AzCoNtext</span><span class="sxs-lookup"><span data-stu-id="597f3-147">Remove-AzContext</span></span>](Remove-AzContext.md)
<span data-ttu-id="597f3-148">從可用的上下文集合中移除內容</span><span class="sxs-lookup"><span data-stu-id="597f3-148">Remove a context from the set of available contexts</span></span>

### [<span data-ttu-id="597f3-149">移除-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="597f3-149">Remove-AzEnvironment</span></span>](Remove-AzEnvironment.md)
<span data-ttu-id="597f3-150">移除端點和中繼資料以連接至指定的 Azure 實例。</span><span class="sxs-lookup"><span data-stu-id="597f3-150">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

### [<span data-ttu-id="597f3-151">重新命名 AzCoNtext</span><span class="sxs-lookup"><span data-stu-id="597f3-151">Rename-AzContext</span></span>](Rename-AzContext.md)
<span data-ttu-id="597f3-152">重新命名 Azure 內容。</span><span class="sxs-lookup"><span data-stu-id="597f3-152">Rename an Azure context.</span></span>  <span data-ttu-id="597f3-153">根據預設，上下文是依使用者帳戶和訂閱來命名。</span><span class="sxs-lookup"><span data-stu-id="597f3-153">By default contexts are named by user account and subscription.</span></span>

### [<span data-ttu-id="597f3-154">解決-AzError</span><span class="sxs-lookup"><span data-stu-id="597f3-154">Resolve-AzError</span></span>](Resolve-AzError.md)
<span data-ttu-id="597f3-155">顯示有關 PowerShell 錯誤的詳細資訊，以及有關 Azure PowerShell 錯誤的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="597f3-155">Display detailed information about PowerShell errors, with extended details for Azure PowerShell errors.</span></span>

### [<span data-ttu-id="597f3-156">儲存-AzCoNtext</span><span class="sxs-lookup"><span data-stu-id="597f3-156">Save-AzContext</span></span>](Save-AzContext.md)
<span data-ttu-id="597f3-157">儲存目前的驗證資訊以供在其他 PowerShell 會話中使用。</span><span class="sxs-lookup"><span data-stu-id="597f3-157">Saves the current authentication information for use in other PowerShell sessions.</span></span>

### [<span data-ttu-id="597f3-158">選取-AzCoNtext</span><span class="sxs-lookup"><span data-stu-id="597f3-158">Select-AzContext</span></span>](Select-AzContext.md)
<span data-ttu-id="597f3-159">選取 Azure PowerShell Cmdlet 中的目標訂閱與帳戶</span><span class="sxs-lookup"><span data-stu-id="597f3-159">Select a subscription and account to target in Azure PowerShell cmdlets</span></span>

### [<span data-ttu-id="597f3-160">傳送-意見反應</span><span class="sxs-lookup"><span data-stu-id="597f3-160">Send-Feedback</span></span>](Send-Feedback.md)
<span data-ttu-id="597f3-161">透過一組引導提示，將意見反應傳送給 Azure PowerShell 小組。</span><span class="sxs-lookup"><span data-stu-id="597f3-161">Sends feedback to the Azure PowerShell team via a set of guided prompts.</span></span>

### [<span data-ttu-id="597f3-162">Set-AzCoNtext</span><span class="sxs-lookup"><span data-stu-id="597f3-162">Set-AzContext</span></span>](Set-AzContext.md)
<span data-ttu-id="597f3-163">設定要在目前會話中使用之 Cmdlet 的租使用者、訂閱及環境。</span><span class="sxs-lookup"><span data-stu-id="597f3-163">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

### [<span data-ttu-id="597f3-164">Set-AzDefault</span><span class="sxs-lookup"><span data-stu-id="597f3-164">Set-AzDefault</span></span>](Set-AzDefault.md)
<span data-ttu-id="597f3-165">在目前的內容中設定預設值</span><span class="sxs-lookup"><span data-stu-id="597f3-165">Sets a default in the current context</span></span>

### [<span data-ttu-id="597f3-166">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="597f3-166">Set-AzEnvironment</span></span>](Set-AzEnvironment.md)
<span data-ttu-id="597f3-167">設定 Azure 環境的屬性。</span><span class="sxs-lookup"><span data-stu-id="597f3-167">Sets properties for an Azure environment.</span></span>

### [<span data-ttu-id="597f3-168">卸載-AzureRm</span><span class="sxs-lookup"><span data-stu-id="597f3-168">Uninstall-AzureRm</span></span>](Uninstall-AzureRm.md)
<span data-ttu-id="597f3-169">從電腦中移除所有 AzureRm 模組。</span><span class="sxs-lookup"><span data-stu-id="597f3-169">Removes all AzureRm modules from a machine.</span></span>

