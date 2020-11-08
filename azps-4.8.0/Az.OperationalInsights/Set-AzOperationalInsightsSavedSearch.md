---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 46427a53a04e94fe42c20cfa2e6ab016a6b8c613
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128887"
---
# <span data-ttu-id="cc12e-101">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="cc12e-101">Set-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="cc12e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cc12e-102">SYNOPSIS</span></span>
<span data-ttu-id="cc12e-103">更新已存在的已儲存搜尋。</span><span class="sxs-lookup"><span data-stu-id="cc12e-103">Updates a saved search that already exists.</span></span>

## <span data-ttu-id="cc12e-104">句法</span><span class="sxs-lookup"><span data-stu-id="cc12e-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [[-FunctionAlias] <String>] [[-FunctionParameter] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc12e-105">說明</span><span class="sxs-lookup"><span data-stu-id="cc12e-105">DESCRIPTION</span></span>
<span data-ttu-id="cc12e-106">**AzOperationalInsightsSavedSearch** Cmdlet 會更新已存在的已儲存搜尋。</span><span class="sxs-lookup"><span data-stu-id="cc12e-106">The **Set-AzOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="cc12e-107">示例</span><span class="sxs-lookup"><span data-stu-id="cc12e-107">EXAMPLES</span></span>

### <span data-ttu-id="cc12e-108">範例1：使用更新的屬性設定已儲存的搜尋</span><span class="sxs-lookup"><span data-stu-id="cc12e-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="cc12e-109">這個命令會將已儲存的搜尋設定為已更新的屬性。</span><span class="sxs-lookup"><span data-stu-id="cc12e-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="cc12e-110">參數</span><span class="sxs-lookup"><span data-stu-id="cc12e-110">PARAMETERS</span></span>

### <span data-ttu-id="cc12e-111">-類別</span><span class="sxs-lookup"><span data-stu-id="cc12e-111">-Category</span></span>
<span data-ttu-id="cc12e-112">指定類別名稱。</span><span class="sxs-lookup"><span data-stu-id="cc12e-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="cc12e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc12e-113">-DefaultProfile</span></span>
<span data-ttu-id="cc12e-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="cc12e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cc12e-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="cc12e-115">-DisplayName</span></span>
<span data-ttu-id="cc12e-116">指定顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="cc12e-116">Specifies the display name.</span></span>

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

### <span data-ttu-id="cc12e-117">-ETag</span><span class="sxs-lookup"><span data-stu-id="cc12e-117">-ETag</span></span>
<span data-ttu-id="cc12e-118">指定 ETag 名稱。</span><span class="sxs-lookup"><span data-stu-id="cc12e-118">Specifies the ETag name.</span></span>

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

### <span data-ttu-id="cc12e-119">-FunctionAlias</span><span class="sxs-lookup"><span data-stu-id="cc12e-119">-FunctionAlias</span></span>
<span data-ttu-id="cc12e-120">如果 query 充當函數，則是函數別名。</span><span class="sxs-lookup"><span data-stu-id="cc12e-120">The function alias if query serves as a function.</span></span>

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

### <span data-ttu-id="cc12e-121">-FunctionParameter</span><span class="sxs-lookup"><span data-stu-id="cc12e-121">-FunctionParameter</span></span>
<span data-ttu-id="cc12e-122">如果 query 充當函數，則是選用的函數參數。</span><span class="sxs-lookup"><span data-stu-id="cc12e-122">The optional function parameters if query serves as a function.</span></span> <span data-ttu-id="cc12e-123">值應採用下列格式： "param-name1： type1 = default_value1，param： type2 = default_value2"。</span><span class="sxs-lookup"><span data-stu-id="cc12e-123">Value should be in the following format: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span></span> <span data-ttu-id="cc12e-124">如需更多範例及正確語法，請參閱 https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions 。</span><span class="sxs-lookup"><span data-stu-id="cc12e-124">For more examples and proper syntax please refer to https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions.</span></span>

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

### <span data-ttu-id="cc12e-125">-Query</span><span class="sxs-lookup"><span data-stu-id="cc12e-125">-Query</span></span>
<span data-ttu-id="cc12e-126">指定查詢名稱。</span><span class="sxs-lookup"><span data-stu-id="cc12e-126">Specifies the query name.</span></span>

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

### <span data-ttu-id="cc12e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc12e-127">-ResourceGroupName</span></span>
<span data-ttu-id="cc12e-128">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc12e-128">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="cc12e-129">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="cc12e-129">-SavedSearchId</span></span>
<span data-ttu-id="cc12e-130">指定已儲存的搜尋識別碼。</span><span class="sxs-lookup"><span data-stu-id="cc12e-130">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="cc12e-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="cc12e-131">-Tag</span></span>
<span data-ttu-id="cc12e-132">已儲存的搜尋標記。</span><span class="sxs-lookup"><span data-stu-id="cc12e-132">The saved search tags.</span></span>

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

### <span data-ttu-id="cc12e-133">-版本</span><span class="sxs-lookup"><span data-stu-id="cc12e-133">-Version</span></span>
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

### <span data-ttu-id="cc12e-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cc12e-134">-WorkspaceName</span></span>
<span data-ttu-id="cc12e-135">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="cc12e-135">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="cc12e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc12e-136">CommonParameters</span></span>
<span data-ttu-id="cc12e-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cc12e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc12e-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cc12e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc12e-139">輸入</span><span class="sxs-lookup"><span data-stu-id="cc12e-139">INPUTS</span></span>

### <span data-ttu-id="cc12e-140">System.object</span><span class="sxs-lookup"><span data-stu-id="cc12e-140">System.String</span></span>

### <span data-ttu-id="cc12e-141">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="cc12e-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="cc12e-142">System.object</span><span class="sxs-lookup"><span data-stu-id="cc12e-142">System.Int64</span></span>

## <span data-ttu-id="cc12e-143">輸出</span><span class="sxs-lookup"><span data-stu-id="cc12e-143">OUTPUTS</span></span>

### <span data-ttu-id="cc12e-144">HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="cc12e-144">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="cc12e-145">筆記</span><span class="sxs-lookup"><span data-stu-id="cc12e-145">NOTES</span></span>

## <span data-ttu-id="cc12e-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="cc12e-146">RELATED LINKS</span></span>

[<span data-ttu-id="cc12e-147">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cc12e-147">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


