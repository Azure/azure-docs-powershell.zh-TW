---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 453AEA42-E29C-4FF2-9210-0DD88B77DC07
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29c7f8bc814ddf5295064d89eeaf34c8e7274916
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967954"
---
# Get-WAPackCloudVMRoleSizeProfile

## 摘要
取得雲端 VM 角色大小設定檔物件。

## 句法

### 空白 (預設) 
```
Get-WAPackCloudVMRoleSizeProfile [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### FromName
```
Get-WAPackCloudVMRoleSizeProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
**WAPackCloudVMRoleSizeProfile** Cmdlet 會取得虛擬機器的雲端 VM 角色大小設定檔物件。

## 示例

### 範例1：使用名稱取得雲端 VM 角色大小設定檔
```
PS C:\> Get-WAPackCloudVMRoleSizeProfile -Name "Small"
```

這個命令會取得名為 Small 的大小設定檔。

### 範例2：取得所有雲端 VM 角色大小設定檔
```
PS C:\> Get-WAPackCloudVMRoleSizeProfile
```

這個命令會取得所有大小設定檔。

## 參數

### -名稱
指定雲端 VM 角色大小設定檔的名稱。

```yaml
Type: String
Parameter Sets: FromName
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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

## 筆記

## 相關連結

[WAPackVM](./Get-WAPackVM.md)


