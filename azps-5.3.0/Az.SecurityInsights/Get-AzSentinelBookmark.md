---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelBookmark.md
ms.openlocfilehash: 53dfedcfe4e61deb5064b20134bf063921532aec
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448572"
---
# <span data-ttu-id="c29df-101">Get-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="c29df-101">Get-AzSentinelBookmark</span></span>

## <span data-ttu-id="c29df-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c29df-102">SYNOPSIS</span></span>
<span data-ttu-id="c29df-103">[取得書簽]。</span><span class="sxs-lookup"><span data-stu-id="c29df-103">Get a Bookmark.</span></span>

## <span data-ttu-id="c29df-104">句法</span><span class="sxs-lookup"><span data-stu-id="c29df-104">SYNTAX</span></span>

### <span data-ttu-id="c29df-105">WorkspaceScope (預設) </span><span class="sxs-lookup"><span data-stu-id="c29df-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c29df-106">BookmarkId.</span><span class="sxs-lookup"><span data-stu-id="c29df-106">BookmarkId.</span></span>
```
Get-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c29df-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c29df-107">ResourceId</span></span>
```
Get-AzSentinelBookmark -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c29df-108">說明</span><span class="sxs-lookup"><span data-stu-id="c29df-108">DESCRIPTION</span></span>
<span data-ttu-id="c29df-109">**AzSentinelBookmark** Cmdlet 會從指定的工作區取得書簽。</span><span class="sxs-lookup"><span data-stu-id="c29df-109">The **Get-AzSentinelBookmark** cmdlet gets a Bookmark from the specified workspace.</span></span>
<span data-ttu-id="c29df-110">如果您指定 *BookmarkId* 參數，則會傳回單一 **書簽** 物件。</span><span class="sxs-lookup"><span data-stu-id="c29df-110">If you specify the *BookmarkId* parameter, a single **Bookmark** object is returned.</span></span>
<span data-ttu-id="c29df-111">如果您沒有指定 *BookmarkId* 參數，則會傳回包含指定工作區中所有書簽的陣列。</span><span class="sxs-lookup"><span data-stu-id="c29df-111">If you do not specify the *BookmarkId* parameter, an array containing all of the Bookmarks in the specified workspace are returned.</span></span>
<span data-ttu-id="c29df-112">您可以使用 **bookmark** 物件來更新書簽，例如，您可以在 **書簽** 中新增記事。</span><span class="sxs-lookup"><span data-stu-id="c29df-112">You can use the **Bookmark** object to update the Bookmark, for example you can add Notes the **Bookmark**.</span></span>

## <span data-ttu-id="c29df-113">示例</span><span class="sxs-lookup"><span data-stu-id="c29df-113">EXAMPLES</span></span>

### <span data-ttu-id="c29df-114">範例1</span><span class="sxs-lookup"><span data-stu-id="c29df-114">Example 1</span></span>
```powershell
PS C:\> $Bookmarks = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="c29df-115">這個範例會取得指定工作區中的所有 **書簽** ，然後將它儲存在 $Bookmarks 變數中。</span><span class="sxs-lookup"><span data-stu-id="c29df-115">This example gets all of the **Bookmarks** in the specified workspace, and then stores it in the $Bookmarks variable.</span></span>

### <span data-ttu-id="c29df-116">範例2</span><span class="sxs-lookup"><span data-stu-id="c29df-116">Example 2</span></span>
```powershell
PS C:\> $Bookmark = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -BookmarkId "MyBookmarkId"
```

<span data-ttu-id="c29df-117">這個範例會在指定的工作區中取得 **書簽** ，然後將它儲存在 $Bookmark 變數中。</span><span class="sxs-lookup"><span data-stu-id="c29df-117">This example gets an **Bookmark** in the specified workspace, and then stores it in the $Bookmark variable.</span></span>

## <span data-ttu-id="c29df-118">參數</span><span class="sxs-lookup"><span data-stu-id="c29df-118">PARAMETERS</span></span>

### <span data-ttu-id="c29df-119">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="c29df-119">-BookmarkId</span></span>
<span data-ttu-id="c29df-120">書簽識別碼，</span><span class="sxs-lookup"><span data-stu-id="c29df-120">Bookmark Id,</span></span>

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

### <span data-ttu-id="c29df-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c29df-121">-DefaultProfile</span></span>
<span data-ttu-id="c29df-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c29df-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c29df-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c29df-123">-ResourceGroupName</span></span>
<span data-ttu-id="c29df-124">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="c29df-124">Resource group name.</span></span>

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

### <span data-ttu-id="c29df-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c29df-125">-ResourceId</span></span>
<span data-ttu-id="c29df-126">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="c29df-126">Resource Id.</span></span>

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

### <span data-ttu-id="c29df-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c29df-127">-WorkspaceName</span></span>
<span data-ttu-id="c29df-128">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="c29df-128">Workspace Name.</span></span>

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

### <span data-ttu-id="c29df-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c29df-129">CommonParameters</span></span>
<span data-ttu-id="c29df-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c29df-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c29df-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c29df-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c29df-132">輸入</span><span class="sxs-lookup"><span data-stu-id="c29df-132">INPUTS</span></span>

### <span data-ttu-id="c29df-133">System.object</span><span class="sxs-lookup"><span data-stu-id="c29df-133">System.String</span></span>
## <span data-ttu-id="c29df-134">輸出</span><span class="sxs-lookup"><span data-stu-id="c29df-134">OUTPUTS</span></span>

### <span data-ttu-id="c29df-135">PSSentinelBookmark （SecurityInsights.）。</span><span class="sxs-lookup"><span data-stu-id="c29df-135">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="c29df-136">筆記</span><span class="sxs-lookup"><span data-stu-id="c29df-136">NOTES</span></span>

## <span data-ttu-id="c29df-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="c29df-137">RELATED LINKS</span></span>
