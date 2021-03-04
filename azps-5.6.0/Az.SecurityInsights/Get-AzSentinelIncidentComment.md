---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/get-azsentinelincidentcomment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncidentComment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncidentComment.md
ms.openlocfilehash: b25e99766c4dc0433b14810352968300fd5bd129
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910597"
---
# <span data-ttu-id="d259a-101">Get-AzSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="d259a-101">Get-AzSentinelIncidentComment</span></span>

## <span data-ttu-id="d259a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d259a-102">SYNOPSIS</span></span>
<span data-ttu-id="d259a-103">取得事件批註。</span><span class="sxs-lookup"><span data-stu-id="d259a-103">Get an Incident Comment.</span></span>

## <span data-ttu-id="d259a-104">語法</span><span class="sxs-lookup"><span data-stu-id="d259a-104">SYNTAX</span></span>

### <span data-ttu-id="d259a-105">IncidentId (預設) </span><span class="sxs-lookup"><span data-stu-id="d259a-105">IncidentId (Default)</span></span>
```
Get-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d259a-106">IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="d259a-106">IncidentCommentId</span></span>
```
Get-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 -IncidentCommentId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d259a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d259a-107">ResourceId</span></span>
```
Get-AzSentinelIncidentComment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d259a-108">描述</span><span class="sxs-lookup"><span data-stu-id="d259a-108">DESCRIPTION</span></span>
<span data-ttu-id="d259a-109">**Get-AzSentinelIncidentComdlet** 會從指定的工作區取得事件批註。</span><span class="sxs-lookup"><span data-stu-id="d259a-109">The **Get-AzSentinelIncidentComment** cmdlet gets a Incident Comment from the specified workspace.</span></span>
<span data-ttu-id="d259a-110">如果您指定 *IncidentCommentId* 和 *IncidentId* 參數，則會返回 **單一 IncidentComment** 物件。</span><span class="sxs-lookup"><span data-stu-id="d259a-110">If you specify the *IncidentCommentId* and *IncidentId* parameters, a single **IncidentComment** object is returned.</span></span>
<span data-ttu-id="d259a-111">如果您未指定 *IncidentCommentId* 參數，會針對指定工作區中指定之事件，會包含所有事件批註的陣列。</span><span class="sxs-lookup"><span data-stu-id="d259a-111">If you do not specify the *IncidentCommentId* parameter, an array containing all of the Incident Comments for the specified Incident in the specified workspace are returned.</span></span>

## <span data-ttu-id="d259a-112">例子</span><span class="sxs-lookup"><span data-stu-id="d259a-112">EXAMPLES</span></span>

### <span data-ttu-id="d259a-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="d259a-113">Example 1</span></span>
```powershell
PS C:\> $IncidentComments = Get-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="d259a-114">此範例會獲得指定工作區中指定事件的所有 **IncidentComment，** 然後將它儲存在$IncidentComments變數。</span><span class="sxs-lookup"><span data-stu-id="d259a-114">This example gets all of the **IncidentComments** for the specified Incident in the specified workspace, and then stores it in the $IncidentComments variable.</span></span>

### <span data-ttu-id="d259a-115">範例 2</span><span class="sxs-lookup"><span data-stu-id="d259a-115">Example 2</span></span>
```powershell
PS C:\> $IncidentComment = Get-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId" -IncidentCommentId "MyIncidentCommentId"
```

<span data-ttu-id="d259a-116">此範例會針對指定工作區中指定的事件獲得一個 **IncidentComment，** 然後將它儲存在$IncidentComment變數中。</span><span class="sxs-lookup"><span data-stu-id="d259a-116">This example gets an **IncidentComment** for the specified Incident in the specified workspace, and then stores it in the $IncidentComment variable.</span></span>

## <span data-ttu-id="d259a-117">參數</span><span class="sxs-lookup"><span data-stu-id="d259a-117">PARAMETERS</span></span>

### <span data-ttu-id="d259a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d259a-118">-DefaultProfile</span></span>
<span data-ttu-id="d259a-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d259a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d259a-120">-IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="d259a-120">-IncidentCommentId</span></span>
<span data-ttu-id="d259a-121">事件批註識別碼。</span><span class="sxs-lookup"><span data-stu-id="d259a-121">Incident Comment Id.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentCommentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d259a-122">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="d259a-122">-IncidentId</span></span>
<span data-ttu-id="d259a-123">事件識別碼。</span><span class="sxs-lookup"><span data-stu-id="d259a-123">Incident Id.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId, IncidentCommentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d259a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d259a-124">-ResourceGroupName</span></span>
<span data-ttu-id="d259a-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="d259a-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId, IncidentCommentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d259a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d259a-126">-ResourceId</span></span>
<span data-ttu-id="d259a-127">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d259a-127">Resource Id.</span></span>

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

### <span data-ttu-id="d259a-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d259a-128">-WorkspaceName</span></span>
<span data-ttu-id="d259a-129">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="d259a-129">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId, IncidentCommentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d259a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d259a-130">CommonParameters</span></span>
<span data-ttu-id="d259a-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d259a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d259a-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d259a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d259a-133">輸入</span><span class="sxs-lookup"><span data-stu-id="d259a-133">INPUTS</span></span>

### <span data-ttu-id="d259a-134">System.String</span><span class="sxs-lookup"><span data-stu-id="d259a-134">System.String</span></span>
## <span data-ttu-id="d259a-135">輸出</span><span class="sxs-lookup"><span data-stu-id="d259a-135">OUTPUTS</span></span>

### <span data-ttu-id="d259a-136">Microsoft.Azure.Commands.SecurityInsights.models.IncidentComments.PSSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="d259a-136">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span></span>
## <span data-ttu-id="d259a-137">筆記</span><span class="sxs-lookup"><span data-stu-id="d259a-137">NOTES</span></span>

## <span data-ttu-id="d259a-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="d259a-138">RELATED LINKS</span></span>
