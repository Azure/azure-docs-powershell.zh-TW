---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 22E8CB18-8CDD-4992-AB81-E1BB400E6BC7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 294e931529b7de939a6a5c20181d48b18da1e892
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967723"
---
# Get-AzureVNetGatewayDiagnostics

## 摘要
取得虛擬網路閘道的目前診斷狀態。

## 句法

```
Get-AzureVNetGatewayDiagnostics -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
**AzureVNetGatewayDiagnostics** Cmdlet 會取得虛擬閘道的目前診斷狀態。
如果 (blob) 存在二進位大型物件，且 **AzureVNetGatewayDiagnostics** 已儲存先前的診斷會話，這個 Cmdlet 也會傳回該 Cmdlet 儲存該診斷會話的 blob URL。

## 示例

## 參數

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

### -VNetName
指定包含此 Cmdlet 為其提供診斷的虛擬網路閘道的虛擬網路。

```yaml
Type: String
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

[開始-AzureVNetGatewayDiagnostics](./Start-AzureVNetGatewayDiagnostics.md)

[停止 AzureVNetGatewayDiagnostics](./Stop-AzureVNetGatewayDiagnostics.md)


