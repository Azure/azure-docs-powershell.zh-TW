---
Module Name: Az.Accounts
Module Guid: 342714fc-4009-4863-8afb-a9067e3db04b
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.accounts
Help Version: 4.6.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Az.Accounts.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Az.Accounts.md
ms.openlocfilehash: d15e053e8801c292add5a80e04726f1eeb1181fe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137937"
---
# <span data-ttu-id="9d85d-101">Az. [帳戶] 模組</span><span class="sxs-lookup"><span data-stu-id="9d85d-101">Az.Accounts Module</span></span>
## <span data-ttu-id="9d85d-102">說明</span><span class="sxs-lookup"><span data-stu-id="9d85d-102">Description</span></span>
<span data-ttu-id="9d85d-103">管理所有 Azure 模組的認證與一般設定。</span><span class="sxs-lookup"><span data-stu-id="9d85d-103">Manages credentials and common configuration for all Azure modules.</span></span>

## <span data-ttu-id="9d85d-104">Az. 帳戶 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9d85d-104">Az.Accounts Cmdlets</span></span>
### [<span data-ttu-id="9d85d-105">附加 AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="9d85d-105">Add-AzEnvironment</span></span>](Add-AzEnvironment.md)
<span data-ttu-id="9d85d-106">新增 Azure 資源管理員實例的端點和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="9d85d-106">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

### [<span data-ttu-id="9d85d-107">Clear-AzCoNtext</span><span class="sxs-lookup"><span data-stu-id="9d85d-107">Clear-AzContext</span></span>](Clear-AzContext.md)
<span data-ttu-id="9d85d-108">移除所有 Azure 認證、帳戶及訂閱資訊。</span><span class="sxs-lookup"><span data-stu-id="9d85d-108">Remove all Azure credentials, account, and subscription information.</span></span>

### [<span data-ttu-id="9d85d-109">Clear-AzDefault</span><span class="sxs-lookup"><span data-stu-id="9d85d-109">Clear-AzDefault</span></span>](Clear-AzDefault.md)
<span data-ttu-id="9d85d-110">清除目前內容中由使用者設定的預設值。</span><span class="sxs-lookup"><span data-stu-id="9d85d-110">Clears the defaults set by the user in the current context.</span></span>

### [<span data-ttu-id="9d85d-111">連接-AzAccount</span><span class="sxs-lookup"><span data-stu-id="9d85d-111">Connect-AzAccount</span></span>](Connect-AzAccount.md)
<span data-ttu-id="9d85d-112">使用已驗證的帳戶連線至 Azure，以便與 Az PowerShell 模組中的 Cmdlet 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="9d85d-112">Connect to Azure with an authenticated account for use with cmdlets from the Az PowerShell modules.</span></span>

### [<span data-ttu-id="9d85d-113">Disable-AzCoNtextAutosave</span><span class="sxs-lookup"><span data-stu-id="9d85d-113">Disable-AzContextAutosave</span></span>](Disable-AzContextAutosave.md)
<span data-ttu-id="9d85d-114">關閉 autosaving Azure 認證。</span><span class="sxs-lookup"><span data-stu-id="9d85d-114">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="9d85d-115">下次開啟 PowerShell 視窗時，系統會忘記您的登入資訊</span><span class="sxs-lookup"><span data-stu-id="9d85d-115">Your login information will be forgotten the next time you open a PowerShell window</span></span>

### [<span data-ttu-id="9d85d-116">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="9d85d-116">Disable-AzDataCollection</span></span>](Disable-AzDataCollection.md)
<span data-ttu-id="9d85d-117">在收集資料時，無法改善 Azure PowerShell Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9d85d-117">Opts out of collecting data to improve the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="9d85d-118">預設會收集資料，除非您明確退出宣告。</span><span class="sxs-lookup"><span data-stu-id="9d85d-118">Data is collected by default unless you explicitly opt out.</span></span>

### [<span data-ttu-id="9d85d-119">Disable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="9d85d-119">Disable-AzureRmAlias</span></span>](Disable-AzureRmAlias.md)
<span data-ttu-id="9d85d-120">針對 Az 模組停用 AzureRm 首碼別名。</span><span class="sxs-lookup"><span data-stu-id="9d85d-120">Disables AzureRm prefix aliases for Az modules.</span></span>

### [<span data-ttu-id="9d85d-121">中斷連線-AzAccount</span><span class="sxs-lookup"><span data-stu-id="9d85d-121">Disconnect-AzAccount</span></span>](Disconnect-AzAccount.md)
<span data-ttu-id="9d85d-122">中斷連線的 Azure 帳戶，並移除與該帳戶相關聯的所有認證與內容。</span><span class="sxs-lookup"><span data-stu-id="9d85d-122">Disconnects a connected Azure account and removes all credentials and contexts associated with that account.</span></span>

### [<span data-ttu-id="9d85d-123">Enable-AzCoNtextAutosave</span><span class="sxs-lookup"><span data-stu-id="9d85d-123">Enable-AzContextAutosave</span></span>](Enable-AzContextAutosave.md)
<span data-ttu-id="9d85d-124">允許在您開啟 PowerShell 視窗時，儲存 azure 認證、帳戶和訂閱資訊，並自動載入。</span><span class="sxs-lookup"><span data-stu-id="9d85d-124">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

### [<span data-ttu-id="9d85d-125">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="9d85d-125">Enable-AzDataCollection</span></span>](Enable-AzDataCollection.md)
<span data-ttu-id="9d85d-126">啟用 Azure PowerShell 以收集資料，以使用 Azure PowerShell Cmdlet 來改善使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="9d85d-126">Enables Azure PowerShell to collect data to improve the user experience with the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="9d85d-127">執行此 Cmdlet 會將您的目前使用者的資料收集加入到目前的電腦上。</span><span class="sxs-lookup"><span data-stu-id="9d85d-127">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span> <span data-ttu-id="9d85d-128">預設會收集資料，除非您明確退出宣告。</span><span class="sxs-lookup"><span data-stu-id="9d85d-128">Data is collected by default unless you explicitly opt out.</span></span>

### [<span data-ttu-id="9d85d-129">Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="9d85d-129">Enable-AzureRmAlias</span></span>](Enable-AzureRmAlias.md)
<span data-ttu-id="9d85d-130">啟用 Az 模組的 AzureRm 首碼別名。</span><span class="sxs-lookup"><span data-stu-id="9d85d-130">Enables AzureRm prefix aliases for Az modules.</span></span>

### [<span data-ttu-id="9d85d-131">AzCoNtext</span><span class="sxs-lookup"><span data-stu-id="9d85d-131">Get-AzContext</span></span>](Get-AzContext.md)
<span data-ttu-id="9d85d-132">取得用來驗證 Azure 資源管理器要求的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="9d85d-132">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

### [<span data-ttu-id="9d85d-133">AzCoNtextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="9d85d-133">Get-AzContextAutosaveSetting</span></span>](Get-AzContextAutosaveSetting.md)
<span data-ttu-id="9d85d-134">顯示有關內容自動儲存功能的中繼資料，包括是否自動儲存內容，以及可以在何處找到已儲存的內容和認證資訊。</span><span class="sxs-lookup"><span data-stu-id="9d85d-134">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

### [<span data-ttu-id="9d85d-135">AzDefault</span><span class="sxs-lookup"><span data-stu-id="9d85d-135">Get-AzDefault</span></span>](Get-AzDefault.md)
<span data-ttu-id="9d85d-136">取得使用者在目前內容中設定的預設值。</span><span class="sxs-lookup"><span data-stu-id="9d85d-136">Get the defaults set by the user in the current context.</span></span>

### [<span data-ttu-id="9d85d-137">AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="9d85d-137">Get-AzEnvironment</span></span>](Get-AzEnvironment.md)
<span data-ttu-id="9d85d-138">取得 Azure 服務實例的端點和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="9d85d-138">Get endpoints and metadata for an instance of Azure services.</span></span>

### [<span data-ttu-id="9d85d-139">AzProfile</span><span class="sxs-lookup"><span data-stu-id="9d85d-139">Get-AzProfile</span></span>](Get-AzProfile.md)
<span data-ttu-id="9d85d-140">取得已安裝的模組支援的服務設定檔。</span><span class="sxs-lookup"><span data-stu-id="9d85d-140">Get the service profiles supported by installed modules.</span></span>

### [<span data-ttu-id="9d85d-141">AzSubscription</span><span class="sxs-lookup"><span data-stu-id="9d85d-141">Get-AzSubscription</span></span>](Get-AzSubscription.md)
<span data-ttu-id="9d85d-142">取得目前帳戶可以存取的訂閱。</span><span class="sxs-lookup"><span data-stu-id="9d85d-142">Get subscriptions that the current account can access.</span></span>

### [<span data-ttu-id="9d85d-143">AzTenant</span><span class="sxs-lookup"><span data-stu-id="9d85d-143">Get-AzTenant</span></span>](Get-AzTenant.md)
<span data-ttu-id="9d85d-144">取得目前使用者的授權承租人。</span><span class="sxs-lookup"><span data-stu-id="9d85d-144">Gets tenants that are authorized for the current user.</span></span>

### [<span data-ttu-id="9d85d-145">匯入-AzCoNtext</span><span class="sxs-lookup"><span data-stu-id="9d85d-145">Import-AzContext</span></span>](Import-AzContext.md)
<span data-ttu-id="9d85d-146">從檔案載入 Azure 驗證資訊。</span><span class="sxs-lookup"><span data-stu-id="9d85d-146">Loads Azure authentication information from a file.</span></span>

### [<span data-ttu-id="9d85d-147">Invoke-AzRestMethod</span><span class="sxs-lookup"><span data-stu-id="9d85d-147">Invoke-AzRestMethod</span></span>](Invoke-AzRestMethod.md)
<span data-ttu-id="9d85d-148">僅針對 Azure 資源管理端點構造及執行 HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="9d85d-148">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

### [<span data-ttu-id="9d85d-149">Register-AzModule</span><span class="sxs-lookup"><span data-stu-id="9d85d-149">Register-AzModule</span></span>](Register-AzModule.md)
<span data-ttu-id="9d85d-150">僅供內部使用-提供 AutoRest 產生的 Cmdlet 的執行時間支援</span><span class="sxs-lookup"><span data-stu-id="9d85d-150">FOR INTERNAL USE ONLY - Provide Runtime Support for AutoRest Generated cmdlets</span></span>

### [<span data-ttu-id="9d85d-151">移除-AzCoNtext</span><span class="sxs-lookup"><span data-stu-id="9d85d-151">Remove-AzContext</span></span>](Remove-AzContext.md)
<span data-ttu-id="9d85d-152">從可用的上下文集合中移除內容</span><span class="sxs-lookup"><span data-stu-id="9d85d-152">Remove a context from the set of available contexts</span></span>

### [<span data-ttu-id="9d85d-153">移除-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="9d85d-153">Remove-AzEnvironment</span></span>](Remove-AzEnvironment.md)
<span data-ttu-id="9d85d-154">移除端點和中繼資料以連接至指定的 Azure 實例。</span><span class="sxs-lookup"><span data-stu-id="9d85d-154">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

### [<span data-ttu-id="9d85d-155">重新命名 AzCoNtext</span><span class="sxs-lookup"><span data-stu-id="9d85d-155">Rename-AzContext</span></span>](Rename-AzContext.md)
<span data-ttu-id="9d85d-156">重新命名 Azure 內容。</span><span class="sxs-lookup"><span data-stu-id="9d85d-156">Rename an Azure context.</span></span>  <span data-ttu-id="9d85d-157">根據預設，上下文是依使用者帳戶和訂閱來命名。</span><span class="sxs-lookup"><span data-stu-id="9d85d-157">By default contexts are named by user account and subscription.</span></span>

### [<span data-ttu-id="9d85d-158">解決-AzError</span><span class="sxs-lookup"><span data-stu-id="9d85d-158">Resolve-AzError</span></span>](Resolve-AzError.md)
<span data-ttu-id="9d85d-159">顯示有關 PowerShell 錯誤的詳細資訊，以及有關 Azure PowerShell 錯誤的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="9d85d-159">Display detailed information about PowerShell errors, with extended details for Azure PowerShell errors.</span></span>

### [<span data-ttu-id="9d85d-160">儲存-AzCoNtext</span><span class="sxs-lookup"><span data-stu-id="9d85d-160">Save-AzContext</span></span>](Save-AzContext.md)
<span data-ttu-id="9d85d-161">儲存目前的驗證資訊以供在其他 PowerShell 會話中使用。</span><span class="sxs-lookup"><span data-stu-id="9d85d-161">Saves the current authentication information for use in other PowerShell sessions.</span></span>

### [<span data-ttu-id="9d85d-162">選取-AzCoNtext</span><span class="sxs-lookup"><span data-stu-id="9d85d-162">Select-AzContext</span></span>](Select-AzContext.md)
<span data-ttu-id="9d85d-163">選取 Azure PowerShell Cmdlet 中的目標訂閱與帳戶</span><span class="sxs-lookup"><span data-stu-id="9d85d-163">Select a subscription and account to target in Azure PowerShell cmdlets</span></span>

### [<span data-ttu-id="9d85d-164">選取-AzProfile</span><span class="sxs-lookup"><span data-stu-id="9d85d-164">Select-AzProfile</span></span>](Select-AzProfile.md)
<span data-ttu-id="9d85d-165">針對支援多個服務設定檔的模組，請載入與指定的服務設定檔相對應的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9d85d-165">For modules that support multiple service profiles - load the cmdlets corresponding with the given service profile.</span></span>

### [<span data-ttu-id="9d85d-166">傳送-意見反應</span><span class="sxs-lookup"><span data-stu-id="9d85d-166">Send-Feedback</span></span>](Send-Feedback.md)
<span data-ttu-id="9d85d-167">透過一組引導提示，將意見反應傳送給 Azure PowerShell 小組。</span><span class="sxs-lookup"><span data-stu-id="9d85d-167">Sends feedback to the Azure PowerShell team via a set of guided prompts.</span></span>

### [<span data-ttu-id="9d85d-168">Set-AzCoNtext</span><span class="sxs-lookup"><span data-stu-id="9d85d-168">Set-AzContext</span></span>](Set-AzContext.md)
<span data-ttu-id="9d85d-169">設定要在目前會話中使用之 Cmdlet 的租使用者、訂閱及環境。</span><span class="sxs-lookup"><span data-stu-id="9d85d-169">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

### [<span data-ttu-id="9d85d-170">Set-AzDefault</span><span class="sxs-lookup"><span data-stu-id="9d85d-170">Set-AzDefault</span></span>](Set-AzDefault.md)
<span data-ttu-id="9d85d-171">在目前的內容中設定預設值</span><span class="sxs-lookup"><span data-stu-id="9d85d-171">Sets a default in the current context</span></span>

### [<span data-ttu-id="9d85d-172">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="9d85d-172">Set-AzEnvironment</span></span>](Set-AzEnvironment.md)
<span data-ttu-id="9d85d-173">設定 Azure 環境的屬性。</span><span class="sxs-lookup"><span data-stu-id="9d85d-173">Sets properties for an Azure environment.</span></span>

### [<span data-ttu-id="9d85d-174">卸載-AzureRm</span><span class="sxs-lookup"><span data-stu-id="9d85d-174">Uninstall-AzureRm</span></span>](Uninstall-AzureRm.md)
<span data-ttu-id="9d85d-175">從電腦中移除所有 AzureRm 模組。</span><span class="sxs-lookup"><span data-stu-id="9d85d-175">Removes all AzureRm modules from a machine.</span></span>

