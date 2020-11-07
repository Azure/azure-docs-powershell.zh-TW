---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 2b29b0f7976f8abba8c2f1d664a40d9a67c03c5a
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2020
ms.locfileid: "93799393"
---
# <span data-ttu-id="5bc21-101">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="5bc21-101">Set-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="5bc21-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5bc21-102">SYNOPSIS</span></span>
<span data-ttu-id="5bc21-103">更新已存在的已儲存搜尋。</span><span class="sxs-lookup"><span data-stu-id="5bc21-103">Updates a saved search that already exists.</span></span>

## <span data-ttu-id="5bc21-104">句法</span><span class="sxs-lookup"><span data-stu-id="5bc21-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5bc21-105">說明</span><span class="sxs-lookup"><span data-stu-id="5bc21-105">DESCRIPTION</span></span>
<span data-ttu-id="5bc21-106">**AzOperationalInsightsSavedSearch** Cmdlet 會更新已存在的已儲存搜尋。</span><span class="sxs-lookup"><span data-stu-id="5bc21-106">The **Set-AzOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="5bc21-107">示例</span><span class="sxs-lookup"><span data-stu-id="5bc21-107">EXAMPLES</span></span>

### <span data-ttu-id="5bc21-108">範例1：使用更新的屬性設定已儲存的搜尋</span><span class="sxs-lookup"><span data-stu-id="5bc21-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="5bc21-109">這個命令會將已儲存的搜尋設定為已更新的屬性。</span><span class="sxs-lookup"><span data-stu-id="5bc21-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="5bc21-110">參數</span><span class="sxs-lookup"><span data-stu-id="5bc21-110">PARAMETERS</span></span>

### <span data-ttu-id="5bc21-111">-類別</span><span class="sxs-lookup"><span data-stu-id="5bc21-111">-Category</span></span>
<span data-ttu-id="5bc21-112">指定類別名稱。</span><span class="sxs-lookup"><span data-stu-id="5bc21-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="5bc21-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bc21-113">-DefaultProfile</span></span>
<span data-ttu-id="5bc21-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="5bc21-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5bc21-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5bc21-115">-DisplayName</span></span>
<span data-ttu-id="5bc21-116">指定顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="5bc21-116">Specifies the display name.</span></span>

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

### <span data-ttu-id="5bc21-117">-ETag</span><span class="sxs-lookup"><span data-stu-id="5bc21-117">-ETag</span></span>
<span data-ttu-id="5bc21-118">指定 ETag 名稱。</span><span class="sxs-lookup"><span data-stu-id="5bc21-118">Specifies the ETag name.</span></span>

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

### <span data-ttu-id="5bc21-119">-Query</span><span class="sxs-lookup"><span data-stu-id="5bc21-119">-Query</span></span>
<span data-ttu-id="5bc21-120">指定查詢名稱。</span><span class="sxs-lookup"><span data-stu-id="5bc21-120">Specifies the query name.</span></span>

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

### <span data-ttu-id="5bc21-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bc21-121">-ResourceGroupName</span></span>
<span data-ttu-id="5bc21-122">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5bc21-122">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="5bc21-123">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="5bc21-123">-SavedSearchId</span></span>
<span data-ttu-id="5bc21-124">指定已儲存的搜尋識別碼。</span><span class="sxs-lookup"><span data-stu-id="5bc21-124">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="5bc21-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="5bc21-125">-Tag</span></span>
<span data-ttu-id="5bc21-126">已儲存的搜尋標記。</span><span class="sxs-lookup"><span data-stu-id="5bc21-126">The saved search tags.</span></span>

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

### <span data-ttu-id="5bc21-127">-版本</span><span class="sxs-lookup"><span data-stu-id="5bc21-127">-Version</span></span>
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

### <span data-ttu-id="5bc21-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5bc21-128">-WorkspaceName</span></span>
<span data-ttu-id="5bc21-129">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="5bc21-129">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="5bc21-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bc21-130">CommonParameters</span></span>
<span data-ttu-id="5bc21-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5bc21-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bc21-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5bc21-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bc21-133">輸入</span><span class="sxs-lookup"><span data-stu-id="5bc21-133">INPUTS</span></span>

### <span data-ttu-id="5bc21-134">System.object</span><span class="sxs-lookup"><span data-stu-id="5bc21-134">System.String</span></span>

### <span data-ttu-id="5bc21-135">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5bc21-135">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5bc21-136">System.object</span><span class="sxs-lookup"><span data-stu-id="5bc21-136">System.Int64</span></span>

## <span data-ttu-id="5bc21-137">輸出</span><span class="sxs-lookup"><span data-stu-id="5bc21-137">OUTPUTS</span></span>

### <span data-ttu-id="5bc21-138">HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="5bc21-138">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="5bc21-139">筆記</span><span class="sxs-lookup"><span data-stu-id="5bc21-139">NOTES</span></span>

## <span data-ttu-id="5bc21-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="5bc21-140">RELATED LINKS</span></span>

[<span data-ttu-id="5bc21-141">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5bc21-141">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


