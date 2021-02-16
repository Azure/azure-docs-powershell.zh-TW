---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdscextensionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtensionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtensionStatus.md
ms.openlocfilehash: b932c7e6f920d538e501b584395f41ce2089b5de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100136538"
---
# Get-AzVMDscExtensionStatus

## 摘要
取得虛擬機器的 DSC 延伸處理常式狀態。

## 句法

### GetDscExtension (預設) 
```
Get-AzVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### VMParameterSet
```
Get-AzVMDscExtensionStatus [-VM <PSVirtualMachine>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
AzVMDscExtensionStatus Cmdlet 會針對資源群組中的虛擬機器， **取得** 所需狀態配置 (DSC) 延伸處理常式的狀態設定。
套用配置時，此 Cmdlet 會產生與 Start-DscConfiguration Cmdlet 一致的輸出。

## 示例

### 範例1

取得虛擬機器的 DSC 延伸處理常式狀態。  (自動生成) 

```powershell
<!-- Aladdin Generated Example --> 
Get-AzVMDscExtensionStatus -Name 'AgentPool01' -ResourceGroupName myresourcegroup -VMName 'VM01'
```

## 參數

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

### -名稱
指定代表延伸的 Azure 資源管理員資源的名稱。
Set-AzVMDscExtension Cmdlet 會將此名稱設定為 AzVMDscExtensionStatus，這是所使用的相同值。
只有在您變更了 Set Cmdlet 中的預設名稱，或在資源管理器範本中使用不同的資源名稱時，才能指定此參數。

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定虛擬機器之資源群組的名稱。

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
指定副檔名所在的虛擬機器物件。

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: VMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VMName
指定此 Cmdlet 取得 DSC 延伸狀態的虛擬機器名稱。

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### System.object

## 輸出

### PSVirtualMachineInstanceView 中的 [計算] 命令

## 筆記

## 相關連結

[Set-AzVMDscExtension](./Set-AzVMDscExtension.md)


