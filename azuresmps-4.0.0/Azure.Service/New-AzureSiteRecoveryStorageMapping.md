---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2D09422F-82B1-4243-B835-8BF223A6F936
online version: ''
schema: 2.0.0
ms.openlocfilehash: a6f02f333601172341de4fe8a0bf629037f712a5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967421"
---
# New-AzureSiteRecoveryStorageMapping

## 摘要
建立 Azure 儲存空間物件與復原儲存物件之間的對應。

## 句法

```
New-AzureSiteRecoveryStorageMapping -PrimaryStorage <ASRStorage> -RecoveryStorage <ASRStorage>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
**新的-AzureSiteRecoveryStorageMapping** Cmdlet 會在 Azure Site Recovery 管理的主要 Azure 儲存空間物件與復原儲存物件之間建立對應。

## 示例

### 範例1：建立儲存物件與恢復儲存物件之間的對應
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $Storages = Get-AzureSiteRecoveryStorage -Server $Servers[0]
PS C:\> New-AzureSiteRecoveryStorageMapping -PrimaryStorage $Storages[0] -RecoveryStorage $Storages[1]
```

第一個命令 Cmdlet 會使用 **AzureSiteRecoveryServer** Cmdlet，為目前的 Azure Site Recovery 保存庫取得伺服器。
該命令會將網站復原伺服器儲存在 $Servers 陣列變數中。

第二個命令會針對 $Servers 陣列中的第一個伺服器，取得網站復原儲存空間，然後將其儲存在 $Storages 中。

最後一個命令會在主要網路和恢復網路之間建立對應。
該命令會將主要儲存物件指定為 $Storages 的第一個元素。
該命令會將復原儲存物件指定為 $Storages 的第二個元素。

## 參數

### -PrimaryStorage
指定要對應至恢復儲存空間的主要儲存空間。
若要取得 **ASRStorage** 物件，請使用 Get-AzureSiteRecoveryStorage Cmdlet。

```yaml
Type: ASRStorage
Parameter Sets: (All)
Aliases: 

Required: True
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

### -RecoveryStorage
指定復原儲存物件。
這個 Cmdlet 會將主要儲存物件對應至此參數指定的儲存物件。
若要取得 **ASRStorage** 物件，請使用 **AzureSiteRecoveryStorage** 。

```yaml
Type: ASRStorage
Parameter Sets: (All)
Aliases: 

Required: True
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

[AzureSiteRecoveryStorage](./Get-AzureSiteRecoveryStorage.md)

[AzureSiteRecoveryStorageMapping](./Get-AzureSiteRecoveryStorageMapping.md)

[移除-AzureSiteRecoveryStorageMapping](./Remove-AzureSiteRecoveryStorageMapping.md)


