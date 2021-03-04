---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 2c58549ee79cd24d29c1e3549d729995313c5748
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905885"
---
# Get-AzExpressRouteCircuitAuthorization

## 簡介
獲得 ExpressRoute 回路授權相關資訊。

## 語法

```
Get-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**Get-AzExpressRouteRouteCircuitAuthorization Cmdlet** 會取得指派給 ExpressRoute 回路之授權的資訊。 ExpressRoute 回路會使用連接提供者而非公用網際網路，將您的內部部署網路連接至 Microsoft 雲端。 ExpressRoute 回路的擁有者可以為每個回路建立 10 個授權;這些授權會產生授權金鑰，虛擬網路擁有者可以使用該金鑰將其網路連接至回路， (每個虛擬網路) 。 您隨時都可以執行 **Get-AzExpressRouteCircuitAuthorization** 來查看授權金鑰以及其他授權相關資訊。

## 例子

### 範例 1：取得所有 ExpressRoute 授權
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit
```

這些命令會返回與 ExpressRoute 回路相關聯的所有 ExpressRoute 授權相關資訊。 第一個命令使用 **Get-AzExpressRouteCircuit** Cmdlet 來建立名為 ContosoCircuit 的回路參照物件;該物件參照會儲存在變數$Circuit。 接著，第二個命令會使用該物件參照和 **Get-AzExpressRouteCircuitAuthorization** Cmdlet 來返回與 ContosoCircuit 相關聯的授權相關資訊。

### 範例 2：使用 Where-Object Cmdlet 取得所有 ExpressRoute 授權
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

這些命令代表範例 1 中所使用的命令變化。 不過，在此案例中，系統只會針對那些可供 (使用的授權 ，也就是說，針對尚未指派給虛擬網路授權的授權，會) 。 若要這麼做，回路授權資訊會從命令 2 中返回，並管道到 **Where-Object** Cmdlet。
**Where-Object** 接著只會挑選那些 *AuthorizationUseStatus* 屬性設為可用的授權。 若要只列出那些無法使用的授權，請針對 Where 子句使用此語法： `{$_.AuthorizationUseStatus -ne "Available"}`

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

### -ExpressRouteCircuit
指定 ExpressRoute 回路授權。

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -名稱
指定此 Cmdlet 所獲得 ExpressRoute 回路授權的名稱。
-Name "ContosoCircuitAuthorization"

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### Microsoft.Azure.Commands.Network.models.PSExpressRouteCircuit

## 輸出

### Microsoft.Azure.Commands.Network.models.PSExpressRouteCircuitAuthorization

## 筆記

## 相關連結

[Add-AzExpressRouteCircuitAuthorization](./Add-AzExpressRouteCircuitAuthorization.md)

[Get-AzExpressRouteCircuit](./Get-AzExpressRouteCircuit.md)

[New-AzExpressRouteCircuitAuthorization](./New-AzExpressRouteCircuitAuthorization.md)

[Remove-AzExpressRouteCircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)
