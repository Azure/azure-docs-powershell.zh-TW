---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 64EF867E-5142-4317-9552-8BC94117208D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 899ecd0256bc3d6f88b8f942fa488db444a9bb41
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967512"
---
# Set-AzureDataDisk

## 摘要
修改 Azure 虛擬機器上現有資料磁片的主機緩存。

## 句法

### NoResize
```
Set-AzureDataDisk [-HostCaching] <String> [-LUN] <Int32> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### 大小
```
Set-AzureDataDisk [-DiskName] <String> [-ResizedSizeInGB] <Int32> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## 說明
**AzureDataDisk** Cmdlet 會修改 Azure 虛擬機器上現有資料磁片的快取屬性。
指定要透過其邏輯單元號碼來更新的資料磁片 (LUN) 。

## 示例

### 範例1：修改資料磁片的主機緩存
```
PS C:\> Get-AzureVM "ContosoService" | Set-AzureDataDisk -VM "VirtualMachine07" -LUN 2 -HostCaching ReadOnly | Update-AzureVM
```

這個命令會透過使用 **ContosoService Cmdlet 來** 取得在服務上執行的虛擬機器（名為）。
命令會使用管線運算子將它們傳遞至目前的 Cmdlet。
該 Cmdlet 會將名為 VirtualMachine07 之虛擬機器的 LUN 2 的資料磁片設定為使用 ReadOnly 主機緩存。
此命令會使用 **add-azurevm** Cmdlet 來更新虛擬機器以反映您所做的變更。

### 範例2：修改虛擬機器上所有資料磁片的主機緩存
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk | Set-AzureDataDisk -HostCaching ReadWrite | Update-AzureVM
```

這個命令會針對 ContosoService 雲端服務上名為 VirtualMachine07 的虛擬機器取得物件。
命令會將它傳遞給 **AzureDataDisk** Cmdlet，以取得該虛擬機器的資料磁片。
目前的 Cmdlet 會將每個資料磁片的主機緩存模式設定為 ReadWrite。
此命令會更新虛擬機器以反映您所做的變更。

## 參數

### -DiskName
指定此 Cmdlet 修改的資料磁片配置名稱。

```yaml
Type: String
Parameter Sets: Resize
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostCaching

> [!WARNING]
> 磁片 4 TiB 及更大的磁片不支援磁片快取。 如果有多個磁片連接至您的 VM，每個小於 4 TiB 的磁片都會支援快取。
>
> 變更 Azure 磁片的快取設定會分離並重新附加目標磁片。 如果是作業系統磁片，則會重新開機 VM。 在變更磁片快取設定之前，請停止此中斷可能影響的所有應用程式/服務。 如果不遵循這些建議，可能會導致資料損毀。

指定磁片的主機層級快取設定。
有效值為：

- 所有
- 唯讀
- 讀

```yaml
Type: String
Parameter Sets: NoResize
Aliases:

Required: True
Position: 0
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

### -LUN
指定虛擬機器中資料磁碟機的 LUN。
有效值為：0到15。

```yaml
Type: Int32
Parameter Sets: NoResize
Aliases:

Required: True
Position: 1
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

### -ResizedSizeInGB
指定資料磁片的新大小（以 gb 為位元組）。
新大小必須大於目前的大小。

```yaml
Type: Int32
Parameter Sets: Resize
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
指定附加至資料磁片的虛擬機器物件。
若要取得虛擬機器物件，請使用 **add-azurevm** Cmdlet。

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

## 筆記

## 相關連結

[附加 AzureDataDisk](./Add-AzureDataDisk.md)

[Add-azurevm](./Get-AzureVM.md)

[AzureDataDisk](./Get-AzureDataDisk.md)

[移除-AzureDataDisk](./Remove-AzureDataDisk.md)

[更新-Add-azurevm](./Update-AzureVM.md)


