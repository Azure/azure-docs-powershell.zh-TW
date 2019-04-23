---
ms.openlocfilehash: 54d7a9da878e085e90479fb229876c9be6dafd74
ms.sourcegitcommit: 89066b7c4b527357bb2024e1ad708df84c131804
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/09/2019
ms.locfileid: "59363986"
---
## <a name="170---april-2019"></a><span data-ttu-id="42d2a-101">1.7.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="42d2a-101">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="42d2a-102">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="42d2a-102">Highlights since the last major release</span></span>
* <span data-ttu-id="42d2a-103">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="42d2a-103">General availability of `Az` module</span></span>
* <span data-ttu-id="42d2a-104">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="42d2a-104">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="42d2a-105">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="42d2a-105">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="42d2a-106">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="42d2a-106">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="42d2a-107">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="42d2a-107">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="42d2a-108">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="42d2a-108">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="42d2a-109">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="42d2a-109">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="42d2a-110">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42d2a-110">Az.Accounts</span></span>
* <span data-ttu-id="42d2a-111">已將 Add-AzEnvironment 和 Set-AzEnvironment 更新為接受 AzureAnalysisServicesEndpointResourceId 參數</span><span class="sxs-lookup"><span data-stu-id="42d2a-111">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="42d2a-112">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="42d2a-112">Az.AnalysisServices</span></span>
* <span data-ttu-id="42d2a-113">在 dataplane Cmdlet 中使用 ServiceClient，並移除原始的驗證邏輯</span><span class="sxs-lookup"><span data-stu-id="42d2a-113">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="42d2a-114">讓 Add-AzureASAccount 成為 Connect-AzAccount 的包裝函式，以避免重大變更</span><span class="sxs-lookup"><span data-stu-id="42d2a-114">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="42d2a-115">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="42d2a-115">Az.Automation</span></span>
* <span data-ttu-id="42d2a-116">修正 Inclusions 的 New-AzAutomationSoftwareUpdateConfiguration Cmdlet 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="42d2a-116">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="42d2a-117">現在，IncludedKbNumber 和 IncludedPackageNameMask 參數應會正常運作。</span><span class="sxs-lookup"><span data-stu-id="42d2a-117">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="42d2a-118">修正 Azure 自動化更新管理動態群組的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="42d2a-118">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42d2a-119">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42d2a-119">Az.Compute</span></span>
* <span data-ttu-id="42d2a-120">將 HyperVGeneration 參數新增至 New-AzDiskConfig 和 New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="42d2a-120">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="42d2a-121">允許使用其他租用戶的資源庫映像來建立 VM。</span><span class="sxs-lookup"><span data-stu-id="42d2a-121">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="42d2a-122">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="42d2a-122">Az.ContainerInstance</span></span>
* <span data-ttu-id="42d2a-123">已修正 New-AzContainerGroup 的 -Command 參數問題，其加入了尾端空白的引數</span><span class="sxs-lookup"><span data-stu-id="42d2a-123">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="42d2a-124">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="42d2a-124">Az.DataFactory</span></span>
* <span data-ttu-id="42d2a-125">已將 ADF .Net SDK 版本更新為 3.0.2</span><span class="sxs-lookup"><span data-stu-id="42d2a-125">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="42d2a-126">已透過 RepoConfiguration 相關設定的額外參數來更新 Set-AzDataFactoryV2 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="42d2a-126">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="42d2a-127">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42d2a-127">Az.Resources</span></span>
* <span data-ttu-id="42d2a-128">改善提供 '-ResourceId' 或 '-ResourceGroupName'、'-Name' 和 '-ResourceType' 參數時，'Get-AzResource' 的提供者處理</span><span class="sxs-lookup"><span data-stu-id="42d2a-128">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="42d2a-129">改善 'Test-AzDeployment' 和 'Test-AzResourceGroupDeployment' 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="42d2a-129">Improve error handling for for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="42d2a-130">處理部署驗證外擲回的錯誤，並改為將其包含在命令輸出中</span><span class="sxs-lookup"><span data-stu-id="42d2a-130">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="42d2a-131">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="42d2a-131">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="42d2a-132">將 '-IgnoreDynamicParameters' 切換參數新增至部署 Cmdlet 的集合，以略過指令碼和作業案例中的提示</span><span class="sxs-lookup"><span data-stu-id="42d2a-132">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="42d2a-133">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="42d2a-133">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="42d2a-134">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42d2a-134">Az.Sql</span></span>
* <span data-ttu-id="42d2a-135">支援資料庫的資料分類。</span><span class="sxs-lookup"><span data-stu-id="42d2a-135">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="42d2a-136">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="42d2a-136">Az.Storage</span></span>
* <span data-ttu-id="42d2a-137">報告以參數 -UseConnectedAccount 建立儲存體內容時的詳細錯誤 (未登入 Azure 帳戶)</span><span class="sxs-lookup"><span data-stu-id="42d2a-137">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="42d2a-138">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="42d2a-138">New-AzStorageContext</span></span>
* <span data-ttu-id="42d2a-139">支援以管理平面 API 管理指定儲存體帳戶的 Blob 服務屬性</span><span class="sxs-lookup"><span data-stu-id="42d2a-139">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="42d2a-140">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="42d2a-140">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="42d2a-141">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="42d2a-141">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="42d2a-142">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="42d2a-142">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="42d2a-143">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="42d2a-143">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="42d2a-144">Blob 的 -AsJob 支援和檔案上傳及下載 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="42d2a-144">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="42d2a-145">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="42d2a-145">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="42d2a-146">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="42d2a-146">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="42d2a-147">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="42d2a-147">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="42d2a-148">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="42d2a-148">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="42d2a-149">1.6.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="42d2a-149">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="42d2a-150">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="42d2a-150">Highlights since the last major release</span></span>
* <span data-ttu-id="42d2a-151">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="42d2a-151">General availability of `Az` module</span></span>
* <span data-ttu-id="42d2a-152">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="42d2a-152">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="42d2a-153">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="42d2a-153">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="42d2a-154">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="42d2a-154">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="42d2a-155">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="42d2a-155">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="42d2a-156">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="42d2a-156">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="42d2a-157">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="42d2a-157">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="42d2a-158">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="42d2a-158">Az.Automation</span></span>
* <span data-ttu-id="42d2a-159">Azure 自動化更新管理變更為支援下列各項新功能：</span><span class="sxs-lookup"><span data-stu-id="42d2a-159">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="42d2a-160">動態分組</span><span class="sxs-lookup"><span data-stu-id="42d2a-160">Dynamic grouping</span></span>
    * <span data-ttu-id="42d2a-161">預先貼文指令碼</span><span class="sxs-lookup"><span data-stu-id="42d2a-161">Pre-Post script</span></span>
    * <span data-ttu-id="42d2a-162">重新啟動設定</span><span class="sxs-lookup"><span data-stu-id="42d2a-162">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42d2a-163">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42d2a-163">Az.Compute</span></span>
* <span data-ttu-id="42d2a-164">修正 Get-AzVmBootDiagnosticsData 中路徑解析的問題</span><span class="sxs-lookup"><span data-stu-id="42d2a-164">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="42d2a-165">將計算用戶端程式庫更新為 25.0.0。</span><span class="sxs-lookup"><span data-stu-id="42d2a-165">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="42d2a-166">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="42d2a-166">Az.KeyVault</span></span>
* <span data-ttu-id="42d2a-167">新增了 KeyVault Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="42d2a-167">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="42d2a-168">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42d2a-168">Az.Network</span></span>
* <span data-ttu-id="42d2a-169">新增適用於 Azure 防火牆的威脅智慧支援</span><span class="sxs-lookup"><span data-stu-id="42d2a-169">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="42d2a-170">新增應用程式閘道防火牆原則頂層資源和自訂規則</span><span class="sxs-lookup"><span data-stu-id="42d2a-170">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="42d2a-171">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="42d2a-171">Az.RecoveryServices</span></span>
* <span data-ttu-id="42d2a-172">已在 Azure VM 原則中新增了 SnapshotRetentionInDays 以支援 Instant RP</span><span class="sxs-lookup"><span data-stu-id="42d2a-172">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="42d2a-173">新增了取消註冊容器的管道支援</span><span class="sxs-lookup"><span data-stu-id="42d2a-173">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="42d2a-174">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42d2a-174">Az.Resources</span></span>
* <span data-ttu-id="42d2a-175">更新適用於 Get-AzResource 和 Get-AzResourceGroup 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="42d2a-175">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="42d2a-176">更新在對 ARM 進行一般呼叫時使用的認證</span><span class="sxs-lookup"><span data-stu-id="42d2a-176">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="42d2a-177">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42d2a-177">Az.Sql</span></span>
* <span data-ttu-id="42d2a-178">變更了 DetectionType 到 string[] 的威脅偵測 Cmdlet 參數，以便在新增了 DetectionTypes 時具備更進一步的保障，同時支援自動完成功能。</span><span class="sxs-lookup"><span data-stu-id="42d2a-178">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="42d2a-179">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="42d2a-179">Az.Storage</span></span>
* <span data-ttu-id="42d2a-180">支援儲存體帳戶上的 Get/Set/Remove 管理原則</span><span class="sxs-lookup"><span data-stu-id="42d2a-180">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="42d2a-181">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="42d2a-181">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="42d2a-182">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="42d2a-182">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="42d2a-183">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="42d2a-183">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="42d2a-184">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="42d2a-184">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="42d2a-185">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="42d2a-185">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="42d2a-186">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="42d2a-186">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="42d2a-187">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="42d2a-187">Az.Websites</span></span>
* <span data-ttu-id="42d2a-188">修正 ARM 範本錯誤 (bug)，防正使用 'New-AzWebApp -IncludeSourceWebAppSlots' 時發生中斷複製所有位置的情況</span><span class="sxs-lookup"><span data-stu-id="42d2a-188">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="42d2a-189">1.5.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="42d2a-189">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="42d2a-190">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42d2a-190">Az.Accounts</span></span>
* <span data-ttu-id="42d2a-191">新增 'Register-AzModule' 命令以支援 AutoRest 產生的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="42d2a-191">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="42d2a-192">適用於 Connect-AzAccount 的更新範例</span><span class="sxs-lookup"><span data-stu-id="42d2a-192">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="42d2a-193">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="42d2a-193">Az.Automation</span></span>
* <span data-ttu-id="42d2a-194">修正了在數個 Azure 自動化 Cmdlet 中擷取某些每月排程時發生的問題</span><span class="sxs-lookup"><span data-stu-id="42d2a-194">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="42d2a-195">修正 Get-AzAutomationDscNode 只會傳回前 20 個節點的問題。</span><span class="sxs-lookup"><span data-stu-id="42d2a-195">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="42d2a-196">現在可以傳回所有節點</span><span class="sxs-lookup"><span data-stu-id="42d2a-196">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="42d2a-197">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="42d2a-197">Az.Cdn</span></span>
* <span data-ttu-id="42d2a-198">新增了 Enable/Disable Custom Domain Https 的 Powershell Cmdlet 並取代了舊的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="42d2a-198">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42d2a-199">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42d2a-199">Az.Compute</span></span>
* <span data-ttu-id="42d2a-200">新增 Get Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="42d2a-200">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="42d2a-201">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="42d2a-201">Az.DataFactory</span></span>
* <span data-ttu-id="42d2a-202">已將 ADF .Net SDK 版本更新為 3.0.1</span><span class="sxs-lookup"><span data-stu-id="42d2a-202">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="42d2a-203">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="42d2a-203">Az.LogicApp</span></span>
* <span data-ttu-id="42d2a-204">修正 ListWorkflows，僅擷取結果的第一頁資料</span><span class="sxs-lookup"><span data-stu-id="42d2a-204">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="42d2a-205">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42d2a-205">Az.Network</span></span>
* <span data-ttu-id="42d2a-206">新增 Network Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="42d2a-206">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="42d2a-207">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="42d2a-207">Az.RecoveryServices</span></span>
* <span data-ttu-id="42d2a-208">新增了Azure VM 中 SQL 伺服器的支援</span><span class="sxs-lookup"><span data-stu-id="42d2a-208">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="42d2a-209">SDK 更新</span><span class="sxs-lookup"><span data-stu-id="42d2a-209">SDK Update</span></span>
* <span data-ttu-id="42d2a-210">移除了 Get-ProtectableItem 中的 VMappContainer 檢查</span><span class="sxs-lookup"><span data-stu-id="42d2a-210">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="42d2a-211">新增了 Get-ProtectableItem 的 Name 和 ServerName 參數</span><span class="sxs-lookup"><span data-stu-id="42d2a-211">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="42d2a-212">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42d2a-212">Az.Resources</span></span>
* <span data-ttu-id="42d2a-213">將 `-TemplateObject` 參數新增至部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="42d2a-213">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="42d2a-214">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="42d2a-214">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="42d2a-215">修正將 `Get-AzResource` 結果輸送至下列項目時的問題：</span><span class="sxs-lookup"><span data-stu-id="42d2a-215">Fix issue when piping the result of `Get-AzResource` to</span></span> `Set-AzResource`
    - <span data-ttu-id="42d2a-216">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="42d2a-216">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="42d2a-217">修正在執行下列項目時，JSON 資料類型變更的問題：</span><span class="sxs-lookup"><span data-stu-id="42d2a-217">Fix issue with JSON data type change when running</span></span> `Set-AzResource`
    - <span data-ttu-id="42d2a-218">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="42d2a-218">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="42d2a-219">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42d2a-219">Az.Sql</span></span>
* <span data-ttu-id="42d2a-220">更新 AuditingEndpointsCommunicator。</span><span class="sxs-lookup"><span data-stu-id="42d2a-220">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="42d2a-221">修正在建立新診斷設定時邊緣案例的行為。</span><span class="sxs-lookup"><span data-stu-id="42d2a-221">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="42d2a-222">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="42d2a-222">Az.Storage</span></span>
* <span data-ttu-id="42d2a-223">在建立儲存體帳戶時支援 BlockBlobStorage 種類       - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="42d2a-223">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="42d2a-224">1.4.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="42d2a-224">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="42d2a-225">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="42d2a-225">Az.AnalysisServices</span></span>
* <span data-ttu-id="42d2a-226">即將淘汰 AddAzureASAccount Cmdlet</span><span class="sxs-lookup"><span data-stu-id="42d2a-226">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="42d2a-227">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="42d2a-227">Az.Automation</span></span>
* <span data-ttu-id="42d2a-228">更新 Import-AzAutomationDscNodeConfiguration 的說明</span><span class="sxs-lookup"><span data-stu-id="42d2a-228">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="42d2a-229">已將設定名稱驗證新增至 Import-AzAutomationDscConfiguration Cmdlet</span><span class="sxs-lookup"><span data-stu-id="42d2a-229">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="42d2a-230">已改善 Import-AzAutomationDscConfiguration Cmdlet 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="42d2a-230">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="42d2a-231">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="42d2a-231">Az.CognitiveServices</span></span>
* <span data-ttu-id="42d2a-232">已將 CustomSubdomainName 新增為 New-AzCognitiveServicesAccount 的新選擇性參數，用來指定資源的子網域。</span><span class="sxs-lookup"><span data-stu-id="42d2a-232">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42d2a-233">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42d2a-233">Az.Compute</span></span>
* <span data-ttu-id="42d2a-234">修正識別碼參數集問題</span><span class="sxs-lookup"><span data-stu-id="42d2a-234">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="42d2a-235">如果未提供 Name 參數，更新 Get-AzVMExtension 以列出所有已安裝的延伸模組</span><span class="sxs-lookup"><span data-stu-id="42d2a-235">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="42d2a-236">將標記和 ResourceId 參數新增至 Update-AzImage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="42d2a-236">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="42d2a-237">沒有執行個體識別碼的 Get-AzVmssVM，和具有 InstanceView 者可以透過執行個體檢視列出 VMSS VM。</span><span class="sxs-lookup"><span data-stu-id="42d2a-237">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="42d2a-238">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="42d2a-238">Az.DataLakeStore</span></span>
* <span data-ttu-id="42d2a-239">為 ADL 刪除的項目列舉和還原新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="42d2a-239">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="42d2a-240">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="42d2a-240">Az.EventHub</span></span>
* <span data-ttu-id="42d2a-241">在 Eventhub 的 CaptureDescription 類別中，已將新的布林值屬性 SkipEmptyArchives 新增至 Skip Empty Archives</span><span class="sxs-lookup"><span data-stu-id="42d2a-241">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="42d2a-242">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="42d2a-242">Az.KeyVault</span></span>
* <span data-ttu-id="42d2a-243">修正 Set-AzKeyVaultSecret 的標記</span><span class="sxs-lookup"><span data-stu-id="42d2a-243">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="42d2a-244">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="42d2a-244">Az.LogicApp</span></span>
* <span data-ttu-id="42d2a-245">在整合帳戶的基本 sku 新增</span><span class="sxs-lookup"><span data-stu-id="42d2a-245">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="42d2a-246">在 XSLT 2.0、XSLT 3.0 和 Liquid 對應類型中新增</span><span class="sxs-lookup"><span data-stu-id="42d2a-246">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="42d2a-247">整合帳戶組件的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="42d2a-247">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="42d2a-248">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="42d2a-248">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="42d2a-249">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="42d2a-249">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="42d2a-250">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="42d2a-250">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="42d2a-251">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="42d2a-251">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="42d2a-252">整合帳戶批次設定的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="42d2a-252">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="42d2a-253">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="42d2a-253">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="42d2a-254">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="42d2a-254">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="42d2a-255">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="42d2a-255">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="42d2a-256">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="42d2a-256">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="42d2a-257">將邏輯應用程式 SDK 更新至 4.1.0 版</span><span class="sxs-lookup"><span data-stu-id="42d2a-257">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="42d2a-258">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="42d2a-258">Az.Monitor</span></span>
* <span data-ttu-id="42d2a-259">更新 Get-AzMetric 的說明</span><span class="sxs-lookup"><span data-stu-id="42d2a-259">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="42d2a-260">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42d2a-260">Az.Network</span></span>
* <span data-ttu-id="42d2a-261">更新 Add-AzApplicationGatewayCustomError 的說明範例</span><span class="sxs-lookup"><span data-stu-id="42d2a-261">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="42d2a-262">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="42d2a-262">Az.OperationalInsights</span></span>
* <span data-ttu-id="42d2a-263">取得 ApplicationInsights 與新資料來源的其他支援。</span><span class="sxs-lookup"><span data-stu-id="42d2a-263">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="42d2a-264">已新增新 'ApplicationInsights' 類型，以支援指定工作區的取得特定和取得所有 ApplicationInsights 資料來源。</span><span class="sxs-lookup"><span data-stu-id="42d2a-264">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="42d2a-265">已新增 New-AzOperationalInsightsApplicationInsightsDataSource Cmdlet 用來建立資料來源，透過指定的 Application-Insights 資源參數：訂用帳戶識別碼、resourceGroupName 和名稱。</span><span class="sxs-lookup"><span data-stu-id="42d2a-265">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="42d2a-266">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42d2a-266">Az.Resources</span></span>
* <span data-ttu-id="42d2a-267">修正 https://github.com/Azure/azure-powershell/issues/8166 的問題</span><span class="sxs-lookup"><span data-stu-id="42d2a-267">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="42d2a-268">修正 https://github.com/Azure/azure-powershell/issues/8235 的問題</span><span class="sxs-lookup"><span data-stu-id="42d2a-268">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="42d2a-269">修正 https://github.com/Azure/azure-powershell/issues/6219 的問題</span><span class="sxs-lookup"><span data-stu-id="42d2a-269">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="42d2a-270">修正防止重複建立 KeyCredentials 的錯誤</span><span class="sxs-lookup"><span data-stu-id="42d2a-270">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="42d2a-271">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42d2a-271">Az.Sql</span></span>
* <span data-ttu-id="42d2a-272">新增 SQL DB 超大規模資料庫層支援</span><span class="sxs-lookup"><span data-stu-id="42d2a-272">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="42d2a-273">已修正以下錯誤：由於在還原要求中設定非必要屬性造成還原失敗</span><span class="sxs-lookup"><span data-stu-id="42d2a-273">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="42d2a-274">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="42d2a-274">Az.Websites</span></span>
* <span data-ttu-id="42d2a-275">Get-AzWebAppSlotMetrics 中的正確範例</span><span class="sxs-lookup"><span data-stu-id="42d2a-275">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="42d2a-276">1.3.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="42d2a-276">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="42d2a-277">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42d2a-277">Az.Accounts</span></span>
* <span data-ttu-id="42d2a-278">更新至最新版本的 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="42d2a-278">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="42d2a-279">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="42d2a-279">Az.AnalysisServices</span></span>
<span data-ttu-id="42d2a-280">Az.AnalysisServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="42d2a-280">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42d2a-281">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42d2a-281">Az.Compute</span></span>
* <span data-ttu-id="42d2a-282">AEM 延伸模組：新增對 UltraSSD 和 P60、P70 和 P80 磁碟的支援</span><span class="sxs-lookup"><span data-stu-id="42d2a-282">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="42d2a-283">更新 AzVMBootDiagnostics 的說明描述</span><span class="sxs-lookup"><span data-stu-id="42d2a-283">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="42d2a-284">更新 Update-AzImage 的說明描述和範例</span><span class="sxs-lookup"><span data-stu-id="42d2a-284">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="42d2a-285">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="42d2a-285">Az.RecoveryServices</span></span>
<span data-ttu-id="42d2a-286">Az.RecoveryServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="42d2a-286">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="42d2a-287">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42d2a-287">Az.Resources</span></span>
* <span data-ttu-id="42d2a-288">修正資源群組標記</span><span class="sxs-lookup"><span data-stu-id="42d2a-288">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="42d2a-289">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="42d2a-289">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="42d2a-290">修正 `Get-AzureRmRoleAssignment`不遵守 -ErrorAction 的問題</span><span class="sxs-lookup"><span data-stu-id="42d2a-290">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="42d2a-291">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="42d2a-291">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="42d2a-292">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42d2a-292">Az.Sql</span></span>
* <span data-ttu-id="42d2a-293">新增 Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="42d2a-293">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="42d2a-294">修正執行 SQL Cmdlet 時無法登入 Azure 帳戶會導致 nullref 例外狀況的問題</span><span class="sxs-lookup"><span data-stu-id="42d2a-294">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="42d2a-295">已修正 Get AzSqlCapability 中的 Null 參考例外狀況</span><span class="sxs-lookup"><span data-stu-id="42d2a-295">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="42d2a-296">1.2.1 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="42d2a-296">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="42d2a-297">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42d2a-297">Az.Accounts</span></span>
* <span data-ttu-id="42d2a-298">包含正確驗證版本的發行</span><span class="sxs-lookup"><span data-stu-id="42d2a-298">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="42d2a-299">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="42d2a-299">Az.AnalysisServices</span></span>
* <span data-ttu-id="42d2a-300">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="42d2a-300">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="42d2a-301">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="42d2a-301">Az.RecoveryServices</span></span>
* <span data-ttu-id="42d2a-302">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="42d2a-302">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="42d2a-303">1.2.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="42d2a-303">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="42d2a-304">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42d2a-304">Az.Accounts</span></span>
* <span data-ttu-id="42d2a-305">僅新增 Windows PowerShell 5.1 互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="42d2a-305">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="42d2a-306">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="42d2a-306">Update incorrect online help URLs</span></span>
* <span data-ttu-id="42d2a-307">在 PS Core 中新增 Uninstall-AzureRm 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="42d2a-307">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="42d2a-308">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="42d2a-308">Az.Aks</span></span>
* <span data-ttu-id="42d2a-309">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="42d2a-309">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="42d2a-310">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="42d2a-310">Az.Automation</span></span>
* <span data-ttu-id="42d2a-311">已新增 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="42d2a-311">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="42d2a-312">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="42d2a-312">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="42d2a-313">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="42d2a-313">Az.Cdn</span></span>
* <span data-ttu-id="42d2a-314">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="42d2a-314">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42d2a-315">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42d2a-315">Az.Compute</span></span>
* <span data-ttu-id="42d2a-316">新增 Invoke-AzVMReimage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="42d2a-316">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="42d2a-317">將 TempDisk 參數新增至 Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="42d2a-317">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="42d2a-318">修正 New-AzVM 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="42d2a-318">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="42d2a-319">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="42d2a-319">Az.ContainerRegistry</span></span>
* <span data-ttu-id="42d2a-320">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="42d2a-320">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="42d2a-321">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="42d2a-321">Az.DataFactory</span></span>
* <span data-ttu-id="42d2a-322">已將 ADF .Net SDK 版本更新為 3.0.0</span><span class="sxs-lookup"><span data-stu-id="42d2a-322">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="42d2a-323">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="42d2a-323">Az.DataLakeStore</span></span>
* <span data-ttu-id="42d2a-324">修正使用 MSI 時 ADLS 端點的問題</span><span class="sxs-lookup"><span data-stu-id="42d2a-324">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="42d2a-325">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="42d2a-325">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="42d2a-326">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="42d2a-326">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="42d2a-327">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="42d2a-327">Az.IotHub</span></span>
* <span data-ttu-id="42d2a-328">將編碼格式新增至 Add-IotHubRoutingEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="42d2a-328">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="42d2a-329">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="42d2a-329">Az.KeyVault</span></span>
* <span data-ttu-id="42d2a-330">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="42d2a-330">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="42d2a-331">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42d2a-331">Az.Network</span></span>
* <span data-ttu-id="42d2a-332">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="42d2a-332">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="42d2a-333">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42d2a-333">Az.Resources</span></span>
* <span data-ttu-id="42d2a-334">修正 「New-AzADAppCredential」和「New-AzADSpCredential」參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="42d2a-334">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="42d2a-335">修正「-TemplateFile」參數路徑並未在執行資源群組部署 Cmdlet 前解析的問題</span><span class="sxs-lookup"><span data-stu-id="42d2a-335">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="42d2a-336">Az.Resources：正確的 New-AzureRmPolicyDefinition -Mode 預設值文件</span><span class="sxs-lookup"><span data-stu-id="42d2a-336">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="42d2a-337">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/7522 的問題</span><span class="sxs-lookup"><span data-stu-id="42d2a-337">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="42d2a-338">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/5747 的問題</span><span class="sxs-lookup"><span data-stu-id="42d2a-338">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="42d2a-339">修正「PSResourceGroupDeployment」物件格式化的問題</span><span class="sxs-lookup"><span data-stu-id="42d2a-339">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="42d2a-340">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="42d2a-340">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="42d2a-341">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="42d2a-341">Az.ServiceFabric</span></span>
* <span data-ttu-id="42d2a-342">將憑證新增到 VMSS 模型但擲回例外狀況時復原，以修正錯誤： https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="42d2a-342">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="42d2a-343">修正某些錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="42d2a-343">Fix some error messages.</span></span>
* <span data-ttu-id="42d2a-344">修正使用預設 ARM 範本為並未移轉至 Az 的 New-AzServiceFabriCluster 建立叢集的問題。</span><span class="sxs-lookup"><span data-stu-id="42d2a-344">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="42d2a-345">檢查延伸模組中的叢集識別碼，修正只將叢集/應用程式憑證新增至對應至該叢集的 VM 擴展集中的問題。</span><span class="sxs-lookup"><span data-stu-id="42d2a-345">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="42d2a-346">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="42d2a-346">Az.SignalR</span></span>
* <span data-ttu-id="42d2a-347">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="42d2a-347">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="42d2a-348">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42d2a-348">Az.Sql</span></span>
* <span data-ttu-id="42d2a-349">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="42d2a-349">Update incorrect online help URLs</span></span>
* <span data-ttu-id="42d2a-350">更新了 LicenseType 參數的描述並新增了可能的值</span><span class="sxs-lookup"><span data-stu-id="42d2a-350">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="42d2a-351">修正當更新受控執行個體身分識別僅為已更新屬性時無法運作的問題</span><span class="sxs-lookup"><span data-stu-id="42d2a-351">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="42d2a-352">支援在受控執行個體上的自訂定序</span><span class="sxs-lookup"><span data-stu-id="42d2a-352">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="42d2a-353">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="42d2a-353">Az.Storage</span></span>
* <span data-ttu-id="42d2a-354">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="42d2a-354">Update incorrect online help URLs</span></span>
* <span data-ttu-id="42d2a-355">在進階儲存體帳戶上取得/設定傳統記錄/計量時提供詳細錯誤訊息，因為進階儲存體帳戶不支援傳統記錄/計量。</span><span class="sxs-lookup"><span data-stu-id="42d2a-355">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="42d2a-356">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="42d2a-356">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="42d2a-357">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="42d2a-357">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="42d2a-358">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="42d2a-358">Az.TrafficManager</span></span>
* <span data-ttu-id="42d2a-359">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="42d2a-359">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="42d2a-360">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="42d2a-360">Az.Websites</span></span>
* <span data-ttu-id="42d2a-361">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="42d2a-361">Update incorrect online help URLs</span></span>
* <span data-ttu-id="42d2a-362">修正「New-AzWebAppSSLBinding」，以便在應用程式於 ASE 上託管時將憑證上傳到正確的資源群組及位置。</span><span class="sxs-lookup"><span data-stu-id="42d2a-362">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="42d2a-363">修正「New-AzWebAppSSLBinding」以便在將 SSL 憑證繫結至應用程式時不要覆寫標記</span><span class="sxs-lookup"><span data-stu-id="42d2a-363">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="42d2a-364">1.1.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="42d2a-364">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="42d2a-365">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42d2a-365">Az.Accounts</span></span>
* <span data-ttu-id="42d2a-366">將 'Local' 範圍新增至 Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="42d2a-366">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42d2a-367">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42d2a-367">Az.Compute</span></span>
* <span data-ttu-id="42d2a-368">在 Restart/Start/Stop/Remove/Set-AzVM 和 Save-AzVMImage 的識別碼參數集中，名稱現在為選用項目</span><span class="sxs-lookup"><span data-stu-id="42d2a-368">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="42d2a-369">已更新說明檔案中的識別碼描述</span><span class="sxs-lookup"><span data-stu-id="42d2a-369">Updated the description of ID in help files</span></span>
* <span data-ttu-id="42d2a-370">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="42d2a-370">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="42d2a-371">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="42d2a-371">Az.DataLakeStore</span></span>
* <span data-ttu-id="42d2a-372">將資料平面的 SDK 版本更新為 1.1.14，以修正 SDK 問題。</span><span class="sxs-lookup"><span data-stu-id="42d2a-372">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="42d2a-373">針對 getfilestatus 和 liststatus 修正 acesstime 和 modificationtime 的負值處理、修正非同步取消權杖</span><span class="sxs-lookup"><span data-stu-id="42d2a-373">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="42d2a-374">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="42d2a-374">Az.EventGrid</span></span>
* <span data-ttu-id="42d2a-375">已更新為使用 2019-01-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="42d2a-375">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="42d2a-376">更新下列 Cmdlet 來支援 2019-01-01 API 版本中的新案例</span><span class="sxs-lookup"><span data-stu-id="42d2a-376">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="42d2a-377">New-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="42d2a-377">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="42d2a-378">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="42d2a-378">Event Time-To-Live,</span></span>
        - <span data-ttu-id="42d2a-379">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="42d2a-379">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="42d2a-380">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="42d2a-380">Dead letter endpoint.</span></span>
    - <span data-ttu-id="42d2a-381">Update-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="42d2a-381">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="42d2a-382">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="42d2a-382">Event Time-To-Live,</span></span>
        - <span data-ttu-id="42d2a-383">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="42d2a-383">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="42d2a-384">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="42d2a-384">Dead letter endpoint.</span></span>
* <span data-ttu-id="42d2a-385">針對 New-AzureRmEventGridSubscription 和 Update-AzureRmEventGridSubscription Cmdlet 中的 EndpointType 選項新增列舉值 (namely、storageQueue 和 hybridConnection)。</span><span class="sxs-lookup"><span data-stu-id="42d2a-385">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="42d2a-386">如果預期需要使用者手動建立或更新事件訂閱，則顯示警告訊息。</span><span class="sxs-lookup"><span data-stu-id="42d2a-386">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="42d2a-387">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="42d2a-387">Az.IotHub</span></span>
* <span data-ttu-id="42d2a-388">已更新至最新版本的 IotHub SDK</span><span class="sxs-lookup"><span data-stu-id="42d2a-388">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="42d2a-389">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="42d2a-389">Az.LogicApp</span></span>
* <span data-ttu-id="42d2a-390">Get-AzLogicApp 會列出所有項目，無須指定名稱</span><span class="sxs-lookup"><span data-stu-id="42d2a-390">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="42d2a-391">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42d2a-391">Az.Resources</span></span>
* <span data-ttu-id="42d2a-392">修正為 'Get-AzResource' 提供 '-ODataQuery' 和 '-ResourceId' 參數時的參數集問題</span><span class="sxs-lookup"><span data-stu-id="42d2a-392">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="42d2a-393">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="42d2a-393">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="42d2a-394">修正 New/Set-AzPolicyDefinition 中的 -Custom 參數處理</span><span class="sxs-lookup"><span data-stu-id="42d2a-394">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="42d2a-395">修正 New-AzDeployment 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="42d2a-395">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="42d2a-396">使 '-MailNickname' 參數成為 'New-AzADUser' 的必要項目</span><span class="sxs-lookup"><span data-stu-id="42d2a-396">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="42d2a-397">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="42d2a-397">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="42d2a-398">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="42d2a-398">Az.SignalR</span></span>
* <span data-ttu-id="42d2a-399">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="42d2a-399">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="42d2a-400">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42d2a-400">Az.Sql</span></span>
* <span data-ttu-id="42d2a-401">將儲存體管理用戶端相依性轉換為一般的 SDK 實作。</span><span class="sxs-lookup"><span data-stu-id="42d2a-401">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="42d2a-402">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="42d2a-402">Az.Storage</span></span>
* <span data-ttu-id="42d2a-403">使用 Sas 權杖、OAuth 或匿名來建立儲存體內容的 StorageAccountName 時，將其設定為實際的儲存體帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="42d2a-403">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="42d2a-404">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="42d2a-404">New-AzStorageContext</span></span>
* <span data-ttu-id="42d2a-405">使用 '-FullUri' 參數建立 Blob 快照集物件的 Sas 權杖、將傳回的 Uri 修正為快照集 Uri</span><span class="sxs-lookup"><span data-stu-id="42d2a-405">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="42d2a-406">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="42d2a-406">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="42d2a-407">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="42d2a-407">Az.Websites</span></span>
* <span data-ttu-id="42d2a-408">修正 'Get-AzDeletedWebApp' 中的日期剖析錯誤</span><span class="sxs-lookup"><span data-stu-id="42d2a-408">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="42d2a-409">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="42d2a-409">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="42d2a-410">1.0.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="42d2a-410">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="42d2a-411">一般</span><span class="sxs-lookup"><span data-stu-id="42d2a-411">General</span></span>

- <span data-ttu-id="42d2a-412">Az 模組正式運作</span><span class="sxs-lookup"><span data-stu-id="42d2a-412">General Availability of Az Module</span></span>
- <span data-ttu-id="42d2a-413">每個模組的線上說明</span><span class="sxs-lookup"><span data-stu-id="42d2a-413">Online help for each module</span></span>
- <span data-ttu-id="42d2a-414">如需詳細資訊和藍圖，請參閱 [Az 公告頁面](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="42d2a-414">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="42d2a-415">如需從 AzureRM 遷移的相關資訊，請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="42d2a-415">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="42d2a-416">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42d2a-416">Az.Accounts</span></span>
- <span data-ttu-id="42d2a-417">已從 Az.Profile 變更</span><span class="sxs-lookup"><span data-stu-id="42d2a-417">Changed from Az.Profile</span></span>
- <span data-ttu-id="42d2a-418">設定檔和內容類型有固定的資料表格式</span><span class="sxs-lookup"><span data-stu-id="42d2a-418">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="42d2a-419">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="42d2a-419">Az.ApiManagement</span></span>
- <span data-ttu-id="42d2a-420">#7002 的修正</span><span class="sxs-lookup"><span data-stu-id="42d2a-420">Fixes for #7002</span></span>
- <span data-ttu-id="42d2a-421">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="42d2a-421">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="42d2a-422">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="42d2a-422">Az.Batch</span></span>
- <span data-ttu-id="42d2a-423">已新增功能，可透過 `PSComputeNode` 上新的 `NodeAgentInformation` 屬性，查看集區中每個 VM 上所執行的 Azure Batch 節點代理程式是哪個版本。</span><span class="sxs-lookup"><span data-stu-id="42d2a-423">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="42d2a-424">`PSDataDisk` 的 `Caching` 預設值現在為 `ReadWrite` 而非 `None`。</span><span class="sxs-lookup"><span data-stu-id="42d2a-424">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="42d2a-425">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="42d2a-425">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="42d2a-426">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="42d2a-426">Az.Billing</span></span>
- <span data-ttu-id="42d2a-427">結合 Billing、Consumption 和 UsageAggregates Cmdlet，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="42d2a-427">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="42d2a-428">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="42d2a-428">Az.CognitivServices</span></span>
- <span data-ttu-id="42d2a-429">針對 New-AzureRmCognitiveServicesAccount 作業上可用的 SkuName 和 Typem 新增完成器</span><span class="sxs-lookup"><span data-stu-id="42d2a-429">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="42d2a-430">已從 Get-AzCognitiveServicesAccountSkus 移除 GetSkusWithAccountParamSetName 參數集</span><span class="sxs-lookup"><span data-stu-id="42d2a-430">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="42d2a-431">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="42d2a-431">Az.ContainerInstance</span></span>
- <span data-ttu-id="42d2a-432">已新增 ManagedIdentity 支援</span><span class="sxs-lookup"><span data-stu-id="42d2a-432">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="42d2a-433">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="42d2a-433">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="42d2a-434">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="42d2a-434">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="42d2a-435">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="42d2a-435">Az.DataLakeStore</span></span>
- <span data-ttu-id="42d2a-436">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="42d2a-436">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="42d2a-437">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="42d2a-437">Az.Monitor</span></span>
- <span data-ttu-id="42d2a-438">Az.Insights 已重新命名為 Az.Monitor，並有次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="42d2a-438">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="42d2a-439">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="42d2a-439">Az.KeyVault</span></span>
- <span data-ttu-id="42d2a-440">已從輸出類型中移除淘汰的 'PurgeDisabled' 屬性</span><span class="sxs-lookup"><span data-stu-id="42d2a-440">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="42d2a-441">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="42d2a-441">Az.MachineLearning</span></span>
- <span data-ttu-id="42d2a-442">已納入來自 Az.MachineLearningCompute 模組的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="42d2a-442">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="42d2a-443">Az.Media</span><span class="sxs-lookup"><span data-stu-id="42d2a-443">Az.Media</span></span>
- <span data-ttu-id="42d2a-444">從 New-AzMediaService 移除淘汰的 -Tags 別名</span><span class="sxs-lookup"><span data-stu-id="42d2a-444">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="42d2a-445">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42d2a-445">Az.Network</span></span>
<span data-ttu-id="42d2a-446">已新增在應用程式閘道中設定 RewriteRuleSets 的支援</span><span class="sxs-lookup"><span data-stu-id="42d2a-446">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="42d2a-447">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="42d2a-447">New cmdlets added:</span></span>
        - <span data-ttu-id="42d2a-448">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="42d2a-448">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="42d2a-449">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="42d2a-449">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="42d2a-450">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="42d2a-450">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="42d2a-451">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="42d2a-451">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="42d2a-452">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="42d2a-452">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="42d2a-453">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="42d2a-453">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="42d2a-454">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="42d2a-454">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="42d2a-455">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="42d2a-455">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="42d2a-456">Cmdlets updated with optional parameter -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="42d2a-456">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="42d2a-457">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="42d2a-457">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="42d2a-458">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="42d2a-458">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="42d2a-459">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="42d2a-459">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="42d2a-460">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="42d2a-460">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="42d2a-461">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="42d2a-461">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="42d2a-462">New-AzureRmApplicationGatewayUrlPathMapConfig 已使用身分識別對應用程式閘道新增 KeyVault 支援。</span><span class="sxs-lookup"><span data-stu-id="42d2a-462">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="42d2a-463">已使用選擇性參數 -KeyVaultSecretId, -KeyVaultSecret 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="42d2a-463">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="42d2a-464">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="42d2a-464">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="42d2a-465">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="42d2a-465">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="42d2a-466">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="42d2a-466">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="42d2a-467">已使用選擇性參數 -UserAssignedIdentity 更新了 New-AzApplicationGateway Cmdlet</span><span class="sxs-lookup"><span data-stu-id="42d2a-467">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="42d2a-468">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="42d2a-468">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="42d2a-469">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="42d2a-469">Az.OperationalInsights</span></span>
- <span data-ttu-id="42d2a-470">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="42d2a-470">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="42d2a-471">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="42d2a-471">Az.Profile</span></span>
- <span data-ttu-id="42d2a-472">模組名稱已變更為 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="42d2a-472">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="42d2a-473">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="42d2a-473">Az.RecoveryServices</span></span>
- <span data-ttu-id="42d2a-474">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="42d2a-474">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="42d2a-475">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42d2a-475">Az.Resources</span></span>
- <span data-ttu-id="42d2a-476">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="42d2a-476">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="42d2a-477">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="42d2a-477">Az.ServiceFabric</span></span>
- <span data-ttu-id="42d2a-478">支援依通用名稱和指紋來指定憑證</span><span class="sxs-lookup"><span data-stu-id="42d2a-478">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="42d2a-479">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="42d2a-479">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="42d2a-480">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="42d2a-480">Az.SIgnalR</span></span>
- <span data-ttu-id="42d2a-481">SIgnalR 的 PowerShell Cmdlet 正式運作</span><span class="sxs-lookup"><span data-stu-id="42d2a-481">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="42d2a-482">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42d2a-482">Az.Sql</span></span>
- <span data-ttu-id="42d2a-483">已對威脅偵測的 Cmdlet 新增 Data_Exfiltration 和 Unsafe_Action 偵測類型</span><span class="sxs-lookup"><span data-stu-id="42d2a-483">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="42d2a-484">已更新 SQL 稽核 Cmdlet 的文件範例</span><span class="sxs-lookup"><span data-stu-id="42d2a-484">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="42d2a-485">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="42d2a-485">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="42d2a-486">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="42d2a-486">Az.Storage</span></span>
- <span data-ttu-id="42d2a-487">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="42d2a-487">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="42d2a-488">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="42d2a-488">Az.Websites</span></span>
- <span data-ttu-id="42d2a-489">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="42d2a-489">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="42d2a-490">0.7.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="42d2a-490">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="42d2a-491">一般</span><span class="sxs-lookup"><span data-stu-id="42d2a-491">General</span></span>

* <span data-ttu-id="42d2a-492">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="42d2a-492">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="42d2a-493">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42d2a-493">Az.Compute</span></span>

* <span data-ttu-id="42d2a-494">針對 `New-AzVm(ss)` Cmdlet 簡單參數集內的 UltraSSD 和資源庫映像新增支援。</span><span class="sxs-lookup"><span data-stu-id="42d2a-494">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="42d2a-495">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="42d2a-495">Az.DataLakeStore</span></span>

* <span data-ttu-id="42d2a-496">修正 adls 帳戶網域的尾端斜線</span><span class="sxs-lookup"><span data-stu-id="42d2a-496">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="42d2a-497">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="42d2a-497">Az.FrontDoor</span></span>

* <span data-ttu-id="42d2a-498">已修正一些中斷的連結</span><span class="sxs-lookup"><span data-stu-id="42d2a-498">Fixed some broken links</span></span>
    - <span data-ttu-id="42d2a-499">在 New-AzureRmFrontDoor 和 Set-AzureRmFrontDoor 文章中，已修正 New-AzureRmFrontDoorHealthProbeSettingObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="42d2a-499">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="42d2a-500">在 New-AzureRmFrontDoorManagedRuleObject 文章中，已修正 New-AzureRmFrontDoorRuleGroupOverrideObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="42d2a-500">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="42d2a-501">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="42d2a-501">Az.RecoveryServices</span></span>

* <span data-ttu-id="42d2a-502">已針對 Azure 檔案共用的還原作業新增用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="42d2a-502">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="42d2a-503">已將 storageAccountName 和 storageAccountResourceGroupName 設為 afs 還原作業的選擇性項目。</span><span class="sxs-lookup"><span data-stu-id="42d2a-503">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="42d2a-504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42d2a-504">Az.Resources</span></span>

* <span data-ttu-id="42d2a-505">修正 https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="42d2a-505">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="42d2a-506">將 Get-AzureRmRoleAssignment 更新為使用訂用帳戶範圍 (如果有在要求傳統管理員時提供的話)。</span><span class="sxs-lookup"><span data-stu-id="42d2a-506">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="42d2a-507">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42d2a-507">Az.Sql</span></span>

* <span data-ttu-id="42d2a-508">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="42d2a-508">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="42d2a-509">已修正搭配使用 Get-AzureRmSqlDatabaseVulnerabilityAssessment 和 DotNet core 時所會發生的問題</span><span class="sxs-lookup"><span data-stu-id="42d2a-509">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="42d2a-510">已修改 SQL 稽核 Cmdlet 相關說明訊息的文件。</span><span class="sxs-lookup"><span data-stu-id="42d2a-510">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="42d2a-511">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="42d2a-511">Az.Storage</span></span>

* <span data-ttu-id="42d2a-512">對 New-AzureRmStorageAccount 新增 -EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="42d2a-512">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="42d2a-513">已修正下列問題：如果沒有輸入 -DestContext，複製檔案 Cmdlet 無法重複使用目的地中的來源內容</span><span class="sxs-lookup"><span data-stu-id="42d2a-513">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="42d2a-514">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="42d2a-514">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="42d2a-515">支援靜態網站設定</span><span class="sxs-lookup"><span data-stu-id="42d2a-515">Support Static Website configuration</span></span>
    - <span data-ttu-id="42d2a-516">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="42d2a-516">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="42d2a-517">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="42d2a-517">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="42d2a-518">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="42d2a-518">Az.Websites</span></span>

* <span data-ttu-id="42d2a-519">Set-AzureRmWebApp 和 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="42d2a-519">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="42d2a-520">已新增新的參數 (-AzureStoragePath)，指定要將 Azure 儲存體路徑掛接至 Windows 和 Linux 容器應用程式中。</span><span class="sxs-lookup"><span data-stu-id="42d2a-520">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="42d2a-521">使用新 Cmdlet New-AzureRmWebAppAzureStoragePath 的輸出作為參數來設定 Azure 儲存體路徑。</span><span class="sxs-lookup"><span data-stu-id="42d2a-521">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="42d2a-522">0.6.1 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="42d2a-522">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="42d2a-523">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="42d2a-523">Az.ApiManagement</span></span>
* <span data-ttu-id="42d2a-524">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="42d2a-524">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="42d2a-525">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="42d2a-525">Az.Automation</span></span>
* <span data-ttu-id="42d2a-526">以 Swagger 為基礎的 Azure 自動化 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="42d2a-526">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="42d2a-527">已新增更新管理 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="42d2a-527">Added Update Management cmdlets</span></span>
* <span data-ttu-id="42d2a-528">已新增原始檔控制 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="42d2a-528">Added Source Control cmdlets</span></span>
* <span data-ttu-id="42d2a-529">已新增 Remove-AzureRmAutomationHybridWorkerGroup Cmdlet</span><span class="sxs-lookup"><span data-stu-id="42d2a-529">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="42d2a-530">已修正 DSC 註冊節點命令</span><span class="sxs-lookup"><span data-stu-id="42d2a-530">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="42d2a-531">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42d2a-531">Az.Compute</span></span>
* <span data-ttu-id="42d2a-532">已修正 SystemAssigned 身分識別的身份識別問題</span><span class="sxs-lookup"><span data-stu-id="42d2a-532">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="42d2a-533">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="42d2a-533">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="42d2a-534">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="42d2a-534">Az.ContainerInstance</span></span>
* <span data-ttu-id="42d2a-535">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="42d2a-535">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="42d2a-536">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="42d2a-536">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="42d2a-537">更新市集 Cmdlet 的範例描述</span><span class="sxs-lookup"><span data-stu-id="42d2a-537">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="42d2a-538">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42d2a-538">Az.Network</span></span>
* <span data-ttu-id="42d2a-539">已新增 Cmdlet：New-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayCustomError、Get-AzureRmApplicationGatewayCustomError、Set-AzureRmApplicationGatewayCustomError、Remove-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayHttpListenerCustomError、Get-AzureRmApplicationGatewayHttpListenerCustomError、Set-AzureRmApplicationGatewayHttpListenerCustomError、Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="42d2a-539">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="42d2a-540">已將 ICMP 加回支援的 AzureFirewall 網路通訊協定</span><span class="sxs-lookup"><span data-stu-id="42d2a-540">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="42d2a-541">更新 Test-AzureRmNetworkWatcherConnectivity Cmdlet，在目的地識別碼、位址和連接埠上新增驗證。</span><span class="sxs-lookup"><span data-stu-id="42d2a-541">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="42d2a-542">修正 VirtualNetwork 對應中的記憶體使用量問題</span><span class="sxs-lookup"><span data-stu-id="42d2a-542">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="42d2a-543">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="42d2a-543">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="42d2a-544">提供修正程式以修改受保護的檔案共用原則。</span><span class="sxs-lookup"><span data-stu-id="42d2a-544">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="42d2a-545">已將原則時區轉換為大寫。</span><span class="sxs-lookup"><span data-stu-id="42d2a-545">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="42d2a-546">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="42d2a-546">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="42d2a-547">已修正 New-AzureRmRecoveryServicesAsrProtectableItem 中的範例</span><span class="sxs-lookup"><span data-stu-id="42d2a-547">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="42d2a-548">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="42d2a-548">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="42d2a-549">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="42d2a-549">Az.Relay</span></span>
* <span data-ttu-id="42d2a-550">已將選擇性參數 -KeyValue 新增至 New-AzureRmRelayKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="42d2a-550">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="42d2a-551">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42d2a-551">Az.Resources</span></span>
* <span data-ttu-id="42d2a-552">在下列項目中更新資源身分識別相關參數的說明文件：`New-AzureRmPolicyAssignment` 和</span><span class="sxs-lookup"><span data-stu-id="42d2a-552">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and</span></span> `Set-AzureRmPolicyAssignment`
* <span data-ttu-id="42d2a-553">新增使用 -Metadata 的 New-AzureRmPolicyDefinition 範例</span><span class="sxs-lookup"><span data-stu-id="42d2a-553">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="42d2a-554">修正：允許在 NetStandard: #7678 #7703 的標籤索引鍵中保留大小寫</span><span class="sxs-lookup"><span data-stu-id="42d2a-554">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="42d2a-555">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="42d2a-555">Az.ServiceFabric</span></span>
* <span data-ttu-id="42d2a-556">針對即將推出的重大變更新增取代資訊</span><span class="sxs-lookup"><span data-stu-id="42d2a-556">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="42d2a-557">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42d2a-557">Az.Sql</span></span>
* <span data-ttu-id="42d2a-558">已在 Azure SQL Database 受控執行個體和 Azure SQL 受控資料庫上新增 CRUD 作業的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="42d2a-558">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="42d2a-559">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="42d2a-559">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="42d2a-560">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="42d2a-560">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="42d2a-561">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="42d2a-561">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="42d2a-562">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="42d2a-562">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="42d2a-563">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="42d2a-563">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="42d2a-564">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="42d2a-564">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="42d2a-565">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="42d2a-565">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="42d2a-566">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="42d2a-566">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="42d2a-567">已在伺服器或資料庫上啟用擴充的稽核原則管理。</span><span class="sxs-lookup"><span data-stu-id="42d2a-567">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="42d2a-568">已新增參數 (PredicateExpression) 以啟用稽核記錄的篩選。</span><span class="sxs-lookup"><span data-stu-id="42d2a-568">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="42d2a-569">已將 Cmdlet 修改為使用 SQL 用戶端，而不是傳統用戶端。</span><span class="sxs-lookup"><span data-stu-id="42d2a-569">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="42d2a-570">Set-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="42d2a-570">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="42d2a-571">Get-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="42d2a-571">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="42d2a-572">Set-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="42d2a-572">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="42d2a-573">Get-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="42d2a-573">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="42d2a-574">已修正使用 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings 和儲存體帳戶名稱參數集的問題</span><span class="sxs-lookup"><span data-stu-id="42d2a-574">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="42d2a-575">0.5.0 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="42d2a-575">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="42d2a-576">一般</span><span class="sxs-lookup"><span data-stu-id="42d2a-576">General</span></span>
* <span data-ttu-id="42d2a-577">已在許多核心 Cmdlet 新增資源完成器 - 這些 Cmdlet 可讓您在以互動方式叫用 Cmdlet 時，使用 TAB 鍵瀏覽現有資源名稱</span><span class="sxs-lookup"><span data-stu-id="42d2a-577">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="42d2a-578">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="42d2a-578">Az.Profile</span></span>
* <span data-ttu-id="42d2a-579">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="42d2a-579">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="42d2a-580">將 Cmdlet Connect-AzAccount 中的參數 TenantId 重新命名為 Tenant 並新增 TenantId 的別名</span><span class="sxs-lookup"><span data-stu-id="42d2a-580">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="42d2a-581">更新 Connect-AzAccount 的 TenantId 說明</span><span class="sxs-lookup"><span data-stu-id="42d2a-581">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="42d2a-582">修正提供租用戶網域時登入失敗的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="42d2a-582">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="42d2a-583">修正租用戶中無訂用帳戶之帳戶內容衝突的問題</span><span class="sxs-lookup"><span data-stu-id="42d2a-583">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="42d2a-584">修正使用 MSI 時 DataLake 端點的問題</span><span class="sxs-lookup"><span data-stu-id="42d2a-584">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="42d2a-585">修正若未連線，'Disconnect-AzAccount' 會擲出錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="42d2a-585">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="42d2a-586">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="42d2a-586">Az.CognitiveServices</span></span>
* <span data-ttu-id="42d2a-587">新增 Get-AzCognitiveServicesAccountSkus 作業。</span><span class="sxs-lookup"><span data-stu-id="42d2a-587">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42d2a-588">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42d2a-588">Az.Compute</span></span>
* <span data-ttu-id="42d2a-589">新增 Add-AzVmssVMDataDisk 和 Remove-AzVmssVMDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="42d2a-589">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="42d2a-590">Get-AzVMImage 顯示 AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="42d2a-590">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="42d2a-591">已修正 SetAzVMChefExtension -BootstrapOptions 和 -JsonAttribute 選項值並未以 json 格式設定的問題。</span><span class="sxs-lookup"><span data-stu-id="42d2a-591">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="42d2a-592">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="42d2a-592">Az.DataLakeStore</span></span>
* <span data-ttu-id="42d2a-593">將 DataLake 套件更新為 1.1.10。</span><span class="sxs-lookup"><span data-stu-id="42d2a-593">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="42d2a-594">將預設並行新增至多執行作業。</span><span class="sxs-lookup"><span data-stu-id="42d2a-594">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="42d2a-595">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="42d2a-595">Az.Insights</span></span>
* <span data-ttu-id="42d2a-596">已修正問題 #7267 (自動調整區域)</span><span class="sxs-lookup"><span data-stu-id="42d2a-596">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="42d2a-597">建立新自動調整規則時未適當設定列舉的參數 (一律會設為預設值) 的問題。</span><span class="sxs-lookup"><span data-stu-id="42d2a-597">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="42d2a-598">已修正問題 #7513 [Insights] Set-AzDiagnosticSetting 在建立設定時需要明確的類別規格</span><span class="sxs-lookup"><span data-stu-id="42d2a-598">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="42d2a-599">目前 Cmdlet 在建立期間不需要明確的類別指示也能啟用，例如 Cmdlet 會如說明所述之方式運作</span><span class="sxs-lookup"><span data-stu-id="42d2a-599">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="42d2a-600">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42d2a-600">Az.Network</span></span>
* <span data-ttu-id="42d2a-601">已將 PeeringType 變更為下列 Cmdlet 的必要參數：-</span><span class="sxs-lookup"><span data-stu-id="42d2a-601">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="42d2a-602">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="42d2a-602">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="42d2a-603">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="42d2a-603">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="42d2a-604">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="42d2a-604">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="42d2a-605">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="42d2a-605">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="42d2a-606">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="42d2a-606">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="42d2a-607">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="42d2a-607">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="42d2a-608">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="42d2a-608">Az.PolicyInsights</span></span>
* <span data-ttu-id="42d2a-609">已新增原則修復 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="42d2a-609">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="42d2a-610">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42d2a-610">Az.Resources</span></span>
* <span data-ttu-id="42d2a-611">修正 https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="42d2a-611">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="42d2a-612">允許使用 'Get-AzResource' 的 '-ResourceId' 參數列出資源</span><span class="sxs-lookup"><span data-stu-id="42d2a-612">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="42d2a-613">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="42d2a-613">Az.ServiceBus</span></span>
* <span data-ttu-id="42d2a-614">已將 MigrationState 唯讀屬性新增至 PSServiceBusMigrationConfigurationAttributes，以便協助了解移轉狀態。</span><span class="sxs-lookup"><span data-stu-id="42d2a-614">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="42d2a-615">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="42d2a-615">Az.ServiceFabric</span></span>
* <span data-ttu-id="42d2a-616">修正將憑證新增至 Linux Vmss。</span><span class="sxs-lookup"><span data-stu-id="42d2a-616">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="42d2a-617">修正 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="42d2a-617">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="42d2a-618">使用新憑證中正確的指紋 (Azure/service-fabric-issues#932)。</span><span class="sxs-lookup"><span data-stu-id="42d2a-618">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="42d2a-619">正確顯示例外狀況 (Azure/service-fabric-issues#1054)。</span><span class="sxs-lookup"><span data-stu-id="42d2a-619">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="42d2a-620">修正 'Update-AzServiceFabricDurability' 以在啟動 Vmss CreateOrUpdate operation 之前更新叢集組態。</span><span class="sxs-lookup"><span data-stu-id="42d2a-620">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="42d2a-621">0.4.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="42d2a-621">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="42d2a-622">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="42d2a-622">Az.Profile</span></span>
* <span data-ttu-id="42d2a-623">修正 CloudShell 中 Get-AzSubscription 的問題</span><span class="sxs-lookup"><span data-stu-id="42d2a-623">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="42d2a-624">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="42d2a-624">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42d2a-625">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42d2a-625">Az.Compute</span></span>
* <span data-ttu-id="42d2a-626">已將新的大小新增至虛擬機器大小允許清單，當使用 'New-AzVm' 的簡單參數集合時，將會開啟加速的網路</span><span class="sxs-lookup"><span data-stu-id="42d2a-626">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="42d2a-627">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="42d2a-627">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="42d2a-628">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="42d2a-628">Az.DataLakeStore</span></span>
* <span data-ttu-id="42d2a-629">新增虛擬網路規則的支援</span><span class="sxs-lookup"><span data-stu-id="42d2a-629">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="42d2a-630">Get-AzDataLakeStoreVirtualNetworkRule：取得或列出 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="42d2a-630">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="42d2a-631">Add-AzDataLakeStoreVirtualNetworkRule：將虛擬網路規則新增至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="42d2a-631">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="42d2a-632">Set-AzDataLakeStoreVirtualNetworkRule：修改指定 Data Lake Store 帳戶中的特定虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="42d2a-632">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="42d2a-633">Remove-AzDataLakeStoreVirtualNetworkRule：刪除 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="42d2a-633">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="42d2a-634">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42d2a-634">Az.Network</span></span>
* <span data-ttu-id="42d2a-635">更新 Cmdlet Test-AzNetworkWatcherConnectivity，將通訊協定值傳遞至後端。</span><span class="sxs-lookup"><span data-stu-id="42d2a-635">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="42d2a-636">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="42d2a-636">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="42d2a-637">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42d2a-637">Az.Resources</span></span>
* <span data-ttu-id="42d2a-638">修正當 Get-AzRoleDefinition 藉由在案例中加上有意義的例外狀況，而擲回無法辨識的例外狀況 (當預設的設定檔中沒有訂用帳戶，且未指定範圍) 問題。</span><span class="sxs-lookup"><span data-stu-id="42d2a-638">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="42d2a-639">也將預設參數集合設定為 'RoleDefinitionNameParameterSet'。</span><span class="sxs-lookup"><span data-stu-id="42d2a-639">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="42d2a-640">0.3.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="42d2a-640">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="42d2a-641">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="42d2a-641">Azure.Storage</span></span>
* <span data-ttu-id="42d2a-642">修正當目的地有中繼資料問題時，複製 Blob/檔案不會一併複製中繼資料的問題</span><span class="sxs-lookup"><span data-stu-id="42d2a-642">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="42d2a-643">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="42d2a-643">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="42d2a-644">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="42d2a-644">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="42d2a-645">支援取得特定位置的儲存體資源使用量，並針對取得全域儲存體資源使用量已過時的情況新增警告訊息。</span><span class="sxs-lookup"><span data-stu-id="42d2a-645">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="42d2a-646">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="42d2a-646">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="42d2a-647">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="42d2a-647">Az.CognitiveServices</span></span>
* <span data-ttu-id="42d2a-648">在沒有現有帳戶的情況下支援 Get-AzCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="42d2a-648">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="42d2a-649">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="42d2a-649">Az.Compute</span></span>
* <span data-ttu-id="42d2a-650">修正 Get-AzVM -ResourceGroupName <rg> 以在必要時傳回超過 50 個結果</span><span class="sxs-lookup"><span data-stu-id="42d2a-650">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="42d2a-651">已將 'SimpleParameterSet' 的範例新增到 New-AzVmss Cmdlet 說明中。</span><span class="sxs-lookup"><span data-stu-id="42d2a-651">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="42d2a-652">已修正 Azure 磁碟加密進度訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="42d2a-652">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="42d2a-653">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="42d2a-653">Az.DataFactoryV2</span></span>
* <span data-ttu-id="42d2a-654">已將 ADF .Net SDK 版本更新為 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="42d2a-654">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="42d2a-655">Az.Network</span><span class="sxs-lookup"><span data-stu-id="42d2a-655">Az.Network</span></span>
* <span data-ttu-id="42d2a-656">已新增 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="42d2a-656">Added NetworkProfile functionality.</span></span> <span data-ttu-id="42d2a-657">已新增新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="42d2a-657">new cmdlets added</span></span>
    - <span data-ttu-id="42d2a-658">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="42d2a-658">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="42d2a-659">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="42d2a-659">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="42d2a-660">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="42d2a-660">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="42d2a-661">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="42d2a-661">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="42d2a-662">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="42d2a-662">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="42d2a-663">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="42d2a-663">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="42d2a-664">已在子網路模型中新增服務關聯連結</span><span class="sxs-lookup"><span data-stu-id="42d2a-664">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="42d2a-665">已新增 New-AzVirtualNetworkTap、Get-AzVirtualNetworkTap、Set-AzVirtualNetworkTap、Remove-AzVirtualNetworkTap Cmdlet</span><span class="sxs-lookup"><span data-stu-id="42d2a-665">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="42d2a-666">已新增 Set-AzNEtworkInterfaceTapConfig、Get-AzNEtworkInterfaceTapConfig 和 Remove-AzNEtworkInterfaceTapConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="42d2a-666">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="42d2a-667">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="42d2a-667">Az.RedisCache</span></span>
* <span data-ttu-id="42d2a-668">日後允許任何字串做為 Size 參數。</span><span class="sxs-lookup"><span data-stu-id="42d2a-668">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="42d2a-669">在 P5 PSArgumentCompleter 快顯視窗中新增 P5</span><span class="sxs-lookup"><span data-stu-id="42d2a-669">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="42d2a-670">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="42d2a-670">Az.Resources</span></span>
* <span data-ttu-id="42d2a-671">將遺漏的 -Mode 參數新增至 Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="42d2a-671">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="42d2a-672">修正 Get-AzProviderOperation Commandlet 錯誤 (bug)，以進行包含使用者的 Origin 作業</span><span class="sxs-lookup"><span data-stu-id="42d2a-672">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="42d2a-673">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="42d2a-673">Az.Sql</span></span>
* <span data-ttu-id="42d2a-674">已修正部分備份 Cmdlet 無法辨識目前 Azure 訂用帳戶的問題</span><span class="sxs-lookup"><span data-stu-id="42d2a-674">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="42d2a-675">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="42d2a-675">Az.Websites</span></span>
* <span data-ttu-id="42d2a-676">新 Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 取得容器連續部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="42d2a-676">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="42d2a-677">新 Cmdlet New-AzWebAppContainerPSSession 與 Enter-WebAppContainerPSSession  - 在 Windows 容器應用程式中初始 PowerShell 遠端工作階段</span><span class="sxs-lookup"><span data-stu-id="42d2a-677">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="42d2a-678">0.2.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="42d2a-678">0.2.0 - September 2018</span></span>
 <span data-ttu-id="42d2a-679">初始版本</span><span class="sxs-lookup"><span data-stu-id="42d2a-679">Initial Release</span></span>