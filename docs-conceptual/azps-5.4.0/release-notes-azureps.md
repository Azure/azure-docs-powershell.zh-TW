---
title: Azure PowerShell 版本資訊
description: 了解 Azure PowerShell 模組的最新更新資訊。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 8cf52259008b2551b780d4cf6f09b4876673723c
ms.sourcegitcommit: 12bb1a6d1f89789bf2a78992f9b8ca848691a4d7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/19/2021
ms.locfileid: "98573613"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="db717-103">Azure PowerShell 版本資訊</span><span class="sxs-lookup"><span data-stu-id="db717-103">Azure PowerShell release notes</span></span>

## <a name="540---january-2021"></a><span data-ttu-id="db717-104">5.4.0-2021 年1月</span><span class="sxs-lookup"><span data-stu-id="db717-104">5.4.0 - January 2021</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="db717-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="db717-105">Az.Accounts</span></span>
* <span data-ttu-id="db717-106">在 debug 訊息上顯示正確的用戶端要求識別碼 [#13745]</span><span class="sxs-lookup"><span data-stu-id="db717-106">Shown correct client request id on debug message [#13745]</span></span>
* <span data-ttu-id="db717-107">已新增常見的 Azure PowerShell 例外狀況類型</span><span class="sxs-lookup"><span data-stu-id="db717-107">Added common Azure PowerShell exception type</span></span>
* <span data-ttu-id="db717-108">支援的儲存體 API 2019-06-01</span><span class="sxs-lookup"><span data-stu-id="db717-108">Supported storage API 2019-06-01</span></span>

#### <a name="azautomation"></a><span data-ttu-id="db717-109">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="db717-109">Az.Automation</span></span>
* <span data-ttu-id="db717-110">修正未針對更新管理排程填入描述的問題</span><span class="sxs-lookup"><span data-stu-id="db717-110">Fixed issue where description was not populated for update management schedules</span></span>

#### <a name="azcosmosdb"></a><span data-ttu-id="db717-111">Az. CosmosDB</span><span class="sxs-lookup"><span data-stu-id="db717-111">Az.CosmosDB</span></span>
* <span data-ttu-id="db717-112">' Az. CosmosDB ' 模組正式推出</span><span class="sxs-lookup"><span data-stu-id="db717-112">General availability of 'Az.CosmosDB' module</span></span>
* <span data-ttu-id="db717-113">限制 New-AzCosmosDBAccount Cmdlet，以對現有的資料庫帳戶進行更新呼叫。</span><span class="sxs-lookup"><span data-stu-id="db717-113">Restricting New-AzCosmosDBAccount cmdlet to make update calls to existing Database Accounts.</span></span>
* <span data-ttu-id="db717-114">SqlContainer 中的 AnalyticalStorageTTL 簡介。</span><span class="sxs-lookup"><span data-stu-id="db717-114">Introducing AnalyticalStorageTTL in SqlContainer.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="db717-115">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="db717-115">Az.IotHub</span></span>
* <span data-ttu-id="db717-116">修正關於產生 SAS 權杖的回歸</span><span class="sxs-lookup"><span data-stu-id="db717-116">Fixed a regression regarding SAS token generation</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="db717-117">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="db717-117">Az.KeyVault</span></span>
* <span data-ttu-id="db717-118">已修正秘密管理模組中的問題</span><span class="sxs-lookup"><span data-stu-id="db717-118">Fixed an issue in Secret Management module</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="db717-119">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="db717-119">Az.LogicApp</span></span>
* <span data-ttu-id="db717-120">修正了「AzLogicAppTriggerHistory」和「AzLogicAppRunAction」只會在第一頁結果中取得 [#9141] 的問題</span><span class="sxs-lookup"><span data-stu-id="db717-120">Fixed issue that 'Get-AzLogicAppTriggerHistory' and 'Get-AzLogicAppRunAction' only retrieving the first page of results [#9141]</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="db717-121">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="db717-121">Az.Monitor</span></span>
* <span data-ttu-id="db717-122">已新增資料收集規則的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="db717-122">Added cmdlets for data collection rules:</span></span> 
    - <span data-ttu-id="db717-123">' AzDataCollectionRule '</span><span class="sxs-lookup"><span data-stu-id="db717-123">'Get-AzDataCollectionRule'</span></span>
    - <span data-ttu-id="db717-124">' AzDataCollectionRule '</span><span class="sxs-lookup"><span data-stu-id="db717-124">'New-AzDataCollectionRule'</span></span>
    - <span data-ttu-id="db717-125">' AzDataCollectionRule '</span><span class="sxs-lookup"><span data-stu-id="db717-125">'Set-AzDataCollectionRule'</span></span>
    - <span data-ttu-id="db717-126">' AzDataCollectionRule '</span><span class="sxs-lookup"><span data-stu-id="db717-126">'Update-AzDataCollectionRule'</span></span>
    - <span data-ttu-id="db717-127">' AzDataCollectionRule '</span><span class="sxs-lookup"><span data-stu-id="db717-127">'Remove-AzDataCollectionRule'</span></span>
* <span data-ttu-id="db717-128">已新增資料收集規則關聯的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-128">Added cmdlets for data collection rules associations</span></span>
    - <span data-ttu-id="db717-129">' AzDataCollectionRuleAssociation '</span><span class="sxs-lookup"><span data-stu-id="db717-129">'Get-AzDataCollectionRuleAssociation'</span></span>
    - <span data-ttu-id="db717-130">' AzDataCollectionRuleAssociation '</span><span class="sxs-lookup"><span data-stu-id="db717-130">'New-AzDataCollectionRuleAssociation'</span></span>
    - <span data-ttu-id="db717-131">' AzDataCollectionRuleAssociation '</span><span class="sxs-lookup"><span data-stu-id="db717-131">'Remove-AzDataCollectionRuleAssociation'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="db717-132">Az.Network</span><span class="sxs-lookup"><span data-stu-id="db717-132">Az.Network</span></span>
* <span data-ttu-id="db717-133">已新增 VpnGatewayNATRule CRUD 的新 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db717-133">Added new cmdlets for CRUD of VpnGatewayNATRule.</span></span>
    - <span data-ttu-id="db717-134">' AzAzVpnGatewayNatRule '</span><span class="sxs-lookup"><span data-stu-id="db717-134">'New-AzAzVpnGatewayNatRule'</span></span>
    - <span data-ttu-id="db717-135">' AzAzVpnGatewayNatRule '</span><span class="sxs-lookup"><span data-stu-id="db717-135">'Update-AzAzVpnGatewayNatRule'</span></span>
    - <span data-ttu-id="db717-136">' AzAzVpnGatewayNatRule '</span><span class="sxs-lookup"><span data-stu-id="db717-136">'Get-AzAzVpnGatewayNatRule'</span></span>
    - <span data-ttu-id="db717-137">' AzAzVpnGatewayNatRule '</span><span class="sxs-lookup"><span data-stu-id="db717-137">'Remove-AzAzVpnGatewayNatRule'</span></span>    
* <span data-ttu-id="db717-138">已更新 Cmdlet，以在 VpnGateway 資源上設定 NATRule，並將其與 VpnSiteLinkConnection 資源建立關聯。</span><span class="sxs-lookup"><span data-stu-id="db717-138">Updated cmdlets to set NATRule on VpnGateway resource and associate it with VpnSiteLinkConnection resource.</span></span>
    - <span data-ttu-id="db717-139">' AzVpnGateway '</span><span class="sxs-lookup"><span data-stu-id="db717-139">'New-AzVpnGateway'</span></span>
    - <span data-ttu-id="db717-140">' AzVpnGateway '</span><span class="sxs-lookup"><span data-stu-id="db717-140">'Update-AzVpnGateway'</span></span> 
    - <span data-ttu-id="db717-141">' AzVpnSiteLinkConnection '</span><span class="sxs-lookup"><span data-stu-id="db717-141">'New-AzVpnSiteLinkConnection'</span></span>
* <span data-ttu-id="db717-142">已更新 Cmdlet，可讓您在虛擬網路閘道連線上設定 ConnectionMode。</span><span class="sxs-lookup"><span data-stu-id="db717-142">Updated cmdlets to enable setting of ConnectionMode on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="db717-143">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="db717-143">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="db717-144">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="db717-144">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="db717-145">已更新 ' AzFirewallPolicyApplicationRule ' Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="db717-145">Updated 'New-AzFirewallPolicyApplicationRule' cmdlet:</span></span>
    - <span data-ttu-id="db717-146">已新增參數 TargetUrl</span><span class="sxs-lookup"><span data-stu-id="db717-146">Added parameter TargetUrl</span></span>
    - <span data-ttu-id="db717-147">已新增參數 TerminateTLS</span><span class="sxs-lookup"><span data-stu-id="db717-147">Added parameter TerminateTLS</span></span>
* <span data-ttu-id="db717-148">已新增 Azure 防火牆 Premium 功能的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-148">Added new cmdlets for Azure Firewall Premium Features</span></span>
    - <span data-ttu-id="db717-149">' AzFirewallPolicyIntrusionDetection '</span><span class="sxs-lookup"><span data-stu-id="db717-149">'New-AzFirewallPolicyIntrusionDetection'</span></span>
    - <span data-ttu-id="db717-150">' AzFirewallPolicyIntrusionDetectionBypassTraffic '</span><span class="sxs-lookup"><span data-stu-id="db717-150">'New-AzFirewallPolicyIntrusionDetectionBypassTraffic'</span></span>
    - <span data-ttu-id="db717-151">' AzFirewallPolicyIntrusionDetectionSignatureOverride '</span><span class="sxs-lookup"><span data-stu-id="db717-151">'New-AzFirewallPolicyIntrusionDetectionSignatureOverride'</span></span>
* <span data-ttu-id="db717-152">已更新 New-AzFirewallPolicy Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="db717-152">Updated New-AzFirewallPolicy cmdlet:</span></span>
    - <span data-ttu-id="db717-153">已新增參數-SkuTier</span><span class="sxs-lookup"><span data-stu-id="db717-153">Added parameter -SkuTier</span></span>
    - <span data-ttu-id="db717-154">已新增參數-身分識別</span><span class="sxs-lookup"><span data-stu-id="db717-154">Added parameter -Identity</span></span>
    - <span data-ttu-id="db717-155">已新增參數-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="db717-155">Added parameter -UserAssignedIdentityId</span></span>
    - <span data-ttu-id="db717-156">已新增參數-IntrusionDetection</span><span class="sxs-lookup"><span data-stu-id="db717-156">Added parameter -IntrusionDetection</span></span>
    - <span data-ttu-id="db717-157">已新增參數-TransportSecurityName</span><span class="sxs-lookup"><span data-stu-id="db717-157">Added parameter -TransportSecurityName</span></span>
    - <span data-ttu-id="db717-158">已新增參數-TransportSecurityKeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="db717-158">Added parameter -TransportSecurityKeyVaultSecretId</span></span>
* <span data-ttu-id="db717-159">已新增新的 Cmdlet，以提取虛擬網路閘道連線的 IKE 安全性關聯。</span><span class="sxs-lookup"><span data-stu-id="db717-159">Added new cmdlet to fetch IKE Security Associations for Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="db717-160">' AzVirtualNetworkGatewayConnectionIkeSa '</span><span class="sxs-lookup"><span data-stu-id="db717-160">'Get-AzVirtualNetworkGatewayConnectionIkeSa'</span></span>
* <span data-ttu-id="db717-161">為 p2sVpnGateway 新增了多個驗證支援</span><span class="sxs-lookup"><span data-stu-id="db717-161">Added multiple Authentication support for p2sVpnGateway</span></span>
    - <span data-ttu-id="db717-162">已更新 New-AzVpnServerConfiguration 和 Update-AzVpnServerConfiguration，以允許設定多個驗證參數。</span><span class="sxs-lookup"><span data-stu-id="db717-162">Updated New-AzVpnServerConfiguration and Update-AzVpnServerConfiguration to allow multiple authentication parameters to be set.</span></span>
* <span data-ttu-id="db717-163">已更新 ' AzVpnGateway ' 和 ' AzP2sVpnGateway ' Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="db717-163">Updated 'New-AzVpnGateway' and 'New-AzP2sVpnGateway' cmdlet:</span></span>
    - <span data-ttu-id="db717-164">已新增參數 EnableRoutingPreferenceInternetFlag</span><span class="sxs-lookup"><span data-stu-id="db717-164">Added parameter EnableRoutingPreferenceInternetFlag</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="db717-165">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="db717-165">Az.RecoveryServices</span></span>
* <span data-ttu-id="db717-166">已新增跨區域還原功能。</span><span class="sxs-lookup"><span data-stu-id="db717-166">Added Cross Region Restore feature.</span></span>  
* <span data-ttu-id="db717-167">當目標專案為可用性群組時，封鎖取得工作負載設定。</span><span class="sxs-lookup"><span data-stu-id="db717-167">Blocked getting workload config when target item is an availability group.</span></span>

#### <a name="azresources"></a><span data-ttu-id="db717-168">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="db717-168">Az.Resources</span></span>
* <span data-ttu-id="db717-169">在新的 Az \* 部署 Cmdlet 中新增-QueryString 參數的支援</span><span class="sxs-lookup"><span data-stu-id="db717-169">Added support for -QueryString parameter in New-Az\*Deployments cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="db717-170">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="db717-170">Az.Sql</span></span>
* <span data-ttu-id="db717-171">已將 ' AzSqlInstanceDatabaseLogReplay ' Cmdlet 設為同步，已新增-AsJob 旗標</span><span class="sxs-lookup"><span data-stu-id="db717-171">Made 'Start-AzSqlInstanceDatabaseLogReplay' cmdlet synchronous, added -AsJob flag</span></span>

#### <a name="azstorage"></a><span data-ttu-id="db717-172">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="db717-172">Az.Storage</span></span>
* <span data-ttu-id="db717-173">修正當清單 blob 與-IncludeVersion 時，ContinuationToken 絕不會是 null</span><span class="sxs-lookup"><span data-stu-id="db717-173">Fix ContinuationToken never null when list blob with -IncludeVersion</span></span>
    - <span data-ttu-id="db717-174">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="db717-174">'Get-AzStorageBlob'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="db717-175">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="db717-175">Az.Websites</span></span>
* <span data-ttu-id="db717-176">已新增 App Service 受控憑證的支援</span><span class="sxs-lookup"><span data-stu-id="db717-176">Added support for App Service Managed certificates</span></span>
    - <span data-ttu-id="db717-177">' AzWebAppCertificate '</span><span class="sxs-lookup"><span data-stu-id="db717-177">'New-AzWebAppCertificate'</span></span>
    - <span data-ttu-id="db717-178">' AzWebAppCertificate '</span><span class="sxs-lookup"><span data-stu-id="db717-178">'Remove-AzWebAppCertificate'</span></span>
* <span data-ttu-id="db717-179">已修正導致 Docker 密碼從 ' Set-azwebapp ' 和 ' Set-azwebappslot ' 中的 appsettings 中移除的問題</span><span class="sxs-lookup"><span data-stu-id="db717-179">Fixed issue that causes Docker Password to be removed from appsettings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="db717-180">感謝我們的社群參與者</span><span class="sxs-lookup"><span data-stu-id="db717-180">Thanks to our community contributors</span></span>
* <span data-ttu-id="db717-181">Ivan Akcheurov (@ivanakcheurov) ，Update Set-AzSecurityWorkspaceSetting.md ( # 13877) </span><span class="sxs-lookup"><span data-stu-id="db717-181">Ivan Akcheurov (@ivanakcheurov), Update Set-AzSecurityWorkspaceSetting.md (#13877)</span></span>
* <span data-ttu-id="db717-182">@javiermarasco，更新範例 ( # 13837) </span><span class="sxs-lookup"><span data-stu-id="db717-182">@javiermarasco, Update example (#13837)</span></span>
* <span data-ttu-id="db717-183">@jhaprakash26，Update Set-AzVirtualNetwork.md ( # 13857) </span><span class="sxs-lookup"><span data-stu-id="db717-183">@jhaprakash26, Update Set-AzVirtualNetwork.md (#13857)</span></span>
* <span data-ttu-id="db717-184">Michael Holmes (@MichaelHolmesWP) 、Update New-AzStorageTableStoredAccessPolicy.md ( # 13871) </span><span class="sxs-lookup"><span data-stu-id="db717-184">Michael Holmes (@MichaelHolmesWP), Update New-AzStorageTableStoredAccessPolicy.md (#13871)</span></span>
* <span data-ttu-id="db717-185">Michael James (@mikejwhat) ，可讓 Get-AzLogicAppTriggerHistory 和 Get-AzLogicAppRunAction 傳回超過30個結果 ( # 13846) </span><span class="sxs-lookup"><span data-stu-id="db717-185">Michael James (@mikejwhat), Allow Get-AzLogicAppTriggerHistory and Get-AzLogicAppRunAction to return more than 30 results (#13846)</span></span>
* <span data-ttu-id="db717-186">@Willem-J-an，修正導致 Docker 密碼從 appsettings 中的 Set-azwebapp (位置)  ( # 13866 中移除的 bug) </span><span class="sxs-lookup"><span data-stu-id="db717-186">@Willem-J-an, Fix bug causing Docker Password to be removed from appsettings in Set-AzWebApp(Slot) (#13866)</span></span>

## <a name="530---december-2020"></a><span data-ttu-id="db717-187">5.3.0 - 2020 年 12 月</span><span class="sxs-lookup"><span data-stu-id="db717-187">5.3.0 - December 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="db717-188">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="db717-188">Az.Accounts</span></span>
* <span data-ttu-id="db717-189">已修正 Windows PowerShell 中不會遵守 Http Proxy 的問題 [#13647]</span><span class="sxs-lookup"><span data-stu-id="db717-189">Fixed the issue that Http proxy is not respected in Windows PowerShell [#13647]</span></span>
* <span data-ttu-id="db717-190">已改善所產生模組中長時間執行作業的偵錯記錄</span><span class="sxs-lookup"><span data-stu-id="db717-190">Improved debug log of long running operations in generated modules</span></span>

#### <a name="azautomation"></a><span data-ttu-id="db717-191">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="db717-191">Az.Automation</span></span>
* <span data-ttu-id="db717-192">已修正 'Start-AzAutomationRunbook' 參數無法將 PSObject 所包裝的字串轉換為 JSON 字串的問題 [#13240]</span><span class="sxs-lookup"><span data-stu-id="db717-192">Fixed issue that parameters of 'Start-AzAutomationRunbook' cannot convert PSObject wrapped string to JSON string [#13240]</span></span>
* <span data-ttu-id="db717-193">已修正 New-AzAutomationUpdateManagementAzureQuery Cmdlet 的 Location 完成碼</span><span class="sxs-lookup"><span data-stu-id="db717-193">Fixed location completer for New-AzAutomationUpdateManagementAzureQuery cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="db717-194">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="db717-194">Az.Compute</span></span>
* <span data-ttu-id="db717-195">已將新參數集 'VMParameterSet' 中的新參數 'VM' 新增至 'Get-AzVMDscExtensionStatus' 和 'Get-AzVMDscExtension' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db717-195">New parameter 'VM' in new parameter set 'VMParameterSet' added to 'Get-AzVMDscExtensionStatus' and 'Get-AzVMDscExtension' cmdlets.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="db717-196">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="db717-196">Az.Databricks</span></span>
* <span data-ttu-id="db717-197">已修正可能導致 'New-AzDatabricksVNetPeering' 在完全佈建之前就傳回的問題 (https://github.com/Azure/autorest.powershell/issues/610)</span><span class="sxs-lookup"><span data-stu-id="db717-197">Fixed an issue that may cause 'New-AzDatabricksVNetPeering' to return before it is fully provisioned (https://github.com/Azure/autorest.powershell/issues/610)</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="db717-198">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="db717-198">Az.DataFactory</span></span>
* <span data-ttu-id="db717-199">已修正 SupportsShouldProcess 問題的 'Invoke-AzDataFactoryV2Pipeline' 命令</span><span class="sxs-lookup"><span data-stu-id="db717-199">Fixed the command 'Invoke-AzDataFactoryV2Pipeline' for SupportsShouldProcess issue</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="db717-200">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="db717-200">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="db717-201">已將 StartVMOnConnect 屬性新增至 hostpool。</span><span class="sxs-lookup"><span data-stu-id="db717-201">Added StartVMOnConnect property to hostpool.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="db717-202">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="db717-202">Az.HDInsight</span></span>
* <span data-ttu-id="db717-203">已新增屬性：AzureHDInsightHostInfo 類別中的 Fqdn 和 EffectiveDiskEncryptionKeyUrl。</span><span class="sxs-lookup"><span data-stu-id="db717-203">Added properties: Fqdn and EffectiveDiskEncryptionKeyUrl in the class AzureHDInsightHostInfo.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="db717-204">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="db717-204">Az.KeyVault</span></span>
* <span data-ttu-id="db717-205">已將新的參數 '-AsPlainText' 新增至 'Get-AzKeyVaultSecret'，以直接以純文字傳回祕密 [#13630]</span><span class="sxs-lookup"><span data-stu-id="db717-205">Added a new parameter '-AsPlainText' to 'Get-AzKeyVaultSecret' to directly return the secret in plain text [#13630]</span></span>
* <span data-ttu-id="db717-206">已支援從受管理的 HSM 完整備份中選擇性地還原金鑰 [#13526]</span><span class="sxs-lookup"><span data-stu-id="db717-206">Supported selective restore a key from a managed HSM full backup [#13526]</span></span>
* <span data-ttu-id="db717-207">已修正一些小問題 [#13583] [#13584]</span><span class="sxs-lookup"><span data-stu-id="db717-207">Fixed some minor issues [#13583] [#13584]</span></span>
* <span data-ttu-id="db717-208">已在 SecretManagement 模組中新增遺失的 'Get-Secret' 傳回物件</span><span class="sxs-lookup"><span data-stu-id="db717-208">Added missing return objects of 'Get-Secret' in SecretManagement module</span></span>
* <span data-ttu-id="db717-209">已修正可能導致不使用預設存取原則來建立保存庫的問題 [#13687]</span><span class="sxs-lookup"><span data-stu-id="db717-209">Fixed an issue that may cause vault to be created without default access policy [#13687]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="db717-210">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="db717-210">Az.Kusto</span></span>
* <span data-ttu-id="db717-211">已將 API 版本更新為 2020-09-18。</span><span class="sxs-lookup"><span data-stu-id="db717-211">Updated API version to 2020-09-18.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="db717-212">Az.Network</span><span class="sxs-lookup"><span data-stu-id="db717-212">Az.Network</span></span>
* <span data-ttu-id="db717-213">已修正在 ExpressRouteCircuit 案例中移除對等互連和連線 Cmdlet 時所發生的問題</span><span class="sxs-lookup"><span data-stu-id="db717-213">Fixed issue in remove peering and connection cmdlet for ExpressRouteCircuit scenario</span></span>
    - <span data-ttu-id="db717-214">'Remove-AzExpressRouteCircuitPeeringConfig' 和 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="db717-214">'Remove-AzExpressRouteCircuitPeeringConfig' and 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="db717-215">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="db717-215">Az.PolicyInsights</span></span>
* <span data-ttu-id="db717-216">已針對 Get-AzPolicyState 新增可傳回編頁結果的支援</span><span class="sxs-lookup"><span data-stu-id="db717-216">Added support for returning paginated results for Get-AzPolicyState</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="db717-217">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="db717-217">Az.RecoveryServices</span></span>
* <span data-ttu-id="db717-218">已啟用 SQL 的 softdelete 功能。</span><span class="sxs-lookup"><span data-stu-id="db717-218">Enabled softdelete feature for SQL.</span></span>
* <span data-ttu-id="db717-219">已修正 SQL AG 還原並移除容器名稱檢查。</span><span class="sxs-lookup"><span data-stu-id="db717-219">Fixed SQL AG restore and removed the container name check.</span></span>
* <span data-ttu-id="db717-220">已變更 Azure 檔案儲存體備份項目的容器名稱格式。</span><span class="sxs-lookup"><span data-stu-id="db717-220">Changed container name format for Azure Files backup item.</span></span>
* <span data-ttu-id="db717-221">已新增復原服務保存庫的 CMK 功能支援。</span><span class="sxs-lookup"><span data-stu-id="db717-221">Added CMK feature support for Recovery services vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="db717-222">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="db717-222">Az.Resources</span></span>
* <span data-ttu-id="db717-223">已修正 'New-AzureManagedApplication' 和 'Set-AzureManagedApplication' 中的 NullRef 例外狀況問題。</span><span class="sxs-lookup"><span data-stu-id="db717-223">Fixed a NullRef exception issue in 'New-AzureManagedApplication' and 'Set-AzureManagedApplication'.</span></span>
* <span data-ttu-id="db717-224">已將 Azure Resource Manager SDK 更新為使用最新的 DeploymentScripts 正式發行 API 版本：2020-10-01。</span><span class="sxs-lookup"><span data-stu-id="db717-224">Updated Azure Resource Manager SDK to use latest DeploymentScripts GA api-version: 2020-10-01.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="db717-225">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="db717-225">Az.ServiceFabric</span></span>
* <span data-ttu-id="db717-226">已修正 'Add-AzServiceFabricNodeType'。</span><span class="sxs-lookup"><span data-stu-id="db717-226">Fixed 'Add-AzServiceFabricNodeType'.</span></span> <span data-ttu-id="db717-227">已在建立虛擬機器擴展集之前，將節點類型新增至 Service Fabric 叢集。</span><span class="sxs-lookup"><span data-stu-id="db717-227">Added node type to service fabric cluster before creating virtual machine scale set.</span></span>

#### <a name="azsql"></a><span data-ttu-id="db717-228">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="db717-228">Az.Sql</span></span>
* <span data-ttu-id="db717-229">已修正 'InstanceFailoverGroup' 命令的參數描述。</span><span class="sxs-lookup"><span data-stu-id="db717-229">Fixed parameter description for 'InstanceFailoverGroup' command.</span></span>
* <span data-ttu-id="db717-230">已更新用來從 SQL 資料分類命令的識別碼中擷取 schemaName、tableName 和 columnName 的邏輯。</span><span class="sxs-lookup"><span data-stu-id="db717-230">Updated the logic in which schemaName, tableName and columnName are being extracted from the id of SQL Data Classification commands.</span></span>
* <span data-ttu-id="db717-231">已修正 'Get-AzSqlDatabaseImportExportStatus' 中的 Status 和 StatusMessage 欄位以符合文件</span><span class="sxs-lookup"><span data-stu-id="db717-231">Fixed Status and StatusMessage fields in 'Get-AzSqlDatabaseImportExportStatus' to conform to documentation</span></span>
* <span data-ttu-id="db717-232">已新增 Microsoft 支援作業 (DevOps) 稽核 Cmdlet：Get-AzSqlServerMSSupportAudit、Set-AzSqlServerMSSupportAudit、Remove-AzSqlServerMSSupportAudit</span><span class="sxs-lookup"><span data-stu-id="db717-232">Added Microsoft support operations (DevOps) auditing cmdlets: Get-AzSqlServerMSSupportAudit, Set-AzSqlServerMSSupportAudit, Remove-AzSqlServerMSSupportAudit</span></span>

#### <a name="azstorage"></a><span data-ttu-id="db717-233">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="db717-233">Az.Storage</span></span>
* <span data-ttu-id="db717-234">已支援儲存體帳戶的建立/更新/取得/列出 EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="db717-234">Supported create/update/get/list EncryptionScope of a Storage account</span></span>
    - <span data-ttu-id="db717-235">'New-AzStorageEncryptionScope'</span><span class="sxs-lookup"><span data-stu-id="db717-235">'New-AzStorageEncryptionScope'</span></span>
    - <span data-ttu-id="db717-236">'Update-AzStorageEncryptionScope'</span><span class="sxs-lookup"><span data-stu-id="db717-236">'Update-AzStorageEncryptionScope'</span></span>
    - <span data-ttu-id="db717-237">'Get-AzStorageEncryptionScope'</span><span class="sxs-lookup"><span data-stu-id="db717-237">'Get-AzStorageEncryptionScope'</span></span>
* <span data-ttu-id="db717-238">已支援使用 [加密範圍] 設定來建立容器和上傳 Blob</span><span class="sxs-lookup"><span data-stu-id="db717-238">Supported create container and upload blob with Encryption Scope setting</span></span>
    - <span data-ttu-id="db717-239">'New-AzRmStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="db717-239">'New-AzRmStorageContainer'</span></span>
    - <span data-ttu-id="db717-240">'New-AzStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="db717-240">'New-AzStorageContainer'</span></span>
    - <span data-ttu-id="db717-241">'Set-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="db717-241">'Set-AzStorageBlobContent'</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="db717-242">感謝我們的社群參與者</span><span class="sxs-lookup"><span data-stu-id="db717-242">Thanks to our community contributors</span></span>
* <span data-ttu-id="db717-243">Andreas Wolter (@AndreasWolter)，移除行銷語言，提供更好的篩選範例 (#13671)</span><span class="sxs-lookup"><span data-stu-id="db717-243">Andreas Wolter (@AndreasWolter), removed marketing language, better example filter (#13671)</span></span>
* <span data-ttu-id="db717-244">Tidjani Belmansour (@BelRarr)，更新 Get-AzBillingInvoice.md (#13634)</span><span class="sxs-lookup"><span data-stu-id="db717-244">Tidjani Belmansour (@BelRarr), Update Get-AzBillingInvoice.md (#13634)</span></span>
* <span data-ttu-id="db717-245">David Klempfner (@DavidKlempfner)</span><span class="sxs-lookup"><span data-stu-id="db717-245">David Klempfner (@DavidKlempfner)</span></span>
  * <span data-ttu-id="db717-246">修正拼字錯誤 (#13677)</span><span class="sxs-lookup"><span data-stu-id="db717-246">Fixed spelling mistake (#13677)</span></span>
  * <span data-ttu-id="db717-247">更新 PSMetricNoDetails.cs (#13676)</span><span class="sxs-lookup"><span data-stu-id="db717-247">Update PSMetricNoDetails.cs (#13676)</span></span>
* <span data-ttu-id="db717-248">@kilobyte97，「remove Cmdlet」的錯誤修正以刪除設定 (#13655)</span><span class="sxs-lookup"><span data-stu-id="db717-248">@kilobyte97, bugfix for remove cmdlet to delete config (#13655)</span></span>
* <span data-ttu-id="db717-249">@kongou-ae，更新 Set-AzFirewall.md (#13727)</span><span class="sxs-lookup"><span data-stu-id="db717-249">@kongou-ae, Update Set-AzFirewall.md (#13727)</span></span>
* <span data-ttu-id="db717-250">@MasterKuat，修正文件中標題和程式碼之間的交換 (#13666)</span><span class="sxs-lookup"><span data-stu-id="db717-250">@MasterKuat, Fix swap between title and code in documentation (#13666)</span></span>
* <span data-ttu-id="db717-251">NickT (@nukeulis)，更新 Set-AzContext.md (#13702)</span><span class="sxs-lookup"><span data-stu-id="db717-251">NickT (@nukeulis), Update Set-AzContext.md (#13702)</span></span>
* <span data-ttu-id="db717-252">@PaulHCode，更新 Start-AzJitNetworkAccessPolicy.md - 修正範例以顯示所示範的適當 Cmdlet (#13713)</span><span class="sxs-lookup"><span data-stu-id="db717-252">@PaulHCode, Update Start-AzJitNetworkAccessPolicy.md - Fix the Example to display the proper cmdlet being demonstrated (#13713)</span></span>
* <span data-ttu-id="db717-253">Ryan Borstelmann (@ryanborMSFT)，移除了訂用帳戶識別碼 (#13715)</span><span class="sxs-lookup"><span data-stu-id="db717-253">Ryan Borstelmann (@ryanborMSFT), Removed Subscription ID (#13715)</span></span>
* <span data-ttu-id="db717-254">Shashikant Shakya (@shshakya)，更新 Set-AzSqlDatabase.md (#13674)</span><span class="sxs-lookup"><span data-stu-id="db717-254">Shashikant Shakya (@shshakya), Update Set-AzSqlDatabase.md (#13674)</span></span>
* <span data-ttu-id="db717-255">Sebastian Olsen (@Spacebjorn)，更新 Get-AzRecoveryServicesBackupItem.md (#13719)</span><span class="sxs-lookup"><span data-stu-id="db717-255">Sebastian Olsen (@Spacebjorn), Update Get-AzRecoveryServicesBackupItem.md (#13719)</span></span>

## <a name="520---december-2020"></a><span data-ttu-id="db717-256">5.2.0 - 2020 年 12 月</span><span class="sxs-lookup"><span data-stu-id="db717-256">5.2.0 - December 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="db717-257">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="db717-257">Az.Accounts</span></span>
* <span data-ttu-id="db717-258">如果無法從基礎程式庫取得，則會受控以剖析原始權杖中的 ExpiresOn 時間</span><span class="sxs-lookup"><span data-stu-id="db717-258">Managed to parse ExpiresOn time from raw token if could not get from underlying library</span></span>
* <span data-ttu-id="db717-259">已改善互動式驗證無法使用時的警告訊息</span><span class="sxs-lookup"><span data-stu-id="db717-259">Improved warning message if Interactive authentication is unavailable</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="db717-260">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="db717-260">Az.ApiManagement</span></span>
* <span data-ttu-id="db717-261">[重大變更] 根據預設，'New-AzApiManagementProduct' 沒有訂用帳戶限制。</span><span class="sxs-lookup"><span data-stu-id="db717-261">[Breaking change] 'New-AzApiManagementProduct' by default has no subscription limit.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="db717-262">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="db717-262">Az.Compute</span></span>
* <span data-ttu-id="db717-263">已編輯 Get-AzVm，以在檢查節流之前，先依據 '-Name' 進行篩選，因為資源太多。</span><span class="sxs-lookup"><span data-stu-id="db717-263">Edited Get-AzVm to filter by '-Name' prior to checking for throttling due to too many resources.</span></span> 
* <span data-ttu-id="db717-264">新的 Cmdlet 'Start-AzVmssRollingExtensionUpgrade'。</span><span class="sxs-lookup"><span data-stu-id="db717-264">New cmdlet 'Start-AzVmssRollingExtensionUpgrade'.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="db717-265">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="db717-265">Az.ContainerRegistry</span></span>
* <span data-ttu-id="db717-266">支援 'Get-AzContainerRegistryUsage' 的管線輸入參數 'Name' 與管線輸入中的值 [#13605]</span><span class="sxs-lookup"><span data-stu-id="db717-266">Supported parameter 'Name' for and value from pipeline input for 'Get-AzContainerRegistryUsage' [#13605]</span></span>
* <span data-ttu-id="db717-267">改善 'Connect-AzContainerRegistry' 的例外狀況</span><span class="sxs-lookup"><span data-stu-id="db717-267">Polished exceptions for 'Connect-AzContainerRegistry'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="db717-268">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="db717-268">Az.DataFactory</span></span>
* <span data-ttu-id="db717-269">已將 ADF .Net SDK 版本更新為 4.13.0</span><span class="sxs-lookup"><span data-stu-id="db717-269">Updated ADF .Net SDK version to 4.13.0</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="db717-270">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="db717-270">Az.HealthcareApis</span></span>
* <span data-ttu-id="db717-271">已新增客戶管理金鑰的支援</span><span class="sxs-lookup"><span data-stu-id="db717-271">Added support for customer managed keys</span></span>

#### <a name="aziothub"></a><span data-ttu-id="db717-272">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="db717-272">Az.IotHub</span></span>
* <span data-ttu-id="db717-273">已修正 SAS 權杖的問題。</span><span class="sxs-lookup"><span data-stu-id="db717-273">Fixed an issue of SAS token.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="db717-274">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="db717-274">Az.KeyVault</span></span>
* <span data-ttu-id="db717-275">在設定金鑰保存庫存取原則時，支援 'all' 做為選項</span><span class="sxs-lookup"><span data-stu-id="db717-275">Supported 'all' as an option when setting key vault access policies</span></span>
* <span data-ttu-id="db717-276">支援 SecretManagement 模組的新版本 [#13366]</span><span class="sxs-lookup"><span data-stu-id="db717-276">Supported new version of SecretManagement module [#13366]</span></span>
* <span data-ttu-id="db717-277">支援 SecretManagementModule 中 'SecretValue' 的 ByteArray、String、PSCredential 和 Hashtable [#12190]</span><span class="sxs-lookup"><span data-stu-id="db717-277">Supported ByteArray, String, PSCredential and Hashtable for 'SecretValue' in SecretManagementModule [#12190]</span></span>
* <span data-ttu-id="db717-278">[重大變更] 重新設計與受控 HSM 相關 Cmdlet 的 API 介面。</span><span class="sxs-lookup"><span data-stu-id="db717-278">[Breaking change] redesigned the API surface of cmdlets related to managed HSM.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="db717-279">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="db717-279">Az.Monitor</span></span>
* <span data-ttu-id="db717-280">已將 'New-AzAutoscaleProfile' 的參數 'Rule' 變更為接受空白清單。</span><span class="sxs-lookup"><span data-stu-id="db717-280">Changed parameter 'Rule' of 'New-AzAutoscaleProfile' to accept empty list.</span></span> <span data-ttu-id="db717-281">[#12903]</span><span class="sxs-lookup"><span data-stu-id="db717-281">[#12903]</span></span>
* <span data-ttu-id="db717-282">已新增新的 Cmdlet，以支援建立更有彈性的診斷設定：</span><span class="sxs-lookup"><span data-stu-id="db717-282">Added new cmdlets to support creating diagnostic settings more flexible:</span></span>
    * <span data-ttu-id="db717-283">'Get-AzDiagnosticSettingCategory'</span><span class="sxs-lookup"><span data-stu-id="db717-283">'Get-AzDiagnosticSettingCategory'</span></span>
    * <span data-ttu-id="db717-284">'New-AzDiagnosticSetting'</span><span class="sxs-lookup"><span data-stu-id="db717-284">'New-AzDiagnosticSetting'</span></span>
    * <span data-ttu-id="db717-285">'New-AzDiagnosticDetailSetting'</span><span class="sxs-lookup"><span data-stu-id="db717-285">'New-AzDiagnosticDetailSetting'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="db717-286">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="db717-286">Az.RecoveryServices</span></span>
* <span data-ttu-id="db717-287">將說明文字和參數集名稱變更為 'Restore-AzRecoveryServicesBackupItem' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db717-287">Made help text and parameter set name changes to 'Restore-AzRecoveryServicesBackupItem' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="db717-288">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="db717-288">Az.Resources</span></span>
* <span data-ttu-id="db717-289">已將 '-Tag' 參數支援新增至 'Set-AzTemplateSpec' 和 'New-AzTemplateSpec'</span><span class="sxs-lookup"><span data-stu-id="db717-289">Added '-Tag' parameter support to 'Set-AzTemplateSpec' and 'New-AzTemplateSpec'</span></span>
* <span data-ttu-id="db717-290">已將標籤顯示支援新增至範本規格的預設格式器</span><span class="sxs-lookup"><span data-stu-id="db717-290">Added Tag display support to default formatter for Template Specs</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="db717-291">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="db717-291">Az.ServiceFabric</span></span>
* <span data-ttu-id="db717-292">已將範例新增至具有 SettingsSectionDescription param 的 'Set-AzServiceFabricSetting'</span><span class="sxs-lookup"><span data-stu-id="db717-292">Added example to 'Set-AzServiceFabricSetting' with SettingsSectionDescription param</span></span>
* <span data-ttu-id="db717-293">已將應用程式相關的 Cmdlet 更新為呼叫支援僅適用於 ARM 部署的資源</span><span class="sxs-lookup"><span data-stu-id="db717-293">Updated application related cmdlets to call out that support is only for ARM deployed resources</span></span>
* <span data-ttu-id="db717-294">標示為已淘汰的叢集憑證 Cmdlet 'Add-AzureRmServiceFabricClusterCertificate' 和 'Remove-AzureRmServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="db717-294">Marked for deprecation cluster cert cmdlets 'Add-AzureRmServiceFabricClusterCertificate' and 'Remove-AzureRmServiceFabricClusterCertificate'</span></span>

#### <a name="azsql"></a><span data-ttu-id="db717-295">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="db717-295">Az.Sql</span></span>
* <span data-ttu-id="db717-296">已將 SecondaryType 新增至下列內容：</span><span class="sxs-lookup"><span data-stu-id="db717-296">Added SecondaryType to the following:</span></span> 
    - <span data-ttu-id="db717-297">'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="db717-297">'New-AzSqlDatabase'</span></span>
    - <span data-ttu-id="db717-298">'Set-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="db717-298">'Set-AzSqlDatabase'</span></span>
    - <span data-ttu-id="db717-299">'New-AzSqlDatabaseSecondary'</span><span class="sxs-lookup"><span data-stu-id="db717-299">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="db717-300">已將 HighAvailabilityReplicaCount 新增至下列內容：</span><span class="sxs-lookup"><span data-stu-id="db717-300">Added HighAvailabilityReplicaCount to the following:</span></span> 
    - <span data-ttu-id="db717-301">'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="db717-301">'New-AzSqlDatabase'</span></span>
    - <span data-ttu-id="db717-302">'Set-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="db717-302">'Set-AzSqlDatabase'</span></span>
* <span data-ttu-id="db717-303">使 ReadReplicaCount 成為下列內容中的 HighAvailabilityReplicaCount 別名：</span><span class="sxs-lookup"><span data-stu-id="db717-303">Made ReadReplicaCount an alias of HighAvailabilityReplicaCount in the following:</span></span> 
    - <span data-ttu-id="db717-304">'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="db717-304">'New-AzSqlDatabase'</span></span>
    - <span data-ttu-id="db717-305">'Set-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="db717-305">'Set-AzSqlDatabase'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="db717-306">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="db717-306">Az.Storage</span></span>
* <span data-ttu-id="db717-307">支援上傳 Azure 檔案大小上限至 4 TiB</span><span class="sxs-lookup"><span data-stu-id="db717-307">Supported upload Azure File size up to 4 TiB</span></span>
    - <span data-ttu-id="db717-308">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="db717-308">'Set-AzStorageFileContent'</span></span>
* <span data-ttu-id="db717-309">已將 Azure.Storage.Blobs 升級至 12.7.0</span><span class="sxs-lookup"><span data-stu-id="db717-309">Upgraded Azure.Storage.Blobs to 12.7.0</span></span>
* <span data-ttu-id="db717-310">已將 Azure.Storage.Files.Shares 升級至 12.5.0</span><span class="sxs-lookup"><span data-stu-id="db717-310">Upgraded Azure.Storage.Files.Shares to 12.5.0</span></span>
* <span data-ttu-id="db717-311">已將 Azure.Storage.Files.DataLake 升級至 12.5.0</span><span class="sxs-lookup"><span data-stu-id="db717-311">Upgraded Azure.Storage.Files.DataLake to 12.5.0</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="db717-312">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="db717-312">Az.StorageSync</span></span>
* <span data-ttu-id="db717-313">已新增具有下載原則和本機快取模式的同步階層處理原則功能</span><span class="sxs-lookup"><span data-stu-id="db717-313">Added Sync tiering policy feature with download policy and local cache mode</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="db717-314">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="db717-314">Az.Websites</span></span>
* <span data-ttu-id="db717-315">防止重複存取限制規則</span><span class="sxs-lookup"><span data-stu-id="db717-315">Prevent duplicate access restriction rules</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="db717-316">感謝我們的社群參與者</span><span class="sxs-lookup"><span data-stu-id="db717-316">Thanks to our community contributors</span></span>
* <span data-ttu-id="db717-317">Andrew Dawson (@dawsonar802)，升級 Get-AzKeyVaultCertificate.md - 取得憑證並將其另存為 pfx 區段，以使用 PowerShell Core (#13557)</span><span class="sxs-lookup"><span data-stu-id="db717-317">Andrew Dawson (@dawsonar802), Update Get-AzKeyVaultCertificate.md - Get cert and save it as pfx section to work with PowerShell Core (#13557)</span></span>
* <span data-ttu-id="db717-318">@iviark，醫療保健 APIs Powershell BYOK 更新 (#13518)</span><span class="sxs-lookup"><span data-stu-id="db717-318">@iviark, Healthcare APIs Powershell BYOK Updates (#13518)</span></span>
* <span data-ttu-id="db717-319">John Duckmanton (@johnduckmanton)，修正 TagPatchOperation 的拼寫 (#13508)</span><span class="sxs-lookup"><span data-stu-id="db717-319">John Duckmanton (@johnduckmanton), Correct spelling of TagPatchOperation (#13508)</span></span>
* <span data-ttu-id="db717-320">Michael James (@mikejwhat)</span><span class="sxs-lookup"><span data-stu-id="db717-320">Michael James (@mikejwhat)</span></span>
  * <span data-ttu-id="db717-321">Get-AzLogicAppRunHistory Help Tidy (#13513)</span><span class="sxs-lookup"><span data-stu-id="db717-321">Get-AzLogicAppRunHistory Help Tidy (#13513)</span></span>
* <span data-ttu-id="db717-322">Richard de Zwart (@mountain65)</span><span class="sxs-lookup"><span data-stu-id="db717-322">Richard de Zwart (@mountain65)</span></span>
  * <span data-ttu-id="db717-323">更新 Update-AzAppConfigurationStore.md (#13485)</span><span class="sxs-lookup"><span data-stu-id="db717-323">Update Update-AzAppConfigurationStore.md (#13485)</span></span>
  * <span data-ttu-id="db717-324">更新 New-AzCosmosDBAccount.md (#13490)</span><span class="sxs-lookup"><span data-stu-id="db717-324">Update New-AzCosmosDBAccount.md (#13490)</span></span>
* <span data-ttu-id="db717-325">@SteppingRazor，New-AzApiManagementProduct：將 SubscriptionsLimit 參數的預設值變更為 None (#13457)</span><span class="sxs-lookup"><span data-stu-id="db717-325">@SteppingRazor, New-AzApiManagementProduct: Change SubscriptionsLimit parameter default value to None (#13457)</span></span>
* <span data-ttu-id="db717-326">Steve Burkett (@SteveBurkettNZ)，修正範例中 WorkspaceResourceId 參數的打字錯誤 (#13589)</span><span class="sxs-lookup"><span data-stu-id="db717-326">Steve Burkett (@SteveBurkettNZ), Fix Typo for WorkspaceResourceId parameter in example (#13589)</span></span>

## <a name="510---november-2020"></a><span data-ttu-id="db717-327">5.1.0 - 2020 年 11 月</span><span class="sxs-lookup"><span data-stu-id="db717-327">5.1.0 - November 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="db717-328">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="db717-328">Az.Accounts</span></span>
* <span data-ttu-id="db717-329">已修正使用 ''Connect-AzAccount -DeviceCode' 時，可能不會遵守 TenantId 的問題 [#13477]</span><span class="sxs-lookup"><span data-stu-id="db717-329">Fixed an issue that TenantId may be not respected if using 'Connect-AzAccount -DeviceCode'[#13477]</span></span>
* <span data-ttu-id="db717-330">已新增 Cmdlet 'Get-AzAccessToken'</span><span class="sxs-lookup"><span data-stu-id="db717-330">Added new cmdlet 'Get-AzAccessToken'</span></span>
* <span data-ttu-id="db717-331">已修正無法存取使用者設定檔路徑時發生錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="db717-331">Fixed an issue that error happens if user profile path is inaccessible</span></span>
* <span data-ttu-id="db717-332">已修正 Connect-AzAccount 期間發生 Write-Object 錯誤的問題 [#13419]</span><span class="sxs-lookup"><span data-stu-id="db717-332">Fixed an issue causing Write-Object error during Connect-AzAccount [#13419]</span></span>
* <span data-ttu-id="db717-333">已將參數 'ContainerRegistryEndpointSuffix' 新增至：'Add-AzEnvironment'、'Set-AzEnvironment'</span><span class="sxs-lookup"><span data-stu-id="db717-333">Added parameter 'ContainerRegistryEndpointSuffix' to: 'Add-AzEnvironment', 'Set-AzEnvironment'</span></span> 
* <span data-ttu-id="db717-334">支援點擊 <kbd>CTRL</kbd>+<kbd>C</kbd> 來中斷登入</span><span class="sxs-lookup"><span data-stu-id="db717-334">Supported interrupting login by hitting <kbd>CTRL</kbd>+<kbd>C</kbd></span></span>
* <span data-ttu-id="db717-335">已修正導致 'Connect-AzAccount -KeyVaultAccessToken' 無法運作的問題 [#13127]</span><span class="sxs-lookup"><span data-stu-id="db717-335">Fixed an issue causing 'Connect-AzAccount -KeyVaultAccessToken' not working [#13127]</span></span>
* <span data-ttu-id="db717-336">已修正 'Invoke-AzRestMethod' 中 Null 參考和方法不區分大小寫的問題</span><span class="sxs-lookup"><span data-stu-id="db717-336">Fixed null reference and method case insensitive in 'Invoke-AzRestMethod'</span></span>

#### <a name="azaks"></a><span data-ttu-id="db717-337">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="db717-337">Az.Aks</span></span>
* <span data-ttu-id="db717-338">已修正使用者無法使用服務主體建立新 Kubernetes 叢集的問題。</span><span class="sxs-lookup"><span data-stu-id="db717-338">Fixed the issue that user cannot use service principal to create a new Kubernetes cluster.</span></span> <span data-ttu-id="db717-339">[#13012]</span><span class="sxs-lookup"><span data-stu-id="db717-339">[#13012]</span></span>

#### <a name="azappconfiguration"></a><span data-ttu-id="db717-340">Az.AppConfiguration</span><span class="sxs-lookup"><span data-stu-id="db717-340">Az.AppConfiguration</span></span>
* <span data-ttu-id="db717-341">'Az.AppConfiguration' 模組的正式推出</span><span class="sxs-lookup"><span data-stu-id="db717-341">General availability of 'Az.AppConfiguration' module</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="db717-342">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="db717-342">Az.DataFactory</span></span>
* <span data-ttu-id="db717-343">已改善 'New-AzDataFactoryV2LinkedServiceEncryptedCredential' 命令的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="db717-343">Improved error message of 'New-AzDataFactoryV2LinkedServiceEncryptedCredential' command</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="db717-344">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="db717-344">Az.DataLakeStore</span></span>
* <span data-ttu-id="db717-345">已將 ADLS 資料平面 SDK 更新為 1.2.4-alpha。</span><span class="sxs-lookup"><span data-stu-id="db717-345">Updated ADLS dataplane SDK to 1.2.4-alpha.</span></span> <span data-ttu-id="db717-346">變更： https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-124-alpha</span><span class="sxs-lookup"><span data-stu-id="db717-346">Changes:https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-124-alpha</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="db717-347">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="db717-347">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="db717-348">已新增 MSIX Package Cmdlet 和更新應用程式 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db717-348">Added new MSIX Package cmdlets and updated Applications cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="db717-349">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="db717-349">Az.EventHub</span></span>
* <span data-ttu-id="db717-350">已修正 EventHub 叢集沒有標記時的叢集命令</span><span class="sxs-lookup"><span data-stu-id="db717-350">Fixed Cluster commands for EventHub cluster without tags</span></span>
* <span data-ttu-id="db717-351">已更新 AzEventHubGeoDRConfiguration 的 PartnerNamespace 命令解說文字</span><span class="sxs-lookup"><span data-stu-id="db717-351">Updated help text for PartnerNamespace of AzEventHubGeoDRConfiguration commands</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="db717-352">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="db717-352">Az.HDInsight</span></span>
* <span data-ttu-id="db717-353">已將 'ResourceProviderConnection' 和 'PrivateLink' 參數新增至 'New-AzHDInsightCluster' Cmdlet 以支援轉送輸出和私人連結功能</span><span class="sxs-lookup"><span data-stu-id="db717-353">Add parameters 'ResourceProviderConnection' and 'PrivateLink' to cmdlet 'New-AzHDInsightCluster' to support relay outbound and private link feature</span></span>
* <span data-ttu-id="db717-354">已將 'AmbariDatabase' 參數新增至 'New-AzHDInsightCluster' Cmdlet，以支援自訂 Ambari 資料庫功能</span><span class="sxs-lookup"><span data-stu-id="db717-354">Add parameter 'AmbariDatabase' to cmdlet 'New-AzHDInsightCluster' to support custom Ambari database feature</span></span>
* <span data-ttu-id="db717-355">將接受值 'AmbariDatabase' 新增至 'Add-AzHDInsightMetastore' Cmdlet 的 'MetastoreType' 參數</span><span class="sxs-lookup"><span data-stu-id="db717-355">Add accept value 'AmbariDatabase' to the parameter 'MetastoreType' of the cmdlet 'Add-AzHDInsightMetastore'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="db717-356">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="db717-356">Az.IotHub</span></span>
* <span data-ttu-id="db717-357">允許在 IoT 中樞建立 Cmdlet 中使用標記。</span><span class="sxs-lookup"><span data-stu-id="db717-357">Allowed tags in IoT Hub create cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="db717-358">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="db717-358">Az.KeyVault</span></span>
* <span data-ttu-id="db717-359">支援更新金鑰保存庫標記</span><span class="sxs-lookup"><span data-stu-id="db717-359">Supported updating key vault tag</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="db717-360">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="db717-360">Az.LogicApp</span></span>
* <span data-ttu-id="db717-361">已修正 Get-AzLogicAppRunHistory 只會取得結果第一頁的問題</span><span class="sxs-lookup"><span data-stu-id="db717-361">Fixed for Get-AzLogicAppRunHistory only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="db717-362">Az.Network</span><span class="sxs-lookup"><span data-stu-id="db717-362">Az.Network</span></span>
* <span data-ttu-id="db717-363">已更新下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-363">Updated below cmdlet</span></span> 
    - <span data-ttu-id="db717-364">'New-AzLoadBalancerFrontendIpConfigCommand'、'Set-AzLoadBalancerFrontendIpConfigCommand'、'Add-AzLoadBalancerFrontendIpConfigCommand'：</span><span class="sxs-lookup"><span data-stu-id="db717-364">'New-AzLoadBalancerFrontendIpConfigCommand', 'Set-AzLoadBalancerFrontendIpConfigCommand', 'Add-AzLoadBalancerFrontendIpConfigCommand':</span></span>
        - <span data-ttu-id="db717-365">已新增 PublicIpAddressPrefix 屬性</span><span class="sxs-lookup"><span data-stu-id="db717-365">Added PublicIpAddressPrefix property</span></span>
        - <span data-ttu-id="db717-366">已新增 PublicIpAddressPrefixId 屬性</span><span class="sxs-lookup"><span data-stu-id="db717-366">Added PublicIpAddressPrefixId property</span></span>
* <span data-ttu-id="db717-367">已將新屬性新增至下列 Cmdlet，以允許進行全域負載平衡</span><span class="sxs-lookup"><span data-stu-id="db717-367">Added new properties to the following cmdlets to allow for global load balancing</span></span>
    - <span data-ttu-id="db717-368">'New-AzLoadBalancer'：</span><span class="sxs-lookup"><span data-stu-id="db717-368">'New-AzLoadBalancer':</span></span>
        - <span data-ttu-id="db717-369">已新增 SKU 層屬性</span><span class="sxs-lookup"><span data-stu-id="db717-369">Added Sku Tier property</span></span>
    - <span data-ttu-id="db717-370">'New-AzPuplicIpAddress'：</span><span class="sxs-lookup"><span data-stu-id="db717-370">'New-AzPuplicIpAddress':</span></span>
        - <span data-ttu-id="db717-371">已新增 SKU 層屬性</span><span class="sxs-lookup"><span data-stu-id="db717-371">Added Sku Tier property</span></span>
    - <span data-ttu-id="db717-372">'New-AzPublicIpPrefix'：</span><span class="sxs-lookup"><span data-stu-id="db717-372">'New-AzPublicIpPrefix':</span></span>
        - <span data-ttu-id="db717-373">已新增 SKU 層屬性</span><span class="sxs-lookup"><span data-stu-id="db717-373">Added Sku Tier property</span></span>
    - <span data-ttu-id="db717-374">'New-AzLoadBalancerBackendAddressConfig'：</span><span class="sxs-lookup"><span data-stu-id="db717-374">'New-AzLoadBalancerBackendAddressConfig':</span></span>
        - <span data-ttu-id="db717-375">已新增 LoadBalancerFrontendIPConfigurationId 屬性</span><span class="sxs-lookup"><span data-stu-id="db717-375">Added LoadBalancerFrontendIPConfigurationId property</span></span>
* <span data-ttu-id="db717-376">已更新規劃來取代下列 Cmdlet 的警告   -'New-AzVirtualHubRoute'   -'New-AzVirtualHubRouteTable'   -'Add-AzVirtualHubRoute'   -'Add-AzVirtualHubRouteTable'   -'Get-AzVirtualHubRouteTable'   -'Remove-AzVirtualHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="db717-376">Updated planning to deprecate warnings for the following cmdlets   -'New-AzVirtualHubRoute'   -'New-AzVirtualHubRouteTable'   -'Add-AzVirtualHubRoute'   -'Add-AzVirtualHubRouteTable'   -'Get-AzVirtualHubRouteTable'   -'Remove-AzVirtualHubRouteTable'</span></span>
* <span data-ttu-id="db717-377">已新增規劃來取代下列 Cmdlet 的 'RouteTable' 引數警告   -'New-AzVirtualHub'   -'Set-AzVirtualHub'   -'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="db717-377">Added planning to deprecate warnings on the argument 'RouteTable' for the following cmdlets   -'New-AzVirtualHub'   -'Set-AzVirtualHub'   -'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="db717-378">已將 '-MinScaleUnits' 和 '-MaxScaleUnits' 引數設為 'Set-AzExpressRouteGateway' 中的選擇性項目</span><span class="sxs-lookup"><span data-stu-id="db717-378">Made arguments '-MinScaleUnits' and '-MaxScaleUnits' optional in 'Set-AzExpressRouteGateway'</span></span>
* <span data-ttu-id="db717-379">已新增 Cmdlet 來支援應用程式閘道的相互驗證和 SSL 設定檔</span><span class="sxs-lookup"><span data-stu-id="db717-379">Added new cmdlets to support Mutual Authentication and SSL Profiles on Application Gateway</span></span>
    - <span data-ttu-id="db717-380">'Get-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="db717-380">'Get-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="db717-381">'New-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="db717-381">'New-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="db717-382">'Remove-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="db717-382">'Remove-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="db717-383">'Set-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="db717-383">'Set-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="db717-384">'Add-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="db717-384">'Add-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="db717-385">'Get-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="db717-385">'Get-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="db717-386">'New-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="db717-386">'New-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="db717-387">'Remove-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="db717-387">'Remove-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="db717-388">'Set-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="db717-388">'Set-AzApplicationGatewayTrustedClientCertificate'</span></span>
    - <span data-ttu-id="db717-389">'Add-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="db717-389">'Add-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="db717-390">'Get-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="db717-390">'Get-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="db717-391">'New-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="db717-391">'New-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="db717-392">'Remove-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="db717-392">'Remove-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="db717-393">'Set-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="db717-393">'Set-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="db717-394">'Get-AzApplicationGatewaySslProfilePolicy'</span><span class="sxs-lookup"><span data-stu-id="db717-394">'Get-AzApplicationGatewaySslProfilePolicy'</span></span>
    - <span data-ttu-id="db717-395">'Remove-AzApplicationGatewaySslProfilePolicy'</span><span class="sxs-lookup"><span data-stu-id="db717-395">'Remove-AzApplicationGatewaySslProfilePolicy'</span></span>
    - <span data-ttu-id="db717-396">'Set-AzApplicationGatewaySslProfilePolicy'</span><span class="sxs-lookup"><span data-stu-id="db717-396">'Set-AzApplicationGatewaySslProfilePolicy'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="db717-397">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="db717-397">Az.RecoveryServices</span></span>
* <span data-ttu-id="db717-398">指定原則 BackupTime 的格式為 UTC。</span><span class="sxs-lookup"><span data-stu-id="db717-398">Specifying policy BackupTime is in UTC.</span></span>
* <span data-ttu-id="db717-399">修改 Get-AzRecoveryServicesBackupJobDetails Cmdlet 中的中斷性變更警告。</span><span class="sxs-lookup"><span data-stu-id="db717-399">Modifying breaking change warning in Get-AzRecoveryServicesBackupJobDetails cmdlet.</span></span>
* <span data-ttu-id="db717-400">更新 Set-AzRecoveryServicesBackupProtectionPolicy Cmdlet 的範例指令碼解說文字。</span><span class="sxs-lookup"><span data-stu-id="db717-400">Updating sample script help text for Set-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="db717-401">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="db717-401">Az.Resources</span></span>
* <span data-ttu-id="db717-402">已修正 What-If 會顯示兩個大小寫不同的資源群組範圍的問題</span><span class="sxs-lookup"><span data-stu-id="db717-402">Fixed an issue where What-If shows two resource group scopes with different casing</span></span>
* <span data-ttu-id="db717-403">已將 'Export-AzResourceGroup' 更新為使用 SDK。</span><span class="sxs-lookup"><span data-stu-id="db717-403">Updated 'Export-AzResourceGroup' to use the SDK.</span></span>
* <span data-ttu-id="db717-404">已將文化特性資訊新增至 parse 方法</span><span class="sxs-lookup"><span data-stu-id="db717-404">Added culture info to parse methods</span></span>

#### <a name="azsql"></a><span data-ttu-id="db717-405">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="db717-405">Az.Sql</span></span>
* <span data-ttu-id="db717-406">已修正 Set-AzSqlDatabaseAudit 不支援超大規模資料庫資料庫和資料庫版本無法判斷的問題</span><span class="sxs-lookup"><span data-stu-id="db717-406">Fixed issues where Set-AzSqlDatabaseAudit were not support Hyperscale database and database edition cannot be determined</span></span>
* <span data-ttu-id="db717-407">已將 MaintenanceConfigurationId 新增至 New-AzSqlInstance' 和 'Set-AzSqlInstance'</span><span class="sxs-lookup"><span data-stu-id="db717-407">Added MaintenanceConfigurationId to 'New-AzSqlInstance' and 'Set-AzSqlInstance'</span></span>
* <span data-ttu-id="db717-408">已修正 GetAzureSqlDatabaseReplicationLink.cs 中的錯誤 (bug)：PartnerServerName 參數會以值進行檢查，而非索引鍵</span><span class="sxs-lookup"><span data-stu-id="db717-408">Fixed a bug in GetAzureSqlDatabaseReplicationLink.cs where PartnerServerName parameter was being checked for by value instead of key</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="db717-409">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="db717-409">Az.Websites</span></span>
* <span data-ttu-id="db717-410">新增最新存取限制功能的支援：ServiceTag、multi-ip 和 http-headers</span><span class="sxs-lookup"><span data-stu-id="db717-410">Added support for new access restriction features: ServiceTag, multi-ip and http-headers</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="db717-411">感謝我們的社群參與者</span><span class="sxs-lookup"><span data-stu-id="db717-411">Thanks to our community contributors</span></span>
* <span data-ttu-id="db717-412">John Q. Martin (@johnmart82)，新增防火牆必要條件資訊 (#13385)</span><span class="sxs-lookup"><span data-stu-id="db717-412">John Q. Martin (@johnmart82), Adding firewall prerequisite information (#13385)</span></span>
* <span data-ttu-id="db717-413">Manikandan Duraisamy (@madurais-msft)，修正 PublicSubnetName 引數 (#13417)</span><span class="sxs-lookup"><span data-stu-id="db717-413">Manikandan Duraisamy (@madurais-msft), Corrected the PublicSubnetName argument (#13417)</span></span>
* <span data-ttu-id="db717-414">@mahortas，更新 -HostNames 參數值 (#13349)</span><span class="sxs-lookup"><span data-stu-id="db717-414">@mahortas, Update for -HostNames parameter values (#13349)</span></span>
* <span data-ttu-id="db717-415">@MariachiForHire，新增支援的 TrafficAnalyticsInterval 值 (#13304)</span><span class="sxs-lookup"><span data-stu-id="db717-415">@MariachiForHire, added supported TrafficAnalyticsInterval values (#13304)</span></span>
* <span data-ttu-id="db717-416">Michael James (@mikejwhat)，允許 Get-AzLogicAppRunHistory 傳回超過 30 個項目 (#13393)</span><span class="sxs-lookup"><span data-stu-id="db717-416">Michael James (@mikejwhat), Allow Get-AzLogicAppRunHistory to return more than 30 entries (#13393)</span></span>
* <span data-ttu-id="db717-417">Shashikant Shakya (@shshakya)，更新 Restore-AzSqlInstanceDatabase.md (#13404)</span><span class="sxs-lookup"><span data-stu-id="db717-417">Shashikant Shakya (@shshakya), Update Restore-AzSqlInstanceDatabase.md (#13404)</span></span>

## <a name="500---october-2020"></a><span data-ttu-id="db717-418">5.0.0 - 2020 年 10 月</span><span class="sxs-lookup"><span data-stu-id="db717-418">5.0.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="db717-419">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="db717-419">Az.Accounts</span></span>
* <span data-ttu-id="db717-420">[中斷性變更] 已移除 'Get-AzProfile' 和 'Select-AzProfile'</span><span class="sxs-lookup"><span data-stu-id="db717-420">[Breaking Change] Removed 'Get-AzProfile' and 'Select-AzProfile'</span></span>
* <span data-ttu-id="db717-421">已將 Azure Directory 驗證程式庫取代為 Microsoft Authentication Library (MSAL)</span><span class="sxs-lookup"><span data-stu-id="db717-421">Replaced Azure Directory Authentication Library with Microsoft Authentication Library(MSAL)</span></span>

#### <a name="azaks"></a><span data-ttu-id="db717-422">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="db717-422">Az.Aks</span></span>
* <span data-ttu-id="db717-423">[中斷性變更]已移除 'New-AzAksCluster' 和 'Set-AzAksCluster' 中的參數別名 'ClientIdAndSecret'。</span><span class="sxs-lookup"><span data-stu-id="db717-423">[Breaking Change] Removed parameter alias 'ClientIdAndSecret' in 'New-AzAksCluster' and 'Set-AzAksCluster'.</span></span>
* <span data-ttu-id="db717-424">[中斷性變更] 已將 'New-AzAksCluster' 中 'NodeVmSetType' 的預設值從 'AvailabilitySet' 變更為 'VirtualMachineScaleSets。</span><span class="sxs-lookup"><span data-stu-id="db717-424">[Breaking Change] Changed the default value of 'NodeVmSetType' in 'New-AzAksCluster' from 'AvailabilitySet' to 'VirtualMachineScaleSets'.</span></span>
* <span data-ttu-id="db717-425">[中斷性變更] 已將 'New-AzAksCluster' 中 'NetworkPlugin' 的預設值從 'None' 變更為 'azure'。</span><span class="sxs-lookup"><span data-stu-id="db717-425">[Breaking Change] Changed the default value of 'NetworkPlugin' in 'New-AzAksCluster' from 'None' to 'azure'.</span></span>
* <span data-ttu-id="db717-426">[中斷性變更] 已移除 'New-AzAksCluster' 中的參數 'NodeOsType'，因為其僅支援一個值 Linux。</span><span class="sxs-lookup"><span data-stu-id="db717-426">[Breaking Change] Removed parameter 'NodeOsType' in 'New-AzAksCluster' as it supports only one value Linux.</span></span>

#### <a name="azbilling"></a><span data-ttu-id="db717-427">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="db717-427">Az.Billing</span></span>
* <span data-ttu-id="db717-428">已新增 'Get-AzBillingAccount' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-428">Added 'Get-AzBillingAccount' cmdlet</span></span>
* <span data-ttu-id="db717-429">已新增 'Get-AzBillingProfile' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-429">Added 'Get-AzBillingProfile' cmdlet</span></span>
* <span data-ttu-id="db717-430">已新增 'Get-AzInvoiceSection' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-430">Added 'Get-AzInvoiceSection' cmdlet</span></span>
* <span data-ttu-id="db717-431">已在 'Get-AzBillingInvoice' Cmdlet 中新增參數</span><span class="sxs-lookup"><span data-stu-id="db717-431">Added new parameters in 'Get-AzBillingInvoice' cmdlet</span></span>
* <span data-ttu-id="db717-432">已從 Get-AzBillingInvoice Cmdlet 的回應中移除屬性 DownloadUrlExpiry、Type、BillingPeriodNames</span><span class="sxs-lookup"><span data-stu-id="db717-432">Removed properties DownloadUrlExpiry, Type, BillingPeriodNames from the response of Get-AzBillingInvoice cmdlet</span></span>

#### <a name="azcdn"></a><span data-ttu-id="db717-433">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="db717-433">Az.Cdn</span></span>
* <span data-ttu-id="db717-434">已新增 Cmdlet 來支援多個來源和私人連結功能</span><span class="sxs-lookup"><span data-stu-id="db717-434">Added cmdlets to support multi-origin and private link functionality</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="db717-435">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="db717-435">Az.CognitiveServices</span></span>
* <span data-ttu-id="db717-436">已將 SDK 更新為 7.4.0-preview。</span><span class="sxs-lookup"><span data-stu-id="db717-436">Updated SDK to 7.4.0-preview.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="db717-437">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="db717-437">Az.Compute</span></span>
* <span data-ttu-id="db717-438">已將 '-VmssId' 參數新增至 'New-AzVm'</span><span class="sxs-lookup"><span data-stu-id="db717-438">Added '-VmssId' parameter to 'New-AzVm'</span></span>
* <span data-ttu-id="db717-439">已將 'PlatformFaultDomainCount' 參數新增至 'New-AzVmss' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db717-439">Added 'PlatformFaultDomainCount' parameter to the 'New-AzVmss' cmdlet.</span></span>
* <span data-ttu-id="db717-440">新的 Cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'</span><span class="sxs-lookup"><span data-stu-id="db717-440">New cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'</span></span>
* <span data-ttu-id="db717-441">已將 'Tier' 和 'LogicalSectorSize' 選擇性參數新增至 New-AzDiskConfig Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db717-441">Added 'Tier' and 'LogicalSectorSize' optional parameters to the New-AzDiskConfig cmdlet.</span></span> 
* <span data-ttu-id="db717-442">已將 'Tier'、'MaxSharesCount'、'DiskIOPSReadOnly' 和 'DiskMBpsReadOnly' 選擇性參數新增至 'New-AzDiskUpdateConfig' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db717-442">Added 'Tier', 'MaxSharesCount', 'DiskIOPSReadOnly', and 'DiskMBpsReadOnly' optional parameters to the 'New-AzDiskUpdateConfig' cmdlet.</span></span> 

#### <a name="azcontainerregistry"></a><span data-ttu-id="db717-443">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="db717-443">Az.ContainerRegistry</span></span>
* <span data-ttu-id="db717-444">[重大變更] 將 API 版本更新為 2019-05-01</span><span class="sxs-lookup"><span data-stu-id="db717-444">[Breaking Change] Updates API version to 2019-05-01</span></span>
* <span data-ttu-id="db717-445">[中斷性變更] 已從 'New-AzContainerRegistry' 中移除 SKU 'Classic' 和參數 'StorageAccountName'</span><span class="sxs-lookup"><span data-stu-id="db717-445">[Breaking Change] Removed SKU 'Classic' and parameter 'StorageAccountName' from 'New-AzContainerRegistry'</span></span>
* <span data-ttu-id="db717-446">已新增 Cmdlet：'Connect-AzContainerRegistry'、'Import-AzContainerRegistry'、'Get-AzContainerRegistryUsage'、'New-AzContainerRegistryNetworkRule'、'Set-AzContainerRegistryNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="db717-446">Added New cmdlets: 'Connect-AzContainerRegistry', 'Import-AzContainerRegistry', 'Get-AzContainerRegistryUsage', 'New-AzContainerRegistryNetworkRule', 'Set-AzContainerRegistryNetworkRule'</span></span>
* <span data-ttu-id="db717-447">已將新參數 'NetworkRuleSet' 新增至 'Update-AzContainerRegistry'</span><span class="sxs-lookup"><span data-stu-id="db717-447">Added new parameter 'NetworkRuleSet' to 'Update-AzContainerRegistry'</span></span>

#### <a name="azdatabricks"></a><span data-ttu-id="db717-448">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="db717-448">Az.Databricks</span></span>
* <span data-ttu-id="db717-449">已修正可能導致更新 Databricks 工作區，但 `-EncryptionKeyVersion` 不會失敗的錯誤。</span><span class="sxs-lookup"><span data-stu-id="db717-449">Fixed a bug that may cause updating databricks workspace without `-EncryptionKeyVersion` to fail.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="db717-450">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="db717-450">Az.DataFactory</span></span>
* <span data-ttu-id="db717-451">已將 ADF .Net SDK 版本更新為 4.12.0</span><span class="sxs-lookup"><span data-stu-id="db717-451">Updated ADF .Net SDK version to 4.12.0</span></span>
* <span data-ttu-id="db717-452">已將 ADF 加密用戶端 SDK 版本更新為 4.14.7587.7</span><span class="sxs-lookup"><span data-stu-id="db717-452">Updated ADF encryption client SDK version to 4.14.7587.7</span></span>
* <span data-ttu-id="db717-453">已新增 'Stop-AzDataFactoryV2TriggerRun' 和 'Invoke-AzDataFactoryV2TriggerRun' 命令</span><span class="sxs-lookup"><span data-stu-id="db717-453">Added 'Stop-AzDataFactoryV2TriggerRun' and 'Invoke-AzDataFactoryV2TriggerRun' commands</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="db717-454">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="db717-454">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="db717-455">需要 Location 屬性，才能建立最上層 arm 物件。</span><span class="sxs-lookup"><span data-stu-id="db717-455">Require Location property for creating top level arm objects.</span></span>
        <span data-ttu-id="db717-456">\* 使 `ApplicationGroupType` 成為 `New-AzWvdApplicationGroup` 的必要項。</span><span class="sxs-lookup"><span data-stu-id="db717-456">\* Made `ApplicationGroupType` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="db717-457">\* 使 `HostPoolArmPath` 成為 `New-AzWvdApplicationGroup` 的必要項。</span><span class="sxs-lookup"><span data-stu-id="db717-457">\* Made `HostPoolArmPath` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="db717-458">\* 已新增 `New-AzWvdHostPool`的 `PreferredAppGroupType`。</span><span class="sxs-lookup"><span data-stu-id="db717-458">\* Added `PreferredAppGroupType` for `New-AzWvdHostPool`.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="db717-459">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="db717-459">Az.Functions</span></span>
* <span data-ttu-id="db717-460">[中斷性變更] 已從 'Get-AzFunctionApp' 的所有參數集 (一個參數集除外) 中移除 'IncludeSlot' 切換參數。</span><span class="sxs-lookup"><span data-stu-id="db717-460">[Breaking Change] Removed 'IncludeSlot' switch parameter from all but one parameter set of 'Get-AzFunctionApp'.</span></span> <span data-ttu-id="db717-461">若已指定 '-IncludeSlot'，此 Cmdlet 現在支援在結果中擷取部署位置。</span><span class="sxs-lookup"><span data-stu-id="db717-461">The cmdlet now supports retrieving deployment slots in the results when '-IncludeSlot' is specified.</span></span> 
* <span data-ttu-id="db717-462">已更新 'New-AzFunctionApp'：</span><span class="sxs-lookup"><span data-stu-id="db717-462">Updated 'New-AzFunctionApp':</span></span>
  - <span data-ttu-id="db717-463">已修正 - DisableApplicationInsights，若已指定此選項，就不會建立 Application Insights 專案。</span><span class="sxs-lookup"><span data-stu-id="db717-463">Fixed -DisableApplicationInsights so that no application insights project is created when this option is specified.</span></span> <span data-ttu-id="db717-464">[#12728]</span><span class="sxs-lookup"><span data-stu-id="db717-464">[#12728]</span></span>
  - <span data-ttu-id="db717-465">[中斷性變更] 已移除建立 PowerShell 6.2 函式應用程式的支援</span><span class="sxs-lookup"><span data-stu-id="db717-465">[Breaking Change] Removed support to create PowerShell 6.2 function apps.</span></span>
  - <span data-ttu-id="db717-466">[中斷性變更] 若未指定 RuntimeVersion 參數，Windows 上 Functions 第 3 版中 PowerShell 函式應用程式的預設執行階段版本已從 6.2 變更為 7.0。</span><span class="sxs-lookup"><span data-stu-id="db717-466">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="db717-467">[中斷性變更] 若未指定 RuntimeVersion 參數，Windows 和 Linux 上 Functions 第 3 版中 Node 函式應用程式的預設執行階段版本已從 10 變更為 12。</span><span class="sxs-lookup"><span data-stu-id="db717-467">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="db717-468">[中斷性變更] 若未指定 RuntimeVersion 參數，Linux 上 Functions 第 3 版中 Python 函式應用程式的預設執行階段版本已從 3.7 變更為 3.8。</span><span class="sxs-lookup"><span data-stu-id="db717-468">[Breaking Change] Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the RuntimeVersion parameter is not specified.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="db717-469">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="db717-469">Az.HDInsight</span></span>
 * <span data-ttu-id="db717-470">針對 New-AzHDInsightCluster Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="db717-470">For New-AzHDInsightCluster cmdlet:</span></span>
     - <span data-ttu-id="db717-471">已將參數 'DefaultStorageAccountName' 取代為 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="db717-471">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="db717-472">已將參數 'DefaultStorageAccountKey' 取代為 'StorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="db717-472">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="db717-473">已將參數 'DefaultStorageAccountType' 取代為 'StorageAccountType'</span><span class="sxs-lookup"><span data-stu-id="db717-473">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="db717-474">已移除參數 'PublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="db717-474">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="db717-475">已移除參數 'OutboundPublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="db717-475">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
     - <span data-ttu-id="db717-476">已新增參數：'StorageFileSystem' 和 'StorageAccountManagedIdentity' 來支援 ADLSGen2</span><span class="sxs-lookup"><span data-stu-id="db717-476">Added new parameters: 'StorageFileSystem' and 'StorageAccountManagedIdentity' to support ADLSGen2</span></span>
     - <span data-ttu-id="db717-477">已新增參數 'EnableIDBroker' 來支援 HDInsight 識別碼代理程式</span><span class="sxs-lookup"><span data-stu-id="db717-477">Added new parameter 'EnableIDBroker' to Support HDInsight ID Broker</span></span>
     - <span data-ttu-id="db717-478">已新增參數：'KafkaClientGroupId'、'KafkaClientGroupName' 和 'KafkaManagementNodeSize' 來支援 Kafka Rest Proxy</span><span class="sxs-lookup"><span data-stu-id="db717-478">Added new parameters: 'KafkaClientGroupId', 'KafkaClientGroupName' and 'KafkaManagementNodeSize' to support Kafka Rest Proxy</span></span>
 * <span data-ttu-id="db717-479">針對 New-AzHDInsightClusterConfig Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="db717-479">For New-AzHDInsightClusterConfig cmdlet:</span></span>
     - <span data-ttu-id="db717-480">已將參數 'DefaultStorageAccountName' 取代為 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="db717-480">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="db717-481">已將參數 'DefaultStorageAccountKey' 取代為 'StorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="db717-481">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="db717-482">已將參數 'DefaultStorageAccountType' 取代為 'StorageAccountType'</span><span class="sxs-lookup"><span data-stu-id="db717-482">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="db717-483">已移除參數 'PublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="db717-483">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="db717-484">已移除參數 'OutboundPublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="db717-484">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="db717-485">針對 AzHDInsightDefaultStorage Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="db717-485">For Set-AzHDInsightDefaultStorage cmdlet:</span></span>
    - <span data-ttu-id="db717-486">已將參數 'StorageAccountName' 取代為 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="db717-486">Replaced parameter 'StorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="db717-487">針對 AzHDInsightSecurityProfile Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="db717-487">For Add-AzHDInsightSecurityProfile cmdlet:</span></span>
    - <span data-ttu-id="db717-488">已將參數 'Domain' 取代為 'DomainResourceId'</span><span class="sxs-lookup"><span data-stu-id="db717-488">Replaced parameter 'Domain' with 'DomainResourceId'</span></span>
    - <span data-ttu-id="db717-489">已移除參數 'OrganizationalUnitDN' 的強制需求</span><span class="sxs-lookup"><span data-stu-id="db717-489">Removed the mandatory requirement for parameter 'OrganizationalUnitDN'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="db717-490">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="db717-490">Az.KeyVault</span></span>
* <span data-ttu-id="db717-491">[中斷性變更] 已淘汰 'New-AzKeyVault' 中的參數 DisableSoftDelete 和 'Update-AzKeyVault' 中的 EnableSoftDelete 參數</span><span class="sxs-lookup"><span data-stu-id="db717-491">[Breaking Change] Deprecated parameter DisableSoftDelete in 'New-AzKeyVault' and EnableSoftDelete in 'Update-AzKeyVault'</span></span>
* <span data-ttu-id="db717-492">[中斷性變更] 已移除屬性 SecretValueText 來避免直接顯示 SecretValue [#12266]</span><span class="sxs-lookup"><span data-stu-id="db717-492">[Breaking Change] Removed attribute SecretValueText to avoid displaying SecretValue directly [#12266]</span></span>
* <span data-ttu-id="db717-493">支援的新資源類型：受控 HSM</span><span class="sxs-lookup"><span data-stu-id="db717-493">Supported new resource type: managed HSM</span></span>
    - <span data-ttu-id="db717-494">受控 HSM 的 CRUD 和要在受控 HSM 上操作金鑰的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-494">CRUD of managed HSM and cmdlets to operate keys on managed HSM</span></span>
    - <span data-ttu-id="db717-495">完整 HSM 備份/還原、AES 金鑰建立、安全性網域備份/還原、RBAC</span><span class="sxs-lookup"><span data-stu-id="db717-495">Full HSM backup/restore, AES key creation, security domain backup/restore, RBAC</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="db717-496">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="db717-496">Az.ManagedServices</span></span>
* <span data-ttu-id="db717-497">[中斷性變更] 已更新參數命名慣例和相關範例</span><span class="sxs-lookup"><span data-stu-id="db717-497">[Breaking Change] Updated parameters naming conventions and associated examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="db717-498">Az.Network</span><span class="sxs-lookup"><span data-stu-id="db717-498">Az.Network</span></span>
* <span data-ttu-id="db717-499">[中斷性變更] 已移除參數 'HostedSubnet' 並改為新增 'Subnet'</span><span class="sxs-lookup"><span data-stu-id="db717-499">[Breaking Change] Removed parameter 'HostedSubnet' and added 'Subnet' instead</span></span>
* <span data-ttu-id="db717-500">已針對虛擬路由器對等路由新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-500">Added new cmdlets for Virtual Router Peer Routes</span></span>
    - <span data-ttu-id="db717-501">'Get-AzVirtualRouterPeerLearnedRoute'</span><span class="sxs-lookup"><span data-stu-id="db717-501">'Get-AzVirtualRouterPeerLearnedRoute'</span></span>
    - <span data-ttu-id="db717-502">'Get-AzVirtualRouterPeerAdvertisedRoute'</span><span class="sxs-lookup"><span data-stu-id="db717-502">'Get-AzVirtualRouterPeerAdvertisedRoute'</span></span>
* <span data-ttu-id="db717-503">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="db717-503">Updated New-AzFirewall cmdlet:</span></span>
    - <span data-ttu-id="db717-504">已新增參數 '-SkuTier'</span><span class="sxs-lookup"><span data-stu-id="db717-504">Added parameter '-SkuTier'</span></span>
    - <span data-ttu-id="db717-505">已新增參數 '-SkuName' 並將 Sku 設為此項的別名</span><span class="sxs-lookup"><span data-stu-id="db717-505">Added parameter '-SkuName' and made Sku as Alias for this</span></span>
    - <span data-ttu-id="db717-506">已移除參數 '-Sku'</span><span class="sxs-lookup"><span data-stu-id="db717-506">Removed parameter '-Sku'</span></span>
* <span data-ttu-id="db717-507">[中斷性變更] 讓 'Connectionlink' 成為 'Start-AzVpnConnectionPacketCapture' 和 'Stop-AzVpnConnectionPacketCapture' 中的必要引數</span><span class="sxs-lookup"><span data-stu-id="db717-507">[Breaking Change] Made 'Connectionlink' argument mandatory in 'Start-AzVpnConnectionPacketCapture' and 'Stop-AzVpnConnectionPacketCapture'</span></span>
* <span data-ttu-id="db717-508">[中斷性變更] 已更新 'New-AzNetworkWatcherConnectionMonitorEndPointObject' 來移除參數 '-Filter'</span><span class="sxs-lookup"><span data-stu-id="db717-508">[Breaking Change] Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' to remove parameter '-Filter'</span></span>
* <span data-ttu-id="db717-509">[中斷性變更] 已將 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' Cmdlet 取代為 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'</span><span class="sxs-lookup"><span data-stu-id="db717-509">[Breaking Change] Replaced 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' cmdlet with 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'</span></span>
* <span data-ttu-id="db717-510">已更新 'New-AzNetworkWatcherConnectionMonitorEndPointObject' Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="db717-510">Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' cmdlet:</span></span>
    - <span data-ttu-id="db717-511">已新增參數 '-Type'</span><span class="sxs-lookup"><span data-stu-id="db717-511">Added parameter '-Type'</span></span>
    - <span data-ttu-id="db717-512">已新增參數 '-CoverageLevel'</span><span class="sxs-lookup"><span data-stu-id="db717-512">Added parameter '-CoverageLevel'</span></span>
    - <span data-ttu-id="db717-513">已新增參數 '-Scope'</span><span class="sxs-lookup"><span data-stu-id="db717-513">Added parameter '-Scope'</span></span>
* <span data-ttu-id="db717-514">已使用新參數 '-DestinationPortBehavior' 更新 'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-514">Updated 'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' cmdlet with new parameter '-DestinationPortBehavior'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="db717-515">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="db717-515">Az.RecoveryServices</span></span>
* <span data-ttu-id="db717-516">已修正參與者權限的工作負載還原。</span><span class="sxs-lookup"><span data-stu-id="db717-516">Fixing Workload Restore for contributor permissions.</span></span>
* <span data-ttu-id="db717-517">已針對 Restore-AzRecoveryServicesBackupItem Cmdlet 新增參數集和驗證。</span><span class="sxs-lookup"><span data-stu-id="db717-517">Added new parameter sets and validations for Restore-AzRecoveryServicesBackupItem cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="db717-518">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="db717-518">Az.Resources</span></span>
* <span data-ttu-id="db717-519">已修正剖析錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="db717-519">Fixed parsing bug</span></span>
* <span data-ttu-id="db717-520">已更新 ARM 範本 What-If Cmdlet 以便從結果中移除預覽訊息</span><span class="sxs-lookup"><span data-stu-id="db717-520">Updated ARM template What-If cmdlets to remove preview message from results</span></span>
* <span data-ttu-id="db717-521">已修正 '-WhatIf ' 設定於較高範圍時範本部署 Cmdlet 損毀的問題 [#13038]</span><span class="sxs-lookup"><span data-stu-id="db717-521">Fixed an issue where template deployment cmdlets crash if '-WhatIf' is set at a higher scope [#13038]</span></span>
* <span data-ttu-id="db717-522">已修正範本部署 Cmdlet 未保留範本參數大小寫的問題</span><span class="sxs-lookup"><span data-stu-id="db717-522">Fixed an issue where template deployment cmdlets does not preserve case for template parameters</span></span>
* <span data-ttu-id="db717-523">已新增要在 'Export-AzResourceGroup' Cmdlet 中使用的預設 API 版本</span><span class="sxs-lookup"><span data-stu-id="db717-523">Added a default API version to be used in 'Export-AzResourceGroup' cmdlet</span></span>
* <span data-ttu-id="db717-524">已針對範本規格 ('Get-AzTemplateSpec'、'Set-AzTemplateSpec'、'New-AzTemplateSpec'、'Remove-AzTemplateSpec'、'Export-AzTemplateSpec') 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-524">Added cmdlets for Template Specs ('Get-AzTemplateSpec', 'Set-AzTemplateSpec', 'New-AzTemplateSpec', 'Remove-AzTemplateSpec', 'Export-AzTemplateSpec')</span></span>
* <span data-ttu-id="db717-525">已新增使用現有的部署 Cmdlet 來部署範本規格的支援 (透過新的 -TemplateSpecId 參數)</span><span class="sxs-lookup"><span data-stu-id="db717-525">Added support for deploying Template Specs using existing deployment cmdlets (via the new -TemplateSpecId parameter)</span></span> 
* <span data-ttu-id="db717-526">已將 'Get-AzResourceGroupDeploymentOperation' 更新為使用 SDK。</span><span class="sxs-lookup"><span data-stu-id="db717-526">Updated 'Get-AzResourceGroupDeploymentOperation' to use the SDK.</span></span>
* <span data-ttu-id="db717-527">已從 '\*-AzDeployment' Cmdlet 中移除 '-ApiVersion' 參數。</span><span class="sxs-lookup"><span data-stu-id="db717-527">Removed '-ApiVersion' parameter from '\*-AzDeployment' cmdlets.</span></span>

#### <a name="azsql"></a><span data-ttu-id="db717-528">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="db717-528">Az.Sql</span></span>
* <span data-ttu-id="db717-529">已修正未指定 networkIsolation 時 New-AzSqlDatabaseExport 失敗的問題 [#13097]</span><span class="sxs-lookup"><span data-stu-id="db717-529">Fixed issue where New-AzSqlDatabaseExport fails if networkIsolation not specified [#13097]</span></span>
* <span data-ttu-id="db717-530">已修正 New-AzSqlDatabaseExport 和 New-AzSqlDatabaseImport 未在結果物件中傳回 OperationStatusLink 的問題 [#13097]</span><span class="sxs-lookup"><span data-stu-id="db717-530">Fixed issue where New-AzSqlDatabaseExport and New-AzSqlDatabaseImport were not returning OperationStatusLink in the result object [#13097]</span></span>
* <span data-ttu-id="db717-531">在備份儲存體備援警告中更新 Azure 配對區域 URL</span><span class="sxs-lookup"><span data-stu-id="db717-531">Update Azure Paired Regions URL in Backup Storage Redundancy Warnings</span></span> 

#### <a name="azstorage"></a><span data-ttu-id="db717-532">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="db717-532">Az.Storage</span></span>
* <span data-ttu-id="db717-533">已移除淘汰的屬性 RestorePolicy.LastEnabledTime</span><span class="sxs-lookup"><span data-stu-id="db717-533">Removed obsolete property RestorePolicy.LastEnabledTime</span></span>
    - <span data-ttu-id="db717-534">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="db717-534">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="db717-535">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="db717-535">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="db717-536">'Get-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="db717-536">'Get-AzStorageBlobServiceProperty'</span></span>
    - <span data-ttu-id="db717-537">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="db717-537">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="db717-538">將 DaysAfterModificationGreaterThan 的類型從 int 變更為 int？</span><span class="sxs-lookup"><span data-stu-id="db717-538">Change Type of DaysAfterModificationGreaterThan from int to int?</span></span>
    - <span data-ttu-id="db717-539">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="db717-539">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="db717-540">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="db717-540">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="db717-541">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="db717-541">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="db717-542">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="db717-542">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="db717-543">使用存取層支援的建立/更新檔案共用</span><span class="sxs-lookup"><span data-stu-id="db717-543">Supported create/update file share with access tier</span></span>
    - <span data-ttu-id="db717-544">'New-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="db717-544">'New-AzRmStorageShare'</span></span>
    - <span data-ttu-id="db717-545">'Update-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="db717-545">'Update-AzRmStorageShare'</span></span>
* <span data-ttu-id="db717-546">在 Datalake Gen2 項目上以遞迴方式支援的設定/更新/移除 Acl</span><span class="sxs-lookup"><span data-stu-id="db717-546">Supported set/update/remove Acl recursively on Datalake Gen2 item</span></span> 
    -  <span data-ttu-id="db717-547">'Set-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="db717-547">'Set-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="db717-548">'Update-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="db717-548">'Update-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="db717-549">'Remove-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="db717-549">'Remove-AzDataLakeGen2AclRecursive'</span></span>
* <span data-ttu-id="db717-550">具有新權限 x,t 支援的容器存取原則</span><span class="sxs-lookup"><span data-stu-id="db717-550">Supported Container access policy with new permission x,t</span></span>
    -  <span data-ttu-id="db717-551">'New-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="db717-551">'New-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="db717-552">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="db717-552">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="db717-553">已變更取得/設定容器存取原則 Cmdlet 的輸出，方法是將子屬性權限類型從 enum 變更為 String</span><span class="sxs-lookup"><span data-stu-id="db717-553">Changed the output of get/set Container access policy cmdlet, by change the child property Permission type from enum to String</span></span>
    -  <span data-ttu-id="db717-554">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="db717-554">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="db717-555">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="db717-555">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="db717-556">已修正使用 json 設定管理原則的範例指令碼問題</span><span class="sxs-lookup"><span data-stu-id="db717-556">Fixed a sample script issue of set management policy with json</span></span>
    -  <span data-ttu-id="db717-557">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="db717-557">'Set-AzStorageAccountManagementPolicy'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="db717-558">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="db717-558">Az.Websites</span></span>
* <span data-ttu-id="db717-559">已新增 Premium V3 定價層的支援</span><span class="sxs-lookup"><span data-stu-id="db717-559">Added support for Premium V3 pricing tier</span></span>
* <span data-ttu-id="db717-560">已將 WebSites SDK 更新為 3.1.0</span><span class="sxs-lookup"><span data-stu-id="db717-560">Updated the WebSites SDK to 3.1.0</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="db717-561">感謝我們的社群參與者</span><span class="sxs-lookup"><span data-stu-id="db717-561">Thanks to our community contributors</span></span>
* <span data-ttu-id="db717-562">@atul-ram，更新 Get-AzDelegation.md (#13176)</span><span class="sxs-lookup"><span data-stu-id="db717-562">@atul-ram, Update Get-AzDelegation.md (#13176)</span></span>
* <span data-ttu-id="db717-563">@dineshreddy007，在使用 WAC 權杖進行堆疊 HCI 註冊的情況下，取得正確指派的應用程式角色。</span><span class="sxs-lookup"><span data-stu-id="db717-563">@dineshreddy007, Get the App Roles assigned correctly in case of Stack HCI registration using WAC token.</span></span> <span data-ttu-id="db717-564">(#13249)</span><span class="sxs-lookup"><span data-stu-id="db717-564">(#13249)</span></span>
* <span data-ttu-id="db717-565">@kongou-ae，更新 New-AzOffice365PolicyProperty.md (#13217)</span><span class="sxs-lookup"><span data-stu-id="db717-565">@kongou-ae, Update New-AzOffice365PolicyProperty.md (#13217)</span></span>
* <span data-ttu-id="db717-566">Lohith Chowdary Chilukuri (@Lochiluk)，更新 Set-AzApplicationGateway.md (#13150)</span><span class="sxs-lookup"><span data-stu-id="db717-566">Lohith Chowdary Chilukuri (@Lochiluk), Update Set-AzApplicationGateway.md (#13150)</span></span>
* <span data-ttu-id="db717-567">Matthew Burleigh (@mburleigh)</span><span class="sxs-lookup"><span data-stu-id="db717-567">Matthew Burleigh (@mburleigh)</span></span>
  * <span data-ttu-id="db717-568">將連結新增至文件 (#13203) 中參考的 PowerShell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-568">Add links to PowerShell cmdlets referenced in the document (#13203)</span></span>
  * <span data-ttu-id="db717-569">將連結新增至文件 (#13190) 中參考的 PowerShell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-569">Add links to PowerShell cmdlets referenced in the document (#13190)</span></span>
  * <span data-ttu-id="db717-570">將連結新增至文件 (#13189) 中參考的 PowerShell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-570">Add links to PowerShell cmdlets referenced in the document (#13189)</span></span>
  * <span data-ttu-id="db717-571">將連結新增至參考的 Cmdlet (#13137)</span><span class="sxs-lookup"><span data-stu-id="db717-571">add links to referenced cmdlets (#13137)</span></span>
  * <span data-ttu-id="db717-572">將連結新增至文件 (#13204) 中參考的 PowerShell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-572">Add links to PowerShell cmdlets referenced in the document (#13204)</span></span>
  * <span data-ttu-id="db717-573">將連結新增至文件 (#13205) 中參考的 PowerShell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-573">Add links to PowerShell cmdlets referenced in the document (#13205)</span></span>

## <a name="480---october-2020"></a><span data-ttu-id="db717-574">4.8.0 - 2020 年 10 月</span><span class="sxs-lookup"><span data-stu-id="db717-574">4.8.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="db717-575">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="db717-575">Az.Accounts</span></span>
* <span data-ttu-id="db717-576">已修正通用程式庫中的日期時間剖析問題 [#13045]</span><span class="sxs-lookup"><span data-stu-id="db717-576">Fixed DateTime parse issue in common libraries [#13045]</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="db717-577">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="db717-577">Az.CognitiveServices</span></span>
* <span data-ttu-id="db717-578">已新增 'New-AzCognitiveServicesAccountApiProperty' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db717-578">Added 'New-AzCognitiveServicesAccountApiProperty' cmdlet.</span></span>
* <span data-ttu-id="db717-579">針對 'New-AzCognitiveServicesAccount' 和 'Set-AzCognitiveServicesAccount' 支援 'ApiProperty' 參數</span><span class="sxs-lookup"><span data-stu-id="db717-579">Supported 'ApiProperty' parameter for 'New-AzCognitiveServicesAccount' and 'Set-AzCognitiveServicesAccount'</span></span>

#### <a name="azcompute"></a><span data-ttu-id="db717-580">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="db717-580">Az.Compute</span></span>
* <span data-ttu-id="db717-581">已藉由田 FailoverTypes 修正 'Update-ASRRecoveryPlan' 中的問題</span><span class="sxs-lookup"><span data-stu-id="db717-581">Fixed issue in 'Update-ASRRecoveryPlan' by populating FailoverTypes</span></span>
* <span data-ttu-id="db717-582">已將 '-Top' 和 '-OrderBy' 選擇性參數新增至 'Get-AzVmImage' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db717-582">Added the '-Top' and '-OrderBy' optional parameters to the 'Get-AzVmImage' cmdlet.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="db717-583">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="db717-583">Az.Databricks</span></span>
* <span data-ttu-id="db717-584">'Az.Databricks' 模組正式發行</span><span class="sxs-lookup"><span data-stu-id="db717-584">General availability of 'Az.Databricks' module</span></span>
* <span data-ttu-id="db717-585">已新增虛擬網路對等互連的支援</span><span class="sxs-lookup"><span data-stu-id="db717-585">Added support for virtual network peering</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="db717-586">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="db717-586">Az.DataFactory</span></span>
* <span data-ttu-id="db717-587">已修正輸出訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="db717-587">Fixed typo in output messages</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="db717-588">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="db717-588">Az.EventHub</span></span>
* <span data-ttu-id="db717-589">已將選擇性切換參數 'TrustedServiceAccessEnabled' 新增至 'Set-AzEventHubNetworkRuleSet' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-589">Added optional switch parameter 'TrustedServiceAccessEnabled' to 'Set-AzEventHubNetworkRuleSet' cmdlet</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="db717-590">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="db717-590">Az.HDInsight</span></span>
* <span data-ttu-id="db717-591">已新增計劃的警告訊息，以取代 'PublicNetworkAccessType' 和 'OutboundPublicNetworkAccessType' 參數</span><span class="sxs-lookup"><span data-stu-id="db717-591">Added warning message for planning to deprecate the parameters 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="db717-592">已新增計劃的警告訊息，以使用 'StorageAccountResourceId' 取代 'DefaultStorageAccountName' 參數</span><span class="sxs-lookup"><span data-stu-id="db717-592">Added warning message for planning to replace the parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="db717-593">已新增計劃的警告訊息，以使用 'StorageAccountKey' 取代 'DefaultStorageAccountKey' 參數</span><span class="sxs-lookup"><span data-stu-id="db717-593">Added warning message for planning to replace the parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
* <span data-ttu-id="db717-594">已新增計劃的警告訊息，以使用 'StorageAccountType' 取代 'DefaultStorageAccountType' 參數</span><span class="sxs-lookup"><span data-stu-id="db717-594">Added warning message for planning to replace the parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
* <span data-ttu-id="db717-595">已新增計劃的警告訊息，以使用 'StorageContainer' 取代 'DefaultStorageContainer' 參數</span><span class="sxs-lookup"><span data-stu-id="db717-595">Added warning message for planning to replace the parameter 'DefaultStorageContainer' with 'StorageContainer'</span></span>
* <span data-ttu-id="db717-596">已新增計劃的警告訊息，以使用 'StorageRootPath' 取代 'DefaultStorageRootPath' 參數</span><span class="sxs-lookup"><span data-stu-id="db717-596">Added warning message for planning to replace the parameter 'DefaultStorageRootPath' with 'StorageRootPath'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="db717-597">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="db717-597">Az.IotHub</span></span>
* <span data-ttu-id="db717-598">已更新裝置 SDK。</span><span class="sxs-lookup"><span data-stu-id="db717-598">Updated devices sdk.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="db717-599">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="db717-599">Az.KeyVault</span></span>
* <span data-ttu-id="db717-600">已提供移除屬性 SecretValueText 的詳細日期</span><span class="sxs-lookup"><span data-stu-id="db717-600">Provided the detailed date of removing property SecretValueText</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="db717-601">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="db717-601">Az.ManagedServices</span></span>
* <span data-ttu-id="db717-602">已在受控服務指派和定義的 Cmdlet 上更新中斷性變更警告</span><span class="sxs-lookup"><span data-stu-id="db717-602">Updated breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="db717-603">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="db717-603">Az.Monitor</span></span>
* <span data-ttu-id="db717-604">已修正無法隱藏警告訊息的錯誤。</span><span class="sxs-lookup"><span data-stu-id="db717-604">Fixed the bug that warning message cannot be suppressed.</span></span> <span data-ttu-id="db717-605">[#12889]</span><span class="sxs-lookup"><span data-stu-id="db717-605">[#12889]</span></span>
* <span data-ttu-id="db717-606">在警示規則準則中支援 'SkipMetricValidation' 參數。</span><span class="sxs-lookup"><span data-stu-id="db717-606">Supported 'SkipMetricValidation' parameter in alert rule criteria.</span></span> <span data-ttu-id="db717-607">藉由導致略過計量驗證，允許針對尚未發出的自訂計量建立警示規則。</span><span class="sxs-lookup"><span data-stu-id="db717-607">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="db717-608">Az.Network</span><span class="sxs-lookup"><span data-stu-id="db717-608">Az.Network</span></span>
* <span data-ttu-id="db717-609">已將 Office365 原則新增至 VPNSite 資源</span><span class="sxs-lookup"><span data-stu-id="db717-609">Added Office365 Policy to VPNSite Resource</span></span>
    - <span data-ttu-id="db717-610">'New-AzO365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="db717-610">'New-AzO365PolicyProperty'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="db717-611">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="db717-611">Az.RecoveryServices</span></span>
* <span data-ttu-id="db717-612">已新增工作負載備份的容器名稱驗證。</span><span class="sxs-lookup"><span data-stu-id="db717-612">Added container name validation for workload backup.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="db717-613">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="db717-613">Az.RedisCache</span></span>
* <span data-ttu-id="db717-614">讓 'New-AzRedisCache' 和 'Set-AzRedisCache' Cmdlet 不會因為註冊 Microsoft.Cache RP 相關的權限問題而失敗</span><span class="sxs-lookup"><span data-stu-id="db717-614">Made 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets not fail because of permission issue related to registering Microsoft.Cache RP</span></span>

#### <a name="azsql"></a><span data-ttu-id="db717-615">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="db717-615">Az.Sql</span></span>
* <span data-ttu-id="db717-616">已將 BackupStorageRedundancy 新增至下列項目：</span><span class="sxs-lookup"><span data-stu-id="db717-616">Added BackupStorageRedundancy to the following:</span></span> 
    - <span data-ttu-id="db717-617">'Restore-AzureRmSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="db717-617">'Restore-AzureRmSqlDatabase'</span></span>
    - <span data-ttu-id="db717-618">'New-AzSqlDatabaseCopy'</span><span class="sxs-lookup"><span data-stu-id="db717-618">'New-AzSqlDatabaseCopy'</span></span>
    - <span data-ttu-id="db717-619">'New-AzSqlDatabaseSecondary'</span><span class="sxs-lookup"><span data-stu-id="db717-619">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="db717-620">已針對所有 SQL DB 參考移除 BackupStorageRedundancy 參數的區分大小寫</span><span class="sxs-lookup"><span data-stu-id="db717-620">Removed case sensitivity for BackupStorageRedundancy parameter for all SQL DB references</span></span> 
* <span data-ttu-id="db717-621">已更新 BackupStorageRedundancy 警告訊息名稱</span><span class="sxs-lookup"><span data-stu-id="db717-621">Updated BackupStorageRedundancy warning message names</span></span>

#### <a name="azstorage"></a><span data-ttu-id="db717-622">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="db717-622">Az.Storage</span></span>
* <span data-ttu-id="db717-623">儲存體帳戶檔案服務上支援的啟用/停用/取得共用虛刪除屬性</span><span class="sxs-lookup"><span data-stu-id="db717-623">Supported enable/disable/get share soft delete properties on file Service of a Storage account</span></span>
    - <span data-ttu-id="db717-624">'Update-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="db717-624">'Update-AzStorageFileServiceProperty'</span></span>
    - <span data-ttu-id="db717-625">'Get-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="db717-625">'Get-AzStorageFileServiceProperty'</span></span>
* <span data-ttu-id="db717-626">支援的清單檔案共用包含已刪除的儲存體帳戶，以及取得單一檔案共用使用方式</span><span class="sxs-lookup"><span data-stu-id="db717-626">Supported list file shares include the deleted ones of a Storage account, and Get single file share usage</span></span>
    - <span data-ttu-id="db717-627">'Get-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="db717-627">'Get-AzRmStorageShare'</span></span>
* <span data-ttu-id="db717-628">支援還原已刪除檔案共用</span><span class="sxs-lookup"><span data-stu-id="db717-628">Supported restore a deleted file share</span></span>
    - <span data-ttu-id="db717-629">'Restore-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="db717-629">'Restore-AzRmStorageShare'</span></span>
* <span data-ttu-id="db717-630">已變更修改 Blob 服務屬性的 Cmdlet，不會從伺服器取得原始屬性，而只會將修改的屬性設定至伺服器。</span><span class="sxs-lookup"><span data-stu-id="db717-630">Changed the cmdlets for modify blob service properties, won't get the original properties from server, but only set the modified properties to server.</span></span>
    - <span data-ttu-id="db717-631">'Enable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="db717-631">'Enable-AzStorageBlobDeleteRetentionPolicy'</span></span>
    - <span data-ttu-id="db717-632">'Disable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="db717-632">'Disable-AzStorageBlobDeleteRetentionPolicy'</span></span>  
    - <span data-ttu-id="db717-633">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="db717-633">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="db717-634">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="db717-634">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="db717-635">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="db717-635">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="db717-636">已修正 New-AzStorageAccount 參數 -Kind 預設值的說明問題 [#12189]</span><span class="sxs-lookup"><span data-stu-id="db717-636">Fixed help issue for New-AzStorageAccount parameter -Kind default value [#12189]</span></span>
* <span data-ttu-id="db717-637">已修正新增範例的問題，以顯示如何在 Blob 上傳中設定正確的 ContentType [#12989]</span><span class="sxs-lookup"><span data-stu-id="db717-637">Fixed issue by add example to show how to set correct ContentType in blob upload [#12989]</span></span>

## <a name="470---september-2020"></a><span data-ttu-id="db717-638">4.7.0 - 2020 年 9 月</span><span class="sxs-lookup"><span data-stu-id="db717-638">4.7.0 - September 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="db717-639">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="db717-639">Az.Accounts</span></span>
* <span data-ttu-id="db717-640">已格式化即將推出的重大變更訊息</span><span class="sxs-lookup"><span data-stu-id="db717-640">Formatted the upcoming breaking change messages</span></span>
* <span data-ttu-id="db717-641">已將 Azure.Core 更新為 1.4.1</span><span class="sxs-lookup"><span data-stu-id="db717-641">Updated Azure.Core to 1.4.1</span></span>

#### <a name="azaks"></a><span data-ttu-id="db717-642">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="db717-642">Az.Aks</span></span>
* <span data-ttu-id="db717-643">已新增 'New-AzAksCluster'、'Set-AzAksCluster' 和 'New-AzAksNodePool' 的用戶端參數驗證邏輯。</span><span class="sxs-lookup"><span data-stu-id="db717-643">Added client side parameter validation logic for 'New-AzAksCluster', 'Set-AzAksCluster' and 'New-AzAksNodePool'.</span></span> <span data-ttu-id="db717-644">[#12372]</span><span class="sxs-lookup"><span data-stu-id="db717-644">[#12372]</span></span>
* <span data-ttu-id="db717-645">已新增對 'New-AzAksCluster' 中附加元件的支援。</span><span class="sxs-lookup"><span data-stu-id="db717-645">Added support for add-ons in 'New-AzAksCluster'.</span></span> <span data-ttu-id="db717-646">[#11239]</span><span class="sxs-lookup"><span data-stu-id="db717-646">[#11239]</span></span>
* <span data-ttu-id="db717-647">已為附加元件新增 Cmdlet 'Enable-AzAksAddOn' 和 'Disable-AzAksAddOn'。</span><span class="sxs-lookup"><span data-stu-id="db717-647">Added cmdlets 'Enable-AzAksAddOn' and 'Disable-AzAksAddOn' for add-ons.</span></span> <span data-ttu-id="db717-648">[#11239]</span><span class="sxs-lookup"><span data-stu-id="db717-648">[#11239]</span></span>
* <span data-ttu-id="db717-649">已為 'New-AzAksCluster' 新增參數 'GenerateSshKey'。</span><span class="sxs-lookup"><span data-stu-id="db717-649">Added parameter 'GenerateSshKey' for 'New-AzAksCluster'.</span></span> <span data-ttu-id="db717-650">[#12371]</span><span class="sxs-lookup"><span data-stu-id="db717-650">[#12371]</span></span>
* <span data-ttu-id="db717-651">已將 api 版本更新為 2020-06-01。</span><span class="sxs-lookup"><span data-stu-id="db717-651">Updated api version to 2020-06-01.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="db717-652">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="db717-652">Az.CognitiveServices</span></span>
* <span data-ttu-id="db717-653">已顯示特定 API 的其他法律條款。</span><span class="sxs-lookup"><span data-stu-id="db717-653">Showed additional legal terms for certain APIs.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="db717-654">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="db717-654">Az.Compute</span></span>
* <span data-ttu-id="db717-655">已將 '-EncryptionType' 選擇性參數新增至 'New-AzVmDiskEncryptionSetConfig'</span><span class="sxs-lookup"><span data-stu-id="db717-655">Added the '-EncryptionType' optional parameter to 'New-AzVmDiskEncryptionSetConfig'</span></span>
* <span data-ttu-id="db717-656">適用於新資源類型的新 Cmdlet：DiskAccess 'Get-AzDiskAccess'、'New-AzDiskAccess'、'Get-AzDiskAccess'</span><span class="sxs-lookup"><span data-stu-id="db717-656">New cmdlets for new resource type: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span></span>
* <span data-ttu-id="db717-657">已將選擇性參數 '-DiskAccessId' 和 '-NetworkAccessPolicy' 新增至 'New-AzSnapshotConfig'</span><span class="sxs-lookup"><span data-stu-id="db717-657">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzSnapshotConfig'</span></span>
* <span data-ttu-id="db717-658">已將選擇性參數 '-DiskAccessId' 和 '-NetworkAccessPolicy' 新增至 'New-AzDiskConfig'</span><span class="sxs-lookup"><span data-stu-id="db717-658">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzDiskConfig'</span></span>
* <span data-ttu-id="db717-659">已將 'PatchStatus' 屬性新增至 VirtualMachine 執行個體檢視</span><span class="sxs-lookup"><span data-stu-id="db717-659">Added 'PatchStatus' property to VirtualMachine Instance View</span></span>
* <span data-ttu-id="db717-660">已將 'VMHealth' 屬性新增至虛擬機器的執行個體檢視，這是以 '-Status' 叫用 'Get-AzVm' 時傳回的物件</span><span class="sxs-lookup"><span data-stu-id="db717-660">Added 'VMHealth' property to the virtual machine's instance view, which is the returned object when 'Get-AzVm' is invoked with '-Status'</span></span>
* <span data-ttu-id="db717-661">已將 'AssignedHost' 欄位新增至 'Get-AzVM' 和 'Get-AzVmss' 執行個體檢視。</span><span class="sxs-lookup"><span data-stu-id="db717-661">Added 'AssignedHost' field to 'Get-AzVM' and 'Get-AzVmss' instance views.</span></span> <span data-ttu-id="db717-662">此欄位會顯示虛擬機器執行個體的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="db717-662">The field shows the resource id of the virtual machine instance</span></span>
* <span data-ttu-id="db717-663">已將選擇性參數 '-SupportAutomaticPlacement' 新增至 'New-AzHostGroup'</span><span class="sxs-lookup"><span data-stu-id="db717-663">Added optional parameter '-SupportAutomaticPlacement' to 'New-AzHostGroup'</span></span> 
* <span data-ttu-id="db717-664">已將 '-HostGroupId' 參數新增至 'New-AzVm' 和 'New-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="db717-664">Added the '-HostGroupId' parameter to 'New-AzVm' and 'New-AzVmss'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="db717-665">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="db717-665">Az.DataFactory</span></span>
* <span data-ttu-id="db717-666">已將 ADF .Net SDK 版本更新為 4.11.0</span><span class="sxs-lookup"><span data-stu-id="db717-666">Updated ADF .Net SDK version to 4.11.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="db717-667">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="db717-667">Az.EventHub</span></span>
* <span data-ttu-id="db717-668">已新增叢集 Cmdlet - 'New-AzEventHubCluster'、'Set-AzEventHubCluster'、'Get-AzEventHubCluster'、'Remove-AzEventHubCluster'、'Get-AzEventHubClustersAvailableRegions'。</span><span class="sxs-lookup"><span data-stu-id="db717-668">Added new Cluster cmdlets - 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span></span>
* <span data-ttu-id="db717-669">已修正問題 #10722：已修正只將 'Listen' 指派給 AuthorizationRule 權限的問題。</span><span class="sxs-lookup"><span data-stu-id="db717-669">Fixed for issue #10722 : Fix for assigning only 'Listen' to AuthorizationRule rights.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="db717-670">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="db717-670">Az.Functions</span></span>
* <span data-ttu-id="db717-671">已移除在不支援 v2 函式的區域中建立 v2 函式的功能。</span><span class="sxs-lookup"><span data-stu-id="db717-671">Removed the ability to create v2 Functions in regions that do not support it.</span></span>
* <span data-ttu-id="db717-672">已取代 PowerShell 6.2。</span><span class="sxs-lookup"><span data-stu-id="db717-672">Deprecated PowerShell 6.2.</span></span> <span data-ttu-id="db717-673">已新增警告，在使用者建立 PowerShell 6.2 函式應用程式時，建議他們改為建立 PowerShell 7.0 函式應用程式。</span><span class="sxs-lookup"><span data-stu-id="db717-673">Added a warning for when a user creates a PowerShell 6.2 function app that advises them to create a PowerShell 7.0 function app instead.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="db717-674">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="db717-674">Az.HDInsight</span></span>
* <span data-ttu-id="db717-675">支援建立具有自動調整設定的叢集</span><span class="sxs-lookup"><span data-stu-id="db717-675">Supported creating cluster with Autoscale configuration</span></span>
    - <span data-ttu-id="db717-676">已將新參數 'v2 Functions' 新增至 Cmdlet 'New-AzHDInsightCluster'</span><span class="sxs-lookup"><span data-stu-id="db717-676">Add new parameter 'AutoscaleConfiguration' to the cmdlet 'New-AzHDInsightCluster'</span></span>
* <span data-ttu-id="db717-677">支援操作叢集的自動調整設定</span><span class="sxs-lookup"><span data-stu-id="db717-677">Supported operating cluster's Autoscale configuration</span></span>
    - <span data-ttu-id="db717-678">已新增 Cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="db717-678">Add new cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="db717-679">已新增 Cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="db717-679">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="db717-680">已新增 Cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="db717-680">Add new cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="db717-681">已新增 Cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="db717-681">Add new cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="db717-682">已新增 Cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span><span class="sxs-lookup"><span data-stu-id="db717-682">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="db717-683">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="db717-683">Az.KeyVault</span></span>
* <span data-ttu-id="db717-684">已新增對 RBAC 授權的支援 [#10557]</span><span class="sxs-lookup"><span data-stu-id="db717-684">Added support for RBAC authorization [#10557]</span></span>
* <span data-ttu-id="db717-685">已加強 'Set-AzKeyVaultAccessPolicy' 中的錯誤處理 [#4007]</span><span class="sxs-lookup"><span data-stu-id="db717-685">Enhanced error handling in 'Set-AzKeyVaultAccessPolicy' [#4007]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="db717-686">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="db717-686">Az.Kusto</span></span>
* <span data-ttu-id="db717-687">正式發行 'Az.Kusto' 模組</span><span class="sxs-lookup"><span data-stu-id="db717-687">General availability of 'Az.Kusto' module</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="db717-688">Az.Network</span><span class="sxs-lookup"><span data-stu-id="db717-688">Az.Network</span></span>
* <span data-ttu-id="db717-689">[重大變更] 已更新下列 Cmdlet 以配合資源虛擬路由器和虛擬中樞</span><span class="sxs-lookup"><span data-stu-id="db717-689">[Breaking Change] Updated below cmdlets to align resource virtual router and virtual hub</span></span>
    - <span data-ttu-id="db717-690">'New-AzVirtualRouter'：</span><span class="sxs-lookup"><span data-stu-id="db717-690">'New-AzVirtualRouter':</span></span> 
        - <span data-ttu-id="db717-691">已新增 -HostedSubnet 參數來支援 IP 設定子資源</span><span class="sxs-lookup"><span data-stu-id="db717-691">Added -HostedSubnet parameter to support IP configuration child resource</span></span>
        - <span data-ttu-id="db717-692">已刪除 -HostedGateway 和 -HostedGatewayId</span><span class="sxs-lookup"><span data-stu-id="db717-692">deleted -HostedGateway and -HostedGatewayId</span></span>
    - <span data-ttu-id="db717-693">'Get-AzVirtualRouter'：</span><span class="sxs-lookup"><span data-stu-id="db717-693">'Get-AzVirtualRouter':</span></span>
        - <span data-ttu-id="db717-694">已新增訂用帳戶層級參數集</span><span class="sxs-lookup"><span data-stu-id="db717-694">Added subscription level parameter set</span></span>
    - <span data-ttu-id="db717-695">'Remove-AzVirtualRouter'</span><span class="sxs-lookup"><span data-stu-id="db717-695">'Remove-AzVirtualRouter'</span></span>
    - <span data-ttu-id="db717-696">'Add-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="db717-696">'Add-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="db717-697">'Get-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="db717-697">'Get-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="db717-698">'Remove-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="db717-698">'Remove-AzVirtualRouterPeer'</span></span>
* <span data-ttu-id="db717-699">已新增 Azure 快速路由連接埠的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-699">Added new cmdlet for Azure Express Route Port</span></span>
    - <span data-ttu-id="db717-700">'New-AzExpressRoutePortLOA'</span><span class="sxs-lookup"><span data-stu-id="db717-700">'New-AzExpressRoutePortLOA'</span></span>
* <span data-ttu-id="db717-701">已將 RemoteBgpCommunities 屬性新增至 VirtualNetwork 對等互連資源</span><span class="sxs-lookup"><span data-stu-id="db717-701">Added RemoteBgpCommunities property to the VirtualNetwork Peering Resource</span></span>
* <span data-ttu-id="db717-702">已修改 'New-AzLoadBalancerFrontendIpConfig'、'New-AzPublicIpAddress' 和 'New-AzPublicIpPrefix' 的警告訊息。</span><span class="sxs-lookup"><span data-stu-id="db717-702">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>
* <span data-ttu-id="db717-703">已將 VpnGatewayIpConfigurations 新增至 'Get-AzVpnGateway' 輸出</span><span class="sxs-lookup"><span data-stu-id="db717-703">Added VpnGatewayIpConfigurations to 'Get-AzVpnGateway' output</span></span>
* <span data-ttu-id="db717-704">已修正 'Set-AzApplicationGatewaySslCertificate' 的錯誤 (bug) [#9488]</span><span class="sxs-lookup"><span data-stu-id="db717-704">Fixed bug for 'Set-AzApplicationGatewaySslCertificate' [#9488]</span></span>
* <span data-ttu-id="db717-705">已將 'AllowActiveFTP' 參數新增至 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="db717-705">Added 'AllowActiveFTP' parameter to 'AzureFirewall'</span></span>
* <span data-ttu-id="db717-706">已更新下列功能命令：在 VirtualWan P2SVpnGateway 上啟用網際網路安全性設定/移除。</span><span class="sxs-lookup"><span data-stu-id="db717-706">Updated below commands for feature: Enable internet security set/remove on VirtualWan P2SVpnGateway.</span></span>
- <span data-ttu-id="db717-707">已更新 'New-AzP2sVpnGateway'：已新增選擇性切換參數 'EnableInternetSecurityFlag'，可讓客戶將其設定為 true，以在 P2SVpnGateway 上啟用網際網路安全性，這將適用於點對站用戶端。</span><span class="sxs-lookup"><span data-stu-id="db717-707">Updated 'New-AzP2sVpnGateway': Added optional switch parameter 'EnableInternetSecurityFlag' for customers to set true to enable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
- <span data-ttu-id="db717-708">已更新 'Update-AzP2sVpnGateway'：已新增選擇性切換參數 'EnableInternetSecurityFlag' 或 'DisableInternetSecurityFlag'，可讓客戶將其設定為 true/false，以在 P2SVpnGateway 上啟用/停用網際網路安全性，這將適用於點對站用戶端。</span><span class="sxs-lookup"><span data-stu-id="db717-708">Updated 'Update-AzP2sVpnGateway': Added optional switch parameters 'EnableInternetSecurityFlag' or 'DisableInternetSecurityFlag' for customers to set true/false to enable/disable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
* <span data-ttu-id="db717-709">已新增 Cmdlet 'Reset-AzP2sVpnGateway'，可讓客戶重設/重新啟動其 VirtualWan P2SVpnGateway 進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="db717-709">Added new cmdlet 'Reset-AzP2sVpnGateway' for customers to reset/reboot their VirtualWan P2SVpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="db717-710">已新增 Cmdlet 'Reset-AzVpnGateway'，可讓客戶重設/重新啟動其 VirtualWan VpnGateway 進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="db717-710">Added new cmdlet 'Reset-AzVpnGateway' for customers to reset/reboot their VirtualWan VpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="db717-711">已更新 'Set-AzVirtualNetworkSubnetConfig'</span><span class="sxs-lookup"><span data-stu-id="db717-711">Updated 'Set-AzVirtualNetworkSubnetConfig'</span></span>
    - <span data-ttu-id="db717-712">如果已在參數中明確設定，請將子網路的 NSG 和路由表屬性設定為 null [#1548][#9718]</span><span class="sxs-lookup"><span data-stu-id="db717-712">Set NSG and Route Table properties of subnet to null if explicitly set in parameters [#1548][#9718]</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="db717-713">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="db717-713">Az.RecoveryServices</span></span>
* <span data-ttu-id="db717-714">已修正工作負載備份項目的刪除狀態。</span><span class="sxs-lookup"><span data-stu-id="db717-714">Fixed the Delete State for workload Backup Items.</span></span>

#### <a name="azresources"></a><span data-ttu-id="db717-715">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="db717-715">Az.Resources</span></span>
* <span data-ttu-id="db717-716">已新增 Set-AzRoleAssignment 的遺漏檢查</span><span class="sxs-lookup"><span data-stu-id="db717-716">Added missing check for Set-AzRoleAssignment</span></span>
* <span data-ttu-id="db717-717">已將重大變更屬性新增至 'Get-AzResourceGroupDeploymentOperation' 的 'SubscriptionId' 參數</span><span class="sxs-lookup"><span data-stu-id="db717-717">Added breaking change attribute to 'SubscriptionId' parameter of 'Get-AzResourceGroupDeploymentOperation'</span></span>
* <span data-ttu-id="db717-718">已更新 ARM 範本 What-If Cmdlet，以顯示「忽略」上次資源變更</span><span class="sxs-lookup"><span data-stu-id="db717-718">Updated ARM template What-If cmdlets to show 'Ignore' resource changes last</span></span>
* <span data-ttu-id="db717-719">已修正部署 Cmdlet 的安全和陣列參數序列化問題 [#12773]</span><span class="sxs-lookup"><span data-stu-id="db717-719">Fixed secure and array parameter serialization issues for deployment cmdlets [#12773]</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="db717-720">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="db717-720">Az.ServiceFabric</span></span>
* <span data-ttu-id="db717-721">已新增適用於受控叢集和節點類型的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="db717-721">Added new cmdlets for managed clusters and node types:</span></span>
    - <span data-ttu-id="db717-722">'New-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="db717-722">'New-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="db717-723">'Get-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="db717-723">'Get-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="db717-724">'Set-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="db717-724">'Set-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="db717-725">'Remove-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="db717-725">'Remove-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="db717-726">'Add-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="db717-726">'Add-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="db717-727">'Remove-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="db717-727">'Remove-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="db717-728">'New-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="db717-728">'New-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="db717-729">'Get-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="db717-729">'Get-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="db717-730">'Set-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="db717-730">'Set-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="db717-731">'Remove-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="db717-731">'Remove-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="db717-732">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="db717-732">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="db717-733">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span><span class="sxs-lookup"><span data-stu-id="db717-733">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span></span>
    - <span data-ttu-id="db717-734">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="db717-734">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="db717-735">'Restart-AzServiceFabricManagedNodeTyp'</span><span class="sxs-lookup"><span data-stu-id="db717-735">'Restart-AzServiceFabricManagedNodeTyp'</span></span>
* <span data-ttu-id="db717-736">已將 Service Fabric SDK 升級為版本 1.2.0，此版本將服務網狀架構資源提供者 api-version 2020-03-01 用於目前模型，以及將 2020-01-01-preview 用於受控叢集。</span><span class="sxs-lookup"><span data-stu-id="db717-736">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2020-03-01 for the current model and 2020-01-01-preview for managed clusters.</span></span>

#### <a name="azsql"></a><span data-ttu-id="db717-737">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="db717-737">Az.Sql</span></span>
* <span data-ttu-id="db717-738">已將 BackupStorageRedundancy 新增至 'New-AzSqlInstance' 及 'Get-AzSqlInstance'</span><span class="sxs-lookup"><span data-stu-id="db717-738">Added BackupStorageRedundancy to 'New-AzSqlInstance' and 'Get-AzSqlInstance'</span></span>
* <span data-ttu-id="db717-739">已新增 Cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="db717-739">Added cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="db717-740">已新增 Cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="db717-740">Added cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="db717-741">已將 Force 參數新增至 'New-AzSqlInstance'</span><span class="sxs-lookup"><span data-stu-id="db717-741">Added Force parameter to 'New-AzSqlInstance'</span></span>
* <span data-ttu-id="db717-742">已新增受控資料庫記錄重新執行服務的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-742">Added cmdlets for Managed Database Log Replay service</span></span>
    - <span data-ttu-id="db717-743">'Start-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="db717-743">'Start-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="db717-744">'Get-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="db717-744">'Get-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="db717-745">'Complete-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="db717-745">'Complete-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="db717-746">'Stop-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="db717-746">'Stop-AzSqlInstanceDatabaseLogReplay'</span></span>
* <span data-ttu-id="db717-747">已新增 Cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="db717-747">Added cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="db717-748">已新增 Cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="db717-748">Added cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="db717-749">已新增 Cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="db717-749">Added cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="db717-750">已更新 Cmdlet 'New-AzSqlDatabaseImport' 和 'New-AzSqlDatabaseExport' 以支援網路隔離功能</span><span class="sxs-lookup"><span data-stu-id="db717-750">Updated cmdlets 'New-AzSqlDatabaseImport' and 'New-AzSqlDatabaseExport' to support network isolation functionality</span></span>
* <span data-ttu-id="db717-751">已新增 Cmdlet 'New-AzSqlDatabaseImportExisting'</span><span class="sxs-lookup"><span data-stu-id="db717-751">Added cmdlet 'New-AzSqlDatabaseImportExisting'</span></span>
* <span data-ttu-id="db717-752">已更新資料庫 Cmdlet 以支援備份儲存體類型規格</span><span class="sxs-lookup"><span data-stu-id="db717-752">Updated Databases cmdlets to support backup storage type specification</span></span>
* <span data-ttu-id="db717-753">已將 Force 參數新增至 'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="db717-753">Added Force parameter to 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="db717-754">已 'New-AzSqlDatabase' 的選取區域中新增 BackupStorageRedundancy 設定的警告</span><span class="sxs-lookup"><span data-stu-id="db717-754">Added warning for BackupStorageRedundancy configuration in select regions in 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="db717-755">已更新伺服器和執行個體的 ActiveDirectoryOnlyAuthentication Cmdlet，以包含 ResourceId 和 InputObject</span><span class="sxs-lookup"><span data-stu-id="db717-755">Updated ActiveDirectoryOnlyAuthentication cmdlets for server and instance to include ResourceId and InputObject</span></span>

#### <a name="azstorage"></a><span data-ttu-id="db717-756">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="db717-756">Az.Storage</span></span>
* <span data-ttu-id="db717-757">已升級至 Microsoft.Azure.Storage.DataMovement 2.0.0 來修正上傳 blob 失敗 [#12220]</span><span class="sxs-lookup"><span data-stu-id="db717-757">Fixed upload blob fail by upgrade to Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span></span>
* <span data-ttu-id="db717-758">支援時間點還原</span><span class="sxs-lookup"><span data-stu-id="db717-758">Supported Point In Time Restore</span></span>
    - <span data-ttu-id="db717-759">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="db717-759">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="db717-760">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="db717-760">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="db717-761">'New-AzStorageBlobRangeToRestore'</span><span class="sxs-lookup"><span data-stu-id="db717-761">'New-AzStorageBlobRangeToRestore'</span></span>
    - <span data-ttu-id="db717-762">'Restore-AzStorageBlobRange'</span><span class="sxs-lookup"><span data-stu-id="db717-762">'Restore-AzStorageBlobRange'</span></span>
* <span data-ttu-id="db717-763">支援執行 get-AzureRMStorageAccount 搭配參數 -IncludeGeoReplicationStats，取得儲存體帳戶的 blob 還原狀態</span><span class="sxs-lookup"><span data-stu-id="db717-763">Supported get blob restore status of Storage account by run get-AzureRMStorageAccount with parameter -IncludeBlobRestoreStatus</span></span> 
    - <span data-ttu-id="db717-764">'Get-AzureRMStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="db717-764">'Get-AzureRMStorageAccount'</span></span>
* <span data-ttu-id="db717-765">已為即將進行的 Cmdlet 輸出變更新增重大變更警告訊息</span><span class="sxs-lookup"><span data-stu-id="db717-765">Added breaking change warning message for upcoming cmdlet output change</span></span>
    - <span data-ttu-id="db717-766">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="db717-766">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="db717-767">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="db717-767">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="db717-768">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="db717-768">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="db717-769">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="db717-769">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="db717-770">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="db717-770">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="db717-771">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="db717-771">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="db717-772">已將 Microsoft.Azure.Cosmos.Table SDK 升級至 1.0.8</span><span class="sxs-lookup"><span data-stu-id="db717-772">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.8</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="db717-773">感謝我們的社群參與者</span><span class="sxs-lookup"><span data-stu-id="db717-773">Thanks to our community contributors</span></span>
* <span data-ttu-id="db717-774">Thomas Van Laere (@ThomVanL)，新增 Dockerfile-alpine-3.10 (#12911)</span><span class="sxs-lookup"><span data-stu-id="db717-774">Thomas Van Laere (@ThomVanL), Add Dockerfile-alpine-3.10 (#12911)</span></span> 
* <span data-ttu-id="db717-775">Lohith Chowdary Chilukuri (@Lochiluk)，更新 Remove-AzNetworkInterfaceIpConfig.md (#12807)</span><span class="sxs-lookup"><span data-stu-id="db717-775">Lohith Chowdary Chilukuri (@Lochiluk), Update Remove-AzNetworkInterfaceIpConfig.md (#12807)</span></span> 
* <span data-ttu-id="db717-776">Roberth Strand (@roberthstrand)，Get-AzResourceGroup - 新範例和清除 (#12828)</span><span class="sxs-lookup"><span data-stu-id="db717-776">Roberth Strand (@roberthstrand), Get-AzResourceGroup - New example, and cleanup (#12828)</span></span> 
* <span data-ttu-id="db717-777">Ravi Mishra (@inmishrar)，將 Azure Web 應用程式執行階段堆疊更新為 DOTNETCORE (#12833)</span><span class="sxs-lookup"><span data-stu-id="db717-777">Ravi Mishra (@inmishrar), update Azure Web App runtime stack to DOTNETCORE (#12833)</span></span> 
* <span data-ttu-id="db717-778">@jack-education，更新 New-azvirtualnetworksubnetconfig 以允許從子網移除 NSG 和路由表 (#12351)</span><span class="sxs-lookup"><span data-stu-id="db717-778">@jack-education, Updated Set-AzVirtualNetworkSubnetConfig to allow NSG and Route Table to be removed from subnet (#12351)</span></span> 
* <span data-ttu-id="db717-779">@hagop-globanet，更新 Add-AzApplicationGatewayCustomError.md (#12784)</span><span class="sxs-lookup"><span data-stu-id="db717-779">@hagop-globanet, Update Add-AzApplicationGatewayCustomError.md (#12784)</span></span> 
* <span data-ttu-id="db717-780">Joshua Van Daalen (@greenSacrifice)</span><span class="sxs-lookup"><span data-stu-id="db717-780">Joshua Van Daalen (@greenSacrifice)</span></span>
  * <span data-ttu-id="db717-781">將 Property 的拼寫更新為 Property (#12821)</span><span class="sxs-lookup"><span data-stu-id="db717-781">Update spelling of Property to Property (#12821)</span></span> 
  * <span data-ttu-id="db717-782">更新 New-AzResourceLock.md 範例 (#12806)</span><span class="sxs-lookup"><span data-stu-id="db717-782">Update New-AzResourceLock.md examples (#12806)</span></span>
* <span data-ttu-id="db717-783">Eragon Riddle (@eragonriddle)，更正範例中的參數欄位名稱 (#12825)</span><span class="sxs-lookup"><span data-stu-id="db717-783">Eragon Riddle (@eragonriddle), Corrected parameter field name in the example (#12825)</span></span> 
* <span data-ttu-id="db717-784">@rossifumax，修正 New-AzConfigurationAssignment.md 中的錯字 (#12701)</span><span class="sxs-lookup"><span data-stu-id="db717-784">@rossifumax, Fix typo in New-AzConfigurationAssignment.md (#12701)</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="db717-785">4.6.1 - 2020 年8 月</span><span class="sxs-lookup"><span data-stu-id="db717-785">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="db717-786">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="db717-786">Az.Compute</span></span>
* <span data-ttu-id="db717-787">已修補 'New-AzVm' 中的 '-EncryptionAtHost' 參數，以移除預設值 false [#12776]</span><span class="sxs-lookup"><span data-stu-id="db717-787">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="db717-788">4.6.0 - 2020 年8 月</span><span class="sxs-lookup"><span data-stu-id="db717-788">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="db717-789">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="db717-789">Az.Accounts</span></span>
* <span data-ttu-id="db717-790">當探索端點未傳回預設 AzureCloud 或其他公用環境時，載入所有公用雲端環境 [#12633]</span><span class="sxs-lookup"><span data-stu-id="db717-790">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="db717-791">在 'Get-AzSubscription' 中公開 SubscriptionPolicies [#12551]</span><span class="sxs-lookup"><span data-stu-id="db717-791">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="db717-792">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="db717-792">Az.Automation</span></span>
* <span data-ttu-id="db717-793">已將 '-RunOn' 參數新增至 'Set-AzAutomationWebhook，以指定混合式背景工作角色群組</span><span class="sxs-lookup"><span data-stu-id="db717-793">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="db717-794">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="db717-794">Az.Compute</span></span>
* <span data-ttu-id="db717-795">已將 '-EncryptionAtHost' 參數新增至 'New-AzVm'、'New-AzVmss'、'New-AzVMConfig'、'New-AzVmssConfig'、'Update-AzVM' 及 'Update-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="db717-795">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="db717-796">已將 'SecurityProfile' 新增至 'Get-AzVM' 和 'Get-AzVmss' 傳回物件</span><span class="sxs-lookup"><span data-stu-id="db717-796">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="db717-797">已將 '-InstanceView' 參數新增為 'Get-AzHostGroup' 的選擇性參數</span><span class="sxs-lookup"><span data-stu-id="db717-797">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="db717-798">已新增 'Invoke-AzVmPatchAssessment' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-798">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="db717-799">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="db717-799">Az.DataFactory</span></span>
* <span data-ttu-id="db717-800">已將遺漏屬性新增至 PSPipelineRun 類別。</span><span class="sxs-lookup"><span data-stu-id="db717-800">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="db717-801">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="db717-801">Az.HDInsight</span></span>
* <span data-ttu-id="db717-802">支援建立具有主機加密功能的叢集。</span><span class="sxs-lookup"><span data-stu-id="db717-802">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="db717-803">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="db717-803">Az.KeyVault</span></span>
* <span data-ttu-id="db717-804">已新增打算停用虛刪除的警告訊息</span><span class="sxs-lookup"><span data-stu-id="db717-804">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="db717-805">已新增打算移除 SecretValueText 屬性的警告訊息</span><span class="sxs-lookup"><span data-stu-id="db717-805">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="db717-806">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="db717-806">Az.Maintenance</span></span>
* <span data-ttu-id="db717-807">已將選擇性的排程相關欄位新增至 'New-AzMaintenanceConfiguration'</span><span class="sxs-lookup"><span data-stu-id="db717-807">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="db717-808">已為 'Get-AzMaintenancePublicConfiguration' 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-808">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="db717-809">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="db717-809">Az.ManagedServices</span></span>
* <span data-ttu-id="db717-810">已在受控服務指派和定義的 Cmdlet 上新增中斷性變更警告</span><span class="sxs-lookup"><span data-stu-id="db717-810">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="db717-811">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="db717-811">Az.Monitor</span></span>
* <span data-ttu-id="db717-812">已擴充 'Set-AzDiagnosticSetting' 中設定的參數，以分隔記錄和計量啟用 [#12482]</span><span class="sxs-lookup"><span data-stu-id="db717-812">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="db717-813">已修正從管線取得計量警示時的 'Add-AzMetricAlertRuleV2' 錯誤</span><span class="sxs-lookup"><span data-stu-id="db717-813">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="db717-814">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="db717-814">Az.Resources</span></span>
* <span data-ttu-id="db717-815">已更新 'Get-AzPolicyAlias' 回應以包含指出別名是否可由 Azure 原則修改的資訊。</span><span class="sxs-lookup"><span data-stu-id="db717-815">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="db717-816">已建立新的 'Set-AzRoleAssignment' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-816">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="db717-817">已新增 'Get-AzDeploymentManagementGroupWhatIfResult'，以取得 ARM 範本在管理群組範圍的假設結果</span><span class="sxs-lookup"><span data-stu-id="db717-817">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="db717-818">已新增 'Get-AzTenantWhatIfResult' Cmdlet，以取得 ARM 範本在租使用者範圍的假設結果</span><span class="sxs-lookup"><span data-stu-id="db717-818">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="db717-819">已覆寫 'New-AzManagementGroupDeployment' 和 'New-AzTenantDeployment' 的 '-WhatIf' 和 '-Confirm'，以使用 ARM 範本 What-If 結果</span><span class="sxs-lookup"><span data-stu-id="db717-819">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="db717-820">已修正新部署 Cmdlet 的 '-WhatIf' 和 '-Confirm' 行為，使其符合 False 和</span><span class="sxs-lookup"><span data-stu-id="db717-820">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="db717-821">已修正 '-TemplateObject' 和 'TemplateParameterObject' 的序列化錯誤 [#1528] [#6292]</span><span class="sxs-lookup"><span data-stu-id="db717-821">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="db717-822">已針對即將進行的輸出類型變更，對 'Get-AzResourceGroupDeploymentOperation' 新增中斷性變更屬性</span><span class="sxs-lookup"><span data-stu-id="db717-822">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="db717-823">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="db717-823">Az.SignalR</span></span>
* <span data-ttu-id="db717-824">已修正 'Restart-AzSignalR' 和 'Update-AzSignalR' 說明檔錯誤</span><span class="sxs-lookup"><span data-stu-id="db717-824">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="db717-825">已新增 'Update-AzSignalRNetworkAcl'、'Set-AzSignalRUpstream' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-825">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="db717-826">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="db717-826">Az.Storage</span></span>
* <span data-ttu-id="db717-827">支援的 Blob 查詢加速</span><span class="sxs-lookup"><span data-stu-id="db717-827">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="db717-828">'Get-AzStorageBlobQueryResult'</span><span class="sxs-lookup"><span data-stu-id="db717-828">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="db717-829">'New-AzStorageBlobQueryConfig'</span><span class="sxs-lookup"><span data-stu-id="db717-829">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="db717-830">已更新說明檔、新增更多描述及修正錯字</span><span class="sxs-lookup"><span data-stu-id="db717-830">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="db717-831">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="db717-831">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="db717-832">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="db717-832">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="db717-833">已修正當相關子目錄不存在時，下載 Blob 會失敗的問題 [#12592]</span><span class="sxs-lookup"><span data-stu-id="db717-833">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="db717-834">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="db717-834">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="db717-835">支援在儲存體帳戶上設定/取得/移除物件複寫原則</span><span class="sxs-lookup"><span data-stu-id="db717-835">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="db717-836">'New-AzStorageObjectReplicationPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="db717-836">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="db717-837">'Set-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="db717-837">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="db717-838">'Get-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="db717-838">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="db717-839">'Remove-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="db717-839">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="db717-840">支援在儲存體帳戶的 Blob 服務上啟用/停用 ChangeFeed</span><span class="sxs-lookup"><span data-stu-id="db717-840">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="db717-841">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="db717-841">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="db717-842">4.5.0 - 2020 年 8 月</span><span class="sxs-lookup"><span data-stu-id="db717-842">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="db717-843">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="db717-843">Az.Accounts</span></span>
* <span data-ttu-id="db717-844">已將 'Connect-AzAccount' 更新為接受參數 'MaxContextPopulation' [#9865]</span><span class="sxs-lookup"><span data-stu-id="db717-844">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="db717-845">已將 SubscriptionClient 版本更新為 2019-06-01 並顯示租用戶網域 [#9838]</span><span class="sxs-lookup"><span data-stu-id="db717-845">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="db717-846">訂用帳戶支援的主租用戶和 managedBy 租用戶資訊</span><span class="sxs-lookup"><span data-stu-id="db717-846">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="db717-847">已更正遙測資料中的模組名稱、版本資訊</span><span class="sxs-lookup"><span data-stu-id="db717-847">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="db717-848">已調整 SqlDatabaseDnsSuffix 和 ServiceManagementUrl (如果環境中繼資料端點傳回不相容的值)</span><span class="sxs-lookup"><span data-stu-id="db717-848">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="db717-849">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="db717-849">Az.Aks</span></span>
* <span data-ttu-id="db717-850">已將 'ClientIdAndSecret' 移除至 'ServicePrincipalIdAndSecret' 並將 'ClientIdAndSecret' 設定為別名 [#12381]。</span><span class="sxs-lookup"><span data-stu-id="db717-850">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="db717-851">已將 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' 移除至 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' 並將原始項目設定為別名 [#12373]。</span><span class="sxs-lookup"><span data-stu-id="db717-851">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="db717-852">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="db717-852">Az.ApiManagement</span></span>
* <span data-ttu-id="db717-853">已新增新的 'Add-AzApiManagementApiToGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db717-853">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="db717-854">已新增新的 'Get-AzApiManagementGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db717-854">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="db717-855">已新增新的 'Get-AzApiManagementGatewayHostnameConfiguration' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db717-855">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="db717-856">已新增新的 'Get-AzApiManagementGatewayKey' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db717-856">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="db717-857">已新增新的 'New-AzApiManagementGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db717-857">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="db717-858">已新增新的 'New-AzApiManagementGatewayHostnameConfiguration' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db717-858">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="db717-859">已新增新的 'New-AzApiManagementResourceLocationObject' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db717-859">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="db717-860">已新增新的 'Remove-AzApiManagementApiFromGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db717-860">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="db717-861">已新增新的 'Remove-AzApiManagementGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db717-861">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="db717-862">已新增新的 'Remove-AzApiManagementGatewayHostnameConfiguration' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db717-862">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="db717-863">已新增新的 'Update-AzApiManagementGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db717-863">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="db717-864">已將新的選擇性 [-GatewayId] 參數新增至 'Get-AzApiManagementApi' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db717-864">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="db717-865">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="db717-865">Az.CognitiveServices</span></span>
* <span data-ttu-id="db717-866">已特別將 'Deny' 作為 NetworkRules 預設動作使用。</span><span class="sxs-lookup"><span data-stu-id="db717-866">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="db717-867">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="db717-867">Az.FrontDoor</span></span>
* <span data-ttu-id="db717-868">已修正當 Enum.Parse 嘗試將 Null 值強制轉型為 Enabled 或 Disabled 列舉值時擲回例外狀況的問題 [#12344]</span><span class="sxs-lookup"><span data-stu-id="db717-868">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="db717-869">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="db717-869">Az.HDInsight</span></span>
* <span data-ttu-id="db717-870">支援使用傳輸中加密功能建立叢集。</span><span class="sxs-lookup"><span data-stu-id="db717-870">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="db717-871">將新參數 'EncryptionInTransit' 新增至 Cmdlet 'New-AzHDInsightCluster'</span><span class="sxs-lookup"><span data-stu-id="db717-871">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="db717-872">將新參數 'EncryptionInTransit' 新增至 Cmdlet 'New-AzHDInsightClusterConfig'</span><span class="sxs-lookup"><span data-stu-id="db717-872">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="db717-873">支援使用私人連結功能建立叢集：</span><span class="sxs-lookup"><span data-stu-id="db717-873">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="db717-874">將新參數 'PublicNetworkAccessType' 和 'OutboundPublicNetworkAccessType' 新增至 Cmdlet 'New-AzHDInsightCluster'</span><span class="sxs-lookup"><span data-stu-id="db717-874">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="db717-875">將新參數 'PublicNetworkAccessType' 和 'OutboundPublicNetworkAccessType' 新增至 Cmdlet 'New-AzHDInsightClusterConfig'</span><span class="sxs-lookup"><span data-stu-id="db717-875">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="db717-876">呼叫 'New-AzHDInsightCluster' 或 'Get-AzHDInsightCluster' 時傳回了虛擬網路資訊</span><span class="sxs-lookup"><span data-stu-id="db717-876">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="db717-877">Az.Network</span><span class="sxs-lookup"><span data-stu-id="db717-877">Az.Network</span></span>
* <span data-ttu-id="db717-878">已將 AddressPrefixType 參數的支援新增至 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="db717-878">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="db717-879">已新增不中斷變更：'Remove-AzExpressRouteCircutPeeringConfig' 中私人對等互連的 PeerAddressType 功能。</span><span class="sxs-lookup"><span data-stu-id="db717-879">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="db717-880">程式碼已變更為忽略 AddressPrefixType 和 PeerAddressType 參數的大小寫。</span><span class="sxs-lookup"><span data-stu-id="db717-880">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="db717-881">已修改 'New-AzLoadBalancerFrontendIpConfig'、'New-AzPublicIpAddress' 和 'New-AzPublicIpPrefix' 的警告訊息。</span><span class="sxs-lookup"><span data-stu-id="db717-881">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="db717-882">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="db717-882">Az.OperationalInsights</span></span>
* <span data-ttu-id="db717-883">已新增 'Remove-AzOperationalInsightsworkspace' 的 '-ForceDelete' 選項</span><span class="sxs-lookup"><span data-stu-id="db717-883">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="db717-884">已新增新的 Cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span><span class="sxs-lookup"><span data-stu-id="db717-884">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="db717-885">已新增新的 Cmdlet 'Restore-AzOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="db717-885">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="db717-886">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="db717-886">Az.RecoveryServices</span></span>
* <span data-ttu-id="db717-887">已改善 Azure 備份容器/項目探索體驗。</span><span class="sxs-lookup"><span data-stu-id="db717-887">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="db717-888">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="db717-888">Az.Resources</span></span>
* <span data-ttu-id="db717-889">已將 'Condition'、'ConditionVersion' 和 'Description' 屬性新增至 'New-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="db717-889">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="db717-890">這包括資料模型的所有相關變更</span><span class="sxs-lookup"><span data-stu-id="db717-890">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="db717-891">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="db717-891">Az.Sql</span></span>
* <span data-ttu-id="db717-892">已修正 'New-AzSqlServer' 和 'Set-AzSqlServer' 中可能的伺服器名稱不區分大小寫錯誤</span><span class="sxs-lookup"><span data-stu-id="db717-892">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="db717-893">已修正 'New-AzSqlDatabaseSecondary' 中現有資料庫錯誤上傳回的錯誤資料庫名稱</span><span class="sxs-lookup"><span data-stu-id="db717-893">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="db717-894">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="db717-894">Az.Storage</span></span>
* <span data-ttu-id="db717-895">支援建立具有新權限 x、t 的容器/blob Sas 權杖</span><span class="sxs-lookup"><span data-stu-id="db717-895">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="db717-896">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="db717-896">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="db717-897">'New-AzStorageContainerSASToken'</span><span class="sxs-lookup"><span data-stu-id="db717-897">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="db717-898">支援建立具有新權限 x、t、f 的帳戶 Sas 權杖</span><span class="sxs-lookup"><span data-stu-id="db717-898">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="db717-899">'New-AzStorageAccountSASToken'</span><span class="sxs-lookup"><span data-stu-id="db717-899">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="db717-900">支援取得單一檔案共用使用方式</span><span class="sxs-lookup"><span data-stu-id="db717-900">Supported get single file share usage</span></span>
    - <span data-ttu-id="db717-901">'Get-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="db717-901">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="db717-902">4.4.0 - 2020 年 7 月</span><span class="sxs-lookup"><span data-stu-id="db717-902">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="db717-903">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="db717-903">Az.Accounts</span></span>
* <span data-ttu-id="db717-904">已新增新的 Cmdlet 'Invoke-AzRestMethod'</span><span class="sxs-lookup"><span data-stu-id="db717-904">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="db717-905">已修正在多處理序案例中可能導致驗證錯誤的問題，例如使用 'Start-Job' 執行多個 Azure PowerShell Cmdlet [#9448]</span><span class="sxs-lookup"><span data-stu-id="db717-905">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="db717-906">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="db717-906">Az.Aks</span></span>
* <span data-ttu-id="db717-907">已修正 'Get-AzAks' 無法取得所有叢集的錯誤 (bug) [#12296]</span><span class="sxs-lookup"><span data-stu-id="db717-907">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="db717-908">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="db717-908">Az.AnalysisServices</span></span>
* <span data-ttu-id="db717-909">已移除驗證的專案參考</span><span class="sxs-lookup"><span data-stu-id="db717-909">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="db717-910">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="db717-910">Az.Automation</span></span>
* <span data-ttu-id="db717-911">已修正具有 escape 字元的字串無法轉換成 json 物件的問題。</span><span class="sxs-lookup"><span data-stu-id="db717-911">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="db717-912">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="db717-912">Az.Compute</span></span>
* <span data-ttu-id="db717-913">在沒有 'latest' 映像版本的情況下使用 'New-AzVmss' 時，新增警告</span><span class="sxs-lookup"><span data-stu-id="db717-913">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="db717-914">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="db717-914">Az.DataFactory</span></span>
* <span data-ttu-id="db717-915">已將全域參數新增至 Data Factory。</span><span class="sxs-lookup"><span data-stu-id="db717-915">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="db717-916">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="db717-916">Az.EventGrid</span></span>
* <span data-ttu-id="db717-917">已更新為使用 2020-06-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="db717-917">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="db717-918">加入新功能：</span><span class="sxs-lookup"><span data-stu-id="db717-918">Added new features:</span></span>
    - <span data-ttu-id="db717-919">輸入對應</span><span class="sxs-lookup"><span data-stu-id="db717-919">Input mapping</span></span>
    - <span data-ttu-id="db717-920">事件傳遞結構描述</span><span class="sxs-lookup"><span data-stu-id="db717-920">Event Delivery Schema</span></span>
    - <span data-ttu-id="db717-921">私人連結</span><span class="sxs-lookup"><span data-stu-id="db717-921">Private Link</span></span>
    - <span data-ttu-id="db717-922">雲端事件 V10 結構描述</span><span class="sxs-lookup"><span data-stu-id="db717-922">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="db717-923">將服務匯流排主題作為目的地</span><span class="sxs-lookup"><span data-stu-id="db717-923">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="db717-924">將 Azure Function 作為目的地</span><span class="sxs-lookup"><span data-stu-id="db717-924">Azure Function As Destination</span></span>
    - <span data-ttu-id="db717-925">WebHook 批次處理</span><span class="sxs-lookup"><span data-stu-id="db717-925">WebHook Batching</span></span>
    - <span data-ttu-id="db717-926">安全 Webhook (AAD 支援)</span><span class="sxs-lookup"><span data-stu-id="db717-926">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="db717-927">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="db717-927">IpFiltering</span></span>
* <span data-ttu-id="db717-928">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="db717-928">Updated cmdlets:</span></span>
    - <span data-ttu-id="db717-929">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span><span class="sxs-lookup"><span data-stu-id="db717-929">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="db717-930">新增選擇性參數以支援 webhook 批次處理。</span><span class="sxs-lookup"><span data-stu-id="db717-930">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="db717-931">新增選擇性參數以使用 AAD 支援安全的 Wdblook。</span><span class="sxs-lookup"><span data-stu-id="db717-931">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="db717-932">為 EndpointType 參數新增新的列舉，以支援 Azure 函式和服務匯流排主題作為新的目的地。</span><span class="sxs-lookup"><span data-stu-id="db717-932">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="db717-933">為傳遞結構描述新增選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="db717-933">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="db717-934">'New-AzEventGridTopic'/'Update-AzEventGridTopic' 和 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="db717-934">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="db717-935">新增選擇性參數以支援 IpFiltering。</span><span class="sxs-lookup"><span data-stu-id="db717-935">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="db717-936">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="db717-936">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="db717-937">新增選擇性參數以支援輸入對應。</span><span class="sxs-lookup"><span data-stu-id="db717-937">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="db717-938">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="db717-938">Az.FrontDoor</span></span>
* <span data-ttu-id="db717-939">已更新模組以使用 API 2020-05-01</span><span class="sxs-lookup"><span data-stu-id="db717-939">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="db717-940">已新增對儲存體、Keyvault 和 Web App Service 資源的私人連結支援</span><span class="sxs-lookup"><span data-stu-id="db717-940">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="db717-941">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="db717-941">Az.HDInsight</span></span>
* <span data-ttu-id="db717-942">支援在國家雲端中建立具有 ADLSGen1/2 儲存體的叢集。</span><span class="sxs-lookup"><span data-stu-id="db717-942">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="db717-943">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="db717-943">Az.Monitor</span></span>
* <span data-ttu-id="db717-944">已修正計量或記錄為 Null 時，'Get-AzDiagnosticSetting' 的錯誤 (bug) [#12272]</span><span class="sxs-lookup"><span data-stu-id="db717-944">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="db717-945">Az.Network</span><span class="sxs-lookup"><span data-stu-id="db717-945">Az.Network</span></span>
* <span data-ttu-id="db717-946">已修正 VWan HubVnet 連線中的參數交換</span><span class="sxs-lookup"><span data-stu-id="db717-946">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="db717-947">為 Azure 網路虛擬設備網站新增了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-947">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="db717-948">'Get-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="db717-948">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="db717-949">'New-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="db717-949">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="db717-950">'Remove-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="db717-950">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="db717-951">'Update-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="db717-951">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="db717-952">'New-AzOffice365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="db717-952">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="db717-953">為 Azure 網路虛擬設備新增了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-953">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="db717-954">'Get-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="db717-954">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="db717-955">'New-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="db717-955">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="db717-956">'Remove-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="db717-956">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="db717-957">'Update-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="db717-957">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="db717-958">'Get-AzNetworkVirtualApplianceSku'</span><span class="sxs-lookup"><span data-stu-id="db717-958">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="db717-959">'New-AzVirtualApplianceSkuProperty'</span><span class="sxs-lookup"><span data-stu-id="db717-959">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="db717-960">將應用程式閘道上架至私人連結通用 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-960">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="db717-961">將 StorageSync 上架至私人連結通用 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-961">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="db717-962">將 SignalR 上架至私人連結通用 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-962">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="db717-963">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="db717-963">Az.RecoveryServices</span></span>
* <span data-ttu-id="db717-964">已移除驗證的專案參考</span><span class="sxs-lookup"><span data-stu-id="db717-964">Removed project reference to Authentication</span></span>
* <span data-ttu-id="db717-965">Azure 備份微調的 Cmdlet 有助於文字更精確。</span><span class="sxs-lookup"><span data-stu-id="db717-965">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="db717-966">Azure 備份新增了使用 'Get-AzRecoveryServicesBackupJob' Cmdlet 來擷取 MAB 代理程式作業的支援。</span><span class="sxs-lookup"><span data-stu-id="db717-966">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="db717-967">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="db717-967">Az.Resources</span></span>
* <span data-ttu-id="db717-968">已將 'Save-AzResourceGroupDeploymentTemplate' 更新為使用 SDK。</span><span class="sxs-lookup"><span data-stu-id="db717-968">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="db717-969">已新增 'Unregister-AzResourceProvider' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db717-969">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="db717-970">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="db717-970">Az.Sql</span></span>
* <span data-ttu-id="db717-971">在 'Set-AzSqlInstanceActiveDirectoryAdministrator' Cmdlet 中新增了服務主體和來賓使用者的支援</span><span class="sxs-lookup"><span data-stu-id="db717-971">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="db717-972">已修正資料分類 Cmdlet 中的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="db717-972">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="db717-973">已新增 Azure SQL 受控執行個體容錯移轉的支援：'Invoke-AzSqlInstanceFailover'</span><span class="sxs-lookup"><span data-stu-id="db717-973">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="db717-974">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="db717-974">Az.Storage</span></span>
* <span data-ttu-id="db717-975">已修正未針對某些資料平面 Cmdlet 新增 UserAgent 的問題。</span><span class="sxs-lookup"><span data-stu-id="db717-975">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="db717-976">支援具有 MinimumTlsVersion 和 AllowBlobPublicAccess 的建立/更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="db717-976">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="db717-977">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="db717-977">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="db717-978">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="db717-978">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="db717-979">支援在儲存體帳戶的 Blob 服務上啟用/停用版本控制</span><span class="sxs-lookup"><span data-stu-id="db717-979">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="db717-980">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="db717-980">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="db717-981">支援 Blob 版本的列出 Blob</span><span class="sxs-lookup"><span data-stu-id="db717-981">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="db717-982">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="db717-982">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="db717-983">支援取得/移除單一 Blob 快照集或 Blob 版本</span><span class="sxs-lookup"><span data-stu-id="db717-983">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="db717-984">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="db717-984">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="db717-985">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="db717-985">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="db717-986">支援從 Azure.Storage.Blobs V12 所產生的 Blob 物件管道</span><span class="sxs-lookup"><span data-stu-id="db717-986">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="db717-987">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="db717-987">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="db717-988">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="db717-988">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="db717-989">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="db717-989">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="db717-990">'Set-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="db717-990">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="db717-991">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="db717-991">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="db717-992">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="db717-992">Az.StorageSync</span></span>
* <span data-ttu-id="db717-993">新增了以 ApiVersion 2020-03-01 為目標的新版 StorageSync SDK</span><span class="sxs-lookup"><span data-stu-id="db717-993">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="db717-994">已新增更新儲存體同步服務 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-994">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="db717-995">'Set-AzStorageSyncService'</span><span class="sxs-lookup"><span data-stu-id="db717-995">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="db717-996">已將 IncomingTrafficPolicy 和 PrivateEndpointConnections 新增至 StorageSyncService Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db717-996">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="db717-997">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="db717-997">Az.Websites</span></span>
* <span data-ttu-id="db717-998">已新增支援而可針對未和 App Service 方案位於相同資源群組中的插槽執行作業</span><span class="sxs-lookup"><span data-stu-id="db717-998">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="db717-999">4.3.0 - 2020 年 6 月</span><span class="sxs-lookup"><span data-stu-id="db717-999">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="db717-1000">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="db717-1000">Az.Accounts</span></span>
* <span data-ttu-id="db717-1001">預設支援的探索環境設定，並透過 'Add-AzEnvironment' 新增環境</span><span class="sxs-lookup"><span data-stu-id="db717-1001">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="db717-1002">更新預先載入的組件 [#12024]、[#11976]</span><span class="sxs-lookup"><span data-stu-id="db717-1002">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="db717-1003">已更新 Azure.Core 組件</span><span class="sxs-lookup"><span data-stu-id="db717-1003">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="db717-1004">已修正可能導致 'Connect-AzAccount' 在多執行緒執行中失敗的問題 [#11201]</span><span class="sxs-lookup"><span data-stu-id="db717-1004">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="db717-1005">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="db717-1005">Az.Aks</span></span>
* <span data-ttu-id="db717-1006">透過對 [ListClusterAdmin](/rest/api/aks/managedclusters/listclusteradmincredentials) 和 [ListClusterUser](/rest/api/aks/managedclusters/listclusterusercredentials) API 的呼叫，取代舊 [AccessProfile API](/rest/api/aks/managedclusters/getaccessprofile) 的使用方式</span><span class="sxs-lookup"><span data-stu-id="db717-1006">Replaced usage of old [AccessProfile API](/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="db717-1007">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="db717-1007">Az.Batch</span></span>
* <span data-ttu-id="db717-1008">已將 Az.Batch 更新為使用 'Microsoft.Azure.Management.Batch' SDK 版本 11.0.0</span><span class="sxs-lookup"><span data-stu-id="db717-1008">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="db717-1009">新增在 'New-AzBatchAccount' Cmdlet 中設定 BatchAccount 身分識別的功能</span><span class="sxs-lookup"><span data-stu-id="db717-1009">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="db717-1010">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="db717-1010">Az.CognitiveServices</span></span>
* <span data-ttu-id="db717-1011">支援的顯示帳戶功能。</span><span class="sxs-lookup"><span data-stu-id="db717-1011">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="db717-1012">支援修改 PublicNetworkAccess。</span><span class="sxs-lookup"><span data-stu-id="db717-1012">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="db717-1013">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="db717-1013">Az.Compute</span></span>
* <span data-ttu-id="db717-1014">已將 SimulateEviction 參數新增至 Set-AzVM 和 Set-AzVmssVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db717-1014">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="db717-1015">已將 'Premium_LRS' 新增至 New-AzGalleryImageVersion Cmdlet 的 StorageAccountType 參數的引數完成器。</span><span class="sxs-lookup"><span data-stu-id="db717-1015">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="db717-1016">已將子狀態新增至 VMCustomScriptExtension [#11297]</span><span class="sxs-lookup"><span data-stu-id="db717-1016">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="db717-1017">已將 'Delete' 新增至 New-AzVM 和 New-AzVMConfig Cmdlet 的 EvictionPolicy 參數的引數完成器。</span><span class="sxs-lookup"><span data-stu-id="db717-1017">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="db717-1018">已修正適用於 SAP 的新 VM 擴充功能名稱</span><span class="sxs-lookup"><span data-stu-id="db717-1018">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="db717-1019">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="db717-1019">Az.DataFactory</span></span>
* <span data-ttu-id="db717-1020">已將 ADF .Net SDK 版本更新為 4.9.0</span><span class="sxs-lookup"><span data-stu-id="db717-1020">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="db717-1021">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="db717-1021">Az.EventHub</span></span>
* <span data-ttu-id="db717-1022">已將受控識別參數新增至 'New-AzEventHubNamespace' 和 'Set-AzEventHubNamespace' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-1022">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="db717-1023">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="db717-1023">Az.Functions</span></span>
* <span data-ttu-id="db717-1024">已新增建立 PowerShell 7.0 和 Java 11 函式應用程式的支援</span><span class="sxs-lookup"><span data-stu-id="db717-1024">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="db717-1025">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="db717-1025">Az.HDInsight</span></span>
* <span data-ttu-id="db717-1026">支援的清單主機和重新開機 HDInsight 叢集的特定主機。</span><span class="sxs-lookup"><span data-stu-id="db717-1026">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="db717-1027">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="db717-1027">Az.HealthcareApis</span></span>
* <span data-ttu-id="db717-1028">已將 SDK 版本更新為 1.1.0</span><span class="sxs-lookup"><span data-stu-id="db717-1028">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="db717-1029">已新增匯出設定和受控識別的支援</span><span class="sxs-lookup"><span data-stu-id="db717-1029">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="db717-1030">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="db717-1030">Az.Monitor</span></span>
* <span data-ttu-id="db717-1031">已修正 'Set-AzActivityLogAlert' 的輸入物件參數</span><span class="sxs-lookup"><span data-stu-id="db717-1031">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="db717-1032">已修正 'Set-AzActionGroup' 的 'InputObject' 參數 [#10868]</span><span class="sxs-lookup"><span data-stu-id="db717-1032">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="db717-1033">Az.Network</span><span class="sxs-lookup"><span data-stu-id="db717-1033">Az.Network</span></span>
* <span data-ttu-id="db717-1034">已將 AddressPrefixType 參數的支援新增至 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="db717-1034">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="db717-1035">已新增 Azure FirewallPolicy 的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-1035">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="db717-1036">'New-AzFirewallPolicyDnsSetting'</span><span class="sxs-lookup"><span data-stu-id="db717-1036">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="db717-1037">在防火牆原則的網路規則中支援目的地 FQDN</span><span class="sxs-lookup"><span data-stu-id="db717-1037">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="db717-1038">已新增對後端位址集區作業的支援</span><span class="sxs-lookup"><span data-stu-id="db717-1038">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="db717-1039">'New-AzLoadBalancerBackendAddressConfig'</span><span class="sxs-lookup"><span data-stu-id="db717-1039">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="db717-1040">'New-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="db717-1040">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="db717-1041">'Set-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="db717-1041">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="db717-1042">'Remove-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="db717-1042">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="db717-1043">'Get-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="db717-1043">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="db717-1044">已新增 ' New-AzIpGroup' 的名稱驗證</span><span class="sxs-lookup"><span data-stu-id="db717-1044">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="db717-1045">已新增 Azure FirewallPolicy 的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-1045">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="db717-1046">'New-AzFirewallPolicyThreatIntelWhitelist'</span><span class="sxs-lookup"><span data-stu-id="db717-1046">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="db717-1047">已更新下列功能命令：在 VirtualWan P2SVpnGateway 上設定/移除自訂 dns 伺服器。</span><span class="sxs-lookup"><span data-stu-id="db717-1047">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="db717-1048">已更新 New-AzP2sVpnGateway：已為客戶新增選擇性參數 '-CustomDnsServer'，以指定要在 P2SVpnGateway 上設定的 dns 伺服器 (可供點對站用戶端使用)。</span><span class="sxs-lookup"><span data-stu-id="db717-1048">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="db717-1049">已更新 Update-AzP2sVpnGateway：已為客戶新增選擇性參數 '-CustomDnsServer'，以指定要在 P2SVpnGateway 上設定的 dns 伺服器 (可供點對站用戶端使用)。</span><span class="sxs-lookup"><span data-stu-id="db717-1049">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="db717-1050">已更新 'Update-AzVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="db717-1050">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="db717-1051">已為客戶新增選擇性參數 '-BgpPeeringAddress'，以指定要在 VpnGateway 上設定的自訂 bgps。</span><span class="sxs-lookup"><span data-stu-id="db717-1051">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="db717-1052">已新增新的 Cmdlet，以支援重設 VirtualHub 資源的路由狀態：</span><span class="sxs-lookup"><span data-stu-id="db717-1052">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="db717-1053">'Reset-AzHubRouter'</span><span class="sxs-lookup"><span data-stu-id="db717-1053">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="db717-1054">已根據防火牆原則的最近 Swagger 變更更新下列事項</span><span class="sxs-lookup"><span data-stu-id="db717-1054">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="db717-1055">變更 RuleGroup、RuleCollectionGroup 和 RuleType 的名稱</span><span class="sxs-lookup"><span data-stu-id="db717-1055">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="db717-1056">已新增對防火牆原則 NAT 規則集合的支援，以支援多個 NAT 規則集合</span><span class="sxs-lookup"><span data-stu-id="db717-1056">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="db717-1057">[重大變更] 已為 'New-AzFirewallPolicyApplicationRule' 和 'New-AzFirewallPolicyNetworkRule' 新增必要參數 'SourceIpGroup'。</span><span class="sxs-lookup"><span data-stu-id="db717-1057">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="db717-1058">[重大變更] 已修正 'New-AzFirewallPolicyApplicationRule'，參數 'SourceAddress' 會是必要的。</span><span class="sxs-lookup"><span data-stu-id="db717-1058">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="db717-1059">[重大變更] 已修正 'New-AzFirewallPolicyApplicationRule'，參數 'SourceAddress' 會是必要的。</span><span class="sxs-lookup"><span data-stu-id="db717-1059">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="db717-1060">[重大變更] 已移除必要參數：'New-AzFirewallPolicyNatRuleCollection' 的 'TranslatedAddress'、'TranslatedPort'。</span><span class="sxs-lookup"><span data-stu-id="db717-1060">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="db717-1061">已新增 Cmdlet 以在應用程式閘道上支援 PrivateLink</span><span class="sxs-lookup"><span data-stu-id="db717-1061">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="db717-1062">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="db717-1062">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="db717-1063">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="db717-1063">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="db717-1064">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="db717-1064">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="db717-1065">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="db717-1065">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="db717-1066">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="db717-1066">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="db717-1067">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span><span class="sxs-lookup"><span data-stu-id="db717-1067">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="db717-1068">已為 VirtualHub 的 HubRouteTables 子資源新增了 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db717-1068">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="db717-1069">'New-AzVHubRoute'</span><span class="sxs-lookup"><span data-stu-id="db717-1069">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="db717-1070">'New-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="db717-1070">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="db717-1071">'Get-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="db717-1071">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="db717-1072">'Update-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="db717-1072">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="db717-1073">'Remove-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="db717-1073">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="db717-1074">已更新現有的 Cmdlet，以支援 VirtualWan 中自訂路由的選擇性 RoutingConfiguration 輸入參數。</span><span class="sxs-lookup"><span data-stu-id="db717-1074">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="db717-1075">'New-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="db717-1075">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="db717-1076">'Set-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="db717-1076">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="db717-1077">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="db717-1077">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="db717-1078">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="db717-1078">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="db717-1079">'New-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="db717-1079">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="db717-1080">'Update-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="db717-1080">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="db717-1081">'New-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="db717-1081">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="db717-1082">'Update-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="db717-1082">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="db717-1083">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="db717-1083">Az.OperationalInsights</span></span>
* <span data-ttu-id="db717-1084">已修正 PSWorkspace 未實作 IOperationalInsightsWorkspace 的錯誤 (bug) [#12135]</span><span class="sxs-lookup"><span data-stu-id="db717-1084">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="db717-1085">已將 'pergb2018' 新增至 'Set-AzOperationalInsightsWorkspace' 中參數 'Sku' 的有效值集</span><span class="sxs-lookup"><span data-stu-id="db717-1085">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="db717-1086">已將參數 'FunctionParameter' 的別名 'FunctionParameters' 新增至</span><span class="sxs-lookup"><span data-stu-id="db717-1086">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="db717-1087">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="db717-1087">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="db717-1088">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="db717-1088">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="db717-1089">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="db717-1089">Az.RecoveryServices</span></span>
* <span data-ttu-id="db717-1090">Azure 備份新增了提取 MAB 項目的支援。</span><span class="sxs-lookup"><span data-stu-id="db717-1090">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="db717-1091">Azure Site Recovery 支援磁碟類型 'StandardSSD_LRS'</span><span class="sxs-lookup"><span data-stu-id="db717-1091">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="db717-1092">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="db717-1092">Az.Resources</span></span>
* <span data-ttu-id="db717-1093">已在 'PSADUser' 上新增 'UsageLocation'、'GivenName'、'Surname'、'AccountEnabled'、'MailNickname'、'Mail' [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="db717-1093">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="db717-1094">已修正 '-Mail' 在 'Get-AzADUser' 上無法運作的問題 [#11981]</span><span class="sxs-lookup"><span data-stu-id="db717-1094">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="db717-1095">已將 '-ExcludeChangeType' 參數新增至 'Get-AzDeploymentWhatIfResult' 和 'Get-AzResourceGroupDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="db717-1095">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="db717-1096">已將 '-WhatIfExcludeChangeType' 參數新增至 'New-AzDeployment' 和 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="db717-1096">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="db717-1097">已更新 'Test-Az\*Deployment' Cmdlet，以顯示更好的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="db717-1097">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="db717-1098">已針對 deployment create 和 What-If Cmdlet 的 '-Name ' 參數修正說明訊息</span><span class="sxs-lookup"><span data-stu-id="db717-1098">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="db717-1099">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="db717-1099">Az.Sql</span></span>
* <span data-ttu-id="db717-1100">已針對 Set SQL Server Azure Active Directory Admin Cmdlet 新增主體的支援</span><span class="sxs-lookup"><span data-stu-id="db717-1100">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="db717-1101">已修正資料分類 Cmdlet 中的同步處理問題。</span><span class="sxs-lookup"><span data-stu-id="db717-1101">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="db717-1102">支援在 'Set-AzSqlServerActiveDirectoryAdministrator' 上依照郵件搜尋使用者 [#12192]</span><span class="sxs-lookup"><span data-stu-id="db717-1102">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="db717-1103">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="db717-1103">Az.Storage</span></span>
* <span data-ttu-id="db717-1104">支援使用 RequireInfrastructureEncryption 建立儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="db717-1104">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="db717-1105">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="db717-1105">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="db717-1106">已將載入 Azure.Core 的邏輯移至 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="db717-1106">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="db717-1107">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="db717-1107">Az.Websites</span></span>
* <span data-ttu-id="db717-1108">已新增保護來刪除已建立的 Web 應用程式 (如果還原在 'Restore-AzDeletedWebApp' 中失敗)</span><span class="sxs-lookup"><span data-stu-id="db717-1108">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="db717-1109">已為 'New-AzWebApp' 和 'New-AzWebAppSlot' 新增 'SourceWebApp.Location'</span><span class="sxs-lookup"><span data-stu-id="db717-1109">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="db717-1110">已修正無法在 'Set-AzWebApp' 和 'Set-AzWebAppSlot' 中變更容器設定的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="db717-1110">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="db717-1111">已修正未提供 Get-AzWebApp 的 -Name 時取得 SiteConfig 的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="db717-1111">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="db717-1112">已新增為 Linux 應用程式建立 ASP 的支援</span><span class="sxs-lookup"><span data-stu-id="db717-1112">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="db717-1113">已在資源群組中新增複製的例外狀況</span><span class="sxs-lookup"><span data-stu-id="db717-1113">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="db717-1114">4.2.0 - 2020 年 6 月</span><span class="sxs-lookup"><span data-stu-id="db717-1114">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="db717-1115">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="db717-1115">Az.Accounts</span></span>
* <span data-ttu-id="db717-1116">已修正可能導致 Az 略過 Azure 自動化或 PowerShell 作業中記錄的問題 [#11492]</span><span class="sxs-lookup"><span data-stu-id="db717-1116">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="db717-1117">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="db717-1117">Az.AnalysisServices</span></span>
* <span data-ttu-id="db717-1118">已更新資料平面 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="db717-1118">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="db717-1119">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="db717-1119">Az.ApiManagement</span></span>
* <span data-ttu-id="db717-1120">已更新服務管理 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="db717-1120">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="db717-1121">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="db717-1121">Az.Billing</span></span>
* <span data-ttu-id="db717-1122">已更新耗用量 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="db717-1122">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="db717-1123">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="db717-1123">Az.CognitiveServices</span></span>
* <span data-ttu-id="db717-1124">支援 PrivateEndpoint 和 PublicNetworkAccess 控制項。</span><span class="sxs-lookup"><span data-stu-id="db717-1124">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="db717-1125">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="db717-1125">Az.DataFactory</span></span>
* <span data-ttu-id="db717-1126">已更新資料處理站 V2 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="db717-1126">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="db717-1127">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="db717-1127">Az.DataShare</span></span>
* <span data-ttu-id="db717-1128">''Az.DataShare'' 模組正式發行</span><span class="sxs-lookup"><span data-stu-id="db717-1128">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="db717-1129">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="db717-1129">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="db717-1130">''Az.DesktopVirtualization'' 模組正式發行</span><span class="sxs-lookup"><span data-stu-id="db717-1130">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="db717-1131">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="db717-1131">Az.OperationalInsights</span></span>
* <span data-ttu-id="db717-1132">已將 SDK 升級至 0.21.0</span><span class="sxs-lookup"><span data-stu-id="db717-1132">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="db717-1133">已將選用參數新增至</span><span class="sxs-lookup"><span data-stu-id="db717-1133">Added optional parameters to</span></span> 
    - <span data-ttu-id="db717-1134">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="db717-1134">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="db717-1135">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="db717-1135">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="db717-1136">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="db717-1136">Az.PolicyInsights</span></span>
* <span data-ttu-id="db717-1137">已更正 'Start-AzPolicyComplianceScan' 的範例 3</span><span class="sxs-lookup"><span data-stu-id="db717-1137">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="db717-1138">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="db717-1138">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="db717-1139">已更新 PowerBI Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="db717-1139">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="db717-1140">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="db717-1140">Az.PrivateDns</span></span>
* <span data-ttu-id="db717-1141">已更正 Remove-AzPrivateDnsRecordSet 的詳細資訊輸出字串格式</span><span class="sxs-lookup"><span data-stu-id="db717-1141">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="db717-1142">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="db717-1142">Az.RecoveryServices</span></span>
* <span data-ttu-id="db717-1143">Azure Site Recovery 支援建立復原計畫，以從 xml 輸入區域到區域複寫。</span><span class="sxs-lookup"><span data-stu-id="db717-1143">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="db717-1144">已更新 SiteRecovery 和備份 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="db717-1144">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="db717-1145">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="db717-1145">Az.Resources</span></span>
* <span data-ttu-id="db717-1146">已將 Tail 參數新增至 Get-AzDeploymentScriptLog 和 Save-AzDeploymentScriptLog Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-1146">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="db717-1147">已格式化輸出屬性，並將其顯示在 Get-AzDeploymentScript Cmdlet 輸出上</span><span class="sxs-lookup"><span data-stu-id="db717-1147">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="db717-1148">已將 -DeploymentScriptInputObject parameter 參數重新命名為 -DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="db717-1148">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="db717-1149">已修正 Cmdlet 訊息中遺漏的檔案/目標名稱。</span><span class="sxs-lookup"><span data-stu-id="db717-1149">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="db717-1150">已更新資源管理員和標記 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="db717-1150">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="db717-1151">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="db717-1151">Az.Sql</span></span>
* <span data-ttu-id="db717-1152">已將 UsePrivateLinkConnection 新增至 'New-AzSqlSyncGroup'、'Update-AzSqlSyncGroup'、'New-AzSqlSyncMember' 和 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="db717-1152">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="db717-1153">已將 SyncMemberAzureDatabaseResourceId 新增至 'New-AzSqlSyncMember' 和 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="db717-1153">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="db717-1154">已將來賓使用者查閱支援新增至 Set SQL Server Azure Active Directory Admin Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-1154">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="db717-1155">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="db717-1155">Az.Storage</span></span>
* <span data-ttu-id="db717-1156">已更新資料平面 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="db717-1156">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="db717-1157">4.1.0 - 2020 年 5 月</span><span class="sxs-lookup"><span data-stu-id="db717-1157">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="db717-1158">上次發佈版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="db717-1158">Highlights since the last release</span></span>
* <span data-ttu-id="db717-1159">支援的 PowerShell 版本：Windows PowerShell 5.1、PowerShell Core 6.2.4+、PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="db717-1159">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="db717-1160">Az.Functions 正式發行</span><span class="sxs-lookup"><span data-stu-id="db717-1160">General availability of Az.Functions</span></span> 
* <span data-ttu-id="db717-1161">Az.ApiManagement、Az.Batch、Az.Compute、Az.KeyVault、Az.Monitor、Az.Network、Az.OperationalInsights、Az.Resources 和 Az.Storage 具有主要版本</span><span class="sxs-lookup"><span data-stu-id="db717-1161">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="db717-1162">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="db717-1162">Az.Accounts</span></span>
* <span data-ttu-id="db717-1163">已更新 'Add-AzEnvironment' 和 'Set-AzEnvironment' 以接受 'AzureSynapseAnalyticsEndpointResourceId' 和 'AzureSynapseAnalyticsEndpointSuffix' 參數</span><span class="sxs-lookup"><span data-stu-id="db717-1163">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="db717-1164">已將 Azure.Core 相關組件新增至 Az.Accounts，支援的 PowerShell 平台包括 Windows PowerShell 5.1、PowerShell Core 6.2.4、PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="db717-1164">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="db717-1165">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="db717-1165">Az.Aks</span></span>
* <span data-ttu-id="db717-1166">已將 API 版本升級至 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="db717-1166">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="db717-1167">支援使用 Windows 容器建立 AKS</span><span class="sxs-lookup"><span data-stu-id="db717-1167">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="db717-1168">已提供新的 Cmdlet：'New-AzAksNodePool'、'Update-AzAksNodePool'、'Remove-AzAksNodePool'、        'Get-AzAksNodePool'、'Install-AzAksKubectl'、'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="db717-1168">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="db717-1169">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="db717-1169">Az.ApiManagement</span></span>
* <span data-ttu-id="db717-1170">'New-AzApiManagement' 與 'Set-AzApiManagement': [-AssignIdentity] 參數已重新命名為 [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="db717-1170">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="db717-1171">'New-AzApiManagement' 與 'Set-AzApiManagement'：已新增下列參數：[-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="db717-1171">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="db717-1172">'Get-AzApiManagementProperty'：已重新命名為 'Get-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="db717-1172">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="db717-1173">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="db717-1173">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="db717-1174">'New-AzApiManagementProperty'：已重新命名為 'New-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="db717-1174">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="db717-1175">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="db717-1175">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="db717-1176">'Set-AzApiManagementProperty'：已重新命名為 'Set-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="db717-1176">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="db717-1177">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="db717-1177">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="db717-1178">'Remove-AzApiManagementProperty'：已重新命名為 'Remove-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="db717-1178">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="db717-1179">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="db717-1179">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="db717-1180">新增的 'Get-AzApiManagementAuthorizationServerClientSecret' Cmdlet 和 'Get-AzApiManagementAuthorizationServer' 將不再傳回用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="db717-1180">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="db717-1181">新增的 'AzApiManagementNamedValueSecretValue' Cmdlet 和 'AzApiManagementNamedValue' 將不會傳回密碼值。</span><span class="sxs-lookup"><span data-stu-id="db717-1181">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="db717-1182">新增的 'Get-AzApiManagementOpenIdConnectProviderClientSecret' Cmdlet 和 'Get-AzApiManagementOpenIdConnectProvider' 將不再傳回用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="db717-1182">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="db717-1183">新增的 'AzApiManagementSubscriptionKey' Cmdlet 和 'AzApiManagementSubscription' 將不再傳回訂用帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="db717-1183">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="db717-1184">新增的 'AzApiManagementTenantAccessSecret' Cmdlet 和 'AzApiManagementTenantAccess' 將不再傳回金鑰。</span><span class="sxs-lookup"><span data-stu-id="db717-1184">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="db717-1185">新增的 'AzApiManagementTenantGitAccessSecret' Cmdlet 和 'AzApiManagementTenantGitAccess' 將不再傳回金鑰。</span><span class="sxs-lookup"><span data-stu-id="db717-1185">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="db717-1186">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="db717-1186">Az.ApplicationInsights</span></span>
* <span data-ttu-id="db717-1187">新增的參數：適用於 'New-AzApplicationInsights' 的 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery'</span><span class="sxs-lookup"><span data-stu-id="db717-1187">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="db717-1188">已建立 Cmdlet 'Update-AzApplicationInsights'</span><span class="sxs-lookup"><span data-stu-id="db717-1188">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="db717-1189">已針對連結的儲存體帳戶建立 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-1189">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="db717-1190">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="db717-1190">Az.Batch</span></span>
* <span data-ttu-id="db717-1191">已將 Az.Batch 更新為使用 'Microsoft.Azure.Batch' SDK 版本 13.0.0 和 'Microsoft.Azure.Management.Batch' SDK 版本 9.0.0。</span><span class="sxs-lookup"><span data-stu-id="db717-1191">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="db717-1192">已新增下列功能：使用新的 '-CertificateKind' 參數選取要新增至 'New-AzBatchCertificate' 的憑證種類。</span><span class="sxs-lookup"><span data-stu-id="db717-1192">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="db717-1193">已從 'PSApplication' 中移除先前一律為 '' 的 'ApplicationPackages' 屬性。</span><span class="sxs-lookup"><span data-stu-id="db717-1193">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="db717-1194">現在可以使用 'Get-AzBatchApplicationPackage' 來取出應用程式內的特定套件。</span><span class="sxs-lookup"><span data-stu-id="db717-1194">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="db717-1195">例如：'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'。</span><span class="sxs-lookup"><span data-stu-id="db717-1195">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="db717-1196">使用 'New-AzBatchPool' 建立集區時，'PSImageReference' 的 'VirtualMachineImageId' 屬性現在只能參考共用映像庫映像。</span><span class="sxs-lookup"><span data-stu-id="db717-1196">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="db717-1197">使用 'New-AzBatchPool' 建立集區時，可以使用 'PSNetworkConfiguration' 的新 'PublicIPAddressConfiguration' 屬性來佈建集區，無需公用 IP。</span><span class="sxs-lookup"><span data-stu-id="db717-1197">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="db717-1198">'PSNetworkConfiguration' 的 'PublicIPs' 屬性也已移至 'PSPublicIPAddressConfiguration'。</span><span class="sxs-lookup"><span data-stu-id="db717-1198">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="db717-1199">只有當 'IPAddressProvisioningType' 是 'UserManaged' 時，才能指定此屬性。</span><span class="sxs-lookup"><span data-stu-id="db717-1199">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="db717-1200">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="db717-1200">Az.Compute</span></span>
* <span data-ttu-id="db717-1201">已將 HostId 參數新增至 'Update-AzVM' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-1201">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="db717-1202">已更新 'New-AzVMConfig'、'New-AzVmssConfig', 'Update-AzVmss'、'Set-AzVMOperatingSystem' 和 'Set-AzVmssOsProfile' Cmdlet 的說明文件。</span><span class="sxs-lookup"><span data-stu-id="db717-1202">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="db717-1203">重大變更</span><span class="sxs-lookup"><span data-stu-id="db717-1203">Breaking changes</span></span>
    - <span data-ttu-id="db717-1204">已從 'Get-AzVMImage' Cmdlet 中移除 FilterExpression 參數。</span><span class="sxs-lookup"><span data-stu-id="db717-1204">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="db717-1205">已從 'New-AzVmssConfig'、'New-AzVMConfig' 和 'Update-AzVM' Cmdlet 中移除 AssignIdentity 參數。</span><span class="sxs-lookup"><span data-stu-id="db717-1205">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="db717-1206">已從 'New-AzVmssConfig' 和 'Update-AzVmss' Cmdlet 中移除 AutomaticRepairMaxInstanceRepairsPercent。</span><span class="sxs-lookup"><span data-stu-id="db717-1206">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="db717-1207">已從 ProximityPlacementGroup 中移除 AvailabilitySetsColocationStatus、VirtualMachinesColocationStatus 和 VirtualMachineScaleSetsColocationStatus。</span><span class="sxs-lookup"><span data-stu-id="db717-1207">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="db717-1208">已從 AutomaticRepairsPolicy 中移除 MaxInstanceRepairsPercent 屬性。</span><span class="sxs-lookup"><span data-stu-id="db717-1208">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="db717-1209">AvailabilitySets、VirtualMachines 和 VirtualMachineScaleSets 的類型已從 IList<SubResource> 變更為 IList<SubResourceWithColocationStatus>。</span><span class="sxs-lookup"><span data-stu-id="db717-1209">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="db717-1210">已更新 ' Update-azvm ' Cmdlet 的描述，以提供更好的描述。</span><span class="sxs-lookup"><span data-stu-id="db717-1210">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="db717-1211">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="db717-1211">Az.DataFactory</span></span>
* <span data-ttu-id="db717-1212">支援受控 IR 中資料流程執行階段屬性的 CRUD。</span><span class="sxs-lookup"><span data-stu-id="db717-1212">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="db717-1213">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="db717-1213">Az.FrontDoor</span></span>
* <span data-ttu-id="db717-1214">已新增用於建立、更新、取出及刪除 Front Door 規則引擎物件的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-1214">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="db717-1215">已新增用於建構 Front Door 規則引擎物件的協助程式 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-1215">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="db717-1216">已將規則引擎參考新增至 Front Door 路由規則物件。</span><span class="sxs-lookup"><span data-stu-id="db717-1216">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="db717-1217">已將私人連結參數新增至 Front Door 後端物件</span><span class="sxs-lookup"><span data-stu-id="db717-1217">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="db717-1218">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="db717-1218">Az.Functions</span></span>
* <span data-ttu-id="db717-1219">''Az.Functions'' 模組正式發行</span><span class="sxs-lookup"><span data-stu-id="db717-1219">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="db717-1220">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="db717-1220">Az.HDInsight</span></span>
* <span data-ttu-id="db717-1221">支援客戶管理的金鑰磁碟加密。</span><span class="sxs-lookup"><span data-stu-id="db717-1221">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="db717-1222">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="db717-1222">Az.HealthcareApis</span></span>
* <span data-ttu-id="db717-1223">存取原則不再預設為目前的主體</span><span class="sxs-lookup"><span data-stu-id="db717-1223">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="db717-1224">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="db717-1224">Az.IotHub</span></span>
* <span data-ttu-id="db717-1225">已新增 Cmdlet 來叫用 IoT 中樞內的查詢，以使用類似 SQL 的語言來取出資訊。</span><span class="sxs-lookup"><span data-stu-id="db717-1225">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="db717-1226">已修正下列問題：沒有子裝置，'Add-AzIotHubDevice' 無法建立已啟用 Edge 的裝置 [#11597]</span><span class="sxs-lookup"><span data-stu-id="db717-1226">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="db717-1227">已新增 Cmdlet 來產生 Iot 中樞、裝置或模組的 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="db717-1227">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="db717-1228">已新增 Cmdlet 來叫用設定計量查詢。</span><span class="sxs-lookup"><span data-stu-id="db717-1228">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="db717-1229">管理大規模的 IoT Edge 自動部署。</span><span class="sxs-lookup"><span data-stu-id="db717-1229">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="db717-1230">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="db717-1230">New cmdlets are:</span></span>
    - <span data-ttu-id="db717-1231">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="db717-1231">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="db717-1232">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="db717-1232">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="db717-1233">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="db717-1233">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="db717-1234">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="db717-1234">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="db717-1235">已新增 Cmdlet 來叫用 IoT Edge 部署計量查詢。</span><span class="sxs-lookup"><span data-stu-id="db717-1235">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="db717-1236">已新增 Cmdlet 將設定內容套用至指定的邊緣裝置。</span><span class="sxs-lookup"><span data-stu-id="db717-1236">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="db717-1237">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="db717-1237">Az.KeyVault</span></span>
* <span data-ttu-id="db717-1238">已移除兩個別名：'New-AzKeyVaultCertificateAdministratorDetails' 和 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="db717-1238">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="db717-1239">建立金鑰保存庫時，依預設會啟用虛刪除</span><span class="sxs-lookup"><span data-stu-id="db717-1239">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="db717-1240">在建立金鑰保存庫時，可以設定網路規則，以管理來自特定網路位置的協助工具</span><span class="sxs-lookup"><span data-stu-id="db717-1240">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="db717-1241">已新增攜帶您自己的金鑰 (BYOK) 的支援</span><span class="sxs-lookup"><span data-stu-id="db717-1241">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="db717-1242">'Add-AzKeyVaultKey' 支援產生金鑰交換金鑰</span><span class="sxs-lookup"><span data-stu-id="db717-1242">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="db717-1243">'Get-AzKeyVaultKey' 支援以 PEM 格式下載公開金鑰</span><span class="sxs-lookup"><span data-stu-id="db717-1243">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="db717-1244">已更新 'Add-AzKeyVaultKey' 說明文件的 'KeyOps' 部分</span><span class="sxs-lookup"><span data-stu-id="db717-1244">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="db717-1245">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="db717-1245">Az.Monitor</span></span>
* <span data-ttu-id="db717-1246">已修正 'AzDiagnosticSettings' 的下列錯誤 (bug)：保留原則不會套用到所有類別 [#11589]</span><span class="sxs-lookup"><span data-stu-id="db717-1246">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="db717-1247">計量警示 V2 支援 WebTest 可用性準則</span><span class="sxs-lookup"><span data-stu-id="db717-1247">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="db717-1248">'New-AzMetricAlertRuleV2Criteria'：已新增建立 webtest 可用性準則的選項</span><span class="sxs-lookup"><span data-stu-id="db717-1248">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="db717-1249">'Add-AzMetricAlertRuleV2'：支援新的 webtest 可用性準則</span><span class="sxs-lookup"><span data-stu-id="db717-1249">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="db717-1250">已移除 PSLogProfile 中 RetentionPolicy 的備援定義 [#7608]</span><span class="sxs-lookup"><span data-stu-id="db717-1250">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="db717-1251">已移除 PSEventData 中定義的備援屬性 [#11353]</span><span class="sxs-lookup"><span data-stu-id="db717-1251">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="db717-1252">已將 'Get-AzLog' 重新命名為 'Get-AzActivityLog'</span><span class="sxs-lookup"><span data-stu-id="db717-1252">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="db717-1253">Az.Network</span><span class="sxs-lookup"><span data-stu-id="db717-1253">Az.Network</span></span>
* <span data-ttu-id="db717-1254">已新增重大變更屬性，以通知區域預設行為將會變更</span><span class="sxs-lookup"><span data-stu-id="db717-1254">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="db717-1255">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="db717-1255">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="db717-1256">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="db717-1256">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="db717-1257">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="db717-1257">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="db717-1258">已新增最上層資源 SecurityPartnerProvider 的支援</span><span class="sxs-lookup"><span data-stu-id="db717-1258">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="db717-1259">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="db717-1259">New cmdlets added:</span></span>
        - <span data-ttu-id="db717-1260">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="db717-1260">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="db717-1261">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="db717-1261">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="db717-1262">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="db717-1262">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="db717-1263">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="db717-1263">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="db717-1264">已在 'PSPrivateLinkResource' 上新增 'RequiredZoneNames'，並在 'PSPrivateEndpointConnection' 上新增 'GroupId'</span><span class="sxs-lookup"><span data-stu-id="db717-1264">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="db717-1265">已針對 New-AzNetworkWatcherConnectionMonitorTestConfigurationObject 修正 SuccessThresholdRoundTripTimeMs 參數的不正確類型</span><span class="sxs-lookup"><span data-stu-id="db717-1265">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="db717-1266">已更新 VirtualWan Cmdlet，將 AllowVnetToVnetTraffic 引數的預設值設為 True。</span><span class="sxs-lookup"><span data-stu-id="db717-1266">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="db717-1267">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="db717-1267">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="db717-1268">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="db717-1268">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="db717-1269">已新增 Cmdlet 來支援私人端點的 DNS 區域群組</span><span class="sxs-lookup"><span data-stu-id="db717-1269">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="db717-1270">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="db717-1270">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="db717-1271">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="db717-1271">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="db717-1272">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="db717-1272">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="db717-1273">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="db717-1273">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="db717-1274">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="db717-1274">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="db717-1275">已將 'DNSEnableProxy'、'DNSRequireProxyForNetworkRules' 和 'DNSServers' 參數新增至 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="db717-1275">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="db717-1276">已將 'EnableDnsProxy'、'DnsProxyNotRequiredForNetworkRule' 和 'DnsServer' 參數新增至 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="db717-1276">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="db717-1277">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="db717-1277">Updated cmdlet:</span></span>
        - <span data-ttu-id="db717-1278">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="db717-1278">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="db717-1279">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="db717-1279">Az.OperationalInsights</span></span>
* <span data-ttu-id="db717-1280">已更新舊版程式碼以套用新產生的 SDK</span><span class="sxs-lookup"><span data-stu-id="db717-1280">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="db717-1281">由於已取代 API，刪除了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-1281">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="db717-1282">'Get-AzOperationalInsightsSavedSearchResult' (別名 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="db717-1282">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="db717-1283">'Get-AzOperationalInsightsSearchResult' (別名 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="db717-1283">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="db717-1284">'Get-AzOperationalInsightsLinkTarget' (別名 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="db717-1284">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="db717-1285">已新增 'Set-AzOperationalInsightsWorkspace' 和 'New-AzOperationalInsightsWorkspace' 的參數</span><span class="sxs-lookup"><span data-stu-id="db717-1285">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="db717-1286">已針對連結的儲存體帳戶建立 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-1286">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="db717-1287">已針對叢集和連結服務建立 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-1287">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="db717-1288">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="db717-1288">Az.RecoveryServices</span></span>
* <span data-ttu-id="db717-1289">Azure Site Recovery 已將保護 Azure 鄰近放置群組虛擬機器的支援新增至 Azure 提供者。</span><span class="sxs-lookup"><span data-stu-id="db717-1289">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="db717-1290">Azure Site Recovery 已將區域的支援新增至區域複本。</span><span class="sxs-lookup"><span data-stu-id="db717-1290">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="db717-1291">Azure 備份已新增適用於 Azure FileShare 復原點的長期保留支援。</span><span class="sxs-lookup"><span data-stu-id="db717-1291">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="db717-1292">Azure 備份已將磁片排除屬性新增至 'Get-AzRecoveryServicesBackupItem' Cmdlet 輸出。</span><span class="sxs-lookup"><span data-stu-id="db717-1292">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="db717-1293">已針對站台復原服務新增保存庫認證檔的私人端點。</span><span class="sxs-lookup"><span data-stu-id="db717-1293">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="db717-1294">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="db717-1294">Az.Resources</span></span>
* <span data-ttu-id="db717-1295">已新增有關在建立新角色定義時檢視延遲的訊息警告</span><span class="sxs-lookup"><span data-stu-id="db717-1295">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="db717-1296">已變更原則 Cmdlet 以輸出強型別物件</span><span class="sxs-lookup"><span data-stu-id="db717-1296">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="db717-1297">已移除用於 'Get-AzResourceLock' Cmdlet 的 '-TenantLevel ' 參數 [#11335]</span><span class="sxs-lookup"><span data-stu-id="db717-1297">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="db717-1298">已修正 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span><span class="sxs-lookup"><span data-stu-id="db717-1298">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="db717-1299">已新增在資源群組範圍中取得 ARM 範本 What-If 結果的 Cmdlet：'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="db717-1299">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="db717-1300">已新增在訂用帳戶範圍中取得 ARM 範本 What-If 結果的 Cmdlet：'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="db717-1300">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="db717-1301">Alias:'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="db717-1301">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="db717-1302">已覆寫 'New-AzDeployment' 和 'New-AzResourceGroupDeployment' 的 '-WhatIf' 和 '-Confirm' 參數，以使用 ARM 範本 What-If 結果</span><span class="sxs-lookup"><span data-stu-id="db717-1302">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="db717-1303">已在部署 Cmdlet 中新增 'ApiVersion' 參數的取代訊息</span><span class="sxs-lookup"><span data-stu-id="db717-1303">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="db717-1304">已新增為部署失敗顯示已改善錯誤訊息的功能</span><span class="sxs-lookup"><span data-stu-id="db717-1304">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="db717-1305">已新增針對部署失敗記錄的 correlationId</span><span class="sxs-lookup"><span data-stu-id="db717-1305">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="db717-1306">已將 'error' 屬性新增至部署指令碼輸出</span><span class="sxs-lookup"><span data-stu-id="db717-1306">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="db717-1307">已將 nuget Microsoft.Azure.Management.ResourceManager 更新為 '3.7.1-preview'</span><span class="sxs-lookup"><span data-stu-id="db717-1307">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="db717-1308">當 DeploymentValidateResult 中的 Error 屬性變更為唯讀時，已從 nuget 3.7.1-preview 中移除特定測試案例</span><span class="sxs-lookup"><span data-stu-id="db717-1308">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="db717-1309">已從 SDK ResourceManager 3.7.1-preview 引進 GenericResourceExpanded</span><span class="sxs-lookup"><span data-stu-id="db717-1309">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="db717-1310">已針對用於部署的所有 Get Cmdlet 以及下列 Cmdlet 新增標籤支援：</span><span class="sxs-lookup"><span data-stu-id="db717-1310">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="db717-1311">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="db717-1311">'New-AzDeployment'</span></span>
    - <span data-ttu-id="db717-1312">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="db717-1312">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="db717-1313">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="db717-1313">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="db717-1314">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="db717-1314">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="db717-1315">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="db717-1315">Az.ServiceFabric</span></span>
* <span data-ttu-id="db717-1316">已修正下列錯誤 (bug)：使用 --SecretIdentifier 新增憑證時取得錯誤憑證指紋</span><span class="sxs-lookup"><span data-stu-id="db717-1316">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="db717-1317">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="db717-1317">Az.Sql</span></span>
* <span data-ttu-id="db717-1318">增強下列項目的效能：</span><span class="sxs-lookup"><span data-stu-id="db717-1318">Enhance performance of:</span></span>
    - <span data-ttu-id="db717-1319">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="db717-1319">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="db717-1320">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="db717-1320">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="db717-1321">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="db717-1321">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="db717-1322">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="db717-1322">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="db717-1323">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="db717-1323">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="db717-1324">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="db717-1324">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="db717-1325">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="db717-1325">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="db717-1326">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="db717-1326">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="db717-1327">已從 Cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy' 移除 'RetentionDays' 參數的用戶端驗證</span><span class="sxs-lookup"><span data-stu-id="db717-1327">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="db717-1328">在 Vnet 中對儲存體帳戶進行稽核時，修正在建立儲存體 Blob 資料參與者角色時發生的錯誤。</span><span class="sxs-lookup"><span data-stu-id="db717-1328">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="db717-1329">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="db717-1329">Az.Storage</span></span>
* <span data-ttu-id="db717-1330">已新增 '-AsJob' 以取得/列出帳戶 Cmdlet 'Get-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="db717-1330">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="db717-1331">使用 KeyvaultEncryption 更新儲存體帳戶以支援金鑰自動輪替時，使 KeyVersion 成為選用項目</span><span class="sxs-lookup"><span data-stu-id="db717-1331">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="db717-1332">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="db717-1332">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="db717-1333">已修正由於管道無法移除 Azure 檔案目錄的問題</span><span class="sxs-lookup"><span data-stu-id="db717-1333">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="db717-1334">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="db717-1334">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="db717-1335">已修正 [#9880]：變更 NetWorkRule DefaultAction 值定義以符合 Swagger。</span><span class="sxs-lookup"><span data-stu-id="db717-1335">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="db717-1336">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="db717-1336">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="db717-1337">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="db717-1337">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="db717-1338">已修正 [#11624]：新增 NetworkRules 時跳過重複的規則，以避免伺服器失敗</span><span class="sxs-lookup"><span data-stu-id="db717-1338">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="db717-1339">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="db717-1339">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="db717-1340">已將 Microsoft.Azure.Cosmos.Table SDK 升級至 1.0.7</span><span class="sxs-lookup"><span data-stu-id="db717-1340">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="db717-1341">已新增警告訊息，以在清單 DataLake Gen2 項目中只傳回部分項目時，提醒使用者再次與 ContinuationToken 一起列出</span><span class="sxs-lookup"><span data-stu-id="db717-1341">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="db717-1342">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="db717-1342">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="db717-1343">已支援使用 Azure Files Active Directory 網域服務驗證來建立或更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="db717-1343">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="db717-1344">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="db717-1344">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="db717-1345">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="db717-1345">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="db717-1346">支援新增或列出儲存體帳戶的 Kerberos 金鑰</span><span class="sxs-lookup"><span data-stu-id="db717-1346">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="db717-1347">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="db717-1347">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="db717-1348">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="db717-1348">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="db717-1349">支援容錯移轉儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="db717-1349">Supported failover Storage account</span></span>
    - <span data-ttu-id="db717-1350">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="db717-1350">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="db717-1351">已更新 'Get-AzStorageBlobCopyState' 的說明</span><span class="sxs-lookup"><span data-stu-id="db717-1351">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="db717-1352">已更新 'Get-AzStorageFileCopyState' 和 'Start-AzStorageBlobCopy' 的說明</span><span class="sxs-lookup"><span data-stu-id="db717-1352">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="db717-1353">已將儲存體用戶端程式庫 v12 整合到佇列和檔案 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-1353">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="db717-1354">已將輸出類型從 CloudFile 變更為 AzureStorageFile，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="db717-1354">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="db717-1355">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="db717-1355">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="db717-1356">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="db717-1356">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="db717-1357">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="db717-1357">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="db717-1358">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="db717-1358">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="db717-1359">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="db717-1359">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="db717-1360">已將輸出類型從 CloudFileDirectory 變更為 AzureStorageFileDirectory，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="db717-1360">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="db717-1361">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="db717-1361">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="db717-1362">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="db717-1362">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="db717-1363">已將輸出類型從 CloudFileShare 變更為 AzureStorageFileShare，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="db717-1363">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="db717-1364">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="db717-1364">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="db717-1365">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="db717-1365">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="db717-1366">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="db717-1366">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="db717-1367">已將輸出類型從 FileShareProperties 變更為 AzureStorageFileShare，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="db717-1367">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="db717-1368">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="db717-1368">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="db717-1369">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="db717-1369">Az.TrafficManager</span></span>
* <span data-ttu-id="db717-1370">已修正 'DisableAzureTrafficManagerEndpoint' 詳細資訊輸出中不正確的設定檔名稱</span><span class="sxs-lookup"><span data-stu-id="db717-1370">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="db717-1371">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="db717-1371">Az.Websites</span></span>
* <span data-ttu-id="db717-1372">已修正 'Update-AzWebAppAccessRestrictionConfig' 說明上的錯字。</span><span class="sxs-lookup"><span data-stu-id="db717-1372">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="db717-1373">3.8.0 - 2020 年 4 月</span><span class="sxs-lookup"><span data-stu-id="db717-1373">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="db717-1374">上次發佈版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="db717-1374">Highlights since the last release</span></span>
* <span data-ttu-id="db717-1375">Az.Storage 支援的 PowerShell 版本：Windows PowerShell 5.1、PowerShell Core 6.2.4+、PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="db717-1375">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="db717-1376">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="db717-1376">Az.Accounts</span></span>
* <span data-ttu-id="db717-1377">更新 'Resolve-AzError' 中的 Azure PowerShell 問卷 URL [#11507]</span><span class="sxs-lookup"><span data-stu-id="db717-1377">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="db717-1378">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="db717-1378">Az.ApiManagement</span></span>
* <span data-ttu-id="db717-1379">在未來版本中新增 Azure 檔案 Cmdlet 輸出變更的重大變更通知</span><span class="sxs-lookup"><span data-stu-id="db717-1379">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="db717-1380">'Set-AzApiManagementGroup' 已更新文件以指定 GroupId 參數</span><span class="sxs-lookup"><span data-stu-id="db717-1380">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="db717-1381">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="db717-1381">Az.Cdn</span></span>
* <span data-ttu-id="db717-1382">已修正 ChinaCDN 相關的定價 SKU 顯示</span><span class="sxs-lookup"><span data-stu-id="db717-1382">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="db717-1383">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="db717-1383">Az.CognitiveServices</span></span>
* <span data-ttu-id="db717-1384">支援身分識別、加密、UserOwnedStorage</span><span class="sxs-lookup"><span data-stu-id="db717-1384">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="db717-1385">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="db717-1385">Az.Compute</span></span>
* <span data-ttu-id="db717-1386">已新增 'Set-AzVmssOrchestrationServiceState' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db717-1386">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="db717-1387">具有 -InstanceView 的 'Get-AzVmss' 會顯示 OrchestrationService 狀態。</span><span class="sxs-lookup"><span data-stu-id="db717-1387">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="db717-1388">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="db717-1388">Az.IotHub</span></span>
* <span data-ttu-id="db717-1389">管理 IoT 裝置對應項設定，新的 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="db717-1389">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="db717-1390">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="db717-1390">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="db717-1391">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="db717-1391">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="db717-1392">已新增 Cmdlet，可在 IoT 中樞的裝置上叫用直接方法。</span><span class="sxs-lookup"><span data-stu-id="db717-1392">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="db717-1393">管理 IoT 裝置模組對應項設定，新的 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="db717-1393">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="db717-1394">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="db717-1394">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="db717-1395">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="db717-1395">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="db717-1396">大規模管理 IoT 自動裝置管理設定。</span><span class="sxs-lookup"><span data-stu-id="db717-1396">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="db717-1397">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="db717-1397">New cmdlets are:</span></span>
    - <span data-ttu-id="db717-1398">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="db717-1398">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="db717-1399">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="db717-1399">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="db717-1400">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="db717-1400">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="db717-1401">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="db717-1401">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="db717-1402">已新增 Cmdlet，叫用 IoT 中樞的邊緣模組方法。</span><span class="sxs-lookup"><span data-stu-id="db717-1402">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="db717-1403">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="db717-1403">Az.KeyVault</span></span>
* <span data-ttu-id="db717-1404">已新增可在保存庫上啟用虛刪除和清除保護的新 Cmdlet 'Update-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="db717-1404">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="db717-1405">已將支援新增至 Microsoft.PowerShell.SecretManagement [#11178]</span><span class="sxs-lookup"><span data-stu-id="db717-1405">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="db717-1406">已修正 'Remove-AzKeyVaultManagedStorageSasDefinition' 範例中的錯誤 [#11479]</span><span class="sxs-lookup"><span data-stu-id="db717-1406">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="db717-1407">已將支援新增至私人端點</span><span class="sxs-lookup"><span data-stu-id="db717-1407">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="db717-1408">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="db717-1408">Az.Maintenance</span></span>
* <span data-ttu-id="db717-1409">發行用於 GA 的維護 Cmdlet 版本</span><span class="sxs-lookup"><span data-stu-id="db717-1409">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="db717-1410">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="db717-1410">Az.Monitor</span></span>
* <span data-ttu-id="db717-1411">已新增私人連結範圍的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-1411">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="db717-1412">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="db717-1412">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="db717-1413">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="db717-1413">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="db717-1414">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="db717-1414">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="db717-1415">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="db717-1415">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="db717-1416">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="db717-1416">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="db717-1417">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="db717-1417">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="db717-1418">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="db717-1418">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="db717-1419">Az.Network</span><span class="sxs-lookup"><span data-stu-id="db717-1419">Az.Network</span></span>
* <span data-ttu-id="db717-1420">已更新 Cmdlet，可在私人 IP 上啟用虛擬網路閘道的連線。</span><span class="sxs-lookup"><span data-stu-id="db717-1420">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="db717-1421">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="db717-1421">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="db717-1422">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="db717-1422">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="db717-1423">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="db717-1423">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="db717-1424">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="db717-1424">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="db717-1425">已更新 Cmdlet，可啟用以 FQDN 為基礎的 LocalNetworkGateways 和 VpnSites</span><span class="sxs-lookup"><span data-stu-id="db717-1425">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="db717-1426">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="db717-1426">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="db717-1427">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="db717-1427">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="db717-1428">已在 ExpressRouteCircuitConnectionConfig 中新增對 IPv6 位址系列的支援 (全球適用)</span><span class="sxs-lookup"><span data-stu-id="db717-1428">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="db717-1429">已新增 'Set-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="db717-1429">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="db717-1430">允許設定所有現有屬性，包括 IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="db717-1430">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="db717-1431">已更新 'Add-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="db717-1431">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="db717-1432">已新增另一個選擇性參數 AddressPrefixType 來指定位址首碼的位址系列</span><span class="sxs-lookup"><span data-stu-id="db717-1432">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="db717-1433">已更新 Cmdlet，可啟用虛擬網路閘道連線上的 DPD 逾時設定。</span><span class="sxs-lookup"><span data-stu-id="db717-1433">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="db717-1434">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="db717-1434">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="db717-1435">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="db717-1435">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="db717-1436">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="db717-1436">Az.PolicyInsights</span></span>
* <span data-ttu-id="db717-1437">已新增用於觸發原則合規性掃描的 'Start-AzPolicyComplianceScan' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-1437">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="db717-1438">已將原則定義、設定定義和指派版本新增至 'Get-AzPolicyState' 輸出</span><span class="sxs-lookup"><span data-stu-id="db717-1438">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="db717-1439">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="db717-1439">Az.ServiceFabric</span></span>
* <span data-ttu-id="db717-1440">已改善 'New-AzServiceFabricCluster' 範例的程式碼格式設定和可用性</span><span class="sxs-lookup"><span data-stu-id="db717-1440">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="db717-1441">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="db717-1441">Az.Sql</span></span>
* <span data-ttu-id="db717-1442">已新增 'Get-AzSqlInstanceOperation' 和 'Stop-AzSqlInstanceOperation' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-1442">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="db717-1443">支援對 VNet 中的儲存體帳戶進行稽核。</span><span class="sxs-lookup"><span data-stu-id="db717-1443">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="db717-1444">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="db717-1444">Az.Storage</span></span>
* <span data-ttu-id="db717-1445">在未來版本中新增 Azure 檔案 Cmdlet 輸出變更的重大變更通知</span><span class="sxs-lookup"><span data-stu-id="db717-1445">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="db717-1446">建立/更新儲存體帳戶時，支援新的 SkuName StandardGZRS、StandardRAGZRS</span><span class="sxs-lookup"><span data-stu-id="db717-1446">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="db717-1447">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="db717-1447">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="db717-1448">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="db717-1448">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="db717-1449">支援 DataLake Gen2</span><span class="sxs-lookup"><span data-stu-id="db717-1449">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="db717-1450">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="db717-1450">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="db717-1451">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="db717-1451">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="db717-1452">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="db717-1452">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="db717-1453">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="db717-1453">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="db717-1454">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="db717-1454">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="db717-1455">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="db717-1455">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="db717-1456">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="db717-1456">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="db717-1457">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="db717-1457">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="db717-1458">0.10.0-preview - 2020 年 4 月</span><span class="sxs-lookup"><span data-stu-id="db717-1458">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="db717-1459">一般</span><span class="sxs-lookup"><span data-stu-id="db717-1459">General</span></span>
* <span data-ttu-id="db717-1460">Az 模組現已在 Azure Stack Hub 中提供預覽。</span><span class="sxs-lookup"><span data-stu-id="db717-1460">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="db717-1461">此模組具有 Linux 和 macOs 的跨平台相容性。</span><span class="sxs-lookup"><span data-stu-id="db717-1461">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="db717-1462">Azure Stack Hub 現在支援使用 Az 模組的 PowerShell Core，如需詳細資訊，請參閱[這裡](/azure-stack/operator/powershell-install-az-module)</span><span class="sxs-lookup"><span data-stu-id="db717-1462">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](/azure-stack/operator/powershell-install-az-module)</span></span>
* <span data-ttu-id="db717-1463">Az 模組支援 2019-03-01-hybrid 設定檔：</span><span class="sxs-lookup"><span data-stu-id="db717-1463">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="db717-1464">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="db717-1464">Az.Billing</span></span>
  - <span data-ttu-id="db717-1465">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="db717-1465">Az.Compute</span></span>
  - <span data-ttu-id="db717-1466">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="db717-1466">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="db717-1467">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="db717-1467">Az.EventHub</span></span>
  - <span data-ttu-id="db717-1468">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="db717-1468">Az.IotHub</span></span>
  - <span data-ttu-id="db717-1469">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="db717-1469">Az.KeyVault</span></span>
  - <span data-ttu-id="db717-1470">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="db717-1470">Az.Monitor</span></span>
  - <span data-ttu-id="db717-1471">Az.Network</span><span class="sxs-lookup"><span data-stu-id="db717-1471">Az.Network</span></span>
  - <span data-ttu-id="db717-1472">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="db717-1472">Az.Resources</span></span>
  - <span data-ttu-id="db717-1473">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="db717-1473">Az.Storage</span></span>
  - <span data-ttu-id="db717-1474">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="db717-1474">Az.Websites</span></span>
* <span data-ttu-id="db717-1475">已引進三個可搭配 Azure Stack Hub 且適用於 az 的新 PowerShell 模組，包括 Az.Databox、Az.IotHub 和 Az. EventHub</span><span class="sxs-lookup"><span data-stu-id="db717-1475">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="db717-1476">命令維持不變，但有次要變更，例如將 AzureRM 變更為 Az</span><span class="sxs-lookup"><span data-stu-id="db717-1476">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="db717-1477">您可以在[這裡](/azure-stack/operator/powershell-install-az-module)找到 Azure Stack Hub 的 PowerShell 文件更新連結</span><span class="sxs-lookup"><span data-stu-id="db717-1477">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](/azure-stack/operator/powershell-install-az-module)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="db717-1478">3.7.0 - 2020 年 3 月</span><span class="sxs-lookup"><span data-stu-id="db717-1478">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="db717-1479">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="db717-1479">Az.Accounts</span></span>
* <span data-ttu-id="db717-1480">已修正 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' 在未登入時擲回 NullReferenceException [#10292]</span><span class="sxs-lookup"><span data-stu-id="db717-1480">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="db717-1481">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="db717-1481">Az.Compute</span></span>
* <span data-ttu-id="db717-1482">已將下列參數新增至 'New-AzDiskConfig' Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="db717-1482">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="db717-1483">DiskIOPSReadOnly、DiskMBpsReadOnly、MaxSharesCount、GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="db717-1483">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="db717-1484">允許 'New-AzGalleryImageVersion' Cmdlet 目標參數的加密屬性。</span><span class="sxs-lookup"><span data-stu-id="db717-1484">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="db717-1485">已修正 'Set-AzVmss' -Reimage 和 'Invoke-AzVMReimage' Cmdlet 的 tempDisk 問題。</span><span class="sxs-lookup"><span data-stu-id="db717-1485">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="db717-1486">[#11354]</span><span class="sxs-lookup"><span data-stu-id="db717-1486">[#11354]</span></span>
* <span data-ttu-id="db717-1487">已針對新的 SAP 延伸模組，將支援新增至下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-1487">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="db717-1488">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="db717-1488">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="db717-1489">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="db717-1489">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="db717-1490">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="db717-1490">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="db717-1491">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="db717-1491">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="db717-1492">已修正說明文件範例中的錯誤</span><span class="sxs-lookup"><span data-stu-id="db717-1492">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="db717-1493">以表格格式顯示 VM PowerState 的確切字串值。</span><span class="sxs-lookup"><span data-stu-id="db717-1493">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="db717-1494">'New-AzVmssConfig'：已修正當 SinglePlacementGroup 停用時 AutomaticRepairs 屬性的序列化。</span><span class="sxs-lookup"><span data-stu-id="db717-1494">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="db717-1495">[#11257]</span><span class="sxs-lookup"><span data-stu-id="db717-1495">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="db717-1496">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="db717-1496">Az.DataFactory</span></span>
* <span data-ttu-id="db717-1497">已將 ADF .Net SDK 版本更新為 4.8.0</span><span class="sxs-lookup"><span data-stu-id="db717-1497">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="db717-1498">已將選擇性參數新增至 'Invoke-AzDataFactoryV2Pipeline' 命令以支援重新執行</span><span class="sxs-lookup"><span data-stu-id="db717-1498">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="db717-1499">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="db717-1499">Az.DataLakeStore</span></span>
* <span data-ttu-id="db717-1500">已新增 'Export-AzDataLakeStoreItem' 和 'Import-AzDataLakeStoreItem' 的中斷性變更描述</span><span class="sxs-lookup"><span data-stu-id="db717-1500">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="db717-1501">已新增 'New-AzDataLakeStoreItem'、'Add-AzDAtaLakeStoreItemContent' 和 'Get-AzDAtaLakeStoreItemContent' 的位元組編碼選項</span><span class="sxs-lookup"><span data-stu-id="db717-1501">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="db717-1502">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="db717-1502">Az.HDInsight</span></span>
* <span data-ttu-id="db717-1503">支援在建立叢集時指定支援的最低 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="db717-1503">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="db717-1504">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="db717-1504">Az.IotHub</span></span>
* <span data-ttu-id="db717-1505">已新增管理每一部裝置的分散式設定支援。</span><span class="sxs-lookup"><span data-stu-id="db717-1505">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="db717-1506">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="db717-1506">New Cmdlets are:</span></span>
    - <span data-ttu-id="db717-1507">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="db717-1507">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="db717-1508">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="db717-1508">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="db717-1509">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="db717-1509">Az.KeyVault</span></span>
* <span data-ttu-id="db717-1510">已將中斷性變更屬性新增至 'New-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="db717-1510">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="db717-1511">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="db717-1511">Az.Monitor</span></span>
* <span data-ttu-id="db717-1512">已更新 'New-AzScheduledQueryRuleLogMetricTrigger' 的文件</span><span class="sxs-lookup"><span data-stu-id="db717-1512">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="db717-1513">Az.Network</span><span class="sxs-lookup"><span data-stu-id="db717-1513">Az.Network</span></span>
* <span data-ttu-id="db717-1514">已更新 Cmdlet 以允許跨租用戶 VirtualHubVnetConnections</span><span class="sxs-lookup"><span data-stu-id="db717-1514">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="db717-1515">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="db717-1515">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="db717-1516">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="db717-1516">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="db717-1517">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="db717-1517">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="db717-1518">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="db717-1518">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="db717-1519">已移除 SQL 管理 SDK 相依性</span><span class="sxs-lookup"><span data-stu-id="db717-1519">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="db717-1520">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="db717-1520">Az.PolicyInsights</span></span>
* <span data-ttu-id="db717-1521">改善錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="db717-1521">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="db717-1522">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="db717-1522">Az.RecoveryServices</span></span>
* <span data-ttu-id="db717-1523">Azure Site Recovery 已新增重新保護的支援，並且已更新 Azure 磁碟加密虛擬機器的 VM 屬性。</span><span class="sxs-lookup"><span data-stu-id="db717-1523">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="db717-1524">已新增 Azure Site Recovery VmwareToAzure 屬性 DR 監視</span><span class="sxs-lookup"><span data-stu-id="db717-1524">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="db717-1525">Azure 備份已新增針對失敗項目重試原則更新的支援。</span><span class="sxs-lookup"><span data-stu-id="db717-1525">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="db717-1526">Azure 備份已新增在備份和還原期間對磁碟排除設定的支援。</span><span class="sxs-lookup"><span data-stu-id="db717-1526">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="db717-1527">Azure 備份已新增在 AzureFileShare 中還原多個檔案/資料夾的支援</span><span class="sxs-lookup"><span data-stu-id="db717-1527">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="db717-1528">Azure 備份已新增在更新 IaasVM 原則時對使用者指定 Resourcegroup 支援的支援</span><span class="sxs-lookup"><span data-stu-id="db717-1528">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="db717-1529">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="db717-1529">Az.Resources</span></span>
* <span data-ttu-id="db717-1530">已修正 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' 以使用實際的資源 apiVersion，而不是預設 apiVersion [#11267]</span><span class="sxs-lookup"><span data-stu-id="db717-1530">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="db717-1531">已新增對於錯誤案例的 correlationId 記錄</span><span class="sxs-lookup"><span data-stu-id="db717-1531">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="db717-1532">小型文件變更為 'Get-AzResourceLock'。</span><span class="sxs-lookup"><span data-stu-id="db717-1532">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="db717-1533">已新增範例。</span><span class="sxs-lookup"><span data-stu-id="db717-1533">Added example.</span></span>
* <span data-ttu-id="db717-1534">已逸出 'Get-AzADUser' 參數值中的單引號 [#11317]</span><span class="sxs-lookup"><span data-stu-id="db717-1534">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="db717-1535">已新增部署指令碼 ('Get-AzDeploymentScript'、'Get-AzDeploymentScriptLog'、'Save-AzDeploymentScriptLog'、'Remove-AzDeploymentScript') 的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-1535">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="db717-1536">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="db717-1536">Az.Sql</span></span>
* <span data-ttu-id="db717-1537">已將可讀取次要參數新增至 'Invoke-AzSqlDatabaseFailover'</span><span class="sxs-lookup"><span data-stu-id="db717-1537">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="db717-1538">已新增 Cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="db717-1538">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="db717-1539">已儲存在資料庫中分類資料行時的敏感度等級。</span><span class="sxs-lookup"><span data-stu-id="db717-1539">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="db717-1540">Az.Support</span><span class="sxs-lookup"><span data-stu-id="db717-1540">Az.Support</span></span>
* <span data-ttu-id="db717-1541">'Az.Support' 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="db717-1541">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="db717-1542">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="db717-1542">Az.Websites</span></span>
* <span data-ttu-id="db717-1543">已透過以下新 Cmdlet 新增使用 webapp 流量路由規則的支援</span><span class="sxs-lookup"><span data-stu-id="db717-1543">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="db717-1544">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="db717-1544">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="db717-1545">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="db717-1545">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="db717-1546">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="db717-1546">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="db717-1547">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="db717-1547">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="db717-1548">3.6.1 - 2020 年 3 月</span><span class="sxs-lookup"><span data-stu-id="db717-1548">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="db717-1549">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="db717-1549">Az.Accounts</span></span>
* <span data-ttu-id="db717-1550">在 'Send-Feedback' 中開啟 Azure PowerShell 問卷頁面 [#11020]</span><span class="sxs-lookup"><span data-stu-id="db717-1550">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="db717-1551">在 'Resolve-Error' 中顯示 Azure PowerShell 問卷 URL [#11021]</span><span class="sxs-lookup"><span data-stu-id="db717-1551">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="db717-1552">已在 UserAgent 中新增 Az 版本</span><span class="sxs-lookup"><span data-stu-id="db717-1552">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="db717-1553">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="db717-1553">Az.ApiManagement</span></span>
* <span data-ttu-id="db717-1554">已新增可在 DeveloperPortal 端點上擷取和設定自訂網域的支援 [#11007]</span><span class="sxs-lookup"><span data-stu-id="db717-1554">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="db717-1555">'Export-AzApiManagementApi' 已新增以 JSON 格式下載 API 定義的支援 [#9987]</span><span class="sxs-lookup"><span data-stu-id="db717-1555">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="db717-1556">'Import-AzApiManagementApi' 已新增從 JSON 文件匯入 OpenAPI 3.0 定義的支援</span><span class="sxs-lookup"><span data-stu-id="db717-1556">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="db717-1557">'New-AzApiManagementIdentityProvider' 和 'Set-AzApiManagementIdentityProvider' 已新增為 AAD B2C 提供者設定「登入租用戶」的支援 [#9784]</span><span class="sxs-lookup"><span data-stu-id="db717-1557">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="db717-1558">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="db717-1558">Az.DataLakeStore</span></span>
* <span data-ttu-id="db717-1559">已在 csproj 和 psd1 中明確新增對 System.Buffers 的參考。</span><span class="sxs-lookup"><span data-stu-id="db717-1559">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="db717-1560">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="db717-1560">Az.IotHub</span></span>
* <span data-ttu-id="db717-1561">已新增在 IoT 中樞中管理裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="db717-1561">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="db717-1562">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="db717-1562">New Cmdlets are:</span></span>
    - <span data-ttu-id="db717-1563">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="db717-1563">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="db717-1564">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="db717-1564">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="db717-1565">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="db717-1565">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="db717-1566">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="db717-1566">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="db717-1567">已新增可在 Iot 中樞的目標 Iot 裝置上管理模組的支援。</span><span class="sxs-lookup"><span data-stu-id="db717-1567">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="db717-1568">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="db717-1568">New Cmdlets are:</span></span>
    - <span data-ttu-id="db717-1569">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="db717-1569">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="db717-1570">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="db717-1570">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="db717-1571">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="db717-1571">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="db717-1572">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="db717-1572">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="db717-1573">已新增 Cmdlet，以取得 Iot 中樞內目標 IoT 裝置的連接字串。</span><span class="sxs-lookup"><span data-stu-id="db717-1573">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="db717-1574">已新增 Cmdlet，以取得 Iot 中樞內目標 IoT 裝置上的模組連接字串。</span><span class="sxs-lookup"><span data-stu-id="db717-1574">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="db717-1575">已新增可取得/設定 IoT 裝置父系裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="db717-1575">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="db717-1576">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="db717-1576">New Cmdlets are:</span></span>
    - <span data-ttu-id="db717-1577">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="db717-1577">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="db717-1578">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="db717-1578">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="db717-1579">已新增可管理裝置父子關聯性的支援。</span><span class="sxs-lookup"><span data-stu-id="db717-1579">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="db717-1580">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="db717-1580">Az.Monitor</span></span>
* <span data-ttu-id="db717-1581">已修正 'Get-AzMetricDefinition' 的輸出值 [#9714]</span><span class="sxs-lookup"><span data-stu-id="db717-1581">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="db717-1582">Az.Network</span><span class="sxs-lookup"><span data-stu-id="db717-1582">Az.Network</span></span>
* <span data-ttu-id="db717-1583">已更新 Sql Management SDK。</span><span class="sxs-lookup"><span data-stu-id="db717-1583">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="db717-1584">已修正 PrivateLinkServiceConnectionState 類別中的命名差異問題。</span><span class="sxs-lookup"><span data-stu-id="db717-1584">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="db717-1585">將欄位 ActionsRequired 對應至 ActionRequired。</span><span class="sxs-lookup"><span data-stu-id="db717-1585">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="db717-1586">已將 PublicNetworkAccess 新增至 'New-AzSqlServer' 和 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="db717-1586">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="db717-1587">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="db717-1587">Az.Resources</span></span>
* <span data-ttu-id="db717-1588">已修正 'Get-AzRoleAssignment' 中的 Null 參考錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="db717-1588">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="db717-1589">已將 'Remove-AzADGroup' 中的 '-Force' 和 '-PassThru' 參數標記為選擇性 [#10849]</span><span class="sxs-lookup"><span data-stu-id="db717-1589">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="db717-1590">已修正 'MailNickname' 不會在 'Remove-AzADGroup' 中傳回的問題 [#11167]</span><span class="sxs-lookup"><span data-stu-id="db717-1590">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="db717-1591">已修正 'Remove-AzADGroup' 管道作業無法運作的問題 [#11171]</span><span class="sxs-lookup"><span data-stu-id="db717-1591">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="db717-1592">已修正 GetAzureRoleAssignmentCommand 中的 Null 參考錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="db717-1592">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="db717-1593">已針對原則 Cmdlet 即將來臨的變更新增重大變更屬性</span><span class="sxs-lookup"><span data-stu-id="db717-1593">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="db717-1594">已更新 'Get-AzResourceGroup' 以在伺服器端執行資源群組標籤篩選</span><span class="sxs-lookup"><span data-stu-id="db717-1594">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="db717-1595">已擴充標籤 Cmdlet 以接受 -ResourceId</span><span class="sxs-lookup"><span data-stu-id="db717-1595">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="db717-1596">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="db717-1596">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="db717-1597">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="db717-1597">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="db717-1598">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="db717-1598">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="db717-1599">已新增標籤 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-1599">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="db717-1600">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="db717-1600">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="db717-1601">從 SDK 3.3.0 引進 ScopedDeployment</span><span class="sxs-lookup"><span data-stu-id="db717-1601">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="db717-1602">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="db717-1602">Az.Sql</span></span>
* <span data-ttu-id="db717-1603">已將 PublicNetworkAccess 新增至 'New-AzSqlServer' 和 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="db717-1603">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="db717-1604">已針對受控資料庫新增對於長期保留備份設定的支援</span><span class="sxs-lookup"><span data-stu-id="db717-1604">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="db717-1605">在受控資料庫上取得/設定 LTR 原則</span><span class="sxs-lookup"><span data-stu-id="db717-1605">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="db717-1606">依受控資料庫、受控執行個體或位置取得 LTR 備份</span><span class="sxs-lookup"><span data-stu-id="db717-1606">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="db717-1607">移除 LTR 備份</span><span class="sxs-lookup"><span data-stu-id="db717-1607">Remove an LTR backup</span></span>
    - <span data-ttu-id="db717-1608">還原 LTR 備份以建立新的受控資料庫</span><span class="sxs-lookup"><span data-stu-id="db717-1608">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="db717-1609">已將 MinimalTlsVersion 新增至 New-AzSqlServer 和 Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="db717-1609">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="db717-1610">已將 MinimalTlsVersion 新增至 New-AzSqlInstance 和 Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="db717-1610">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="db717-1611">已提高適用於 Az.Network 的 SQL SDK 版本</span><span class="sxs-lookup"><span data-stu-id="db717-1611">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="db717-1612">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="db717-1612">Az.Storage</span></span>
* <span data-ttu-id="db717-1613">已在 ImmutabilityPolicy 中支援 AllowProtectedAppendWrite</span><span class="sxs-lookup"><span data-stu-id="db717-1613">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="db717-1614">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="db717-1614">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="db717-1615">已針對未來版本中的 AzureStorageTable 類型變更新增重大變更警告訊息</span><span class="sxs-lookup"><span data-stu-id="db717-1615">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="db717-1616">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="db717-1616">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="db717-1617">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="db717-1617">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="db717-1618">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="db717-1618">Az.Websites</span></span>
* <span data-ttu-id="db717-1619">已為 'New-AzAppServicePlan' 和 'Set-AzAppServicePlan' 新增標籤參數</span><span class="sxs-lookup"><span data-stu-id="db717-1619">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="db717-1620">將自訂網域新增至網站時如果擲回例外狀況，則會停止執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-1620">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="db717-1621">已新增支援而可針對未和 App Service 方案位於相同資源群組中的 App Service 執行作業</span><span class="sxs-lookup"><span data-stu-id="db717-1621">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="db717-1622">已將存取限制套用至不同資源群組中的 WebApp/函式</span><span class="sxs-lookup"><span data-stu-id="db717-1622">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="db717-1623">已修正為 WebAppSlots 設定自訂主機名稱的問題</span><span class="sxs-lookup"><span data-stu-id="db717-1623">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="db717-1624">3.5.0 - 2020 年 2 月</span><span class="sxs-lookup"><span data-stu-id="db717-1624">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="db717-1625">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="db717-1625">Highlights since the last major release</span></span>
* <span data-ttu-id="db717-1626">更新用戶端遙測。</span><span class="sxs-lookup"><span data-stu-id="db717-1626">Updated client side telemetry.</span></span>
* <span data-ttu-id="db717-1627">Az.IotHub 已新增 Cmdlet 來支援裝置管理。</span><span class="sxs-lookup"><span data-stu-id="db717-1627">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="db717-1628">Az.SqlVirtualMachine 已新增用於可用性群組接聽程式的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db717-1628">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="db717-1629">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="db717-1629">Az.Accounts</span></span>
* <span data-ttu-id="db717-1630">已將 SubscriptionId、TenantId 和執行時間新增至用戶端遙測的資料</span><span class="sxs-lookup"><span data-stu-id="db717-1630">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="db717-1631">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="db717-1631">Az.Automation</span></span>
* <span data-ttu-id="db717-1632">已修正 'New-AzAutomationSoftwareUpdateConfiguration' 參考文件中範例 1 的錯字</span><span class="sxs-lookup"><span data-stu-id="db717-1632">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="db717-1633">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="db717-1633">Az.CognitiveServices</span></span>
* <span data-ttu-id="db717-1634">已將 SDK 更新至 7.0</span><span class="sxs-lookup"><span data-stu-id="db717-1634">Updated SDK to 7.0</span></span>
* <span data-ttu-id="db717-1635">已改善伺服器回應空白主體時的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="db717-1635">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="db717-1636">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="db717-1636">Az.Compute</span></span>
* <span data-ttu-id="db717-1637">已允許 ProximityPlacementGroupId 在更新期間為空白值</span><span class="sxs-lookup"><span data-stu-id="db717-1637">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="db717-1638">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="db717-1638">Az.FrontDoor</span></span>
* <span data-ttu-id="db717-1639">已新增 Cmdlet 來取得可在 WAF 中使用的受控規則定義</span><span class="sxs-lookup"><span data-stu-id="db717-1639">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="db717-1640">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="db717-1640">Az.IotHub</span></span>
* <span data-ttu-id="db717-1641">已新增在 IoT 中樞中管理裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="db717-1641">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="db717-1642">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="db717-1642">New Cmdlets are:</span></span>
    - <span data-ttu-id="db717-1643">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="db717-1643">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="db717-1644">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="db717-1644">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="db717-1645">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="db717-1645">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="db717-1646">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="db717-1646">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="db717-1647">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="db717-1647">Az.KeyVault</span></span>
* <span data-ttu-id="db717-1648">已修正 Add-AzKeyVaultKey.md 的重複文字</span><span class="sxs-lookup"><span data-stu-id="db717-1648">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="db717-1649">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="db717-1649">Az.Monitor</span></span>
* <span data-ttu-id="db717-1650">已修正 Get-AzLog Cmdlet 的描述。</span><span class="sxs-lookup"><span data-stu-id="db717-1650">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="db717-1651">已將名為 ActionGroupI 的新參數新增至 'New-AzMetricAlertRuleV2' 命令。</span><span class="sxs-lookup"><span data-stu-id="db717-1651">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="db717-1652">使用者可以提供 ActionGroupId(string) 或 ActionGorup(ActivityLogAlertActionGroup)。</span><span class="sxs-lookup"><span data-stu-id="db717-1652">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="db717-1653">Az.Network</span><span class="sxs-lookup"><span data-stu-id="db717-1653">Az.Network</span></span>
* <span data-ttu-id="db717-1654">已為 'New-AzPrivateLinkService' Cmdlet 的參數 '-EnableProxyProtocol' 新增一個額外的參數附註。</span><span class="sxs-lookup"><span data-stu-id="db717-1654">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="db717-1655">已修正 Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 和 Start-AzVirtualnetworkGatewayPacketCapture.md 中的 FilterData 範例。</span><span class="sxs-lookup"><span data-stu-id="db717-1655">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="db717-1656">已新增封包擷取範例，可在 Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 和 Start-AzVirtualnetworkGatewayPacketCapture.md 中擷取所有內部和外部封包。</span><span class="sxs-lookup"><span data-stu-id="db717-1656">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="db717-1657">支援 VNet 防火牆上的 Azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="db717-1657">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="db717-1658">未新增任何 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db717-1658">No new cmdlets are added.</span></span> <span data-ttu-id="db717-1659">放寬 VNet 防火牆上的防火牆原則限制</span><span class="sxs-lookup"><span data-stu-id="db717-1659">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="db717-1660">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="db717-1660">Az.RecoveryServices</span></span>
* <span data-ttu-id="db717-1661">已為 SQL Database 新增「還原為檔案」支援。</span><span class="sxs-lookup"><span data-stu-id="db717-1661">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="db717-1662">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="db717-1662">Az.Resources</span></span>
* <span data-ttu-id="db717-1663">已重構範本部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-1663">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="db717-1664">已新增用於在管理群組上管理部署的 Cmdlet：\*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="db717-1664">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="db717-1665">已新增用於在租用戶範圍上管理部署的 Cmdlet：\*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="db717-1665">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="db717-1666">已重構 \*-AzDeployment Cmdlet，以便在特定訂用帳戶範圍內工作</span><span class="sxs-lookup"><span data-stu-id="db717-1666">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="db717-1667">為 \*-AzDeployment Cmdlet 建立別名 \*-AzSubscriptionDeployment</span><span class="sxs-lookup"><span data-stu-id="db717-1667">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="db717-1668">已修正未設定參數 'AvailableToOtherTenants' 時的 'Update-AzADApplication'</span><span class="sxs-lookup"><span data-stu-id="db717-1668">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="db717-1669">已移除 ApplicationObjectWithoutCredentialParameterSet 來避免 AmbiguousParameterSetException。</span><span class="sxs-lookup"><span data-stu-id="db717-1669">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="db717-1670">已重新產生說明檔</span><span class="sxs-lookup"><span data-stu-id="db717-1670">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="db717-1671">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="db717-1671">Az.Sql</span></span>
* <span data-ttu-id="db717-1672">已在受控執行個體上新增跨訂用帳戶的時間點還原支援。</span><span class="sxs-lookup"><span data-stu-id="db717-1672">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="db717-1673">已新增變更現有 SQL 受控執行個體硬體世代的支援</span><span class="sxs-lookup"><span data-stu-id="db717-1673">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="db717-1674">已修正 'Update-AzSqlServerVulnerabilityAssessmentSetting' 說明範例：parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="db717-1674">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="db717-1675">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="db717-1675">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="db717-1676">已新增用於可用性群組接聽程式的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-1676">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="db717-1677">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="db717-1677">Az.StorageSync</span></span>
* <span data-ttu-id="db717-1678">已更新 'Invoke-AzStorageSyncCompatibilityCheck' 中支援的字元集。</span><span class="sxs-lookup"><span data-stu-id="db717-1678">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="db717-1679">3.4.0 - 2020 年 2 月</span><span class="sxs-lookup"><span data-stu-id="db717-1679">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="db717-1680">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="db717-1680">Highlights since the last major release</span></span>
* <span data-ttu-id="db717-1681">Az.CosmosDB 初始版本 0.1.0 已發行</span><span class="sxs-lookup"><span data-stu-id="db717-1681">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="db717-1682">Az.Network ConnectionMonitor V2 支援已新增</span><span class="sxs-lookup"><span data-stu-id="db717-1682">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="db717-1683">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="db717-1683">Az.Accounts</span></span>
* <span data-ttu-id="db717-1684">當 AzureRmContext.json 無法使用時，停用內容自動儲存</span><span class="sxs-lookup"><span data-stu-id="db717-1684">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="db717-1685">將 Azure Powershell Common 的參考更新至 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="db717-1685">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="db717-1686">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="db717-1686">Az.ApiManagement</span></span>
* <span data-ttu-id="db717-1687">**Get-AzApiManagementApiSchema** 已修正取得與 API 相關聯的 Open-Api 結構描述   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="db717-1687">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="db717-1688">**New-AzApiManagementProduct** _ 和 _ *Set-AzApiManagementProduct*\*</span><span class="sxs-lookup"><span data-stu-id="db717-1688">**New-AzApiManagementProduct** _ and _ *Set-AzApiManagementProduct*\*</span></span>
  - <span data-ttu-id="db717-1689"> https://github.com/Azure/azure-powershell/issues/10472 的修正文件</span><span class="sxs-lookup"><span data-stu-id="db717-1689">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="db717-1690">**Set-AzApiManagementApi** 新增的範例，示範如何使用 Cmdlet 來更新 ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="db717-1690">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="db717-1691">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="db717-1691">Az.Compute</span></span>
* <span data-ttu-id="db717-1692">將 VM 狀態的數目限制為 100，以避免在沒有 VM 名稱的情況下執行 Get-AzVM -Status 時進行節流。</span><span class="sxs-lookup"><span data-stu-id="db717-1692">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="db717-1693">新增 Update-AzDiskEncryptionSet Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-1693">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="db717-1694">將 EncryptionType 和 DiskEncryptionSetId 參數新增至下列 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="db717-1694">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="db717-1695">New-AzDiskUpdateConfig、New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="db717-1695">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="db717-1696">將 ColocationStatus 參數新增至 Get-AzProximityPlacementGroup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db717-1696">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="db717-1697">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="db717-1697">Az.DataFactory</span></span>
* <span data-ttu-id="db717-1698">將 ADF .Net SDK 版本更新為 4.7.0</span><span class="sxs-lookup"><span data-stu-id="db717-1698">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="db717-1699">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="db717-1699">Az.DeploymentManager</span></span>
* <span data-ttu-id="db717-1700">新增資源的 LIST 作業</span><span class="sxs-lookup"><span data-stu-id="db717-1700">Adds LIST operations for resources</span></span>
* <span data-ttu-id="db717-1701">新增執行健康情況檢查步驟作業的功能</span><span class="sxs-lookup"><span data-stu-id="db717-1701">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="db717-1702">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="db717-1702">Az.HDInsight</span></span>
* <span data-ttu-id="db717-1703">修正 New-AzHDInsightCluster 的文件錯誤。</span><span class="sxs-lookup"><span data-stu-id="db717-1703">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="db717-1704">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="db717-1704">Az.KeyVault</span></span>
* <span data-ttu-id="db717-1705">將 Name 別名新增至 VaultName 屬性，使 Remove-AzureKeyVault 與 New-AzureKeyVault 一致。</span><span class="sxs-lookup"><span data-stu-id="db717-1705">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="db717-1706">Az.Network</span><span class="sxs-lookup"><span data-stu-id="db717-1706">Az.Network</span></span>
* <span data-ttu-id="db717-1707">新增至 Set-AzNetworkWatcherConfigFlowLog.md 以示範流量分析停用案例的新範例。</span><span class="sxs-lookup"><span data-stu-id="db717-1707">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="db717-1708">新增將管理 IP 設定指派給 Azure 防火牆的支援 - 防火牆將用於其管理流量的專用子網路和公用 IP</span><span class="sxs-lookup"><span data-stu-id="db717-1708">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="db717-1709">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="db717-1709">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="db717-1710">已新增可接受公用 IP 位址物件的參數 -ManagementPublicIpAddress (非強制)</span><span class="sxs-lookup"><span data-stu-id="db717-1710">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="db717-1711">已在防火牆物件上新增方法 SetManagementIpConfiguration - 需要子網路和公用 IP 位址作為輸入 - 子網路名稱必須是 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="db717-1711">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="db717-1712">已更正 Get-AzNetworkSecurityGroup 範例，以顯示 NSG (不是網路介面) 的範例。</span><span class="sxs-lookup"><span data-stu-id="db717-1712">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="db717-1713">已修正 New-AzVpnSite 命令中，導致資源識別碼完成器無法完成參數的錯字。</span><span class="sxs-lookup"><span data-stu-id="db717-1713">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="db717-1714">已在應用程式閘道中新增重寫規則動作集內 URL 設定的支援</span><span class="sxs-lookup"><span data-stu-id="db717-1714">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="db717-1715">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="db717-1715">New cmdlets added:</span></span>
        - <span data-ttu-id="db717-1716">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="db717-1716">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="db717-1717">使用選擇性參數 UrlConfiguration 更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-1717">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="db717-1718">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="db717-1718">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="db717-1719">新增對於 NetworkWatcher ConnectionMonitor 第 2 版資源的支援</span><span class="sxs-lookup"><span data-stu-id="db717-1719">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="db717-1720">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="db717-1720">Az.PolicyInsights</span></span>
* <span data-ttu-id="db717-1721">支援在決定要補救的資源之前，評估合規性</span><span class="sxs-lookup"><span data-stu-id="db717-1721">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="db717-1722">將 '-ResourceDiscoverMode' 參數新增至 Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="db717-1722">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="db717-1723">新增 Get-AzPolicyMetadata Cmdlet 以取得原則中繼資料資源</span><span class="sxs-lookup"><span data-stu-id="db717-1723">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="db717-1724">已更新 API 版本 2019-10-01 的 Get-AzPolicyState 和 Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="db717-1724">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="db717-1725">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="db717-1725">Az.RecoveryServices</span></span>
* <span data-ttu-id="db717-1726">Azure Site Recovery 支援移除已複寫的磁碟。</span><span class="sxs-lookup"><span data-stu-id="db717-1726">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="db717-1727">Azure 備份在建立復原服務保存庫時新增了新增標記的支援。</span><span class="sxs-lookup"><span data-stu-id="db717-1727">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="db717-1728">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="db717-1728">Az.Resources</span></span>
* <span data-ttu-id="db717-1729">以內容訂閱的預設值，讓 \*-AzPolicyAssignment Cmdlet 中的 -Scope 成為選擇性</span><span class="sxs-lookup"><span data-stu-id="db717-1729">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="db717-1730">新增使用密碼和金鑰認證建立 ADServicePrincipal 的範例</span><span class="sxs-lookup"><span data-stu-id="db717-1730">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="db717-1731">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="db717-1731">Az.Sql</span></span>
<span data-ttu-id="db717-1732">修正 New-AzSqlDatabaseSecondary Cmdlet 來檢查 PartnerDatabaseName 是否存在，而不是 DatabaseName 是否存在。</span><span class="sxs-lookup"><span data-stu-id="db717-1732">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="db717-1733">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="db717-1733">Az.Storage</span></span>
* <span data-ttu-id="db717-1734">支援在建立儲存體帳戶中設定資料表/佇列加密 Keytype</span><span class="sxs-lookup"><span data-stu-id="db717-1734">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="db717-1735">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="db717-1735">New-AzStorageAccount</span></span>
* <span data-ttu-id="db717-1736">在 StorageException 沒有 ExtendedErrorInformation 時顯示 RequestId</span><span class="sxs-lookup"><span data-stu-id="db717-1736">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="db717-1737">修正 Cmdlet Start-AzStorageBlobCopy 的範例 6</span><span class="sxs-lookup"><span data-stu-id="db717-1737">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="db717-1738">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="db717-1738">Az.Websites</span></span>
* <span data-ttu-id="db717-1739">Set-AzWebapp 和 Set-AzWebappSlot 支援 AlwaysOn、MinTls 和 FtpsState 屬性</span><span class="sxs-lookup"><span data-stu-id="db717-1739">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="db717-1740">修正在使用單一 Set-AzWebApp 命令的同時設定 HttpsOnly 和變更 AppservicePlan，將 HttpsOnly 重設為預設值的問題</span><span class="sxs-lookup"><span data-stu-id="db717-1740">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="db717-1741">3.3.0 - 2020 年 1 月</span><span class="sxs-lookup"><span data-stu-id="db717-1741">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="db717-1742">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="db717-1742">Az.Accounts</span></span>
* <span data-ttu-id="db717-1743">已更新 Add-AzEnvironment 和 Set-AzEnvironment 以接受 AzureAttestationServiceEndpointResourceId 和 AzureAttestationServiceEndpointSuffix 參數</span><span class="sxs-lookup"><span data-stu-id="db717-1743">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="db717-1744">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="db717-1744">Az.Cdn</span></span>
* <span data-ttu-id="db717-1745">在 New-AzCdnEndpoint Cmdlet 中顯示錯誤回應詳細資料</span><span class="sxs-lookup"><span data-stu-id="db717-1745">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="db717-1746">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="db717-1746">Az.Compute</span></span>
* <span data-ttu-id="db717-1747">修正具有受控 OD 磁碟 (沒有 OS 設定檔) 之 VM 的 Set-AzVMCustomScriptExtension Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db717-1747">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="db717-1748">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="db717-1748">Az.ContainerInstance</span></span>
* <span data-ttu-id="db717-1749">修正了 New-AzContainerGroup 範例所使用的參數名稱</span><span class="sxs-lookup"><span data-stu-id="db717-1749">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="db717-1750">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="db717-1750">Az.DataBoxEdge</span></span>
* <span data-ttu-id="db717-1751">新增了 Cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="db717-1751">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="db717-1752">取得 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="db717-1752">Get the Edge Storage Container</span></span>
* <span data-ttu-id="db717-1753">新增了 Cmdlet 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="db717-1753">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="db717-1754">建立新的 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="db717-1754">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="db717-1755">新增了 Cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="db717-1755">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="db717-1756">移除 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="db717-1756">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="db717-1757">新增了 Cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="db717-1757">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="db717-1758">用來重新整理 Edge 儲存體容器資料的叫用動作</span><span class="sxs-lookup"><span data-stu-id="db717-1758">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="db717-1759">新增了 Cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="db717-1759">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="db717-1760">取得 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="db717-1760">Get the Edge Storage Account</span></span>
* <span data-ttu-id="db717-1761">新增了 Cmdlet 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="db717-1761">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="db717-1762">建立新的 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="db717-1762">Create new Edge Storage Account</span></span>
* <span data-ttu-id="db717-1763">新增了 Cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="db717-1763">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="db717-1764">移除 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="db717-1764">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="db717-1765">叫用 Cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="db717-1765">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="db717-1766">用來重新整理共用資料的叫用動作</span><span class="sxs-lookup"><span data-stu-id="db717-1766">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="db717-1767">新增了 Cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="db717-1767">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="db717-1768">設定 az databoxedge 儲存體帳戶憑證</span><span class="sxs-lookup"><span data-stu-id="db717-1768">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="db717-1769">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="db717-1769">Az.DataFactory</span></span>
* <span data-ttu-id="db717-1770">新增適用於 Get-AzDataFactoryV2IntegrationRuntime Cmd 的 AutoUpdateETA、LatestVersion、PushedVersion、TaskQueueId 和 VersionStatus 屬性</span><span class="sxs-lookup"><span data-stu-id="db717-1770">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="db717-1771">將 ADF .Net SDK 版本更新為 4.6.0</span><span class="sxs-lookup"><span data-stu-id="db717-1771">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="db717-1772">為 'Set-AzureRmDataFactoryV2IntegrationRuntime' Cmd 新增參數 'PublicIPs'，以使用靜態公用 IP 位址建立 Azure-SSIS IR。</span><span class="sxs-lookup"><span data-stu-id="db717-1772">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="db717-1773">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="db717-1773">Az.DevTestLabs</span></span>
* <span data-ttu-id="db717-1774">移除 Get-AzDtlAllowedVMSizesPolicy.md 中中斷的連結</span><span class="sxs-lookup"><span data-stu-id="db717-1774">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="db717-1775">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="db717-1775">Az.EventHub</span></span>
* <span data-ttu-id="db717-1776">問題 10634 的修正內容：修正 Null 物件參考以移除 eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="db717-1776">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="db717-1777">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="db717-1777">Az.HDInsight</span></span>
* <span data-ttu-id="db717-1778">修正 Invoke-AzHDInsightHiveJob.md 錯誤。</span><span class="sxs-lookup"><span data-stu-id="db717-1778">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="db717-1779">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="db717-1779">Az.MachineLearning</span></span>
* <span data-ttu-id="db717-1780">由於不再提供 MachineLearningCompute，已移除下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-1780">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="db717-1781">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="db717-1781">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="db717-1782">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="db717-1782">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="db717-1783">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="db717-1783">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="db717-1784">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="db717-1784">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="db717-1785">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="db717-1785">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="db717-1786">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="db717-1786">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="db717-1787">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="db717-1787">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="db717-1788">Az.Network</span><span class="sxs-lookup"><span data-stu-id="db717-1788">Az.Network</span></span>
* <span data-ttu-id="db717-1789">將 Microsoft.Azure.Management.Sql 相依性從 1.36-preview 升級到 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="db717-1789">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="db717-1790">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="db717-1790">Az.RecoveryServices</span></span>
* <span data-ttu-id="db717-1791">Azure Site Recovery 對使用 Azure 至 Azure 提供者的客戶受控金鑰進行待用加密的受控磁碟 VM 支援變更。</span><span class="sxs-lookup"><span data-stu-id="db717-1791">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="db717-1792">Azure Site Recovery 支援將磁碟加密集識別碼輸入為選擇性輸入，以啟用 VMware 至 Azure 的保護。</span><span class="sxs-lookup"><span data-stu-id="db717-1792">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="db717-1793">Azure Site Recovery 支援將磁碟加密集識別碼輸入為磁碟層級的選擇性輸入，以啟用 VMware 至 Azure 的保護。</span><span class="sxs-lookup"><span data-stu-id="db717-1793">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="db717-1794">Azure Site Recovery 支援以將適用於 HyperV 的磁碟加密集對應更新至 Azure 的複寫受保護項目。</span><span class="sxs-lookup"><span data-stu-id="db717-1794">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="db717-1795">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="db717-1795">Az.Resources</span></span>
* <span data-ttu-id="db717-1796">修正 'Remove-AzTag' 說明文件中的錯誤。</span><span class="sxs-lookup"><span data-stu-id="db717-1796">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="db717-1797">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="db717-1797">Az.Sql</span></span>
* <span data-ttu-id="db717-1798">修正弱點評定設定基準 Cmdlet 功能，以在 Azure 資料庫的主要資料庫中運作，並在受控執行個體系統資料庫中加以限制。</span><span class="sxs-lookup"><span data-stu-id="db717-1798">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="db717-1799">修正建立 SQL 執行個體容錯移轉群組時的錯誤</span><span class="sxs-lookup"><span data-stu-id="db717-1799">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="db717-1800">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="db717-1800">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="db717-1801">將 DR 新增為新的有效授權類型</span><span class="sxs-lookup"><span data-stu-id="db717-1801">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="db717-1802">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="db717-1802">Az.Storage</span></span>
* <span data-ttu-id="db717-1803">在後續版本中新增 DefaultAction 值變更的重大變更警告訊息</span><span class="sxs-lookup"><span data-stu-id="db717-1803">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="db717-1804">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="db717-1804">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="db717-1805">使用參數 -IncludeGeoReplicationStats 執行 get-AzureRMStorageAccount，支援取得儲存體帳戶的上次同步處理時間</span><span class="sxs-lookup"><span data-stu-id="db717-1805">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="db717-1806">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="db717-1806">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="db717-1807">3.2.0 - 2019 年 12 月</span><span class="sxs-lookup"><span data-stu-id="db717-1807">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="db717-1808">一般</span><span class="sxs-lookup"><span data-stu-id="db717-1808">General</span></span>
* <span data-ttu-id="db717-1809">更新 .psd1 中的更新參考，以便所有模組均可使用相對路徑</span><span class="sxs-lookup"><span data-stu-id="db717-1809">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="db717-1810">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="db717-1810">Az.Accounts</span></span>
* <span data-ttu-id="db717-1811">針對 Az 4.0 預覽的用戶端遙測設定正確的 UserAgent</span><span class="sxs-lookup"><span data-stu-id="db717-1811">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="db717-1812">當 Az 4.0 預覽中的內容為 null 時，顯示使用者易記的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="db717-1812">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="db717-1813">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="db717-1813">Az.Batch</span></span>
* <span data-ttu-id="db717-1814">修正問題 [#10602](https://github.com/Azure/azure-powershell/issues/10602)，其中 **New-AzBatchPool** 並未適當地將 'VirtualMachineConfiguration.ContainerConfiguration' 或 'VirtualMachineConfiguration.DataDisks' 傳送到伺服器。</span><span class="sxs-lookup"><span data-stu-id="db717-1814">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="db717-1815">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="db717-1815">Az.DataFactory</span></span>
* <span data-ttu-id="db717-1816">將 ADF .Net SDK 版本更新為 4.5.0</span><span class="sxs-lookup"><span data-stu-id="db717-1816">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="db717-1817">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="db717-1817">Az.FrontDoor</span></span>
* <span data-ttu-id="db717-1818">已新增 WAF 受控規則排除支援</span><span class="sxs-lookup"><span data-stu-id="db717-1818">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="db717-1819">在自動完成中新增 SocketAddr</span><span class="sxs-lookup"><span data-stu-id="db717-1819">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="db717-1820">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="db717-1820">Az.HealthcareApis</span></span>
* <span data-ttu-id="db717-1821">例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="db717-1821">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="db717-1822">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="db717-1822">Az.KeyVault</span></span>
* <span data-ttu-id="db717-1823">已修正存取可能未設定的值時發生的錯誤</span><span class="sxs-lookup"><span data-stu-id="db717-1823">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="db717-1824">橢圓曲線密碼編譯憑證管理</span><span class="sxs-lookup"><span data-stu-id="db717-1824">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="db717-1825">已新增為憑證原則指定 Curve 的支援</span><span class="sxs-lookup"><span data-stu-id="db717-1825">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="db717-1826">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="db717-1826">Az.Monitor</span></span>
* <span data-ttu-id="db717-1827">在 Add Diagnostic Settings 命令中新增選用的引數。</span><span class="sxs-lookup"><span data-stu-id="db717-1827">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="db717-1828">如果存在切換引數，表示匯出到 Log Analytics 必須是固定的結構描述 (也稱為</span><span class="sxs-lookup"><span data-stu-id="db717-1828">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="db717-1829">專用，資料類型)</span><span class="sxs-lookup"><span data-stu-id="db717-1829">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="db717-1830">Az.Network</span><span class="sxs-lookup"><span data-stu-id="db717-1830">Az.Network</span></span>
* <span data-ttu-id="db717-1831">在 AzureFirewall 應用程式、Nat 和網路規則中支援 IpGroups。</span><span class="sxs-lookup"><span data-stu-id="db717-1831">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="db717-1832">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="db717-1832">Az.Resources</span></span>
* <span data-ttu-id="db717-1833">修正如果範本名稱與一些內建參數名稱衝突，則範本部署無法讀取範本參數的問題。</span><span class="sxs-lookup"><span data-stu-id="db717-1833">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="db717-1834">更新原則 Cmdliet 以使用新的 API 版本 2019-09-01，其中引進原則集合定義內的群組支援。</span><span class="sxs-lookup"><span data-stu-id="db717-1834">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="db717-1835">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="db717-1835">Az.Sql</span></span>
* <span data-ttu-id="db717-1836">已將弱點評估自動啟用中的儲存體建立升級為 StorageV2</span><span class="sxs-lookup"><span data-stu-id="db717-1836">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="db717-1837">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="db717-1837">Az.Storage</span></span>
* <span data-ttu-id="db717-1838">支援使用以 Oauth 驗證為基礎的儲存體內容來產生 Blob/Constainer Idenity 為基礎的 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="db717-1838">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="db717-1839">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="db717-1839">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="db717-1840">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="db717-1840">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="db717-1841">支援撤銷儲存體帳戶使用者委派金鑰，因此會撤銷所有 Idenity SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="db717-1841">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="db717-1842">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="db717-1842">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="db717-1843">升級至 Microsoft.Azure.Management.Storage 14.2.0，以支援新的 API 版本 2019-06-01。</span><span class="sxs-lookup"><span data-stu-id="db717-1843">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="db717-1844">針對檔案共用 Cmdlet 的管理平面中超過 5120 的值支援 QuotaGiB (Gibibye 中的共用配額)，並將 'Quota' 參數別名新增到 'QuotaGiB' 參數中。</span><span class="sxs-lookup"><span data-stu-id="db717-1844">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="db717-1845">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="db717-1845">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="db717-1846">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="db717-1846">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="db717-1847">在參數 'Quota' 中新增參數別名 'QuotaGiB'</span><span class="sxs-lookup"><span data-stu-id="db717-1847">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="db717-1848">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="db717-1848">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="db717-1849">修正 Set-AzStorageContainerAcl 可清除已儲存之存取原則的問題。</span><span class="sxs-lookup"><span data-stu-id="db717-1849">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="db717-1850">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="db717-1850">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="db717-1851">3.1.0 - 2019 年 11 月</span><span class="sxs-lookup"><span data-stu-id="db717-1851">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="db717-1852">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="db717-1852">Highlights since the last major release</span></span>
* <span data-ttu-id="db717-1853">已發佈 Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="db717-1853">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="db717-1854">已發佈 Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="db717-1854">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="db717-1855">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="db717-1855">Az.Compute</span></span>
* <span data-ttu-id="db717-1856">VM Reapply 功能</span><span class="sxs-lookup"><span data-stu-id="db717-1856">VM Reapply feature</span></span>
    - <span data-ttu-id="db717-1857">將 Reapply 參數新增到 Set-AzVM Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-1857">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="db717-1858">VM 擴展集 AutomaticRepairs 功能：</span><span class="sxs-lookup"><span data-stu-id="db717-1858">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="db717-1859">將 EnableAutomaticRepair、AutomaticRepairGracePeriod 和 AutomaticRepairMaxInstanceRepairsPercent 參數新增到下列 Cmdlet： New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="db717-1859">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="db717-1860">適用於 New-AzVM 的跨租用戶資源庫映像支援</span><span class="sxs-lookup"><span data-stu-id="db717-1860">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="db717-1861">將 'Spot' 新增到 New-AzVM、New-AzVMConfig 和 New-AzVmss Cmdlet 中的 Priority 參數引數完成程式</span><span class="sxs-lookup"><span data-stu-id="db717-1861">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="db717-1862">將 DiskIOPSReadWrite 和 DiskMBpsReadWrite 參數新增到 Add-AzVmssDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-1862">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="db717-1863">將 New-AzGalleryImageVersion Cmdlet 的 SourceImageId 參數變更為選擇性</span><span class="sxs-lookup"><span data-stu-id="db717-1863">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="db717-1864">將 OSDiskImage 和 DataDiskImage 參數新增到 New-AzGalleryImageVersion Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-1864">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="db717-1865">將 HyperVGeneration 參數新增到 New-AzGalleryImageDefinition Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-1865">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="db717-1866">將 SkipExtensionsOnOverprovisionedVMs 參數新增到 New-AzVmss、New-AzVmssConfig 和 Update-AzVmss Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-1866">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="db717-1867">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="db717-1867">Az.DataBoxEdge</span></span>
* <span data-ttu-id="db717-1868">已新增 Cmdlet `Get-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="db717-1868">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="db717-1869">取得訂單</span><span class="sxs-lookup"><span data-stu-id="db717-1869">Get the Order</span></span>
* <span data-ttu-id="db717-1870">已新增 Cmdlet `New-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="db717-1870">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="db717-1871">建立新訂單</span><span class="sxs-lookup"><span data-stu-id="db717-1871">Create new Order</span></span>
* <span data-ttu-id="db717-1872">已新增 Cmdlet `Remove-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="db717-1872">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="db717-1873">移除訂單</span><span class="sxs-lookup"><span data-stu-id="db717-1873">Remove the Order</span></span>
* <span data-ttu-id="db717-1874">Cmdlet `New-AzDataBoxEdgeShare` 中的變更</span><span class="sxs-lookup"><span data-stu-id="db717-1874">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="db717-1875">立即建立本機共用</span><span class="sxs-lookup"><span data-stu-id="db717-1875">Now creates Local Share</span></span>
* <span data-ttu-id="db717-1876">已新增 Cmdlet `Set-AzDataBoxEdgeRole`</span><span class="sxs-lookup"><span data-stu-id="db717-1876">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="db717-1877">IotRole 現在對應到共用</span><span class="sxs-lookup"><span data-stu-id="db717-1877">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="db717-1878">已新增 Cmdlet `Invoke-AzDataBoxEdgeDevice`</span><span class="sxs-lookup"><span data-stu-id="db717-1878">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="db717-1879">在裝置上叫用掃描更新、下載更新並安裝更新</span><span class="sxs-lookup"><span data-stu-id="db717-1879">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="db717-1880">已新增 Cmdlet `Get-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="db717-1880">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="db717-1881">取得觸發程序的相關資訊</span><span class="sxs-lookup"><span data-stu-id="db717-1881">Gets the information about Triggers</span></span>
* <span data-ttu-id="db717-1882">已新增 Cmdlet `New-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="db717-1882">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="db717-1883">建立新的觸發程序</span><span class="sxs-lookup"><span data-stu-id="db717-1883">Create new Triggers</span></span>
* <span data-ttu-id="db717-1884">已新增 Cmdlet `Remove-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="db717-1884">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="db717-1885">移除觸發程序</span><span class="sxs-lookup"><span data-stu-id="db717-1885">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="db717-1886">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="db717-1886">Az.DataFactory</span></span>
* <span data-ttu-id="db717-1887">將 ADF .Net SDK 版本更新為 4.4.0</span><span class="sxs-lookup"><span data-stu-id="db717-1887">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="db717-1888">為 'Set-AzureRmDataFactoryV2IntegrationRuntime' CMD 新增參數 'ExpressCustomSetup'，以在無需自訂設定指令碼的情況下啟用設定組態和第三方元件。</span><span class="sxs-lookup"><span data-stu-id="db717-1888">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="db717-1889">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="db717-1889">Az.DataLakeStore</span></span>
* <span data-ttu-id="db717-1890">更新 Get-AzDataLakeStoreDeletedItem 和 Restore-AzDataLakeStoreDeletedItem 的文件</span><span class="sxs-lookup"><span data-stu-id="db717-1890">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="db717-1891">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="db717-1891">Az.EventHub</span></span>
* <span data-ttu-id="db717-1892">修正 10301 的問題：修正 SAS 權杖日期格式</span><span class="sxs-lookup"><span data-stu-id="db717-1892">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="db717-1893">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="db717-1893">Az.FrontDoor</span></span>
* <span data-ttu-id="db717-1894">將 MinimumTlsVersion 參數新增到 Enable-AzFrontDoorCustomDomainHttps 和 New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="db717-1894">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="db717-1895">將 HealthProbeMethod 和 EnabledState 參數新增到 New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="db717-1895">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="db717-1896">新增新的 cmdlet 以建立 BackendPoolsSettings 物件，以傳遞到 Front Door 的建立/更新</span><span class="sxs-lookup"><span data-stu-id="db717-1896">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="db717-1897">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="db717-1897">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="db717-1898">Az.Network</span><span class="sxs-lookup"><span data-stu-id="db717-1898">Az.Network</span></span>
* <span data-ttu-id="db717-1899">變更 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' 和 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData 選項範例。</span><span class="sxs-lookup"><span data-stu-id="db717-1899">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="db717-1900">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="db717-1900">Az.PrivateDns</span></span>
* <span data-ttu-id="db717-1901">已將 PrivateDns .net SDK 更新為 1.0.0 版</span><span class="sxs-lookup"><span data-stu-id="db717-1901">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="db717-1902">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="db717-1902">Az.RecoveryServices</span></span>
* <span data-ttu-id="db717-1903">Azure Site Recovery 支援在啟用保護時選取磁碟類型。</span><span class="sxs-lookup"><span data-stu-id="db717-1903">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="db717-1904">Azure Site Recovery 復原計劃針對動作編輯的錯誤 (bug) 修正。</span><span class="sxs-lookup"><span data-stu-id="db717-1904">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="db717-1905">Azure 備份 SQL 還原支援接受 filestream DB.</span><span class="sxs-lookup"><span data-stu-id="db717-1905">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="db717-1906">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="db717-1906">Az.RedisCache</span></span>
* <span data-ttu-id="db717-1907">已在 'New-AzRedisCache' 和 'Set-AzRedisCache' Cmdlet 中新增了 'MinimumTlsVersion'參數。</span><span class="sxs-lookup"><span data-stu-id="db717-1907">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="db717-1908">此外，也在 'Get-AzRedisCache' Cmdlet 的輸出中新增了 'MinimumTlsVersion'。</span><span class="sxs-lookup"><span data-stu-id="db717-1908">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="db717-1909">已針對 'Set-AzRedisCache' 和 'New-AzRedisCache' Cmdlet 新增了 '-Size' 參數的驗證</span><span class="sxs-lookup"><span data-stu-id="db717-1909">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="db717-1910">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="db717-1910">Az.Resources</span></span>
- <span data-ttu-id="db717-1911">更新了原則 Cmdlet 以使用新的 API 版本 2019-06-01，其在原則指派中具有新的 EnforcementMode 屬性。</span><span class="sxs-lookup"><span data-stu-id="db717-1911">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="db717-1912">更新了建立原則定義說明範例</span><span class="sxs-lookup"><span data-stu-id="db717-1912">Updated create policy definition help example</span></span>
- <span data-ttu-id="db717-1913">修正錯誤 (bug) Remove-AZADServicePrincipal -ServicePrincipalName，當找不到服務主體名稱時擲回 Null 參考。</span><span class="sxs-lookup"><span data-stu-id="db717-1913">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="db717-1914">修正錯誤 (bug) New-AZADServicePrincipal，當租用戶沒有任何訂用帳戶擲回 Null 參考。</span><span class="sxs-lookup"><span data-stu-id="db717-1914">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="db717-1915">將 New-azadserviceprincipal 變更為只將認證新增到相關聯的應用程式。</span><span class="sxs-lookup"><span data-stu-id="db717-1915">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="db717-1916">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="db717-1916">Az.Sql</span></span>
* <span data-ttu-id="db717-1917">新增了對 ReadReplicaCount 資料庫的支援。</span><span class="sxs-lookup"><span data-stu-id="db717-1917">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="db717-1918">修正了未設定區域備援時的 Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="db717-1918">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="db717-1919">3.0.0 - 2019 年 11 月</span><span class="sxs-lookup"><span data-stu-id="db717-1919">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="db717-1920">一般</span><span class="sxs-lookup"><span data-stu-id="db717-1920">General</span></span>
* <span data-ttu-id="db717-1921">已發行 Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="db717-1921">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="db717-1922">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="db717-1922">Az.Accounts</span></span>
* <span data-ttu-id="db717-1923">為 'Resolve-Error' 別名新增了淘汰訊息。</span><span class="sxs-lookup"><span data-stu-id="db717-1923">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="db717-1924">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="db717-1924">Az.Advisor</span></span>
* <span data-ttu-id="db717-1925">已為 Get-AzAdvisorRecommendation Cmdlet 新增了新的 'Operational Excellence' 類別。</span><span class="sxs-lookup"><span data-stu-id="db717-1925">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="db717-1926">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="db717-1926">Az.Batch</span></span>
* <span data-ttu-id="db717-1927">已將 `BatchAccountContext` 中的 `CoreQuota` 重新命名為 `DedicatedCoreQuota`。</span><span class="sxs-lookup"><span data-stu-id="db717-1927">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="db717-1928">另外還有新的 `LowPriorityCoreQuota`。</span><span class="sxs-lookup"><span data-stu-id="db717-1928">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="db717-1929">這會影響 **Get-AzBatchAccount**。</span><span class="sxs-lookup"><span data-stu-id="db717-1929">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="db717-1930">**New-AzBatchTask** `-ResourceFile` 參數現在會採用 `PSResourceFile` 物件集合，可使用新的 **New-AzBatchResourceFile** Cmdlet 加以建構。</span><span class="sxs-lookup"><span data-stu-id="db717-1930">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="db717-1931">新增 **New-AzBatchResourceFile** Cmdlet 以協助建立 `PSResourceFile` 物件。</span><span class="sxs-lookup"><span data-stu-id="db717-1931">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="db717-1932">這些可以提供給 `-ResourceFile` 參數中的 **New-AzBatchTask**。</span><span class="sxs-lookup"><span data-stu-id="db717-1932">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="db717-1933">除了現有的 `HttpUrl` 方式，這也會支援兩種新的資源檔類型：</span><span class="sxs-lookup"><span data-stu-id="db717-1933">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="db717-1934">`AutoStorageContainerName` 以資源檔為基礎，會將整個自動儲存體容器下載至 Batch-節點。</span><span class="sxs-lookup"><span data-stu-id="db717-1934">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="db717-1935">`StorageContainerUrl` 以資源檔為基礎，會將 URL 中指定的容器下載至 Batch-節點。</span><span class="sxs-lookup"><span data-stu-id="db717-1935">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="db717-1936">已移除 **AzBatchApplication** 所傳回之 `PSApplication` 的 `ApplicationPackages` 屬性。</span><span class="sxs-lookup"><span data-stu-id="db717-1936">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="db717-1937">您現在可以使用 **AzBatchApplicationPackage** 來取出應用程式內的特定套件。</span><span class="sxs-lookup"><span data-stu-id="db717-1937">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="db717-1938">例如： `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication` 。</span><span class="sxs-lookup"><span data-stu-id="db717-1938">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="db717-1939">將 **Get-AzBatchApplicationPackage**、**New-AzBatchApplicationPackage**、**Remove-AzBatchApplicationPackage**、**Get-AzBatchApplication**、**New-AzBatchApplication**、**Remove-AzBatchApplication** 和 **Set-AzBatchApplication** 上的 `ApplicationId` 重新命名為 `ApplicationName`。</span><span class="sxs-lookup"><span data-stu-id="db717-1939">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="db717-1940">`ApplicationId` 現在是 `ApplicationName` 的別名。</span><span class="sxs-lookup"><span data-stu-id="db717-1940">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="db717-1941">已在 `PSWindowsUserConfiguration` 中新增新的 `PSUserAccount` 屬性。</span><span class="sxs-lookup"><span data-stu-id="db717-1941">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="db717-1942">已將 `PSApplicationPackage` 上的 `Version` 重新命名為 `Name`。</span><span class="sxs-lookup"><span data-stu-id="db717-1942">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="db717-1943">已將 `PSResourceFile` 上的 `BlobSource` 重新命名為 `HttpUrl`。</span><span class="sxs-lookup"><span data-stu-id="db717-1943">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="db717-1944">已從 `PSVirtualMachineConfiguration` 移除 `OSDisk` 屬性。</span><span class="sxs-lookup"><span data-stu-id="db717-1944">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="db717-1945">已移除 **AzBatchPoolOSVersion**。</span><span class="sxs-lookup"><span data-stu-id="db717-1945">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="db717-1946">不再支援此作業。</span><span class="sxs-lookup"><span data-stu-id="db717-1946">This operation is no longer supported.</span></span>
* <span data-ttu-id="db717-1947">已從下列 `PSCloudServiceConfiguration` 中移除 `TargetOSVersion`。</span><span class="sxs-lookup"><span data-stu-id="db717-1947">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="db717-1948">已將 `PSCloudServiceConfiguration` 上的 `CurrentOSVersion` 重新命名為 `OSVersion`。</span><span class="sxs-lookup"><span data-stu-id="db717-1948">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="db717-1949">已從 `PSPoolUsageMetrics` 移除 `DataEgressGiB` 和 `DataIngressGiB`。</span><span class="sxs-lookup"><span data-stu-id="db717-1949">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="db717-1950">已移除 **AzBatchNodeAgentSku**，並以 **AzBatchSupportedImage** 取代。</span><span class="sxs-lookup"><span data-stu-id="db717-1950">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="db717-1951">**AzBatchSupportedImage** 會傳回與 **AzBatchNodeAgentSku** 相同但格式較好用的資料。</span><span class="sxs-lookup"><span data-stu-id="db717-1951">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="db717-1952">系統現在也會傳回新的未驗證映像。</span><span class="sxs-lookup"><span data-stu-id="db717-1952">New non-verified images are also now returned.</span></span> <span data-ttu-id="db717-1953">此外，也包含每個映像的 `Capabilities` 和 `BatchSupportEndOfLife` 的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="db717-1953">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="db717-1954">新增了一項功能，可透過 **New-azbatchpool** 的新 `MountConfiguration` 參數，在集區的每個節點上裝載遠端檔案系統。</span><span class="sxs-lookup"><span data-stu-id="db717-1954">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="db717-1955">現在支援網路安全性規則，根據流量的來源連接埠封鎖對集區的網路存取。</span><span class="sxs-lookup"><span data-stu-id="db717-1955">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="db717-1956">這會透過 `PSNetworkSecurityGroupRule`上的 `SourcePortRanges` 屬性來完成。</span><span class="sxs-lookup"><span data-stu-id="db717-1956">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="db717-1957">執行容器時，Batch 現在支援在容器工作目錄中或 Batch 工作的工作目錄中執行工作。</span><span class="sxs-lookup"><span data-stu-id="db717-1957">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="db717-1958">這是由 `PSTaskContainerSettings` 上的 `WorkingDirectory` 屬性所控制。</span><span class="sxs-lookup"><span data-stu-id="db717-1958">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="db717-1959">新增了一項功能，可透過新的 `PublicIPs` 屬性，在 `PSNetworkConfiguration` 上指定公用 IP 集合。</span><span class="sxs-lookup"><span data-stu-id="db717-1959">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="db717-1960">如此可確保集區中的節點將會有來自清單使用者所提供的 IP。</span><span class="sxs-lookup"><span data-stu-id="db717-1960">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="db717-1961">未指定時，`PSSTartTask` 上的 `WaitForSuccess` 預設值現在為 `$True` (之前是 `$False`)。</span><span class="sxs-lookup"><span data-stu-id="db717-1961">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="db717-1962">未指定時，`PSAutoUserSpecification` 上的 `Scope` 預設值現在為 `Pool` (之前在 Windows 上是 `Task`，在 Linux 上是 `Pool`)。</span><span class="sxs-lookup"><span data-stu-id="db717-1962">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="db717-1963">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="db717-1963">Az.Cdn</span></span>
* <span data-ttu-id="db717-1964">已將 UrlRewriteAction and CacheKeyQueryStringAction 引進 RulesEngine。</span><span class="sxs-lookup"><span data-stu-id="db717-1964">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="db717-1965">已修正 AzDeliveryRuleCondition Cmdlet 中的數個錯誤 (bug)，例如遺漏 'Selector’ 輸入。</span><span class="sxs-lookup"><span data-stu-id="db717-1965">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="db717-1966">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="db717-1966">Az.Compute</span></span>
* <span data-ttu-id="db717-1967">磁碟加密集功能</span><span class="sxs-lookup"><span data-stu-id="db717-1967">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="db717-1968">新的 Cmdlet： New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="db717-1968">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="db717-1969">DiskEncryptionSetId 參數已新增至下列 Cmdlet： Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="db717-1969">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="db717-1970">DiskEncryptionSetId 和 EncryptionType 參數已新增至下列 Cmdlet： New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="db717-1970">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="db717-1971">將 PublicIPAddressVersion 參數新增至 New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="db717-1971">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="db717-1972">將自訂指令碼擴充功能的 FileUris 從公用設定移至受保護的設定</span><span class="sxs-lookup"><span data-stu-id="db717-1972">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="db717-1973">將 ScaleInPolicy 新增至 New-AzVmss、New-AzVmssConfig 和 Update-AzVmss Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-1973">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="db717-1974">重大變更</span><span class="sxs-lookup"><span data-stu-id="db717-1974">Breaking changes</span></span>
    - <span data-ttu-id="db717-1975">上傳 CreateOption 時，會針對 New-AzDiskConfig 使用 UploadSizeInBytes 參數而非 DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="db717-1975">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="db717-1976">在 GalleryImageVersion 物件中，會使用 StorageProfile.Source.Id 取代 PublishingProfile.Source.ManagedImage.Id</span><span class="sxs-lookup"><span data-stu-id="db717-1976">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="db717-1977">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="db717-1977">Az.DataFactory</span></span>
* <span data-ttu-id="db717-1978">將 ADF .Net SDK 版本更新為 4.3.0</span><span class="sxs-lookup"><span data-stu-id="db717-1978">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="db717-1979">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="db717-1979">Az.DataLakeStore</span></span>
* <span data-ttu-id="db717-1980">更新 ADLS SDK 版本 (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) ，提供下列修正程式</span><span class="sxs-lookup"><span data-stu-id="db717-1980">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="db717-1981">避免在無法將資源回收筒或目錄專案的建立時間還原序列化 (creationtime) 時擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="db717-1981">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="db717-1982">在 adlsclient 中公開每個要求超時設定</span><span class="sxs-lookup"><span data-stu-id="db717-1982">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="db717-1983">修正傳遞原始 syncflag 以進行 badoffset 復原</span><span class="sxs-lookup"><span data-stu-id="db717-1983">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="db717-1984">修正 EnumerateDirectory 以在檢查回應後取得接續權杖</span><span class="sxs-lookup"><span data-stu-id="db717-1984">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="db717-1985">修正 Concat 錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="db717-1985">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="db717-1986">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="db717-1986">Az.FrontDoor</span></span>
* <span data-ttu-id="db717-1987">修正了多個模組中的各種錯字問題</span><span class="sxs-lookup"><span data-stu-id="db717-1987">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="db717-1988">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="db717-1988">Az.HDInsight</span></span>
* <span data-ttu-id="db717-1989">修正當使用 Get-AzHDInsightCluster 取得具有 ADLSGen1 儲存體的叢集時，客戶會收到「不是有效的 Base-64 字串」的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="db717-1989">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="db717-1990">將名為 'ApplicationId' 的參數新增至 Add-AzHDInsightClusterIdentity、New-AzHDInsightClusterConfig 和 New-AzHDInsightCluster 三個 Cmdlet 中，讓客戶可以提供服務主體應用程式識別碼來存取 Azure Data Lake。</span><span class="sxs-lookup"><span data-stu-id="db717-1990">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="db717-1991">已將 Microsoft.Azure.Management.HDInsight 從 2.1.0 變更為 5.1.0</span><span class="sxs-lookup"><span data-stu-id="db717-1991">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="db717-1992">已移除五個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="db717-1992">Removed five cmdlets:</span></span>
    - <span data-ttu-id="db717-1993">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="db717-1993">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="db717-1994">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="db717-1994">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="db717-1995">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="db717-1995">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="db717-1996">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="db717-1996">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="db717-1997">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="db717-1997">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="db717-1998">新增了三個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="db717-1998">Added three cmdlets:</span></span>
    - <span data-ttu-id="db717-1999">Get-AzHDInsightMonitoring 用來取代 Get-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="db717-1999">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="db717-2000">Enable-AzHDInsightMonitoring 用來取代 Enable-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="db717-2000">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="db717-2001">Disable-AzHDInsightMonitoring 用來取代 Disable-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="db717-2001">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="db717-2002">修正了 Cmdlet AzHDInsightProperties，以支援來自特定位置的取得功能資訊。</span><span class="sxs-lookup"><span data-stu-id="db717-2002">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="db717-2003">已從 Add-AzHDInsightConfigValue 移除參數集 ('Spark1', 'Spark2')。</span><span class="sxs-lookup"><span data-stu-id="db717-2003">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="db717-2004">將範例新增至 Cmdlet Add-AzHDInsightSecurityProfile 的說明文件。</span><span class="sxs-lookup"><span data-stu-id="db717-2004">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="db717-2005">已變更下列 Cmdlet 的輸出類型：</span><span class="sxs-lookup"><span data-stu-id="db717-2005">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="db717-2006">已將 Get-AzHDInsightProperties 的輸出類型從 CapabilitiesResponse 變更為 AzureHDInsightCapabilities。</span><span class="sxs-lookup"><span data-stu-id="db717-2006">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="db717-2007">已將 Remove-AzHDInsightCluster 的輸出類型從 ClusterGetResponse 變更為 bool。</span><span class="sxs-lookup"><span data-stu-id="db717-2007">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="db717-2008">已將 Set-AzHDInsightGatewaySettings HttpConnectivitySettings 的輸出類型變更為 GatewaySettings。</span><span class="sxs-lookup"><span data-stu-id="db717-2008">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="db717-2009">已新增一些狀況測試案例。</span><span class="sxs-lookup"><span data-stu-id="db717-2009">Added some scenario test cases.</span></span>
* <span data-ttu-id="db717-2010">移除一些別名：'Add-AzHDInsightConfigValues'、'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="db717-2010">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="db717-2011">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="db717-2011">Az.IotHub</span></span>
* <span data-ttu-id="db717-2012">重大變更：</span><span class="sxs-lookup"><span data-stu-id="db717-2012">Breaking changes:</span></span>
    - <span data-ttu-id="db717-2013">Cmdlet 'Add-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="db717-2013">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="db717-2014">已移除 Cmdlet 'Add-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="db717-2014">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="db717-2015">Cmdlet 'Get-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="db717-2015">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="db717-2016">已移除 Cmdlet 'Get-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="db717-2016">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="db717-2017">已移除類型為 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' 的屬性 'OperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="db717-2017">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="db717-2018">已移除類型為 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' 的屬性 'OperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="db717-2018">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="db717-2019">Cmdlet 'New-AzIotHubExportDevice' 已不再支援別名 'New-AzIotHubExportDevices'。</span><span class="sxs-lookup"><span data-stu-id="db717-2019">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="db717-2020">Cmdlet 'New-AzIotHubImportDevice' 已不再支援別名 'New-AzIotHubImportDevices'。</span><span class="sxs-lookup"><span data-stu-id="db717-2020">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="db717-2021">Cmdlet 'Remove-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="db717-2021">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="db717-2022">已移除 Cmdlet 'Remove-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="db717-2022">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="db717-2023">Cmdlet 'Set-AzIotHub' 已不再支援參數 'OperationsMonitoringProperties'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="db717-2023">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="db717-2024">已移除 Cmdlet 'Set-AzIotHub' 的參數集 'UpdateOperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="db717-2024">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="db717-2025">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="db717-2025">Az.RecoveryServices</span></span>
* <span data-ttu-id="db717-2026">Azure Site Recovery 支援將 NSG、公用 IP 和 Azure 的內部負載平衡器網路資源設定為 Azure。</span><span class="sxs-lookup"><span data-stu-id="db717-2026">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="db717-2027">Azure Site Recovery 支援從 VMware 寫入 Azure 受控磁碟。</span><span class="sxs-lookup"><span data-stu-id="db717-2027">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="db717-2028">Azure Site Recovery 支援從 VMware 到 Azure 的 NIC 縮減。</span><span class="sxs-lookup"><span data-stu-id="db717-2028">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="db717-2029">Azure Site Recovery 支援從 Azure 到 Azure 的加速網路。</span><span class="sxs-lookup"><span data-stu-id="db717-2029">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="db717-2030">Azure Site Recovery 支援從 Azure 到 Azure 的代理程式自動更新。</span><span class="sxs-lookup"><span data-stu-id="db717-2030">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="db717-2031">Azure Site Recovery 支援從 Azure 到 Azure 的標準 SSD。</span><span class="sxs-lookup"><span data-stu-id="db717-2031">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="db717-2032">Azure Site Recovery 支援從 Azure 到 Azure 的 Azure 磁碟加密傳遞。</span><span class="sxs-lookup"><span data-stu-id="db717-2032">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="db717-2033">Azure Site Recovery 提供從 Azure 到 Azure 的新增磁碟保護支援。</span><span class="sxs-lookup"><span data-stu-id="db717-2033">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="db717-2034">已新增 VM 的 SoftDelete 功能，並新增了 SoftDelete 的測試</span><span class="sxs-lookup"><span data-stu-id="db717-2034">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="db717-2035">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="db717-2035">Az.Resources</span></span>
* <span data-ttu-id="db717-2036">將相依性組件 Microsoft.Extensions.Caching.Memory 從1.1.1 更新為 2.2</span><span class="sxs-lookup"><span data-stu-id="db717-2036">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="db717-2037">Az.Network</span><span class="sxs-lookup"><span data-stu-id="db717-2037">Az.Network</span></span>
* <span data-ttu-id="db717-2038">變更 PrivateEndpointConnection 的所有 Cmdlet，以支援一般服務提供者。</span><span class="sxs-lookup"><span data-stu-id="db717-2038">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="db717-2039">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="db717-2039">Updated cmdlet:</span></span>
        - <span data-ttu-id="db717-2040">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="db717-2040">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="db717-2041">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="db717-2041">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="db717-2042">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="db717-2042">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="db717-2043">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="db717-2043">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="db717-2044">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="db717-2044">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="db717-2045">為 PrivateLinkResource 新增新的 Cmdlet，其同時支援一般服務提供者。</span><span class="sxs-lookup"><span data-stu-id="db717-2045">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="db717-2046">新的 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="db717-2046">New cmdlet:</span></span>
        - <span data-ttu-id="db717-2047">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="db717-2047">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="db717-2048">新增功能 Proxy Protocol V2 的新欄位和參數。</span><span class="sxs-lookup"><span data-stu-id="db717-2048">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="db717-2049">在 PrivateLinkService 中新增屬性 EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="db717-2049">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="db717-2050">在 PrivateEndpointConnection 中新增屬性 LinkIdentifier</span><span class="sxs-lookup"><span data-stu-id="db717-2050">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="db717-2051">更新了 New-AzPrivateLinkService 以新增選擇性參數 EnableProxyProtocol。</span><span class="sxs-lookup"><span data-stu-id="db717-2051">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="db717-2052">修正 'New-AzApplicationGatewaySku' 參考文件中不正確的參數描述</span><span class="sxs-lookup"><span data-stu-id="db717-2052">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="db717-2053">新增 Cmdlet 以支援 Azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="db717-2053">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="db717-2054">為 VirtualHub的子資源 RouteTables 新增支援</span><span class="sxs-lookup"><span data-stu-id="db717-2054">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="db717-2055">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="db717-2055">New cmdlets added:</span></span>
        - <span data-ttu-id="db717-2056">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="db717-2056">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="db717-2057">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="db717-2057">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="db717-2058">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="db717-2058">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="db717-2059">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="db717-2059">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="db717-2060">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="db717-2060">Set-AzVirtualHub</span></span>
* <span data-ttu-id="db717-2061">新增 VirtualHub 的新屬性 SKU 和 VirtualWan 的 VirtualWANType 支援</span><span class="sxs-lookup"><span data-stu-id="db717-2061">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="db717-2062">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="db717-2062">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="db717-2063">New-AzVirtualHub：新增了參數 SKU</span><span class="sxs-lookup"><span data-stu-id="db717-2063">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="db717-2064">Update-AzVirtualHub：新增了參數 SKU</span><span class="sxs-lookup"><span data-stu-id="db717-2064">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="db717-2065">New-AzVirtualWan：新增了參數 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="db717-2065">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="db717-2066">Update-AzVirtualWan：新增了參數 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="db717-2066">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="db717-2067">為 HubVnetConnection、VpnConnection 和 ExpressRouteConnection 新增 EnableInternetSecurity 屬性的支援</span><span class="sxs-lookup"><span data-stu-id="db717-2067">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="db717-2068">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="db717-2068">New cmdlets added:</span></span>
        - <span data-ttu-id="db717-2069">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="db717-2069">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="db717-2070">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="db717-2070">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="db717-2071">New-AzureRmVirtualHubVnetConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="db717-2071">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="db717-2072">New-AzureRmVpnConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="db717-2072">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="db717-2073">Update-AzureRmVpnConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="db717-2073">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="db717-2074">New-AzureRmExpressRouteConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="db717-2074">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="db717-2075">Set-AzureRmExpressRouteConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="db717-2075">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="db717-2076">新增設定 TopLevel WebApplicationFirewall 原則的支援</span><span class="sxs-lookup"><span data-stu-id="db717-2076">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="db717-2077">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="db717-2077">New cmdlets added:</span></span>
        - <span data-ttu-id="db717-2078">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="db717-2078">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="db717-2079">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="db717-2079">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="db717-2080">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="db717-2080">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="db717-2081">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="db717-2081">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="db717-2082">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="db717-2082">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="db717-2083">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="db717-2083">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="db717-2084">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="db717-2084">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="db717-2085">New-AzApplicationGatewayFirewallPolicy：新增了參數 PolicySetting、ManagedRule</span><span class="sxs-lookup"><span data-stu-id="db717-2085">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="db717-2086">已在 CustomRule 上新增對 Geo-Match 運算子的支援</span><span class="sxs-lookup"><span data-stu-id="db717-2086">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="db717-2087">已將 GeoMatch 新增至 FirewallCondition 上的運算子</span><span class="sxs-lookup"><span data-stu-id="db717-2087">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="db717-2088">已新增 perListener 和 perSite 防火牆原則的支援</span><span class="sxs-lookup"><span data-stu-id="db717-2088">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="db717-2089">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="db717-2089">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="db717-2090">New-AzApplicationGatewayHttpListener：新增了參數 FirewallPolicy、FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="db717-2090">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="db717-2091">New-AzApplicationGatewayPathRuleConfig：新增了參數 FirewallPolicy、FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="db717-2091">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="db717-2092">將 'PSBastion' 中名稱為 AzureBastionSubnet 的必要子網路修正為可不區分大小寫</span><span class="sxs-lookup"><span data-stu-id="db717-2092">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="db717-2093">支援網路規則中的目的地 FQDN，以及適用於 Azure 防火牆的 NAT 規則中轉譯的 FQDN</span><span class="sxs-lookup"><span data-stu-id="db717-2093">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="db717-2094">為 IpGroup的上層資源 RouteTables 新增支援</span><span class="sxs-lookup"><span data-stu-id="db717-2094">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="db717-2095">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="db717-2095">New cmdlets added:</span></span>
        - <span data-ttu-id="db717-2096">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="db717-2096">New-AzIpGroup</span></span>
        - <span data-ttu-id="db717-2097">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="db717-2097">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="db717-2098">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="db717-2098">Get-AzIpGroup</span></span>
        - <span data-ttu-id="db717-2099">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="db717-2099">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="db717-2100">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="db717-2100">Az.ServiceFabric</span></span>
* <span data-ttu-id="db717-2101">移除 Add-AzServiceFabricApplicationCertificate Cmdlet，因為 Add-AzVmssSecret 會涵蓋此案例。</span><span class="sxs-lookup"><span data-stu-id="db717-2101">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="db717-2102">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="db717-2102">Az.Sql</span></span>
* <span data-ttu-id="db717-2103">已新增在受控執行個體上還原已卸載之資料庫的支援。</span><span class="sxs-lookup"><span data-stu-id="db717-2103">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="db717-2104">已從程式碼中淘汰舊版的審核 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db717-2104">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="db717-2105">移除了已淘汰的別名：</span><span class="sxs-lookup"><span data-stu-id="db717-2105">Removed deprecated aliases:</span></span>
* <span data-ttu-id="db717-2106">Get-AzSqlDatabaseIndexRecommendations (改為使用 Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="db717-2106">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="db717-2107">Get-AzSqlDatabaseRestorePoints (改為使用 Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="db717-2107">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="db717-2108">移除 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-2108">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="db717-2109">移除已淘汰的弱點評估設定 Cmdlet 的別名</span><span class="sxs-lookup"><span data-stu-id="db717-2109">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="db717-2110">淘汰進階威脅偵測設定 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-2110">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="db717-2111">在 Disable 中新增 Cmdlet 以啟用資料庫中資料行的敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="db717-2111">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="db717-2112">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="db717-2112">Az.Storage</span></span>
* <span data-ttu-id="db717-2113">支援在建立或更新儲存體帳戶時啟用大型檔案共用</span><span class="sxs-lookup"><span data-stu-id="db717-2113">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="db717-2114">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="db717-2114">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="db717-2115">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="db717-2115">Set-AzStorageAccount</span></span>
* <span data-ttu-id="db717-2116">當關閉/取得檔案控制代碼時，跳過檢查輸入路徑是否為檔案目錄或檔案，以避免物件處於 DeletePending 狀態時失敗</span><span class="sxs-lookup"><span data-stu-id="db717-2116">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="db717-2117">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="db717-2117">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="db717-2118">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="db717-2118">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="db717-2119">2.8.0 - 2019 年10月</span><span class="sxs-lookup"><span data-stu-id="db717-2119">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="db717-2120">一般</span><span class="sxs-lookup"><span data-stu-id="db717-2120">General</span></span>
* <span data-ttu-id="db717-2121">Az.HealthcareApis 1.0.0 版本</span><span class="sxs-lookup"><span data-stu-id="db717-2121">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="db717-2122">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="db717-2122">Az.Accounts</span></span>
* <span data-ttu-id="db717-2123">針對產生的模組更新遙測和重寫 URL，修正 Windows 單元測試。</span><span class="sxs-lookup"><span data-stu-id="db717-2123">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="db717-2124">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="db717-2124">Az.ApiManagement</span></span>
* <span data-ttu-id="db717-2125">**Set-AzApiManagementApi** - 已新增在 ApiVersionSet 中更新 API 的支援</span><span class="sxs-lookup"><span data-stu-id="db717-2125">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="db717-2126">修正 https://github.com/Azure/azure-powershell/issues/10068 的問題</span><span class="sxs-lookup"><span data-stu-id="db717-2126">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="db717-2127">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="db717-2127">Az.Automation</span></span>
* <span data-ttu-id="db717-2128">已針對 Linux 重新啟動設定參數修正了 New-AzureAutomationSoftwareUpdateConfiguration Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db717-2128">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="db717-2129">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="db717-2129">Az.Batch</span></span>
* <span data-ttu-id="db717-2130">**Get-AzBatchNodeAgentSku** 已被取代，在版本 2.0.0 中會由 **Get-AzBatchSupportImage** 取代。</span><span class="sxs-lookup"><span data-stu-id="db717-2130">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="db717-2131">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="db717-2131">Az.Compute</span></span>
* <span data-ttu-id="db717-2132">在 New-AzVM 和 New-AzVmss Cmdlet 中新增 Priority、EvictionPolicy 和 MaxPrice 參數</span><span class="sxs-lookup"><span data-stu-id="db717-2132">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="db717-2133">修正 Add-AzVMAdditionalUnattendContent 和 Add-AzVMSshPublicKey Cmdlet 的警告訊息和說明文件</span><span class="sxs-lookup"><span data-stu-id="db717-2133">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="db717-2134">修正 Linux VM 的 -skipVmBackup 例外狀況，以及 Set-AzVMDiskEncryptionExtension 的受控磁碟。</span><span class="sxs-lookup"><span data-stu-id="db717-2134">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="db717-2135">修正 Set-AzVMDiskEncryptionExtension 中更新加密設定中的錯誤 (bug)，兩種傳遞案例。</span><span class="sxs-lookup"><span data-stu-id="db717-2135">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="db717-2136">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="db717-2136">Az.DataFactory</span></span>
* <span data-ttu-id="db717-2137">針對 ADF V2 資料流程新增 CRUD 命令：Set-AzDataFactoryV2DataFlow、Remove-AzDataFactoryV2DataFlow 和 Get-AzDataFactoryV2DataFlow。</span><span class="sxs-lookup"><span data-stu-id="db717-2137">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="db717-2138">針對 ADF V2 資料流程偵錯工作階段新增動作命令：Start-AzDataFactoryV2DataFlowDebugSession、Get-AzDataFactoryV2DataFlowDebugSession、Add-AzDataFactoryV2DataFlowDebugSessionPackage、Invoke-AzDataFactoryV2DataFlowDebugSessionCommand 和 Stop-AzDataFactoryV2DataFlowDebugSession。</span><span class="sxs-lookup"><span data-stu-id="db717-2138">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="db717-2139">將 ADF .Net SDK 版本更新為 4.2.0</span><span class="sxs-lookup"><span data-stu-id="db717-2139">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="db717-2140">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="db717-2140">Az.DataLakeStore</span></span>
* <span data-ttu-id="db717-2141">修正帳戶驗證，以便在沒有網域的情況下傳遞具有 '-' 的帳戶</span><span class="sxs-lookup"><span data-stu-id="db717-2141">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="db717-2142">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="db717-2142">Az.HealthcareApis</span></span>
* <span data-ttu-id="db717-2143">已將 Powershell 版本更新為 1.0.0</span><span class="sxs-lookup"><span data-stu-id="db717-2143">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="db717-2144">已將 SDK 版本更新為 1.0.2</span><span class="sxs-lookup"><span data-stu-id="db717-2144">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="db717-2145">更新測試以參考新的 SDK 版本</span><span class="sxs-lookup"><span data-stu-id="db717-2145">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="db717-2146">已將輸出結構從巢狀更新為壓平合併。</span><span class="sxs-lookup"><span data-stu-id="db717-2146">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="db717-2147">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="db717-2147">Az.IotHub</span></span>
* <span data-ttu-id="db717-2148">新增新的路由來源：DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="db717-2148">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="db717-2149">次要錯誤修正：Get-AzIothub 未傳回 subscriptionId</span><span class="sxs-lookup"><span data-stu-id="db717-2149">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="db717-2150">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="db717-2150">Az.Monitor</span></span>
* <span data-ttu-id="db717-2151">已針對動作群組新增新的動作群組接收器   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="db717-2151">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="db717-2152">針對接收器使用已啟用的一般警示結構描述。</span><span class="sxs-lookup"><span data-stu-id="db717-2152">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="db717-2153">這不適用於 SMS、Azure App 撨送、ITSM 和 Voice 接收器</span><span class="sxs-lookup"><span data-stu-id="db717-2153">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="db717-2154">Webhooks 現在支援 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="db717-2154">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="db717-2155">Az.Network</span><span class="sxs-lookup"><span data-stu-id="db717-2155">Az.Network</span></span>
* <span data-ttu-id="db717-2156">新增新的 Cmdlet Get-AzAvailableServiceAlias 以便進行呼叫並取得可用於服務端點原則的別名。</span><span class="sxs-lookup"><span data-stu-id="db717-2156">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="db717-2157">已在虛擬網路閘道連線新增了流量選取器的支援</span><span class="sxs-lookup"><span data-stu-id="db717-2157">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="db717-2158">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="db717-2158">New cmdlets added:</span></span>
        - <span data-ttu-id="db717-2159">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="db717-2159">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="db717-2160">已更新選用參數的 Cmdlet -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="db717-2160">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="db717-2161">新增網路安全性規則組態中針對 ESP 和 AH 通訊協定的支援</span><span class="sxs-lookup"><span data-stu-id="db717-2161">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="db717-2162">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="db717-2162">Updated cmdlets:</span></span>
        - <span data-ttu-id="db717-2163">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="db717-2163">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="db717-2164">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="db717-2164">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="db717-2165">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="db717-2165">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="db717-2166">改善 Cortex Cmdlet 中的例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="db717-2166">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="db717-2167">適用於 VirtualNetworkGateways 的新項目和 SKU</span><span class="sxs-lookup"><span data-stu-id="db717-2167">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="db717-2168">引進新一代的 VirtualNetworkGateways。</span><span class="sxs-lookup"><span data-stu-id="db717-2168">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="db717-2169">引進適用於 VirtualNetworkGateways 的全新高輸送量 SKU。</span><span class="sxs-lookup"><span data-stu-id="db717-2169">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="db717-2170">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="db717-2170">Az.RedisCache</span></span>
* <span data-ttu-id="db717-2171">更新了 'Set-AzRedisCache' 參考文件，納入了 '-Size' 參數缺少的值</span><span class="sxs-lookup"><span data-stu-id="db717-2171">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="db717-2172">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="db717-2172">Az.Sql</span></span>
* <span data-ttu-id="db717-2173">新增在受控執行個體上設定 Active Directory 系統管理員的支援</span><span class="sxs-lookup"><span data-stu-id="db717-2173">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="db717-2174">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="db717-2174">Az.Storage</span></span>
* <span data-ttu-id="db717-2175">將儲存體用戶端程式庫升級為 11.1.0</span><span class="sxs-lookup"><span data-stu-id="db717-2175">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="db717-2176">列出具有管理平面 API 的容器，將會以 NextPageLink 列出</span><span class="sxs-lookup"><span data-stu-id="db717-2176">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="db717-2177">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="db717-2177">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="db717-2178">列出訂用帳戶中的儲存體帳戶，將會以 NextPageLink 列出</span><span class="sxs-lookup"><span data-stu-id="db717-2178">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="db717-2179">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="db717-2179">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="db717-2180">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="db717-2180">Az.StorageSync</span></span>
* <span data-ttu-id="db717-2181">修正 Reset-AzStorageSyncServerCertificate 中的問題 9810。</span><span class="sxs-lookup"><span data-stu-id="db717-2181">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="db717-2182">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="db717-2182">Az.Websites</span></span>
* <span data-ttu-id="db717-2183">Set-AzWebApp 更新應用程式的 ASP 時失敗</span><span class="sxs-lookup"><span data-stu-id="db717-2183">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="db717-2184">2.7.0 - 2019 年 9 月</span><span class="sxs-lookup"><span data-stu-id="db717-2184">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="db717-2185">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="db717-2185">Az.ApiManagement</span></span>
* <span data-ttu-id="db717-2186">更新 'Set-AzApiManagementPolicy' 參考文件中的 '-Format' 參數描述</span><span class="sxs-lookup"><span data-stu-id="db717-2186">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="db717-2187">已移除參考文件中的 'Update-AzApiManagementDeployment' 參考，此 Cmdlet 已被取代。</span><span class="sxs-lookup"><span data-stu-id="db717-2187">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="db717-2188">改為使用 'Set-AzApiManagement'。</span><span class="sxs-lookup"><span data-stu-id="db717-2188">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="db717-2189">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="db717-2189">Az.Automation</span></span>
* <span data-ttu-id="db717-2190">已修正 'Register-AzAutomationDscNode' 參考文件中範例的錯別字</span><span class="sxs-lookup"><span data-stu-id="db717-2190">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="db717-2191">已新增 Register-AzAutomationDSCNode 的 OS 限制說明</span><span class="sxs-lookup"><span data-stu-id="db717-2191">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="db717-2192">已針對 -Wait 選項修正了 Start-AzAutomationRunbook Cmdlet 的 Null 參考例外狀況。</span><span class="sxs-lookup"><span data-stu-id="db717-2192">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="db717-2193">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="db717-2193">Az.Compute</span></span>
* <span data-ttu-id="db717-2194">在 New-AzDiskConfig 中新增 UploadSizeInBytes 參數</span><span class="sxs-lookup"><span data-stu-id="db717-2194">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="db717-2195">在 New-AzSnapshotConfig 中新增增量參數</span><span class="sxs-lookup"><span data-stu-id="db717-2195">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="db717-2196">新增低優先順序虛擬機器功能：</span><span class="sxs-lookup"><span data-stu-id="db717-2196">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="db717-2197">已將 MaxPrice、EvictionPolicy 和 Priority 參數新增到 New-AzVMConfig。</span><span class="sxs-lookup"><span data-stu-id="db717-2197">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="db717-2198">已將 MaxPrice 參數新增到 New-AzVmssConfig、Update-AzVM 和 Update-AzVmss Cmdlet 中。</span><span class="sxs-lookup"><span data-stu-id="db717-2198">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="db717-2199">修正 Get-AzAvailabilitySet Cmdlet 的參考問題，以免在訂用帳戶中列出所有可用性設定組。</span><span class="sxs-lookup"><span data-stu-id="db717-2199">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="db717-2200">修正 Get-AzRemoteDesktopFile 的 Null 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="db717-2200">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="db717-2201">修正適用於端點相關位置的 VHD Seek 方法。</span><span class="sxs-lookup"><span data-stu-id="db717-2201">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="db717-2202">修正 New-AzVM 和 Update-AzVM 的 UltraSSD 問題。</span><span class="sxs-lookup"><span data-stu-id="db717-2202">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="db717-2203">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="db717-2203">Az.DataFactory</span></span>
* <span data-ttu-id="db717-2204">為 ADF V2 新增 3 個新命令 - Add-AzDataFactoryV2TriggerSubscription、Remove-AzDataFactoryV2TriggerSubscription 和 Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="db717-2204">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="db717-2205">已將 ADF .Net SDK 版本更新為 4.1.3</span><span class="sxs-lookup"><span data-stu-id="db717-2205">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="db717-2206">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="db717-2206">Az.HDInsight</span></span>
* <span data-ttu-id="db717-2207">呼叫重大變更</span><span class="sxs-lookup"><span data-stu-id="db717-2207">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="db717-2208">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="db717-2208">Az.IotHub</span></span>
* <span data-ttu-id="db717-2209">針對異地配對災害復原區域新增叫用 IotHub 容錯移轉的支援。</span><span class="sxs-lookup"><span data-stu-id="db717-2209">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="db717-2210">新增管理 IotHub 訊息擴充的支援。</span><span class="sxs-lookup"><span data-stu-id="db717-2210">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="db717-2211">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="db717-2211">New cmdlets are:</span></span>
    - <span data-ttu-id="db717-2212">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="db717-2212">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="db717-2213">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="db717-2213">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="db717-2214">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="db717-2214">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="db717-2215">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="db717-2215">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="db717-2216">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="db717-2216">Az.Monitor</span></span>
* <span data-ttu-id="db717-2217">指向最近的監視 SDK，例如 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="db717-2217">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="db717-2218">在 Metrics Cmdlet 中新增不會造成中斷的變更，例如單位列舉支援數個新值。</span><span class="sxs-lookup"><span data-stu-id="db717-2218">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="db717-2219">這些 Cmdlet 是唯讀的，因此 Cmdlet 的輸出中不會有任何變更。</span><span class="sxs-lookup"><span data-stu-id="db717-2219">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="db717-2220">**ActionGroups** 要求的 api-version 現在為 **2019-06-01**，之前為 **2018-03-01**。</span><span class="sxs-lookup"><span data-stu-id="db717-2220">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="db717-2221">已針對此項變更新增多個案例測試。</span><span class="sxs-lookup"><span data-stu-id="db717-2221">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="db717-2222">**EmailReceiver** 和 **WebhookReceiver** 類別的建構函式新增了一個新的強制引數，例如稱為 **useCommonAlertSchema** 的布林值。</span><span class="sxs-lookup"><span data-stu-id="db717-2222">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="db717-2223">目前，該值已修正為 **false** 以隱藏 Cmdlet 的重大變更。</span><span class="sxs-lookup"><span data-stu-id="db717-2223">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="db717-2224">**注意**：這是暫時性的變更，必須由警示小組驗證。</span><span class="sxs-lookup"><span data-stu-id="db717-2224">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="db717-2225">**Source** 類別之建構函式的引數順序 (與 **ScheduledQueryRuleSource** 類別相關) 已變更，不再是先前的 SDK。</span><span class="sxs-lookup"><span data-stu-id="db717-2225">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="db717-2226">此變更需要修正兩個單元測試：這兩個單元已進行編譯，但無法通過測試。</span><span class="sxs-lookup"><span data-stu-id="db717-2226">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="db717-2227">**AlertingAction** 類別之建構函式的引數順序 (與 **ScheduledQueryRuleSource** 類別相關) 已變更，不再是先前的 SDK。</span><span class="sxs-lookup"><span data-stu-id="db717-2227">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="db717-2228">此變更需要修正兩個單元測試：這兩個單元已進行編譯，但無法通過測試。</span><span class="sxs-lookup"><span data-stu-id="db717-2228">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="db717-2229">適用於計量警示 V2 的支援動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="db717-2229">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="db717-2230">New-AzMetricAlertRuleV2Criteria：目前也建立動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="db717-2230">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="db717-2231">Add-AzMetricAlertRuleV2：目前也接受動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="db717-2231">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="db717-2232">已排程查詢規則 Cmdlet (SQR) 中的改善項目</span><span class="sxs-lookup"><span data-stu-id="db717-2232">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="db717-2233">Cmdlets 接受兩種格式的 'Location' 參數，包含位置 (例如 eastus) 或位置顯示名稱 (例如美國東部)</span><span class="sxs-lookup"><span data-stu-id="db717-2233">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="db717-2234">在說明檔案中適當地描述 ’Enabled’ 參數</span><span class="sxs-lookup"><span data-stu-id="db717-2234">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="db717-2235">已新增 'ActionGroup' 選用參數的範例</span><span class="sxs-lookup"><span data-stu-id="db717-2235">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="db717-2236">說明檔內容全面改善</span><span class="sxs-lookup"><span data-stu-id="db717-2236">Overall improved help files</span></span>
* <span data-ttu-id="db717-2237">修正判斷 'Set-AzActionRule' 範圍類型的錯誤</span><span class="sxs-lookup"><span data-stu-id="db717-2237">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="db717-2238">Az.Network</span><span class="sxs-lookup"><span data-stu-id="db717-2238">Az.Network</span></span>
* <span data-ttu-id="db717-2239">修正 'New-AzApplicationGateway' 參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="db717-2239">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="db717-2240">在 'Get-AzNetworkWatcherPacketCapture' 參考文件中新增註解，說明擷取封包取得之所有屬性的相關資訊</span><span class="sxs-lookup"><span data-stu-id="db717-2240">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="db717-2241">已修正 'Test-AzNetworkWatcherIPFlow' 參考文件中的範例，以便正確地列舉 NIC</span><span class="sxs-lookup"><span data-stu-id="db717-2241">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="db717-2242">改善了雲端例外狀況剖析，以便顯示其他詳細資料 (若有)</span><span class="sxs-lookup"><span data-stu-id="db717-2242">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="db717-2243">改善了雲端例外狀況剖析，以便處理 SDK 例外狀況的其他類型</span><span class="sxs-lookup"><span data-stu-id="db717-2243">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="db717-2244">修正了不正確的安全性規則模型對應</span><span class="sxs-lookup"><span data-stu-id="db717-2244">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="db717-2245">在網路介面中新增了屬性以提供 IP 功能</span><span class="sxs-lookup"><span data-stu-id="db717-2245">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="db717-2246">在 PSNetworkInterface 中新增了 'PrivateEndpoint' 屬性作為 PSResourceId 類型</span><span class="sxs-lookup"><span data-stu-id="db717-2246">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="db717-2247">在 PSNetworkInterfaceIPConfiguration 中新增了 'PrivateLinkConnectionProperties' 屬性作為 PSIpConfigurationConnectivityInformation 類型</span><span class="sxs-lookup"><span data-stu-id="db717-2247">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="db717-2248">新增了模型類別 PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="db717-2248">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="db717-2249">針對 Azure 防火牆資源新增了 ApplicationRuleProtocolType 'mssql'</span><span class="sxs-lookup"><span data-stu-id="db717-2249">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="db717-2250">在虛擬 WAN 中支援多連結</span><span class="sxs-lookup"><span data-stu-id="db717-2250">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="db717-2251">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-2251">New cmdlets</span></span>
        - <span data-ttu-id="db717-2252">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="db717-2252">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="db717-2253">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="db717-2253">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="db717-2254">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="db717-2254">Updated cmdlet:</span></span>
        - <span data-ttu-id="db717-2255">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="db717-2255">New-VpnSite</span></span>
        - <span data-ttu-id="db717-2256">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="db717-2256">Update-VpnSite</span></span>
        - <span data-ttu-id="db717-2257">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="db717-2257">New-VpnConnection</span></span>
        - <span data-ttu-id="db717-2258">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="db717-2258">Update-VpnConnection</span></span>
* <span data-ttu-id="db717-2259">修正了文件中的部分 PowerShell 範例，改為使用 Az Cmdlet 而非 AzureRM Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-2259">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="db717-2260">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="db717-2260">Az.RecoveryServices</span></span>
* <span data-ttu-id="db717-2261">透過 ProtectedItemsCount 屬性更新 AzureVMpolicy 物件</span><span class="sxs-lookup"><span data-stu-id="db717-2261">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="db717-2262">新增了 VM 原則和原始儲存體帳戶還原的測試</span><span class="sxs-lookup"><span data-stu-id="db717-2262">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="db717-2263">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="db717-2263">Az.Resources</span></span>
* <span data-ttu-id="db717-2264">修正無法在沒有參數範圍的情況下呼叫 New-AzRoleAssignment 的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="db717-2264">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="db717-2265">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="db717-2265">Az.ServiceFabric</span></span>
* <span data-ttu-id="db717-2266">修正了 'Update-AzServiceFabricReliability' 參考文件中範例的錯字</span><span class="sxs-lookup"><span data-stu-id="db717-2266">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="db717-2267">新增 Cmdlet 以管理應用程式和服務：</span><span class="sxs-lookup"><span data-stu-id="db717-2267">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="db717-2268">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="db717-2268">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="db717-2269">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="db717-2269">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="db717-2270">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="db717-2270">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="db717-2271">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="db717-2271">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="db717-2272">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="db717-2272">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="db717-2273">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="db717-2273">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="db717-2274">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="db717-2274">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="db717-2275">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="db717-2275">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="db717-2276">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="db717-2276">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="db717-2277">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="db717-2277">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="db717-2278">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="db717-2278">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="db717-2279">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="db717-2279">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="db717-2280">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="db717-2280">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="db717-2281">已將 Service Fabric SDK 更新為版本 1.2.0，此版本使用服務網狀架構資源提供者 api-version 2019-03-01。</span><span class="sxs-lookup"><span data-stu-id="db717-2281">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="db717-2282">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="db717-2282">Az.SignalR</span></span>
* <span data-ttu-id="db717-2283">新增 Update、Restart、CheckNameAvailability、GetUsage 等 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-2283">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="db717-2284">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="db717-2284">Az.Sql</span></span>
* <span data-ttu-id="db717-2285">更新 'Get-AzSqlElasticPool' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="db717-2285">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="db717-2286">新增了虛擬核心範例以建立彈性集區 (New-AzSqlElasticPool)。</span><span class="sxs-lookup"><span data-stu-id="db717-2286">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="db717-2287">移除 EmailAddresses 的驗證，並確認 Set-AzSqlServerAdvancedThreatProtectionPolicy 和 Set-AzSqlDatabaseAdvancedThreatProtectionPolicy 中的 EmailAdmins 為空的情況下 EmailAdmins 的狀態並非 false</span><span class="sxs-lookup"><span data-stu-id="db717-2287">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="db717-2288">當多個啟用稽核分類的診斷設定存在時，啟用了伺服器/資料庫稽核設定的移除功能。</span><span class="sxs-lookup"><span data-stu-id="db717-2288">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="db717-2289">修正多個 Sql 弱點評估 Cmdlet 中的電子郵件地址驗證 (Update-AzSqlDatabaseVulnerabilityAssessmentSetting、Update-AzSqlServerVulnerabilityAssessmentSetting、Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting 和 Update-AzSqlInstanceVulnerabilityAssessmentSetting)。</span><span class="sxs-lookup"><span data-stu-id="db717-2289">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="db717-2290">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="db717-2290">Az.Storage</span></span>
* <span data-ttu-id="db717-2291">已更新 'Get-AzStorageAccountKey' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="db717-2291">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="db717-2292">在上傳/下載 Azure 檔案中，支援保留目的地檔案中的來源檔案 SMB 屬性 (檔案屬性、檔案建立時間、檔案最後入時間)</span><span class="sxs-lookup"><span data-stu-id="db717-2292">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="db717-2293">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="db717-2293">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="db717-2294">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="db717-2294">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="db717-2295">修正上傳區塊 Blob 的屬性/metadate 在啟用 ImmutabilityPolicy 的容器中失敗的問題。</span><span class="sxs-lookup"><span data-stu-id="db717-2295">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="db717-2296">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="db717-2296">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="db717-2297">支援透過管理平面 API 管理 Azure 檔案共用</span><span class="sxs-lookup"><span data-stu-id="db717-2297">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="db717-2298">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="db717-2298">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="db717-2299">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="db717-2299">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="db717-2300">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="db717-2300">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="db717-2301">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="db717-2301">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="db717-2302">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="db717-2302">Az.Websites</span></span>
* <span data-ttu-id="db717-2303">修正將應用程式遷移到新的 ASP 時系統會刪除 webapp 標籤的問題</span><span class="sxs-lookup"><span data-stu-id="db717-2303">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="db717-2304">修正 Publish-AzureWebapp 以在 Linux 和 Windows 上運作</span><span class="sxs-lookup"><span data-stu-id="db717-2304">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="db717-2305">更新 'Get-AzWebAppPublishingProfile' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="db717-2305">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="db717-2306">2.6.0 - 2019 年 8 月</span><span class="sxs-lookup"><span data-stu-id="db717-2306">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="db717-2307">一般</span><span class="sxs-lookup"><span data-stu-id="db717-2307">General</span></span>
* <span data-ttu-id="db717-2308">修正了多個模組中的各種錯字問題</span><span class="sxs-lookup"><span data-stu-id="db717-2308">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="db717-2309">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="db717-2309">Az.Accounts</span></span>
* <span data-ttu-id="db717-2310">支援 Azure Functions 驗證中使用者指派的 MSI (#9479)</span><span class="sxs-lookup"><span data-stu-id="db717-2310">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="db717-2311">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="db717-2311">Az.Aks</span></span>
* <span data-ttu-id="db717-2312">修正 'Get-AzAks' 的輸出問題</span><span class="sxs-lookup"><span data-stu-id="db717-2312">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="db717-2313">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="db717-2313">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="db717-2314">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="db717-2314">Az.ApiManagement</span></span>
* <span data-ttu-id="db717-2315">修正 https://github.com/Azure/azure-powershell/issues/9351 的問題</span><span class="sxs-lookup"><span data-stu-id="db717-2315">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="db717-2316">更新 .Net NuGet 版本，此版本不會強制執行 productId、apiId、groupId 和 userId 的限制</span><span class="sxs-lookup"><span data-stu-id="db717-2316">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="db717-2317">**Get-AzApiManagementProduct** - 新增了使用 API 查詢產品的支援。</span><span class="sxs-lookup"><span data-stu-id="db717-2317">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="db717-2318">**New-AzApiManagementApiRevision** - 修正在建立新 API 版本時並未設定 ApiRevisionDescription 的問題 https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="db717-2318">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="db717-2319">將模型 'PsApiManagementOAuth2AuthrozationServer' 中的錯字修正為 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="db717-2319">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="db717-2320">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="db717-2320">Az.Batch</span></span>
* <span data-ttu-id="db717-2321">修正了說明訊息和文件中的錯字，將 Windows 首字變大寫</span><span class="sxs-lookup"><span data-stu-id="db717-2321">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="db717-2322">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="db717-2322">Az.Cdn</span></span>
* <span data-ttu-id="db717-2323">修正了 CDN 模組轉換協助程式中的錯字</span><span class="sxs-lookup"><span data-stu-id="db717-2323">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="db717-2324">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="db717-2324">Az.Compute</span></span>
* <span data-ttu-id="db717-2325">將 VmssId 新增到 New-AzVMConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-2325">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="db717-2326">將 TerminateScheduledEvents 和 TerminateScheduledEventNotBeforeTimeoutInMinutes 參數新增到 New-AzVmssConfig 和 Update-AzVmss 中</span><span class="sxs-lookup"><span data-stu-id="db717-2326">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="db717-2327">將 HyperVGeneration 屬性新增到 VM 映像物件中</span><span class="sxs-lookup"><span data-stu-id="db717-2327">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="db717-2328">新增 Host 和 HostGroup 功能</span><span class="sxs-lookup"><span data-stu-id="db717-2328">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="db717-2329">新的 Cmdlet： New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="db717-2329">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="db717-2330">已將 HostId 參數新增到 New-AzVMConfig 和 New-AzVM 中</span><span class="sxs-lookup"><span data-stu-id="db717-2330">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="db717-2331">更新 'Invoke-AzVMRunCommand' 文件中的範例，使用了正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="db717-2331">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="db717-2332">更新 'Set-AzVMDiskEncryptionExtension' 和 'Set-AzVmssDiskEncryptionExtension' 參考文件中的 '-VolumeType' 描述</span><span class="sxs-lookup"><span data-stu-id="db717-2332">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="db717-2333">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="db717-2333">Az.DataFactory</span></span>
* <span data-ttu-id="db717-2334">修正錯字，將 'New-AzDataFactoryEncryptValue' 文件中的 'Windows' 變成首字大寫</span><span class="sxs-lookup"><span data-stu-id="db717-2334">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="db717-2335">已將 ADF .Net SDK 版本更新為 4.1.2</span><span class="sxs-lookup"><span data-stu-id="db717-2335">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="db717-2336">對 'Set-AzureRmDataFactoryV2IntegrationRuntime' Cmd 新增參數 'DataProxyIntegrationRuntimeName'、'DataProxyStagingLinkedServiceName' 和 'DataProxyStagingPath'，以將自我裝載整合執行階段設定為適用於 SSIS 整合執行階段的 Proxy</span><span class="sxs-lookup"><span data-stu-id="db717-2336">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="db717-2337">更新了 PSTriggerRun 以顯示觸發的管線、訊息、屬性和 PSActivityRun，以顯示活動類型</span><span class="sxs-lookup"><span data-stu-id="db717-2337">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="db717-2338">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="db717-2338">Az.DataLakeStore</span></span>
* <span data-ttu-id="db717-2339">修正 Get-DataLakeStoreDeletedItem 凸排的問題，避免產生任何錯誤或遠端例外狀況。</span><span class="sxs-lookup"><span data-stu-id="db717-2339">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="db717-2340">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="db717-2340">Az.EventHub</span></span>
* <span data-ttu-id="db717-2341">修正 #9658 的問題：Set-AzEventHubNetworkRuleSet 中 VirtualNteworkRule 參數的錯字問題</span><span class="sxs-lookup"><span data-stu-id="db717-2341">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="db717-2342">修正 #9558 的問題：Set-AzEventHubNamespace 使用 PATCH 而非 PUT</span><span class="sxs-lookup"><span data-stu-id="db717-2342">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="db717-2343">已將 EnableKafka 參數新增到 Set-AzEventHubNamespace Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-2343">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="db717-2344">修正 #9786 的問題：無法建立僅限接聽權限的規則</span><span class="sxs-lookup"><span data-stu-id="db717-2344">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="db717-2345">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="db717-2345">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="db717-2346">修正了文件中 'Azure'均為小寫的錯字問題</span><span class="sxs-lookup"><span data-stu-id="db717-2346">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="db717-2347">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="db717-2347">Az.Monitor</span></span>
* <span data-ttu-id="db717-2348">已修正說明文件中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="db717-2348">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="db717-2349">Az.Network</span><span class="sxs-lookup"><span data-stu-id="db717-2349">Az.Network</span></span>
* <span data-ttu-id="db717-2350">更新了 New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="db717-2350">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="db717-2351">取代了 'PublicIpAddress' 參數，因為伺服器端從未使用過此參數。</span><span class="sxs-lookup"><span data-stu-id="db717-2351">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="db717-2352">新增了選用參數 'Primary'，指出正確的 IP 設定是否為主要。</span><span class="sxs-lookup"><span data-stu-id="db717-2352">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="db717-2353">改善了 SDK 要求錯誤例外狀況的處理方式 - 修正了之前未正確處理的 SDK 例外狀況而導致金鑰錯誤詳細資料並未顯示的問題</span><span class="sxs-lookup"><span data-stu-id="db717-2353">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="db717-2354">調整了 Ipv6 IP 首碼的驗證邏輯，以便檢查正確的 IPv6 前置長度。</span><span class="sxs-lookup"><span data-stu-id="db717-2354">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="db717-2355">更新了 Get-AzVirtualNetworkSubnetConfig：依子網路 ID 新增了要取得的參數集。</span><span class="sxs-lookup"><span data-stu-id="db717-2355">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="db717-2356">對 AzNetworkServiceTag 新增位置參數的描述</span><span class="sxs-lookup"><span data-stu-id="db717-2356">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="db717-2357">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="db717-2357">Az.OperationalInsights</span></span>
* <span data-ttu-id="db717-2358">更新了 'New-AzOperationalInsightsLinuxSyslogDataSource' 文件</span><span class="sxs-lookup"><span data-stu-id="db717-2358">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="db717-2359">新增了範例</span><span class="sxs-lookup"><span data-stu-id="db717-2359">Added example</span></span>
    - <span data-ttu-id="db717-2360">更新了 '-Name' 參數的說明</span><span class="sxs-lookup"><span data-stu-id="db717-2360">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="db717-2361">新增了 New-AzOperationalInsightsWindowsEventDataSource 的範例</span><span class="sxs-lookup"><span data-stu-id="db717-2361">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="db717-2362">對 New-AzOperationalInsightsWindowsEventDataSource 變更了 -Name 參數的描述</span><span class="sxs-lookup"><span data-stu-id="db717-2362">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="db717-2363">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="db717-2363">Az.RecoveryServices</span></span>
* <span data-ttu-id="db717-2364">更新 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="db717-2364">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="db717-2365">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="db717-2365">Az.Resources</span></span>
* <span data-ttu-id="db717-2366">新增對於 Microsoft.Resource 新 API 版本 2019-05-10 的支援</span><span class="sxs-lookup"><span data-stu-id="db717-2366">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="db717-2367">新增對 'copy.count = 0' 中的變數、資源和屬性的支援</span><span class="sxs-lookup"><span data-stu-id="db717-2367">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="db717-2368">完整模式中將會刪除具有 'condition = false' 或 'copy.count = 0' 的資源</span><span class="sxs-lookup"><span data-stu-id="db717-2368">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="db717-2369">在說明文件的訂閱層級中新增了指派原則範例</span><span class="sxs-lookup"><span data-stu-id="db717-2369">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="db717-2370">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="db717-2370">Az.ServiceBus</span></span>
* <span data-ttu-id="db717-2371">修正 #9658 的問題：Set-AzServiceBusNetworkRuleSet 中 VirtualNetworkRule 參數的錯字</span><span class="sxs-lookup"><span data-stu-id="db717-2371">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="db717-2372">修正 #9786 的問題：無法建立僅限接聽權限的規則</span><span class="sxs-lookup"><span data-stu-id="db717-2372">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="db717-2373">新增了 'Test-AzServiceBusNameAvailability' 命令以檢查佇列和主題的名稱可用性</span><span class="sxs-lookup"><span data-stu-id="db717-2373">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="db717-2374">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="db717-2374">Az.ServiceFabric</span></span>
* <span data-ttu-id="db717-2375">修正新增節點類型 Cmdlet 錯誤 (bug)：</span><span class="sxs-lookup"><span data-stu-id="db717-2375">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="db717-2376">當資源群組具有其他與服務網狀架構叢集不相關之 vmss 時的 NullReferenceException 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="db717-2376">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="db717-2377">修正問題： https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="db717-2377">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="db717-2378">修正若 virtualNetwork 在與叢集不同的資源群組中時 Cmdlet 會失敗的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="db717-2378">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="db717-2379">修正問題： https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="db717-2379">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="db717-2380">取代 Add-AzServiceFabricApplicationCertificate Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-2380">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="db717-2381">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="db717-2381">Az.Sql</span></span>
* <span data-ttu-id="db717-2382">更新舊版 Auditing Cmdlet 文件。</span><span class="sxs-lookup"><span data-stu-id="db717-2382">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="db717-2383">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="db717-2383">Az.Storage</span></span>
* <span data-ttu-id="db717-2384">更新 Get/Close-AzStorageFileHandle 的說明，在 Cmdlet 範例中新增更多案例並更新參數描述</span><span class="sxs-lookup"><span data-stu-id="db717-2384">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="db717-2385">支援上傳 Blob 和複製 Blob 中的 StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="db717-2385">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="db717-2386">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="db717-2386">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="db717-2387">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="db717-2387">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="db717-2388">支援複製 Blob 中的 Rehydrate Priority</span><span class="sxs-lookup"><span data-stu-id="db717-2388">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="db717-2389">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="db717-2389">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="db717-2390">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="db717-2390">Az.Websites</span></span>
* <span data-ttu-id="db717-2391">釐清 Set-AzWebApp 和 Set-AzWebAppSlot 中的 -AppSettings 參數的</span><span class="sxs-lookup"><span data-stu-id="db717-2391">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="db717-2392">2.5.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="db717-2392">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="db717-2393">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="db717-2393">Az.Accounts</span></span>
* <span data-ttu-id="db717-2394">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="db717-2394">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="db717-2395">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="db717-2395">Az.ApplicationInsights</span></span>
* <span data-ttu-id="db717-2396">修正 'Remove-AzApplicationInsightsApiKey' 文件中範例的錯字</span><span class="sxs-lookup"><span data-stu-id="db717-2396">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="db717-2397">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="db717-2397">Az.Automation</span></span>
* <span data-ttu-id="db717-2398">修正資源字串中的錯字</span><span class="sxs-lookup"><span data-stu-id="db717-2398">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="db717-2399">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="db717-2399">Az.CognitiveServices</span></span>
* <span data-ttu-id="db717-2400">新增了 NetworkRuleSet 支援。</span><span class="sxs-lookup"><span data-stu-id="db717-2400">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="db717-2401">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="db717-2401">Az.Compute</span></span>
* <span data-ttu-id="db717-2402">新增 虛擬機器執行個體檢視物件缺少的屬性 (ComputerName、OsName、OsVersion 和 HyperVGeneration)。</span><span class="sxs-lookup"><span data-stu-id="db717-2402">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="db717-2403">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="db717-2403">Az.ContainerRegistry</span></span>
* <span data-ttu-id="db717-2404">修正 Replication 參數的 Remove-AzContainerRegistryReplication 中的錯字</span><span class="sxs-lookup"><span data-stu-id="db717-2404">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="db717-2405">如需詳細資訊，請參閱 https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="db717-2405">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="db717-2406">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="db717-2406">Az.DataFactory</span></span>
* <span data-ttu-id="db717-2407">已將 ADF .Net SDK 版本更新為 4.1.0</span><span class="sxs-lookup"><span data-stu-id="db717-2407">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="db717-2408">修正 'Get-AzDataFactoryV2PipelineRun' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="db717-2408">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="db717-2409">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="db717-2409">Az.EventHub</span></span>
* <span data-ttu-id="db717-2410">新增了 Cmmdlet 以產生 SAS 權杖：New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="db717-2410">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="db717-2411">在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="db717-2411">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="db717-2412">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="db717-2412">Az.KeyVault</span></span>
* <span data-ttu-id="db717-2413">新增了為憑證原則指定 KeySize 的支援</span><span class="sxs-lookup"><span data-stu-id="db717-2413">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="db717-2414">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="db717-2414">Az.LogicApp</span></span>
* <span data-ttu-id="db717-2415">修正 Get-AzIntegrationAccountMap 以列出所有對應類型</span><span class="sxs-lookup"><span data-stu-id="db717-2415">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="db717-2416">新增了用於篩選的 MapType 參數</span><span class="sxs-lookup"><span data-stu-id="db717-2416">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="db717-2417">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="db717-2417">Az.ManagedServices</span></span>
* <span data-ttu-id="db717-2418">新增了 API 版本 2019-06-01 (GA) 的支援</span><span class="sxs-lookup"><span data-stu-id="db717-2418">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="db717-2419">Az.Network</span><span class="sxs-lookup"><span data-stu-id="db717-2419">Az.Network</span></span>
* <span data-ttu-id="db717-2420">新增私人端點和私人連結服務的支援</span><span class="sxs-lookup"><span data-stu-id="db717-2420">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="db717-2421">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-2421">New cmdlets</span></span>
        - <span data-ttu-id="db717-2422">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="db717-2422">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="db717-2423">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="db717-2423">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="db717-2424">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="db717-2424">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="db717-2425">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="db717-2425">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="db717-2426">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="db717-2426">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="db717-2427">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="db717-2427">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="db717-2428">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="db717-2428">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="db717-2429">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="db717-2429">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="db717-2430">已更新下列功能命令：Virtualnetwork 中子網路上的 PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies 旗標</span><span class="sxs-lookup"><span data-stu-id="db717-2430">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="db717-2431">更新了 New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="db717-2431">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="db717-2432">新增了選用參數 -PrivateEndpointNetworkPoliciesFlag，此參數會設定是否要套用此子網路中的私人端點網路原則。</span><span class="sxs-lookup"><span data-stu-id="db717-2432">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="db717-2433">新增了選用參數 -PrivateLinkServiceNetworkPoliciesFlag，此參數會設定是否要套用此子網路中的私人連結服務網路原則。</span><span class="sxs-lookup"><span data-stu-id="db717-2433">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="db717-2434">AzPrivateLinkService 的 Cmdlet 參數 'ServiceName' 已更名為 'Name' 搭配別名 'ServiceName' 以提供回溯相容性</span><span class="sxs-lookup"><span data-stu-id="db717-2434">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="db717-2435">針對網路安全性規則組態啟用 ICMP 通訊協定</span><span class="sxs-lookup"><span data-stu-id="db717-2435">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="db717-2436">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-2436">Updated cmdlets</span></span>
        - <span data-ttu-id="db717-2437">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="db717-2437">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="db717-2438">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="db717-2438">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="db717-2439">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="db717-2439">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="db717-2440">新增 ConnectionProtocolType (Ikev1/Ikev2) 作為 New-AzVirtualNetworkGatewayConnection 的可設定參數</span><span class="sxs-lookup"><span data-stu-id="db717-2440">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="db717-2441">在 LoadBalancerFrontendIpConfiguration 中新增 PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="db717-2441">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="db717-2442">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="db717-2442">Updated cmdlet:</span></span>
        - <span data-ttu-id="db717-2443">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="db717-2443">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="db717-2444">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="db717-2444">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="db717-2445">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="db717-2445">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="db717-2446">更新應用程式閘道 New-AzApplicationGatewayProbeConfig 命令以支援探查中的自訂連接埠</span><span class="sxs-lookup"><span data-stu-id="db717-2446">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="db717-2447">更新了 New-AzApplicationGatewayProbeConfig：新增了用來探查後端伺服器的選用參數 Port。</span><span class="sxs-lookup"><span data-stu-id="db717-2447">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="db717-2448">此參數適用於 Standard_V2 和 WAF_V2 SKU。</span><span class="sxs-lookup"><span data-stu-id="db717-2448">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="db717-2449">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="db717-2449">Az.OperationalInsights</span></span>
* <span data-ttu-id="db717-2450">更新了預設版本，讓已儲存的搜尋為 1。</span><span class="sxs-lookup"><span data-stu-id="db717-2450">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="db717-2451">修正了自訂記錄 Null 處理</span><span class="sxs-lookup"><span data-stu-id="db717-2451">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="db717-2452">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="db717-2452">Az.RecoveryServices</span></span>
* <span data-ttu-id="db717-2453">更新 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="db717-2453">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="db717-2454">更新 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="db717-2454">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="db717-2455">更新 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="db717-2455">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="db717-2456">更新 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="db717-2456">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="db717-2457">更新 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="db717-2457">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="db717-2458">更新 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="db717-2458">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="db717-2459">更新 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="db717-2459">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="db717-2460">更新 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="db717-2460">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="db717-2461">針對 Azure File Share 的 Unregistering 容器更新了服務呼叫</span><span class="sxs-lookup"><span data-stu-id="db717-2461">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="db717-2462">更新 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="db717-2462">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="db717-2463">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="db717-2463">Az.Resources</span></span>
- <span data-ttu-id="db717-2464">移除 'New-AzResourceGroupDeployment' 文件中參考的遺漏 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-2464">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="db717-2465">更新原則 Cmdlet 以使用新的 API 版本 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="db717-2465">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="db717-2466">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="db717-2466">Az.ServiceBus</span></span>
* <span data-ttu-id="db717-2467">新增了 Cmmdlet 以產生 SAS 權杖：New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="db717-2467">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="db717-2468">在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="db717-2468">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="db717-2469">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="db717-2469">Az.Sql</span></span>
* <span data-ttu-id="db717-2470">修正 Set-AzSqlDatabaseSecondary Cmdlet 遺漏的範例</span><span class="sxs-lookup"><span data-stu-id="db717-2470">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="db717-2471">修正集合弱點評量期性掃描並未提供任何電子郵件地址的問題</span><span class="sxs-lookup"><span data-stu-id="db717-2471">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="db717-2472">修正警告訊息中的錯字。</span><span class="sxs-lookup"><span data-stu-id="db717-2472">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="db717-2473">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="db717-2473">Az.Storage</span></span>
* <span data-ttu-id="db717-2474">更新 'Get-AzStorageAccount' 參考文件中的範例，以使用正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="db717-2474">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="db717-2475">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="db717-2475">Az.StorageSync</span></span>
* <span data-ttu-id="db717-2476">新增 Invoke-AzStorageSyncChangeDetection Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db717-2476">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="db717-2477">修正問題 9551 以接受 TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="db717-2477">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="db717-2478">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="db717-2478">Az.Websites</span></span>
* <span data-ttu-id="db717-2479">修正 Get-AzWebApp 和 Set-AzWebApp 並未傳回部分 SiteConfig 屬性的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="db717-2479">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="db717-2480">新增 Get-AzDeletedWebApp 和 Restore-AzDeletedWebApp 的位置參數</span><span class="sxs-lookup"><span data-stu-id="db717-2480">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="db717-2481">修正 New-AzWebApp -IncludeSourceWebAppSlots 複製 Web 應用程式的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="db717-2481">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="db717-2482">2.4.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="db717-2482">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="db717-2483">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="db717-2483">Az.Accounts</span></span>
* <span data-ttu-id="db717-2484">新增設定檔 Cmdlet 的支援</span><span class="sxs-lookup"><span data-stu-id="db717-2484">Add support for profile cmdlets</span></span>
* <span data-ttu-id="db717-2485">在產生的 Cmdlet 中新增環境和資料平面的支援</span><span class="sxs-lookup"><span data-stu-id="db717-2485">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="db717-2486">修正以下錯誤，在 Windows PowerShell 中不正確的端點在某些情況下用於資料平面 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-2486">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="db717-2487">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="db717-2487">Az.Advisor</span></span>
* <span data-ttu-id="db717-2488">Az.Advisor 的 GA 版本</span><span class="sxs-lookup"><span data-stu-id="db717-2488">GA release of Az.Advisor</span></span>
* <span data-ttu-id="db717-2489">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="db717-2489">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="db717-2490">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="db717-2490">Az.ApiManagement</span></span>
* <span data-ttu-id="db717-2491">修正 https://github.com/Azure/azure-powershell/issues/8671 的問題</span><span class="sxs-lookup"><span data-stu-id="db717-2491">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="db717-2492">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="db717-2492">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="db717-2493">新增了依使用者和產品查詢訂用帳戶的支援</span><span class="sxs-lookup"><span data-stu-id="db717-2493">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="db717-2494">新增了使用 Scope '/'、'/apis'、'/apis/echo-api' 進行查詢的支援</span><span class="sxs-lookup"><span data-stu-id="db717-2494">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="db717-2495">修正 https://github.com/Azure/azure-powershell/issues/9307 和 https://github.com/Azure/azure-powershell/issues/8432 的問題</span><span class="sxs-lookup"><span data-stu-id="db717-2495">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="db717-2496">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="db717-2496">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="db717-2497">新增了可在匯入 Api 時指定 'ApiVersion' 和 'ApiVersionSetId' 的支援</span><span class="sxs-lookup"><span data-stu-id="db717-2497">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="db717-2498">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="db717-2498">Az.Automation</span></span>
* <span data-ttu-id="db717-2499">修正了 Set-AzAutomationConnectionFieldValue Cmdlet 錯誤以處理字串值。</span><span class="sxs-lookup"><span data-stu-id="db717-2499">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="db717-2500">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="db717-2500">Az.Compute</span></span>
* <span data-ttu-id="db717-2501">將 HyperVGeneration 參數新增到 New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="db717-2501">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="db717-2502">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="db717-2502">Az.DataFactory</span></span>
* <span data-ttu-id="db717-2503">更新取得活動執行、取得管線執行和取得觸發程序執行 ADF Cmdlet 的輸出，以支援 Select-Object 管道。</span><span class="sxs-lookup"><span data-stu-id="db717-2503">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="db717-2504">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="db717-2504">Az.EventGrid</span></span>
* <span data-ttu-id="db717-2505">修正 'New-AzEventGridSubscription' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="db717-2505">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="db717-2506">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="db717-2506">Az.IotHub</span></span>
* <span data-ttu-id="db717-2507">新增對重新產生授權原則金鑰的支援。</span><span class="sxs-lookup"><span data-stu-id="db717-2507">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="db717-2508">Az.Network</span><span class="sxs-lookup"><span data-stu-id="db717-2508">Az.Network</span></span>
* <span data-ttu-id="db717-2509">已將 'RoutingPreference' 新增到公用 ip 標籤</span><span class="sxs-lookup"><span data-stu-id="db717-2509">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="db717-2510">改善 'Get-AzNetworkServiceTag' 參考文件的範例</span><span class="sxs-lookup"><span data-stu-id="db717-2510">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="db717-2511">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="db717-2511">Az.PolicyInsights</span></span>
* <span data-ttu-id="db717-2512">修正 Get-AzPolicyState 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="db717-2512">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="db717-2513">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="db717-2513">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="db717-2514">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="db717-2514">Az.OperationalInsights</span></span>
* <span data-ttu-id="db717-2515">修正了 Get-AzOperationalInsightsDataSource 中傳回的 CustomLog 資料來源模型</span><span class="sxs-lookup"><span data-stu-id="db717-2515">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="db717-2516">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="db717-2516">Az.RecoveryServices</span></span>
* <span data-ttu-id="db717-2517">修正 IaaSVM 的 get-policy 命令</span><span class="sxs-lookup"><span data-stu-id="db717-2517">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="db717-2518">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="db717-2518">Az.Resources</span></span>
    - <span data-ttu-id="db717-2519">修正 Get-AzPolicyState -Top 參數的說明文字</span><span class="sxs-lookup"><span data-stu-id="db717-2519">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="db717-2520">新增 Get-AzPolicyAlias 的用戶端分頁支援</span><span class="sxs-lookup"><span data-stu-id="db717-2520">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="db717-2521">新增 Set-AzPolicyAssignment、-PolicyParameters 和 -PolicyParametersObject 的新參數</span><span class="sxs-lookup"><span data-stu-id="db717-2521">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="db717-2522">原則 Cmdlet 的幾個文件與範例更新</span><span class="sxs-lookup"><span data-stu-id="db717-2522">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="db717-2523">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="db717-2523">Az.ServiceBus</span></span>
* <span data-ttu-id="db717-2524">修正問題 #4938 - 設定 MaxSizeInMegabytes 時，New-AzureRmServiceBusQueue 傳回 BadRequest</span><span class="sxs-lookup"><span data-stu-id="db717-2524">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="db717-2525">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="db717-2525">Az.Sql</span></span>
* <span data-ttu-id="db717-2526">從預覽版本新增執行個體容錯移轉群組 Cmdlet 至公用版本</span><span class="sxs-lookup"><span data-stu-id="db717-2526">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="db717-2527">支援使用新的 Cmdlet 進行 Azure SQL Server\資料庫稽核。</span><span class="sxs-lookup"><span data-stu-id="db717-2527">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="db717-2528">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="db717-2528">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="db717-2529">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="db717-2529">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="db717-2530">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="db717-2530">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="db717-2531">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="db717-2531">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="db717-2532">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="db717-2532">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="db717-2533">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="db717-2533">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="db717-2534">從弱點評量設定移除電子郵件條件約束</span><span class="sxs-lookup"><span data-stu-id="db717-2534">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="db717-2535">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="db717-2535">Az.Storage</span></span>
* <span data-ttu-id="db717-2536">在 Cmdlet 中將 2 個參數 '-IndexDocument' 和 '-ErrorDocument404Path' 從必要變更為選用：</span><span class="sxs-lookup"><span data-stu-id="db717-2536">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="db717-2537">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="db717-2537">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="db717-2538">藉新增範例更新 Get-AzStorageBlobContent 的說明</span><span class="sxs-lookup"><span data-stu-id="db717-2538">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="db717-2539">當 Cmdlet 失敗並出現 StorageException 時顯示錯誤詳細資訊</span><span class="sxs-lookup"><span data-stu-id="db717-2539">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="db717-2540">支援使用 Azure 檔案 AAD DS 驗證建立或更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="db717-2540">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="db717-2541">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="db717-2541">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="db717-2542">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="db717-2542">Set-AzStorageAccount</span></span>
* <span data-ttu-id="db717-2543">支援清單或關閉檔案共用、檔案目錄或檔案的檔案控制代碼</span><span class="sxs-lookup"><span data-stu-id="db717-2543">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="db717-2544">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="db717-2544">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="db717-2545">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="db717-2545">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="db717-2546">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="db717-2546">Az.StorageSync</span></span>
* <span data-ttu-id="db717-2547">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="db717-2547">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="db717-2548">2.3.2 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="db717-2548">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="db717-2549">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="db717-2549">Az.Accounts</span></span>
* <span data-ttu-id="db717-2550">修正函式呼叫時在某些情況下使用了不正確 URL 的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="db717-2550">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="db717-2551">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="db717-2551">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="db717-2552">修正從 AzureRM 到 Az Cmdlet 的別名問題</span><span class="sxs-lookup"><span data-stu-id="db717-2552">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="db717-2553">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="db717-2553">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="db717-2554">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="db717-2554">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="db717-2555">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="db717-2555">Az.Compute</span></span>
* <span data-ttu-id="db717-2556">New-AzVm and New-AzVmss 簡單參數集合現在接受 'ProximityPlacementGroup' 參數。</span><span class="sxs-lookup"><span data-stu-id="db717-2556">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="db717-2557">修正 'New-AzVM' 參考文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="db717-2557">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="db717-2558">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="db717-2558">Az.Dns</span></span>
* <span data-ttu-id="db717-2559">修正了 'Set-AzDnsZone' 說明範例中的錯字。</span><span class="sxs-lookup"><span data-stu-id="db717-2559">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="db717-2560">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="db717-2560">Az.EventGrid</span></span>
* <span data-ttu-id="db717-2561">已更新為使用 2019-06-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="db717-2561">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="db717-2562">新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="db717-2562">New cmdlets:</span></span>
    - <span data-ttu-id="db717-2563">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="db717-2563">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="db717-2564">建立新的 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="db717-2564">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="db717-2565">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="db717-2565">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="db717-2566">取得事件方格網域的詳細資料，或取得目前 Azure 訂用帳戶中的所有事件方格網域清單。</span><span class="sxs-lookup"><span data-stu-id="db717-2566">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="db717-2567">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="db717-2567">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="db717-2568">移除 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="db717-2568">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="db717-2569">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="db717-2569">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="db717-2570">重新產生 Azure 事件方格網域適用的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="db717-2570">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="db717-2571">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="db717-2571">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="db717-2572">取得用來; 事件發佈至事件方格網域的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="db717-2572">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="db717-2573">New-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="db717-2573">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="db717-2574">建立新的 Azure事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="db717-2574">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="db717-2575">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="db717-2575">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="db717-2576">取得事件方格網域主題的詳細資料，或取得目前 Azure 中特定事件方格網域下的所有事件方格網域主題清單</span><span class="sxs-lookup"><span data-stu-id="db717-2576">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="db717-2577">Remove-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="db717-2577">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="db717-2578">移除現有的 Azure 事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="db717-2578">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="db717-2579">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="db717-2579">Updated cmdlets:</span></span>
    - <span data-ttu-id="db717-2580">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="db717-2580">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="db717-2581">新增新的必要參數，以支援新的事件方格網域和事件方格網域主題管線，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="db717-2581">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="db717-2582">新增新的必要參數，以指定新的事件方格網域名稱和/或事件方格網域主題名稱，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="db717-2582">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="db717-2583">為網域和網域主題新增新的參數集合，以允許重新使用現有的參數 (例如 EndPointType、SubjectBeginsWith 等)。</span><span class="sxs-lookup"><span data-stu-id="db717-2583">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="db717-2584">新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="db717-2584">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="db717-2585">事件訂用帳戶過期日期，</span><span class="sxs-lookup"><span data-stu-id="db717-2585">Event subscription expiration date,</span></span>
            - <span data-ttu-id="db717-2586">進階篩選參數。</span><span class="sxs-lookup"><span data-stu-id="db717-2586">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="db717-2587">為 servicebusqueue 新增新的列舉成為目的地。</span><span class="sxs-lookup"><span data-stu-id="db717-2587">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="db717-2588">不允許使用 'All' in -IncludedEventType 選項並取代為</span><span class="sxs-lookup"><span data-stu-id="db717-2588">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="db717-2589">Get-AzEventGridTopic、Get-AzEventGridDomain、Get-AzEventGridDomainTopic、Get-AzEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="db717-2589">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="db717-2590">新增新的選用參數 (Top、ODataQuery 和 NextLink) 以支援結果分頁和篩選條件。</span><span class="sxs-lookup"><span data-stu-id="db717-2590">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="db717-2591">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="db717-2591">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="db717-2592">新增新的必要參數，以支援事件方格網域和事件方格網域主題管線，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="db717-2592">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="db717-2593">新增新的必要參數，以指定事件方格網域名稱和/或事件方格網域主題名稱，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="db717-2593">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="db717-2594">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="db717-2594">Az.FrontDoor</span></span>
* <span data-ttu-id="db717-2595">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="db717-2595">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="db717-2596">新增轉換支援和新的運算子自動完成值 (RegEx)</span><span class="sxs-lookup"><span data-stu-id="db717-2596">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="db717-2597">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="db717-2597">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="db717-2598">新增新的自動完成值</span><span class="sxs-lookup"><span data-stu-id="db717-2598">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="db717-2599">Az.Network</span><span class="sxs-lookup"><span data-stu-id="db717-2599">Az.Network</span></span>
* <span data-ttu-id="db717-2600">新增對虛擬網路閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="db717-2600">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="db717-2601">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-2601">New cmdlets</span></span>
        - <span data-ttu-id="db717-2602">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="db717-2602">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="db717-2603">新增 AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="db717-2603">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="db717-2604">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-2604">New cmdlets</span></span>
        - <span data-ttu-id="db717-2605">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="db717-2605">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="db717-2606">新增 PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="db717-2606">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="db717-2607">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-2607">New cmdlets</span></span>
        - <span data-ttu-id="db717-2608">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="db717-2608">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="db717-2609">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="db717-2609">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="db717-2610">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="db717-2610">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="db717-2611">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="db717-2611">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="db717-2612">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="db717-2612">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="db717-2613">新增 PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="db717-2613">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="db717-2614">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-2614">New cmdlets</span></span>
        - <span data-ttu-id="db717-2615">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="db717-2615">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="db717-2616">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="db717-2616">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="db717-2617">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="db717-2617">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="db717-2618">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="db717-2618">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="db717-2619">已更新下列功能命令：VpnConnection 上的 UseLocalAzureIpAddress 旗標</span><span class="sxs-lookup"><span data-stu-id="db717-2619">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="db717-2620">更新了 New-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="db717-2620">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="db717-2621">更新了 Set-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="db717-2621">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="db717-2622">在 ExpressRoute 對等互連中新增了唯讀欄位 PeeredConnections。</span><span class="sxs-lookup"><span data-stu-id="db717-2622">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="db717-2623">在 ExpressRoute 中新增了唯讀欄位 GlobalReachEnabled。</span><span class="sxs-lookup"><span data-stu-id="db717-2623">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="db717-2624">新增了重大變更屬性以取消取代 ExpressRouteCircuit 模型中的 AllowGlobalReach 欄位</span><span class="sxs-lookup"><span data-stu-id="db717-2624">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="db717-2625">修正了使用 TargetListenerID 搭配 AzApplicationGatewayRedirectConfiguration Cmdlet 的問題 8756 錯誤</span><span class="sxs-lookup"><span data-stu-id="db717-2625">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="db717-2626">修正了 New-AzApplicationGatewayPathRuleConfig 中的錯誤，防止進行重寫規則集合設定。</span><span class="sxs-lookup"><span data-stu-id="db717-2626">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="db717-2627">修正了在 NetworkInterfaceIpConfiguration 中顯示 VirtualNetworkTaps 的問題</span><span class="sxs-lookup"><span data-stu-id="db717-2627">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="db717-2628">修正了 Cortex Get Cmdlet 以列出所有部分</span><span class="sxs-lookup"><span data-stu-id="db717-2628">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="db717-2629">修正了 ExpressRouteGateways 和 VpnGatewayVirtualHub 的參考建立</span><span class="sxs-lookup"><span data-stu-id="db717-2629">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="db717-2630">新增了 AzureFirewall 和 NatGateway 中對可用性區域的支援</span><span class="sxs-lookup"><span data-stu-id="db717-2630">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="db717-2631">新增了 Cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="db717-2631">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="db717-2632">新增針對 Azure 防火牆的多個公用 IP 位址的支援</span><span class="sxs-lookup"><span data-stu-id="db717-2632">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="db717-2633">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="db717-2633">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="db717-2634">新增了參數 -PublicIpAddress 以接受一或多個 Public IP Address 物件</span><span class="sxs-lookup"><span data-stu-id="db717-2634">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="db717-2635">新增了參數 -VirtualNetwork 以接受虛擬網路物件</span><span class="sxs-lookup"><span data-stu-id="db717-2635">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="db717-2636">在防火牆物件中新增了 AddPublicIpAddress 和 RemovePublicIpAddress 方法 - 以接受 Public IP Address 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="db717-2636">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="db717-2637">參數 -PublicIpName 和 -VirtualNetworkName 已被取代</span><span class="sxs-lookup"><span data-stu-id="db717-2637">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="db717-2638">已更新下列功能命令：將 VpnClient AAD 驗證選項設為虛擬網路閘道資源。</span><span class="sxs-lookup"><span data-stu-id="db717-2638">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="db717-2639">已更新 New-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="db717-2639">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="db717-2640">已更新 Set-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="db717-2640">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="db717-2641">已更新 Set-AzVirtualNetworkGateway：新增了選用的切換參數 RemoveAadAuthentication 以從閘道移除 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="db717-2641">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="db717-2642">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="db717-2642">Az.OperationalInsights</span></span>
* <span data-ttu-id="db717-2643">在 'New-AzureRmOperationalInsightsWorkspace' 命令中啟用 **pergb2018** 定價層</span><span class="sxs-lookup"><span data-stu-id="db717-2643">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="db717-2644">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="db717-2644">Az.Resources</span></span>
* <span data-ttu-id="db717-2645">支援其他範本匯出選項</span><span class="sxs-lookup"><span data-stu-id="db717-2645">Support for additional Template Export options</span></span>
    - <span data-ttu-id="db717-2646">將 '-SkipResourceNameParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="db717-2646">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="db717-2647">將 '-SkipAllParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="db717-2647">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="db717-2648">將 '-Resource' parameter 新增到 Export-AzResourceGroup 以篩選已匯出的資源</span><span class="sxs-lookup"><span data-stu-id="db717-2648">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="db717-2649">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="db717-2649">Az.ServiceFabric</span></span>
* <span data-ttu-id="db717-2650">修正在某些情況下，新增 ByExistingKeyVault 憑證會產生錯誤指紋的問題</span><span class="sxs-lookup"><span data-stu-id="db717-2650">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="db717-2651">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="db717-2651">Az.Sql</span></span>
* <span data-ttu-id="db717-2652">修正進階威脅防護儲存體端點尾碼</span><span class="sxs-lookup"><span data-stu-id="db717-2652">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="db717-2653">修正進階威脅防護啟用覆寫進階威脅防護原則</span><span class="sxs-lookup"><span data-stu-id="db717-2653">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="db717-2654">為 Management.Sql 新增 Cmdlet 以允許客戶為受控執行個體新增 TDE 金鑰並設定 TDE 保護程式</span><span class="sxs-lookup"><span data-stu-id="db717-2654">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="db717-2655">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="db717-2655">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="db717-2656">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="db717-2656">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="db717-2657">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="db717-2657">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="db717-2658">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="db717-2658">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="db717-2659">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="db717-2659">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="db717-2660">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="db717-2660">Az.Storage</span></span>
* <span data-ttu-id="db717-2661">在建立儲體帳戶時支援 Kind FileStorage 和 SkuName Premium_ZRS</span><span class="sxs-lookup"><span data-stu-id="db717-2661">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="db717-2662">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="db717-2662">New-AzStorageAccount</span></span>
* <span data-ttu-id="db717-2663">釐清了 Blob 不變性 Cmdlet 的說明</span><span class="sxs-lookup"><span data-stu-id="db717-2663">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="db717-2664">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="db717-2664">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="db717-2665">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="db717-2665">Az.Websites</span></span>
* <span data-ttu-id="db717-2666">將 Get-AzWebAppCertificate 最佳化，以便依伺服器而非用戶端上的資源群組篩選</span><span class="sxs-lookup"><span data-stu-id="db717-2666">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="db717-2667">將 -UseDisasterRecovery 切換參數新增到 Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="db717-2667">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="db717-2668">2.2.0 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="db717-2668">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="db717-2669">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="db717-2669">Az.Cdn</span></span>
* <span data-ttu-id="db717-2670">已更新 Cmdlet，可支援以 API 2019-04-15 版為基礎的 rulesEngine 功能。</span><span class="sxs-lookup"><span data-stu-id="db717-2670">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="db717-2671">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="db717-2671">Az.Compute</span></span>
* <span data-ttu-id="db717-2672">已新增 `NoWait` 參數，會啟動作業並在作業完成之前立即傳回結果。</span><span class="sxs-lookup"><span data-stu-id="db717-2672">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="db717-2673">已更新的 Cmdlet： Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="db717-2673">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="db717-2674">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="db717-2674">Az.EventHub</span></span>
* <span data-ttu-id="db717-2675">修正 #9231 - Get-AzEventHubNamespace 不會傳回標記</span><span class="sxs-lookup"><span data-stu-id="db717-2675">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="db717-2676">修正 #9230 - Get-AzEventHubNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db717-2676">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="db717-2677">Az.Network</span><span class="sxs-lookup"><span data-stu-id="db717-2677">Az.Network</span></span>
* <span data-ttu-id="db717-2678">更新 Nat 閘道的 ResourceId 和 InputObject</span><span class="sxs-lookup"><span data-stu-id="db717-2678">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="db717-2679">新增 ResourceId 和 InputObject 的別名</span><span class="sxs-lookup"><span data-stu-id="db717-2679">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="db717-2680">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="db717-2680">Az.PolicyInsights</span></span>
* <span data-ttu-id="db717-2681">修正 Get-AzPolicyEvent 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="db717-2681">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="db717-2682">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="db717-2682">Az.RecoveryServices</span></span>
* <span data-ttu-id="db717-2683">IaaSVM 原則的最小保留天數從 1 天變更為 7 天</span><span class="sxs-lookup"><span data-stu-id="db717-2683">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="db717-2684">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="db717-2684">Az.ServiceBus</span></span>
* <span data-ttu-id="db717-2685">修正 issue #9182 - Get-AzServiceBusNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db717-2685">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="db717-2686">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="db717-2686">Az.ServiceFabric</span></span>
* <span data-ttu-id="db717-2687">修正 'Update-AzServiceFabricReliability' 錯誤訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="db717-2687">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="db717-2688">修正 Service Fabric 命令列中的遺漏字元</span><span class="sxs-lookup"><span data-stu-id="db717-2688">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="db717-2689">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="db717-2689">Az.Sql</span></span>
* <span data-ttu-id="db717-2690">為 New-AzureSqlInstance Cmdlet 新增 DnsZonePartner 參數，以支援受控執行個體的 AutoDr。</span><span class="sxs-lookup"><span data-stu-id="db717-2690">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="db717-2691">即將淘汰 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-2691">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="db717-2692">將威脅偵測 Cmdlet 重新命名為進階威脅防護</span><span class="sxs-lookup"><span data-stu-id="db717-2692">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="db717-2693">New-AzSqlInstance -StorageSizeInGB 和 -LicenseType 現在是選擇性的參數。</span><span class="sxs-lookup"><span data-stu-id="db717-2693">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="db717-2694">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="db717-2694">Az.Websites</span></span>
* <span data-ttu-id="db717-2695">修正 Set-AzWebApp 和 Set-AzWebAppSlot 搭配使用 -WebApp 屬性時會移除標記的問題</span><span class="sxs-lookup"><span data-stu-id="db717-2695">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="db717-2696">2.1.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="db717-2696">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="db717-2697">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="db717-2697">Az.ApiManagement</span></span>
* <span data-ttu-id="db717-2698">已建立新的 Cmdlet，用以管理全域和 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="db717-2698">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="db717-2699">**Get-AzApiManagementDiagnostic** - 取得設定於全域或 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="db717-2699">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="db717-2700">**New-AzApiManagementDiagnostic** - 在全域範圍或 API 範圍建立新的診斷</span><span class="sxs-lookup"><span data-stu-id="db717-2700">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="db717-2701">**New-AzApiManagementHttpMessageDiagnostic** - 建立關於要記錄哪些標頭和本文位元組大小的診斷設定</span><span class="sxs-lookup"><span data-stu-id="db717-2701">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="db717-2702">**New-AzApiManagementPipelineDiagnosticSetting** - 建立閘道的傳入/傳出 HTTP 訊息的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="db717-2702">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="db717-2703">**New-AzApiManagementSamplingSetting** - 建立診斷要求/回應的取樣設定</span><span class="sxs-lookup"><span data-stu-id="db717-2703">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="db717-2704">**Remove-AzApiManagementDiagnostic** - 移除全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="db717-2704">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="db717-2705">**Set-AzApiManagementDiagnostic** - 更新全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="db717-2705">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="db717-2706">已建立新的 Cmdlet 用以管理 ApiManagement 服務中的快取</span><span class="sxs-lookup"><span data-stu-id="db717-2706">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="db717-2707">**Get-AzApiManagementCache** - 取得識別碼所指定的快取或所有快取的詳細資料</span><span class="sxs-lookup"><span data-stu-id="db717-2707">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="db717-2708">**New-AzApiManagementCache** - 建立新的「預設」快取或特定 Azure「區域」中的快取</span><span class="sxs-lookup"><span data-stu-id="db717-2708">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="db717-2709">**Remove-AzApiManagementCache** - 移除快取</span><span class="sxs-lookup"><span data-stu-id="db717-2709">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="db717-2710">**Update-AzApiManagementCache** - 更新快取</span><span class="sxs-lookup"><span data-stu-id="db717-2710">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="db717-2711">已建立新的 Cmdlet 用以管理 API 結構描述</span><span class="sxs-lookup"><span data-stu-id="db717-2711">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="db717-2712">**New-AzApiManagementSchema** - 為 API 建立新的結構描述</span><span class="sxs-lookup"><span data-stu-id="db717-2712">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="db717-2713">**Get-AzApiManagementSchema** - 取得在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="db717-2713">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="db717-2714">**Remove-AzApiManagementSchema** - 移除在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="db717-2714">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="db717-2715">**Set-AzApiManagementSchema** - 更新在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="db717-2715">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="db717-2716">已建立新的 Cmdlet 用以產生使用者權杖。</span><span class="sxs-lookup"><span data-stu-id="db717-2716">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="db717-2717">**New-AzApiManagementUserToken** - 產生預設有效期為 8 小時的新使用者權杖。'GIT' 使用者的權杖可使用此 Cmdlet 產生。/</span><span class="sxs-lookup"><span data-stu-id="db717-2717">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="db717-2718">已建立新的 Cmdlet 用以擷取網路狀態</span><span class="sxs-lookup"><span data-stu-id="db717-2718">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="db717-2719">**Get-AzApiManagementNetworkStatus** - 取得 API 管理服務相依資源的網路狀態連線。</span><span class="sxs-lookup"><span data-stu-id="db717-2719">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="db717-2720">這在將 ApiManagement 服務部署到虛擬網路和驗證是否有任何相依性中斷時，將可發揮效用。</span><span class="sxs-lookup"><span data-stu-id="db717-2720">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="db717-2721">已更新 Cmdlet **New-AzApiManagement**，用以管理 ApiManagement 服務</span><span class="sxs-lookup"><span data-stu-id="db717-2721">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="db717-2722">已加入新的「使用量」SKU 的支援</span><span class="sxs-lookup"><span data-stu-id="db717-2722">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="db717-2723">已加入為「使用量」SKU 開啟 'EnableClientCertificate' 旗標的支援</span><span class="sxs-lookup"><span data-stu-id="db717-2723">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="db717-2724">新的 Cmdlet **New-AzApiManagementSslSetting** 允許在「後端」和「前端」設定 'TLS/SSL' 設定。</span><span class="sxs-lookup"><span data-stu-id="db717-2724">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="db717-2725">這也可用來在 ApiManagement 服務的「前端」設定「編碼器」 (例如 '3DES') 和 'ServerProtocols' (例如 'Http2')。</span><span class="sxs-lookup"><span data-stu-id="db717-2725">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="db717-2726">已加入在 ApiManagement 服務上設定 'DeveloperPortal' 主機名稱的支援。</span><span class="sxs-lookup"><span data-stu-id="db717-2726">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="db717-2727">已更新 Cmdlet **Get-AzApiManagementSsoToken**，以使用 'PsApiManagement' 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="db717-2727">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="db717-2728">已更新 Cmdlet 以顯示內嵌錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="db717-2728">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="db717-2729">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy :錯誤碼：ValidationError 錯誤訊息：有一或多個欄位包含不正確的值：錯誤詳細資料：[Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10:Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="db717-2729">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="db717-2730">已更新 Cmdlet **Export-AzApiManagementApi**，以採用 'OpenApi 3.0' 格式匯出 API</span><span class="sxs-lookup"><span data-stu-id="db717-2730">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="db717-2731">已更新 Cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="db717-2731">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="db717-2732">以從 'OpenApi 3.0' 文件規格匯入 API</span><span class="sxs-lookup"><span data-stu-id="db717-2732">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="db717-2733">以覆寫任何 ('Swagger'、'Wadl'、'Wsdl'、'OpenApi') 文件中指定的 'PsApiManagementSchema' 屬性。</span><span class="sxs-lookup"><span data-stu-id="db717-2733">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="db717-2734">以覆寫任何文件中指定的 'ServiceUrl' 屬性。</span><span class="sxs-lookup"><span data-stu-id="db717-2734">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="db717-2735">已更新 Cmdlet **Get-AzApiManagementPolicy**，以透過使用 'rawxml' 的非 XML 逸出「格式」傳回原則</span><span class="sxs-lookup"><span data-stu-id="db717-2735">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="db717-2736">已更新 Cmdlet **Set-AzApiManagementPolicy**，以接受使用 'rawxml' 的非 XML 逸出「格式」和使用 'xml' 溢出的 XML 格式的原則</span><span class="sxs-lookup"><span data-stu-id="db717-2736">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="db717-2737">已更新 Cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="db717-2737">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="db717-2738">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="db717-2738">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="db717-2739">以在 'ApiVersionSet' 中建立 API</span><span class="sxs-lookup"><span data-stu-id="db717-2739">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="db717-2740">以使用 'SourceApiId' 和 'SourceApiRevision' 複製 API。</span><span class="sxs-lookup"><span data-stu-id="db717-2740">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="db717-2741">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="db717-2741">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="db717-2742">已更新 Cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="db717-2742">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="db717-2743">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="db717-2743">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="db717-2744">以在 'ApiVersionSet' 中更新 API</span><span class="sxs-lookup"><span data-stu-id="db717-2744">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="db717-2745">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="db717-2745">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="db717-2746">已更新 Cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="db717-2746">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="db717-2747">以使用 'SourceApiRevision' 複製 (複製標記、產品、作業和原則) 現有的修訂。</span><span class="sxs-lookup"><span data-stu-id="db717-2747">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="db717-2748">新的修訂會採用父代的 'ApiId'。</span><span class="sxs-lookup"><span data-stu-id="db717-2748">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="db717-2749">以提供 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="db717-2749">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="db717-2750">以在複製 API 時覆寫 'ServiceUrl'。</span><span class="sxs-lookup"><span data-stu-id="db717-2750">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="db717-2751">已更新 Cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="db717-2751">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="db717-2752">以透過 'Authority' 設定 'AAD' 或 'AADB2C'</span><span class="sxs-lookup"><span data-stu-id="db717-2752">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="db717-2753">以設定 'SignupPolicy'、'SigninPolicy'、'ProfileEditingPolicy' 和 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="db717-2753">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="db717-2754">已更新 Cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="db717-2754">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="db717-2755">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="db717-2755">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="db717-2756">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="db717-2756">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="db717-2757">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="db717-2757">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="db717-2758">已更新 Cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="db717-2758">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="db717-2759">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="db717-2759">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="db717-2760">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="db717-2760">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="db717-2761">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="db717-2761">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="db717-2762">已更新下列 Cmdlet，以接受 'ResourceId' 作為輸入</span><span class="sxs-lookup"><span data-stu-id="db717-2762">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="db717-2763">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="db717-2763">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="db717-2764">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="db717-2764">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="db717-2765">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="db717-2765">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="db717-2766">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="db717-2766">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="db717-2767">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="db717-2767">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="db717-2768">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="db717-2768">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="db717-2769">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="db717-2769">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="db717-2770">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="db717-2770">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="db717-2771">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="db717-2771">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="db717-2772">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="db717-2772">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="db717-2773">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="db717-2773">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="db717-2774">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="db717-2774">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="db717-2775">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="db717-2775">Az.Automation</span></span>
* <span data-ttu-id="db717-2776">已更新 Get-AzAutomationJobOutputRecord 以處理 JSON 和文字記錄值。</span><span class="sxs-lookup"><span data-stu-id="db717-2776">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="db717-2777">修正 https://github.com/Azure/azure-powershell/issues/7977 的問題</span><span class="sxs-lookup"><span data-stu-id="db717-2777">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="db717-2778">修正 https://github.com/Azure/azure-powershell/issues/8600 的問題</span><span class="sxs-lookup"><span data-stu-id="db717-2778">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="db717-2779">已將 Start-AzAutomationDscCompilationJob 的行為變更為僅啟動作業而不等候作業完成。</span><span class="sxs-lookup"><span data-stu-id="db717-2779">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="db717-2780">修正 https://github.com/Azure/azure-powershell/issues/8347 的問題</span><span class="sxs-lookup"><span data-stu-id="db717-2780">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="db717-2781">修正 Get-AzAutomationDscNode 在使用 -Name 時會傳回所有節點的問題。</span><span class="sxs-lookup"><span data-stu-id="db717-2781">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="db717-2782">現在它只會相符的節點。</span><span class="sxs-lookup"><span data-stu-id="db717-2782">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="db717-2783">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="db717-2783">Az.Compute</span></span>
* <span data-ttu-id="db717-2784">將 ProtectFromScaleIn 和 ProtectFromScaleSetAction 參數新增至 Update-AzVmssVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db717-2784">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="db717-2785">在不支援「美國東部」時，New-AzVM wimple 參數現在依預設會使用可用的位置</span><span class="sxs-lookup"><span data-stu-id="db717-2785">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="db717-2786">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="db717-2786">Az.DataLakeStore</span></span>
* <span data-ttu-id="db717-2787">更新 ADLS SDK 以使用 httpclient，並透過 Azure 架構整合資料平面測試</span><span class="sxs-lookup"><span data-stu-id="db717-2787">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="db717-2788">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="db717-2788">Az.Monitor</span></span>
* <span data-ttu-id="db717-2789">已修正說明範例中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="db717-2789">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="db717-2790">Az.Network</span><span class="sxs-lookup"><span data-stu-id="db717-2790">Az.Network</span></span>
* <span data-ttu-id="db717-2791">將 DisableBgpRoutePropagation 旗標新增至有效路由表輸出</span><span class="sxs-lookup"><span data-stu-id="db717-2791">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="db717-2792">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="db717-2792">Updated cmdlet:</span></span>
        - <span data-ttu-id="db717-2793">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="db717-2793">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="db717-2794">修正 New-AzApplicationGatewayTrustedRootCertificate 文件中的雙破折號</span><span class="sxs-lookup"><span data-stu-id="db717-2794">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="db717-2795">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="db717-2795">Az.Resources</span></span>
* <span data-ttu-id="db717-2796">新增 Cmdlet Get-AzureRmDenyAssignment 用以擷取拒絕指派</span><span class="sxs-lookup"><span data-stu-id="db717-2796">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="db717-2797">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="db717-2797">Az.Sql</span></span>
* <span data-ttu-id="db717-2798">將進階威脅防護 Cmdlet 重新命名為進階資料安全性的，並依預設啟用弱點評量</span><span class="sxs-lookup"><span data-stu-id="db717-2798">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="db717-2799">2.0.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="db717-2799">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="db717-2800">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="db717-2800">Az.Accounts</span></span>
* <span data-ttu-id="db717-2801">更新驗證程式庫以修正 ADFS 的使用者名稱/密碼驗證問題</span><span class="sxs-lookup"><span data-stu-id="db717-2801">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="db717-2802">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="db717-2802">Az.CognitiveServices</span></span>
* <span data-ttu-id="db717-2803">只顯示 Bing 搜尋服務的 Bing 免責聲明。</span><span class="sxs-lookup"><span data-stu-id="db717-2803">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="db717-2804">改善建立帳戶失敗時的錯誤。</span><span class="sxs-lookup"><span data-stu-id="db717-2804">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="db717-2805">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="db717-2805">Az.Compute</span></span>
* <span data-ttu-id="db717-2806">鄰近放置群組功能。</span><span class="sxs-lookup"><span data-stu-id="db717-2806">Proximity placement group feature.</span></span>
    - <span data-ttu-id="db717-2807">新增下列 Cmdlet： New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="db717-2807">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="db717-2808">將新參數 ProximityPlacementGroupId 新增至下列 Cmdlet： New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="db717-2808">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="db717-2809">將 StorageAccountType 參數新增至 New-AzGalleryImageVersion。</span><span class="sxs-lookup"><span data-stu-id="db717-2809">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="db717-2810">New-AzGalleryImageVersion 的 TargetRegion 可包含 StorageAccountType。</span><span class="sxs-lookup"><span data-stu-id="db717-2810">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="db717-2811">將 SkipShutdown 切換參數新增至 Stop-AzVM 和 Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="db717-2811">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="db717-2812">重大變更</span><span class="sxs-lookup"><span data-stu-id="db717-2812">Breaking changes</span></span>
    - <span data-ttu-id="db717-2813">將 Set-AzVMBootDiagnostics 變更為 Set-AzVMBootDiagnostic。</span><span class="sxs-lookup"><span data-stu-id="db717-2813">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="db717-2814">將 Export-AzLogAnalyticThrottledRequests 變更為 Export-AzLogAnalyticThrottledRequests。</span><span class="sxs-lookup"><span data-stu-id="db717-2814">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="db717-2815">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="db717-2815">Az.DeploymentManager</span></span>
* <span data-ttu-id="db717-2816">第一版正式運作的 Azure 部署管理員 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-2816">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="db717-2817">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="db717-2817">Az.Dns</span></span>
* <span data-ttu-id="db717-2818">自動的 DNS NameServer 委派</span><span class="sxs-lookup"><span data-stu-id="db717-2818">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="db717-2819">建立 DNS 區域 Cmdlet 可接受父代區域名稱作為其他選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="db717-2819">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="db717-2820">針對新建立的子系區域，在父代區域中新增 NS 記錄。</span><span class="sxs-lookup"><span data-stu-id="db717-2820">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="db717-2821">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="db717-2821">Az.FrontDoor</span></span>
* <span data-ttu-id="db717-2822">第一版正式運作的 Azure FrontDoor Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-2822">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="db717-2823">重新命名 WAF Cmdlet 以包含 'Waf'</span><span class="sxs-lookup"><span data-stu-id="db717-2823">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="db717-2824">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="db717-2824">Az.HDInsight</span></span>
* <span data-ttu-id="db717-2825">移除兩個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="db717-2825">Removed two cmdlets:</span></span>
    - <span data-ttu-id="db717-2826">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="db717-2826">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="db717-2827">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="db717-2827">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="db717-2828">已新增 Set-AzHDInsightGatewayCredential Cmdlet 來取代 Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="db717-2828">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="db717-2829">更新 Get-AzHDInsightJobOutput Cmdlet 以區分讀者角色和 HDInsight 操作員角色：</span><span class="sxs-lookup"><span data-stu-id="db717-2829">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="db717-2830">具有讀者角色的使用者必須明確指定 'DefaultStorageAccountKey' 參數，否則會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="db717-2830">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="db717-2831">具有 HDInsight 操作員角色的使用者不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="db717-2831">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="db717-2832">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="db717-2832">Az.Monitor</span></span>
* <span data-ttu-id="db717-2833">SQR API 的新 Cmdlet (已排程的查詢規則)</span><span class="sxs-lookup"><span data-stu-id="db717-2833">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="db717-2834">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="db717-2834">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="db717-2835">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="db717-2835">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="db717-2836">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="db717-2836">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="db717-2837">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="db717-2837">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="db717-2838">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="db717-2838">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="db717-2839">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="db717-2839">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="db717-2840">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="db717-2840">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="db717-2841">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="db717-2841">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="db717-2842">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="db717-2842">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="db717-2843">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="db717-2843">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="db717-2844">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="db717-2844">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="db717-2845">[更多](/rest/api/monitor/scheduledqueryrules) SQR API 的相關資訊</span><span class="sxs-lookup"><span data-stu-id="db717-2845">[More](/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="db717-2846">更新 Az.Monitor.md，以包含用於 GenV2 (非傳統) 計量式警示規則的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-2846">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="db717-2847">Az.Network</span><span class="sxs-lookup"><span data-stu-id="db717-2847">Az.Network</span></span>
* <span data-ttu-id="db717-2848">新增 Nat 閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="db717-2848">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="db717-2849">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-2849">New cmdlets</span></span>
        - <span data-ttu-id="db717-2850">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="db717-2850">New-AzNatGateway</span></span>
        - <span data-ttu-id="db717-2851">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="db717-2851">Get-AzNatGateway</span></span>
        - <span data-ttu-id="db717-2852">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="db717-2852">Set-AzNatGateway</span></span>
        - <span data-ttu-id="db717-2853">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="db717-2853">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="db717-2854">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-2854">Updated cmdlets</span></span>
        - <span data-ttu-id="db717-2855">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="db717-2855">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="db717-2856">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="db717-2856">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="db717-2857">已更新下列功能命令：設定/移除 Brooklyn 閘道上的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="db717-2857">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="db717-2858">已更新 New-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="db717-2858">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="db717-2859">已更新 Set-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="db717-2859">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="db717-2860">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="db717-2860">Az.PolicyInsights</span></span>
* <span data-ttu-id="db717-2861">支援查詢原則的評估詳細資料。</span><span class="sxs-lookup"><span data-stu-id="db717-2861">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="db717-2862">將 '-Expand' 參數新增至 Get-AzPolicyState。</span><span class="sxs-lookup"><span data-stu-id="db717-2862">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="db717-2863">支援 '-Expand PolicyEvaluationDetails'。</span><span class="sxs-lookup"><span data-stu-id="db717-2863">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="db717-2864">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="db717-2864">Az.RecoveryServices</span></span>
* <span data-ttu-id="db717-2865">支援跨訂用帳戶的 Azure 到 Azure 站台復原。</span><span class="sxs-lookup"><span data-stu-id="db717-2865">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="db717-2866">標示 Azure Site Recovery 上即將進行的重大變更。</span><span class="sxs-lookup"><span data-stu-id="db717-2866">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="db717-2867">Azure Site Recovery 復原計劃和行動計劃的修正。</span><span class="sxs-lookup"><span data-stu-id="db717-2867">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="db717-2868">Azure 到 Azure 的 Azure Site Recovery 更新網路對應修正。</span><span class="sxs-lookup"><span data-stu-id="db717-2868">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="db717-2869">受控磁碟中 Azure 到 Azure 的 Azure Site Recovery 更新保護方向修正。</span><span class="sxs-lookup"><span data-stu-id="db717-2869">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="db717-2870">其他小幅修正。</span><span class="sxs-lookup"><span data-stu-id="db717-2870">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="db717-2871">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="db717-2871">Az.Relay</span></span>
* <span data-ttu-id="db717-2872">修正客戶訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="db717-2872">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="db717-2873">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="db717-2873">Az.ServiceBus</span></span>
* <span data-ttu-id="db717-2874">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-2874">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="db717-2875">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="db717-2875">Az.Storage</span></span>
* <span data-ttu-id="db717-2876">升級至儲存體用戶端程式庫 10.0.1 (此 SDK 中所有物件的命名空間會從 'Microsoft.WindowsAzure.Storage. *' 變更為 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="db717-2876">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="db717-2877">升級至 Microsoft.Azure.Management.Storage 11.0.0，以支援新的 API 版本 2019-04-01。</span><span class="sxs-lookup"><span data-stu-id="db717-2877">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="db717-2878">建立儲存體帳戶中的預設儲存體帳戶類型從 'Storage' 變更為 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="db717-2878">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="db717-2879">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="db717-2879">New-AzStorageAccount</span></span>
* <span data-ttu-id="db717-2880">藉由加入 '-'，將儲存體帳戶 Cmdlet 輸出 Sku.Name 變成和輸入 SkuName 一致，例如將 'StandardLRS' 變更為 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="db717-2880">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="db717-2881">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="db717-2881">New-AzStorageAccount</span></span>
    - <span data-ttu-id="db717-2882">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="db717-2882">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="db717-2883">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="db717-2883">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="db717-2884">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="db717-2884">Az.Websites</span></span>
* <span data-ttu-id="db717-2885">Get-AzWebApp 傳回的 PSSite 物件現在會設定 'Kind' 屬性</span><span class="sxs-lookup"><span data-stu-id="db717-2885">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="db717-2886">Get-AzWebApp\*Metrics 和 Get-AzAppServicePlanMetrics 已標示為淘汰</span><span class="sxs-lookup"><span data-stu-id="db717-2886">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="db717-2887">1.8.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="db717-2887">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="db717-2888">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="db717-2888">Highlights since the last major release</span></span>
* <span data-ttu-id="db717-2889">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="db717-2889">General availability of `Az` module</span></span>
* <span data-ttu-id="db717-2890">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="db717-2890">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="db717-2891">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="db717-2891">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="db717-2892">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="db717-2892">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="db717-2893">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="db717-2893">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="db717-2894">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="db717-2894">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="db717-2895">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-2895">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="db717-2896">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="db717-2896">Az.Accounts</span></span>
* <span data-ttu-id="db717-2897">更新 Uninstall-AzureRm 以在 Mac 中正確刪除模組</span><span class="sxs-lookup"><span data-stu-id="db717-2897">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="db717-2898">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="db717-2898">Az.Batch</span></span>
* <span data-ttu-id="db717-2899">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="db717-2899">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="db717-2900">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="db717-2900">Az.Cdn</span></span>
* <span data-ttu-id="db717-2901">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="db717-2901">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="db717-2902">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="db717-2902">Az.CognitiveServices</span></span>
* <span data-ttu-id="db717-2903">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="db717-2903">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="db717-2904">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="db717-2904">Az.Compute</span></span>
* <span data-ttu-id="db717-2905">如果磁碟的資源識別碼中有小寫資源群組，則修正 AEM 安裝問題</span><span class="sxs-lookup"><span data-stu-id="db717-2905">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="db717-2906">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="db717-2906">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="db717-2907">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="db717-2907">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="db717-2908">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="db717-2908">Az.DataFactory</span></span>
* <span data-ttu-id="db717-2909">如果受控整合執行階段的 NodeCount 不是 Null，則新增 SsisProperties。</span><span class="sxs-lookup"><span data-stu-id="db717-2909">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="db717-2910">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="db717-2910">Az.DataLakeStore</span></span>
* <span data-ttu-id="db717-2911">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="db717-2911">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="db717-2912">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="db717-2912">Az.EventGrid</span></span>
* <span data-ttu-id="db717-2913">已更新端點的說明文字，指出應該先建立資源，才能使用建立/更新事件訂用帳戶 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db717-2913">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="db717-2914">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="db717-2914">Az.EventHub</span></span>
* <span data-ttu-id="db717-2915">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-2915">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="db717-2916">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="db717-2916">Az.HDInsight</span></span>
* <span data-ttu-id="db717-2917">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="db717-2917">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="db717-2918">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="db717-2918">Az.IotHub</span></span>
* <span data-ttu-id="db717-2919">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="db717-2919">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="db717-2920">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="db717-2920">Az.KeyVault</span></span>
* <span data-ttu-id="db717-2921">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="db717-2921">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="db717-2922">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="db717-2922">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="db717-2923">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="db717-2923">Az.MachineLearning</span></span>
* <span data-ttu-id="db717-2924">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="db717-2924">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="db717-2925">Az.Media</span><span class="sxs-lookup"><span data-stu-id="db717-2925">Az.Media</span></span>
* <span data-ttu-id="db717-2926">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="db717-2926">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="db717-2927">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="db717-2927">Az.Monitor</span></span>
  * <span data-ttu-id="db717-2928">適用於 GenV2 (非傳統) 計量型警示規則的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-2928">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="db717-2929">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="db717-2929">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="db717-2930">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="db717-2930">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="db717-2931">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="db717-2931">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="db717-2932">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="db717-2932">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="db717-2933">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="db717-2933">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="db717-2934">監視器 SDK 已更新為版本 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="db717-2934">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="db717-2935">Az.Network</span><span class="sxs-lookup"><span data-stu-id="db717-2935">Az.Network</span></span>
* <span data-ttu-id="db717-2936">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="db717-2936">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="db717-2937">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="db717-2937">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="db717-2938">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="db717-2938">Az.NotificationHubs</span></span>
* <span data-ttu-id="db717-2939">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="db717-2939">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="db717-2940">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="db717-2940">Az.OperationalInsights</span></span>
* <span data-ttu-id="db717-2941">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="db717-2941">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="db717-2942">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="db717-2942">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="db717-2943">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="db717-2943">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="db717-2944">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="db717-2944">Az.RecoveryServices</span></span>
* <span data-ttu-id="db717-2945">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="db717-2945">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="db717-2946">已更新 Azure VM 中 SQL 的資料表格式</span><span class="sxs-lookup"><span data-stu-id="db717-2946">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="db717-2947">已新增替代方法來擷取 AzureFileShare 中的位置</span><span class="sxs-lookup"><span data-stu-id="db717-2947">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="db717-2948">已根據時區更新 SchedulePolicy 物件中的 ScheduleRunDays</span><span class="sxs-lookup"><span data-stu-id="db717-2948">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="db717-2949">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="db717-2949">Az.RedisCache</span></span>
* <span data-ttu-id="db717-2950">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="db717-2950">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="db717-2951">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="db717-2951">Az.Resources</span></span>
* <span data-ttu-id="db717-2952">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="db717-2952">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="db717-2953">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="db717-2953">Az.Sql</span></span>
* <span data-ttu-id="db717-2954">以通用程式碼取代監視器 SDK 的相依性</span><span class="sxs-lookup"><span data-stu-id="db717-2954">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="db717-2955">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="db717-2955">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="db717-2956">已增強多個資料行分類的程序。</span><span class="sxs-lookup"><span data-stu-id="db717-2956">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="db717-2957">在來自 Get-AzSqlServerServiceObjective 的回應中包含 sku 屬性 (sku 名稱、系列、容量)，並依預設格式化為資料表。</span><span class="sxs-lookup"><span data-stu-id="db717-2957">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="db717-2958">依位置 Get-AzSqlServerServiceObjective 的能力，而區域中不需要預先存在的伺服器。</span><span class="sxs-lookup"><span data-stu-id="db717-2958">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="db717-2959">在受控執行個體中支援建立時區參數。</span><span class="sxs-lookup"><span data-stu-id="db717-2959">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="db717-2960">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="db717-2960">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="db717-2961">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="db717-2961">Az.Websites</span></span>
* <span data-ttu-id="db717-2962">將 Set-AzWebApp 和 Set-AzWebAppSlot 修正為不在執行時移除標記</span><span class="sxs-lookup"><span data-stu-id="db717-2962">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="db717-2963">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="db717-2963">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="db717-2964">已更新網站 SDK。</span><span class="sxs-lookup"><span data-stu-id="db717-2964">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="db717-2965">已從 PSAppServicePlan 中移除 AdminSiteName 屬性。</span><span class="sxs-lookup"><span data-stu-id="db717-2965">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="db717-2966">1.7.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="db717-2966">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="db717-2967">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="db717-2967">Highlights since the last major release</span></span>
* <span data-ttu-id="db717-2968">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="db717-2968">General availability of `Az` module</span></span>
* <span data-ttu-id="db717-2969">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="db717-2969">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="db717-2970">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="db717-2970">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="db717-2971">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="db717-2971">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="db717-2972">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="db717-2972">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="db717-2973">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="db717-2973">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="db717-2974">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-2974">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="db717-2975">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="db717-2975">Az.Accounts</span></span>
* <span data-ttu-id="db717-2976">已將 Add-AzEnvironment 和 Set-AzEnvironment 更新為接受 AzureAnalysisServicesEndpointResourceId 參數</span><span class="sxs-lookup"><span data-stu-id="db717-2976">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="db717-2977">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="db717-2977">Az.AnalysisServices</span></span>
* <span data-ttu-id="db717-2978">在 dataplane Cmdlet 中使用 ServiceClient，並移除原始的驗證邏輯</span><span class="sxs-lookup"><span data-stu-id="db717-2978">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="db717-2979">讓 Add-AzureASAccount 成為 Connect-AzAccount 的包裝函式，以避免重大變更</span><span class="sxs-lookup"><span data-stu-id="db717-2979">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="db717-2980">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="db717-2980">Az.Automation</span></span>
* <span data-ttu-id="db717-2981">修正 Inclusions 的 New-AzAutomationSoftwareUpdateConfiguration Cmdlet 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="db717-2981">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="db717-2982">現在，IncludedKbNumber 和 IncludedPackageNameMask 參數應會正常運作。</span><span class="sxs-lookup"><span data-stu-id="db717-2982">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="db717-2983">修正 Azure 自動化更新管理動態群組的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="db717-2983">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="db717-2984">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="db717-2984">Az.Compute</span></span>
* <span data-ttu-id="db717-2985">將 HyperVGeneration 參數新增至 New-AzDiskConfig 和 New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="db717-2985">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="db717-2986">允許使用其他租用戶的資源庫映像來建立 VM。</span><span class="sxs-lookup"><span data-stu-id="db717-2986">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="db717-2987">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="db717-2987">Az.ContainerInstance</span></span>
* <span data-ttu-id="db717-2988">已修正 New-AzContainerGroup 的 -Command 參數問題，其加入了尾端空白的引數</span><span class="sxs-lookup"><span data-stu-id="db717-2988">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="db717-2989">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="db717-2989">Az.DataFactory</span></span>
* <span data-ttu-id="db717-2990">已將 ADF .Net SDK 版本更新為 3.0.2</span><span class="sxs-lookup"><span data-stu-id="db717-2990">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="db717-2991">已透過 RepoConfiguration 相關設定的額外參數來更新 Set-AzDataFactoryV2 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db717-2991">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="db717-2992">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="db717-2992">Az.Resources</span></span>
* <span data-ttu-id="db717-2993">改善提供 '-ResourceId' 或 '-ResourceGroupName'、'-Name' 和 '-ResourceType' 參數時，'Get-AzResource' 的提供者處理</span><span class="sxs-lookup"><span data-stu-id="db717-2993">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="db717-2994">改善 'Test-AzDeployment' 和 'Test-AzResourceGroupDeployment' 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="db717-2994">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="db717-2995">處理部署驗證外擲回的錯誤，並改為將其包含在命令輸出中</span><span class="sxs-lookup"><span data-stu-id="db717-2995">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="db717-2996">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="db717-2996">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="db717-2997">將 '-IgnoreDynamicParameters' 切換參數新增至部署 Cmdlet 的集合，以略過指令碼和作業案例中的提示</span><span class="sxs-lookup"><span data-stu-id="db717-2997">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="db717-2998">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="db717-2998">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="db717-2999">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="db717-2999">Az.Sql</span></span>
* <span data-ttu-id="db717-3000">支援資料庫的資料分類。</span><span class="sxs-lookup"><span data-stu-id="db717-3000">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="db717-3001">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="db717-3001">Az.Storage</span></span>
* <span data-ttu-id="db717-3002">報告以參數 -UseConnectedAccount 建立儲存體內容時的詳細錯誤 (未登入 Azure 帳戶)</span><span class="sxs-lookup"><span data-stu-id="db717-3002">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="db717-3003">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="db717-3003">New-AzStorageContext</span></span>
* <span data-ttu-id="db717-3004">支援以管理平面 API 管理指定儲存體帳戶的 Blob 服務屬性</span><span class="sxs-lookup"><span data-stu-id="db717-3004">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="db717-3005">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="db717-3005">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="db717-3006">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="db717-3006">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="db717-3007">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="db717-3007">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="db717-3008">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="db717-3008">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="db717-3009">Blob 的 -AsJob 支援和檔案上傳及下載 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-3009">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="db717-3010">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="db717-3010">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="db717-3011">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="db717-3011">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="db717-3012">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="db717-3012">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="db717-3013">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="db717-3013">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="db717-3014">1.6.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="db717-3014">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="db717-3015">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="db717-3015">Highlights since the last major release</span></span>
* <span data-ttu-id="db717-3016">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="db717-3016">General availability of `Az` module</span></span>
* <span data-ttu-id="db717-3017">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="db717-3017">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="db717-3018">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="db717-3018">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="db717-3019">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="db717-3019">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="db717-3020">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="db717-3020">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="db717-3021">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="db717-3021">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="db717-3022">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-3022">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="db717-3023">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="db717-3023">Az.Automation</span></span>
* <span data-ttu-id="db717-3024">Azure 自動化更新管理變更為支援下列各項新功能：</span><span class="sxs-lookup"><span data-stu-id="db717-3024">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="db717-3025">動態分組</span><span class="sxs-lookup"><span data-stu-id="db717-3025">Dynamic grouping</span></span>
    * <span data-ttu-id="db717-3026">預先貼文指令碼</span><span class="sxs-lookup"><span data-stu-id="db717-3026">Pre-Post script</span></span>
    * <span data-ttu-id="db717-3027">重新啟動設定</span><span class="sxs-lookup"><span data-stu-id="db717-3027">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="db717-3028">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="db717-3028">Az.Compute</span></span>
* <span data-ttu-id="db717-3029">修正 Get-AzVmBootDiagnosticsData 中路徑解析的問題</span><span class="sxs-lookup"><span data-stu-id="db717-3029">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="db717-3030">將計算用戶端程式庫更新為 25.0.0。</span><span class="sxs-lookup"><span data-stu-id="db717-3030">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="db717-3031">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="db717-3031">Az.KeyVault</span></span>
* <span data-ttu-id="db717-3032">新增了 KeyVault Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="db717-3032">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="db717-3033">Az.Network</span><span class="sxs-lookup"><span data-stu-id="db717-3033">Az.Network</span></span>
* <span data-ttu-id="db717-3034">新增適用於 Azure 防火牆的威脅智慧支援</span><span class="sxs-lookup"><span data-stu-id="db717-3034">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="db717-3035">新增應用程式閘道防火牆原則頂層資源和自訂規則</span><span class="sxs-lookup"><span data-stu-id="db717-3035">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="db717-3036">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="db717-3036">Az.RecoveryServices</span></span>
* <span data-ttu-id="db717-3037">已在 Azure VM 原則中新增了 SnapshotRetentionInDays 以支援 Instant RP</span><span class="sxs-lookup"><span data-stu-id="db717-3037">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="db717-3038">新增了取消註冊容器的管道支援</span><span class="sxs-lookup"><span data-stu-id="db717-3038">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="db717-3039">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="db717-3039">Az.Resources</span></span>
* <span data-ttu-id="db717-3040">更新適用於 Get-AzResource 和 Get-AzResourceGroup 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="db717-3040">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="db717-3041">更新在對 ARM 進行一般呼叫時使用的認證</span><span class="sxs-lookup"><span data-stu-id="db717-3041">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="db717-3042">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="db717-3042">Az.Sql</span></span>
* <span data-ttu-id="db717-3043">變更了 DetectionType 到 string[] 的威脅偵測 Cmdlet 參數，以便在新增了 DetectionTypes 時具備更進一步的保障，同時支援自動完成功能。</span><span class="sxs-lookup"><span data-stu-id="db717-3043">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="db717-3044">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="db717-3044">Az.Storage</span></span>
* <span data-ttu-id="db717-3045">支援儲存體帳戶上的 Get/Set/Remove 管理原則</span><span class="sxs-lookup"><span data-stu-id="db717-3045">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="db717-3046">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="db717-3046">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="db717-3047">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="db717-3047">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="db717-3048">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="db717-3048">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="db717-3049">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="db717-3049">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="db717-3050">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="db717-3050">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="db717-3051">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="db717-3051">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="db717-3052">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="db717-3052">Az.Websites</span></span>
* <span data-ttu-id="db717-3053">修正 ARM 範本錯誤 (bug)，防正使用 'New-AzWebApp -IncludeSourceWebAppSlots' 時發生中斷複製所有位置的情況</span><span class="sxs-lookup"><span data-stu-id="db717-3053">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="db717-3054">1.5.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="db717-3054">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="db717-3055">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="db717-3055">Az.Accounts</span></span>
* <span data-ttu-id="db717-3056">新增 'Register-AzModule' 命令以支援 AutoRest 產生的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-3056">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="db717-3057">適用於 Connect-AzAccount 的更新範例</span><span class="sxs-lookup"><span data-stu-id="db717-3057">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="db717-3058">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="db717-3058">Az.Automation</span></span>
* <span data-ttu-id="db717-3059">修正了在數個 Azure 自動化 Cmdlet 中擷取某些每月排程時發生的問題</span><span class="sxs-lookup"><span data-stu-id="db717-3059">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="db717-3060">修正 Get-AzAutomationDscNode 只會傳回前 20 個節點的問題。</span><span class="sxs-lookup"><span data-stu-id="db717-3060">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="db717-3061">現在可以傳回所有節點</span><span class="sxs-lookup"><span data-stu-id="db717-3061">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="db717-3062">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="db717-3062">Az.Cdn</span></span>
* <span data-ttu-id="db717-3063">新增了 Enable/Disable Custom Domain Https 的 Powershell Cmdlet 並取代了舊的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-3063">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="db717-3064">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="db717-3064">Az.Compute</span></span>
* <span data-ttu-id="db717-3065">新增 Get Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="db717-3065">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="db717-3066">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="db717-3066">Az.DataFactory</span></span>
* <span data-ttu-id="db717-3067">已將 ADF .Net SDK 版本更新為 3.0.1</span><span class="sxs-lookup"><span data-stu-id="db717-3067">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="db717-3068">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="db717-3068">Az.LogicApp</span></span>
* <span data-ttu-id="db717-3069">修正 ListWorkflows，僅擷取結果的第一頁資料</span><span class="sxs-lookup"><span data-stu-id="db717-3069">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="db717-3070">Az.Network</span><span class="sxs-lookup"><span data-stu-id="db717-3070">Az.Network</span></span>
* <span data-ttu-id="db717-3071">新增 Network Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="db717-3071">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="db717-3072">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="db717-3072">Az.RecoveryServices</span></span>
* <span data-ttu-id="db717-3073">新增了Azure VM 中 SQL 伺服器的支援</span><span class="sxs-lookup"><span data-stu-id="db717-3073">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="db717-3074">SDK 更新</span><span class="sxs-lookup"><span data-stu-id="db717-3074">SDK Update</span></span>
* <span data-ttu-id="db717-3075">移除了 Get-ProtectableItem 中的 VMappContainer 檢查</span><span class="sxs-lookup"><span data-stu-id="db717-3075">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="db717-3076">新增了 Get-ProtectableItem 的 Name 和 ServerName 參數</span><span class="sxs-lookup"><span data-stu-id="db717-3076">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="db717-3077">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="db717-3077">Az.Resources</span></span>
* <span data-ttu-id="db717-3078">將 `-TemplateObject` 參數新增至部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-3078">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="db717-3079">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="db717-3079">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="db717-3080">修正將 `Get-AzResource` 結果輸送至 `Set-AzResource` 的問題</span><span class="sxs-lookup"><span data-stu-id="db717-3080">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="db717-3081">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="db717-3081">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="db717-3082">修正在執行 `Set-AzResource` 時 JSON 資料類型變更的問題</span><span class="sxs-lookup"><span data-stu-id="db717-3082">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="db717-3083">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="db717-3083">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="db717-3084">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="db717-3084">Az.Sql</span></span>
* <span data-ttu-id="db717-3085">更新 AuditingEndpointsCommunicator。</span><span class="sxs-lookup"><span data-stu-id="db717-3085">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="db717-3086">修正在建立新診斷設定時邊緣案例的行為。</span><span class="sxs-lookup"><span data-stu-id="db717-3086">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="db717-3087">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="db717-3087">Az.Storage</span></span>
* <span data-ttu-id="db717-3088">在建立儲存體帳戶時支援 BlockBlobStorage 種類       - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="db717-3088">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="db717-3089">1.4.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="db717-3089">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="db717-3090">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="db717-3090">Az.AnalysisServices</span></span>
* <span data-ttu-id="db717-3091">即將淘汰 AddAzureASAccount Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-3091">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="db717-3092">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="db717-3092">Az.Automation</span></span>
* <span data-ttu-id="db717-3093">更新 Import-AzAutomationDscNodeConfiguration 的說明</span><span class="sxs-lookup"><span data-stu-id="db717-3093">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="db717-3094">已將設定名稱驗證新增至 Import-AzAutomationDscConfiguration Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-3094">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="db717-3095">已改善 Import-AzAutomationDscConfiguration Cmdlet 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="db717-3095">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="db717-3096">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="db717-3096">Az.CognitiveServices</span></span>
* <span data-ttu-id="db717-3097">已將 CustomSubdomainName 新增為 New-AzCognitiveServicesAccount 的新選擇性參數，用來指定資源的子網域。</span><span class="sxs-lookup"><span data-stu-id="db717-3097">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="db717-3098">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="db717-3098">Az.Compute</span></span>
* <span data-ttu-id="db717-3099">修正識別碼參數集問題</span><span class="sxs-lookup"><span data-stu-id="db717-3099">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="db717-3100">如果未提供 Name 參數，更新 Get-AzVMExtension 以列出所有已安裝的延伸模組</span><span class="sxs-lookup"><span data-stu-id="db717-3100">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="db717-3101">將標記和 ResourceId 參數新增至 Update-AzImage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-3101">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="db717-3102">沒有執行個體識別碼的 Get-AzVmssVM，和具有 InstanceView 者可以透過執行個體檢視列出 VMSS VM。</span><span class="sxs-lookup"><span data-stu-id="db717-3102">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="db717-3103">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="db717-3103">Az.DataLakeStore</span></span>
* <span data-ttu-id="db717-3104">為 ADL 刪除的項目列舉和還原新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-3104">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="db717-3105">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="db717-3105">Az.EventHub</span></span>
* <span data-ttu-id="db717-3106">在 Eventhub 的 CaptureDescription 類別中，已將新的布林值屬性 SkipEmptyArchives 新增至 Skip Empty Archives</span><span class="sxs-lookup"><span data-stu-id="db717-3106">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="db717-3107">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="db717-3107">Az.KeyVault</span></span>
* <span data-ttu-id="db717-3108">修正 Set-AzKeyVaultSecret 的標記</span><span class="sxs-lookup"><span data-stu-id="db717-3108">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="db717-3109">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="db717-3109">Az.LogicApp</span></span>
* <span data-ttu-id="db717-3110">在整合帳戶的基本 sku 新增</span><span class="sxs-lookup"><span data-stu-id="db717-3110">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="db717-3111">在 XSLT 2.0、XSLT 3.0 和 Liquid 對應類型中新增</span><span class="sxs-lookup"><span data-stu-id="db717-3111">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="db717-3112">整合帳戶組件的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-3112">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="db717-3113">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="db717-3113">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="db717-3114">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="db717-3114">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="db717-3115">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="db717-3115">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="db717-3116">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="db717-3116">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="db717-3117">整合帳戶批次設定的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-3117">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="db717-3118">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="db717-3118">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="db717-3119">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="db717-3119">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="db717-3120">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="db717-3120">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="db717-3121">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="db717-3121">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="db717-3122">將邏輯應用程式 SDK 更新至 4.1.0 版</span><span class="sxs-lookup"><span data-stu-id="db717-3122">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="db717-3123">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="db717-3123">Az.Monitor</span></span>
* <span data-ttu-id="db717-3124">更新 Get-AzMetric 的說明</span><span class="sxs-lookup"><span data-stu-id="db717-3124">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="db717-3125">Az.Network</span><span class="sxs-lookup"><span data-stu-id="db717-3125">Az.Network</span></span>
* <span data-ttu-id="db717-3126">更新 Add-AzApplicationGatewayCustomError 的說明範例</span><span class="sxs-lookup"><span data-stu-id="db717-3126">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="db717-3127">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="db717-3127">Az.OperationalInsights</span></span>
* <span data-ttu-id="db717-3128">取得 ApplicationInsights 與新資料來源的其他支援。</span><span class="sxs-lookup"><span data-stu-id="db717-3128">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="db717-3129">已新增新 'ApplicationInsights' 類型，以支援指定工作區的取得特定和取得所有 ApplicationInsights 資料來源。</span><span class="sxs-lookup"><span data-stu-id="db717-3129">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="db717-3130">已新增 New-AzOperationalInsightsApplicationInsightsDataSource Cmdlet 用來建立資料來源，透過指定的 Application-Insights 資源參數：訂用帳戶識別碼、resourceGroupName 和名稱。</span><span class="sxs-lookup"><span data-stu-id="db717-3130">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="db717-3131">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="db717-3131">Az.Resources</span></span>
* <span data-ttu-id="db717-3132">修正 https://github.com/Azure/azure-powershell/issues/8166 的問題</span><span class="sxs-lookup"><span data-stu-id="db717-3132">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="db717-3133">修正 https://github.com/Azure/azure-powershell/issues/8235 的問題</span><span class="sxs-lookup"><span data-stu-id="db717-3133">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="db717-3134">修正 https://github.com/Azure/azure-powershell/issues/6219 的問題</span><span class="sxs-lookup"><span data-stu-id="db717-3134">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="db717-3135">修正防止重複建立 KeyCredentials 的錯誤</span><span class="sxs-lookup"><span data-stu-id="db717-3135">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="db717-3136">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="db717-3136">Az.Sql</span></span>
* <span data-ttu-id="db717-3137">新增 SQL DB 超大規模層支援</span><span class="sxs-lookup"><span data-stu-id="db717-3137">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="db717-3138">已修正以下錯誤：由於在還原要求中設定非必要屬性造成還原失敗</span><span class="sxs-lookup"><span data-stu-id="db717-3138">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="db717-3139">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="db717-3139">Az.Websites</span></span>
* <span data-ttu-id="db717-3140">Get-AzWebAppSlotMetrics 中的正確範例</span><span class="sxs-lookup"><span data-stu-id="db717-3140">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="db717-3141">1.3.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="db717-3141">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="db717-3142">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="db717-3142">Az.Accounts</span></span>
* <span data-ttu-id="db717-3143">更新至最新版本的 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="db717-3143">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="db717-3144">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="db717-3144">Az.AnalysisServices</span></span>
<span data-ttu-id="db717-3145">Az.AnalysisServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="db717-3145">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="db717-3146">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="db717-3146">Az.Compute</span></span>
* <span data-ttu-id="db717-3147">AEM 延伸模組：新增對 UltraSSD 和 P60、P70 和 P80 磁碟的支援</span><span class="sxs-lookup"><span data-stu-id="db717-3147">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="db717-3148">更新 AzVMBootDiagnostics 的說明描述</span><span class="sxs-lookup"><span data-stu-id="db717-3148">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="db717-3149">更新 Update-AzImage 的說明描述和範例</span><span class="sxs-lookup"><span data-stu-id="db717-3149">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="db717-3150">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="db717-3150">Az.RecoveryServices</span></span>
<span data-ttu-id="db717-3151">Az.RecoveryServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="db717-3151">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="db717-3152">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="db717-3152">Az.Resources</span></span>
* <span data-ttu-id="db717-3153">修正資源群組標記</span><span class="sxs-lookup"><span data-stu-id="db717-3153">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="db717-3154">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="db717-3154">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="db717-3155">修正 `Get-AzureRmRoleAssignment`不遵守 -ErrorAction 的問題</span><span class="sxs-lookup"><span data-stu-id="db717-3155">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="db717-3156">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="db717-3156">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="db717-3157">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="db717-3157">Az.Sql</span></span>
* <span data-ttu-id="db717-3158">新增 Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="db717-3158">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="db717-3159">修正執行 SQL Cmdlet 時無法登入 Azure 帳戶會導致 nullref 例外狀況的問題</span><span class="sxs-lookup"><span data-stu-id="db717-3159">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="db717-3160">已修正 Get AzSqlCapability 中的 Null 參考例外狀況</span><span class="sxs-lookup"><span data-stu-id="db717-3160">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="db717-3161">1.2.1 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="db717-3161">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="db717-3162">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="db717-3162">Az.Accounts</span></span>
* <span data-ttu-id="db717-3163">包含正確驗證版本的發行</span><span class="sxs-lookup"><span data-stu-id="db717-3163">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="db717-3164">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="db717-3164">Az.AnalysisServices</span></span>
* <span data-ttu-id="db717-3165">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="db717-3165">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="db717-3166">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="db717-3166">Az.RecoveryServices</span></span>
* <span data-ttu-id="db717-3167">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="db717-3167">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="db717-3168">1.2.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="db717-3168">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="db717-3169">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="db717-3169">Az.Accounts</span></span>
* <span data-ttu-id="db717-3170">僅新增 Windows PowerShell 5.1 互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="db717-3170">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="db717-3171">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="db717-3171">Update incorrect online help URLs</span></span>
* <span data-ttu-id="db717-3172">在 PS Core 中新增 Uninstall-AzureRm 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="db717-3172">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="db717-3173">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="db717-3173">Az.Aks</span></span>
* <span data-ttu-id="db717-3174">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="db717-3174">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="db717-3175">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="db717-3175">Az.Automation</span></span>
* <span data-ttu-id="db717-3176">已新增 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="db717-3176">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="db717-3177">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="db717-3177">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="db717-3178">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="db717-3178">Az.Cdn</span></span>
* <span data-ttu-id="db717-3179">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="db717-3179">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="db717-3180">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="db717-3180">Az.Compute</span></span>
* <span data-ttu-id="db717-3181">新增 Invoke-AzVMReimage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-3181">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="db717-3182">將 TempDisk 參數新增至 Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="db717-3182">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="db717-3183">修正 New-AzVM 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="db717-3183">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="db717-3184">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="db717-3184">Az.ContainerRegistry</span></span>
* <span data-ttu-id="db717-3185">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="db717-3185">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="db717-3186">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="db717-3186">Az.DataFactory</span></span>
* <span data-ttu-id="db717-3187">已將 ADF .Net SDK 版本更新為 3.0.0</span><span class="sxs-lookup"><span data-stu-id="db717-3187">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="db717-3188">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="db717-3188">Az.DataLakeStore</span></span>
* <span data-ttu-id="db717-3189">修正使用 MSI 時 ADLS 端點的問題</span><span class="sxs-lookup"><span data-stu-id="db717-3189">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="db717-3190">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="db717-3190">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="db717-3191">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="db717-3191">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="db717-3192">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="db717-3192">Az.IotHub</span></span>
* <span data-ttu-id="db717-3193">將編碼格式新增至 Add-IotHubRoutingEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db717-3193">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="db717-3194">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="db717-3194">Az.KeyVault</span></span>
* <span data-ttu-id="db717-3195">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="db717-3195">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="db717-3196">Az.Network</span><span class="sxs-lookup"><span data-stu-id="db717-3196">Az.Network</span></span>
* <span data-ttu-id="db717-3197">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="db717-3197">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="db717-3198">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="db717-3198">Az.Resources</span></span>
* <span data-ttu-id="db717-3199">修正 「New-AzADAppCredential」和「New-AzADSpCredential」參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="db717-3199">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="db717-3200">修正「-TemplateFile」參數路徑並未在執行資源群組部署 Cmdlet 前解析的問題</span><span class="sxs-lookup"><span data-stu-id="db717-3200">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="db717-3201">Az.Resources：正確的 New-AzureRmPolicyDefinition -Mode 預設值文件</span><span class="sxs-lookup"><span data-stu-id="db717-3201">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="db717-3202">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/7522 的問題</span><span class="sxs-lookup"><span data-stu-id="db717-3202">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="db717-3203">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/5747 的問題</span><span class="sxs-lookup"><span data-stu-id="db717-3203">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="db717-3204">修正「PSResourceGroupDeployment」物件格式化的問題</span><span class="sxs-lookup"><span data-stu-id="db717-3204">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="db717-3205">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="db717-3205">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="db717-3206">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="db717-3206">Az.ServiceFabric</span></span>
* <span data-ttu-id="db717-3207">將憑證新增到 VMSS 模型但擲回例外狀況時復原，以修正錯誤： https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="db717-3207">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="db717-3208">修正某些錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="db717-3208">Fix some error messages.</span></span>
* <span data-ttu-id="db717-3209">修正使用預設 ARM 範本為並未移轉至 Az 的 New-AzServiceFabriCluster 建立叢集的問題。</span><span class="sxs-lookup"><span data-stu-id="db717-3209">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="db717-3210">檢查延伸模組中的叢集識別碼，修正只將叢集/應用程式憑證新增至對應至該叢集的 VM 擴展集中的問題。</span><span class="sxs-lookup"><span data-stu-id="db717-3210">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="db717-3211">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="db717-3211">Az.SignalR</span></span>
* <span data-ttu-id="db717-3212">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="db717-3212">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="db717-3213">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="db717-3213">Az.Sql</span></span>
* <span data-ttu-id="db717-3214">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="db717-3214">Update incorrect online help URLs</span></span>
* <span data-ttu-id="db717-3215">更新了 LicenseType 參數的描述並新增了可能的值</span><span class="sxs-lookup"><span data-stu-id="db717-3215">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="db717-3216">修正當更新受控執行個體身分識別僅為已更新屬性時無法運作的問題</span><span class="sxs-lookup"><span data-stu-id="db717-3216">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="db717-3217">支援在受控執行個體上的自訂定序</span><span class="sxs-lookup"><span data-stu-id="db717-3217">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="db717-3218">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="db717-3218">Az.Storage</span></span>
* <span data-ttu-id="db717-3219">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="db717-3219">Update incorrect online help URLs</span></span>
* <span data-ttu-id="db717-3220">在進階儲存體帳戶上取得/設定傳統記錄/計量時提供詳細錯誤訊息，因為進階儲存體帳戶不支援傳統記錄/計量。</span><span class="sxs-lookup"><span data-stu-id="db717-3220">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="db717-3221">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="db717-3221">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="db717-3222">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="db717-3222">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="db717-3223">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="db717-3223">Az.TrafficManager</span></span>
* <span data-ttu-id="db717-3224">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="db717-3224">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="db717-3225">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="db717-3225">Az.Websites</span></span>
* <span data-ttu-id="db717-3226">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="db717-3226">Update incorrect online help URLs</span></span>
* <span data-ttu-id="db717-3227">修正「New-AzWebAppSSLBinding」，以便在應用程式於 ASE 上託管時將憑證上傳到正確的資源群組及位置。</span><span class="sxs-lookup"><span data-stu-id="db717-3227">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="db717-3228">修正「New-AzWebAppSSLBinding」以便在將 SSL 憑證繫結至應用程式時不要覆寫標記</span><span class="sxs-lookup"><span data-stu-id="db717-3228">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="db717-3229">1.1.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="db717-3229">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="db717-3230">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="db717-3230">Az.Accounts</span></span>
* <span data-ttu-id="db717-3231">將 'Local' 範圍新增至 Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="db717-3231">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="db717-3232">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="db717-3232">Az.Compute</span></span>
* <span data-ttu-id="db717-3233">在 Restart/Start/Stop/Remove/Set-AzVM 和 Save-AzVMImage 的識別碼參數集中，名稱現在為選用項目</span><span class="sxs-lookup"><span data-stu-id="db717-3233">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="db717-3234">已更新說明檔案中的識別碼描述</span><span class="sxs-lookup"><span data-stu-id="db717-3234">Updated the description of ID in help files</span></span>
* <span data-ttu-id="db717-3235">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="db717-3235">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="db717-3236">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="db717-3236">Az.DataLakeStore</span></span>
* <span data-ttu-id="db717-3237">將資料平面的 SDK 版本更新為 1.1.14，以修正 SDK 問題。</span><span class="sxs-lookup"><span data-stu-id="db717-3237">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="db717-3238">針對 getfilestatus 和 liststatus 修正 acesstime 和 modificationtime 的負值處理、修正非同步取消權杖</span><span class="sxs-lookup"><span data-stu-id="db717-3238">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="db717-3239">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="db717-3239">Az.EventGrid</span></span>
* <span data-ttu-id="db717-3240">已更新為使用 2019-01-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="db717-3240">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="db717-3241">更新下列 Cmdlet 來支援 2019-01-01 API 版本中的新案例</span><span class="sxs-lookup"><span data-stu-id="db717-3241">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="db717-3242">New-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="db717-3242">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="db717-3243">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="db717-3243">Event Time-To-Live,</span></span>
        - <span data-ttu-id="db717-3244">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="db717-3244">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="db717-3245">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="db717-3245">Dead letter endpoint.</span></span>
    - <span data-ttu-id="db717-3246">Update-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="db717-3246">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="db717-3247">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="db717-3247">Event Time-To-Live,</span></span>
        - <span data-ttu-id="db717-3248">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="db717-3248">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="db717-3249">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="db717-3249">Dead letter endpoint.</span></span>
* <span data-ttu-id="db717-3250">針對 New-AzureRmEventGridSubscription 和 Update-AzureRmEventGridSubscription Cmdlet 中的 EndpointType 選項新增列舉值 (namely、storageQueue 和 hybridConnection)。</span><span class="sxs-lookup"><span data-stu-id="db717-3250">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="db717-3251">如果預期需要使用者手動建立或更新事件訂閱，則顯示警告訊息。</span><span class="sxs-lookup"><span data-stu-id="db717-3251">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="db717-3252">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="db717-3252">Az.IotHub</span></span>
* <span data-ttu-id="db717-3253">已更新至最新版本的 IotHub SDK</span><span class="sxs-lookup"><span data-stu-id="db717-3253">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="db717-3254">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="db717-3254">Az.LogicApp</span></span>
* <span data-ttu-id="db717-3255">Get-AzLogicApp 會列出所有項目，無須指定名稱</span><span class="sxs-lookup"><span data-stu-id="db717-3255">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="db717-3256">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="db717-3256">Az.Resources</span></span>
* <span data-ttu-id="db717-3257">修正為 'Get-AzResource' 提供 '-ODataQuery' 和 '-ResourceId' 參數時的參數集問題</span><span class="sxs-lookup"><span data-stu-id="db717-3257">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="db717-3258">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="db717-3258">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="db717-3259">修正 New/Set-AzPolicyDefinition 中的 -Custom 參數處理</span><span class="sxs-lookup"><span data-stu-id="db717-3259">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="db717-3260">修正 New-AzDeployment 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="db717-3260">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="db717-3261">使 '-MailNickname' 參數成為 'New-AzADUser' 的必要項目</span><span class="sxs-lookup"><span data-stu-id="db717-3261">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="db717-3262">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="db717-3262">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="db717-3263">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="db717-3263">Az.SignalR</span></span>
* <span data-ttu-id="db717-3264">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="db717-3264">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="db717-3265">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="db717-3265">Az.Sql</span></span>
* <span data-ttu-id="db717-3266">將儲存體管理用戶端相依性轉換為一般的 SDK 實作。</span><span class="sxs-lookup"><span data-stu-id="db717-3266">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="db717-3267">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="db717-3267">Az.Storage</span></span>
* <span data-ttu-id="db717-3268">使用 Sas 權杖、OAuth 或匿名來建立儲存體內容的 StorageAccountName 時，將其設定為實際的儲存體帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="db717-3268">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="db717-3269">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="db717-3269">New-AzStorageContext</span></span>
* <span data-ttu-id="db717-3270">使用 '-FullUri' 參數建立 Blob 快照集物件的 Sas 權杖、將傳回的 Uri 修正為快照集 Uri</span><span class="sxs-lookup"><span data-stu-id="db717-3270">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="db717-3271">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="db717-3271">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="db717-3272">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="db717-3272">Az.Websites</span></span>
* <span data-ttu-id="db717-3273">修正 'Get-AzDeletedWebApp' 中的日期剖析錯誤</span><span class="sxs-lookup"><span data-stu-id="db717-3273">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="db717-3274">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="db717-3274">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="db717-3275">1.0.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="db717-3275">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="db717-3276">一般</span><span class="sxs-lookup"><span data-stu-id="db717-3276">General</span></span>

- <span data-ttu-id="db717-3277">Az 模組正式運作</span><span class="sxs-lookup"><span data-stu-id="db717-3277">General Availability of Az Module</span></span>
- <span data-ttu-id="db717-3278">每個模組的線上說明</span><span class="sxs-lookup"><span data-stu-id="db717-3278">Online help for each module</span></span>
- <span data-ttu-id="db717-3279">如需詳細資訊和藍圖，請參閱 [Az 公告頁面](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="db717-3279">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="db717-3280">如需從 AzureRM 遷移的相關資訊，請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="db717-3280">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="db717-3281">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="db717-3281">Az.Accounts</span></span>
- <span data-ttu-id="db717-3282">已從 Az.Profile 變更</span><span class="sxs-lookup"><span data-stu-id="db717-3282">Changed from Az.Profile</span></span>
- <span data-ttu-id="db717-3283">設定檔和內容類型有固定的資料表格式</span><span class="sxs-lookup"><span data-stu-id="db717-3283">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="db717-3284">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="db717-3284">Az.ApiManagement</span></span>
- <span data-ttu-id="db717-3285">#7002 的修正</span><span class="sxs-lookup"><span data-stu-id="db717-3285">Fixes for #7002</span></span>
- <span data-ttu-id="db717-3286">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="db717-3286">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="db717-3287">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="db717-3287">Az.Batch</span></span>
- <span data-ttu-id="db717-3288">已新增功能，可透過 `PSComputeNode` 上新的 `NodeAgentInformation` 屬性，查看集區中每個 VM 上所執行的 Azure Batch 節點代理程式是哪個版本。</span><span class="sxs-lookup"><span data-stu-id="db717-3288">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="db717-3289">`PSDataDisk` 的 `Caching` 預設值現在為 `ReadWrite` 而非 `None`。</span><span class="sxs-lookup"><span data-stu-id="db717-3289">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="db717-3290">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="db717-3290">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="db717-3291">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="db717-3291">Az.Billing</span></span>
- <span data-ttu-id="db717-3292">結合 Billing、Consumption 和 UsageAggregates Cmdlet，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="db717-3292">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="db717-3293">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="db717-3293">Az.CognitivServices</span></span>
- <span data-ttu-id="db717-3294">針對 New-AzureRmCognitiveServicesAccount 作業上可用的 SkuName 和 Typem 新增完成器</span><span class="sxs-lookup"><span data-stu-id="db717-3294">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="db717-3295">已從 Get-AzCognitiveServicesAccountSkus 移除 GetSkusWithAccountParamSetName 參數集</span><span class="sxs-lookup"><span data-stu-id="db717-3295">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="db717-3296">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="db717-3296">Az.ContainerInstance</span></span>
- <span data-ttu-id="db717-3297">已新增 ManagedIdentity 支援</span><span class="sxs-lookup"><span data-stu-id="db717-3297">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="db717-3298">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="db717-3298">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="db717-3299">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="db717-3299">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="db717-3300">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="db717-3300">Az.DataLakeStore</span></span>
- <span data-ttu-id="db717-3301">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="db717-3301">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="db717-3302">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="db717-3302">Az.Monitor</span></span>
- <span data-ttu-id="db717-3303">Az.Insights 已重新命名為 Az.Monitor，並有次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="db717-3303">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="db717-3304">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="db717-3304">Az.KeyVault</span></span>
- <span data-ttu-id="db717-3305">已從輸出類型中移除淘汰的 'PurgeDisabled' 屬性</span><span class="sxs-lookup"><span data-stu-id="db717-3305">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="db717-3306">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="db717-3306">Az.MachineLearning</span></span>
- <span data-ttu-id="db717-3307">已納入來自 Az.MachineLearningCompute 模組的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-3307">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="db717-3308">Az.Media</span><span class="sxs-lookup"><span data-stu-id="db717-3308">Az.Media</span></span>
- <span data-ttu-id="db717-3309">從 New-AzMediaService 移除淘汰的 -Tags 別名</span><span class="sxs-lookup"><span data-stu-id="db717-3309">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="db717-3310">Az.Network</span><span class="sxs-lookup"><span data-stu-id="db717-3310">Az.Network</span></span>
<span data-ttu-id="db717-3311">已新增在應用程式閘道中設定 RewriteRuleSets 的支援</span><span class="sxs-lookup"><span data-stu-id="db717-3311">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="db717-3312">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="db717-3312">New cmdlets added:</span></span>
        - <span data-ttu-id="db717-3313">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="db717-3313">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="db717-3314">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="db717-3314">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="db717-3315">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="db717-3315">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="db717-3316">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="db717-3316">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="db717-3317">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="db717-3317">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="db717-3318">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="db717-3318">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="db717-3319">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="db717-3319">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="db717-3320">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="db717-3320">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="db717-3321">Cmdlets updated with optional parameter -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="db717-3321">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="db717-3322">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="db717-3322">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="db717-3323">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="db717-3323">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="db717-3324">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="db717-3324">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="db717-3325">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="db717-3325">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="db717-3326">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="db717-3326">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="db717-3327">New-AzureRmApplicationGatewayUrlPathMapConfig 已使用身分識別對應用程式閘道新增 KeyVault 支援。</span><span class="sxs-lookup"><span data-stu-id="db717-3327">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="db717-3328">已使用選擇性參數 -KeyVaultSecretId, -KeyVaultSecret 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-3328">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="db717-3329">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="db717-3329">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="db717-3330">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="db717-3330">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="db717-3331">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="db717-3331">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="db717-3332">已使用選擇性參數 -UserAssignedIdentity 更新了 New-AzApplicationGateway Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-3332">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="db717-3333">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="db717-3333">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="db717-3334">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="db717-3334">Az.OperationalInsights</span></span>
- <span data-ttu-id="db717-3335">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="db717-3335">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="db717-3336">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="db717-3336">Az.Profile</span></span>
- <span data-ttu-id="db717-3337">模組名稱已變更為 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="db717-3337">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="db717-3338">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="db717-3338">Az.RecoveryServices</span></span>
- <span data-ttu-id="db717-3339">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="db717-3339">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="db717-3340">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="db717-3340">Az.Resources</span></span>
- <span data-ttu-id="db717-3341">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="db717-3341">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="db717-3342">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="db717-3342">Az.ServiceFabric</span></span>
- <span data-ttu-id="db717-3343">支援依通用名稱和指紋來指定憑證</span><span class="sxs-lookup"><span data-stu-id="db717-3343">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="db717-3344">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="db717-3344">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="db717-3345">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="db717-3345">Az.SIgnalR</span></span>
- <span data-ttu-id="db717-3346">SIgnalR 的 PowerShell Cmdlet 正式運作</span><span class="sxs-lookup"><span data-stu-id="db717-3346">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="db717-3347">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="db717-3347">Az.Sql</span></span>
- <span data-ttu-id="db717-3348">已對威脅偵測的 Cmdlet 新增 Data_Exfiltration 和 Unsafe_Action 偵測類型</span><span class="sxs-lookup"><span data-stu-id="db717-3348">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="db717-3349">已更新 SQL 稽核 Cmdlet 的文件範例</span><span class="sxs-lookup"><span data-stu-id="db717-3349">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="db717-3350">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="db717-3350">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="db717-3351">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="db717-3351">Az.Storage</span></span>
- <span data-ttu-id="db717-3352">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="db717-3352">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="db717-3353">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="db717-3353">Az.Websites</span></span>
- <span data-ttu-id="db717-3354">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="db717-3354">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="db717-3355">0.7.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="db717-3355">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="db717-3356">一般</span><span class="sxs-lookup"><span data-stu-id="db717-3356">General</span></span>

* <span data-ttu-id="db717-3357">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="db717-3357">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="db717-3358">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="db717-3358">Az.Compute</span></span>

* <span data-ttu-id="db717-3359">針對 `New-AzVm(ss)` Cmdlet 簡單參數集內的 UltraSSD 和資源庫映像新增支援。</span><span class="sxs-lookup"><span data-stu-id="db717-3359">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="db717-3360">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="db717-3360">Az.DataLakeStore</span></span>

* <span data-ttu-id="db717-3361">修正 adls 帳戶網域的尾端斜線</span><span class="sxs-lookup"><span data-stu-id="db717-3361">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="db717-3362">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="db717-3362">Az.FrontDoor</span></span>

* <span data-ttu-id="db717-3363">已修正一些中斷的連結</span><span class="sxs-lookup"><span data-stu-id="db717-3363">Fixed some broken links</span></span>
    - <span data-ttu-id="db717-3364">在 New-AzureRmFrontDoor 和 Set-AzureRmFrontDoor 文章中，已修正 New-AzureRmFrontDoorHealthProbeSettingObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="db717-3364">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="db717-3365">在 New-AzureRmFrontDoorManagedRuleObject 文章中，已修正 New-AzureRmFrontDoorRuleGroupOverrideObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="db717-3365">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="db717-3366">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="db717-3366">Az.RecoveryServices</span></span>

* <span data-ttu-id="db717-3367">已針對 Azure 檔案共用的還原作業新增用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="db717-3367">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="db717-3368">已將 storageAccountName 和 storageAccountResourceGroupName 設為 afs 還原作業的選擇性項目。</span><span class="sxs-lookup"><span data-stu-id="db717-3368">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="db717-3369">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="db717-3369">Az.Resources</span></span>

* <span data-ttu-id="db717-3370">修正 https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="db717-3370">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="db717-3371">將 Get-AzureRmRoleAssignment 更新為使用訂用帳戶範圍 (如果有在要求傳統管理員時提供的話)。</span><span class="sxs-lookup"><span data-stu-id="db717-3371">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="db717-3372">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="db717-3372">Az.Sql</span></span>

* <span data-ttu-id="db717-3373">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="db717-3373">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="db717-3374">已修正搭配使用 Get-AzureRmSqlDatabaseVulnerabilityAssessment 和 DotNet core 時所會發生的問題</span><span class="sxs-lookup"><span data-stu-id="db717-3374">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="db717-3375">已修改 SQL 稽核 Cmdlet 相關說明訊息的文件。</span><span class="sxs-lookup"><span data-stu-id="db717-3375">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="db717-3376">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="db717-3376">Az.Storage</span></span>

* <span data-ttu-id="db717-3377">對 New-AzureRmStorageAccount 新增 -EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="db717-3377">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="db717-3378">已修正下列問題：如果沒有輸入 -DestContext，複製檔案 Cmdlet 無法重複使用目的地中的來源內容</span><span class="sxs-lookup"><span data-stu-id="db717-3378">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="db717-3379">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="db717-3379">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="db717-3380">支援靜態網站設定</span><span class="sxs-lookup"><span data-stu-id="db717-3380">Support Static Website configuration</span></span>
    - <span data-ttu-id="db717-3381">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="db717-3381">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="db717-3382">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="db717-3382">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="db717-3383">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="db717-3383">Az.Websites</span></span>

* <span data-ttu-id="db717-3384">Set-AzureRmWebApp 和 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="db717-3384">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="db717-3385">已新增新的參數 (-AzureStoragePath)，指定要將 Azure 儲存體路徑掛接至 Windows 和 Linux 容器應用程式中。</span><span class="sxs-lookup"><span data-stu-id="db717-3385">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="db717-3386">使用新 Cmdlet New-AzureRmWebAppAzureStoragePath 的輸出作為參數來設定 Azure 儲存體路徑。</span><span class="sxs-lookup"><span data-stu-id="db717-3386">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="db717-3387">0.6.1 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="db717-3387">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="db717-3388">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="db717-3388">Az.ApiManagement</span></span>
* <span data-ttu-id="db717-3389">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="db717-3389">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="db717-3390">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="db717-3390">Az.Automation</span></span>
* <span data-ttu-id="db717-3391">以 Swagger 為基礎的 Azure 自動化 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-3391">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="db717-3392">已新增更新管理 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-3392">Added Update Management cmdlets</span></span>
* <span data-ttu-id="db717-3393">已新增原始檔控制 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-3393">Added Source Control cmdlets</span></span>
* <span data-ttu-id="db717-3394">已新增 Remove-AzureRmAutomationHybridWorkerGroup Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-3394">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="db717-3395">已修正 DSC 註冊節點命令</span><span class="sxs-lookup"><span data-stu-id="db717-3395">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="db717-3396">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="db717-3396">Az.Compute</span></span>
* <span data-ttu-id="db717-3397">已修正 SystemAssigned 身分識別的身份識別問題</span><span class="sxs-lookup"><span data-stu-id="db717-3397">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="db717-3398">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="db717-3398">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="db717-3399">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="db717-3399">Az.ContainerInstance</span></span>
* <span data-ttu-id="db717-3400">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="db717-3400">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="db717-3401">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="db717-3401">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="db717-3402">更新市集 Cmdlet 的範例描述</span><span class="sxs-lookup"><span data-stu-id="db717-3402">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="db717-3403">Az.Network</span><span class="sxs-lookup"><span data-stu-id="db717-3403">Az.Network</span></span>
* <span data-ttu-id="db717-3404">已新增 Cmdlet：New-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayCustomError、Get-AzureRmApplicationGatewayCustomError、Set-AzureRmApplicationGatewayCustomError、Remove-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayHttpListenerCustomError、Get-AzureRmApplicationGatewayHttpListenerCustomError、Set-AzureRmApplicationGatewayHttpListenerCustomError、Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="db717-3404">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="db717-3405">已將 ICMP 加回支援的 AzureFirewall 網路通訊協定</span><span class="sxs-lookup"><span data-stu-id="db717-3405">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="db717-3406">更新 Test-AzureRmNetworkWatcherConnectivity Cmdlet，在目的地識別碼、位址和連接埠上新增驗證。</span><span class="sxs-lookup"><span data-stu-id="db717-3406">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="db717-3407">修正 VirtualNetwork 對應中的記憶體使用量問題</span><span class="sxs-lookup"><span data-stu-id="db717-3407">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="db717-3408">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="db717-3408">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="db717-3409">提供修正程式以修改受保護的檔案共用原則。</span><span class="sxs-lookup"><span data-stu-id="db717-3409">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="db717-3410">已將原則時區轉換為大寫。</span><span class="sxs-lookup"><span data-stu-id="db717-3410">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="db717-3411">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="db717-3411">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="db717-3412">已修正 New-AzureRmRecoveryServicesAsrProtectableItem 中的範例</span><span class="sxs-lookup"><span data-stu-id="db717-3412">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="db717-3413">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="db717-3413">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="db717-3414">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="db717-3414">Az.Relay</span></span>
* <span data-ttu-id="db717-3415">已將選擇性參數 -KeyValue 新增至 New-AzureRmRelayKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="db717-3415">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="db717-3416">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="db717-3416">Az.Resources</span></span>
* <span data-ttu-id="db717-3417">更新 `New-AzureRmPolicyAssignment` 和 `Set-AzureRmPolicyAssignment` 中資源身分識別相關參數的說明文件</span><span class="sxs-lookup"><span data-stu-id="db717-3417">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="db717-3418">新增使用 -Metadata 的 New-AzureRmPolicyDefinition 範例</span><span class="sxs-lookup"><span data-stu-id="db717-3418">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="db717-3419">修正：允許在 NetStandard: #7678 #7703 的標籤索引鍵中保留大小寫</span><span class="sxs-lookup"><span data-stu-id="db717-3419">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="db717-3420">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="db717-3420">Az.ServiceFabric</span></span>
* <span data-ttu-id="db717-3421">針對即將推出的重大變更新增取代資訊</span><span class="sxs-lookup"><span data-stu-id="db717-3421">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="db717-3422">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="db717-3422">Az.Sql</span></span>
* <span data-ttu-id="db717-3423">已在 Azure SQL Database 受控執行個體和 Azure SQL 受控資料庫上新增 CRUD 作業的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-3423">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="db717-3424">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="db717-3424">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="db717-3425">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="db717-3425">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="db717-3426">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="db717-3426">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="db717-3427">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="db717-3427">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="db717-3428">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="db717-3428">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="db717-3429">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="db717-3429">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="db717-3430">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="db717-3430">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="db717-3431">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="db717-3431">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="db717-3432">已在伺服器或資料庫上啟用擴充的稽核原則管理。</span><span class="sxs-lookup"><span data-stu-id="db717-3432">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="db717-3433">已新增參數 (PredicateExpression) 以啟用稽核記錄的篩選。</span><span class="sxs-lookup"><span data-stu-id="db717-3433">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="db717-3434">已將 Cmdlet 修改為使用 SQL 用戶端，而不是傳統用戶端。</span><span class="sxs-lookup"><span data-stu-id="db717-3434">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="db717-3435">Set-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="db717-3435">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="db717-3436">Get-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="db717-3436">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="db717-3437">Set-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="db717-3437">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="db717-3438">Get-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="db717-3438">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="db717-3439">已修正使用 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings 和儲存體帳戶名稱參數集的問題</span><span class="sxs-lookup"><span data-stu-id="db717-3439">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="db717-3440">0.5.0 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="db717-3440">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="db717-3441">一般</span><span class="sxs-lookup"><span data-stu-id="db717-3441">General</span></span>
* <span data-ttu-id="db717-3442">已在許多核心 Cmdlet 新增資源完成器 - 這些 Cmdlet 可讓您在以互動方式叫用 Cmdlet 時，使用 TAB 鍵瀏覽現有資源名稱</span><span class="sxs-lookup"><span data-stu-id="db717-3442">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="db717-3443">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="db717-3443">Az.Profile</span></span>
* <span data-ttu-id="db717-3444">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="db717-3444">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="db717-3445">將 Cmdlet Connect-AzAccount 中的參數 TenantId 重新命名為 Tenant 並新增 TenantId 的別名</span><span class="sxs-lookup"><span data-stu-id="db717-3445">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="db717-3446">更新 Connect-AzAccount 的 TenantId 說明</span><span class="sxs-lookup"><span data-stu-id="db717-3446">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="db717-3447">修正提供租用戶網域時登入失敗的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="db717-3447">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="db717-3448">修正租用戶中無訂用帳戶之帳戶內容衝突的問題</span><span class="sxs-lookup"><span data-stu-id="db717-3448">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="db717-3449">修正使用 MSI 時 DataLake 端點的問題</span><span class="sxs-lookup"><span data-stu-id="db717-3449">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="db717-3450">修正若未連線，'Disconnect-AzAccount' 會擲出錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="db717-3450">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="db717-3451">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="db717-3451">Az.CognitiveServices</span></span>
* <span data-ttu-id="db717-3452">新增 Get-AzCognitiveServicesAccountSkus 作業。</span><span class="sxs-lookup"><span data-stu-id="db717-3452">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="db717-3453">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="db717-3453">Az.Compute</span></span>
* <span data-ttu-id="db717-3454">新增 Add-AzVmssVMDataDisk 和 Remove-AzVmssVMDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-3454">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="db717-3455">Get-AzVMImage 顯示 AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="db717-3455">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="db717-3456">已修正 SetAzVMChefExtension -BootstrapOptions 和 -JsonAttribute 選項值並未以 json 格式設定的問題。</span><span class="sxs-lookup"><span data-stu-id="db717-3456">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="db717-3457">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="db717-3457">Az.DataLakeStore</span></span>
* <span data-ttu-id="db717-3458">將 DataLake 套件更新為 1.1.10。</span><span class="sxs-lookup"><span data-stu-id="db717-3458">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="db717-3459">將預設並行新增至多執行作業。</span><span class="sxs-lookup"><span data-stu-id="db717-3459">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="db717-3460">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="db717-3460">Az.Insights</span></span>
* <span data-ttu-id="db717-3461">已修正問題 #7267 (自動調整區域)</span><span class="sxs-lookup"><span data-stu-id="db717-3461">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="db717-3462">建立新自動調整規則時未適當設定列舉的參數 (一律會設為預設值) 的問題。</span><span class="sxs-lookup"><span data-stu-id="db717-3462">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="db717-3463">已修正問題 #7513 [Insights] Set-AzDiagnosticSetting 在建立設定時需要明確的類別規格</span><span class="sxs-lookup"><span data-stu-id="db717-3463">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="db717-3464">目前 Cmdlet 在建立期間不需要明確的類別指示也能啟用，例如 Cmdlet 會如說明所述之方式運作</span><span class="sxs-lookup"><span data-stu-id="db717-3464">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="db717-3465">Az.Network</span><span class="sxs-lookup"><span data-stu-id="db717-3465">Az.Network</span></span>
* <span data-ttu-id="db717-3466">已將 PeeringType 變更為下列 Cmdlet 的必要參數：-</span><span class="sxs-lookup"><span data-stu-id="db717-3466">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="db717-3467">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="db717-3467">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="db717-3468">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="db717-3468">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="db717-3469">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="db717-3469">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="db717-3470">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="db717-3470">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="db717-3471">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="db717-3471">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="db717-3472">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="db717-3472">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="db717-3473">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="db717-3473">Az.PolicyInsights</span></span>
* <span data-ttu-id="db717-3474">已新增原則修復 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-3474">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="db717-3475">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="db717-3475">Az.Resources</span></span>
* <span data-ttu-id="db717-3476">修正 https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="db717-3476">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="db717-3477">允許使用 'Get-AzResource' 的 '-ResourceId' 參數列出資源</span><span class="sxs-lookup"><span data-stu-id="db717-3477">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="db717-3478">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="db717-3478">Az.ServiceBus</span></span>
* <span data-ttu-id="db717-3479">已將 MigrationState 唯讀屬性新增至 PSServiceBusMigrationConfigurationAttributes，以便協助了解移轉狀態。</span><span class="sxs-lookup"><span data-stu-id="db717-3479">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="db717-3480">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="db717-3480">Az.ServiceFabric</span></span>
* <span data-ttu-id="db717-3481">修正將憑證新增至 Linux Vmss。</span><span class="sxs-lookup"><span data-stu-id="db717-3481">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="db717-3482">修正 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="db717-3482">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="db717-3483">使用新憑證中正確的指紋 (Azure/service-fabric-issues#932)。</span><span class="sxs-lookup"><span data-stu-id="db717-3483">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="db717-3484">正確顯示例外狀況 (Azure/service-fabric-issues#1054)。</span><span class="sxs-lookup"><span data-stu-id="db717-3484">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="db717-3485">修正 'Update-AzServiceFabricDurability' 以在啟動 Vmss CreateOrUpdate operation 之前更新叢集組態。</span><span class="sxs-lookup"><span data-stu-id="db717-3485">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="db717-3486">0.4.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="db717-3486">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="db717-3487">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="db717-3487">Az.Profile</span></span>
* <span data-ttu-id="db717-3488">修正 CloudShell 中 Get-AzSubscription 的問題</span><span class="sxs-lookup"><span data-stu-id="db717-3488">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="db717-3489">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="db717-3489">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="db717-3490">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="db717-3490">Az.Compute</span></span>
* <span data-ttu-id="db717-3491">已將新的大小新增至虛擬機器大小允許清單，當使用 'New-AzVm' 的簡單參數集合時，將會開啟加速的網路</span><span class="sxs-lookup"><span data-stu-id="db717-3491">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="db717-3492">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db717-3492">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="db717-3493">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="db717-3493">Az.DataLakeStore</span></span>
* <span data-ttu-id="db717-3494">新增虛擬網路規則的支援</span><span class="sxs-lookup"><span data-stu-id="db717-3494">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="db717-3495">Get-AzDataLakeStoreVirtualNetworkRule：取得或列出 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="db717-3495">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="db717-3496">Add-AzDataLakeStoreVirtualNetworkRule：將虛擬網路規則新增至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="db717-3496">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="db717-3497">Set-AzDataLakeStoreVirtualNetworkRule：修改指定 Data Lake Store 帳戶中的特定虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="db717-3497">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="db717-3498">Remove-AzDataLakeStoreVirtualNetworkRule：刪除 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="db717-3498">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="db717-3499">Az.Network</span><span class="sxs-lookup"><span data-stu-id="db717-3499">Az.Network</span></span>
* <span data-ttu-id="db717-3500">更新 Cmdlet Test-AzNetworkWatcherConnectivity，將通訊協定值傳遞至後端。</span><span class="sxs-lookup"><span data-stu-id="db717-3500">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="db717-3501">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db717-3501">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="db717-3502">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="db717-3502">Az.Resources</span></span>
* <span data-ttu-id="db717-3503">修正當 Get-AzRoleDefinition 藉由在案例中加上有意義的例外狀況，而擲回無法辨識的例外狀況 (當預設的設定檔中沒有訂用帳戶，且未指定範圍) 問題。</span><span class="sxs-lookup"><span data-stu-id="db717-3503">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="db717-3504">也將預設參數集合設定為 'RoleDefinitionNameParameterSet'。</span><span class="sxs-lookup"><span data-stu-id="db717-3504">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="db717-3505">0.3.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="db717-3505">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="db717-3506">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="db717-3506">Azure.Storage</span></span>
* <span data-ttu-id="db717-3507">修正當目的地有中繼資料問題時，複製 Blob/檔案不會一併複製中繼資料的問題</span><span class="sxs-lookup"><span data-stu-id="db717-3507">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="db717-3508">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="db717-3508">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="db717-3509">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="db717-3509">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="db717-3510">支援取得特定位置的儲存體資源使用量，並針對取得全域儲存體資源使用量已過時的情況新增警告訊息。</span><span class="sxs-lookup"><span data-stu-id="db717-3510">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="db717-3511">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="db717-3511">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="db717-3512">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="db717-3512">Az.CognitiveServices</span></span>
* <span data-ttu-id="db717-3513">在沒有現有帳戶的情況下支援 Get-AzCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="db717-3513">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="db717-3514">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="db717-3514">Az.Compute</span></span>
* <span data-ttu-id="db717-3515">修正 Get-AzVM -ResourceGroupName <rg> 以在必要時傳回超過 50 個結果</span><span class="sxs-lookup"><span data-stu-id="db717-3515">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="db717-3516">已將 'SimpleParameterSet' 的範例新增到 New-AzVmss Cmdlet 說明中。</span><span class="sxs-lookup"><span data-stu-id="db717-3516">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="db717-3517">已修正 Azure 磁碟加密進度訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="db717-3517">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="db717-3518">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="db717-3518">Az.DataFactoryV2</span></span>
* <span data-ttu-id="db717-3519">已將 ADF .Net SDK 版本更新為 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="db717-3519">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="db717-3520">Az.Network</span><span class="sxs-lookup"><span data-stu-id="db717-3520">Az.Network</span></span>
* <span data-ttu-id="db717-3521">已新增 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="db717-3521">Added NetworkProfile functionality.</span></span> <span data-ttu-id="db717-3522">已新增新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-3522">new cmdlets added</span></span>
    - <span data-ttu-id="db717-3523">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="db717-3523">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="db717-3524">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="db717-3524">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="db717-3525">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="db717-3525">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="db717-3526">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="db717-3526">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="db717-3527">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="db717-3527">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="db717-3528">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="db717-3528">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="db717-3529">已在子網路模型中新增服務關聯連結</span><span class="sxs-lookup"><span data-stu-id="db717-3529">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="db717-3530">已新增 New-AzVirtualNetworkTap、Get-AzVirtualNetworkTap、Set-AzVirtualNetworkTap、Remove-AzVirtualNetworkTap Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-3530">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="db717-3531">已新增 Set-AzNEtworkInterfaceTapConfig、Get-AzNEtworkInterfaceTapConfig 和 Remove-AzNEtworkInterfaceTapConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db717-3531">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="db717-3532">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="db717-3532">Az.RedisCache</span></span>
* <span data-ttu-id="db717-3533">日後允許任何字串做為 Size 參數。</span><span class="sxs-lookup"><span data-stu-id="db717-3533">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="db717-3534">在 P5 PSArgumentCompleter 快顯視窗中新增 P5</span><span class="sxs-lookup"><span data-stu-id="db717-3534">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="db717-3535">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="db717-3535">Az.Resources</span></span>
* <span data-ttu-id="db717-3536">將遺漏的 -Mode 參數新增至 Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="db717-3536">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="db717-3537">修正 Get-AzProviderOperation Commandlet 錯誤 (bug)，以進行包含使用者的 Origin 作業</span><span class="sxs-lookup"><span data-stu-id="db717-3537">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="db717-3538">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="db717-3538">Az.Sql</span></span>
* <span data-ttu-id="db717-3539">已修正部分備份 Cmdlet 無法辨識目前 Azure 訂用帳戶的問題</span><span class="sxs-lookup"><span data-stu-id="db717-3539">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="db717-3540">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="db717-3540">Az.Websites</span></span>
* <span data-ttu-id="db717-3541">新 Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 取得容器連續部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="db717-3541">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="db717-3542">新 Cmdlet New-AzWebAppContainerPSSession 與 Enter-WebAppContainerPSSession  - 在 Windows 容器應用程式中初始 PowerShell 遠端工作階段</span><span class="sxs-lookup"><span data-stu-id="db717-3542">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="db717-3543">0.2.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="db717-3543">0.2.0 - September 2018</span></span>
 <span data-ttu-id="db717-3544">初始版本</span><span class="sxs-lookup"><span data-stu-id="db717-3544">Initial Release</span></span>