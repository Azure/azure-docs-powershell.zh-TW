---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
ms.openlocfilehash: d60284cec84c1b0a023f06a77acfe794d8d5315f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959570"
---
# <span data-ttu-id="682a6-101">New-AzCosmosDBVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="682a6-101">New-AzCosmosDBVirtualNetworkRule</span></span>

## <span data-ttu-id="682a6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="682a6-102">SYNOPSIS</span></span>
<span data-ttu-id="682a6-103">建立新的 CosmosDB VirtualNetworkRule 物件 (PSVirtualNetworkRule]) 。</span><span class="sxs-lookup"><span data-stu-id="682a6-103">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="682a6-104">句法</span><span class="sxs-lookup"><span data-stu-id="682a6-104">SYNTAX</span></span>

```
New-AzCosmosDBVirtualNetworkRule -Id <String> [-IgnoreMissingVNetServiceEndpoint <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="682a6-105">說明</span><span class="sxs-lookup"><span data-stu-id="682a6-105">DESCRIPTION</span></span>
<span data-ttu-id="682a6-106">建立新的 CosmosDB VirtualNetworkRule 物件 (PSVirtualNetworkRule]) 。</span><span class="sxs-lookup"><span data-stu-id="682a6-106">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="682a6-107">示例</span><span class="sxs-lookup"><span data-stu-id="682a6-107">EXAMPLES</span></span>

### <span data-ttu-id="682a6-108">範例1</span><span class="sxs-lookup"><span data-stu-id="682a6-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBVirtualNetworkRule -Id {id} -IgnoreMissingVNetServiceEndpoint 0
Id  IgnoreMissingVNetServiceEndpoint
--   --------------------------------
{id}                            False
```

## <span data-ttu-id="682a6-109">參數</span><span class="sxs-lookup"><span data-stu-id="682a6-109">PARAMETERS</span></span>

### <span data-ttu-id="682a6-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="682a6-110">-DefaultProfile</span></span>
<span data-ttu-id="682a6-111">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="682a6-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="682a6-112">-識別碼</span><span class="sxs-lookup"><span data-stu-id="682a6-112">-Id</span></span>
<span data-ttu-id="682a6-113">子網的資源識別碼，例如：/subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span><span class="sxs-lookup"><span data-stu-id="682a6-113">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="682a6-114">-IgnoreMissingVNetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="682a6-114">-IgnoreMissingVNetServiceEndpoint</span></span>
<span data-ttu-id="682a6-115">布林值，指出在虛擬網路啟用 vnet 服務端點前，是否要建立防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="682a6-115">Boolean to indicate if to create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="682a6-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="682a6-116">CommonParameters</span></span>
<span data-ttu-id="682a6-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="682a6-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="682a6-118">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="682a6-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="682a6-119">輸入</span><span class="sxs-lookup"><span data-stu-id="682a6-119">INPUTS</span></span>

### <span data-ttu-id="682a6-120">所有</span><span class="sxs-lookup"><span data-stu-id="682a6-120">None</span></span>

## <span data-ttu-id="682a6-121">輸出</span><span class="sxs-lookup"><span data-stu-id="682a6-121">OUTPUTS</span></span>

### <span data-ttu-id="682a6-122">PSVirtualNetworkRule 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="682a6-122">Microsoft.Azure.Commands.CosmosDB.Models.PSVirtualNetworkRule</span></span>

## <span data-ttu-id="682a6-123">筆記</span><span class="sxs-lookup"><span data-stu-id="682a6-123">NOTES</span></span>

## <span data-ttu-id="682a6-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="682a6-124">RELATED LINKS</span></span>
