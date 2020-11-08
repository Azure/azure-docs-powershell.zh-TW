---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubclustersavailableregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubClustersAvailableRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubClustersAvailableRegion.md
ms.openlocfilehash: 712e9274eabe27bbe5f4a8acce704926e1e895fe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135980"
---
# <span data-ttu-id="87051-101">Get-AzEventHubClustersAvailableRegion</span><span class="sxs-lookup"><span data-stu-id="87051-101">Get-AzEventHubClustersAvailableRegion</span></span>

## <span data-ttu-id="87051-102">摘要</span><span class="sxs-lookup"><span data-stu-id="87051-102">SYNOPSIS</span></span>
<span data-ttu-id="87051-103">取得特定資源群組中單一 Eventhub 群集或群集清單的詳細資料</span><span class="sxs-lookup"><span data-stu-id="87051-103">Gets the details of single Eventhub cluster or the list of clusters in the given Resource Group</span></span>

## <span data-ttu-id="87051-104">句法</span><span class="sxs-lookup"><span data-stu-id="87051-104">SYNTAX</span></span>

```
Get-AzEventHubClustersAvailableRegion [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87051-105">說明</span><span class="sxs-lookup"><span data-stu-id="87051-105">DESCRIPTION</span></span>
<span data-ttu-id="87051-106">可供建立專用之區域的 Get-AzEventHubClustersAvailableRegion Cmdlet 清單。</span><span class="sxs-lookup"><span data-stu-id="87051-106">The Get-AzEventHubClustersAvailableRegion cmdlet list of regions where dedicated are available to create.</span></span>

## <span data-ttu-id="87051-107">示例</span><span class="sxs-lookup"><span data-stu-id="87051-107">EXAMPLES</span></span>

### <span data-ttu-id="87051-108">範例1</span><span class="sxs-lookup"><span data-stu-id="87051-108">Example 1</span></span>
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

<span data-ttu-id="87051-109">會傳回區域清單，其中</span><span class="sxs-lookup"><span data-stu-id="87051-109">List of regions is returned where</span></span>

## <span data-ttu-id="87051-110">參數</span><span class="sxs-lookup"><span data-stu-id="87051-110">PARAMETERS</span></span>

### <span data-ttu-id="87051-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87051-111">-DefaultProfile</span></span>
<span data-ttu-id="87051-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="87051-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87051-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87051-113">CommonParameters</span></span>
<span data-ttu-id="87051-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="87051-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87051-115">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="87051-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87051-116">輸入</span><span class="sxs-lookup"><span data-stu-id="87051-116">INPUTS</span></span>

### <span data-ttu-id="87051-117">所有</span><span class="sxs-lookup"><span data-stu-id="87051-117">None</span></span>

## <span data-ttu-id="87051-118">輸出</span><span class="sxs-lookup"><span data-stu-id="87051-118">OUTPUTS</span></span>

### <span data-ttu-id="87051-119">System.object. IEnumerable ' 1 [PSEventHubsAvailableCluster，1.5.0.0，，Version =，Culture = 中性，PublicKeyToken = null]」）。））））））</span><span class="sxs-lookup"><span data-stu-id="87051-119">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubsAvailableCluster, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="87051-120">筆記</span><span class="sxs-lookup"><span data-stu-id="87051-120">NOTES</span></span>

## <span data-ttu-id="87051-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="87051-121">RELATED LINKS</span></span>
