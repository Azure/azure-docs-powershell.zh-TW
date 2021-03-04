---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/powershell/module/az.network/add-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 9812316b20db927dea9bfe999cad54fe002bfc93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901998"
---
# Add-AzExpressRouteCircuitAuthorization

## 簡介
新增 ExpressRoute 回路授權。

## 語法

```
Add-AzExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**Add-AzExpressRouteRouteCircuitAuthorization** Cmdlet 會新增 ExpressRoute 回路的授權。 ExpressRoute 回路會使用連接提供者而非公用網際網路，將您的內部部署網路連接至 Microsoft 雲端。 ExpressRoute 回路的擁有者可以為每個回路建立 10 個授權;這些授權會產生授權金鑰，虛擬網路擁有者可以使用該金鑰將其網路連接至回路， (每個虛擬網路) 。 **Add-AzExpressRouteCircteCircuitAuthorization** 會為回路新增新的授權，並同時產生對應的授權金鑰。 您隨時都可以執行 Get-AzExpressRouteCircuitAuthorization Cmdlet 來查看這些金鑰，然後視需要複製並轉寄到適當的網路擁有者。
請注意，執行 **Add-AzExpressRouteRouteCircuitAuthorization** 之後，您必須撥打 Set-AzExpressRouteCircuit Cmdlet 以啟用金鑰。 如果您未撥打 **Set-AzExpressRouteCircuit，** 則授權會新增到回路中，但無法啟用。

## 例子

### 範例 1：新增授權至指定的 ExpressRoute 回路
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

此範例中的命令會新增授權至現有的 ExpressRoute 回路。 第一個命令使用 **Get-AzExpressRouteCircuit** 來建立名為 ContosoCircuit 之回路的物件參照。 該物件參照會儲存在名為 $Circuit 的變數中。
第二個命令是使用 **Add-AzExpressRouteRouteCircuitAuthorization** Cmdlet 在 ExpressRoute 回路中 (ContosoCircuitAuthorization) 新授權。 此命令會新增授權，但無法啟用該授權。 啟用授權需要範例最後一個命令中顯示的 **Set-AzExpressRouteCircuit。**

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
指定此 Cmdlet 新增授權的 ExpressRoute 回路。

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
指定要新增的回路授權名稱。

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

### Microsoft.Azure.Commands.Network.models.PSExpressRouteCircuit

## 輸出

### Microsoft.Azure.Commands.Network.models.PSExpressRouteCircuit

## 筆記

## 相關連結

[Get-AzExpressRouteCircuit](./Get-AzExpressRouteCircuit.md)

[Get-AzExpressRouteCircuitAuthorization](./Get-AzExpressRouteCircuitAuthorization.md)

[New-AzExpressRouteCircuitAuthorization](./New-AzExpressRouteCircuitAuthorization.md)

[Remove-AzExpressRouteCircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)

[Set-AzExpressRouteCircuit](./Set-AzExpressRouteCircuit.md)
