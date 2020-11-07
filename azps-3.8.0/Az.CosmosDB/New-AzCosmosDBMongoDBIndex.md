---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbmongodbindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
ms.openlocfilehash: c88e1567a7784f89eadd112d7a985b1f2f286a40
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959589"
---
# <span data-ttu-id="015b0-101">New-AzCosmosDBMongoDBIndex</span><span class="sxs-lookup"><span data-stu-id="015b0-101">New-AzCosmosDBMongoDBIndex</span></span>

## <span data-ttu-id="015b0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="015b0-102">SYNOPSIS</span></span>
<span data-ttu-id="015b0-103">建立新的 CosmosDB MongoDB 索引。</span><span class="sxs-lookup"><span data-stu-id="015b0-103">Creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="015b0-104">句法</span><span class="sxs-lookup"><span data-stu-id="015b0-104">SYNTAX</span></span>

```
New-AzCosmosDBMongoDBIndex [-TtlInSeconds <Int32>] [-Unique <Boolean>] [-Key <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="015b0-105">說明</span><span class="sxs-lookup"><span data-stu-id="015b0-105">DESCRIPTION</span></span>
<span data-ttu-id="015b0-106">**新的-AzCosmosDBMongoDBIndex** 會建立新的 CosmosDB MongoDB 索引。</span><span class="sxs-lookup"><span data-stu-id="015b0-106">The **New-AzCosmosDBMongoDBIndex** creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="015b0-107">示例</span><span class="sxs-lookup"><span data-stu-id="015b0-107">EXAMPLES</span></span>

### <span data-ttu-id="015b0-108">範例1</span><span class="sxs-lookup"><span data-stu-id="015b0-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBMongoDBIndex -TtlInSeconds {val} -Unique 1 -Key "key1"
Key                                                       Options
---                                                       -------
Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexKeys Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexOptions
```

## <span data-ttu-id="015b0-109">參數</span><span class="sxs-lookup"><span data-stu-id="015b0-109">PARAMETERS</span></span>

### <span data-ttu-id="015b0-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="015b0-110">-DefaultProfile</span></span>
<span data-ttu-id="015b0-111">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="015b0-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="015b0-112">-鍵</span><span class="sxs-lookup"><span data-stu-id="015b0-112">-Key</span></span>
<span data-ttu-id="015b0-113">以字串形式顯示的主要值陣列。</span><span class="sxs-lookup"><span data-stu-id="015b0-113">Array of key values as strings.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="015b0-114">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="015b0-114">-TtlInSeconds</span></span>
<span data-ttu-id="015b0-115">索引到期前的秒數。</span><span class="sxs-lookup"><span data-stu-id="015b0-115">Number of seconds after which the index expires.</span></span>

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

### <span data-ttu-id="015b0-116">-唯一</span><span class="sxs-lookup"><span data-stu-id="015b0-116">-Unique</span></span>
<span data-ttu-id="015b0-117">[Bool]，表示該索引是否是唯一的。</span><span class="sxs-lookup"><span data-stu-id="015b0-117">Bool to indicate if the index is unique or not.</span></span>

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

### <span data-ttu-id="015b0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="015b0-118">CommonParameters</span></span>
<span data-ttu-id="015b0-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="015b0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="015b0-120">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="015b0-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="015b0-121">輸入</span><span class="sxs-lookup"><span data-stu-id="015b0-121">INPUTS</span></span>

### <span data-ttu-id="015b0-122">所有</span><span class="sxs-lookup"><span data-stu-id="015b0-122">None</span></span>

## <span data-ttu-id="015b0-123">輸出</span><span class="sxs-lookup"><span data-stu-id="015b0-123">OUTPUTS</span></span>

### <span data-ttu-id="015b0-124">PSMongoIndex 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="015b0-124">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndex</span></span>

## <span data-ttu-id="015b0-125">筆記</span><span class="sxs-lookup"><span data-stu-id="015b0-125">NOTES</span></span>

## <span data-ttu-id="015b0-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="015b0-126">RELATED LINKS</span></span>
