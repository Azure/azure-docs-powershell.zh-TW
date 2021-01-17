---
Module Name: Az.Peering
Module Guid: 6c848b97-4dd4-49ef-b385-43c64905d25a
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.peering.md
Help Version: 0.1.0
Locale: e-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Az.Peering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Az.Peering.md
ms.openlocfilehash: 568c235bee84238d53849e8fb9dc3258e907cb18
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436279"
---
# Az。對等模組
## 說明
Microsoft 對等服務可讓客戶與 Microsoft 連線至 Azure，並將其網路資源表示為 ARM 物件。

## Az。對等 Cmdlet
### [AzLegacyPeering](Get-AzLegacyPeering.md)
用來將舊版對等資源轉換為 Azure 資源管理 (ARM) 資源。 

### [AzPeerAsn](Get-AzPeerAsn.md)
從 ARM 取得 PeerAsn 物件。

### [AzPeering](Get-AzPeering.md)
取得訂閱的對等資源

### [AzPeeringLocation](Get-AzPeeringLocation.md)
取得 Microsoft 提供的對等位置

### [AzPeeringReceivedRoute](Get-AzPeeringReceivedRoute.md)
列出對等的已接收路線。

### [AzPeeringRegisteredAsn](Get-AzPeeringRegisteredAsn.md)
取得網際網路交換路由伺服器類型 peerings 的註冊 ASN。

### [AzPeeringRegisteredPrefix](Get-AzPeeringRegisteredPrefix.md)
取得或列出 peerings 的已註冊前置詞。

### [AzPeeringService](Get-AzPeeringService.md)
取得單一物件之對等服務物件的清單。

### [AzPeeringServiceCountry](Get-AzPeeringServiceCountry.md)
列出對等服務可用的國家/地區。

### [AzPeeringServiceLocation](Get-AzPeeringServiceLocation.md)
取得 Microsoft 所提供的對等服務位置清單。

### [AzPeeringServicePrefix](Get-AzPeeringServicePrefix.md)
取得訂閱的對等服務首碼清單。

### [AzPeeringServiceProvider](Get-AzPeeringServiceProvider.md)
取得與 Microsoft 合作的對等服務提供者的清單。

### [新-AzPeerAsn](New-AzPeerAsn.md)
建立新的對等 ASN 

### [新-AzPeerAsnContactDetail](New-AzPeerAsnContactDetail.md)
為 PeerAsn 建立記憶體連絡人詳細資料。 

### [新-AzPeering](New-AzPeering.md)
建立新的對等 ARM 資源

### [新-AzPeeringDirectConnectionObject](New-AzPeeringDirectConnectionObject.md)
在記憶體 PSObject 中建立，以用於建立或修改對等。

### [新-AzPeeringExchangeConnectionObject](New-AzPeeringExchangeConnectionObject.md)
在記憶體 PSObject 中建立，以用於建立或修改對等。

### [新-AzPeeringRegisteredAsn](New-AzPeeringRegisteredAsn.md)
建立對等的註冊 ASN

### [新-AzPeeringRegisteredPrefix](New-AzPeeringRegisteredPrefix.md)
針對對等物件建立已註冊的首碼。

### [新-AzPeeringService](New-AzPeeringService.md)
建立新的對等服務。

### [新-AzPeeringServicePrefix](New-AzPeeringServicePrefix.md)
建立新的對等服務首碼

### [移除-AzPeerAsn](Remove-AzPeerAsn.md)
移除對等 Asn

### [移除-AzPeering](Remove-AzPeering.md)
刪除或移除對等。 這將會刪除該資源的所有子資源或警示。

### [移除-AzPeeringRegisteredAsn](Remove-AzPeeringRegisteredAsn.md)
從父對等資源刪除或移除已註冊的 ASN。

### [移除-AzPeeringRegisteredPrefix](Remove-AzPeeringRegisteredPrefix.md)
從父對等資源刪除或移除已註冊的首碼。

### [移除-AzPeeringServicePrefix](Remove-AzPeeringServicePrefix.md)
移除新的對等服務首碼

### [Set-AzPeerAsn](Set-AzPeerAsn.md)
更新連絡人資訊

### [Set-AzPeeringDirectConnectionObject](Set-AzPeeringDirectConnectionObject.md)
設定或更新直連連線資訊。 

### [Set-AzPeeringExchangeConnectionObject](Set-AzPeeringExchangeConnectionObject.md)
設定或更新 Exchange 連線資訊。 

### [Set-AzPeeringRegisteredAsn](Set-AzPeeringRegisteredAsn.md)
從父對等資源設定或更新已註冊的 ASN。

### [Set-AzPeeringRegisteredPrefix](Set-AzPeeringRegisteredPrefix.md)
從上層對等資源設定或更新已註冊的首碼。

### [更新-AzPeering](Update-AzPeering.md)
設定對等。 將此命令與 or 搭配 `Set-AzDirectPeeringConnectionObject` 使用 `Set-AzExchangePeeringConnectionObject` 。

