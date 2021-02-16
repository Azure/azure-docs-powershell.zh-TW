---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 3426b93ec9551ba6218634fa87adeff09b5872af
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131066"
---
# <span data-ttu-id="b2e1f-101">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="b2e1f-101">New-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="b2e1f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b2e1f-102">SYNOPSIS</span></span>
<span data-ttu-id="b2e1f-103">使用指定的參數建立新的已儲存搜尋。</span><span class="sxs-lookup"><span data-stu-id="b2e1f-103">Creates a new saved search with the specified parameters.</span></span>

## <span data-ttu-id="b2e1f-104">句法</span><span class="sxs-lookup"><span data-stu-id="b2e1f-104">SYNTAX</span></span>

```
New-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-FunctionAlias] <String>] [[-FunctionParameter] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2e1f-105">說明</span><span class="sxs-lookup"><span data-stu-id="b2e1f-105">DESCRIPTION</span></span>
<span data-ttu-id="b2e1f-106">**新的-AzOperationalInsightsSavedSearch** Cmdlet 會使用指定的工作區參數來建立新的已儲存搜尋。</span><span class="sxs-lookup"><span data-stu-id="b2e1f-106">The **New-AzOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="b2e1f-107">示例</span><span class="sxs-lookup"><span data-stu-id="b2e1f-107">EXAMPLES</span></span>

### <span data-ttu-id="b2e1f-108">範例1：建立新的已儲存搜尋</span><span class="sxs-lookup"><span data-stu-id="b2e1f-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="b2e1f-109">這個命令會建立新的已儲存搜尋。</span><span class="sxs-lookup"><span data-stu-id="b2e1f-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="b2e1f-110">參數</span><span class="sxs-lookup"><span data-stu-id="b2e1f-110">PARAMETERS</span></span>

### <span data-ttu-id="b2e1f-111">-類別</span><span class="sxs-lookup"><span data-stu-id="b2e1f-111">-Category</span></span>
<span data-ttu-id="b2e1f-112">指定類別名稱。</span><span class="sxs-lookup"><span data-stu-id="b2e1f-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="b2e1f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2e1f-113">-DefaultProfile</span></span>
<span data-ttu-id="b2e1f-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b2e1f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2e1f-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b2e1f-115">-DisplayName</span></span>
<span data-ttu-id="b2e1f-116">指定已儲存的搜尋顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="b2e1f-116">Specifies the saved search display name.</span></span>

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

### <span data-ttu-id="b2e1f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b2e1f-117">-Force</span></span>
<span data-ttu-id="b2e1f-118">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="b2e1f-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b2e1f-119">-FunctionAlias</span><span class="sxs-lookup"><span data-stu-id="b2e1f-119">-FunctionAlias</span></span>
<span data-ttu-id="b2e1f-120">如果 query 充當函數，則是函數別名。</span><span class="sxs-lookup"><span data-stu-id="b2e1f-120">The function alias if query serves as a function.</span></span>

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

### <span data-ttu-id="b2e1f-121">-FunctionParameter</span><span class="sxs-lookup"><span data-stu-id="b2e1f-121">-FunctionParameter</span></span>
<span data-ttu-id="b2e1f-122">如果 query 充當函數，則是選用的函數參數。</span><span class="sxs-lookup"><span data-stu-id="b2e1f-122">The optional function parameters if query serves as a function.</span></span> <span data-ttu-id="b2e1f-123">值應採用下列格式： "param-name1： type1 = default_value1，param： type2 = default_value2"。</span><span class="sxs-lookup"><span data-stu-id="b2e1f-123">Value should be in the following format: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span></span> <span data-ttu-id="b2e1f-124">如需更多範例及正確語法，請參閱 https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions 。</span><span class="sxs-lookup"><span data-stu-id="b2e1f-124">For more examples and proper syntax please refer to https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions.</span></span>

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

### <span data-ttu-id="b2e1f-125">-Query</span><span class="sxs-lookup"><span data-stu-id="b2e1f-125">-Query</span></span>
<span data-ttu-id="b2e1f-126">指定已儲存之搜尋的查詢運算式。</span><span class="sxs-lookup"><span data-stu-id="b2e1f-126">Specifies the query expression for the saved search.</span></span>

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

### <span data-ttu-id="b2e1f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2e1f-127">-ResourceGroupName</span></span>
<span data-ttu-id="b2e1f-128">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b2e1f-128">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="b2e1f-129">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="b2e1f-129">-SavedSearchId</span></span>
<span data-ttu-id="b2e1f-130">指定已儲存的搜尋識別碼。</span><span class="sxs-lookup"><span data-stu-id="b2e1f-130">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="b2e1f-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="b2e1f-131">-Tag</span></span>
<span data-ttu-id="b2e1f-132">已儲存的搜尋標記。</span><span class="sxs-lookup"><span data-stu-id="b2e1f-132">The saved search tags.</span></span>

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

### <span data-ttu-id="b2e1f-133">-版本</span><span class="sxs-lookup"><span data-stu-id="b2e1f-133">-Version</span></span>
<span data-ttu-id="b2e1f-134">指定版本。</span><span class="sxs-lookup"><span data-stu-id="b2e1f-134">Specifies the version.</span></span>

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

### <span data-ttu-id="b2e1f-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b2e1f-135">-WorkspaceName</span></span>
<span data-ttu-id="b2e1f-136">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="b2e1f-136">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="b2e1f-137">-確認</span><span class="sxs-lookup"><span data-stu-id="b2e1f-137">-Confirm</span></span>
<span data-ttu-id="b2e1f-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b2e1f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2e1f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2e1f-139">-WhatIf</span></span>
<span data-ttu-id="b2e1f-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b2e1f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2e1f-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b2e1f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2e1f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2e1f-142">CommonParameters</span></span>
<span data-ttu-id="b2e1f-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b2e1f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2e1f-144">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b2e1f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2e1f-145">輸入</span><span class="sxs-lookup"><span data-stu-id="b2e1f-145">INPUTS</span></span>

### <span data-ttu-id="b2e1f-146">System.object</span><span class="sxs-lookup"><span data-stu-id="b2e1f-146">System.String</span></span>

### <span data-ttu-id="b2e1f-147">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b2e1f-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b2e1f-148">System.object</span><span class="sxs-lookup"><span data-stu-id="b2e1f-148">System.Int64</span></span>

## <span data-ttu-id="b2e1f-149">輸出</span><span class="sxs-lookup"><span data-stu-id="b2e1f-149">OUTPUTS</span></span>

### <span data-ttu-id="b2e1f-150">HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="b2e1f-150">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="b2e1f-151">筆記</span><span class="sxs-lookup"><span data-stu-id="b2e1f-151">NOTES</span></span>

## <span data-ttu-id="b2e1f-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="b2e1f-152">RELATED LINKS</span></span>

[<span data-ttu-id="b2e1f-153">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b2e1f-153">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


