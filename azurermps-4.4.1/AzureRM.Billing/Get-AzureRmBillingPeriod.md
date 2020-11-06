---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
ms.openlocfilehash: f6b75a1c161515ee45571ba3db6d2f84b95af967
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447156"
---
# Get-AzureRmBillingPeriod

## 摘要
取得訂閱的計費期間。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

###  (預設) 清單
```
Get-AzureRmBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### 通過
```
Get-AzureRmBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmBillingPeriod** Cmdlet 會取得訂閱的計費期間。

## 示例

### 範例1
```
PS C:\> Get-AzureRmBillingPeriod
```

取得訂閱的所有可用帳單週期。

### 範例2
```
PS C:\> Get-AzureRmBillingPeriod -Name 201704-1
```

以指定名稱取得訂閱的帳單期限。

### 範例3
```
PS C:\> Get-AzureRmBillingPeriod -MaxCount 2
```

最多可以取得訂閱的2個帳單期間。

## 參數

### -MaxCount
決定要傳回的最大記錄數。

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
要取得之特定帳單期間的名稱。

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Single
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有

## 輸出

### [System.object]。清單 ' 1 [PSBillingPeriod，0.12.0.0，#... 帳單，版本 =，Culture = 中性，PublicKeyToken = null）]
PSBillingPeriod 中的 [.]

## 筆記

## 相關連結

