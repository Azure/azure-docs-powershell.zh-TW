---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: c8ad9196cd0f89670de38f6c99550e397016661e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457059"
---
# <span data-ttu-id="138cd-101">New-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="138cd-101">New-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="138cd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="138cd-102">SYNOPSIS</span></span>
<span data-ttu-id="138cd-103">使用指定的參數建立新的已儲存搜尋。</span><span class="sxs-lookup"><span data-stu-id="138cd-103">Creates a new saved search with the specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="138cd-104">句法</span><span class="sxs-lookup"><span data-stu-id="138cd-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="138cd-105">說明</span><span class="sxs-lookup"><span data-stu-id="138cd-105">DESCRIPTION</span></span>
<span data-ttu-id="138cd-106">**新的-AzureRmOperationalInsightsSavedSearch** Cmdlet 會使用指定的工作區參數來建立新的已儲存搜尋。</span><span class="sxs-lookup"><span data-stu-id="138cd-106">The **New-AzureRmOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="138cd-107">示例</span><span class="sxs-lookup"><span data-stu-id="138cd-107">EXAMPLES</span></span>

### <span data-ttu-id="138cd-108">範例1：建立新的已儲存搜尋</span><span class="sxs-lookup"><span data-stu-id="138cd-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzureRmOperationalInsightSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="138cd-109">這個命令會建立新的已儲存搜尋。</span><span class="sxs-lookup"><span data-stu-id="138cd-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="138cd-110">參數</span><span class="sxs-lookup"><span data-stu-id="138cd-110">PARAMETERS</span></span>

### <span data-ttu-id="138cd-111">-類別</span><span class="sxs-lookup"><span data-stu-id="138cd-111">-Category</span></span>
<span data-ttu-id="138cd-112">指定類別名稱。</span><span class="sxs-lookup"><span data-stu-id="138cd-112">Specifies the category name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="138cd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="138cd-113">-DefaultProfile</span></span>
<span data-ttu-id="138cd-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="138cd-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="138cd-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="138cd-115">-DisplayName</span></span>
<span data-ttu-id="138cd-116">指定已儲存的搜尋顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="138cd-116">Specifies the saved search display name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="138cd-117">-Force</span><span class="sxs-lookup"><span data-stu-id="138cd-117">-Force</span></span>
<span data-ttu-id="138cd-118">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="138cd-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="138cd-119">-Query</span><span class="sxs-lookup"><span data-stu-id="138cd-119">-Query</span></span>
<span data-ttu-id="138cd-120">指定查詢名稱。</span><span class="sxs-lookup"><span data-stu-id="138cd-120">Specifies the query name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="138cd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="138cd-121">-ResourceGroupName</span></span>
<span data-ttu-id="138cd-122">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="138cd-122">Specifies the resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="138cd-123">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="138cd-123">-SavedSearchId</span></span>
<span data-ttu-id="138cd-124">指定已儲存的搜尋識別碼。</span><span class="sxs-lookup"><span data-stu-id="138cd-124">Specifies the saved search ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="138cd-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="138cd-125">-Tag</span></span>
<span data-ttu-id="138cd-126">已儲存的搜尋標記。</span><span class="sxs-lookup"><span data-stu-id="138cd-126">The saved search tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="138cd-127">-版本</span><span class="sxs-lookup"><span data-stu-id="138cd-127">-Version</span></span>
<span data-ttu-id="138cd-128">指定版本。</span><span class="sxs-lookup"><span data-stu-id="138cd-128">Specifies the version.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="138cd-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="138cd-129">-WorkspaceName</span></span>
<span data-ttu-id="138cd-130">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="138cd-130">Specifies the workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="138cd-131">-確認</span><span class="sxs-lookup"><span data-stu-id="138cd-131">-Confirm</span></span>
<span data-ttu-id="138cd-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="138cd-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="138cd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="138cd-133">-WhatIf</span></span>
<span data-ttu-id="138cd-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="138cd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="138cd-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="138cd-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="138cd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="138cd-136">CommonParameters</span></span>
<span data-ttu-id="138cd-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="138cd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="138cd-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="138cd-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="138cd-139">輸入</span><span class="sxs-lookup"><span data-stu-id="138cd-139">INPUTS</span></span>

### <span data-ttu-id="138cd-140">所有</span><span class="sxs-lookup"><span data-stu-id="138cd-140">None</span></span>
<span data-ttu-id="138cd-141">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="138cd-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="138cd-142">輸出</span><span class="sxs-lookup"><span data-stu-id="138cd-142">OUTPUTS</span></span>

## <span data-ttu-id="138cd-143">筆記</span><span class="sxs-lookup"><span data-stu-id="138cd-143">NOTES</span></span>

## <span data-ttu-id="138cd-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="138cd-144">RELATED LINKS</span></span>

[<span data-ttu-id="138cd-145">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="138cd-145">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


