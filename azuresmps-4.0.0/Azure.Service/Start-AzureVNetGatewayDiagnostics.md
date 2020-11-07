---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 9FCECA04-9855-461C-9470-85312993C4B1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5bb7bb3e708720b481edc4489d858c70736eac95
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967472"
---
# Start-AzureVNetGatewayDiagnostics

## 摘要
為 VPN 閘道啟動閘道診斷程式。

## 句法

```
Start-AzureVNetGatewayDiagnostics -VNetName <String> -CaptureDurationInSeconds <Int32>
 [-ContainerName <String>] -StorageContext <AzureStorageContext> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 說明
**AzureVNetGatewayDiagnostics** Cmdlet 會針對虛擬私人網路絡 (VPN) 閘道，啟動新的閘道診斷會話。
一次只能執行一個閘道診斷會話。
如果您在閘道診斷會話執行時執行這個 Cmdlet，這個 Cmdlet 會傳回錯誤。

## 示例

## 參數

### -CaptureDurationInSeconds
指定捕獲持續時間（以秒為單位）。

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -容器
指定 Azure 容器的名稱。
這個 Cmdlet 會將結果儲存在此參數指定的容器中。

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

### -StorageCoNtext
指定 Azure 儲存區內容。
這個 Cmdlet 會使用此參數指定的儲存區內容來儲存結果。

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VNetName
指定包含此 Cmdlet 執行診斷之虛擬網路閘道的虛擬網路。

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

[AzureVNetGatewayDiagnostics](./Get-AzureVNetGatewayDiagnostics.md)

[停止 AzureVNetGatewayDiagnostics](./Stop-AzureVNetGatewayDiagnostics.md)


