---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 58DABEB0-D3B6-478B-9B83-80E4C67A7792
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d4717e795bcfea9728cbabb1b7c788713907aaa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93968016"
---
# Get-AzureRemoteAppVNet

## 摘要
在 Azure 中檢索有關 Azure RemoteApp 虛擬網路的資訊。

## 句法

```
Get-AzureRemoteAppVNet [[-VNetName] <String>] [-IncludeSharedKey] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 說明
**AzureRemoteAppVNet** Cmdlet 會在 Microsoft Azure 中檢索有關 Azure RemoteApp 虛擬網路的資訊。
這個 Cmdlet 會傳回包含指定虛擬網路相關資訊的物件。
如果未指定虛擬網路，此 Cmdlet 會傳回目前訂閱中所有虛擬網路的相關資訊。

## 示例

### 範例1：檢索虛擬網路的相關資訊
```
PS C:\> Get-AzureRemoteAppVNet -VNetName "ContosoVNet"
```

這個命令會取得名為 ContosoVNet 的虛擬網路的相關資訊。

## 參數

### -IncludeSharedKey
表示此 Cmdlet 在針對虛擬網路所取得的資訊中包含共用金鑰值。

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

### -VNetName
指定 Azure RemoteApp 虛擬網路的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: True
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

## 筆記

## 相關連結

[Set-AzureRemoteAppVNet](./Set-AzureRemoteAppVNet.md)


