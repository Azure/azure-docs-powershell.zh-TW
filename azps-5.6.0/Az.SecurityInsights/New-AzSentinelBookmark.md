---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/new-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelBookmark.md
ms.openlocfilehash: 31c9728a95e5cfc52b283a8dddc0e24ffffe1630
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908010"
---
# <span data-ttu-id="909ce-101">New-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="909ce-101">New-AzSentinelBookmark</span></span>

## <span data-ttu-id="909ce-102">簡介</span><span class="sxs-lookup"><span data-stu-id="909ce-102">SYNOPSIS</span></span>
<span data-ttu-id="909ce-103">建立書簽。</span><span class="sxs-lookup"><span data-stu-id="909ce-103">Create a Bookmark.</span></span>

## <span data-ttu-id="909ce-104">語法</span><span class="sxs-lookup"><span data-stu-id="909ce-104">SYNTAX</span></span>

```
New-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> [-BookmarkId <String>]
 -DisplayName <String> [-IncidentInfo <PSSentinelBookmarkIncidentInfo>]
 [-Label <System.Collections.Generic.IList`1[System.String]>] [-Notes <String>] -Query <String>
 [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="909ce-105">描述</span><span class="sxs-lookup"><span data-stu-id="909ce-105">DESCRIPTION</span></span>
<span data-ttu-id="909ce-106">**New-AzSentinelBookmark** Cmdlet 會從指定的工作區建立書簽。</span><span class="sxs-lookup"><span data-stu-id="909ce-106">The **New-AzSentinelBookmark** cmdlet creates a Bookmark from the specified workspace.</span></span>
<span data-ttu-id="909ce-107">您可以使用確認 *參數$ConfirmPreference* Windows PowerShell 變數來控制 Cmdlet 是否提示您確認。</span><span class="sxs-lookup"><span data-stu-id="909ce-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="909ce-108">例子</span><span class="sxs-lookup"><span data-stu-id="909ce-108">EXAMPLES</span></span>

### <span data-ttu-id="909ce-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="909ce-109">Example 1</span></span>
```powershell
PS C:\> $Bookmark = New-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DisplayName "MyBookmark" -Query "SecurityAlert | take 1"
```

<span data-ttu-id="909ce-110">此範例會 **于指定的工作區** 中建立書簽，然後將它儲存在$Bookmark變數中。</span><span class="sxs-lookup"><span data-stu-id="909ce-110">This example creates a **Bookmark** in the specified workspace, and then stores it in the $Bookmark variable.</span></span>

## <span data-ttu-id="909ce-111">參數</span><span class="sxs-lookup"><span data-stu-id="909ce-111">PARAMETERS</span></span>

### <span data-ttu-id="909ce-112">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="909ce-112">-BookmarkId</span></span>
<span data-ttu-id="909ce-113">書簽識別碼，</span><span class="sxs-lookup"><span data-stu-id="909ce-113">Bookmark Id,</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="909ce-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="909ce-114">-DefaultProfile</span></span>
<span data-ttu-id="909ce-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="909ce-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="909ce-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="909ce-116">-DisplayName</span></span>
<span data-ttu-id="909ce-117">書簽規則顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="909ce-117">Bookmark Rule Display Name.</span></span>

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

### <span data-ttu-id="909ce-118">-IncidentInfo</span><span class="sxs-lookup"><span data-stu-id="909ce-118">-IncidentInfo</span></span>
<span data-ttu-id="909ce-119">書簽事件資訊。</span><span class="sxs-lookup"><span data-stu-id="909ce-119">Bookmark Incident Info.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="909ce-120">-標籤</span><span class="sxs-lookup"><span data-stu-id="909ce-120">-Label</span></span>
<span data-ttu-id="909ce-121">事件標籤。</span><span class="sxs-lookup"><span data-stu-id="909ce-121">Incident Labels.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="909ce-122">-記事</span><span class="sxs-lookup"><span data-stu-id="909ce-122">-Notes</span></span>
<span data-ttu-id="909ce-123">將筆記加入書簽。</span><span class="sxs-lookup"><span data-stu-id="909ce-123">Bookmark Notes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="909ce-124">-查詢</span><span class="sxs-lookup"><span data-stu-id="909ce-124">-Query</span></span>
<span data-ttu-id="909ce-125">書簽查詢。</span><span class="sxs-lookup"><span data-stu-id="909ce-125">Bookmark Query.</span></span>

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

### <span data-ttu-id="909ce-126">-QueryResult</span><span class="sxs-lookup"><span data-stu-id="909ce-126">-QueryResult</span></span>
<span data-ttu-id="909ce-127">書簽查詢結果。</span><span class="sxs-lookup"><span data-stu-id="909ce-127">Bookmark Query Result.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="909ce-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="909ce-128">-ResourceGroupName</span></span>
<span data-ttu-id="909ce-129">資源組名。</span><span class="sxs-lookup"><span data-stu-id="909ce-129">Resource group name.</span></span>

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

### <span data-ttu-id="909ce-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="909ce-130">-WorkspaceName</span></span>
<span data-ttu-id="909ce-131">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="909ce-131">Workspace Name.</span></span>

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

### <span data-ttu-id="909ce-132">-確認</span><span class="sxs-lookup"><span data-stu-id="909ce-132">-Confirm</span></span>
<span data-ttu-id="909ce-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="909ce-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="909ce-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="909ce-134">-WhatIf</span></span>
<span data-ttu-id="909ce-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="909ce-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="909ce-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="909ce-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="909ce-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="909ce-137">CommonParameters</span></span>
<span data-ttu-id="909ce-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="909ce-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="909ce-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="909ce-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="909ce-140">輸入</span><span class="sxs-lookup"><span data-stu-id="909ce-140">INPUTS</span></span>

### <span data-ttu-id="909ce-141">Microsoft.Azure.Commands.SecurityInsights.models.Bookmarks.PSSentinelBookmarkIncidentInfo</span><span class="sxs-lookup"><span data-stu-id="909ce-141">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span></span>
## <span data-ttu-id="909ce-142">輸出</span><span class="sxs-lookup"><span data-stu-id="909ce-142">OUTPUTS</span></span>

### <span data-ttu-id="909ce-143">Microsoft.Azure.Commands.SecurityInsights.models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="909ce-143">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="909ce-144">筆記</span><span class="sxs-lookup"><span data-stu-id="909ce-144">NOTES</span></span>

## <span data-ttu-id="909ce-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="909ce-145">RELATED LINKS</span></span>
