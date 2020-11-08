---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubCluster.md
ms.openlocfilehash: 4e2657d6a4af26b96a2e7a97a56b735838610005
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140144"
---
# <span data-ttu-id="910ce-101">Get-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="910ce-101">Get-AzEventHubCluster</span></span>

## <span data-ttu-id="910ce-102">摘要</span><span class="sxs-lookup"><span data-stu-id="910ce-102">SYNOPSIS</span></span>
<span data-ttu-id="910ce-103">取得單一事件中心群集的詳細資料，或取得事件中心群集的清單。</span><span class="sxs-lookup"><span data-stu-id="910ce-103">Gets the details of a single Event Hub Cluster , or gets a list of Event Hub Clusters.</span></span>

## <span data-ttu-id="910ce-104">句法</span><span class="sxs-lookup"><span data-stu-id="910ce-104">SYNTAX</span></span>

```
Get-AzEventHubCluster [-ResourceGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="910ce-105">說明</span><span class="sxs-lookup"><span data-stu-id="910ce-105">DESCRIPTION</span></span>
<span data-ttu-id="910ce-106">Get-AzEventHubCluster Cmdlet 會傳回事件中心群集的詳細資料，或傳回指定資源群組中所有事件中心群集的清單。</span><span class="sxs-lookup"><span data-stu-id="910ce-106">The Get-AzEventHubCluster cmdlet returns either the details of an Event Hub Cluster, or a list of all Event Hub Clusters in given resource group.</span></span>
<span data-ttu-id="910ce-107">如果提供了 [群集名稱]，則會傳回單一群集的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="910ce-107">If the cluster name is provided, the details of a single cluster are returned.</span></span>
<span data-ttu-id="910ce-108">如果未提供群集名稱，則會傳回指定資源群組中的所有群集清單。</span><span class="sxs-lookup"><span data-stu-id="910ce-108">If an cluster name is not provided, a list of all clusters in the specified resource group is returned.</span></span>

## <span data-ttu-id="910ce-109">示例</span><span class="sxs-lookup"><span data-stu-id="910ce-109">EXAMPLES</span></span>

### <span data-ttu-id="910ce-110">範例1</span><span class="sxs-lookup"><span data-stu-id="910ce-110">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557

Id        : /subscriptions/326100e2-f69d-4268-8503-075374f62b6e/resourceGroups/RSG-Cluster27651/providers/Microsoft.Eve
            ntHub/clusters/Eventhub-Cluster-5557
Name      : Eventhub-Cluster-5557
Location  : southcentralus
CreatedAt : 09/10/2020 22:09:57
UpdatedAt : 09/10/2020 23:02:48
MetricId  :
Status    :
Sku       : Microsoft.Azure.Commands.EventHub.Models.PSEventHubsClusterSkuAttributes
Tags      : {[ClusterTag2, Tag4], [ClusterTag1, Tag3]}

```

<span data-ttu-id="910ce-111">從資源群組 [RSG-Cluster27651] 傳回群集「Eventhub-5557」的 detials</span><span class="sxs-lookup"><span data-stu-id="910ce-111">Returns the detials of cluster 'Eventhub-Cluster-5557' from the resource group 'RSG-Cluster27651'</span></span>

## <span data-ttu-id="910ce-112">參數</span><span class="sxs-lookup"><span data-stu-id="910ce-112">PARAMETERS</span></span>

### <span data-ttu-id="910ce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="910ce-113">-DefaultProfile</span></span>
<span data-ttu-id="910ce-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="910ce-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="910ce-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="910ce-115">-Name</span></span>
<span data-ttu-id="910ce-116">群集名稱</span><span class="sxs-lookup"><span data-stu-id="910ce-116">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="910ce-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="910ce-117">-ResourceGroupName</span></span>
<span data-ttu-id="910ce-118">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="910ce-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="910ce-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="910ce-119">CommonParameters</span></span>
<span data-ttu-id="910ce-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="910ce-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="910ce-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="910ce-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="910ce-122">輸入</span><span class="sxs-lookup"><span data-stu-id="910ce-122">INPUTS</span></span>

### <span data-ttu-id="910ce-123">System.object</span><span class="sxs-lookup"><span data-stu-id="910ce-123">System.String</span></span>

## <span data-ttu-id="910ce-124">輸出</span><span class="sxs-lookup"><span data-stu-id="910ce-124">OUTPUTS</span></span>

### <span data-ttu-id="910ce-125">PSEventHubAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="910ce-125">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="910ce-126">筆記</span><span class="sxs-lookup"><span data-stu-id="910ce-126">NOTES</span></span>

## <span data-ttu-id="910ce-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="910ce-127">RELATED LINKS</span></span>
