---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/set-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 25d973d6a568695fbca7371b229cf9bb18fcd5cd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911542"
---
# <span data-ttu-id="3fe7c-101">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="3fe7c-101">Set-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="3fe7c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3fe7c-102">SYNOPSIS</span></span>
<span data-ttu-id="3fe7c-103">更新已儲存的搜尋。</span><span class="sxs-lookup"><span data-stu-id="3fe7c-103">Updates a saved search that already exists.</span></span>

## <span data-ttu-id="3fe7c-104">語法</span><span class="sxs-lookup"><span data-stu-id="3fe7c-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [[-FunctionAlias] <String>] [[-FunctionParameter] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3fe7c-105">描述</span><span class="sxs-lookup"><span data-stu-id="3fe7c-105">DESCRIPTION</span></span>
<span data-ttu-id="3fe7c-106">**Set-AzOperationalInsightsSavedSearch** Cmdlet 會更新已儲存的搜尋。</span><span class="sxs-lookup"><span data-stu-id="3fe7c-106">The **Set-AzOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="3fe7c-107">例子</span><span class="sxs-lookup"><span data-stu-id="3fe7c-107">EXAMPLES</span></span>

### <span data-ttu-id="3fe7c-108">範例 1：設定已更新屬性的已儲存搜尋</span><span class="sxs-lookup"><span data-stu-id="3fe7c-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="3fe7c-109">此命令會設定已儲存的搜尋與更新的屬性。</span><span class="sxs-lookup"><span data-stu-id="3fe7c-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="3fe7c-110">參數</span><span class="sxs-lookup"><span data-stu-id="3fe7c-110">PARAMETERS</span></span>

### <span data-ttu-id="3fe7c-111">-類別</span><span class="sxs-lookup"><span data-stu-id="3fe7c-111">-Category</span></span>
<span data-ttu-id="3fe7c-112">指定類別名稱。</span><span class="sxs-lookup"><span data-stu-id="3fe7c-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="3fe7c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fe7c-113">-DefaultProfile</span></span>
<span data-ttu-id="3fe7c-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="3fe7c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3fe7c-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3fe7c-115">-DisplayName</span></span>
<span data-ttu-id="3fe7c-116">指定顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="3fe7c-116">Specifies the display name.</span></span>

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

### <span data-ttu-id="3fe7c-117">-ETag</span><span class="sxs-lookup"><span data-stu-id="3fe7c-117">-ETag</span></span>
<span data-ttu-id="3fe7c-118">指定 ETag 名稱。</span><span class="sxs-lookup"><span data-stu-id="3fe7c-118">Specifies the ETag name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fe7c-119">-FunctionAlias</span><span class="sxs-lookup"><span data-stu-id="3fe7c-119">-FunctionAlias</span></span>
<span data-ttu-id="3fe7c-120">如果查詢做為函數，則函數別名。</span><span class="sxs-lookup"><span data-stu-id="3fe7c-120">The function alias if query serves as a function.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fe7c-121">-FunctionParameter</span><span class="sxs-lookup"><span data-stu-id="3fe7c-121">-FunctionParameter</span></span>
<span data-ttu-id="3fe7c-122">如果查詢做為函數，則選擇性函數參數。</span><span class="sxs-lookup"><span data-stu-id="3fe7c-122">The optional function parameters if query serves as a function.</span></span> <span data-ttu-id="3fe7c-123">值應採用下列格式：'param-name1：type1 = default_value1，param-name2：type2 = default_value2'。</span><span class="sxs-lookup"><span data-stu-id="3fe7c-123">Value should be in the following format: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span></span> <span data-ttu-id="3fe7c-124">如需更多範例和適當的語法，請參閱 https://docs.microsoft.com/azure/kusto/query/functions/user-defined-functions 。</span><span class="sxs-lookup"><span data-stu-id="3fe7c-124">For more examples and proper syntax please refer to https://docs.microsoft.com/azure/kusto/query/functions/user-defined-functions.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FunctionParameters

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fe7c-125">-查詢</span><span class="sxs-lookup"><span data-stu-id="3fe7c-125">-Query</span></span>
<span data-ttu-id="3fe7c-126">指定查詢名稱。</span><span class="sxs-lookup"><span data-stu-id="3fe7c-126">Specifies the query name.</span></span>

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

### <span data-ttu-id="3fe7c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fe7c-127">-ResourceGroupName</span></span>
<span data-ttu-id="3fe7c-128">指定資源組名。</span><span class="sxs-lookup"><span data-stu-id="3fe7c-128">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="3fe7c-129">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="3fe7c-129">-SavedSearchId</span></span>
<span data-ttu-id="3fe7c-130">指定儲存的搜尋識別碼。</span><span class="sxs-lookup"><span data-stu-id="3fe7c-130">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="3fe7c-131">-標記</span><span class="sxs-lookup"><span data-stu-id="3fe7c-131">-Tag</span></span>
<span data-ttu-id="3fe7c-132">儲存的搜尋標記。</span><span class="sxs-lookup"><span data-stu-id="3fe7c-132">The saved search tags.</span></span>

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

### <span data-ttu-id="3fe7c-133">-版本</span><span class="sxs-lookup"><span data-stu-id="3fe7c-133">-Version</span></span>
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

### <span data-ttu-id="3fe7c-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3fe7c-134">-WorkspaceName</span></span>
<span data-ttu-id="3fe7c-135">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="3fe7c-135">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="3fe7c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fe7c-136">CommonParameters</span></span>
<span data-ttu-id="3fe7c-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3fe7c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fe7c-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3fe7c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fe7c-139">輸入</span><span class="sxs-lookup"><span data-stu-id="3fe7c-139">INPUTS</span></span>

### <span data-ttu-id="3fe7c-140">System.String</span><span class="sxs-lookup"><span data-stu-id="3fe7c-140">System.String</span></span>

### <span data-ttu-id="3fe7c-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="3fe7c-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="3fe7c-142">System.Int64</span><span class="sxs-lookup"><span data-stu-id="3fe7c-142">System.Int64</span></span>

## <span data-ttu-id="3fe7c-143">輸出</span><span class="sxs-lookup"><span data-stu-id="3fe7c-143">OUTPUTS</span></span>

### <span data-ttu-id="3fe7c-144">System.Net.HTTPStatusCode</span><span class="sxs-lookup"><span data-stu-id="3fe7c-144">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="3fe7c-145">筆記</span><span class="sxs-lookup"><span data-stu-id="3fe7c-145">NOTES</span></span>

## <span data-ttu-id="3fe7c-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="3fe7c-146">RELATED LINKS</span></span>

[<span data-ttu-id="3fe7c-147">Azure 營運深入資訊 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3fe7c-147">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


