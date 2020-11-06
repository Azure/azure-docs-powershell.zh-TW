---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 5853447dfc91511782e99ebafae644e14b6649b3
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2020
ms.locfileid: "93623368"
---
# <span data-ttu-id="048e1-101">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="048e1-101">New-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="048e1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="048e1-102">SYNOPSIS</span></span>
<span data-ttu-id="048e1-103">使用指定的參數建立新的已儲存搜尋。</span><span class="sxs-lookup"><span data-stu-id="048e1-103">Creates a new saved search with the specified parameters.</span></span>

## <span data-ttu-id="048e1-104">句法</span><span class="sxs-lookup"><span data-stu-id="048e1-104">SYNTAX</span></span>

```
New-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="048e1-105">說明</span><span class="sxs-lookup"><span data-stu-id="048e1-105">DESCRIPTION</span></span>
<span data-ttu-id="048e1-106">**新的-AzOperationalInsightsSavedSearch** Cmdlet 會使用指定的工作區參數來建立新的已儲存搜尋。</span><span class="sxs-lookup"><span data-stu-id="048e1-106">The **New-AzOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="048e1-107">示例</span><span class="sxs-lookup"><span data-stu-id="048e1-107">EXAMPLES</span></span>

### <span data-ttu-id="048e1-108">範例1：建立新的已儲存搜尋</span><span class="sxs-lookup"><span data-stu-id="048e1-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzOperationalInsightSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="048e1-109">這個命令會建立新的已儲存搜尋。</span><span class="sxs-lookup"><span data-stu-id="048e1-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="048e1-110">參數</span><span class="sxs-lookup"><span data-stu-id="048e1-110">PARAMETERS</span></span>

### <span data-ttu-id="048e1-111">-類別</span><span class="sxs-lookup"><span data-stu-id="048e1-111">-Category</span></span>
<span data-ttu-id="048e1-112">指定類別名稱。</span><span class="sxs-lookup"><span data-stu-id="048e1-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="048e1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="048e1-113">-DefaultProfile</span></span>
<span data-ttu-id="048e1-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="048e1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="048e1-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="048e1-115">-DisplayName</span></span>
<span data-ttu-id="048e1-116">指定已儲存的搜尋顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="048e1-116">Specifies the saved search display name.</span></span>

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

### <span data-ttu-id="048e1-117">-Force</span><span class="sxs-lookup"><span data-stu-id="048e1-117">-Force</span></span>
<span data-ttu-id="048e1-118">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="048e1-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="048e1-119">-Query</span><span class="sxs-lookup"><span data-stu-id="048e1-119">-Query</span></span>
<span data-ttu-id="048e1-120">指定查詢名稱。</span><span class="sxs-lookup"><span data-stu-id="048e1-120">Specifies the query name.</span></span>

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

### <span data-ttu-id="048e1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="048e1-121">-ResourceGroupName</span></span>
<span data-ttu-id="048e1-122">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="048e1-122">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="048e1-123">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="048e1-123">-SavedSearchId</span></span>
<span data-ttu-id="048e1-124">指定已儲存的搜尋識別碼。</span><span class="sxs-lookup"><span data-stu-id="048e1-124">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="048e1-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="048e1-125">-Tag</span></span>
<span data-ttu-id="048e1-126">已儲存的搜尋標記。</span><span class="sxs-lookup"><span data-stu-id="048e1-126">The saved search tags.</span></span>

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

### <span data-ttu-id="048e1-127">-版本</span><span class="sxs-lookup"><span data-stu-id="048e1-127">-Version</span></span>
<span data-ttu-id="048e1-128">指定版本。</span><span class="sxs-lookup"><span data-stu-id="048e1-128">Specifies the version.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="048e1-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="048e1-129">-WorkspaceName</span></span>
<span data-ttu-id="048e1-130">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="048e1-130">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="048e1-131">-確認</span><span class="sxs-lookup"><span data-stu-id="048e1-131">-Confirm</span></span>
<span data-ttu-id="048e1-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="048e1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="048e1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="048e1-133">-WhatIf</span></span>
<span data-ttu-id="048e1-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="048e1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="048e1-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="048e1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="048e1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="048e1-136">CommonParameters</span></span>
<span data-ttu-id="048e1-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="048e1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="048e1-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="048e1-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="048e1-139">輸入</span><span class="sxs-lookup"><span data-stu-id="048e1-139">INPUTS</span></span>

### <span data-ttu-id="048e1-140">System.object</span><span class="sxs-lookup"><span data-stu-id="048e1-140">System.String</span></span>

### <span data-ttu-id="048e1-141">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="048e1-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="048e1-142">System.object</span><span class="sxs-lookup"><span data-stu-id="048e1-142">System.Int64</span></span>

## <span data-ttu-id="048e1-143">輸出</span><span class="sxs-lookup"><span data-stu-id="048e1-143">OUTPUTS</span></span>

### <span data-ttu-id="048e1-144">HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="048e1-144">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="048e1-145">筆記</span><span class="sxs-lookup"><span data-stu-id="048e1-145">NOTES</span></span>

## <span data-ttu-id="048e1-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="048e1-146">RELATED LINKS</span></span>

[<span data-ttu-id="048e1-147">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="048e1-147">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


