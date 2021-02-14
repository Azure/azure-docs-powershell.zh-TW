---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelBookmark.md
ms.openlocfilehash: 544c019fd52c0cb5723cbeafb5a82df072ac284e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100134619"
---
# <span data-ttu-id="3345d-101">Remove-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="3345d-101">Remove-AzSentinelBookmark</span></span>

## <span data-ttu-id="3345d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3345d-102">SYNOPSIS</span></span>
<span data-ttu-id="3345d-103">刪除書簽。</span><span class="sxs-lookup"><span data-stu-id="3345d-103">Delete a Bookmark.</span></span>

## <span data-ttu-id="3345d-104">句法</span><span class="sxs-lookup"><span data-stu-id="3345d-104">SYNTAX</span></span>

### <span data-ttu-id="3345d-105">BookmarkId.</span><span class="sxs-lookup"><span data-stu-id="3345d-105">BookmarkId.</span></span> <span data-ttu-id="3345d-106"> (預設) </span><span class="sxs-lookup"><span data-stu-id="3345d-106">(Default)</span></span>
```
Remove-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3345d-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="3345d-107">InputObject</span></span>
```
Remove-AzSentinelBookmark -InputObject <PSSentinelBookmark> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3345d-108">說明</span><span class="sxs-lookup"><span data-stu-id="3345d-108">DESCRIPTION</span></span>
<span data-ttu-id="3345d-109">**AzSentinelBookmark** Cmdlet 會從指定的工作區永久刪除書簽。</span><span class="sxs-lookup"><span data-stu-id="3345d-109">The **Remove-AzSentinelBookmark** cmdlet permanently deletes a Bookmark from a specified workspace.</span></span>
<span data-ttu-id="3345d-110">您可以使用管線運算子傳遞 **Bookmark** 物件，或者也可以指定所需的參數。</span><span class="sxs-lookup"><span data-stu-id="3345d-110">You can pass an **Bookmark** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="3345d-111">您可以使用 Confirm 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3345d-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="3345d-112">示例</span><span class="sxs-lookup"><span data-stu-id="3345d-112">EXAMPLES</span></span>

### <span data-ttu-id="3345d-113">範例1</span><span class="sxs-lookup"><span data-stu-id="3345d-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -BookmarkId "MyBookmarkId"
```

<span data-ttu-id="3345d-114">這個命令會從工作區移除書簽。</span><span class="sxs-lookup"><span data-stu-id="3345d-114">This command removes the Bookmark from the workspace.</span></span>

## <span data-ttu-id="3345d-115">參數</span><span class="sxs-lookup"><span data-stu-id="3345d-115">PARAMETERS</span></span>

### <span data-ttu-id="3345d-116">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="3345d-116">-BookmarkId</span></span>
<span data-ttu-id="3345d-117">書簽識別碼，</span><span class="sxs-lookup"><span data-stu-id="3345d-117">Bookmark Id,</span></span>

```yaml
Type: System.String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3345d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3345d-118">-DefaultProfile</span></span>
<span data-ttu-id="3345d-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3345d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3345d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3345d-120">-InputObject</span></span>
<span data-ttu-id="3345d-121">InputObject.</span><span class="sxs-lookup"><span data-stu-id="3345d-121">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3345d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3345d-122">-PassThru</span></span>
<span data-ttu-id="3345d-123">PassThru</span><span class="sxs-lookup"><span data-stu-id="3345d-123">PassThru</span></span>

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

### <span data-ttu-id="3345d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3345d-124">-ResourceGroupName</span></span>
<span data-ttu-id="3345d-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="3345d-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3345d-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3345d-126">-WorkspaceName</span></span>
<span data-ttu-id="3345d-127">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="3345d-127">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3345d-128">-確認</span><span class="sxs-lookup"><span data-stu-id="3345d-128">-Confirm</span></span>
<span data-ttu-id="3345d-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3345d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3345d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3345d-130">-WhatIf</span></span>
<span data-ttu-id="3345d-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3345d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3345d-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3345d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3345d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3345d-133">CommonParameters</span></span>
<span data-ttu-id="3345d-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3345d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3345d-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3345d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3345d-136">輸入</span><span class="sxs-lookup"><span data-stu-id="3345d-136">INPUTS</span></span>

### <span data-ttu-id="3345d-137">System.object</span><span class="sxs-lookup"><span data-stu-id="3345d-137">System.String</span></span>
### <span data-ttu-id="3345d-138">PSSentinelBookmark （SecurityInsights.）。</span><span class="sxs-lookup"><span data-stu-id="3345d-138">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="3345d-139">輸出</span><span class="sxs-lookup"><span data-stu-id="3345d-139">OUTPUTS</span></span>

### <span data-ttu-id="3345d-140">PSSentinelBookmark （SecurityInsights.）。</span><span class="sxs-lookup"><span data-stu-id="3345d-140">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="3345d-141">筆記</span><span class="sxs-lookup"><span data-stu-id="3345d-141">NOTES</span></span>

## <span data-ttu-id="3345d-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="3345d-142">RELATED LINKS</span></span>
