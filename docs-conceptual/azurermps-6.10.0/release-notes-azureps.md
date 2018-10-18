---
title: Azure PowerShell 變更記錄 | Microsoft Docs
description: 這是在最新版中對 Azure powershell 所做的變更歷程記錄。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 08/28/2018
ms.openlocfilehash: 6a33d1a85fc61d0281bf1183163185b0dc4d3a12
ms.sourcegitcommit: f6f5e256143aa6c097de3e57e930d8badea49f30
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/18/2018
ms.locfileid: "49399054"
---
# <a name="release-notes"></a><span data-ttu-id="ce770-103">版本資訊</span><span class="sxs-lookup"><span data-stu-id="ce770-103">Release notes</span></span>

<span data-ttu-id="ce770-104">這是此版本中對 Azure PowerShell 所做的變更清單。</span><span class="sxs-lookup"><span data-stu-id="ce770-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6100---october-2018"></a><span data-ttu-id="ce770-105">6.10.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="ce770-105">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="ce770-106">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="ce770-106">Azure.Storage</span></span>
* <span data-ttu-id="ce770-107">修正當目的地有中繼資料問題時，複製 Blob/檔案不會一併複製中繼資料的問題</span><span class="sxs-lookup"><span data-stu-id="ce770-107">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="ce770-108">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ce770-108">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="ce770-109">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="ce770-109">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="ce770-110">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ce770-110">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="ce770-111">在沒有現有帳戶的情況下支援 Get-AzureRmCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="ce770-111">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ce770-112">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ce770-112">AzureRM.Compute</span></span>
* <span data-ttu-id="ce770-113">修正 Get-AzureRmVM -ResourceGroupName <rg> 以在必要時傳回超過 50 個結果</span><span class="sxs-lookup"><span data-stu-id="ce770-113">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="ce770-114">已將 'SimpleParameterSet' 的範例新增到 New-AzureRmVmss Cmdlet 說明中。</span><span class="sxs-lookup"><span data-stu-id="ce770-114">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="ce770-115">已修正 Azure 磁碟加密進度訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="ce770-115">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="ce770-116">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ce770-116">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="ce770-117">已將 ADF .Net SDK 版本更新為 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="ce770-117">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ce770-118">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ce770-118">AzureRM.Network</span></span>
* <span data-ttu-id="ce770-119">已新增 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="ce770-119">Added NetworkProfile functionality.</span></span> <span data-ttu-id="ce770-120">已新增新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ce770-120">new cmdlets added</span></span>
    - <span data-ttu-id="ce770-121">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ce770-121">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="ce770-122">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ce770-122">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="ce770-123">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ce770-123">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="ce770-124">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ce770-124">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="ce770-125">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="ce770-125">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="ce770-126">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="ce770-126">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="ce770-127">已在子網路模型中新增服務關聯連結</span><span class="sxs-lookup"><span data-stu-id="ce770-127">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="ce770-128">已新增 New-AzureRmVirtualNetworkTap、Get-AzureRmVirtualNetworkTap、Set-AzureRmVirtualNetworkTap 和 Remove-AzureRmVirtualNetworkTap Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ce770-128">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="ce770-129">已新增 Set-AzureRmNEtworkInterfaceTapConfig、Get-AzureRmNEtworkInterfaceTapConfig 和 Remove-AzureRmNEtworkInterfaceTapConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ce770-129">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="ce770-130">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ce770-130">AzureRM.RedisCache</span></span>
* <span data-ttu-id="ce770-131">日後允許任何字串做為 Size 參數。</span><span class="sxs-lookup"><span data-stu-id="ce770-131">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="ce770-132">在 P5 PSArgumentCompleter 快顯視窗中新增 P5</span><span class="sxs-lookup"><span data-stu-id="ce770-132">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ce770-133">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ce770-133">AzureRM.Resources</span></span>
* <span data-ttu-id="ce770-134">將遺漏的 -Mode 參數新增至 Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ce770-134">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="ce770-135">修正 Get-AzureRmProviderOperation Commandlet 錯誤 (bug)，以進行包含使用者的 Origin 作業</span><span class="sxs-lookup"><span data-stu-id="ce770-135">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ce770-136">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ce770-136">AzureRM.Sql</span></span>
* <span data-ttu-id="ce770-137">已修正部分備份 Cmdlet 無法辨識目前 Azure 訂用帳戶的問題</span><span class="sxs-lookup"><span data-stu-id="ce770-137">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="ce770-138">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="ce770-138">AzureRM.Storage</span></span>
* <span data-ttu-id="ce770-139">支援取得特定位置的儲存體資源使用量，並針對取得全域儲存體資源使用量已過時的情況新增警告訊息。</span><span class="sxs-lookup"><span data-stu-id="ce770-139">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="ce770-140">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="ce770-140">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ce770-141">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ce770-141">AzureRM.Websites</span></span>
* <span data-ttu-id="ce770-142">新 Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - 取得容器連續部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="ce770-142">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="ce770-143">新 Cmdlet New-AzureRMWebAppContainerPSSession 與 Enter-WebAppContainerPSSession  - 在 Windows 容器應用程式中初始 PowerShell 遠端工作階段</span><span class="sxs-lookup"><span data-stu-id="ce770-143">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="ce770-144">6.9.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="ce770-144">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ce770-145">一般</span><span class="sxs-lookup"><span data-stu-id="ce770-145">General</span></span>
* <span data-ttu-id="ce770-146">已將 AzureRM.SignalR 新增至 AzureRM 彙總模組</span><span class="sxs-lookup"><span data-stu-id="ce770-146">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="ce770-147">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ce770-147">AzureRM.Profile</span></span>
* <span data-ttu-id="ce770-148">儲存體通用程式碼的小幅變更</span><span class="sxs-lookup"><span data-stu-id="ce770-148">Minor changes to the storage common code</span></span>
* <span data-ttu-id="ce770-149">已更新說明檔以包含完整的參數類型。</span><span class="sxs-lookup"><span data-stu-id="ce770-149">Updated help files to include full parameter types.</span></span>
- <span data-ttu-id="ce770-150">已變更 - 非強制性的 ServicePrincipal 位在 ServicePrincipalCertificateWithSubscriptionId 參數集</span><span class="sxs-lookup"><span data-stu-id="ce770-150">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="ce770-151">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="ce770-151">Azure.Storage</span></span>
* <span data-ttu-id="ce770-152">支援使用 OAuth 建立儲存體內容。</span><span class="sxs-lookup"><span data-stu-id="ce770-152">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="ce770-153">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="ce770-153">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="ce770-154">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="ce770-154">AzureRM.Cdn</span></span>
* <span data-ttu-id="ce770-155">已在 CDN 定價 SKU 中新增 Standard_Microsoft。</span><span class="sxs-lookup"><span data-stu-id="ce770-155">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="ce770-156">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ce770-156">AzureRM.Compute</span></span>
* <span data-ttu-id="ce770-157">將金鑰保存庫和儲存體上的相依性移至一般相依性</span><span class="sxs-lookup"><span data-stu-id="ce770-157">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="ce770-158">對 AEM Cmdlet 新增更多的虛擬機器大小支援</span><span class="sxs-lookup"><span data-stu-id="ce770-158">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="ce770-159">將 PublicIPPrefix 參數新增至 New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="ce770-159">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="ce770-160">將 ResourceId 參數新增至 Invoke-AzureRmVMRunCommand Cmdelt</span><span class="sxs-lookup"><span data-stu-id="ce770-160">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="ce770-161">新增 Invoke-AzureRmVmssVMRunCommand Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ce770-161">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="ce770-162">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="ce770-162">AzureRM.Dns</span></span>
* <span data-ttu-id="ce770-163">已新增建立 DNS 記錄時的別名記錄支援</span><span class="sxs-lookup"><span data-stu-id="ce770-163">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="ce770-164">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="ce770-164">AzureRM.Insights</span></span>
* <span data-ttu-id="ce770-165">已修正問題 #6833 和 #7102 (診斷設定區域)</span><span class="sxs-lookup"><span data-stu-id="ce770-165">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="ce770-166">建立和列出/取得診斷設定時的預設名稱問題 (例如 'service')</span><span class="sxs-lookup"><span data-stu-id="ce770-166">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="ce770-167">以類別建立診斷設定的問題</span><span class="sxs-lookup"><span data-stu-id="ce770-167">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="ce770-168">已新增計量時間粒紋參數的取代訊息</span><span class="sxs-lookup"><span data-stu-id="ce770-168">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="ce770-169">Timegrains 參數還是可用 (這是非中斷性變更)，但會在後端中遭到忽略，因為只有 PT1M 有效</span><span class="sxs-lookup"><span data-stu-id="ce770-169">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ce770-170">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ce770-170">AzureRM.Network</span></span>
* <span data-ttu-id="ce770-171">LoadBalancer Cmdlet 的變更</span><span class="sxs-lookup"><span data-stu-id="ce770-171">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="ce770-172">LoadBalancerInboundNatPoolConfig：已新增 IdleTimeoutInMinutes、EnableFloatingIp 和 EnableTcpReset 參數</span><span class="sxs-lookup"><span data-stu-id="ce770-172">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="ce770-173">LoadBalancerInboundNatRuleConfig：已新增 EnableTcpReset 參數</span><span class="sxs-lookup"><span data-stu-id="ce770-173">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="ce770-174">LoadBalancerRuleConfig：已新增 EnableTcpReset 參數</span><span class="sxs-lookup"><span data-stu-id="ce770-174">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="ce770-175">LoadBalancerProbeConfig：已為 Protocol 參數新增 "Https" 值的支援</span><span class="sxs-lookup"><span data-stu-id="ce770-175">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="ce770-176">已為新 LoadBalancer 的子資源 OutboundRule 新增命令</span><span class="sxs-lookup"><span data-stu-id="ce770-176">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="ce770-177">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ce770-177">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="ce770-178">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ce770-178">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="ce770-179">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ce770-179">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="ce770-180">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ce770-180">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="ce770-181">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ce770-181">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="ce770-182">已為 PSNetworkInterface 新增 HostedWorkloads 屬性</span><span class="sxs-lookup"><span data-stu-id="ce770-182">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="ce770-183">已為以下功能新增 Cmdlet：由 ARM 支援的 Azure 防火牆</span><span class="sxs-lookup"><span data-stu-id="ce770-183">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="ce770-184">已新增 Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="ce770-184">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="ce770-185">已新增 Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="ce770-185">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="ce770-186">已新增 New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="ce770-186">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="ce770-187">已新增 Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="ce770-187">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="ce770-188">已新增 New-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="ce770-188">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="ce770-189">已新增 New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="ce770-189">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="ce770-190">已新增 New-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="ce770-190">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="ce770-191">已新增 New-AzureRmFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="ce770-191">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="ce770-192">已新增 New-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="ce770-192">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="ce770-193">已新增 New-AzureRmFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ce770-193">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="ce770-194">已在應用程式閘道中新增受信任根憑證和自動調整組態的支援</span><span class="sxs-lookup"><span data-stu-id="ce770-194">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="ce770-195">已新增的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ce770-195">New Cmdlets added:</span></span>
      - <span data-ttu-id="ce770-196">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ce770-196">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="ce770-197">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ce770-197">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="ce770-198">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ce770-198">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="ce770-199">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ce770-199">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="ce770-200">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ce770-200">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="ce770-201">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce770-201">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="ce770-202">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce770-202">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="ce770-203">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce770-203">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="ce770-204">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce770-204">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="ce770-205">已使用選擇性參數 TrustedRootCertificate 更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ce770-205">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="ce770-206">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ce770-206">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="ce770-207">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ce770-207">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="ce770-208">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="ce770-208">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="ce770-209">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="ce770-209">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="ce770-210">已使用選擇性參數 AutoscaleConfiguration 更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ce770-210">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="ce770-211">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ce770-211">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="ce770-212">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ce770-212">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="ce770-213">為介面端點 Get-AzureInterfaceEndpoint 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ce770-213">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="ce770-214">已在子網路中新增多個位址前置詞的支援。</span><span class="sxs-lookup"><span data-stu-id="ce770-214">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="ce770-215">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ce770-215">Updated cmdlets:</span></span>
  - <span data-ttu-id="ce770-216">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ce770-216">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="ce770-217">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ce770-217">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="ce770-218">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ce770-218">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="ce770-219">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ce770-219">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="ce770-220">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ce770-220">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="ce770-221">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ce770-221">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="ce770-222">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ce770-222">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="ce770-223">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ce770-223">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="ce770-224">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce770-224">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="ce770-225">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce770-225">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="ce770-226">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce770-226">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="ce770-227">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ce770-227">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="ce770-228">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ce770-228">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="ce770-229">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="ce770-229">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="ce770-230">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="ce770-230">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="ce770-231">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ce770-231">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="ce770-232">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ce770-232">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="ce770-233">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ce770-233">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="ce770-234">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ce770-234">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="ce770-235">為子網路委派新增 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce770-235">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="ce770-236">New-AzureRmDelegation：建立可新增至子網路的新委派</span><span class="sxs-lookup"><span data-stu-id="ce770-236">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="ce770-237">Remove-AzureRmDelegation：用於子網路，可從該子網路中移除提供的委派名稱</span><span class="sxs-lookup"><span data-stu-id="ce770-237">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="ce770-238">Add-AzureRmDelegation：用於子網路，可將提供的服務名稱新增為該子網路的委派</span><span class="sxs-lookup"><span data-stu-id="ce770-238">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="ce770-239">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="ce770-239">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="ce770-240">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="ce770-240">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="ce770-241">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="ce770-241">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="ce770-242">支援受控磁碟</span><span class="sxs-lookup"><span data-stu-id="ce770-242">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="ce770-243">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ce770-243">AzureRM.RedisCache</span></span>
* <span data-ttu-id="ce770-244">已更新深入解析相依性。</span><span class="sxs-lookup"><span data-stu-id="ce770-244">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ce770-245">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ce770-245">AzureRM.Resources</span></span>
* <span data-ttu-id="ce770-246">使用新參數 RollbackAction 更新 New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ce770-246">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="ce770-247">使用新參數新增 OnErrorDeployment 的支援。</span><span class="sxs-lookup"><span data-stu-id="ce770-247">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="ce770-248">支援原則指派上的受控識別。</span><span class="sxs-lookup"><span data-stu-id="ce770-248">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="ce770-249">以 'New-AzureRmPolicyAssignment' 指派原則時不再需要具有預設值的參數</span><span class="sxs-lookup"><span data-stu-id="ce770-249">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="ce770-250">新增 Get-AzureRmPolicyAlias Cmdlet 來擷取原則別名</span><span class="sxs-lookup"><span data-stu-id="ce770-250">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ce770-251">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ce770-251">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ce770-252">已修正問題 #7161</span><span class="sxs-lookup"><span data-stu-id="ce770-252">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="ce770-253">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="ce770-253">AzureRM.SignalR</span></span>
* <span data-ttu-id="ce770-254">將 SKU 名稱更新為 Free_F1 和 Standard_S1</span><span class="sxs-lookup"><span data-stu-id="ce770-254">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="ce770-255">將版本欄位新增至 PSSignalRResource 物件，以及將連接字串新增至 PSSignalRKeys 物件。</span><span class="sxs-lookup"><span data-stu-id="ce770-255">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="ce770-256">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="ce770-256">AzureRM.Storage</span></span>
* <span data-ttu-id="ce770-257">在 AzureRm.Storage 中支援不變原則</span><span class="sxs-lookup"><span data-stu-id="ce770-257">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="ce770-258">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ce770-258">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="ce770-259">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ce770-259">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="ce770-260">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ce770-260">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="ce770-261">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ce770-261">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="ce770-262">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ce770-262">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="ce770-263">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="ce770-263">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="ce770-264">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="ce770-264">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="ce770-265">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ce770-265">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="ce770-266">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ce770-266">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="ce770-267">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ce770-267">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="ce770-268">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ce770-268">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ce770-269">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ce770-269">AzureRM.Websites</span></span>
* <span data-ttu-id="ce770-270">已新增兩個 Cmdlet：Get-AzureRmDeletedWebApp 和 Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="ce770-270">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="ce770-271">New-AzureRmAppServicePlan - 已新增 HyperV 切換以使用 Windows 容器建立 App Service 方案</span><span class="sxs-lookup"><span data-stu-id="ce770-271">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="ce770-272">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - 已新增參數 (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) 來建立和管理 Windows 容器應用程式</span><span class="sxs-lookup"><span data-stu-id="ce770-272">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="ce770-273">6.8.1 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="ce770-273">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ce770-274">一般</span><span class="sxs-lookup"><span data-stu-id="ce770-274">General</span></span>
* <span data-ttu-id="ce770-275">已修正未設定預設資源群組的問題。</span><span class="sxs-lookup"><span data-stu-id="ce770-275">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="ce770-276">已更新通用執行階段組件</span><span class="sxs-lookup"><span data-stu-id="ce770-276">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="ce770-277">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ce770-277">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="ce770-278">已修正未設定預設資源群組的問題。</span><span class="sxs-lookup"><span data-stu-id="ce770-278">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="ce770-279">已修正的問題 https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="ce770-279">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="ce770-280">Import-AzureRmApiManagementApi 和 \*-AzureRmApiManagementCertificate cmdlets 目前處理相對路徑</span><span class="sxs-lookup"><span data-stu-id="ce770-280">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="ce770-281">已修正的問題 https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="ce770-281">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="ce770-282">CertificateInformation 為可設定的屬性，允許 Set-AzureRmApiManagement Cmdlet 正常運作。</span><span class="sxs-lookup"><span data-stu-id="ce770-282">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="ce770-283">已藉由升級至 4.0.4-preview NuGet 而修正</span><span class="sxs-lookup"><span data-stu-id="ce770-283">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="ce770-284">已修正的問題 https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="ce770-284">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="ce770-285">已修正依產品名稱搜尋的 Odata 篩選條件</span><span class="sxs-lookup"><span data-stu-id="ce770-285">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="ce770-286">已修正的問題 https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="ce770-286">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="ce770-287">已修正依 API 名稱搜尋的 Odata 篩選條件</span><span class="sxs-lookup"><span data-stu-id="ce770-287">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="ce770-288">已新增對 AzureMonitor 記錄器的支援</span><span class="sxs-lookup"><span data-stu-id="ce770-288">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="ce770-289">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ce770-289">AzureRM.Compute</span></span>
* <span data-ttu-id="ce770-290">已修正在錯誤輸出中遺漏目標的問題。</span><span class="sxs-lookup"><span data-stu-id="ce770-290">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="ce770-291">已修正搭配受控磁碟的 VM 之儲存體帳戶類型的問題</span><span class="sxs-lookup"><span data-stu-id="ce770-291">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="ce770-292">已修正未設定預設資源群組的問題。</span><span class="sxs-lookup"><span data-stu-id="ce770-292">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="ce770-293">修正適用於其他環境的 AEM 擴充 Cmdlet，例如 Azure China</span><span class="sxs-lookup"><span data-stu-id="ce770-293">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ce770-294">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ce770-294">AzureRM.Network</span></span>
* <span data-ttu-id="ce770-295">已將預設的 Cmdlet 輸出表示法變更為資料表檢視</span><span class="sxs-lookup"><span data-stu-id="ce770-295">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="ce770-296">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="ce770-296">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="ce770-297">修正在嘗試調整已暫停的容量時，Update-AzureRmPowerBIEmbeddedCapacity 中發生的錯誤</span><span class="sxs-lookup"><span data-stu-id="ce770-297">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="ce770-298">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ce770-298">AzureRM.Resources</span></span>
* <span data-ttu-id="ce770-299">已修正從 MarketPlace 建立受控應用程式發生的問題。</span><span class="sxs-lookup"><span data-stu-id="ce770-299">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ce770-300">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ce770-300">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ce770-301">已修正的問題</span><span class="sxs-lookup"><span data-stu-id="ce770-301">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ce770-302">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ce770-302">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ce770-303">已新增對 MultiValue 路由方法的支援</span><span class="sxs-lookup"><span data-stu-id="ce770-303">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="ce770-304">為 MultiValue 路由新增 'MaxReturn' 參數</span><span class="sxs-lookup"><span data-stu-id="ce770-304">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="ce770-305">已新增對子網路路由方法的支援</span><span class="sxs-lookup"><span data-stu-id="ce770-305">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="ce770-306">支援端點中的 IP 位址範圍 (子網路)</span><span class="sxs-lookup"><span data-stu-id="ce770-306">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="ce770-307">已新增對設定檔中自訂標頭的支援</span><span class="sxs-lookup"><span data-stu-id="ce770-307">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="ce770-308">已新增對設定檔中預期狀態碼的支援</span><span class="sxs-lookup"><span data-stu-id="ce770-308">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="ce770-309">已新增對端點中自訂標頭的支援</span><span class="sxs-lookup"><span data-stu-id="ce770-309">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="ce770-310">6.8.0 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="ce770-310">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ce770-311">一般</span><span class="sxs-lookup"><span data-stu-id="ce770-311">General</span></span>
* <span data-ttu-id="ce770-312">已修正未設定預設資源群組的問題。</span><span class="sxs-lookup"><span data-stu-id="ce770-312">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="ce770-313">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ce770-313">AzureRM.Profile</span></span>
* <span data-ttu-id="ce770-314">已將到期屬性新增至在 Connect-AzureRmAccount 期間傳回的權杖</span><span class="sxs-lookup"><span data-stu-id="ce770-314">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ce770-315">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ce770-315">AzureRM.Compute</span></span>
* <span data-ttu-id="ce770-316">已修正在錯誤輸出中遺漏目標的問題。</span><span class="sxs-lookup"><span data-stu-id="ce770-316">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="ce770-317">已修正搭配受控磁碟的 VM 之儲存體帳戶類型的問題</span><span class="sxs-lookup"><span data-stu-id="ce770-317">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="ce770-318">修正適用於其他環境的 AEM 擴充 Cmdlet，例如 Azure China</span><span class="sxs-lookup"><span data-stu-id="ce770-318">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="ce770-319">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="ce770-319">AzureRM.IotHub</span></span>
* <span data-ttu-id="ce770-320">修正 New-AzureRmIotHubExportDevices 和 New-AzureRmIotHubImportDevices 的範例</span><span class="sxs-lookup"><span data-stu-id="ce770-320">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ce770-321">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ce770-321">AzureRM.Network</span></span>
* <span data-ttu-id="ce770-322">已將預設模式表示法變更為資料表檢視</span><span class="sxs-lookup"><span data-stu-id="ce770-322">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="ce770-323">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="ce770-323">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="ce770-324">修正在嘗試調整已暫停的容量時，Update-AzureRmPowerBIEmbeddedCapacity 中發生的錯誤</span><span class="sxs-lookup"><span data-stu-id="ce770-324">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ce770-325">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ce770-325">AzureRM.Resources</span></span>
* <span data-ttu-id="ce770-326">已修正從 MarketPlace 建立受控應用程式發生的問題。</span><span class="sxs-lookup"><span data-stu-id="ce770-326">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ce770-327">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ce770-327">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ce770-328">修正問題</span><span class="sxs-lookup"><span data-stu-id="ce770-328">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ce770-329">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ce770-329">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ce770-330">支援 MultiValue 路由方法</span><span class="sxs-lookup"><span data-stu-id="ce770-330">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="ce770-331">為 MultiValue 路由新增 'MaxReturn' 參數</span><span class="sxs-lookup"><span data-stu-id="ce770-331">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="ce770-332">支援子網路路由方法</span><span class="sxs-lookup"><span data-stu-id="ce770-332">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="ce770-333">支援端點中的 IP 位址範圍 (子網路)</span><span class="sxs-lookup"><span data-stu-id="ce770-333">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="ce770-334">支援設定檔中的自訂標頭</span><span class="sxs-lookup"><span data-stu-id="ce770-334">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="ce770-335">支援設定檔中的預期狀態碼</span><span class="sxs-lookup"><span data-stu-id="ce770-335">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="ce770-336">支援端點中的自訂標頭</span><span class="sxs-lookup"><span data-stu-id="ce770-336">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ce770-337">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ce770-337">AzureRM.Websites</span></span>
* <span data-ttu-id="ce770-338">已修正未正確設定預設資源群組的問題。</span><span class="sxs-lookup"><span data-stu-id="ce770-338">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="ce770-339">6.7.0 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="ce770-339">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ce770-340">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ce770-340">AzureRM.Profile</span></span>
* <span data-ttu-id="ce770-341">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-341">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="ce770-342">將使用者識別碼新增至預設內容名稱，以避免內容發生衝突</span><span class="sxs-lookup"><span data-stu-id="ce770-342">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="ce770-343">修正 Clear-AzureRmContext 在選擇內容 #6398 時出現的問題</span><span class="sxs-lookup"><span data-stu-id="ce770-343">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="ce770-344">允許將租用戶網域傳遞給 'Connect-AzureRmAccount' 的 '-TenantId' 參數</span><span class="sxs-lookup"><span data-stu-id="ce770-344">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="ce770-345">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="ce770-345">Azure.Storage</span></span>
* <span data-ttu-id="ce770-346">移除 Azure 檔案共用 5TB 的配額限制</span><span class="sxs-lookup"><span data-stu-id="ce770-346">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="ce770-347">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="ce770-347">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="ce770-348">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ce770-348">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="ce770-349">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-349">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="ce770-350">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ce770-350">Azure.AnalysisServices</span></span>
* <span data-ttu-id="ce770-351">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-351">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="ce770-352">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ce770-352">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="ce770-353">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-353">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="ce770-354">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="ce770-354">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="ce770-355">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-355">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="ce770-356">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="ce770-356">AzureRM.Automation</span></span>
* <span data-ttu-id="ce770-357">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-357">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="ce770-358">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="ce770-358">AzureRM.Backup</span></span>
* <span data-ttu-id="ce770-359">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-359">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="ce770-360">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="ce770-360">AzureRM.Batch</span></span>
* <span data-ttu-id="ce770-361">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-361">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="ce770-362">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="ce770-362">AzureRM.Billing</span></span>
* <span data-ttu-id="ce770-363">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-363">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="ce770-364">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="ce770-364">AzureRM.Cdn</span></span>
* <span data-ttu-id="ce770-365">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-365">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="ce770-366">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ce770-366">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="ce770-367">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-367">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ce770-368">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ce770-368">AzureRM.Compute</span></span>
* <span data-ttu-id="ce770-369">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-369">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="ce770-370">將 EvictionPolicy 參數新增至 New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="ce770-370">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="ce770-371">若未指定位置，則使用 New-AzureRmVm 的 DiskFileParameterSet 中的預設位置。</span><span class="sxs-lookup"><span data-stu-id="ce770-371">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="ce770-372">修正 Save-AzureRmVMImage 中的參數描述</span><span class="sxs-lookup"><span data-stu-id="ce770-372">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="ce770-373">修正某些單次傳遞相關案例的 Get-AzureRmVMDiskEncryptionStatus Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ce770-373">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="ce770-374">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="ce770-374">AzureRM.Consumption</span></span>
* <span data-ttu-id="ce770-375">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-375">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="ce770-376">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ce770-376">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="ce770-377">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-377">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="ce770-378">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ce770-378">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="ce770-379">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-379">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="ce770-380">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="ce770-380">AzureRM.DataFactories</span></span>
* <span data-ttu-id="ce770-381">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-381">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="ce770-382">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ce770-382">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="ce770-383">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-383">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="ce770-384">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="ce770-384">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="ce770-385">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-385">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="ce770-386">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ce770-386">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="ce770-387">修正從 PowerShell 命令列設定 DebugPreference 時的偵錯問</span><span class="sxs-lookup"><span data-stu-id="ce770-387">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="ce770-388">更新 Set-AzureRmDataLakeStoreItemAcl 範例</span><span class="sxs-lookup"><span data-stu-id="ce770-388">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="ce770-389">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-389">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="ce770-390">更新 Set-AzureRmDataLakeStoreItemAclEntry 範例</span><span class="sxs-lookup"><span data-stu-id="ce770-390">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="ce770-391">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="ce770-391">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="ce770-392">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-392">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="ce770-393">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="ce770-393">AzureRM.Dns</span></span>
* <span data-ttu-id="ce770-394">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-394">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="ce770-395">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ce770-395">AzureRM.EventGrid</span></span>
* <span data-ttu-id="ce770-396">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-396">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="ce770-397">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="ce770-397">AzureRM.EventHub</span></span>
* <span data-ttu-id="ce770-398">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-398">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="ce770-399">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ce770-399">AzureRM.HDInsight</span></span>
* <span data-ttu-id="ce770-400">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-400">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="ce770-401">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="ce770-401">AzureRM.Insights</span></span>
* <span data-ttu-id="ce770-402">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-402">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="ce770-403">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="ce770-403">AzureRM.IotHub</span></span>
* <span data-ttu-id="ce770-404">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-404">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ce770-405">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ce770-405">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ce770-406">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-406">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="ce770-407">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ce770-407">AzureRM.LogicApp</span></span>
* <span data-ttu-id="ce770-408">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-408">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="ce770-409">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="ce770-409">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="ce770-410">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-410">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="ce770-411">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="ce770-411">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="ce770-412">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-412">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="ce770-413">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="ce770-413">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="ce770-414">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-414">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="ce770-415">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="ce770-415">AzureRM.Media</span></span>
* <span data-ttu-id="ce770-416">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-416">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ce770-417">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ce770-417">AzureRM.Network</span></span>
* <span data-ttu-id="ce770-418">已新增 Set-AzureRmLocalNetworkGateway 範例</span><span class="sxs-lookup"><span data-stu-id="ce770-418">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="ce770-419">已新增 Add-AzureRmVirtualNetworkGatewayIpConfig、Get-AzureRmVirtualNetworkGatewayConnectionSharedKey 和 New-AzureRmVirtualNetworkGatewayConnection 的範例和描述</span><span class="sxs-lookup"><span data-stu-id="ce770-419">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="ce770-420">已新增 Remove-AzureRmVirtualNetworkGatewayIpConfig 和 Reset-AzureRmVirtualNetworkGateway 的範例</span><span class="sxs-lookup"><span data-stu-id="ce770-420">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="ce770-421">已新增 Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey 的範例</span><span class="sxs-lookup"><span data-stu-id="ce770-421">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="ce770-422">已新增 Set-AzureRmVirtualNetworkGatewayConnectionSharedKey 的範例</span><span class="sxs-lookup"><span data-stu-id="ce770-422">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="ce770-423">已新增 Set-AzureRmVirtualNetworkGatewayConnection 的範例</span><span class="sxs-lookup"><span data-stu-id="ce770-423">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="ce770-424">已使用最新的程式碼產生器重新產生 ApplicationSecurityGroup、RouteTable 和 Usage</span><span class="sxs-lookup"><span data-stu-id="ce770-424">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="ce770-425">已釐清在嘗試取得未結束的子網路時，Get-AzureRmVirtualNetworkSubnetConfig 出現的錯誤</span><span class="sxs-lookup"><span data-stu-id="ce770-425">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="ce770-426">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="ce770-426">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="ce770-427">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-427">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="ce770-428">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ce770-428">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="ce770-429">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-429">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="ce770-430">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ce770-430">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="ce770-431">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-431">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="ce770-432">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="ce770-432">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="ce770-433">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-433">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="ce770-434">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ce770-434">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="ce770-435">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-435">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="ce770-436">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="ce770-436">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="ce770-437">已將原則篩選條件新增至 Get-AzureRmRecoveryServicesBackItem Xmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce770-437">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="ce770-438">命令會傳回受指定原則識別碼保護的備份項目清單。</span><span class="sxs-lookup"><span data-stu-id="ce770-438">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="ce770-439">已將 Microsoft.Azure.Management.RecoveryServices.Backup 更新為版本 3.0.0-preview。</span><span class="sxs-lookup"><span data-stu-id="ce770-439">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="ce770-440">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-440">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="ce770-441">已將 TargetResourceGroupName 參數新增至 Restore-AzureRmRecoveryServicesBackupItem。</span><span class="sxs-lookup"><span data-stu-id="ce770-441">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="ce770-442">受控磁碟還原的資源群組。</span><span class="sxs-lookup"><span data-stu-id="ce770-442">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="ce770-443">適用於具有受控磁碟的 VM 備份。</span><span class="sxs-lookup"><span data-stu-id="ce770-443">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="ce770-444">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="ce770-444">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="ce770-445">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-445">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="ce770-446">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ce770-446">AzureRM.RedisCache</span></span>
* <span data-ttu-id="ce770-447">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-447">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="ce770-448">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="ce770-448">AzureRM.Relay</span></span>
* <span data-ttu-id="ce770-449">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-449">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ce770-450">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ce770-450">AzureRM.Resources</span></span>
* <span data-ttu-id="ce770-451">支援在訂用帳戶範圍部署範本。</span><span class="sxs-lookup"><span data-stu-id="ce770-451">Support template deployment at subscription scope.</span></span> <span data-ttu-id="ce770-452">新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ce770-452">Add new Cmdlets:</span></span>
    - <span data-ttu-id="ce770-453">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ce770-453">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="ce770-454">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ce770-454">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="ce770-455">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ce770-455">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="ce770-456">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ce770-456">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="ce770-457">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ce770-457">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="ce770-458">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="ce770-458">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="ce770-459">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="ce770-459">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="ce770-460">修正在將內容傳遞至 Set-AzureRmResource 時擲回錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="ce770-460">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="ce770-461">修正 New-AzureRmResourceGroupDeployment 中的範例</span><span class="sxs-lookup"><span data-stu-id="ce770-461">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="ce770-462">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-462">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="ce770-463">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="ce770-463">AzureRM.Scheduler</span></span>
* <span data-ttu-id="ce770-464">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-464">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ce770-465">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ce770-465">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ce770-466">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-466">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="ce770-467">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ce770-467">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="ce770-468">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-468">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ce770-469">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ce770-469">AzureRM.Sql</span></span>
* <span data-ttu-id="ce770-470">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-470">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="ce770-471">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="ce770-471">AzureRM.Storage</span></span>
* <span data-ttu-id="ce770-472">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-472">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="ce770-473">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="ce770-473">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="ce770-474">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-474">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="ce770-475">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="ce770-475">AzureRM.Tags</span></span>
* <span data-ttu-id="ce770-476">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-476">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ce770-477">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ce770-477">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ce770-478">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-478">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="ce770-479">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="ce770-479">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="ce770-480">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-480">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ce770-481">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ce770-481">AzureRM.Websites</span></span>
* <span data-ttu-id="ce770-482">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="ce770-482">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="ce770-483">6.6.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="ce770-483">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ce770-484">一般</span><span class="sxs-lookup"><span data-stu-id="ce770-484">General</span></span>
* <span data-ttu-id="ce770-485">已更新所有說明檔以包含完整的參數類型和正確的輸入/輸出類型。</span><span class="sxs-lookup"><span data-stu-id="ce770-485">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="ce770-486">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ce770-486">AzureRM.Profile</span></span>
* <span data-ttu-id="ce770-487">已更新 Common.Strategy 程式庫，以便能驗證資源目前的設定與目標資源相容。</span><span class="sxs-lookup"><span data-stu-id="ce770-487">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="ce770-488">已將 ps1xml 類型新增至 Common.Storage</span><span class="sxs-lookup"><span data-stu-id="ce770-488">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="ce770-489">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="ce770-489">Azure.Storage</span></span>
* <span data-ttu-id="ce770-490">已新增從 DefaultProfile 取得儲存體內容的支援</span><span class="sxs-lookup"><span data-stu-id="ce770-490">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="ce770-491">已將 Ps1XmlAttribute 新增至 Cmdlet 輸出類型屬性。</span><span class="sxs-lookup"><span data-stu-id="ce770-491">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="ce770-492">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ce770-492">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="ce770-493">已修正的問題 https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="ce770-493">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="ce770-494">已修正 Automapper 中的錯誤，以將 PsApiManagementApi 轉譯為 ApiContract</span><span class="sxs-lookup"><span data-stu-id="ce770-494">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="ce770-495">已修正的問題 https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="ce770-495">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="ce770-496">已修正 File.Save 中的錯誤，不多載編碼類型</span><span class="sxs-lookup"><span data-stu-id="ce770-496">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="ce770-497">已修正的問題 https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="ce770-497">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="ce770-498">已升級至 4.0.3 Nuget 版本，其修正了 apiId 的模式例外狀況</span><span class="sxs-lookup"><span data-stu-id="ce770-498">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ce770-499">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ce770-499">AzureRM.Compute</span></span>
* <span data-ttu-id="ce770-500">修正因為重新命名 PremiumLRS 儲存體帳戶類型，而在 New-AzureRmVm 中使用 DiskFileParameterSet 建立 VM 失敗的問題。</span><span class="sxs-lookup"><span data-stu-id="ce770-500">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="ce770-501">修正 Invoke-AzureRmVMRunCommand Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ce770-501">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="ce770-502">更新 Get-AzureRmAvailabilitySet，以列出訂用帳戶中所有可用性設定組。</span><span class="sxs-lookup"><span data-stu-id="ce770-502">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="ce770-503">(ResouceGroupName 參數現在為選用。)</span><span class="sxs-lookup"><span data-stu-id="ce770-503">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="ce770-504">更新 'New-AzureRmVm' 的 SimpleParameterSet，以在符合資格的 VM 上啟用加速網路。</span><span class="sxs-lookup"><span data-stu-id="ce770-504">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="ce770-505">更新 New-AzureRmVmss 簡單參數集，讓使用者指定的 LB 已存在時 vmss 建立會失敗。</span><span class="sxs-lookup"><span data-stu-id="ce770-505">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="ce770-506">更新 New-AzureRmDisk 的範例</span><span class="sxs-lookup"><span data-stu-id="ce770-506">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="ce770-507">新增 'New-AzureRmVM' 的範例</span><span class="sxs-lookup"><span data-stu-id="ce770-507">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="ce770-508">更新 Set-AzureRmVMOSDisk 的說明</span><span class="sxs-lookup"><span data-stu-id="ce770-508">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="ce770-509">更新 Set-AzureRmVMBginfoExtension 的範例 1 以更正拼字和前置詞。</span><span class="sxs-lookup"><span data-stu-id="ce770-509">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="ce770-510">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ce770-510">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="ce770-511">已將 ADF .Net SDK 版本更新為 1.1.0。</span><span class="sxs-lookup"><span data-stu-id="ce770-511">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="ce770-512">支援跨資料處理站的自我裝載整合執行階段共用。</span><span class="sxs-lookup"><span data-stu-id="ce770-512">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="ce770-513">新增新參數 -SharedIntegrationRuntimeResourceId 至 Set-AzureRmDataFactoryV2IntegrationRuntime Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce770-513">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="ce770-514">將新的選用參數 -LinkedDataFactoryName 新增至 Remove-AzureRmDataFactoryV2IntegrationRuntime Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce770-514">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="ce770-515">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ce770-515">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="ce770-516">已將 DataPlane SDK (Microsoft.Azure.DataLake.Store) 版本更新為 1.1.9</span><span class="sxs-lookup"><span data-stu-id="ce770-516">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="ce770-517">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="ce770-517">AzureRM.EventHub</span></span>
* <span data-ttu-id="ce770-518">已在移除 Cmdlet 中更新了 InputObject 和 ResourceId 的管線</span><span class="sxs-lookup"><span data-stu-id="ce770-518">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="ce770-519">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="ce770-519">AzureRM.Insights</span></span>
* <span data-ttu-id="ce770-520">已修正說明檔案中的 OutputType 格式</span><span class="sxs-lookup"><span data-stu-id="ce770-520">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="ce770-521">使用 Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="ce770-521">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ce770-522">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ce770-522">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ce770-523">修正 Set-AzureRmKeyVaultAccessPolicy 中的管線問題</span><span class="sxs-lookup"><span data-stu-id="ce770-523">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ce770-524">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ce770-524">AzureRM.Network</span></span>
* <span data-ttu-id="ce770-525">已新增 LoadBalancerInboundNatPoolConfig Cmdlet 的範例。</span><span class="sxs-lookup"><span data-stu-id="ce770-525">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ce770-526">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ce770-526">AzureRM.Resources</span></span>
* <span data-ttu-id="ce770-527">修正在提供 'Get-AzureRmResource' 標籤名稱和值時發生的問題</span><span class="sxs-lookup"><span data-stu-id="ce770-527">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="ce770-528">修正 'Set-AzureRmResource' 的管線狀況</span><span class="sxs-lookup"><span data-stu-id="ce770-528">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ce770-529">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ce770-529">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ce770-530">已在移除 Cmdlet 中更新了 InputObject 和 ResourceId 的管線</span><span class="sxs-lookup"><span data-stu-id="ce770-530">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="ce770-531">已修正一些問題</span><span class="sxs-lookup"><span data-stu-id="ce770-531">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="ce770-532">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ce770-532">AzureRM.Sql</span></span>
* <span data-ttu-id="ce770-533">透過下列 Cmdlet 新增伺服器進階威脅防護支援：</span><span class="sxs-lookup"><span data-stu-id="ce770-533">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="ce770-534">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ce770-534">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="ce770-535">透過下列 Cmdlet 新增弱點評量支援：</span><span class="sxs-lookup"><span data-stu-id="ce770-535">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="ce770-536">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="ce770-536">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="ce770-537">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="ce770-537">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="ce770-538">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="ce770-538">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="ce770-539">已修正 Remove-AzureRmSqlServerFirewallRule 的範例</span><span class="sxs-lookup"><span data-stu-id="ce770-539">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="ce770-540">修正 Get-AzureSqlSyncGroupLog 中非美國文化不正確的日期時間處理方式</span><span class="sxs-lookup"><span data-stu-id="ce770-540">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="ce770-541">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="ce770-541">AzureRM.Storage</span></span>
* <span data-ttu-id="ce770-542">將 Ps1XmlAttribute 新增至 Cmdlet 輸出類型屬性</span><span class="sxs-lookup"><span data-stu-id="ce770-542">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="ce770-543">在資料表檢視中顯示 StorageAccount Cmdlet 輸出</span><span class="sxs-lookup"><span data-stu-id="ce770-543">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="ce770-544">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ce770-544">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="ce770-545">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ce770-545">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="ce770-546">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ce770-546">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="ce770-547">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="ce770-547">AzureRM.Tags</span></span>
* <span data-ttu-id="ce770-548">移除標籤 Cmdlet 說明中不正確的陳述式</span><span class="sxs-lookup"><span data-stu-id="ce770-548">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="ce770-549">6.5.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="ce770-549">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ce770-550">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ce770-550">AzureRM.Profile</span></span>
* <span data-ttu-id="ce770-551">已更新 'Get-AzureRmContextAutosaveSetting' 的說明</span><span class="sxs-lookup"><span data-stu-id="ce770-551">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="ce770-552">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="ce770-552">Azure.Storage</span></span>
* <span data-ttu-id="ce770-553">支援使用唯寫 SAS 權杖上傳 Blob 或檔案</span><span class="sxs-lookup"><span data-stu-id="ce770-553">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="ce770-554">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ce770-554">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="ce770-555">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ce770-555">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="ce770-556">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ce770-556">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="ce770-557">將必要屬性 ResourceGroupName 新增至 AS。</span><span class="sxs-lookup"><span data-stu-id="ce770-557">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="ce770-558">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="ce770-558">AzureRM.Automation</span></span>
* <span data-ttu-id="ce770-559">針對 'New-AzureRMAutomationSchedule' 更新說明和新增範例</span><span class="sxs-lookup"><span data-stu-id="ce770-559">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ce770-560">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ce770-560">AzureRM.Compute</span></span>
* <span data-ttu-id="ce770-561">將 -Tag 參數新增至 Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ce770-561">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="ce770-562">新增 'Add-AzureRmVmssExtension' 的範例</span><span class="sxs-lookup"><span data-stu-id="ce770-562">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="ce770-563">新增 'Remove-AzureRmVmssExtension' 的範例</span><span class="sxs-lookup"><span data-stu-id="ce770-563">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="ce770-564">更新 'Set-AzureRmVMAccessExtension' 的說明</span><span class="sxs-lookup"><span data-stu-id="ce770-564">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="ce770-565">針對 New-AzureRmVmss 更新 SimpleParameterSet，以將 SinglePlacementGroup 預設值設為 false，並且新增切換參數 'SinglePlacementGroup'，該參數可讓使用者在單一放置群組中建立 VMSS。</span><span class="sxs-lookup"><span data-stu-id="ce770-565">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="ce770-566">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="ce770-566">AzureRM.EventHub</span></span>
* <span data-ttu-id="ce770-567">已將唯讀屬性 'PendingReplicationOperationsCount' 新增至 PSEventHubDRConfigurationAttributes 類別，如此會在複寫進行時給予擱置複寫作業計數</span><span class="sxs-lookup"><span data-stu-id="ce770-567">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ce770-568">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ce770-568">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ce770-569">更新 Set-AzureRmKeyVaultAccessPolicy 的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="ce770-569">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="ce770-570">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ce770-570">AzureRM.LogicApp</span></span>
* <span data-ttu-id="ce770-571">已修正 New-AzureRmLogicApp 中的「無法解析參數集合」錯誤</span><span class="sxs-lookup"><span data-stu-id="ce770-571">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ce770-572">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ce770-572">AzureRM.Network</span></span>
* <span data-ttu-id="ce770-573">針對 Set/Add-AzureRmVirtualNetworkPeering 在多租用戶中的虛擬網路之間啟用對等互連</span><span class="sxs-lookup"><span data-stu-id="ce770-573">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="ce770-574">已更新應用程式閘道的下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ce770-574">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="ce770-575">New-AzureRmApplicationGateway：已新增 EnableFIPS 旗標和區域支援</span><span class="sxs-lookup"><span data-stu-id="ce770-575">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="ce770-576">New-AzureRmApplicationGatewaySku：已新增 SKU Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="ce770-576">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="ce770-577">Set-AzureRmApplicationGatewaySku：已新增 SKU Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="ce770-577">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="ce770-578">已使用最新的產生器版本重新產生 RouteTable Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ce770-578">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="ce770-579">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="ce770-579">AzureRM.Relay</span></span>
* <span data-ttu-id="ce770-580">已更新 Markdown 檔案，修正範例中的參數名稱問題</span><span class="sxs-lookup"><span data-stu-id="ce770-580">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ce770-581">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ce770-581">AzureRM.Resources</span></span>
* <span data-ttu-id="ce770-582">更新 Roleassignment 和 roledefinition Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ce770-582">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="ce770-583">移除分頁時完成的額外 roledefinition 呼叫。</span><span class="sxs-lookup"><span data-stu-id="ce770-583">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="ce770-584">修正 Get-AzureRmRoleAssignment Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ce770-584">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="ce770-585">修正 -ExpandPrincipalGroups 命令參數功能</span><span class="sxs-lookup"><span data-stu-id="ce770-585">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="ce770-586">修正 'Get-AzureRmResource' 中 '-ResourceType' 參數區分大小寫的問題</span><span class="sxs-lookup"><span data-stu-id="ce770-586">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ce770-587">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ce770-587">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ce770-588">已將 top 和 skip 參數新增至清單 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ce770-588">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="ce770-589">已將標準新增至進階命名空間移轉 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ce770-589">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="ce770-590">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="ce770-590">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="ce770-591">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="ce770-591">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="ce770-592">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="ce770-592">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="ce770-593">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="ce770-593">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="ce770-594">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="ce770-594">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="ce770-595">已將唯讀屬性 'PendingReplicationOperationsCount' 新增至 PSServiceBusDRConfigurationAttributes 類別，如此會在複寫進行時給予擱置複寫作業計數</span><span class="sxs-lookup"><span data-stu-id="ce770-595">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="ce770-596">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ce770-596">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="ce770-597">更新 'New-AzureRmServiceFabricCluster' 的範例</span><span class="sxs-lookup"><span data-stu-id="ce770-597">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ce770-598">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ce770-598">AzureRM.Sql</span></span>
* <span data-ttu-id="ce770-599">新增 Management.Sql 的新 Cmdlet，以允許客戶將 TDE 憑證新增至 SQL Server 執行個體或受控執行個體</span><span class="sxs-lookup"><span data-stu-id="ce770-599">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="ce770-600">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="ce770-600">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="ce770-601">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="ce770-601">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ce770-602">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ce770-602">AzureRM.Websites</span></span>
* <span data-ttu-id="ce770-603">`Set-AzureRmWebApp -AssignIdentity` 和 `Set-AzureRmWebAppSlot -AssignIdentity` 設為 false 時，現在也會從網站 object.Removing 預覽標記移除 Identity 屬性。</span><span class="sxs-lookup"><span data-stu-id="ce770-603">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="ce770-604">`Get-AzureRmWebAppMetrics`，`Get-AzureRmAppServicePlanMetrics` 範例已更新</span><span class="sxs-lookup"><span data-stu-id="ce770-604">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="ce770-605">`Set-AzureRmWebApp -PhpVersion` 支援有效的 PHP 版本</span><span class="sxs-lookup"><span data-stu-id="ce770-605">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="ce770-606">6.4.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="ce770-606">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ce770-607">一般</span><span class="sxs-lookup"><span data-stu-id="ce770-607">General</span></span>
* <span data-ttu-id="ce770-608">已修正大部分模組說明檔案中的 OutputType 格式</span><span class="sxs-lookup"><span data-stu-id="ce770-608">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="ce770-609">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ce770-609">AzureRM.Profile</span></span>
* <span data-ttu-id="ce770-610">Ps1Xml 屬性已新增至基本輸出類型</span><span class="sxs-lookup"><span data-stu-id="ce770-610">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ce770-611">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ce770-611">AzureRM.Compute</span></span>
* <span data-ttu-id="ce770-612">VMSS 的 IP 標記功能</span><span class="sxs-lookup"><span data-stu-id="ce770-612">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="ce770-613">已新增 'New-AzureRmVmssIpTagConfig' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ce770-613">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="ce770-614">IpTag 參數已新增至 New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="ce770-614">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="ce770-615">VMSS 的自動 OS 復原功能</span><span class="sxs-lookup"><span data-stu-id="ce770-615">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="ce770-616">DisableAutoRollback 參數已新增至 New-AzureRmVmssConfig 和 Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ce770-616">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="ce770-617">VMSS 的 OS 升級記錄功能</span><span class="sxs-lookup"><span data-stu-id="ce770-617">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="ce770-618">OSUpgradeHistory 參數已新增至 Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ce770-618">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="ce770-619">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="ce770-619">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="ce770-620">透過下列命令，新增目錄 ACL 的支援：</span><span class="sxs-lookup"><span data-stu-id="ce770-620">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="ce770-621">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ce770-621">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="ce770-622">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ce770-622">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="ce770-623">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ce770-623">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="ce770-624">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ce770-624">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="ce770-625">新增 Set-AzureRmDataLakeStoreItemAclEntry、Remove-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl 的取消支援和進度追蹤</span><span class="sxs-lookup"><span data-stu-id="ce770-625">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="ce770-626">新增 Export-AzureRmDataLakeStoreChildItemProperties 的取消支援</span><span class="sxs-lookup"><span data-stu-id="ce770-626">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="ce770-627">修正針對 Cmdlet (造成遞迴作業) 偵錯訊息進行排清</span><span class="sxs-lookup"><span data-stu-id="ce770-627">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="ce770-628">修正 DataLake Cmdlet 的測試位置</span><span class="sxs-lookup"><span data-stu-id="ce770-628">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="ce770-629">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="ce770-629">AzureRM.EventHub</span></span>
* <span data-ttu-id="ce770-630">將 Optional MaxCount 參數新增至清單作業 Cmdlet Get-AzureRmEventHub 和 Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="ce770-630">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="ce770-631">已修正 New-AzureRmEventHub Cmdlet 在建立新 EventHub 時至少需要一個參數的問題。</span><span class="sxs-lookup"><span data-stu-id="ce770-631">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="ce770-632">提供預設參數集。</span><span class="sxs-lookup"><span data-stu-id="ce770-632">Provided Default Parameter set.</span></span>
* <span data-ttu-id="ce770-633">將選擇性參數 -KeyValue 新增至 New-AzureRmEventHubKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="ce770-633">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ce770-634">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ce770-634">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ce770-635">修正 Get-AzureRmKeyVault -Tag 傳回所有資源的問題</span><span class="sxs-lookup"><span data-stu-id="ce770-635">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ce770-636">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ce770-636">AzureRM.Network</span></span>
* <span data-ttu-id="ce770-637">針對區域備援 VirtualNetworkGateways 公開新的 SKU</span><span class="sxs-lookup"><span data-stu-id="ce770-637">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="ce770-638">已透過 ARM 新增功能：ExpressRoute 合作夥伴 API 的新命令</span><span class="sxs-lookup"><span data-stu-id="ce770-638">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="ce770-639">已新增 Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ce770-639">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="ce770-640">已新增 Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ce770-640">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="ce770-641">已新增 Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="ce770-641">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="ce770-642">已新增 Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="ce770-642">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="ce770-643">已新增 Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="ce770-643">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="ce770-644">已新增 Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="ce770-644">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="ce770-645">已新增 Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="ce770-645">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="ce770-646">已新增 Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ce770-646">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="ce770-647">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="ce770-647">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="ce770-648">已新增 Get-AzureRmRecoveryServicesBackupStatus Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce770-648">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="ce770-649">此 Cmdlet 會採用虛擬機器識別碼，並且檢查虛擬機器是否受到訂用帳戶中某些保存庫的保護。</span><span class="sxs-lookup"><span data-stu-id="ce770-649">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="ce770-650">如果有此類保存庫存在，Cmdlet 會輸出保存庫詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ce770-650">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ce770-651">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ce770-651">AzureRM.Resources</span></span>
* <span data-ttu-id="ce770-652">更新 Get-AzureRmPolicyAssignment Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="ce770-652">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="ce770-653">在管理群組層級新增清單 -Scope 值的支援</span><span class="sxs-lookup"><span data-stu-id="ce770-653">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="ce770-654">在管理群組層級新增對於使用 -Scope 值擷取個別指派的支援</span><span class="sxs-lookup"><span data-stu-id="ce770-654">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="ce770-655">將 -Effective 和 -All 參數新增至 control 參數</span><span class="sxs-lookup"><span data-stu-id="ce770-655">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="ce770-656">更新 Get/New/Remove/Set-AzureRmPolicyDefinition Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ce770-656">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="ce770-657">新增 -ManagementGroupName 參數，以將作業套用至指定管理群組</span><span class="sxs-lookup"><span data-stu-id="ce770-657">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="ce770-658">新增 -SubscriptionId 參數，以將作業套用至指定訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="ce770-658">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="ce770-659">更新 Get/New/Remove/Set-AzureRmPolicySetDefinition Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ce770-659">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="ce770-660">新增 -ManagementGroupName 參數，以將作業套用至指定管理群組</span><span class="sxs-lookup"><span data-stu-id="ce770-660">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="ce770-661">新增 -SubscriptionId 參數，以將作業套用至指定訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="ce770-661">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="ce770-662">在 'New-AzureRmResourceGroupDeployment' 中使用 'TemplateParameterObject' 時，在參數中新增 KeyVault 秘密參考支援</span><span class="sxs-lookup"><span data-stu-id="ce770-662">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="ce770-663">修正針對 'New-AzureRmADAppCredential' 略過 '-EndDate' 參數的問題</span><span class="sxs-lookup"><span data-stu-id="ce770-663">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="ce770-664">修正 'Add-AzureRmADGroupMember' 使用了錯誤的 URL 提出要求的問題</span><span class="sxs-lookup"><span data-stu-id="ce770-664">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="ce770-665">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ce770-665">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ce770-666">將選擇性參數 -KeyValue 新增至 New-AzureRmServiceBusKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="ce770-666">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ce770-667">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ce770-667">AzureRM.Sql</span></span>
* <span data-ttu-id="ce770-668">在 New-AzureRmSqlDatabaseRestorePoint 說明中釐清了 SQLDW 的使用者定義還原點</span><span class="sxs-lookup"><span data-stu-id="ce770-668">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="ce770-669">已在數個 Cmdlet 中更新 -ComputeGeneration 參數的文件</span><span class="sxs-lookup"><span data-stu-id="ce770-669">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="ce770-670">6.3.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="ce770-670">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ce770-671">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ce770-671">AzureRM.Profile</span></span>
* <span data-ttu-id="ce770-672">已更新的 Enable-AzureRmContextAutoSave 錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="ce770-672">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="ce770-673">執行不包含先前內容的 'Connect-AzureRmAccount' 時，建立每個訂用帳戶的內容</span><span class="sxs-lookup"><span data-stu-id="ce770-673">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="ce770-674">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="ce770-674">Azure.Storage</span></span>
* <span data-ttu-id="ce770-675">在說明檔中新增了關於 -Permissions 參數的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="ce770-675">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ce770-676">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ce770-676">AzureRM.Compute</span></span>
* <span data-ttu-id="ce770-677">'Get-AzureRmVmDiskEncryptionStatus' 修正了沒有資料磁碟的 VM 所發生的問題</span><span class="sxs-lookup"><span data-stu-id="ce770-677">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="ce770-678">更新 Compute 用戶端程式庫版本來修正下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ce770-678">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="ce770-679">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="ce770-679">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="ce770-680">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="ce770-680">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="ce770-681">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="ce770-681">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="ce770-682">已修正下列 Cmdlet，以正確顯示「作業識別碼」和「作業狀態」：</span><span class="sxs-lookup"><span data-stu-id="ce770-682">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="ce770-683">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ce770-683">Start-AzureRmVM</span></span>
    - <span data-ttu-id="ce770-684">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ce770-684">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="ce770-685">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ce770-685">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="ce770-686">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ce770-686">Set-AzureRmVM</span></span>
    - <span data-ttu-id="ce770-687">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="ce770-687">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="ce770-688">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ce770-688">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="ce770-689">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="ce770-689">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="ce770-690">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="ce770-690">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="ce770-691">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ce770-691">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="ce770-692">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ce770-692">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="ce770-693">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ce770-693">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="ce770-694">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ce770-694">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="ce770-695">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="ce770-695">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="ce770-696">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="ce770-696">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="ce770-697">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="ce770-697">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="ce770-698">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="ce770-698">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="ce770-699">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="ce770-699">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="ce770-700">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="ce770-700">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="ce770-701">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ce770-701">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="ce770-702">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ce770-702">AzureRM.EventGrid</span></span>
* <span data-ttu-id="ce770-703">將 Update-AzureRmEventGridSubscription Cmdlet 中 SubjectBeginsWith/SubjectEndsWith 的 ValidateNotNullOrEmpty 驗證條件移除，以允許視需要將這些參數變更為空白字串。</span><span class="sxs-lookup"><span data-stu-id="ce770-703">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ce770-704">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ce770-704">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ce770-705">修正此問題：當 Get-AzureRmKeyVault -Tag 執行時，未傳回任何 Tag</span><span class="sxs-lookup"><span data-stu-id="ce770-705">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="ce770-706">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ce770-706">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="ce770-707">Policy Insights Cmdlet 的公開版本</span><span class="sxs-lookup"><span data-stu-id="ce770-707">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="ce770-708">使用 API 版本 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="ce770-708">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="ce770-709">將 PolicyDefinitionReferenceId 新增至 Get-AzureRmPolicyStateSummary 的結果中</span><span class="sxs-lookup"><span data-stu-id="ce770-709">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="ce770-710">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="ce770-710">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="ce770-711">已將 -Vault 參數新增至 RecoveryServices.Backup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce770-711">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="ce770-712">當傳遞時，這會覆寫 Set-AzureRmRecoveryServicesContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce770-712">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ce770-713">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ce770-713">AzureRM.Sql</span></span>
* <span data-ttu-id="ce770-714">說明檔中已更新的 Get-AzureRmSqlDatabaseExpanded 範例</span><span class="sxs-lookup"><span data-stu-id="ce770-714">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ce770-715">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ce770-715">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ce770-716">已更新說明檔的 Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="ce770-716">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ce770-717">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ce770-717">AzureRM.Websites</span></span>
* <span data-ttu-id="ce770-718">'Set-AzureRmWebApp' 已更新為在使用 -AssignIdentity 時不會覆寫 AppSettings</span><span class="sxs-lookup"><span data-stu-id="ce770-718">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="ce770-719">'New-AzureRmWebAppSlot' 已更新為接受 AppServicePlan 作為選擇性參數</span><span class="sxs-lookup"><span data-stu-id="ce770-719">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="ce770-720">6.2.1 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="ce770-720">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="ce770-721">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ce770-721">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="ce770-722">已更新 PSWorkspace 模型，可允許 Network 使用 type 作為參數</span><span class="sxs-lookup"><span data-stu-id="ce770-722">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="ce770-723">6.2.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="ce770-723">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ce770-724">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ce770-724">AzureRM.Profile</span></span>
* <span data-ttu-id="ce770-725">修正問題：Newtonsoft.Json 10.0.3 版未在模組匯入時載入</span><span class="sxs-lookup"><span data-stu-id="ce770-725">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ce770-726">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ce770-726">AzureRM.Compute</span></span>
* <span data-ttu-id="ce770-727">VMSS VM 更新功能</span><span class="sxs-lookup"><span data-stu-id="ce770-727">VMSS VM Update feature</span></span>
    - <span data-ttu-id="ce770-728">新增 'Update-AzureRmVmssVM' 和 'New-AzureRmVMDataDisk' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ce770-728">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="ce770-729">將 VirtualMachineScaleSetVM 參數新增至 'Add-AzureRmVMDataDisk' Cmdlet，以支援將資料磁碟新增至 Vmss VM。</span><span class="sxs-lookup"><span data-stu-id="ce770-729">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="ce770-730">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ce770-730">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="ce770-731">已將 ADF .Net SDK 更新為版本 0.8.0-preview，包含以下變更：</span><span class="sxs-lookup"><span data-stu-id="ce770-731">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="ce770-732">新增設定中心存放庫的作業</span><span class="sxs-lookup"><span data-stu-id="ce770-732">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="ce770-733">將 QuickBooks LinkedService 更新為公開 consumerKey 和 consumerSecret 屬性</span><span class="sxs-lookup"><span data-stu-id="ce770-733">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="ce770-734">更新從 SecretBase 到 Object 的數個模型類型</span><span class="sxs-lookup"><span data-stu-id="ce770-734">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="ce770-735">新增 Blob 事件觸發程序</span><span class="sxs-lookup"><span data-stu-id="ce770-735">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="ce770-736">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ce770-736">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ce770-737">更新文件和範例輸出</span><span class="sxs-lookup"><span data-stu-id="ce770-737">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="ce770-738">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ce770-738">AzureRM.Network</span></span>
* <span data-ttu-id="ce770-739">啟用網路監看員 Cmdlet 上的流量分析參數</span><span class="sxs-lookup"><span data-stu-id="ce770-739">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ce770-740">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ce770-740">AzureRM.Resources</span></span>
* <span data-ttu-id="ce770-741">針對從 'Get-AzureRmResource' 傳回的 'PSResource' 物件，修正其中的 'Properties' 屬性問題</span><span class="sxs-lookup"><span data-stu-id="ce770-741">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="ce770-742">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="ce770-742">AzureRM.Scheduler</span></span>
* <span data-ttu-id="ce770-743">修正更新 ServiceBusQueueJob 時沒有設定新驗證值的問題</span><span class="sxs-lookup"><span data-stu-id="ce770-743">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="ce770-744">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ce770-744">AzureRM.Sql</span></span>
* <span data-ttu-id="ce770-745">透過選擇性 LicenseType 參數更新下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ce770-745">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="ce770-746">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ce770-746">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="ce770-747">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ce770-747">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="ce770-748">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="ce770-748">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="ce770-749">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ce770-749">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="ce770-750">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ce770-750">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ce770-751">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ce770-751">AzureRM.Websites</span></span>
* <span data-ttu-id="ce770-752">更新 'New-AzureRMWebApp' 以使用來自策略程式庫的常見演算法。</span><span class="sxs-lookup"><span data-stu-id="ce770-752">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="ce770-753">6.1.0 - 2018 年 5 月</span><span class="sxs-lookup"><span data-stu-id="ce770-753">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ce770-754">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ce770-754">AzureRM.Profile</span></span>
* <span data-ttu-id="ce770-755">修正執行 'Clear-AzureRmContext' 會讓空白內容保留先前的預設內容名稱，導致使用者無法以舊名稱建立新內容的問題</span><span class="sxs-lookup"><span data-stu-id="ce770-755">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="ce770-756">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ce770-756">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="ce770-757">啟用 AS 上的閘道建立關聯/取消關聯作業。</span><span class="sxs-lookup"><span data-stu-id="ce770-757">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="ce770-758">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ce770-758">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="ce770-759">已新增 ApiVersions、ApiReleases 和 ApiRevisions 支援</span><span class="sxs-lookup"><span data-stu-id="ce770-759">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="ce770-760">已新增 ServiceFabric 後端支援</span><span class="sxs-lookup"><span data-stu-id="ce770-760">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="ce770-761">已新增 Application Insights 記錄器支援</span><span class="sxs-lookup"><span data-stu-id="ce770-761">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="ce770-762">已新增將 'Basic' sku 辨識為有效 sku 的 API 管理服務支援</span><span class="sxs-lookup"><span data-stu-id="ce770-762">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="ce770-763">已針對安裝由私人 CA 發出的憑證做為根或 CA 新增支援</span><span class="sxs-lookup"><span data-stu-id="ce770-763">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="ce770-764">已針對透過 KeyVault 和多個 Proxy 主機名稱接受自訂 SSL 憑證新增支援</span><span class="sxs-lookup"><span data-stu-id="ce770-764">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="ce770-765">已新增 MSI 身分識別支援</span><span class="sxs-lookup"><span data-stu-id="ce770-765">Added support for MSI identity</span></span>
* <span data-ttu-id="ce770-766">已新增透過 URL 接受原則的支援 附註：下列 Cmdlet 會在未來的版本中淘汰</span><span class="sxs-lookup"><span data-stu-id="ce770-766">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="ce770-767">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="ce770-767">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="ce770-768">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce770-768">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="ce770-769">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="ce770-769">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="ce770-770">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="ce770-770">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="ce770-771">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="ce770-771">AzureRM.Batch</span></span>
* <span data-ttu-id="ce770-772">發行新的 Cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="ce770-772">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="ce770-773">發行新的 Cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="ce770-773">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="ce770-774">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="ce770-774">AzureRM.Consumption</span></span>
* <span data-ttu-id="ce770-775">在 Cmdlet Get-AzureRmConsumptionUsageDetail 上新增新參數 Expand、ResourceGroup、InstanceName、InstanceId、Tags 和 Top</span><span class="sxs-lookup"><span data-stu-id="ce770-775">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="ce770-776">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ce770-776">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="ce770-777">針對 Export-AzureRmDataLakeStoreChildItemProperties 修正範例</span><span class="sxs-lookup"><span data-stu-id="ce770-777">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="ce770-778">修正 Set-AzureRmDataLakeStoreItemAclEntry 中 Recurse 案例的 Null 參數例外狀況</span><span class="sxs-lookup"><span data-stu-id="ce770-778">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="ce770-779">修正 Set-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl、Remove-AzureRmDataLakeStoreItemAclEntry 的說明檔</span><span class="sxs-lookup"><span data-stu-id="ce770-779">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="ce770-780">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ce770-780">AzureRM.Network</span></span>
* <span data-ttu-id="ce770-781">將網路 SDK 版本從 18.0.0-預覽提高到 19.0.0-預覽</span><span class="sxs-lookup"><span data-stu-id="ce770-781">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="ce770-782">新增 Cmdlet 來建立通訊協定設定</span><span class="sxs-lookup"><span data-stu-id="ce770-782">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="ce770-783">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce770-783">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="ce770-784">新增 Cmdlet 以將新線路連線新增至現有的快速路由線路。</span><span class="sxs-lookup"><span data-stu-id="ce770-784">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="ce770-785">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="ce770-785">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="ce770-786">新增 Cmdlet 以將線路連線從現有的快速路由線路移除。</span><span class="sxs-lookup"><span data-stu-id="ce770-786">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="ce770-787">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="ce770-787">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="ce770-788">新增 Cmdlet 來擷取線路連線</span><span class="sxs-lookup"><span data-stu-id="ce770-788">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="ce770-789">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="ce770-789">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="ce770-790">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ce770-790">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="ce770-791">固定的伺服器驗證使用方式與產生的憑證 (問題 #5998)</span><span class="sxs-lookup"><span data-stu-id="ce770-791">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ce770-792">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ce770-792">AzureRM.Sql</span></span>
* <span data-ttu-id="ce770-793">已更新稽核 Cmdlet 以允許移除 AuditActions 或 AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="ce770-793">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="ce770-794">已修正 Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy 在設定新的彈性保留原則時，命令會失敗的問題；錯誤為：使用 azure 復原服務保存庫設定長期保留原則，且不再支援原則。</span><span class="sxs-lookup"><span data-stu-id="ce770-794">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="ce770-795">請提交具有新彈性保留原則的要求。</span><span class="sxs-lookup"><span data-stu-id="ce770-795">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="ce770-796">更新所有 Azure Sql Database/ElasticPool 建立/更新相關的 Cmdlet 以使用新的資料庫 API，其可支援縮放和階層相關屬性的 Sku 屬性。</span><span class="sxs-lookup"><span data-stu-id="ce770-796">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="ce770-797">更新的 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="ce770-797">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="ce770-798">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ce770-798">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="ce770-799">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ce770-799">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="ce770-800">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="ce770-800">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="ce770-801">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ce770-801">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="ce770-802">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ce770-802">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ce770-803">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ce770-803">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ce770-804">更新 'Get-AzureRmTrafficManagerProfile' 的參數，以便在使用 -Name 參數時需要 -ResourceGroupName 參數。</span><span class="sxs-lookup"><span data-stu-id="ce770-804">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
