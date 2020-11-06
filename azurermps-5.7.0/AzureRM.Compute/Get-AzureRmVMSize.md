---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMSize.md
ms.openlocfilehash: d75ff7f549ddb1efd9f5640b9b2d634449faa21c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449941"
---
# Get-AzureRmVMSize

## 摘要
取得可用的虛擬機器大小。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### ListVirtualMachineSizeParamSet (預設) 
```
Get-AzureRmVMSize [-Location] <String> [<CommonParameters>]
```

### ListAvailableSizesForAvailabilitySet
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String> [<CommonParameters>]
```

### ListAvailableSizesForVirtualMachine
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-VMName] <String> [<CommonParameters>]
```

## 說明
**AzureRmVMSize** Cmdlet 會取得可用的虛擬機器大小。

## 示例

### 範例1：取得位置的虛擬電腦大小
```
PS C:\> Get-AzureRmVMSize -Location "Central US"
```

這個命令會取得指定位置中虛擬機器的可用大小。

### 範例2：取得可用性集的大小
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

這個命令會針對您可以在名為 AvailabilitySet17 的可用性集中部署的虛擬機器，取得可用的大小。

### 範例3：取得現有虛擬機器的大小
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

這個命令會取得名為 VirtualMachine12 的現有虛擬機器的可用大小。
您可以將此虛擬機器的大小調整為此命令所取得的大小。

## 參數

### -AvailabilitySetName
指定此 Cmdlet 取得可用虛擬機器大小的可用性集名稱。

```yaml
Type: String
Parameter Sets: ListAvailableSizesForAvailabilitySet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -位置
指定此 Cmdlet 取得可用虛擬機器大小的位置。

```yaml
Type: String
Parameter Sets: ListVirtualMachineSizeParamSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定虛擬機器之資源群組的名稱。

```yaml
Type: String
Parameter Sets: ListAvailableSizesForAvailabilitySet, ListAvailableSizesForVirtualMachine
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
指定虛擬機器的名稱，這個 Cmdlet 會取得可用的虛擬電腦大小來調整大小。

```yaml
Type: String
Parameter Sets: ListAvailableSizesForVirtualMachine
Aliases: 

Required: True
Position: 1
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

[AzureRmVM](./Get-AzureRmVM.md)


