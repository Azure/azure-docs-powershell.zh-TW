---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/new-azsentinelincidentcomment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentComment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentComment.md
ms.openlocfilehash: 0fe04e773e02a8b6b61f9c57d8316ac8936f05aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904841"
---
# <span data-ttu-id="7d34e-101">New-AzSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="7d34e-101">New-AzSentinelIncidentComment</span></span>

## <span data-ttu-id="7d34e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7d34e-102">SYNOPSIS</span></span>
<span data-ttu-id="7d34e-103">新增事件批註至事件。</span><span class="sxs-lookup"><span data-stu-id="7d34e-103">Add an Incident Comment to an Incident.</span></span>

## <span data-ttu-id="7d34e-104">語法</span><span class="sxs-lookup"><span data-stu-id="7d34e-104">SYNTAX</span></span>

```
New-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 [-IncidentCommentId <String>] -Message <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d34e-105">描述</span><span class="sxs-lookup"><span data-stu-id="7d34e-105">DESCRIPTION</span></span>
<span data-ttu-id="7d34e-106">**New-AzSentinelIncidentComdlet** 會從指定的工作區建立事件批註。</span><span class="sxs-lookup"><span data-stu-id="7d34e-106">The **New-AzSentinelIncidentComment** cmdlet creates a Incident Comment from the specified workspace.</span></span>
<span data-ttu-id="7d34e-107">您可以使用確認 *參數$ConfirmPreference* Windows PowerShell 變數來控制 Cmdlet 是否提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7d34e-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="7d34e-108">例子</span><span class="sxs-lookup"><span data-stu-id="7d34e-108">EXAMPLES</span></span>

### <span data-ttu-id="7d34e-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="7d34e-109">Example 1</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
PS C:\> $IncidentComment = New-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId ($Incident.Name) -Message "Still needs investigation"
```

<span data-ttu-id="7d34e-110">此範例會于指定的工作區 **中建立一個 IncidentComment，** 然後將它儲存在$IncidentComment變數中。</span><span class="sxs-lookup"><span data-stu-id="7d34e-110">This example creates an **IncidentComment** in the specified workspace, and then stores it in the $IncidentComment variable.</span></span>

## <span data-ttu-id="7d34e-111">參數</span><span class="sxs-lookup"><span data-stu-id="7d34e-111">PARAMETERS</span></span>

### <span data-ttu-id="7d34e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d34e-112">-DefaultProfile</span></span>
<span data-ttu-id="7d34e-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7d34e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d34e-114">-IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="7d34e-114">-IncidentCommentId</span></span>
<span data-ttu-id="7d34e-115">事件批註識別碼。</span><span class="sxs-lookup"><span data-stu-id="7d34e-115">Incident Comment Id.</span></span>

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

### <span data-ttu-id="7d34e-116">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="7d34e-116">-IncidentId</span></span>
<span data-ttu-id="7d34e-117">事件識別碼。</span><span class="sxs-lookup"><span data-stu-id="7d34e-117">Incident Id.</span></span>

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

### <span data-ttu-id="7d34e-118">-訊息</span><span class="sxs-lookup"><span data-stu-id="7d34e-118">-Message</span></span>
<span data-ttu-id="7d34e-119">事件訊息。</span><span class="sxs-lookup"><span data-stu-id="7d34e-119">Incident Message.</span></span>

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

### <span data-ttu-id="7d34e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d34e-120">-ResourceGroupName</span></span>
<span data-ttu-id="7d34e-121">資源組名。</span><span class="sxs-lookup"><span data-stu-id="7d34e-121">Resource group name.</span></span>

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

### <span data-ttu-id="7d34e-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7d34e-122">-WorkspaceName</span></span>
<span data-ttu-id="7d34e-123">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="7d34e-123">Workspace Name.</span></span>

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

### <span data-ttu-id="7d34e-124">-確認</span><span class="sxs-lookup"><span data-stu-id="7d34e-124">-Confirm</span></span>
<span data-ttu-id="7d34e-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7d34e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d34e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d34e-126">-WhatIf</span></span>
<span data-ttu-id="7d34e-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7d34e-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7d34e-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7d34e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d34e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d34e-129">CommonParameters</span></span>
<span data-ttu-id="7d34e-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7d34e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d34e-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7d34e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d34e-132">輸入</span><span class="sxs-lookup"><span data-stu-id="7d34e-132">INPUTS</span></span>

### <span data-ttu-id="7d34e-133">沒有</span><span class="sxs-lookup"><span data-stu-id="7d34e-133">None</span></span>
## <span data-ttu-id="7d34e-134">輸出</span><span class="sxs-lookup"><span data-stu-id="7d34e-134">OUTPUTS</span></span>

### <span data-ttu-id="7d34e-135">Microsoft.Azure.Commands.SecurityInsights.models.IncidentComments.PSSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="7d34e-135">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span></span>
## <span data-ttu-id="7d34e-136">筆記</span><span class="sxs-lookup"><span data-stu-id="7d34e-136">NOTES</span></span>

## <span data-ttu-id="7d34e-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d34e-137">RELATED LINKS</span></span>
