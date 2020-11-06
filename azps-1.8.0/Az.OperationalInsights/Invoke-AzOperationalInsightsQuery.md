---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/invoke-azoperationalinsightsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
ms.openlocfilehash: 64a7835f1401e8b256e6f549203baaf8e8191606
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621302"
---
# Invoke-AzOperationalInsightsQuery

## 摘要
根據指定的參數傳回搜尋結果。

## 句法

### ByWorkspaceId (預設) 
```
Invoke-AzOperationalInsightsQuery -WorkspaceId <String> -Query <String> [-Timespan <TimeSpan>] [-Wait <Int32>]
 [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByWorkspaceObject
```
Invoke-AzOperationalInsightsQuery -Workspace <PSWorkspace> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
**AzOperationalInsightsQuery** Cmdlet 會根據指定的參數傳回搜尋結果。
您可以在傳回物件的 Metadata 屬性中，存取搜尋的狀態。
如果狀態為 [待處理]，則搜尋尚未完成，結果則會從封存。
您可以從傳回物件的 Value 屬性中取得搜尋結果。

## 示例

### 範例1：使用查詢取得搜尋結果
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $queryResults.Results
...
```

呼叫後，$queryResults。結果將包含查詢中所有產生的資料列。

### 範例2：轉換 $results。結果 IEnumberable 至陣列
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $resultsArray = [System.Linq.Enumerable]::ToArray($results.Results)
...
```

某些查詢會傳回非常大的資料集。 因此，此 Cmdlet 的預設行為是返回 IEnumerable 來減少記憶體成本。 如果您想要有結果陣列，您可以使用 LINQ ToArray ( # A1 延伸方法，將 IEnumerable 轉換成陣列。

### 範例3：使用查詢針對特定時間範圍取得搜尋結果
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -Timespan (New-TimeSpan -Hours 24)
PS C:\> $queryResults.Results
...
```

此查詢的結果將限制為過去24小時。

### 範例4：在查詢結果中加入轉譯 & 統計資料
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -IncludeRender -IncludeStatistics
PS C:\> $queryResults.Results
...
PS C:\> $queryResults.Render
...
PS C:\> $queryResults.Statistics
...
```

如需轉譯 [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) 與統計資訊的詳細資訊，請參閱。

## 參數

### -AsJob
在背景中執行 Cmdlet

```yaml
Type: System.Management.Automation.SwitchParameter
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

### -IncludeRender
如果已指定，度量查詢的轉譯資訊將會包含在回應中。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeStatistics
如果已指定，查詢的統計資料就會包含在回應中。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Query
要執行的查詢。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Timespan
要與查詢系結的 timespan。

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -稍候
會將上限放在伺服器處理查詢時花費的時間長度。
請參閱 https://dev.loganalytics.io/documentation/Using-the-API/Timeouts

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -工作區
工作區

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WorkspaceId
工作區識別碼。

```yaml
Type: System.String
Parameter Sets: ByWorkspaceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### PSWorkspace 中的 OperationalInsights。

## 輸出

### PSQueryResponse 中的 OperationalInsights。

## 筆記

## 相關連結
