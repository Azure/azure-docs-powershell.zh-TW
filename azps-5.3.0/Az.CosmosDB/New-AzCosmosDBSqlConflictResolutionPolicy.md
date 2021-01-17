---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
ms.openlocfilehash: b11142be65935522a73d3a068be0ee329994e2ee
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449558"
---
# <span data-ttu-id="84e32-101">New-AzCosmosDBSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="84e32-101">New-AzCosmosDBSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="84e32-102">摘要</span><span class="sxs-lookup"><span data-stu-id="84e32-102">SYNOPSIS</span></span>
<span data-ttu-id="84e32-103">建立 PSSqlConflictResolutionPolicy 類型的新物件。</span><span class="sxs-lookup"><span data-stu-id="84e32-103">Creates a new object of type PSSqlConflictResolutionPolicy.</span></span> <span data-ttu-id="84e32-104">您可以將它作為 AzCosmosDBSqlContainer 的參數值來傳遞。</span><span class="sxs-lookup"><span data-stu-id="84e32-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="84e32-105">句法</span><span class="sxs-lookup"><span data-stu-id="84e32-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84e32-106">說明</span><span class="sxs-lookup"><span data-stu-id="84e32-106">DESCRIPTION</span></span>
<span data-ttu-id="84e32-107">與 Sql API 的 ConflictResolutionPolicy 相對應的物件。</span><span class="sxs-lookup"><span data-stu-id="84e32-107">Object corresponding to Sql API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="84e32-108">示例</span><span class="sxs-lookup"><span data-stu-id="84e32-108">EXAMPLES</span></span>

### <span data-ttu-id="84e32-109">範例1</span><span class="sxs-lookup"><span data-stu-id="84e32-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

<span data-ttu-id="84e32-110">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="84e32-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="84e32-111">參數</span><span class="sxs-lookup"><span data-stu-id="84e32-111">PARAMETERS</span></span>

### <span data-ttu-id="84e32-112">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="84e32-112">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="84e32-113">要在類型為 [自訂] 時提供。</span><span class="sxs-lookup"><span data-stu-id="84e32-113">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="84e32-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84e32-114">-DefaultProfile</span></span>
<span data-ttu-id="84e32-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="84e32-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84e32-116">-Path</span><span class="sxs-lookup"><span data-stu-id="84e32-116">-Path</span></span>
<span data-ttu-id="84e32-117">在 LastWriterWins 類型時提供。</span><span class="sxs-lookup"><span data-stu-id="84e32-117">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="84e32-118">-類型</span><span class="sxs-lookup"><span data-stu-id="84e32-118">-Type</span></span>
<span data-ttu-id="84e32-119">可以具有下列值： LastWriterWins、Custom、Manual。</span><span class="sxs-lookup"><span data-stu-id="84e32-119">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="84e32-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84e32-120">CommonParameters</span></span>
<span data-ttu-id="84e32-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="84e32-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84e32-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="84e32-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84e32-123">輸入</span><span class="sxs-lookup"><span data-stu-id="84e32-123">INPUTS</span></span>

### <span data-ttu-id="84e32-124">所有</span><span class="sxs-lookup"><span data-stu-id="84e32-124">None</span></span>

## <span data-ttu-id="84e32-125">輸出</span><span class="sxs-lookup"><span data-stu-id="84e32-125">OUTPUTS</span></span>

### <span data-ttu-id="84e32-126">PSSqlConflictResolutionPolicy 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="84e32-126">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="84e32-127">筆記</span><span class="sxs-lookup"><span data-stu-id="84e32-127">NOTES</span></span>

## <span data-ttu-id="84e32-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="84e32-128">RELATED LINKS</span></span>
