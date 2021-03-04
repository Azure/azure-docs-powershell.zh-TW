---
Module Name: Az.Peering
Module Guid: 6c848b97-4dd4-49ef-b385-43c64905d25a
Download Help Link: https://docs.microsoft.com/powershell/module/az.peering.md
Help Version: 0.1.0
Locale: e-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Az.Peering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Az.Peering.md
ms.openlocfilehash: 36b7be0ce3cae3ef0e58f71bc8486168d02daf50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911514"
---
# Az.對等模組
## 描述
Microsoft 對等服務可讓客戶和 Microsoft 連接至 Azure，並將其網路資源以 ARM 物件表示。

## Az.Peering Cmdlets
### [Get-AzLegacyPeering](Get-AzLegacyPeering.md)
用來將舊版對等資源轉換為 Azure 資源管理 (ARM) 資源。 

### [Get-AzPeerAsn](Get-AzPeerAsn.md)
從 ARM 中獲得對等物件。

### [Get-AzPeering](Get-AzPeering.md)
獲得訂閱的對等資源

### [Get-AzPeeringLocation](Get-AzPeeringLocation.md)
獲得 Microsoft 提供的對等位置

### [Get-AzPeeringReceivedRoute](Get-AzPeeringReceivedRoute.md)
列出對等的接收路由。

### [Get-AzPeeringRegisteredAsn](Get-AzPeeringRegisteredAsn.md)
針對網際網路交換路由伺服器類型對等，獲得登錄的 ASN。

### [Get-AzPeeringRegisteredPrefix](Get-AzPeeringRegisteredPrefix.md)
獲得或列出對等互連的登錄首碼。

### [Get-AzPeeringService](Get-AzPeeringService.md)
取得單一物件的對等服務物件清單。

### [Get-AzPeeringServiceCountry](Get-AzPeeringServiceCountry.md)
列出可供對等服務使用的國家/地區。

### [Get-AzPeeringServiceLocation](Get-AzPeeringServiceLocation.md)
獲得 Microsoft 提供的對等服務位置清單。

### [Get-AzPeeringServicePrefix](Get-AzPeeringServicePrefix.md)
獲得訂閱的對等服務首碼清單。

### [Get-AzPeeringServiceProvider](Get-AzPeeringServiceProvider.md)
獲得與 Microsoft 合作之對等服務提供者的清單。

### [New-AzPeerAsn](New-AzPeerAsn.md)
建立新對等 ASN 

### [New-AzPeerAsnContactDetail](New-AzPeerAsnContactDetail.md)
為 PeerAsn 建立記憶體中的連絡人詳細資料。 

### [New-AzPeering](New-AzPeering.md)
建立新的對等 ARM 資源

### [New-AzPeeringDirectConnectionObject](New-AzPeeringDirectConnectionObject.md)
在記憶體中建立 PSObject，以用於建立或修改對等。

### [New-AzPeeringExchangeConnectionObject](New-AzPeeringExchangeConnectionObject.md)
在記憶體中建立 PSObject，以用於建立或修改對等。

### [New-AzPeeringRegisteredAsn](New-AzPeeringRegisteredAsn.md)
建立已註冊的 ASN 以對等

### [New-AzPeeringRegisteredPrefix](New-AzPeeringRegisteredPrefix.md)
建立對等物件的登錄首碼。

### [New-AzPeeringService](New-AzPeeringService.md)
建立新的對等服務。

### [New-AzPeeringServicePrefix](New-AzPeeringServicePrefix.md)
建立新的對等服務首碼

### [Remove-AzPeerAsn](Remove-AzPeerAsn.md)
移除對等 Asn

### [Remove-AzPeering](Remove-AzPeering.md)
刪除或移除對等。 這會刪除所有子資源或提醒資源。

### [Remove-AzPeeringRegisteredAsn](Remove-AzPeeringRegisteredAsn.md)
從父對等資源刪除或移除已登錄的 ASN。

### [Remove-AzPeeringRegisteredPrefix](Remove-AzPeeringRegisteredPrefix.md)
刪除或移除父對等資源的登錄首碼。

### [Remove-AzPeeringServicePrefix](Remove-AzPeeringServicePrefix.md)
移除新的對等服務首碼

### [Set-AzPeerAsn](Set-AzPeerAsn.md)
更新連絡人資訊

### [Set-AzPeeringDirectConnectionObject](Set-AzPeeringDirectConnectionObject.md)
設定或更新直接連接資訊。 

### [Set-AzPeeringExchangeConnectionObject](Set-AzPeeringExchangeConnectionObject.md)
設定或更新 Exchange 連接資訊。 

### [Set-AzPeeringRegisteredAsn](Set-AzPeeringRegisteredAsn.md)
從父對等資源設定或更新已登錄的 ASN。

### [Set-AzPeeringRegisteredPrefix](Set-AzPeeringRegisteredPrefix.md)
設定或更新來自父對等資源的登錄首碼。

### [Update-AzPeering](Update-AzPeering.md)
設定對等。 將此命令與或 `Set-AzDirectPeeringConnectionObject` 同時使用 `Set-AzExchangePeeringConnectionObject` 。

