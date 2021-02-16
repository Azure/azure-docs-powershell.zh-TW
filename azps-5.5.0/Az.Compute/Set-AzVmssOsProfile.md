---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
ms.openlocfilehash: 71bd8ca26755118a4bb9c075ae89bad765922f3d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100141194"
---
# Set-AzVmssOsProfile

## 摘要
設定 VMSS 作業系統配置檔案屬性。

## 句法

```
Set-AzVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**AzVmssOsProfile** Cmdlet 會設定虛擬機器縮放設定作業系統配置檔案屬性。

## 示例

### 範例1：設定 VMSS 的作業系統配置檔案屬性
```
PS C:\> Set-AzVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

這個命令會為屬於名為 ContosoVMSS 之 VMSS 的虛擬機器設定作業系統配置檔案屬性。
此命令會為 VMSS 中的所有虛擬機器實例設定電腦名稱稱首碼，以測試並提供系統管理員的使用者名稱和密碼。

## 參數

### -AdditionalUnattendContent
指定無人參與的內容物件。
您可以使用 Add-AzVMAdditionalUnattendContent 來建立物件。

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
**僅限 Windows 的限制：** 無法結束 \" 。\" <br>
不 **允許的值：** \"administrator \" 、 \" admin \" 、 \" user \" 、 \" user1 \" 、 \" test \" 、 \" 使用者 \" \" 2、 \" \" \" 123、user3、 \" admin1 \" 、 \" 1 \" 、 \" \" 、 \" a \" 、 \" actuser、、 \" \" \" \" admin2 \" 、 \" aspnet \" 、 \" 備份 \" support_388945a0、 \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" 主機、test2、test3、、user4、user5、、、、、、、、、、、、、、、、 <br>
**最小長度 (Linux) ：** 1 個字元 <br>
**最大長度 (Linux) ：** 64 字元 <br>
**(Windows) 的最大長度：** 20 個字元  <br>
<li> 如需 Linux VM 的根目錄存取權，請參閱在 [Azure 中使用 linux 虛擬機器上的根許可權](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)。<br>
<li> 如需 Linux 上不應在這個欄位中使用之內建系統使用者的清單，請參閱 [在 Azure 上選取 [Linux 的使用者名稱](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)]。

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
電腦名稱稱的長度必須是1到15個字元。

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
指定自訂資料的基本64編碼字串。
這會解碼為二進位陣列，並儲存為虛擬機器上的檔案。
二進位陣列的最大長度為65535個位元組。 <br>
若要針對您的 VM 使用雲端初始化，請參閱 [在建立期間使用雲端初始化自訂 LINUX VM](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)。

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

### -LinuxConfigurationDisablePasswordAuthentication
表示這個 Cmdlet 停用密碼驗證。

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

### -監聽器
指定 Windows 遠端系統管理 (WinRM) 偵聽程式。
這會啟用遠端 Windows PowerShell。
您可以使用 Add-AzVmssWinRMListener Cmdlet 來建立偵聽程式。

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
指定 SSH) 公用金鑰組象 (的安全 Shell。
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

### 密碼
指定包含要放在虛擬機器上之憑證參照的機密物件。
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
可能的值可以是 [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) 從 [TimeZoneInfo](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones)傳回的時區值。

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
指出是否已針對自動更新啟用 VMSS 中的虛擬機器。

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

### -WindowsConfigurationProvisionVMAgent
指出是否應該在 VMSS 的虛擬機器上預配虛擬機器代理程式。

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
在執行 Cmdlet 之前提示您進行確認。

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
顯示在執行 Cmdlet 時會發生什麼情況。 未執行 Cmdlet。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### PSVirtualMachineScaleSet 中的 [計算] 命令。

### System.object

### "CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]

### AdditionalUnattendContent [] 的計算模型。

### WinRMListener [] 的計算模型。

### SshPublicKey [] 的計算模型。

### VaultSecretGroup [] 的計算模型。

## 輸出

### PSVirtualMachineScaleSet 中的 [計算] 命令。

## 筆記

## 相關連結

[附加 AzVMAdditionalUnattendContent](./Add-AzVMAdditionalUnattendContent.md)

[附加 AzVmssWinRMListener](./Add-AzVmssWinRMListener.md)

[附加 AzVMSshPublicKey](./Add-AzVMSshPublicKey.md)

[附加 AzVmssSecret](./Add-AzVmssSecret.md)

[新-AzVmssConfig](./New-AzVmssConfig.md)


