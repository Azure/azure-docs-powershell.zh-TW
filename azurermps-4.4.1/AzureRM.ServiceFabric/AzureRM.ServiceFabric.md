---
Module Name: AzureRM.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
ms.openlocfilehash: 9c71788abd7707931df2c25279c265bbe9967bbf
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/23/2019
ms.locfileid: "93441980"
---
# AzureRM ServiceFabric Module
## 說明
Azure Service Fabric 模組，您可以用來自動化結束雙端作業，例如建立安全的群集、透過群集憑證進行滾動、新增或移除群集中的節點等。下列列出所有作業的完整清單。

## AzureRM ServiceFabric Cmdlet
### [附加 AzureRmServiceFabricApplicationCertificate](Add-AzureRmServiceFabricApplicationCertificate.md)
新增用來做為應用程式憑證的憑證

### [附加 AzureRmServiceFabricClientCertificate](Add-AzureRmServiceFabricClientCertificate.md)
在用戶端驗證的群集設定中加入通用名稱或指紋

### [附加 AzureRmServiceFabricClusterCertificate](Add-AzureRmServiceFabricClusterCertificate.md)
將次要群集憑證新增至群集，以便在現有的憑證上滾動 

### [附加 AzureRmServiceFabricNode](Add-AzureRmServiceFabricNode.md)
新增節點/Vm 至特定節點類型至群集

### [附加 AzureRmServiceFabricNodeType](Add-AzureRmServiceFabricNodeType.md)
新增節點類型/Vm 至現有的群集

### [AzureRmServiceFabricCluster](Get-AzureRmServiceFabricCluster.md)
取得群集資源的詳細資料 

### [新-AzureRmServiceFabricCluster](New-AzureRmServiceFabricCluster.md)
建立新的 ServiceFabric 群集。 這個命令有許多不同的重載來涵蓋各種情況

### [移除-AzureRmServiceFabricClientCertificate](Remove-AzureRmServiceFabricClientCertificate.md)
移除用來存取群集的用戶端憑證

### [移除-AzureRmServiceFabricClusterCertificate](Remove-AzureRmServiceFabricClusterCertificate.md)
移除群集憑證以用於群集安全性

### [移除-AzureRmServiceFabricNode](Remove-AzureRmServiceFabricNode.md)
從群集中移除特定節點類型的節點

### [移除-AzureRmServiceFabricNodeType](Remove-AzureRmServiceFabricNodeType.md)
從群集中移除節點類型

### [移除-AzureRmServiceFabricSetting](Remove-AzureRmServiceFabricSetting.md)
從群集中移除一或多個 ServiceFabric 設定

### [Set-AzureRmServiceFabricSetting](Set-AzureRmServiceFabricSetting.md)
在群集中新增或更新一個或多個 ServiceFabric 設定

### [Set-AzureRmServiceFabricUpgradeType](Set-AzureRmServiceFabricUpgradeType.md)
變更群集的 ServiceFabric 升級類型

### [更新-AzureRmServiceFabricDurability](Update-AzureRmServiceFabricDurability.md)
變更群集的持久性層級

### [更新-AzureRmServiceFabricReliability](Update-AzureRmServiceFabricReliability.md)
變更群集的可靠性層級
