---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/update-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelBookmark.md
ms.openlocfilehash: eccb0ce5a9a92eae956c11273bf6397f20473e39
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902173"
---
# <span data-ttu-id="32a71-101">Update-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="32a71-101">Update-AzSentinelBookmark</span></span>

## <span data-ttu-id="32a71-102">簡介</span><span class="sxs-lookup"><span data-stu-id="32a71-102">SYNOPSIS</span></span>
<span data-ttu-id="32a71-103">更新書簽。</span><span class="sxs-lookup"><span data-stu-id="32a71-103">Update a Bookmark.</span></span>

## <span data-ttu-id="32a71-104">語法</span><span class="sxs-lookup"><span data-stu-id="32a71-104">SYNTAX</span></span>

### <span data-ttu-id="32a71-105">BookmarkId。</span><span class="sxs-lookup"><span data-stu-id="32a71-105">BookmarkId.</span></span> <span data-ttu-id="32a71-106"> (預設) </span><span class="sxs-lookup"><span data-stu-id="32a71-106">(Default)</span></span>
```
Update-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String>
 [-DisplayName <String>] [-IncidentInfo <PSSentinelBookmarkIncidentInfo>]
 [-Label <System.Collections.Generic.IList`1[System.String]>] [-Notes <String>] [-Query <String>]
 [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32a71-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="32a71-107">InputObject</span></span>
```
Update-AzSentinelBookmark -InputObject <PSSentinelBookmark> [-DisplayName <String>]
 [-IncidentInfo <PSSentinelBookmarkIncidentInfo>] [-Label <System.Collections.Generic.IList`1[System.String]>]
 [-Notes <String>] [-Query <String>] [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32a71-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="32a71-108">ResourceId</span></span>
```
Update-AzSentinelBookmark -ResourceId <String> [-DisplayName <String>]
 [-IncidentInfo <PSSentinelBookmarkIncidentInfo>] [-Label <System.Collections.Generic.IList`1[System.String]>]
 [-Notes <String>] [-Query <String>] [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32a71-109">描述</span><span class="sxs-lookup"><span data-stu-id="32a71-109">DESCRIPTION</span></span>
<span data-ttu-id="32a71-110">**Update-AzSentinelBookmark** Cmdlet 會更新指定工作區中的書簽。</span><span class="sxs-lookup"><span data-stu-id="32a71-110">The **Update-AzSentinelBookmark** cmdlet updates the bookmark in the specified workspace.</span></span>
<span data-ttu-id="32a71-111">您可以傳遞 **書簽** 物件做為參數，或是使用管線運算子，或者您也可以指定所需的 *BookmarkId* 參數。</span><span class="sxs-lookup"><span data-stu-id="32a71-111">You can pass an **Bookmark** object as a parameter or by using the pipeline operator, or alternatively you can specify the required *BookmarkId* parameters.</span></span>
<span data-ttu-id="32a71-112">您可以使用確認 *參數$ConfirmPreference* Windows PowerShell 變數來控制 Cmdlet 是否提示您確認。</span><span class="sxs-lookup"><span data-stu-id="32a71-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="32a71-113">例子</span><span class="sxs-lookup"><span data-stu-id="32a71-113">EXAMPLES</span></span>

### <span data-ttu-id="32a71-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="32a71-114">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceNAme" -BookmarkId "MyBookmarkId" -Notes "Found something interesting"
```

<span data-ttu-id="32a71-115">命令會設定 Notes 屬性來 *更新書簽* 。</span><span class="sxs-lookup"><span data-stu-id="32a71-115">The command updates the Bookmark by setting the *Notes* property.</span></span>  <span data-ttu-id="32a71-116">所有其他的排泄都保持不變。</span><span class="sxs-lookup"><span data-stu-id="32a71-116">All other propreties stay the same.</span></span>

### <span data-ttu-id="32a71-117">範例 2</span><span class="sxs-lookup"><span data-stu-id="32a71-117">Example 2</span></span>
```powershell
PS C:\> $Bookmark = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceNAme" -BookmarkId "MyBookmarkId"
PS C:\> $Bookmark | Set-AzSentinelBookmark -Notes "Found something interesting"
```

<span data-ttu-id="32a71-118">第一個命令會從指定的工作區獲得 *BookmarkId* 書簽，然後將它儲存在$Bookmark變數中。</span><span class="sxs-lookup"><span data-stu-id="32a71-118">The first command gets the Bookmark by *BookmarkId* from the specified workspace, and then stores it in the $Bookmark variable.</span></span>
<span data-ttu-id="32a71-119">第二個命令會更新 Notes 屬性。</span><span class="sxs-lookup"><span data-stu-id="32a71-119">The second command updates the Notes property.</span></span>   <span data-ttu-id="32a71-120">所有其他的排泄都保持不變。</span><span class="sxs-lookup"><span data-stu-id="32a71-120">All other propreties stay the same.</span></span>

## <span data-ttu-id="32a71-121">參數</span><span class="sxs-lookup"><span data-stu-id="32a71-121">PARAMETERS</span></span>

### <span data-ttu-id="32a71-122">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="32a71-122">-BookmarkId</span></span>
<span data-ttu-id="32a71-123">書簽識別碼，</span><span class="sxs-lookup"><span data-stu-id="32a71-123">Bookmark Id,</span></span>

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

### <span data-ttu-id="32a71-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32a71-124">-DefaultProfile</span></span>
<span data-ttu-id="32a71-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="32a71-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32a71-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="32a71-126">-DisplayName</span></span>
<span data-ttu-id="32a71-127">書簽規則顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="32a71-127">Bookmark Rule Display Name.</span></span>

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

### <span data-ttu-id="32a71-128">-IncidentInfo</span><span class="sxs-lookup"><span data-stu-id="32a71-128">-IncidentInfo</span></span>
<span data-ttu-id="32a71-129">書簽事件資訊。</span><span class="sxs-lookup"><span data-stu-id="32a71-129">Bookmark Incident Info.</span></span>

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

### <span data-ttu-id="32a71-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="32a71-130">-InputObject</span></span>
<span data-ttu-id="32a71-131">InputObject。</span><span class="sxs-lookup"><span data-stu-id="32a71-131">InputObject.</span></span>

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

### <span data-ttu-id="32a71-132">-標籤</span><span class="sxs-lookup"><span data-stu-id="32a71-132">-Label</span></span>
<span data-ttu-id="32a71-133">事件標籤。</span><span class="sxs-lookup"><span data-stu-id="32a71-133">Incident Labels.</span></span>

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

### <span data-ttu-id="32a71-134">-記事</span><span class="sxs-lookup"><span data-stu-id="32a71-134">-Notes</span></span>
<span data-ttu-id="32a71-135">將筆記加入書簽。</span><span class="sxs-lookup"><span data-stu-id="32a71-135">Bookmark Notes.</span></span>

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

### <span data-ttu-id="32a71-136">-查詢</span><span class="sxs-lookup"><span data-stu-id="32a71-136">-Query</span></span>
<span data-ttu-id="32a71-137">書簽查詢。</span><span class="sxs-lookup"><span data-stu-id="32a71-137">Bookmark Query.</span></span>

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

### <span data-ttu-id="32a71-138">-QueryResult</span><span class="sxs-lookup"><span data-stu-id="32a71-138">-QueryResult</span></span>
<span data-ttu-id="32a71-139">書簽查詢結果。</span><span class="sxs-lookup"><span data-stu-id="32a71-139">Bookmark Query Result.</span></span>

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

### <span data-ttu-id="32a71-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32a71-140">-ResourceGroupName</span></span>
<span data-ttu-id="32a71-141">資源組名。</span><span class="sxs-lookup"><span data-stu-id="32a71-141">Resource group name.</span></span>

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

### <span data-ttu-id="32a71-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="32a71-142">-ResourceId</span></span>
<span data-ttu-id="32a71-143">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="32a71-143">Resource Id.</span></span>

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

### <span data-ttu-id="32a71-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="32a71-144">-WorkspaceName</span></span>
<span data-ttu-id="32a71-145">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="32a71-145">Workspace Name.</span></span>

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

### <span data-ttu-id="32a71-146">-確認</span><span class="sxs-lookup"><span data-stu-id="32a71-146">-Confirm</span></span>
<span data-ttu-id="32a71-147">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="32a71-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32a71-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32a71-148">-WhatIf</span></span>
<span data-ttu-id="32a71-149">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="32a71-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32a71-150">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="32a71-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32a71-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32a71-151">CommonParameters</span></span>
<span data-ttu-id="32a71-152">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="32a71-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32a71-153">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="32a71-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32a71-154">輸入</span><span class="sxs-lookup"><span data-stu-id="32a71-154">INPUTS</span></span>

### <span data-ttu-id="32a71-155">Microsoft.Azure.Commands.SecurityInsights.models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="32a71-155">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>

### <span data-ttu-id="32a71-156">System.String</span><span class="sxs-lookup"><span data-stu-id="32a71-156">System.String</span></span>

### <span data-ttu-id="32a71-157">Microsoft.Azure.Commands.SecurityInsights.models.Bookmarks.PSSentinelBookmarkIncidentInfo</span><span class="sxs-lookup"><span data-stu-id="32a71-157">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span></span>

## <span data-ttu-id="32a71-158">輸出</span><span class="sxs-lookup"><span data-stu-id="32a71-158">OUTPUTS</span></span>

### <span data-ttu-id="32a71-159">Microsoft.Azure.Commands.SecurityInsights.models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="32a71-159">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>

## <span data-ttu-id="32a71-160">筆記</span><span class="sxs-lookup"><span data-stu-id="32a71-160">NOTES</span></span>

## <span data-ttu-id="32a71-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="32a71-161">RELATED LINKS</span></span>
