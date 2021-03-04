---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdblocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
ms.openlocfilehash: 829bd1f01be1226346d67f9b662915675cd70f80
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910729"
---
# <span data-ttu-id="9489d-101">New-AzCosmosDBLocationObject</span><span class="sxs-lookup"><span data-stu-id="9489d-101">New-AzCosmosDBLocationObject</span></span>

## <span data-ttu-id="9489d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9489d-102">SYNOPSIS</span></span>
<span data-ttu-id="9489d-103">在 PSLocation (中) 。</span><span class="sxs-lookup"><span data-stu-id="9489d-103">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="9489d-104">語法</span><span class="sxs-lookup"><span data-stu-id="9489d-104">SYNTAX</span></span>

```
New-AzCosmosDBLocationObject -LocationName <String> [-FailoverPriority <Int32>] [-IsZoneRedundant <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9489d-105">描述</span><span class="sxs-lookup"><span data-stu-id="9489d-105">DESCRIPTION</span></span>
<span data-ttu-id="9489d-106">在 PSLocation (中) 。</span><span class="sxs-lookup"><span data-stu-id="9489d-106">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="9489d-107">例子</span><span class="sxs-lookup"><span data-stu-id="9489d-107">EXAMPLES</span></span>

### <span data-ttu-id="9489d-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="9489d-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBLocationObject -LocationName {locationName} -FailoverPriority 2 -IsZoneRedundant 0

LocationName     FailoverPriority IsZoneRedundant
------------     ---------------- ---------------
{locationName}                 2           False
```

## <span data-ttu-id="9489d-109">參數</span><span class="sxs-lookup"><span data-stu-id="9489d-109">PARAMETERS</span></span>

### <span data-ttu-id="9489d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9489d-110">-DefaultProfile</span></span>
<span data-ttu-id="9489d-111">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9489d-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9489d-112">-FailoverPriority</span><span class="sxs-lookup"><span data-stu-id="9489d-112">-FailoverPriority</span></span>
<span data-ttu-id="9489d-113">位置的容錯移轉優先順序。</span><span class="sxs-lookup"><span data-stu-id="9489d-113">Failover priority of the location.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9489d-114">-IsZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="9489d-114">-IsZoneRedundant</span></span>
<span data-ttu-id="9489d-115">布林值，表示此區域是否為可用性區域。</span><span class="sxs-lookup"><span data-stu-id="9489d-115">Boolean to indicate whether or not this region is an AvailabilityZone.</span></span>

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

### <span data-ttu-id="9489d-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="9489d-116">-LocationName</span></span>
<span data-ttu-id="9489d-117">字串中位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="9489d-117">Name of the Location in string.</span></span>

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

### <span data-ttu-id="9489d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9489d-118">CommonParameters</span></span>
<span data-ttu-id="9489d-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9489d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9489d-120">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9489d-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9489d-121">輸入</span><span class="sxs-lookup"><span data-stu-id="9489d-121">INPUTS</span></span>

### <span data-ttu-id="9489d-122">沒有</span><span class="sxs-lookup"><span data-stu-id="9489d-122">None</span></span>

## <span data-ttu-id="9489d-123">輸出</span><span class="sxs-lookup"><span data-stu-id="9489d-123">OUTPUTS</span></span>

### <span data-ttu-id="9489d-124">Microsoft.Azure.Commands.AzsDB.models.PSLocation</span><span class="sxs-lookup"><span data-stu-id="9489d-124">Microsoft.Azure.Commands.CosmosDB.Models.PSLocation</span></span>

## <span data-ttu-id="9489d-125">筆記</span><span class="sxs-lookup"><span data-stu-id="9489d-125">NOTES</span></span>

## <span data-ttu-id="9489d-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="9489d-126">RELATED LINKS</span></span>
