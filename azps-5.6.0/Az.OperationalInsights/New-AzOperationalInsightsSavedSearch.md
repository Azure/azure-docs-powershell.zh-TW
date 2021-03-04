---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: cba56fd21263d4accba296cd7aab181f18b09200
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911597"
---
# <span data-ttu-id="c389b-101">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="c389b-101">New-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="c389b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c389b-102">SYNOPSIS</span></span>
<span data-ttu-id="c389b-103">使用指定的參數建立新的已儲存搜尋。</span><span class="sxs-lookup"><span data-stu-id="c389b-103">Creates a new saved search with the specified parameters.</span></span>

## <span data-ttu-id="c389b-104">語法</span><span class="sxs-lookup"><span data-stu-id="c389b-104">SYNTAX</span></span>

```
New-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-FunctionAlias] <String>] [[-FunctionParameter] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c389b-105">描述</span><span class="sxs-lookup"><span data-stu-id="c389b-105">DESCRIPTION</span></span>
<span data-ttu-id="c389b-106">**New-AzOperationalInsightsSavedSearch** Cmdlet 會使用工作區的指定參數，建立新的已儲存搜尋。</span><span class="sxs-lookup"><span data-stu-id="c389b-106">The **New-AzOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="c389b-107">例子</span><span class="sxs-lookup"><span data-stu-id="c389b-107">EXAMPLES</span></span>

### <span data-ttu-id="c389b-108">範例 1：建立新儲存的搜尋</span><span class="sxs-lookup"><span data-stu-id="c389b-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="c389b-109">此命令會建立一個新的已儲存搜尋。</span><span class="sxs-lookup"><span data-stu-id="c389b-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="c389b-110">參數</span><span class="sxs-lookup"><span data-stu-id="c389b-110">PARAMETERS</span></span>

### <span data-ttu-id="c389b-111">-類別</span><span class="sxs-lookup"><span data-stu-id="c389b-111">-Category</span></span>
<span data-ttu-id="c389b-112">指定類別名稱。</span><span class="sxs-lookup"><span data-stu-id="c389b-112">Specifies the category name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c389b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c389b-113">-DefaultProfile</span></span>
<span data-ttu-id="c389b-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="c389b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c389b-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c389b-115">-DisplayName</span></span>
<span data-ttu-id="c389b-116">指定儲存的搜尋顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="c389b-116">Specifies the saved search display name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c389b-117">-強制</span><span class="sxs-lookup"><span data-stu-id="c389b-117">-Force</span></span>
<span data-ttu-id="c389b-118">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="c389b-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c389b-119">-FunctionAlias</span><span class="sxs-lookup"><span data-stu-id="c389b-119">-FunctionAlias</span></span>
<span data-ttu-id="c389b-120">如果查詢做為函數，則函數別名。</span><span class="sxs-lookup"><span data-stu-id="c389b-120">The function alias if query serves as a function.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c389b-121">-FunctionParameter</span><span class="sxs-lookup"><span data-stu-id="c389b-121">-FunctionParameter</span></span>
<span data-ttu-id="c389b-122">如果查詢做為函數，則選擇性函數參數。</span><span class="sxs-lookup"><span data-stu-id="c389b-122">The optional function parameters if query serves as a function.</span></span> <span data-ttu-id="c389b-123">值應採用下列格式：'param-name1：type1 = default_value1，param-name2：type2 = default_value2'。</span><span class="sxs-lookup"><span data-stu-id="c389b-123">Value should be in the following format: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span></span> <span data-ttu-id="c389b-124">如需更多範例和適當的語法，請參閱 https://docs.microsoft.com/azure/kusto/query/functions/user-defined-functions 。</span><span class="sxs-lookup"><span data-stu-id="c389b-124">For more examples and proper syntax please refer to https://docs.microsoft.com/azure/kusto/query/functions/user-defined-functions.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FunctionParameters

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c389b-125">-查詢</span><span class="sxs-lookup"><span data-stu-id="c389b-125">-Query</span></span>
<span data-ttu-id="c389b-126">指定已儲存搜尋的查詢運算式。</span><span class="sxs-lookup"><span data-stu-id="c389b-126">Specifies the query expression for the saved search.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c389b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c389b-127">-ResourceGroupName</span></span>
<span data-ttu-id="c389b-128">指定資源組名。</span><span class="sxs-lookup"><span data-stu-id="c389b-128">Specifies the resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c389b-129">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="c389b-129">-SavedSearchId</span></span>
<span data-ttu-id="c389b-130">指定儲存的搜尋識別碼。</span><span class="sxs-lookup"><span data-stu-id="c389b-130">Specifies the saved search ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c389b-131">-標記</span><span class="sxs-lookup"><span data-stu-id="c389b-131">-Tag</span></span>
<span data-ttu-id="c389b-132">儲存的搜尋標記。</span><span class="sxs-lookup"><span data-stu-id="c389b-132">The saved search tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c389b-133">-版本</span><span class="sxs-lookup"><span data-stu-id="c389b-133">-Version</span></span>
<span data-ttu-id="c389b-134">指定版本。</span><span class="sxs-lookup"><span data-stu-id="c389b-134">Specifies the version.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: 1
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c389b-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c389b-135">-WorkspaceName</span></span>
<span data-ttu-id="c389b-136">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="c389b-136">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c389b-137">-確認</span><span class="sxs-lookup"><span data-stu-id="c389b-137">-Confirm</span></span>
<span data-ttu-id="c389b-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c389b-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c389b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c389b-139">-WhatIf</span></span>
<span data-ttu-id="c389b-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c389b-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c389b-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c389b-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c389b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c389b-142">CommonParameters</span></span>
<span data-ttu-id="c389b-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c389b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c389b-144">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c389b-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c389b-145">輸入</span><span class="sxs-lookup"><span data-stu-id="c389b-145">INPUTS</span></span>

### <span data-ttu-id="c389b-146">System.String</span><span class="sxs-lookup"><span data-stu-id="c389b-146">System.String</span></span>

### <span data-ttu-id="c389b-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c389b-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c389b-148">System.Int64</span><span class="sxs-lookup"><span data-stu-id="c389b-148">System.Int64</span></span>

## <span data-ttu-id="c389b-149">輸出</span><span class="sxs-lookup"><span data-stu-id="c389b-149">OUTPUTS</span></span>

### <span data-ttu-id="c389b-150">System.Net.HTTPStatusCode</span><span class="sxs-lookup"><span data-stu-id="c389b-150">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="c389b-151">筆記</span><span class="sxs-lookup"><span data-stu-id="c389b-151">NOTES</span></span>

## <span data-ttu-id="c389b-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="c389b-152">RELATED LINKS</span></span>

[<span data-ttu-id="c389b-153">Azure 營運深入資訊 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c389b-153">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


