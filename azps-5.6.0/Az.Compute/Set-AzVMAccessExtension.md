---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAccessExtension.md
ms.openlocfilehash: 3b5d877186ec82cad5246b122908eb0ca19ab47c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914878"
---
# Set-AzVMAccessExtension

## 簡介
新增 VMAccess 擴充功能至虛擬機器。

## 語法

```
Set-AzVMAccessExtension [-Credential <PSCredential>] [-ResourceGroupName] <String> [-VMName] <String>
 [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 描述
**Set-Az VMAccessExtension** Cmdlet 會將虛擬機器 Access (VMAccess) Virtual Machine VMAccess Extension 新增到虛擬機器。 VMAccess Extension 可用來設定暫時密碼，登入電腦後應該立即變更密碼。 Windows 網網域控制站不支援此功能。

## 例子

### 範例 1：新增 VMAccess 擴充功能
```powershell
PS C:\> Set-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.4" -UserName "PFuller" -Password "Password"
```

此命令會新增 ResourceGroup11 中 VirtualMachine07 虛擬機器的 VMAccess 擴充功能。
命令會指定 VMAccess 的名稱和類型處理常式版本。

### 範例 2

新增 VMAccess 擴充功能至虛擬機器。  (自動) 

```powershell <!-- Aladdin Generated Example --> 
Set-AzVMAccessExtension -Credential <PSCredential> -Location 'Central US' -Name 'ContosoTest' -ResourceGroupName 'ResourceGroup11' -TypeHandlerVersion '2.4' -VMName 'VirtualMachine07'
```

## 參數

### -認證
將虛擬機器的使用者名稱和密碼指定為 **PSCredential** 物件。
如果您在 VM 上輸入的名稱與目前的本地系統管理員帳戶不同，VMAccess 擴充功能會新增具有該名稱的當地系統管理員帳戶，並將您指定的密碼指派給該帳戶。 如果 VM 上的本地系統管理員帳戶存在，它會重設密碼，如果帳戶已停用，VMAccess 擴充功能就會啟用。
若要取得認證，請使用 Get-Credential Cmdlet。
如需要詳細資訊，請鍵入 `Get-Help Get-Credential` 。

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -DisableAutoUpgradeMinorVersion
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ForceRerun
表示此 Cmdlet 強制在虛擬機器上重新進行相同的擴充功能組配置，而不需要卸載並重新安裝擴充功能。
該值可以是與目前值不同的任何字串。
如果未變更 forceUpdateTag，處理常式仍然會使用公用或受保護的設定更新。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -位置
指定虛擬機器的位置。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -名稱
指定此 Cmdlet 新增的副檔名。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NoWait
啟動作業，並立即在作業完成之前返回。 若要判斷作業是否成功完成，請使用一些其他機制。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
指定虛擬機器的資源組名。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TypeHandlerVersion
指定要用於此虛擬機器的擴充功能版本。
若要取得版本，請執行 Get-AzVMExtensionImage Cmdlet，其值為 Microsoft.Compute for *PublisherName* 參數，而 VMAccessAgent 為 *Type* 參數。 typeHandlerVersion 必須是 2.0 或更大的版本，因為版本 1 已被使用。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
指定虛擬機器的名稱。
此 Cmdlet 會為此參數指定的虛擬機器新增 VMAccess。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -確認
執行 Cmdlet 之前，提示您確認。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示 Cmdlet 執行時會發生什麼情況。
不會執行 Cmdlet。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### System.Management.Automation.PSCredential

### System.String

### System.Management.Automation.SwitchParameter

## 輸出

### Microsoft.Azure.Commands.Compute.models.PSAzureOperationResponse

## 筆記

## 相關連結

[Get-AzEVAccessExtension](./Get-AzVMAccessExtension.md)

[Remove-AzEVAccessExtension](./Remove-AzVMAccessExtension.md)

[Set-AzVMExtension](./Set-AzVMExtension.md)

[Get-Az解說ExtensionImage](./Get-AzVMExtensionImage.md)


