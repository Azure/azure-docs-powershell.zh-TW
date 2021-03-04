---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: 75eb0ef60443cdbf2dfe3fa53202d3c8141d4888
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911750"
---
# Set-AzVMOperatingSystem

## 簡介
設定虛擬機器的作業系統屬性。

## 語法

### Windows (預設) 
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-EnableHotpatching]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WindowsWinRmHttps
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-EnableHotpatching] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WindowsDisableMSAGEnt
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-EnableHotpatching]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WindowsDisableWINAgentWinRmHttps
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-EnableHotpatching] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Linux
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String> [-Credential] <PSCredential>
 [[-CustomData] <String>] [-PatchMode <String>] [-DisablePasswordAuthentication]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**Set-Az VIRTUALOperatingSystem** Cmdlet 會設定虛擬機器的作業系統屬性。
您可以指定登入認證、電腦名稱稱和作業系統類型。

## 例子

### 範例 1：設定新虛擬機器的作業系統屬性
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform"
```

第一個命令會將密碼轉換為安全字串，然後將它儲存在$SecurePassword變數中。
如需要詳細資訊，請鍵入 `Get-Help ConvertTo-SecureString` 。
第二個命令會為 FullerP 使用者建立認證，以及儲存在 $SecurePassword 中的密碼，然後將認證儲存在 $Credential 變數中。
如需要詳細資訊，請鍵入 `Get-Help New-Object` 。
第三個命令會獲得名為 ResourceGroup11 的資源群組中名為 AvailabilitySet03 的可用性集，然後將該物件儲存在 $AvailabilitySet 變數中。
第四個命令會建立虛擬機器物件，然後將它儲存在$VirtualMachine變數。
該命令會為虛擬機器指定名稱和大小。
虛擬機器屬於儲存在 $AvailabilitySet 的可用性集。
接下來四個命令會指派值給變數，以用於下列命令。
由於您可以直接在 **Set-Az%。OPeratingSystem** 命令中指定這些字串，因此此方法僅適用于可讀性。
不過，您可能會在腳本中使用這類方法。
最後一個命令會設定儲存在 $VirtualMachine 中的虛擬機器作業系統$VirtualMachine。
命令會使用儲存在 $Credential 中的認證。
該命令會針對某些參數使用先前命令中指派的變數。

### 範例 2：設定已啟用熱修補功能的新虛擬機器的作業系統屬性
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform" -EnableHotPatching
```

第一個命令會將密碼轉換為安全字串，然後將它儲存在$SecurePassword變數中。
如需要詳細資訊，請鍵入 `Get-Help ConvertTo-SecureString` 。
第二個命令會為 FullerP 使用者建立認證，以及儲存在 $SecurePassword 中的密碼，然後將認證儲存在 $Credential 變數中。
如需要詳細資訊，請鍵入 `Get-Help New-Object` 。
第三個命令會獲得名為 ResourceGroup11 的資源群組中名為 AvailabilitySet03 的可用性集，然後將該物件儲存在 $AvailabilitySet 變數中。
第四個命令會建立虛擬機器物件，然後將它儲存在$VirtualMachine變數。
該命令會為虛擬機器指定名稱和大小。
虛擬機器屬於儲存在 $AvailabilitySet 的可用性集。
接下來四個命令會指派值給變數，以用於下列命令。
由於您可以直接在 **Set-Az%。OPeratingSystem** 命令中指定這些字串，因此此方法僅適用于可讀性。
不過，您可能會在腳本中使用這類方法。
最後一個命令會設定儲存在 $VirtualMachine 中的虛擬機器作業系統$VirtualMachine。
命令會使用儲存在 $Credential 中的認證。
該命令會針對某些參數使用先前命令中指派的變數。
此命令可在虛擬機器上啟用 Hotpatching。

### 範例 3：設定新 Linux 虛擬機器的作業系統屬性
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -PatchMode "AutomaticByPlatform"
```

第一個命令會將密碼轉換為安全字串，然後將它儲存在$SecurePassword變數中。
如需要詳細資訊，請鍵入 `Get-Help ConvertTo-SecureString` 。
第二個命令會為 FullerP 使用者建立認證，以及儲存在 $SecurePassword 中的密碼，然後將認證儲存在 $Credential 變數中。
如需要詳細資訊，請鍵入 `Get-Help New-Object` 。
第三個命令會獲得名為 ResourceGroup11 的資源群組中名為 AvailabilitySet03 的可用性集，然後將該物件儲存在 $AvailabilitySet 變數中。
第四個命令會建立虛擬機器物件，然後將它儲存在$VirtualMachine變數。
該命令會為虛擬機器指定名稱和大小。
虛擬機器屬於儲存在 $AvailabilitySet 的可用性集。
接下來兩個命令會指派值給變數，以用於下列命令。
最後一個命令會設定儲存在 $VirtualMachine 中的虛擬機器作業系統$VirtualMachine。
命令會使用儲存在 $Credential 中的認證。
該命令會針對某些參數使用先前命令中指派的變數。
該命令將虛擬機器上的修補模式值設定為「AutomaticByPlatform」。

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
將虛擬機器的使用者名稱和密碼指定為 **PSCredential** 物件。
若要取得認證，請使用 Get-Credential Cmdlet。
如需要詳細資訊，請鍵入 `Get-Help Get-Credential` 。

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
指定要傳遞到虛擬機器的字串。 詳細資訊請參閱 [Azure 虛擬機器上的自訂資料](https://docs.microsoft.com/en-us/azure/virtual-machines/custom-data)。
**注意：不建議在自訂資料中儲存敏感性資訊。**


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

### -DisablePasswordAuthentication
表示此 Cmdlet 會停用密碼驗證。

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
停用部署 VM 代理程式。

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

### -EnableHotpatching
讓客戶不需要重新開機，即可修補其 Azure 虛擬機器。 針對 enableHotpatching，'provisionMSAGEnt' 必須設為 True，而 'patchMode' 必須設為 'AutomaticByPlatform'。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Linux
表示作業系統類型為 Linux。

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
指定將來賓內修補模式新修補至IaaS 虛擬機器。<br><br>
可能的值有：<br>
**手動** - 您可以控制修補程式對虛擬機器的適用。 您可以手動在 VM 中申請修補程式，以執行這項操作。 在此模式中，自動更新會停用;屬性 WindowsConfiguration.enableAutomaticUpdates 必須為 False<br>
**AutomaticByOS** - 作業系統會自動更新虛擬機器。 WindowsConfiguration.enableAutomaticUpdates 的屬性必須為 True。 <br >
**AutomaticByPlatform** - 作業系統會自動更新虛擬機器。 屬性布布部為 TRUE，且 WindowsConfiguration.enableAutomaticUpdates 必須為 True

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

### -ProvisionMSEVAgent
表示設定要求虛擬機器代理程式安裝在虛擬機器上。

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
可以從[TimeZoneInfo.GetSystemTimeZones TimeZoneInfo.Id時區取得可能的值](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones)。 [](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id)

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
使用 Cmdlet 建立虛擬機器New-AzVMConfig物件。

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
表示作業系統類型為 Windows。

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
這必須儲存在金鑰保存庫中。

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
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### Microsoft.Azure.Commands.Compute.models.PSVirtualMachine

### System.Management.Automation.SwitchParameter

### System.String

### System.Management.Automation.PSCredential

### System.Uri

## 輸出

### Microsoft.Azure.Commands.Compute.models.PSVirtualMachine

## 筆記

## 相關連結

[Get-AzMS](./Get-AzVM.md)

[New-AzMSCONFIG](./New-AzVMConfig.md)


