---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/remove-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
ms.openlocfilehash: 79e7ff902d75387180e519bbaf8a5cdc3e2431a1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917926"
---
# <span data-ttu-id="3f6ee-101">Remove-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="3f6ee-101">Remove-AzSearchQueryKey</span></span>

## <span data-ttu-id="3f6ee-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3f6ee-102">SYNOPSIS</span></span>
<span data-ttu-id="3f6ee-103">從 Azure 認知搜尋服務移除查詢鍵。</span><span class="sxs-lookup"><span data-stu-id="3f6ee-103">Remove the query key from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="3f6ee-104">語法</span><span class="sxs-lookup"><span data-stu-id="3f6ee-104">SYNTAX</span></span>

### <span data-ttu-id="3f6ee-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3f6ee-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyValue <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f6ee-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f6ee-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentObject] <PSSearchService> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f6ee-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f6ee-107">ParentResourceIdParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentResourceId] <String> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f6ee-108">描述</span><span class="sxs-lookup"><span data-stu-id="3f6ee-108">DESCRIPTION</span></span>
<span data-ttu-id="3f6ee-109">**Remove-AzSearchQueryKey** Cmdlet 會從 Azure 認知搜尋服務移除查詢鍵。</span><span class="sxs-lookup"><span data-stu-id="3f6ee-109">The **Remove-AzSearchQueryKey** cmdlet removes the query key from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="3f6ee-110">例子</span><span class="sxs-lookup"><span data-stu-id="3f6ee-110">EXAMPLES</span></span>

### <span data-ttu-id="3f6ee-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="3f6ee-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name         Key                             
----         ---                             
             D260F448EA192EBC19D59F7E5670E8BB
NewQueryKey1 B4C13E3F6FA76100D3488673CFDCD438

PS C:\> Remove-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -KeyValue B4C13E3F6FA76100D3488673CFDCD438

Confirm
Are you sure you want to remove query key 'B4C13E3F6FA76100D3488673CFDCD438'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="3f6ee-112">此範例會從 Azure 認知搜尋服務移除查詢鍵。</span><span class="sxs-lookup"><span data-stu-id="3f6ee-112">The example removes the query key from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="3f6ee-113">參數</span><span class="sxs-lookup"><span data-stu-id="3f6ee-113">PARAMETERS</span></span>

### <span data-ttu-id="3f6ee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f6ee-114">-DefaultProfile</span></span>
<span data-ttu-id="3f6ee-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3f6ee-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f6ee-116">-強制</span><span class="sxs-lookup"><span data-stu-id="3f6ee-116">-Force</span></span>
<span data-ttu-id="3f6ee-117">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="3f6ee-117">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f6ee-118">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="3f6ee-118">-KeyValue</span></span>
<span data-ttu-id="3f6ee-119">Azure 認知搜尋服務查詢索引鍵值。</span><span class="sxs-lookup"><span data-stu-id="3f6ee-119">Azure Cognitive Search Service query key value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f6ee-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3f6ee-120">-ParentObject</span></span>
<span data-ttu-id="3f6ee-121">Azure 認知搜尋服務輸入物件。</span><span class="sxs-lookup"><span data-stu-id="3f6ee-121">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f6ee-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="3f6ee-122">-ParentResourceId</span></span>
<span data-ttu-id="3f6ee-123">Azure 認知搜尋服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="3f6ee-123">Azure Cognitive Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f6ee-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f6ee-124">-PassThru</span></span>
<span data-ttu-id="3f6ee-125">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="3f6ee-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="3f6ee-126">如果指定此參數，則成功時會返回 True。</span><span class="sxs-lookup"><span data-stu-id="3f6ee-126">If this switch is specified, it returns true if successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f6ee-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f6ee-127">-ResourceGroupName</span></span>
<span data-ttu-id="3f6ee-128">資源組名。</span><span class="sxs-lookup"><span data-stu-id="3f6ee-128">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f6ee-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3f6ee-129">-ServiceName</span></span>
<span data-ttu-id="3f6ee-130">Azure 認知搜尋服務名稱。</span><span class="sxs-lookup"><span data-stu-id="3f6ee-130">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f6ee-131">-確認</span><span class="sxs-lookup"><span data-stu-id="3f6ee-131">-Confirm</span></span>
<span data-ttu-id="3f6ee-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3f6ee-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f6ee-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f6ee-133">-WhatIf</span></span>
<span data-ttu-id="3f6ee-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3f6ee-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f6ee-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3f6ee-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f6ee-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f6ee-136">CommonParameters</span></span>
<span data-ttu-id="3f6ee-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3f6ee-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f6ee-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3f6ee-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f6ee-139">輸入</span><span class="sxs-lookup"><span data-stu-id="3f6ee-139">INPUTS</span></span>

### <span data-ttu-id="3f6ee-140">Microsoft.Azure.Commands.management.Search.models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="3f6ee-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="3f6ee-141">System.String</span><span class="sxs-lookup"><span data-stu-id="3f6ee-141">System.String</span></span>

## <span data-ttu-id="3f6ee-142">輸出</span><span class="sxs-lookup"><span data-stu-id="3f6ee-142">OUTPUTS</span></span>

### <span data-ttu-id="3f6ee-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3f6ee-143">System.Boolean</span></span>

## <span data-ttu-id="3f6ee-144">筆記</span><span class="sxs-lookup"><span data-stu-id="3f6ee-144">NOTES</span></span>

## <span data-ttu-id="3f6ee-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="3f6ee-145">RELATED LINKS</span></span>

[<span data-ttu-id="3f6ee-146">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="3f6ee-146">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="3f6ee-147">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="3f6ee-147">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)
