---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlinconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
ms.openlocfilehash: c67627068ef2fc90f8322b2e8b63dd6cd68acbe3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916422"
---
# <span data-ttu-id="9afa7-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="9afa7-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span></span>

## <span data-ttu-id="9afa7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9afa7-102">SYNOPSIS</span></span>
<span data-ttu-id="9afa7-103">建立 PSConflictResolutionPolicy 類型的新物件。</span><span class="sxs-lookup"><span data-stu-id="9afa7-103">Creates a new object of type PSConflictResolutionPolicy.</span></span> <span data-ttu-id="9afa7-104">它可以傳遞為 Set-AzCosmosDBGremlinGraph 的參數值。</span><span class="sxs-lookup"><span data-stu-id="9afa7-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="9afa7-105">語法</span><span class="sxs-lookup"><span data-stu-id="9afa7-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9afa7-106">描述</span><span class="sxs-lookup"><span data-stu-id="9afa7-106">DESCRIPTION</span></span>
<span data-ttu-id="9afa7-107">對應至墨林 API ConflictResolutionPolicy 的物件。</span><span class="sxs-lookup"><span data-stu-id="9afa7-107">Object corresponding to Gremlin API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="9afa7-108">例子</span><span class="sxs-lookup"><span data-stu-id="9afa7-108">EXAMPLES</span></span>

### <span data-ttu-id="9afa7-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="9afa7-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

## <span data-ttu-id="9afa7-110">參數</span><span class="sxs-lookup"><span data-stu-id="9afa7-110">PARAMETERS</span></span>

### <span data-ttu-id="9afa7-111">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="9afa7-111">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="9afa7-112">在自訂類型時提供。</span><span class="sxs-lookup"><span data-stu-id="9afa7-112">To be provided when the type is custom.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9afa7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9afa7-113">-DefaultProfile</span></span>
<span data-ttu-id="9afa7-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9afa7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9afa7-115">-路徑</span><span class="sxs-lookup"><span data-stu-id="9afa7-115">-Path</span></span>
<span data-ttu-id="9afa7-116">當類型為 LastWriterWins 時提供。</span><span class="sxs-lookup"><span data-stu-id="9afa7-116">To be provided when the type is LastWriterWins.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9afa7-117">-類型</span><span class="sxs-lookup"><span data-stu-id="9afa7-117">-Type</span></span>
<span data-ttu-id="9afa7-118">可以有值：LastWriterWins，自訂，手動。</span><span class="sxs-lookup"><span data-stu-id="9afa7-118">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="9afa7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9afa7-119">CommonParameters</span></span>
<span data-ttu-id="9afa7-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9afa7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9afa7-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9afa7-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9afa7-122">輸入</span><span class="sxs-lookup"><span data-stu-id="9afa7-122">INPUTS</span></span>

### <span data-ttu-id="9afa7-123">沒有</span><span class="sxs-lookup"><span data-stu-id="9afa7-123">None</span></span>

## <span data-ttu-id="9afa7-124">輸出</span><span class="sxs-lookup"><span data-stu-id="9afa7-124">OUTPUTS</span></span>

### <span data-ttu-id="9afa7-125">Microsoft.Azure.Commands.AzsDB.Models.PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="9afa7-125">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

## <span data-ttu-id="9afa7-126">筆記</span><span class="sxs-lookup"><span data-stu-id="9afa7-126">NOTES</span></span>

## <span data-ttu-id="9afa7-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="9afa7-127">RELATED LINKS</span></span>
