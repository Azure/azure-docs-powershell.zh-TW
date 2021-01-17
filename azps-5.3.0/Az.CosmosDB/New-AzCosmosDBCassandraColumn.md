---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandracolumn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
ms.openlocfilehash: 31563c11a1df418d0f53c1eeb80e8bc02691188c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98446096"
---
# <span data-ttu-id="bac9f-101">New-AzCosmosDBCassandraColumn</span><span class="sxs-lookup"><span data-stu-id="bac9f-101">New-AzCosmosDBCassandraColumn</span></span>

## <span data-ttu-id="bac9f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bac9f-102">SYNOPSIS</span></span>
<span data-ttu-id="bac9f-103">建立新的 CosmosDB Cassandra 欄。</span><span class="sxs-lookup"><span data-stu-id="bac9f-103">Creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="bac9f-104">句法</span><span class="sxs-lookup"><span data-stu-id="bac9f-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraColumn -Name <String> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bac9f-105">說明</span><span class="sxs-lookup"><span data-stu-id="bac9f-105">DESCRIPTION</span></span>
<span data-ttu-id="bac9f-106">**新的-AzCosmosDBCassandraColumn** 會建立新的 CosmosDB Cassandra 資料行。</span><span class="sxs-lookup"><span data-stu-id="bac9f-106">The **New-AzCosmosDBCassandraColumn** creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="bac9f-107">示例</span><span class="sxs-lookup"><span data-stu-id="bac9f-107">EXAMPLES</span></span>

### <span data-ttu-id="bac9f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="bac9f-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraColumn -Name "name" -Type int

Name Type
---- ----
name int
```

## <span data-ttu-id="bac9f-109">參數</span><span class="sxs-lookup"><span data-stu-id="bac9f-109">PARAMETERS</span></span>

### <span data-ttu-id="bac9f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bac9f-110">-DefaultProfile</span></span>
<span data-ttu-id="bac9f-111">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bac9f-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bac9f-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="bac9f-112">-Name</span></span>
<span data-ttu-id="bac9f-113">Cassandra 資料行的名稱。</span><span class="sxs-lookup"><span data-stu-id="bac9f-113">Name of Cassandra Column.</span></span>

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

### <span data-ttu-id="bac9f-114">-類型</span><span class="sxs-lookup"><span data-stu-id="bac9f-114">-Type</span></span>
<span data-ttu-id="bac9f-115">Cassandra 資料行的類型。</span><span class="sxs-lookup"><span data-stu-id="bac9f-115">Type of Cassandra Column.</span></span>

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

### <span data-ttu-id="bac9f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bac9f-116">CommonParameters</span></span>
<span data-ttu-id="bac9f-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bac9f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bac9f-118">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bac9f-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bac9f-119">輸入</span><span class="sxs-lookup"><span data-stu-id="bac9f-119">INPUTS</span></span>

### <span data-ttu-id="bac9f-120">所有</span><span class="sxs-lookup"><span data-stu-id="bac9f-120">None</span></span>

## <span data-ttu-id="bac9f-121">輸出</span><span class="sxs-lookup"><span data-stu-id="bac9f-121">OUTPUTS</span></span>

### <span data-ttu-id="bac9f-122">PSColumn 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="bac9f-122">Microsoft.Azure.Commands.CosmosDB.Models.PSColumn</span></span>

## <span data-ttu-id="bac9f-123">筆記</span><span class="sxs-lookup"><span data-stu-id="bac9f-123">NOTES</span></span>

## <span data-ttu-id="bac9f-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="bac9f-124">RELATED LINKS</span></span>
