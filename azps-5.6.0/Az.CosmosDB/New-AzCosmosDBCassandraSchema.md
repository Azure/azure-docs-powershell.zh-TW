---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbcassandraschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
ms.openlocfilehash: 3a19e0c60b5a32e1d1083b1afba55a8bf3045fe9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909825"
---
# <span data-ttu-id="e779e-101">New-AzCosmosDBCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="e779e-101">New-AzCosmosDBCassandraSchema</span></span>

## <span data-ttu-id="e779e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e779e-102">SYNOPSIS</span></span>
<span data-ttu-id="e779e-103">建立新一個一次的花式架構。</span><span class="sxs-lookup"><span data-stu-id="e779e-103">Creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="e779e-104">語法</span><span class="sxs-lookup"><span data-stu-id="e779e-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraSchema [-Column <PSColumn[]>] [-PartitionKey <String[]>] [-ClusterKey <PSClusterKey[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e779e-105">描述</span><span class="sxs-lookup"><span data-stu-id="e779e-105">DESCRIPTION</span></span>
<span data-ttu-id="e779e-106">**New-AzCosmosDBCassandraSchema** 會建立一個新的一個以一種新為一格的一個。。</span><span class="sxs-lookup"><span data-stu-id="e779e-106">The **New-AzCosmosDBCassandraSchema** creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="e779e-107">例子</span><span class="sxs-lookup"><span data-stu-id="e779e-107">EXAMPLES</span></span>

### <span data-ttu-id="e779e-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="e779e-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraSchema -Column {PSColumn[]} -PartitionKey <String[]> -ClusterKey {PSClusterKey[]}

Columns PartitionKeys ClusterKeys
------- ------------- -----------
{column1}     {a}     {clusterkey1}
```

## <span data-ttu-id="e779e-109">參數</span><span class="sxs-lookup"><span data-stu-id="e779e-109">PARAMETERS</span></span>

### <span data-ttu-id="e779e-110">-ClusterKey</span><span class="sxs-lookup"><span data-stu-id="e779e-110">-ClusterKey</span></span>
<span data-ttu-id="e779e-111">PSClusterKey 物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="e779e-111">Array of PSClusterKey objects.</span></span>

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

### <span data-ttu-id="e779e-112">-欄</span><span class="sxs-lookup"><span data-stu-id="e779e-112">-Column</span></span>
<span data-ttu-id="e779e-113">PSColumn 物件。</span><span class="sxs-lookup"><span data-stu-id="e779e-113">PSColumn object.</span></span>

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

### <span data-ttu-id="e779e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e779e-114">-DefaultProfile</span></span>
<span data-ttu-id="e779e-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e779e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e779e-116">-PartitionKey</span><span class="sxs-lookup"><span data-stu-id="e779e-116">-PartitionKey</span></span>
<span data-ttu-id="e779e-117">包含分割鍵的字串陣列。</span><span class="sxs-lookup"><span data-stu-id="e779e-117">Array of strings containing Partition Keys.</span></span>

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

### <span data-ttu-id="e779e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e779e-118">CommonParameters</span></span>
<span data-ttu-id="e779e-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e779e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e779e-120">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e779e-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e779e-121">輸入</span><span class="sxs-lookup"><span data-stu-id="e779e-121">INPUTS</span></span>

### <span data-ttu-id="e779e-122">沒有</span><span class="sxs-lookup"><span data-stu-id="e779e-122">None</span></span>

## <span data-ttu-id="e779e-123">輸出</span><span class="sxs-lookup"><span data-stu-id="e779e-123">OUTPUTS</span></span>

### <span data-ttu-id="e779e-124">Microsoft.Azure.Commands.AzsDB.Models.PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="e779e-124">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

## <span data-ttu-id="e779e-125">筆記</span><span class="sxs-lookup"><span data-stu-id="e779e-125">NOTES</span></span>

## <span data-ttu-id="e779e-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="e779e-126">RELATED LINKS</span></span>
