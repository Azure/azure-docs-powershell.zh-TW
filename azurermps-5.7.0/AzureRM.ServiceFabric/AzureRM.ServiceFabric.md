---
Module Name: AzureRM.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
ms.openlocfilehash: 0bd157b8df4cca37c92a4d4f2984011dbd924e34
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/23/2019
ms.locfileid: "93441708"
---
# AzureRM ServiceFabric Module
## 說明
Azure Service Fabric 模組，您可以用來自動化結束雙端作業，例如建立安全的群集、透過群集憑證進行滾動、新增或移除群集中的節點等。下列列出所有作業的完整清單。

## AzureRM ServiceFabric Cmdlet
### [附加 AzureRmServiceFabricApplicationCertificate](Add-AzureRmServiceFabricApplicationCertificate.md)
在組成群集 (s) ，將新憑證新增到虛擬電腦規模集。 憑證是用來做為應用程式憑證的。

### [附加 AzureRmServiceFabricClientCertificate](Add-AzureRmServiceFabricClientCertificate.md)
在群集中加入通用名稱或指紋，以進行用戶端驗證。

### [附加 AzureRmServiceFabricClusterCertificate](Add-AzureRmServiceFabricClusterCertificate.md)
將次要群集憑證新增至群集。

### [附加 AzureRmServiceFabricNode](Add-AzureRmServiceFabricNode.md)
新增節點至群集中的特定節點類型。

### [附加 AzureRmServiceFabricNodeType](Add-AzureRmServiceFabricNodeType.md)
在現有的群集中新增節點類型。

### [AzureRmServiceFabricCluster](Get-AzureRmServiceFabricCluster.md)
取得 [群集] 資源的詳細資料。

### [新-AzureRmServiceFabricCluster](New-AzureRmServiceFabricCluster.md)
這個命令會使用您提供的憑證或系統產生的自我簽署憑證來設定新的服務結構群集。 它可以使用您所提供的預設範本或自訂範本。 您可以選擇將自行簽署的憑證匯出到哪個資料夾，或稍後從金鑰電子倉庫將其回遷。 

### [移除-AzureRmServiceFabricClientCertificate](Remove-AzureRmServiceFabricClientCertificate.md)
移除用戶端憑證 (s) 或證書受領人 (s) 名稱 (s) ，才能用於用戶端驗證至群集。

### [移除-AzureRmServiceFabricClusterCertificate](Remove-AzureRmServiceFabricClusterCertificate.md)
移除群集憑證以用於群集安全。

### [移除-AzureRmServiceFabricNode](Remove-AzureRmServiceFabricNode.md)
從群集中移除特定節點類型的節點。

### [移除-AzureRmServiceFabricNodeType](Remove-AzureRmServiceFabricNodeType.md)
從群集中移除完整的節點類型。

### [移除-AzureRmServiceFabricSetting](Remove-AzureRmServiceFabricSetting.md)
從群集中移除一或多個服務結構設定。

### [Set-AzureRmServiceFabricSetting](Set-AzureRmServiceFabricSetting.md)
在群集中新增或更新一或多個 Service Fabric 設定。

### [Set-AzureRmServiceFabricUpgradeType](Set-AzureRmServiceFabricUpgradeType.md)
變更群集的 Service Fabric 升級類型。

### [更新-AzureRmServiceFabricDurability](Update-AzureRmServiceFabricDurability.md)
更新群集中節點類型的持久性層或 VmSku。

### [更新-AzureRmServiceFabricReliability](Update-AzureRmServiceFabricReliability.md)
在群集中更新主要節點類型的可靠性層級。

