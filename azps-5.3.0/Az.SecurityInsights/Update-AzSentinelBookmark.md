---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelBookmark.md
ms.openlocfilehash: ebc0ffd78f653276e66b85d263db41803a48c356
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448508"
---
# <span data-ttu-id="59e95-101">Update-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="59e95-101">Update-AzSentinelBookmark</span></span>

## <span data-ttu-id="59e95-102">摘要</span><span class="sxs-lookup"><span data-stu-id="59e95-102">SYNOPSIS</span></span>
<span data-ttu-id="59e95-103">更新書簽。</span><span class="sxs-lookup"><span data-stu-id="59e95-103">Update a Bookmark.</span></span>

## <span data-ttu-id="59e95-104">句法</span><span class="sxs-lookup"><span data-stu-id="59e95-104">SYNTAX</span></span>

### <span data-ttu-id="59e95-105">BookmarkId.</span><span class="sxs-lookup"><span data-stu-id="59e95-105">BookmarkId.</span></span> <span data-ttu-id="59e95-106"> (預設) </span><span class="sxs-lookup"><span data-stu-id="59e95-106">(Default)</span></span>
```
Update-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String>
 [-DisplayName <String>] [-IncidentInfo <PSSentinelBookmarkIncidentInfo>]
 [-Label <System.Collections.Generic.IList`1[System.String]>] [-Notes <String>] [-Query <String>]
 [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59e95-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="59e95-107">InputObject</span></span>
```
Update-AzSentinelBookmark -InputObject <PSSentinelBookmark> [-DisplayName <String>]
 [-IncidentInfo <PSSentinelBookmarkIncidentInfo>] [-Label <System.Collections.Generic.IList`1[System.String]>]
 [-Notes <String>] [-Query <String>] [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59e95-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="59e95-108">ResourceId</span></span>
```
Update-AzSentinelBookmark -ResourceId <String> [-DisplayName <String>]
 [-IncidentInfo <PSSentinelBookmarkIncidentInfo>] [-Label <System.Collections.Generic.IList`1[System.String]>]
 [-Notes <String>] [-Query <String>] [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59e95-109">說明</span><span class="sxs-lookup"><span data-stu-id="59e95-109">DESCRIPTION</span></span>
<span data-ttu-id="59e95-110">**更新-AzSentinelBookmark** Cmdlet 會更新指定工作區中的書簽。</span><span class="sxs-lookup"><span data-stu-id="59e95-110">The **Update-AzSentinelBookmark** cmdlet updates the bookmark in the specified workspace.</span></span>
<span data-ttu-id="59e95-111">您可以將 **書簽** 物件作為參數或使用管線運算子來傳遞，或者也可以指定所需的 *BookmarkId* 參數。</span><span class="sxs-lookup"><span data-stu-id="59e95-111">You can pass an **Bookmark** object as a parameter or by using the pipeline operator, or alternatively you can specify the required *BookmarkId* parameters.</span></span>
<span data-ttu-id="59e95-112">您可以使用 *Confirm* 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="59e95-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="59e95-113">示例</span><span class="sxs-lookup"><span data-stu-id="59e95-113">EXAMPLES</span></span>

### <span data-ttu-id="59e95-114">範例1</span><span class="sxs-lookup"><span data-stu-id="59e95-114">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceNAme" -BookmarkId "MyBookmarkId" -Notes "Found something interesting"
```

<span data-ttu-id="59e95-115">此命令會透過設定 *記事* 屬性來更新書簽。</span><span class="sxs-lookup"><span data-stu-id="59e95-115">The command updates the Bookmark by setting the *Notes* property.</span></span>  <span data-ttu-id="59e95-116">所有其他 propreties 會保持不變。</span><span class="sxs-lookup"><span data-stu-id="59e95-116">All other propreties stay the same.</span></span>

### <span data-ttu-id="59e95-117">範例2</span><span class="sxs-lookup"><span data-stu-id="59e95-117">Example 2</span></span>
```powershell
PS C:\> $Bookmark = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceNAme" -BookmarkId "MyBookmarkId"
PS C:\> $Bookmark | Set-AzSentinelBookmark -Notes "Found something interesting"
```

<span data-ttu-id="59e95-118">第一個命令會從指定的工作區 *BookmarkId* 來取得書簽，然後將其儲存在 $Bookmark 變數中。</span><span class="sxs-lookup"><span data-stu-id="59e95-118">The first command gets the Bookmark by *BookmarkId* from the specified workspace, and then stores it in the $Bookmark variable.</span></span>
<span data-ttu-id="59e95-119">第二個命令會更新記事屬性。</span><span class="sxs-lookup"><span data-stu-id="59e95-119">The second command updates the Notes property.</span></span>   <span data-ttu-id="59e95-120">所有其他 propreties 會保持不變。</span><span class="sxs-lookup"><span data-stu-id="59e95-120">All other propreties stay the same.</span></span>

## <span data-ttu-id="59e95-121">參數</span><span class="sxs-lookup"><span data-stu-id="59e95-121">PARAMETERS</span></span>

### <span data-ttu-id="59e95-122">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="59e95-122">-BookmarkId</span></span>
<span data-ttu-id="59e95-123">書簽識別碼，</span><span class="sxs-lookup"><span data-stu-id="59e95-123">Bookmark Id,</span></span>

```yaml
Type: String
Parameter Sets: BookmarkId., ParentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59e95-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59e95-124">-DefaultProfile</span></span>
<span data-ttu-id="59e95-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="59e95-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59e95-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="59e95-126">-DisplayName</span></span>
<span data-ttu-id="59e95-127">書簽規則顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="59e95-127">Bookmark Rule Display Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59e95-128">-IncidentInfo</span><span class="sxs-lookup"><span data-stu-id="59e95-128">-IncidentInfo</span></span>
<span data-ttu-id="59e95-129">書簽事件資訊。</span><span class="sxs-lookup"><span data-stu-id="59e95-129">Bookmark Incident Info.</span></span>

```yaml
Type: PSSentinelBookmarkIncidentInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59e95-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59e95-130">-InputObject</span></span>
<span data-ttu-id="59e95-131">InputObject.</span><span class="sxs-lookup"><span data-stu-id="59e95-131">InputObject.</span></span>

```yaml
Type: PSSentinelBookmark
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59e95-132">-標籤</span><span class="sxs-lookup"><span data-stu-id="59e95-132">-Label</span></span>
<span data-ttu-id="59e95-133">事件標籤。</span><span class="sxs-lookup"><span data-stu-id="59e95-133">Incident Labels.</span></span>

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

### <span data-ttu-id="59e95-134">-記事</span><span class="sxs-lookup"><span data-stu-id="59e95-134">-Notes</span></span>
<span data-ttu-id="59e95-135">[書簽筆記]。</span><span class="sxs-lookup"><span data-stu-id="59e95-135">Bookmark Notes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59e95-136">-Query</span><span class="sxs-lookup"><span data-stu-id="59e95-136">-Query</span></span>
<span data-ttu-id="59e95-137">[書簽查詢]。</span><span class="sxs-lookup"><span data-stu-id="59e95-137">Bookmark Query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59e95-138">-QueryResult</span><span class="sxs-lookup"><span data-stu-id="59e95-138">-QueryResult</span></span>
<span data-ttu-id="59e95-139">[書簽查詢結果]。</span><span class="sxs-lookup"><span data-stu-id="59e95-139">Bookmark Query Result.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59e95-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59e95-140">-ResourceGroupName</span></span>
<span data-ttu-id="59e95-141">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="59e95-141">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59e95-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59e95-142">-ResourceId</span></span>
<span data-ttu-id="59e95-143">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="59e95-143">Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59e95-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="59e95-144">-WorkspaceName</span></span>
<span data-ttu-id="59e95-145">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="59e95-145">Workspace Name.</span></span>

```yaml
Type: String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59e95-146">-確認</span><span class="sxs-lookup"><span data-stu-id="59e95-146">-Confirm</span></span>
<span data-ttu-id="59e95-147">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="59e95-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59e95-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59e95-148">-WhatIf</span></span>
<span data-ttu-id="59e95-149">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="59e95-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59e95-150">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="59e95-150">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59e95-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59e95-151">CommonParameters</span></span>
<span data-ttu-id="59e95-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="59e95-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59e95-153">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="59e95-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59e95-154">輸入</span><span class="sxs-lookup"><span data-stu-id="59e95-154">INPUTS</span></span>

### <span data-ttu-id="59e95-155">PSSentinelBookmark （SecurityInsights.）。</span><span class="sxs-lookup"><span data-stu-id="59e95-155">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>

### <span data-ttu-id="59e95-156">System.object</span><span class="sxs-lookup"><span data-stu-id="59e95-156">System.String</span></span>

### <span data-ttu-id="59e95-157">PSSentinelBookmarkIncidentInfo （SecurityInsights.）。</span><span class="sxs-lookup"><span data-stu-id="59e95-157">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span></span>

## <span data-ttu-id="59e95-158">輸出</span><span class="sxs-lookup"><span data-stu-id="59e95-158">OUTPUTS</span></span>

### <span data-ttu-id="59e95-159">PSSentinelBookmark （SecurityInsights.）。</span><span class="sxs-lookup"><span data-stu-id="59e95-159">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>

## <span data-ttu-id="59e95-160">筆記</span><span class="sxs-lookup"><span data-stu-id="59e95-160">NOTES</span></span>

## <span data-ttu-id="59e95-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="59e95-161">RELATED LINKS</span></span>
