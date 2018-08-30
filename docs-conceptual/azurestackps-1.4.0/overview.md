# <a name="azure-stack-module-140"></a><span data-ttu-id="6ec6f-101">Azure Stack 模組 1.4.0</span><span class="sxs-lookup"><span data-stu-id="6ec6f-101">Azure Stack Module 1.4.0</span></span>

## <a name="requirements"></a><span data-ttu-id="6ec6f-102">需求：</span><span class="sxs-lookup"><span data-stu-id="6ec6f-102">Requirements:</span></span>
<span data-ttu-id="6ec6f-103">支援的最低 Azure Stack 版本為 1804 版。</span><span class="sxs-lookup"><span data-stu-id="6ec6f-103">Minimum supported Azure Stack version is 1804.</span></span>

<span data-ttu-id="6ec6f-104">請注意：如果您使用的是舊版，請安裝版本 1.2.11</span><span class="sxs-lookup"><span data-stu-id="6ec6f-104">Note: If you are using an earlier version install version 1.2.11</span></span>

## <a name="known-issues"></a><span data-ttu-id="6ec6f-105">已知問題：</span><span class="sxs-lookup"><span data-stu-id="6ec6f-105">Known issues:</span></span>

- <span data-ttu-id="6ec6f-106">需要 Azure Stack 1803 版本才能關閉警示</span><span class="sxs-lookup"><span data-stu-id="6ec6f-106">Close Alert requires Azure Stack version 1803</span></span>
- <span data-ttu-id="6ec6f-107">New-AzsOffer 不允許建立具公用狀態的供應項目。</span><span class="sxs-lookup"><span data-stu-id="6ec6f-107">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="6ec6f-108">Set-AzsOffer Cmdlet 之後需要呼叫以變更狀態。</span><span class="sxs-lookup"><span data-stu-id="6ec6f-108">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="6ec6f-109">必須重新部署才能移除 IP 集區</span><span class="sxs-lookup"><span data-stu-id="6ec6f-109">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="6ec6f-110">重大變更</span><span class="sxs-lookup"><span data-stu-id="6ec6f-110">Breaking Changes</span></span>
<span data-ttu-id="6ec6f-111">自版本 1.3.0 以來均無重大變更。</span><span class="sxs-lookup"><span data-stu-id="6ec6f-111">There are no breaking changes from the version 1.3.0.</span></span> <span data-ttu-id="6ec6f-112">從 1.2.11 移轉的所有中斷性變更記錄於此 https://aka.ms/azspowershellmigration</span><span class="sxs-lookup"><span data-stu-id="6ec6f-112">All breaking changes migrating from 1.2.11 are documented here https://aka.ms/azspowershellmigration</span></span>

## <a name="install"></a><span data-ttu-id="6ec6f-113">Install</span><span class="sxs-lookup"><span data-stu-id="6ec6f-113">Install</span></span>
```
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2017-03-09-profile -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.4.0
```
## <a name="release-notes"></a><span data-ttu-id="6ec6f-114">版本資訊</span><span class="sxs-lookup"><span data-stu-id="6ec6f-114">Release Notes</span></span>
    * <span data-ttu-id="6ec6f-115">Azurestack 1.4.0 版本自先前版本 1.3.0 以來並無重大變更</span><span class="sxs-lookup"><span data-stu-id="6ec6f-115">Azurestack 1.4.0 version has no breaking changes from the previous release 1.3.0</span></span>
    * <span data-ttu-id="6ec6f-116">Azs.AzureBridge.Admin</span><span class="sxs-lookup"><span data-stu-id="6ec6f-116">Azs.AzureBridge.Admin</span></span>
        - <span data-ttu-id="6ec6f-117">修正在分頁結果中僅傳送單一頁面的 BUG</span><span class="sxs-lookup"><span data-stu-id="6ec6f-117">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="6ec6f-118">Azs.Backup.Admin</span><span class="sxs-lookup"><span data-stu-id="6ec6f-118">Azs.Backup.Admin</span></span>
        - <span data-ttu-id="6ec6f-119">已將 BackupFrequencyInHours、IsBackupSchedulerEnabled 及 BackupRetentionPeriodInDays 等新參數新增至 Cmdlet Set-AzsBackupShare</span><span class="sxs-lookup"><span data-stu-id="6ec6f-119">Added new parameters BackupFrequencyInHours, IsBackupSchedulerEnabled, BackupRetentionPeriodInDays in cmdlet Set-AzsBackupShare</span></span>
        - <span data-ttu-id="6ec6f-120">已新增 Cmdlet New-EncyptionKeyBase64，以協助建立加密金鑰</span><span class="sxs-lookup"><span data-stu-id="6ec6f-120">Added a cmdlet New-EncyptionKeyBase64 to facilitate creating encryption key</span></span>
        - <span data-ttu-id="6ec6f-121">修正在分頁結果中僅傳送單一頁面的 BUG</span><span class="sxs-lookup"><span data-stu-id="6ec6f-121">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="6ec6f-122">Azs.Commerce.Admin</span><span class="sxs-lookup"><span data-stu-id="6ec6f-122">Azs.Commerce.Admin</span></span>
        - <span data-ttu-id="6ec6f-123">修正在分頁結果中僅傳送單一頁面的 BUG</span><span class="sxs-lookup"><span data-stu-id="6ec6f-123">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="6ec6f-124">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="6ec6f-124">Azs.Fabric.Admin</span></span>
        - <span data-ttu-id="6ec6f-125">修正在分頁結果中僅傳送單一頁面的 BUG</span><span class="sxs-lookup"><span data-stu-id="6ec6f-125">Fix for the bug that returned only a single page in paginated results</span></span>
        - <span data-ttu-id="6ec6f-126">已新增 Cmdlet Add-AzsScaleUnitNode，讓管理員可將新的縮放單位節點新增至 azurestack 戳記</span><span class="sxs-lookup"><span data-stu-id="6ec6f-126">Added a cmdlet Add-AzsScaleUnitNode to enable admin to add new scale unit nodes to the azurestack stamp</span></span>
        - <span data-ttu-id="6ec6f-127">已新增 Cmdlet 和 New-AzsScaleUnitNodeObject，以協助建立縮放單位參數物件</span><span class="sxs-lookup"><span data-stu-id="6ec6f-127">Added cmdlet and New-AzsScaleUnitNodeObject to facilitate the creation scale unit parameter objects</span></span>
    * <span data-ttu-id="6ec6f-128">Azs.Gallery.Admin</span><span class="sxs-lookup"><span data-stu-id="6ec6f-128">Azs.Gallery.Admin</span></span>
        - <span data-ttu-id="6ec6f-129">修正在分頁結果中僅傳送單一頁面的 BUG</span><span class="sxs-lookup"><span data-stu-id="6ec6f-129">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="6ec6f-130">Azs.InfrastructureInsights.Admin</span><span class="sxs-lookup"><span data-stu-id="6ec6f-130">Azs.InfrastructureInsights.Admin</span></span>
        - <span data-ttu-id="6ec6f-131">修正在分頁結果中僅傳送單一頁面的 BUG</span><span class="sxs-lookup"><span data-stu-id="6ec6f-131">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="6ec6f-132">Azs.Network.Admin</span><span class="sxs-lookup"><span data-stu-id="6ec6f-132">Azs.Network.Admin</span></span>
        - <span data-ttu-id="6ec6f-133">修正在分頁結果中僅傳送單一頁面的 BUG</span><span class="sxs-lookup"><span data-stu-id="6ec6f-133">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="6ec6f-134">Azs.Update.Admin</span><span class="sxs-lookup"><span data-stu-id="6ec6f-134">Azs.Update.Admin</span></span>
        - <span data-ttu-id="6ec6f-135">修正在分頁結果中僅傳送單一頁面的 BUG</span><span class="sxs-lookup"><span data-stu-id="6ec6f-135">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="6ec6f-136">Azs.Subscriptions</span><span class="sxs-lookup"><span data-stu-id="6ec6f-136">Azs.Subscriptions</span></span>
        - <span data-ttu-id="6ec6f-137">修正在分頁結果中僅傳送單一頁面的 BUG</span><span class="sxs-lookup"><span data-stu-id="6ec6f-137">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="6ec6f-138">Azs.Subscriptions.Admin</span><span class="sxs-lookup"><span data-stu-id="6ec6f-138">Azs.Subscriptions.Admin</span></span>
        - <span data-ttu-id="6ec6f-139">已新增 Cmdlet Move-AzsSubscription，以便在受委派的提供者供應項目之間移動訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="6ec6f-139">Added a cmdlet Move-AzsSubscription to move subscriptions between delegated provider offers</span></span>
        - <span data-ttu-id="6ec6f-140">已新增 Cmdlet Test-AzsMoveSubscription，以便驗證該使用者訂用帳戶可以在受委派的提供者供應項目之間移動</span><span class="sxs-lookup"><span data-stu-id="6ec6f-140">Added a cmdlet Test-AzsMoveSubscription to validate that user subscriptions can be moved between delegated provider offers</span></span>
        - <span data-ttu-id="6ec6f-141">修正在分頁結果中僅傳送單一頁面的 BUG</span><span class="sxs-lookup"><span data-stu-id="6ec6f-141">Fix for the bug that returned only a single page in paginated results'</span></span>

## <a name="content"></a><span data-ttu-id="6ec6f-142">內容：</span><span class="sxs-lookup"><span data-stu-id="6ec6f-142">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="6ec6f-143">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="6ec6f-143">Azure Bridge</span></span>
<span data-ttu-id="6ec6f-144">Azure Stack AzureBridge 管理員模組的預覽版本可讓您從 Azure 同步發佈映像。</span><span class="sxs-lookup"><span data-stu-id="6ec6f-144">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="6ec6f-145">Backup </span><span class="sxs-lookup"><span data-stu-id="6ec6f-145">Backup</span></span>
<span data-ttu-id="6ec6f-146">備份管理員模組的預覽版本可允許管理員：</span><span class="sxs-lookup"><span data-stu-id="6ec6f-146">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="6ec6f-147">設定備份的儲存位置</span><span class="sxs-lookup"><span data-stu-id="6ec6f-147">Configure where backups are stored</span></span>
- <span data-ttu-id="6ec6f-148">執行備份</span><span class="sxs-lookup"><span data-stu-id="6ec6f-148">Perform backups</span></span>
- <span data-ttu-id="6ec6f-149">列出並還原已完成的備份</span><span class="sxs-lookup"><span data-stu-id="6ec6f-149">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="6ec6f-150">商業</span><span class="sxs-lookup"><span data-stu-id="6ec6f-150">Commerce</span></span>
<span data-ttu-id="6ec6f-151">Azure Stack 商務管理員模組的預覽版本可提供方法來檢視 Azure Stack 系統間的彙總資料使用量。</span><span class="sxs-lookup"><span data-stu-id="6ec6f-151">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="6ec6f-152">計算</span><span class="sxs-lookup"><span data-stu-id="6ec6f-152">Compute</span></span>
<span data-ttu-id="6ec6f-153">Azure Stack 計算管理員模組的預覽版本可提供功能來管理計算配額、平台映像和虛擬機器擴充功能。</span><span class="sxs-lookup"><span data-stu-id="6ec6f-153">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="6ec6f-154">網狀架構</span><span class="sxs-lookup"><span data-stu-id="6ec6f-154">Fabric</span></span>
<span data-ttu-id="6ec6f-155">Azure Stack 網狀架構管理員模組的預覽版本可讓系統管理員檢視和管理基礎結構元件：</span><span class="sxs-lookup"><span data-stu-id="6ec6f-155">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="6ec6f-156">縮放單位節點的停止、啟動和關閉</span><span class="sxs-lookup"><span data-stu-id="6ec6f-156">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="6ec6f-157">針對 FRU 相關活動清空和繼續縮放單位節點</span><span class="sxs-lookup"><span data-stu-id="6ec6f-157">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="6ec6f-158">縮放單位節點修復</span><span class="sxs-lookup"><span data-stu-id="6ec6f-158">Repair of scale unit nodes</span></span>
- <span data-ttu-id="6ec6f-159">基礎結構角色重新啟動</span><span class="sxs-lookup"><span data-stu-id="6ec6f-159">Restart of Infrastructure role</span></span>
- <span data-ttu-id="6ec6f-160">基礎結構角色執行個體的停止、啟動和關閉</span><span class="sxs-lookup"><span data-stu-id="6ec6f-160">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="6ec6f-161">建立新的 IP 集區</span><span class="sxs-lookup"><span data-stu-id="6ec6f-161">Create new IP Pools</span></span>

### <a name="gallery"></a><span data-ttu-id="6ec6f-162">資源庫</span><span class="sxs-lookup"><span data-stu-id="6ec6f-162">Gallery</span></span>
<span data-ttu-id="6ec6f-163">Azure Stack 資源庫管理員模組的預覽版本可提供功能來管理 Azure Stack 市集中的資源庫項目。</span><span class="sxs-lookup"><span data-stu-id="6ec6f-163">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="6ec6f-164">基礎結構深入解析</span><span class="sxs-lookup"><span data-stu-id="6ec6f-164">Infrastructure Insights</span></span>
<span data-ttu-id="6ec6f-165">基礎結構深入解析管理員模組的預覽版本可讓系統管理員：</span><span class="sxs-lookup"><span data-stu-id="6ec6f-165">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="6ec6f-166">檢視其 Azure Stack 戳記資源的健康情況</span><span class="sxs-lookup"><span data-stu-id="6ec6f-166">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="6ec6f-167">檢視和管理警示</span><span class="sxs-lookup"><span data-stu-id="6ec6f-167">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="6ec6f-168">KeyVault</span><span class="sxs-lookup"><span data-stu-id="6ec6f-168">KeyVault</span></span>
<span data-ttu-id="6ec6f-169">Azure Stack KeyVault 管理員模組的預覽版本可讓系統管理員檢視 KeyVault 配額。</span><span class="sxs-lookup"><span data-stu-id="6ec6f-169">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="6ec6f-170">網路</span><span class="sxs-lookup"><span data-stu-id="6ec6f-170">Network</span></span>
<span data-ttu-id="6ec6f-171">網路管理員模組的預覽版本可以執行：</span><span class="sxs-lookup"><span data-stu-id="6ec6f-171">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="6ec6f-172">網路配額管理</span><span class="sxs-lookup"><span data-stu-id="6ec6f-172">Management of network quotas</span></span>
- <span data-ttu-id="6ec6f-173">檢視配置的網路資源，例如公用 IP 位址、虛擬網路、負載平衡器</span><span class="sxs-lookup"><span data-stu-id="6ec6f-173">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="6ec6f-174">提供 Cmdlet 以顯示系統管理員概觀</span><span class="sxs-lookup"><span data-stu-id="6ec6f-174">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="6ec6f-175">儲存體</span><span class="sxs-lookup"><span data-stu-id="6ec6f-175">Storage</span></span>
<span data-ttu-id="6ec6f-176">Azure Stack 儲存體管理員模組的預覽版本。</span><span class="sxs-lookup"><span data-stu-id="6ec6f-176">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="6ec6f-177">在此版本中，我們提供的功能有：</span><span class="sxs-lookup"><span data-stu-id="6ec6f-177">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="6ec6f-178">管理儲存體配額</span><span class="sxs-lookup"><span data-stu-id="6ec6f-178">Manage storage quotas</span></span>
- <span data-ttu-id="6ec6f-179">記憶體回收刪除的儲存體資源</span><span class="sxs-lookup"><span data-stu-id="6ec6f-179">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="6ec6f-180">還原已刪除的儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="6ec6f-180">Restore deleted storage accounts</span></span>
- <span data-ttu-id="6ec6f-181">將容器從一個共用遷移到另一個</span><span class="sxs-lookup"><span data-stu-id="6ec6f-181">Migrate containers from one share to another</span></span>
- <span data-ttu-id="6ec6f-182">檢視個別儲存元件的相關資訊</span><span class="sxs-lookup"><span data-stu-id="6ec6f-182">View information about the individual storage components</span></span>
- <span data-ttu-id="6ec6f-183">檢視使用量和效能資訊</span><span class="sxs-lookup"><span data-stu-id="6ec6f-183">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="6ec6f-184">訂用帳戶管理員</span><span class="sxs-lookup"><span data-stu-id="6ec6f-184">Subscription Admin</span></span>
<span data-ttu-id="6ec6f-185">Azure Stack 訂用帳戶管理員模組的預覽版本。</span><span class="sxs-lookup"><span data-stu-id="6ec6f-185">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="6ec6f-186">此模組可提供功能讓系統管理員：</span><span class="sxs-lookup"><span data-stu-id="6ec6f-186">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="6ec6f-187">管理方案和供應項目</span><span class="sxs-lookup"><span data-stu-id="6ec6f-187">Manage plans and offers</span></span>
- <span data-ttu-id="6ec6f-188">檢視使用量和效能資訊</span><span class="sxs-lookup"><span data-stu-id="6ec6f-188">View usage and performance information</span></span>
- <span data-ttu-id="6ec6f-189">管理 RBAC</span><span class="sxs-lookup"><span data-stu-id="6ec6f-189">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="6ec6f-190">訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="6ec6f-190">Subscription</span></span>
<span data-ttu-id="6ec6f-191">Azure Stack 訂用帳戶模組的預覽版本。</span><span class="sxs-lookup"><span data-stu-id="6ec6f-191">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="6ec6f-192">此模組可提供功能讓使用者：</span><span class="sxs-lookup"><span data-stu-id="6ec6f-192">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="6ec6f-193">建立、刪除和更新訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="6ec6f-193">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="6ec6f-194">更新</span><span class="sxs-lookup"><span data-stu-id="6ec6f-194">Update</span></span>
<span data-ttu-id="6ec6f-195">Azure Stack 更新管理員模組的預覽版本。</span><span class="sxs-lookup"><span data-stu-id="6ec6f-195">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="6ec6f-196">在此模組中系統管理員可以：</span><span class="sxs-lookup"><span data-stu-id="6ec6f-196">In this module administrators can:</span></span>
- <span data-ttu-id="6ec6f-197">列出及安裝可用更新</span><span class="sxs-lookup"><span data-stu-id="6ec6f-197">List and install available updates</span></span>
- <span data-ttu-id="6ec6f-198">繼續中斷的更新</span><span class="sxs-lookup"><span data-stu-id="6ec6f-198">Resume interrupted updates</span></span>
- <span data-ttu-id="6ec6f-199">檢視已安裝的更新</span><span class="sxs-lookup"><span data-stu-id="6ec6f-199">View installed updates</span></span>
