---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbmongodbindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
ms.openlocfilehash: c88e1567a7784f89eadd112d7a985b1f2f286a40
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285497"
---
# <span data-ttu-id="1b074-101">New-AzCosmosDBMongoDBIndex</span><span class="sxs-lookup"><span data-stu-id="1b074-101">New-AzCosmosDBMongoDBIndex</span></span>

## <span data-ttu-id="1b074-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1b074-102">SYNOPSIS</span></span>
<span data-ttu-id="1b074-103">建立新的 CosmosDB MongoDB 索引。</span><span class="sxs-lookup"><span data-stu-id="1b074-103">Creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="1b074-104">句法</span><span class="sxs-lookup"><span data-stu-id="1b074-104">SYNTAX</span></span>

```
New-AzCosmosDBMongoDBIndex [-TtlInSeconds <Int32>] [-Unique <Boolean>] [-Key <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b074-105">說明</span><span class="sxs-lookup"><span data-stu-id="1b074-105">DESCRIPTION</span></span>
<span data-ttu-id="1b074-106">**新的-AzCosmosDBMongoDBIndex** 會建立新的 CosmosDB MongoDB 索引。</span><span class="sxs-lookup"><span data-stu-id="1b074-106">The **New-AzCosmosDBMongoDBIndex** creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="1b074-107">示例</span><span class="sxs-lookup"><span data-stu-id="1b074-107">EXAMPLES</span></span>

### <span data-ttu-id="1b074-108">範例1</span><span class="sxs-lookup"><span data-stu-id="1b074-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBMongoDBIndex -TtlInSeconds {val} -Unique 1 -Key "key1"
Key                                                       Options
---                                                       -------
Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexKeys Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexOptions
```

## <span data-ttu-id="1b074-109">參數</span><span class="sxs-lookup"><span data-stu-id="1b074-109">PARAMETERS</span></span>

### <span data-ttu-id="1b074-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b074-110">-DefaultProfile</span></span>
<span data-ttu-id="1b074-111">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1b074-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b074-112">-鍵</span><span class="sxs-lookup"><span data-stu-id="1b074-112">-Key</span></span>
<span data-ttu-id="1b074-113">以字串形式顯示的主要值陣列。</span><span class="sxs-lookup"><span data-stu-id="1b074-113">Array of key values as strings.</span></span>

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

### <span data-ttu-id="1b074-114">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="1b074-114">-TtlInSeconds</span></span>
<span data-ttu-id="1b074-115">索引到期前的秒數。</span><span class="sxs-lookup"><span data-stu-id="1b074-115">Number of seconds after which the index expires.</span></span>

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

### <span data-ttu-id="1b074-116">-唯一</span><span class="sxs-lookup"><span data-stu-id="1b074-116">-Unique</span></span>
<span data-ttu-id="1b074-117">[Bool]，表示該索引是否是唯一的。</span><span class="sxs-lookup"><span data-stu-id="1b074-117">Bool to indicate if the index is unique or not.</span></span>

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

### <span data-ttu-id="1b074-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b074-118">CommonParameters</span></span>
<span data-ttu-id="1b074-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1b074-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b074-120">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1b074-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b074-121">輸入</span><span class="sxs-lookup"><span data-stu-id="1b074-121">INPUTS</span></span>

### <span data-ttu-id="1b074-122">所有</span><span class="sxs-lookup"><span data-stu-id="1b074-122">None</span></span>

## <span data-ttu-id="1b074-123">輸出</span><span class="sxs-lookup"><span data-stu-id="1b074-123">OUTPUTS</span></span>

### <span data-ttu-id="1b074-124">PSMongoIndex 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="1b074-124">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndex</span></span>

## <span data-ttu-id="1b074-125">筆記</span><span class="sxs-lookup"><span data-stu-id="1b074-125">NOTES</span></span>

## <span data-ttu-id="1b074-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="1b074-126">RELATED LINKS</span></span>
