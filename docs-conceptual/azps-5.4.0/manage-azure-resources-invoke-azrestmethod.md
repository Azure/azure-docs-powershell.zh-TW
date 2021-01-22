---
title: 使用 Invoke-AzRestMethod 管理 Azure 資源
description: 如何使用 Azure PowerShell 透過 Invoke-AzRestMethod Cmdlet 來管理資源。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/24/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 5fdb8543630198d141d42626dc3a8b85f0bcdaa7
ms.sourcegitcommit: 12bb1a6d1f89789bf2a78992f9b8ca848691a4d7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/19/2021
ms.locfileid: "98573637"
---
# <a name="manage-azure-resources-with-invoke-azrestmethod"></a>使用 Invoke-AzRestMethod 管理 Azure 資源

[Invoke-AzRestMethod](/powershell/module/az.accounts/invoke-azrestmethod) 是 Azure PowerShell Cmdlet，在 Az PowerShell 模組 4.4.0 版引進。 其允許您使用 Az 內容對 Azure Resource Management (ARM) 端點提出自訂 HTTP 要求。

當您想要針對 Az PowerShell 模組中尚未提供的功能來管理 Azure 服務時，此 Cmdlet 會很有用。

## <a name="how-to-use-invoke-azrestmethod"></a>如何使用 Invoke-AzRestMethod

舉例來說，您可以只允許存取特定網路的 Azure Container Registry (ACR)，或拒絕公用存取。 截至 Az PowerShell 模組 4.5.0 版，這項功能尚無法在 [Az.ContainerRegistry PowerShell 模組](/powershell/module/Az.ContainerRegistry/)中使用。 不過，此功能可以在過渡期中使用 `Invoke-AzRestMethod` 進行管理。

## <a name="using-invoke-azrestmethod-with-get-operations"></a>搭配 GET 作業使用 Invoke-AzRestMethod

下列範例示範如何搭配 GET 作業使用 `Invoke-AzRestMethod`：

```azurepowershell-interactive
$getParams = @{
  ResourceGroupName = 'myresourcegroup'
  ResourceProviderName = 'Microsoft.ContainerRegistry'
  ResourceType = 'registries'
  Name = 'myacr'
  ApiVersion = '2019-12-01-preview'
  Method = 'GET'
}
Invoke-AzRestMethod @getParams
```

為了允許有最大彈性，`Invoke-AzRestMethod` 的大部分參數都是選擇性的。
不過，當您管理資源群組中的資源時，很可能需要提供資源的完整識別碼，或像是資源群組、資源提供者和資源類型的參數。

當目標資源需要一個以上的名稱時，`ResourceType` 和 `Name` 參數可以接受多個值。 例如，若要在 Log Analytics 工作區中操作已儲存的搜尋，參數看起來會如下列範例所示：`-ResourceType @('workspaces', 'savedsearches') -Name @('my-la', 'my-search')`。

根據陣列中的位置使用對應，此 Cmdlet 會建構下列資源：`Id:'/workspaces/my-la/savedsearches/my-search'`。

`APIVersion` 參數可讓您使用特定的 API 版本，包括預覽版。 您可以在 [azure-rest-api-specs](https://github.com/Azure/azure-rest-api-specs) GitHub 存放庫中找到適用於 Azure 資源提供者的支援 API 版本。

您可以在下列位置中找到 2019-12-01-preview 版本 ACR 的定義：[azure-rest-api-specs/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/](https://github.com/Azure/azure-rest-api-specs/tree/master/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview)。

## <a name="using-invoke-azrestmethod-with-patch-operations"></a>搭配 PATCH 作業使用 Invoke-AzRestMethod

您可以使用 `Invoke-AzRestMethod` Cmdlet 在 `myresourcegroup` 資源群組中停用名為 `myacr` 的現有 ACR 公用存取。

若要停用公用網路存取，您需要對 API 進行 **PATCH** 呼叫，變更 `publicNetwokAccess` 參數的值，如下列範例所示：

```azurepowershell-interactive
$patchParams = @{
  ResourceGroupName = 'myresourcegroup'
  Name = 'myacr'
  ResourceProviderName = 'Microsoft.ContainerRegistry'
  ResourceType = 'registries'
  ApiVersion = '2019-12-01-preview'
  Payload = '{ "properties": {
     "publicNetworkAccess": "Disabled"
     } }'
  Method = 'PATCH'
}
Invoke-AzRestMethod @patchParams
```

`Payload` 屬性是 JSON 字串，可顯示要修改屬性的路徑。

此 API 的所有參數都會在與此 API 相關聯的 **rest-api-spec** 檔案中加以說明。
您可以在 2019-12-01 預覽版本 API 的[容器登錄 JSON 檔案](https://github.com/Azure/azure-rest-api-specs/blob/2a9da9a79d0a7b74089567ec4f0289f3e0f31bec/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/2019-12-01-preview/containerregistry.json)中找到 publicNetworkAccess 參數的定義。

若只要允許從特定 IP 位址存取登錄，則必須修改承載，如下列範例所示：

```azurepowershell-interactive
$specificIpParams = @{
  ResourceGroupName = 'myresourcegroup'
  Name = 'myacr'
  ResourceProviderName = 'Microsoft.ContainerRegistry'
  ResourceType = 'registries'
  ApiVersion = '2019-12-01-preview'
  Payload = '{ "properties": {
      "networkRuleSet": {
      "defaultAction": "Deny",
      "ipRules": [ {
         "action": "Allow",
         "value": "24.22.123.123"
         } ]
      }
  } }'
  -Method = 'PATCH'
}
Invoke-AzRestMethod @specificIpParams
```

## <a name="comparison-to-get-azresource-new-azresource-and-remove-azresource"></a>與 Get-AzResource、New-AzResource 和 Remove-AzResource 的比較

`*-AzResource` Cmdlet 可讓您藉由指定資源類型、API 版本和要更新的屬性，自訂對 Azure 的 REST API 呼叫。 不過，您必須先將屬性建立為 `PSObject`。 此程序會使複雜度提高一層，而且很容易就會變得複雜。

`Invoke-AzRestMethod` 提供簡單的 Azure 資源管理方式。 如先前範例所示，您可以建立 JSON 字串，並使用該字串來自訂 REST API 呼叫，而不需要預先建立任何 `PSObjects`。

如果已經熟悉 `*-AzResource` Cmdlet，則可以繼續使用。 我們不打算停止支援。 在 `Invoke-AzRestMethod` 中，我們已將新的 Cmdlet 新增至您的工具組。

## <a name="see-also"></a>另請參閱

* [Get-AzResource](/powershell/module/az.resources/get-azresource)
* [New-AzResource](/powershell/module/az.resources/new-azresource)
* [Remove-AzResource](/powershell/module/az.resources/remove-azresource)
