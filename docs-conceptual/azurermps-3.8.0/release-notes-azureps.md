---
title: Azure PowerShell 變更記錄 | Microsoft Docs
description: 這是在最新版中對 Azure powershell 所做的變更歷程記錄。
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: 2e17b6f7f62f25d8d91c4d32a4a1ae5c45b8665d
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/06/2018
ms.locfileid: "34821797"
---
# <a name="release-notes"></a><span data-ttu-id="ba79d-103">版本資訊</span><span class="sxs-lookup"><span data-stu-id="ba79d-103">Release notes</span></span>

<span data-ttu-id="ba79d-104">這是此版本中對 Azure PowerShell 所做的變更清單。</span><span class="sxs-lookup"><span data-stu-id="ba79d-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-380"></a><span data-ttu-id="ba79d-105">3.8.0 版</span><span class="sxs-lookup"><span data-stu-id="ba79d-105">Version 3.8.0</span></span>
* <span data-ttu-id="ba79d-106">計算</span><span class="sxs-lookup"><span data-stu-id="ba79d-106">Compute</span></span>
  - <span data-ttu-id="ba79d-107">修正 Get-\* Cmdlet 中的錯誤，以便擷取多頁的資料 (120 個以上的項目)</span><span class="sxs-lookup"><span data-stu-id="ba79d-107">Fix bug in Get-\* cmdlets, to allow retrieving multiple pages of data (more than 120 items)</span></span>
* <span data-ttu-id="ba79d-108">DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="ba79d-108">DataLakeAnalytics</span></span>
  - <span data-ttu-id="ba79d-109">有助於讓某些命令具有適當用語和範例的修正。</span><span class="sxs-lookup"><span data-stu-id="ba79d-109">Fix help for some commands to have the proper verbage and examples.</span></span>
* <span data-ttu-id="ba79d-110">DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ba79d-110">DataLakeStore</span></span>
  - <span data-ttu-id="ba79d-111">將前端和後端的支援新增至 `Get-AzureRMDataLakeStoreItemContent` Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ba79d-111">Add support for head and tail to the `Get-AzureRMDataLakeStoreItemContent` cmdlet.</span></span> <span data-ttu-id="ba79d-112">這能夠傳回要顯示之前面 N 個或最後 N 個新行分隔的資料列。</span><span class="sxs-lookup"><span data-stu-id="ba79d-112">This enables returning the top N or last N new line delimited rows to be displayed.</span></span>
* <span data-ttu-id="ba79d-113">HDInsight</span><span class="sxs-lookup"><span data-stu-id="ba79d-113">HDInsight</span></span>
  - <span data-ttu-id="ba79d-114">已新增 RServer 叢集類型的支援</span><span class="sxs-lookup"><span data-stu-id="ba79d-114">Added support for RServer cluster type</span></span>
    + <span data-ttu-id="ba79d-115">在 New-AzureRmHDInsightCluster 或 New-AzureRmHDInsightClusterConfig 中可針對 RServer 叢集指定 Edgenode VM 大小</span><span class="sxs-lookup"><span data-stu-id="ba79d-115">Edgenode VM size can be specified for RServer cluster in New-AzureRmHDInsightCluster or New-AzureRmHDInsightClusterConfig</span></span>
    + <span data-ttu-id="ba79d-116">RServer 現在是 Add-AzureRmHDInsightConfigValues 中的設定選項。</span><span class="sxs-lookup"><span data-stu-id="ba79d-116">RServer is now a configuration option in Add-AzureRmHDInsightConfigValues.</span></span> <span data-ttu-id="ba79d-117">它允許設定 RStudio 旗標來表示 RStudio 安裝應該完成。</span><span class="sxs-lookup"><span data-stu-id="ba79d-117">It allows for RStudio flag to be set to indicate that R Studio installation should be done.</span></span>
* <span data-ttu-id="ba79d-118">LogicApp</span><span class="sxs-lookup"><span data-stu-id="ba79d-118">LogicApp</span></span>
  - <span data-ttu-id="ba79d-119">已針對 contentlink 問題修正 Set-AzureRmIntegrationAccountSchema 和 Set-AzureRmIntegrationAccountMap Cmdlet (content 和 contentlink 的設定均導致更新失敗)。</span><span class="sxs-lookup"><span data-stu-id="ba79d-119">Set-AzureRmIntegrationAccountSchema and Set-AzureRmIntegrationAccountMap cmdlets are fixed for the contentlink issue(Both content and contentlink were set resulting in update failure).</span></span>
* <span data-ttu-id="ba79d-120">網路</span><span class="sxs-lookup"><span data-stu-id="ba79d-120">Network</span></span>
  - <span data-ttu-id="ba79d-121">已將新 Web 應用程式防火牆功能的支援新增至應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="ba79d-121">Added support for new web application firewall features to Application Gateways</span></span>
    + <span data-ttu-id="ba79d-122">已新增 New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig</span><span class="sxs-lookup"><span data-stu-id="ba79d-122">Added New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>
    + <span data-ttu-id="ba79d-123">已新增 Get-AzureRmApplicationGatewayAvailableWafRuleSets (別名：List-AzureRmApplicationGatewayAvailableWafRuleSets)</span><span class="sxs-lookup"><span data-stu-id="ba79d-123">Added Get-AzureRmApplicationGatewayAvailableWafRuleSets (Alias: List-AzureRmApplicationGatewayAvailableWafRuleSets)</span></span>
    + <span data-ttu-id="ba79d-124">已更新 New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration：已新增參數 -RuleSetType -RuleSetVersion 和 -DisabledRuleGroups</span><span class="sxs-lookup"><span data-stu-id="ba79d-124">Updated New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration: Added parameter -RuleSetType -RuleSetVersion and -DisabledRuleGroups</span></span>
    + <span data-ttu-id="ba79d-125">已更新 Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration：已新增參數 -RuleSetType -RuleSetVersion 和 -DisabledRuleGroups</span><span class="sxs-lookup"><span data-stu-id="ba79d-125">Updated Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration: Added parameter -RuleSetType -RuleSetVersion and -DisabledRuleGroups</span></span>
  - <span data-ttu-id="ba79d-126">已將 IPSec 原則的支援新增至虛擬網路閘道連線</span><span class="sxs-lookup"><span data-stu-id="ba79d-126">Added support for IPSec policies to Virtual Network Gateway Connections</span></span>
  - <span data-ttu-id="ba79d-127">已新增 New-AzureRmIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="ba79d-127">Added New-AzureRmIpsecPolicy</span></span>
  - <span data-ttu-id="ba79d-128">已更新 New-AzureRmVirtualNetworkGatewayConnection：已新增參數 -IpsecPolicies 和 -UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="ba79d-128">Updated New-AzureRmVirtualNetworkGatewayConnection: Added parameter -IpsecPolicies and -UsePolicyBasedTrafficSelectors</span></span>
* <span data-ttu-id="ba79d-129">設定檔</span><span class="sxs-lookup"><span data-stu-id="ba79d-129">Profile</span></span>
  - <span data-ttu-id="ba79d-130">已淘汰︰Save-AzureRmProfile 已重新命名為 Save-AzureRmContext，舊的 Cmdlet 名稱有別名，在下一版本中將會移除此別名。</span><span class="sxs-lookup"><span data-stu-id="ba79d-130">*Obsolete*: Save-AzureRmProfile is renamed to Save-AzureRmContext, there is an alias to the old cmdlet name, the alias will be removed in the next release.</span></span>
  - <span data-ttu-id="ba79d-131">已淘汰︰Select-AzureRmProfile 已重新命名為 Import-AzureRmContext，舊的 Cmdlet 名稱有別名，在下一版本中將會移除此別名。</span><span class="sxs-lookup"><span data-stu-id="ba79d-131">*Obsolete*: Select-AzureRmProfile is renamed to Import-AzureRmContext, there is an alias to the old cmdlet name, the alias will be removed in the next release.</span></span>
  - <span data-ttu-id="ba79d-132">下一版本將會變更設定檔 Cmdlet 的 PSAzureContext 和 PSAzureProfile 輸出類型。</span><span class="sxs-lookup"><span data-stu-id="ba79d-132">The PSAzureContext and PSAzureProfile output types of profile cmdlets will be changed in the next release.</span></span>
  - <span data-ttu-id="ba79d-133">下一版本的 Save-AzureRmContext Cmdlet 不會有 OutputType。</span><span class="sxs-lookup"><span data-stu-id="ba79d-133">The Save-AzureRmContext cmdlet will have no OutputType in the next release.</span></span>
  - <span data-ttu-id="ba79d-134">修正 Cmdlet 通用程式碼中的錯誤，以將符合 FIPS 規範的演算法用於資料雜湊：https://github.com/Azure/azure-powershell/issues/3651</span><span class="sxs-lookup"><span data-stu-id="ba79d-134">Fix bug in cmdlet common code to use FIPS-compliant algorithm for data hashes: https://github.com/Azure/azure-powershell/issues/3651</span></span>
* <span data-ttu-id="ba79d-135">Sql</span><span class="sxs-lookup"><span data-stu-id="ba79d-135">Sql</span></span>
  - <span data-ttu-id="ba79d-136">Azure 容錯移轉群組 Cmdlet 的錯誤修正</span><span class="sxs-lookup"><span data-stu-id="ba79d-136">Bug fixes on Azure Failover Group Cmdlets</span></span>
  - <span data-ttu-id="ba79d-137">修正作業輪詢</span><span class="sxs-lookup"><span data-stu-id="ba79d-137">Fix for operation polling</span></span>
  - <span data-ttu-id="ba79d-138">修正當 FailoverPolicy 設定為 Manual 時的 GracePeriodWithDataLossHour 值</span><span class="sxs-lookup"><span data-stu-id="ba79d-138">Fix GracePeriodWithDataLossHour value when setting FailoverPolicy to Manual</span></span>
* <span data-ttu-id="ba79d-139">TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ba79d-139">TrafficManager</span></span>
  - <span data-ttu-id="ba79d-140">支援地理流量路由方法</span><span class="sxs-lookup"><span data-stu-id="ba79d-140">Support for the Geographic traffic routing method</span></span>
    + <span data-ttu-id="ba79d-141">New-AzureRmTrafficManagerProfile 之 TrafficRoutingMethod 參數的新值 'Geographic'</span><span class="sxs-lookup"><span data-stu-id="ba79d-141">New value 'Geographic' for the TrafficRoutingMethod parameter of New-AzureRmTrafficManagerProfile</span></span>
    + <span data-ttu-id="ba79d-142">New-AzureRmTrafficManagerEndpoint 和 Add-AzureRmTrafficManagerEndpointConfig 的新參數 'GeoMapping'</span><span class="sxs-lookup"><span data-stu-id="ba79d-142">New parameter 'GeoMapping' for the New-AzureRmTrafficManagerEndpoint and Add-AzureRmTrafficManagerEndpointConfig</span></span>
    + <span data-ttu-id="ba79d-143">在 Get-AzureRmTrafficManagerProfile 傳回設定檔集合時修正其管線處理</span><span class="sxs-lookup"><span data-stu-id="ba79d-143">Fix piping for Get-AzureRmTrafficManagerProfile when it returns a collection of profiles</span></span>
* <span data-ttu-id="ba79d-144">ServiceManagement</span><span class="sxs-lookup"><span data-stu-id="ba79d-144">ServiceManagement</span></span>
  - <span data-ttu-id="ba79d-145">Restart-AzureVM：已新增 InitiateMaintenance 參數，以便在 VM 重新啟動期間執行維護。</span><span class="sxs-lookup"><span data-stu-id="ba79d-145">Restart-AzureVM: Added InitiateMaintenance parameter for performing maintenance during VM restart.</span></span>
  - <span data-ttu-id="ba79d-146">Get-AzureVM：已新增維護 狀態欄位。</span><span class="sxs-lookup"><span data-stu-id="ba79d-146">Get-AzureVM: Added Maintenance Status field.</span></span>
  - <span data-ttu-id="ba79d-147">已新增 Cmdlet 來支援復原服務保存庫升級</span><span class="sxs-lookup"><span data-stu-id="ba79d-147">Added new cmdlets to support Recovery Services vault upgrade</span></span>
    + <span data-ttu-id="ba79d-148">Test-AzureRecoveryServicesVaultUpgrade</span><span class="sxs-lookup"><span data-stu-id="ba79d-148">Test-AzureRecoveryServicesVaultUpgrade</span></span>
    + <span data-ttu-id="ba79d-149">Invoke-AzureRecoveryServicesVaultUpgrade</span><span class="sxs-lookup"><span data-stu-id="ba79d-149">Invoke-AzureRecoveryServicesVaultUpgrade</span></span>
