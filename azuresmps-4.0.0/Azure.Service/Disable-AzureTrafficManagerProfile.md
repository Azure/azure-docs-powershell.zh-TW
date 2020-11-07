---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: ECE9C2A6-7DA2-4477-B877-9970FBE26D7C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8f378cbf8926a650699ec50a2a0a42873dcb7528
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967139"
---
# Disable-AzureTrafficManagerProfile

## 摘要
停用流量管理器設定檔。

## 句法

```
Disable-AzureTrafficManagerProfile -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
**Disable AzureTrafficManagerProfile** Cmdlet 會停用 Microsoft Azure 流量管理器設定檔。
您可以使用 *PassThru* 參數來顯示操作是否成功。

## 示例

### 範例1：停用流量管理器設定檔並顯示結果
```
PS C:\>Disable-AzureTrafficManagerProfile -Name "MyProfile" -PassThru
True
```

這個命令會停用名為 MyProfile 的流量管理器設定檔。
命令會指定 *PassThru* 參數，以顯示命令是否已成功完成。

### 範例2：停用流量管理器設定檔，且不顯示任何結果
```
PS C:\>Disable-AzureTrafficManagerProfile -Name "MyProfile"
```

這個命令會停用名為 MyProfile 的流量管理器設定檔，但不會顯示命令是否已成功完成。

## 參數

### -名稱
指定要停用之流量管理器設定檔的名稱。

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
如果操作成功，且您指定 *PassThru* 參數，則此 Cmdlet 會傳回 $True 的值。

## 筆記

## 相關連結

[Enable-AzureTrafficManagerProfile](./Enable-AzureTrafficManagerProfile.md)

[AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[新-AzureTrafficManagerProfile](./New-AzureTrafficManagerProfile.md)

[移除-AzureTrafficManagerProfile](./Remove-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


