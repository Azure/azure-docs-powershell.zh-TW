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
ms.openlocfilehash: 3cb71087a61a0fcd06c014394e8f9e5654d4c1a8
ms.sourcegitcommit: 19dffee617477001f98d43e39a50ce1fad087b74
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/27/2018
ms.locfileid: "47178998"
---
# <a name="release-notes"></a><span data-ttu-id="1dde5-103">版本資訊</span><span class="sxs-lookup"><span data-stu-id="1dde5-103">Release notes</span></span>

<span data-ttu-id="1dde5-104">這是此版本中對 Azure PowerShell 所做的變更清單。</span><span class="sxs-lookup"><span data-stu-id="1dde5-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="690---september-2018"></a><span data-ttu-id="1dde5-105">6.9.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="1dde5-105">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="1dde5-106">一般</span><span class="sxs-lookup"><span data-stu-id="1dde5-106">General</span></span>
* <span data-ttu-id="1dde5-107">已將 AzureRM.SignalR 新增至 AzureRM 彙總模組</span><span class="sxs-lookup"><span data-stu-id="1dde5-107">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="1dde5-108">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="1dde5-108">AzureRM.Profile</span></span>
* <span data-ttu-id="1dde5-109">儲存體通用程式碼的小幅變更</span><span class="sxs-lookup"><span data-stu-id="1dde5-109">Minor changes to the storage common code</span></span>
* <span data-ttu-id="1dde5-110">已更新說明檔以包含完整的參數類型。</span><span class="sxs-lookup"><span data-stu-id="1dde5-110">Updated help files to include full parameter types.</span></span>
- <span data-ttu-id="1dde5-111">已變更 - 非強制性的 ServicePrincipal 位在 ServicePrincipalCertificateWithSubscriptionId 參數集</span><span class="sxs-lookup"><span data-stu-id="1dde5-111">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="1dde5-112">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="1dde5-112">Azure.Storage</span></span>
* <span data-ttu-id="1dde5-113">支援使用 OAuth 建立儲存體內容。</span><span class="sxs-lookup"><span data-stu-id="1dde5-113">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="1dde5-114">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="1dde5-114">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="1dde5-115">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="1dde5-115">AzureRM.Cdn</span></span>
* <span data-ttu-id="1dde5-116">已在 CDN 定價 SKU 中新增 Standard_Microsoft。</span><span class="sxs-lookup"><span data-stu-id="1dde5-116">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="1dde5-117">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="1dde5-117">AzureRM.Compute</span></span>
* <span data-ttu-id="1dde5-118">將金鑰保存庫和儲存體上的相依性移至一般相依性</span><span class="sxs-lookup"><span data-stu-id="1dde5-118">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="1dde5-119">對 AEM Cmdlet 新增更多的虛擬機器大小支援</span><span class="sxs-lookup"><span data-stu-id="1dde5-119">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="1dde5-120">將 PublicIPPrefix 參數新增至 New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="1dde5-120">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="1dde5-121">將 ResourceId 參數新增至 Invoke-AzureRmVMRunCommand Cmdelt</span><span class="sxs-lookup"><span data-stu-id="1dde5-121">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="1dde5-122">新增 Invoke-AzureRmVmssVMRunCommand Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1dde5-122">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="1dde5-123">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="1dde5-123">AzureRM.Dns</span></span>
* <span data-ttu-id="1dde5-124">已新增建立 DNS 記錄時的別名記錄支援</span><span class="sxs-lookup"><span data-stu-id="1dde5-124">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="1dde5-125">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="1dde5-125">AzureRM.Insights</span></span>
* <span data-ttu-id="1dde5-126">已修正問題 #6833 和 #7102 (診斷設定區域)</span><span class="sxs-lookup"><span data-stu-id="1dde5-126">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="1dde5-127">建立和列出/取得診斷設定時的預設名稱問題 (例如 'service')</span><span class="sxs-lookup"><span data-stu-id="1dde5-127">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="1dde5-128">以類別建立診斷設定的問題</span><span class="sxs-lookup"><span data-stu-id="1dde5-128">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="1dde5-129">已新增計量時間粒紋參數的取代訊息</span><span class="sxs-lookup"><span data-stu-id="1dde5-129">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="1dde5-130">Timegrains 參數還是可用 (這是非中斷性變更)，但會在後端中遭到忽略，因為只有 PT1M 有效</span><span class="sxs-lookup"><span data-stu-id="1dde5-130">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="1dde5-131">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="1dde5-131">AzureRM.Network</span></span>
* <span data-ttu-id="1dde5-132">LoadBalancer Cmdlet 的變更</span><span class="sxs-lookup"><span data-stu-id="1dde5-132">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="1dde5-133">LoadBalancerInboundNatPoolConfig：已新增 IdleTimeoutInMinutes、EnableFloatingIp 和 EnableTcpReset 參數</span><span class="sxs-lookup"><span data-stu-id="1dde5-133">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="1dde5-134">LoadBalancerInboundNatRuleConfig：已新增 EnableTcpReset 參數</span><span class="sxs-lookup"><span data-stu-id="1dde5-134">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="1dde5-135">LoadBalancerRuleConfig：已新增 EnableTcpReset 參數</span><span class="sxs-lookup"><span data-stu-id="1dde5-135">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="1dde5-136">LoadBalancerProbeConfig：已為 Protocol 參數新增 "Https" 值的支援</span><span class="sxs-lookup"><span data-stu-id="1dde5-136">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="1dde5-137">已為新 LoadBalancer 的子資源 OutboundRule 新增命令</span><span class="sxs-lookup"><span data-stu-id="1dde5-137">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="1dde5-138">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1dde5-138">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="1dde5-139">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1dde5-139">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="1dde5-140">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1dde5-140">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="1dde5-141">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1dde5-141">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="1dde5-142">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1dde5-142">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="1dde5-143">已為 PSNetworkInterface 新增 HostedWorkloads 屬性</span><span class="sxs-lookup"><span data-stu-id="1dde5-143">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="1dde5-144">已為以下功能新增 Cmdlet：由 ARM 支援的 Azure 防火牆</span><span class="sxs-lookup"><span data-stu-id="1dde5-144">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="1dde5-145">已新增 Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="1dde5-145">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="1dde5-146">已新增 Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="1dde5-146">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="1dde5-147">已新增 New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="1dde5-147">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="1dde5-148">已新增 Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="1dde5-148">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="1dde5-149">已新增 New-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="1dde5-149">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="1dde5-150">已新增 New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="1dde5-150">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="1dde5-151">已新增 New-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="1dde5-151">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="1dde5-152">已新增 New-AzureRmFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="1dde5-152">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="1dde5-153">已新增 New-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="1dde5-153">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="1dde5-154">已新增 New-AzureRmFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1dde5-154">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="1dde5-155">已在應用程式閘道中新增受信任根憑證和自動調整組態的支援</span><span class="sxs-lookup"><span data-stu-id="1dde5-155">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="1dde5-156">已新增的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="1dde5-156">New Cmdlets added:</span></span>
      - <span data-ttu-id="1dde5-157">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1dde5-157">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="1dde5-158">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1dde5-158">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="1dde5-159">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1dde5-159">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="1dde5-160">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1dde5-160">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="1dde5-161">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1dde5-161">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="1dde5-162">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="1dde5-162">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="1dde5-163">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="1dde5-163">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="1dde5-164">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="1dde5-164">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="1dde5-165">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="1dde5-165">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="1dde5-166">已使用選擇性參數 TrustedRootCertificate 更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1dde5-166">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="1dde5-167">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1dde5-167">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="1dde5-168">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1dde5-168">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="1dde5-169">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="1dde5-169">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="1dde5-170">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="1dde5-170">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="1dde5-171">已使用選擇性參數 AutoscaleConfiguration 更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1dde5-171">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="1dde5-172">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1dde5-172">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="1dde5-173">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1dde5-173">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="1dde5-174">為介面端點 Get-AzureInterfaceEndpoint 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1dde5-174">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="1dde5-175">已在子網路中新增多個位址前置詞的支援。</span><span class="sxs-lookup"><span data-stu-id="1dde5-175">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="1dde5-176">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="1dde5-176">Updated cmdlets:</span></span>
  - <span data-ttu-id="1dde5-177">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1dde5-177">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="1dde5-178">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1dde5-178">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="1dde5-179">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1dde5-179">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="1dde5-180">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1dde5-180">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="1dde5-181">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="1dde5-181">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="1dde5-182">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="1dde5-182">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="1dde5-183">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="1dde5-183">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="1dde5-184">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="1dde5-184">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="1dde5-185">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1dde5-185">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="1dde5-186">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1dde5-186">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="1dde5-187">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1dde5-187">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="1dde5-188">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="1dde5-188">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="1dde5-189">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="1dde5-189">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="1dde5-190">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="1dde5-190">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="1dde5-191">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="1dde5-191">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="1dde5-192">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1dde5-192">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="1dde5-193">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1dde5-193">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="1dde5-194">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1dde5-194">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="1dde5-195">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="1dde5-195">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="1dde5-196">為子網路委派新增 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1dde5-196">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="1dde5-197">New-AzureRmDelegation：建立可新增至子網路的新委派</span><span class="sxs-lookup"><span data-stu-id="1dde5-197">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="1dde5-198">Remove-AzureRmDelegation：用於子網路，可從該子網路中移除提供的委派名稱</span><span class="sxs-lookup"><span data-stu-id="1dde5-198">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="1dde5-199">Add-AzureRmDelegation：用於子網路，可將提供的服務名稱新增為該子網路的委派</span><span class="sxs-lookup"><span data-stu-id="1dde5-199">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="1dde5-200">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="1dde5-200">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="1dde5-201">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="1dde5-201">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="1dde5-202">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="1dde5-202">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="1dde5-203">支援受控磁碟</span><span class="sxs-lookup"><span data-stu-id="1dde5-203">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="1dde5-204">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="1dde5-204">AzureRM.RedisCache</span></span>
* <span data-ttu-id="1dde5-205">已更新深入解析相依性。</span><span class="sxs-lookup"><span data-stu-id="1dde5-205">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="1dde5-206">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="1dde5-206">AzureRM.Resources</span></span>
* <span data-ttu-id="1dde5-207">使用新參數 RollbackAction 更新 New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1dde5-207">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="1dde5-208">使用新參數新增 OnErrorDeployment 的支援。</span><span class="sxs-lookup"><span data-stu-id="1dde5-208">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="1dde5-209">支援原則指派上的受控識別。</span><span class="sxs-lookup"><span data-stu-id="1dde5-209">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="1dde5-210">以 'New-AzureRmPolicyAssignment' 指派原則時不再需要具有預設值的參數</span><span class="sxs-lookup"><span data-stu-id="1dde5-210">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="1dde5-211">新增 Get-AzureRmPolicyAlias Cmdlet 來擷取原則別名</span><span class="sxs-lookup"><span data-stu-id="1dde5-211">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="1dde5-212">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1dde5-212">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="1dde5-213">已修正問題 #7161</span><span class="sxs-lookup"><span data-stu-id="1dde5-213">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="1dde5-214">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="1dde5-214">AzureRM.SignalR</span></span>
* <span data-ttu-id="1dde5-215">將 SKU 名稱更新為 Free_F1 和 Standard_S1</span><span class="sxs-lookup"><span data-stu-id="1dde5-215">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="1dde5-216">將版本欄位新增至 PSSignalRResource 物件，以及將連接字串新增至 PSSignalRKeys 物件。</span><span class="sxs-lookup"><span data-stu-id="1dde5-216">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="1dde5-217">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="1dde5-217">AzureRM.Storage</span></span>
* <span data-ttu-id="1dde5-218">在 AzureRm.Storage 中支援不變原則</span><span class="sxs-lookup"><span data-stu-id="1dde5-218">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="1dde5-219">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1dde5-219">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="1dde5-220">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1dde5-220">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="1dde5-221">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1dde5-221">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="1dde5-222">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1dde5-222">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="1dde5-223">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1dde5-223">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="1dde5-224">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="1dde5-224">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="1dde5-225">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="1dde5-225">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="1dde5-226">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1dde5-226">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="1dde5-227">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1dde5-227">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="1dde5-228">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1dde5-228">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="1dde5-229">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1dde5-229">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="1dde5-230">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="1dde5-230">AzureRM.Websites</span></span>
* <span data-ttu-id="1dde5-231">已新增兩個 Cmdlet：Get-AzureRmDeletedWebApp 和 Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="1dde5-231">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="1dde5-232">New-AzureRmAppServicePlan - 已新增 HyperV 切換以使用 Windows 容器建立 App Service 方案</span><span class="sxs-lookup"><span data-stu-id="1dde5-232">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="1dde5-233">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - 已新增參數 (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) 來建立和管理 Windows 容器應用程式</span><span class="sxs-lookup"><span data-stu-id="1dde5-233">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="1dde5-234">6.8.1 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="1dde5-234">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="1dde5-235">一般</span><span class="sxs-lookup"><span data-stu-id="1dde5-235">General</span></span>
* <span data-ttu-id="1dde5-236">已修正未設定預設資源群組的問題。</span><span class="sxs-lookup"><span data-stu-id="1dde5-236">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="1dde5-237">已更新通用執行階段組件</span><span class="sxs-lookup"><span data-stu-id="1dde5-237">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="1dde5-238">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1dde5-238">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="1dde5-239">已修正未設定預設資源群組的問題。</span><span class="sxs-lookup"><span data-stu-id="1dde5-239">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="1dde5-240">已修正的問題 https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="1dde5-240">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="1dde5-241">Import-AzureRmApiManagementApi 和 \*-AzureRmApiManagementCertificate cmdlets 目前處理相對路徑</span><span class="sxs-lookup"><span data-stu-id="1dde5-241">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="1dde5-242">已修正的問題 https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="1dde5-242">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="1dde5-243">CertificateInformation 為可設定的屬性，允許 Set-AzureRmApiManagement Cmdlet 正常運作。</span><span class="sxs-lookup"><span data-stu-id="1dde5-243">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="1dde5-244">已藉由升級至 4.0.4-preview NuGet 而修正</span><span class="sxs-lookup"><span data-stu-id="1dde5-244">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="1dde5-245">已修正的問題 https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="1dde5-245">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="1dde5-246">已修正依產品名稱搜尋的 Odata 篩選條件</span><span class="sxs-lookup"><span data-stu-id="1dde5-246">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="1dde5-247">已修正的問題 https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="1dde5-247">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="1dde5-248">已修正依 API 名稱搜尋的 Odata 篩選條件</span><span class="sxs-lookup"><span data-stu-id="1dde5-248">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="1dde5-249">已新增對 AzureMonitor 記錄器的支援</span><span class="sxs-lookup"><span data-stu-id="1dde5-249">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="1dde5-250">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="1dde5-250">AzureRM.Compute</span></span>
* <span data-ttu-id="1dde5-251">已修正在錯誤輸出中遺漏目標的問題。</span><span class="sxs-lookup"><span data-stu-id="1dde5-251">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="1dde5-252">已修正搭配受控磁碟的 VM 之儲存體帳戶類型的問題</span><span class="sxs-lookup"><span data-stu-id="1dde5-252">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="1dde5-253">已修正未設定預設資源群組的問題。</span><span class="sxs-lookup"><span data-stu-id="1dde5-253">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="1dde5-254">修正適用於其他環境的 AEM 擴充 Cmdlet，例如 Azure China</span><span class="sxs-lookup"><span data-stu-id="1dde5-254">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="1dde5-255">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="1dde5-255">AzureRM.Network</span></span>
* <span data-ttu-id="1dde5-256">已將預設的 Cmdlet 輸出表示法變更為資料表檢視</span><span class="sxs-lookup"><span data-stu-id="1dde5-256">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="1dde5-257">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="1dde5-257">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="1dde5-258">修正在嘗試調整已暫停的容量時，Update-AzureRmPowerBIEmbeddedCapacity 中發生的錯誤</span><span class="sxs-lookup"><span data-stu-id="1dde5-258">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="1dde5-259">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="1dde5-259">AzureRM.Resources</span></span>
* <span data-ttu-id="1dde5-260">已修正從 MarketPlace 建立受控應用程式發生的問題。</span><span class="sxs-lookup"><span data-stu-id="1dde5-260">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="1dde5-261">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1dde5-261">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="1dde5-262">已修正的問題</span><span class="sxs-lookup"><span data-stu-id="1dde5-262">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="1dde5-263">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="1dde5-263">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="1dde5-264">已新增對 MultiValue 路由方法的支援</span><span class="sxs-lookup"><span data-stu-id="1dde5-264">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="1dde5-265">為 MultiValue 路由新增 'MaxReturn' 參數</span><span class="sxs-lookup"><span data-stu-id="1dde5-265">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="1dde5-266">已新增對子網路路由方法的支援</span><span class="sxs-lookup"><span data-stu-id="1dde5-266">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="1dde5-267">支援端點中的 IP 位址範圍 (子網路)</span><span class="sxs-lookup"><span data-stu-id="1dde5-267">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="1dde5-268">已新增對設定檔中自訂標頭的支援</span><span class="sxs-lookup"><span data-stu-id="1dde5-268">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="1dde5-269">已新增對設定檔中預期狀態碼的支援</span><span class="sxs-lookup"><span data-stu-id="1dde5-269">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="1dde5-270">已新增對端點中自訂標頭的支援</span><span class="sxs-lookup"><span data-stu-id="1dde5-270">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="1dde5-271">6.8.0 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="1dde5-271">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="1dde5-272">一般</span><span class="sxs-lookup"><span data-stu-id="1dde5-272">General</span></span>
* <span data-ttu-id="1dde5-273">已修正未設定預設資源群組的問題。</span><span class="sxs-lookup"><span data-stu-id="1dde5-273">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="1dde5-274">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="1dde5-274">AzureRM.Profile</span></span>
* <span data-ttu-id="1dde5-275">已將到期屬性新增至在 Connect-AzureRmAccount 期間傳回的權杖</span><span class="sxs-lookup"><span data-stu-id="1dde5-275">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="1dde5-276">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="1dde5-276">AzureRM.Compute</span></span>
* <span data-ttu-id="1dde5-277">已修正在錯誤輸出中遺漏目標的問題。</span><span class="sxs-lookup"><span data-stu-id="1dde5-277">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="1dde5-278">已修正搭配受控磁碟的 VM 之儲存體帳戶類型的問題</span><span class="sxs-lookup"><span data-stu-id="1dde5-278">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="1dde5-279">修正適用於其他環境的 AEM 擴充 Cmdlet，例如 Azure China</span><span class="sxs-lookup"><span data-stu-id="1dde5-279">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="1dde5-280">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="1dde5-280">AzureRM.IotHub</span></span>
* <span data-ttu-id="1dde5-281">修正 New-AzureRmIotHubExportDevices 和 New-AzureRmIotHubImportDevices 的範例</span><span class="sxs-lookup"><span data-stu-id="1dde5-281">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="1dde5-282">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="1dde5-282">AzureRM.Network</span></span>
* <span data-ttu-id="1dde5-283">已將預設模式表示法變更為資料表檢視</span><span class="sxs-lookup"><span data-stu-id="1dde5-283">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="1dde5-284">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="1dde5-284">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="1dde5-285">修正在嘗試調整已暫停的容量時，Update-AzureRmPowerBIEmbeddedCapacity 中發生的錯誤</span><span class="sxs-lookup"><span data-stu-id="1dde5-285">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="1dde5-286">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="1dde5-286">AzureRM.Resources</span></span>
* <span data-ttu-id="1dde5-287">已修正從 MarketPlace 建立受控應用程式發生的問題。</span><span class="sxs-lookup"><span data-stu-id="1dde5-287">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="1dde5-288">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1dde5-288">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="1dde5-289">修正問題</span><span class="sxs-lookup"><span data-stu-id="1dde5-289">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="1dde5-290">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="1dde5-290">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="1dde5-291">支援 MultiValue 路由方法</span><span class="sxs-lookup"><span data-stu-id="1dde5-291">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="1dde5-292">為 MultiValue 路由新增 'MaxReturn' 參數</span><span class="sxs-lookup"><span data-stu-id="1dde5-292">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="1dde5-293">支援子網路路由方法</span><span class="sxs-lookup"><span data-stu-id="1dde5-293">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="1dde5-294">支援端點中的 IP 位址範圍 (子網路)</span><span class="sxs-lookup"><span data-stu-id="1dde5-294">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="1dde5-295">支援設定檔中的自訂標頭</span><span class="sxs-lookup"><span data-stu-id="1dde5-295">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="1dde5-296">支援設定檔中的預期狀態碼</span><span class="sxs-lookup"><span data-stu-id="1dde5-296">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="1dde5-297">支援端點中的自訂標頭</span><span class="sxs-lookup"><span data-stu-id="1dde5-297">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="1dde5-298">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="1dde5-298">AzureRM.Websites</span></span>
* <span data-ttu-id="1dde5-299">已修正未正確設定預設資源群組的問題。</span><span class="sxs-lookup"><span data-stu-id="1dde5-299">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="1dde5-300">6.7.0 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="1dde5-300">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="1dde5-301">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="1dde5-301">AzureRM.Profile</span></span>
* <span data-ttu-id="1dde5-302">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-302">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="1dde5-303">將使用者識別碼新增至預設內容名稱，以避免內容發生衝突</span><span class="sxs-lookup"><span data-stu-id="1dde5-303">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="1dde5-304">修正 Clear-AzureRmContext 在選擇內容 #6398 時出現的問題</span><span class="sxs-lookup"><span data-stu-id="1dde5-304">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="1dde5-305">允許將租用戶網域傳遞給 'Connect-AzureRmAccount' 的 '-TenantId' 參數</span><span class="sxs-lookup"><span data-stu-id="1dde5-305">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="1dde5-306">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="1dde5-306">Azure.Storage</span></span>
* <span data-ttu-id="1dde5-307">移除 Azure 檔案共用 5TB 的配額限制</span><span class="sxs-lookup"><span data-stu-id="1dde5-307">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="1dde5-308">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="1dde5-308">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="1dde5-309">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1dde5-309">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="1dde5-310">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-310">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="1dde5-311">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1dde5-311">Azure.AnalysisServices</span></span>
* <span data-ttu-id="1dde5-312">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-312">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="1dde5-313">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1dde5-313">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="1dde5-314">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-314">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="1dde5-315">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="1dde5-315">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="1dde5-316">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-316">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="1dde5-317">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="1dde5-317">AzureRM.Automation</span></span>
* <span data-ttu-id="1dde5-318">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-318">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="1dde5-319">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="1dde5-319">AzureRM.Backup</span></span>
* <span data-ttu-id="1dde5-320">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-320">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="1dde5-321">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="1dde5-321">AzureRM.Batch</span></span>
* <span data-ttu-id="1dde5-322">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-322">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="1dde5-323">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="1dde5-323">AzureRM.Billing</span></span>
* <span data-ttu-id="1dde5-324">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-324">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="1dde5-325">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="1dde5-325">AzureRM.Cdn</span></span>
* <span data-ttu-id="1dde5-326">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-326">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="1dde5-327">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1dde5-327">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="1dde5-328">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-328">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="1dde5-329">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="1dde5-329">AzureRM.Compute</span></span>
* <span data-ttu-id="1dde5-330">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-330">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="1dde5-331">將 EvictionPolicy 參數新增至 New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="1dde5-331">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="1dde5-332">若未指定位置，則使用 New-AzureRmVm 的 DiskFileParameterSet 中的預設位置。</span><span class="sxs-lookup"><span data-stu-id="1dde5-332">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="1dde5-333">修正 Save-AzureRmVMImage 中的參數描述</span><span class="sxs-lookup"><span data-stu-id="1dde5-333">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="1dde5-334">修正某些單次傳遞相關案例的 Get-AzureRmVMDiskEncryptionStatus Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1dde5-334">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="1dde5-335">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="1dde5-335">AzureRM.Consumption</span></span>
* <span data-ttu-id="1dde5-336">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-336">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="1dde5-337">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="1dde5-337">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="1dde5-338">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-338">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="1dde5-339">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1dde5-339">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="1dde5-340">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-340">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="1dde5-341">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="1dde5-341">AzureRM.DataFactories</span></span>
* <span data-ttu-id="1dde5-342">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-342">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="1dde5-343">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="1dde5-343">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="1dde5-344">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-344">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="1dde5-345">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="1dde5-345">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="1dde5-346">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-346">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="1dde5-347">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1dde5-347">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="1dde5-348">修正從 PowerShell 命令列設定 DebugPreference 時的偵錯問</span><span class="sxs-lookup"><span data-stu-id="1dde5-348">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="1dde5-349">更新 Set-AzureRmDataLakeStoreItemAcl 範例</span><span class="sxs-lookup"><span data-stu-id="1dde5-349">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="1dde5-350">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-350">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="1dde5-351">更新 Set-AzureRmDataLakeStoreItemAclEntry 範例</span><span class="sxs-lookup"><span data-stu-id="1dde5-351">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="1dde5-352">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="1dde5-352">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="1dde5-353">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-353">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="1dde5-354">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="1dde5-354">AzureRM.Dns</span></span>
* <span data-ttu-id="1dde5-355">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-355">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="1dde5-356">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="1dde5-356">AzureRM.EventGrid</span></span>
* <span data-ttu-id="1dde5-357">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-357">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="1dde5-358">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="1dde5-358">AzureRM.EventHub</span></span>
* <span data-ttu-id="1dde5-359">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-359">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="1dde5-360">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="1dde5-360">AzureRM.HDInsight</span></span>
* <span data-ttu-id="1dde5-361">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-361">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="1dde5-362">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="1dde5-362">AzureRM.Insights</span></span>
* <span data-ttu-id="1dde5-363">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-363">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="1dde5-364">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="1dde5-364">AzureRM.IotHub</span></span>
* <span data-ttu-id="1dde5-365">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-365">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="1dde5-366">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1dde5-366">AzureRM.KeyVault</span></span>
* <span data-ttu-id="1dde5-367">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-367">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="1dde5-368">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="1dde5-368">AzureRM.LogicApp</span></span>
* <span data-ttu-id="1dde5-369">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-369">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="1dde5-370">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="1dde5-370">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="1dde5-371">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-371">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="1dde5-372">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="1dde5-372">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="1dde5-373">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-373">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="1dde5-374">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="1dde5-374">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="1dde5-375">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-375">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="1dde5-376">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="1dde5-376">AzureRM.Media</span></span>
* <span data-ttu-id="1dde5-377">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-377">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="1dde5-378">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="1dde5-378">AzureRM.Network</span></span>
* <span data-ttu-id="1dde5-379">已新增 Set-AzureRmLocalNetworkGateway 範例</span><span class="sxs-lookup"><span data-stu-id="1dde5-379">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="1dde5-380">已新增 Add-AzureRmVirtualNetworkGatewayIpConfig、Get-AzureRmVirtualNetworkGatewayConnectionSharedKey 和 New-AzureRmVirtualNetworkGatewayConnection 的範例和描述</span><span class="sxs-lookup"><span data-stu-id="1dde5-380">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="1dde5-381">已新增 Remove-AzureRmVirtualNetworkGatewayIpConfig 和 Reset-AzureRmVirtualNetworkGateway 的範例</span><span class="sxs-lookup"><span data-stu-id="1dde5-381">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="1dde5-382">已新增 Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey 的範例</span><span class="sxs-lookup"><span data-stu-id="1dde5-382">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="1dde5-383">已新增 Set-AzureRmVirtualNetworkGatewayConnectionSharedKey 的範例</span><span class="sxs-lookup"><span data-stu-id="1dde5-383">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="1dde5-384">已新增 Set-AzureRmVirtualNetworkGatewayConnection 的範例</span><span class="sxs-lookup"><span data-stu-id="1dde5-384">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="1dde5-385">已使用最新的程式碼產生器重新產生 ApplicationSecurityGroup、RouteTable 和 Usage</span><span class="sxs-lookup"><span data-stu-id="1dde5-385">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="1dde5-386">已釐清在嘗試取得未結束的子網路時，Get-AzureRmVirtualNetworkSubnetConfig 出現的錯誤</span><span class="sxs-lookup"><span data-stu-id="1dde5-386">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="1dde5-387">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="1dde5-387">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="1dde5-388">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-388">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="1dde5-389">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1dde5-389">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="1dde5-390">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-390">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="1dde5-391">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="1dde5-391">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="1dde5-392">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-392">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="1dde5-393">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="1dde5-393">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="1dde5-394">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-394">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="1dde5-395">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1dde5-395">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="1dde5-396">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-396">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="1dde5-397">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="1dde5-397">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="1dde5-398">已將原則篩選條件新增至 Get-AzureRmRecoveryServicesBackItem Xmdlet。</span><span class="sxs-lookup"><span data-stu-id="1dde5-398">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="1dde5-399">命令會傳回受指定原則識別碼保護的備份項目清單。</span><span class="sxs-lookup"><span data-stu-id="1dde5-399">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="1dde5-400">已將 Microsoft.Azure.Management.RecoveryServices.Backup 更新為版本 3.0.0-preview。</span><span class="sxs-lookup"><span data-stu-id="1dde5-400">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="1dde5-401">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-401">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="1dde5-402">已將 TargetResourceGroupName 參數新增至 Restore-AzureRmRecoveryServicesBackupItem。</span><span class="sxs-lookup"><span data-stu-id="1dde5-402">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="1dde5-403">受控磁碟還原的資源群組。</span><span class="sxs-lookup"><span data-stu-id="1dde5-403">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="1dde5-404">適用於具有受控磁碟的 VM 備份。</span><span class="sxs-lookup"><span data-stu-id="1dde5-404">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="1dde5-405">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="1dde5-405">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="1dde5-406">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-406">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="1dde5-407">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="1dde5-407">AzureRM.RedisCache</span></span>
* <span data-ttu-id="1dde5-408">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-408">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="1dde5-409">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="1dde5-409">AzureRM.Relay</span></span>
* <span data-ttu-id="1dde5-410">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-410">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="1dde5-411">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="1dde5-411">AzureRM.Resources</span></span>
* <span data-ttu-id="1dde5-412">支援在訂用帳戶範圍部署範本。</span><span class="sxs-lookup"><span data-stu-id="1dde5-412">Support template deployment at subscription scope.</span></span> <span data-ttu-id="1dde5-413">新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="1dde5-413">Add new Cmdlets:</span></span>
    - <span data-ttu-id="1dde5-414">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="1dde5-414">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="1dde5-415">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="1dde5-415">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="1dde5-416">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="1dde5-416">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="1dde5-417">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="1dde5-417">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="1dde5-418">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="1dde5-418">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="1dde5-419">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="1dde5-419">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="1dde5-420">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="1dde5-420">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="1dde5-421">修正在將內容傳遞至 Set-AzureRmResource 時擲回錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="1dde5-421">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="1dde5-422">修正 New-AzureRmResourceGroupDeployment 中的範例</span><span class="sxs-lookup"><span data-stu-id="1dde5-422">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="1dde5-423">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-423">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="1dde5-424">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="1dde5-424">AzureRM.Scheduler</span></span>
* <span data-ttu-id="1dde5-425">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-425">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="1dde5-426">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1dde5-426">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="1dde5-427">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-427">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="1dde5-428">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1dde5-428">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="1dde5-429">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-429">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="1dde5-430">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="1dde5-430">AzureRM.Sql</span></span>
* <span data-ttu-id="1dde5-431">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-431">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="1dde5-432">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="1dde5-432">AzureRM.Storage</span></span>
* <span data-ttu-id="1dde5-433">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-433">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="1dde5-434">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="1dde5-434">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="1dde5-435">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-435">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="1dde5-436">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="1dde5-436">AzureRM.Tags</span></span>
* <span data-ttu-id="1dde5-437">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-437">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="1dde5-438">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="1dde5-438">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="1dde5-439">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-439">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="1dde5-440">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="1dde5-440">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="1dde5-441">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-441">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="1dde5-442">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="1dde5-442">AzureRM.Websites</span></span>
* <span data-ttu-id="1dde5-443">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="1dde5-443">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="1dde5-444">6.6.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="1dde5-444">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="1dde5-445">一般</span><span class="sxs-lookup"><span data-stu-id="1dde5-445">General</span></span>
* <span data-ttu-id="1dde5-446">已更新所有說明檔以包含完整的參數類型和正確的輸入/輸出類型。</span><span class="sxs-lookup"><span data-stu-id="1dde5-446">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="1dde5-447">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="1dde5-447">AzureRM.Profile</span></span>
* <span data-ttu-id="1dde5-448">已更新 Common.Strategy 程式庫，以便能驗證資源目前的設定與目標資源相容。</span><span class="sxs-lookup"><span data-stu-id="1dde5-448">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="1dde5-449">已將 ps1xml 類型新增至 Common.Storage</span><span class="sxs-lookup"><span data-stu-id="1dde5-449">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="1dde5-450">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="1dde5-450">Azure.Storage</span></span>
* <span data-ttu-id="1dde5-451">已新增從 DefaultProfile 取得儲存體內容的支援</span><span class="sxs-lookup"><span data-stu-id="1dde5-451">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="1dde5-452">已將 Ps1XmlAttribute 新增至 Cmdlet 輸出類型屬性。</span><span class="sxs-lookup"><span data-stu-id="1dde5-452">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="1dde5-453">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1dde5-453">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="1dde5-454">已修正的問題 https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="1dde5-454">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="1dde5-455">已修正 Automapper 中的錯誤，以將 PsApiManagementApi 轉譯為 ApiContract</span><span class="sxs-lookup"><span data-stu-id="1dde5-455">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="1dde5-456">已修正的問題 https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="1dde5-456">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="1dde5-457">已修正 File.Save 中的錯誤，不多載編碼類型</span><span class="sxs-lookup"><span data-stu-id="1dde5-457">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="1dde5-458">已修正的問題 https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="1dde5-458">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="1dde5-459">已升級至 4.0.3 Nuget 版本，其修正了 apiId 的模式例外狀況</span><span class="sxs-lookup"><span data-stu-id="1dde5-459">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="1dde5-460">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="1dde5-460">AzureRM.Compute</span></span>
* <span data-ttu-id="1dde5-461">修正因為重新命名 PremiumLRS 儲存體帳戶類型，而在 New-AzureRmVm 中使用 DiskFileParameterSet 建立 VM 失敗的問題。</span><span class="sxs-lookup"><span data-stu-id="1dde5-461">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="1dde5-462">修正 Invoke-AzureRmVMRunCommand Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1dde5-462">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="1dde5-463">更新 Get-AzureRmAvailabilitySet，以列出訂用帳戶中所有可用性設定組。</span><span class="sxs-lookup"><span data-stu-id="1dde5-463">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="1dde5-464">(ResouceGroupName 參數現在為選用。)</span><span class="sxs-lookup"><span data-stu-id="1dde5-464">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="1dde5-465">更新 'New-AzureRmVm' 的 SimpleParameterSet，以在符合資格的 VM 上啟用加速網路。</span><span class="sxs-lookup"><span data-stu-id="1dde5-465">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="1dde5-466">更新 New-AzureRmVmss 簡單參數集，讓使用者指定的 LB 已存在時 vmss 建立會失敗。</span><span class="sxs-lookup"><span data-stu-id="1dde5-466">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="1dde5-467">更新 New-AzureRmDisk 的範例</span><span class="sxs-lookup"><span data-stu-id="1dde5-467">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="1dde5-468">新增 'New-AzureRmVM' 的範例</span><span class="sxs-lookup"><span data-stu-id="1dde5-468">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="1dde5-469">更新 Set-AzureRmVMOSDisk 的說明</span><span class="sxs-lookup"><span data-stu-id="1dde5-469">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="1dde5-470">更新 Set-AzureRmVMBginfoExtension 的範例 1 以更正拼字和前置詞。</span><span class="sxs-lookup"><span data-stu-id="1dde5-470">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="1dde5-471">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="1dde5-471">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="1dde5-472">已將 ADF .Net SDK 版本更新為 1.1.0。</span><span class="sxs-lookup"><span data-stu-id="1dde5-472">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="1dde5-473">支援跨資料處理站的自我裝載整合執行階段共用。</span><span class="sxs-lookup"><span data-stu-id="1dde5-473">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="1dde5-474">新增新參數 -SharedIntegrationRuntimeResourceId 至 Set-AzureRmDataFactoryV2IntegrationRuntime Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1dde5-474">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="1dde5-475">將新的選用參數 -LinkedDataFactoryName 新增至 Remove-AzureRmDataFactoryV2IntegrationRuntime Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1dde5-475">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="1dde5-476">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1dde5-476">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="1dde5-477">已將 DataPlane SDK (Microsoft.Azure.DataLake.Store) 版本更新為 1.1.9</span><span class="sxs-lookup"><span data-stu-id="1dde5-477">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="1dde5-478">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="1dde5-478">AzureRM.EventHub</span></span>
* <span data-ttu-id="1dde5-479">已在移除 Cmdlet 中更新了 InputObject 和 ResourceId 的管線</span><span class="sxs-lookup"><span data-stu-id="1dde5-479">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="1dde5-480">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="1dde5-480">AzureRM.Insights</span></span>
* <span data-ttu-id="1dde5-481">已修正說明檔案中的 OutputType 格式</span><span class="sxs-lookup"><span data-stu-id="1dde5-481">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="1dde5-482">使用 Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="1dde5-482">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="1dde5-483">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1dde5-483">AzureRM.KeyVault</span></span>
* <span data-ttu-id="1dde5-484">修正 Set-AzureRmKeyVaultAccessPolicy 中的管線問題</span><span class="sxs-lookup"><span data-stu-id="1dde5-484">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="1dde5-485">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="1dde5-485">AzureRM.Network</span></span>
* <span data-ttu-id="1dde5-486">已新增 LoadBalancerInboundNatPoolConfig Cmdlet 的範例。</span><span class="sxs-lookup"><span data-stu-id="1dde5-486">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="1dde5-487">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="1dde5-487">AzureRM.Resources</span></span>
* <span data-ttu-id="1dde5-488">修正在提供 'Get-AzureRmResource' 標籤名稱和值時發生的問題</span><span class="sxs-lookup"><span data-stu-id="1dde5-488">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="1dde5-489">修正 'Set-AzureRmResource' 的管線狀況</span><span class="sxs-lookup"><span data-stu-id="1dde5-489">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="1dde5-490">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1dde5-490">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="1dde5-491">已在移除 Cmdlet 中更新了 InputObject 和 ResourceId 的管線</span><span class="sxs-lookup"><span data-stu-id="1dde5-491">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="1dde5-492">已修正一些問題</span><span class="sxs-lookup"><span data-stu-id="1dde5-492">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="1dde5-493">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="1dde5-493">AzureRM.Sql</span></span>
* <span data-ttu-id="1dde5-494">透過下列 Cmdlet 新增伺服器進階威脅防護支援：</span><span class="sxs-lookup"><span data-stu-id="1dde5-494">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="1dde5-495">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1dde5-495">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="1dde5-496">透過下列 Cmdlet 新增弱點評量支援：</span><span class="sxs-lookup"><span data-stu-id="1dde5-496">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="1dde5-497">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="1dde5-497">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="1dde5-498">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="1dde5-498">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="1dde5-499">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="1dde5-499">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="1dde5-500">已修正 Remove-AzureRmSqlServerFirewallRule 的範例</span><span class="sxs-lookup"><span data-stu-id="1dde5-500">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="1dde5-501">修正 Get-AzureSqlSyncGroupLog 中非美國文化不正確的日期時間處理方式</span><span class="sxs-lookup"><span data-stu-id="1dde5-501">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="1dde5-502">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="1dde5-502">AzureRM.Storage</span></span>
* <span data-ttu-id="1dde5-503">將 Ps1XmlAttribute 新增至 Cmdlet 輸出類型屬性</span><span class="sxs-lookup"><span data-stu-id="1dde5-503">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="1dde5-504">在資料表檢視中顯示 StorageAccount Cmdlet 輸出</span><span class="sxs-lookup"><span data-stu-id="1dde5-504">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="1dde5-505">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1dde5-505">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="1dde5-506">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1dde5-506">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="1dde5-507">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1dde5-507">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="1dde5-508">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="1dde5-508">AzureRM.Tags</span></span>
* <span data-ttu-id="1dde5-509">移除標籤 Cmdlet 說明中不正確的陳述式</span><span class="sxs-lookup"><span data-stu-id="1dde5-509">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="1dde5-510">6.5.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="1dde5-510">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="1dde5-511">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="1dde5-511">AzureRM.Profile</span></span>
* <span data-ttu-id="1dde5-512">已更新 'Get-AzureRmContextAutosaveSetting' 的說明</span><span class="sxs-lookup"><span data-stu-id="1dde5-512">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="1dde5-513">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="1dde5-513">Azure.Storage</span></span>
* <span data-ttu-id="1dde5-514">支援使用唯寫 SAS 權杖上傳 Blob 或檔案</span><span class="sxs-lookup"><span data-stu-id="1dde5-514">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="1dde5-515">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="1dde5-515">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="1dde5-516">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="1dde5-516">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="1dde5-517">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1dde5-517">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="1dde5-518">將必要屬性 ResourceGroupName 新增至 AS。</span><span class="sxs-lookup"><span data-stu-id="1dde5-518">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="1dde5-519">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="1dde5-519">AzureRM.Automation</span></span>
* <span data-ttu-id="1dde5-520">針對 'New-AzureRMAutomationSchedule' 更新說明和新增範例</span><span class="sxs-lookup"><span data-stu-id="1dde5-520">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="1dde5-521">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="1dde5-521">AzureRM.Compute</span></span>
* <span data-ttu-id="1dde5-522">將 -Tag 參數新增至 Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1dde5-522">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="1dde5-523">新增 'Add-AzureRmVmssExtension' 的範例</span><span class="sxs-lookup"><span data-stu-id="1dde5-523">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="1dde5-524">新增 'Remove-AzureRmVmssExtension' 的範例</span><span class="sxs-lookup"><span data-stu-id="1dde5-524">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="1dde5-525">更新 'Set-AzureRmVMAccessExtension' 的說明</span><span class="sxs-lookup"><span data-stu-id="1dde5-525">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="1dde5-526">針對 New-AzureRmVmss 更新 SimpleParameterSet，以將 SinglePlacementGroup 預設值設為 false，並且新增切換參數 'SinglePlacementGroup'，該參數可讓使用者在單一放置群組中建立 VMSS。</span><span class="sxs-lookup"><span data-stu-id="1dde5-526">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="1dde5-527">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="1dde5-527">AzureRM.EventHub</span></span>
* <span data-ttu-id="1dde5-528">已將唯讀屬性 'PendingReplicationOperationsCount' 新增至 PSEventHubDRConfigurationAttributes 類別，如此會在複寫進行時給予擱置複寫作業計數</span><span class="sxs-lookup"><span data-stu-id="1dde5-528">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="1dde5-529">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1dde5-529">AzureRM.KeyVault</span></span>
* <span data-ttu-id="1dde5-530">更新 Set-AzureRmKeyVaultAccessPolicy 的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="1dde5-530">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="1dde5-531">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="1dde5-531">AzureRM.LogicApp</span></span>
* <span data-ttu-id="1dde5-532">已修正 New-AzureRmLogicApp 中的「無法解析參數集合」錯誤</span><span class="sxs-lookup"><span data-stu-id="1dde5-532">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="1dde5-533">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="1dde5-533">AzureRM.Network</span></span>
* <span data-ttu-id="1dde5-534">針對 Set/Add-AzureRmVirtualNetworkPeering 在多租用戶中的虛擬網路之間啟用對等互連</span><span class="sxs-lookup"><span data-stu-id="1dde5-534">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="1dde5-535">已更新應用程式閘道的下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1dde5-535">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="1dde5-536">New-AzureRmApplicationGateway：已新增 EnableFIPS 旗標和區域支援</span><span class="sxs-lookup"><span data-stu-id="1dde5-536">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="1dde5-537">New-AzureRmApplicationGatewaySku：已新增 SKU Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="1dde5-537">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="1dde5-538">Set-AzureRmApplicationGatewaySku：已新增 SKU Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="1dde5-538">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="1dde5-539">已使用最新的產生器版本重新產生 RouteTable Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1dde5-539">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="1dde5-540">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="1dde5-540">AzureRM.Relay</span></span>
* <span data-ttu-id="1dde5-541">已更新 Markdown 檔案，修正範例中的參數名稱問題</span><span class="sxs-lookup"><span data-stu-id="1dde5-541">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="1dde5-542">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="1dde5-542">AzureRM.Resources</span></span>
* <span data-ttu-id="1dde5-543">更新 Roleassignment 和 roledefinition Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="1dde5-543">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="1dde5-544">移除分頁時完成的額外 roledefinition 呼叫。</span><span class="sxs-lookup"><span data-stu-id="1dde5-544">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="1dde5-545">修正 Get-AzureRmRoleAssignment Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1dde5-545">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="1dde5-546">修正 -ExpandPrincipalGroups 命令參數功能</span><span class="sxs-lookup"><span data-stu-id="1dde5-546">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="1dde5-547">修正 'Get-AzureRmResource' 中 '-ResourceType' 參數區分大小寫的問題</span><span class="sxs-lookup"><span data-stu-id="1dde5-547">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="1dde5-548">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1dde5-548">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="1dde5-549">已將 top 和 skip 參數新增至清單 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1dde5-549">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="1dde5-550">已將標準新增至進階命名空間移轉 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="1dde5-550">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="1dde5-551">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="1dde5-551">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="1dde5-552">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="1dde5-552">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="1dde5-553">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="1dde5-553">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="1dde5-554">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="1dde5-554">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="1dde5-555">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="1dde5-555">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="1dde5-556">已將唯讀屬性 'PendingReplicationOperationsCount' 新增至 PSServiceBusDRConfigurationAttributes 類別，如此會在複寫進行時給予擱置複寫作業計數</span><span class="sxs-lookup"><span data-stu-id="1dde5-556">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="1dde5-557">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1dde5-557">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="1dde5-558">更新 'New-AzureRmServiceFabricCluster' 的範例</span><span class="sxs-lookup"><span data-stu-id="1dde5-558">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="1dde5-559">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="1dde5-559">AzureRM.Sql</span></span>
* <span data-ttu-id="1dde5-560">新增 Management.Sql 的新 Cmdlet，以允許客戶將 TDE 憑證新增至 SQL Server 執行個體或受控執行個體</span><span class="sxs-lookup"><span data-stu-id="1dde5-560">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="1dde5-561">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="1dde5-561">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="1dde5-562">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="1dde5-562">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="1dde5-563">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="1dde5-563">AzureRM.Websites</span></span>
* <span data-ttu-id="1dde5-564">`Set-AzureRmWebApp -AssignIdentity` 和 `Set-AzureRmWebAppSlot -AssignIdentity` 設為 false 時，現在也會從網站 object.Removing 預覽標記移除 Identity 屬性。</span><span class="sxs-lookup"><span data-stu-id="1dde5-564">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="1dde5-565">`Get-AzureRmWebAppMetrics`，`Get-AzureRmAppServicePlanMetrics` 範例已更新</span><span class="sxs-lookup"><span data-stu-id="1dde5-565">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="1dde5-566">`Set-AzureRmWebApp -PhpVersion` 支援有效的 PHP 版本</span><span class="sxs-lookup"><span data-stu-id="1dde5-566">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="1dde5-567">6.4.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="1dde5-567">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="1dde5-568">一般</span><span class="sxs-lookup"><span data-stu-id="1dde5-568">General</span></span>
* <span data-ttu-id="1dde5-569">已修正大部分模組說明檔案中的 OutputType 格式</span><span class="sxs-lookup"><span data-stu-id="1dde5-569">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="1dde5-570">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="1dde5-570">AzureRM.Profile</span></span>
* <span data-ttu-id="1dde5-571">Ps1Xml 屬性已新增至基本輸出類型</span><span class="sxs-lookup"><span data-stu-id="1dde5-571">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="1dde5-572">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="1dde5-572">AzureRM.Compute</span></span>
* <span data-ttu-id="1dde5-573">VMSS 的 IP 標記功能</span><span class="sxs-lookup"><span data-stu-id="1dde5-573">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="1dde5-574">已新增 'New-AzureRmVmssIpTagConfig' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1dde5-574">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="1dde5-575">IpTag 參數已新增至 New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="1dde5-575">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="1dde5-576">VMSS 的自動 OS 復原功能</span><span class="sxs-lookup"><span data-stu-id="1dde5-576">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="1dde5-577">DisableAutoRollback 參數已新增至 New-AzureRmVmssConfig 和 Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1dde5-577">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="1dde5-578">VMSS 的 OS 升級記錄功能</span><span class="sxs-lookup"><span data-stu-id="1dde5-578">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="1dde5-579">OSUpgradeHistory 參數已新增至 Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1dde5-579">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="1dde5-580">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="1dde5-580">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="1dde5-581">透過下列命令，新增目錄 ACL 的支援：</span><span class="sxs-lookup"><span data-stu-id="1dde5-581">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="1dde5-582">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="1dde5-582">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="1dde5-583">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="1dde5-583">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="1dde5-584">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="1dde5-584">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="1dde5-585">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1dde5-585">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="1dde5-586">新增 Set-AzureRmDataLakeStoreItemAclEntry、Remove-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl 的取消支援和進度追蹤</span><span class="sxs-lookup"><span data-stu-id="1dde5-586">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="1dde5-587">新增 Export-AzureRmDataLakeStoreChildItemProperties 的取消支援</span><span class="sxs-lookup"><span data-stu-id="1dde5-587">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="1dde5-588">修正針對 Cmdlet (造成遞迴作業) 偵錯訊息進行排清</span><span class="sxs-lookup"><span data-stu-id="1dde5-588">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="1dde5-589">修正 DataLake Cmdlet 的測試位置</span><span class="sxs-lookup"><span data-stu-id="1dde5-589">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="1dde5-590">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="1dde5-590">AzureRM.EventHub</span></span>
* <span data-ttu-id="1dde5-591">將 Optional MaxCount 參數新增至清單作業 Cmdlet Get-AzureRmEventHub 和 Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="1dde5-591">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="1dde5-592">已修正 New-AzureRmEventHub Cmdlet 在建立新 EventHub 時至少需要一個參數的問題。</span><span class="sxs-lookup"><span data-stu-id="1dde5-592">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="1dde5-593">提供預設參數集。</span><span class="sxs-lookup"><span data-stu-id="1dde5-593">Provided Default Parameter set.</span></span>
* <span data-ttu-id="1dde5-594">將選擇性參數 -KeyValue 新增至 New-AzureRmEventHubKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="1dde5-594">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="1dde5-595">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1dde5-595">AzureRM.KeyVault</span></span>
* <span data-ttu-id="1dde5-596">修正 Get-AzureRmKeyVault -Tag 傳回所有資源的問題</span><span class="sxs-lookup"><span data-stu-id="1dde5-596">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="1dde5-597">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="1dde5-597">AzureRM.Network</span></span>
* <span data-ttu-id="1dde5-598">針對區域備援 VirtualNetworkGateways 公開新的 SKU</span><span class="sxs-lookup"><span data-stu-id="1dde5-598">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="1dde5-599">已透過 ARM 新增功能：ExpressRoute 合作夥伴 API 的新命令</span><span class="sxs-lookup"><span data-stu-id="1dde5-599">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="1dde5-600">已新增 Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="1dde5-600">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="1dde5-601">已新增 Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="1dde5-601">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="1dde5-602">已新增 Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="1dde5-602">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="1dde5-603">已新增 Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="1dde5-603">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="1dde5-604">已新增 Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="1dde5-604">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="1dde5-605">已新增 Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="1dde5-605">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="1dde5-606">已新增 Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="1dde5-606">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="1dde5-607">已新增 Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="1dde5-607">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="1dde5-608">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="1dde5-608">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="1dde5-609">已新增 Get-AzureRmRecoveryServicesBackupStatus Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1dde5-609">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="1dde5-610">此 Cmdlet 會採用虛擬機器識別碼，並且檢查虛擬機器是否受到訂用帳戶中某些保存庫的保護。</span><span class="sxs-lookup"><span data-stu-id="1dde5-610">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="1dde5-611">如果有此類保存庫存在，Cmdlet 會輸出保存庫詳細資料。</span><span class="sxs-lookup"><span data-stu-id="1dde5-611">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="1dde5-612">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="1dde5-612">AzureRM.Resources</span></span>
* <span data-ttu-id="1dde5-613">更新 Get-AzureRmPolicyAssignment Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="1dde5-613">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="1dde5-614">在管理群組層級新增清單 -Scope 值的支援</span><span class="sxs-lookup"><span data-stu-id="1dde5-614">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="1dde5-615">在管理群組層級新增對於使用 -Scope 值擷取個別指派的支援</span><span class="sxs-lookup"><span data-stu-id="1dde5-615">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="1dde5-616">將 -Effective 和 -All 參數新增至 control 參數</span><span class="sxs-lookup"><span data-stu-id="1dde5-616">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="1dde5-617">更新 Get/New/Remove/Set-AzureRmPolicyDefinition Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1dde5-617">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="1dde5-618">新增 -ManagementGroupName 參數，以將作業套用至指定管理群組</span><span class="sxs-lookup"><span data-stu-id="1dde5-618">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="1dde5-619">新增 -SubscriptionId 參數，以將作業套用至指定訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="1dde5-619">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="1dde5-620">更新 Get/New/Remove/Set-AzureRmPolicySetDefinition Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1dde5-620">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="1dde5-621">新增 -ManagementGroupName 參數，以將作業套用至指定管理群組</span><span class="sxs-lookup"><span data-stu-id="1dde5-621">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="1dde5-622">新增 -SubscriptionId 參數，以將作業套用至指定訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="1dde5-622">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="1dde5-623">在 'New-AzureRmResourceGroupDeployment' 中使用 'TemplateParameterObject' 時，在參數中新增 KeyVault 秘密參考支援</span><span class="sxs-lookup"><span data-stu-id="1dde5-623">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="1dde5-624">修正針對 'New-AzureRmADAppCredential' 略過 '-EndDate' 參數的問題</span><span class="sxs-lookup"><span data-stu-id="1dde5-624">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="1dde5-625">修正 'Add-AzureRmADGroupMember' 使用了錯誤的 URL 提出要求的問題</span><span class="sxs-lookup"><span data-stu-id="1dde5-625">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="1dde5-626">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1dde5-626">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="1dde5-627">將選擇性參數 -KeyValue 新增至 New-AzureRmServiceBusKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="1dde5-627">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="1dde5-628">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="1dde5-628">AzureRM.Sql</span></span>
* <span data-ttu-id="1dde5-629">在 New-AzureRmSqlDatabaseRestorePoint 說明中釐清了 SQLDW 的使用者定義還原點</span><span class="sxs-lookup"><span data-stu-id="1dde5-629">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="1dde5-630">已在數個 Cmdlet 中更新 -ComputeGeneration 參數的文件</span><span class="sxs-lookup"><span data-stu-id="1dde5-630">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="1dde5-631">6.3.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="1dde5-631">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="1dde5-632">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="1dde5-632">AzureRM.Profile</span></span>
* <span data-ttu-id="1dde5-633">已更新的 Enable-AzureRmContextAutoSave 錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="1dde5-633">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="1dde5-634">執行不包含先前內容的 'Connect-AzureRmAccount' 時，建立每個訂用帳戶的內容</span><span class="sxs-lookup"><span data-stu-id="1dde5-634">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="1dde5-635">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="1dde5-635">Azure.Storage</span></span>
* <span data-ttu-id="1dde5-636">在說明檔中新增了關於 -Permissions 參數的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="1dde5-636">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="1dde5-637">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="1dde5-637">AzureRM.Compute</span></span>
* <span data-ttu-id="1dde5-638">'Get-AzureRmVmDiskEncryptionStatus' 修正了沒有資料磁碟的 VM 所發生的問題</span><span class="sxs-lookup"><span data-stu-id="1dde5-638">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="1dde5-639">更新 Compute 用戶端程式庫版本來修正下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1dde5-639">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="1dde5-640">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="1dde5-640">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="1dde5-641">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="1dde5-641">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="1dde5-642">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="1dde5-642">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="1dde5-643">已修正下列 Cmdlet，以正確顯示「作業識別碼」和「作業狀態」：</span><span class="sxs-lookup"><span data-stu-id="1dde5-643">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="1dde5-644">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="1dde5-644">Start-AzureRmVM</span></span>
    - <span data-ttu-id="1dde5-645">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="1dde5-645">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="1dde5-646">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="1dde5-646">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="1dde5-647">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="1dde5-647">Set-AzureRmVM</span></span>
    - <span data-ttu-id="1dde5-648">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="1dde5-648">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="1dde5-649">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1dde5-649">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="1dde5-650">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="1dde5-650">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="1dde5-651">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="1dde5-651">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="1dde5-652">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1dde5-652">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="1dde5-653">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1dde5-653">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="1dde5-654">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1dde5-654">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="1dde5-655">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1dde5-655">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="1dde5-656">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="1dde5-656">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="1dde5-657">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="1dde5-657">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="1dde5-658">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="1dde5-658">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="1dde5-659">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="1dde5-659">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="1dde5-660">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="1dde5-660">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="1dde5-661">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="1dde5-661">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="1dde5-662">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1dde5-662">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="1dde5-663">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="1dde5-663">AzureRM.EventGrid</span></span>
* <span data-ttu-id="1dde5-664">將 Update-AzureRmEventGridSubscription Cmdlet 中 SubjectBeginsWith/SubjectEndsWith 的 ValidateNotNullOrEmpty 驗證條件移除，以允許視需要將這些參數變更為空白字串。</span><span class="sxs-lookup"><span data-stu-id="1dde5-664">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="1dde5-665">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1dde5-665">AzureRM.KeyVault</span></span>
* <span data-ttu-id="1dde5-666">修正此問題：當 Get-AzureRmKeyVault -Tag 執行時，未傳回任何 Tag</span><span class="sxs-lookup"><span data-stu-id="1dde5-666">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="1dde5-667">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="1dde5-667">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="1dde5-668">Policy Insights Cmdlet 的公開版本</span><span class="sxs-lookup"><span data-stu-id="1dde5-668">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="1dde5-669">使用 API 版本 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="1dde5-669">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="1dde5-670">將 PolicyDefinitionReferenceId 新增至 Get-AzureRmPolicyStateSummary 的結果中</span><span class="sxs-lookup"><span data-stu-id="1dde5-670">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="1dde5-671">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="1dde5-671">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="1dde5-672">已將 -Vault 參數新增至 RecoveryServices.Backup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1dde5-672">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="1dde5-673">當傳遞時，這會覆寫 Set-AzureRmRecoveryServicesContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1dde5-673">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="1dde5-674">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="1dde5-674">AzureRM.Sql</span></span>
* <span data-ttu-id="1dde5-675">說明檔中已更新的 Get-AzureRmSqlDatabaseExpanded 範例</span><span class="sxs-lookup"><span data-stu-id="1dde5-675">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="1dde5-676">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="1dde5-676">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="1dde5-677">已更新說明檔的 Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="1dde5-677">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="1dde5-678">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="1dde5-678">AzureRM.Websites</span></span>
* <span data-ttu-id="1dde5-679">'Set-AzureRmWebApp' 已更新為在使用 -AssignIdentity 時不會覆寫 AppSettings</span><span class="sxs-lookup"><span data-stu-id="1dde5-679">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="1dde5-680">'New-AzureRmWebAppSlot' 已更新為接受 AppServicePlan 作為選擇性參數</span><span class="sxs-lookup"><span data-stu-id="1dde5-680">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="1dde5-681">6.2.1 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="1dde5-681">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="1dde5-682">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1dde5-682">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="1dde5-683">已更新 PSWorkspace 模型，可允許 Network 使用 type 作為參數</span><span class="sxs-lookup"><span data-stu-id="1dde5-683">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="1dde5-684">6.2.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="1dde5-684">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="1dde5-685">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="1dde5-685">AzureRM.Profile</span></span>
* <span data-ttu-id="1dde5-686">修正問題：Newtonsoft.Json 10.0.3 版未在模組匯入時載入</span><span class="sxs-lookup"><span data-stu-id="1dde5-686">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="1dde5-687">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="1dde5-687">AzureRM.Compute</span></span>
* <span data-ttu-id="1dde5-688">VMSS VM 更新功能</span><span class="sxs-lookup"><span data-stu-id="1dde5-688">VMSS VM Update feature</span></span>
    - <span data-ttu-id="1dde5-689">新增 'Update-AzureRmVmssVM' 和 'New-AzureRmVMDataDisk' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1dde5-689">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="1dde5-690">將 VirtualMachineScaleSetVM 參數新增至 'Add-AzureRmVMDataDisk' Cmdlet，以支援將資料磁碟新增至 Vmss VM。</span><span class="sxs-lookup"><span data-stu-id="1dde5-690">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="1dde5-691">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="1dde5-691">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="1dde5-692">已將 ADF .Net SDK 更新為版本 0.8.0-preview，包含以下變更：</span><span class="sxs-lookup"><span data-stu-id="1dde5-692">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="1dde5-693">新增設定中心存放庫的作業</span><span class="sxs-lookup"><span data-stu-id="1dde5-693">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="1dde5-694">將 QuickBooks LinkedService 更新為公開 consumerKey 和 consumerSecret 屬性</span><span class="sxs-lookup"><span data-stu-id="1dde5-694">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="1dde5-695">更新從 SecretBase 到 Object 的數個模型類型</span><span class="sxs-lookup"><span data-stu-id="1dde5-695">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="1dde5-696">新增 Blob 事件觸發程序</span><span class="sxs-lookup"><span data-stu-id="1dde5-696">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="1dde5-697">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1dde5-697">AzureRM.KeyVault</span></span>
* <span data-ttu-id="1dde5-698">更新文件和範例輸出</span><span class="sxs-lookup"><span data-stu-id="1dde5-698">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="1dde5-699">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="1dde5-699">AzureRM.Network</span></span>
* <span data-ttu-id="1dde5-700">啟用網路監看員 Cmdlet 上的流量分析參數</span><span class="sxs-lookup"><span data-stu-id="1dde5-700">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="1dde5-701">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="1dde5-701">AzureRM.Resources</span></span>
* <span data-ttu-id="1dde5-702">針對從 'Get-AzureRmResource' 傳回的 'PSResource' 物件，修正其中的 'Properties' 屬性問題</span><span class="sxs-lookup"><span data-stu-id="1dde5-702">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="1dde5-703">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="1dde5-703">AzureRM.Scheduler</span></span>
* <span data-ttu-id="1dde5-704">修正更新 ServiceBusQueueJob 時沒有設定新驗證值的問題</span><span class="sxs-lookup"><span data-stu-id="1dde5-704">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="1dde5-705">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="1dde5-705">AzureRM.Sql</span></span>
* <span data-ttu-id="1dde5-706">透過選擇性 LicenseType 參數更新下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1dde5-706">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="1dde5-707">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1dde5-707">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="1dde5-708">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="1dde5-708">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="1dde5-709">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="1dde5-709">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="1dde5-710">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="1dde5-710">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="1dde5-711">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1dde5-711">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="1dde5-712">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="1dde5-712">AzureRM.Websites</span></span>
* <span data-ttu-id="1dde5-713">更新 'New-AzureRMWebApp' 以使用來自策略程式庫的常見演算法。</span><span class="sxs-lookup"><span data-stu-id="1dde5-713">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="1dde5-714">6.1.0 - 2018 年 5 月</span><span class="sxs-lookup"><span data-stu-id="1dde5-714">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="1dde5-715">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="1dde5-715">AzureRM.Profile</span></span>
* <span data-ttu-id="1dde5-716">修正執行 'Clear-AzureRmContext' 會讓空白內容保留先前的預設內容名稱，導致使用者無法以舊名稱建立新內容的問題</span><span class="sxs-lookup"><span data-stu-id="1dde5-716">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="1dde5-717">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1dde5-717">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="1dde5-718">啟用 AS 上的閘道建立關聯/取消關聯作業。</span><span class="sxs-lookup"><span data-stu-id="1dde5-718">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="1dde5-719">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1dde5-719">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="1dde5-720">已新增 ApiVersions、ApiReleases 和 ApiRevisions 支援</span><span class="sxs-lookup"><span data-stu-id="1dde5-720">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="1dde5-721">已新增 ServiceFabric 後端支援</span><span class="sxs-lookup"><span data-stu-id="1dde5-721">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="1dde5-722">已新增 Application Insights 記錄器支援</span><span class="sxs-lookup"><span data-stu-id="1dde5-722">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="1dde5-723">已新增將 'Basic' sku 辨識為有效 sku 的 API 管理服務支援</span><span class="sxs-lookup"><span data-stu-id="1dde5-723">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="1dde5-724">已針對安裝由私人 CA 發出的憑證做為根或 CA 新增支援</span><span class="sxs-lookup"><span data-stu-id="1dde5-724">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="1dde5-725">已針對透過 KeyVault 和多個 Proxy 主機名稱接受自訂 SSL 憑證新增支援</span><span class="sxs-lookup"><span data-stu-id="1dde5-725">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="1dde5-726">已新增 MSI 身分識別支援</span><span class="sxs-lookup"><span data-stu-id="1dde5-726">Added support for MSI identity</span></span>
* <span data-ttu-id="1dde5-727">已新增透過 URL 接受原則的支援 附註：下列 Cmdlet 會在未來的版本中淘汰</span><span class="sxs-lookup"><span data-stu-id="1dde5-727">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="1dde5-728">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="1dde5-728">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="1dde5-729">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="1dde5-729">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="1dde5-730">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="1dde5-730">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="1dde5-731">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="1dde5-731">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="1dde5-732">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="1dde5-732">AzureRM.Batch</span></span>
* <span data-ttu-id="1dde5-733">發行新的 Cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="1dde5-733">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="1dde5-734">發行新的 Cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="1dde5-734">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="1dde5-735">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="1dde5-735">AzureRM.Consumption</span></span>
* <span data-ttu-id="1dde5-736">在 Cmdlet Get-AzureRmConsumptionUsageDetail 上新增新參數 Expand、ResourceGroup、InstanceName、InstanceId、Tags 和 Top</span><span class="sxs-lookup"><span data-stu-id="1dde5-736">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="1dde5-737">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1dde5-737">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="1dde5-738">針對 Export-AzureRmDataLakeStoreChildItemProperties 修正範例</span><span class="sxs-lookup"><span data-stu-id="1dde5-738">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="1dde5-739">修正 Set-AzureRmDataLakeStoreItemAclEntry 中 Recurse 案例的 Null 參數例外狀況</span><span class="sxs-lookup"><span data-stu-id="1dde5-739">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="1dde5-740">修正 Set-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl、Remove-AzureRmDataLakeStoreItemAclEntry 的說明檔</span><span class="sxs-lookup"><span data-stu-id="1dde5-740">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="1dde5-741">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="1dde5-741">AzureRM.Network</span></span>
* <span data-ttu-id="1dde5-742">將網路 SDK 版本從 18.0.0-預覽提高到 19.0.0-預覽</span><span class="sxs-lookup"><span data-stu-id="1dde5-742">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="1dde5-743">新增 Cmdlet 來建立通訊協定設定</span><span class="sxs-lookup"><span data-stu-id="1dde5-743">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="1dde5-744">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="1dde5-744">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="1dde5-745">新增 Cmdlet 以將新線路連線新增至現有的快速路由線路。</span><span class="sxs-lookup"><span data-stu-id="1dde5-745">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="1dde5-746">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="1dde5-746">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="1dde5-747">新增 Cmdlet 以將線路連線從現有的快速路由線路移除。</span><span class="sxs-lookup"><span data-stu-id="1dde5-747">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="1dde5-748">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="1dde5-748">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="1dde5-749">新增 Cmdlet 來擷取線路連線</span><span class="sxs-lookup"><span data-stu-id="1dde5-749">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="1dde5-750">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="1dde5-750">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="1dde5-751">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1dde5-751">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="1dde5-752">固定的伺服器驗證使用方式與產生的憑證 (問題 #5998)</span><span class="sxs-lookup"><span data-stu-id="1dde5-752">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="1dde5-753">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="1dde5-753">AzureRM.Sql</span></span>
* <span data-ttu-id="1dde5-754">已更新稽核 Cmdlet 以允許移除 AuditActions 或 AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="1dde5-754">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="1dde5-755">已修正 Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy 在設定新的彈性保留原則時，命令會失敗的問題；錯誤為：使用 azure 復原服務保存庫設定長期保留原則，且不再支援原則。</span><span class="sxs-lookup"><span data-stu-id="1dde5-755">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="1dde5-756">請提交具有新彈性保留原則的要求。</span><span class="sxs-lookup"><span data-stu-id="1dde5-756">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="1dde5-757">更新所有 Azure Sql Database/ElasticPool 建立/更新相關的 Cmdlet 以使用新的資料庫 API，其可支援縮放和階層相關屬性的 Sku 屬性。</span><span class="sxs-lookup"><span data-stu-id="1dde5-757">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="1dde5-758">更新的 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="1dde5-758">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="1dde5-759">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1dde5-759">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="1dde5-760">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="1dde5-760">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="1dde5-761">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="1dde5-761">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="1dde5-762">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="1dde5-762">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="1dde5-763">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1dde5-763">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="1dde5-764">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="1dde5-764">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="1dde5-765">更新 'Get-AzureRmTrafficManagerProfile' 的參數，以便在使用 -Name 參數時需要 -ResourceGroupName 參數。</span><span class="sxs-lookup"><span data-stu-id="1dde5-765">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
