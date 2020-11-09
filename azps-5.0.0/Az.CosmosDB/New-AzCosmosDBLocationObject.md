---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdblocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
ms.openlocfilehash: 59fee5840ec279c7ed11b9b9d738561caf03ec66
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285504"
---
# <span data-ttu-id="2ed65-101">New-AzCosmosDBLocationObject</span><span class="sxs-lookup"><span data-stu-id="2ed65-101">New-AzCosmosDBLocationObject</span></span>

## <span data-ttu-id="2ed65-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2ed65-102">SYNOPSIS</span></span>
<span data-ttu-id="2ed65-103">建立新的 CosmosDB Location 物件 (PSLocation) 。</span><span class="sxs-lookup"><span data-stu-id="2ed65-103">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="2ed65-104">句法</span><span class="sxs-lookup"><span data-stu-id="2ed65-104">SYNTAX</span></span>

```
New-AzCosmosDBLocationObject -LocationName <String> [-FailoverPriority <Int32>] [-IsZoneRedundant <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ed65-105">說明</span><span class="sxs-lookup"><span data-stu-id="2ed65-105">DESCRIPTION</span></span>
<span data-ttu-id="2ed65-106">建立新的 CosmosDB Location 物件 (PSLocation) 。</span><span class="sxs-lookup"><span data-stu-id="2ed65-106">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="2ed65-107">示例</span><span class="sxs-lookup"><span data-stu-id="2ed65-107">EXAMPLES</span></span>

### <span data-ttu-id="2ed65-108">範例1</span><span class="sxs-lookup"><span data-stu-id="2ed65-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBLocationObject -LocationName {locationName} -FailoverPriority 2 -IsZoneRedundant 0

LocationName     FailoverPriority IsZoneRedundant
------------     ---------------- ---------------
{locationName}                 2           False
```

## <span data-ttu-id="2ed65-109">參數</span><span class="sxs-lookup"><span data-stu-id="2ed65-109">PARAMETERS</span></span>

### <span data-ttu-id="2ed65-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ed65-110">-DefaultProfile</span></span>
<span data-ttu-id="2ed65-111">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2ed65-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ed65-112">-FailoverPriority</span><span class="sxs-lookup"><span data-stu-id="2ed65-112">-FailoverPriority</span></span>
<span data-ttu-id="2ed65-113">位置的容錯移轉優先順序。</span><span class="sxs-lookup"><span data-stu-id="2ed65-113">Failover priority of the location.</span></span>

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

### <span data-ttu-id="2ed65-114">-IsZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="2ed65-114">-IsZoneRedundant</span></span>
<span data-ttu-id="2ed65-115">指示此區域是否為 AvailabilityZone 的布林值。</span><span class="sxs-lookup"><span data-stu-id="2ed65-115">Boolean to indicate whether or not this region is an AvailabilityZone.</span></span>

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

### <span data-ttu-id="2ed65-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="2ed65-116">-LocationName</span></span>
<span data-ttu-id="2ed65-117">字串中位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="2ed65-117">Name of the Location in string.</span></span>

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

### <span data-ttu-id="2ed65-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ed65-118">CommonParameters</span></span>
<span data-ttu-id="2ed65-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2ed65-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ed65-120">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2ed65-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ed65-121">輸入</span><span class="sxs-lookup"><span data-stu-id="2ed65-121">INPUTS</span></span>

### <span data-ttu-id="2ed65-122">所有</span><span class="sxs-lookup"><span data-stu-id="2ed65-122">None</span></span>

## <span data-ttu-id="2ed65-123">輸出</span><span class="sxs-lookup"><span data-stu-id="2ed65-123">OUTPUTS</span></span>

### <span data-ttu-id="2ed65-124">PSLocation 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="2ed65-124">Microsoft.Azure.Commands.CosmosDB.Models.PSLocation</span></span>

## <span data-ttu-id="2ed65-125">筆記</span><span class="sxs-lookup"><span data-stu-id="2ed65-125">NOTES</span></span>

## <span data-ttu-id="2ed65-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="2ed65-126">RELATED LINKS</span></span>
