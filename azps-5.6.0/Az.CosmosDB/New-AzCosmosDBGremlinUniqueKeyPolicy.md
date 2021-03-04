---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
ms.openlocfilehash: 54f7a1cb17413fe9d6703dbd0e909555e0c3926a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903282"
---
# <span data-ttu-id="6673b-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="6673b-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span></span>

## <span data-ttu-id="6673b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6673b-102">SYNOPSIS</span></span>
<span data-ttu-id="6673b-103">建立一個新的部格DB UniqueKeyPolicy 物件。</span><span class="sxs-lookup"><span data-stu-id="6673b-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="6673b-104">語法</span><span class="sxs-lookup"><span data-stu-id="6673b-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6673b-105">描述</span><span class="sxs-lookup"><span data-stu-id="6673b-105">DESCRIPTION</span></span>
<span data-ttu-id="6673b-106">**New-AzCosmosDBGremlinUniqueKeyPolicy** Cmdlet 會建立 PSUniqueKeyPolicy 類型的新物件。</span><span class="sxs-lookup"><span data-stu-id="6673b-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="6673b-107">例子</span><span class="sxs-lookup"><span data-stu-id="6673b-107">EXAMPLES</span></span>

### <span data-ttu-id="6673b-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="6673b-108">Example 1</span></span>
```powershell
PS C:\> $uk = New-AzCosmosDBGremlinUniqueKey -Path "abc"

 New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey $uk,$uk
 
 UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="6673b-109">參數</span><span class="sxs-lookup"><span data-stu-id="6673b-109">PARAMETERS</span></span>

### <span data-ttu-id="6673b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6673b-110">-DefaultProfile</span></span>
<span data-ttu-id="6673b-111">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6673b-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6673b-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="6673b-112">-UniqueKey</span></span>
<span data-ttu-id="6673b-113">類型 PSUniqueKey 的物件陣列。</span><span class="sxs-lookup"><span data-stu-id="6673b-113">Array of objects of type PSUniqueKey.</span></span>

```yaml
Type: PSSqlUniqueKey[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6673b-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6673b-114">CommonParameters</span></span>
<span data-ttu-id="6673b-115">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6673b-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6673b-116">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6673b-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6673b-117">輸入</span><span class="sxs-lookup"><span data-stu-id="6673b-117">INPUTS</span></span>

### <span data-ttu-id="6673b-118">沒有</span><span class="sxs-lookup"><span data-stu-id="6673b-118">None</span></span>

## <span data-ttu-id="6673b-119">輸出</span><span class="sxs-lookup"><span data-stu-id="6673b-119">OUTPUTS</span></span>

### <span data-ttu-id="6673b-120">Microsoft.Azure.Commands.AzsDB.models.PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="6673b-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

## <span data-ttu-id="6673b-121">筆記</span><span class="sxs-lookup"><span data-stu-id="6673b-121">NOTES</span></span>

## <span data-ttu-id="6673b-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="6673b-122">RELATED LINKS</span></span>
