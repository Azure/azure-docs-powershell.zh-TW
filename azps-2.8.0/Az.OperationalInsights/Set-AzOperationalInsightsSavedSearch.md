---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 535fbe737184b996ee0caa030c83137ea8cd1019
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2020
ms.locfileid: "93799589"
---
# <span data-ttu-id="decc1-101">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="decc1-101">Set-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="decc1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="decc1-102">SYNOPSIS</span></span>
<span data-ttu-id="decc1-103">更新已存在的已儲存搜尋。</span><span class="sxs-lookup"><span data-stu-id="decc1-103">Updates a saved search that already exists.</span></span>

## <span data-ttu-id="decc1-104">句法</span><span class="sxs-lookup"><span data-stu-id="decc1-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="decc1-105">說明</span><span class="sxs-lookup"><span data-stu-id="decc1-105">DESCRIPTION</span></span>
<span data-ttu-id="decc1-106">**AzOperationalInsightsSavedSearch** Cmdlet 會更新已存在的已儲存搜尋。</span><span class="sxs-lookup"><span data-stu-id="decc1-106">The **Set-AzOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="decc1-107">示例</span><span class="sxs-lookup"><span data-stu-id="decc1-107">EXAMPLES</span></span>

### <span data-ttu-id="decc1-108">範例1：使用更新的屬性設定已儲存的搜尋</span><span class="sxs-lookup"><span data-stu-id="decc1-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="decc1-109">這個命令會將已儲存的搜尋設定為已更新的屬性。</span><span class="sxs-lookup"><span data-stu-id="decc1-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="decc1-110">參數</span><span class="sxs-lookup"><span data-stu-id="decc1-110">PARAMETERS</span></span>

### <span data-ttu-id="decc1-111">-類別</span><span class="sxs-lookup"><span data-stu-id="decc1-111">-Category</span></span>
<span data-ttu-id="decc1-112">指定類別名稱。</span><span class="sxs-lookup"><span data-stu-id="decc1-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="decc1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="decc1-113">-DefaultProfile</span></span>
<span data-ttu-id="decc1-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="decc1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="decc1-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="decc1-115">-DisplayName</span></span>
<span data-ttu-id="decc1-116">指定顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="decc1-116">Specifies the display name.</span></span>

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

### <span data-ttu-id="decc1-117">-ETag</span><span class="sxs-lookup"><span data-stu-id="decc1-117">-ETag</span></span>
<span data-ttu-id="decc1-118">指定 ETag 名稱。</span><span class="sxs-lookup"><span data-stu-id="decc1-118">Specifies the ETag name.</span></span>

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

### <span data-ttu-id="decc1-119">-Query</span><span class="sxs-lookup"><span data-stu-id="decc1-119">-Query</span></span>
<span data-ttu-id="decc1-120">指定查詢名稱。</span><span class="sxs-lookup"><span data-stu-id="decc1-120">Specifies the query name.</span></span>

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

### <span data-ttu-id="decc1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="decc1-121">-ResourceGroupName</span></span>
<span data-ttu-id="decc1-122">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="decc1-122">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="decc1-123">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="decc1-123">-SavedSearchId</span></span>
<span data-ttu-id="decc1-124">指定已儲存的搜尋識別碼。</span><span class="sxs-lookup"><span data-stu-id="decc1-124">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="decc1-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="decc1-125">-Tag</span></span>
<span data-ttu-id="decc1-126">已儲存的搜尋標記。</span><span class="sxs-lookup"><span data-stu-id="decc1-126">The saved search tags.</span></span>

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

### <span data-ttu-id="decc1-127">-版本</span><span class="sxs-lookup"><span data-stu-id="decc1-127">-Version</span></span>
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

### <span data-ttu-id="decc1-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="decc1-128">-WorkspaceName</span></span>
<span data-ttu-id="decc1-129">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="decc1-129">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="decc1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="decc1-130">CommonParameters</span></span>
<span data-ttu-id="decc1-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="decc1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="decc1-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="decc1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="decc1-133">輸入</span><span class="sxs-lookup"><span data-stu-id="decc1-133">INPUTS</span></span>

### <span data-ttu-id="decc1-134">System.object</span><span class="sxs-lookup"><span data-stu-id="decc1-134">System.String</span></span>

### <span data-ttu-id="decc1-135">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="decc1-135">System.Collections.Hashtable</span></span>

### <span data-ttu-id="decc1-136">System.object</span><span class="sxs-lookup"><span data-stu-id="decc1-136">System.Int64</span></span>

## <span data-ttu-id="decc1-137">輸出</span><span class="sxs-lookup"><span data-stu-id="decc1-137">OUTPUTS</span></span>

### <span data-ttu-id="decc1-138">HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="decc1-138">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="decc1-139">筆記</span><span class="sxs-lookup"><span data-stu-id="decc1-139">NOTES</span></span>

## <span data-ttu-id="decc1-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="decc1-140">RELATED LINKS</span></span>

[<span data-ttu-id="decc1-141">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="decc1-141">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


