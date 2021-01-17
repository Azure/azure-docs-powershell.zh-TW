---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelIncident.md
ms.openlocfilehash: c98270b4e69d80e18ba721de0a6379d40d21fc75
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448496"
---
# <span data-ttu-id="d266c-101">Update-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="d266c-101">Update-AzSentinelIncident</span></span>

## <span data-ttu-id="d266c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d266c-102">SYNOPSIS</span></span>
<span data-ttu-id="d266c-103">更新事件。</span><span class="sxs-lookup"><span data-stu-id="d266c-103">Update an Incident.</span></span>

## <span data-ttu-id="d266c-104">句法</span><span class="sxs-lookup"><span data-stu-id="d266c-104">SYNTAX</span></span>

### <span data-ttu-id="d266c-105">IncidentId (預設) </span><span class="sxs-lookup"><span data-stu-id="d266c-105">IncidentId (Default)</span></span>
```
Update-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> -IncidentID <String>
 [-Classification <String>] [-ClassificationComment <String>] [-ClassificationReason <String>]
 [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d266c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d266c-106">InputObject</span></span>
```
Update-AzSentinelIncident -InputObject <PSSentinelIncident> [-Classification <String>]
 [-ClassificationComment <String>] [-ClassificationReason <String>] [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d266c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d266c-107">ResourceId</span></span>
```
Update-AzSentinelIncident -ResourceId <String> [-Classification <String>] [-ClassificationComment <String>]
 [-ClassificationReason <String>] [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d266c-108">說明</span><span class="sxs-lookup"><span data-stu-id="d266c-108">DESCRIPTION</span></span>
<span data-ttu-id="d266c-109">**更新-AzSentinelIncident** Cmdlet 會更新指定工作區中的事件。</span><span class="sxs-lookup"><span data-stu-id="d266c-109">The **Update-AzSentinelIncident** cmdlet updates the Incident in the specified workspace.</span></span>
<span data-ttu-id="d266c-110">您可以將 **Incident** 物件傳遞為參數或使用管線運算子，或者也可以指定所需的參數。</span><span class="sxs-lookup"><span data-stu-id="d266c-110">You can pass an **Incident** object as a parameter or by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="d266c-111">您可以使用 *Confirm* 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d266c-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="d266c-112">示例</span><span class="sxs-lookup"><span data-stu-id="d266c-112">EXAMPLES</span></span>

### <span data-ttu-id="d266c-113">範例1</span><span class="sxs-lookup"><span data-stu-id="d266c-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId" -Severity High
```

<span data-ttu-id="d266c-114">此命令會 *IncidentId* 並將 [ *嚴重性* ] 屬性設為 [ *高*]，以取得事件。</span><span class="sxs-lookup"><span data-stu-id="d266c-114">The command gets the Incident by *IncidentId* and sets the *Severity* property to *High*.</span></span>  <span data-ttu-id="d266c-115">所有其他屬性都保持不變。</span><span class="sxs-lookup"><span data-stu-id="d266c-115">All other properties remain the same.</span></span>

## <span data-ttu-id="d266c-116">參數</span><span class="sxs-lookup"><span data-stu-id="d266c-116">PARAMETERS</span></span>

### <span data-ttu-id="d266c-117">-分類</span><span class="sxs-lookup"><span data-stu-id="d266c-117">-Classification</span></span>
<span data-ttu-id="d266c-118">事件 Classificaiton。</span><span class="sxs-lookup"><span data-stu-id="d266c-118">Incident Classificaiton.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: BenignPositive, FalsePositive, TruePositive, Undetermined

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d266c-119">-ClassificationComment</span><span class="sxs-lookup"><span data-stu-id="d266c-119">-ClassificationComment</span></span>
<span data-ttu-id="d266c-120">事件 Classificaiton 批註。</span><span class="sxs-lookup"><span data-stu-id="d266c-120">Incident Classificaiton Comment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d266c-121">-ClassificationReason</span><span class="sxs-lookup"><span data-stu-id="d266c-121">-ClassificationReason</span></span>
<span data-ttu-id="d266c-122">事件 Classificaiton 原因。</span><span class="sxs-lookup"><span data-stu-id="d266c-122">Incident Classificaiton Reason.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: InaccurateData, IncorrectAlertLogic, SuspiciousActivity, SuspiciousButExpected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d266c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d266c-123">-DefaultProfile</span></span>
<span data-ttu-id="d266c-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d266c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d266c-125">-描述</span><span class="sxs-lookup"><span data-stu-id="d266c-125">-Description</span></span>
<span data-ttu-id="d266c-126">說明.</span><span class="sxs-lookup"><span data-stu-id="d266c-126">Description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d266c-127">-IncidentID</span><span class="sxs-lookup"><span data-stu-id="d266c-127">-IncidentID</span></span>
<span data-ttu-id="d266c-128">事件 Id。</span><span class="sxs-lookup"><span data-stu-id="d266c-128">Incident Id.</span></span>

```yaml
Type: String
Parameter Sets: IncidentId, ParentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d266c-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d266c-129">-InputObject</span></span>
<span data-ttu-id="d266c-130">InputObject.</span><span class="sxs-lookup"><span data-stu-id="d266c-130">InputObject.</span></span>

```yaml
Type: PSSentinelIncident
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d266c-131">-標籤</span><span class="sxs-lookup"><span data-stu-id="d266c-131">-Label</span></span>
<span data-ttu-id="d266c-132">事件標籤。</span><span class="sxs-lookup"><span data-stu-id="d266c-132">Incident Labels.</span></span>

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

### <span data-ttu-id="d266c-133">-擁有者</span><span class="sxs-lookup"><span data-stu-id="d266c-133">-Owner</span></span>
<span data-ttu-id="d266c-134">事件擁有者。</span><span class="sxs-lookup"><span data-stu-id="d266c-134">Incident Owner.</span></span>

```yaml
Type: PSSentinelIncidentOwner
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d266c-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d266c-135">-ResourceGroupName</span></span>
<span data-ttu-id="d266c-136">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="d266c-136">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d266c-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d266c-137">-ResourceId</span></span>
<span data-ttu-id="d266c-138">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="d266c-138">Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d266c-139">-嚴重度</span><span class="sxs-lookup"><span data-stu-id="d266c-139">-Severity</span></span>
<span data-ttu-id="d266c-140">事件嚴重度。</span><span class="sxs-lookup"><span data-stu-id="d266c-140">Incident Severity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: High, Informational, Low, Medium

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d266c-141">-狀態</span><span class="sxs-lookup"><span data-stu-id="d266c-141">-Status</span></span>
<span data-ttu-id="d266c-142">事件狀態。</span><span class="sxs-lookup"><span data-stu-id="d266c-142">Incident Status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Active, Closed, New

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d266c-143">-標題</span><span class="sxs-lookup"><span data-stu-id="d266c-143">-Title</span></span>
<span data-ttu-id="d266c-144">事件標題。</span><span class="sxs-lookup"><span data-stu-id="d266c-144">Incident Title.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d266c-145">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d266c-145">-WorkspaceName</span></span>
<span data-ttu-id="d266c-146">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="d266c-146">Workspace Name.</span></span>

```yaml
Type: String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d266c-147">-確認</span><span class="sxs-lookup"><span data-stu-id="d266c-147">-Confirm</span></span>
<span data-ttu-id="d266c-148">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d266c-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d266c-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d266c-149">-WhatIf</span></span>
<span data-ttu-id="d266c-150">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d266c-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d266c-151">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d266c-151">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d266c-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d266c-152">CommonParameters</span></span>
<span data-ttu-id="d266c-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d266c-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d266c-154">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d266c-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d266c-155">輸入</span><span class="sxs-lookup"><span data-stu-id="d266c-155">INPUTS</span></span>

### <span data-ttu-id="d266c-156">PSSentinelIncident （SecurityInsights）的命令。</span><span class="sxs-lookup"><span data-stu-id="d266c-156">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>

### <span data-ttu-id="d266c-157">System.object</span><span class="sxs-lookup"><span data-stu-id="d266c-157">System.String</span></span>

### <span data-ttu-id="d266c-158">[System.object]. IList "1 [PSSentinelIncidentLabel，SecurityInsights，SecurityInsights = 0.1.0.0，Culture = 中性，PublicKeyToken = null]] （" 區域性 = null）]]）。</span><span class="sxs-lookup"><span data-stu-id="d266c-158">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="d266c-159">PSSentinelIncidentOwner （SecurityInsights）的命令。</span><span class="sxs-lookup"><span data-stu-id="d266c-159">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span></span>

## <span data-ttu-id="d266c-160">輸出</span><span class="sxs-lookup"><span data-stu-id="d266c-160">OUTPUTS</span></span>

### <span data-ttu-id="d266c-161">PSSentinelIncident （SecurityInsights）的命令。</span><span class="sxs-lookup"><span data-stu-id="d266c-161">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>

## <span data-ttu-id="d266c-162">筆記</span><span class="sxs-lookup"><span data-stu-id="d266c-162">NOTES</span></span>

## <span data-ttu-id="d266c-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="d266c-163">RELATED LINKS</span></span>
