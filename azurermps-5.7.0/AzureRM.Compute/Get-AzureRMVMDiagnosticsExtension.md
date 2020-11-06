---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D5BEA683-44AE-4D71-827D-02A03F0BEAE9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRMVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRMVMDiagnosticsExtension.md
ms.openlocfilehash: 32d3d5a152f36c0e4e5f8e3e4e4ecc2b8eb6ee31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449398"
---
# Get-AzureRmVMDiagnosticsExtension

## 摘要
取得虛擬機器上的診斷延伸設定。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [<CommonParameters>]
```

## 說明
**AzureRmVMDiagnosticsExtension** Cmdlet 會取得虛擬機器上 Azure Diagnostics 延伸的設定。

## 示例

### 範例1：取得套用至虛擬機器的診斷延伸
```
PS C:\> Get-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22"
```

這個命令會取得已套用到名為 ContosoVM22 的虛擬機器的診斷延伸。

## 參數

### -名稱
指定此 Cmdlet 取得其設定的診斷延伸名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定虛擬機器之資源群組的名稱。

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

### -狀態
指示此 Cmdlet 使用 Status 值。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
指定此 Cmdlet 取得診斷延伸的虛擬機器名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

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

[移除-AzureRmVMDiagnosticsExtension](./Remove-AzureRmVMDiagnosticsExtension.md)

[Set-AzureRmVMDiagnosticsExtension](./Set-AzureRMVMDiagnosticsExtension.md)


