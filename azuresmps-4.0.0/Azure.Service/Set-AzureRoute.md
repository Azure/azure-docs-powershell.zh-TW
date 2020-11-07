---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A7DFF559-188D-4CF9-9315-CA327E0C5C0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: d502ba2961e5238426228e4ac58a29b922be81f3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967269"
---
# Set-AzureRoute

## 摘要
在路由表中建立路由。

## 句法

```
Set-AzureRoute -RouteName <String> -AddressPrefix <String> -NextHopType <String> [-NextHopIpAddress <String>]
 -RouteTable <IRouteTable> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
**AzureRoute** Cmdlet 會在路由表中建立路由。
新的路由幾乎會立即在與路由資料表相關聯的虛擬機器上生效。

## 示例

### 範例1：新增虛擬裝置的下一個躍點路由
```
PS C:\> New-AzureRouteTable -Name "ApplianceRouteTable" -Location "Central US" -Label "Appliance Route Table" | Set-AzureRoute -RouteName "ApplianceRoute03" -AddressPrefix "10.0.0.0/24" -NextHopType VirtualAppliance -NextHopIpAddress "10.0.1.5"

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute}                    AppRT                         Central US                    Appliance Route Table
```

這個命令會在指定的位置建立名為 ApplianceRouteTable 的路由表。
命令會將路由資料表傳送至目前的 Cmdlet。
目前的 Cmdlet 會新增一個名為 ApplianceRoute03 的路由，這是一個 VirtualAppliance 的下一個躍點類型。
此命令會指定下一個躍點 IP 位址和路由的位址首碼。

### 範例2：新增網際網路下一個躍點路由
```
PS C:\> Get-AzureRouteTable -Name "ApplianceRouteTable" | Set-AzureRoute -RouteName "InternetRoute" -AddressPrefix "0.0.0.0/0" -NextHopType Internet

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute, internetroute}     AppRT                         Central US                    Appliance Route Table
```

這個命令會取得名為 ApplianceRouteTable 的路由表。
命令會將路由資料表傳送至目前的 Cmdlet。
目前的 Cmdlet 會新增一個名為 InternetRoute 的路由，這是網際網路的下一個躍點類型。
此命令會指定路由的位址首碼。

## 參數

### -AddressPrefix
指定新路由的位址首碼。

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

### -NextHopIpAddress
為使用這個路線之通訊的下一個躍點指定裝置的 IP 位址。
只有在您為 *NextHopType* 參數指定 VirtualAppliance 值時，才能指定此值。

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

### -NextHopType
指定使用此路由之流量的下一個躍點類型。
有效值為： 

- VPNGateway
- VNETLocal
- 互聯
- VirtualAppliance
- 非

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

### -RouteName
指定此 Cmdlet 所新增之新路由的名稱。

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

### -RouteTable
指定此 Cmdlet 將新路由新增到哪個路由表。

```yaml
Type: IRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

## 筆記

## 相關連結

[移除-AzureRoute](./Remove-AzureRoute.md)


