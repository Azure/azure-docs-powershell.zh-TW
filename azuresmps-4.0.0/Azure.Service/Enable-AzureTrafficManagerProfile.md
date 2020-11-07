---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 51A1B699-03F6-4BB9-9186-FDFFB094F16A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 72420272e04519fa888660f8ccb6d432ecb0ee5d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967821"
---
# Enable-AzureTrafficManagerProfile

## 摘要
啟用流量管理器設定檔。

## 句法

```
Enable-AzureTrafficManagerProfile -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
**Enable-AzureTrafficManagerProfile** Cmdlet 可啟用 Microsoft Azure 流量管理器設定檔。
指定 *PassThru* 參數，以顯示該作業是否會成功。

## 示例

### 範例1：啟用流量管理器設定檔
```
PS C:\>Enable-AzureTrafficManagerProfile -Name "MyProfile"
```

這個命令會啟用一個名為 MyProfile 的流量管理器設定檔。

### 範例2：啟用流量管理器設定檔並顯示結果
```
PS C:\>Enable-AzureTrafficManagerProfile -Name "MyProfile" -PassThru
True
```

這個命令會啟用一個名為 MyProfile 的流量管理器設定檔，並顯示該命令是否已成功完成。

## 參數

### -名稱
指定要啟用的流量管理器設定檔名稱。

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

### -PassThru
如果操作成功，則傳回 $True;否則，請 $False。
根據預設，這個 Cmdlet 不會產生任何輸出。

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

### -設定檔
指定此 Cmdlet 讀取的 Azure 設定檔。 如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。

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

### System.object
這個 Cmdlet 會產生 $True 或 $False。
如果操作成功且您指定 *PassThru* 參數，則此 Cmdlet 會傳回 $True 的值。

## 筆記

## 相關連結

[Disable-AzureTrafficManagerProfile](./Disable-AzureTrafficManagerProfile.md)

[AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[新-AzureTrafficManagerProfile](./New-AzureTrafficManagerProfile.md)

[移除-AzureTrafficManagerProfile](./Remove-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


