---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 01bf8c630f4fc4d137e98be5b1996eaf47ea3363
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/23/2019
ms.locfileid: "93611355"
---
# Az ServiceFabric 模組
## 說明
Azure Service Fabric 模組，您可以用來自動化結束雙端作業，例如建立安全的群集、透過群集憑證進行滾動、新增或移除群集中的節點等。下列列出所有作業的完整清單。

## Az ServiceFabric Cmdlet
### [附加 AzServiceFabricApplicationCertificate](Add-AzServiceFabricApplicationCertificate.md)
在組成群集 (s) ，將新憑證新增到虛擬電腦規模集。 憑證是用來做為應用程式憑證的。

### [附加 AzServiceFabricClientCertificate](Add-AzServiceFabricClientCertificate.md)
在群集中加入通用名稱或指紋，以進行用戶端驗證。

### [附加 AzServiceFabricClusterCertificate](Add-AzServiceFabricClusterCertificate.md)
將次要群集憑證新增至群集。

### [附加 AzServiceFabricNode](Add-AzServiceFabricNode.md)
新增節點至群集中的特定節點類型。

### [附加 AzServiceFabricNodeType](Add-AzServiceFabricNodeType.md)
在現有的群集中新增節點類型。

### [AzServiceFabricCluster](Get-AzServiceFabricCluster.md)
取得 [群集] 資源的詳細資料。

### [新-AzServiceFabricCluster](New-AzServiceFabricCluster.md)
這個命令會使用您提供的憑證或系統產生的自我簽署憑證來設定新的服務結構群集。 它可以使用您所提供的預設範本或自訂範本。 您可以選擇將自行簽署的憑證匯出到哪個資料夾，或稍後從金鑰電子倉庫將其回遷。 

### [移除-AzServiceFabricClientCertificate](Remove-AzServiceFabricClientCertificate.md)
移除用戶端憑證 (s) 或證書受領人 (s) 名稱 (s) ，才能用於用戶端驗證至群集。

### [移除-AzServiceFabricClusterCertificate](Remove-AzServiceFabricClusterCertificate.md)
移除群集憑證以用於群集安全。

### [移除-AzServiceFabricNode](Remove-AzServiceFabricNode.md)
從群集中移除特定節點類型的節點。

### [移除-AzServiceFabricNodeType](Remove-AzServiceFabricNodeType.md)
從群集中移除完整的節點類型。

### [移除-AzServiceFabricSetting](Remove-AzServiceFabricSetting.md)
從群集中移除一或多個服務結構設定。

### [Set-AzServiceFabricSetting](Set-AzServiceFabricSetting.md)
在群集中新增或更新一或多個 Service Fabric 設定。

### [Set-AzServiceFabricUpgradeType](Set-AzServiceFabricUpgradeType.md)
變更群集的 Service Fabric 升級類型。

### [更新-AzServiceFabricDurability](Update-AzServiceFabricDurability.md)
更新群集中節點類型的持久性層或 VmSku。

### [更新-AzServiceFabricReliability](Update-AzServiceFabricReliability.md)
在群集中更新主要節點類型的可靠性層級。

