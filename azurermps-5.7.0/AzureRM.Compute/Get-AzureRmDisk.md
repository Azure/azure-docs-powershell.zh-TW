---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
ms.openlocfilehash: e34016b3bc7677c9591c07e54dd42a88a820d44b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449948"
---
# Get-AzureRmDisk

## 摘要
取得磁片的屬性。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>] [<CommonParameters>]
```

## 說明
**AzureRmDisk** Cmdlet 會取得磁片的屬性。

## 示例

### 範例1
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

這個命令會取得資源群組 ' ResourceGroup01 ' 中名為 ' Disk01 ' 磁片的屬性。

### 範例2
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01'
```

這個命令會取得資源群組 ' ResourceGroup01 ' 中所有磁片的屬性。

### 範例3
```
PS C:\> Get-AzureRmDisk
```

這個命令會取得訂閱下所有磁片的屬性。

## 參數

### -DiskName
指定磁片的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
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

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

## 輸出

### Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskList

## 筆記

## 相關連結

