---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 56b1a9378914a7fa2220e948b64c357b06f6f4dc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128771"
---
# Get-AzDataLakeAnalyticsComputePolicy

## 摘要
取得資料 Lake Analytics 計算原則或計算原則清單。

## 句法

```
Get-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzDataLakeAnalyticsComputePolicy** 會取得指定的 Azure Data Lake Analytics 計算原則或原則清單。

## 示例

### 範例1：取得指定的計算原則
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

這個命令會取得帳戶 "contosoadla" 中名為 "myPolicy" 的指定計算原則。

### 範例2：取得帳戶中的所有計算原則清單
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -AccountName "contosoadla"
```

這個命令會取得帳戶 "contosoadla" 中所有計算原則的清單

## 參數

### -帳戶
要從中取得計算原則或原則的帳戶名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

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

### -名稱
要取得之計算原則的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
您帳戶所在之資源群組的名稱。
[選用]，如果未提供，就會嘗試探索。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

## 輸出

### Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy

## 筆記

## 相關連結
