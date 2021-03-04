---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/remove-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelBookmark.md
ms.openlocfilehash: ed75d128053a4b08fc7d63a4ef8b02254d868408
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908458"
---
# <span data-ttu-id="2f8b4-101">Remove-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="2f8b4-101">Remove-AzSentinelBookmark</span></span>

## <span data-ttu-id="2f8b4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2f8b4-102">SYNOPSIS</span></span>
<span data-ttu-id="2f8b4-103">刪除書簽。</span><span class="sxs-lookup"><span data-stu-id="2f8b4-103">Delete a Bookmark.</span></span>

## <span data-ttu-id="2f8b4-104">語法</span><span class="sxs-lookup"><span data-stu-id="2f8b4-104">SYNTAX</span></span>

### <span data-ttu-id="2f8b4-105">BookmarkId。</span><span class="sxs-lookup"><span data-stu-id="2f8b4-105">BookmarkId.</span></span> <span data-ttu-id="2f8b4-106"> (預設) </span><span class="sxs-lookup"><span data-stu-id="2f8b4-106">(Default)</span></span>
```
Remove-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f8b4-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="2f8b4-107">InputObject</span></span>
```
Remove-AzSentinelBookmark -InputObject <PSSentinelBookmark> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f8b4-108">描述</span><span class="sxs-lookup"><span data-stu-id="2f8b4-108">DESCRIPTION</span></span>
<span data-ttu-id="2f8b4-109">**Remove-AzSentinelBookmark** Cmdlet 會永久刪除指定工作區中的書簽。</span><span class="sxs-lookup"><span data-stu-id="2f8b4-109">The **Remove-AzSentinelBookmark** cmdlet permanently deletes a Bookmark from a specified workspace.</span></span>
<span data-ttu-id="2f8b4-110">您可以使用管線運算子傳遞 **書簽** 物件，或者您也可以指定所需的參數。</span><span class="sxs-lookup"><span data-stu-id="2f8b4-110">You can pass an **Bookmark** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="2f8b4-111">您可以使用確認參數$ConfirmPreference Windows PowerShell 變數來控制 Cmdlet 是否提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2f8b4-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="2f8b4-112">例子</span><span class="sxs-lookup"><span data-stu-id="2f8b4-112">EXAMPLES</span></span>

### <span data-ttu-id="2f8b4-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="2f8b4-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -BookmarkId "MyBookmarkId"
```

<span data-ttu-id="2f8b4-114">此命令會從工作區移除書簽。</span><span class="sxs-lookup"><span data-stu-id="2f8b4-114">This command removes the Bookmark from the workspace.</span></span>

## <span data-ttu-id="2f8b4-115">參數</span><span class="sxs-lookup"><span data-stu-id="2f8b4-115">PARAMETERS</span></span>

### <span data-ttu-id="2f8b4-116">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="2f8b4-116">-BookmarkId</span></span>
<span data-ttu-id="2f8b4-117">書簽識別碼，</span><span class="sxs-lookup"><span data-stu-id="2f8b4-117">Bookmark Id,</span></span>

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

### <span data-ttu-id="2f8b4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f8b4-118">-DefaultProfile</span></span>
<span data-ttu-id="2f8b4-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2f8b4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f8b4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f8b4-120">-InputObject</span></span>
<span data-ttu-id="2f8b4-121">InputObject。</span><span class="sxs-lookup"><span data-stu-id="2f8b4-121">InputObject.</span></span>

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

### <span data-ttu-id="2f8b4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f8b4-122">-PassThru</span></span>
<span data-ttu-id="2f8b4-123">PassThru</span><span class="sxs-lookup"><span data-stu-id="2f8b4-123">PassThru</span></span>

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

### <span data-ttu-id="2f8b4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f8b4-124">-ResourceGroupName</span></span>
<span data-ttu-id="2f8b4-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="2f8b4-125">Resource group name.</span></span>

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

### <span data-ttu-id="2f8b4-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2f8b4-126">-WorkspaceName</span></span>
<span data-ttu-id="2f8b4-127">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="2f8b4-127">Workspace Name.</span></span>

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

### <span data-ttu-id="2f8b4-128">-確認</span><span class="sxs-lookup"><span data-stu-id="2f8b4-128">-Confirm</span></span>
<span data-ttu-id="2f8b4-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2f8b4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f8b4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f8b4-130">-WhatIf</span></span>
<span data-ttu-id="2f8b4-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2f8b4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f8b4-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2f8b4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f8b4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f8b4-133">CommonParameters</span></span>
<span data-ttu-id="2f8b4-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2f8b4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f8b4-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f8b4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f8b4-136">輸入</span><span class="sxs-lookup"><span data-stu-id="2f8b4-136">INPUTS</span></span>

### <span data-ttu-id="2f8b4-137">System.String</span><span class="sxs-lookup"><span data-stu-id="2f8b4-137">System.String</span></span>
### <span data-ttu-id="2f8b4-138">Microsoft.Azure.Commands.SecurityInsights.models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="2f8b4-138">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="2f8b4-139">輸出</span><span class="sxs-lookup"><span data-stu-id="2f8b4-139">OUTPUTS</span></span>

### <span data-ttu-id="2f8b4-140">Microsoft.Azure.Commands.SecurityInsights.models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="2f8b4-140">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="2f8b4-141">筆記</span><span class="sxs-lookup"><span data-stu-id="2f8b4-141">NOTES</span></span>

## <span data-ttu-id="2f8b4-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="2f8b4-142">RELATED LINKS</span></span>
