---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/new-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 36bf1bbfeb0c44189f5eeeaa0988d0314980e48d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447833"
---
# New-AzureRmDataLakeAnalyticsAccount

## 摘要
建立資料 Lake Analytics 帳戶。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
New-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tag] <Hashtable>] [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>]
 [-QueryStoreRetention <Int32>] [-Tier <TierType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
**新的-AzureRmDataLakeAnalyticsAccount** Cmdlet 會建立 Azure Data Lake Analytics 帳戶。

## 示例

### 範例1：建立資料 Lake Analytics 帳戶
```
PS C:\>New-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

這個命令會在名為 ContosoOrg 的資源群組中，建立一個名為 ContosoAdlAccount 的資料 Lake Analytics 帳戶，該帳戶會使用 ContosoAdlStore 資料存放區。

## 參數

### -DefaultDataLakeStore
指定要設定為預設資料來源的 Data Lake Store 帳戶名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -位置
指定建立資料 Lake Analytics 帳戶的位置。
目前僅支援東美國2。

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxAnalyticsUnits
此帳戶的選用最大支援分析單位。

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelism

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxJobCount
同時在帳戶下執行的選用最大作業數。 如果沒有指定，則預設為3

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -名稱
指定 Data Lake Analytics 帳戶名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -QueryStoreRetention
保留作業中繼資料的可選天數。 如果沒有指定，則預設值為30天。

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定資料 Lake Analytics 帳戶的資源組名稱。
若要建立資源群組，請使用 New-AzureRmResourceGroup Cmdlet。

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
與此帳戶相關聯之標記的字串字典

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### 層級
此帳戶要使用的預期承諾層級。

```yaml
Type: TierType
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment100AUHours, Commitment500AUHours, Commitment1000AUHours, Commitment5000AUHours, Commitment10000AUHours, Commitment50000AUHours, Commitment100000AUHours, Commitment500000AUHours

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有
這個 Cmdlet 不接受任何輸入。

## 輸出

### PSDataLakeAnalyticsAccount
新建立的帳戶的詳細資料。

## 筆記

## 相關連結

[AzureRmDataLakeAnalyticsAccount](./Get-AzureRmDataLakeAnalyticsAccount.md)

[移除-AzureRmDataLakeAnalyticsAccount](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[Set-AzureRmDataLakeAnalyticsAccount](./Set-AzureRmDataLakeAnalyticsAccount.md)

[Test-AzureRmDataLakeAnalyticsAccount](./Test-AzureRmDataLakeAnalyticsAccount.md)


