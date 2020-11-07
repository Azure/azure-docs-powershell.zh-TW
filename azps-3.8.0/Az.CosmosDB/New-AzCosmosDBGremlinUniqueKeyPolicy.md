---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
ms.openlocfilehash: 593e299a6d7a1aa8131848f6de5f6c7aec8bd8c9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959587"
---
# <span data-ttu-id="84cfb-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="84cfb-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span></span>

## <span data-ttu-id="84cfb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="84cfb-102">SYNOPSIS</span></span>
<span data-ttu-id="84cfb-103">建立新的 CosmosDB UniqueKeyPolicy 物件。</span><span class="sxs-lookup"><span data-stu-id="84cfb-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="84cfb-104">句法</span><span class="sxs-lookup"><span data-stu-id="84cfb-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey <PSUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="84cfb-105">說明</span><span class="sxs-lookup"><span data-stu-id="84cfb-105">DESCRIPTION</span></span>
<span data-ttu-id="84cfb-106">**新的-AzCosmosDBGremlinUniqueKeyPolicy** Cmdlet 會建立 PSUniqueKeyPolicy 類型的新物件。</span><span class="sxs-lookup"><span data-stu-id="84cfb-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="84cfb-107">示例</span><span class="sxs-lookup"><span data-stu-id="84cfb-107">EXAMPLES</span></span>

### <span data-ttu-id="84cfb-108">範例1</span><span class="sxs-lookup"><span data-stu-id="84cfb-108">Example 1</span></span>
```powershell
PS C:\> $uk = New-AzCosmosDBGremlinUniqueKey -Path "abc"

 New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey $uk,$uk
 
 UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="84cfb-109">參數</span><span class="sxs-lookup"><span data-stu-id="84cfb-109">PARAMETERS</span></span>

### <span data-ttu-id="84cfb-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84cfb-110">-DefaultProfile</span></span>
<span data-ttu-id="84cfb-111">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="84cfb-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84cfb-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="84cfb-112">-UniqueKey</span></span>
<span data-ttu-id="84cfb-113">類型 PSUniqueKey 的物件陣列。</span><span class="sxs-lookup"><span data-stu-id="84cfb-113">Array of objects of type PSUniqueKey.</span></span>

```yaml
Type: PSUniqueKey[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84cfb-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84cfb-114">CommonParameters</span></span>
<span data-ttu-id="84cfb-115">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="84cfb-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84cfb-116">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="84cfb-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84cfb-117">輸入</span><span class="sxs-lookup"><span data-stu-id="84cfb-117">INPUTS</span></span>

### <span data-ttu-id="84cfb-118">所有</span><span class="sxs-lookup"><span data-stu-id="84cfb-118">None</span></span>

## <span data-ttu-id="84cfb-119">輸出</span><span class="sxs-lookup"><span data-stu-id="84cfb-119">OUTPUTS</span></span>

### <span data-ttu-id="84cfb-120">PSUniqueKeyPolicy 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="84cfb-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

## <span data-ttu-id="84cfb-121">筆記</span><span class="sxs-lookup"><span data-stu-id="84cfb-121">NOTES</span></span>

## <span data-ttu-id="84cfb-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="84cfb-122">RELATED LINKS</span></span>
