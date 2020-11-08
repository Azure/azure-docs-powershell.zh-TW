---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
ms.openlocfilehash: 275019b1eaf4854c4fd9e5be84791368fe09efba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969825"
---
# <span data-ttu-id="aac34-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="aac34-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span></span>

## <span data-ttu-id="aac34-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aac34-102">SYNOPSIS</span></span>
<span data-ttu-id="aac34-103">建立新的 CosmosDB UniqueKeyPolicy 物件。</span><span class="sxs-lookup"><span data-stu-id="aac34-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="aac34-104">句法</span><span class="sxs-lookup"><span data-stu-id="aac34-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aac34-105">說明</span><span class="sxs-lookup"><span data-stu-id="aac34-105">DESCRIPTION</span></span>
<span data-ttu-id="aac34-106">**新的-AzCosmosDBGremlinUniqueKeyPolicy** Cmdlet 會建立 PSUniqueKeyPolicy 類型的新物件。</span><span class="sxs-lookup"><span data-stu-id="aac34-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="aac34-107">示例</span><span class="sxs-lookup"><span data-stu-id="aac34-107">EXAMPLES</span></span>

### <span data-ttu-id="aac34-108">範例1</span><span class="sxs-lookup"><span data-stu-id="aac34-108">Example 1</span></span>
```powershell
PS C:\> $uk = New-AzCosmosDBGremlinUniqueKey -Path "abc"

 New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey $uk,$uk
 
 UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="aac34-109">參數</span><span class="sxs-lookup"><span data-stu-id="aac34-109">PARAMETERS</span></span>

### <span data-ttu-id="aac34-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aac34-110">-DefaultProfile</span></span>
<span data-ttu-id="aac34-111">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="aac34-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aac34-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="aac34-112">-UniqueKey</span></span>
<span data-ttu-id="aac34-113">類型 PSUniqueKey 的物件陣列。</span><span class="sxs-lookup"><span data-stu-id="aac34-113">Array of objects of type PSUniqueKey.</span></span>

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

### <span data-ttu-id="aac34-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aac34-114">CommonParameters</span></span>
<span data-ttu-id="aac34-115">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aac34-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aac34-116">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="aac34-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aac34-117">輸入</span><span class="sxs-lookup"><span data-stu-id="aac34-117">INPUTS</span></span>

### <span data-ttu-id="aac34-118">所有</span><span class="sxs-lookup"><span data-stu-id="aac34-118">None</span></span>

## <span data-ttu-id="aac34-119">輸出</span><span class="sxs-lookup"><span data-stu-id="aac34-119">OUTPUTS</span></span>

### <span data-ttu-id="aac34-120">PSUniqueKeyPolicy 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="aac34-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

## <span data-ttu-id="aac34-121">筆記</span><span class="sxs-lookup"><span data-stu-id="aac34-121">NOTES</span></span>

## <span data-ttu-id="aac34-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="aac34-122">RELATED LINKS</span></span>
