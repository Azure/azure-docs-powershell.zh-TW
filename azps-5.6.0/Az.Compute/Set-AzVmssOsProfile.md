---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
ms.openlocfilehash: 046812a0339a0dd33df140f29e00ec8b882c91cd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903645"
---
# Set-AzVmssOsProfile

## 簡介
設定 VMSS 作業系統配置檔案屬性。

## 語法

```
Set-AzVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 描述
**Set-AzEvssOsProfile** Cmdlet 會設定虛擬機器縮放集作業系統配置檔案屬性。

## 例子

### 範例 1：設定 VMSS 的作業系統配置檔案屬性
```
PS C:\> Set-AzVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

此命令會針對名稱為 Contoso VMSS 的虛擬機器設定作業系統配置檔案屬性。
該命令會設定 VMSS 中所有虛擬機器實例的電腦名稱稱首碼，以進行測試，並提供給系統管理員使用者名稱和密碼。

## 參數

### -AdditionalUnattendContent
指定自動執行的內容物件。
您可以使用Add-AzVMAdditionalUnattendContent建立物件。

```yaml
Type: Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AdminPassword
指定要用於 VMSS 中所有虛擬機器實例的系統管理員密碼。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AdminUsername
指定要用於 VMSS 中所有虛擬機器實例的系統管理員帳戶名稱。 <br>
**Windows 限制：** 無法以 \" 結尾。\" <br>
**不允許的值：** \"系統管理員 \" ， \" 系統管理員 \" ， \" 使用者， \" \" \" user1， \" \" test， \" \" user2， \" \" \" test， user3， \" \" \" admin1， \" \" 1， \" 1， 123， \" \" \" a， \" actuser， \" \" \" adm， \" \" admin2， \" aspnet， \" \" \" backup， \" \" console， \" \" david， \" \" guest， \" \" john， \" \" owner， \" \" root， \" \" server， \" \" sql， \" \" support， \" \" support_388945a0， \" sys， \" \" \" test2， \" \" test3， \" \" user4， \" user5. \" <br>
**Linux 版 (長度) ：1** 個字元 <br>
**Linux (長度) ：64** 個字元 <br>
**Windows (長度) ：20** 個字元  <br>
<li> 若要取得 Linux VM 的根存取權，請參閱在 Azure 的 Linux 虛擬機器 [上使用根許可權](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)。<br>
<li> 有關 Linux 上不應在此欄位中使用的內建系統使用者清單，請參閱選取 Azure 上的 [Linux 使用者名稱](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)。

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

### -ComputerNamePrefix
指定 VMSS 中所有虛擬機器實例的電腦名稱稱首碼。
電腦名稱稱必須長 1 到 15 個字元。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CustomData
指定自訂資料的底數為 64 的編碼字串。
這會解碼為二進位陣列，該陣列會儲存為虛擬機器上的檔案。
二進位陣列的長度上限為 65535 位元組。 <br>
若要針對您的 VM 使用雲端 init，請參閱在建立期間使用[雲端 init 自訂 Linux VM。](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
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

### -LinuxConfigurationDisablePasswordAuthentication
表示此 Cmdlet 會停用密碼驗證。

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -聆聽者
指定 Windows Remote Management (WinRM) 聆聽者。
這會啟用遠端 Windows PowerShell。
您可以使用 Add-AzVmssWinRMListener Cmdlet 來建立聆聽者。

```yaml
Type: Microsoft.Azure.Management.Compute.Models.WinRMListener[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicKey
指定安全命令命令 (SSH) 鍵物件。
您可以使用 Add-AzVMSshPublicKey Cmdlet 來建立物件。

```yaml
Type: Microsoft.Azure.Management.Compute.Models.SshPublicKey[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -機密
指定密碼物件，其中包含要放在虛擬機器上的憑證參照。
您可以使用 Add-AzVmssSecret Cmdlet 來建立機密物件。

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -時區
指定虛擬機器的時區。 例如， \" 太平洋標準時間 \" 。 <br>
可以從[TimeZoneInfo.GetSystemTimeZones TimeZoneInfo.Id時區取得可能的值](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones)。 [](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
指定 VMSS 物件。
您可以使用 New-AzVmssConfig Cmdlet 來建立物件。

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -WindowsConfigurationEnableAutomaticUpdate
指出 VMSS 中的虛擬機器是否已啟用自動更新。

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WindowsConfigurationProvisionMSAGEnt
指出是否應該在 VMSS 的虛擬機器上部署虛擬機器代理程式。

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示 Cmdlet 執行時會發生什麼情況。 不會執行 Cmdlet。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSet

### System.String

### System.Nullable'1[[System.Boolean， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]

### Microsoft.Azure.management.Compute.models.AdditionalUnattendContent[]

### Microsoft.Azure.management.Compute.models.WinRMListener[]

### Microsoft.Azure.management.Compute.models.SshPublicKey[]

### Microsoft.Azure.management.Compute.models.VaultSecretGroup[]

## 輸出

### Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSet

## 筆記

## 相關連結

[Add-AzVMAdditionalUnattendContent](./Add-AzVMAdditionalUnattendContent.md)

[Add-AzEvssWinRMListener](./Add-AzVmssWinRMListener.md)

[Add-AzMSshPublicKey](./Add-AzVMSshPublicKey.md)

[Add-AzEvssSecret](./Add-AzVmssSecret.md)

[New-AzEvssConfig](./New-AzVmssConfig.md)


