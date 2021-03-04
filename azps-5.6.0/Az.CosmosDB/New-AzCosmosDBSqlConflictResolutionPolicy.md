---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqlconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
ms.openlocfilehash: e5742cde3a39cb2bf7dc96b952b3129d353235f0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910253"
---
# <span data-ttu-id="05e5e-101">New-AzCosmosDBSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="05e5e-101">New-AzCosmosDBSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="05e5e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="05e5e-102">SYNOPSIS</span></span>
<span data-ttu-id="05e5e-103">建立 PSSqlConflictResolutionPolicy 類型的新物件。</span><span class="sxs-lookup"><span data-stu-id="05e5e-103">Creates a new object of type PSSqlConflictResolutionPolicy.</span></span> <span data-ttu-id="05e5e-104">它可以傳遞為 Set-AzCosmosDBSqlContainer 的參數值。</span><span class="sxs-lookup"><span data-stu-id="05e5e-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="05e5e-105">語法</span><span class="sxs-lookup"><span data-stu-id="05e5e-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05e5e-106">描述</span><span class="sxs-lookup"><span data-stu-id="05e5e-106">DESCRIPTION</span></span>
<span data-ttu-id="05e5e-107">對應至 Sql API ConflictResolutionPolicy 的物件。</span><span class="sxs-lookup"><span data-stu-id="05e5e-107">Object corresponding to Sql API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="05e5e-108">例子</span><span class="sxs-lookup"><span data-stu-id="05e5e-108">EXAMPLES</span></span>

### <span data-ttu-id="05e5e-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="05e5e-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

<span data-ttu-id="05e5e-110">{{ 在這裡新增範例描述 }}</span><span class="sxs-lookup"><span data-stu-id="05e5e-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="05e5e-111">參數</span><span class="sxs-lookup"><span data-stu-id="05e5e-111">PARAMETERS</span></span>

### <span data-ttu-id="05e5e-112">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="05e5e-112">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="05e5e-113">在自訂類型時提供。</span><span class="sxs-lookup"><span data-stu-id="05e5e-113">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="05e5e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05e5e-114">-DefaultProfile</span></span>
<span data-ttu-id="05e5e-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="05e5e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05e5e-116">-路徑</span><span class="sxs-lookup"><span data-stu-id="05e5e-116">-Path</span></span>
<span data-ttu-id="05e5e-117">當類型為 LastWriterWins 時提供。</span><span class="sxs-lookup"><span data-stu-id="05e5e-117">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="05e5e-118">-類型</span><span class="sxs-lookup"><span data-stu-id="05e5e-118">-Type</span></span>
<span data-ttu-id="05e5e-119">可以有值：LastWriterWins，自訂，手動。</span><span class="sxs-lookup"><span data-stu-id="05e5e-119">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="05e5e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05e5e-120">CommonParameters</span></span>
<span data-ttu-id="05e5e-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="05e5e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05e5e-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="05e5e-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05e5e-123">輸入</span><span class="sxs-lookup"><span data-stu-id="05e5e-123">INPUTS</span></span>

### <span data-ttu-id="05e5e-124">沒有</span><span class="sxs-lookup"><span data-stu-id="05e5e-124">None</span></span>

## <span data-ttu-id="05e5e-125">輸出</span><span class="sxs-lookup"><span data-stu-id="05e5e-125">OUTPUTS</span></span>

### <span data-ttu-id="05e5e-126">Microsoft.Azure.Commands.AzsDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="05e5e-126">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="05e5e-127">筆記</span><span class="sxs-lookup"><span data-stu-id="05e5e-127">NOTES</span></span>

## <span data-ttu-id="05e5e-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="05e5e-128">RELATED LINKS</span></span>
