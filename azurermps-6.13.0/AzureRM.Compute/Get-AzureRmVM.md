---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVM.md
ms.openlocfilehash: 8601a7cc6a02211a0264030784485a5ecb4d29fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447435"
---
# Get-AzureRmVM

## 摘要
取得虛擬機器的屬性。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### ListAllVirtualMachinesParamSet (預設) 
```
Get-AzureRmVM [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListVirtualMachineInResourceGroupParamSet
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetVirtualMachineInResourceGroupParamSet
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListLocationVirtualMachinesParamSet
```
Get-AzureRmVM -Location <String> [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListNextLinkVirtualMachinesParamSet
```
Get-AzureRmVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmVM** Cmdlet 會取得 Azure 虛擬機器的 [模型] 視圖和 [實例] 視圖。
模型視圖是使用者指定的虛擬機器屬性。
[實例] 視圖是虛擬機器的實例層級狀態。
指定 *Status* 參數，只取得虛擬機器的 [實例] 視圖。

## 示例

### 範例1：取得模型和實例視圖屬性
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

這個命令會取得名為 VirtualMachine07 的虛擬機器的模型視圖和實例視圖屬性。

### 範例2：取得實例視圖屬性
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status
```

這個命令會取得名為 VirtualMachine07 的虛擬機器的屬性。
這個命令會指定 *Status* 參數。
因此，命令只會取得實例視圖屬性。

### 範例3：取得資源群組中所有虛擬機器的屬性
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11"
```

這個命令會取得名為 ResourceGroup11 之資源群組中所有虛擬機器的屬性。

### 範例4：取得您訂閱中的所有虛擬機器
```
PS C:\> Get-AzureRmVM
```

這個命令會取得您訂閱中的所有虛擬機器。

### 範例5：取得位置中的所有虛擬機器。
```
PS C:\> Get-AzureRmVM -Location "westus"
```

這個命令會取得西部美區域中的所有虛擬機器。

## 參數

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

### -DisplayHint
決定虛擬機器物件的顯示方式。
有效值為：-精簡：只顯示最上層屬性--展開：顯示所有層級中的所有屬性

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.DisplayHintType
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases:
Accepted values: Compact, Expand

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -位置
指定虛擬機器的清單位置。

```yaml
Type: System.String
Parameter Sets: ListLocationVirtualMachinesParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -名稱
指定要取得的虛擬機器名稱。

```yaml
Type: System.String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NextLink
指定 [下一步] 連結。

```yaml
Type: System.Uri
Parameter Sets: ListNextLinkVirtualMachinesParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定資源群組的名稱。

```yaml
Type: System.String
Parameter Sets: ListVirtualMachineInResourceGroupParamSet, GetVirtualMachineInResourceGroupParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -狀態
表示此 Cmdlet 只會取得虛擬機器的實例視圖。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

### 系統 Uri

### DisplayHintType 中的 [計算] 命令

## 輸出

### PSVirtualMachine 中的 [計算] 命令

### PSVirtualMachineInstanceView 中的 [計算] 命令

## 筆記

## 相關連結

[新-AzureRmVM](./New-AzureRmVM.md)

[移除-AzureRmVM](./Remove-AzureRmVM.md)

[重新開機-AzureRmVM](./Restart-AzureRmVM.md)

[開始-AzureRmVM](./Start-AzureRmVM.md)

[停止 AzureRmVM](./Stop-AzureRmVM.md)

[更新-AzureRmVM](./Update-AzureRmVM.md)


