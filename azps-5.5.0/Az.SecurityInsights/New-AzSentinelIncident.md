---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncident.md
ms.openlocfilehash: b3618f178ea5dee54991c037da78ac51f2ed4502
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100139878"
---
# <span data-ttu-id="e9ba0-101">New-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="e9ba0-101">New-AzSentinelIncident</span></span>

## <span data-ttu-id="e9ba0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e9ba0-102">SYNOPSIS</span></span>
<span data-ttu-id="e9ba0-103">建立事件。</span><span class="sxs-lookup"><span data-stu-id="e9ba0-103">Create an Incident.</span></span>

## <span data-ttu-id="e9ba0-104">句法</span><span class="sxs-lookup"><span data-stu-id="e9ba0-104">SYNTAX</span></span>

```
New-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> [-IncidentId <String>]
 [-Classificaton <String>] [-ClassificationComment <String>] [-ClassificationReason <String>]
 [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9ba0-105">說明</span><span class="sxs-lookup"><span data-stu-id="e9ba0-105">DESCRIPTION</span></span>
<span data-ttu-id="e9ba0-106">**新的-AzSentinelIncident** Cmdlet 會從指定的工作區建立事件。</span><span class="sxs-lookup"><span data-stu-id="e9ba0-106">The **New-AzSentinelIncident** cmdlet creates a Incident from the specified workspace.</span></span>
<span data-ttu-id="e9ba0-107">您可以使用 *Confirm* 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e9ba0-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="e9ba0-108">示例</span><span class="sxs-lookup"><span data-stu-id="e9ba0-108">EXAMPLES</span></span>

### <span data-ttu-id="e9ba0-109">範例1</span><span class="sxs-lookup"><span data-stu-id="e9ba0-109">Example 1</span></span>
```powershell
PS C:\> $Incident = New-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Title "NewIncident" -Severity Low -Status New
```

<span data-ttu-id="e9ba0-110">這個範例會在指定的工作區中建立一個 **事件** ，然後將它儲存在 $Incident 變數中。</span><span class="sxs-lookup"><span data-stu-id="e9ba0-110">This example creates an **Incident** in the specified workspace, and then stores it in the $Incident variable.</span></span>

## <span data-ttu-id="e9ba0-111">參數</span><span class="sxs-lookup"><span data-stu-id="e9ba0-111">PARAMETERS</span></span>

### <span data-ttu-id="e9ba0-112">-ClassificationComment</span><span class="sxs-lookup"><span data-stu-id="e9ba0-112">-ClassificationComment</span></span>
<span data-ttu-id="e9ba0-113">事件 Classificaiton 批註。</span><span class="sxs-lookup"><span data-stu-id="e9ba0-113">Incident Classificaiton Comment.</span></span>

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

### <span data-ttu-id="e9ba0-114">-ClassificationReason</span><span class="sxs-lookup"><span data-stu-id="e9ba0-114">-ClassificationReason</span></span>
<span data-ttu-id="e9ba0-115">事件 Classificaiton 原因。</span><span class="sxs-lookup"><span data-stu-id="e9ba0-115">Incident Classificaiton Reason.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: InaccurateData, IncorrectAlertLogic, SuspiciousActivity, SuspiciousButExpected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9ba0-116">-Classificaton</span><span class="sxs-lookup"><span data-stu-id="e9ba0-116">-Classificaton</span></span>
<span data-ttu-id="e9ba0-117">事件 Classificaiton。</span><span class="sxs-lookup"><span data-stu-id="e9ba0-117">Incident Classificaiton.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: BenignPositive, FalsePositive, TruePositive, Undetermined

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9ba0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9ba0-118">-DefaultProfile</span></span>
<span data-ttu-id="e9ba0-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e9ba0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9ba0-120">-描述</span><span class="sxs-lookup"><span data-stu-id="e9ba0-120">-Description</span></span>
<span data-ttu-id="e9ba0-121">說明.</span><span class="sxs-lookup"><span data-stu-id="e9ba0-121">Description.</span></span>

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

### <span data-ttu-id="e9ba0-122">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="e9ba0-122">-IncidentId</span></span>
<span data-ttu-id="e9ba0-123">事件 Id。</span><span class="sxs-lookup"><span data-stu-id="e9ba0-123">Incident Id.</span></span>

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

### <span data-ttu-id="e9ba0-124">-標籤</span><span class="sxs-lookup"><span data-stu-id="e9ba0-124">-Label</span></span>
<span data-ttu-id="e9ba0-125">事件標籤。</span><span class="sxs-lookup"><span data-stu-id="e9ba0-125">Incident Labels.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9ba0-126">-擁有者</span><span class="sxs-lookup"><span data-stu-id="e9ba0-126">-Owner</span></span>
<span data-ttu-id="e9ba0-127">事件擁有者。</span><span class="sxs-lookup"><span data-stu-id="e9ba0-127">Incident Owner.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9ba0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9ba0-128">-ResourceGroupName</span></span>
<span data-ttu-id="e9ba0-129">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="e9ba0-129">Resource group name.</span></span>

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

### <span data-ttu-id="e9ba0-130">-嚴重度</span><span class="sxs-lookup"><span data-stu-id="e9ba0-130">-Severity</span></span>
<span data-ttu-id="e9ba0-131">事件嚴重度。</span><span class="sxs-lookup"><span data-stu-id="e9ba0-131">Incident Severity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: High, Informational, Low, Medium

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9ba0-132">-狀態</span><span class="sxs-lookup"><span data-stu-id="e9ba0-132">-Status</span></span>
<span data-ttu-id="e9ba0-133">事件狀態。</span><span class="sxs-lookup"><span data-stu-id="e9ba0-133">Incident Status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Active, Closed, New

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9ba0-134">-標題</span><span class="sxs-lookup"><span data-stu-id="e9ba0-134">-Title</span></span>
<span data-ttu-id="e9ba0-135">事件標題。</span><span class="sxs-lookup"><span data-stu-id="e9ba0-135">Incident Title.</span></span>

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

### <span data-ttu-id="e9ba0-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e9ba0-136">-WorkspaceName</span></span>
<span data-ttu-id="e9ba0-137">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="e9ba0-137">Workspace Name.</span></span>

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

### <span data-ttu-id="e9ba0-138">-確認</span><span class="sxs-lookup"><span data-stu-id="e9ba0-138">-Confirm</span></span>
<span data-ttu-id="e9ba0-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e9ba0-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9ba0-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9ba0-140">-WhatIf</span></span>
<span data-ttu-id="e9ba0-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e9ba0-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e9ba0-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e9ba0-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9ba0-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9ba0-143">CommonParameters</span></span>
<span data-ttu-id="e9ba0-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e9ba0-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9ba0-145">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e9ba0-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9ba0-146">輸入</span><span class="sxs-lookup"><span data-stu-id="e9ba0-146">INPUTS</span></span>

### <span data-ttu-id="e9ba0-147">[System.object]. IList "1 [PSSentinelIncidentLabel，SecurityInsights，SecurityInsights = 0.1.0.0，Culture = 中性，PublicKeyToken = null]] （" 區域性 = null）]]）。</span><span class="sxs-lookup"><span data-stu-id="e9ba0-147">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
### <span data-ttu-id="e9ba0-148">PSSentinelIncidentOwner （SecurityInsights）的命令。</span><span class="sxs-lookup"><span data-stu-id="e9ba0-148">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span></span>
## <span data-ttu-id="e9ba0-149">輸出</span><span class="sxs-lookup"><span data-stu-id="e9ba0-149">OUTPUTS</span></span>

### <span data-ttu-id="e9ba0-150">PSSentinelIncident （SecurityInsights）的命令。</span><span class="sxs-lookup"><span data-stu-id="e9ba0-150">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="e9ba0-151">筆記</span><span class="sxs-lookup"><span data-stu-id="e9ba0-151">NOTES</span></span>

## <span data-ttu-id="e9ba0-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="e9ba0-152">RELATED LINKS</span></span>
