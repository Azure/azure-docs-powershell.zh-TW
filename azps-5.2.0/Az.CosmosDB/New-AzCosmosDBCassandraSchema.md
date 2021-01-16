---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
ms.openlocfilehash: 997f9e0751eb616fdc9e64f73d66b3f15b7ed756
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98283859"
---
# <span data-ttu-id="9cad4-101">New-AzCosmosDBCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="9cad4-101">New-AzCosmosDBCassandraSchema</span></span>

## <span data-ttu-id="9cad4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9cad4-102">SYNOPSIS</span></span>
<span data-ttu-id="9cad4-103">建立新的 CosmosDB Cassandra 架構。</span><span class="sxs-lookup"><span data-stu-id="9cad4-103">Creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="9cad4-104">句法</span><span class="sxs-lookup"><span data-stu-id="9cad4-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraSchema [-Column <PSColumn[]>] [-PartitionKey <String[]>] [-ClusterKey <PSClusterKey[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9cad4-105">說明</span><span class="sxs-lookup"><span data-stu-id="9cad4-105">DESCRIPTION</span></span>
<span data-ttu-id="9cad4-106">**新的-AzCosmosDBCassandraSchema** 會建立新的 CosmosDB Cassandra 架構。</span><span class="sxs-lookup"><span data-stu-id="9cad4-106">The **New-AzCosmosDBCassandraSchema** creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="9cad4-107">示例</span><span class="sxs-lookup"><span data-stu-id="9cad4-107">EXAMPLES</span></span>

### <span data-ttu-id="9cad4-108">範例1</span><span class="sxs-lookup"><span data-stu-id="9cad4-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraSchema -Column {PSColumn[]} -PartitionKey <String[]> -ClusterKey {PSClusterKey[]}

Columns PartitionKeys ClusterKeys
------- ------------- -----------
{column1}     {a}     {clusterkey1}
```

## <span data-ttu-id="9cad4-109">參數</span><span class="sxs-lookup"><span data-stu-id="9cad4-109">PARAMETERS</span></span>

### <span data-ttu-id="9cad4-110">-ClusterKey</span><span class="sxs-lookup"><span data-stu-id="9cad4-110">-ClusterKey</span></span>
<span data-ttu-id="9cad4-111">PSClusterKey 物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="9cad4-111">Array of PSClusterKey objects.</span></span>

```yaml
Type: PSClusterKey[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cad4-112">-欄</span><span class="sxs-lookup"><span data-stu-id="9cad4-112">-Column</span></span>
<span data-ttu-id="9cad4-113">PSColumn 物件。</span><span class="sxs-lookup"><span data-stu-id="9cad4-113">PSColumn object.</span></span>

```yaml
Type: PSColumn[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cad4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cad4-114">-DefaultProfile</span></span>
<span data-ttu-id="9cad4-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9cad4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cad4-116">-PartitionKey</span><span class="sxs-lookup"><span data-stu-id="9cad4-116">-PartitionKey</span></span>
<span data-ttu-id="9cad4-117">包含分區鍵的字串陣列。</span><span class="sxs-lookup"><span data-stu-id="9cad4-117">Array of strings containing Partition Keys.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cad4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cad4-118">CommonParameters</span></span>
<span data-ttu-id="9cad4-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9cad4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cad4-120">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9cad4-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cad4-121">輸入</span><span class="sxs-lookup"><span data-stu-id="9cad4-121">INPUTS</span></span>

### <span data-ttu-id="9cad4-122">所有</span><span class="sxs-lookup"><span data-stu-id="9cad4-122">None</span></span>

## <span data-ttu-id="9cad4-123">輸出</span><span class="sxs-lookup"><span data-stu-id="9cad4-123">OUTPUTS</span></span>

### <span data-ttu-id="9cad4-124">PSCassandraSchema 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="9cad4-124">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

## <span data-ttu-id="9cad4-125">筆記</span><span class="sxs-lookup"><span data-stu-id="9cad4-125">NOTES</span></span>

## <span data-ttu-id="9cad4-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="9cad4-126">RELATED LINKS</span></span>
