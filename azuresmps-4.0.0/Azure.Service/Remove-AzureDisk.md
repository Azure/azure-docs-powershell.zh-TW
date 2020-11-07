---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 75A50C59-28D1-4D29-A420-D24BF479F79E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29e5e7e0bc2fcc0ce93186cf966f18d6c9c3e372
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967603"
---
# Remove-AzureDisk

## 摘要
從 Azure 磁片資訊庫移除磁片。

## 句法

```
Remove-AzureDisk [-DiskName] <String> [-DeleteVHD] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## 說明
**AzureDisk** Cmdlet 會從目前訂閱的 Azure 磁片資訊庫中移除磁片。
根據預設，這個 Cmdlet 不會從 blob 儲存體中刪除虛擬硬碟 (VHD) 檔案。
若要刪除 VHD，請指定 *DeleteVHD* 參數。

## 示例

### 範例1：移除磁片
```
PS C:\> Remove-AzureDisk -DiskName "ContosoDataDisk"
```

這個命令會從磁片存放庫中移除名為 ContosoDataDisk 磁片的磁片。
該命令不會刪除 VHD。

### 範例2：移除並刪除磁片
```
PS C:\> Remove-AzureDisk -DiskName "ContosoDataDisk" -DeleteVHD
```

這個命令會從磁片存放庫中移除名為 ContosoDataDisk 磁片的磁片。
這個命令會指定 DeleteVHD 參數。
因此，命令會從 Azure 儲存空間中刪除 VHD。

## 參數

### -DeleteVHD
表示此 Cmdlet 會從 blob 儲存體中移除 VHD。

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

### -DiskName
指定此 Cmdlet 移除之磁片儲備庫中的資料磁片名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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

[AzureDisk](./Get-AzureDisk.md)

[更新-AzureDisk](./Update-AzureDisk.md)


