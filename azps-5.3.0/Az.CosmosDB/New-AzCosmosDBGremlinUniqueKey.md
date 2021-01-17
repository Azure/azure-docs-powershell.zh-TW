---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
ms.openlocfilehash: a51075274c20d0beeb9e73c26ec72f5f69fdf388
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98446072"
---
# <span data-ttu-id="71497-101">New-AzCosmosDBGremlinUniqueKey</span><span class="sxs-lookup"><span data-stu-id="71497-101">New-AzCosmosDBGremlinUniqueKey</span></span>

## <span data-ttu-id="71497-102">摘要</span><span class="sxs-lookup"><span data-stu-id="71497-102">SYNOPSIS</span></span>
<span data-ttu-id="71497-103">建立新的 CosmosDB UniqueKeyPolicy 物件。</span><span class="sxs-lookup"><span data-stu-id="71497-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="71497-104">句法</span><span class="sxs-lookup"><span data-stu-id="71497-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71497-105">說明</span><span class="sxs-lookup"><span data-stu-id="71497-105">DESCRIPTION</span></span>
<span data-ttu-id="71497-106">**新的-AzCosmosDBGremlinUniqueKeyPolicy** Cmdlet 會建立 PSUniqueKeyPolicy 類型的新物件。</span><span class="sxs-lookup"><span data-stu-id="71497-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="71497-107">示例</span><span class="sxs-lookup"><span data-stu-id="71497-107">EXAMPLES</span></span>

### <span data-ttu-id="71497-108">範例1</span><span class="sxs-lookup"><span data-stu-id="71497-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinUniqueKey -Path "abc"
UniqueKeys
----------
{Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey}
```

## <span data-ttu-id="71497-109">參數</span><span class="sxs-lookup"><span data-stu-id="71497-109">PARAMETERS</span></span>

### <span data-ttu-id="71497-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71497-110">-DefaultProfile</span></span>
<span data-ttu-id="71497-111">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="71497-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71497-112">-Path</span><span class="sxs-lookup"><span data-stu-id="71497-112">-Path</span></span>
<span data-ttu-id="71497-113">路徑值字串的陣列</span><span class="sxs-lookup"><span data-stu-id="71497-113">Array of string of path values</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71497-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71497-114">CommonParameters</span></span>
<span data-ttu-id="71497-115">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="71497-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71497-116">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="71497-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71497-117">輸入</span><span class="sxs-lookup"><span data-stu-id="71497-117">INPUTS</span></span>

### <span data-ttu-id="71497-118">所有</span><span class="sxs-lookup"><span data-stu-id="71497-118">None</span></span>

## <span data-ttu-id="71497-119">輸出</span><span class="sxs-lookup"><span data-stu-id="71497-119">OUTPUTS</span></span>

### <span data-ttu-id="71497-120">PSUniqueKey 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="71497-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey</span></span>

## <span data-ttu-id="71497-121">筆記</span><span class="sxs-lookup"><span data-stu-id="71497-121">NOTES</span></span>

## <span data-ttu-id="71497-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="71497-122">RELATED LINKS</span></span>
