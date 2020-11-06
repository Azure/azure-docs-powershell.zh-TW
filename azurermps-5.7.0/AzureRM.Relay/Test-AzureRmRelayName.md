---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/test-azurermrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
ms.openlocfilehash: adf7c4b7f8d80e16b49d9d55b742a55279232a07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450523"
---
# Test-AzureRmRelayName

## 摘要
檢查指定命名空間名稱的可用性

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Test-AzureRmRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**Test AzureRmRelayName** Cmdlet 會檢查命名空間名稱的可用性

## 示例

### 範例1
```
PS C:\> Test-AzureRmRelayName -Namespace TestingtheAvailability
```

### 範例2
```
PS C:\> Test-AzureRmRelayName -Namespace Testi
```

### 範例3
```
PS C:\> Test-AzureRmRelayName -Namespace Test123
```

傳回命名空間名稱的可用性狀態

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### -命名空間
中繼命名空間名稱。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### -命名空間
 System.object

## 輸出

### [CheckNameAvailabilityResultAttributes、0.1.0.0、Culture = 中性、PublicKeyToken = null]，Culture = 非特定語言，PublicKeyToken = null]

### 範例1
NameAvailable 原因訊息
------------- ------ -------
         True   None

### 範例2
NameAvailable 原因訊息
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.

### 範例3
NameAvailable 原因訊息
-------------    ------ -------
        False NameInUse The specified service namespace is not available.

## 筆記

## 相關連結

