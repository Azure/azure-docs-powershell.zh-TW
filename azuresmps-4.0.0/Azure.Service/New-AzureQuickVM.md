---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F94584BC-EC02-412D-B089-B98A6FF8F505
online version: ''
schema: 2.0.0
ms.openlocfilehash: a5b7758a7316fa6c34ffe6b5225cd252f39c5d7c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967355"
---
# New-AzureQuickVM

## 摘要
配置並建立 Azure 虛擬機器。

## 句法

### Windows (預設) 
```
New-AzureQuickVM [-Windows] -ServiceName <String> [-Name <String>] -ImageName <String> [-Password <String>]
 [-ReverseDnsFqdn <String>] [-Location <String>] [-AffinityGroup <String>] [-AdminUsername <String>]
 [-Certificates <CertificateSettingList>] [-WaitForBoot] [-DisableWinRMHttps] [-EnableWinRMHttp]
 [-WinRMCertificate <X509Certificate2>] [-X509Certificates <X509Certificate2[]>] [-NoExportPrivateKey]
 [-NoWinRMEndpoint] [-VNetName <String>] [-SubnetNames <String[]>] [-DnsSettings <DnsServer[]>]
 [-HostCaching <String>] [-AvailabilitySetName <String>] [-InstanceSize <String>] [-MediaLocation <String>]
 [-DisableGuestAgent] [-CustomDataFile <String>] [-ReservedIPName <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Linux
```
New-AzureQuickVM [-Linux] -ServiceName <String> [-Name <String>] -ImageName <String> [-Password <String>]
 [-ReverseDnsFqdn <String>] [-Location <String>] [-AffinityGroup <String>] [-LinuxUser <String>] [-WaitForBoot]
 [-SSHPublicKeys <SSHPublicKeyList>] [-SSHKeyPairs <SSHKeyPairList>] [-VNetName <String>]
 [-SubnetNames <String[]>] [-DnsSettings <DnsServer[]>] [-HostCaching <String>] [-AvailabilitySetName <String>]
 [-InstanceSize <String>] [-MediaLocation <String>] [-DisableGuestAgent] [-CustomDataFile <String>]
 [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## 說明
**新的-AzureQuickVM** Cmdlet 會設定並建立 Azure 虛擬機器。
這個 Cmdlet 可以將虛擬機器部署到現有的 Azure 服務。
這個 Cmdlet 也可以建立託管新虛擬機器的 Azure 服務。

## 示例

### 範例1：建立虛擬機器
```
PS C:\> New-AzureQuickVM -Windows -ServiceName "ContosoService17" -Name "VirutalMachine01" -ImageName "Image07" -Password "password" -AdminUsername "AdminMain" -WaitForBoot
```

這個命令會建立在現有的服務中執行 Windows 作業系統的虛擬機器。
這個 Cmdlet 會以指定的映射為虛擬機器基礎。
命令會指定 *WaitForBoot* 參數。
因此，此 Cmdlet 會等待虛擬機器開始進行。

### 範例2：使用憑證建立虛擬機器
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
PS C:\> New-AzureQuickVM -Windows -ServiceName "MySvc1" -name "MyWinVM1" -ImageName "Image07" -Password "password" -AdminUserName "AdminMain" -WinRMCertificate $certs[0] -X509Certificates $certs[1], $certs[2] -WaitForBoot
```

第一個命令會從書店取得憑證，並將其儲存在 $certs 變數中。

第二個命令會建立在現有的服務中執行 Windows 作業系統的虛擬機器。
根據預設，WinRM Https 偵聽程式在虛擬機器上是啟用的。
命令會指定 *WaitForBoot* 參數。
因此，此 Cmdlet 會等待虛擬機器開始進行。
該命令會將 WinRM 憑證及 X509Certificates 上傳到託管服務。

### 範例3：建立執行 Linux 作業系統的虛擬機器
```
PS C:\> New-AzureQuickVM -Linux -ServiceName "ContosoServiceLinux01" -Name "LinuxVirtualMachine01" -ImageName "LinuxImage01" -LinuxUser "RootMain" -Password "password" -Location "Central US"
```

這個命令會建立一個從影像執行 Linux 作業系統的虛擬機器。
這個命令會建立服務來託管新的虛擬機器。
該命令會指定服務的位置。

### 範例4：建立虛擬機器並建立服務以託管新的虛擬機器
```
PS C:\> $Locations = Get-AzureLocation
PS C:\> $Images = Get-AzureVMImage
PS C:\> New-AzureQuickVM -Windows -InstanceSize "Large" -ServiceName "ContosoService03" -Name " VirtualMachine25" -ImageName $images[4].imagename -Password "password" -AdminUsername "AdminMain" -Location $Locations[0].name
```

第一個命令會使用 **AzureLocation** Cmdlet 來取得位置，然後將它們儲存在 $Locations 陣列變數中。

第二個命令會使用 **AzureVMImage** Cmdlet 取得可用的影像，然後將它們儲存在 $Images 陣列變數中。

最後一個命令會建立一個名為 VirtualMachine25 的大型虛擬機器。
虛擬機器會執行 Windows 作業系統。
它是以 $Images 中的其中一個圖像為基礎。
此命令會為新的虛擬機器建立名為 ContosoService03 的服務。
服務位於 $Locations 中的位置。

### 範例5：建立擁有保留 IP 名稱的虛擬機器
```
PS C:\> $Locations = Get-AzureLocation
PS C:\> $Images = Get-AzureVMImage
PS C:\> New-AzureQuickVM -Windows -InstanceSize "Large" -ServiceName "ContosoService04" -Name "VirtualMachine27" -ImageName $Images[4].imagename -Password "password" -AdminUsername "AdminMain" -Location $Locations[0].name -ReservedIPName $ipName
```

第一個命令會取得位置，然後將它們儲存在 $Locations 陣列變數中。

第二個命令會取得可用的影像，然後將它們儲存在 $Images 陣列變數中。

最終命令會根據 $Images 中的其中一個圖像，建立一個名為 VirtualMachine27 的虛擬機器。
命令會在 $Locations 中的位置建立服務。
虛擬機器有保留的 IP 名稱，先前儲存在 $ipName 變數中。

## 參數

### -AdminUsername
指定此 Cmdlet 在虛擬機器上建立之系統管理員帳戶的使用者名稱。

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

### -AffinityGroup
指定虛擬機器的地緣群組。
只有在這個 Cmdlet 為虛擬機器建立 Azure 服務時，才能指定此參數或 *Location* 參數。

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

### -AvailabilitySetName
指定此 Cmdlet 建立虛擬機器之可用性集的名稱。

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

### -憑證
指定此 Cmdlet 用來建立服務的憑證清單。

```yaml
Type: CertificateSettingList
Parameter Sets: Windows
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

如果客體作業系統是 Windows 作業系統，這個 Cmdlet 會將這個資料儲存為一個名為%SYSTEMDRIVE%\AzureData\CustomData.bin. 的二進位檔案。

如果客體作業系統是 Linux，此 Cmdlet 會使用 ovf-env.xml 檔案傳遞資料。
安裝會將該檔案複製到/var/lib/waagent 目錄。
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

### -DisableGuestAgent
表示此 Cmdlet 會將基礎結構停成服務 (IaaS) 提供來賓代理程式。

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

### -DisableWinRMHttps
表示此 Cmdlet 停用 HTTPS 上的 Windows 遠端系統管理 (WinRM) 。
根據預設，WinRM 是透過 HTTPS 啟用的。

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DnsSettings
指定定義新部署之 DNS 設定的 DNS 伺服器物件陣列。
若要建立 **DnsServer** 物件，請使用 **AzureDns** Cmdlet。

```yaml
Type: DnsServer[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableWinRMHttp
表示此 Cmdlet 啟用 WinRM over HTTP。

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostCaching
指定作業系統磁片的主機緩衝模式。
有效值為： 

- 唯讀
- 讀

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

### -ImageName
指定此 Cmdlet 用來建立作業系統磁片的磁片影像名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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

### -InstanceSize
指定實例的大小。
有效值為： 

- ExtraSmall
- 小規模
- 深淺
- 大中型
- ExtraLarge
- A5
- A6
- A7
- A8
- A9
- Basic_A0
- Basic_A1
- Basic_A2
- Basic_A3
- Basic_A4
- Standard_D1
- Standard_D2
- Standard_D3
- Standard_D4
- Standard_D11
- Standard_D12
- Standard_D13
- Standard_D14

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Linux
表示此 Cmdlet 會建立以 Linux 為基礎的虛擬機器。

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
指定此 Cmdlet 在虛擬機器上建立之 Linux 系統管理員帳戶的使用者名稱。

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

### -位置
指定託管虛擬機器的 Azure 資料中心。
如果您指定此參數，則 Cmdlet 會在指定的位置建立 Azure 服務。
只有在這個 Cmdlet 為虛擬機器建立 Azure 服務時，才能指定此參數或 *AffinityGroup* 參數。

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

### -MediaLocation
指定此 Cmdlet 建立虛擬機器磁片的 Azure 儲存位置。

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

### -名稱
指定此 Cmdlet 所建立之虛擬機器的名稱。

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

### -NoExportPrivateKey
指示此設定不會上傳私用金鑰。

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWinRMEndpoint
指示此 Cmdlet 不會為虛擬機器新增 WinRM 端點。

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Password
指定系統管理帳戶的密碼。

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

### -ReservedIPName
指定保留的 IP 名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ReverseDnsFqdn
指定反向 DNS 查詢的完整功能變數名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceName
指定此 Cmdlet 將新的虛擬機器新增至其中的新或現有 Azure 服務的名稱。

如果您指定新服務，此 Cmdlet 會建立它。
若要建立新的服務，您必須指定 *Location* 或 *AffinityGroup* 參數。

如果您指定現有的服務，請勿指定 *Location* 或 *AffinityGroup* 。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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

### -SubnetNames
指定虛擬機器子網的名稱陣列。

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VNetName
指定虛擬機器的虛擬網路名稱。

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

### -WaitForBoot
表示此 Cmdlet 會等待虛擬機器到達狀態 ReadyRole。
如果虛擬機器達到下列其中一種狀態，則 Cmdlet 會失敗： FailedStartingVM、ProvisioningFailed 或 ProvisioningTimeout。

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

### -Windows
表示此 Cmdlet 會建立 Windows 虛擬機器。

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

### -WinRMCertificate
指定此 Cmdlet 與 WinRM 端點相關聯的憑證。

```yaml
Type: X509Certificate2
Parameter Sets: Windows
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
Parameter Sets: Windows
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

[AzureLocation](./Get-AzureLocation.md)

[AzureVMImage](./Get-AzureVMImage.md)

[新-AzureDns](./New-AzureDns.md)


