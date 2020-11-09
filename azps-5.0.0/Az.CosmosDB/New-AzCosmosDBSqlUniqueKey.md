---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
ms.openlocfilehash: e3c96cfd4051a186e0584d810088bc06a57ad862
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285476"
---
# <span data-ttu-id="afd8a-101">New-AzCosmosDBSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="afd8a-101">New-AzCosmosDBSqlUniqueKey</span></span>

## <span data-ttu-id="afd8a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="afd8a-102">SYNOPSIS</span></span>
<span data-ttu-id="afd8a-103">建立新的 CosmosDB Sql UniqueKey 物件。</span><span class="sxs-lookup"><span data-stu-id="afd8a-103">Creates a new CosmosDB Sql UniqueKey object.</span></span>

## <span data-ttu-id="afd8a-104">句法</span><span class="sxs-lookup"><span data-stu-id="afd8a-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="afd8a-105">說明</span><span class="sxs-lookup"><span data-stu-id="afd8a-105">DESCRIPTION</span></span>
<span data-ttu-id="afd8a-106">**新的-AzCosmosDBSqlUniqueKey** Cmdlet 會建立 PSUniqueKey 類型的新物件。</span><span class="sxs-lookup"><span data-stu-id="afd8a-106">The **New-AzCosmosDBSqlUniqueKey** cmdlet creates a new object of type PSUniqueKey.</span></span>

## <span data-ttu-id="afd8a-107">示例</span><span class="sxs-lookup"><span data-stu-id="afd8a-107">EXAMPLES</span></span>

### <span data-ttu-id="afd8a-108">範例1</span><span class="sxs-lookup"><span data-stu-id="afd8a-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlUniqueKey -Path {path}

Path
----
{path}
```

## <span data-ttu-id="afd8a-109">參數</span><span class="sxs-lookup"><span data-stu-id="afd8a-109">PARAMETERS</span></span>

### <span data-ttu-id="afd8a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afd8a-110">-DefaultProfile</span></span>
<span data-ttu-id="afd8a-111">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="afd8a-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afd8a-112">-Path</span><span class="sxs-lookup"><span data-stu-id="afd8a-112">-Path</span></span>
<span data-ttu-id="afd8a-113">路徑值字串的陣列</span><span class="sxs-lookup"><span data-stu-id="afd8a-113">Array of string of path values</span></span>

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

### <span data-ttu-id="afd8a-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afd8a-114">CommonParameters</span></span>
<span data-ttu-id="afd8a-115">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="afd8a-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afd8a-116">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="afd8a-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afd8a-117">輸入</span><span class="sxs-lookup"><span data-stu-id="afd8a-117">INPUTS</span></span>

### <span data-ttu-id="afd8a-118">所有</span><span class="sxs-lookup"><span data-stu-id="afd8a-118">None</span></span>

## <span data-ttu-id="afd8a-119">輸出</span><span class="sxs-lookup"><span data-stu-id="afd8a-119">OUTPUTS</span></span>

### <span data-ttu-id="afd8a-120">PSSqlUniqueKey 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="afd8a-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey</span></span>

## <span data-ttu-id="afd8a-121">筆記</span><span class="sxs-lookup"><span data-stu-id="afd8a-121">NOTES</span></span>

## <span data-ttu-id="afd8a-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="afd8a-122">RELATED LINKS</span></span>
