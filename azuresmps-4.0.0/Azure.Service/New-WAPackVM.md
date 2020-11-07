---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: AA7BD103-5C91-4E3B-9E46-2CAEDA5BA615
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8f5643756cfad93399664298378e97264dedc2f
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/08/2020
ms.locfileid: "93968844"
---
# New-WAPackVM

## 摘要
建立虛擬機器。

## 句法

### CreateVMFromTemplate (預設) 
```
New-WAPackVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential> [-VNet <VMNetwork>]
 [-ProductKey <String>] [-Windows] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### CreateLinuxVMFromTemplate
```
New-WAPackVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential> [-VNet <VMNetwork>] [-Linux]
 [-AdministratorSSHKey <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### CreateVMFromOSDisk
```
New-WAPackVM -Name <String> [-VNet <VMNetwork>] -OSDisk <VirtualHardDisk> -VMSizeProfile <HardwareProfile>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
這些主題已棄用，未來將會移除。
本主題描述 Microsoft Azure PowerShell 模組的0.8.1 版本中的 Cmdlet。
若要找出您正在使用的模組版本，請從 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。

**新的-WAPackVM** Cmdlet 會建立虛擬機器。

## 示例

### 範例1：使用範本建立 Windows 作業系統的虛擬機器
```
PS C:\> $Credentials = Get-Credential PS C:\> $Template = Get-WAPackVMTemplate -Name "ContosoTemplate04"PS C:\> New-WAPackVM -Name "ContosoV023" -Template $Template -VMCredential $Credentials -Windows
```

第一個命令會建立一個 **PSCredential** 物件，然後將它儲存在 $Credentials 變數中。
此 Cmdlet 會提示您輸入帳戶和密碼。
如需詳細資訊，請輸入 `Get-Help Get-Credential` 。

第二個命令會使用 **WAPackVMTemplate** Cmdlet 取得名為 ContosoTemplate04 的虛擬機器範本，然後將它儲存在 $Template 變數中。

最終命令會根據 $Template 變數中儲存的範本，建立一個名為 ContosoV023 的虛擬機器。
此命令會指定 *windows* 參數，因此虛擬機器必須執行 windows 作業系統版本。

### 範例2：使用範本建立 Linux 作業系統的虛擬機器
```
PS C:\> $Credentials = Get-Credential
PS C:\> $Template = Get-WAPackVMTemplate -Name "ContosoTemplate19"
PS C:\> New-WAPackVM -Linux -Name "ContosoV028" -Template $Template -VMCredential $Credentials
```

第一個命令會建立一個 **PSCredential** 物件，然後將它儲存在 $Credentials 變數中。

第二個命令會使用 **WAPackVMTemplate** Cmdlet 取得名為 ContosoTemplate19 的虛擬機器範本，然後將它儲存在 $Template 變數中。

最終命令會根據 $Template 變數中儲存的範本，建立一個名為 ContosoV028 的虛擬機器。
此命令會指定 *Linux* 參數，因此虛擬機器必須執行 Linux 作業系統版本。

### 範例3：從作業系統磁片和大小設定檔建立虛擬機器
```
PS C:\> $OSDisk = Get-WAPackVMOSDisk -Name "ContosoDiskOS"
PS C:\> $SizeProfile = Get-WAPackVMSizeProfile -Name "MediumSizeVM"
PS C:\> New-WAPackVM -Name "ContosoV073" -OSDisk $OSDisk -VMSizeProfile $SizeProfile
```

第一個命令會使用 **WAPackVMOSDisk** Cmdlet 取得名為 ContosoDiskOS 的作業系統磁片，然後將它儲存在 $OSDisk 變數中。

第二個命令會使用 **WAPackVMSizeProfile** Cmdlet 取得名為 MediumSizeVM 的大小設定檔，然後將它儲存在 $SizeProfile 變數中。

最後一個命令會從儲存在 $OSDisk 的作業系統磁片和 $SizeProfile 中儲存的大小設定檔，建立一個名為 ContosoV073 的虛擬機器。

## 參數

### -AdministratorSSHKey
指定管理員帳戶 (SSH) 金鑰的安全 Shell。

```yaml
Type: String
Parameter Sets: CreateLinuxVMFromTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Linux
表示 Cmdlet 會建立虛擬機器來執行 Linux 作業系統。

```yaml
Type: SwitchParameter
Parameter Sets: CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -名稱
指定虛擬機器的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OSDisk
指定作業系統磁片做為 **VirtualHardDisk** 物件。
若要取得作業系統磁片，請使用 **WAPackVMOSDisk** Cmdlet。

```yaml
Type: VirtualHardDisk
Parameter Sets: CreateVMFromOSDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProductKey
指定產品金鑰。
產品金鑰是一個用於識別產品授權的25位數數位。
針對您打算在虛擬機器或主機上安裝的作業系統，使用產品金鑰。

```yaml
Type: String
Parameter Sets: CreateVMFromTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -範本
指定範本。
這個 Cmdlet 會根據您指定的範本建立虛擬機器。
若要取得範本物件，請使用 Get-WAPackVMTemplate Cmdlet。

```yaml
Type: VMTemplate
Parameter Sets: CreateVMFromTemplate, CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMCredential
指定本機系統管理員帳戶的認證。
若要取得 **PSCredential** 物件，請使用 **取得認證** Cmdlet。
如需詳細資訊，請輸入 `Get-Help Get-Credential` 。

```yaml
Type: PSCredential
Parameter Sets: CreateVMFromTemplate, CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMSizeProfile
將虛擬機器的大小設定檔指定為 **HardwareProfile** 物件。
若要取得大小設定檔，請使用 **WAPackVMSizeProfile** Cmdlet。

```yaml
Type: HardwareProfile
Parameter Sets: CreateVMFromOSDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VNet
指定虛擬網路。
此 Cmdlet 會將虛擬機器連接至您指定的虛擬網路。
若要取得虛擬網路，請使用 **WAPackVNet** Cmdlet。

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Windows
表示 Cmdlet 會建立虛擬機器來執行 Windows 作業系統。

```yaml
Type: SwitchParameter
Parameter Sets: CreateVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

## 筆記

## 相關連結

[WAPackVM](./Get-WAPackVM.md)

[移除-WAPackVM](./Remove-WAPackVM.md)

[重新開機-WAPackVM](./Restart-WAPackVM.md)

[Resume-WAPackVM](./Resume-WAPackVM.md)

[Set-WAPackVM](./Set-WAPackVM.md)

[開始-WAPackVM](./Start-WAPackVM.md)

[停止 WAPackVM](./Stop-WAPackVM.md)

[暫停-WAPackVM](./Suspend-WAPackVM.md)

[WAPackVMSizeProfile](./Get-WAPackVMSizeProfile.md)

[WAPackVMTemplate](./Get-WAPackVMTemplate.md)

[WAPackVMOSDisk](./Get-WAPackVMOSDisk.md)


