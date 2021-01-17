---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelincidentcomment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncidentComment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncidentComment.md
ms.openlocfilehash: d33c126da2a77736871a9ec1f950382168f52bee
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448564"
---
# <span data-ttu-id="fd961-101">Get-AzSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="fd961-101">Get-AzSentinelIncidentComment</span></span>

## <span data-ttu-id="fd961-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fd961-102">SYNOPSIS</span></span>
<span data-ttu-id="fd961-103">取得事件的意見。</span><span class="sxs-lookup"><span data-stu-id="fd961-103">Get an Incident Comment.</span></span>

## <span data-ttu-id="fd961-104">句法</span><span class="sxs-lookup"><span data-stu-id="fd961-104">SYNTAX</span></span>

### <span data-ttu-id="fd961-105">IncidentId (預設) </span><span class="sxs-lookup"><span data-stu-id="fd961-105">IncidentId (Default)</span></span>
```
Get-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd961-106">IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="fd961-106">IncidentCommentId</span></span>
```
Get-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 -IncidentCommentId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd961-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd961-107">ResourceId</span></span>
```
Get-AzSentinelIncidentComment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fd961-108">說明</span><span class="sxs-lookup"><span data-stu-id="fd961-108">DESCRIPTION</span></span>
<span data-ttu-id="fd961-109">**AzSentinelIncidentComment** Cmdlet 會從指定的工作區取得事件批註。</span><span class="sxs-lookup"><span data-stu-id="fd961-109">The **Get-AzSentinelIncidentComment** cmdlet gets a Incident Comment from the specified workspace.</span></span>
<span data-ttu-id="fd961-110">如果您指定 *IncidentCommentId* 和 *IncidentId* 參數，則會傳回單一 **IncidentComment** 物件。</span><span class="sxs-lookup"><span data-stu-id="fd961-110">If you specify the *IncidentCommentId* and *IncidentId* parameters, a single **IncidentComment** object is returned.</span></span>
<span data-ttu-id="fd961-111">如果您沒有指定 *IncidentCommentId* 參數，則會傳回一個陣列，其中包含指定的工作區中指定事件的所有事件注釋。</span><span class="sxs-lookup"><span data-stu-id="fd961-111">If you do not specify the *IncidentCommentId* parameter, an array containing all of the Incident Comments for the specified Incident in the specified workspace are returned.</span></span>

## <span data-ttu-id="fd961-112">示例</span><span class="sxs-lookup"><span data-stu-id="fd961-112">EXAMPLES</span></span>

### <span data-ttu-id="fd961-113">範例1</span><span class="sxs-lookup"><span data-stu-id="fd961-113">Example 1</span></span>
```powershell
PS C:\> $IncidentComments = Get-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="fd961-114">這個範例會在指定的工作區中取得指定事件的所有 **IncidentComments** ，然後將其儲存在 $IncidentComments 變數中。</span><span class="sxs-lookup"><span data-stu-id="fd961-114">This example gets all of the **IncidentComments** for the specified Incident in the specified workspace, and then stores it in the $IncidentComments variable.</span></span>

### <span data-ttu-id="fd961-115">範例2</span><span class="sxs-lookup"><span data-stu-id="fd961-115">Example 2</span></span>
```powershell
PS C:\> $IncidentComment = Get-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId" -IncidentCommentId "MyIncidentCommentId"
```

<span data-ttu-id="fd961-116">這個範例會在指定的工作區中取得指定事件的 **IncidentComment** ，然後將其儲存在 $IncidentComment 變數中。</span><span class="sxs-lookup"><span data-stu-id="fd961-116">This example gets an **IncidentComment** for the specified Incident in the specified workspace, and then stores it in the $IncidentComment variable.</span></span>

## <span data-ttu-id="fd961-117">參數</span><span class="sxs-lookup"><span data-stu-id="fd961-117">PARAMETERS</span></span>

### <span data-ttu-id="fd961-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd961-118">-DefaultProfile</span></span>
<span data-ttu-id="fd961-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fd961-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd961-120">-IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="fd961-120">-IncidentCommentId</span></span>
<span data-ttu-id="fd961-121">事件批註識別碼。</span><span class="sxs-lookup"><span data-stu-id="fd961-121">Incident Comment Id.</span></span>

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

### <span data-ttu-id="fd961-122">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="fd961-122">-IncidentId</span></span>
<span data-ttu-id="fd961-123">事件 Id。</span><span class="sxs-lookup"><span data-stu-id="fd961-123">Incident Id.</span></span>

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

### <span data-ttu-id="fd961-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd961-124">-ResourceGroupName</span></span>
<span data-ttu-id="fd961-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="fd961-125">Resource group name.</span></span>

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

### <span data-ttu-id="fd961-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd961-126">-ResourceId</span></span>
<span data-ttu-id="fd961-127">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="fd961-127">Resource Id.</span></span>

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

### <span data-ttu-id="fd961-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fd961-128">-WorkspaceName</span></span>
<span data-ttu-id="fd961-129">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="fd961-129">Workspace Name.</span></span>

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

### <span data-ttu-id="fd961-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd961-130">CommonParameters</span></span>
<span data-ttu-id="fd961-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fd961-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd961-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fd961-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd961-133">輸入</span><span class="sxs-lookup"><span data-stu-id="fd961-133">INPUTS</span></span>

### <span data-ttu-id="fd961-134">System.object</span><span class="sxs-lookup"><span data-stu-id="fd961-134">System.String</span></span>
## <span data-ttu-id="fd961-135">輸出</span><span class="sxs-lookup"><span data-stu-id="fd961-135">OUTPUTS</span></span>

### <span data-ttu-id="fd961-136">SecurityInsights IncidentComments. PSSentinelIncidentComment （）</span><span class="sxs-lookup"><span data-stu-id="fd961-136">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span></span>
## <span data-ttu-id="fd961-137">筆記</span><span class="sxs-lookup"><span data-stu-id="fd961-137">NOTES</span></span>

## <span data-ttu-id="fd961-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="fd961-138">RELATED LINKS</span></span>
