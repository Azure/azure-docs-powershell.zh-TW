---
Module Name: Az.Monitor
Module Guid: 698c387c-bd6b-41c6-82ce-721f1ef39548
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.monitor
Help Version: 4.0.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Az.Monitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Az.Monitor.md
ms.openlocfilehash: ce60ca11184537254fa899317241e69849eb0b1c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279102"
---
# Az. 監視器模組
## 說明
本主題顯示 Azure Insights Cmdlet 的說明主題。

## Az. 監視 Cmdlet
### [附加 AzAutoscaleSetting](Add-AzAutoscaleSetting.md)
建立自動縮放設定。

### [附加 AzLogProfile](Add-AzLogProfile.md)
建立新的活動記錄設定檔。 此設定檔是用來將活動記錄封存至 Azure 儲存空間帳戶，或在相同訂閱中將它資料流程至 Azure 事件中樞。 

### [附加 AzMetricAlertRule](Add-AzMetricAlertRule.md)
新增或更新以公制為基礎的警示規則。

### [附加 AzMetricAlertRuleV2](Add-AzMetricAlertRuleV2.md)
新增或更新基 (非傳統) 公制規則。

### [附加 AzWebtestAlertRule](Add-AzWebtestAlertRule.md)
新增或更新 webtest 提醒規則。

### [Disable-AzActivityLogAlert](Disable-AzActivityLogAlert.md)
停用活動記錄通知並設定其標記。

### [Enable-AzActivityLogAlert](Enable-AzActivityLogAlert.md)
啟用活動記錄通知並設定其標記。

### [AzActionGroup](Get-AzActionGroup.md)
取得動作群組 (s) 。

### [AzActivityLog](Get-AzActivityLog.md)
檢索活動記錄事件。

### [AzActivityLogAlert](Get-AzActivityLogAlert.md)
取得一或多個活動記錄通知資源。

### [AzAlertHistory](Get-AzAlertHistory.md)
取得預警的歷程記錄。

### [AzAlertRule](Get-AzAlertRule.md)
取得警示規則。

### [AzAutoscaleHistory](Get-AzAutoscaleHistory.md)
取得自動縮放歷程記錄。

### [AzAutoscaleSetting](Get-AzAutoscaleSetting.md)
取得自動縮放設定。

### [AzDiagnosticSetting](Get-AzDiagnosticSetting.md)
取得已記錄的類別和時間 grains。

### [AzDiagnosticSettingCategory](Get-AzDiagnosticSettingCategory.md)
取得或列出 Azure 資源支援的診斷設定類別。

### [AzInsightsPrivateLinkScope](Get-AzInsightsPrivateLinkScope.md)
取得私人連結範圍

### [AzInsightsPrivateLinkScopedResource](Get-AzInsightsPrivateLinkScopedResource.md)
取得私人連結範圍資源

### [AzLogProfile](Get-AzLogProfile.md)
取得記錄設定檔。

### [AzMetric](Get-AzMetric.md)
取得資源的度量值。

### [AzMetricAlertRuleV2](Get-AzMetricAlertRuleV2.md)
取得 V2 (非傳統) 標準警示規則

### [AzMetricDefinition](Get-AzMetricDefinition.md)
取得公制定義。

### [AzScheduledQueryRule](Get-AzScheduledQueryRule.md)
取得排程的查詢資源

### [新-AzActionGroup](New-AzActionGroup.md)
在記憶體中建立 ActionGroup 參考物件。

### [新-AzActionGroupReceiver](New-AzActionGroupReceiver.md)
建立新的 [動作群組收件者]。

### [新-AzActivityLogAlertCondition](New-AzActivityLogAlertCondition.md)
在記憶體中建立新的活動記錄警示條件物件。

### [新-AzAlertRuleEmail](New-AzAlertRuleEmail.md)
建立警示規則的電子郵件動作。

### [新-AzAlertRuleWebhook](New-AzAlertRuleWebhook.md)
建立警示規則 webhook。

### [新-AzAutoscaleNotification](New-AzAutoscaleNotification.md)
建立自動縮放電子郵件通知。

### [新-AzAutoscaleProfile](New-AzAutoscaleProfile.md)
建立自動縮放設定檔。

### [新-AzAutoscaleRule](New-AzAutoscaleRule.md)
建立自動縮放規則。

### [新-AzAutoscaleWebhook](New-AzAutoscaleWebhook.md)
建立自動縮放 webhook。

### [新-AzDiagnosticDetailSetting](New-AzDiagnosticDetailSetting.md)
建立 PSDiagnosticDetailSetting 物件，類型可以是公制或 log

### [新-AzDiagnosticSetting](New-AzDiagnosticSetting.md)
建立 PSServiceDiagnosticSettings 物件。

### [新-AzInsightsPrivateLinkScope](New-AzInsightsPrivateLinkScope.md)
建立私人連結範圍

### [新-AzInsightsPrivateLinkScopedResource](New-AzInsightsPrivateLinkScopedResource.md)
針對私人連結範圍資源建立

### [新-AzMetricAlertRuleV2Criteria](New-AzMetricAlertRuleV2Criteria.md)
建立可以用來建立新度量警示的 [局部準則] 物件

### [新-AzMetricAlertRuleV2DimensionSelection](New-AzMetricAlertRuleV2DimensionSelection.md)
建立可用於構造標準警示準則的局部維度選擇物件。

### [新-AzMetricFilter](New-AzMetricFilter.md)
建立可用於查詢度量單位的度量維度篩選。

### [新-AzScheduledQueryRule](New-AzScheduledQueryRule.md)
 (排程的查詢規則類型建立記錄警報規則) 

### [新-AzScheduledQueryRuleAlertingAction](New-AzScheduledQueryRuleAlertingAction.md)
建立 [警示動作] 類型的物件

### [新-AzScheduledQueryRuleAznsActionGroup](New-AzScheduledQueryRuleAznsActionGroup.md)
建立 Azns 動作群組類型的物件

### [新-AzScheduledQueryRuleLogMetricTrigger](New-AzScheduledQueryRuleLogMetricTrigger.md)
建立類型記錄度量觸發程式的物件。

### [新-AzScheduledQueryRuleSchedule](New-AzScheduledQueryRuleSchedule.md)
建立排程類型的物件

### [新-AzScheduledQueryRuleSource](New-AzScheduledQueryRuleSource.md)
建立來源類型的物件

### [新-AzScheduledQueryRuleTriggerCondition](New-AzScheduledQueryRuleTriggerCondition.md)
建立觸發條件類型的物件

### [移除-AzActionGroup](Remove-AzActionGroup.md)
移除動作群組。

### [移除-AzActivityLogAlert](Remove-AzActivityLogAlert.md)
移除活動記錄通知。

### [移除-AzAlertRule](Remove-AzAlertRule.md)
移除警示規則。

### [移除-AzAutoscaleSetting](Remove-AzAutoscaleSetting.md)
移除自動縮放設定。

### [移除-AzDiagnosticSetting](Remove-AzDiagnosticSetting.md)
移除 a 資源的診斷設定。

### [移除-AzInsightsPrivateLinkScope](Remove-AzInsightsPrivateLinkScope.md)
刪除私人連結範圍

### [移除-AzInsightsPrivateLinkScopedResource](Remove-AzInsightsPrivateLinkScopedResource.md)
針對私人連結範圍資源刪除

### [移除-AzLogProfile](Remove-AzLogProfile.md)
移除記錄設定檔。

### [移除-AzMetricAlertRuleV2](Remove-AzMetricAlertRuleV2.md)
移除 V2 (非傳統) 標準警示規則。

### [移除-AzScheduledQueryRule](Remove-AzScheduledQueryRule.md)
移除記錄提醒規則

### [Set-AzActionGroup](Set-AzActionGroup.md)
建立新的或更新現有的動作群組。

### [Set-AzActivityLogAlert](Set-AzActivityLogAlert.md)
建立新的或設定現有的活動記錄通知。

### [Set-AzDiagnosticSetting](Set-AzDiagnosticSetting.md)
設定資源的記錄和標準設定。

### [Set-AzScheduledQueryRule](Set-AzScheduledQueryRule.md)
更新記錄提醒規則

### [更新-AzInsightsPrivateLinkScope](Update-AzInsightsPrivateLinkScope.md)
私人連結範圍的更新

### [更新-AzScheduledQueryRule](Update-AzScheduledQueryRule.md)
更新記錄提醒規則

