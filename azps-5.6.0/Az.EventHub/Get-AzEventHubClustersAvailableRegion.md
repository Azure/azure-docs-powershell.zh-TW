---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhubclustersavailableregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubClustersAvailableRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubClustersAvailableRegion.md
ms.openlocfilehash: 633881b298059c35a54591bb1ff93d4e93a267d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902601"
---
# <span data-ttu-id="f6437-101">Get-AzEventHubClustersAvailableRegion</span><span class="sxs-lookup"><span data-stu-id="f6437-101">Get-AzEventHubClustersAvailableRegion</span></span>

## <span data-ttu-id="f6437-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f6437-102">SYNOPSIS</span></span>
<span data-ttu-id="f6437-103">在給定資源群組中，獲得單一 Eventhub 群組或群組清單的詳細資訊</span><span class="sxs-lookup"><span data-stu-id="f6437-103">Gets the details of single Eventhub cluster or the list of clusters in the given Resource Group</span></span>

## <span data-ttu-id="f6437-104">語法</span><span class="sxs-lookup"><span data-stu-id="f6437-104">SYNTAX</span></span>

```
Get-AzEventHubClustersAvailableRegion [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6437-105">描述</span><span class="sxs-lookup"><span data-stu-id="f6437-105">DESCRIPTION</span></span>
<span data-ttu-id="f6437-106">可Get-AzEventHubClustersAvailableRegion私人區域的 Cmdlet 清單。</span><span class="sxs-lookup"><span data-stu-id="f6437-106">The Get-AzEventHubClustersAvailableRegion cmdlet list of regions where dedicated are available to create.</span></span>

## <span data-ttu-id="f6437-107">例子</span><span class="sxs-lookup"><span data-stu-id="f6437-107">EXAMPLES</span></span>

### <span data-ttu-id="f6437-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="f6437-108">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubClustersAvailableRegion

Location
--------
northcentralus
westeurope
uksouth
westcentralus
australiasoutheast
ukwest
brazilsouth
centralus
australiaeast
eastus
southcentralus
japaneast
northeurope
eastus2
southeastasia
eastasia
westus
westus2
```

<span data-ttu-id="f6437-109">區域清單會回到</span><span class="sxs-lookup"><span data-stu-id="f6437-109">List of regions is returned where</span></span>

## <span data-ttu-id="f6437-110">參數</span><span class="sxs-lookup"><span data-stu-id="f6437-110">PARAMETERS</span></span>

### <span data-ttu-id="f6437-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6437-111">-DefaultProfile</span></span>
<span data-ttu-id="f6437-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f6437-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6437-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6437-113">CommonParameters</span></span>
<span data-ttu-id="f6437-114">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f6437-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6437-115">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f6437-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6437-116">輸入</span><span class="sxs-lookup"><span data-stu-id="f6437-116">INPUTS</span></span>

### <span data-ttu-id="f6437-117">沒有</span><span class="sxs-lookup"><span data-stu-id="f6437-117">None</span></span>

## <span data-ttu-id="f6437-118">輸出</span><span class="sxs-lookup"><span data-stu-id="f6437-118">OUTPUTS</span></span>

### <span data-ttu-id="f6437-119">System.Collections.Generic.IEnumerable'1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubsAvailableCluster, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.5.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="f6437-119">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubsAvailableCluster, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f6437-120">筆記</span><span class="sxs-lookup"><span data-stu-id="f6437-120">NOTES</span></span>

## <span data-ttu-id="f6437-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="f6437-121">RELATED LINKS</span></span>
