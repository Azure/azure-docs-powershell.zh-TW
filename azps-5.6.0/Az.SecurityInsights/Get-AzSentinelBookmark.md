---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/get-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelBookmark.md
ms.openlocfilehash: 5093f924f87f146550b13e3858f9a93b3f193ca0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915869"
---
# <span data-ttu-id="9d23b-101">Get-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="9d23b-101">Get-AzSentinelBookmark</span></span>

## <span data-ttu-id="9d23b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9d23b-102">SYNOPSIS</span></span>
<span data-ttu-id="9d23b-103">取得書簽。</span><span class="sxs-lookup"><span data-stu-id="9d23b-103">Get a Bookmark.</span></span>

## <span data-ttu-id="9d23b-104">語法</span><span class="sxs-lookup"><span data-stu-id="9d23b-104">SYNTAX</span></span>

### <span data-ttu-id="9d23b-105">WorkspaceScope (預設) </span><span class="sxs-lookup"><span data-stu-id="9d23b-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d23b-106">BookmarkId。</span><span class="sxs-lookup"><span data-stu-id="9d23b-106">BookmarkId.</span></span>
```
Get-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d23b-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d23b-107">ResourceId</span></span>
```
Get-AzSentinelBookmark -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d23b-108">描述</span><span class="sxs-lookup"><span data-stu-id="9d23b-108">DESCRIPTION</span></span>
<span data-ttu-id="9d23b-109">**Get-AzSentinelBookmark** Cmdlet 會從指定的工作區取得書簽。</span><span class="sxs-lookup"><span data-stu-id="9d23b-109">The **Get-AzSentinelBookmark** cmdlet gets a Bookmark from the specified workspace.</span></span>
<span data-ttu-id="9d23b-110">如果您指定 *BookmarkId* 參數，會返回單 **一書簽** 物件。</span><span class="sxs-lookup"><span data-stu-id="9d23b-110">If you specify the *BookmarkId* parameter, a single **Bookmark** object is returned.</span></span>
<span data-ttu-id="9d23b-111">如果您未指定 *BookmarkId* 參數，會返回包含指定工作區中所有書簽的陣列。</span><span class="sxs-lookup"><span data-stu-id="9d23b-111">If you do not specify the *BookmarkId* parameter, an array containing all of the Bookmarks in the specified workspace are returned.</span></span>
<span data-ttu-id="9d23b-112">您可以使用書簽 **物件** 來更新書簽，例如，您可以新增 **筆記書簽。**</span><span class="sxs-lookup"><span data-stu-id="9d23b-112">You can use the **Bookmark** object to update the Bookmark, for example you can add Notes the **Bookmark**.</span></span>

## <span data-ttu-id="9d23b-113">例子</span><span class="sxs-lookup"><span data-stu-id="9d23b-113">EXAMPLES</span></span>

### <span data-ttu-id="9d23b-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="9d23b-114">Example 1</span></span>
```powershell
PS C:\> $Bookmarks = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="9d23b-115">此範例會獲得指定工作區中所有的書簽，然後將它儲存在 $Bookmarks 變數中。</span><span class="sxs-lookup"><span data-stu-id="9d23b-115">This example gets all of the **Bookmarks** in the specified workspace, and then stores it in the $Bookmarks variable.</span></span>

### <span data-ttu-id="9d23b-116">範例 2</span><span class="sxs-lookup"><span data-stu-id="9d23b-116">Example 2</span></span>
```powershell
PS C:\> $Bookmark = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -BookmarkId "MyBookmarkId"
```

<span data-ttu-id="9d23b-117">此範例 **會獲得指定** 工作區中的書簽，然後將它儲存在$Bookmark變數。</span><span class="sxs-lookup"><span data-stu-id="9d23b-117">This example gets an **Bookmark** in the specified workspace, and then stores it in the $Bookmark variable.</span></span>

## <span data-ttu-id="9d23b-118">參數</span><span class="sxs-lookup"><span data-stu-id="9d23b-118">PARAMETERS</span></span>

### <span data-ttu-id="9d23b-119">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="9d23b-119">-BookmarkId</span></span>
<span data-ttu-id="9d23b-120">書簽識別碼，</span><span class="sxs-lookup"><span data-stu-id="9d23b-120">Bookmark Id,</span></span>

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

### <span data-ttu-id="9d23b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d23b-121">-DefaultProfile</span></span>
<span data-ttu-id="9d23b-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9d23b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d23b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d23b-123">-ResourceGroupName</span></span>
<span data-ttu-id="9d23b-124">資源組名。</span><span class="sxs-lookup"><span data-stu-id="9d23b-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d23b-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d23b-125">-ResourceId</span></span>
<span data-ttu-id="9d23b-126">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="9d23b-126">Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d23b-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9d23b-127">-WorkspaceName</span></span>
<span data-ttu-id="9d23b-128">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="9d23b-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d23b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d23b-129">CommonParameters</span></span>
<span data-ttu-id="9d23b-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9d23b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d23b-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9d23b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d23b-132">輸入</span><span class="sxs-lookup"><span data-stu-id="9d23b-132">INPUTS</span></span>

### <span data-ttu-id="9d23b-133">System.String</span><span class="sxs-lookup"><span data-stu-id="9d23b-133">System.String</span></span>
## <span data-ttu-id="9d23b-134">輸出</span><span class="sxs-lookup"><span data-stu-id="9d23b-134">OUTPUTS</span></span>

### <span data-ttu-id="9d23b-135">Microsoft.Azure.Commands.SecurityInsights.models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="9d23b-135">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="9d23b-136">筆記</span><span class="sxs-lookup"><span data-stu-id="9d23b-136">NOTES</span></span>

## <span data-ttu-id="9d23b-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="9d23b-137">RELATED LINKS</span></span>
