---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelincidentcomment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentComment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentComment.md
ms.openlocfilehash: 8824832b1b3d09a24998891ad4636e3a3e0f1e19
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448536"
---
# <span data-ttu-id="6f2da-101">New-AzSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="6f2da-101">New-AzSentinelIncidentComment</span></span>

## <span data-ttu-id="6f2da-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6f2da-102">SYNOPSIS</span></span>
<span data-ttu-id="6f2da-103">在事件中加入事件的意見。</span><span class="sxs-lookup"><span data-stu-id="6f2da-103">Add an Incident Comment to an Incident.</span></span>

## <span data-ttu-id="6f2da-104">句法</span><span class="sxs-lookup"><span data-stu-id="6f2da-104">SYNTAX</span></span>

```
New-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 [-IncidentCommentId <String>] -Message <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f2da-105">說明</span><span class="sxs-lookup"><span data-stu-id="6f2da-105">DESCRIPTION</span></span>
<span data-ttu-id="6f2da-106">**新的-AzSentinelIncidentComment** Cmdlet 會從指定的工作區建立事件批註。</span><span class="sxs-lookup"><span data-stu-id="6f2da-106">The **New-AzSentinelIncidentComment** cmdlet creates a Incident Comment from the specified workspace.</span></span>
<span data-ttu-id="6f2da-107">您可以使用 *Confirm* 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6f2da-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="6f2da-108">示例</span><span class="sxs-lookup"><span data-stu-id="6f2da-108">EXAMPLES</span></span>

### <span data-ttu-id="6f2da-109">範例1</span><span class="sxs-lookup"><span data-stu-id="6f2da-109">Example 1</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
PS C:\> $IncidentComment = New-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId ($Incident.Name) -Message "Still needs investigation"
```

<span data-ttu-id="6f2da-110">這個範例會在指定的工作區中建立 **IncidentComment** ，然後將其儲存在 $IncidentComment 變數中。</span><span class="sxs-lookup"><span data-stu-id="6f2da-110">This example creates an **IncidentComment** in the specified workspace, and then stores it in the $IncidentComment variable.</span></span>

## <span data-ttu-id="6f2da-111">參數</span><span class="sxs-lookup"><span data-stu-id="6f2da-111">PARAMETERS</span></span>

### <span data-ttu-id="6f2da-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f2da-112">-DefaultProfile</span></span>
<span data-ttu-id="6f2da-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6f2da-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f2da-114">-IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="6f2da-114">-IncidentCommentId</span></span>
<span data-ttu-id="6f2da-115">事件批註識別碼。</span><span class="sxs-lookup"><span data-stu-id="6f2da-115">Incident Comment Id.</span></span>

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

### <span data-ttu-id="6f2da-116">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="6f2da-116">-IncidentId</span></span>
<span data-ttu-id="6f2da-117">事件 Id。</span><span class="sxs-lookup"><span data-stu-id="6f2da-117">Incident Id.</span></span>

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

### <span data-ttu-id="6f2da-118">-訊息</span><span class="sxs-lookup"><span data-stu-id="6f2da-118">-Message</span></span>
<span data-ttu-id="6f2da-119">事件訊息。</span><span class="sxs-lookup"><span data-stu-id="6f2da-119">Incident Message.</span></span>

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

### <span data-ttu-id="6f2da-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f2da-120">-ResourceGroupName</span></span>
<span data-ttu-id="6f2da-121">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="6f2da-121">Resource group name.</span></span>

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

### <span data-ttu-id="6f2da-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6f2da-122">-WorkspaceName</span></span>
<span data-ttu-id="6f2da-123">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="6f2da-123">Workspace Name.</span></span>

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

### <span data-ttu-id="6f2da-124">-確認</span><span class="sxs-lookup"><span data-stu-id="6f2da-124">-Confirm</span></span>
<span data-ttu-id="6f2da-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6f2da-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f2da-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f2da-126">-WhatIf</span></span>
<span data-ttu-id="6f2da-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6f2da-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6f2da-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6f2da-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f2da-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f2da-129">CommonParameters</span></span>
<span data-ttu-id="6f2da-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6f2da-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f2da-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6f2da-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f2da-132">輸入</span><span class="sxs-lookup"><span data-stu-id="6f2da-132">INPUTS</span></span>

### <span data-ttu-id="6f2da-133">所有</span><span class="sxs-lookup"><span data-stu-id="6f2da-133">None</span></span>
## <span data-ttu-id="6f2da-134">輸出</span><span class="sxs-lookup"><span data-stu-id="6f2da-134">OUTPUTS</span></span>

### <span data-ttu-id="6f2da-135">SecurityInsights IncidentComments. PSSentinelIncidentComment （）</span><span class="sxs-lookup"><span data-stu-id="6f2da-135">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span></span>
## <span data-ttu-id="6f2da-136">筆記</span><span class="sxs-lookup"><span data-stu-id="6f2da-136">NOTES</span></span>

## <span data-ttu-id="6f2da-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="6f2da-137">RELATED LINKS</span></span>
