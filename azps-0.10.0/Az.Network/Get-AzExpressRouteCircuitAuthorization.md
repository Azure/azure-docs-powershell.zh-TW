---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 3b51a16d6ff2de8292b1bbb66f7f5ab24cc17b93
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794428"
---
# Get-AzExpressRouteCircuitAuthorization

## 摘要
取得 ExpressRoute 線路授權的相關資訊。

## 句法

```
Get-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzExpressRouteCircuitAuthorization** Cmdlet 會取得指派給 ExpressRoute 回路之授權的相關資訊。 ExpressRoute 回路使用連線提供者（而不是公用網際網路），將您的內部部署網路連線至 Microsoft 雲端。 ExpressRoute 電路的擁有者可以為每個電路建立最多10個授權;這些授權會產生一個授權金鑰，虛擬網路擁有者可以使用它將自己的網路連線至 (每個虛擬網路) 一個授權的線路。 您可以隨時執行 **AzExpressRouteCircuitAuthorization** ，隨時查看授權金鑰以及授權的其他相關資訊。

## 示例

### 範例1：取得所有 ExpressRoute 授權
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit
```

這些命令會傳回與 ExpressRoute 回路相關聯之所有 ExpressRoute 授權的相關資訊。 第一個命令使用 **AzExpressRouteCircuit** Cmdlet 來建立物件參照名為 ContosoCircuit 的電路;該物件參照會儲存在 $Circuit 的變數中。 然後，第二個命令會使用該物件參照及 **AzExpressRouteCircuitAuthorization** Cmdlet，傳回與 ContosoCircuit 相關的授權資訊。

### 範例2：使用 Where-Object Cmdlet 取得所有 ExpressRoute 授權
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

這些命令代表範例1中所用命令的變化。 不過，在此情況下，只會針對那些可使用 (的授權傳回信息，也就是對於尚未指派給虛擬網路) 的授權。 若要這樣做，請在命令2中傳回線路授權資訊，並以管道 **方式** 傳送到物件 Cmdlet。
**在其中，物件** 只會挑選 *AuthorizationUseStatus* 屬性設定為 [可用] 的授權。 若要只列出那些無法使用的授權，請使用此語法做為 Where 子句：

`{$_.AuthorizationUseStatus -ne "Available"}`

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

### -ExpressRouteCircuit
指定 ExpressRoute 線路驗證。

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -名稱
指定此 Cmdlet 取得的 ExpressRoute 線路授權名稱。

-Name "ContosoCircuitAuthorization"

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### PSExpressRouteCircuit
**AzExpressRouteCircuitAuthorization** 會接受 PSExpressRouteCircuit 物件的流水線式實例（ **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** 物件）。

## 輸出

### PSExpressRouteCircuitAuthorization
**AzExpressRouteCircuitAuthorization** 會傳回 PSExpressRouteCircuitAuthorization 物件的實例（ **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization** 物件）。

## 筆記

## 相關連結

[附加 AzExpressRouteCircuitAuthorization](./Add-AzExpressRouteCircuitAuthorization.md)

[AzExpressRouteCircuit](./Get-AzExpressRouteCircuit.md)

[新-AzExpressRouteCircuitAuthorization](./New-AzExpressRouteCircuitAuthorization.md)

[移除-AzExpressRouteCircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)
