---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
ms.openlocfilehash: 4662368f89f77c331619472feefe16736c40ef55
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958028"
---
# <span data-ttu-id="d13d6-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="d13d6-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span></span>

## <span data-ttu-id="d13d6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d13d6-102">SYNOPSIS</span></span>
<span data-ttu-id="d13d6-103">建立 PSConflictResolutionPolicy 類型的新物件。</span><span class="sxs-lookup"><span data-stu-id="d13d6-103">Creates a new object of type PSConflictResolutionPolicy.</span></span> <span data-ttu-id="d13d6-104">您可以將它作為 AzCosmosDBGremlinGraph 的參數值來傳遞。</span><span class="sxs-lookup"><span data-stu-id="d13d6-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="d13d6-105">句法</span><span class="sxs-lookup"><span data-stu-id="d13d6-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d13d6-106">說明</span><span class="sxs-lookup"><span data-stu-id="d13d6-106">DESCRIPTION</span></span>
<span data-ttu-id="d13d6-107">對應至 Gremlin API ConflictResolutionPolicy 的物件。</span><span class="sxs-lookup"><span data-stu-id="d13d6-107">Object corresponding to Gremlin API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="d13d6-108">示例</span><span class="sxs-lookup"><span data-stu-id="d13d6-108">EXAMPLES</span></span>

### <span data-ttu-id="d13d6-109">範例1</span><span class="sxs-lookup"><span data-stu-id="d13d6-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

## <span data-ttu-id="d13d6-110">參數</span><span class="sxs-lookup"><span data-stu-id="d13d6-110">PARAMETERS</span></span>

### <span data-ttu-id="d13d6-111">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="d13d6-111">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="d13d6-112">要在類型為 [自訂] 時提供。</span><span class="sxs-lookup"><span data-stu-id="d13d6-112">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="d13d6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d13d6-113">-DefaultProfile</span></span>
<span data-ttu-id="d13d6-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d13d6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d13d6-115">-Path</span><span class="sxs-lookup"><span data-stu-id="d13d6-115">-Path</span></span>
<span data-ttu-id="d13d6-116">在 LastWriterWins 類型時提供。</span><span class="sxs-lookup"><span data-stu-id="d13d6-116">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="d13d6-117">-類型</span><span class="sxs-lookup"><span data-stu-id="d13d6-117">-Type</span></span>
<span data-ttu-id="d13d6-118">可以具有下列值： LastWriterWins、Custom、Manual。</span><span class="sxs-lookup"><span data-stu-id="d13d6-118">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="d13d6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d13d6-119">CommonParameters</span></span>
<span data-ttu-id="d13d6-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d13d6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d13d6-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d13d6-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d13d6-122">輸入</span><span class="sxs-lookup"><span data-stu-id="d13d6-122">INPUTS</span></span>

### <span data-ttu-id="d13d6-123">所有</span><span class="sxs-lookup"><span data-stu-id="d13d6-123">None</span></span>

## <span data-ttu-id="d13d6-124">輸出</span><span class="sxs-lookup"><span data-stu-id="d13d6-124">OUTPUTS</span></span>

### <span data-ttu-id="d13d6-125">PSConflictResolutionPolicy 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="d13d6-125">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

## <span data-ttu-id="d13d6-126">筆記</span><span class="sxs-lookup"><span data-stu-id="d13d6-126">NOTES</span></span>

## <span data-ttu-id="d13d6-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="d13d6-127">RELATED LINKS</span></span>
