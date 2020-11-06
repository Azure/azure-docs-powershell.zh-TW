---
Module Name: AzureRM.Profile
Module Guid: 342714fc-4009-4863-8afb-a9067e3db04b
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/AzureRM.Profile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/AzureRM.Profile.md
ms.openlocfilehash: bc3ccc2c2b0574eee40357fb0079fe22124ea3e6
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/23/2019
ms.locfileid: "93442252"
---
# <span data-ttu-id="b766d-101">AzureRM. 設定檔模組</span><span class="sxs-lookup"><span data-stu-id="b766d-101">AzureRM.Profile Module</span></span>
## <span data-ttu-id="b766d-102">說明</span><span class="sxs-lookup"><span data-stu-id="b766d-102">Description</span></span>
<span data-ttu-id="b766d-103">管理所有 Azure 模組的認證與一般設定。</span><span class="sxs-lookup"><span data-stu-id="b766d-103">Manages credentials and common configuration for all Azure modules.</span></span>

## <span data-ttu-id="b766d-104">AzureRM。設定檔 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b766d-104">AzureRM.Profile Cmdlets</span></span>
### [<span data-ttu-id="b766d-105">附加 AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="b766d-105">Add-AzureRmAccount</span></span>](Add-AzureRmAccount.md)
<span data-ttu-id="b766d-106">新增要用於 Azure 資源管理器 Cmdlet 要求的已驗證帳戶。</span><span class="sxs-lookup"><span data-stu-id="b766d-106">Adds an authenticated account to use for Azure Resource Manager cmdlet requests.</span></span>

### [<span data-ttu-id="b766d-107">附加 AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="b766d-107">Add-AzureRmEnvironment</span></span>](Add-AzureRmEnvironment.md)
<span data-ttu-id="b766d-108">新增 Azure 資源管理員實例的端點和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="b766d-108">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

### [<span data-ttu-id="b766d-109">Clear-AzureRmCoNtext</span><span class="sxs-lookup"><span data-stu-id="b766d-109">Clear-AzureRmContext</span></span>](Clear-AzureRmContext.md)
<span data-ttu-id="b766d-110">移除所有 Azure 認證、帳戶及訂閱資訊。</span><span class="sxs-lookup"><span data-stu-id="b766d-110">Remove all Azure credentials, account, and subscription information.</span></span>

### [<span data-ttu-id="b766d-111">Disable-AzureRmCoNtextAutosave</span><span class="sxs-lookup"><span data-stu-id="b766d-111">Disable-AzureRmContextAutosave</span></span>](Disable-AzureRmContextAutosave.md)
<span data-ttu-id="b766d-112">關閉 autosaving Azure 認證。</span><span class="sxs-lookup"><span data-stu-id="b766d-112">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="b766d-113">下次開啟 PowerShell 視窗時，系統會忘記您的登入資訊</span><span class="sxs-lookup"><span data-stu-id="b766d-113">Your login information will be forgotten the next time you open a PowerShell window</span></span>

### [<span data-ttu-id="b766d-114">Disable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="b766d-114">Disable-AzureRmDataCollection</span></span>](Disable-AzureRmDataCollection.md)
<span data-ttu-id="b766d-115">在收集資料時，無法改善 AzurePowerShell Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b766d-115">Opts out of collecting data to improve the AzurePowerShell cmdlets.</span></span> <span data-ttu-id="b766d-116">除非您明確加入宣告，否則不會收集資料。</span><span class="sxs-lookup"><span data-stu-id="b766d-116">Data is not collected unless you explicitly opt in.</span></span>

### [<span data-ttu-id="b766d-117">Enable-AzureRmCoNtextAutosave</span><span class="sxs-lookup"><span data-stu-id="b766d-117">Enable-AzureRmContextAutosave</span></span>](Enable-AzureRmContextAutosave.md)
<span data-ttu-id="b766d-118">允許在您開啟 PowerShell 視窗時，儲存 azure 認證、帳戶和訂閱資訊，並自動載入。</span><span class="sxs-lookup"><span data-stu-id="b766d-118">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

### [<span data-ttu-id="b766d-119">Enable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="b766d-119">Enable-AzureRmDataCollection</span></span>](Enable-AzureRmDataCollection.md)
<span data-ttu-id="b766d-120">啟用 Azure PowerShell 以收集資料，以使用 AzurePowerShell Cmdlet 來改善使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="b766d-120">Enables Azure PowerShell to collect data to improve the user experience with AzurePowerShell cmdlets.</span></span>
<span data-ttu-id="b766d-121">執行此 Cmdlet 會將您的目前使用者的資料收集加入到目前的電腦上。</span><span class="sxs-lookup"><span data-stu-id="b766d-121">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span>
<span data-ttu-id="b766d-122">除非您明確加入宣告，否則不會收集任何資料。</span><span class="sxs-lookup"><span data-stu-id="b766d-122">No data is collected unless you explicitly opt in.</span></span>

### [<span data-ttu-id="b766d-123">AzureRmCoNtext</span><span class="sxs-lookup"><span data-stu-id="b766d-123">Get-AzureRmContext</span></span>](Get-AzureRmContext.md)
<span data-ttu-id="b766d-124">取得用來驗證 Azure 資源管理器要求的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="b766d-124">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

### [<span data-ttu-id="b766d-125">AzureRmCoNtextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="b766d-125">Get-AzureRmContextAutosaveSetting</span></span>](Get-AzureRmContextAutosaveSetting.md)
<span data-ttu-id="b766d-126">顯示有關內容自動儲存功能的中繼資料，包括 whterh 內容會自動儲存，以及可在何處找到已儲存的內容和認證資訊。</span><span class="sxs-lookup"><span data-stu-id="b766d-126">Display metadata about the context autosave feature, including whterh the context is automatically saved, and where saved context and credential information can be found.</span></span>

### [<span data-ttu-id="b766d-127">AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="b766d-127">Get-AzureRmEnvironment</span></span>](Get-AzureRmEnvironment.md)
<span data-ttu-id="b766d-128">取得 Azure 服務實例的端點和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="b766d-128">Get endpoints and metadata for an instance of Azure services.</span></span>

### [<span data-ttu-id="b766d-129">AzureRmSubscription</span><span class="sxs-lookup"><span data-stu-id="b766d-129">Get-AzureRmSubscription</span></span>](Get-AzureRmSubscription.md)
<span data-ttu-id="b766d-130">取得目前帳戶可以存取的訂閱。</span><span class="sxs-lookup"><span data-stu-id="b766d-130">Get subscriptions that the current account can access.</span></span>

### [<span data-ttu-id="b766d-131">AzureRmTenant</span><span class="sxs-lookup"><span data-stu-id="b766d-131">Get-AzureRmTenant</span></span>](Get-AzureRmTenant.md)
<span data-ttu-id="b766d-132">取得目前使用者的授權承租人。</span><span class="sxs-lookup"><span data-stu-id="b766d-132">Gets tenants that are authorized for the current user.</span></span>

### [<span data-ttu-id="b766d-133">匯入-AzureRmCoNtext</span><span class="sxs-lookup"><span data-stu-id="b766d-133">Import-AzureRmContext</span></span>](Import-AzureRmContext.md)
<span data-ttu-id="b766d-134">從檔案載入 Azure 驗證資訊。</span><span class="sxs-lookup"><span data-stu-id="b766d-134">Loads Azure authentication information from a file.</span></span>

### [<span data-ttu-id="b766d-135">移除-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="b766d-135">Remove-AzureRmAccount</span></span>](Remove-AzureRmAccount.md)
<span data-ttu-id="b766d-136">移除所有與此帳戶相關聯的認證與內容。</span><span class="sxs-lookup"><span data-stu-id="b766d-136">Remove all credentials and contexts associated with this account.</span></span>

### [<span data-ttu-id="b766d-137">移除-AzureRmCoNtext</span><span class="sxs-lookup"><span data-stu-id="b766d-137">Remove-AzureRmContext</span></span>](Remove-AzureRmContext.md)
<span data-ttu-id="b766d-138">從可用的上下文集合中移除內容</span><span class="sxs-lookup"><span data-stu-id="b766d-138">Remove a context from the set of available contexts</span></span>

### [<span data-ttu-id="b766d-139">移除-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="b766d-139">Remove-AzureRmEnvironment</span></span>](Remove-AzureRmEnvironment.md)
<span data-ttu-id="b766d-140">移除端點和中繼資料以連接至指定的 Azure 實例。</span><span class="sxs-lookup"><span data-stu-id="b766d-140">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

### [<span data-ttu-id="b766d-141">重新命名 AzureRmCoNtext</span><span class="sxs-lookup"><span data-stu-id="b766d-141">Rename-AzureRmContext</span></span>](Rename-AzureRmContext.md)
<span data-ttu-id="b766d-142">重新命名 Azure 內容。</span><span class="sxs-lookup"><span data-stu-id="b766d-142">Rename an Azure context.</span></span>  <span data-ttu-id="b766d-143">根據預設，上下文是依使用者帳戶和訂閱來命名。</span><span class="sxs-lookup"><span data-stu-id="b766d-143">By default contexts are named by user account and subscription.</span></span>

### [<span data-ttu-id="b766d-144">解決-AzureRmError</span><span class="sxs-lookup"><span data-stu-id="b766d-144">Resolve-AzureRmError</span></span>](Resolve-AzureRmError.md)
<span data-ttu-id="b766d-145">顯示有關 PowerShell 錯誤的詳細資訊，以及有關 Azure PowerShell 錯誤的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="b766d-145">Display detailed information about PowerShell errors, with extended details for Azure PowerShell errors.</span></span>

### [<span data-ttu-id="b766d-146">儲存-AzureRmCoNtext</span><span class="sxs-lookup"><span data-stu-id="b766d-146">Save-AzureRmContext</span></span>](Save-AzureRmContext.md)
<span data-ttu-id="b766d-147">儲存目前的驗證資訊以供在其他 PowerShell 會話中使用。</span><span class="sxs-lookup"><span data-stu-id="b766d-147">Saves the current authentication information for use in other PowerShell sessions.</span></span>

### [<span data-ttu-id="b766d-148">選取-AzureRmCoNtext</span><span class="sxs-lookup"><span data-stu-id="b766d-148">Select-AzureRmContext</span></span>](Select-AzureRmContext.md)
<span data-ttu-id="b766d-149">選取要在 Azure PowerShell Cmdlet 中針對 (或帳戶、租使用者) 的訂閱</span><span class="sxs-lookup"><span data-stu-id="b766d-149">Select a subscription to target (or account, tenant) in Azure PowerShell cmdlets</span></span>

### [<span data-ttu-id="b766d-150">傳送-意見反應</span><span class="sxs-lookup"><span data-stu-id="b766d-150">Send-Feedback</span></span>](Send-Feedback.md)
<span data-ttu-id="b766d-151">透過一組引導提示，將意見反應傳送給 Azure PowerShell 小組。</span><span class="sxs-lookup"><span data-stu-id="b766d-151">Sends feedback to the Azure PowerShell team via a set of guided prompts.</span></span>

### [<span data-ttu-id="b766d-152">Set-AzureRmCoNtext</span><span class="sxs-lookup"><span data-stu-id="b766d-152">Set-AzureRmContext</span></span>](Set-AzureRmContext.md)
<span data-ttu-id="b766d-153">設定要在目前會話中使用之 Cmdlet 的租使用者、訂閱及環境。</span><span class="sxs-lookup"><span data-stu-id="b766d-153">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

### [<span data-ttu-id="b766d-154">Set-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="b766d-154">Set-AzureRmEnvironment</span></span>](Set-AzureRmEnvironment.md)
<span data-ttu-id="b766d-155">設定 Azure 環境的屬性。</span><span class="sxs-lookup"><span data-stu-id="b766d-155">Sets properties for an Azure environment.</span></span>

