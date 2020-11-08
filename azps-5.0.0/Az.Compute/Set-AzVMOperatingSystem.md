---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: c22e1a09f20eca32cb21056ae45334f0d55ce14b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138939"
---
# Set-AzVMOperatingSystem

## 摘要
設定虛擬機器的作業系統屬性。

## 句法

### Windows (預設) 
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### WindowsWinRmHttps
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WindowsDisableVMAgent
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### WindowsDisableVMAgentWinRmHttps
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Linux
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String> [-Credential] <PSCredential>
 [[-CustomData] <String>] [-DisablePasswordAuthentication] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
**AzVMOperatingSystem** Cmdlet 會設定虛擬機器的作業系統屬性。
您可以指定登入認證、電腦名稱稱及作業系統類型。

## 示例

### 範例1：為新的虛擬機器設定作業系統屬性
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $$VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform"
```

第一個命令會將密碼轉換成安全字串，然後將密碼儲存在 $SecurePassword 變數中。
如需詳細資訊，請輸入 `Get-Help ConvertTo-SecureString` 。
第二個命令會為使用者 FullerP 及儲存在 $SecurePassword 中的密碼建立認證，然後將認證儲存在 $Credential 變數中。
如需詳細資訊，請輸入 `Get-Help New-Object` 。
第三個命令會在名為 [ResourceGroup11] 的資源群組中取得名為 AvailabilitySet03 的可用性集，然後將該物件儲存在 $AvailabilitySet 變數中。
第四個命令會建立一個虛擬電腦物件，然後將它儲存在 $VirtualMachine 變數中。
該命令會將名稱和大小指派給虛擬機器。
虛擬機器屬於儲存在 $AvailabilitySet 的可用性集。
接下來的四個命令會將值指派給要在下列命令中使用的變數。
因為您可以直接在 **AzVMOperatingSystem** 命令中指定這些字串，所以這個方法只適用于可讀性。
不過，您可能會在腳本中使用這種方法。
最終命令會針對儲存在 $VirtualMachine 中的虛擬機器設定作業系統屬性。
命令會使用儲存在 $Credential 中的認證。
此命令會使用在先前命令中為某些參數指定的變數。

## 參數

### -ComputerName
指定電腦的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -認證
指定虛擬機器的使用者名稱和密碼作為 **PSCredential** 物件。
若要取得認證，請使用 Get-Credential Cmdlet。
如需詳細資訊，請輸入 `Get-Help Get-Credential` 。

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CustomData
指定自訂資料的基本64編碼字串。
這會解碼為二進位陣列，並儲存為虛擬機器上的檔案。
二進位陣列的最大長度為65535個位元組。<br>
**注意：請勿在 customData 屬性中傳遞任何機密或密碼**<br>
建立 VM 之後，就無法更新此屬性。 <br>
customData 會傳送至 VM 以儲存為檔案，如需詳細資訊，請參閱 [Azure vm 上的自訂資料](https://azure.microsoft.com/en-us/blog/custom-data-and-cloud-init-on-windows-azure/) <br>
若要針對您的 Linux VM 使用雲端初始化，請參閱 [在建立期間使用雲端初始化自訂 LINUX vm](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init)

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

### -DisablePasswordAuthentication
表示這個 Cmdlet 停用密碼驗證。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DisableVMAgent
停用 [預配 VM 代理程式]。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAutoUpdate
表示此 Cmdlet 啟用自動更新。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Linux
表示作業系統類型是 Linux。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PatchMode
指定訪客內修補到 IaaS 虛擬機器的模式。<br><br>
可能的值包括：<br>
**手動** -將修補程式的應用程式控制至虛擬機器。 您可以在 VM 中手動套用修補程式來執行此動作。 在此模式中，會停用自動更新;屬性 WindowsConfiguration 的 enableAutomaticUpdates 必須是 false<br>
**AutomaticByOS** -虛擬機器將自動由作業系統更新。 WindowsConfiguration 屬性必須為 true。 <br >
**AutomaticByPlatform** -虛擬機器將由 OS 自動更新。 [屬性 provisionVMAgent] 和 WindowsConfiguration enableAutomaticUpdates 必須為 true

```yaml
Type: System.String
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProvisionVMAgent
指示設定需要在虛擬機器上安裝虛擬機器代理程式。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -時區
指定虛擬機器的時區。 例如， \" 太平洋標準時間 \" 。 <br>
可能的值可以是 [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) 從 [TimeZoneInfo](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones)傳回的時區值。

```yaml
Type: System.String
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
指定要設定作業系統屬性的本機虛擬機器物件。
若要取得虛擬機器物件，請使用 Get-AzVM Cmdlet。
使用 New-AzVMConfig Cmdlet 建立虛擬機器物件。

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Windows
表示作業系統類型是 Windows。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WinRMCertificateUrl
指定 WinRM 憑證的 URI。
這需要儲存在金鑰保存庫中。

```yaml
Type: System.Uri
Parameter Sets: WindowsWinRmHttps, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WinRMHttp
表示此作業系統使用 HTTP WinRM。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WinRMHttps
表示此作業系統使用 HTTPS WinRM。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsWinRmHttps, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### PSVirtualMachine 中的 [計算] 命令

### SwitchParameter 的系統管理功能

### System.object

### 系統管理. PSCredential

### 系統 Uri

## 輸出

### PSVirtualMachine 中的 [計算] 命令

## 筆記

## 相關連結

[AzVM](./Get-AzVM.md)

[新-AzVMConfig](./New-AzVMConfig.md)


