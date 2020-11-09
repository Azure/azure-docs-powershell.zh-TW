---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 064196C3-ABF3-4F3A-A4AB-EB0D27098C70
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
ms.openlocfilehash: babe273e97d2b1b9a1e09959ba252557e2a7e7d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284567"
---
# Set-AzVMExtension

## 摘要
更新擴充屬性或將延伸新增至虛擬機器。

## 句法

### 設定 (預設) 
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-Settings <Hashtable>]
 [-ProtectedSettings <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SettingString
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-SettingString <String>]
 [-ProtectedSettingString <String>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**AzVMExtension** Cmdlet 會更新現有虛擬機器延伸的屬性，或將延伸新增至虛擬機器。

## 示例

### 範例1：使用雜湊資料表修改設定
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "ContosoTest" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -Settings $Settings -ProtectedSettings $ProtectedSettings;
```

前兩個命令使用標準的 Windows PowerShell 語法來建立雜湊資料表，然後將這些雜湊資料表儲存在 $Settings 並 $ProtectedSettings 變數中。
如需詳細資訊，請輸入 `Get-Help about_Hash_Tables` 。
第二個命令包含先前建立並儲存在變數中的兩個值。
最後一個命令會根據 $Settings 和 $ProtectedSettings 的內容，來修改 ResourceGroup11 中名為 VirtualMachine22 的虛擬機器延伸。
此命令會指定包含發行者及延伸類型的其他必要資訊。

### 範例2：使用字串修改設定
```
PS C:\> $SettingsString = '{"fileUris":[],"commandToExecute":""}';
PS C:\> $ProtectedSettingsString = '{"storageAccountName":"' + $stoname + '","storageAccountKey":"' + $stokey + '"}';
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -SettingString $SettingsString -ProtectedSettingString $ProtectedSettingsString ;
```

前兩個命令會建立包含設定的字串，然後將它們儲存在 $SettingsString 並 $ProtectedSettingsString 變數中。
最後一個命令會根據 $SettingsString 和 $ProtectedSettingsString 的內容，來修改 ResourceGroup11 中名為 VirtualMachine22 的虛擬機器延伸。
此命令會指定包含發行者及延伸類型的其他必要資訊。

## 參數

### -AsJob
在背景中執行 Cmdlet

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

### -DisableAutoUpgradeMinorVersion
表示此 Cmdlet 可防止 Azure 來賓代理程式自動將延伸更新為較新的次要版本。
根據預設，這個 Cmdlet 可讓來賓代理程式更新延伸。

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

### -ExtensionType
指定延伸類型。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Type

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ForceRerun
表示此 Cmdlet 會強制在虛擬機器上重新執行相同的延伸設定，而不需卸載並重新安裝延伸。
這個值可以是與目前值不同的任何字串。
如果 forceUpdateTag 未變更，處理常式仍會套用公用或受保護設定的更新。

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
指定延伸的名稱。

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
在作業完成之前，立即開始作業並立即返回。 若要判斷該作業是否已順利完成，請使用一些其他的機制。

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

### -ProtectedSettings
以雜湊資料表的方式指定延伸的專用配置。
這個 Cmdlet 會加密私人配置。

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Settings
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProtectedSettingString
以字串形式指定延伸的專用配置。
這個 Cmdlet 會加密私人配置。

```yaml
Type: System.String
Parameter Sets: SettingString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Publisher
指定延伸發行者的名稱。
發行者在註冊延伸時提供名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定虛擬機器之資源群組的名稱。

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

### -設定
以雜湊資料表的方式指定延伸的公用配置。
這個 Cmdlet 不會加密公用配置。

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Settings
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SettingString
以字串形式指定延伸的公用配置。
這個 Cmdlet 不會加密公用配置。

```yaml
Type: System.String
Parameter Sets: SettingString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TypeHandlerVersion
指定此虛擬機器要使用的副檔名版本。

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
這個 Cmdlet 會修改此參數指定之虛擬機器的延伸。

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
在執行 Cmdlet 之前提示您進行確認。

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
顯示在執行 Cmdlet 時會發生什麼情況。
未執行 Cmdlet。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### System.object

### [System.object] 集合. Hashtable

### SwitchParameter 的系統管理功能

## 輸出

### PSAzureOperationResponse 中的 [計算] 命令

## 筆記

## 相關連結

[AzVMExtension](./Get-AzVMExtension.md)

[移除-AzVMExtension](./Remove-AzVMExtension.md)


