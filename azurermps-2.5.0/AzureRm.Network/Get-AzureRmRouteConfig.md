---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermrouteconfig
schema: 2.0.0
ms.openlocfilehash: 907ca017518304a38340e9539aa4e8faf4216d59
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802341"
---
# Get-AzureRmRouteConfig

## 摘要
從路由資料表取得路由。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
**AzureRmRouteConfig** Cmdlet 會從 Azure 路由表取得路由。
您可以依名稱指定路由。

## 示例

### 範例1：取得路由資料表
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Get-AzureRmRouteConfig -Name "Route07"
Name              : route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

這個命令會使用 **AzureRmRouteTable** Cmdlet 取得名為 RouteTable01 的路由資料表。
命令會使用管線運算子，將該表傳遞至目前的 Cmdlet。
目前的 Cmdlet 會在路由表中取得名為 RouteTable01 的名為 Route07 的路由。

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定此 Cmdlet 所取得之路由的名稱。

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

### -RouteTable
指定由此 Cmdlet 取得路由的路由表。

```yaml
Type: PSRouteTable
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

### PSRouteTable
形參 "RouteTable" 接受管線中 "PSRouteTable" 類型的值

## 輸出

### PSRoute 中的 [.]

## 筆記

## 相關連結

[附加 AzureRmRouteConfig](./Add-AzureRmRouteConfig.md)

[AzureRmRouteTable](./Get-AzureRmRouteTable.md)

[新-AzureRmRouteConfig](./New-AzureRmRouteConfig.md)

[移除-AzureRmRouteConfig](./Remove-AzureRmRouteConfig.md)

[Set-AzureRmRouteConfig](./Set-AzureRmRouteConfig.md)


