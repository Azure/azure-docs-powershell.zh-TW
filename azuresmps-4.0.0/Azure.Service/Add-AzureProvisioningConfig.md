---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 0B3EF123-8424-4CCA-95E8-01301B70CBDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: f84db81f51a4f8d0da605917f99e14c1721cd89d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967828"
---
# Add-AzureProvisioningConfig

## 摘要
新增 Azure 虛擬機器的置備設定。

## 句法

### Windows (預設) 
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-CustomDataFile <String>] [-Windows]
 [-AdminUsername <String>] [-Password <String>] [-ResetPasswordOnFirstLogon] [-DisableAutomaticUpdates]
 [-NoRDPEndpoint] [-TimeZone <String>] [-Certificates <CertificateSettingList>] [-EnableWinRMHttp]
 [-DisableWinRMHttps] [-WinRMCertificate <X509Certificate2>] [-X509Certificates <X509Certificate2[]>]
 [-NoExportPrivateKey] [-NoWinRMEndpoint] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### Linux
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-Linux] [-LinuxUser <String>]
 [-DisableSSH] [-NoSSHEndpoint] [-NoSSHPassword] [-SSHPublicKeys <SSHPublicKeyList>]
 [-SSHKeyPairs <SSHKeyPairList>] [-CustomDataFile <String>] [-Password <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### WindowsDomain
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-CustomDataFile <String>]
 -AdminUsername <String> [-WindowsDomain] [-Password <String>] [-ResetPasswordOnFirstLogon]
 [-DisableAutomaticUpdates] [-NoRDPEndpoint] [-TimeZone <String>] [-Certificates <CertificateSettingList>]
 -JoinDomain <String> -Domain <String> -DomainUserName <String> -DomainPassword <String>
 [-MachineObjectOU <String>] [-EnableWinRMHttp] [-DisableWinRMHttps] [-WinRMCertificate <X509Certificate2>]
 [-X509Certificates <X509Certificate2[]>] [-NoExportPrivateKey] [-NoWinRMEndpoint] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## 說明
**AzureProvisioningConfig** Cmdlet 會將預配配置資訊新增至 Azure 虛擬機器設定。
您可以使用 [配置] 物件來建立虛擬機器。

這個 Cmdlet 支援不同的置備設定，包括獨立 Windows 伺服器、加入 Active Directory 網域的 Windows 伺服器，以及 Linux 版伺服器。

若要建立 Active Directory 網域加入的伺服器，請指定 Active Directory 網域的完整功能變數名稱，以及具有將虛擬機器加入至網域許可權的使用者的網域認證。

## 示例

### 範例1：建立獨立的虛擬機器
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" | New-AzureVM -ServiceName "ContosoService"
```

這個命令會使用 **AzureVMConfig** Cmdlet 來建立虛擬機器設定物件。
命令會使用管線運算子，將該物件傳遞至目前的 Cmdlet。
目前的 Cmdlet 會為執行 Windows 作業系統的虛擬機器新增置備配置。
此設定包含管理員的使用者名稱和密碼。
該命令會將設定傳遞到 **新的 add-azurevm** Cmdlet，這會建立虛擬機器。

### 範例2：建立加入網域的虛擬機器
```
PS C:\> New-AzureVMConfig -Name "DomainVM" -InstanceSize Small -ImageName "Image09" | Add-AzureProvisioningConfig -WindowsDomain -Password "password" -AdminUsername "AdminMain" -ResetPasswordOnFirstLogon -JoinDomain "contoso.com" -Domain "contoso" -DomainUserName "DomainAdminUser" -DomainPassword "DomainPassword" -MachineObjectOU 'OU=AzureVMs,DC=contoso,DC=com' | New-AzureVM -ServiceName "ContosoService"
```

這個命令會建立虛擬機器設定物件，然後將它傳遞到目前的 Cmdlet。
目前的 Cmdlet 會新增虛擬機器的置備設定，以與 contoso 網域加入。
此命令包含將虛擬機器加入至網域所需的使用者名稱和密碼。
此設定要求使用者在第一次登入時變更使用者密碼。
命令會根據置備物件建立虛擬機器。

### 範例3：建立以 Linux 為基礎的虛擬機器
```
PS C:\> New-AzureVMConfig -Name "LinuxVM" -InstanceSize Small -ImageName "LinuxImage03" | Add-AzureProvisioningConfig -Linux -LinuxUser "LinuxRoot" -Password "password" | New-AzureVM -ServiceName "ContosoService"
```

這個命令會建立虛擬機器設定物件，然後將它傳遞到目前的 Cmdlet。
目前的 Cmdlet 會為執行 Linux 作業系統的虛擬機器新增預配配置。
此設定包括超級使用者名稱和密碼。
命令會根據置備物件建立虛擬機器。

### 範例4：建立包含 WinRM 憑證的虛擬機器
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image11" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -WinRMCertificate $certs[0] -X509Certificates $certs[1], $certs[2] | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

第一個命令會從憑證存放區取得憑證，然後將它們儲存在 $certs 的陣列變數中。

第二個命令會建立虛擬機器設定物件，然後將它傳遞到目前的 Cmdlet。
目前的 Cmdlet 會新增包括 WinRM 憑證的預配配置。
命令會根據置備物件建立虛擬機器。

### 範例5：建立已在 HTTP 上啟用 WinRM 的虛擬機器
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image14" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -EnableWinRMHttp | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

這個命令會建立虛擬機器設定物件，然後將它傳遞到目前的 Cmdlet。
目前的 Cmdlet 會新增已在 HTTP 上啟用 WinRM 的置備配置。
命令會根據置備物件建立虛擬機器。

### 範例6：建立已在 HTTPS 上停用 WinRM 的虛擬機器
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -DisableWinRMHttps | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

這個命令會建立虛擬機器設定物件，然後將它傳遞到目前的 Cmdlet。
目前的 Cmdlet 會新增在 HTTPS 上停用 WinRM 的置備設定。
命令會根據置備物件建立虛擬機器。

### 範例7：建立沒有金鑰匯出的虛擬機器
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -X509Certificates $certs[0], $certs[1] -NoExportPrivateKey | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

第一個命令會從憑證存放區取得憑證，然後將它們儲存在 $certs 的陣列變數中。

第二個命令會建立虛擬機器設定物件，然後將它傳遞到目前的 Cmdlet。
目前的 Cmdlet 會新增包含憑證的虛擬機器的提供設定，但不會匯出私人金鑰。
命令會根據置備物件建立虛擬機器。

## 參數

### -AdminUsername
指定此設定在虛擬機器上建立之系統管理員帳戶的使用者名稱。

```yaml
Type: String
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -憑證
指定此設定在虛擬機器上安裝的一組憑證。

```yaml
Type: CertificateSettingList
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomDataFile
指定虛擬機器的資料檔案。
這個 Cmdlet 會將檔案的內容編碼為 Base64。
檔案長度必須小於 64 kb。

如果客體作業系統是 Windows 作業系統，此設定會將這個資料儲存為一個名為%SYSTEMDRIVE%\AzureData\CustomData.bin. 的二進位檔案

如果客體作業系統是 Linux，此設定就會使用 ovf-env.xml 檔案傳遞資料。
[配置] 會將該檔案複製到/var/lib/waagent 目錄。
此代理程式也會在/var/lib/waagent/CustomData. 中儲存 Base64 編碼資料

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableAutomaticUpdates
表示此設定會停用自動更新。

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableGuestAgent
表示此設定會將基礎結構停成服務 (IaaS) 來賓代理程式。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableSSH
表示此設定會停用 SSH。

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWinRMHttps
指示此設定會停用 HTTPS 上的 Windows 遠端系統管理 (WinRM) 。
根據預設，WinRM 是透過 HTTPS 啟用的。

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -網域
指定擁有將電腦新增至網域許可權的帳戶之網域的名稱。

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainPassword
指定擁有將電腦新增至網域許可權之使用者帳戶的密碼。

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainUserName
指定擁有將電腦新增至網域許可權的使用者帳戶名稱。

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableWinRMHttp
指示此設定啟用 WinRM over HTTP。

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationAction
指定這個 Cmdlet 回應資訊事件的方式。

此參數可接受的值為：

- 持續
- 理會
- 看
- SilentlyContinue
- 停止
- 封存

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
指定資訊變數。

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JoinDomain
指定要加入之網域 (FQDN) 的完整功能變數名稱。

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Linux
表示此設定會建立 Linux 配置。

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LinuxUser
指定此設定在虛擬機器上建立之 Linux 系統管理員帳戶的使用者名稱。

```yaml
Type: String
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MachineObjectOU
指定在設定建立電腦帳戶的組織單位 (OU) 的完整名稱。

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoExportPrivateKey
指示此設定不會上傳私用金鑰。

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoRDPEndpoint
表示此設定會建立沒有遠端桌面端點的虛擬機器。

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoSSHEndpoint
表示此設定會建立沒有 SSH 端點的虛擬機器。

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoSSHPassword
表示此設定會建立沒有 SSH 密碼的虛擬機器。

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWinRMEndpoint
指示此設定不會為虛擬機器新增 WinRM 端點。

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Password
指定管理員帳戶的密碼。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -設定檔
指定此 Cmdlet 讀取的 Azure 設定檔。
如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResetPasswordOnFirstLogon
表示虛擬機器要求使用者在第一次登入時變更密碼。

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SSHKeyPairs
指定 SSH 金鑰組。

```yaml
Type: SSHKeyPairList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SSHPublicKeys
指定 SSH 公開金鑰。

```yaml
Type: SSHPublicKeyList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -時區
指定虛擬機器的時區，例如，太平洋標準時間或加拿大中部標準時間。

```yaml
Type: String
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
指定虛擬電腦物件。

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Windows
指示此設定會建立可執行 Windows 作業系統的獨立虛擬機器。

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WindowsDomain
指示此設定會建立已加入 Active Directory 網域的 Windows server。

```yaml
Type: SwitchParameter
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WinRMCertificate
指定此設定會與 WinRM 端點相關聯的憑證。

```yaml
Type: X509Certificate2
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -X509Certificates
指定部署至託管服務的 X509 憑證陣列。

```yaml
Type: X509Certificate2[]
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

## 筆記

## 相關連結

[Add-azurevm](./New-AzureVM.md)

[新-AzureVMConfig](./New-AzureVMConfig.md)


