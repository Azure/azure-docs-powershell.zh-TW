---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: b35ba1bcd976bbc563dd8e3ad6640279a5a8a1dd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904829"
---
# Az.ServiceFabric 模組
## 描述
您可以使用 Azure Service Fabric 模組來自動化兩端作業，例如建立安全性群組狀組、捲動組狀憑證、新增或移除該組集中的節點等等。以下列出所有作業的完整清單。

## Az.ServiceFabric Cmdlets
### [Add-AzServiceFabricClientCertificate](Add-AzServiceFabricClientCertificate.md)
將常用名稱或指紋新增到該組組，以用於用戶端驗證。

### [Add-AzServiceFabricClusterCertificate](Add-AzServiceFabricClusterCertificate.md)
新增次要組群憑證至該組。

### [Add-AzServiceFabricManagedClusterClientCertificate](Add-AzServiceFabricManagedClusterClientCertificate.md)
在組塊中新增憑證通用名稱或指紋。 這將會再次註冊憑證，以用於用戶端驗證目的。

### [Add-AzServiceFabricManagedNodeTypeEVExtension](Add-AzServiceFabricManagedNodeTypeVMExtension.md)
新增 vm 擴充功能至節點類型。

### [Add-AzServiceFabricManagedNodeTypeMSSECret](Add-AzServiceFabricManagedNodeTypeVMSecret.md)
新增憑證金鑰至節點類型。

### [Add-AzServiceFabricNode](Add-AzServiceFabricNode.md)
將節點新增到該群中的特定節點類型。

### [Add-AzServiceFabricNodeType](Add-AzServiceFabricNodeType.md)
新增節點類型至現有組。

### [Get-AzServiceFabricApplication](Get-AzServiceFabricApplication.md)
取得 Service Fabric 應用程式詳細資料。

### [Get-AzServiceFabricApplicationType](Get-AzServiceFabricApplicationType.md)
取得 Service Fabric 應用程式類型詳細資料。

### [Get-AzServiceFabricApplicationTypeVersion](Get-AzServiceFabricApplicationTypeVersion.md)
取得 Service Fabric 應用程式類型版本詳細資料。

### [Get-AzServiceFabricCluster](Get-AzServiceFabricCluster.md)
取得組群資源詳細資料。

### [Get-AzServiceFabricManagedCluster](Get-AzServiceFabricManagedCluster.md)
取得受管理的組群資源詳細資料。

### [Get-AzServiceFabricManagedNodeType](Get-AzServiceFabricManagedNodeType.md)
取得受管理的節點類型資源詳細資料。

### [Get-AzServiceFabricService](Get-AzServiceFabricService.md)
取得指定應用程式和組群下的 Service Fabric 服務詳細資料。

### [New-AzServiceFabricApplication](New-AzServiceFabricApplication.md)
在指定的資源群組和群組下建立新的服務結構應用程式。

### [New-AzServiceFabricApplicationType](New-AzServiceFabricApplicationType.md)
在指定的資源群組和群組下，建立新的服務結構應用程式類型。

### [New-AzServiceFabricApplicationTypeVersion](New-AzServiceFabricApplicationTypeVersion.md)
在指定的資源群組和群組下建立新應用程式類型版本。

### [New-AzServiceFabricCluster](New-AzServiceFabricCluster.md)
此命令會使用您提供的憑證或系統產生的自我簽署憑證來設定新的服務結構組組。 它可以使用預設範本或您提供的自訂範本。 您可以選擇指定資料夾，將自我簽署憑證匯出至該憑證，或稍後從金鑰庫抓取。

### [New-AzServiceFabricManagedCluster](New-AzServiceFabricManagedCluster.md)
建立新受管理的集區。

### [New-AzServiceFabricManagedNodeType](New-AzServiceFabricManagedNodeType.md)
建立新節點類型資源。

### [New-AzServiceFabricService](New-AzServiceFabricService.md)
在指定的應用程式和組集中建立新的服務結構服務。

### [Remove-AzServiceFabricApplication](Remove-AzServiceFabricApplication.md)
從組群移除應用程式。 這會移除應用程式下的所有服務。

### [Remove-AzServiceFabricApplicationType](Remove-AzServiceFabricApplicationType.md)
從組群移除服務結構應用程式類型。 這會移除此資源下的所有類型版本。

### [Remove-AzServiceFabricApplicationTypeVersion](Remove-AzServiceFabricApplicationTypeVersion.md)
從組集中移除服務結構的應用程式類型版本。

### [Remove-AzServiceFabricClientCertificate](Remove-AzServiceFabricClientCertificate.md)
移除用戶端憑證 () 或憑證 () 名稱 () ，以用於用戶端驗證至該組。

### [Remove-AzServiceFabricClusterCertificate](Remove-AzServiceFabricClusterCertificate.md)
移除用於保護集區安全性的集區憑證。

### [Remove-AzServiceFabricManagedCluster](Remove-AzServiceFabricManagedCluster.md)
移除組群資源。

### [Remove-AzServiceFabricManagedClusterClientCertificate](Remove-AzServiceFabricManagedClusterClientCertificate.md)
以指紋或通用名稱重新叫用用戶端憑證。

### [Remove-AzServiceFabricManagedNodeType](Remove-AzServiceFabricManagedNodeType.md)
移除節點類型或節點類型中的特定節點。

### [Remove-AzServiceFabricManagedNodeTypeMSEVExtension](Remove-AzServiceFabricManagedNodeTypeVMExtension.md)
從節點類型移除 vm 副檔名。

### [Remove-AzServiceFabricNode](Remove-AzServiceFabricNode.md)
從一個組移除特定節點類型的節點。

### [Remove-AzServiceFabricNodeType](Remove-AzServiceFabricNodeType.md)
從一個組移除完整的節點類型。

### [Remove-AzServiceFabricService](Remove-AzServiceFabricService.md)
從組群移除服務。

### [Remove-AzServiceFabricSetting](Remove-AzServiceFabricSetting.md)
從組群移除一或多個服務結構設定。

### [Restart-AzServiceFabricManagedNodeType](Restart-AzServiceFabricManagedNodeType.md)
從節點類型重新開機特定節點。

### [Set-AzServiceFabricManagedCluster](Set-AzServiceFabricManagedCluster.md)
設定組群資源屬性。

### [Set-AzServiceFabricManagedNodeType](Set-AzServiceFabricManagedNodeType.md)
使用 -Reimage 參數設定節點類型資源屬性，或在節點類型的特定數個數上執行重新映射動作。

### [Set-AzServiceFabricSetting](Set-AzServiceFabricSetting.md)
新增或更新一或多個服務佈設定至該組。

### [Set-AzServiceFabricUpgradeType](Set-AzServiceFabricUpgradeType.md)
變更組群的服務結構升級類型。

### [Update-AzServiceFabricApplication](Update-AzServiceFabricApplication.md)
更新服務結構應用程式。 這可讓您更新應用程式參數和/或升級應用程式類型版本，以觸發應用程式升級。

### [Update-AzServiceFabricDurability](Update-AzServiceFabricDurability.md)
更新該組集中節點類型的節點層級或 VmSKU。

### [Update-AzServiceFabricReliability](Update-AzServiceFabricReliability.md)
更新組集中主要節點類型的可靠性層級。

