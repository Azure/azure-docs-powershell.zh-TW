---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FDEDBF4F-7507-43FF-A983-7E431C0C1950
online version: ''
schema: 2.0.0
ms.openlocfilehash: 967fbaf83efa12bd305fc9fe075a9abffdd62dc3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967181"
---
# Add-AzureDataDisk

## 摘要
將資料磁片新增至虛擬機器。

## 句法

### CreateNew (預設) 
```
Add-AzureDataDisk [-CreateNew] [-DiskSizeInGB] <Int32> [-DiskLabel] <String> [-LUN] <Int32>
 [-MediaLocation <String>] [-HostCaching <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Import
```
Add-AzureDataDisk [-Import] [-DiskName] <String> [-LUN] <Int32> [-HostCaching <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### ImportFrom
```
Add-AzureDataDisk [-ImportFrom] [-DiskLabel] <String> [-LUN] <Int32> -MediaLocation <String>
 [-HostCaching <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## 說明
**載入 AzureDataDisk** Cmdlet 會將新的或現有的資料磁片新增至 Azure 虛擬電腦物件。
使用 *CreateNew* 參數來建立具有指定大小和標籤的新資料磁片。
使用匯 *入* 參數，從影像存放庫附加現有的磁片。
使用 *ImportFrom* 參數，在儲存空間帳戶的 blob 中附加現有的磁片。
您可以指定附加資料磁片的主機緩存模式。

## 示例

### 範例1：從知識庫中匯入資料磁片
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Add-AzureDataDisk -Import -DiskName "Disk68" -LUN 0 | Update-AzureVM
```

這個命令會使用 **VirtualMachine07 Cmdlet，** 在 ContosoService 雲端服務中取得名為的虛擬機器的虛擬機器物件。
命令會使用管線運算子將它傳遞到目前的 Cmdlet。
該命令會將現有的資料磁片從儲存庫附加到虛擬機器。
資料磁片的 LUN 為0。
此命令會使用 **add-azurevm** Cmdlet 來更新虛擬機器以反映您所做的變更。

### 範例2：新增資料磁片
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine08" | Add-AzureDataDisk -CreateNew -DiskSizeInGB 128 -DiskLabel "main" -LUN 0 | Update-AzureVM
```

這個命令會取得名為 VirtualMachine08 的虛擬機器的虛擬機器物件。
命令會將它傳遞到目前的 Cmdlet。
該命令會附加一個名為 MyNewDisk 的新資料磁片。
這個 Cmdlet 會在目前訂閱的預設儲存空間帳戶中，在 vhd 容器中建立磁片。
此命令會更新虛擬機器以反映您所做的變更。

### 範例3：從指定的位置新增資料磁片
```
PS C:\> Get-AzureVM "ContosoService" -Name "Database" | Add-AzureDataDisk -ImportFrom -MediaLocation "https://contosostorage.blob.core.windows.net/container07/Disk14.vhd" -DiskLabel "main" -LUN 0 | Update-AzureVM
```

這個命令會取得名為 Database 的虛擬機器的虛擬電腦物件。
命令會將它傳遞到目前的 Cmdlet。
該命令會從指定的位置附加名為 Disk14 的現有資料磁片。
此命令會更新虛擬機器以反映您所做的變更。

## 參數

### -CreateNew
表示此 Cmdlet 會建立資料磁片。

```yaml
Type: SwitchParameter
Parameter Sets: CreateNew
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskLabel
指定新資料磁片的磁片標籤。

```yaml
Type: String
Parameter Sets: CreateNew, ImportFrom
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskName
指定磁片存放庫中資料磁片的名稱。

```yaml
Type: String
Parameter Sets: Import
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DiskSizeInGB
為新的資料磁片指定邏輯磁片大小（以千百萬位元組計）。

```yaml
Type: Int32
Parameter Sets: CreateNew
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostCaching
指定磁片的主機層級快取設定。
有效值為： 

- 所有 
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

### 匯入
表示此 Cmdlet 會從影像存放庫中匯入現有的資料磁片。

```yaml
Type: SwitchParameter
Parameter Sets: Import
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImportFrom
表示此 Cmdlet 會從儲存空間帳戶的 blob 中匯入現有的資料磁片。

```yaml
Type: SwitchParameter
Parameter Sets: ImportFrom
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
指定虛擬機器中資料磁碟機的邏輯單元號碼 (LUN) 。
有效值為：0到15。
每個資料磁片都必須有唯一的 LUN。

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MediaLocation
指定此 Cmdlet 儲存資料磁片的 Azure 儲存空間帳戶中的 blob 位置。
如果您沒有指定位置，此 Cmdlet 會將資料磁片儲存在目前訂閱預設儲存空間帳戶的 vhd 容器中。
如果 vhd 容器不存在，則 Cmdlet 會建立 vhd 容器。

```yaml
Type: String
Parameter Sets: CreateNew
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ImportFrom
Aliases: 

Required: True
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

### -VM
指定此 Cmdlet 附加資料磁片的虛擬機器物件。
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

[AzureDataDisk](./Get-AzureDataDisk.md)

[Add-azurevm](./Get-AzureVM.md)

[移除-AzureDataDisk](./Remove-AzureDataDisk.md)

[Set-AzureDataDisk](./Set-AzureDataDisk.md)

[更新-Add-azurevm](./Update-AzureVM.md)


