---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
ms.openlocfilehash: b11142be65935522a73d3a068be0ee329994e2ee
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959584"
---
# <span data-ttu-id="2ef5a-101">New-AzCosmosDBSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="2ef5a-101">New-AzCosmosDBSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="2ef5a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2ef5a-102">SYNOPSIS</span></span>
<span data-ttu-id="2ef5a-103">建立 PSSqlConflictResolutionPolicy 類型的新物件。</span><span class="sxs-lookup"><span data-stu-id="2ef5a-103">Creates a new object of type PSSqlConflictResolutionPolicy.</span></span> <span data-ttu-id="2ef5a-104">您可以將它作為 AzCosmosDBSqlContainer 的參數值來傳遞。</span><span class="sxs-lookup"><span data-stu-id="2ef5a-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="2ef5a-105">句法</span><span class="sxs-lookup"><span data-stu-id="2ef5a-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ef5a-106">說明</span><span class="sxs-lookup"><span data-stu-id="2ef5a-106">DESCRIPTION</span></span>
<span data-ttu-id="2ef5a-107">與 Sql API 的 ConflictResolutionPolicy 相對應的物件。</span><span class="sxs-lookup"><span data-stu-id="2ef5a-107">Object corresponding to Sql API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="2ef5a-108">示例</span><span class="sxs-lookup"><span data-stu-id="2ef5a-108">EXAMPLES</span></span>

### <span data-ttu-id="2ef5a-109">範例1</span><span class="sxs-lookup"><span data-stu-id="2ef5a-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

<span data-ttu-id="2ef5a-110">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="2ef5a-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="2ef5a-111">參數</span><span class="sxs-lookup"><span data-stu-id="2ef5a-111">PARAMETERS</span></span>

### <span data-ttu-id="2ef5a-112">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="2ef5a-112">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="2ef5a-113">要在類型為 [自訂] 時提供。</span><span class="sxs-lookup"><span data-stu-id="2ef5a-113">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="2ef5a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ef5a-114">-DefaultProfile</span></span>
<span data-ttu-id="2ef5a-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2ef5a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ef5a-116">-Path</span><span class="sxs-lookup"><span data-stu-id="2ef5a-116">-Path</span></span>
<span data-ttu-id="2ef5a-117">在 LastWriterWins 類型時提供。</span><span class="sxs-lookup"><span data-stu-id="2ef5a-117">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="2ef5a-118">-類型</span><span class="sxs-lookup"><span data-stu-id="2ef5a-118">-Type</span></span>
<span data-ttu-id="2ef5a-119">可以具有下列值： LastWriterWins、Custom、Manual。</span><span class="sxs-lookup"><span data-stu-id="2ef5a-119">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="2ef5a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ef5a-120">CommonParameters</span></span>
<span data-ttu-id="2ef5a-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2ef5a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ef5a-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2ef5a-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ef5a-123">輸入</span><span class="sxs-lookup"><span data-stu-id="2ef5a-123">INPUTS</span></span>

### <span data-ttu-id="2ef5a-124">所有</span><span class="sxs-lookup"><span data-stu-id="2ef5a-124">None</span></span>

## <span data-ttu-id="2ef5a-125">輸出</span><span class="sxs-lookup"><span data-stu-id="2ef5a-125">OUTPUTS</span></span>

### <span data-ttu-id="2ef5a-126">PSSqlConflictResolutionPolicy 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="2ef5a-126">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="2ef5a-127">筆記</span><span class="sxs-lookup"><span data-stu-id="2ef5a-127">NOTES</span></span>

## <span data-ttu-id="2ef5a-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="2ef5a-128">RELATED LINKS</span></span>
