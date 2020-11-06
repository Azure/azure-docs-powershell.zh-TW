---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 62cfc4fc3555b9eb798a1d64c53b0b25e9abc14c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621628"
---
# Remove-AzExpressRouteCircuitAuthorization

## 摘要
移除現有的 ExpressRoute 配置授權。

## 句法

```
Remove-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzExpressRouteCircuitAuthorization** Cmdlet 會移除指派給 ExpressRoute 回路的授權。 ExpressRoute 回路使用連線提供者（而不是公用網際網路），將您的內部部署網路連線至 Azure。 ExpressRoute 電路的擁有者可以為每個電路建立最多10個授權;這些授權會產生授權金鑰，虛擬網路擁有者可以使用它將自己的網路連線至線路。 每個虛擬網路只能有一個授權。 不過，線路擁有者可以隨時使用 **移除 AzExpressRouteCircuitAuthorization** 來移除指派給虛擬網路的授權。 在這種情況下，對應的虛擬網路將無法再使用 ExpressRoute 線路連線至 Azure。

## 示例

### 範例1：從 ExpressRoute 回路移除線路授權
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

這個範例會從 ExpressRoute 回路中移除線路授權。 第一個命令使用 **AzExpressRouteCircuit** Cmdlet 來建立名為 ContosoCircuit 的 ExpressRoute 回路的物件參照，並將結果儲存在名為 $Circuit 的變數中。
第二個命令會標示要移除的線路授權 ContosoCircuitAuthorization。
第三個命令使用 Set-AzExpressRouteCircuit Cmdlet 來確認移除儲存在 $Circuit 變數中的 ExpressRoute 電路。

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

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
指定此 Cmdlet 移除的 ExpressRouteCircuit 物件。

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
指定此 Cmdlet 移除之線路授權的名稱。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### PSExpressRouteCircuit 中的 [.]

## 輸出

### PSExpressRouteCircuit 中的 [.]

## 筆記

## 相關連結

[附加 AzExpressRouteCircuitAuthorization](./Add-AzExpressRouteCircuitAuthorization.md)

[AzExpressRouteCircuit](./Get-AzExpressRouteCircuit.md)

[AzExpressRouteCircuitAuthorization](./Get-AzExpressRouteCircuitAuthorization.md)

[新-AzExpressRouteCircuitAuthorization](./New-AzExpressRouteCircuitAuthorization.md)

[Set-AzExpressRouteCircuit](./Set-AzExpressRouteCircuit.md)
