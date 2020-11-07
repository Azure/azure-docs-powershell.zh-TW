---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 5d963384d08dfed2e7e8516b892d2a3680c9332c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965738"
---
# Az ServiceFabric 模組
## 說明
Azure Service Fabric 模組，您可以用來自動化結束雙端作業，例如建立安全的群集、透過群集憑證進行滾動、新增或移除群集中的節點等。下列列出所有作業的完整清單。

## Az ServiceFabric Cmdlet

### [附加 AzServiceFabricClientCertificate](Add-AzServiceFabricClientCertificate.md)
在群集中加入通用名稱或指紋，以進行用戶端驗證。

### [附加 AzServiceFabricClusterCertificate](Add-AzServiceFabricClusterCertificate.md)
將次要群集憑證新增至群集。

### [附加 AzServiceFabricNode](Add-AzServiceFabricNode.md)
新增節點至群集中的特定節點類型。

### [附加 AzServiceFabricNodeType](Add-AzServiceFabricNodeType.md)
在現有的群集中新增節點類型。

### [AzServiceFabricApplication](Get-AzServiceFabricApplication.md)
取得 Service Fabric 應用程式的詳細資料。

### [AzServiceFabricApplicationType](Get-AzServiceFabricApplicationType.md)
取得 Service Fabric 應用程式類型的詳細資料。

### [AzServiceFabricApplicationTypeVersion](Get-AzServiceFabricApplicationTypeVersion.md)
取得 Service Fabric 應用程式類型版本詳細資料。

### [AzServiceFabricCluster](Get-AzServiceFabricCluster.md)
取得 [群集] 資源的詳細資料。

### [AzServiceFabricService](Get-AzServiceFabricService.md)
在指定的應用程式和群集下取得服務結構服務的詳細資料。

### [新-AzServiceFabricApplication](New-AzServiceFabricApplication.md)
在指定的資源群組和群集底下建立新的服務結構應用程式。

### [新-AzServiceFabricApplicationType](New-AzServiceFabricApplicationType.md)
在指定的資源群組和群集底下建立新的 service fabric 應用程式類型。

### [新-AzServiceFabricApplicationTypeVersion](New-AzServiceFabricApplicationTypeVersion.md)
在指定的資源群組和群集底下建立新的應用程式類型版本。

### [新-AzServiceFabricCluster](New-AzServiceFabricCluster.md)
這個命令會使用您提供的憑證或系統產生的自我簽署憑證來設定新的服務結構群集。 它可以使用您所提供的預設範本或自訂範本。 您可以選擇將自行簽署的憑證匯出到哪個資料夾，或稍後從金鑰電子倉庫將其回遷。 

### [新-AzServiceFabricService](New-AzServiceFabricService.md)
在指定的應用程式和群集下建立新的 service fabric service。

### [移除-AzServiceFabricApplication](Remove-AzServiceFabricApplication.md)
從群集中移除應用程式。 這將會移除應用程式下的所有服務。

### [移除-AzServiceFabricApplicationType](Remove-AzServiceFabricApplicationType.md)
從群集中移除服務結構應用程式類型。 這會移除此資源下的所有類型版本。

### [移除-AzServiceFabricApplicationTypeVersion](Remove-AzServiceFabricApplicationTypeVersion.md)
從群集中移除應用程式類型版本的服務結構。

### [移除-AzServiceFabricClientCertificate](Remove-AzServiceFabricClientCertificate.md)
移除用戶端憑證 (s) 或證書受領人 (s) 名稱 (s) ，才能用於用戶端驗證至群集。

### [移除-AzServiceFabricClusterCertificate](Remove-AzServiceFabricClusterCertificate.md)
移除群集憑證以用於群集安全。

### [移除-AzServiceFabricNode](Remove-AzServiceFabricNode.md)
從群集中移除特定節點類型的節點。

### [移除-AzServiceFabricNodeType](Remove-AzServiceFabricNodeType.md)
從群集中移除完整的節點類型。

### [移除-AzServiceFabricService](Remove-AzServiceFabricService.md)
從群集中移除服務。

### [移除-AzServiceFabricSetting](Remove-AzServiceFabricSetting.md)
從群集中移除一或多個服務結構設定。

### [Set-AzServiceFabricSetting](Set-AzServiceFabricSetting.md)
在群集中新增或更新一或多個 Service Fabric 設定。

### [Set-AzServiceFabricUpgradeType](Set-AzServiceFabricUpgradeType.md)
變更群集的 Service Fabric 升級類型。

### [更新-AzServiceFabricApplication](Update-AzServiceFabricApplication.md)
更新服務結構應用程式。 這可讓您更新應用程式參數和/或升級應用程式類型版本，這將會觸發應用程式升級。

### [更新-AzServiceFabricDurability](Update-AzServiceFabricDurability.md)
更新群集中節點類型的持久性層或 VmSku。

### [更新-AzServiceFabricReliability](Update-AzServiceFabricReliability.md)
在群集中更新主要節點類型的可靠性層級。

