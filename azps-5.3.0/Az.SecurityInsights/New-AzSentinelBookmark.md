---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelBookmark.md
ms.openlocfilehash: 3c30edd841eb2e773c5d813e798e63fc9858437d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448556"
---
# <span data-ttu-id="cbeba-101">New-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="cbeba-101">New-AzSentinelBookmark</span></span>

## <span data-ttu-id="cbeba-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cbeba-102">SYNOPSIS</span></span>
<span data-ttu-id="cbeba-103">建立書簽。</span><span class="sxs-lookup"><span data-stu-id="cbeba-103">Create a Bookmark.</span></span>

## <span data-ttu-id="cbeba-104">句法</span><span class="sxs-lookup"><span data-stu-id="cbeba-104">SYNTAX</span></span>

```
New-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> [-BookmarkId <String>]
 -DisplayName <String> [-IncidentInfo <PSSentinelBookmarkIncidentInfo>]
 [-Label <System.Collections.Generic.IList`1[System.String]>] [-Notes <String>] -Query <String>
 [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbeba-105">說明</span><span class="sxs-lookup"><span data-stu-id="cbeba-105">DESCRIPTION</span></span>
<span data-ttu-id="cbeba-106">**新的-AzSentinelBookmark** Cmdlet 會從指定的工作區建立書簽。</span><span class="sxs-lookup"><span data-stu-id="cbeba-106">The **New-AzSentinelBookmark** cmdlet creates a Bookmark from the specified workspace.</span></span>
<span data-ttu-id="cbeba-107">您可以使用 *Confirm* 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cbeba-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="cbeba-108">示例</span><span class="sxs-lookup"><span data-stu-id="cbeba-108">EXAMPLES</span></span>

### <span data-ttu-id="cbeba-109">範例1</span><span class="sxs-lookup"><span data-stu-id="cbeba-109">Example 1</span></span>
```powershell
PS C:\> $Bookmark = New-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DisplayName "MyBookmark" -Query "SecurityAlert | take 1"
```

<span data-ttu-id="cbeba-110">這個範例會在指定的工作區中建立 **書簽** ，然後將它儲存在 $Bookmark 變數中。</span><span class="sxs-lookup"><span data-stu-id="cbeba-110">This example creates a **Bookmark** in the specified workspace, and then stores it in the $Bookmark variable.</span></span>

## <span data-ttu-id="cbeba-111">參數</span><span class="sxs-lookup"><span data-stu-id="cbeba-111">PARAMETERS</span></span>

### <span data-ttu-id="cbeba-112">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="cbeba-112">-BookmarkId</span></span>
<span data-ttu-id="cbeba-113">書簽識別碼，</span><span class="sxs-lookup"><span data-stu-id="cbeba-113">Bookmark Id,</span></span>

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

### <span data-ttu-id="cbeba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbeba-114">-DefaultProfile</span></span>
<span data-ttu-id="cbeba-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cbeba-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbeba-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="cbeba-116">-DisplayName</span></span>
<span data-ttu-id="cbeba-117">書簽規則顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="cbeba-117">Bookmark Rule Display Name.</span></span>

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

### <span data-ttu-id="cbeba-118">-IncidentInfo</span><span class="sxs-lookup"><span data-stu-id="cbeba-118">-IncidentInfo</span></span>
<span data-ttu-id="cbeba-119">書簽事件資訊。</span><span class="sxs-lookup"><span data-stu-id="cbeba-119">Bookmark Incident Info.</span></span>

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

### <span data-ttu-id="cbeba-120">-標籤</span><span class="sxs-lookup"><span data-stu-id="cbeba-120">-Label</span></span>
<span data-ttu-id="cbeba-121">事件標籤。</span><span class="sxs-lookup"><span data-stu-id="cbeba-121">Incident Labels.</span></span>

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

### <span data-ttu-id="cbeba-122">-記事</span><span class="sxs-lookup"><span data-stu-id="cbeba-122">-Notes</span></span>
<span data-ttu-id="cbeba-123">[書簽筆記]。</span><span class="sxs-lookup"><span data-stu-id="cbeba-123">Bookmark Notes.</span></span>

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

### <span data-ttu-id="cbeba-124">-Query</span><span class="sxs-lookup"><span data-stu-id="cbeba-124">-Query</span></span>
<span data-ttu-id="cbeba-125">[書簽查詢]。</span><span class="sxs-lookup"><span data-stu-id="cbeba-125">Bookmark Query.</span></span>

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

### <span data-ttu-id="cbeba-126">-QueryResult</span><span class="sxs-lookup"><span data-stu-id="cbeba-126">-QueryResult</span></span>
<span data-ttu-id="cbeba-127">[書簽查詢結果]。</span><span class="sxs-lookup"><span data-stu-id="cbeba-127">Bookmark Query Result.</span></span>

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

### <span data-ttu-id="cbeba-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbeba-128">-ResourceGroupName</span></span>
<span data-ttu-id="cbeba-129">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="cbeba-129">Resource group name.</span></span>

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

### <span data-ttu-id="cbeba-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cbeba-130">-WorkspaceName</span></span>
<span data-ttu-id="cbeba-131">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="cbeba-131">Workspace Name.</span></span>

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

### <span data-ttu-id="cbeba-132">-確認</span><span class="sxs-lookup"><span data-stu-id="cbeba-132">-Confirm</span></span>
<span data-ttu-id="cbeba-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cbeba-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbeba-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbeba-134">-WhatIf</span></span>
<span data-ttu-id="cbeba-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cbeba-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cbeba-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cbeba-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbeba-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbeba-137">CommonParameters</span></span>
<span data-ttu-id="cbeba-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cbeba-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbeba-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cbeba-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbeba-140">輸入</span><span class="sxs-lookup"><span data-stu-id="cbeba-140">INPUTS</span></span>

### <span data-ttu-id="cbeba-141">PSSentinelBookmarkIncidentInfo （SecurityInsights.）。</span><span class="sxs-lookup"><span data-stu-id="cbeba-141">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span></span>
## <span data-ttu-id="cbeba-142">輸出</span><span class="sxs-lookup"><span data-stu-id="cbeba-142">OUTPUTS</span></span>

### <span data-ttu-id="cbeba-143">PSSentinelBookmark （SecurityInsights.）。</span><span class="sxs-lookup"><span data-stu-id="cbeba-143">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="cbeba-144">筆記</span><span class="sxs-lookup"><span data-stu-id="cbeba-144">NOTES</span></span>

## <span data-ttu-id="cbeba-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="cbeba-145">RELATED LINKS</span></span>
