---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
ms.openlocfilehash: abc97b0473353a0bc71aae59386bc5b5770b730b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909121"
---
# <span data-ttu-id="1fbb0-101">New-AzCosmosDBVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1fbb0-101">New-AzCosmosDBVirtualNetworkRule</span></span>

## <span data-ttu-id="1fbb0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1fbb0-102">SYNOPSIS</span></span>
<span data-ttu-id="1fbb0-103">在 PSVirtualNetworkRule (建立一個新的一個部 10000000000) 。</span><span class="sxs-lookup"><span data-stu-id="1fbb0-103">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="1fbb0-104">語法</span><span class="sxs-lookup"><span data-stu-id="1fbb0-104">SYNTAX</span></span>

```
New-AzCosmosDBVirtualNetworkRule -Id <String> [-IgnoreMissingVNetServiceEndpoint <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1fbb0-105">描述</span><span class="sxs-lookup"><span data-stu-id="1fbb0-105">DESCRIPTION</span></span>
<span data-ttu-id="1fbb0-106">在 PSVirtualNetworkRule (建立一個新的一個部 10000000000) 。</span><span class="sxs-lookup"><span data-stu-id="1fbb0-106">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="1fbb0-107">例子</span><span class="sxs-lookup"><span data-stu-id="1fbb0-107">EXAMPLES</span></span>

### <span data-ttu-id="1fbb0-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="1fbb0-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBVirtualNetworkRule -Id {id} -IgnoreMissingVNetServiceEndpoint 0
Id  IgnoreMissingVNetServiceEndpoint
--   --------------------------------
{id}                            False
```

## <span data-ttu-id="1fbb0-109">參數</span><span class="sxs-lookup"><span data-stu-id="1fbb0-109">PARAMETERS</span></span>

### <span data-ttu-id="1fbb0-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fbb0-110">-DefaultProfile</span></span>
<span data-ttu-id="1fbb0-111">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1fbb0-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fbb0-112">-Id</span><span class="sxs-lookup"><span data-stu-id="1fbb0-112">-Id</span></span>
<span data-ttu-id="1fbb0-113">子網的資源識別碼，例如：/subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/子網/{子網Name}</span><span class="sxs-lookup"><span data-stu-id="1fbb0-113">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span></span>

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

### <span data-ttu-id="1fbb0-114">-IgnoreMissingVNetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="1fbb0-114">-IgnoreMissingVNetServiceEndpoint</span></span>
<span data-ttu-id="1fbb0-115">布林值，指出在啟用 vnet 服務端點之前，是否建立防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="1fbb0-115">Boolean to indicate if to create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="1fbb0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fbb0-116">CommonParameters</span></span>
<span data-ttu-id="1fbb0-117">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1fbb0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fbb0-118">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1fbb0-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fbb0-119">輸入</span><span class="sxs-lookup"><span data-stu-id="1fbb0-119">INPUTS</span></span>

### <span data-ttu-id="1fbb0-120">沒有</span><span class="sxs-lookup"><span data-stu-id="1fbb0-120">None</span></span>

## <span data-ttu-id="1fbb0-121">輸出</span><span class="sxs-lookup"><span data-stu-id="1fbb0-121">OUTPUTS</span></span>

### <span data-ttu-id="1fbb0-122">Microsoft.Azure.Commands.AzsDB.models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1fbb0-122">Microsoft.Azure.Commands.CosmosDB.Models.PSVirtualNetworkRule</span></span>

## <span data-ttu-id="1fbb0-123">筆記</span><span class="sxs-lookup"><span data-stu-id="1fbb0-123">NOTES</span></span>

## <span data-ttu-id="1fbb0-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="1fbb0-124">RELATED LINKS</span></span>
