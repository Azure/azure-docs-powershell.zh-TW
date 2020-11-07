---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
ms.openlocfilehash: bf91d1948b4040a35ee77f2a1111861a03076783
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959573"
---
# <span data-ttu-id="d514a-101">New-AzCosmosDBSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="d514a-101">New-AzCosmosDBSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="d514a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d514a-102">SYNOPSIS</span></span>
<span data-ttu-id="d514a-103">建立新的 CosmosDB SqlUniqueKeyPolicy 物件。</span><span class="sxs-lookup"><span data-stu-id="d514a-103">Creates a new CosmosDB SqlUniqueKeyPolicy object.</span></span>

## <span data-ttu-id="d514a-104">句法</span><span class="sxs-lookup"><span data-stu-id="d514a-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d514a-105">說明</span><span class="sxs-lookup"><span data-stu-id="d514a-105">DESCRIPTION</span></span>
<span data-ttu-id="d514a-106">**新的-AzCosmosDBSqlUniqueKeyPolicy** Cmdlet 會建立 PSSqlUniqueKeyPolicy 類型的新物件。</span><span class="sxs-lookup"><span data-stu-id="d514a-106">The **New-AzCosmosDBSqlUniqueKeyPolicy** cmdlet creates a new object of type PSSqlUniqueKeyPolicy.</span></span>

## <span data-ttu-id="d514a-107">示例</span><span class="sxs-lookup"><span data-stu-id="d514a-107">EXAMPLES</span></span>

### <span data-ttu-id="d514a-108">範例1</span><span class="sxs-lookup"><span data-stu-id="d514a-108">Example 1</span></span>
```powershell
PS C:\>New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey {psUniqueKey1, psUniqueKey2}

UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="d514a-109">參數</span><span class="sxs-lookup"><span data-stu-id="d514a-109">PARAMETERS</span></span>

### <span data-ttu-id="d514a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d514a-110">-DefaultProfile</span></span>
<span data-ttu-id="d514a-111">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d514a-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d514a-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="d514a-112">-UniqueKey</span></span>
<span data-ttu-id="d514a-113">資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="d514a-113">Database name.</span></span>

```yaml
Type: PSSqlUniqueKey[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d514a-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d514a-114">CommonParameters</span></span>
<span data-ttu-id="d514a-115">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d514a-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d514a-116">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d514a-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d514a-117">輸入</span><span class="sxs-lookup"><span data-stu-id="d514a-117">INPUTS</span></span>

### <span data-ttu-id="d514a-118">所有</span><span class="sxs-lookup"><span data-stu-id="d514a-118">None</span></span>

## <span data-ttu-id="d514a-119">輸出</span><span class="sxs-lookup"><span data-stu-id="d514a-119">OUTPUTS</span></span>

### <span data-ttu-id="d514a-120">PSSqlUniqueKeyPolicy 中的 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="d514a-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="d514a-121">筆記</span><span class="sxs-lookup"><span data-stu-id="d514a-121">NOTES</span></span>

## <span data-ttu-id="d514a-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="d514a-122">RELATED LINKS</span></span>
