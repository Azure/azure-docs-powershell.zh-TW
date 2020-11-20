---
title: Azure PowerShell 版本資訊
description: 了解 Azure PowerShell 模組的最新更新資訊。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 280486e45dad73c935f03cedc619c0de762deb12
ms.sourcegitcommit: d81c3b0f0f7289104be03869eb675128b61db7d3
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/17/2020
ms.locfileid: "94715160"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="8c5c8-103">Azure PowerShell 版本資訊</span><span class="sxs-lookup"><span data-stu-id="8c5c8-103">Azure PowerShell release notes</span></span>

## <a name="510---november-2020"></a><span data-ttu-id="8c5c8-104">5.1.0 - 2020 年 11 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-104">5.1.0 - November 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8c5c8-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8c5c8-105">Az.Accounts</span></span>
* <span data-ttu-id="8c5c8-106">已修正使用 ''Connect-AzAccount -DeviceCode' 時，可能不會遵守 TenantId 的問題 [#13477]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-106">Fixed an issue that TenantId may be not respected if using 'Connect-AzAccount -DeviceCode'[#13477]</span></span>
* <span data-ttu-id="8c5c8-107">已新增 Cmdlet 'Get-AzAccessToken'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-107">Added new cmdlet 'Get-AzAccessToken'</span></span>
* <span data-ttu-id="8c5c8-108">已修正無法存取使用者設定檔路徑時發生錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-108">Fixed an issue that error happens if user profile path is inaccessible</span></span>
* <span data-ttu-id="8c5c8-109">已修正 Connect-AzAccount 期間發生 Write-Object 錯誤的問題 [#13419]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-109">Fixed an issue causing Write-Object error during Connect-AzAccount [#13419]</span></span>
* <span data-ttu-id="8c5c8-110">已將參數 'ContainerRegistryEndpointSuffix' 新增至：'Add-AzEnvironment'、'Set-AzEnvironment'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-110">Added parameter 'ContainerRegistryEndpointSuffix' to: 'Add-AzEnvironment', 'Set-AzEnvironment'</span></span> 
* <span data-ttu-id="8c5c8-111">支援點擊 <kbd>CTRL</kbd>+<kbd>C</kbd> 來中斷登入</span><span class="sxs-lookup"><span data-stu-id="8c5c8-111">Supported interrupting login by hitting <kbd>CTRL</kbd>+<kbd>C</kbd></span></span>
* <span data-ttu-id="8c5c8-112">已修正導致 'Connect-AzAccount -KeyVaultAccessToken' 無法運作的問題 [#13127]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-112">Fixed an issue causing 'Connect-AzAccount -KeyVaultAccessToken' not working [#13127]</span></span>
* <span data-ttu-id="8c5c8-113">已修正 'Invoke-AzRestMethod' 中 Null 參考和方法不區分大小寫的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-113">Fixed null reference and method case insensitive in 'Invoke-AzRestMethod'</span></span>

#### <a name="azaks"></a><span data-ttu-id="8c5c8-114">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="8c5c8-114">Az.Aks</span></span>
* <span data-ttu-id="8c5c8-115">已修正使用者無法使用服務主體建立新 Kubernetes 叢集的問題。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-115">Fixed the issue that user cannot use service principal to create a new Kubernetes cluster.</span></span> <span data-ttu-id="8c5c8-116">[#13012]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-116">[#13012]</span></span>

#### <a name="azappconfiguration"></a><span data-ttu-id="8c5c8-117">Az.AppConfiguration</span><span class="sxs-lookup"><span data-stu-id="8c5c8-117">Az.AppConfiguration</span></span>
* <span data-ttu-id="8c5c8-118">'Az.AppConfiguration' 模組的正式推出</span><span class="sxs-lookup"><span data-stu-id="8c5c8-118">General availability of 'Az.AppConfiguration' module</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8c5c8-119">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8c5c8-119">Az.DataFactory</span></span>
* <span data-ttu-id="8c5c8-120">已改善 'New-AzDataFactoryV2LinkedServiceEncryptedCredential' 命令的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="8c5c8-120">Improved error message of 'New-AzDataFactoryV2LinkedServiceEncryptedCredential' command</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8c5c8-121">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8c5c8-121">Az.DataLakeStore</span></span>
* <span data-ttu-id="8c5c8-122">已將 ADLS 資料平面 SDK 更新為 1.2.4-alpha。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-122">Updated ADLS dataplane SDK to 1.2.4-alpha.</span></span> <span data-ttu-id="8c5c8-123">變更： https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-124-alpha</span><span class="sxs-lookup"><span data-stu-id="8c5c8-123">Changes:https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-124-alpha</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="8c5c8-124">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="8c5c8-124">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="8c5c8-125">已新增 MSIX Package Cmdlet 和更新應用程式 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-125">Added new MSIX Package cmdlets and updated Applications cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8c5c8-126">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8c5c8-126">Az.EventHub</span></span>
* <span data-ttu-id="8c5c8-127">已修正 EventHub 叢集沒有標記時的叢集命令</span><span class="sxs-lookup"><span data-stu-id="8c5c8-127">Fixed Cluster commands for EventHub cluster without tags</span></span>
* <span data-ttu-id="8c5c8-128">已更新 AzEventHubGeoDRConfiguration 的 PartnerNamespace 命令解說文字</span><span class="sxs-lookup"><span data-stu-id="8c5c8-128">Updated help text for PartnerNamespace of AzEventHubGeoDRConfiguration commands</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="8c5c8-129">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8c5c8-129">Az.HDInsight</span></span>
* <span data-ttu-id="8c5c8-130">已將 'ResourceProviderConnection' 和 'PrivateLink' 參數新增至 'New-AzHDInsightCluster' Cmdlet 以支援轉送輸出和私人連結功能</span><span class="sxs-lookup"><span data-stu-id="8c5c8-130">Add parameters 'ResourceProviderConnection' and 'PrivateLink' to cmdlet 'New-AzHDInsightCluster' to support relay outbound and private link feature</span></span>
* <span data-ttu-id="8c5c8-131">已將 'AmbariDatabase' 參數新增至 'New-AzHDInsightCluster' Cmdlet，以支援自訂 Ambari 資料庫功能</span><span class="sxs-lookup"><span data-stu-id="8c5c8-131">Add parameter 'AmbariDatabase' to cmdlet 'New-AzHDInsightCluster' to support custom Ambari database feature</span></span>
* <span data-ttu-id="8c5c8-132">將接受值 'AmbariDatabase' 新增至 'Add-AzHDInsightMetastore' Cmdlet 的 'MetastoreType' 參數</span><span class="sxs-lookup"><span data-stu-id="8c5c8-132">Add accept value 'AmbariDatabase' to the parameter 'MetastoreType' of the cmdlet 'Add-AzHDInsightMetastore'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8c5c8-133">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8c5c8-133">Az.IotHub</span></span>
* <span data-ttu-id="8c5c8-134">允許在 IoT 中樞建立 Cmdlet 中使用標記。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-134">Allowed tags in IoT Hub create cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8c5c8-135">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8c5c8-135">Az.KeyVault</span></span>
* <span data-ttu-id="8c5c8-136">支援更新金鑰保存庫標記</span><span class="sxs-lookup"><span data-stu-id="8c5c8-136">Supported updating key vault tag</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8c5c8-137">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8c5c8-137">Az.LogicApp</span></span>
* <span data-ttu-id="8c5c8-138">已修正 Get-AzLogicAppRunHistory 只會取得結果第一頁的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-138">Fixed for Get-AzLogicAppRunHistory only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8c5c8-139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c5c8-139">Az.Network</span></span>
* <span data-ttu-id="8c5c8-140">已更新下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-140">Updated below cmdlet</span></span> 
    - <span data-ttu-id="8c5c8-141">'New-AzLoadBalancerFrontendIpConfigCommand'、'Set-AzLoadBalancerFrontendIpConfigCommand'、'Add-AzLoadBalancerFrontendIpConfigCommand'：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-141">'New-AzLoadBalancerFrontendIpConfigCommand', 'Set-AzLoadBalancerFrontendIpConfigCommand', 'Add-AzLoadBalancerFrontendIpConfigCommand':</span></span>
        - <span data-ttu-id="8c5c8-142">已新增 PublicIpAddressPrefix 屬性</span><span class="sxs-lookup"><span data-stu-id="8c5c8-142">Added PublicIpAddressPrefix property</span></span>
        - <span data-ttu-id="8c5c8-143">已新增 PublicIpAddressPrefixId 屬性</span><span class="sxs-lookup"><span data-stu-id="8c5c8-143">Added PublicIpAddressPrefixId property</span></span>
* <span data-ttu-id="8c5c8-144">已將新屬性新增至下列 Cmdlet，以允許進行全域負載平衡</span><span class="sxs-lookup"><span data-stu-id="8c5c8-144">Added new properties to the following cmdlets to allow for global load balancing</span></span>
    - <span data-ttu-id="8c5c8-145">'New-AzLoadBalancer'：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-145">'New-AzLoadBalancer':</span></span>
        - <span data-ttu-id="8c5c8-146">已新增 SKU 層屬性</span><span class="sxs-lookup"><span data-stu-id="8c5c8-146">Added Sku Tier property</span></span>
    - <span data-ttu-id="8c5c8-147">'New-AzPuplicIpAddress'：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-147">'New-AzPuplicIpAddress':</span></span>
        - <span data-ttu-id="8c5c8-148">已新增 SKU 層屬性</span><span class="sxs-lookup"><span data-stu-id="8c5c8-148">Added Sku Tier property</span></span>
    - <span data-ttu-id="8c5c8-149">'New-AzPublicIpPrefix'：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-149">'New-AzPublicIpPrefix':</span></span>
        - <span data-ttu-id="8c5c8-150">已新增 SKU 層屬性</span><span class="sxs-lookup"><span data-stu-id="8c5c8-150">Added Sku Tier property</span></span>
    - <span data-ttu-id="8c5c8-151">'New-AzLoadBalancerBackendAddressConfig'：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-151">'New-AzLoadBalancerBackendAddressConfig':</span></span>
        - <span data-ttu-id="8c5c8-152">已新增 LoadBalancerFrontendIPConfigurationId 屬性</span><span class="sxs-lookup"><span data-stu-id="8c5c8-152">Added LoadBalancerFrontendIPConfigurationId property</span></span>
* <span data-ttu-id="8c5c8-153">已更新規劃來取代下列 Cmdlet 的警告   -'New-AzVirtualHubRoute'   -'New-AzVirtualHubRouteTable'   -'Add-AzVirtualHubRoute'   -'Add-AzVirtualHubRouteTable'   -'Get-AzVirtualHubRouteTable'   -'Remove-AzVirtualHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-153">Updated planning to deprecate warnings for the following cmdlets   -'New-AzVirtualHubRoute'   -'New-AzVirtualHubRouteTable'   -'Add-AzVirtualHubRoute'   -'Add-AzVirtualHubRouteTable'   -'Get-AzVirtualHubRouteTable'   -'Remove-AzVirtualHubRouteTable'</span></span>
* <span data-ttu-id="8c5c8-154">已新增規劃來取代下列 Cmdlet 的 'RouteTable' 引數警告   -'New-AzVirtualHub'   -'Set-AzVirtualHub'   -'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-154">Added planning to deprecate warnings on the argument 'RouteTable' for the following cmdlets   -'New-AzVirtualHub'   -'Set-AzVirtualHub'   -'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="8c5c8-155">已將 '-MinScaleUnits' 和 '-MaxScaleUnits' 引數設為 'Set-AzExpressRouteGateway' 中的選擇性項目</span><span class="sxs-lookup"><span data-stu-id="8c5c8-155">Made arguments '-MinScaleUnits' and '-MaxScaleUnits' optional in 'Set-AzExpressRouteGateway'</span></span>
* <span data-ttu-id="8c5c8-156">已新增 Cmdlet 來支援應用程式閘道的相互驗證和 SSL 設定檔</span><span class="sxs-lookup"><span data-stu-id="8c5c8-156">Added new cmdlets to support Mutual Authentication and SSL Profiles on Application Gateway</span></span>
    - <span data-ttu-id="8c5c8-157">'Get-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-157">'Get-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="8c5c8-158">'New-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-158">'New-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="8c5c8-159">'Remove-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-159">'Remove-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="8c5c8-160">'Set-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-160">'Set-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="8c5c8-161">'Add-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-161">'Add-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="8c5c8-162">'Get-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-162">'Get-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="8c5c8-163">'New-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-163">'New-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="8c5c8-164">'Remove-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-164">'Remove-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="8c5c8-165">'Set-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-165">'Set-AzApplicationGatewayTrustedClientCertificate'</span></span>
    - <span data-ttu-id="8c5c8-166">'Add-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-166">'Add-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="8c5c8-167">'Get-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-167">'Get-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="8c5c8-168">'New-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-168">'New-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="8c5c8-169">'Remove-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-169">'Remove-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="8c5c8-170">'Set-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-170">'Set-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="8c5c8-171">'Get-AzApplicationGatewaySslProfilePolicy'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-171">'Get-AzApplicationGatewaySslProfilePolicy'</span></span>
    - <span data-ttu-id="8c5c8-172">'Remove-AzApplicationGatewaySslProfilePolicy'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-172">'Remove-AzApplicationGatewaySslProfilePolicy'</span></span>
    - <span data-ttu-id="8c5c8-173">'Set-AzApplicationGatewaySslProfilePolicy'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-173">'Set-AzApplicationGatewaySslProfilePolicy'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8c5c8-174">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-174">Az.RecoveryServices</span></span>
* <span data-ttu-id="8c5c8-175">指定原則 BackupTime 的格式為 UTC。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-175">Specifying policy BackupTime is in UTC.</span></span>
* <span data-ttu-id="8c5c8-176">修改 Get-AzRecoveryServicesBackupJobDetails Cmdlet 中的中斷性變更警告。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-176">Modifying breaking change warning in Get-AzRecoveryServicesBackupJobDetails cmdlet.</span></span>
* <span data-ttu-id="8c5c8-177">更新 Set-AzRecoveryServicesBackupProtectionPolicy Cmdlet 的範例指令碼解說文字。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-177">Updating sample script help text for Set-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8c5c8-178">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c5c8-178">Az.Resources</span></span>
* <span data-ttu-id="8c5c8-179">已修正 What-If 會顯示兩個大小寫不同的資源群組範圍的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-179">Fixed an issue where What-If shows two resource group scopes with different casing</span></span>
* <span data-ttu-id="8c5c8-180">已將 'Export-AzResourceGroup' 更新為使用 SDK。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-180">Updated 'Export-AzResourceGroup' to use the SDK.</span></span>
* <span data-ttu-id="8c5c8-181">已將文化特性資訊新增至 parse 方法</span><span class="sxs-lookup"><span data-stu-id="8c5c8-181">Added culture info to parse methods</span></span>

#### <a name="azsql"></a><span data-ttu-id="8c5c8-182">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c5c8-182">Az.Sql</span></span>
* <span data-ttu-id="8c5c8-183">已修正 Set-AzSqlDatabaseAudit 不支援超大規模資料庫資料庫和資料庫版本無法判斷的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-183">Fixed issues where Set-AzSqlDatabaseAudit were not support Hyperscale database and database edition cannot be determined</span></span>
* <span data-ttu-id="8c5c8-184">已將 MaintenanceConfigurationId 新增至 New-AzSqlInstance' 和 'Set-AzSqlInstance'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-184">Added MaintenanceConfigurationId to 'New-AzSqlInstance' and 'Set-AzSqlInstance'</span></span>
* <span data-ttu-id="8c5c8-185">已修正 GetAzureSqlDatabaseReplicationLink.cs 中的錯誤 (bug)：PartnerServerName 參數會以值進行檢查，而非索引鍵</span><span class="sxs-lookup"><span data-stu-id="8c5c8-185">Fixed a bug in GetAzureSqlDatabaseReplicationLink.cs where PartnerServerName parameter was being checked for by value instead of key</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8c5c8-186">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8c5c8-186">Az.Websites</span></span>
* <span data-ttu-id="8c5c8-187">新增最新存取限制功能的支援：ServiceTag、multi-ip 和 http-headers</span><span class="sxs-lookup"><span data-stu-id="8c5c8-187">Added support for new access restriction features: ServiceTag, multi-ip and http-headers</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="8c5c8-188">感謝我們的社群參與者</span><span class="sxs-lookup"><span data-stu-id="8c5c8-188">Thanks to our community contributors</span></span>
* <span data-ttu-id="8c5c8-189">John Q. Martin (@johnmart82)，新增防火牆必要條件資訊 (#13385)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-189">John Q. Martin (@johnmart82), Adding firewall prerequisite information (#13385)</span></span>
* <span data-ttu-id="8c5c8-190">Manikandan Duraisamy (@madurais-msft)，修正 PublicSubnetName 引數 (#13417)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-190">Manikandan Duraisamy (@madurais-msft), Corrected the PublicSubnetName argument (#13417)</span></span>
* <span data-ttu-id="8c5c8-191">@mahortas，更新 -HostNames 參數值 (#13349)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-191">@mahortas, Update for -HostNames parameter values (#13349)</span></span>
* <span data-ttu-id="8c5c8-192">@MariachiForHire，新增支援的 TrafficAnalyticsInterval 值 (#13304)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-192">@MariachiForHire, added supported TrafficAnalyticsInterval values (#13304)</span></span>
* <span data-ttu-id="8c5c8-193">Michael James (@mikejwhat)，允許 Get-AzLogicAppRunHistory 傳回超過 30 個項目 (#13393)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-193">Michael James (@mikejwhat), Allow Get-AzLogicAppRunHistory to return more than 30 entries (#13393)</span></span>
* <span data-ttu-id="8c5c8-194">Shashikant Shakya (@shshakya)，更新 Restore-AzSqlInstanceDatabase.md (#13404)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-194">Shashikant Shakya (@shshakya), Update Restore-AzSqlInstanceDatabase.md (#13404)</span></span>

## <a name="500---october-2020"></a><span data-ttu-id="8c5c8-195">5.0.0 - 2020 年 10 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-195">5.0.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8c5c8-196">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8c5c8-196">Az.Accounts</span></span>
* <span data-ttu-id="8c5c8-197">[中斷性變更] 已移除 'Get-AzProfile' 和 'Select-AzProfile'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-197">[Breaking Change] Removed 'Get-AzProfile' and 'Select-AzProfile'</span></span>
* <span data-ttu-id="8c5c8-198">已將 Azure Directory 驗證程式庫取代為 Microsoft Authentication Library (MSAL)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-198">Replaced Azure Directory Authentication Library with Microsoft Authentication Library(MSAL)</span></span>

#### <a name="azaks"></a><span data-ttu-id="8c5c8-199">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="8c5c8-199">Az.Aks</span></span>
* <span data-ttu-id="8c5c8-200">[中斷性變更]已移除 'New-AzAksCluster' 和 'Set-AzAksCluster' 中的參數別名 'ClientIdAndSecret'。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-200">[Breaking Change] Removed parameter alias 'ClientIdAndSecret' in 'New-AzAksCluster' and 'Set-AzAksCluster'.</span></span>
* <span data-ttu-id="8c5c8-201">[中斷性變更] 已將 'New-AzAksCluster' 中 'NodeVmSetType' 的預設值從 'AvailabilitySet' 變更為 'VirtualMachineScaleSets。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-201">[Breaking Change] Changed the default value of 'NodeVmSetType' in 'New-AzAksCluster' from 'AvailabilitySet' to 'VirtualMachineScaleSets'.</span></span>
* <span data-ttu-id="8c5c8-202">[中斷性變更] 已將 'New-AzAksCluster' 中 'NetworkPlugin' 的預設值從 'None' 變更為 'azure'。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-202">[Breaking Change] Changed the default value of 'NetworkPlugin' in 'New-AzAksCluster' from 'None' to 'azure'.</span></span>
* <span data-ttu-id="8c5c8-203">[中斷性變更] 已移除 'New-AzAksCluster' 中的參數 'NodeOsType'，因為其僅支援一個值 Linux。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-203">[Breaking Change] Removed parameter 'NodeOsType' in 'New-AzAksCluster' as it supports only one value Linux.</span></span>

#### <a name="azbilling"></a><span data-ttu-id="8c5c8-204">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="8c5c8-204">Az.Billing</span></span>
* <span data-ttu-id="8c5c8-205">已新增 'Get-AzBillingAccount' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-205">Added 'Get-AzBillingAccount' cmdlet</span></span>
* <span data-ttu-id="8c5c8-206">已新增 'Get-AzBillingProfile' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-206">Added 'Get-AzBillingProfile' cmdlet</span></span>
* <span data-ttu-id="8c5c8-207">已新增 'Get-AzInvoiceSection' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-207">Added 'Get-AzInvoiceSection' cmdlet</span></span>
* <span data-ttu-id="8c5c8-208">已在 'Get-AzBillingInvoice' Cmdlet 中新增參數</span><span class="sxs-lookup"><span data-stu-id="8c5c8-208">Added new parameters in 'Get-AzBillingInvoice' cmdlet</span></span>
* <span data-ttu-id="8c5c8-209">已從 Get-AzBillingInvoice Cmdlet 的回應中移除屬性 DownloadUrlExpiry、Type、BillingPeriodNames</span><span class="sxs-lookup"><span data-stu-id="8c5c8-209">Removed properties DownloadUrlExpiry, Type, BillingPeriodNames from the response of Get-AzBillingInvoice cmdlet</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8c5c8-210">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8c5c8-210">Az.Cdn</span></span>
* <span data-ttu-id="8c5c8-211">已新增 Cmdlet 來支援多個來源和私人連結功能</span><span class="sxs-lookup"><span data-stu-id="8c5c8-211">Added cmdlets to support multi-origin and private link functionality</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="8c5c8-212">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-212">Az.CognitiveServices</span></span>
* <span data-ttu-id="8c5c8-213">已將 SDK 更新為 7.4.0-preview。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-213">Updated SDK to 7.4.0-preview.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8c5c8-214">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c5c8-214">Az.Compute</span></span>
* <span data-ttu-id="8c5c8-215">已將 '-VmssId' 參數新增至 'New-AzVm'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-215">Added '-VmssId' parameter to 'New-AzVm'</span></span>
* <span data-ttu-id="8c5c8-216">已將 'PlatformFaultDomainCount' 參數新增至 'New-AzVmss' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-216">Added 'PlatformFaultDomainCount' parameter to the 'New-AzVmss' cmdlet.</span></span>
* <span data-ttu-id="8c5c8-217">新的 Cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-217">New cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'</span></span>
* <span data-ttu-id="8c5c8-218">已將 'Tier' 和 'LogicalSectorSize' 選擇性參數新增至 New-AzDiskConfig Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-218">Added 'Tier' and 'LogicalSectorSize' optional parameters to the New-AzDiskConfig cmdlet.</span></span> 
* <span data-ttu-id="8c5c8-219">已將 'Tier'、'MaxSharesCount'、'DiskIOPSReadOnly' 和 'DiskMBpsReadOnly' 選擇性參數新增至 'New-AzDiskUpdateConfig' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-219">Added 'Tier', 'MaxSharesCount', 'DiskIOPSReadOnly', and 'DiskMBpsReadOnly' optional parameters to the 'New-AzDiskUpdateConfig' cmdlet.</span></span> 

#### <a name="azcontainerregistry"></a><span data-ttu-id="8c5c8-220">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8c5c8-220">Az.ContainerRegistry</span></span>
* <span data-ttu-id="8c5c8-221">[重大變更] 將 API 版本更新為 2019-05-01</span><span class="sxs-lookup"><span data-stu-id="8c5c8-221">[Breaking Change] Updates API version to 2019-05-01</span></span>
* <span data-ttu-id="8c5c8-222">[中斷性變更] 已從 'New-AzContainerRegistry' 中移除 SKU 'Classic' 和參數 'StorageAccountName'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-222">[Breaking Change] Removed SKU 'Classic' and parameter 'StorageAccountName' from 'New-AzContainerRegistry'</span></span>
* <span data-ttu-id="8c5c8-223">已新增 Cmdlet：'Connect-AzContainerRegistry'、'Import-AzContainerRegistry'、'Get-AzContainerRegistryUsage'、'New-AzContainerRegistryNetworkRule'、'Set-AzContainerRegistryNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-223">Added New cmdlets: 'Connect-AzContainerRegistry', 'Import-AzContainerRegistry', 'Get-AzContainerRegistryUsage', 'New-AzContainerRegistryNetworkRule', 'Set-AzContainerRegistryNetworkRule'</span></span>
* <span data-ttu-id="8c5c8-224">已將新參數 'NetworkRuleSet' 新增至 'Update-AzContainerRegistry'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-224">Added new parameter 'NetworkRuleSet' to 'Update-AzContainerRegistry'</span></span>

#### <a name="azdatabricks"></a><span data-ttu-id="8c5c8-225">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="8c5c8-225">Az.Databricks</span></span>
* <span data-ttu-id="8c5c8-226">已修正可能導致更新 Databricks 工作區，但 `-EncryptionKeyVersion` 不會失敗的錯誤。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-226">Fixed a bug that may cause updating databricks workspace without `-EncryptionKeyVersion` to fail.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8c5c8-227">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8c5c8-227">Az.DataFactory</span></span>
* <span data-ttu-id="8c5c8-228">已將 ADF .Net SDK 版本更新為 4.12.0</span><span class="sxs-lookup"><span data-stu-id="8c5c8-228">Updated ADF .Net SDK version to 4.12.0</span></span>
* <span data-ttu-id="8c5c8-229">已將 ADF 加密用戶端 SDK 版本更新為 4.14.7587.7</span><span class="sxs-lookup"><span data-stu-id="8c5c8-229">Updated ADF encryption client SDK version to 4.14.7587.7</span></span>
* <span data-ttu-id="8c5c8-230">已新增 'Stop-AzDataFactoryV2TriggerRun' 和 'Invoke-AzDataFactoryV2TriggerRun' 命令</span><span class="sxs-lookup"><span data-stu-id="8c5c8-230">Added 'Stop-AzDataFactoryV2TriggerRun' and 'Invoke-AzDataFactoryV2TriggerRun' commands</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="8c5c8-231">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="8c5c8-231">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="8c5c8-232">需要 Location 屬性，才能建立最上層 arm 物件。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-232">Require Location property for creating top level arm objects.</span></span>
        <span data-ttu-id="8c5c8-233">\* 使 `ApplicationGroupType` 成為 `New-AzWvdApplicationGroup` 的必要項。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-233">\* Made `ApplicationGroupType` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="8c5c8-234">\* 使 `HostPoolArmPath` 成為 `New-AzWvdApplicationGroup` 的必要項。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-234">\* Made `HostPoolArmPath` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="8c5c8-235">\* 已新增 `New-AzWvdHostPool`的 `PreferredAppGroupType`。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-235">\* Added `PreferredAppGroupType` for `New-AzWvdHostPool`.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="8c5c8-236">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="8c5c8-236">Az.Functions</span></span>
* <span data-ttu-id="8c5c8-237">[中斷性變更] 已從 'Get-AzFunctionApp' 的所有參數集 (一個參數集除外) 中移除 'IncludeSlot' 切換參數。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-237">[Breaking Change] Removed 'IncludeSlot' switch parameter from all but one parameter set of 'Get-AzFunctionApp'.</span></span> <span data-ttu-id="8c5c8-238">若已指定 '-IncludeSlot'，此 Cmdlet 現在支援在結果中擷取部署位置。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-238">The cmdlet now supports retrieving deployment slots in the results when '-IncludeSlot' is specified.</span></span> 
* <span data-ttu-id="8c5c8-239">已更新 'New-AzFunctionApp'：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-239">Updated 'New-AzFunctionApp':</span></span>
  - <span data-ttu-id="8c5c8-240">已修正 - DisableApplicationInsights，若已指定此選項，就不會建立 Application Insights 專案。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-240">Fixed -DisableApplicationInsights so that no application insights project is created when this option is specified.</span></span> <span data-ttu-id="8c5c8-241">[#12728]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-241">[#12728]</span></span>
  - <span data-ttu-id="8c5c8-242">[中斷性變更] 已移除建立 PowerShell 6.2 函式應用程式的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-242">[Breaking Change] Removed support to create PowerShell 6.2 function apps.</span></span>
  - <span data-ttu-id="8c5c8-243">[中斷性變更] 若未指定 RuntimeVersion 參數，Windows 上 Functions 第 3 版中 PowerShell 函式應用程式的預設執行階段版本已從 6.2 變更為 7.0。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-243">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="8c5c8-244">[中斷性變更] 若未指定 RuntimeVersion 參數，Windows 和 Linux 上 Functions 第 3 版中 Node 函式應用程式的預設執行階段版本已從 10 變更為 12。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-244">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="8c5c8-245">[中斷性變更] 若未指定 RuntimeVersion 參數，Linux 上 Functions 第 3 版中 Python 函式應用程式的預設執行階段版本已從 3.7 變更為 3.8。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-245">[Breaking Change] Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the RuntimeVersion parameter is not specified.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8c5c8-246">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8c5c8-246">Az.HDInsight</span></span>
 * <span data-ttu-id="8c5c8-247">針對 New-AzHDInsightCluster Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-247">For New-AzHDInsightCluster cmdlet:</span></span>
     - <span data-ttu-id="8c5c8-248">已將參數 'DefaultStorageAccountName' 取代為 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-248">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="8c5c8-249">已將參數 'DefaultStorageAccountKey' 取代為 'StorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-249">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="8c5c8-250">已將參數 'DefaultStorageAccountType' 取代為 'StorageAccountType'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-250">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="8c5c8-251">已移除參數 'PublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-251">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="8c5c8-252">已移除參數 'OutboundPublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-252">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
     - <span data-ttu-id="8c5c8-253">已新增參數：'StorageFileSystem' 和 'StorageAccountManagedIdentity' 來支援 ADLSGen2</span><span class="sxs-lookup"><span data-stu-id="8c5c8-253">Added new parameters: 'StorageFileSystem' and 'StorageAccountManagedIdentity' to support ADLSGen2</span></span>
     - <span data-ttu-id="8c5c8-254">已新增參數 'EnableIDBroker' 來支援 HDInsight 識別碼代理程式</span><span class="sxs-lookup"><span data-stu-id="8c5c8-254">Added new parameter 'EnableIDBroker' to Support HDInsight ID Broker</span></span>
     - <span data-ttu-id="8c5c8-255">已新增參數：'KafkaClientGroupId'、'KafkaClientGroupName' 和 'KafkaManagementNodeSize' 來支援 Kafka Rest Proxy</span><span class="sxs-lookup"><span data-stu-id="8c5c8-255">Added new parameters: 'KafkaClientGroupId', 'KafkaClientGroupName' and 'KafkaManagementNodeSize' to support Kafka Rest Proxy</span></span>
 * <span data-ttu-id="8c5c8-256">針對 New-AzHDInsightClusterConfig Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-256">For New-AzHDInsightClusterConfig cmdlet:</span></span>
     - <span data-ttu-id="8c5c8-257">已將參數 'DefaultStorageAccountName' 取代為 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-257">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="8c5c8-258">已將參數 'DefaultStorageAccountKey' 取代為 'StorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-258">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="8c5c8-259">已將參數 'DefaultStorageAccountType' 取代為 'StorageAccountType'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-259">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="8c5c8-260">已移除參數 'PublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-260">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="8c5c8-261">已移除參數 'OutboundPublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-261">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="8c5c8-262">針對 AzHDInsightDefaultStorage Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-262">For Set-AzHDInsightDefaultStorage cmdlet:</span></span>
    - <span data-ttu-id="8c5c8-263">已將參數 'StorageAccountName' 取代為 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-263">Replaced parameter 'StorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="8c5c8-264">針對 AzHDInsightSecurityProfile Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-264">For Add-AzHDInsightSecurityProfile cmdlet:</span></span>
    - <span data-ttu-id="8c5c8-265">已將參數 'Domain' 取代為 'DomainResourceId'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-265">Replaced parameter 'Domain' with 'DomainResourceId'</span></span>
    - <span data-ttu-id="8c5c8-266">已移除參數 'OrganizationalUnitDN' 的強制需求</span><span class="sxs-lookup"><span data-stu-id="8c5c8-266">Removed the mandatory requirement for parameter 'OrganizationalUnitDN'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8c5c8-267">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8c5c8-267">Az.KeyVault</span></span>
* <span data-ttu-id="8c5c8-268">[中斷性變更] 已淘汰 'New-AzKeyVault' 中的參數 DisableSoftDelete 和 'Update-AzKeyVault' 中的 EnableSoftDelete 參數</span><span class="sxs-lookup"><span data-stu-id="8c5c8-268">[Breaking Change] Deprecated parameter DisableSoftDelete in 'New-AzKeyVault' and EnableSoftDelete in 'Update-AzKeyVault'</span></span>
* <span data-ttu-id="8c5c8-269">[中斷性變更] 已移除屬性 SecretValueText 來避免直接顯示 SecretValue [#12266]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-269">[Breaking Change] Removed attribute SecretValueText to avoid displaying SecretValue directly [#12266]</span></span>
* <span data-ttu-id="8c5c8-270">支援的新資源類型：受控 HSM</span><span class="sxs-lookup"><span data-stu-id="8c5c8-270">Supported new resource type: managed HSM</span></span>
    - <span data-ttu-id="8c5c8-271">受控 HSM 的 CRUD 和要在受控 HSM 上操作金鑰的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-271">CRUD of managed HSM and cmdlets to operate keys on managed HSM</span></span>
    - <span data-ttu-id="8c5c8-272">完整 HSM 備份/還原、AES 金鑰建立、安全性網域備份/還原、RBAC</span><span class="sxs-lookup"><span data-stu-id="8c5c8-272">Full HSM backup/restore, AES key creation, security domain backup/restore, RBAC</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="8c5c8-273">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-273">Az.ManagedServices</span></span>
* <span data-ttu-id="8c5c8-274">[中斷性變更] 已更新參數命名慣例和相關範例</span><span class="sxs-lookup"><span data-stu-id="8c5c8-274">[Breaking Change] Updated parameters naming conventions and associated examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8c5c8-275">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c5c8-275">Az.Network</span></span>
* <span data-ttu-id="8c5c8-276">[中斷性變更] 已移除參數 'HostedSubnet' 並改為新增 'Subnet'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-276">[Breaking Change] Removed parameter 'HostedSubnet' and added 'Subnet' instead</span></span>
* <span data-ttu-id="8c5c8-277">已針對虛擬路由器對等路由新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-277">Added new cmdlets for Virtual Router Peer Routes</span></span>
    - <span data-ttu-id="8c5c8-278">'Get-AzVirtualRouterPeerLearnedRoute'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-278">'Get-AzVirtualRouterPeerLearnedRoute'</span></span>
    - <span data-ttu-id="8c5c8-279">'Get-AzVirtualRouterPeerAdvertisedRoute'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-279">'Get-AzVirtualRouterPeerAdvertisedRoute'</span></span>
* <span data-ttu-id="8c5c8-280">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-280">Updated New-AzFirewall cmdlet:</span></span>
    - <span data-ttu-id="8c5c8-281">已新增參數 '-SkuTier'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-281">Added parameter '-SkuTier'</span></span>
    - <span data-ttu-id="8c5c8-282">已新增參數 '-SkuName' 並將 Sku 設為此項的別名</span><span class="sxs-lookup"><span data-stu-id="8c5c8-282">Added parameter '-SkuName' and made Sku as Alias for this</span></span>
    - <span data-ttu-id="8c5c8-283">已移除參數 '-Sku'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-283">Removed parameter '-Sku'</span></span>
* <span data-ttu-id="8c5c8-284">[中斷性變更] 讓 'Connectionlink' 成為 'Start-AzVpnConnectionPacketCapture' 和 'Stop-AzVpnConnectionPacketCapture' 中的必要引數</span><span class="sxs-lookup"><span data-stu-id="8c5c8-284">[Breaking Change] Made 'Connectionlink' argument mandatory in 'Start-AzVpnConnectionPacketCapture' and 'Stop-AzVpnConnectionPacketCapture'</span></span>
* <span data-ttu-id="8c5c8-285">[中斷性變更] 已更新 'New-AzNetworkWatcherConnectionMonitorEndPointObject' 來移除參數 '-Filter'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-285">[Breaking Change] Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' to remove parameter '-Filter'</span></span>
* <span data-ttu-id="8c5c8-286">[中斷性變更] 已將 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' Cmdlet 取代為 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-286">[Breaking Change] Replaced 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' cmdlet with 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'</span></span>
* <span data-ttu-id="8c5c8-287">已更新 'New-AzNetworkWatcherConnectionMonitorEndPointObject' Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-287">Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' cmdlet:</span></span>
    - <span data-ttu-id="8c5c8-288">已新增參數 '-Type'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-288">Added parameter '-Type'</span></span>
    - <span data-ttu-id="8c5c8-289">已新增參數 '-CoverageLevel'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-289">Added parameter '-CoverageLevel'</span></span>
    - <span data-ttu-id="8c5c8-290">已新增參數 '-Scope'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-290">Added parameter '-Scope'</span></span>
* <span data-ttu-id="8c5c8-291">已使用新參數 '-DestinationPortBehavior' 更新 'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-291">Updated 'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' cmdlet with new parameter '-DestinationPortBehavior'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8c5c8-292">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-292">Az.RecoveryServices</span></span>
* <span data-ttu-id="8c5c8-293">已修正參與者權限的工作負載還原。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-293">Fixing Workload Restore for contributor permissions.</span></span>
* <span data-ttu-id="8c5c8-294">已針對 Restore-AzRecoveryServicesBackupItem Cmdlet 新增參數集和驗證。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-294">Added new parameter sets and validations for Restore-AzRecoveryServicesBackupItem cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8c5c8-295">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c5c8-295">Az.Resources</span></span>
* <span data-ttu-id="8c5c8-296">已修正剖析錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-296">Fixed parsing bug</span></span>
* <span data-ttu-id="8c5c8-297">已更新 ARM 範本 What-If Cmdlet 以便從結果中移除預覽訊息</span><span class="sxs-lookup"><span data-stu-id="8c5c8-297">Updated ARM template What-If cmdlets to remove preview message from results</span></span>
* <span data-ttu-id="8c5c8-298">已修正 '-WhatIf ' 設定於較高範圍時範本部署 Cmdlet 損毀的問題 [#13038]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-298">Fixed an issue where template deployment cmdlets crash if '-WhatIf' is set at a higher scope [#13038]</span></span>
* <span data-ttu-id="8c5c8-299">已修正範本部署 Cmdlet 未保留範本參數大小寫的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-299">Fixed an issue where template deployment cmdlets does not preserve case for template parameters</span></span>
* <span data-ttu-id="8c5c8-300">已新增要在 'Export-AzResourceGroup' Cmdlet 中使用的預設 API 版本</span><span class="sxs-lookup"><span data-stu-id="8c5c8-300">Added a default API version to be used in 'Export-AzResourceGroup' cmdlet</span></span>
* <span data-ttu-id="8c5c8-301">已針對範本規格 ('Get-AzTemplateSpec'、'Set-AzTemplateSpec'、'New-AzTemplateSpec'、'Remove-AzTemplateSpec'、'Export-AzTemplateSpec') 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-301">Added cmdlets for Template Specs ('Get-AzTemplateSpec', 'Set-AzTemplateSpec', 'New-AzTemplateSpec', 'Remove-AzTemplateSpec', 'Export-AzTemplateSpec')</span></span>
* <span data-ttu-id="8c5c8-302">已新增使用現有的部署 Cmdlet 來部署範本規格的支援 (透過新的 -TemplateSpecId 參數)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-302">Added support for deploying Template Specs using existing deployment cmdlets (via the new -TemplateSpecId parameter)</span></span> 
* <span data-ttu-id="8c5c8-303">已將 'Get-AzResourceGroupDeploymentOperation' 更新為使用 SDK。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-303">Updated 'Get-AzResourceGroupDeploymentOperation' to use the SDK.</span></span>
* <span data-ttu-id="8c5c8-304">已從 '\*-AzDeployment' Cmdlet 中移除 '-ApiVersion' 參數。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-304">Removed '-ApiVersion' parameter from '\*-AzDeployment' cmdlets.</span></span>

#### <a name="azsql"></a><span data-ttu-id="8c5c8-305">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c5c8-305">Az.Sql</span></span>
* <span data-ttu-id="8c5c8-306">已修正未指定 networkIsolation 時 New-AzSqlDatabaseExport 失敗的問題 [#13097]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-306">Fixed issue where New-AzSqlDatabaseExport fails if networkIsolation not specified [#13097]</span></span>
* <span data-ttu-id="8c5c8-307">已修正 New-AzSqlDatabaseExport 和 New-AzSqlDatabaseImport 未在結果物件中傳回 OperationStatusLink 的問題 [#13097]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-307">Fixed issue where New-AzSqlDatabaseExport and New-AzSqlDatabaseImport were not returning OperationStatusLink in the result object [#13097]</span></span>
* <span data-ttu-id="8c5c8-308">在備份儲存體備援警告中更新 Azure 配對區域 URL</span><span class="sxs-lookup"><span data-stu-id="8c5c8-308">Update Azure Paired Regions URL in Backup Storage Redundancy Warnings</span></span> 

#### <a name="azstorage"></a><span data-ttu-id="8c5c8-309">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8c5c8-309">Az.Storage</span></span>
* <span data-ttu-id="8c5c8-310">已移除淘汰的屬性 RestorePolicy.LastEnabledTime</span><span class="sxs-lookup"><span data-stu-id="8c5c8-310">Removed obsolete property RestorePolicy.LastEnabledTime</span></span>
    - <span data-ttu-id="8c5c8-311">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-311">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="8c5c8-312">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-312">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="8c5c8-313">'Get-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-313">'Get-AzStorageBlobServiceProperty'</span></span>
    - <span data-ttu-id="8c5c8-314">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-314">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="8c5c8-315">將 DaysAfterModificationGreaterThan 的類型從 int 變更為 int？</span><span class="sxs-lookup"><span data-stu-id="8c5c8-315">Change Type of DaysAfterModificationGreaterThan from int to int?</span></span>
    - <span data-ttu-id="8c5c8-316">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-316">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="8c5c8-317">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-317">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="8c5c8-318">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-318">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="8c5c8-319">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-319">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="8c5c8-320">使用存取層支援的建立/更新檔案共用</span><span class="sxs-lookup"><span data-stu-id="8c5c8-320">Supported create/update file share with access tier</span></span>
    - <span data-ttu-id="8c5c8-321">'New-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-321">'New-AzRmStorageShare'</span></span>
    - <span data-ttu-id="8c5c8-322">'Update-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-322">'Update-AzRmStorageShare'</span></span>
* <span data-ttu-id="8c5c8-323">在 Datalake Gen2 項目上以遞迴方式支援的設定/更新/移除 Acl</span><span class="sxs-lookup"><span data-stu-id="8c5c8-323">Supported set/update/remove Acl recursively on Datalake Gen2 item</span></span> 
    -  <span data-ttu-id="8c5c8-324">'Set-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-324">'Set-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="8c5c8-325">'Update-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-325">'Update-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="8c5c8-326">'Remove-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-326">'Remove-AzDataLakeGen2AclRecursive'</span></span>
* <span data-ttu-id="8c5c8-327">具有新權限 x,t 支援的容器存取原則</span><span class="sxs-lookup"><span data-stu-id="8c5c8-327">Supported Container access policy with new permission x,t</span></span>
    -  <span data-ttu-id="8c5c8-328">'New-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-328">'New-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="8c5c8-329">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-329">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="8c5c8-330">已變更取得/設定容器存取原則 Cmdlet 的輸出，方法是將子屬性權限類型從 enum 變更為 String</span><span class="sxs-lookup"><span data-stu-id="8c5c8-330">Changed the output of get/set Container access policy cmdlet, by change the child property Permission type from enum to String</span></span>
    -  <span data-ttu-id="8c5c8-331">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-331">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="8c5c8-332">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-332">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="8c5c8-333">已修正使用 json 設定管理原則的範例指令碼問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-333">Fixed a sample script issue of set management policy with json</span></span>
    -  <span data-ttu-id="8c5c8-334">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-334">'Set-AzStorageAccountManagementPolicy'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8c5c8-335">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8c5c8-335">Az.Websites</span></span>
* <span data-ttu-id="8c5c8-336">已新增 Premium V3 定價層的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-336">Added support for Premium V3 pricing tier</span></span>
* <span data-ttu-id="8c5c8-337">已將 WebSites SDK 更新為 3.1.0</span><span class="sxs-lookup"><span data-stu-id="8c5c8-337">Updated the WebSites SDK to 3.1.0</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="8c5c8-338">感謝我們的社群參與者</span><span class="sxs-lookup"><span data-stu-id="8c5c8-338">Thanks to our community contributors</span></span>
* <span data-ttu-id="8c5c8-339">@atul-ram，更新 Get-AzDelegation.md (#13176)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-339">@atul-ram, Update Get-AzDelegation.md (#13176)</span></span>
* <span data-ttu-id="8c5c8-340">@dineshreddy007，在使用 WAC 權杖進行堆疊 HCI 註冊的情況下，取得正確指派的應用程式角色。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-340">@dineshreddy007, Get the App Roles assigned correctly in case of Stack HCI registration using WAC token.</span></span> <span data-ttu-id="8c5c8-341">(#13249)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-341">(#13249)</span></span>
* <span data-ttu-id="8c5c8-342">@kongou-ae，更新 New-AzOffice365PolicyProperty.md (#13217)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-342">@kongou-ae, Update New-AzOffice365PolicyProperty.md (#13217)</span></span>
* <span data-ttu-id="8c5c8-343">Lohith Chowdary Chilukuri (@Lochiluk)，更新 Set-AzApplicationGateway.md (#13150)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-343">Lohith Chowdary Chilukuri (@Lochiluk), Update Set-AzApplicationGateway.md (#13150)</span></span>
* <span data-ttu-id="8c5c8-344">Matthew Burleigh (@mburleigh)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-344">Matthew Burleigh (@mburleigh)</span></span>
  * <span data-ttu-id="8c5c8-345">將連結新增至文件 (#13203) 中參考的 PowerShell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-345">Add links to PowerShell cmdlets referenced in the document (#13203)</span></span>
  * <span data-ttu-id="8c5c8-346">將連結新增至文件 (#13190) 中參考的 PowerShell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-346">Add links to PowerShell cmdlets referenced in the document (#13190)</span></span>
  * <span data-ttu-id="8c5c8-347">將連結新增至文件 (#13189) 中參考的 PowerShell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-347">Add links to PowerShell cmdlets referenced in the document (#13189)</span></span>
  * <span data-ttu-id="8c5c8-348">將連結新增至參考的 Cmdlet (#13137)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-348">add links to referenced cmdlets (#13137)</span></span>
  * <span data-ttu-id="8c5c8-349">將連結新增至文件 (#13204) 中參考的 PowerShell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-349">Add links to PowerShell cmdlets referenced in the document (#13204)</span></span>
  * <span data-ttu-id="8c5c8-350">將連結新增至文件 (#13205) 中參考的 PowerShell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-350">Add links to PowerShell cmdlets referenced in the document (#13205)</span></span>

## <a name="480---october-2020"></a><span data-ttu-id="8c5c8-351">4.8.0 - 2020 年 10 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-351">4.8.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8c5c8-352">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8c5c8-352">Az.Accounts</span></span>
* <span data-ttu-id="8c5c8-353">已修正通用程式庫中的日期時間剖析問題 [#13045]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-353">Fixed DateTime parse issue in common libraries [#13045]</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8c5c8-354">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-354">Az.CognitiveServices</span></span>
* <span data-ttu-id="8c5c8-355">已新增 'New-AzCognitiveServicesAccountApiProperty' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-355">Added 'New-AzCognitiveServicesAccountApiProperty' cmdlet.</span></span>
* <span data-ttu-id="8c5c8-356">針對 'New-AzCognitiveServicesAccount' 和 'Set-AzCognitiveServicesAccount' 支援 'ApiProperty' 參數</span><span class="sxs-lookup"><span data-stu-id="8c5c8-356">Supported 'ApiProperty' parameter for 'New-AzCognitiveServicesAccount' and 'Set-AzCognitiveServicesAccount'</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8c5c8-357">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c5c8-357">Az.Compute</span></span>
* <span data-ttu-id="8c5c8-358">已藉由田 FailoverTypes 修正 'Update-ASRRecoveryPlan' 中的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-358">Fixed issue in 'Update-ASRRecoveryPlan' by populating FailoverTypes</span></span>
* <span data-ttu-id="8c5c8-359">已將 '-Top' 和 '-OrderBy' 選擇性參數新增至 'Get-AzVmImage' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-359">Added the '-Top' and '-OrderBy' optional parameters to the 'Get-AzVmImage' cmdlet.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="8c5c8-360">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="8c5c8-360">Az.Databricks</span></span>
* <span data-ttu-id="8c5c8-361">'Az.Databricks' 模組正式發行</span><span class="sxs-lookup"><span data-stu-id="8c5c8-361">General availability of 'Az.Databricks' module</span></span>
* <span data-ttu-id="8c5c8-362">已新增虛擬網路對等互連的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-362">Added support for virtual network peering</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8c5c8-363">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8c5c8-363">Az.DataFactory</span></span>
* <span data-ttu-id="8c5c8-364">已修正輸出訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="8c5c8-364">Fixed typo in output messages</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8c5c8-365">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8c5c8-365">Az.EventHub</span></span>
* <span data-ttu-id="8c5c8-366">已將選擇性切換參數 'TrustedServiceAccessEnabled' 新增至 'Set-AzEventHubNetworkRuleSet' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-366">Added optional switch parameter 'TrustedServiceAccessEnabled' to 'Set-AzEventHubNetworkRuleSet' cmdlet</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8c5c8-367">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8c5c8-367">Az.HDInsight</span></span>
* <span data-ttu-id="8c5c8-368">已新增計劃的警告訊息，以取代 'PublicNetworkAccessType' 和 'OutboundPublicNetworkAccessType' 參數</span><span class="sxs-lookup"><span data-stu-id="8c5c8-368">Added warning message for planning to deprecate the parameters 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="8c5c8-369">已新增計劃的警告訊息，以使用 'StorageAccountResourceId' 取代 'DefaultStorageAccountName' 參數</span><span class="sxs-lookup"><span data-stu-id="8c5c8-369">Added warning message for planning to replace the parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="8c5c8-370">已新增計劃的警告訊息，以使用 'StorageAccountKey' 取代 'DefaultStorageAccountKey' 參數</span><span class="sxs-lookup"><span data-stu-id="8c5c8-370">Added warning message for planning to replace the parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
* <span data-ttu-id="8c5c8-371">已新增計劃的警告訊息，以使用 'StorageAccountType' 取代 'DefaultStorageAccountType' 參數</span><span class="sxs-lookup"><span data-stu-id="8c5c8-371">Added warning message for planning to replace the parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
* <span data-ttu-id="8c5c8-372">已新增計劃的警告訊息，以使用 'StorageContainer' 取代 'DefaultStorageContainer' 參數</span><span class="sxs-lookup"><span data-stu-id="8c5c8-372">Added warning message for planning to replace the parameter 'DefaultStorageContainer' with 'StorageContainer'</span></span>
* <span data-ttu-id="8c5c8-373">已新增計劃的警告訊息，以使用 'StorageRootPath' 取代 'DefaultStorageRootPath' 參數</span><span class="sxs-lookup"><span data-stu-id="8c5c8-373">Added warning message for planning to replace the parameter 'DefaultStorageRootPath' with 'StorageRootPath'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8c5c8-374">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8c5c8-374">Az.IotHub</span></span>
* <span data-ttu-id="8c5c8-375">已更新裝置 SDK。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-375">Updated devices sdk.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8c5c8-376">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8c5c8-376">Az.KeyVault</span></span>
* <span data-ttu-id="8c5c8-377">已提供移除屬性 SecretValueText 的詳細日期</span><span class="sxs-lookup"><span data-stu-id="8c5c8-377">Provided the detailed date of removing property SecretValueText</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="8c5c8-378">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-378">Az.ManagedServices</span></span>
* <span data-ttu-id="8c5c8-379">已在受控服務指派和定義的 Cmdlet 上更新中斷性變更警告</span><span class="sxs-lookup"><span data-stu-id="8c5c8-379">Updated breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8c5c8-380">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8c5c8-380">Az.Monitor</span></span>
* <span data-ttu-id="8c5c8-381">已修正無法隱藏警告訊息的錯誤。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-381">Fixed the bug that warning message cannot be suppressed.</span></span> <span data-ttu-id="8c5c8-382">[#12889]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-382">[#12889]</span></span>
* <span data-ttu-id="8c5c8-383">在警示規則準則中支援 'SkipMetricValidation' 參數。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-383">Supported 'SkipMetricValidation' parameter in alert rule criteria.</span></span> <span data-ttu-id="8c5c8-384">藉由導致略過計量驗證，允許針對尚未發出的自訂計量建立警示規則。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-384">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8c5c8-385">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c5c8-385">Az.Network</span></span>
* <span data-ttu-id="8c5c8-386">已將 Office365 原則新增至 VPNSite 資源</span><span class="sxs-lookup"><span data-stu-id="8c5c8-386">Added Office365 Policy to VPNSite Resource</span></span>
    - <span data-ttu-id="8c5c8-387">'New-AzO365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-387">'New-AzO365PolicyProperty'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8c5c8-388">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-388">Az.RecoveryServices</span></span>
* <span data-ttu-id="8c5c8-389">已新增工作負載備份的容器名稱驗證。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-389">Added container name validation for workload backup.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="8c5c8-390">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8c5c8-390">Az.RedisCache</span></span>
* <span data-ttu-id="8c5c8-391">讓 'New-AzRedisCache' 和 'Set-AzRedisCache' Cmdlet 不會因為註冊 Microsoft.Cache RP 相關的權限問題而失敗</span><span class="sxs-lookup"><span data-stu-id="8c5c8-391">Made 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets not fail because of permission issue related to registering Microsoft.Cache RP</span></span>

#### <a name="azsql"></a><span data-ttu-id="8c5c8-392">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c5c8-392">Az.Sql</span></span>
* <span data-ttu-id="8c5c8-393">已將 BackupStorageRedundancy 新增至下列項目：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-393">Added BackupStorageRedundancy to the following:</span></span> 
    - <span data-ttu-id="8c5c8-394">'Restore-AzureRmSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-394">'Restore-AzureRmSqlDatabase'</span></span>
    - <span data-ttu-id="8c5c8-395">'New-AzSqlDatabaseCopy'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-395">'New-AzSqlDatabaseCopy'</span></span>
    - <span data-ttu-id="8c5c8-396">'New-AzSqlDatabaseSecondary'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-396">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="8c5c8-397">已針對所有 SQL DB 參考移除 BackupStorageRedundancy 參數的區分大小寫</span><span class="sxs-lookup"><span data-stu-id="8c5c8-397">Removed case sensitivity for BackupStorageRedundancy parameter for all SQL DB references</span></span> 
* <span data-ttu-id="8c5c8-398">已更新 BackupStorageRedundancy 警告訊息名稱</span><span class="sxs-lookup"><span data-stu-id="8c5c8-398">Updated BackupStorageRedundancy warning message names</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8c5c8-399">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8c5c8-399">Az.Storage</span></span>
* <span data-ttu-id="8c5c8-400">儲存體帳戶檔案服務上支援的啟用/停用/取得共用虛刪除屬性</span><span class="sxs-lookup"><span data-stu-id="8c5c8-400">Supported enable/disable/get share soft delete properties on file Service of a Storage account</span></span>
    - <span data-ttu-id="8c5c8-401">'Update-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-401">'Update-AzStorageFileServiceProperty'</span></span>
    - <span data-ttu-id="8c5c8-402">'Get-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-402">'Get-AzStorageFileServiceProperty'</span></span>
* <span data-ttu-id="8c5c8-403">支援的清單檔案共用包含已刪除的儲存體帳戶，以及取得單一檔案共用使用方式</span><span class="sxs-lookup"><span data-stu-id="8c5c8-403">Supported list file shares include the deleted ones of a Storage account, and Get single file share usage</span></span>
    - <span data-ttu-id="8c5c8-404">'Get-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-404">'Get-AzRmStorageShare'</span></span>
* <span data-ttu-id="8c5c8-405">支援還原已刪除檔案共用</span><span class="sxs-lookup"><span data-stu-id="8c5c8-405">Supported restore a deleted file share</span></span>
    - <span data-ttu-id="8c5c8-406">'Restore-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-406">'Restore-AzRmStorageShare'</span></span>
* <span data-ttu-id="8c5c8-407">已變更修改 Blob 服務屬性的 Cmdlet，不會從伺服器取得原始屬性，而只會將修改的屬性設定至伺服器。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-407">Changed the cmdlets for modify blob service properties, won't get the original properties from server, but only set the modified properties to server.</span></span>
    - <span data-ttu-id="8c5c8-408">'Enable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-408">'Enable-AzStorageBlobDeleteRetentionPolicy'</span></span>
    - <span data-ttu-id="8c5c8-409">'Disable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-409">'Disable-AzStorageBlobDeleteRetentionPolicy'</span></span>  
    - <span data-ttu-id="8c5c8-410">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-410">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="8c5c8-411">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-411">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="8c5c8-412">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-412">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="8c5c8-413">已修正 New-AzStorageAccount 參數 -Kind 預設值的說明問題 [#12189]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-413">Fixed help issue for New-AzStorageAccount parameter -Kind default value [#12189]</span></span>
* <span data-ttu-id="8c5c8-414">已修正新增範例的問題，以顯示如何在 Blob 上傳中設定正確的 ContentType [#12989]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-414">Fixed issue by add example to show how to set correct ContentType in blob upload [#12989]</span></span>

## <a name="470---september-2020"></a><span data-ttu-id="8c5c8-415">4.7.0 - 2020 年 9 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-415">4.7.0 - September 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8c5c8-416">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8c5c8-416">Az.Accounts</span></span>
* <span data-ttu-id="8c5c8-417">已格式化即將推出的重大變更訊息</span><span class="sxs-lookup"><span data-stu-id="8c5c8-417">Formatted the upcoming breaking change messages</span></span>
* <span data-ttu-id="8c5c8-418">已將 Azure.Core 更新為 1.4.1</span><span class="sxs-lookup"><span data-stu-id="8c5c8-418">Updated Azure.Core to 1.4.1</span></span>

#### <a name="azaks"></a><span data-ttu-id="8c5c8-419">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="8c5c8-419">Az.Aks</span></span>
* <span data-ttu-id="8c5c8-420">已新增 'New-AzAksCluster'、'Set-AzAksCluster' 和 'New-AzAksNodePool' 的用戶端參數驗證邏輯。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-420">Added client side parameter validation logic for 'New-AzAksCluster', 'Set-AzAksCluster' and 'New-AzAksNodePool'.</span></span> <span data-ttu-id="8c5c8-421">[#12372]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-421">[#12372]</span></span>
* <span data-ttu-id="8c5c8-422">已新增對 'New-AzAksCluster' 中附加元件的支援。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-422">Added support for add-ons in 'New-AzAksCluster'.</span></span> <span data-ttu-id="8c5c8-423">[#11239]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-423">[#11239]</span></span>
* <span data-ttu-id="8c5c8-424">已為附加元件新增 Cmdlet 'Enable-AzAksAddOn' 和 'Disable-AzAksAddOn'。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-424">Added cmdlets 'Enable-AzAksAddOn' and 'Disable-AzAksAddOn' for add-ons.</span></span> <span data-ttu-id="8c5c8-425">[#11239]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-425">[#11239]</span></span>
* <span data-ttu-id="8c5c8-426">已為 'New-AzAksCluster' 新增參數 'GenerateSshKey'。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-426">Added parameter 'GenerateSshKey' for 'New-AzAksCluster'.</span></span> <span data-ttu-id="8c5c8-427">[#12371]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-427">[#12371]</span></span>
* <span data-ttu-id="8c5c8-428">已將 api 版本更新為 2020-06-01。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-428">Updated api version to 2020-06-01.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8c5c8-429">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-429">Az.CognitiveServices</span></span>
* <span data-ttu-id="8c5c8-430">已顯示特定 API 的其他法律條款。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-430">Showed additional legal terms for certain APIs.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8c5c8-431">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c5c8-431">Az.Compute</span></span>
* <span data-ttu-id="8c5c8-432">已將 '-EncryptionType' 選擇性參數新增至 'New-AzVmDiskEncryptionSetConfig'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-432">Added the '-EncryptionType' optional parameter to 'New-AzVmDiskEncryptionSetConfig'</span></span>
* <span data-ttu-id="8c5c8-433">適用於新資源類型的新 Cmdlet：DiskAccess 'Get-AzDiskAccess'、'New-AzDiskAccess'、'Get-AzDiskAccess'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-433">New cmdlets for new resource type: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span></span>
* <span data-ttu-id="8c5c8-434">已將選擇性參數 '-DiskAccessId' 和 '-NetworkAccessPolicy' 新增至 'New-AzSnapshotConfig'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-434">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzSnapshotConfig'</span></span>
* <span data-ttu-id="8c5c8-435">已將選擇性參數 '-DiskAccessId' 和 '-NetworkAccessPolicy' 新增至 'New-AzDiskConfig'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-435">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzDiskConfig'</span></span>
* <span data-ttu-id="8c5c8-436">已將 'PatchStatus' 屬性新增至 VirtualMachine 執行個體檢視</span><span class="sxs-lookup"><span data-stu-id="8c5c8-436">Added 'PatchStatus' property to VirtualMachine Instance View</span></span>
* <span data-ttu-id="8c5c8-437">已將 'VMHealth' 屬性新增至虛擬機器的執行個體檢視，這是以 '-Status' 叫用 'Get-AzVm' 時傳回的物件</span><span class="sxs-lookup"><span data-stu-id="8c5c8-437">Added 'VMHealth' property to the virtual machine's instance view, which is the returned object when 'Get-AzVm' is invoked with '-Status'</span></span>
* <span data-ttu-id="8c5c8-438">已將 'AssignedHost' 欄位新增至 'Get-AzVM' 和 'Get-AzVmss' 執行個體檢視。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-438">Added 'AssignedHost' field to 'Get-AzVM' and 'Get-AzVmss' instance views.</span></span> <span data-ttu-id="8c5c8-439">此欄位會顯示虛擬機器執行個體的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="8c5c8-439">The field shows the resource id of the virtual machine instance</span></span>
* <span data-ttu-id="8c5c8-440">已將選擇性參數 '-SupportAutomaticPlacement' 新增至 'New-AzHostGroup'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-440">Added optional parameter '-SupportAutomaticPlacement' to 'New-AzHostGroup'</span></span> 
* <span data-ttu-id="8c5c8-441">已將 '-HostGroupId' 參數新增至 'New-AzVm' 和 'New-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-441">Added the '-HostGroupId' parameter to 'New-AzVm' and 'New-AzVmss'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8c5c8-442">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8c5c8-442">Az.DataFactory</span></span>
* <span data-ttu-id="8c5c8-443">已將 ADF .Net SDK 版本更新為 4.11.0</span><span class="sxs-lookup"><span data-stu-id="8c5c8-443">Updated ADF .Net SDK version to 4.11.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8c5c8-444">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8c5c8-444">Az.EventHub</span></span>
* <span data-ttu-id="8c5c8-445">已新增叢集 Cmdlet - 'New-AzEventHubCluster'、'Set-AzEventHubCluster'、'Get-AzEventHubCluster'、'Remove-AzEventHubCluster'、'Get-AzEventHubClustersAvailableRegions'。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-445">Added new Cluster cmdlets - 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span></span>
* <span data-ttu-id="8c5c8-446">已修正問題 #10722：已修正只將 'Listen' 指派給 AuthorizationRule 權限的問題。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-446">Fixed for issue #10722 : Fix for assigning only 'Listen' to AuthorizationRule rights.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="8c5c8-447">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="8c5c8-447">Az.Functions</span></span>
* <span data-ttu-id="8c5c8-448">已移除在不支援 v2 函式的區域中建立 v2 函式的功能。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-448">Removed the ability to create v2 Functions in regions that do not support it.</span></span>
* <span data-ttu-id="8c5c8-449">已取代 PowerShell 6.2。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-449">Deprecated PowerShell 6.2.</span></span> <span data-ttu-id="8c5c8-450">已新增警告，在使用者建立 PowerShell 6.2 函式應用程式時，建議他們改為建立 PowerShell 7.0 函式應用程式。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-450">Added a warning for when a user creates a PowerShell 6.2 function app that advises them to create a PowerShell 7.0 function app instead.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8c5c8-451">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8c5c8-451">Az.HDInsight</span></span>
* <span data-ttu-id="8c5c8-452">支援建立具有自動調整設定的叢集</span><span class="sxs-lookup"><span data-stu-id="8c5c8-452">Supported creating cluster with Autoscale configuration</span></span>
    - <span data-ttu-id="8c5c8-453">已將新參數 'v2 Functions' 新增至 Cmdlet 'New-AzHDInsightCluster'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-453">Add new parameter 'AutoscaleConfiguration' to the cmdlet 'New-AzHDInsightCluster'</span></span>
* <span data-ttu-id="8c5c8-454">支援操作叢集的自動調整設定</span><span class="sxs-lookup"><span data-stu-id="8c5c8-454">Supported operating cluster's Autoscale configuration</span></span>
    - <span data-ttu-id="8c5c8-455">已新增 Cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-455">Add new cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="8c5c8-456">已新增 Cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-456">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="8c5c8-457">已新增 Cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-457">Add new cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="8c5c8-458">已新增 Cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-458">Add new cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="8c5c8-459">已新增 Cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-459">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8c5c8-460">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8c5c8-460">Az.KeyVault</span></span>
* <span data-ttu-id="8c5c8-461">已新增對 RBAC 授權的支援 [#10557]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-461">Added support for RBAC authorization [#10557]</span></span>
* <span data-ttu-id="8c5c8-462">已加強 'Set-AzKeyVaultAccessPolicy' 中的錯誤處理 [#4007]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-462">Enhanced error handling in 'Set-AzKeyVaultAccessPolicy' [#4007]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="8c5c8-463">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="8c5c8-463">Az.Kusto</span></span>
* <span data-ttu-id="8c5c8-464">正式發行 'Az.Kusto' 模組</span><span class="sxs-lookup"><span data-stu-id="8c5c8-464">General availability of 'Az.Kusto' module</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8c5c8-465">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c5c8-465">Az.Network</span></span>
* <span data-ttu-id="8c5c8-466">[重大變更] 已更新下列 Cmdlet 以配合資源虛擬路由器和虛擬中樞</span><span class="sxs-lookup"><span data-stu-id="8c5c8-466">[Breaking Change] Updated below cmdlets to align resource virtual router and virtual hub</span></span>
    - <span data-ttu-id="8c5c8-467">'New-AzVirtualRouter'：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-467">'New-AzVirtualRouter':</span></span> 
        - <span data-ttu-id="8c5c8-468">已新增 -HostedSubnet 參數來支援 IP 設定子資源</span><span class="sxs-lookup"><span data-stu-id="8c5c8-468">Added -HostedSubnet parameter to support IP configuration child resource</span></span>
        - <span data-ttu-id="8c5c8-469">已刪除 -HostedGateway 和 -HostedGatewayId</span><span class="sxs-lookup"><span data-stu-id="8c5c8-469">deleted -HostedGateway and -HostedGatewayId</span></span>
    - <span data-ttu-id="8c5c8-470">'Get-AzVirtualRouter'：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-470">'Get-AzVirtualRouter':</span></span>
        - <span data-ttu-id="8c5c8-471">已新增訂用帳戶層級參數集</span><span class="sxs-lookup"><span data-stu-id="8c5c8-471">Added subscription level parameter set</span></span>
    - <span data-ttu-id="8c5c8-472">'Remove-AzVirtualRouter'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-472">'Remove-AzVirtualRouter'</span></span>
    - <span data-ttu-id="8c5c8-473">'Add-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-473">'Add-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="8c5c8-474">'Get-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-474">'Get-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="8c5c8-475">'Remove-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-475">'Remove-AzVirtualRouterPeer'</span></span>
* <span data-ttu-id="8c5c8-476">已新增 Azure 快速路由連接埠的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-476">Added new cmdlet for Azure Express Route Port</span></span>
    - <span data-ttu-id="8c5c8-477">'New-AzExpressRoutePortLOA'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-477">'New-AzExpressRoutePortLOA'</span></span>
* <span data-ttu-id="8c5c8-478">已將 RemoteBgpCommunities 屬性新增至 VirtualNetwork 對等互連資源</span><span class="sxs-lookup"><span data-stu-id="8c5c8-478">Added RemoteBgpCommunities property to the VirtualNetwork Peering Resource</span></span>
* <span data-ttu-id="8c5c8-479">已修改 'New-AzLoadBalancerFrontendIpConfig'、'New-AzPublicIpAddress' 和 'New-AzPublicIpPrefix' 的警告訊息。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-479">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>
* <span data-ttu-id="8c5c8-480">已將 VpnGatewayIpConfigurations 新增至 'Get-AzVpnGateway' 輸出</span><span class="sxs-lookup"><span data-stu-id="8c5c8-480">Added VpnGatewayIpConfigurations to 'Get-AzVpnGateway' output</span></span>
* <span data-ttu-id="8c5c8-481">已修正 'Set-AzApplicationGatewaySslCertificate' 的錯誤 (bug) [#9488]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-481">Fixed bug for 'Set-AzApplicationGatewaySslCertificate' [#9488]</span></span>
* <span data-ttu-id="8c5c8-482">已將 'AllowActiveFTP' 參數新增至 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-482">Added 'AllowActiveFTP' parameter to 'AzureFirewall'</span></span>
* <span data-ttu-id="8c5c8-483">已更新下列功能命令：在 VirtualWan P2SVpnGateway 上啟用網際網路安全性設定/移除。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-483">Updated below commands for feature: Enable internet security set/remove on VirtualWan P2SVpnGateway.</span></span>
- <span data-ttu-id="8c5c8-484">已更新 'New-AzP2sVpnGateway'：已新增選擇性切換參數 'EnableInternetSecurityFlag'，可讓客戶將其設定為 true，以在 P2SVpnGateway 上啟用網際網路安全性，這將適用於點對站用戶端。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-484">Updated 'New-AzP2sVpnGateway': Added optional switch parameter 'EnableInternetSecurityFlag' for customers to set true to enable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
- <span data-ttu-id="8c5c8-485">已更新 'Update-AzP2sVpnGateway'：已新增選擇性切換參數 'EnableInternetSecurityFlag' 或 'DisableInternetSecurityFlag'，可讓客戶將其設定為 true/false，以在 P2SVpnGateway 上啟用/停用網際網路安全性，這將適用於點對站用戶端。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-485">Updated 'Update-AzP2sVpnGateway': Added optional switch parameters 'EnableInternetSecurityFlag' or 'DisableInternetSecurityFlag' for customers to set true/false to enable/disable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
* <span data-ttu-id="8c5c8-486">已新增 Cmdlet 'Reset-AzP2sVpnGateway'，可讓客戶重設/重新啟動其 VirtualWan P2SVpnGateway 進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-486">Added new cmdlet 'Reset-AzP2sVpnGateway' for customers to reset/reboot their VirtualWan P2SVpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="8c5c8-487">已新增 Cmdlet 'Reset-AzVpnGateway'，可讓客戶重設/重新啟動其 VirtualWan VpnGateway 進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-487">Added new cmdlet 'Reset-AzVpnGateway' for customers to reset/reboot their VirtualWan VpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="8c5c8-488">已更新 'Set-AzVirtualNetworkSubnetConfig'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-488">Updated 'Set-AzVirtualNetworkSubnetConfig'</span></span>
    - <span data-ttu-id="8c5c8-489">如果已在參數中明確設定，請將子網路的 NSG 和路由表屬性設定為 null [#1548][#9718]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-489">Set NSG and Route Table properties of subnet to null if explicitly set in parameters [#1548][#9718]</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8c5c8-490">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-490">Az.RecoveryServices</span></span>
* <span data-ttu-id="8c5c8-491">已修正工作負載備份項目的刪除狀態。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-491">Fixed the Delete State for workload Backup Items.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8c5c8-492">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c5c8-492">Az.Resources</span></span>
* <span data-ttu-id="8c5c8-493">已新增 Set-AzRoleAssignment 的遺漏檢查</span><span class="sxs-lookup"><span data-stu-id="8c5c8-493">Added missing check for Set-AzRoleAssignment</span></span>
* <span data-ttu-id="8c5c8-494">已將重大變更屬性新增至 'Get-AzResourceGroupDeploymentOperation' 的 'SubscriptionId' 參數</span><span class="sxs-lookup"><span data-stu-id="8c5c8-494">Added breaking change attribute to 'SubscriptionId' parameter of 'Get-AzResourceGroupDeploymentOperation'</span></span>
* <span data-ttu-id="8c5c8-495">已更新 ARM 範本 What-If Cmdlet，以顯示「忽略」上次資源變更</span><span class="sxs-lookup"><span data-stu-id="8c5c8-495">Updated ARM template What-If cmdlets to show 'Ignore' resource changes last</span></span>
* <span data-ttu-id="8c5c8-496">已修正部署 Cmdlet 的安全和陣列參數序列化問題 [#12773]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-496">Fixed secure and array parameter serialization issues for deployment cmdlets [#12773]</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8c5c8-497">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8c5c8-497">Az.ServiceFabric</span></span>
* <span data-ttu-id="8c5c8-498">已新增適用於受控叢集和節點類型的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-498">Added new cmdlets for managed clusters and node types:</span></span>
    - <span data-ttu-id="8c5c8-499">'New-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-499">'New-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="8c5c8-500">'Get-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-500">'Get-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="8c5c8-501">'Set-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-501">'Set-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="8c5c8-502">'Remove-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-502">'Remove-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="8c5c8-503">'Add-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-503">'Add-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="8c5c8-504">'Remove-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-504">'Remove-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="8c5c8-505">'New-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-505">'New-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="8c5c8-506">'Get-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-506">'Get-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="8c5c8-507">'Set-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-507">'Set-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="8c5c8-508">'Remove-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-508">'Remove-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="8c5c8-509">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-509">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="8c5c8-510">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-510">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span></span>
    - <span data-ttu-id="8c5c8-511">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-511">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="8c5c8-512">'Restart-AzServiceFabricManagedNodeTyp'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-512">'Restart-AzServiceFabricManagedNodeTyp'</span></span>
* <span data-ttu-id="8c5c8-513">已將 Service Fabric SDK 升級為版本 1.2.0，此版本將服務網狀架構資源提供者 api-version 2020-03-01 用於目前模型，以及將 2020-01-01-preview 用於受控叢集。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-513">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2020-03-01 for the current model and 2020-01-01-preview for managed clusters.</span></span>

#### <a name="azsql"></a><span data-ttu-id="8c5c8-514">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c5c8-514">Az.Sql</span></span>
* <span data-ttu-id="8c5c8-515">已將 BackupStorageRedundancy 新增至 'New-AzSqlInstance' 及 'Get-AzSqlInstance'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-515">Added BackupStorageRedundancy to 'New-AzSqlInstance' and 'Get-AzSqlInstance'</span></span>
* <span data-ttu-id="8c5c8-516">已新增 Cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-516">Added cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="8c5c8-517">已新增 Cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-517">Added cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="8c5c8-518">已將 Force 參數新增至 'New-AzSqlInstance'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-518">Added Force parameter to 'New-AzSqlInstance'</span></span>
* <span data-ttu-id="8c5c8-519">已新增受控資料庫記錄重新執行服務的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-519">Added cmdlets for Managed Database Log Replay service</span></span>
    - <span data-ttu-id="8c5c8-520">'Start-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-520">'Start-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="8c5c8-521">'Get-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-521">'Get-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="8c5c8-522">'Complete-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-522">'Complete-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="8c5c8-523">'Stop-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-523">'Stop-AzSqlInstanceDatabaseLogReplay'</span></span>
* <span data-ttu-id="8c5c8-524">已新增 Cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-524">Added cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="8c5c8-525">已新增 Cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-525">Added cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="8c5c8-526">已新增 Cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-526">Added cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="8c5c8-527">已更新 Cmdlet 'New-AzSqlDatabaseImport' 和 'New-AzSqlDatabaseExport' 以支援網路隔離功能</span><span class="sxs-lookup"><span data-stu-id="8c5c8-527">Updated cmdlets 'New-AzSqlDatabaseImport' and 'New-AzSqlDatabaseExport' to support network isolation functionality</span></span>
* <span data-ttu-id="8c5c8-528">已新增 Cmdlet 'New-AzSqlDatabaseImportExisting'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-528">Added cmdlet 'New-AzSqlDatabaseImportExisting'</span></span>
* <span data-ttu-id="8c5c8-529">已更新資料庫 Cmdlet 以支援備份儲存體類型規格</span><span class="sxs-lookup"><span data-stu-id="8c5c8-529">Updated Databases cmdlets to support backup storage type specification</span></span>
* <span data-ttu-id="8c5c8-530">已將 Force 參數新增至 'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-530">Added Force parameter to 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="8c5c8-531">已 'New-AzSqlDatabase' 的選取區域中新增 BackupStorageRedundancy 設定的警告</span><span class="sxs-lookup"><span data-stu-id="8c5c8-531">Added warning for BackupStorageRedundancy configuration in select regions in 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="8c5c8-532">已更新伺服器和執行個體的 ActiveDirectoryOnlyAuthentication Cmdlet，以包含 ResourceId 和 InputObject</span><span class="sxs-lookup"><span data-stu-id="8c5c8-532">Updated ActiveDirectoryOnlyAuthentication cmdlets for server and instance to include ResourceId and InputObject</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8c5c8-533">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8c5c8-533">Az.Storage</span></span>
* <span data-ttu-id="8c5c8-534">已升級至 Microsoft.Azure.Storage.DataMovement 2.0.0 來修正上傳 blob 失敗 [#12220]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-534">Fixed upload blob fail by upgrade to Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span></span>
* <span data-ttu-id="8c5c8-535">支援時間點還原</span><span class="sxs-lookup"><span data-stu-id="8c5c8-535">Supported Point In Time Restore</span></span>
    - <span data-ttu-id="8c5c8-536">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-536">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="8c5c8-537">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-537">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="8c5c8-538">'New-AzStorageBlobRangeToRestore'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-538">'New-AzStorageBlobRangeToRestore'</span></span>
    - <span data-ttu-id="8c5c8-539">'Restore-AzStorageBlobRange'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-539">'Restore-AzStorageBlobRange'</span></span>
* <span data-ttu-id="8c5c8-540">支援執行 get-AzureRMStorageAccount 搭配參數 -IncludeGeoReplicationStats，取得儲存體帳戶的 blob 還原狀態</span><span class="sxs-lookup"><span data-stu-id="8c5c8-540">Supported get blob restore status of Storage account by run get-AzureRMStorageAccount with parameter -IncludeBlobRestoreStatus</span></span> 
    - <span data-ttu-id="8c5c8-541">'Get-AzureRMStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-541">'Get-AzureRMStorageAccount'</span></span>
* <span data-ttu-id="8c5c8-542">已為即將進行的 Cmdlet 輸出變更新增重大變更警告訊息</span><span class="sxs-lookup"><span data-stu-id="8c5c8-542">Added breaking change warning message for upcoming cmdlet output change</span></span>
    - <span data-ttu-id="8c5c8-543">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-543">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="8c5c8-544">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-544">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="8c5c8-545">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-545">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="8c5c8-546">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-546">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="8c5c8-547">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-547">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="8c5c8-548">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-548">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="8c5c8-549">已將 Microsoft.Azure.Cosmos.Table SDK 升級至 1.0.8</span><span class="sxs-lookup"><span data-stu-id="8c5c8-549">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.8</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="8c5c8-550">感謝我們的社群參與者</span><span class="sxs-lookup"><span data-stu-id="8c5c8-550">Thanks to our community contributors</span></span>
* <span data-ttu-id="8c5c8-551">Thomas Van Laere (@ThomVanL)，新增 Dockerfile-alpine-3.10 (#12911)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-551">Thomas Van Laere (@ThomVanL), Add Dockerfile-alpine-3.10 (#12911)</span></span> 
* <span data-ttu-id="8c5c8-552">Lohith Chowdary Chilukuri (@Lochiluk)，更新 Remove-AzNetworkInterfaceIpConfig.md (#12807)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-552">Lohith Chowdary Chilukuri (@Lochiluk), Update Remove-AzNetworkInterfaceIpConfig.md (#12807)</span></span> 
* <span data-ttu-id="8c5c8-553">Roberth Strand (@roberthstrand)，Get-AzResourceGroup - 新範例和清除 (#12828)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-553">Roberth Strand (@roberthstrand), Get-AzResourceGroup - New example, and cleanup (#12828)</span></span> 
* <span data-ttu-id="8c5c8-554">Ravi Mishra (@inmishrar)，將 Azure Web 應用程式執行階段堆疊更新為 DOTNETCORE (#12833)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-554">Ravi Mishra (@inmishrar), update Azure Web App runtime stack to DOTNETCORE (#12833)</span></span> 
* <span data-ttu-id="8c5c8-555">@jack-education，更新 New-azvirtualnetworksubnetconfig 以允許從子網移除 NSG 和路由表 (#12351)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-555">@jack-education, Updated Set-AzVirtualNetworkSubnetConfig to allow NSG and Route Table to be removed from subnet (#12351)</span></span> 
* <span data-ttu-id="8c5c8-556">@hagop-globanet，更新 Add-AzApplicationGatewayCustomError.md (#12784)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-556">@hagop-globanet, Update Add-AzApplicationGatewayCustomError.md (#12784)</span></span> 
* <span data-ttu-id="8c5c8-557">Joshua Van Daalen (@greenSacrifice)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-557">Joshua Van Daalen (@greenSacrifice)</span></span>
  * <span data-ttu-id="8c5c8-558">將 Property 的拼寫更新為 Property (#12821)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-558">Update spelling of Property to Property (#12821)</span></span> 
  * <span data-ttu-id="8c5c8-559">更新 New-AzResourceLock.md 範例 (#12806)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-559">Update New-AzResourceLock.md examples (#12806)</span></span>
* <span data-ttu-id="8c5c8-560">Eragon Riddle (@eragonriddle)，更正範例中的參數欄位名稱 (#12825)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-560">Eragon Riddle (@eragonriddle), Corrected parameter field name in the example (#12825)</span></span> 
* <span data-ttu-id="8c5c8-561">@rossifumax，修正 New-AzConfigurationAssignment.md 中的錯字 (#12701)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-561">@rossifumax, Fix typo in New-AzConfigurationAssignment.md (#12701)</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="8c5c8-562">4.6.1 - 2020 年8 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-562">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="8c5c8-563">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c5c8-563">Az.Compute</span></span>
* <span data-ttu-id="8c5c8-564">已修補 'New-AzVm' 中的 '-EncryptionAtHost' 參數，以移除預設值 false [#12776]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-564">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="8c5c8-565">4.6.0 - 2020 年8 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-565">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8c5c8-566">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8c5c8-566">Az.Accounts</span></span>
* <span data-ttu-id="8c5c8-567">當探索端點未傳回預設 AzureCloud 或其他公用環境時，載入所有公用雲端環境 [#12633]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-567">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="8c5c8-568">在 'Get-AzSubscription' 中公開 SubscriptionPolicies [#12551]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-568">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8c5c8-569">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8c5c8-569">Az.Automation</span></span>
* <span data-ttu-id="8c5c8-570">已將 '-RunOn' 參數新增至 'Set-AzAutomationWebhook，以指定混合式背景工作角色群組</span><span class="sxs-lookup"><span data-stu-id="8c5c8-570">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8c5c8-571">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c5c8-571">Az.Compute</span></span>
* <span data-ttu-id="8c5c8-572">已將 '-EncryptionAtHost' 參數新增至 'New-AzVm'、'New-AzVmss'、'New-AzVMConfig'、'New-AzVmssConfig'、'Update-AzVM' 及 'Update-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-572">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="8c5c8-573">已將 'SecurityProfile' 新增至 'Get-AzVM' 和 'Get-AzVmss' 傳回物件</span><span class="sxs-lookup"><span data-stu-id="8c5c8-573">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="8c5c8-574">已將 '-InstanceView' 參數新增為 'Get-AzHostGroup' 的選擇性參數</span><span class="sxs-lookup"><span data-stu-id="8c5c8-574">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="8c5c8-575">已新增 'Invoke-AzVmPatchAssessment' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-575">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8c5c8-576">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8c5c8-576">Az.DataFactory</span></span>
* <span data-ttu-id="8c5c8-577">已將遺漏屬性新增至 PSPipelineRun 類別。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-577">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8c5c8-578">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8c5c8-578">Az.HDInsight</span></span>
* <span data-ttu-id="8c5c8-579">支援建立具有主機加密功能的叢集。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-579">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8c5c8-580">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8c5c8-580">Az.KeyVault</span></span>
* <span data-ttu-id="8c5c8-581">已新增打算停用虛刪除的警告訊息</span><span class="sxs-lookup"><span data-stu-id="8c5c8-581">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="8c5c8-582">已新增打算移除 SecretValueText 屬性的警告訊息</span><span class="sxs-lookup"><span data-stu-id="8c5c8-582">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="8c5c8-583">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="8c5c8-583">Az.Maintenance</span></span>
* <span data-ttu-id="8c5c8-584">已將選擇性的排程相關欄位新增至 'New-AzMaintenanceConfiguration'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-584">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="8c5c8-585">已為 'Get-AzMaintenancePublicConfiguration' 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-585">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="8c5c8-586">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-586">Az.ManagedServices</span></span>
* <span data-ttu-id="8c5c8-587">已在受控服務指派和定義的 Cmdlet 上新增中斷性變更警告</span><span class="sxs-lookup"><span data-stu-id="8c5c8-587">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8c5c8-588">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8c5c8-588">Az.Monitor</span></span>
* <span data-ttu-id="8c5c8-589">已擴充 'Set-AzDiagnosticSetting' 中設定的參數，以分隔記錄和計量啟用 [#12482]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-589">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="8c5c8-590">已修正從管線取得計量警示時的 'Add-AzMetricAlertRuleV2' 錯誤</span><span class="sxs-lookup"><span data-stu-id="8c5c8-590">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="8c5c8-591">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c5c8-591">Az.Resources</span></span>
* <span data-ttu-id="8c5c8-592">已更新 'Get-AzPolicyAlias' 回應以包含指出別名是否可由 Azure 原則修改的資訊。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-592">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="8c5c8-593">已建立新的 'Set-AzRoleAssignment' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-593">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="8c5c8-594">已新增 'Get-AzDeploymentManagementGroupWhatIfResult'，以取得 ARM 範本在管理群組範圍的假設結果</span><span class="sxs-lookup"><span data-stu-id="8c5c8-594">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="8c5c8-595">已新增 'Get-AzTenantWhatIfResult' Cmdlet，以取得 ARM 範本在租使用者範圍的假設結果</span><span class="sxs-lookup"><span data-stu-id="8c5c8-595">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="8c5c8-596">已覆寫 'New-AzManagementGroupDeployment' 和 'New-AzTenantDeployment' 的 '-WhatIf' 和 '-Confirm'，以使用 ARM 範本 What-If 結果</span><span class="sxs-lookup"><span data-stu-id="8c5c8-596">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="8c5c8-597">已修正新部署 Cmdlet 的 '-WhatIf' 和 '-Confirm' 行為，使其符合 False 和</span><span class="sxs-lookup"><span data-stu-id="8c5c8-597">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="8c5c8-598">已修正 '-TemplateObject' 和 'TemplateParameterObject' 的序列化錯誤 [#1528] [#6292]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-598">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="8c5c8-599">已針對即將進行的輸出類型變更，對 'Get-AzResourceGroupDeploymentOperation' 新增中斷性變更屬性</span><span class="sxs-lookup"><span data-stu-id="8c5c8-599">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="8c5c8-600">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="8c5c8-600">Az.SignalR</span></span>
* <span data-ttu-id="8c5c8-601">已修正 'Restart-AzSignalR' 和 'Update-AzSignalR' 說明檔錯誤</span><span class="sxs-lookup"><span data-stu-id="8c5c8-601">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="8c5c8-602">已新增 'Update-AzSignalRNetworkAcl'、'Set-AzSignalRUpstream' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-602">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8c5c8-603">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8c5c8-603">Az.Storage</span></span>
* <span data-ttu-id="8c5c8-604">支援的 Blob 查詢加速</span><span class="sxs-lookup"><span data-stu-id="8c5c8-604">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="8c5c8-605">'Get-AzStorageBlobQueryResult'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-605">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="8c5c8-606">'New-AzStorageBlobQueryConfig'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-606">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="8c5c8-607">已更新說明檔、新增更多描述及修正錯字</span><span class="sxs-lookup"><span data-stu-id="8c5c8-607">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="8c5c8-608">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-608">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="8c5c8-609">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-609">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="8c5c8-610">已修正當相關子目錄不存在時，下載 Blob 會失敗的問題 [#12592]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-610">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="8c5c8-611">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-611">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="8c5c8-612">支援在儲存體帳戶上設定/取得/移除物件複寫原則</span><span class="sxs-lookup"><span data-stu-id="8c5c8-612">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="8c5c8-613">'New-AzStorageObjectReplicationPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-613">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="8c5c8-614">'Set-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-614">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="8c5c8-615">'Get-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-615">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="8c5c8-616">'Remove-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-616">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="8c5c8-617">支援在儲存體帳戶的 Blob 服務上啟用/停用 ChangeFeed</span><span class="sxs-lookup"><span data-stu-id="8c5c8-617">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="8c5c8-618">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-618">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="8c5c8-619">4.5.0 - 2020 年 8 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-619">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8c5c8-620">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8c5c8-620">Az.Accounts</span></span>
* <span data-ttu-id="8c5c8-621">已將 'Connect-AzAccount' 更新為接受參數 'MaxContextPopulation' [#9865]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-621">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="8c5c8-622">已將 SubscriptionClient 版本更新為 2019-06-01 並顯示租用戶網域 [#9838]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-622">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="8c5c8-623">訂用帳戶支援的主租用戶和 managedBy 租用戶資訊</span><span class="sxs-lookup"><span data-stu-id="8c5c8-623">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="8c5c8-624">已更正遙測資料中的模組名稱、版本資訊</span><span class="sxs-lookup"><span data-stu-id="8c5c8-624">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="8c5c8-625">已調整 SqlDatabaseDnsSuffix 和 ServiceManagementUrl (如果環境中繼資料端點傳回不相容的值)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-625">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="8c5c8-626">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="8c5c8-626">Az.Aks</span></span>
* <span data-ttu-id="8c5c8-627">已將 'ClientIdAndSecret' 移除至 'ServicePrincipalIdAndSecret' 並將 'ClientIdAndSecret' 設定為別名 [#12381]。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-627">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="8c5c8-628">已將 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' 移除至 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' 並將原始項目設定為別名 [#12373]。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-628">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8c5c8-629">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8c5c8-629">Az.ApiManagement</span></span>
* <span data-ttu-id="8c5c8-630">已新增新的 'Add-AzApiManagementApiToGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-630">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="8c5c8-631">已新增新的 'Get-AzApiManagementGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-631">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="8c5c8-632">已新增新的 'Get-AzApiManagementGatewayHostnameConfiguration' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-632">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="8c5c8-633">已新增新的 'Get-AzApiManagementGatewayKey' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-633">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="8c5c8-634">已新增新的 'New-AzApiManagementGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-634">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="8c5c8-635">已新增新的 'New-AzApiManagementGatewayHostnameConfiguration' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-635">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="8c5c8-636">已新增新的 'New-AzApiManagementResourceLocationObject' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-636">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="8c5c8-637">已新增新的 'Remove-AzApiManagementApiFromGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-637">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="8c5c8-638">已新增新的 'Remove-AzApiManagementGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-638">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="8c5c8-639">已新增新的 'Remove-AzApiManagementGatewayHostnameConfiguration' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-639">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="8c5c8-640">已新增新的 'Update-AzApiManagementGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-640">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="8c5c8-641">已將新的選擇性 [-GatewayId] 參數新增至 'Get-AzApiManagementApi' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-641">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8c5c8-642">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-642">Az.CognitiveServices</span></span>
* <span data-ttu-id="8c5c8-643">已特別將 'Deny' 作為 NetworkRules 預設動作使用。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-643">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8c5c8-644">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8c5c8-644">Az.FrontDoor</span></span>
* <span data-ttu-id="8c5c8-645">已修正當 Enum.Parse 嘗試將 Null 值強制轉型為 Enabled 或 Disabled 列舉值時擲回例外狀況的問題 [#12344]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-645">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8c5c8-646">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8c5c8-646">Az.HDInsight</span></span>
* <span data-ttu-id="8c5c8-647">支援使用傳輸中加密功能建立叢集。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-647">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="8c5c8-648">將新參數 'EncryptionInTransit' 新增至 Cmdlet 'New-AzHDInsightCluster'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-648">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="8c5c8-649">將新參數 'EncryptionInTransit' 新增至 Cmdlet 'New-AzHDInsightClusterConfig'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-649">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="8c5c8-650">支援使用私人連結功能建立叢集：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-650">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="8c5c8-651">將新參數 'PublicNetworkAccessType' 和 'OutboundPublicNetworkAccessType' 新增至 Cmdlet 'New-AzHDInsightCluster'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-651">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="8c5c8-652">將新參數 'PublicNetworkAccessType' 和 'OutboundPublicNetworkAccessType' 新增至 Cmdlet 'New-AzHDInsightClusterConfig'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-652">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="8c5c8-653">呼叫 'New-AzHDInsightCluster' 或 'Get-AzHDInsightCluster' 時傳回了虛擬網路資訊</span><span class="sxs-lookup"><span data-stu-id="8c5c8-653">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8c5c8-654">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c5c8-654">Az.Network</span></span>
* <span data-ttu-id="8c5c8-655">已將 AddressPrefixType 參數的支援新增至 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-655">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="8c5c8-656">已新增不中斷變更：'Remove-AzExpressRouteCircutPeeringConfig' 中私人對等互連的 PeerAddressType 功能。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-656">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="8c5c8-657">程式碼已變更為忽略 AddressPrefixType 和 PeerAddressType 參數的大小寫。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-657">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="8c5c8-658">已修改 'New-AzLoadBalancerFrontendIpConfig'、'New-AzPublicIpAddress' 和 'New-AzPublicIpPrefix' 的警告訊息。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-658">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8c5c8-659">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8c5c8-659">Az.OperationalInsights</span></span>
* <span data-ttu-id="8c5c8-660">已新增 'Remove-AzOperationalInsightsworkspace' 的 '-ForceDelete' 選項</span><span class="sxs-lookup"><span data-stu-id="8c5c8-660">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="8c5c8-661">已新增新的 Cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-661">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="8c5c8-662">已新增新的 Cmdlet 'Restore-AzOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-662">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8c5c8-663">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-663">Az.RecoveryServices</span></span>
* <span data-ttu-id="8c5c8-664">已改善 Azure 備份容器/項目探索體驗。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-664">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8c5c8-665">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c5c8-665">Az.Resources</span></span>
* <span data-ttu-id="8c5c8-666">已將 'Condition'、'ConditionVersion' 和 'Description' 屬性新增至 'New-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-666">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="8c5c8-667">這包括資料模型的所有相關變更</span><span class="sxs-lookup"><span data-stu-id="8c5c8-667">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="8c5c8-668">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c5c8-668">Az.Sql</span></span>
* <span data-ttu-id="8c5c8-669">已修正 'New-AzSqlServer' 和 'Set-AzSqlServer' 中可能的伺服器名稱不區分大小寫錯誤</span><span class="sxs-lookup"><span data-stu-id="8c5c8-669">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="8c5c8-670">已修正 'New-AzSqlDatabaseSecondary' 中現有資料庫錯誤上傳回的錯誤資料庫名稱</span><span class="sxs-lookup"><span data-stu-id="8c5c8-670">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8c5c8-671">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8c5c8-671">Az.Storage</span></span>
* <span data-ttu-id="8c5c8-672">支援建立具有新權限 x、t 的容器/blob Sas 權杖</span><span class="sxs-lookup"><span data-stu-id="8c5c8-672">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="8c5c8-673">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-673">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="8c5c8-674">'New-AzStorageContainerSASToken'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-674">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="8c5c8-675">支援建立具有新權限 x、t、f 的帳戶 Sas 權杖</span><span class="sxs-lookup"><span data-stu-id="8c5c8-675">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="8c5c8-676">'New-AzStorageAccountSASToken'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-676">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="8c5c8-677">支援取得單一檔案共用使用方式</span><span class="sxs-lookup"><span data-stu-id="8c5c8-677">Supported get single file share usage</span></span>
    - <span data-ttu-id="8c5c8-678">'Get-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-678">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="8c5c8-679">4.4.0 - 2020 年 7 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-679">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8c5c8-680">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8c5c8-680">Az.Accounts</span></span>
* <span data-ttu-id="8c5c8-681">已新增新的 Cmdlet 'Invoke-AzRestMethod'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-681">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="8c5c8-682">已修正在多處理序案例中可能導致驗證錯誤的問題，例如使用 'Start-Job' 執行多個 Azure PowerShell Cmdlet [#9448]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-682">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="8c5c8-683">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="8c5c8-683">Az.Aks</span></span>
* <span data-ttu-id="8c5c8-684">已修正 'Get-AzAks' 無法取得所有叢集的錯誤 (bug) [#12296]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-684">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="8c5c8-685">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-685">Az.AnalysisServices</span></span>
* <span data-ttu-id="8c5c8-686">已移除驗證的專案參考</span><span class="sxs-lookup"><span data-stu-id="8c5c8-686">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8c5c8-687">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8c5c8-687">Az.Automation</span></span>
* <span data-ttu-id="8c5c8-688">已修正具有 escape 字元的字串無法轉換成 json 物件的問題。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-688">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8c5c8-689">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c5c8-689">Az.Compute</span></span>
* <span data-ttu-id="8c5c8-690">在沒有 'latest' 映像版本的情況下使用 'New-AzVmss' 時，新增警告</span><span class="sxs-lookup"><span data-stu-id="8c5c8-690">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8c5c8-691">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8c5c8-691">Az.DataFactory</span></span>
* <span data-ttu-id="8c5c8-692">已將全域參數新增至 Data Factory。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-692">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8c5c8-693">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8c5c8-693">Az.EventGrid</span></span>
* <span data-ttu-id="8c5c8-694">已更新為使用 2020-06-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-694">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="8c5c8-695">加入新功能：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-695">Added new features:</span></span>
    - <span data-ttu-id="8c5c8-696">輸入對應</span><span class="sxs-lookup"><span data-stu-id="8c5c8-696">Input mapping</span></span>
    - <span data-ttu-id="8c5c8-697">事件傳遞結構描述</span><span class="sxs-lookup"><span data-stu-id="8c5c8-697">Event Delivery Schema</span></span>
    - <span data-ttu-id="8c5c8-698">私人連結</span><span class="sxs-lookup"><span data-stu-id="8c5c8-698">Private Link</span></span>
    - <span data-ttu-id="8c5c8-699">雲端事件 V10 結構描述</span><span class="sxs-lookup"><span data-stu-id="8c5c8-699">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="8c5c8-700">將服務匯流排主題作為目的地</span><span class="sxs-lookup"><span data-stu-id="8c5c8-700">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="8c5c8-701">將 Azure Function 作為目的地</span><span class="sxs-lookup"><span data-stu-id="8c5c8-701">Azure Function As Destination</span></span>
    - <span data-ttu-id="8c5c8-702">WebHook 批次處理</span><span class="sxs-lookup"><span data-stu-id="8c5c8-702">WebHook Batching</span></span>
    - <span data-ttu-id="8c5c8-703">安全 Webhook (AAD 支援)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-703">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="8c5c8-704">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="8c5c8-704">IpFiltering</span></span>
* <span data-ttu-id="8c5c8-705">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-705">Updated cmdlets:</span></span>
    - <span data-ttu-id="8c5c8-706">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span><span class="sxs-lookup"><span data-stu-id="8c5c8-706">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="8c5c8-707">新增選擇性參數以支援 webhook 批次處理。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-707">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="8c5c8-708">新增選擇性參數以使用 AAD 支援安全的 Wdblook。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-708">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="8c5c8-709">為 EndpointType 參數新增新的列舉，以支援 Azure 函式和服務匯流排主題作為新的目的地。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-709">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="8c5c8-710">為傳遞結構描述新增選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-710">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="8c5c8-711">'New-AzEventGridTopic'/'Update-AzEventGridTopic' 和 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="8c5c8-711">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="8c5c8-712">新增選擇性參數以支援 IpFiltering。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-712">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="8c5c8-713">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="8c5c8-713">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="8c5c8-714">新增選擇性參數以支援輸入對應。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-714">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8c5c8-715">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8c5c8-715">Az.FrontDoor</span></span>
* <span data-ttu-id="8c5c8-716">已更新模組以使用 API 2020-05-01</span><span class="sxs-lookup"><span data-stu-id="8c5c8-716">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="8c5c8-717">已新增對儲存體、Keyvault 和 Web App Service 資源的私人連結支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-717">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8c5c8-718">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8c5c8-718">Az.HDInsight</span></span>
* <span data-ttu-id="8c5c8-719">支援在國家雲端中建立具有 ADLSGen1/2 儲存體的叢集。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-719">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8c5c8-720">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8c5c8-720">Az.Monitor</span></span>
* <span data-ttu-id="8c5c8-721">已修正計量或記錄為 Null 時，'Get-AzDiagnosticSetting' 的錯誤 (bug) [#12272]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-721">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8c5c8-722">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c5c8-722">Az.Network</span></span>
* <span data-ttu-id="8c5c8-723">已修正 VWan HubVnet 連線中的參數交換</span><span class="sxs-lookup"><span data-stu-id="8c5c8-723">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="8c5c8-724">為 Azure 網路虛擬設備網站新增了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-724">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="8c5c8-725">'Get-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-725">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="8c5c8-726">'New-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-726">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="8c5c8-727">'Remove-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-727">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="8c5c8-728">'Update-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-728">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="8c5c8-729">'New-AzOffice365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-729">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="8c5c8-730">為 Azure 網路虛擬設備新增了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-730">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="8c5c8-731">'Get-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-731">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="8c5c8-732">'New-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-732">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="8c5c8-733">'Remove-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-733">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="8c5c8-734">'Update-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-734">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="8c5c8-735">'Get-AzNetworkVirtualApplianceSku'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-735">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="8c5c8-736">'New-AzVirtualApplianceSkuProperty'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-736">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="8c5c8-737">將應用程式閘道上架至私人連結通用 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-737">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="8c5c8-738">將 StorageSync 上架至私人連結通用 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-738">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="8c5c8-739">將 SignalR 上架至私人連結通用 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-739">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8c5c8-740">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-740">Az.RecoveryServices</span></span>
* <span data-ttu-id="8c5c8-741">已移除驗證的專案參考</span><span class="sxs-lookup"><span data-stu-id="8c5c8-741">Removed project reference to Authentication</span></span>
* <span data-ttu-id="8c5c8-742">Azure 備份微調的 Cmdlet 有助於文字更精確。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-742">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="8c5c8-743">Azure 備份新增了使用 'Get-AzRecoveryServicesBackupJob' Cmdlet 來擷取 MAB 代理程式作業的支援。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-743">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8c5c8-744">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c5c8-744">Az.Resources</span></span>
* <span data-ttu-id="8c5c8-745">已將 'Save-AzResourceGroupDeploymentTemplate' 更新為使用 SDK。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-745">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="8c5c8-746">已新增 'Unregister-AzResourceProvider' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-746">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="8c5c8-747">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c5c8-747">Az.Sql</span></span>
* <span data-ttu-id="8c5c8-748">在 'Set-AzSqlInstanceActiveDirectoryAdministrator' Cmdlet 中新增了服務主體和來賓使用者的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-748">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="8c5c8-749">已修正資料分類 Cmdlet 中的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-749">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="8c5c8-750">已新增 Azure SQL 受控執行個體容錯移轉的支援：'Invoke-AzSqlInstanceFailover'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-750">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8c5c8-751">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8c5c8-751">Az.Storage</span></span>
* <span data-ttu-id="8c5c8-752">已修正未針對某些資料平面 Cmdlet 新增 UserAgent 的問題。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-752">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="8c5c8-753">支援具有 MinimumTlsVersion 和 AllowBlobPublicAccess 的建立/更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="8c5c8-753">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="8c5c8-754">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-754">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="8c5c8-755">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-755">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="8c5c8-756">支援在儲存體帳戶的 Blob 服務上啟用/停用版本控制</span><span class="sxs-lookup"><span data-stu-id="8c5c8-756">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="8c5c8-757">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-757">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="8c5c8-758">支援 Blob 版本的列出 Blob</span><span class="sxs-lookup"><span data-stu-id="8c5c8-758">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="8c5c8-759">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-759">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="8c5c8-760">支援取得/移除單一 Blob 快照集或 Blob 版本</span><span class="sxs-lookup"><span data-stu-id="8c5c8-760">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="8c5c8-761">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-761">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="8c5c8-762">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-762">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="8c5c8-763">支援從 Azure.Storage.Blobs V12 所產生的 Blob 物件管道</span><span class="sxs-lookup"><span data-stu-id="8c5c8-763">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="8c5c8-764">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-764">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="8c5c8-765">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-765">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="8c5c8-766">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-766">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="8c5c8-767">'Set-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-767">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="8c5c8-768">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-768">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="8c5c8-769">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="8c5c8-769">Az.StorageSync</span></span>
* <span data-ttu-id="8c5c8-770">新增了以 ApiVersion 2020-03-01 為目標的新版 StorageSync SDK</span><span class="sxs-lookup"><span data-stu-id="8c5c8-770">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="8c5c8-771">已新增更新儲存體同步服務 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-771">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="8c5c8-772">'Set-AzStorageSyncService'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-772">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="8c5c8-773">已將 IncomingTrafficPolicy 和 PrivateEndpointConnections 新增至 StorageSyncService Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-773">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8c5c8-774">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8c5c8-774">Az.Websites</span></span>
* <span data-ttu-id="8c5c8-775">已新增支援而可針對未和 App Service 方案位於相同資源群組中的插槽執行作業</span><span class="sxs-lookup"><span data-stu-id="8c5c8-775">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="8c5c8-776">4.3.0 - 2020 年 6 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-776">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8c5c8-777">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8c5c8-777">Az.Accounts</span></span>
* <span data-ttu-id="8c5c8-778">預設支援的探索環境設定，並透過 'Add-AzEnvironment' 新增環境</span><span class="sxs-lookup"><span data-stu-id="8c5c8-778">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="8c5c8-779">更新預先載入的組件 [#12024]、[#11976]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-779">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="8c5c8-780">已更新 Azure.Core 組件</span><span class="sxs-lookup"><span data-stu-id="8c5c8-780">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="8c5c8-781">已修正可能導致 'Connect-AzAccount' 在多執行緒執行中失敗的問題 [#11201]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-781">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="8c5c8-782">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="8c5c8-782">Az.Aks</span></span>
* <span data-ttu-id="8c5c8-783">透過對 [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) 和 [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) API 的呼叫，取代舊 [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) 的使用方式</span><span class="sxs-lookup"><span data-stu-id="8c5c8-783">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="8c5c8-784">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8c5c8-784">Az.Batch</span></span>
* <span data-ttu-id="8c5c8-785">已將 Az.Batch 更新為使用 'Microsoft.Azure.Management.Batch' SDK 版本 11.0.0</span><span class="sxs-lookup"><span data-stu-id="8c5c8-785">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="8c5c8-786">新增在 'New-AzBatchAccount' Cmdlet 中設定 BatchAccount 身分識別的功能</span><span class="sxs-lookup"><span data-stu-id="8c5c8-786">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8c5c8-787">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-787">Az.CognitiveServices</span></span>
* <span data-ttu-id="8c5c8-788">支援的顯示帳戶功能。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-788">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="8c5c8-789">支援修改 PublicNetworkAccess。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-789">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8c5c8-790">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c5c8-790">Az.Compute</span></span>
* <span data-ttu-id="8c5c8-791">已將 SimulateEviction 參數新增至 Set-AzVM 和 Set-AzVmssVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-791">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="8c5c8-792">已將 'Premium_LRS' 新增至 New-AzGalleryImageVersion Cmdlet 的 StorageAccountType 參數的引數完成器。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-792">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="8c5c8-793">已將子狀態新增至 VMCustomScriptExtension [#11297]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-793">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="8c5c8-794">已將 'Delete' 新增至 New-AzVM 和 New-AzVMConfig Cmdlet 的 EvictionPolicy 參數的引數完成器。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-794">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="8c5c8-795">已修正適用於 SAP 的新 VM 擴充功能名稱</span><span class="sxs-lookup"><span data-stu-id="8c5c8-795">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8c5c8-796">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8c5c8-796">Az.DataFactory</span></span>
* <span data-ttu-id="8c5c8-797">已將 ADF .Net SDK 版本更新為 4.9.0</span><span class="sxs-lookup"><span data-stu-id="8c5c8-797">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8c5c8-798">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8c5c8-798">Az.EventHub</span></span>
* <span data-ttu-id="8c5c8-799">已將受控識別參數新增至 'New-AzEventHubNamespace' 和 'Set-AzEventHubNamespace' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-799">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="8c5c8-800">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="8c5c8-800">Az.Functions</span></span>
* <span data-ttu-id="8c5c8-801">已新增建立 PowerShell 7.0 和 Java 11 函式應用程式的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-801">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8c5c8-802">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8c5c8-802">Az.HDInsight</span></span>
* <span data-ttu-id="8c5c8-803">支援的清單主機和重新開機 HDInsight 叢集的特定主機。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-803">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="8c5c8-804">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="8c5c8-804">Az.HealthcareApis</span></span>
* <span data-ttu-id="8c5c8-805">已將 SDK 版本更新為 1.1.0</span><span class="sxs-lookup"><span data-stu-id="8c5c8-805">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="8c5c8-806">已新增匯出設定和受控識別的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-806">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8c5c8-807">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8c5c8-807">Az.Monitor</span></span>
* <span data-ttu-id="8c5c8-808">已修正 'Set-AzActivityLogAlert' 的輸入物件參數</span><span class="sxs-lookup"><span data-stu-id="8c5c8-808">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="8c5c8-809">已修正 'Set-AzActionGroup' 的 'InputObject' 參數 [#10868]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-809">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8c5c8-810">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c5c8-810">Az.Network</span></span>
* <span data-ttu-id="8c5c8-811">已將 AddressPrefixType 參數的支援新增至 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-811">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="8c5c8-812">已新增 Azure FirewallPolicy 的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-812">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="8c5c8-813">'New-AzFirewallPolicyDnsSetting'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-813">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="8c5c8-814">在防火牆原則的網路規則中支援目的地 FQDN</span><span class="sxs-lookup"><span data-stu-id="8c5c8-814">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="8c5c8-815">已新增對後端位址集區作業的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-815">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="8c5c8-816">'New-AzLoadBalancerBackendAddressConfig'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-816">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="8c5c8-817">'New-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-817">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="8c5c8-818">'Set-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-818">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="8c5c8-819">'Remove-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-819">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="8c5c8-820">'Get-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-820">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="8c5c8-821">已新增 ' New-AzIpGroup' 的名稱驗證</span><span class="sxs-lookup"><span data-stu-id="8c5c8-821">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="8c5c8-822">已新增 Azure FirewallPolicy 的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-822">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="8c5c8-823">'New-AzFirewallPolicyThreatIntelWhitelist'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-823">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="8c5c8-824">已更新下列功能命令：在 VirtualWan P2SVpnGateway 上設定/移除自訂 dns 伺服器。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-824">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="8c5c8-825">已更新 New-AzP2sVpnGateway：已為客戶新增選擇性參數 '-CustomDnsServer'，以指定要在 P2SVpnGateway 上設定的 dns 伺服器 (可供點對站用戶端使用)。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-825">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="8c5c8-826">已更新 Update-AzP2sVpnGateway：已為客戶新增選擇性參數 '-CustomDnsServer'，以指定要在 P2SVpnGateway 上設定的 dns 伺服器 (可供點對站用戶端使用)。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-826">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="8c5c8-827">已更新 'Update-AzVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-827">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="8c5c8-828">已為客戶新增選擇性參數 '-BgpPeeringAddress'，以指定要在 VpnGateway 上設定的自訂 bgps。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-828">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="8c5c8-829">已新增新的 Cmdlet，以支援重設 VirtualHub 資源的路由狀態：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-829">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="8c5c8-830">'Reset-AzHubRouter'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-830">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="8c5c8-831">已根據防火牆原則的最近 Swagger 變更更新下列事項</span><span class="sxs-lookup"><span data-stu-id="8c5c8-831">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="8c5c8-832">變更 RuleGroup、RuleCollectionGroup 和 RuleType 的名稱</span><span class="sxs-lookup"><span data-stu-id="8c5c8-832">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="8c5c8-833">已新增對防火牆原則 NAT 規則集合的支援，以支援多個 NAT 規則集合</span><span class="sxs-lookup"><span data-stu-id="8c5c8-833">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="8c5c8-834">[重大變更] 已為 'New-AzFirewallPolicyApplicationRule' 和 'New-AzFirewallPolicyNetworkRule' 新增必要參數 'SourceIpGroup'。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-834">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="8c5c8-835">[重大變更] 已修正 'New-AzFirewallPolicyApplicationRule'，參數 'SourceAddress' 會是必要的。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-835">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="8c5c8-836">[重大變更] 已修正 'New-AzFirewallPolicyApplicationRule'，參數 'SourceAddress' 會是必要的。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-836">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="8c5c8-837">[重大變更] 已移除必要參數：'New-AzFirewallPolicyNatRuleCollection' 的 'TranslatedAddress'、'TranslatedPort'。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-837">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="8c5c8-838">已新增 Cmdlet 以在應用程式閘道上支援 PrivateLink</span><span class="sxs-lookup"><span data-stu-id="8c5c8-838">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="8c5c8-839">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-839">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="8c5c8-840">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-840">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="8c5c8-841">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-841">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="8c5c8-842">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-842">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="8c5c8-843">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-843">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="8c5c8-844">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-844">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="8c5c8-845">已為 VirtualHub 的 HubRouteTables 子資源新增了 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-845">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="8c5c8-846">'New-AzVHubRoute'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-846">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="8c5c8-847">'New-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-847">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="8c5c8-848">'Get-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-848">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="8c5c8-849">'Update-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-849">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="8c5c8-850">'Remove-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-850">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="8c5c8-851">已更新現有的 Cmdlet，以支援 VirtualWan 中自訂路由的選擇性 RoutingConfiguration 輸入參數。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-851">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="8c5c8-852">'New-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-852">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="8c5c8-853">'Set-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-853">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="8c5c8-854">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-854">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="8c5c8-855">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-855">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="8c5c8-856">'New-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-856">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="8c5c8-857">'Update-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-857">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="8c5c8-858">'New-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-858">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="8c5c8-859">'Update-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-859">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8c5c8-860">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8c5c8-860">Az.OperationalInsights</span></span>
* <span data-ttu-id="8c5c8-861">已修正 PSWorkspace 未實作 IOperationalInsightsWorkspace 的錯誤 (bug) [#12135]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-861">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="8c5c8-862">已將 'pergb2018' 新增至 'Set-AzOperationalInsightsWorkspace' 中參數 'Sku' 的有效值集</span><span class="sxs-lookup"><span data-stu-id="8c5c8-862">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="8c5c8-863">已將參數 'FunctionParameter' 的別名 'FunctionParameters' 新增至</span><span class="sxs-lookup"><span data-stu-id="8c5c8-863">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="8c5c8-864">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-864">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="8c5c8-865">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-865">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8c5c8-866">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-866">Az.RecoveryServices</span></span>
* <span data-ttu-id="8c5c8-867">Azure 備份新增了提取 MAB 項目的支援。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-867">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="8c5c8-868">Azure Site Recovery 支援磁碟類型 'StandardSSD_LRS'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-868">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="8c5c8-869">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c5c8-869">Az.Resources</span></span>
* <span data-ttu-id="8c5c8-870">已在 'PSADUser' 上新增 'UsageLocation'、'GivenName'、'Surname'、'AccountEnabled'、'MailNickname'、'Mail' [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-870">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="8c5c8-871">已修正 '-Mail' 在 'Get-AzADUser' 上無法運作的問題 [#11981]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-871">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="8c5c8-872">已將 '-ExcludeChangeType' 參數新增至 'Get-AzDeploymentWhatIfResult' 和 'Get-AzResourceGroupDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-872">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="8c5c8-873">已將 '-WhatIfExcludeChangeType' 參數新增至 'New-AzDeployment' 和 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-873">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="8c5c8-874">已更新 'Test-Az\*Deployment' Cmdlet，以顯示更好的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="8c5c8-874">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="8c5c8-875">已針對 deployment create 和 What-If Cmdlet 的 '-Name ' 參數修正說明訊息</span><span class="sxs-lookup"><span data-stu-id="8c5c8-875">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="8c5c8-876">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c5c8-876">Az.Sql</span></span>
* <span data-ttu-id="8c5c8-877">已針對 Set SQL Server Azure Active Directory Admin Cmdlet 新增主體的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-877">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="8c5c8-878">已修正資料分類 Cmdlet 中的同步處理問題。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-878">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="8c5c8-879">支援在 'Set-AzSqlServerActiveDirectoryAdministrator' 上依照郵件搜尋使用者 [#12192]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-879">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8c5c8-880">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8c5c8-880">Az.Storage</span></span>
* <span data-ttu-id="8c5c8-881">支援使用 RequireInfrastructureEncryption 建立儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="8c5c8-881">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="8c5c8-882">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-882">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="8c5c8-883">已將載入 Azure.Core 的邏輯移至 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8c5c8-883">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8c5c8-884">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8c5c8-884">Az.Websites</span></span>
* <span data-ttu-id="8c5c8-885">已新增保護來刪除已建立的 Web 應用程式 (如果還原在 'Restore-AzDeletedWebApp' 中失敗)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-885">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="8c5c8-886">已為 'New-AzWebApp' 和 'New-AzWebAppSlot' 新增 'SourceWebApp.Location'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-886">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="8c5c8-887">已修正無法在 'Set-AzWebApp' 和 'Set-AzWebAppSlot' 中變更容器設定的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-887">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="8c5c8-888">已修正未提供 Get-AzWebApp 的 -Name 時取得 SiteConfig 的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-888">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="8c5c8-889">已新增為 Linux 應用程式建立 ASP 的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-889">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="8c5c8-890">已在資源群組中新增複製的例外狀況</span><span class="sxs-lookup"><span data-stu-id="8c5c8-890">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="8c5c8-891">4.2.0 - 2020 年 6 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-891">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8c5c8-892">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8c5c8-892">Az.Accounts</span></span>
* <span data-ttu-id="8c5c8-893">已修正可能導致 Az 略過 Azure 自動化或 PowerShell 作業中記錄的問題 [#11492]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-893">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="8c5c8-894">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-894">Az.AnalysisServices</span></span>
* <span data-ttu-id="8c5c8-895">已更新資料平面 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="8c5c8-895">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8c5c8-896">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8c5c8-896">Az.ApiManagement</span></span>
* <span data-ttu-id="8c5c8-897">已更新服務管理 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="8c5c8-897">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="8c5c8-898">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="8c5c8-898">Az.Billing</span></span>
* <span data-ttu-id="8c5c8-899">已更新耗用量 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="8c5c8-899">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8c5c8-900">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-900">Az.CognitiveServices</span></span>
* <span data-ttu-id="8c5c8-901">支援 PrivateEndpoint 和 PublicNetworkAccess 控制項。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-901">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="8c5c8-902">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8c5c8-902">Az.DataFactory</span></span>
* <span data-ttu-id="8c5c8-903">已更新資料處理站 V2 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="8c5c8-903">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="8c5c8-904">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="8c5c8-904">Az.DataShare</span></span>
* <span data-ttu-id="8c5c8-905">''Az.DataShare'' 模組正式發行</span><span class="sxs-lookup"><span data-stu-id="8c5c8-905">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="8c5c8-906">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="8c5c8-906">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="8c5c8-907">''Az.DesktopVirtualization'' 模組正式發行</span><span class="sxs-lookup"><span data-stu-id="8c5c8-907">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8c5c8-908">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8c5c8-908">Az.OperationalInsights</span></span>
* <span data-ttu-id="8c5c8-909">已將 SDK 升級至 0.21.0</span><span class="sxs-lookup"><span data-stu-id="8c5c8-909">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="8c5c8-910">已將選用參數新增至</span><span class="sxs-lookup"><span data-stu-id="8c5c8-910">Added optional parameters to</span></span> 
    - <span data-ttu-id="8c5c8-911">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-911">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="8c5c8-912">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-912">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8c5c8-913">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8c5c8-913">Az.PolicyInsights</span></span>
* <span data-ttu-id="8c5c8-914">已更正 'Start-AzPolicyComplianceScan' 的範例 3</span><span class="sxs-lookup"><span data-stu-id="8c5c8-914">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="8c5c8-915">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="8c5c8-915">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="8c5c8-916">已更新 PowerBI Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="8c5c8-916">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="8c5c8-917">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="8c5c8-917">Az.PrivateDns</span></span>
* <span data-ttu-id="8c5c8-918">已更正 Remove-AzPrivateDnsRecordSet 的詳細資訊輸出字串格式</span><span class="sxs-lookup"><span data-stu-id="8c5c8-918">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8c5c8-919">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-919">Az.RecoveryServices</span></span>
* <span data-ttu-id="8c5c8-920">Azure Site Recovery 支援建立復原計畫，以從 xml 輸入區域到區域複寫。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-920">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="8c5c8-921">已更新 SiteRecovery 和備份 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="8c5c8-921">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="8c5c8-922">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c5c8-922">Az.Resources</span></span>
* <span data-ttu-id="8c5c8-923">已將 Tail 參數新增至 Get-AzDeploymentScriptLog 和 Save-AzDeploymentScriptLog Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-923">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="8c5c8-924">已格式化輸出屬性，並將其顯示在 Get-AzDeploymentScript Cmdlet 輸出上</span><span class="sxs-lookup"><span data-stu-id="8c5c8-924">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="8c5c8-925">已將 -DeploymentScriptInputObject parameter 參數重新命名為 -DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="8c5c8-925">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="8c5c8-926">已修正 Cmdlet 訊息中遺漏的檔案/目標名稱。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-926">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="8c5c8-927">已更新資源管理員和標記 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="8c5c8-927">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="8c5c8-928">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c5c8-928">Az.Sql</span></span>
* <span data-ttu-id="8c5c8-929">已將 UsePrivateLinkConnection 新增至 'New-AzSqlSyncGroup'、'Update-AzSqlSyncGroup'、'New-AzSqlSyncMember' 和 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-929">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="8c5c8-930">已將 SyncMemberAzureDatabaseResourceId 新增至 'New-AzSqlSyncMember' 和 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-930">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="8c5c8-931">已將來賓使用者查閱支援新增至 Set SQL Server Azure Active Directory Admin Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-931">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8c5c8-932">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8c5c8-932">Az.Storage</span></span>
* <span data-ttu-id="8c5c8-933">已更新資料平面 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="8c5c8-933">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="8c5c8-934">4.1.0 - 2020 年 5 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-934">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="8c5c8-935">上次發佈版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="8c5c8-935">Highlights since the last release</span></span>
* <span data-ttu-id="8c5c8-936">支援的 PowerShell 版本：Windows PowerShell 5.1、PowerShell Core 6.2.4+、PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="8c5c8-936">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="8c5c8-937">Az.Functions 正式發行</span><span class="sxs-lookup"><span data-stu-id="8c5c8-937">General availability of Az.Functions</span></span> 
* <span data-ttu-id="8c5c8-938">Az.ApiManagement、Az.Batch、Az.Compute、Az.KeyVault、Az.Monitor、Az.Network、Az.OperationalInsights、Az.Resources 和 Az.Storage 具有主要版本</span><span class="sxs-lookup"><span data-stu-id="8c5c8-938">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8c5c8-939">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8c5c8-939">Az.Accounts</span></span>
* <span data-ttu-id="8c5c8-940">已更新 'Add-AzEnvironment' 和 'Set-AzEnvironment' 以接受 'AzureSynapseAnalyticsEndpointResourceId' 和 'AzureSynapseAnalyticsEndpointSuffix' 參數</span><span class="sxs-lookup"><span data-stu-id="8c5c8-940">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="8c5c8-941">已將 Azure.Core 相關組件新增至 Az.Accounts，支援的 PowerShell 平台包括 Windows PowerShell 5.1、PowerShell Core 6.2.4、PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="8c5c8-941">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="8c5c8-942">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="8c5c8-942">Az.Aks</span></span>
* <span data-ttu-id="8c5c8-943">已將 API 版本升級至 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="8c5c8-943">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="8c5c8-944">支援使用 Windows 容器建立 AKS</span><span class="sxs-lookup"><span data-stu-id="8c5c8-944">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="8c5c8-945">已提供新的 Cmdlet：'New-AzAksNodePool'、'Update-AzAksNodePool'、'Remove-AzAksNodePool'、        'Get-AzAksNodePool'、'Install-AzAksKubectl'、'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-945">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8c5c8-946">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8c5c8-946">Az.ApiManagement</span></span>
* <span data-ttu-id="8c5c8-947">'New-AzApiManagement' 與 'Set-AzApiManagement': [-AssignIdentity] 參數已重新命名為 [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-947">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="8c5c8-948">'New-AzApiManagement' 與 'Set-AzApiManagement'：已新增下列參數：[-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-948">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="8c5c8-949">'Get-AzApiManagementProperty'：已重新命名為 'Get-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-949">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="8c5c8-950">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-950">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="8c5c8-951">'New-AzApiManagementProperty'：已重新命名為 'New-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-951">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="8c5c8-952">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-952">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="8c5c8-953">'Set-AzApiManagementProperty'：已重新命名為 'Set-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-953">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="8c5c8-954">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-954">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="8c5c8-955">'Remove-AzApiManagementProperty'：已重新命名為 'Remove-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-955">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="8c5c8-956">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-956">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="8c5c8-957">新增的 'Get-AzApiManagementAuthorizationServerClientSecret' Cmdlet 和 'Get-AzApiManagementAuthorizationServer' 將不再傳回用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-957">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="8c5c8-958">新增的 'AzApiManagementNamedValueSecretValue' Cmdlet 和 'AzApiManagementNamedValue' 將不會傳回密碼值。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-958">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="8c5c8-959">新增的 'Get-AzApiManagementOpenIdConnectProviderClientSecret' Cmdlet 和 'Get-AzApiManagementOpenIdConnectProvider' 將不再傳回用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-959">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="8c5c8-960">新增的 'AzApiManagementSubscriptionKey' Cmdlet 和 'AzApiManagementSubscription' 將不再傳回訂用帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-960">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="8c5c8-961">新增的 'AzApiManagementTenantAccessSecret' Cmdlet 和 'AzApiManagementTenantAccess' 將不再傳回金鑰。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-961">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="8c5c8-962">新增的 'AzApiManagementTenantGitAccessSecret' Cmdlet 和 'AzApiManagementTenantGitAccess' 將不再傳回金鑰。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-962">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="8c5c8-963">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="8c5c8-963">Az.ApplicationInsights</span></span>
* <span data-ttu-id="8c5c8-964">新增的參數：適用於 'New-AzApplicationInsights' 的 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-964">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="8c5c8-965">已建立 Cmdlet 'Update-AzApplicationInsights'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-965">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="8c5c8-966">已針對連結的儲存體帳戶建立 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-966">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="8c5c8-967">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8c5c8-967">Az.Batch</span></span>
* <span data-ttu-id="8c5c8-968">已將 Az.Batch 更新為使用 'Microsoft.Azure.Batch' SDK 版本 13.0.0 和 'Microsoft.Azure.Management.Batch' SDK 版本 9.0.0。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-968">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="8c5c8-969">已新增下列功能：使用新的 '-CertificateKind' 參數選取要新增至 'New-AzBatchCertificate' 的憑證種類。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-969">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="8c5c8-970">已從 'PSApplication' 中移除先前一律為 '' 的 'ApplicationPackages' 屬性。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-970">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="8c5c8-971">現在可以使用 'Get-AzBatchApplicationPackage' 來取出應用程式內的特定套件。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-971">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="8c5c8-972">例如：'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-972">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="8c5c8-973">使用 'New-AzBatchPool' 建立集區時，'PSImageReference' 的 'VirtualMachineImageId' 屬性現在只能參考共用映像庫映像。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-973">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="8c5c8-974">使用 'New-AzBatchPool' 建立集區時，可以使用 'PSNetworkConfiguration' 的新 'PublicIPAddressConfiguration' 屬性來佈建集區，無需公用 IP。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-974">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="8c5c8-975">'PSNetworkConfiguration' 的 'PublicIPs' 屬性也已移至 'PSPublicIPAddressConfiguration'。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-975">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="8c5c8-976">只有當 'IPAddressProvisioningType' 是 'UserManaged' 時，才能指定此屬性。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-976">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8c5c8-977">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c5c8-977">Az.Compute</span></span>
* <span data-ttu-id="8c5c8-978">已將 HostId 參數新增至 'Update-AzVM' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-978">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="8c5c8-979">已更新 'New-AzVMConfig'、'New-AzVmssConfig', 'Update-AzVmss'、'Set-AzVMOperatingSystem' 和 'Set-AzVmssOsProfile' Cmdlet 的說明文件。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-979">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="8c5c8-980">重大變更</span><span class="sxs-lookup"><span data-stu-id="8c5c8-980">Breaking changes</span></span>
    - <span data-ttu-id="8c5c8-981">已從 'Get-AzVMImage' Cmdlet 中移除 FilterExpression 參數。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-981">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="8c5c8-982">已從 'New-AzVmssConfig'、'New-AzVMConfig' 和 'Update-AzVM' Cmdlet 中移除 AssignIdentity 參數。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-982">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="8c5c8-983">已從 'New-AzVmssConfig' 和 'Update-AzVmss' Cmdlet 中移除 AutomaticRepairMaxInstanceRepairsPercent。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-983">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="8c5c8-984">已從 ProximityPlacementGroup 中移除 AvailabilitySetsColocationStatus、VirtualMachinesColocationStatus 和 VirtualMachineScaleSetsColocationStatus。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-984">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="8c5c8-985">已從 AutomaticRepairsPolicy 中移除 MaxInstanceRepairsPercent 屬性。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-985">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="8c5c8-986">AvailabilitySets、VirtualMachines 和 VirtualMachineScaleSets 的類型已從 IList<SubResource> 變更為 IList<SubResourceWithColocationStatus>。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-986">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="8c5c8-987">已更新 ' Update-azvm ' Cmdlet 的描述，以提供更好的描述。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-987">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="8c5c8-988">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8c5c8-988">Az.DataFactory</span></span>
* <span data-ttu-id="8c5c8-989">支援受控 IR 中資料流程執行階段屬性的 CRUD。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-989">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8c5c8-990">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8c5c8-990">Az.FrontDoor</span></span>
* <span data-ttu-id="8c5c8-991">已新增用於建立、更新、取出及刪除 Front Door 規則引擎物件的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-991">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="8c5c8-992">已新增用於建構 Front Door 規則引擎物件的協助程式 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-992">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="8c5c8-993">已將規則引擎參考新增至 Front Door 路由規則物件。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-993">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="8c5c8-994">已將私人連結參數新增至 Front Door 後端物件</span><span class="sxs-lookup"><span data-stu-id="8c5c8-994">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="8c5c8-995">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="8c5c8-995">Az.Functions</span></span>
* <span data-ttu-id="8c5c8-996">''Az.Functions'' 模組正式發行</span><span class="sxs-lookup"><span data-stu-id="8c5c8-996">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8c5c8-997">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8c5c8-997">Az.HDInsight</span></span>
* <span data-ttu-id="8c5c8-998">支援客戶管理的金鑰磁碟加密。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-998">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="8c5c8-999">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="8c5c8-999">Az.HealthcareApis</span></span>
* <span data-ttu-id="8c5c8-1000">存取原則不再預設為目前的主體</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1000">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8c5c8-1001">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1001">Az.IotHub</span></span>
* <span data-ttu-id="8c5c8-1002">已新增 Cmdlet 來叫用 IoT 中樞內的查詢，以使用類似 SQL 的語言來取出資訊。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1002">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="8c5c8-1003">已修正下列問題：沒有子裝置，'Add-AzIotHubDevice' 無法建立已啟用 Edge 的裝置 [#11597]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1003">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="8c5c8-1004">已新增 Cmdlet 來產生 Iot 中樞、裝置或模組的 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1004">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="8c5c8-1005">已新增 Cmdlet 來叫用設定計量查詢。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1005">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="8c5c8-1006">管理大規模的 IoT Edge 自動部署。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1006">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="8c5c8-1007">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1007">New cmdlets are:</span></span>
    - <span data-ttu-id="8c5c8-1008">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1008">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="8c5c8-1009">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1009">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="8c5c8-1010">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1010">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="8c5c8-1011">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1011">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="8c5c8-1012">已新增 Cmdlet 來叫用 IoT Edge 部署計量查詢。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1012">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="8c5c8-1013">已新增 Cmdlet 將設定內容套用至指定的邊緣裝置。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1013">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8c5c8-1014">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1014">Az.KeyVault</span></span>
* <span data-ttu-id="8c5c8-1015">已移除兩個別名：'New-AzKeyVaultCertificateAdministratorDetails' 和 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1015">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="8c5c8-1016">建立金鑰保存庫時，依預設會啟用虛刪除</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1016">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="8c5c8-1017">在建立金鑰保存庫時，可以設定網路規則，以管理來自特定網路位置的協助工具</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1017">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="8c5c8-1018">已新增攜帶您自己的金鑰 (BYOK) 的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1018">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="8c5c8-1019">'Add-AzKeyVaultKey' 支援產生金鑰交換金鑰</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1019">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="8c5c8-1020">'Get-AzKeyVaultKey' 支援以 PEM 格式下載公開金鑰</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1020">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="8c5c8-1021">已更新 'Add-AzKeyVaultKey' 說明文件的 'KeyOps' 部分</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1021">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8c5c8-1022">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1022">Az.Monitor</span></span>
* <span data-ttu-id="8c5c8-1023">已修正 'AzDiagnosticSettings' 的下列錯誤 (bug)：保留原則不會套用到所有類別 [#11589]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1023">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="8c5c8-1024">計量警示 V2 支援 WebTest 可用性準則</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1024">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="8c5c8-1025">'New-AzMetricAlertRuleV2Criteria'：已新增建立 webtest 可用性準則的選項</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1025">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="8c5c8-1026">'Add-AzMetricAlertRuleV2'：支援新的 webtest 可用性準則</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1026">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="8c5c8-1027">已移除 PSLogProfile 中 RetentionPolicy 的備援定義 [#7608]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1027">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="8c5c8-1028">已移除 PSEventData 中定義的備援屬性 [#11353]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1028">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="8c5c8-1029">已將 'Get-AzLog' 重新命名為 'Get-AzActivityLog'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1029">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8c5c8-1030">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1030">Az.Network</span></span>
* <span data-ttu-id="8c5c8-1031">已新增重大變更屬性，以通知區域預設行為將會變更</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1031">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="8c5c8-1032">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1032">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="8c5c8-1033">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1033">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="8c5c8-1034">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1034">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="8c5c8-1035">已新增最上層資源 SecurityPartnerProvider 的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1035">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="8c5c8-1036">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1036">New cmdlets added:</span></span>
        - <span data-ttu-id="8c5c8-1037">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1037">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="8c5c8-1038">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1038">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="8c5c8-1039">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1039">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="8c5c8-1040">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1040">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="8c5c8-1041">已在 'PSPrivateLinkResource' 上新增 'RequiredZoneNames'，並在 'PSPrivateEndpointConnection' 上新增 'GroupId'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1041">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="8c5c8-1042">已針對 New-AzNetworkWatcherConnectionMonitorTestConfigurationObject 修正 SuccessThresholdRoundTripTimeMs 參數的不正確類型</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1042">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="8c5c8-1043">已更新 VirtualWan Cmdlet，將 AllowVnetToVnetTraffic 引數的預設值設為 True。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1043">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="8c5c8-1044">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1044">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="8c5c8-1045">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1045">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="8c5c8-1046">已新增 Cmdlet 來支援私人端點的 DNS 區域群組</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1046">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="8c5c8-1047">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1047">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="8c5c8-1048">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1048">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="8c5c8-1049">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1049">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="8c5c8-1050">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1050">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="8c5c8-1051">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1051">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="8c5c8-1052">已將 'DNSEnableProxy'、'DNSRequireProxyForNetworkRules' 和 'DNSServers' 參數新增至 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1052">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="8c5c8-1053">已將 'EnableDnsProxy'、'DnsProxyNotRequiredForNetworkRule' 和 'DnsServer' 參數新增至 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1053">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="8c5c8-1054">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1054">Updated cmdlet:</span></span>
        - <span data-ttu-id="8c5c8-1055">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1055">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8c5c8-1056">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1056">Az.OperationalInsights</span></span>
* <span data-ttu-id="8c5c8-1057">已更新舊版程式碼以套用新產生的 SDK</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1057">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="8c5c8-1058">由於已取代 API，刪除了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1058">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="8c5c8-1059">'Get-AzOperationalInsightsSavedSearchResult' (別名 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1059">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="8c5c8-1060">'Get-AzOperationalInsightsSearchResult' (別名 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1060">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="8c5c8-1061">'Get-AzOperationalInsightsLinkTarget' (別名 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1061">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="8c5c8-1062">已新增 'Set-AzOperationalInsightsWorkspace' 和 'New-AzOperationalInsightsWorkspace' 的參數</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1062">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="8c5c8-1063">已針對連結的儲存體帳戶建立 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1063">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="8c5c8-1064">已針對叢集和連結服務建立 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1064">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8c5c8-1065">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1065">Az.RecoveryServices</span></span>
* <span data-ttu-id="8c5c8-1066">Azure Site Recovery 已將保護 Azure 鄰近放置群組虛擬機器的支援新增至 Azure 提供者。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1066">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="8c5c8-1067">Azure Site Recovery 已將區域的支援新增至區域複本。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1067">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="8c5c8-1068">Azure 備份已新增適用於 Azure FileShare 復原點的長期保留支援。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1068">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="8c5c8-1069">Azure 備份已將磁片排除屬性新增至 'Get-AzRecoveryServicesBackupItem' Cmdlet 輸出。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1069">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="8c5c8-1070">已針對站台復原服務新增保存庫認證檔的私人端點。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1070">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8c5c8-1071">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1071">Az.Resources</span></span>
* <span data-ttu-id="8c5c8-1072">已新增有關在建立新角色定義時檢視延遲的訊息警告</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1072">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="8c5c8-1073">已變更原則 Cmdlet 以輸出強型別物件</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1073">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="8c5c8-1074">已移除用於 'Get-AzResourceLock' Cmdlet 的 '-TenantLevel ' 參數 [#11335]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1074">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="8c5c8-1075">已修正 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1075">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="8c5c8-1076">已新增在資源群組範圍中取得 ARM 範本 What-If 結果的 Cmdlet：'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1076">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="8c5c8-1077">已新增在訂用帳戶範圍中取得 ARM 範本 What-If 結果的 Cmdlet：'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1077">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="8c5c8-1078">Alias:'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1078">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="8c5c8-1079">已覆寫 'New-AzDeployment' 和 'New-AzResourceGroupDeployment' 的 '-WhatIf' 和 '-Confirm' 參數，以使用 ARM 範本 What-If 結果</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1079">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="8c5c8-1080">已在部署 Cmdlet 中新增 'ApiVersion' 參數的取代訊息</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1080">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="8c5c8-1081">已新增為部署失敗顯示已改善錯誤訊息的功能</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1081">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="8c5c8-1082">已新增針對部署失敗記錄的 correlationId</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1082">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="8c5c8-1083">已將 'error' 屬性新增至部署指令碼輸出</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1083">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="8c5c8-1084">已將 nuget Microsoft.Azure.Management.ResourceManager 更新為 '3.7.1-preview'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1084">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="8c5c8-1085">當 DeploymentValidateResult 中的 Error 屬性變更為唯讀時，已從 nuget 3.7.1-preview 中移除特定測試案例</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1085">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="8c5c8-1086">已從 SDK ResourceManager 3.7.1-preview 引進 GenericResourceExpanded</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1086">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="8c5c8-1087">已針對用於部署的所有 Get Cmdlet 以及下列 Cmdlet 新增標籤支援：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1087">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="8c5c8-1088">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1088">'New-AzDeployment'</span></span>
    - <span data-ttu-id="8c5c8-1089">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1089">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="8c5c8-1090">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1090">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="8c5c8-1091">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1091">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8c5c8-1092">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1092">Az.ServiceFabric</span></span>
* <span data-ttu-id="8c5c8-1093">已修正下列錯誤 (bug)：使用 --SecretIdentifier 新增憑證時取得錯誤憑證指紋</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1093">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="8c5c8-1094">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1094">Az.Sql</span></span>
* <span data-ttu-id="8c5c8-1095">增強下列項目的效能：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1095">Enhance performance of:</span></span>
    - <span data-ttu-id="8c5c8-1096">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1096">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="8c5c8-1097">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1097">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="8c5c8-1098">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1098">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="8c5c8-1099">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1099">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="8c5c8-1100">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1100">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="8c5c8-1101">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1101">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="8c5c8-1102">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1102">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="8c5c8-1103">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1103">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="8c5c8-1104">已從 Cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy' 移除 'RetentionDays' 參數的用戶端驗證</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1104">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="8c5c8-1105">在 Vnet 中對儲存體帳戶進行稽核時，修正在建立儲存體 Blob 資料參與者角色時發生的錯誤。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1105">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8c5c8-1106">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1106">Az.Storage</span></span>
* <span data-ttu-id="8c5c8-1107">已新增 '-AsJob' 以取得/列出帳戶 Cmdlet 'Get-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1107">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="8c5c8-1108">使用 KeyvaultEncryption 更新儲存體帳戶以支援金鑰自動輪替時，使 KeyVersion 成為選用項目</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1108">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="8c5c8-1109">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1109">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="8c5c8-1110">已修正由於管道無法移除 Azure 檔案目錄的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1110">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="8c5c8-1111">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1111">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="8c5c8-1112">已修正 [#9880]：變更 NetWorkRule DefaultAction 值定義以符合 Swagger。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1112">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="8c5c8-1113">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1113">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="8c5c8-1114">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1114">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="8c5c8-1115">已修正 [#11624]：新增 NetworkRules 時跳過重複的規則，以避免伺服器失敗</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1115">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="8c5c8-1116">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1116">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="8c5c8-1117">已將 Microsoft.Azure.Cosmos.Table SDK 升級至 1.0.7</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1117">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="8c5c8-1118">已新增警告訊息，以在清單 DataLake Gen2 項目中只傳回部分項目時，提醒使用者再次與 ContinuationToken 一起列出</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1118">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="8c5c8-1119">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1119">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="8c5c8-1120">已支援使用 Azure Files Active Directory 網域服務驗證來建立或更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1120">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="8c5c8-1121">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1121">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="8c5c8-1122">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1122">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="8c5c8-1123">支援新增或列出儲存體帳戶的 Kerberos 金鑰</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1123">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="8c5c8-1124">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1124">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="8c5c8-1125">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1125">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="8c5c8-1126">支援容錯移轉儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1126">Supported failover Storage account</span></span>
    - <span data-ttu-id="8c5c8-1127">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1127">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="8c5c8-1128">已更新 'Get-AzStorageBlobCopyState' 的說明</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1128">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="8c5c8-1129">已更新 'Get-AzStorageFileCopyState' 和 'Start-AzStorageBlobCopy' 的說明</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1129">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="8c5c8-1130">已將儲存體用戶端程式庫 v12 整合到佇列和檔案 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1130">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="8c5c8-1131">已將輸出類型從 CloudFile 變更為 AzureStorageFile，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1131">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="8c5c8-1132">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1132">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="8c5c8-1133">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1133">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="8c5c8-1134">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1134">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="8c5c8-1135">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1135">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="8c5c8-1136">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1136">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="8c5c8-1137">已將輸出類型從 CloudFileDirectory 變更為 AzureStorageFileDirectory，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1137">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="8c5c8-1138">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1138">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="8c5c8-1139">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1139">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="8c5c8-1140">已將輸出類型從 CloudFileShare 變更為 AzureStorageFileShare，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1140">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="8c5c8-1141">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1141">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="8c5c8-1142">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1142">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="8c5c8-1143">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1143">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="8c5c8-1144">已將輸出類型從 FileShareProperties 變更為 AzureStorageFileShare，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1144">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="8c5c8-1145">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1145">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="8c5c8-1146">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1146">Az.TrafficManager</span></span>
* <span data-ttu-id="8c5c8-1147">已修正 'DisableAzureTrafficManagerEndpoint' 詳細資訊輸出中不正確的設定檔名稱</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1147">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8c5c8-1148">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1148">Az.Websites</span></span>
* <span data-ttu-id="8c5c8-1149">已修正 'Update-AzWebAppAccessRestrictionConfig' 說明上的錯字。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1149">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="8c5c8-1150">3.8.0 - 2020 年 4 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1150">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="8c5c8-1151">上次發佈版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1151">Highlights since the last release</span></span>
* <span data-ttu-id="8c5c8-1152">Az.Storage 支援的 PowerShell 版本：Windows PowerShell 5.1、PowerShell Core 6.2.4+、PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1152">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8c5c8-1153">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1153">Az.Accounts</span></span>
* <span data-ttu-id="8c5c8-1154">更新 'Resolve-AzError' 中的 Azure PowerShell 問卷 URL [#11507]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1154">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8c5c8-1155">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1155">Az.ApiManagement</span></span>
* <span data-ttu-id="8c5c8-1156">在未來版本中新增 Azure 檔案 Cmdlet 輸出變更的重大變更通知</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1156">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="8c5c8-1157">'Set-AzApiManagementGroup' 已更新文件以指定 GroupId 參數</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1157">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8c5c8-1158">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1158">Az.Cdn</span></span>
* <span data-ttu-id="8c5c8-1159">已修正 ChinaCDN 相關的定價 SKU 顯示</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1159">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8c5c8-1160">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1160">Az.CognitiveServices</span></span>
* <span data-ttu-id="8c5c8-1161">支援身分識別、加密、UserOwnedStorage</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1161">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8c5c8-1162">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1162">Az.Compute</span></span>
* <span data-ttu-id="8c5c8-1163">已新增 'Set-AzVmssOrchestrationServiceState' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1163">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="8c5c8-1164">具有 -InstanceView 的 'Get-AzVmss' 會顯示 OrchestrationService 狀態。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1164">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8c5c8-1165">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1165">Az.IotHub</span></span>
* <span data-ttu-id="8c5c8-1166">管理 IoT 裝置對應項設定，新的 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1166">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="8c5c8-1167">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1167">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="8c5c8-1168">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1168">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="8c5c8-1169">已新增 Cmdlet，可在 IoT 中樞的裝置上叫用直接方法。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1169">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="8c5c8-1170">管理 IoT 裝置模組對應項設定，新的 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1170">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="8c5c8-1171">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1171">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="8c5c8-1172">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1172">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="8c5c8-1173">大規模管理 IoT 自動裝置管理設定。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1173">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="8c5c8-1174">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1174">New cmdlets are:</span></span>
    - <span data-ttu-id="8c5c8-1175">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1175">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="8c5c8-1176">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1176">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="8c5c8-1177">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1177">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="8c5c8-1178">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1178">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="8c5c8-1179">已新增 Cmdlet，叫用 IoT 中樞的邊緣模組方法。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1179">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8c5c8-1180">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1180">Az.KeyVault</span></span>
* <span data-ttu-id="8c5c8-1181">已新增可在保存庫上啟用虛刪除和清除保護的新 Cmdlet 'Update-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1181">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="8c5c8-1182">已將支援新增至 Microsoft.PowerShell.SecretManagement [#11178]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1182">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="8c5c8-1183">已修正 'Remove-AzKeyVaultManagedStorageSasDefinition' 範例中的錯誤 [#11479]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1183">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="8c5c8-1184">已將支援新增至私人端點</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1184">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="8c5c8-1185">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1185">Az.Maintenance</span></span>
* <span data-ttu-id="8c5c8-1186">發行用於 GA 的維護 Cmdlet 版本</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1186">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8c5c8-1187">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1187">Az.Monitor</span></span>
* <span data-ttu-id="8c5c8-1188">已新增私人連結範圍的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1188">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="8c5c8-1189">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1189">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="8c5c8-1190">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1190">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="8c5c8-1191">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1191">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="8c5c8-1192">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1192">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="8c5c8-1193">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1193">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="8c5c8-1194">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1194">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="8c5c8-1195">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1195">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8c5c8-1196">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1196">Az.Network</span></span>
* <span data-ttu-id="8c5c8-1197">已更新 Cmdlet，可在私人 IP 上啟用虛擬網路閘道的連線。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1197">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="8c5c8-1198">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1198">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="8c5c8-1199">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1199">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="8c5c8-1200">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1200">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="8c5c8-1201">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1201">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="8c5c8-1202">已更新 Cmdlet，可啟用以 FQDN 為基礎的 LocalNetworkGateways 和 VpnSites</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1202">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="8c5c8-1203">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1203">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="8c5c8-1204">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1204">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="8c5c8-1205">已在 ExpressRouteCircuitConnectionConfig 中新增對 IPv6 位址系列的支援 (全球適用)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1205">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="8c5c8-1206">已新增 'Set-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1206">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="8c5c8-1207">允許設定所有現有屬性，包括 IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1207">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="8c5c8-1208">已更新 'Add-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1208">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="8c5c8-1209">已新增另一個選擇性參數 AddressPrefixType 來指定位址首碼的位址系列</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1209">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="8c5c8-1210">已更新 Cmdlet，可啟用虛擬網路閘道連線上的 DPD 逾時設定。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1210">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="8c5c8-1211">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1211">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="8c5c8-1212">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1212">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8c5c8-1213">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1213">Az.PolicyInsights</span></span>
* <span data-ttu-id="8c5c8-1214">已新增用於觸發原則合規性掃描的 'Start-AzPolicyComplianceScan' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1214">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="8c5c8-1215">已將原則定義、設定定義和指派版本新增至 'Get-AzPolicyState' 輸出</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1215">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8c5c8-1216">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1216">Az.ServiceFabric</span></span>
* <span data-ttu-id="8c5c8-1217">已改善 'New-AzServiceFabricCluster' 範例的程式碼格式設定和可用性</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1217">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="8c5c8-1218">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1218">Az.Sql</span></span>
* <span data-ttu-id="8c5c8-1219">已新增 'Get-AzSqlInstanceOperation' 和 'Stop-AzSqlInstanceOperation' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1219">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="8c5c8-1220">支援對 VNet 中的儲存體帳戶進行稽核。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1220">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8c5c8-1221">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1221">Az.Storage</span></span>
* <span data-ttu-id="8c5c8-1222">在未來版本中新增 Azure 檔案 Cmdlet 輸出變更的重大變更通知</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1222">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="8c5c8-1223">建立/更新儲存體帳戶時，支援新的 SkuName StandardGZRS、StandardRAGZRS</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1223">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="8c5c8-1224">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1224">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="8c5c8-1225">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1225">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="8c5c8-1226">支援 DataLake Gen2</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1226">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="8c5c8-1227">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1227">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="8c5c8-1228">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1228">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="8c5c8-1229">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1229">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="8c5c8-1230">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1230">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="8c5c8-1231">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1231">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="8c5c8-1232">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1232">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="8c5c8-1233">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1233">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="8c5c8-1234">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1234">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="8c5c8-1235">0.10.0-preview - 2020 年 4 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1235">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="8c5c8-1236">一般</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1236">General</span></span>
* <span data-ttu-id="8c5c8-1237">Az 模組現已在 Azure Stack Hub 中提供預覽。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1237">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="8c5c8-1238">此模組具有 Linux 和 macOs 的跨平台相容性。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1238">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="8c5c8-1239">Azure Stack Hub 現在支援使用 Az 模組的 PowerShell Core，如需詳細資訊，請參閱[這裡](https://aka.ms/az4AzureStack)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1239">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="8c5c8-1240">Az 模組支援 2019-03-01-hybrid 設定檔：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1240">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="8c5c8-1241">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1241">Az.Billing</span></span>
  - <span data-ttu-id="8c5c8-1242">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1242">Az.Compute</span></span>
  - <span data-ttu-id="8c5c8-1243">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1243">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="8c5c8-1244">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1244">Az.EventHub</span></span>
  - <span data-ttu-id="8c5c8-1245">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1245">Az.IotHub</span></span>
  - <span data-ttu-id="8c5c8-1246">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1246">Az.KeyVault</span></span>
  - <span data-ttu-id="8c5c8-1247">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1247">Az.Monitor</span></span>
  - <span data-ttu-id="8c5c8-1248">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1248">Az.Network</span></span>
  - <span data-ttu-id="8c5c8-1249">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1249">Az.Resources</span></span>
  - <span data-ttu-id="8c5c8-1250">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1250">Az.Storage</span></span>
  - <span data-ttu-id="8c5c8-1251">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1251">Az.Websites</span></span>
* <span data-ttu-id="8c5c8-1252">已引進三個可搭配 Azure Stack Hub 且適用於 az 的新 PowerShell 模組，包括 Az.Databox、Az.IotHub 和 Az. EventHub</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1252">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="8c5c8-1253">命令維持不變，但有次要變更，例如將 AzureRM 變更為 Az</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1253">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="8c5c8-1254">您可以在[這裡](https://aka.ms/InstallASHPowerShell)找到 Azure Stack Hub 的 PowerShell 文件更新連結</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1254">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="8c5c8-1255">3.7.0 - 2020 年 3 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1255">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8c5c8-1256">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1256">Az.Accounts</span></span>
* <span data-ttu-id="8c5c8-1257">已修正 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' 在未登入時擲回 NullReferenceException [#10292]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1257">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8c5c8-1258">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1258">Az.Compute</span></span>
* <span data-ttu-id="8c5c8-1259">已將下列參數新增至 'New-AzDiskConfig' Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1259">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="8c5c8-1260">DiskIOPSReadOnly、DiskMBpsReadOnly、MaxSharesCount、GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1260">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="8c5c8-1261">允許 'New-AzGalleryImageVersion' Cmdlet 目標參數的加密屬性。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1261">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="8c5c8-1262">已修正 'Set-AzVmss' -Reimage 和 'Invoke-AzVMReimage' Cmdlet 的 tempDisk 問題。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1262">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="8c5c8-1263">[#11354]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1263">[#11354]</span></span>
* <span data-ttu-id="8c5c8-1264">已針對新的 SAP 延伸模組，將支援新增至下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1264">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="8c5c8-1265">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1265">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="8c5c8-1266">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1266">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="8c5c8-1267">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1267">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="8c5c8-1268">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1268">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="8c5c8-1269">已修正說明文件範例中的錯誤</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1269">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="8c5c8-1270">以表格格式顯示 VM PowerState 的確切字串值。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1270">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="8c5c8-1271">'New-AzVmssConfig'：已修正當 SinglePlacementGroup 停用時 AutomaticRepairs 屬性的序列化。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1271">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="8c5c8-1272">[#11257]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1272">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8c5c8-1273">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1273">Az.DataFactory</span></span>
* <span data-ttu-id="8c5c8-1274">已將 ADF .Net SDK 版本更新為 4.8.0</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1274">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="8c5c8-1275">已將選擇性參數新增至 'Invoke-AzDataFactoryV2Pipeline' 命令以支援重新執行</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1275">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8c5c8-1276">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1276">Az.DataLakeStore</span></span>
* <span data-ttu-id="8c5c8-1277">已新增 'Export-AzDataLakeStoreItem' 和 'Import-AzDataLakeStoreItem' 的中斷性變更描述</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1277">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="8c5c8-1278">已新增 'New-AzDataLakeStoreItem'、'Add-AzDAtaLakeStoreItemContent' 和 'Get-AzDAtaLakeStoreItemContent' 的位元組編碼選項</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1278">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8c5c8-1279">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1279">Az.HDInsight</span></span>
* <span data-ttu-id="8c5c8-1280">支援在建立叢集時指定支援的最低 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1280">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8c5c8-1281">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1281">Az.IotHub</span></span>
* <span data-ttu-id="8c5c8-1282">已新增管理每一部裝置的分散式設定支援。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1282">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="8c5c8-1283">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1283">New Cmdlets are:</span></span>
    - <span data-ttu-id="8c5c8-1284">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1284">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="8c5c8-1285">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1285">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8c5c8-1286">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1286">Az.KeyVault</span></span>
* <span data-ttu-id="8c5c8-1287">已將中斷性變更屬性新增至 'New-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1287">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8c5c8-1288">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1288">Az.Monitor</span></span>
* <span data-ttu-id="8c5c8-1289">已更新 'New-AzScheduledQueryRuleLogMetricTrigger' 的文件</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1289">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8c5c8-1290">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1290">Az.Network</span></span>
* <span data-ttu-id="8c5c8-1291">已更新 Cmdlet 以允許跨租用戶 VirtualHubVnetConnections</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1291">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="8c5c8-1292">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1292">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="8c5c8-1293">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1293">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="8c5c8-1294">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1294">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="8c5c8-1295">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1295">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="8c5c8-1296">已移除 SQL 管理 SDK 相依性</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1296">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8c5c8-1297">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1297">Az.PolicyInsights</span></span>
* <span data-ttu-id="8c5c8-1298">改善錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1298">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8c5c8-1299">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1299">Az.RecoveryServices</span></span>
* <span data-ttu-id="8c5c8-1300">Azure Site Recovery 已新增重新保護的支援，並且已更新 Azure 磁碟加密虛擬機器的 VM 屬性。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1300">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="8c5c8-1301">已新增 Azure Site Recovery VmwareToAzure 屬性 DR 監視</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1301">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="8c5c8-1302">Azure 備份已新增針對失敗項目重試原則更新的支援。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1302">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="8c5c8-1303">Azure 備份已新增在備份和還原期間對磁碟排除設定的支援。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1303">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="8c5c8-1304">Azure 備份已新增在 AzureFileShare 中還原多個檔案/資料夾的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1304">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="8c5c8-1305">Azure 備份已新增在更新 IaasVM 原則時對使用者指定 Resourcegroup 支援的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1305">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="8c5c8-1306">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1306">Az.Resources</span></span>
* <span data-ttu-id="8c5c8-1307">已修正 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' 以使用實際的資源 apiVersion，而不是預設 apiVersion [#11267]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1307">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="8c5c8-1308">已新增對於錯誤案例的 correlationId 記錄</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1308">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="8c5c8-1309">小型文件變更為 'Get-AzResourceLock'。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1309">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="8c5c8-1310">已新增範例。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1310">Added example.</span></span>
* <span data-ttu-id="8c5c8-1311">已逸出 'Get-AzADUser' 參數值中的單引號 [#11317]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1311">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="8c5c8-1312">已新增部署指令碼 ('Get-AzDeploymentScript'、'Get-AzDeploymentScriptLog'、'Save-AzDeploymentScriptLog'、'Remove-AzDeploymentScript') 的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1312">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="8c5c8-1313">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1313">Az.Sql</span></span>
* <span data-ttu-id="8c5c8-1314">已將可讀取次要參數新增至 'Invoke-AzSqlDatabaseFailover'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1314">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="8c5c8-1315">已新增 Cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1315">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="8c5c8-1316">已儲存在資料庫中分類資料行時的敏感度等級。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1316">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="8c5c8-1317">Az.Support</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1317">Az.Support</span></span>
* <span data-ttu-id="8c5c8-1318">'Az.Support' 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1318">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8c5c8-1319">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1319">Az.Websites</span></span>
* <span data-ttu-id="8c5c8-1320">已透過以下新 Cmdlet 新增使用 webapp 流量路由規則的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1320">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="8c5c8-1321">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1321">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="8c5c8-1322">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1322">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="8c5c8-1323">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1323">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="8c5c8-1324">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1324">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="8c5c8-1325">3.6.1 - 2020 年 3 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1325">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8c5c8-1326">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1326">Az.Accounts</span></span>
* <span data-ttu-id="8c5c8-1327">在 'Send-Feedback' 中開啟 Azure PowerShell 問卷頁面 [#11020]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1327">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="8c5c8-1328">在 'Resolve-Error' 中顯示 Azure PowerShell 問卷 URL [#11021]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1328">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="8c5c8-1329">已在 UserAgent 中新增 Az 版本</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1329">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8c5c8-1330">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1330">Az.ApiManagement</span></span>
* <span data-ttu-id="8c5c8-1331">已新增可在 DeveloperPortal 端點上擷取和設定自訂網域的支援 [#11007]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1331">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="8c5c8-1332">'Export-AzApiManagementApi' 已新增以 JSON 格式下載 API 定義的支援 [#9987]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1332">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="8c5c8-1333">'Import-AzApiManagementApi' 已新增從 JSON 文件匯入 OpenAPI 3.0 定義的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1333">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="8c5c8-1334">'New-AzApiManagementIdentityProvider' 和 'Set-AzApiManagementIdentityProvider' 已新增為 AAD B2C 提供者設定「登入租用戶」的支援 [#9784]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1334">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8c5c8-1335">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1335">Az.DataLakeStore</span></span>
* <span data-ttu-id="8c5c8-1336">已在 csproj 和 psd1 中明確新增對 System.Buffers 的參考。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1336">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8c5c8-1337">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1337">Az.IotHub</span></span>
* <span data-ttu-id="8c5c8-1338">已新增在 IoT 中樞中管理裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1338">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="8c5c8-1339">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1339">New Cmdlets are:</span></span>
    - <span data-ttu-id="8c5c8-1340">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1340">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="8c5c8-1341">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1341">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="8c5c8-1342">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1342">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="8c5c8-1343">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1343">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="8c5c8-1344">已新增可在 Iot 中樞的目標 Iot 裝置上管理模組的支援。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1344">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="8c5c8-1345">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1345">New Cmdlets are:</span></span>
    - <span data-ttu-id="8c5c8-1346">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1346">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="8c5c8-1347">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1347">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="8c5c8-1348">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1348">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="8c5c8-1349">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1349">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="8c5c8-1350">已新增 Cmdlet，以取得 Iot 中樞內目標 IoT 裝置的連接字串。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1350">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="8c5c8-1351">已新增 Cmdlet，以取得 Iot 中樞內目標 IoT 裝置上的模組連接字串。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1351">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="8c5c8-1352">已新增可取得/設定 IoT 裝置父系裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1352">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="8c5c8-1353">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1353">New Cmdlets are:</span></span>
    - <span data-ttu-id="8c5c8-1354">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1354">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="8c5c8-1355">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1355">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="8c5c8-1356">已新增可管理裝置父子關聯性的支援。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1356">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8c5c8-1357">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1357">Az.Monitor</span></span>
* <span data-ttu-id="8c5c8-1358">已修正 'Get-AzMetricDefinition' 的輸出值 [#9714]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1358">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8c5c8-1359">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1359">Az.Network</span></span>
* <span data-ttu-id="8c5c8-1360">已更新 Sql Management SDK。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1360">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="8c5c8-1361">已修正 PrivateLinkServiceConnectionState 類別中的命名差異問題。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1361">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="8c5c8-1362">將欄位 ActionsRequired 對應至 ActionRequired。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1362">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="8c5c8-1363">已將 PublicNetworkAccess 新增至 'New-AzSqlServer' 和 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1363">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="8c5c8-1364">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1364">Az.Resources</span></span>
* <span data-ttu-id="8c5c8-1365">已修正 'Get-AzRoleAssignment' 中的 Null 參考錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1365">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="8c5c8-1366">已將 'Remove-AzADGroup' 中的 '-Force' 和 '-PassThru' 參數標記為選擇性 [#10849]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1366">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="8c5c8-1367">已修正 'MailNickname' 不會在 'Remove-AzADGroup' 中傳回的問題 [#11167]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1367">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="8c5c8-1368">已修正 'Remove-AzADGroup' 管道作業無法運作的問題 [#11171]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1368">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="8c5c8-1369">已修正 GetAzureRoleAssignmentCommand 中的 Null 參考錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1369">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="8c5c8-1370">已針對原則 Cmdlet 即將來臨的變更新增重大變更屬性</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1370">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="8c5c8-1371">已更新 'Get-AzResourceGroup' 以在伺服器端執行資源群組標籤篩選</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1371">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="8c5c8-1372">已擴充標籤 Cmdlet 以接受 -ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1372">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="8c5c8-1373">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1373">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="8c5c8-1374">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1374">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="8c5c8-1375">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1375">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="8c5c8-1376">已新增標籤 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1376">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="8c5c8-1377">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1377">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="8c5c8-1378">從 SDK 3.3.0 引進 ScopedDeployment</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1378">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="8c5c8-1379">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1379">Az.Sql</span></span>
* <span data-ttu-id="8c5c8-1380">已將 PublicNetworkAccess 新增至 'New-AzSqlServer' 和 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1380">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="8c5c8-1381">已針對受控資料庫新增對於長期保留備份設定的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1381">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="8c5c8-1382">在受控資料庫上取得/設定 LTR 原則</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1382">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="8c5c8-1383">依受控資料庫、受控執行個體或位置取得 LTR 備份</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1383">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="8c5c8-1384">移除 LTR 備份</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1384">Remove an LTR backup</span></span>
    - <span data-ttu-id="8c5c8-1385">還原 LTR 備份以建立新的受控資料庫</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1385">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="8c5c8-1386">已將 MinimalTlsVersion 新增至 New-AzSqlServer 和 Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1386">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="8c5c8-1387">已將 MinimalTlsVersion 新增至 New-AzSqlInstance 和 Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1387">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="8c5c8-1388">已提高適用於 Az.Network 的 SQL SDK 版本</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1388">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8c5c8-1389">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1389">Az.Storage</span></span>
* <span data-ttu-id="8c5c8-1390">已在 ImmutabilityPolicy 中支援 AllowProtectedAppendWrite</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1390">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="8c5c8-1391">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1391">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="8c5c8-1392">已針對未來版本中的 AzureStorageTable 類型變更新增重大變更警告訊息</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1392">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="8c5c8-1393">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1393">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="8c5c8-1394">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1394">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8c5c8-1395">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1395">Az.Websites</span></span>
* <span data-ttu-id="8c5c8-1396">已為 'New-AzAppServicePlan' 和 'Set-AzAppServicePlan' 新增標籤參數</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1396">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="8c5c8-1397">將自訂網域新增至網站時如果擲回例外狀況，則會停止執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1397">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="8c5c8-1398">已新增支援而可針對未和 App Service 方案位於相同資源群組中的 App Service 執行作業</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1398">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="8c5c8-1399">已將存取限制套用至不同資源群組中的 WebApp/函式</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1399">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="8c5c8-1400">已修正為 WebAppSlots 設定自訂主機名稱的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1400">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="8c5c8-1401">3.5.0 - 2020 年 2 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1401">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8c5c8-1402">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1402">Highlights since the last major release</span></span>
* <span data-ttu-id="8c5c8-1403">更新用戶端遙測。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1403">Updated client side telemetry.</span></span>
* <span data-ttu-id="8c5c8-1404">Az.IotHub 已新增 Cmdlet 來支援裝置管理。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1404">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="8c5c8-1405">Az.SqlVirtualMachine 已新增用於可用性群組接聽程式的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1405">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8c5c8-1406">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1406">Az.Accounts</span></span>
* <span data-ttu-id="8c5c8-1407">已將 SubscriptionId、TenantId 和執行時間新增至用戶端遙測的資料</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1407">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8c5c8-1408">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1408">Az.Automation</span></span>
* <span data-ttu-id="8c5c8-1409">已修正 'New-AzAutomationSoftwareUpdateConfiguration' 參考文件中範例 1 的錯字</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1409">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8c5c8-1410">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1410">Az.CognitiveServices</span></span>
* <span data-ttu-id="8c5c8-1411">已將 SDK 更新至 7.0</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1411">Updated SDK to 7.0</span></span>
* <span data-ttu-id="8c5c8-1412">已改善伺服器回應空白主體時的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1412">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8c5c8-1413">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1413">Az.Compute</span></span>
* <span data-ttu-id="8c5c8-1414">已允許 ProximityPlacementGroupId 在更新期間為空白值</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1414">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8c5c8-1415">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1415">Az.FrontDoor</span></span>
* <span data-ttu-id="8c5c8-1416">已新增 Cmdlet 來取得可在 WAF 中使用的受控規則定義</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1416">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8c5c8-1417">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1417">Az.IotHub</span></span>
* <span data-ttu-id="8c5c8-1418">已新增在 IoT 中樞中管理裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1418">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="8c5c8-1419">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1419">New Cmdlets are:</span></span>
    - <span data-ttu-id="8c5c8-1420">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1420">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="8c5c8-1421">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1421">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="8c5c8-1422">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1422">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="8c5c8-1423">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1423">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8c5c8-1424">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1424">Az.KeyVault</span></span>
* <span data-ttu-id="8c5c8-1425">已修正 Add-AzKeyVaultKey.md 的重複文字</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1425">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8c5c8-1426">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1426">Az.Monitor</span></span>
* <span data-ttu-id="8c5c8-1427">已修正 Get-AzLog Cmdlet 的描述。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1427">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="8c5c8-1428">已將名為 ActionGroupI 的新參數新增至 'New-AzMetricAlertRuleV2' 命令。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1428">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="8c5c8-1429">使用者可以提供 ActionGroupId(string) 或 ActionGorup(ActivityLogAlertActionGroup)。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1429">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8c5c8-1430">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1430">Az.Network</span></span>
* <span data-ttu-id="8c5c8-1431">已為 'New-AzPrivateLinkService' Cmdlet 的參數 '-EnableProxyProtocol' 新增一個額外的參數附註。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1431">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="8c5c8-1432">已修正 Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 和 Start-AzVirtualnetworkGatewayPacketCapture.md 中的 FilterData 範例。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1432">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="8c5c8-1433">已新增封包擷取範例，可在 Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 和 Start-AzVirtualnetworkGatewayPacketCapture.md 中擷取所有內部和外部封包。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1433">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="8c5c8-1434">支援 VNet 防火牆上的 Azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1434">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="8c5c8-1435">未新增任何 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1435">No new cmdlets are added.</span></span> <span data-ttu-id="8c5c8-1436">放寬 VNet 防火牆上的防火牆原則限制</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1436">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8c5c8-1437">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1437">Az.RecoveryServices</span></span>
* <span data-ttu-id="8c5c8-1438">已為 SQL Database 新增「還原為檔案」支援。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1438">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8c5c8-1439">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1439">Az.Resources</span></span>
* <span data-ttu-id="8c5c8-1440">已重構範本部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1440">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="8c5c8-1441">已新增用於在管理群組上管理部署的 Cmdlet：\*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1441">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="8c5c8-1442">已新增用於在租用戶範圍上管理部署的 Cmdlet：\*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1442">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="8c5c8-1443">已重構 \*-AzDeployment Cmdlet，以便在特定訂用帳戶範圍內工作</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1443">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="8c5c8-1444">為 \*-AzDeployment Cmdlet 建立別名 \*-AzSubscriptionDeployment</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1444">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="8c5c8-1445">已修正未設定參數 'AvailableToOtherTenants' 時的 'Update-AzADApplication'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1445">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="8c5c8-1446">已移除 ApplicationObjectWithoutCredentialParameterSet 來避免 AmbiguousParameterSetException。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1446">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="8c5c8-1447">已重新產生說明檔</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1447">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="8c5c8-1448">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1448">Az.Sql</span></span>
* <span data-ttu-id="8c5c8-1449">已在受控執行個體上新增跨訂用帳戶的時間點還原支援。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1449">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="8c5c8-1450">已新增變更現有 SQL 受控執行個體硬體世代的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1450">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="8c5c8-1451">已修正 'Update-AzSqlServerVulnerabilityAssessmentSetting' 說明範例：parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1451">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="8c5c8-1452">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1452">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="8c5c8-1453">已新增用於可用性群組接聽程式的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1453">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="8c5c8-1454">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1454">Az.StorageSync</span></span>
* <span data-ttu-id="8c5c8-1455">已更新 'Invoke-AzStorageSyncCompatibilityCheck' 中支援的字元集。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1455">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="8c5c8-1456">3.4.0 - 2020 年 2 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1456">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8c5c8-1457">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1457">Highlights since the last major release</span></span>
* <span data-ttu-id="8c5c8-1458">Az.CosmosDB 初始版本 0.1.0 已發行</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1458">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="8c5c8-1459">Az.Network ConnectionMonitor V2 支援已新增</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1459">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8c5c8-1460">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1460">Az.Accounts</span></span>
* <span data-ttu-id="8c5c8-1461">當 AzureRmContext.json 無法使用時，停用內容自動儲存</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1461">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="8c5c8-1462">將 Azure Powershell Common 的參考更新至 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1462">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8c5c8-1463">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1463">Az.ApiManagement</span></span>
* <span data-ttu-id="8c5c8-1464">**Get-AzApiManagementApiSchema** 已修正取得與 API 相關聯的 Open-Api 結構描述   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1464">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="8c5c8-1465">**New-AzApiManagementProduct** _ 和 _ *Set-AzApiManagementProduct*\*</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1465">**New-AzApiManagementProduct** _ and _ *Set-AzApiManagementProduct*\*</span></span>
  - <span data-ttu-id="8c5c8-1466"> https://github.com/Azure/azure-powershell/issues/10472 的修正文件</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1466">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="8c5c8-1467">**Set-AzApiManagementApi** 新增的範例，示範如何使用 Cmdlet 來更新 ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1467">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8c5c8-1468">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1468">Az.Compute</span></span>
* <span data-ttu-id="8c5c8-1469">將 VM 狀態的數目限制為 100，以避免在沒有 VM 名稱的情況下執行 Get-AzVM -Status 時進行節流。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1469">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="8c5c8-1470">新增 Update-AzDiskEncryptionSet Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1470">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="8c5c8-1471">將 EncryptionType 和 DiskEncryptionSetId 參數新增至下列 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1471">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="8c5c8-1472">New-AzDiskUpdateConfig、New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1472">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="8c5c8-1473">將 ColocationStatus 參數新增至 Get-AzProximityPlacementGroup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1473">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8c5c8-1474">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1474">Az.DataFactory</span></span>
* <span data-ttu-id="8c5c8-1475">將 ADF .Net SDK 版本更新為 4.7.0</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1475">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="8c5c8-1476">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1476">Az.DeploymentManager</span></span>
* <span data-ttu-id="8c5c8-1477">新增資源的 LIST 作業</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1477">Adds LIST operations for resources</span></span>
* <span data-ttu-id="8c5c8-1478">新增執行健康情況檢查步驟作業的功能</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1478">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8c5c8-1479">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1479">Az.HDInsight</span></span>
* <span data-ttu-id="8c5c8-1480">修正 New-AzHDInsightCluster 的文件錯誤。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1480">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8c5c8-1481">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1481">Az.KeyVault</span></span>
* <span data-ttu-id="8c5c8-1482">將 Name 別名新增至 VaultName 屬性，使 Remove-AzureKeyVault 與 New-AzureKeyVault 一致。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1482">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8c5c8-1483">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1483">Az.Network</span></span>
* <span data-ttu-id="8c5c8-1484">新增至 Set-AzNetworkWatcherConfigFlowLog.md 以示範流量分析停用案例的新範例。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1484">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="8c5c8-1485">新增將管理 IP 設定指派給 Azure 防火牆的支援 - 防火牆將用於其管理流量的專用子網路和公用 IP</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1485">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="8c5c8-1486">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1486">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="8c5c8-1487">已新增可接受公用 IP 位址物件的參數 -ManagementPublicIpAddress (非強制)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1487">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="8c5c8-1488">已在防火牆物件上新增方法 SetManagementIpConfiguration - 需要子網路和公用 IP 位址作為輸入 - 子網路名稱必須是 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1488">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="8c5c8-1489">已更正 Get-AzNetworkSecurityGroup 範例，以顯示 NSG (不是網路介面) 的範例。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1489">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="8c5c8-1490">已修正 New-AzVpnSite 命令中，導致資源識別碼完成器無法完成參數的錯字。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1490">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="8c5c8-1491">已在應用程式閘道中新增重寫規則動作集內 URL 設定的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1491">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="8c5c8-1492">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1492">New cmdlets added:</span></span>
        - <span data-ttu-id="8c5c8-1493">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1493">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="8c5c8-1494">使用選擇性參數 UrlConfiguration 更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1494">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="8c5c8-1495">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1495">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="8c5c8-1496">新增對於 NetworkWatcher ConnectionMonitor 第 2 版資源的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1496">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8c5c8-1497">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1497">Az.PolicyInsights</span></span>
* <span data-ttu-id="8c5c8-1498">支援在決定要補救的資源之前，評估合規性</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1498">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="8c5c8-1499">將 '-ResourceDiscoverMode' 參數新增至 Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1499">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="8c5c8-1500">新增 Get-AzPolicyMetadata Cmdlet 以取得原則中繼資料資源</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1500">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="8c5c8-1501">已更新 API 版本 2019-10-01 的 Get-AzPolicyState 和 Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1501">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8c5c8-1502">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1502">Az.RecoveryServices</span></span>
* <span data-ttu-id="8c5c8-1503">Azure Site Recovery 支援移除已複寫的磁碟。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1503">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="8c5c8-1504">Azure 備份在建立復原服務保存庫時新增了新增標記的支援。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1504">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8c5c8-1505">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1505">Az.Resources</span></span>
* <span data-ttu-id="8c5c8-1506">以內容訂閱的預設值，讓 \*-AzPolicyAssignment Cmdlet 中的 -Scope 成為選擇性</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1506">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="8c5c8-1507">新增使用密碼和金鑰認證建立 ADServicePrincipal 的範例</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1507">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="8c5c8-1508">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1508">Az.Sql</span></span>
<span data-ttu-id="8c5c8-1509">修正 New-AzSqlDatabaseSecondary Cmdlet 來檢查 PartnerDatabaseName 是否存在，而不是 DatabaseName 是否存在。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1509">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8c5c8-1510">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1510">Az.Storage</span></span>
* <span data-ttu-id="8c5c8-1511">支援在建立儲存體帳戶中設定資料表/佇列加密 Keytype</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1511">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="8c5c8-1512">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1512">New-AzStorageAccount</span></span>
* <span data-ttu-id="8c5c8-1513">在 StorageException 沒有 ExtendedErrorInformation 時顯示 RequestId</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1513">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="8c5c8-1514">修正 Cmdlet Start-AzStorageBlobCopy 的範例 6</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1514">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8c5c8-1515">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1515">Az.Websites</span></span>
* <span data-ttu-id="8c5c8-1516">Set-AzWebapp 和 Set-AzWebappSlot 支援 AlwaysOn、MinTls 和 FtpsState 屬性</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1516">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="8c5c8-1517">修正在使用單一 Set-AzWebApp 命令的同時設定 HttpsOnly 和變更 AppservicePlan，將 HttpsOnly 重設為預設值的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1517">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="8c5c8-1518">3.3.0 - 2020 年 1 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1518">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8c5c8-1519">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1519">Az.Accounts</span></span>
* <span data-ttu-id="8c5c8-1520">已更新 Add-AzEnvironment 和 Set-AzEnvironment 以接受 AzureAttestationServiceEndpointResourceId 和 AzureAttestationServiceEndpointSuffix 參數</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1520">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8c5c8-1521">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1521">Az.Cdn</span></span>
* <span data-ttu-id="8c5c8-1522">在 New-AzCdnEndpoint Cmdlet 中顯示錯誤回應詳細資料</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1522">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8c5c8-1523">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1523">Az.Compute</span></span>
* <span data-ttu-id="8c5c8-1524">修正具有受控 OD 磁碟 (沒有 OS 設定檔) 之 VM 的 Set-AzVMCustomScriptExtension Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1524">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="8c5c8-1525">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1525">Az.ContainerInstance</span></span>
* <span data-ttu-id="8c5c8-1526">修正了 New-AzContainerGroup 範例所使用的參數名稱</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1526">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="8c5c8-1527">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1527">Az.DataBoxEdge</span></span>
* <span data-ttu-id="8c5c8-1528">新增了 Cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1528">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="8c5c8-1529">取得 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1529">Get the Edge Storage Container</span></span>
* <span data-ttu-id="8c5c8-1530">新增了 Cmdlet 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1530">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="8c5c8-1531">建立新的 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1531">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="8c5c8-1532">新增了 Cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1532">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="8c5c8-1533">移除 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1533">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="8c5c8-1534">新增了 Cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1534">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="8c5c8-1535">用來重新整理 Edge 儲存體容器資料的叫用動作</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1535">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="8c5c8-1536">新增了 Cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1536">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="8c5c8-1537">取得 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1537">Get the Edge Storage Account</span></span>
* <span data-ttu-id="8c5c8-1538">新增了 Cmdlet 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1538">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="8c5c8-1539">建立新的 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1539">Create new Edge Storage Account</span></span>
* <span data-ttu-id="8c5c8-1540">新增了 Cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1540">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="8c5c8-1541">移除 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1541">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="8c5c8-1542">叫用 Cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1542">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="8c5c8-1543">用來重新整理共用資料的叫用動作</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1543">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="8c5c8-1544">新增了 Cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1544">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="8c5c8-1545">設定 az databoxedge 儲存體帳戶憑證</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1545">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8c5c8-1546">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1546">Az.DataFactory</span></span>
* <span data-ttu-id="8c5c8-1547">新增適用於 Get-AzDataFactoryV2IntegrationRuntime Cmd 的 AutoUpdateETA、LatestVersion、PushedVersion、TaskQueueId 和 VersionStatus 屬性</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1547">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="8c5c8-1548">將 ADF .Net SDK 版本更新為 4.6.0</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1548">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="8c5c8-1549">為 'Set-AzureRmDataFactoryV2IntegrationRuntime' Cmd 新增參數 'PublicIPs'，以使用靜態公用 IP 位址建立 Azure-SSIS IR。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1549">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="8c5c8-1550">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1550">Az.DevTestLabs</span></span>
* <span data-ttu-id="8c5c8-1551">移除 Get-AzDtlAllowedVMSizesPolicy.md 中中斷的連結</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1551">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8c5c8-1552">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1552">Az.EventHub</span></span>
* <span data-ttu-id="8c5c8-1553">問題 10634 的修正內容：修正 Null 物件參考以移除 eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1553">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8c5c8-1554">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1554">Az.HDInsight</span></span>
* <span data-ttu-id="8c5c8-1555">修正 Invoke-AzHDInsightHiveJob.md 錯誤。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1555">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="8c5c8-1556">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1556">Az.MachineLearning</span></span>
* <span data-ttu-id="8c5c8-1557">由於不再提供 MachineLearningCompute，已移除下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1557">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="8c5c8-1558">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1558">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="8c5c8-1559">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1559">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="8c5c8-1560">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1560">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="8c5c8-1561">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1561">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="8c5c8-1562">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1562">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="8c5c8-1563">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1563">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="8c5c8-1564">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1564">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8c5c8-1565">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1565">Az.Network</span></span>
* <span data-ttu-id="8c5c8-1566">將 Microsoft.Azure.Management.Sql 相依性從 1.36-preview 升級到 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1566">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8c5c8-1567">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1567">Az.RecoveryServices</span></span>
* <span data-ttu-id="8c5c8-1568">Azure Site Recovery 對使用 Azure 至 Azure 提供者的客戶受控金鑰進行待用加密的受控磁碟 VM 支援變更。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1568">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="8c5c8-1569">Azure Site Recovery 支援將磁碟加密集識別碼輸入為選擇性輸入，以啟用 VMware 至 Azure 的保護。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1569">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="8c5c8-1570">Azure Site Recovery 支援將磁碟加密集識別碼輸入為磁碟層級的選擇性輸入，以啟用 VMware 至 Azure 的保護。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1570">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="8c5c8-1571">Azure Site Recovery 支援以將適用於 HyperV 的磁碟加密集對應更新至 Azure 的複寫受保護項目。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1571">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8c5c8-1572">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1572">Az.Resources</span></span>
* <span data-ttu-id="8c5c8-1573">修正 'Remove-AzTag' 說明文件中的錯誤。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1573">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="8c5c8-1574">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1574">Az.Sql</span></span>
* <span data-ttu-id="8c5c8-1575">修正弱點評定設定基準 Cmdlet 功能，以在 Azure 資料庫的主要資料庫中運作，並在受控執行個體系統資料庫中加以限制。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1575">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="8c5c8-1576">修正建立 SQL 執行個體容錯移轉群組時的錯誤</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1576">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="8c5c8-1577">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1577">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="8c5c8-1578">將 DR 新增為新的有效授權類型</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1578">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8c5c8-1579">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1579">Az.Storage</span></span>
* <span data-ttu-id="8c5c8-1580">在後續版本中新增 DefaultAction 值變更的重大變更警告訊息</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1580">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="8c5c8-1581">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1581">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="8c5c8-1582">使用參數 -IncludeGeoReplicationStats 執行 get-AzureRMStorageAccount，支援取得儲存體帳戶的上次同步處理時間</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1582">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="8c5c8-1583">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1583">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="8c5c8-1584">3.2.0 - 2019 年 12 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1584">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="8c5c8-1585">一般</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1585">General</span></span>
* <span data-ttu-id="8c5c8-1586">更新 .psd1 中的更新參考，以便所有模組均可使用相對路徑</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1586">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8c5c8-1587">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1587">Az.Accounts</span></span>
* <span data-ttu-id="8c5c8-1588">針對 Az 4.0 預覽的用戶端遙測設定正確的 UserAgent</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1588">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="8c5c8-1589">當 Az 4.0 預覽中的內容為 null 時，顯示使用者易記的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1589">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="8c5c8-1590">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1590">Az.Batch</span></span>
* <span data-ttu-id="8c5c8-1591">修正問題 [#10602](https://github.com/Azure/azure-powershell/issues/10602)，其中 **New-AzBatchPool** 並未適當地將 'VirtualMachineConfiguration.ContainerConfiguration' 或 'VirtualMachineConfiguration.DataDisks' 傳送到伺服器。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1591">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8c5c8-1592">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1592">Az.DataFactory</span></span>
* <span data-ttu-id="8c5c8-1593">將 ADF .Net SDK 版本更新為 4.5.0</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1593">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8c5c8-1594">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1594">Az.FrontDoor</span></span>
* <span data-ttu-id="8c5c8-1595">已新增 WAF 受控規則排除支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1595">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="8c5c8-1596">在自動完成中新增 SocketAddr</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1596">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="8c5c8-1597">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1597">Az.HealthcareApis</span></span>
* <span data-ttu-id="8c5c8-1598">例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1598">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8c5c8-1599">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1599">Az.KeyVault</span></span>
* <span data-ttu-id="8c5c8-1600">已修正存取可能未設定的值時發生的錯誤</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1600">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="8c5c8-1601">橢圓曲線密碼編譯憑證管理</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1601">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="8c5c8-1602">已新增為憑證原則指定 Curve 的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1602">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8c5c8-1603">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1603">Az.Monitor</span></span>
* <span data-ttu-id="8c5c8-1604">在 Add Diagnostic Settings 命令中新增選用的引數。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1604">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="8c5c8-1605">如果存在切換引數，表示匯出到 Log Analytics 必須是固定的結構描述 (也稱為</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1605">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="8c5c8-1606">專用，資料類型)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1606">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8c5c8-1607">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1607">Az.Network</span></span>
* <span data-ttu-id="8c5c8-1608">在 AzureFirewall 應用程式、Nat 和網路規則中支援 IpGroups。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1608">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8c5c8-1609">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1609">Az.Resources</span></span>
* <span data-ttu-id="8c5c8-1610">修正如果範本名稱與一些內建參數名稱衝突，則範本部署無法讀取範本參數的問題。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1610">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="8c5c8-1611">更新原則 Cmdliet 以使用新的 API 版本 2019-09-01，其中引進原則集合定義內的群組支援。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1611">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="8c5c8-1612">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1612">Az.Sql</span></span>
* <span data-ttu-id="8c5c8-1613">已將弱點評估自動啟用中的儲存體建立升級為 StorageV2</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1613">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8c5c8-1614">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1614">Az.Storage</span></span>
* <span data-ttu-id="8c5c8-1615">支援使用以 Oauth 驗證為基礎的儲存體內容來產生 Blob/Constainer Idenity 為基礎的 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1615">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="8c5c8-1616">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1616">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="8c5c8-1617">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1617">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="8c5c8-1618">支援撤銷儲存體帳戶使用者委派金鑰，因此會撤銷所有 Idenity SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1618">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="8c5c8-1619">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1619">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="8c5c8-1620">升級至 Microsoft.Azure.Management.Storage 14.2.0，以支援新的 API 版本 2019-06-01。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1620">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="8c5c8-1621">針對檔案共用 Cmdlet 的管理平面中超過 5120 的值支援 QuotaGiB (Gibibye 中的共用配額)，並將 'Quota' 參數別名新增到 'QuotaGiB' 參數中。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1621">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="8c5c8-1622">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1622">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="8c5c8-1623">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1623">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="8c5c8-1624">在參數 'Quota' 中新增參數別名 'QuotaGiB'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1624">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="8c5c8-1625">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1625">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="8c5c8-1626">修正 Set-AzStorageContainerAcl 可清除已儲存之存取原則的問題。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1626">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="8c5c8-1627">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1627">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="8c5c8-1628">3.1.0 - 2019 年 11 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1628">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8c5c8-1629">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1629">Highlights since the last major release</span></span>
* <span data-ttu-id="8c5c8-1630">已發佈 Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1630">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="8c5c8-1631">已發佈 Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1631">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8c5c8-1632">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1632">Az.Compute</span></span>
* <span data-ttu-id="8c5c8-1633">VM Reapply 功能</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1633">VM Reapply feature</span></span>
    - <span data-ttu-id="8c5c8-1634">將 Reapply 參數新增到 Set-AzVM Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1634">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="8c5c8-1635">VM 擴展集 AutomaticRepairs 功能：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1635">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="8c5c8-1636">將 EnableAutomaticRepair、AutomaticRepairGracePeriod 和 AutomaticRepairMaxInstanceRepairsPercent 參數新增到下列 Cmdlet： New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1636">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="8c5c8-1637">適用於 New-AzVM 的跨租用戶資源庫映像支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1637">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="8c5c8-1638">將 'Spot' 新增到 New-AzVM、New-AzVMConfig 和 New-AzVmss Cmdlet 中的 Priority 參數引數完成程式</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1638">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="8c5c8-1639">將 DiskIOPSReadWrite 和 DiskMBpsReadWrite 參數新增到 Add-AzVmssDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1639">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="8c5c8-1640">將 New-AzGalleryImageVersion Cmdlet 的 SourceImageId 參數變更為選擇性</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1640">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="8c5c8-1641">將 OSDiskImage 和 DataDiskImage 參數新增到 New-AzGalleryImageVersion Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1641">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="8c5c8-1642">將 HyperVGeneration 參數新增到 New-AzGalleryImageDefinition Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1642">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="8c5c8-1643">將 SkipExtensionsOnOverprovisionedVMs 參數新增到 New-AzVmss、New-AzVmssConfig 和 Update-AzVmss Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1643">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="8c5c8-1644">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1644">Az.DataBoxEdge</span></span>
* <span data-ttu-id="8c5c8-1645">已新增 Cmdlet `Get-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1645">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="8c5c8-1646">取得訂單</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1646">Get the Order</span></span>
* <span data-ttu-id="8c5c8-1647">已新增 Cmdlet `New-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1647">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="8c5c8-1648">建立新訂單</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1648">Create new Order</span></span>
* <span data-ttu-id="8c5c8-1649">已新增 Cmdlet `Remove-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1649">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="8c5c8-1650">移除訂單</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1650">Remove the Order</span></span>
* <span data-ttu-id="8c5c8-1651">Cmdlet `New-AzDataBoxEdgeShare` 中的變更</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1651">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="8c5c8-1652">立即建立本機共用</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1652">Now creates Local Share</span></span>
* <span data-ttu-id="8c5c8-1653">已新增 Cmdlet `Set-AzDataBoxEdgeRole`</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1653">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="8c5c8-1654">IotRole 現在對應到共用</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1654">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="8c5c8-1655">已新增 Cmdlet `Invoke-AzDataBoxEdgeDevice`</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1655">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="8c5c8-1656">在裝置上叫用掃描更新、下載更新並安裝更新</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1656">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="8c5c8-1657">已新增 Cmdlet `Get-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1657">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="8c5c8-1658">取得觸發程序的相關資訊</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1658">Gets the information about Triggers</span></span>
* <span data-ttu-id="8c5c8-1659">已新增 Cmdlet `New-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1659">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="8c5c8-1660">建立新的觸發程序</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1660">Create new Triggers</span></span>
* <span data-ttu-id="8c5c8-1661">已新增 Cmdlet `Remove-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1661">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="8c5c8-1662">移除觸發程序</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1662">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8c5c8-1663">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1663">Az.DataFactory</span></span>
* <span data-ttu-id="8c5c8-1664">將 ADF .Net SDK 版本更新為 4.4.0</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1664">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="8c5c8-1665">為 'Set-AzureRmDataFactoryV2IntegrationRuntime' CMD 新增參數 'ExpressCustomSetup'，以在無需自訂設定指令碼的情況下啟用設定組態和第三方元件。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1665">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8c5c8-1666">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1666">Az.DataLakeStore</span></span>
* <span data-ttu-id="8c5c8-1667">更新 Get-AzDataLakeStoreDeletedItem 和 Restore-AzDataLakeStoreDeletedItem 的文件</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1667">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8c5c8-1668">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1668">Az.EventHub</span></span>
* <span data-ttu-id="8c5c8-1669">修正 10301 的問題：修正 SAS 權杖日期格式</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1669">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8c5c8-1670">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1670">Az.FrontDoor</span></span>
* <span data-ttu-id="8c5c8-1671">將 MinimumTlsVersion 參數新增到 Enable-AzFrontDoorCustomDomainHttps 和 New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1671">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="8c5c8-1672">將 HealthProbeMethod 和 EnabledState 參數新增到 New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1672">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="8c5c8-1673">新增新的 cmdlet 以建立 BackendPoolsSettings 物件，以傳遞到 Front Door 的建立/更新</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1673">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="8c5c8-1674">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1674">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8c5c8-1675">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1675">Az.Network</span></span>
* <span data-ttu-id="8c5c8-1676">變更 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' 和 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData 選項範例。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1676">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="8c5c8-1677">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1677">Az.PrivateDns</span></span>
* <span data-ttu-id="8c5c8-1678">已將 PrivateDns .net SDK 更新為 1.0.0 版</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1678">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8c5c8-1679">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1679">Az.RecoveryServices</span></span>
* <span data-ttu-id="8c5c8-1680">Azure Site Recovery 支援在啟用保護時選取磁碟類型。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1680">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="8c5c8-1681">Azure Site Recovery 復原計劃針對動作編輯的錯誤 (bug) 修正。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1681">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="8c5c8-1682">Azure 備份 SQL 還原支援接受 filestream DB.</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1682">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="8c5c8-1683">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1683">Az.RedisCache</span></span>
* <span data-ttu-id="8c5c8-1684">已在 'New-AzRedisCache' 和 'Set-AzRedisCache' Cmdlet 中新增了 'MinimumTlsVersion'參數。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1684">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="8c5c8-1685">此外，也在 'Get-AzRedisCache' Cmdlet 的輸出中新增了 'MinimumTlsVersion'。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1685">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="8c5c8-1686">已針對 'Set-AzRedisCache' 和 'New-AzRedisCache' Cmdlet 新增了 '-Size' 參數的驗證</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1686">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="8c5c8-1687">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1687">Az.Resources</span></span>
- <span data-ttu-id="8c5c8-1688">更新了原則 Cmdlet 以使用新的 API 版本 2019-06-01，其在原則指派中具有新的 EnforcementMode 屬性。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1688">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="8c5c8-1689">更新了建立原則定義說明範例</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1689">Updated create policy definition help example</span></span>
- <span data-ttu-id="8c5c8-1690">修正錯誤 (bug) Remove-AZADServicePrincipal -ServicePrincipalName，當找不到服務主體名稱時擲回 Null 參考。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1690">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="8c5c8-1691">修正錯誤 (bug) New-AZADServicePrincipal，當租用戶沒有任何訂用帳戶擲回 Null 參考。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1691">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="8c5c8-1692">將 New-azadserviceprincipal 變更為只將認證新增到相關聯的應用程式。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1692">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="8c5c8-1693">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1693">Az.Sql</span></span>
* <span data-ttu-id="8c5c8-1694">新增了對 ReadReplicaCount 資料庫的支援。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1694">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="8c5c8-1695">修正了未設定區域備援時的 Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1695">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="8c5c8-1696">3.0.0 - 2019 年 11 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1696">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="8c5c8-1697">一般</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1697">General</span></span>
* <span data-ttu-id="8c5c8-1698">已發行 Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1698">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8c5c8-1699">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1699">Az.Accounts</span></span>
* <span data-ttu-id="8c5c8-1700">為 'Resolve-Error' 別名新增了淘汰訊息。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1700">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="8c5c8-1701">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1701">Az.Advisor</span></span>
* <span data-ttu-id="8c5c8-1702">已為 Get-AzAdvisorRecommendation Cmdlet 新增了新的 'Operational Excellence' 類別。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1702">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="8c5c8-1703">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1703">Az.Batch</span></span>
* <span data-ttu-id="8c5c8-1704">已將 `BatchAccountContext` 中的 `CoreQuota` 重新命名為 `DedicatedCoreQuota`。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1704">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="8c5c8-1705">另外還有新的 `LowPriorityCoreQuota`。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1705">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="8c5c8-1706">這會影響 **Get-AzBatchAccount**。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1706">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="8c5c8-1707">**New-AzBatchTask** `-ResourceFile` 參數現在會採用 `PSResourceFile` 物件集合，可使用新的 **New-AzBatchResourceFile** Cmdlet 加以建構。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1707">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="8c5c8-1708">新增 **New-AzBatchResourceFile** Cmdlet 以協助建立 `PSResourceFile` 物件。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1708">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="8c5c8-1709">這些可以提供給 `-ResourceFile` 參數中的 **New-AzBatchTask**。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1709">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="8c5c8-1710">除了現有的 `HttpUrl` 方式，這也會支援兩種新的資源檔類型：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1710">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="8c5c8-1711">`AutoStorageContainerName` 以資源檔為基礎，會將整個自動儲存體容器下載至 Batch-節點。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1711">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="8c5c8-1712">`StorageContainerUrl` 以資源檔為基礎，會將 URL 中指定的容器下載至 Batch-節點。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1712">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="8c5c8-1713">已移除 **AzBatchApplication** 所傳回之 `PSApplication` 的 `ApplicationPackages` 屬性。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1713">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="8c5c8-1714">您現在可以使用 **AzBatchApplicationPackage** 來取出應用程式內的特定套件。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1714">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="8c5c8-1715">例如：`Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1715">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="8c5c8-1716">將 **Get-AzBatchApplicationPackage**、**New-AzBatchApplicationPackage**、**Remove-AzBatchApplicationPackage**、**Get-AzBatchApplication**、**New-AzBatchApplication**、**Remove-AzBatchApplication** 和 **Set-AzBatchApplication** 上的 `ApplicationId` 重新命名為 `ApplicationName`。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1716">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="8c5c8-1717">`ApplicationId` 現在是 `ApplicationName` 的別名。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1717">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="8c5c8-1718">已在 `PSWindowsUserConfiguration` 中新增新的 `PSUserAccount` 屬性。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1718">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="8c5c8-1719">已將 `PSApplicationPackage` 上的 `Version` 重新命名為 `Name`。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1719">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="8c5c8-1720">已將 `PSResourceFile` 上的 `BlobSource` 重新命名為 `HttpUrl`。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1720">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="8c5c8-1721">已從 `PSVirtualMachineConfiguration` 移除 `OSDisk` 屬性。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1721">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="8c5c8-1722">已移除 **AzBatchPoolOSVersion**。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1722">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="8c5c8-1723">不再支援此作業。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1723">This operation is no longer supported.</span></span>
* <span data-ttu-id="8c5c8-1724">已從下列 `PSCloudServiceConfiguration` 中移除 `TargetOSVersion`。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1724">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="8c5c8-1725">已將 `PSCloudServiceConfiguration` 上的 `CurrentOSVersion` 重新命名為 `OSVersion`。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1725">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="8c5c8-1726">已從 `PSPoolUsageMetrics` 移除 `DataEgressGiB` 和 `DataIngressGiB`。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1726">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="8c5c8-1727">已移除 **AzBatchNodeAgentSku**，並以 **AzBatchSupportedImage** 取代。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1727">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="8c5c8-1728">**AzBatchSupportedImage** 會傳回與 **AzBatchNodeAgentSku** 相同但格式較好用的資料。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1728">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="8c5c8-1729">系統現在也會傳回新的未驗證映像。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1729">New non-verified images are also now returned.</span></span> <span data-ttu-id="8c5c8-1730">此外，也包含每個映像的 `Capabilities` 和 `BatchSupportEndOfLife` 的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1730">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="8c5c8-1731">新增了一項功能，可透過 **New-azbatchpool** 的新 `MountConfiguration` 參數，在集區的每個節點上裝載遠端檔案系統。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1731">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="8c5c8-1732">現在支援網路安全性規則，根據流量的來源連接埠封鎖對集區的網路存取。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1732">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="8c5c8-1733">這會透過 `PSNetworkSecurityGroupRule`上的 `SourcePortRanges` 屬性來完成。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1733">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="8c5c8-1734">執行容器時，Batch 現在支援在容器工作目錄中或 Batch 工作的工作目錄中執行工作。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1734">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="8c5c8-1735">這是由 `PSTaskContainerSettings` 上的 `WorkingDirectory` 屬性所控制。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1735">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="8c5c8-1736">新增了一項功能，可透過新的 `PublicIPs` 屬性，在 `PSNetworkConfiguration` 上指定公用 IP 集合。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1736">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="8c5c8-1737">如此可確保集區中的節點將會有來自清單使用者所提供的 IP。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1737">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="8c5c8-1738">未指定時，`PSSTartTask` 上的 `WaitForSuccess` 預設值現在為 `$True` (之前是 `$False`)。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1738">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="8c5c8-1739">未指定時，`PSAutoUserSpecification` 上的 `Scope` 預設值現在為 `Pool` (之前在 Windows 上是 `Task`，在 Linux 上是 `Pool`)。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1739">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8c5c8-1740">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1740">Az.Cdn</span></span>
* <span data-ttu-id="8c5c8-1741">已將 UrlRewriteAction and CacheKeyQueryStringAction 引進 RulesEngine。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1741">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="8c5c8-1742">已修正 AzDeliveryRuleCondition Cmdlet 中的數個錯誤 (bug)，例如遺漏 'Selector’ 輸入。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1742">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8c5c8-1743">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1743">Az.Compute</span></span>
* <span data-ttu-id="8c5c8-1744">磁碟加密集功能</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1744">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="8c5c8-1745">新的 Cmdlet： New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1745">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="8c5c8-1746">DiskEncryptionSetId 參數已新增至下列 Cmdlet： Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1746">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="8c5c8-1747">DiskEncryptionSetId 和 EncryptionType 參數已新增至下列 Cmdlet： New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1747">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="8c5c8-1748">將 PublicIPAddressVersion 參數新增至 New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1748">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="8c5c8-1749">將自訂指令碼擴充功能的 FileUris 從公用設定移至受保護的設定</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1749">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="8c5c8-1750">將 ScaleInPolicy 新增至 New-AzVmss、New-AzVmssConfig 和 Update-AzVmss Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1750">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="8c5c8-1751">重大變更</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1751">Breaking changes</span></span>
    - <span data-ttu-id="8c5c8-1752">上傳 CreateOption 時，會針對 New-AzDiskConfig 使用 UploadSizeInBytes 參數而非 DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1752">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="8c5c8-1753">在 GalleryImageVersion 物件中，會使用 StorageProfile.Source.Id 取代 PublishingProfile.Source.ManagedImage.Id</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1753">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8c5c8-1754">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1754">Az.DataFactory</span></span>
* <span data-ttu-id="8c5c8-1755">將 ADF .Net SDK 版本更新為 4.3.0</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1755">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8c5c8-1756">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1756">Az.DataLakeStore</span></span>
* <span data-ttu-id="8c5c8-1757">更新 ADLS SDK 版本 (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) ，提供下列修正程式</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1757">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="8c5c8-1758">避免在無法將資源回收筒或目錄專案的建立時間還原序列化 (creationtime) 時擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1758">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="8c5c8-1759">在 adlsclient 中公開每個要求超時設定</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1759">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="8c5c8-1760">修正傳遞原始 syncflag 以進行 badoffset 復原</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1760">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="8c5c8-1761">修正 EnumerateDirectory 以在檢查回應後取得接續權杖</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1761">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="8c5c8-1762">修正 Concat 錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1762">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8c5c8-1763">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1763">Az.FrontDoor</span></span>
* <span data-ttu-id="8c5c8-1764">修正了多個模組中的各種錯字問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1764">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8c5c8-1765">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1765">Az.HDInsight</span></span>
* <span data-ttu-id="8c5c8-1766">修正當使用 Get-AzHDInsightCluster 取得具有 ADLSGen1 儲存體的叢集時，客戶會收到「不是有效的 Base-64 字串」的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1766">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="8c5c8-1767">將名為 'ApplicationId' 的參數新增至 Add-AzHDInsightClusterIdentity、New-AzHDInsightClusterConfig 和 New-AzHDInsightCluster 三個 Cmdlet 中，讓客戶可以提供服務主體應用程式識別碼來存取 Azure Data Lake。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1767">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="8c5c8-1768">已將 Microsoft.Azure.Management.HDInsight 從 2.1.0 變更為 5.1.0</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1768">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="8c5c8-1769">已移除五個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1769">Removed five cmdlets:</span></span>
    - <span data-ttu-id="8c5c8-1770">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1770">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="8c5c8-1771">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1771">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="8c5c8-1772">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1772">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="8c5c8-1773">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1773">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="8c5c8-1774">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1774">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="8c5c8-1775">新增了三個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1775">Added three cmdlets:</span></span>
    - <span data-ttu-id="8c5c8-1776">Get-AzHDInsightMonitoring 用來取代 Get-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1776">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="8c5c8-1777">Enable-AzHDInsightMonitoring 用來取代 Enable-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1777">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="8c5c8-1778">Disable-AzHDInsightMonitoring 用來取代 Disable-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1778">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="8c5c8-1779">修正了 Cmdlet AzHDInsightProperties，以支援來自特定位置的取得功能資訊。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1779">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="8c5c8-1780">已從 Add-AzHDInsightConfigValue 移除參數集 ('Spark1', 'Spark2')。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1780">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="8c5c8-1781">將範例新增至 Cmdlet Add-AzHDInsightSecurityProfile 的說明文件。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1781">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="8c5c8-1782">已變更下列 Cmdlet 的輸出類型：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1782">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="8c5c8-1783">已將 Get-AzHDInsightProperties 的輸出類型從 CapabilitiesResponse 變更為 AzureHDInsightCapabilities。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1783">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="8c5c8-1784">已將 Remove-AzHDInsightCluster 的輸出類型從 ClusterGetResponse 變更為 bool。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1784">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="8c5c8-1785">已將 Set-AzHDInsightGatewaySettings HttpConnectivitySettings 的輸出類型變更為 GatewaySettings。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1785">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="8c5c8-1786">已新增一些狀況測試案例。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1786">Added some scenario test cases.</span></span>
* <span data-ttu-id="8c5c8-1787">移除一些別名：'Add-AzHDInsightConfigValues'、'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1787">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8c5c8-1788">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1788">Az.IotHub</span></span>
* <span data-ttu-id="8c5c8-1789">重大變更：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1789">Breaking changes:</span></span>
    - <span data-ttu-id="8c5c8-1790">Cmdlet 'Add-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1790">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="8c5c8-1791">已移除 Cmdlet 'Add-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1791">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="8c5c8-1792">Cmdlet 'Get-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1792">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="8c5c8-1793">已移除 Cmdlet 'Get-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1793">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="8c5c8-1794">已移除類型為 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' 的屬性 'OperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1794">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="8c5c8-1795">已移除類型為 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' 的屬性 'OperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1795">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="8c5c8-1796">Cmdlet 'New-AzIotHubExportDevice' 已不再支援別名 'New-AzIotHubExportDevices'。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1796">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="8c5c8-1797">Cmdlet 'New-AzIotHubImportDevice' 已不再支援別名 'New-AzIotHubImportDevices'。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1797">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="8c5c8-1798">Cmdlet 'Remove-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1798">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="8c5c8-1799">已移除 Cmdlet 'Remove-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1799">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="8c5c8-1800">Cmdlet 'Set-AzIotHub' 已不再支援參數 'OperationsMonitoringProperties'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1800">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="8c5c8-1801">已移除 Cmdlet 'Set-AzIotHub' 的參數集 'UpdateOperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1801">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8c5c8-1802">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1802">Az.RecoveryServices</span></span>
* <span data-ttu-id="8c5c8-1803">Azure Site Recovery 支援將 NSG、公用 IP 和 Azure 的內部負載平衡器網路資源設定為 Azure。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1803">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="8c5c8-1804">Azure Site Recovery 支援從 VMware 寫入 Azure 受控磁碟。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1804">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="8c5c8-1805">Azure Site Recovery 支援從 VMware 到 Azure 的 NIC 縮減。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1805">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="8c5c8-1806">Azure Site Recovery 支援從 Azure 到 Azure 的加速網路。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1806">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="8c5c8-1807">Azure Site Recovery 支援從 Azure 到 Azure 的代理程式自動更新。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1807">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="8c5c8-1808">Azure Site Recovery 支援從 Azure 到 Azure 的標準 SSD。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1808">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="8c5c8-1809">Azure Site Recovery 支援從 Azure 到 Azure 的 Azure 磁碟加密傳遞。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1809">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="8c5c8-1810">Azure Site Recovery 提供從 Azure 到 Azure 的新增磁碟保護支援。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1810">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="8c5c8-1811">已新增 VM 的 SoftDelete 功能，並新增了 SoftDelete 的測試</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1811">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="8c5c8-1812">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1812">Az.Resources</span></span>
* <span data-ttu-id="8c5c8-1813">將相依性組件 Microsoft.Extensions.Caching.Memory 從1.1.1 更新為 2.2</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1813">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8c5c8-1814">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1814">Az.Network</span></span>
* <span data-ttu-id="8c5c8-1815">變更 PrivateEndpointConnection 的所有 Cmdlet，以支援一般服務提供者。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1815">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="8c5c8-1816">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1816">Updated cmdlet:</span></span>
        - <span data-ttu-id="8c5c8-1817">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1817">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8c5c8-1818">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1818">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8c5c8-1819">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1819">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8c5c8-1820">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1820">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8c5c8-1821">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1821">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="8c5c8-1822">為 PrivateLinkResource 新增新的 Cmdlet，其同時支援一般服務提供者。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1822">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="8c5c8-1823">新的 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1823">New cmdlet:</span></span>
        - <span data-ttu-id="8c5c8-1824">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1824">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="8c5c8-1825">新增功能 Proxy Protocol V2 的新欄位和參數。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1825">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="8c5c8-1826">在 PrivateLinkService 中新增屬性 EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1826">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="8c5c8-1827">在 PrivateEndpointConnection 中新增屬性 LinkIdentifier</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1827">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="8c5c8-1828">更新了 New-AzPrivateLinkService 以新增選擇性參數 EnableProxyProtocol。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1828">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="8c5c8-1829">修正 'New-AzApplicationGatewaySku' 參考文件中不正確的參數描述</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1829">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="8c5c8-1830">新增 Cmdlet 以支援 Azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1830">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="8c5c8-1831">為 VirtualHub的子資源 RouteTables 新增支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1831">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="8c5c8-1832">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1832">New cmdlets added:</span></span>
        - <span data-ttu-id="8c5c8-1833">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1833">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="8c5c8-1834">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1834">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="8c5c8-1835">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1835">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="8c5c8-1836">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1836">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="8c5c8-1837">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1837">Set-AzVirtualHub</span></span>
* <span data-ttu-id="8c5c8-1838">新增 VirtualHub 的新屬性 SKU 和 VirtualWan 的 VirtualWANType 支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1838">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="8c5c8-1839">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1839">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="8c5c8-1840">New-AzVirtualHub：新增了參數 SKU</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1840">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="8c5c8-1841">Update-AzVirtualHub：新增了參數 SKU</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1841">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="8c5c8-1842">New-AzVirtualWan：新增了參數 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1842">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="8c5c8-1843">Update-AzVirtualWan：新增了參數 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1843">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="8c5c8-1844">為 HubVnetConnection、VpnConnection 和 ExpressRouteConnection 新增 EnableInternetSecurity 屬性的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1844">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="8c5c8-1845">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1845">New cmdlets added:</span></span>
        - <span data-ttu-id="8c5c8-1846">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1846">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="8c5c8-1847">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1847">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="8c5c8-1848">New-AzureRmVirtualHubVnetConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1848">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="8c5c8-1849">New-AzureRmVpnConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1849">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="8c5c8-1850">Update-AzureRmVpnConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1850">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="8c5c8-1851">New-AzureRmExpressRouteConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1851">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="8c5c8-1852">Set-AzureRmExpressRouteConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1852">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="8c5c8-1853">新增設定 TopLevel WebApplicationFirewall 原則的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1853">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="8c5c8-1854">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1854">New cmdlets added:</span></span>
        - <span data-ttu-id="8c5c8-1855">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1855">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="8c5c8-1856">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1856">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="8c5c8-1857">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1857">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="8c5c8-1858">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1858">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="8c5c8-1859">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1859">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="8c5c8-1860">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1860">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="8c5c8-1861">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1861">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="8c5c8-1862">New-AzApplicationGatewayFirewallPolicy：新增了參數 PolicySetting、ManagedRule</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1862">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="8c5c8-1863">已在 CustomRule 上新增對 Geo-Match 運算子的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1863">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="8c5c8-1864">已將 GeoMatch 新增至 FirewallCondition 上的運算子</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1864">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="8c5c8-1865">已新增 perListener 和 perSite 防火牆原則的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1865">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="8c5c8-1866">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1866">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="8c5c8-1867">New-AzApplicationGatewayHttpListener：新增了參數 FirewallPolicy、FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1867">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="8c5c8-1868">New-AzApplicationGatewayPathRuleConfig：新增了參數 FirewallPolicy、FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1868">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="8c5c8-1869">將 'PSBastion' 中名稱為 AzureBastionSubnet 的必要子網路修正為可不區分大小寫</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1869">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="8c5c8-1870">支援網路規則中的目的地 FQDN，以及適用於 Azure 防火牆的 NAT 規則中轉譯的 FQDN</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1870">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="8c5c8-1871">為 IpGroup的上層資源 RouteTables 新增支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1871">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="8c5c8-1872">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1872">New cmdlets added:</span></span>
        - <span data-ttu-id="8c5c8-1873">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1873">New-AzIpGroup</span></span>
        - <span data-ttu-id="8c5c8-1874">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1874">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="8c5c8-1875">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1875">Get-AzIpGroup</span></span>
        - <span data-ttu-id="8c5c8-1876">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1876">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8c5c8-1877">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1877">Az.ServiceFabric</span></span>
* <span data-ttu-id="8c5c8-1878">移除 Add-AzServiceFabricApplicationCertificate Cmdlet，因為 Add-AzVmssSecret 會涵蓋此案例。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1878">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="8c5c8-1879">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1879">Az.Sql</span></span>
* <span data-ttu-id="8c5c8-1880">已新增在受控執行個體上還原已卸載之資料庫的支援。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1880">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="8c5c8-1881">已從程式碼中淘汰舊版的審核 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1881">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="8c5c8-1882">移除了已淘汰的別名：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1882">Removed deprecated aliases:</span></span>
* <span data-ttu-id="8c5c8-1883">Get-AzSqlDatabaseIndexRecommendations (改為使用 Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1883">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="8c5c8-1884">Get-AzSqlDatabaseRestorePoints (改為使用 Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1884">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="8c5c8-1885">移除 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1885">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="8c5c8-1886">移除已淘汰的弱點評估設定 Cmdlet 的別名</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1886">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="8c5c8-1887">淘汰進階威脅偵測設定 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1887">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="8c5c8-1888">在 Disable 中新增 Cmdlet 以啟用資料庫中資料行的敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1888">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8c5c8-1889">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1889">Az.Storage</span></span>
* <span data-ttu-id="8c5c8-1890">支援在建立或更新儲存體帳戶時啟用大型檔案共用</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1890">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="8c5c8-1891">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1891">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="8c5c8-1892">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1892">Set-AzStorageAccount</span></span>
* <span data-ttu-id="8c5c8-1893">當關閉/取得檔案控制代碼時，跳過檢查輸入路徑是否為檔案目錄或檔案，以避免物件處於 DeletePending 狀態時失敗</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1893">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="8c5c8-1894">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1894">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="8c5c8-1895">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1895">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="8c5c8-1896">2.8.0 - 2019 年10月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1896">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="8c5c8-1897">一般</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1897">General</span></span>
* <span data-ttu-id="8c5c8-1898">Az.HealthcareApis 1.0.0 版本</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1898">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8c5c8-1899">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1899">Az.Accounts</span></span>
* <span data-ttu-id="8c5c8-1900">針對產生的模組更新遙測和重寫 URL，修正 Windows 單元測試。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1900">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8c5c8-1901">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1901">Az.ApiManagement</span></span>
* <span data-ttu-id="8c5c8-1902">**Set-AzApiManagementApi** - 已新增在 ApiVersionSet 中更新 API 的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1902">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="8c5c8-1903">修正 https://github.com/Azure/azure-powershell/issues/10068 的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1903">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8c5c8-1904">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1904">Az.Automation</span></span>
* <span data-ttu-id="8c5c8-1905">已針對 Linux 重新啟動設定參數修正了 New-AzureAutomationSoftwareUpdateConfiguration Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1905">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="8c5c8-1906">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1906">Az.Batch</span></span>
* <span data-ttu-id="8c5c8-1907">**Get-AzBatchNodeAgentSku** 已被取代，在版本 2.0.0 中會由 **Get-AzBatchSupportImage** 取代。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1907">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8c5c8-1908">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1908">Az.Compute</span></span>
* <span data-ttu-id="8c5c8-1909">在 New-AzVM 和 New-AzVmss Cmdlet 中新增 Priority、EvictionPolicy 和 MaxPrice 參數</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1909">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="8c5c8-1910">修正 Add-AzVMAdditionalUnattendContent 和 Add-AzVMSshPublicKey Cmdlet 的警告訊息和說明文件</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1910">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="8c5c8-1911">修正 Linux VM 的 -skipVmBackup 例外狀況，以及 Set-AzVMDiskEncryptionExtension 的受控磁碟。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1911">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="8c5c8-1912">修正 Set-AzVMDiskEncryptionExtension 中更新加密設定中的錯誤 (bug)，兩種傳遞案例。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1912">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8c5c8-1913">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1913">Az.DataFactory</span></span>
* <span data-ttu-id="8c5c8-1914">針對 ADF V2 資料流程新增 CRUD 命令：Set-AzDataFactoryV2DataFlow、Remove-AzDataFactoryV2DataFlow 和 Get-AzDataFactoryV2DataFlow。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1914">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="8c5c8-1915">針對 ADF V2 資料流程偵錯工作階段新增動作命令：Start-AzDataFactoryV2DataFlowDebugSession、Get-AzDataFactoryV2DataFlowDebugSession、Add-AzDataFactoryV2DataFlowDebugSessionPackage、Invoke-AzDataFactoryV2DataFlowDebugSessionCommand 和 Stop-AzDataFactoryV2DataFlowDebugSession。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1915">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="8c5c8-1916">將 ADF .Net SDK 版本更新為 4.2.0</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1916">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8c5c8-1917">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1917">Az.DataLakeStore</span></span>
* <span data-ttu-id="8c5c8-1918">修正帳戶驗證，以便在沒有網域的情況下傳遞具有 '-' 的帳戶</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1918">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="8c5c8-1919">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1919">Az.HealthcareApis</span></span>
* <span data-ttu-id="8c5c8-1920">已將 Powershell 版本更新為 1.0.0</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1920">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="8c5c8-1921">已將 SDK 版本更新為 1.0.2</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1921">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="8c5c8-1922">更新測試以參考新的 SDK 版本</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1922">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="8c5c8-1923">已將輸出結構從巢狀更新為壓平合併。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1923">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8c5c8-1924">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1924">Az.IotHub</span></span>
* <span data-ttu-id="8c5c8-1925">新增新的路由來源：DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1925">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="8c5c8-1926">次要錯誤修正：Get-AzIothub 未傳回 subscriptionId</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1926">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8c5c8-1927">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1927">Az.Monitor</span></span>
* <span data-ttu-id="8c5c8-1928">已針對動作群組新增新的動作群組接收器   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1928">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="8c5c8-1929">針對接收器使用已啟用的一般警示結構描述。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1929">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="8c5c8-1930">這不適用於 SMS、Azure App 撨送、ITSM 和 Voice 接收器</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1930">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="8c5c8-1931">Webhooks 現在支援 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1931">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8c5c8-1932">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1932">Az.Network</span></span>
* <span data-ttu-id="8c5c8-1933">新增新的 Cmdlet Get-AzAvailableServiceAlias 以便進行呼叫並取得可用於服務端點原則的別名。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1933">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="8c5c8-1934">已在虛擬網路閘道連線新增了流量選取器的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1934">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="8c5c8-1935">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1935">New cmdlets added:</span></span>
        - <span data-ttu-id="8c5c8-1936">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1936">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="8c5c8-1937">已更新選用參數的 Cmdlet -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1937">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="8c5c8-1938">新增網路安全性規則組態中針對 ESP 和 AH 通訊協定的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1938">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="8c5c8-1939">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1939">Updated cmdlets:</span></span>
        - <span data-ttu-id="8c5c8-1940">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1940">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="8c5c8-1941">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1941">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="8c5c8-1942">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1942">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="8c5c8-1943">改善 Cortex Cmdlet 中的例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1943">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="8c5c8-1944">適用於 VirtualNetworkGateways 的新項目和 SKU</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1944">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="8c5c8-1945">引進新一代的 VirtualNetworkGateways。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1945">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="8c5c8-1946">引進適用於 VirtualNetworkGateways 的全新高輸送量 SKU。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1946">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="8c5c8-1947">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1947">Az.RedisCache</span></span>
* <span data-ttu-id="8c5c8-1948">更新了 'Set-AzRedisCache' 參考文件，納入了 '-Size' 參數缺少的值</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1948">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="8c5c8-1949">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1949">Az.Sql</span></span>
* <span data-ttu-id="8c5c8-1950">新增在受控執行個體上設定 Active Directory 系統管理員的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1950">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8c5c8-1951">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1951">Az.Storage</span></span>
* <span data-ttu-id="8c5c8-1952">將儲存體用戶端程式庫升級為 11.1.0</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1952">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="8c5c8-1953">列出具有管理平面 API 的容器，將會以 NextPageLink 列出</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1953">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="8c5c8-1954">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1954">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="8c5c8-1955">列出訂用帳戶中的儲存體帳戶，將會以 NextPageLink 列出</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1955">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="8c5c8-1956">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1956">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="8c5c8-1957">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1957">Az.StorageSync</span></span>
* <span data-ttu-id="8c5c8-1958">修正 Reset-AzStorageSyncServerCertificate 中的問題 9810。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1958">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8c5c8-1959">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1959">Az.Websites</span></span>
* <span data-ttu-id="8c5c8-1960">Set-AzWebApp 更新應用程式的 ASP 時失敗</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1960">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="8c5c8-1961">2.7.0 - 2019 年 9 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1961">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="8c5c8-1962">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1962">Az.ApiManagement</span></span>
* <span data-ttu-id="8c5c8-1963">更新 'Set-AzApiManagementPolicy' 參考文件中的 '-Format' 參數描述</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1963">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="8c5c8-1964">已移除參考文件中的 'Update-AzApiManagementDeployment' 參考，此 Cmdlet 已被取代。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1964">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="8c5c8-1965">改為使用 'Set-AzApiManagement'。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1965">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8c5c8-1966">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1966">Az.Automation</span></span>
* <span data-ttu-id="8c5c8-1967">已修正 'Register-AzAutomationDscNode' 參考文件中範例的錯別字</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1967">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="8c5c8-1968">已新增 Register-AzAutomationDSCNode 的 OS 限制說明</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1968">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="8c5c8-1969">已針對 -Wait 選項修正了 Start-AzAutomationRunbook Cmdlet 的 Null 參考例外狀況。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1969">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8c5c8-1970">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1970">Az.Compute</span></span>
* <span data-ttu-id="8c5c8-1971">在 New-AzDiskConfig 中新增 UploadSizeInBytes 參數</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1971">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="8c5c8-1972">在 New-AzSnapshotConfig 中新增增量參數</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1972">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="8c5c8-1973">新增低優先順序虛擬機器功能：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1973">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="8c5c8-1974">已將 MaxPrice、EvictionPolicy 和 Priority 參數新增到 New-AzVMConfig。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1974">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="8c5c8-1975">已將 MaxPrice 參數新增到 New-AzVmssConfig、Update-AzVM 和 Update-AzVmss Cmdlet 中。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1975">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="8c5c8-1976">修正 Get-AzAvailabilitySet Cmdlet 的參考問題，以免在訂用帳戶中列出所有可用性設定組。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1976">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="8c5c8-1977">修正 Get-AzRemoteDesktopFile 的 Null 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1977">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="8c5c8-1978">修正適用於端點相關位置的 VHD Seek 方法。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1978">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="8c5c8-1979">修正 New-AzVM 和 Update-AzVM 的 UltraSSD 問題。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1979">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8c5c8-1980">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1980">Az.DataFactory</span></span>
* <span data-ttu-id="8c5c8-1981">為 ADF V2 新增 3 個新命令 - Add-AzDataFactoryV2TriggerSubscription、Remove-AzDataFactoryV2TriggerSubscription 和 Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1981">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="8c5c8-1982">已將 ADF .Net SDK 版本更新為 4.1.3</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1982">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8c5c8-1983">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1983">Az.HDInsight</span></span>
* <span data-ttu-id="8c5c8-1984">呼叫重大變更</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1984">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8c5c8-1985">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1985">Az.IotHub</span></span>
* <span data-ttu-id="8c5c8-1986">針對異地配對災害復原區域新增叫用 IotHub 容錯移轉的支援。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1986">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="8c5c8-1987">新增管理 IotHub 訊息擴充的支援。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1987">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="8c5c8-1988">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1988">New cmdlets are:</span></span>
    - <span data-ttu-id="8c5c8-1989">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1989">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="8c5c8-1990">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1990">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="8c5c8-1991">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1991">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="8c5c8-1992">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1992">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8c5c8-1993">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1993">Az.Monitor</span></span>
* <span data-ttu-id="8c5c8-1994">指向最近的監視 SDK，例如 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1994">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="8c5c8-1995">在 Metrics Cmdlet 中新增不會造成中斷的變更，例如單位列舉支援數個新值。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1995">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="8c5c8-1996">這些 Cmdlet 是唯讀的，因此 Cmdlet 的輸出中不會有任何變更。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1996">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="8c5c8-1997">**ActionGroups** 要求的 api-version 現在為 **2019-06-01**，之前為 **2018-03-01**。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1997">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="8c5c8-1998">已針對此項變更新增多個案例測試。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1998">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="8c5c8-1999">**EmailReceiver** 和 **WebhookReceiver** 類別的建構函式新增了一個新的強制引數，例如稱為 **useCommonAlertSchema** 的布林值。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-1999">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="8c5c8-2000">目前，該值已修正為 **false** 以隱藏 Cmdlet 的重大變更。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2000">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="8c5c8-2001">**注意**：這是暫時性的變更，必須由警示小組驗證。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2001">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="8c5c8-2002">**Source** 類別之建構函式的引數順序 (與 **ScheduledQueryRuleSource** 類別相關) 已變更，不再是先前的 SDK。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2002">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="8c5c8-2003">此變更需要修正兩個單元測試：這兩個單元已進行編譯，但無法通過測試。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2003">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="8c5c8-2004">**AlertingAction** 類別之建構函式的引數順序 (與 **ScheduledQueryRuleSource** 類別相關) 已變更，不再是先前的 SDK。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2004">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="8c5c8-2005">此變更需要修正兩個單元測試：這兩個單元已進行編譯，但無法通過測試。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2005">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="8c5c8-2006">適用於計量警示 V2 的支援動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2006">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="8c5c8-2007">New-AzMetricAlertRuleV2Criteria：目前也建立動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2007">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="8c5c8-2008">Add-AzMetricAlertRuleV2：目前也接受動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2008">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="8c5c8-2009">已排程查詢規則 Cmdlet (SQR) 中的改善項目</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2009">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="8c5c8-2010">Cmdlets 接受兩種格式的 'Location' 參數，包含位置 (例如 eastus) 或位置顯示名稱 (例如美國東部)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2010">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="8c5c8-2011">在說明檔案中適當地描述 ’Enabled’ 參數</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2011">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="8c5c8-2012">已新增 'ActionGroup' 選用參數的範例</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2012">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="8c5c8-2013">說明檔內容全面改善</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2013">Overall improved help files</span></span>
* <span data-ttu-id="8c5c8-2014">修正判斷 'Set-AzActionRule' 範圍類型的錯誤</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2014">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8c5c8-2015">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2015">Az.Network</span></span>
* <span data-ttu-id="8c5c8-2016">修正 'New-AzApplicationGateway' 參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2016">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="8c5c8-2017">在 'Get-AzNetworkWatcherPacketCapture' 參考文件中新增註解，說明擷取封包取得之所有屬性的相關資訊</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2017">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="8c5c8-2018">已修正 'Test-AzNetworkWatcherIPFlow' 參考文件中的範例，以便正確地列舉 NIC</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2018">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="8c5c8-2019">改善了雲端例外狀況剖析，以便顯示其他詳細資料 (若有)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2019">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="8c5c8-2020">改善了雲端例外狀況剖析，以便處理 SDK 例外狀況的其他類型</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2020">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="8c5c8-2021">修正了不正確的安全性規則模型對應</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2021">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="8c5c8-2022">在網路介面中新增了屬性以提供 IP 功能</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2022">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="8c5c8-2023">在 PSNetworkInterface 中新增了 'PrivateEndpoint' 屬性作為 PSResourceId 類型</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2023">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="8c5c8-2024">在 PSNetworkInterfaceIPConfiguration 中新增了 'PrivateLinkConnectionProperties' 屬性作為 PSIpConfigurationConnectivityInformation 類型</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2024">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="8c5c8-2025">新增了模型類別 PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2025">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="8c5c8-2026">針對 Azure 防火牆資源新增了 ApplicationRuleProtocolType 'mssql'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2026">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="8c5c8-2027">在虛擬 WAN 中支援多連結</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2027">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="8c5c8-2028">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2028">New cmdlets</span></span>
        - <span data-ttu-id="8c5c8-2029">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2029">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="8c5c8-2030">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2030">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="8c5c8-2031">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2031">Updated cmdlet:</span></span>
        - <span data-ttu-id="8c5c8-2032">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2032">New-VpnSite</span></span>
        - <span data-ttu-id="8c5c8-2033">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2033">Update-VpnSite</span></span>
        - <span data-ttu-id="8c5c8-2034">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2034">New-VpnConnection</span></span>
        - <span data-ttu-id="8c5c8-2035">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2035">Update-VpnConnection</span></span>
* <span data-ttu-id="8c5c8-2036">修正了文件中的部分 PowerShell 範例，改為使用 Az Cmdlet 而非 AzureRM Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2036">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8c5c8-2037">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2037">Az.RecoveryServices</span></span>
* <span data-ttu-id="8c5c8-2038">透過 ProtectedItemsCount 屬性更新 AzureVMpolicy 物件</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2038">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="8c5c8-2039">新增了 VM 原則和原始儲存體帳戶還原的測試</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2039">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="8c5c8-2040">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2040">Az.Resources</span></span>
* <span data-ttu-id="8c5c8-2041">修正無法在沒有參數範圍的情況下呼叫 New-AzRoleAssignment 的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2041">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8c5c8-2042">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2042">Az.ServiceFabric</span></span>
* <span data-ttu-id="8c5c8-2043">修正了 'Update-AzServiceFabricReliability' 參考文件中範例的錯字</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2043">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="8c5c8-2044">新增 Cmdlet 以管理應用程式和服務：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2044">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="8c5c8-2045">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2045">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="8c5c8-2046">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2046">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="8c5c8-2047">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2047">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="8c5c8-2048">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2048">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="8c5c8-2049">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2049">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="8c5c8-2050">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2050">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="8c5c8-2051">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2051">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="8c5c8-2052">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2052">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="8c5c8-2053">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2053">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="8c5c8-2054">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2054">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="8c5c8-2055">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2055">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="8c5c8-2056">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2056">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="8c5c8-2057">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2057">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="8c5c8-2058">已將 Service Fabric SDK 更新為版本 1.2.0，此版本使用服務網狀架構資源提供者 api-version 2019-03-01。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2058">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="8c5c8-2059">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2059">Az.SignalR</span></span>
* <span data-ttu-id="8c5c8-2060">新增 Update、Restart、CheckNameAvailability、GetUsage 等 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2060">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="8c5c8-2061">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2061">Az.Sql</span></span>
* <span data-ttu-id="8c5c8-2062">更新 'Get-AzSqlElasticPool' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2062">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="8c5c8-2063">新增了虛擬核心範例以建立彈性集區 (New-AzSqlElasticPool)。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2063">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="8c5c8-2064">移除 EmailAddresses 的驗證，並確認 Set-AzSqlServerAdvancedThreatProtectionPolicy 和 Set-AzSqlDatabaseAdvancedThreatProtectionPolicy 中的 EmailAdmins 為空的情況下 EmailAdmins 的狀態並非 false</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2064">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="8c5c8-2065">當多個啟用稽核分類的診斷設定存在時，啟用了伺服器/資料庫稽核設定的移除功能。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2065">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="8c5c8-2066">修正多個 Sql 弱點評估 Cmdlet 中的電子郵件地址驗證 (Update-AzSqlDatabaseVulnerabilityAssessmentSetting、Update-AzSqlServerVulnerabilityAssessmentSetting、Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting 和 Update-AzSqlInstanceVulnerabilityAssessmentSetting)。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2066">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8c5c8-2067">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2067">Az.Storage</span></span>
* <span data-ttu-id="8c5c8-2068">已更新 'Get-AzStorageAccountKey' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2068">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="8c5c8-2069">在上傳/下載 Azure 檔案中，支援保留目的地檔案中的來源檔案 SMB 屬性 (檔案屬性、檔案建立時間、檔案最後入時間)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2069">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="8c5c8-2070">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2070">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="8c5c8-2071">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2071">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="8c5c8-2072">修正上傳區塊 Blob 的屬性/metadate 在啟用 ImmutabilityPolicy 的容器中失敗的問題。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2072">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="8c5c8-2073">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2073">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="8c5c8-2074">支援透過管理平面 API 管理 Azure 檔案共用</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2074">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="8c5c8-2075">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2075">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="8c5c8-2076">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2076">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="8c5c8-2077">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2077">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="8c5c8-2078">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2078">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8c5c8-2079">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2079">Az.Websites</span></span>
* <span data-ttu-id="8c5c8-2080">修正將應用程式遷移到新的 ASP 時系統會刪除 webapp 標籤的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2080">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="8c5c8-2081">修正 Publish-AzureWebapp 以在 Linux 和 Windows 上運作</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2081">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="8c5c8-2082">更新 'Get-AzWebAppPublishingProfile' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2082">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="8c5c8-2083">2.6.0 - 2019 年 8 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2083">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="8c5c8-2084">一般</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2084">General</span></span>
* <span data-ttu-id="8c5c8-2085">修正了多個模組中的各種錯字問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2085">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8c5c8-2086">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2086">Az.Accounts</span></span>
* <span data-ttu-id="8c5c8-2087">支援 Azure Functions 驗證中使用者指派的 MSI (#9479)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2087">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="8c5c8-2088">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2088">Az.Aks</span></span>
* <span data-ttu-id="8c5c8-2089">修正 'Get-AzAks' 的輸出問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2089">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="8c5c8-2090">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2090">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8c5c8-2091">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2091">Az.ApiManagement</span></span>
* <span data-ttu-id="8c5c8-2092">修正 https://github.com/Azure/azure-powershell/issues/9351 的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2092">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="8c5c8-2093">更新 .Net NuGet 版本，此版本不會強制執行 productId、apiId、groupId 和 userId 的限制</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2093">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="8c5c8-2094">**Get-AzApiManagementProduct** - 新增了使用 API 查詢產品的支援。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2094">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="8c5c8-2095">**New-AzApiManagementApiRevision** - 修正在建立新 API 版本時並未設定 ApiRevisionDescription 的問題 https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2095">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="8c5c8-2096">將模型 'PsApiManagementOAuth2AuthrozationServer' 中的錯字修正為 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2096">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="8c5c8-2097">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2097">Az.Batch</span></span>
* <span data-ttu-id="8c5c8-2098">修正了說明訊息和文件中的錯字，將 Windows 首字變大寫</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2098">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8c5c8-2099">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2099">Az.Cdn</span></span>
* <span data-ttu-id="8c5c8-2100">修正了 CDN 模組轉換協助程式中的錯字</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2100">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8c5c8-2101">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2101">Az.Compute</span></span>
* <span data-ttu-id="8c5c8-2102">將 VmssId 新增到 New-AzVMConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2102">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="8c5c8-2103">將 TerminateScheduledEvents 和 TerminateScheduledEventNotBeforeTimeoutInMinutes 參數新增到 New-AzVmssConfig 和 Update-AzVmss 中</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2103">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="8c5c8-2104">將 HyperVGeneration 屬性新增到 VM 映像物件中</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2104">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="8c5c8-2105">新增 Host 和 HostGroup 功能</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2105">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="8c5c8-2106">新的 Cmdlet： New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2106">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="8c5c8-2107">已將 HostId 參數新增到 New-AzVMConfig 和 New-AzVM 中</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2107">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="8c5c8-2108">更新 'Invoke-AzVMRunCommand' 文件中的範例，使用了正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2108">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="8c5c8-2109">更新 'Set-AzVMDiskEncryptionExtension' 和 'Set-AzVmssDiskEncryptionExtension' 參考文件中的 '-VolumeType' 描述</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2109">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8c5c8-2110">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2110">Az.DataFactory</span></span>
* <span data-ttu-id="8c5c8-2111">修正錯字，將 'New-AzDataFactoryEncryptValue' 文件中的 'Windows' 變成首字大寫</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2111">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="8c5c8-2112">已將 ADF .Net SDK 版本更新為 4.1.2</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2112">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="8c5c8-2113">對 'Set-AzureRmDataFactoryV2IntegrationRuntime' Cmd 新增參數 'DataProxyIntegrationRuntimeName'、'DataProxyStagingLinkedServiceName' 和 'DataProxyStagingPath'，以將自我裝載整合執行階段設定為適用於 SSIS 整合執行階段的 Proxy</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2113">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="8c5c8-2114">更新了 PSTriggerRun 以顯示觸發的管線、訊息、屬性和 PSActivityRun，以顯示活動類型</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2114">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8c5c8-2115">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2115">Az.DataLakeStore</span></span>
* <span data-ttu-id="8c5c8-2116">修正 Get-DataLakeStoreDeletedItem 凸排的問題，避免產生任何錯誤或遠端例外狀況。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2116">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8c5c8-2117">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2117">Az.EventHub</span></span>
* <span data-ttu-id="8c5c8-2118">修正 #9658 的問題：Set-AzEventHubNetworkRuleSet 中 VirtualNteworkRule 參數的錯字問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2118">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="8c5c8-2119">修正 #9558 的問題：Set-AzEventHubNamespace 使用 PATCH 而非 PUT</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2119">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="8c5c8-2120">已將 EnableKafka 參數新增到 Set-AzEventHubNamespace Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2120">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="8c5c8-2121">修正 #9786 的問題：無法建立僅限接聽權限的規則</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2121">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="8c5c8-2122">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2122">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="8c5c8-2123">修正了文件中 'Azure'均為小寫的錯字問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2123">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8c5c8-2124">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2124">Az.Monitor</span></span>
* <span data-ttu-id="8c5c8-2125">已修正說明文件中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2125">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8c5c8-2126">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2126">Az.Network</span></span>
* <span data-ttu-id="8c5c8-2127">更新了 New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2127">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="8c5c8-2128">取代了 'PublicIpAddress' 參數，因為伺服器端從未使用過此參數。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2128">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="8c5c8-2129">新增了選用參數 'Primary'，指出正確的 IP 設定是否為主要。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2129">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="8c5c8-2130">改善了 SDK 要求錯誤例外狀況的處理方式 - 修正了之前未正確處理的 SDK 例外狀況而導致金鑰錯誤詳細資料並未顯示的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2130">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="8c5c8-2131">調整了 Ipv6 IP 首碼的驗證邏輯，以便檢查正確的 IPv6 前置長度。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2131">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="8c5c8-2132">更新了 Get-AzVirtualNetworkSubnetConfig：依子網路 ID 新增了要取得的參數集。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2132">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="8c5c8-2133">對 AzNetworkServiceTag 新增位置參數的描述</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2133">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8c5c8-2134">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2134">Az.OperationalInsights</span></span>
* <span data-ttu-id="8c5c8-2135">更新了 'New-AzOperationalInsightsLinuxSyslogDataSource' 文件</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2135">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="8c5c8-2136">新增了範例</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2136">Added example</span></span>
    - <span data-ttu-id="8c5c8-2137">更新了 '-Name' 參數的說明</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2137">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="8c5c8-2138">新增了 New-AzOperationalInsightsWindowsEventDataSource 的範例</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2138">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="8c5c8-2139">對 New-AzOperationalInsightsWindowsEventDataSource 變更了 -Name 參數的描述</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2139">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8c5c8-2140">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2140">Az.RecoveryServices</span></span>
* <span data-ttu-id="8c5c8-2141">更新 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2141">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="8c5c8-2142">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2142">Az.Resources</span></span>
* <span data-ttu-id="8c5c8-2143">新增對於 Microsoft.Resource 新 API 版本 2019-05-10 的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2143">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="8c5c8-2144">新增對 'copy.count = 0' 中的變數、資源和屬性的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2144">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="8c5c8-2145">完整模式中將會刪除具有 'condition = false' 或 'copy.count = 0' 的資源</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2145">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="8c5c8-2146">在說明文件的訂閱層級中新增了指派原則範例</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2146">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8c5c8-2147">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2147">Az.ServiceBus</span></span>
* <span data-ttu-id="8c5c8-2148">修正 #9658 的問題：Set-AzServiceBusNetworkRuleSet 中 VirtualNetworkRule 參數的錯字</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2148">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="8c5c8-2149">修正 #9786 的問題：無法建立僅限接聽權限的規則</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2149">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="8c5c8-2150">新增了 'Test-AzServiceBusNameAvailability' 命令以檢查佇列和主題的名稱可用性</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2150">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8c5c8-2151">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2151">Az.ServiceFabric</span></span>
* <span data-ttu-id="8c5c8-2152">修正新增節點類型 Cmdlet 錯誤 (bug)：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2152">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="8c5c8-2153">當資源群組具有其他與服務網狀架構叢集不相關之 vmss 時的 NullReferenceException 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2153">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="8c5c8-2154">修正問題： https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2154">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="8c5c8-2155">修正若 virtualNetwork 在與叢集不同的資源群組中時 Cmdlet 會失敗的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2155">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="8c5c8-2156">修正問題： https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2156">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="8c5c8-2157">取代 Add-AzServiceFabricApplicationCertificate Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2157">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="8c5c8-2158">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2158">Az.Sql</span></span>
* <span data-ttu-id="8c5c8-2159">更新舊版 Auditing Cmdlet 文件。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2159">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8c5c8-2160">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2160">Az.Storage</span></span>
* <span data-ttu-id="8c5c8-2161">更新 Get/Close-AzStorageFileHandle 的說明，在 Cmdlet 範例中新增更多案例並更新參數描述</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2161">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="8c5c8-2162">支援上傳 Blob 和複製 Blob 中的 StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2162">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="8c5c8-2163">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2163">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="8c5c8-2164">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2164">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="8c5c8-2165">支援複製 Blob 中的 Rehydrate Priority</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2165">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="8c5c8-2166">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2166">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8c5c8-2167">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2167">Az.Websites</span></span>
* <span data-ttu-id="8c5c8-2168">釐清 Set-AzWebApp 和 Set-AzWebAppSlot 中的 -AppSettings 參數的</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2168">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="8c5c8-2169">2.5.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2169">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8c5c8-2170">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2170">Az.Accounts</span></span>
* <span data-ttu-id="8c5c8-2171">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2171">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="8c5c8-2172">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2172">Az.ApplicationInsights</span></span>
* <span data-ttu-id="8c5c8-2173">修正 'Remove-AzApplicationInsightsApiKey' 文件中範例的錯字</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2173">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8c5c8-2174">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2174">Az.Automation</span></span>
* <span data-ttu-id="8c5c8-2175">修正資源字串中的錯字</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2175">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8c5c8-2176">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2176">Az.CognitiveServices</span></span>
* <span data-ttu-id="8c5c8-2177">新增了 NetworkRuleSet 支援。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2177">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8c5c8-2178">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2178">Az.Compute</span></span>
* <span data-ttu-id="8c5c8-2179">新增 虛擬機器執行個體檢視物件缺少的屬性 (ComputerName、OsName、OsVersion 和 HyperVGeneration)。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2179">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="8c5c8-2180">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2180">Az.ContainerRegistry</span></span>
* <span data-ttu-id="8c5c8-2181">修正 Replication 參數的 Remove-AzContainerRegistryReplication 中的錯字</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2181">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="8c5c8-2182">如需詳細資訊，請參閱 https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2182">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8c5c8-2183">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2183">Az.DataFactory</span></span>
* <span data-ttu-id="8c5c8-2184">已將 ADF .Net SDK 版本更新為 4.1.0</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2184">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="8c5c8-2185">修正 'Get-AzDataFactoryV2PipelineRun' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2185">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8c5c8-2186">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2186">Az.EventHub</span></span>
* <span data-ttu-id="8c5c8-2187">新增了 Cmmdlet 以產生 SAS 權杖：New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2187">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="8c5c8-2188">在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2188">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8c5c8-2189">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2189">Az.KeyVault</span></span>
* <span data-ttu-id="8c5c8-2190">新增了為憑證原則指定 KeySize 的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2190">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8c5c8-2191">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2191">Az.LogicApp</span></span>
* <span data-ttu-id="8c5c8-2192">修正 Get-AzIntegrationAccountMap 以列出所有對應類型</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2192">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="8c5c8-2193">新增了用於篩選的 MapType 參數</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2193">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="8c5c8-2194">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2194">Az.ManagedServices</span></span>
* <span data-ttu-id="8c5c8-2195">新增了 API 版本 2019-06-01 (GA) 的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2195">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8c5c8-2196">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2196">Az.Network</span></span>
* <span data-ttu-id="8c5c8-2197">新增私人端點和私人連結服務的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2197">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="8c5c8-2198">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2198">New cmdlets</span></span>
        - <span data-ttu-id="8c5c8-2199">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2199">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="8c5c8-2200">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2200">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="8c5c8-2201">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2201">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8c5c8-2202">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2202">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8c5c8-2203">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2203">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8c5c8-2204">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2204">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8c5c8-2205">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2205">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="8c5c8-2206">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2206">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="8c5c8-2207">已更新下列功能命令：Virtualnetwork 中子網路上的 PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies 旗標</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2207">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="8c5c8-2208">更新了 New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2208">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="8c5c8-2209">新增了選用參數 -PrivateEndpointNetworkPoliciesFlag，此參數會設定是否要套用此子網路中的私人端點網路原則。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2209">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="8c5c8-2210">新增了選用參數 -PrivateLinkServiceNetworkPoliciesFlag，此參數會設定是否要套用此子網路中的私人連結服務網路原則。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2210">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="8c5c8-2211">AzPrivateLinkService 的 Cmdlet 參數 'ServiceName' 已更名為 'Name' 搭配別名 'ServiceName' 以提供回溯相容性</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2211">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="8c5c8-2212">針對網路安全性規則組態啟用 ICMP 通訊協定</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2212">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="8c5c8-2213">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2213">Updated cmdlets</span></span>
        - <span data-ttu-id="8c5c8-2214">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2214">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="8c5c8-2215">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2215">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="8c5c8-2216">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2216">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="8c5c8-2217">新增 ConnectionProtocolType (Ikev1/Ikev2) 作為 New-AzVirtualNetworkGatewayConnection 的可設定參數</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2217">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="8c5c8-2218">在 LoadBalancerFrontendIpConfiguration 中新增 PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2218">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="8c5c8-2219">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2219">Updated cmdlet:</span></span>
        - <span data-ttu-id="8c5c8-2220">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2220">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="8c5c8-2221">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2221">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="8c5c8-2222">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2222">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="8c5c8-2223">更新應用程式閘道 New-AzApplicationGatewayProbeConfig 命令以支援探查中的自訂連接埠</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2223">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="8c5c8-2224">更新了 New-AzApplicationGatewayProbeConfig：新增了用來探查後端伺服器的選用參數 Port。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2224">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="8c5c8-2225">此參數適用於 Standard_V2 和 WAF_V2 SKU。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2225">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8c5c8-2226">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2226">Az.OperationalInsights</span></span>
* <span data-ttu-id="8c5c8-2227">更新了預設版本，讓已儲存的搜尋為 1。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2227">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="8c5c8-2228">修正了自訂記錄 Null 處理</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2228">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8c5c8-2229">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2229">Az.RecoveryServices</span></span>
* <span data-ttu-id="8c5c8-2230">更新 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2230">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="8c5c8-2231">更新 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2231">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="8c5c8-2232">更新 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2232">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="8c5c8-2233">更新 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2233">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="8c5c8-2234">更新 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2234">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="8c5c8-2235">更新 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2235">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="8c5c8-2236">更新 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2236">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="8c5c8-2237">更新 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2237">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="8c5c8-2238">針對 Azure File Share 的 Unregistering 容器更新了服務呼叫</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2238">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="8c5c8-2239">更新 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2239">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="8c5c8-2240">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2240">Az.Resources</span></span>
- <span data-ttu-id="8c5c8-2241">移除 'New-AzResourceGroupDeployment' 文件中參考的遺漏 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2241">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="8c5c8-2242">更新原則 Cmdlet 以使用新的 API 版本 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2242">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8c5c8-2243">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2243">Az.ServiceBus</span></span>
* <span data-ttu-id="8c5c8-2244">新增了 Cmmdlet 以產生 SAS 權杖：New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2244">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="8c5c8-2245">在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2245">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="8c5c8-2246">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2246">Az.Sql</span></span>
* <span data-ttu-id="8c5c8-2247">修正 Set-AzSqlDatabaseSecondary Cmdlet 遺漏的範例</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2247">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="8c5c8-2248">修正集合弱點評量期性掃描並未提供任何電子郵件地址的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2248">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="8c5c8-2249">修正警告訊息中的錯字。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2249">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8c5c8-2250">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2250">Az.Storage</span></span>
* <span data-ttu-id="8c5c8-2251">更新 'Get-AzStorageAccount' 參考文件中的範例，以使用正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2251">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="8c5c8-2252">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2252">Az.StorageSync</span></span>
* <span data-ttu-id="8c5c8-2253">新增 Invoke-AzStorageSyncChangeDetection Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2253">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="8c5c8-2254">修正問題 9551 以接受 TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2254">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8c5c8-2255">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2255">Az.Websites</span></span>
* <span data-ttu-id="8c5c8-2256">修正 Get-AzWebApp 和 Set-AzWebApp 並未傳回部分 SiteConfig 屬性的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2256">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="8c5c8-2257">新增 Get-AzDeletedWebApp 和 Restore-AzDeletedWebApp 的位置參數</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2257">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="8c5c8-2258">修正 New-AzWebApp -IncludeSourceWebAppSlots 複製 Web 應用程式的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2258">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="8c5c8-2259">2.4.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2259">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8c5c8-2260">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2260">Az.Accounts</span></span>
* <span data-ttu-id="8c5c8-2261">新增設定檔 Cmdlet 的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2261">Add support for profile cmdlets</span></span>
* <span data-ttu-id="8c5c8-2262">在產生的 Cmdlet 中新增環境和資料平面的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2262">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="8c5c8-2263">修正以下錯誤，在 Windows PowerShell 中不正確的端點在某些情況下用於資料平面 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2263">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="8c5c8-2264">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2264">Az.Advisor</span></span>
* <span data-ttu-id="8c5c8-2265">Az.Advisor 的 GA 版本</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2265">GA release of Az.Advisor</span></span>
* <span data-ttu-id="8c5c8-2266">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2266">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8c5c8-2267">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2267">Az.ApiManagement</span></span>
* <span data-ttu-id="8c5c8-2268">修正 https://github.com/Azure/azure-powershell/issues/8671 的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2268">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="8c5c8-2269">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2269">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="8c5c8-2270">新增了依使用者和產品查詢訂用帳戶的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2270">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="8c5c8-2271">新增了使用 Scope '/'、'/apis'、'/apis/echo-api' 進行查詢的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2271">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="8c5c8-2272">修正 https://github.com/Azure/azure-powershell/issues/9307 和 https://github.com/Azure/azure-powershell/issues/8432 的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2272">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="8c5c8-2273">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2273">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="8c5c8-2274">新增了可在匯入 Api 時指定 'ApiVersion' 和 'ApiVersionSetId' 的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2274">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8c5c8-2275">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2275">Az.Automation</span></span>
* <span data-ttu-id="8c5c8-2276">修正了 Set-AzAutomationConnectionFieldValue Cmdlet 錯誤以處理字串值。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2276">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8c5c8-2277">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2277">Az.Compute</span></span>
* <span data-ttu-id="8c5c8-2278">將 HyperVGeneration 參數新增到 New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2278">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8c5c8-2279">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2279">Az.DataFactory</span></span>
* <span data-ttu-id="8c5c8-2280">更新取得活動執行、取得管線執行和取得觸發程序執行 ADF Cmdlet 的輸出，以支援 Select-Object 管道。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2280">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8c5c8-2281">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2281">Az.EventGrid</span></span>
* <span data-ttu-id="8c5c8-2282">修正 'New-AzEventGridSubscription' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2282">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8c5c8-2283">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2283">Az.IotHub</span></span>
* <span data-ttu-id="8c5c8-2284">新增對重新產生授權原則金鑰的支援。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2284">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8c5c8-2285">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2285">Az.Network</span></span>
* <span data-ttu-id="8c5c8-2286">已將 'RoutingPreference' 新增到公用 ip 標籤</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2286">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="8c5c8-2287">改善 'Get-AzNetworkServiceTag' 參考文件的範例</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2287">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8c5c8-2288">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2288">Az.PolicyInsights</span></span>
* <span data-ttu-id="8c5c8-2289">修正 Get-AzPolicyState 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2289">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="8c5c8-2290">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2290">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8c5c8-2291">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2291">Az.OperationalInsights</span></span>
* <span data-ttu-id="8c5c8-2292">修正了 Get-AzOperationalInsightsDataSource 中傳回的 CustomLog 資料來源模型</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2292">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8c5c8-2293">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2293">Az.RecoveryServices</span></span>
* <span data-ttu-id="8c5c8-2294">修正 IaaSVM 的 get-policy 命令</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2294">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="8c5c8-2295">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2295">Az.Resources</span></span>
    - <span data-ttu-id="8c5c8-2296">修正 Get-AzPolicyState -Top 參數的說明文字</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2296">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="8c5c8-2297">新增 Get-AzPolicyAlias 的用戶端分頁支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2297">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="8c5c8-2298">新增 Set-AzPolicyAssignment、-PolicyParameters 和 -PolicyParametersObject 的新參數</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2298">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="8c5c8-2299">原則 Cmdlet 的幾個文件與範例更新</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2299">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8c5c8-2300">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2300">Az.ServiceBus</span></span>
* <span data-ttu-id="8c5c8-2301">修正問題 #4938 - 設定 MaxSizeInMegabytes 時，New-AzureRmServiceBusQueue 傳回 BadRequest</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2301">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="8c5c8-2302">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2302">Az.Sql</span></span>
* <span data-ttu-id="8c5c8-2303">從預覽版本新增執行個體容錯移轉群組 Cmdlet 至公用版本</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2303">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="8c5c8-2304">支援使用新的 Cmdlet 進行 Azure SQL Server\資料庫稽核。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2304">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="8c5c8-2305">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2305">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="8c5c8-2306">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2306">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="8c5c8-2307">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2307">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="8c5c8-2308">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2308">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="8c5c8-2309">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2309">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="8c5c8-2310">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2310">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="8c5c8-2311">從弱點評量設定移除電子郵件條件約束</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2311">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8c5c8-2312">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2312">Az.Storage</span></span>
* <span data-ttu-id="8c5c8-2313">在 Cmdlet 中將 2 個參數 '-IndexDocument' 和 '-ErrorDocument404Path' 從必要變更為選用：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2313">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="8c5c8-2314">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2314">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="8c5c8-2315">藉新增範例更新 Get-AzStorageBlobContent 的說明</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2315">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="8c5c8-2316">當 Cmdlet 失敗並出現 StorageException 時顯示錯誤詳細資訊</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2316">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="8c5c8-2317">支援使用 Azure 檔案 AAD DS 驗證建立或更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2317">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="8c5c8-2318">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2318">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="8c5c8-2319">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2319">Set-AzStorageAccount</span></span>
* <span data-ttu-id="8c5c8-2320">支援清單或關閉檔案共用、檔案目錄或檔案的檔案控制代碼</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2320">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="8c5c8-2321">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2321">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="8c5c8-2322">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2322">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="8c5c8-2323">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2323">Az.StorageSync</span></span>
* <span data-ttu-id="8c5c8-2324">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2324">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="8c5c8-2325">2.3.2 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2325">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8c5c8-2326">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2326">Az.Accounts</span></span>
* <span data-ttu-id="8c5c8-2327">修正函式呼叫時在某些情況下使用了不正確 URL 的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2327">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="8c5c8-2328">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2328">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="8c5c8-2329">修正從 AzureRM 到 Az Cmdlet 的別名問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2329">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="8c5c8-2330">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2330">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="8c5c8-2331">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2331">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8c5c8-2332">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2332">Az.Compute</span></span>
* <span data-ttu-id="8c5c8-2333">New-AzVm and New-AzVmss 簡單參數集合現在接受 'ProximityPlacementGroup' 參數。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2333">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="8c5c8-2334">修正 'New-AzVM' 參考文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2334">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="8c5c8-2335">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2335">Az.Dns</span></span>
* <span data-ttu-id="8c5c8-2336">修正了 'Set-AzDnsZone' 說明範例中的錯字。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2336">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8c5c8-2337">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2337">Az.EventGrid</span></span>
* <span data-ttu-id="8c5c8-2338">已更新為使用 2019-06-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2338">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="8c5c8-2339">新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2339">New cmdlets:</span></span>
    - <span data-ttu-id="8c5c8-2340">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2340">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="8c5c8-2341">建立新的 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2341">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="8c5c8-2342">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2342">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="8c5c8-2343">取得事件方格網域的詳細資料，或取得目前 Azure 訂用帳戶中的所有事件方格網域清單。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2343">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="8c5c8-2344">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2344">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="8c5c8-2345">移除 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2345">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="8c5c8-2346">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2346">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="8c5c8-2347">重新產生 Azure 事件方格網域適用的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2347">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="8c5c8-2348">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2348">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="8c5c8-2349">取得用來; 事件發佈至事件方格網域的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2349">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="8c5c8-2350">New-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2350">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="8c5c8-2351">建立新的 Azure事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2351">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="8c5c8-2352">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2352">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="8c5c8-2353">取得事件方格網域主題的詳細資料，或取得目前 Azure 中特定事件方格網域下的所有事件方格網域主題清單</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2353">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="8c5c8-2354">Remove-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2354">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="8c5c8-2355">移除現有的 Azure 事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2355">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="8c5c8-2356">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2356">Updated cmdlets:</span></span>
    - <span data-ttu-id="8c5c8-2357">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2357">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="8c5c8-2358">新增新的必要參數，以支援新的事件方格網域和事件方格網域主題管線，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2358">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="8c5c8-2359">新增新的必要參數，以指定新的事件方格網域名稱和/或事件方格網域主題名稱，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2359">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="8c5c8-2360">為網域和網域主題新增新的參數集合，以允許重新使用現有的參數 (例如 EndPointType、SubjectBeginsWith 等)。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2360">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="8c5c8-2361">新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2361">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="8c5c8-2362">事件訂用帳戶過期日期，</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2362">Event subscription expiration date,</span></span>
            - <span data-ttu-id="8c5c8-2363">進階篩選參數。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2363">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="8c5c8-2364">為 servicebusqueue 新增新的列舉成為目的地。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2364">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="8c5c8-2365">不允許使用 'All' in -IncludedEventType 選項並取代為</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2365">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="8c5c8-2366">Get-AzEventGridTopic、Get-AzEventGridDomain、Get-AzEventGridDomainTopic、Get-AzEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2366">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="8c5c8-2367">新增新的選用參數 (Top、ODataQuery 和 NextLink) 以支援結果分頁和篩選條件。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2367">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="8c5c8-2368">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2368">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="8c5c8-2369">新增新的必要參數，以支援事件方格網域和事件方格網域主題管線，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2369">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="8c5c8-2370">新增新的必要參數，以指定事件方格網域名稱和/或事件方格網域主題名稱，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2370">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8c5c8-2371">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2371">Az.FrontDoor</span></span>
* <span data-ttu-id="8c5c8-2372">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2372">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="8c5c8-2373">新增轉換支援和新的運算子自動完成值 (RegEx)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2373">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="8c5c8-2374">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2374">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="8c5c8-2375">新增新的自動完成值</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2375">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8c5c8-2376">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2376">Az.Network</span></span>
* <span data-ttu-id="8c5c8-2377">新增對虛擬網路閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2377">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="8c5c8-2378">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2378">New cmdlets</span></span>
        - <span data-ttu-id="8c5c8-2379">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2379">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="8c5c8-2380">新增 AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2380">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="8c5c8-2381">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2381">New cmdlets</span></span>
        - <span data-ttu-id="8c5c8-2382">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2382">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="8c5c8-2383">新增 PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2383">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="8c5c8-2384">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2384">New cmdlets</span></span>
        - <span data-ttu-id="8c5c8-2385">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2385">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="8c5c8-2386">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2386">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="8c5c8-2387">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2387">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="8c5c8-2388">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2388">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="8c5c8-2389">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2389">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="8c5c8-2390">新增 PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2390">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="8c5c8-2391">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2391">New cmdlets</span></span>
        - <span data-ttu-id="8c5c8-2392">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2392">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="8c5c8-2393">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2393">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="8c5c8-2394">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2394">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="8c5c8-2395">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2395">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="8c5c8-2396">已更新下列功能命令：VpnConnection 上的 UseLocalAzureIpAddress 旗標</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2396">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="8c5c8-2397">更新了 New-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2397">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="8c5c8-2398">更新了 Set-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2398">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="8c5c8-2399">在 ExpressRoute 對等互連中新增了唯讀欄位 PeeredConnections。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2399">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="8c5c8-2400">在 ExpressRoute 中新增了唯讀欄位 GlobalReachEnabled。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2400">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="8c5c8-2401">新增了重大變更屬性以取消取代 ExpressRouteCircuit 模型中的 AllowGlobalReach 欄位</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2401">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="8c5c8-2402">修正了使用 TargetListenerID 搭配 AzApplicationGatewayRedirectConfiguration Cmdlet 的問題 8756 錯誤</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2402">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="8c5c8-2403">修正了 New-AzApplicationGatewayPathRuleConfig 中的錯誤，防止進行重寫規則集合設定。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2403">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="8c5c8-2404">修正了在 NetworkInterfaceIpConfiguration 中顯示 VirtualNetworkTaps 的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2404">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="8c5c8-2405">修正了 Cortex Get Cmdlet 以列出所有部分</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2405">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="8c5c8-2406">修正了 ExpressRouteGateways 和 VpnGatewayVirtualHub 的參考建立</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2406">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="8c5c8-2407">新增了 AzureFirewall 和 NatGateway 中對可用性區域的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2407">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="8c5c8-2408">新增了 Cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2408">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="8c5c8-2409">新增針對 Azure 防火牆的多個公用 IP 位址的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2409">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="8c5c8-2410">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2410">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="8c5c8-2411">新增了參數 -PublicIpAddress 以接受一或多個 Public IP Address 物件</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2411">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="8c5c8-2412">新增了參數 -VirtualNetwork 以接受虛擬網路物件</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2412">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="8c5c8-2413">在防火牆物件中新增了 AddPublicIpAddress 和 RemovePublicIpAddress 方法 - 以接受 Public IP Address 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2413">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="8c5c8-2414">參數 -PublicIpName 和 -VirtualNetworkName 已被取代</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2414">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="8c5c8-2415">已更新下列功能命令：將 VpnClient AAD 驗證選項設為虛擬網路閘道資源。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2415">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="8c5c8-2416">已更新 New-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2416">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="8c5c8-2417">已更新 Set-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2417">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="8c5c8-2418">已更新 Set-AzVirtualNetworkGateway：新增了選用的切換參數 RemoveAadAuthentication 以從閘道移除 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2418">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8c5c8-2419">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2419">Az.OperationalInsights</span></span>
* <span data-ttu-id="8c5c8-2420">在 'New-AzureRmOperationalInsightsWorkspace' 命令中啟用 **pergb2018** 定價層</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2420">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="8c5c8-2421">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2421">Az.Resources</span></span>
* <span data-ttu-id="8c5c8-2422">支援其他範本匯出選項</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2422">Support for additional Template Export options</span></span>
    - <span data-ttu-id="8c5c8-2423">將 '-SkipResourceNameParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2423">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="8c5c8-2424">將 '-SkipAllParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2424">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="8c5c8-2425">將 '-Resource' parameter 新增到 Export-AzResourceGroup 以篩選已匯出的資源</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2425">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8c5c8-2426">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2426">Az.ServiceFabric</span></span>
* <span data-ttu-id="8c5c8-2427">修正在某些情況下，新增 ByExistingKeyVault 憑證會產生錯誤指紋的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2427">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="8c5c8-2428">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2428">Az.Sql</span></span>
* <span data-ttu-id="8c5c8-2429">修正進階威脅防護儲存體端點尾碼</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2429">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="8c5c8-2430">修正進階威脅防護啟用覆寫進階威脅防護原則</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2430">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="8c5c8-2431">為 Management.Sql 新增 Cmdlet 以允許客戶為受控執行個體新增 TDE 金鑰並設定 TDE 保護程式</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2431">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="8c5c8-2432">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2432">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="8c5c8-2433">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2433">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="8c5c8-2434">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2434">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="8c5c8-2435">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2435">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="8c5c8-2436">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2436">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8c5c8-2437">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2437">Az.Storage</span></span>
* <span data-ttu-id="8c5c8-2438">在建立儲體帳戶時支援 Kind FileStorage 和 SkuName Premium_ZRS</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2438">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="8c5c8-2439">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2439">New-AzStorageAccount</span></span>
* <span data-ttu-id="8c5c8-2440">釐清了 Blob 不變性 Cmdlet 的說明</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2440">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="8c5c8-2441">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2441">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8c5c8-2442">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2442">Az.Websites</span></span>
* <span data-ttu-id="8c5c8-2443">將 Get-AzWebAppCertificate 最佳化，以便依伺服器而非用戶端上的資源群組篩選</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2443">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="8c5c8-2444">將 -UseDisasterRecovery 切換參數新增到 Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2444">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="8c5c8-2445">2.2.0 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2445">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="8c5c8-2446">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2446">Az.Cdn</span></span>
* <span data-ttu-id="8c5c8-2447">已更新 Cmdlet，可支援以 API 2019-04-15 版為基礎的 rulesEngine 功能。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2447">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8c5c8-2448">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2448">Az.Compute</span></span>
* <span data-ttu-id="8c5c8-2449">已新增 `NoWait` 參數，會啟動作業並在作業完成之前立即傳回結果。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2449">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="8c5c8-2450">已更新的 Cmdlet： Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2450">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8c5c8-2451">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2451">Az.EventHub</span></span>
* <span data-ttu-id="8c5c8-2452">修正 #9231 - Get-AzEventHubNamespace 不會傳回標記</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2452">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="8c5c8-2453">修正 #9230 - Get-AzEventHubNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2453">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8c5c8-2454">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2454">Az.Network</span></span>
* <span data-ttu-id="8c5c8-2455">更新 Nat 閘道的 ResourceId 和 InputObject</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2455">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="8c5c8-2456">新增 ResourceId 和 InputObject 的別名</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2456">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8c5c8-2457">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2457">Az.PolicyInsights</span></span>
* <span data-ttu-id="8c5c8-2458">修正 Get-AzPolicyEvent 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2458">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8c5c8-2459">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2459">Az.RecoveryServices</span></span>
* <span data-ttu-id="8c5c8-2460">IaaSVM 原則的最小保留天數從 1 天變更為 7 天</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2460">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8c5c8-2461">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2461">Az.ServiceBus</span></span>
* <span data-ttu-id="8c5c8-2462">修正 issue #9182 - Get-AzServiceBusNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2462">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8c5c8-2463">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2463">Az.ServiceFabric</span></span>
* <span data-ttu-id="8c5c8-2464">修正 'Update-AzServiceFabricReliability' 錯誤訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2464">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="8c5c8-2465">修正 Service Fabric 命令列中的遺漏字元</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2465">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="8c5c8-2466">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2466">Az.Sql</span></span>
* <span data-ttu-id="8c5c8-2467">為 New-AzureSqlInstance Cmdlet 新增 DnsZonePartner 參數，以支援受控執行個體的 AutoDr。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2467">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="8c5c8-2468">即將淘汰 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2468">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="8c5c8-2469">將威脅偵測 Cmdlet 重新命名為進階威脅防護</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2469">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="8c5c8-2470">New-AzSqlInstance -StorageSizeInGB 和 -LicenseType 現在是選擇性的參數。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2470">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8c5c8-2471">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2471">Az.Websites</span></span>
* <span data-ttu-id="8c5c8-2472">修正 Set-AzWebApp 和 Set-AzWebAppSlot 搭配使用 -WebApp 屬性時會移除標記的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2472">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="8c5c8-2473">2.1.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2473">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="8c5c8-2474">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2474">Az.ApiManagement</span></span>
* <span data-ttu-id="8c5c8-2475">已建立新的 Cmdlet，用以管理全域和 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2475">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="8c5c8-2476">**Get-AzApiManagementDiagnostic** - 取得設定於全域或 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2476">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="8c5c8-2477">**New-AzApiManagementDiagnostic** - 在全域範圍或 API 範圍建立新的診斷</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2477">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="8c5c8-2478">**New-AzApiManagementHttpMessageDiagnostic** - 建立關於要記錄哪些標頭和本文位元組大小的診斷設定</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2478">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="8c5c8-2479">**New-AzApiManagementPipelineDiagnosticSetting** - 建立閘道的傳入/傳出 HTTP 訊息的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2479">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="8c5c8-2480">**New-AzApiManagementSamplingSetting** - 建立診斷要求/回應的取樣設定</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2480">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="8c5c8-2481">**Remove-AzApiManagementDiagnostic** - 移除全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2481">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="8c5c8-2482">**Set-AzApiManagementDiagnostic** - 更新全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2482">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="8c5c8-2483">已建立新的 Cmdlet 用以管理 ApiManagement 服務中的快取</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2483">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="8c5c8-2484">**Get-AzApiManagementCache** - 取得識別碼所指定的快取或所有快取的詳細資料</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2484">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="8c5c8-2485">**New-AzApiManagementCache** - 建立新的「預設」快取或特定 Azure「區域」中的快取</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2485">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="8c5c8-2486">**Remove-AzApiManagementCache** - 移除快取</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2486">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="8c5c8-2487">**Update-AzApiManagementCache** - 更新快取</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2487">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="8c5c8-2488">已建立新的 Cmdlet 用以管理 API 結構描述</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2488">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="8c5c8-2489">**New-AzApiManagementSchema** - 為 API 建立新的結構描述</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2489">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="8c5c8-2490">**Get-AzApiManagementSchema** - 取得在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2490">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="8c5c8-2491">**Remove-AzApiManagementSchema** - 移除在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2491">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="8c5c8-2492">**Set-AzApiManagementSchema** - 更新在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2492">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="8c5c8-2493">已建立新的 Cmdlet 用以產生使用者權杖。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2493">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="8c5c8-2494">**New-AzApiManagementUserToken** - 產生預設有效期為 8 小時的新使用者權杖。'GIT' 使用者的權杖可使用此 Cmdlet 產生。/</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2494">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="8c5c8-2495">已建立新的 Cmdlet 用以擷取網路狀態</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2495">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="8c5c8-2496">**Get-AzApiManagementNetworkStatus** - 取得 API 管理服務相依資源的網路狀態連線。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2496">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="8c5c8-2497">這在將 ApiManagement 服務部署到虛擬網路和驗證是否有任何相依性中斷時，將可發揮效用。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2497">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="8c5c8-2498">已更新 Cmdlet **New-AzApiManagement**，用以管理 ApiManagement 服務</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2498">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="8c5c8-2499">已加入新的「使用量」SKU 的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2499">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="8c5c8-2500">已加入為「使用量」SKU 開啟 'EnableClientCertificate' 旗標的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2500">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="8c5c8-2501">新的 Cmdlet **New-AzApiManagementSslSetting** 允許在「後端」和「前端」設定 'TLS/SSL' 設定。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2501">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="8c5c8-2502">這也可用來在 ApiManagement 服務的「前端」設定「編碼器」 (例如 '3DES') 和 'ServerProtocols' (例如 'Http2')。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2502">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="8c5c8-2503">已加入在 ApiManagement 服務上設定 'DeveloperPortal' 主機名稱的支援。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2503">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="8c5c8-2504">已更新 Cmdlet **Get-AzApiManagementSsoToken**，以使用 'PsApiManagement' 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2504">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="8c5c8-2505">已更新 Cmdlet 以顯示內嵌錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2505">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="8c5c8-2506">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy :錯誤碼：ValidationError 錯誤訊息：有一或多個欄位包含不正確的值：錯誤詳細資料：[Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10:Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2506">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="8c5c8-2507">已更新 Cmdlet **Export-AzApiManagementApi**，以採用 'OpenApi 3.0' 格式匯出 API</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2507">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="8c5c8-2508">已更新 Cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2508">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="8c5c8-2509">以從 'OpenApi 3.0' 文件規格匯入 API</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2509">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="8c5c8-2510">以覆寫任何 ('Swagger'、'Wadl'、'Wsdl'、'OpenApi') 文件中指定的 'PsApiManagementSchema' 屬性。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2510">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="8c5c8-2511">以覆寫任何文件中指定的 'ServiceUrl' 屬性。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2511">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="8c5c8-2512">已更新 Cmdlet **Get-AzApiManagementPolicy**，以透過使用 'rawxml' 的非 XML 逸出「格式」傳回原則</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2512">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="8c5c8-2513">已更新 Cmdlet **Set-AzApiManagementPolicy**，以接受使用 'rawxml' 的非 XML 逸出「格式」和使用 'xml' 溢出的 XML 格式的原則</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2513">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="8c5c8-2514">已更新 Cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2514">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="8c5c8-2515">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2515">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="8c5c8-2516">以在 'ApiVersionSet' 中建立 API</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2516">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="8c5c8-2517">以使用 'SourceApiId' 和 'SourceApiRevision' 複製 API。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2517">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="8c5c8-2518">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2518">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="8c5c8-2519">已更新 Cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2519">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="8c5c8-2520">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2520">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="8c5c8-2521">以在 'ApiVersionSet' 中更新 API</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2521">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="8c5c8-2522">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2522">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="8c5c8-2523">已更新 Cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2523">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="8c5c8-2524">以使用 'SourceApiRevision' 複製 (複製標記、產品、作業和原則) 現有的修訂。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2524">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="8c5c8-2525">新的修訂會採用父代的 'ApiId'。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2525">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="8c5c8-2526">以提供 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2526">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="8c5c8-2527">以在複製 API 時覆寫 'ServiceUrl'。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2527">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="8c5c8-2528">已更新 Cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2528">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="8c5c8-2529">以透過 'Authority' 設定 'AAD' 或 'AADB2C'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2529">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="8c5c8-2530">以設定 'SignupPolicy'、'SigninPolicy'、'ProfileEditingPolicy' 和 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2530">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="8c5c8-2531">已更新 Cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2531">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="8c5c8-2532">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2532">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="8c5c8-2533">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2533">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="8c5c8-2534">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2534">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="8c5c8-2535">已更新 Cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2535">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="8c5c8-2536">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2536">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="8c5c8-2537">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2537">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="8c5c8-2538">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2538">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="8c5c8-2539">已更新下列 Cmdlet，以接受 'ResourceId' 作為輸入</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2539">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="8c5c8-2540">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2540">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="8c5c8-2541">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2541">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="8c5c8-2542">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2542">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="8c5c8-2543">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2543">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="8c5c8-2544">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2544">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="8c5c8-2545">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2545">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="8c5c8-2546">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2546">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="8c5c8-2547">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2547">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="8c5c8-2548">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2548">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="8c5c8-2549">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2549">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="8c5c8-2550">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2550">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="8c5c8-2551">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2551">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8c5c8-2552">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2552">Az.Automation</span></span>
* <span data-ttu-id="8c5c8-2553">已更新 Get-AzAutomationJobOutputRecord 以處理 JSON 和文字記錄值。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2553">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="8c5c8-2554">修正 https://github.com/Azure/azure-powershell/issues/7977 的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2554">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="8c5c8-2555">修正 https://github.com/Azure/azure-powershell/issues/8600 的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2555">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="8c5c8-2556">已將 Start-AzAutomationDscCompilationJob 的行為變更為僅啟動作業而不等候作業完成。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2556">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="8c5c8-2557">修正 https://github.com/Azure/azure-powershell/issues/8347 的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2557">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="8c5c8-2558">修正 Get-AzAutomationDscNode 在使用 -Name 時會傳回所有節點的問題。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2558">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="8c5c8-2559">現在它只會相符的節點。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2559">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8c5c8-2560">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2560">Az.Compute</span></span>
* <span data-ttu-id="8c5c8-2561">將 ProtectFromScaleIn 和 ProtectFromScaleSetAction 參數新增至 Update-AzVmssVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2561">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="8c5c8-2562">在不支援「美國東部」時，New-AzVM wimple 參數現在依預設會使用可用的位置</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2562">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8c5c8-2563">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2563">Az.DataLakeStore</span></span>
* <span data-ttu-id="8c5c8-2564">更新 ADLS SDK 以使用 httpclient，並透過 Azure 架構整合資料平面測試</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2564">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8c5c8-2565">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2565">Az.Monitor</span></span>
* <span data-ttu-id="8c5c8-2566">已修正說明範例中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2566">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8c5c8-2567">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2567">Az.Network</span></span>
* <span data-ttu-id="8c5c8-2568">將 DisableBgpRoutePropagation 旗標新增至有效路由表輸出</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2568">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="8c5c8-2569">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2569">Updated cmdlet:</span></span>
        - <span data-ttu-id="8c5c8-2570">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2570">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="8c5c8-2571">修正 New-AzApplicationGatewayTrustedRootCertificate 文件中的雙破折號</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2571">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="8c5c8-2572">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2572">Az.Resources</span></span>
* <span data-ttu-id="8c5c8-2573">新增 Cmdlet Get-AzureRmDenyAssignment 用以擷取拒絕指派</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2573">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="8c5c8-2574">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2574">Az.Sql</span></span>
* <span data-ttu-id="8c5c8-2575">將進階威脅防護 Cmdlet 重新命名為進階資料安全性的，並依預設啟用弱點評量</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2575">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="8c5c8-2576">2.0.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2576">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8c5c8-2577">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2577">Az.Accounts</span></span>
* <span data-ttu-id="8c5c8-2578">更新驗證程式庫以修正 ADFS 的使用者名稱/密碼驗證問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2578">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8c5c8-2579">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2579">Az.CognitiveServices</span></span>
* <span data-ttu-id="8c5c8-2580">只顯示 Bing 搜尋服務的 Bing 免責聲明。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2580">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="8c5c8-2581">改善建立帳戶失敗時的錯誤。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2581">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8c5c8-2582">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2582">Az.Compute</span></span>
* <span data-ttu-id="8c5c8-2583">鄰近放置群組功能。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2583">Proximity placement group feature.</span></span>
    - <span data-ttu-id="8c5c8-2584">新增下列 Cmdlet： New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2584">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="8c5c8-2585">將新參數 ProximityPlacementGroupId 新增至下列 Cmdlet： New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2585">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="8c5c8-2586">將 StorageAccountType 參數新增至 New-AzGalleryImageVersion。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2586">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="8c5c8-2587">New-AzGalleryImageVersion 的 TargetRegion 可包含 StorageAccountType。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2587">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="8c5c8-2588">將 SkipShutdown 切換參數新增至 Stop-AzVM 和 Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2588">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="8c5c8-2589">重大變更</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2589">Breaking changes</span></span>
    - <span data-ttu-id="8c5c8-2590">將 Set-AzVMBootDiagnostics 變更為 Set-AzVMBootDiagnostic。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2590">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="8c5c8-2591">將 Export-AzLogAnalyticThrottledRequests 變更為 Export-AzLogAnalyticThrottledRequests。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2591">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="8c5c8-2592">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2592">Az.DeploymentManager</span></span>
* <span data-ttu-id="8c5c8-2593">第一版正式運作的 Azure 部署管理員 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2593">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="8c5c8-2594">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2594">Az.Dns</span></span>
* <span data-ttu-id="8c5c8-2595">自動的 DNS NameServer 委派</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2595">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="8c5c8-2596">建立 DNS 區域 Cmdlet 可接受父代區域名稱作為其他選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2596">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="8c5c8-2597">針對新建立的子系區域，在父代區域中新增 NS 記錄。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2597">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8c5c8-2598">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2598">Az.FrontDoor</span></span>
* <span data-ttu-id="8c5c8-2599">第一版正式運作的 Azure FrontDoor Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2599">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="8c5c8-2600">重新命名 WAF Cmdlet 以包含 'Waf'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2600">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="8c5c8-2601">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2601">Az.HDInsight</span></span>
* <span data-ttu-id="8c5c8-2602">移除兩個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2602">Removed two cmdlets:</span></span>
    - <span data-ttu-id="8c5c8-2603">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2603">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="8c5c8-2604">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2604">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="8c5c8-2605">已新增 Set-AzHDInsightGatewayCredential Cmdlet 來取代 Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2605">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="8c5c8-2606">更新 Get-AzHDInsightJobOutput Cmdlet 以區分讀者角色和 HDInsight 操作員角色：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2606">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="8c5c8-2607">具有讀者角色的使用者必須明確指定 'DefaultStorageAccountKey' 參數，否則會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2607">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="8c5c8-2608">具有 HDInsight 操作員角色的使用者不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2608">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8c5c8-2609">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2609">Az.Monitor</span></span>
* <span data-ttu-id="8c5c8-2610">SQR API 的新 Cmdlet (已排程的查詢規則)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2610">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="8c5c8-2611">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2611">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="8c5c8-2612">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2612">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="8c5c8-2613">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2613">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="8c5c8-2614">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2614">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="8c5c8-2615">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2615">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="8c5c8-2616">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2616">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="8c5c8-2617">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2617">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8c5c8-2618">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2618">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8c5c8-2619">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2619">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8c5c8-2620">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2620">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8c5c8-2621">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2621">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8c5c8-2622">[更多](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) SQR API 的相關資訊</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2622">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="8c5c8-2623">更新 Az.Monitor.md，以包含用於 GenV2 (非傳統) 計量式警示規則的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2623">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8c5c8-2624">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2624">Az.Network</span></span>
* <span data-ttu-id="8c5c8-2625">新增 Nat 閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2625">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="8c5c8-2626">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2626">New cmdlets</span></span>
        - <span data-ttu-id="8c5c8-2627">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2627">New-AzNatGateway</span></span>
        - <span data-ttu-id="8c5c8-2628">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2628">Get-AzNatGateway</span></span>
        - <span data-ttu-id="8c5c8-2629">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2629">Set-AzNatGateway</span></span>
        - <span data-ttu-id="8c5c8-2630">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2630">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="8c5c8-2631">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2631">Updated cmdlets</span></span>
        - <span data-ttu-id="8c5c8-2632">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2632">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="8c5c8-2633">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2633">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="8c5c8-2634">已更新下列功能命令：設定/移除 Brooklyn 閘道上的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2634">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="8c5c8-2635">已更新 New-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2635">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="8c5c8-2636">已更新 Set-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2636">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8c5c8-2637">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2637">Az.PolicyInsights</span></span>
* <span data-ttu-id="8c5c8-2638">支援查詢原則的評估詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2638">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="8c5c8-2639">將 '-Expand' 參數新增至 Get-AzPolicyState。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2639">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="8c5c8-2640">支援 '-Expand PolicyEvaluationDetails'。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2640">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8c5c8-2641">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2641">Az.RecoveryServices</span></span>
* <span data-ttu-id="8c5c8-2642">支援跨訂用帳戶的 Azure 到 Azure 站台復原。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2642">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="8c5c8-2643">標示 Azure Site Recovery 上即將進行的重大變更。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2643">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="8c5c8-2644">Azure Site Recovery 復原計劃和行動計劃的修正。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2644">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="8c5c8-2645">Azure 到 Azure 的 Azure Site Recovery 更新網路對應修正。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2645">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="8c5c8-2646">受控磁碟中 Azure 到 Azure 的 Azure Site Recovery 更新保護方向修正。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2646">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="8c5c8-2647">其他小幅修正。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2647">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="8c5c8-2648">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2648">Az.Relay</span></span>
* <span data-ttu-id="8c5c8-2649">修正客戶訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2649">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8c5c8-2650">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2650">Az.ServiceBus</span></span>
* <span data-ttu-id="8c5c8-2651">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2651">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8c5c8-2652">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2652">Az.Storage</span></span>
* <span data-ttu-id="8c5c8-2653">升級至儲存體用戶端程式庫 10.0.1 (此 SDK 中所有物件的命名空間會從 'Microsoft.WindowsAzure.Storage. *' 變更為 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2653">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="8c5c8-2654">升級至 Microsoft.Azure.Management.Storage 11.0.0，以支援新的 API 版本 2019-04-01。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2654">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="8c5c8-2655">建立儲存體帳戶中的預設儲存體帳戶類型從 'Storage' 變更為 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2655">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="8c5c8-2656">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2656">New-AzStorageAccount</span></span>
* <span data-ttu-id="8c5c8-2657">藉由加入 '-'，將儲存體帳戶 Cmdlet 輸出 Sku.Name 變成和輸入 SkuName 一致，例如將 'StandardLRS' 變更為 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2657">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="8c5c8-2658">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2658">New-AzStorageAccount</span></span>
    - <span data-ttu-id="8c5c8-2659">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2659">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="8c5c8-2660">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2660">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8c5c8-2661">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2661">Az.Websites</span></span>
* <span data-ttu-id="8c5c8-2662">Get-AzWebApp 傳回的 PSSite 物件現在會設定 'Kind' 屬性</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2662">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="8c5c8-2663">Get-AzWebApp\*Metrics 和 Get-AzAppServicePlanMetrics 已標示為淘汰</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2663">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="8c5c8-2664">1.8.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2664">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8c5c8-2665">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2665">Highlights since the last major release</span></span>
* <span data-ttu-id="8c5c8-2666">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2666">General availability of `Az` module</span></span>
* <span data-ttu-id="8c5c8-2667">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2667">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="8c5c8-2668">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2668">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="8c5c8-2669">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2669">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="8c5c8-2670">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2670">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8c5c8-2671">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2671">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="8c5c8-2672">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2672">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8c5c8-2673">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2673">Az.Accounts</span></span>
* <span data-ttu-id="8c5c8-2674">更新 Uninstall-AzureRm 以在 Mac 中正確刪除模組</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2674">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="8c5c8-2675">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2675">Az.Batch</span></span>
* <span data-ttu-id="8c5c8-2676">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2676">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8c5c8-2677">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2677">Az.Cdn</span></span>
* <span data-ttu-id="8c5c8-2678">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2678">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8c5c8-2679">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2679">Az.CognitiveServices</span></span>
* <span data-ttu-id="8c5c8-2680">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2680">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8c5c8-2681">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2681">Az.Compute</span></span>
* <span data-ttu-id="8c5c8-2682">如果磁碟的資源識別碼中有小寫資源群組，則修正 AEM 安裝問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2682">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="8c5c8-2683">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2683">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8c5c8-2684">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2684">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8c5c8-2685">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2685">Az.DataFactory</span></span>
* <span data-ttu-id="8c5c8-2686">如果受控整合執行階段的 NodeCount 不是 Null，則新增 SsisProperties。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2686">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8c5c8-2687">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2687">Az.DataLakeStore</span></span>
* <span data-ttu-id="8c5c8-2688">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2688">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8c5c8-2689">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2689">Az.EventGrid</span></span>
* <span data-ttu-id="8c5c8-2690">已更新端點的說明文字，指出應該先建立資源，才能使用建立/更新事件訂用帳戶 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2690">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8c5c8-2691">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2691">Az.EventHub</span></span>
* <span data-ttu-id="8c5c8-2692">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2692">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8c5c8-2693">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2693">Az.HDInsight</span></span>
* <span data-ttu-id="8c5c8-2694">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2694">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8c5c8-2695">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2695">Az.IotHub</span></span>
* <span data-ttu-id="8c5c8-2696">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2696">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8c5c8-2697">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2697">Az.KeyVault</span></span>
* <span data-ttu-id="8c5c8-2698">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2698">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8c5c8-2699">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2699">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="8c5c8-2700">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2700">Az.MachineLearning</span></span>
* <span data-ttu-id="8c5c8-2701">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2701">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="8c5c8-2702">Az.Media</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2702">Az.Media</span></span>
* <span data-ttu-id="8c5c8-2703">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2703">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8c5c8-2704">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2704">Az.Monitor</span></span>
  * <span data-ttu-id="8c5c8-2705">適用於 GenV2 (非傳統) 計量型警示規則的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2705">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="8c5c8-2706">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2706">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="8c5c8-2707">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2707">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="8c5c8-2708">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2708">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="8c5c8-2709">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2709">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="8c5c8-2710">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2710">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="8c5c8-2711">監視器 SDK 已更新為版本 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2711">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8c5c8-2712">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2712">Az.Network</span></span>
* <span data-ttu-id="8c5c8-2713">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2713">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8c5c8-2714">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2714">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="8c5c8-2715">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2715">Az.NotificationHubs</span></span>
* <span data-ttu-id="8c5c8-2716">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2716">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8c5c8-2717">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2717">Az.OperationalInsights</span></span>
* <span data-ttu-id="8c5c8-2718">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2718">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="8c5c8-2719">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2719">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="8c5c8-2720">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2720">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8c5c8-2721">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2721">Az.RecoveryServices</span></span>
* <span data-ttu-id="8c5c8-2722">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2722">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8c5c8-2723">已更新 Azure VM 中 SQL 的資料表格式</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2723">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="8c5c8-2724">已新增替代方法來擷取 AzureFileShare 中的位置</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2724">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="8c5c8-2725">已根據時區更新 SchedulePolicy 物件中的 ScheduleRunDays</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2725">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="8c5c8-2726">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2726">Az.RedisCache</span></span>
* <span data-ttu-id="8c5c8-2727">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2727">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8c5c8-2728">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2728">Az.Resources</span></span>
* <span data-ttu-id="8c5c8-2729">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2729">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="8c5c8-2730">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2730">Az.Sql</span></span>
* <span data-ttu-id="8c5c8-2731">以通用程式碼取代監視器 SDK 的相依性</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2731">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="8c5c8-2732">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2732">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8c5c8-2733">已增強多個資料行分類的程序。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2733">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="8c5c8-2734">在來自 Get-AzSqlServerServiceObjective 的回應中包含 sku 屬性 (sku 名稱、系列、容量)，並依預設格式化為資料表。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2734">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="8c5c8-2735">依位置 Get-AzSqlServerServiceObjective 的能力，而區域中不需要預先存在的伺服器。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2735">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="8c5c8-2736">在受控執行個體中支援建立時區參數。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2736">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="8c5c8-2737">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2737">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8c5c8-2738">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2738">Az.Websites</span></span>
* <span data-ttu-id="8c5c8-2739">將 Set-AzWebApp 和 Set-AzWebAppSlot 修正為不在執行時移除標記</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2739">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="8c5c8-2740">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2740">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8c5c8-2741">已更新網站 SDK。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2741">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="8c5c8-2742">已從 PSAppServicePlan 中移除 AdminSiteName 屬性。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2742">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="8c5c8-2743">1.7.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2743">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8c5c8-2744">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2744">Highlights since the last major release</span></span>
* <span data-ttu-id="8c5c8-2745">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2745">General availability of `Az` module</span></span>
* <span data-ttu-id="8c5c8-2746">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2746">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="8c5c8-2747">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2747">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="8c5c8-2748">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2748">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="8c5c8-2749">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2749">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8c5c8-2750">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2750">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="8c5c8-2751">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2751">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8c5c8-2752">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2752">Az.Accounts</span></span>
* <span data-ttu-id="8c5c8-2753">已將 Add-AzEnvironment 和 Set-AzEnvironment 更新為接受 AzureAnalysisServicesEndpointResourceId 參數</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2753">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="8c5c8-2754">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2754">Az.AnalysisServices</span></span>
* <span data-ttu-id="8c5c8-2755">在 dataplane Cmdlet 中使用 ServiceClient，並移除原始的驗證邏輯</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2755">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="8c5c8-2756">讓 Add-AzureASAccount 成為 Connect-AzAccount 的包裝函式，以避免重大變更</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2756">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8c5c8-2757">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2757">Az.Automation</span></span>
* <span data-ttu-id="8c5c8-2758">修正 Inclusions 的 New-AzAutomationSoftwareUpdateConfiguration Cmdlet 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2758">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="8c5c8-2759">現在，IncludedKbNumber 和 IncludedPackageNameMask 參數應會正常運作。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2759">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="8c5c8-2760">修正 Azure 自動化更新管理動態群組的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2760">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8c5c8-2761">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2761">Az.Compute</span></span>
* <span data-ttu-id="8c5c8-2762">將 HyperVGeneration 參數新增至 New-AzDiskConfig 和 New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2762">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="8c5c8-2763">允許使用其他租用戶的資源庫映像來建立 VM。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2763">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="8c5c8-2764">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2764">Az.ContainerInstance</span></span>
* <span data-ttu-id="8c5c8-2765">已修正 New-AzContainerGroup 的 -Command 參數問題，其加入了尾端空白的引數</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2765">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8c5c8-2766">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2766">Az.DataFactory</span></span>
* <span data-ttu-id="8c5c8-2767">已將 ADF .Net SDK 版本更新為 3.0.2</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2767">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="8c5c8-2768">已透過 RepoConfiguration 相關設定的額外參數來更新 Set-AzDataFactoryV2 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2768">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8c5c8-2769">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2769">Az.Resources</span></span>
* <span data-ttu-id="8c5c8-2770">改善提供 '-ResourceId' 或 '-ResourceGroupName'、'-Name' 和 '-ResourceType' 參數時，'Get-AzResource' 的提供者處理</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2770">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="8c5c8-2771">改善 'Test-AzDeployment' 和 'Test-AzResourceGroupDeployment' 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2771">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="8c5c8-2772">處理部署驗證外擲回的錯誤，並改為將其包含在命令輸出中</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2772">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="8c5c8-2773">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2773">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="8c5c8-2774">將 '-IgnoreDynamicParameters' 切換參數新增至部署 Cmdlet 的集合，以略過指令碼和作業案例中的提示</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2774">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="8c5c8-2775">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2775">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="8c5c8-2776">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2776">Az.Sql</span></span>
* <span data-ttu-id="8c5c8-2777">支援資料庫的資料分類。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2777">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8c5c8-2778">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2778">Az.Storage</span></span>
* <span data-ttu-id="8c5c8-2779">報告以參數 -UseConnectedAccount 建立儲存體內容時的詳細錯誤 (未登入 Azure 帳戶)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2779">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="8c5c8-2780">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2780">New-AzStorageContext</span></span>
* <span data-ttu-id="8c5c8-2781">支援以管理平面 API 管理指定儲存體帳戶的 Blob 服務屬性</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2781">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="8c5c8-2782">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2782">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="8c5c8-2783">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2783">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="8c5c8-2784">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2784">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="8c5c8-2785">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2785">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="8c5c8-2786">Blob 的 -AsJob 支援和檔案上傳及下載 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2786">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="8c5c8-2787">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2787">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="8c5c8-2788">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2788">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="8c5c8-2789">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2789">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="8c5c8-2790">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2790">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="8c5c8-2791">1.6.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2791">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8c5c8-2792">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2792">Highlights since the last major release</span></span>
* <span data-ttu-id="8c5c8-2793">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2793">General availability of `Az` module</span></span>
* <span data-ttu-id="8c5c8-2794">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2794">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="8c5c8-2795">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2795">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="8c5c8-2796">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2796">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="8c5c8-2797">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2797">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8c5c8-2798">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2798">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="8c5c8-2799">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2799">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8c5c8-2800">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2800">Az.Automation</span></span>
* <span data-ttu-id="8c5c8-2801">Azure 自動化更新管理變更為支援下列各項新功能：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2801">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="8c5c8-2802">動態分組</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2802">Dynamic grouping</span></span>
    * <span data-ttu-id="8c5c8-2803">預先貼文指令碼</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2803">Pre-Post script</span></span>
    * <span data-ttu-id="8c5c8-2804">重新啟動設定</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2804">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8c5c8-2805">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2805">Az.Compute</span></span>
* <span data-ttu-id="8c5c8-2806">修正 Get-AzVmBootDiagnosticsData 中路徑解析的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2806">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="8c5c8-2807">將計算用戶端程式庫更新為 25.0.0。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2807">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8c5c8-2808">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2808">Az.KeyVault</span></span>
* <span data-ttu-id="8c5c8-2809">新增了 KeyVault Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2809">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8c5c8-2810">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2810">Az.Network</span></span>
* <span data-ttu-id="8c5c8-2811">新增適用於 Azure 防火牆的威脅智慧支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2811">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="8c5c8-2812">新增應用程式閘道防火牆原則頂層資源和自訂規則</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2812">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8c5c8-2813">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2813">Az.RecoveryServices</span></span>
* <span data-ttu-id="8c5c8-2814">已在 Azure VM 原則中新增了 SnapshotRetentionInDays 以支援 Instant RP</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2814">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="8c5c8-2815">新增了取消註冊容器的管道支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2815">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="8c5c8-2816">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2816">Az.Resources</span></span>
* <span data-ttu-id="8c5c8-2817">更新適用於 Get-AzResource 和 Get-AzResourceGroup 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2817">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="8c5c8-2818">更新在對 ARM 進行一般呼叫時使用的認證</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2818">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="8c5c8-2819">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2819">Az.Sql</span></span>
* <span data-ttu-id="8c5c8-2820">變更了 DetectionType 到 string[] 的威脅偵測 Cmdlet 參數，以便在新增了 DetectionTypes 時具備更進一步的保障，同時支援自動完成功能。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2820">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8c5c8-2821">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2821">Az.Storage</span></span>
* <span data-ttu-id="8c5c8-2822">支援儲存體帳戶上的 Get/Set/Remove 管理原則</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2822">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="8c5c8-2823">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2823">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="8c5c8-2824">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2824">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="8c5c8-2825">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2825">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="8c5c8-2826">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2826">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="8c5c8-2827">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2827">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="8c5c8-2828">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2828">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8c5c8-2829">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2829">Az.Websites</span></span>
* <span data-ttu-id="8c5c8-2830">修正 ARM 範本錯誤 (bug)，防正使用 'New-AzWebApp -IncludeSourceWebAppSlots' 時發生中斷複製所有位置的情況</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2830">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="8c5c8-2831">1.5.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2831">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8c5c8-2832">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2832">Az.Accounts</span></span>
* <span data-ttu-id="8c5c8-2833">新增 'Register-AzModule' 命令以支援 AutoRest 產生的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2833">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="8c5c8-2834">適用於 Connect-AzAccount 的更新範例</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2834">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8c5c8-2835">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2835">Az.Automation</span></span>
* <span data-ttu-id="8c5c8-2836">修正了在數個 Azure 自動化 Cmdlet 中擷取某些每月排程時發生的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2836">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="8c5c8-2837">修正 Get-AzAutomationDscNode 只會傳回前 20 個節點的問題。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2837">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="8c5c8-2838">現在可以傳回所有節點</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2838">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8c5c8-2839">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2839">Az.Cdn</span></span>
* <span data-ttu-id="8c5c8-2840">新增了 Enable/Disable Custom Domain Https 的 Powershell Cmdlet 並取代了舊的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2840">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8c5c8-2841">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2841">Az.Compute</span></span>
* <span data-ttu-id="8c5c8-2842">新增 Get Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2842">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8c5c8-2843">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2843">Az.DataFactory</span></span>
* <span data-ttu-id="8c5c8-2844">已將 ADF .Net SDK 版本更新為 3.0.1</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2844">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8c5c8-2845">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2845">Az.LogicApp</span></span>
* <span data-ttu-id="8c5c8-2846">修正 ListWorkflows，僅擷取結果的第一頁資料</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2846">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8c5c8-2847">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2847">Az.Network</span></span>
* <span data-ttu-id="8c5c8-2848">新增 Network Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2848">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8c5c8-2849">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2849">Az.RecoveryServices</span></span>
* <span data-ttu-id="8c5c8-2850">新增了Azure VM 中 SQL 伺服器的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2850">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="8c5c8-2851">SDK 更新</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2851">SDK Update</span></span>
* <span data-ttu-id="8c5c8-2852">移除了 Get-ProtectableItem 中的 VMappContainer 檢查</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2852">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="8c5c8-2853">新增了 Get-ProtectableItem 的 Name 和 ServerName 參數</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2853">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="8c5c8-2854">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2854">Az.Resources</span></span>
* <span data-ttu-id="8c5c8-2855">將 `-TemplateObject` 參數新增至部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2855">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="8c5c8-2856">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2856">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="8c5c8-2857">修正將 `Get-AzResource` 結果輸送至 `Set-AzResource` 的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2857">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="8c5c8-2858">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2858">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="8c5c8-2859">修正在執行 `Set-AzResource` 時 JSON 資料類型變更的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2859">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="8c5c8-2860">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2860">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="8c5c8-2861">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2861">Az.Sql</span></span>
* <span data-ttu-id="8c5c8-2862">更新 AuditingEndpointsCommunicator。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2862">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="8c5c8-2863">修正在建立新診斷設定時邊緣案例的行為。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2863">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8c5c8-2864">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2864">Az.Storage</span></span>
* <span data-ttu-id="8c5c8-2865">在建立儲存體帳戶時支援 BlockBlobStorage 種類       - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2865">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="8c5c8-2866">1.4.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2866">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="8c5c8-2867">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2867">Az.AnalysisServices</span></span>
* <span data-ttu-id="8c5c8-2868">即將淘汰 AddAzureASAccount Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2868">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8c5c8-2869">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2869">Az.Automation</span></span>
* <span data-ttu-id="8c5c8-2870">更新 Import-AzAutomationDscNodeConfiguration 的說明</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2870">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="8c5c8-2871">已將設定名稱驗證新增至 Import-AzAutomationDscConfiguration Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2871">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="8c5c8-2872">已改善 Import-AzAutomationDscConfiguration Cmdlet 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2872">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8c5c8-2873">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2873">Az.CognitiveServices</span></span>
* <span data-ttu-id="8c5c8-2874">已將 CustomSubdomainName 新增為 New-AzCognitiveServicesAccount 的新選擇性參數，用來指定資源的子網域。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2874">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8c5c8-2875">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2875">Az.Compute</span></span>
* <span data-ttu-id="8c5c8-2876">修正識別碼參數集問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2876">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="8c5c8-2877">如果未提供 Name 參數，更新 Get-AzVMExtension 以列出所有已安裝的延伸模組</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2877">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="8c5c8-2878">將標記和 ResourceId 參數新增至 Update-AzImage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2878">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="8c5c8-2879">沒有執行個體識別碼的 Get-AzVmssVM，和具有 InstanceView 者可以透過執行個體檢視列出 VMSS VM。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2879">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8c5c8-2880">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2880">Az.DataLakeStore</span></span>
* <span data-ttu-id="8c5c8-2881">為 ADL 刪除的項目列舉和還原新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2881">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8c5c8-2882">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2882">Az.EventHub</span></span>
* <span data-ttu-id="8c5c8-2883">在 Eventhub 的 CaptureDescription 類別中，已將新的布林值屬性 SkipEmptyArchives 新增至 Skip Empty Archives</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2883">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8c5c8-2884">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2884">Az.KeyVault</span></span>
* <span data-ttu-id="8c5c8-2885">修正 Set-AzKeyVaultSecret 的標記</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2885">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8c5c8-2886">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2886">Az.LogicApp</span></span>
* <span data-ttu-id="8c5c8-2887">在整合帳戶的基本 sku 新增</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2887">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="8c5c8-2888">在 XSLT 2.0、XSLT 3.0 和 Liquid 對應類型中新增</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2888">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="8c5c8-2889">整合帳戶組件的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2889">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="8c5c8-2890">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2890">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="8c5c8-2891">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2891">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="8c5c8-2892">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2892">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="8c5c8-2893">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2893">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="8c5c8-2894">整合帳戶批次設定的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2894">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="8c5c8-2895">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2895">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="8c5c8-2896">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2896">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="8c5c8-2897">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2897">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="8c5c8-2898">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2898">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="8c5c8-2899">將邏輯應用程式 SDK 更新至 4.1.0 版</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2899">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8c5c8-2900">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2900">Az.Monitor</span></span>
* <span data-ttu-id="8c5c8-2901">更新 Get-AzMetric 的說明</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2901">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8c5c8-2902">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2902">Az.Network</span></span>
* <span data-ttu-id="8c5c8-2903">更新 Add-AzApplicationGatewayCustomError 的說明範例</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2903">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8c5c8-2904">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2904">Az.OperationalInsights</span></span>
* <span data-ttu-id="8c5c8-2905">取得 ApplicationInsights 與新資料來源的其他支援。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2905">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="8c5c8-2906">已新增新 'ApplicationInsights' 類型，以支援指定工作區的取得特定和取得所有 ApplicationInsights 資料來源。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2906">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="8c5c8-2907">已新增 New-AzOperationalInsightsApplicationInsightsDataSource Cmdlet 用來建立資料來源，透過指定的 Application-Insights 資源參數：訂用帳戶識別碼、resourceGroupName 和名稱。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2907">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8c5c8-2908">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2908">Az.Resources</span></span>
* <span data-ttu-id="8c5c8-2909">修正 https://github.com/Azure/azure-powershell/issues/8166 的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2909">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="8c5c8-2910">修正 https://github.com/Azure/azure-powershell/issues/8235 的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2910">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="8c5c8-2911">修正 https://github.com/Azure/azure-powershell/issues/6219 的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2911">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="8c5c8-2912">修正防止重複建立 KeyCredentials 的錯誤</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2912">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="8c5c8-2913">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2913">Az.Sql</span></span>
* <span data-ttu-id="8c5c8-2914">新增 SQL DB 超大規模層支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2914">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="8c5c8-2915">已修正以下錯誤：由於在還原要求中設定非必要屬性造成還原失敗</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2915">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8c5c8-2916">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2916">Az.Websites</span></span>
* <span data-ttu-id="8c5c8-2917">Get-AzWebAppSlotMetrics 中的正確範例</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2917">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="8c5c8-2918">1.3.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2918">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8c5c8-2919">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2919">Az.Accounts</span></span>
* <span data-ttu-id="8c5c8-2920">更新至最新版本的 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2920">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="8c5c8-2921">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2921">Az.AnalysisServices</span></span>
<span data-ttu-id="8c5c8-2922">Az.AnalysisServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2922">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8c5c8-2923">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2923">Az.Compute</span></span>
* <span data-ttu-id="8c5c8-2924">AEM 延伸模組：新增對 UltraSSD 和 P60、P70 和 P80 磁碟的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2924">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="8c5c8-2925">更新 AzVMBootDiagnostics 的說明描述</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2925">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="8c5c8-2926">更新 Update-AzImage 的說明描述和範例</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2926">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8c5c8-2927">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2927">Az.RecoveryServices</span></span>
<span data-ttu-id="8c5c8-2928">Az.RecoveryServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2928">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8c5c8-2929">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2929">Az.Resources</span></span>
* <span data-ttu-id="8c5c8-2930">修正資源群組標記</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2930">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="8c5c8-2931">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2931">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="8c5c8-2932">修正 `Get-AzureRmRoleAssignment`不遵守 -ErrorAction 的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2932">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="8c5c8-2933">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2933">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="8c5c8-2934">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2934">Az.Sql</span></span>
* <span data-ttu-id="8c5c8-2935">新增 Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2935">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="8c5c8-2936">修正執行 SQL Cmdlet 時無法登入 Azure 帳戶會導致 nullref 例外狀況的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2936">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="8c5c8-2937">已修正 Get AzSqlCapability 中的 Null 參考例外狀況</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2937">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="8c5c8-2938">1.2.1 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2938">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8c5c8-2939">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2939">Az.Accounts</span></span>
* <span data-ttu-id="8c5c8-2940">包含正確驗證版本的發行</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2940">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="8c5c8-2941">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2941">Az.AnalysisServices</span></span>
* <span data-ttu-id="8c5c8-2942">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2942">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8c5c8-2943">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2943">Az.RecoveryServices</span></span>
* <span data-ttu-id="8c5c8-2944">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2944">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="8c5c8-2945">1.2.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2945">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8c5c8-2946">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2946">Az.Accounts</span></span>
* <span data-ttu-id="8c5c8-2947">僅新增 Windows PowerShell 5.1 互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2947">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8c5c8-2948">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2948">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8c5c8-2949">在 PS Core 中新增 Uninstall-AzureRm 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2949">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="8c5c8-2950">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2950">Az.Aks</span></span>
* <span data-ttu-id="8c5c8-2951">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2951">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8c5c8-2952">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2952">Az.Automation</span></span>
* <span data-ttu-id="8c5c8-2953">已新增 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2953">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="8c5c8-2954">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2954">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8c5c8-2955">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2955">Az.Cdn</span></span>
* <span data-ttu-id="8c5c8-2956">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2956">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8c5c8-2957">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2957">Az.Compute</span></span>
* <span data-ttu-id="8c5c8-2958">新增 Invoke-AzVMReimage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2958">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="8c5c8-2959">將 TempDisk 參數新增至 Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2959">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="8c5c8-2960">修正 New-AzVM 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2960">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="8c5c8-2961">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2961">Az.ContainerRegistry</span></span>
* <span data-ttu-id="8c5c8-2962">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2962">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8c5c8-2963">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2963">Az.DataFactory</span></span>
* <span data-ttu-id="8c5c8-2964">已將 ADF .Net SDK 版本更新為 3.0.0</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2964">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8c5c8-2965">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2965">Az.DataLakeStore</span></span>
* <span data-ttu-id="8c5c8-2966">修正使用 MSI 時 ADLS 端點的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2966">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="8c5c8-2967">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2967">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="8c5c8-2968">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2968">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8c5c8-2969">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2969">Az.IotHub</span></span>
* <span data-ttu-id="8c5c8-2970">將編碼格式新增至 Add-IotHubRoutingEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2970">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8c5c8-2971">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2971">Az.KeyVault</span></span>
* <span data-ttu-id="8c5c8-2972">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2972">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8c5c8-2973">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2973">Az.Network</span></span>
* <span data-ttu-id="8c5c8-2974">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2974">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="8c5c8-2975">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2975">Az.Resources</span></span>
* <span data-ttu-id="8c5c8-2976">修正 「New-AzADAppCredential」和「New-AzADSpCredential」參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2976">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="8c5c8-2977">修正「-TemplateFile」參數路徑並未在執行資源群組部署 Cmdlet 前解析的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2977">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="8c5c8-2978">Az.Resources：正確的 New-AzureRmPolicyDefinition -Mode 預設值文件</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2978">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="8c5c8-2979">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/7522 的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2979">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="8c5c8-2980">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/5747 的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2980">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="8c5c8-2981">修正「PSResourceGroupDeployment」物件格式化的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2981">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="8c5c8-2982">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2982">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8c5c8-2983">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2983">Az.ServiceFabric</span></span>
* <span data-ttu-id="8c5c8-2984">將憑證新增到 VMSS 模型但擲回例外狀況時復原，以修正錯誤： https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2984">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="8c5c8-2985">修正某些錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2985">Fix some error messages.</span></span>
* <span data-ttu-id="8c5c8-2986">修正使用預設 ARM 範本為並未移轉至 Az 的 New-AzServiceFabriCluster 建立叢集的問題。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2986">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="8c5c8-2987">檢查延伸模組中的叢集識別碼，修正只將叢集/應用程式憑證新增至對應至該叢集的 VM 擴展集中的問題。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2987">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="8c5c8-2988">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2988">Az.SignalR</span></span>
* <span data-ttu-id="8c5c8-2989">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2989">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="8c5c8-2990">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2990">Az.Sql</span></span>
* <span data-ttu-id="8c5c8-2991">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2991">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8c5c8-2992">更新了 LicenseType 參數的描述並新增了可能的值</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2992">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="8c5c8-2993">修正當更新受控執行個體身分識別僅為已更新屬性時無法運作的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2993">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="8c5c8-2994">支援在受控執行個體上的自訂定序</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2994">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8c5c8-2995">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2995">Az.Storage</span></span>
* <span data-ttu-id="8c5c8-2996">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2996">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8c5c8-2997">在進階儲存體帳戶上取得/設定傳統記錄/計量時提供詳細錯誤訊息，因為進階儲存體帳戶不支援傳統記錄/計量。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2997">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="8c5c8-2998">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2998">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="8c5c8-2999">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="8c5c8-2999">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="8c5c8-3000">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3000">Az.TrafficManager</span></span>
* <span data-ttu-id="8c5c8-3001">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3001">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8c5c8-3002">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3002">Az.Websites</span></span>
* <span data-ttu-id="8c5c8-3003">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3003">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8c5c8-3004">修正「New-AzWebAppSSLBinding」，以便在應用程式於 ASE 上託管時將憑證上傳到正確的資源群組及位置。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3004">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="8c5c8-3005">修正「New-AzWebAppSSLBinding」以便在將 SSL 憑證繫結至應用程式時不要覆寫標記</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3005">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="8c5c8-3006">1.1.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3006">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8c5c8-3007">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3007">Az.Accounts</span></span>
* <span data-ttu-id="8c5c8-3008">將 'Local' 範圍新增至 Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3008">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8c5c8-3009">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3009">Az.Compute</span></span>
* <span data-ttu-id="8c5c8-3010">在 Restart/Start/Stop/Remove/Set-AzVM 和 Save-AzVMImage 的識別碼參數集中，名稱現在為選用項目</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3010">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="8c5c8-3011">已更新說明檔案中的識別碼描述</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3011">Updated the description of ID in help files</span></span>
* <span data-ttu-id="8c5c8-3012">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3012">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8c5c8-3013">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3013">Az.DataLakeStore</span></span>
* <span data-ttu-id="8c5c8-3014">將資料平面的 SDK 版本更新為 1.1.14，以修正 SDK 問題。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3014">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="8c5c8-3015">針對 getfilestatus 和 liststatus 修正 acesstime 和 modificationtime 的負值處理、修正非同步取消權杖</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3015">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8c5c8-3016">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3016">Az.EventGrid</span></span>
* <span data-ttu-id="8c5c8-3017">已更新為使用 2019-01-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3017">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="8c5c8-3018">更新下列 Cmdlet 來支援 2019-01-01 API 版本中的新案例</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3018">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="8c5c8-3019">New-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3019">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="8c5c8-3020">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3020">Event Time-To-Live,</span></span>
        - <span data-ttu-id="8c5c8-3021">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3021">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="8c5c8-3022">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3022">Dead letter endpoint.</span></span>
    - <span data-ttu-id="8c5c8-3023">Update-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3023">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="8c5c8-3024">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3024">Event Time-To-Live,</span></span>
        - <span data-ttu-id="8c5c8-3025">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3025">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="8c5c8-3026">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3026">Dead letter endpoint.</span></span>
* <span data-ttu-id="8c5c8-3027">針對 New-AzureRmEventGridSubscription 和 Update-AzureRmEventGridSubscription Cmdlet 中的 EndpointType 選項新增列舉值 (namely、storageQueue 和 hybridConnection)。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3027">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="8c5c8-3028">如果預期需要使用者手動建立或更新事件訂閱，則顯示警告訊息。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3028">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8c5c8-3029">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3029">Az.IotHub</span></span>
* <span data-ttu-id="8c5c8-3030">已更新至最新版本的 IotHub SDK</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3030">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8c5c8-3031">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3031">Az.LogicApp</span></span>
* <span data-ttu-id="8c5c8-3032">Get-AzLogicApp 會列出所有項目，無須指定名稱</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3032">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="8c5c8-3033">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3033">Az.Resources</span></span>
* <span data-ttu-id="8c5c8-3034">修正為 'Get-AzResource' 提供 '-ODataQuery' 和 '-ResourceId' 參數時的參數集問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3034">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="8c5c8-3035">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3035">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="8c5c8-3036">修正 New/Set-AzPolicyDefinition 中的 -Custom 參數處理</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3036">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="8c5c8-3037">修正 New-AzDeployment 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3037">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="8c5c8-3038">使 '-MailNickname' 參數成為 'New-AzADUser' 的必要項目</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3038">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="8c5c8-3039">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3039">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="8c5c8-3040">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3040">Az.SignalR</span></span>
* <span data-ttu-id="8c5c8-3041">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3041">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="8c5c8-3042">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3042">Az.Sql</span></span>
* <span data-ttu-id="8c5c8-3043">將儲存體管理用戶端相依性轉換為一般的 SDK 實作。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3043">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8c5c8-3044">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3044">Az.Storage</span></span>
* <span data-ttu-id="8c5c8-3045">使用 Sas 權杖、OAuth 或匿名來建立儲存體內容的 StorageAccountName 時，將其設定為實際的儲存體帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3045">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="8c5c8-3046">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3046">New-AzStorageContext</span></span>
* <span data-ttu-id="8c5c8-3047">使用 '-FullUri' 參數建立 Blob 快照集物件的 Sas 權杖、將傳回的 Uri 修正為快照集 Uri</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3047">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="8c5c8-3048">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3048">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8c5c8-3049">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3049">Az.Websites</span></span>
* <span data-ttu-id="8c5c8-3050">修正 'Get-AzDeletedWebApp' 中的日期剖析錯誤</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3050">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="8c5c8-3051">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3051">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="8c5c8-3052">1.0.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3052">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="8c5c8-3053">一般</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3053">General</span></span>

- <span data-ttu-id="8c5c8-3054">Az 模組正式運作</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3054">General Availability of Az Module</span></span>
- <span data-ttu-id="8c5c8-3055">每個模組的線上說明</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3055">Online help for each module</span></span>
- <span data-ttu-id="8c5c8-3056">如需詳細資訊和藍圖，請參閱 [Az 公告頁面](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3056">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="8c5c8-3057">如需從 AzureRM 遷移的相關資訊，請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3057">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="8c5c8-3058">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3058">Az.Accounts</span></span>
- <span data-ttu-id="8c5c8-3059">已從 Az.Profile 變更</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3059">Changed from Az.Profile</span></span>
- <span data-ttu-id="8c5c8-3060">設定檔和內容類型有固定的資料表格式</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3060">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="8c5c8-3061">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3061">Az.ApiManagement</span></span>
- <span data-ttu-id="8c5c8-3062">#7002 的修正</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3062">Fixes for #7002</span></span>
- <span data-ttu-id="8c5c8-3063">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3063">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="8c5c8-3064">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3064">Az.Batch</span></span>
- <span data-ttu-id="8c5c8-3065">已新增功能，可透過 `PSComputeNode` 上新的 `NodeAgentInformation` 屬性，查看集區中每個 VM 上所執行的 Azure Batch 節點代理程式是哪個版本。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3065">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="8c5c8-3066">`PSDataDisk` 的 `Caching` 預設值現在為 `ReadWrite` 而非 `None`。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3066">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="8c5c8-3067">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3067">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="8c5c8-3068">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3068">Az.Billing</span></span>
- <span data-ttu-id="8c5c8-3069">結合 Billing、Consumption 和 UsageAggregates Cmdlet，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3069">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="8c5c8-3070">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3070">Az.CognitivServices</span></span>
- <span data-ttu-id="8c5c8-3071">針對 New-AzureRmCognitiveServicesAccount 作業上可用的 SkuName 和 Typem 新增完成器</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3071">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="8c5c8-3072">已從 Get-AzCognitiveServicesAccountSkus 移除 GetSkusWithAccountParamSetName 參數集</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3072">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="8c5c8-3073">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3073">Az.ContainerInstance</span></span>
- <span data-ttu-id="8c5c8-3074">已新增 ManagedIdentity 支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3074">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="8c5c8-3075">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3075">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="8c5c8-3076">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3076">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="8c5c8-3077">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3077">Az.DataLakeStore</span></span>
- <span data-ttu-id="8c5c8-3078">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3078">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="8c5c8-3079">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3079">Az.Monitor</span></span>
- <span data-ttu-id="8c5c8-3080">Az.Insights 已重新命名為 Az.Monitor，並有次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3080">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="8c5c8-3081">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3081">Az.KeyVault</span></span>
- <span data-ttu-id="8c5c8-3082">已從輸出類型中移除淘汰的 'PurgeDisabled' 屬性</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3082">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="8c5c8-3083">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3083">Az.MachineLearning</span></span>
- <span data-ttu-id="8c5c8-3084">已納入來自 Az.MachineLearningCompute 模組的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3084">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="8c5c8-3085">Az.Media</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3085">Az.Media</span></span>
- <span data-ttu-id="8c5c8-3086">從 New-AzMediaService 移除淘汰的 -Tags 別名</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3086">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="8c5c8-3087">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3087">Az.Network</span></span>
<span data-ttu-id="8c5c8-3088">已新增在應用程式閘道中設定 RewriteRuleSets 的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3088">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="8c5c8-3089">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3089">New cmdlets added:</span></span>
        - <span data-ttu-id="8c5c8-3090">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3090">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8c5c8-3091">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3091">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8c5c8-3092">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3092">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8c5c8-3093">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3093">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8c5c8-3094">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3094">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8c5c8-3095">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3095">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="8c5c8-3096">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3096">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="8c5c8-3097">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3097">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="8c5c8-3098">Cmdlets updated with optional parameter -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3098">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="8c5c8-3099">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3099">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="8c5c8-3100">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3100">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="8c5c8-3101">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3101">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="8c5c8-3102">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3102">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="8c5c8-3103">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3103">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="8c5c8-3104">New-AzureRmApplicationGatewayUrlPathMapConfig 已使用身分識別對應用程式閘道新增 KeyVault 支援。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3104">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="8c5c8-3105">已使用選擇性參數 -KeyVaultSecretId, -KeyVaultSecret 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3105">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="8c5c8-3106">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3106">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="8c5c8-3107">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3107">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="8c5c8-3108">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3108">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="8c5c8-3109">已使用選擇性參數 -UserAssignedIdentity 更新了 New-AzApplicationGateway Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3109">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="8c5c8-3110">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3110">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="8c5c8-3111">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3111">Az.OperationalInsights</span></span>
- <span data-ttu-id="8c5c8-3112">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3112">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="8c5c8-3113">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3113">Az.Profile</span></span>
- <span data-ttu-id="8c5c8-3114">模組名稱已變更為 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3114">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="8c5c8-3115">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3115">Az.RecoveryServices</span></span>
- <span data-ttu-id="8c5c8-3116">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3116">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="8c5c8-3117">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3117">Az.Resources</span></span>
- <span data-ttu-id="8c5c8-3118">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3118">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="8c5c8-3119">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3119">Az.ServiceFabric</span></span>
- <span data-ttu-id="8c5c8-3120">支援依通用名稱和指紋來指定憑證</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3120">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="8c5c8-3121">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3121">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="8c5c8-3122">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3122">Az.SIgnalR</span></span>
- <span data-ttu-id="8c5c8-3123">SIgnalR 的 PowerShell Cmdlet 正式運作</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3123">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="8c5c8-3124">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3124">Az.Sql</span></span>
- <span data-ttu-id="8c5c8-3125">已對威脅偵測的 Cmdlet 新增 Data_Exfiltration 和 Unsafe_Action 偵測類型</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3125">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="8c5c8-3126">已更新 SQL 稽核 Cmdlet 的文件範例</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3126">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="8c5c8-3127">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3127">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="8c5c8-3128">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3128">Az.Storage</span></span>
- <span data-ttu-id="8c5c8-3129">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3129">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="8c5c8-3130">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3130">Az.Websites</span></span>
- <span data-ttu-id="8c5c8-3131">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3131">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="8c5c8-3132">0.7.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3132">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="8c5c8-3133">一般</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3133">General</span></span>

* <span data-ttu-id="8c5c8-3134">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3134">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="8c5c8-3135">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3135">Az.Compute</span></span>

* <span data-ttu-id="8c5c8-3136">針對 `New-AzVm(ss)` Cmdlet 簡單參數集內的 UltraSSD 和資源庫映像新增支援。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3136">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="8c5c8-3137">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3137">Az.DataLakeStore</span></span>

* <span data-ttu-id="8c5c8-3138">修正 adls 帳戶網域的尾端斜線</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3138">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="8c5c8-3139">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3139">Az.FrontDoor</span></span>

* <span data-ttu-id="8c5c8-3140">已修正一些中斷的連結</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3140">Fixed some broken links</span></span>
    - <span data-ttu-id="8c5c8-3141">在 New-AzureRmFrontDoor 和 Set-AzureRmFrontDoor 文章中，已修正 New-AzureRmFrontDoorHealthProbeSettingObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3141">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="8c5c8-3142">在 New-AzureRmFrontDoorManagedRuleObject 文章中，已修正 New-AzureRmFrontDoorRuleGroupOverrideObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3142">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="8c5c8-3143">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3143">Az.RecoveryServices</span></span>

* <span data-ttu-id="8c5c8-3144">已針對 Azure 檔案共用的還原作業新增用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3144">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="8c5c8-3145">已將 storageAccountName 和 storageAccountResourceGroupName 設為 afs 還原作業的選擇性項目。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3145">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="8c5c8-3146">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3146">Az.Resources</span></span>

* <span data-ttu-id="8c5c8-3147">修正 https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3147">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="8c5c8-3148">將 Get-AzureRmRoleAssignment 更新為使用訂用帳戶範圍 (如果有在要求傳統管理員時提供的話)。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3148">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="8c5c8-3149">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3149">Az.Sql</span></span>

* <span data-ttu-id="8c5c8-3150">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3150">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="8c5c8-3151">已修正搭配使用 Get-AzureRmSqlDatabaseVulnerabilityAssessment 和 DotNet core 時所會發生的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3151">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="8c5c8-3152">已修改 SQL 稽核 Cmdlet 相關說明訊息的文件。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3152">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="8c5c8-3153">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3153">Az.Storage</span></span>

* <span data-ttu-id="8c5c8-3154">對 New-AzureRmStorageAccount 新增 -EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3154">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="8c5c8-3155">已修正下列問題：如果沒有輸入 -DestContext，複製檔案 Cmdlet 無法重複使用目的地中的來源內容</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3155">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="8c5c8-3156">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3156">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="8c5c8-3157">支援靜態網站設定</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3157">Support Static Website configuration</span></span>
    - <span data-ttu-id="8c5c8-3158">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3158">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="8c5c8-3159">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3159">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="8c5c8-3160">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3160">Az.Websites</span></span>

* <span data-ttu-id="8c5c8-3161">Set-AzureRmWebApp 和 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3161">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="8c5c8-3162">已新增新的參數 (-AzureStoragePath)，指定要將 Azure 儲存體路徑掛接至 Windows 和 Linux 容器應用程式中。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3162">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="8c5c8-3163">使用新 Cmdlet New-AzureRmWebAppAzureStoragePath 的輸出作為參數來設定 Azure 儲存體路徑。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3163">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="8c5c8-3164">0.6.1 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3164">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="8c5c8-3165">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3165">Az.ApiManagement</span></span>
* <span data-ttu-id="8c5c8-3166">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3166">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="8c5c8-3167">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3167">Az.Automation</span></span>
* <span data-ttu-id="8c5c8-3168">以 Swagger 為基礎的 Azure 自動化 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3168">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="8c5c8-3169">已新增更新管理 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3169">Added Update Management cmdlets</span></span>
* <span data-ttu-id="8c5c8-3170">已新增原始檔控制 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3170">Added Source Control cmdlets</span></span>
* <span data-ttu-id="8c5c8-3171">已新增 Remove-AzureRmAutomationHybridWorkerGroup Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3171">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="8c5c8-3172">已修正 DSC 註冊節點命令</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3172">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="8c5c8-3173">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3173">Az.Compute</span></span>
* <span data-ttu-id="8c5c8-3174">已修正 SystemAssigned 身分識別的身份識別問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3174">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="8c5c8-3175">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3175">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="8c5c8-3176">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3176">Az.ContainerInstance</span></span>
* <span data-ttu-id="8c5c8-3177">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3177">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="8c5c8-3178">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3178">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="8c5c8-3179">更新市集 Cmdlet 的範例描述</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3179">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="8c5c8-3180">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3180">Az.Network</span></span>
* <span data-ttu-id="8c5c8-3181">已新增 Cmdlet：New-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayCustomError、Get-AzureRmApplicationGatewayCustomError、Set-AzureRmApplicationGatewayCustomError、Remove-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayHttpListenerCustomError、Get-AzureRmApplicationGatewayHttpListenerCustomError、Set-AzureRmApplicationGatewayHttpListenerCustomError、Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3181">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="8c5c8-3182">已將 ICMP 加回支援的 AzureFirewall 網路通訊協定</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3182">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="8c5c8-3183">更新 Test-AzureRmNetworkWatcherConnectivity Cmdlet，在目的地識別碼、位址和連接埠上新增驗證。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3183">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="8c5c8-3184">修正 VirtualNetwork 對應中的記憶體使用量問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3184">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="8c5c8-3185">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3185">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="8c5c8-3186">提供修正程式以修改受保護的檔案共用原則。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3186">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="8c5c8-3187">已將原則時區轉換為大寫。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3187">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="8c5c8-3188">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3188">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="8c5c8-3189">已修正 New-AzureRmRecoveryServicesAsrProtectableItem 中的範例</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3189">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="8c5c8-3190">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3190">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="8c5c8-3191">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3191">Az.Relay</span></span>
* <span data-ttu-id="8c5c8-3192">已將選擇性參數 -KeyValue 新增至 New-AzureRmRelayKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3192">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="8c5c8-3193">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3193">Az.Resources</span></span>
* <span data-ttu-id="8c5c8-3194">更新 `New-AzureRmPolicyAssignment` 和 `Set-AzureRmPolicyAssignment` 中資源身分識別相關參數的說明文件</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3194">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="8c5c8-3195">新增使用 -Metadata 的 New-AzureRmPolicyDefinition 範例</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3195">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="8c5c8-3196">修正：允許在 NetStandard: #7678 #7703 的標籤索引鍵中保留大小寫</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3196">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="8c5c8-3197">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3197">Az.ServiceFabric</span></span>
* <span data-ttu-id="8c5c8-3198">針對即將推出的重大變更新增取代資訊</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3198">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="8c5c8-3199">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3199">Az.Sql</span></span>
* <span data-ttu-id="8c5c8-3200">已在 Azure SQL Database 受控執行個體和 Azure SQL 受控資料庫上新增 CRUD 作業的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3200">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="8c5c8-3201">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3201">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8c5c8-3202">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3202">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8c5c8-3203">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3203">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8c5c8-3204">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3204">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8c5c8-3205">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3205">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="8c5c8-3206">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3206">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="8c5c8-3207">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3207">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="8c5c8-3208">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3208">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="8c5c8-3209">已在伺服器或資料庫上啟用擴充的稽核原則管理。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3209">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="8c5c8-3210">已新增參數 (PredicateExpression) 以啟用稽核記錄的篩選。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3210">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="8c5c8-3211">已將 Cmdlet 修改為使用 SQL 用戶端，而不是傳統用戶端。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3211">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="8c5c8-3212">Set-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3212">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="8c5c8-3213">Get-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3213">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="8c5c8-3214">Set-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3214">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="8c5c8-3215">Get-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3215">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="8c5c8-3216">已修正使用 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings 和儲存體帳戶名稱參數集的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3216">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="8c5c8-3217">0.5.0 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3217">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="8c5c8-3218">一般</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3218">General</span></span>
* <span data-ttu-id="8c5c8-3219">已在許多核心 Cmdlet 新增資源完成器 - 這些 Cmdlet 可讓您在以互動方式叫用 Cmdlet 時，使用 TAB 鍵瀏覽現有資源名稱</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3219">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="8c5c8-3220">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3220">Az.Profile</span></span>
* <span data-ttu-id="8c5c8-3221">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3221">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="8c5c8-3222">將 Cmdlet Connect-AzAccount 中的參數 TenantId 重新命名為 Tenant 並新增 TenantId 的別名</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3222">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="8c5c8-3223">更新 Connect-AzAccount 的 TenantId 說明</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3223">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="8c5c8-3224">修正提供租用戶網域時登入失敗的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3224">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="8c5c8-3225">修正租用戶中無訂用帳戶之帳戶內容衝突的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3225">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="8c5c8-3226">修正使用 MSI 時 DataLake 端點的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3226">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="8c5c8-3227">修正若未連線，'Disconnect-AzAccount' 會擲出錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3227">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="8c5c8-3228">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3228">Az.CognitiveServices</span></span>
* <span data-ttu-id="8c5c8-3229">新增 Get-AzCognitiveServicesAccountSkus 作業。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3229">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8c5c8-3230">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3230">Az.Compute</span></span>
* <span data-ttu-id="8c5c8-3231">新增 Add-AzVmssVMDataDisk 和 Remove-AzVmssVMDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3231">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="8c5c8-3232">Get-AzVMImage 顯示 AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3232">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="8c5c8-3233">已修正 SetAzVMChefExtension -BootstrapOptions 和 -JsonAttribute 選項值並未以 json 格式設定的問題。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3233">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8c5c8-3234">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3234">Az.DataLakeStore</span></span>
* <span data-ttu-id="8c5c8-3235">將 DataLake 套件更新為 1.1.10。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3235">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="8c5c8-3236">將預設並行新增至多執行作業。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3236">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="8c5c8-3237">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3237">Az.Insights</span></span>
* <span data-ttu-id="8c5c8-3238">已修正問題 #7267 (自動調整區域)</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3238">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="8c5c8-3239">建立新自動調整規則時未適當設定列舉的參數 (一律會設為預設值) 的問題。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3239">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="8c5c8-3240">已修正問題 #7513 [Insights] Set-AzDiagnosticSetting 在建立設定時需要明確的類別規格</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3240">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="8c5c8-3241">目前 Cmdlet 在建立期間不需要明確的類別指示也能啟用，例如 Cmdlet 會如說明所述之方式運作</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3241">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8c5c8-3242">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3242">Az.Network</span></span>
* <span data-ttu-id="8c5c8-3243">已將 PeeringType 變更為下列 Cmdlet 的必要參數：-</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3243">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="8c5c8-3244">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3244">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="8c5c8-3245">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3245">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="8c5c8-3246">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3246">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="8c5c8-3247">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3247">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="8c5c8-3248">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3248">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="8c5c8-3249">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3249">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8c5c8-3250">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3250">Az.PolicyInsights</span></span>
* <span data-ttu-id="8c5c8-3251">已新增原則修復 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3251">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="8c5c8-3252">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3252">Az.Resources</span></span>
* <span data-ttu-id="8c5c8-3253">修正 https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3253">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="8c5c8-3254">允許使用 'Get-AzResource' 的 '-ResourceId' 參數列出資源</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3254">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8c5c8-3255">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3255">Az.ServiceBus</span></span>
* <span data-ttu-id="8c5c8-3256">已將 MigrationState 唯讀屬性新增至 PSServiceBusMigrationConfigurationAttributes，以便協助了解移轉狀態。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3256">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8c5c8-3257">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3257">Az.ServiceFabric</span></span>
* <span data-ttu-id="8c5c8-3258">修正將憑證新增至 Linux Vmss。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3258">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="8c5c8-3259">修正 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3259">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="8c5c8-3260">使用新憑證中正確的指紋 (Azure/service-fabric-issues#932)。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3260">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="8c5c8-3261">正確顯示例外狀況 (Azure/service-fabric-issues#1054)。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3261">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="8c5c8-3262">修正 'Update-AzServiceFabricDurability' 以在啟動 Vmss CreateOrUpdate operation 之前更新叢集組態。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3262">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="8c5c8-3263">0.4.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3263">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="8c5c8-3264">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3264">Az.Profile</span></span>
* <span data-ttu-id="8c5c8-3265">修正 CloudShell 中 Get-AzSubscription 的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3265">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="8c5c8-3266">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3266">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8c5c8-3267">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3267">Az.Compute</span></span>
* <span data-ttu-id="8c5c8-3268">已將新的大小新增至虛擬機器大小允許清單，當使用 'New-AzVm' 的簡單參數集合時，將會開啟加速的網路</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3268">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="8c5c8-3269">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3269">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8c5c8-3270">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3270">Az.DataLakeStore</span></span>
* <span data-ttu-id="8c5c8-3271">新增虛擬網路規則的支援</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3271">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="8c5c8-3272">Get-AzDataLakeStoreVirtualNetworkRule：取得或列出 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3272">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="8c5c8-3273">Add-AzDataLakeStoreVirtualNetworkRule：將虛擬網路規則新增至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3273">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="8c5c8-3274">Set-AzDataLakeStoreVirtualNetworkRule：修改指定 Data Lake Store 帳戶中的特定虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3274">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="8c5c8-3275">Remove-AzDataLakeStoreVirtualNetworkRule：刪除 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3275">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8c5c8-3276">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3276">Az.Network</span></span>
* <span data-ttu-id="8c5c8-3277">更新 Cmdlet Test-AzNetworkWatcherConnectivity，將通訊協定值傳遞至後端。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3277">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="8c5c8-3278">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3278">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8c5c8-3279">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3279">Az.Resources</span></span>
* <span data-ttu-id="8c5c8-3280">修正當 Get-AzRoleDefinition 藉由在案例中加上有意義的例外狀況，而擲回無法辨識的例外狀況 (當預設的設定檔中沒有訂用帳戶，且未指定範圍) 問題。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3280">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="8c5c8-3281">也將預設參數集合設定為 'RoleDefinitionNameParameterSet'。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3281">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="8c5c8-3282">0.3.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3282">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="8c5c8-3283">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3283">Azure.Storage</span></span>
* <span data-ttu-id="8c5c8-3284">修正當目的地有中繼資料問題時，複製 Blob/檔案不會一併複製中繼資料的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3284">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="8c5c8-3285">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3285">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="8c5c8-3286">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3286">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="8c5c8-3287">支援取得特定位置的儲存體資源使用量，並針對取得全域儲存體資源使用量已過時的情況新增警告訊息。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3287">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="8c5c8-3288">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3288">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8c5c8-3289">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3289">Az.CognitiveServices</span></span>
* <span data-ttu-id="8c5c8-3290">在沒有現有帳戶的情況下支援 Get-AzCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3290">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8c5c8-3291">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3291">Az.Compute</span></span>
* <span data-ttu-id="8c5c8-3292">修正 Get-AzVM -ResourceGroupName <rg> 以在必要時傳回超過 50 個結果</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3292">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="8c5c8-3293">已將 'SimpleParameterSet' 的範例新增到 New-AzVmss Cmdlet 說明中。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3293">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="8c5c8-3294">已修正 Azure 磁碟加密進度訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3294">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="8c5c8-3295">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3295">Az.DataFactoryV2</span></span>
* <span data-ttu-id="8c5c8-3296">已將 ADF .Net SDK 版本更新為 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3296">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8c5c8-3297">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3297">Az.Network</span></span>
* <span data-ttu-id="8c5c8-3298">已新增 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3298">Added NetworkProfile functionality.</span></span> <span data-ttu-id="8c5c8-3299">已新增新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3299">new cmdlets added</span></span>
    - <span data-ttu-id="8c5c8-3300">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3300">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="8c5c8-3301">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3301">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="8c5c8-3302">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3302">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="8c5c8-3303">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3303">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="8c5c8-3304">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3304">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="8c5c8-3305">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3305">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="8c5c8-3306">已在子網路模型中新增服務關聯連結</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3306">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="8c5c8-3307">已新增 New-AzVirtualNetworkTap、Get-AzVirtualNetworkTap、Set-AzVirtualNetworkTap、Remove-AzVirtualNetworkTap Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3307">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="8c5c8-3308">已新增 Set-AzNEtworkInterfaceTapConfig、Get-AzNEtworkInterfaceTapConfig 和 Remove-AzNEtworkInterfaceTapConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3308">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="8c5c8-3309">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3309">Az.RedisCache</span></span>
* <span data-ttu-id="8c5c8-3310">日後允許任何字串做為 Size 參數。</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3310">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="8c5c8-3311">在 P5 PSArgumentCompleter 快顯視窗中新增 P5</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3311">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="8c5c8-3312">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3312">Az.Resources</span></span>
* <span data-ttu-id="8c5c8-3313">將遺漏的 -Mode 參數新增至 Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3313">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="8c5c8-3314">修正 Get-AzProviderOperation Commandlet 錯誤 (bug)，以進行包含使用者的 Origin 作業</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3314">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="8c5c8-3315">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3315">Az.Sql</span></span>
* <span data-ttu-id="8c5c8-3316">已修正部分備份 Cmdlet 無法辨識目前 Azure 訂用帳戶的問題</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3316">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8c5c8-3317">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3317">Az.Websites</span></span>
* <span data-ttu-id="8c5c8-3318">新 Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 取得容器連續部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3318">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="8c5c8-3319">新 Cmdlet New-AzWebAppContainerPSSession 與 Enter-WebAppContainerPSSession  - 在 Windows 容器應用程式中初始 PowerShell 遠端工作階段</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3319">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="8c5c8-3320">0.2.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3320">0.2.0 - September 2018</span></span>
 <span data-ttu-id="8c5c8-3321">初始版本</span><span class="sxs-lookup"><span data-stu-id="8c5c8-3321">Initial Release</span></span>
