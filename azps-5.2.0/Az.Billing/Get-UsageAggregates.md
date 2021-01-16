---
external help file: Microsoft.Azure.PowerShell.Cmdlets.UsageAggregates.dll-Help.xml
Module Name: Az.Billing
ms.assetid: 52B3ECCB-80E5-4E16-954A-B83D0BDC7E22
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-usageaggregates
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
ms.openlocfilehash: 858966f5fb20f001dc21363875362673884fcc90
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98277140"
---
# Get-UsageAggregates

## 摘要
取得報告的 Azure 訂閱使用狀況詳細資料。

## 句法

```
Get-UsageAggregates -ReportedStartTime <DateTime> -ReportedEndTime <DateTime>
 [-AggregationGranularity <AggregationGranularity>] [-ShowDetails <Boolean>] [-ContinuationToken <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**UsageAggregates** Cmdlet 會透過下列屬性取得匯總的 Azure 訂閱使用資料： 
- 報告使用方式的開始和結束時間。
- [每日] 或 [每小時] 的匯總精確度。
- 同一資源多個實例的實例層級詳細資料。
針對一致的結果，傳回的資料是根據 Azure 資源報告使用狀況詳細資料的時間。
如需詳細資訊，請參閱 https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) Microsoft 開發人員網路文件庫中的 AZURE 帳單 REST API 參考 (。

## 示例

### 範例1：檢索訂閱資料
```
PS C:\>Get-UsageAggregates -ReportedStartTime "5/2/2015" -ReportedEndTime "5/5/2015"
```

這個命令會針對5/2/2015 和5/5/2015 之間的訂閱檢索報告的使用方式資料。

## 參數

### -AggregationGranularity
指定資料的匯總精確度。
有效值為： [每日] 和 [每小時]。
預設值為 [每日]。

```yaml
Type: Microsoft.Azure.Commerce.UsageAggregates.Models.AggregationGranularity
Parameter Sets: (All)
Aliases:
Accepted values: Daily, Hourly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContinuationToken
指定從先前通話中的回應本文中檢索到的延續標記。
針對大型結果集，回應會使用延續標記進行分頁。
延續標記會充當進度的書簽。
如果您沒有指定此參數，則會從 *ReportedStartTime* 中指定的日期或小時數開始檢索資料。
我們建議您追蹤資料的 [回應] 頁面中的下一個連結。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportedEndTime
指定在 Azure 帳單系統中記錄資源使用狀況時所報告的結束時間。
Azure 是一種分散式系統，遍佈世界各地的多個資料中心，因此在資源實際使用時間和使用方式事件達到帳單系統之間有延遲，這是資源使用量所報告的時間。
若要取得針對某個時段報告之訂閱的所有使用方式事件，您需要依報告的時間進行查詢。
即使您是依報告的時間進行查詢，此 Cmdlet 也會依資源使用時間來匯總回應資料。
[資源使用狀況] 資料對於分析資料而言是實用的樞紐分析表。

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportedStartTime
指定在 Azure 帳單系統中記錄資源使用狀況時所報告的開始時間。

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShowDetails
指示此 Cmdlet 是否會傳回使用方式資料的實例層級詳細資料。
預設值為 [$True]。
如果 $False，服務會將結果聚集在伺服器端，因此會傳回較少的匯總群組。
例如，如果您執行的是三個網站，預設會針對網站使用方式取得三個明細專案。
不過，當此值為 $False 時，相同的 **subscriptionId**、 **meterId**、 **usageStartTime** 和 **usageEndTime** 的所有資料都會折迭為單一明細專案。

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有

## 輸出

### UsageAggregationGetResponse 中的 UsageAggregates。

## 筆記

## 相關連結
