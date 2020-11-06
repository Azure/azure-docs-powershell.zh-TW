---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmAvailabilitySet.md
ms.openlocfilehash: 5f2769987c87942af78bda238de00df94168249a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449955"
---
# Get-AzureRmAvailabilitySet

## 摘要
取得資源群組中的 Azure 可用性集合。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [<CommonParameters>]
```

## 說明
**AzureRmAvailabilitySet** Cmdlet 可在資源群組中取得 Azure 可用性集。
您可以指定要取得的特定可用性集的名稱。

## 示例

### 範例1：取得特定的可用性集
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
```

這個命令會在名為 ResourceGroup11 的資源群組中取得名為 AvailablitySet03 的可用性集。

### 範例2：取得所有的可用性集
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11"
```

這個命令會在名為 ResourceGroup11 的資源群組中取得所有的可用性集。

## 參數

### -名稱
指定此 Cmdlet 所取得之可用性集的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定資源群組的名稱。

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

### 所有
這個 Cmdlet 不接受任何輸入。

## 輸出

## 筆記

## 相關連結

[新-AzureRmAvailabilitySet](./New-AzureRmAvailabilitySet.md)

[移除-AzureRmAvailabilitySet](./Remove-AzureRmAvailabilitySet.md)


