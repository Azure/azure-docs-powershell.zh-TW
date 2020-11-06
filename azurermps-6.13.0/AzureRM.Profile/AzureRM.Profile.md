---
Module Name: AzureRM.Profile
Module Guid: 342714fc-4009-4863-8afb-a9067e3db04b
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile
Help Version: 4.6.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/AzureRM.Profile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/AzureRM.Profile.md
ms.openlocfilehash: b9aa5f188d2c4c0167068d304487a0a7d4c7ea2d
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/23/2019
ms.locfileid: "93442211"
---
# <span data-ttu-id="b3141-101">AzureRM. 設定檔模組</span><span class="sxs-lookup"><span data-stu-id="b3141-101">AzureRM.Profile Module</span></span>
## <span data-ttu-id="b3141-102">說明</span><span class="sxs-lookup"><span data-stu-id="b3141-102">Description</span></span>
<span data-ttu-id="b3141-103">管理所有 Azure 模組的認證與一般設定。</span><span class="sxs-lookup"><span data-stu-id="b3141-103">Manages credentials and common configuration for all Azure modules.</span></span>

## <span data-ttu-id="b3141-104">AzureRM。設定檔 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b3141-104">AzureRM.Profile Cmdlets</span></span>
### [<span data-ttu-id="b3141-105">附加 AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="b3141-105">Add-AzureRmEnvironment</span></span>](Add-AzureRmEnvironment.md)
<span data-ttu-id="b3141-106">新增 Azure 資源管理員實例的端點和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="b3141-106">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

### [<span data-ttu-id="b3141-107">Clear-AzureRmCoNtext</span><span class="sxs-lookup"><span data-stu-id="b3141-107">Clear-AzureRmContext</span></span>](Clear-AzureRmContext.md)
<span data-ttu-id="b3141-108">移除所有 Azure 認證、帳戶及訂閱資訊。</span><span class="sxs-lookup"><span data-stu-id="b3141-108">Remove all Azure credentials, account, and subscription information.</span></span>

### [<span data-ttu-id="b3141-109">Clear-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="b3141-109">Clear-AzureRmDefault</span></span>](Clear-AzureRmDefault.md)
<span data-ttu-id="b3141-110">清除目前內容中由使用者設定的預設值。</span><span class="sxs-lookup"><span data-stu-id="b3141-110">Clears the defaults set by the user in the current context.</span></span>

### [<span data-ttu-id="b3141-111">連接-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="b3141-111">Connect-AzureRmAccount</span></span>](Connect-AzureRmAccount.md)
<span data-ttu-id="b3141-112">使用已驗證的帳戶連線至 Azure，以與 Azure 資源管理器 Cmdlet 要求搭配使用。</span><span class="sxs-lookup"><span data-stu-id="b3141-112">Connect to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

### [<span data-ttu-id="b3141-113">Disable-AzureRmCoNtextAutosave</span><span class="sxs-lookup"><span data-stu-id="b3141-113">Disable-AzureRmContextAutosave</span></span>](Disable-AzureRmContextAutosave.md)
<span data-ttu-id="b3141-114">關閉 autosaving Azure 認證。</span><span class="sxs-lookup"><span data-stu-id="b3141-114">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="b3141-115">下次開啟 PowerShell 視窗時，系統會忘記您的登入資訊</span><span class="sxs-lookup"><span data-stu-id="b3141-115">Your login information will be forgotten the next time you open a PowerShell window</span></span>

### [<span data-ttu-id="b3141-116">Disable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="b3141-116">Disable-AzureRmDataCollection</span></span>](Disable-AzureRmDataCollection.md)
<span data-ttu-id="b3141-117">在收集資料時，無法改善 AzurePowerShell Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b3141-117">Opts out of collecting data to improve the AzurePowerShell cmdlets.</span></span> <span data-ttu-id="b3141-118">除非您明確加入宣告，否則不會收集資料。</span><span class="sxs-lookup"><span data-stu-id="b3141-118">Data is not collected unless you explicitly opt in.</span></span>

### [<span data-ttu-id="b3141-119">中斷連線-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="b3141-119">Disconnect-AzureRmAccount</span></span>](Disconnect-AzureRmAccount.md)
<span data-ttu-id="b3141-120">中斷連線的 Azure 帳戶，並移除與該帳戶相關聯的所有認證與內容。</span><span class="sxs-lookup"><span data-stu-id="b3141-120">Disconnects a connected Azure account and removes all credentials and contexts associated with that account.</span></span>

### [<span data-ttu-id="b3141-121">Enable-AzureRmCoNtextAutosave</span><span class="sxs-lookup"><span data-stu-id="b3141-121">Enable-AzureRmContextAutosave</span></span>](Enable-AzureRmContextAutosave.md)
<span data-ttu-id="b3141-122">允許在您開啟 PowerShell 視窗時，儲存 azure 認證、帳戶和訂閱資訊，並自動載入。</span><span class="sxs-lookup"><span data-stu-id="b3141-122">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

### [<span data-ttu-id="b3141-123">Enable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="b3141-123">Enable-AzureRmDataCollection</span></span>](Enable-AzureRmDataCollection.md)
<span data-ttu-id="b3141-124">啟用 Azure PowerShell 以收集資料，以使用 AzurePowerShell Cmdlet 來改善使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="b3141-124">Enables Azure PowerShell to collect data to improve the user experience with AzurePowerShell cmdlets.</span></span>
<span data-ttu-id="b3141-125">執行此 Cmdlet 會將您的目前使用者的資料收集加入到目前的電腦上。</span><span class="sxs-lookup"><span data-stu-id="b3141-125">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span>
<span data-ttu-id="b3141-126">除非您明確加入宣告，否則不會收集任何資料。</span><span class="sxs-lookup"><span data-stu-id="b3141-126">No data is collected unless you explicitly opt in.</span></span>

### [<span data-ttu-id="b3141-127">AzureRmCoNtext</span><span class="sxs-lookup"><span data-stu-id="b3141-127">Get-AzureRmContext</span></span>](Get-AzureRmContext.md)
<span data-ttu-id="b3141-128">取得用來驗證 Azure 資源管理器要求的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="b3141-128">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

### [<span data-ttu-id="b3141-129">AzureRmCoNtextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="b3141-129">Get-AzureRmContextAutosaveSetting</span></span>](Get-AzureRmContextAutosaveSetting.md)
<span data-ttu-id="b3141-130">顯示有關內容自動儲存功能的中繼資料，包括是否自動儲存內容，以及可以在何處找到已儲存的內容和認證資訊。</span><span class="sxs-lookup"><span data-stu-id="b3141-130">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

### [<span data-ttu-id="b3141-131">AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="b3141-131">Get-AzureRmDefault</span></span>](Get-AzureRmDefault.md)
<span data-ttu-id="b3141-132">取得使用者在目前內容中設定的預設值。</span><span class="sxs-lookup"><span data-stu-id="b3141-132">Get the defaults set by the user in the current context.</span></span>

### [<span data-ttu-id="b3141-133">AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="b3141-133">Get-AzureRmEnvironment</span></span>](Get-AzureRmEnvironment.md)
<span data-ttu-id="b3141-134">取得 Azure 服務實例的端點和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="b3141-134">Get endpoints and metadata for an instance of Azure services.</span></span>

### [<span data-ttu-id="b3141-135">AzureRmSubscription</span><span class="sxs-lookup"><span data-stu-id="b3141-135">Get-AzureRmSubscription</span></span>](Get-AzureRmSubscription.md)
<span data-ttu-id="b3141-136">取得目前帳戶可以存取的訂閱。</span><span class="sxs-lookup"><span data-stu-id="b3141-136">Get subscriptions that the current account can access.</span></span>

### [<span data-ttu-id="b3141-137">AzureRmTenant</span><span class="sxs-lookup"><span data-stu-id="b3141-137">Get-AzureRmTenant</span></span>](Get-AzureRmTenant.md)
<span data-ttu-id="b3141-138">取得目前使用者的授權承租人。</span><span class="sxs-lookup"><span data-stu-id="b3141-138">Gets tenants that are authorized for the current user.</span></span>

### [<span data-ttu-id="b3141-139">匯入-AzureRmCoNtext</span><span class="sxs-lookup"><span data-stu-id="b3141-139">Import-AzureRmContext</span></span>](Import-AzureRmContext.md)
<span data-ttu-id="b3141-140">從檔案載入 Azure 驗證資訊。</span><span class="sxs-lookup"><span data-stu-id="b3141-140">Loads Azure authentication information from a file.</span></span>

### [<span data-ttu-id="b3141-141">移除-AzureRmCoNtext</span><span class="sxs-lookup"><span data-stu-id="b3141-141">Remove-AzureRmContext</span></span>](Remove-AzureRmContext.md)
<span data-ttu-id="b3141-142">從可用的上下文集合中移除內容</span><span class="sxs-lookup"><span data-stu-id="b3141-142">Remove a context from the set of available contexts</span></span>

### [<span data-ttu-id="b3141-143">移除-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="b3141-143">Remove-AzureRmEnvironment</span></span>](Remove-AzureRmEnvironment.md)
<span data-ttu-id="b3141-144">移除端點和中繼資料以連接至指定的 Azure 實例。</span><span class="sxs-lookup"><span data-stu-id="b3141-144">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

### [<span data-ttu-id="b3141-145">重新命名 AzureRmCoNtext</span><span class="sxs-lookup"><span data-stu-id="b3141-145">Rename-AzureRmContext</span></span>](Rename-AzureRmContext.md)
<span data-ttu-id="b3141-146">重新命名 Azure 內容。</span><span class="sxs-lookup"><span data-stu-id="b3141-146">Rename an Azure context.</span></span>  <span data-ttu-id="b3141-147">根據預設，上下文是依使用者帳戶和訂閱來命名。</span><span class="sxs-lookup"><span data-stu-id="b3141-147">By default contexts are named by user account and subscription.</span></span>

### [<span data-ttu-id="b3141-148">解決-AzureRmError</span><span class="sxs-lookup"><span data-stu-id="b3141-148">Resolve-AzureRmError</span></span>](Resolve-AzureRmError.md)
<span data-ttu-id="b3141-149">顯示有關 PowerShell 錯誤的詳細資訊，以及有關 Azure PowerShell 錯誤的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="b3141-149">Display detailed information about PowerShell errors, with extended details for Azure PowerShell errors.</span></span>

### [<span data-ttu-id="b3141-150">儲存-AzureRmCoNtext</span><span class="sxs-lookup"><span data-stu-id="b3141-150">Save-AzureRmContext</span></span>](Save-AzureRmContext.md)
<span data-ttu-id="b3141-151">儲存目前的驗證資訊以供在其他 PowerShell 會話中使用。</span><span class="sxs-lookup"><span data-stu-id="b3141-151">Saves the current authentication information for use in other PowerShell sessions.</span></span>

### [<span data-ttu-id="b3141-152">選取-AzureRmCoNtext</span><span class="sxs-lookup"><span data-stu-id="b3141-152">Select-AzureRmContext</span></span>](Select-AzureRmContext.md)
<span data-ttu-id="b3141-153">選取 Azure PowerShell Cmdlet 中的目標訂閱與帳戶</span><span class="sxs-lookup"><span data-stu-id="b3141-153">Select a subscription and account to target in Azure PowerShell cmdlets</span></span>

### [<span data-ttu-id="b3141-154">傳送-意見反應</span><span class="sxs-lookup"><span data-stu-id="b3141-154">Send-Feedback</span></span>](Send-Feedback.md)
<span data-ttu-id="b3141-155">透過一組引導提示，將意見反應傳送給 Azure PowerShell 小組。</span><span class="sxs-lookup"><span data-stu-id="b3141-155">Sends feedback to the Azure PowerShell team via a set of guided prompts.</span></span>

### [<span data-ttu-id="b3141-156">Set-AzureRmCoNtext</span><span class="sxs-lookup"><span data-stu-id="b3141-156">Set-AzureRmContext</span></span>](Set-AzureRmContext.md)
<span data-ttu-id="b3141-157">設定要在目前會話中使用之 Cmdlet 的租使用者、訂閱及環境。</span><span class="sxs-lookup"><span data-stu-id="b3141-157">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

### [<span data-ttu-id="b3141-158">Set-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="b3141-158">Set-AzureRmDefault</span></span>](Set-AzureRmDefault.md)
<span data-ttu-id="b3141-159">在目前的內容中設定預設值</span><span class="sxs-lookup"><span data-stu-id="b3141-159">Sets a default in the current context</span></span>

### [<span data-ttu-id="b3141-160">Set-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="b3141-160">Set-AzureRmEnvironment</span></span>](Set-AzureRmEnvironment.md)
<span data-ttu-id="b3141-161">設定 Azure 環境的屬性。</span><span class="sxs-lookup"><span data-stu-id="b3141-161">Sets properties for an Azure environment.</span></span>

