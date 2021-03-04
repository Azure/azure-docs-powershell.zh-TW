---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/powershell/module/az.network/new-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 9c247784a9f890d97aee301383656f97ef9c7dd4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913154"
---
# New-AzExpressRouteCircuitAuthorization

## 簡介
建立 ExpressRoute 回路授權。

## 語法

```
New-AzExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 描述
**New-AzExpressRouteRouteCircuitAuthorization** Cmdlet 會建立一個可以新加入 ExpressRoute 回路的回路授權。 ExpressRoute 回路會使用連接提供者而非公用網際網路，將您的內部部署網路連接至 Microsoft 雲端。 ExpressRoute 回路的擁有者可以為每個回路建立 10 個授權;這些授權會產生授權金鑰，由虛擬網路擁有者用來將網路連接至回路。 每個虛擬網路只能有一個授權。
建立 ExpressRoute 回路之後，您可以使用 **Add-AzExpressRouteCircuitAuthorization** 來新增該回路的授權。
或者，您可以使用 **New-AzExpressRouteRouteCircuitAuthorization** 來建立可在建立回路時新回路中新增的授權。

## 例子

### 範例 1：建立新回路授權
```
$Authorization = New-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

此命令會建立名為 ContosoCircuitAuthorization 的新回路授權，然後將該物件儲存在名為 contosoCircuitAuthorization 的$Authorization。 將物件另存到變數很重要：雖然 **New-AzExpressRouteCircuitAuthorization** 可以建立回路授權，但無法將該授權新加到回路路由。 相反地，在$Authorization ExpressRoute 回路New-AzExpressRouteCircuit使用變數變數。
詳細資訊請參閱 Cmdlet New-AzExpressRouteCircuit檔。

## 參數

### -DefaultProfile
用於與 azure 通訊的認證、帳戶、租使用者和訂閱。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定新 ExpressRoute 回路授權的唯一名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### 沒有

## 輸出

### Microsoft.Azure.Commands.Network.models.PSExpressRouteCircuitAuthorization

## 筆記

## 相關連結

[Add-AzExpressRouteCircuitAuthorization](./Add-AzExpressRouteCircuitAuthorization.md)

[Get-AzExpressRouteCircuitAuthorization](./Get-AzExpressRouteCircuitAuthorization.md)

[Remove-AzExpressRouteCircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)

