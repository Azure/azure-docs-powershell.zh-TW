---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccountKey.md
ms.openlocfilehash: a9cea343a67e7e23e820c0995484aab9a1434f90
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957859"
---
# <span data-ttu-id="ea3a1-101">New-AzCosmosDBAccountKey</span><span class="sxs-lookup"><span data-stu-id="ea3a1-101">New-AzCosmosDBAccountKey</span></span>

## <span data-ttu-id="ea3a1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ea3a1-102">SYNOPSIS</span></span>
<span data-ttu-id="ea3a1-103">重新產生指定的 CosmosDB 帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="ea3a1-103">Regenerate a given CosmosDB Account Key.</span></span>

## <span data-ttu-id="ea3a1-104">句法</span><span class="sxs-lookup"><span data-stu-id="ea3a1-104">SYNTAX</span></span>

### <span data-ttu-id="ea3a1-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ea3a1-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBAccountKey -ResourceGroupName <String> -Name <String> [-KeyKind <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea3a1-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea3a1-106">ByResourceIdParameterSet</span></span>
```
New-AzCosmosDBAccountKey [-KeyKind <String>] -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea3a1-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea3a1-107">ByObjectParameterSet</span></span>
```
New-AzCosmosDBAccountKey [-KeyKind <String>] -InputObject <PSDatabaseAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea3a1-108">說明</span><span class="sxs-lookup"><span data-stu-id="ea3a1-108">DESCRIPTION</span></span>
<span data-ttu-id="ea3a1-109">在指定的 ResourceGroup 中建立新的 CosmosDB 帳戶。</span><span class="sxs-lookup"><span data-stu-id="ea3a1-109">Create a new CosmosDB Account in the given ResourceGroup.</span></span>

## <span data-ttu-id="ea3a1-110">示例</span><span class="sxs-lookup"><span data-stu-id="ea3a1-110">EXAMPLES</span></span>

### <span data-ttu-id="ea3a1-111">範例1</span><span class="sxs-lookup"><span data-stu-id="ea3a1-111">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBAccountKey -ResourceGroupName rg -Name dbname
```

<span data-ttu-id="ea3a1-112">在 ResourceGroup rg 中，會針對帳戶名稱 dbname 產生新的金鑰。</span><span class="sxs-lookup"><span data-stu-id="ea3a1-112">New keys are generated for Account with account name dbname in ResourceGroup rg.</span></span>

## <span data-ttu-id="ea3a1-113">參數</span><span class="sxs-lookup"><span data-stu-id="ea3a1-113">PARAMETERS</span></span>

### <span data-ttu-id="ea3a1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea3a1-114">-AsJob</span></span>
<span data-ttu-id="ea3a1-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ea3a1-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea3a1-116">-確認</span><span class="sxs-lookup"><span data-stu-id="ea3a1-116">-Confirm</span></span>
<span data-ttu-id="ea3a1-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ea3a1-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea3a1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea3a1-118">-DefaultProfile</span></span>
<span data-ttu-id="ea3a1-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ea3a1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea3a1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea3a1-120">-InputObject</span></span>
<span data-ttu-id="ea3a1-121">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="ea3a1-121">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea3a1-122">-KeyKind</span><span class="sxs-lookup"><span data-stu-id="ea3a1-122">-KeyKind</span></span>
<span data-ttu-id="ea3a1-123">要重新產生的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="ea3a1-123">The access key to regenerate.</span></span>
<span data-ttu-id="ea3a1-124">已接受的值： primary、primaryReadonly、副、secondaryReadonly</span><span class="sxs-lookup"><span data-stu-id="ea3a1-124">Accepted values: primary, primaryReadonly, secondary, secondaryReadonly</span></span>

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

### <span data-ttu-id="ea3a1-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="ea3a1-125">-Name</span></span>
<span data-ttu-id="ea3a1-126">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="ea3a1-126">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea3a1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea3a1-127">-ResourceGroupName</span></span>
<span data-ttu-id="ea3a1-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ea3a1-128">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea3a1-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea3a1-129">-ResourceId</span></span>
<span data-ttu-id="ea3a1-130">資源的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="ea3a1-130">ResourceId of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea3a1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea3a1-131">-WhatIf</span></span>
<span data-ttu-id="ea3a1-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ea3a1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea3a1-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ea3a1-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea3a1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea3a1-134">CommonParameters</span></span>
<span data-ttu-id="ea3a1-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ea3a1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea3a1-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ea3a1-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea3a1-137">輸入</span><span class="sxs-lookup"><span data-stu-id="ea3a1-137">INPUTS</span></span>

### <span data-ttu-id="ea3a1-138">所有</span><span class="sxs-lookup"><span data-stu-id="ea3a1-138">None</span></span>

## <span data-ttu-id="ea3a1-139">輸出</span><span class="sxs-lookup"><span data-stu-id="ea3a1-139">OUTPUTS</span></span>

### <span data-ttu-id="ea3a1-140">System.void</span><span class="sxs-lookup"><span data-stu-id="ea3a1-140">System.Void</span></span>

## <span data-ttu-id="ea3a1-141">筆記</span><span class="sxs-lookup"><span data-stu-id="ea3a1-141">NOTES</span></span>

## <span data-ttu-id="ea3a1-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="ea3a1-142">RELATED LINKS</span></span>
