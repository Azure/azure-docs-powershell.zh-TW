---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 95DCD2EC-8327-4A46-B624-289D0A28F7EA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4614910b8c0ccd36bb8ef75ee98f662cf69a276a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967800"
---
# Get-AzureDisk

## 摘要
取得有關 Azure 磁片資訊庫中磁片的資訊。

## 句法

```
Get-AzureDisk [[-DiskName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## 說明
**AzureDisk** Cmdlet 會取得儲存在目前訂閱之 Azure 磁片資訊庫中之磁片的相關資訊。
這個 Cmdlet 會傳回儲備庫中所有磁片的資訊清單。
若要查看特定磁片的資訊，請指定磁片的名稱。

## 示例

### 範例1：取得磁片相關資訊
```
PS C:\> Get-AzureDisk -DiskName "ContosoDataDisk"
```

這個命令會從磁片資訊庫取得名為 ContosoDataDisk 磁片的資訊資料。

### 範例2：取得所有磁片的相關資訊
```
PS C:\> Get-AzureDisk
```

這個命令會取得磁片資訊庫中所有磁片的相關資訊。

### 範例3：取得磁片相關資訊
```
PS C:\> Get-AzureDisk | Where-Object {$_.AttachedTo -eq $Null } | Format-Table -AutoSize -Property "DiskName","DiskSizeInGB","MediaLink"
```

這個命令會取得磁片資訊庫中目前未連接至虛擬機器之所有磁片的資料。
此命令會取得所有磁片的相關資訊，並將每個物件傳遞到 **物件** Cmdlet。
該 Cmdlet 會刪除 **AttachedTo** 屬性的值不是 $Null 的任何磁片。
命令會使用 [ **Format-table** Cmdlet]，將清單格式化為表格。

## 參數

### -DiskName
指定此 Cmdlet 取得資訊之磁片資訊庫中的磁片名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

## 筆記

## 相關連結

[附加 AzureDisk](./Add-AzureDisk.md)

[移除-AzureDisk](./Remove-AzureDisk.md)

[更新-AzureDisk](./Update-AzureDisk.md)


