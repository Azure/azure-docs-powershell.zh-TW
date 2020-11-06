---
Module Name: AzureRM.Insights
Module Guid: 698c387c-bd6b-41c6-82ce-721f1ef39548
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/AzureRM.Insights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/AzureRM.Insights.md
ms.openlocfilehash: d4f7819a3ddbf49f4a3c4ed56cd8273b1f2e1848
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/23/2019
ms.locfileid: "93442236"
---
# AzureRM Insights 模組
## 說明
本主題顯示 Azure Insights Cmdlet 的說明主題。

## AzureRM Insights Cmdlet
### [附加 AzureRmAutoscaleSetting](Add-AzureRmAutoscaleSetting.md)
建立自動縮放設定。

### [附加 AzureRmLogAlertRule](Add-AzureRmLogAlertRule.md)
新增或取代記錄提醒規則。

### [附加 AzureRmLogProfile](Add-AzureRmLogProfile.md)
建立新的活動記錄設定檔。 此設定檔是用來將活動記錄封存至 Azure 儲存空間帳戶，或在相同訂閱中將它資料流程至 Azure 事件中樞。 

- 僅支援 **儲存空間** 帳戶標準儲存空間帳戶 (premium 儲存空間帳戶不支援) 。 它可能是 ARM 類型或傳統模式。 如果它是記錄在儲存空間帳戶中，則儲存活動記錄的成本會以標準的標準儲存費率計費。 每個訂閱只能有一個記錄 consequentially 每個訂閱只能使用一個儲存空間帳戶來匯出活動記錄。 

- **事件中心** -每個訂閱只能有一個記錄設定檔 consequentially 每個訂閱只能使用一個事件中樞來匯出活動記錄。 如果活動記錄是流入事件中樞，則會套用標準事件中樞定價。 

在活動記錄檔中，事件可與區域或「全域」相關。 [全域] 是指這些事件是地區 agnostics，且與區域無關，事實上大部分事件都屬於這種類別。 如果活動記錄設定檔是從入口網站進行設定，則會將 [全域] 與您在使用者介面中選取的任何其他區域一起隱出。 使用 Cmdlet 時，"Global" 是「全域」的位置，必須從任何其他區域明確提及。 

**注意** ：- **在位置中設定「全域」失敗，會導致大部分的活動記錄不會匯出。** 

### [附加 AzureRmMetricAlertRule](Add-AzureRmMetricAlertRule.md)
新增或更新以公制為基礎的警示規則。

### [附加 AzureRmWebtestAlertRule](Add-AzureRmWebtestAlertRule.md)
新增或更新 webtest 提醒規則。

### [Disable-AzureRmActivityLogAlert](Disable-AzureRmActivityLogAlert.md)
停用活動記錄通知並設定其標記。

### [Enable-AzureRmActivityLogAlert](Enable-AzureRmActivityLogAlert.md)
啟用活動記錄通知並設定其標記。

### [AzureRmActionGroup](Get-AzureRmActionGroup.md)
取得動作群組 (s) 。

### [AzureRmActivityLogAlert](Get-AzureRmActivityLogAlert.md)
取得一或多個活動記錄通知資源。

### [AzureRmAlertHistory](Get-AzureRmAlertHistory.md)
取得預警的歷程記錄。

### [AzureRmAlertRule](Get-AzureRmAlertRule.md)
取得警示規則。

### [AzureRmAutoscaleHistory](Get-AzureRmAutoscaleHistory.md)
取得自動縮放歷程記錄。

### [AzureRmAutoscaleSetting](Get-AzureRmAutoscaleSetting.md)
取得自動縮放設定。

### [AzureRmDiagnosticSetting](Get-AzureRmDiagnosticSetting.md)
取得已記錄的類別和時間 grains。

### [AzureRmLog](Get-AzureRmLog.md)
取得事件的記錄。

### [AzureRmLogProfile](Get-AzureRmLogProfile.md)
取得記錄設定檔。

### [AzureRmMetric](Get-AzureRmMetric.md)
取得資源的度量值。

### [AzureRmMetricDefinition](Get-AzureRmMetricDefinition.md)
取得公制定義。

### [AzureRmUsage](Get-AzureRmUsage.md)
取得資源的使用標準。

### [新-AzureRmActionGroup](New-AzureRmActionGroup.md)
在記憶體中建立 ActionGroup 參考物件。

### [新-AzureRmActionGroupReceiver](New-AzureRmActionGroupReceiver.md)
建立新的 [動作群組收件者]。

### [新-AzureRmActivityLogAlertCondition](New-AzureRmActivityLogAlertCondition.md)
在記憶體中建立新的活動記錄警示條件物件。

### [新-AzureRmAlertRuleEmail](New-AzureRmAlertRuleEmail.md)
建立警示規則的電子郵件動作。

### [新-AzureRmAlertRuleWebhook](New-AzureRmAlertRuleWebhook.md)
建立警示規則 webhook。

### [新-AzureRmAutoscaleNotification](New-AzureRmAutoscaleNotification.md)
建立自動縮放電子郵件通知。

### [新-AzureRmAutoscaleProfile](New-AzureRmAutoscaleProfile.md)
建立自動縮放設定檔。

### [新-AzureRmAutoscaleRule](New-AzureRmAutoscaleRule.md)
建立自動縮放規則。

### [新-AzureRmAutoscaleWebhook](New-AzureRmAutoscaleWebhook.md)
建立自動縮放 webhook。

### [移除-AzureRmActionGroup](Remove-AzureRmActionGroup.md)
移除動作群組。

### [移除-AzureRmActivityLogAlert](Remove-AzureRmActivityLogAlert.md)
移除活動記錄通知。

### [移除-AzureRmAlertRule](Remove-AzureRmAlertRule.md)
移除警示規則。

### [移除-AzureRmAutoscaleSetting](Remove-AzureRmAutoscaleSetting.md)
移除自動縮放設定。

### [移除-AzureRmLogProfile](Remove-AzureRmLogProfile.md)
移除記錄設定檔。

### [Set-AzureRmActionGroup](Set-AzureRmActionGroup.md)
建立新的或更新現有的動作群組。

### [Set-AzureRmActivityLogAlert](Set-AzureRmActivityLogAlert.md)
建立新的或設定現有的活動記錄通知。

### [Set-AzureRmDiagnosticSetting](Set-AzureRmDiagnosticSetting.md)
設定資源的記錄和標準設定。

