---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
ms.openlocfilehash: 1ac6f9b17f954361d95e6855a618c7dbbf3d20f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914901"
---
# Get-AzVmssVM

## 簡介
獲得 VMSS 虛擬機器的屬性。

## 語法

### DefaultParameter (預設) 
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### FriendMethod
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**Get-Az Vmss VM Cmdlet** 會取得虛擬機器的虛擬機器縮放集模型 (VMSS) 實例視圖。
模型視圖是使用者指定的虛擬機器屬性。
實例視圖是虛擬機器的實例層級狀態。
指定 *狀態* 參數以僅取得虛擬機器的實例視圖。

## 例子

### 範例 1：取得 VMSS 虛擬機器的屬性
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

此命令會獲得名為 VMSS001 的 VMSS 虛擬機器屬性，該虛擬機器屬於名為 Group001 的資源群組。
由於命令未指定 *InstanceView* 參數，因此 Cmdlet 會獲得虛擬機器的模型視圖。

### 範例 2：取得 VMSS 虛擬機器的模型視圖屬性
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

此命令會獲得名為 VMSS004 的 VMSS 虛擬機器屬性，該虛擬機器屬於名為 Group002 的資源群組。
該命令會取得儲存在變數中的實例識別碼$ID取得模型視圖。

### 範例 3：取得 VMSS 虛擬機器的實例視圖屬性
```
PS C:\> Get-AzVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

此命令會獲得名為 VMSS004 的 VMSS 虛擬機器屬性，該虛擬機器屬於名為 Group002 的資源群組。
由於命令指定 *InstanceView* 參數，因此 Cmdlet 會獲得虛擬機器的實例視圖。
該命令會取得儲存在變數中的實例識別碼$ID取得實例視圖。

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

### -InstanceId
指定取得模型視圖的實例識別碼。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InstanceView
表示此 Cmdlet 僅會獲得虛擬機器的實例視圖。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
指定 VMSS 的資源組名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMScaleSetName
為 VMSS 的名稱命名。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
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

### Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSetVT

## 筆記

## 相關連結

[Set-AzEvssVM](./Set-AzVmssVM.md)

[Get-AzEvss](./Get-AzVmss.md)


