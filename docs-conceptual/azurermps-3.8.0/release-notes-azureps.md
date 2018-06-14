---
title: Azure PowerShell 變更記錄 | Microsoft Docs
description: 這是在最新版中對 Azure powershell 所做的變更歷程記錄。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: b777a5fe036cda58a930ac0f5aaef3b9a7c2b420
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/08/2018
ms.locfileid: "34853435"
---
# <a name="release-notes"></a>版本資訊

這是此版本中對 Azure PowerShell 所做的變更清單。

## <a name="version-380"></a>3.8.0 版
* 計算
  - 修正 Get-* Cmdlet 中的錯誤，以便擷取多頁的資料 (120 個以上的項目)
* DataLakeAnalytics
  - 有助於讓某些命令具有適當用語和範例的修正。
* DataLakeStore
  - 將前端和後端的支援新增至 `Get-AzureRMDataLakeStoreItemContent` Cmdlet。 這能夠傳回要顯示之前面 N 個或最後 N 個新行分隔的資料列。
* HDInsight
  - 已新增 RServer 叢集類型的支援
    + 在 New-AzureRmHDInsightCluster 或 New-AzureRmHDInsightClusterConfig 中可針對 RServer 叢集指定 Edgenode VM 大小
    + RServer 現在是 Add-AzureRmHDInsightConfigValues 中的設定選項。 它允許設定 RStudio 旗標來表示 RStudio 安裝應該完成。
* LogicApp
  - 已針對 contentlink 問題修正 Set-AzureRmIntegrationAccountSchema 和 Set-AzureRmIntegrationAccountMap Cmdlet (content 和 contentlink 的設定均導致更新失敗)。
* 網路
  - 已將新 Web 應用程式防火牆功能的支援新增至應用程式閘道
    + 已新增 New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig
    + 已新增 Get-AzureRmApplicationGatewayAvailableWafRuleSets (別名：List-AzureRmApplicationGatewayAvailableWafRuleSets)
    + 已更新 New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration：已新增參數 -RuleSetType -RuleSetVersion 和 -DisabledRuleGroups
    + 已更新 Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration：已新增參數 -RuleSetType -RuleSetVersion 和 -DisabledRuleGroups
  - 已將 IPSec 原則的支援新增至虛擬網路閘道連線
  - 已新增 New-AzureRmIpsecPolicy
  - 已更新 New-AzureRmVirtualNetworkGatewayConnection：已新增參數 -IpsecPolicies 和 -UsePolicyBasedTrafficSelectors
* 設定檔
  - 已淘汰︰Save-AzureRmProfile 已重新命名為 Save-AzureRmContext，舊的 Cmdlet 名稱有別名，在下一版本中將會移除此別名。
  - 已淘汰︰Select-AzureRmProfile 已重新命名為 Import-AzureRmContext，舊的 Cmdlet 名稱有別名，在下一版本中將會移除此別名。
  - 下一版本將會變更設定檔 Cmdlet 的 PSAzureContext 和 PSAzureProfile 輸出類型。
  - 下一版本的 Save-AzureRmContext Cmdlet 不會有 OutputType。
  - 修正 Cmdlet 通用程式碼中的錯誤，以將符合 FIPS 規範的演算法用於資料雜湊：https://github.com/Azure/azure-powershell/issues/3651
* Sql
  - Azure 容錯移轉群組 Cmdlet 的錯誤修正
  - 修正作業輪詢
  - 修正當 FailoverPolicy 設定為 Manual 時的 GracePeriodWithDataLossHour 值
* TrafficManager
  - 支援地理流量路由方法
    + New-AzureRmTrafficManagerProfile 之 TrafficRoutingMethod 參數的新值 'Geographic'
    + New-AzureRmTrafficManagerEndpoint 和 Add-AzureRmTrafficManagerEndpointConfig 的新參數 'GeoMapping'
    + 在 Get-AzureRmTrafficManagerProfile 傳回設定檔集合時修正其管線處理
* ServiceManagement
  - Restart-AzureVM：已新增 InitiateMaintenance 參數，以便在 VM 重新啟動期間執行維護。
  - Get-AzureVM：已新增維護 狀態欄位。
  - 已新增 Cmdlet 來支援復原服務保存庫升級
    + Test-AzureRecoveryServicesVaultUpgrade
    + Invoke-AzureRecoveryServicesVaultUpgrade
