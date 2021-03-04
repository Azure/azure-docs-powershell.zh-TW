---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmdscextensionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtensionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtensionStatus.md
ms.openlocfilehash: b17b8198b54a6c1fd85b2f8bcb37b4c73e8be0ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917382"
---
# Get-AzVMDscExtensionStatus

## 簡介
獲得虛擬機器的 DSC 擴充處理常式狀態。

## 語法

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

## 描述
**Get-Az VIRTUALDscExtensionStatus Cmdlet** 會取得資源群組中虛擬機器的所需狀態組態 (DSC) 擴充處理常式的狀態。
當已使用群組原則時，此 Cmdlet 會產生與 Start-DscConfiguration一致的輸出。

## 例子

### 範例 1

獲得虛擬機器的 DSC 擴充處理常式狀態。  (自動) 

```powershell
<!-- Aladdin Generated Example --> 
Get-AzVMDscExtensionStatus -Name 'AgentPool01' -ResourceGroupName myresourcegroup -VMName 'VM01'
```

## 參數

### -DefaultProfile
用於與 azure 通訊的認證、帳戶、租使用者和訂閱。

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
指定代表擴充功能之 Azure Resource Manager 資源的名稱。
此Set-AzVMDscExtension Cmdlet 將這個名稱設定為 Microsoft.Powershell.DSC，這是 **Get-AzCMDscExtensionStatus** 所使用的相同值。
只有在您變更了 Set Cmdlet 中的預設名稱，或在 Resource Manager 範本中使用不同的資源名稱時，才指定此參數。

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
指定虛擬機器的資源組名。

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
指定擴充功能所位於的虛擬機器物件。

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
指定此 Cmdlet 會獲得 DSC 擴充功能狀態的虛擬機器名稱。

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
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### System.String

## 輸出

### Microsoft.Azure.Commands.Compute.models.PSVirtualMachineInstanceView

## 筆記

## 相關連結

[Set-AzMSDscExtension](./Set-AzVMDscExtension.md)


