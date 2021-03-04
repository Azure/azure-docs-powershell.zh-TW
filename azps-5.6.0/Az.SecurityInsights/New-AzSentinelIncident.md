---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/new-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncident.md
ms.openlocfilehash: 6cb65832484c7038f5740c481836d8fe889ebc94
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915866"
---
# <span data-ttu-id="9decf-101">New-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="9decf-101">New-AzSentinelIncident</span></span>

## <span data-ttu-id="9decf-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9decf-102">SYNOPSIS</span></span>
<span data-ttu-id="9decf-103">建立事件。</span><span class="sxs-lookup"><span data-stu-id="9decf-103">Create an Incident.</span></span>

## <span data-ttu-id="9decf-104">語法</span><span class="sxs-lookup"><span data-stu-id="9decf-104">SYNTAX</span></span>

```
New-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> [-IncidentId <String>]
 [-Classificaton <String>] [-ClassificationComment <String>] [-ClassificationReason <String>]
 [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9decf-105">描述</span><span class="sxs-lookup"><span data-stu-id="9decf-105">DESCRIPTION</span></span>
<span data-ttu-id="9decf-106">**New-AzSentinelIncident** Cmdlet 會從指定的工作區建立事件。</span><span class="sxs-lookup"><span data-stu-id="9decf-106">The **New-AzSentinelIncident** cmdlet creates a Incident from the specified workspace.</span></span>
<span data-ttu-id="9decf-107">您可以使用確認 *參數$ConfirmPreference* Windows PowerShell 變數來控制 Cmdlet 是否提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9decf-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="9decf-108">例子</span><span class="sxs-lookup"><span data-stu-id="9decf-108">EXAMPLES</span></span>

### <span data-ttu-id="9decf-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="9decf-109">Example 1</span></span>
```powershell
PS C:\> $Incident = New-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Title "NewIncident" -Severity Low -Status New
```

<span data-ttu-id="9decf-110">此範例會于指定的 **工作區中建立** 事件，然後將它儲存在$Incident變數中。</span><span class="sxs-lookup"><span data-stu-id="9decf-110">This example creates an **Incident** in the specified workspace, and then stores it in the $Incident variable.</span></span>

## <span data-ttu-id="9decf-111">參數</span><span class="sxs-lookup"><span data-stu-id="9decf-111">PARAMETERS</span></span>

### <span data-ttu-id="9decf-112">-ClassificationComment</span><span class="sxs-lookup"><span data-stu-id="9decf-112">-ClassificationComment</span></span>
<span data-ttu-id="9decf-113">事件類別批註。</span><span class="sxs-lookup"><span data-stu-id="9decf-113">Incident Classificaiton Comment.</span></span>

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

### <span data-ttu-id="9decf-114">-ClassificationReason</span><span class="sxs-lookup"><span data-stu-id="9decf-114">-ClassificationReason</span></span>
<span data-ttu-id="9decf-115">Incident Classificaiton 原因。</span><span class="sxs-lookup"><span data-stu-id="9decf-115">Incident Classificaiton Reason.</span></span>

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

### <span data-ttu-id="9decf-116">-Classificaton</span><span class="sxs-lookup"><span data-stu-id="9decf-116">-Classificaton</span></span>
<span data-ttu-id="9decf-117">Incident Classificaiton.</span><span class="sxs-lookup"><span data-stu-id="9decf-117">Incident Classificaiton.</span></span>

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

### <span data-ttu-id="9decf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9decf-118">-DefaultProfile</span></span>
<span data-ttu-id="9decf-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9decf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9decf-120">-描述</span><span class="sxs-lookup"><span data-stu-id="9decf-120">-Description</span></span>
<span data-ttu-id="9decf-121">描述。</span><span class="sxs-lookup"><span data-stu-id="9decf-121">Description.</span></span>

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

### <span data-ttu-id="9decf-122">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="9decf-122">-IncidentId</span></span>
<span data-ttu-id="9decf-123">事件識別碼。</span><span class="sxs-lookup"><span data-stu-id="9decf-123">Incident Id.</span></span>

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

### <span data-ttu-id="9decf-124">-標籤</span><span class="sxs-lookup"><span data-stu-id="9decf-124">-Label</span></span>
<span data-ttu-id="9decf-125">事件標籤。</span><span class="sxs-lookup"><span data-stu-id="9decf-125">Incident Labels.</span></span>

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

### <span data-ttu-id="9decf-126">-擁有者</span><span class="sxs-lookup"><span data-stu-id="9decf-126">-Owner</span></span>
<span data-ttu-id="9decf-127">事件擁有者。</span><span class="sxs-lookup"><span data-stu-id="9decf-127">Incident Owner.</span></span>

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

### <span data-ttu-id="9decf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9decf-128">-ResourceGroupName</span></span>
<span data-ttu-id="9decf-129">資源組名。</span><span class="sxs-lookup"><span data-stu-id="9decf-129">Resource group name.</span></span>

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

### <span data-ttu-id="9decf-130">-嚴重性</span><span class="sxs-lookup"><span data-stu-id="9decf-130">-Severity</span></span>
<span data-ttu-id="9decf-131">事件嚴重性。</span><span class="sxs-lookup"><span data-stu-id="9decf-131">Incident Severity.</span></span>

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

### <span data-ttu-id="9decf-132">-狀態</span><span class="sxs-lookup"><span data-stu-id="9decf-132">-Status</span></span>
<span data-ttu-id="9decf-133">事件狀態。</span><span class="sxs-lookup"><span data-stu-id="9decf-133">Incident Status.</span></span>

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

### <span data-ttu-id="9decf-134">-標題</span><span class="sxs-lookup"><span data-stu-id="9decf-134">-Title</span></span>
<span data-ttu-id="9decf-135">事件標題。</span><span class="sxs-lookup"><span data-stu-id="9decf-135">Incident Title.</span></span>

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

### <span data-ttu-id="9decf-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9decf-136">-WorkspaceName</span></span>
<span data-ttu-id="9decf-137">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="9decf-137">Workspace Name.</span></span>

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

### <span data-ttu-id="9decf-138">-確認</span><span class="sxs-lookup"><span data-stu-id="9decf-138">-Confirm</span></span>
<span data-ttu-id="9decf-139">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9decf-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9decf-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9decf-140">-WhatIf</span></span>
<span data-ttu-id="9decf-141">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9decf-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9decf-142">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9decf-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9decf-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9decf-143">CommonParameters</span></span>
<span data-ttu-id="9decf-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9decf-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9decf-145">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9decf-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9decf-146">輸入</span><span class="sxs-lookup"><span data-stu-id="9decf-146">INPUTS</span></span>

### <span data-ttu-id="9decf-147">System.Collections.Generic.IList'1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="9decf-147">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
### <span data-ttu-id="9decf-148">Microsoft.Azure.Commands.SecurityInsights.models.Incidents.PSSentinelIncidentOwner</span><span class="sxs-lookup"><span data-stu-id="9decf-148">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span></span>
## <span data-ttu-id="9decf-149">輸出</span><span class="sxs-lookup"><span data-stu-id="9decf-149">OUTPUTS</span></span>

### <span data-ttu-id="9decf-150">Microsoft.Azure.Commands.SecurityInsights.models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="9decf-150">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="9decf-151">筆記</span><span class="sxs-lookup"><span data-stu-id="9decf-151">NOTES</span></span>

## <span data-ttu-id="9decf-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="9decf-152">RELATED LINKS</span></span>
