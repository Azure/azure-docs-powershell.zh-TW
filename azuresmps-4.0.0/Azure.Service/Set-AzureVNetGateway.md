---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 70899AAC-BF64-4FFA-9DAF-92E859D0B271
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3b30172f947c1c8bf39a8be84039d9166d6ea290
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967860"
---
# Set-AzureVNetGateway

## 摘要
啟用或停用 Azure 虛擬網路的 VPN 閘道。

## 句法

### 連接 (預設) 
```
Set-AzureVNetGateway [-Connect] -VNetName <String> -LocalNetworkSiteName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### 卸下
```
Set-AzureVNetGateway [-Disconnect] -VNetName <String> -LocalNetworkSiteName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
**AzureVNetGateway** Cmdlet 可啟用或停用 Azure 虛擬網路 (VPN) 閘道的虛擬私人網路絡。
虛擬網路閘道是用來連線至虛擬網路的 VPN 端點。
指定 [連線 *]* 或 *[中斷連接]* 參數，以啟用或停用內部部署本機網路網站與虛擬網路之間的 VPN 連線。

## 示例

### 範例1：為虛擬網路啟用虛擬網路閘道
```
PS C:\> Set-AzureVNetGateway -Connect -VnetName "ContosoProdNet" -LocalNetworkSiteName "ContosoBranchOffice"
```

這個命令會在名為 ContosoProdNet 的 Azure 虛擬網路或名為 ContosoBranchOffice 的本機網路網站的 VPN 裝置之間啟用虛擬網路閘道。

### 範例2：停用虛擬網路的虛擬網路閘道
```
PS C:\> Set-AzureVNetGateway -Disconnect -VnetName "ContosoProdNet" -LocalNetworkSiteName "ContosoBranchOffice"
```

這個命令會停用名為 ContosoProdNet 的 Azure 虛擬網路閘道與名為 ContosoBranchOffice 之區域網路網站之 VPN 裝置之間的虛擬網路閘道。

## 參數

### -連接
表示此 Cmdlet 啟用虛擬網路與本機網路網站之間的 VPN 連線。

```yaml
Type: SwitchParameter
Parameter Sets: Connect
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### 中斷連線
表示此 Cmdlet 會停用虛擬網路與本機網路網站之間的 VPN 連線。

```yaml
Type: SwitchParameter
Parameter Sets: Disconnect
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LocalNetworkSiteName
指定此 Cmdlet 啟用或停用 VPN 連線之內部部署本機網路網站的名稱。

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
指定此 Cmdlet 啟用或停用 VPN 連線的虛擬網路。

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

[AzureVNetGateway](./Get-AzureVNetGateway.md)

[新-AzureVNetGateway](./New-AzureVNetGateway.md)

[移除-AzureVNetGateway](./Remove-AzureVNetGateway.md)

[Reset-AzureVNetGateway](./Reset-AzureVNetGateway.md)

[調整大小-AzureVNetGateway](./Resize-AzureVNetGateway.md)


