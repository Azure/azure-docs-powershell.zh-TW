---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/update-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelIncident.md
ms.openlocfilehash: 03062015b1f9d14688488887ed226f1b697589ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917921"
---
# <span data-ttu-id="7da72-101">Update-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="7da72-101">Update-AzSentinelIncident</span></span>

## <span data-ttu-id="7da72-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7da72-102">SYNOPSIS</span></span>
<span data-ttu-id="7da72-103">更新事件。</span><span class="sxs-lookup"><span data-stu-id="7da72-103">Update an Incident.</span></span>

## <span data-ttu-id="7da72-104">語法</span><span class="sxs-lookup"><span data-stu-id="7da72-104">SYNTAX</span></span>

### <span data-ttu-id="7da72-105">IncidentId (預設) </span><span class="sxs-lookup"><span data-stu-id="7da72-105">IncidentId (Default)</span></span>
```
Update-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> -IncidentID <String>
 [-Classification <String>] [-ClassificationComment <String>] [-ClassificationReason <String>]
 [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7da72-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="7da72-106">InputObject</span></span>
```
Update-AzSentinelIncident -InputObject <PSSentinelIncident> [-Classification <String>]
 [-ClassificationComment <String>] [-ClassificationReason <String>] [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7da72-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7da72-107">ResourceId</span></span>
```
Update-AzSentinelIncident -ResourceId <String> [-Classification <String>] [-ClassificationComment <String>]
 [-ClassificationReason <String>] [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7da72-108">描述</span><span class="sxs-lookup"><span data-stu-id="7da72-108">DESCRIPTION</span></span>
<span data-ttu-id="7da72-109">**Update-AzSentinelIncident** Cmdlet 會更新指定工作區中的事件。</span><span class="sxs-lookup"><span data-stu-id="7da72-109">The **Update-AzSentinelIncident** cmdlet updates the Incident in the specified workspace.</span></span>
<span data-ttu-id="7da72-110">您可以傳遞 **事件** 物件做為參數，或是使用管線運算子，或者您也可以指定所需的參數。</span><span class="sxs-lookup"><span data-stu-id="7da72-110">You can pass an **Incident** object as a parameter or by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="7da72-111">您可以使用確認 *參數$ConfirmPreference* Windows PowerShell 變數來控制 Cmdlet 是否提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7da72-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="7da72-112">例子</span><span class="sxs-lookup"><span data-stu-id="7da72-112">EXAMPLES</span></span>

### <span data-ttu-id="7da72-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="7da72-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId" -Severity High
```

<span data-ttu-id="7da72-114">該命令會按 IncidentId 獲得 *[事件值* ，並設定嚴重性 *屬性* 為 *高*。</span><span class="sxs-lookup"><span data-stu-id="7da72-114">The command gets the Incident by *IncidentId* and sets the *Severity* property to *High*.</span></span>  <span data-ttu-id="7da72-115">所有其他屬性會保持相同。</span><span class="sxs-lookup"><span data-stu-id="7da72-115">All other properties remain the same.</span></span>

## <span data-ttu-id="7da72-116">參數</span><span class="sxs-lookup"><span data-stu-id="7da72-116">PARAMETERS</span></span>

### <span data-ttu-id="7da72-117">-分類</span><span class="sxs-lookup"><span data-stu-id="7da72-117">-Classification</span></span>
<span data-ttu-id="7da72-118">Incident Classificaiton.</span><span class="sxs-lookup"><span data-stu-id="7da72-118">Incident Classificaiton.</span></span>

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

### <span data-ttu-id="7da72-119">-ClassificationComment</span><span class="sxs-lookup"><span data-stu-id="7da72-119">-ClassificationComment</span></span>
<span data-ttu-id="7da72-120">事件類別批註。</span><span class="sxs-lookup"><span data-stu-id="7da72-120">Incident Classificaiton Comment.</span></span>

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

### <span data-ttu-id="7da72-121">-ClassificationReason</span><span class="sxs-lookup"><span data-stu-id="7da72-121">-ClassificationReason</span></span>
<span data-ttu-id="7da72-122">Incident Classificaiton 原因。</span><span class="sxs-lookup"><span data-stu-id="7da72-122">Incident Classificaiton Reason.</span></span>

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

### <span data-ttu-id="7da72-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7da72-123">-DefaultProfile</span></span>
<span data-ttu-id="7da72-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7da72-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7da72-125">-描述</span><span class="sxs-lookup"><span data-stu-id="7da72-125">-Description</span></span>
<span data-ttu-id="7da72-126">描述。</span><span class="sxs-lookup"><span data-stu-id="7da72-126">Description.</span></span>

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

### <span data-ttu-id="7da72-127">-IncidentID</span><span class="sxs-lookup"><span data-stu-id="7da72-127">-IncidentID</span></span>
<span data-ttu-id="7da72-128">事件識別碼。</span><span class="sxs-lookup"><span data-stu-id="7da72-128">Incident Id.</span></span>

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

### <span data-ttu-id="7da72-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7da72-129">-InputObject</span></span>
<span data-ttu-id="7da72-130">InputObject。</span><span class="sxs-lookup"><span data-stu-id="7da72-130">InputObject.</span></span>

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

### <span data-ttu-id="7da72-131">-標籤</span><span class="sxs-lookup"><span data-stu-id="7da72-131">-Label</span></span>
<span data-ttu-id="7da72-132">事件標籤。</span><span class="sxs-lookup"><span data-stu-id="7da72-132">Incident Labels.</span></span>

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

### <span data-ttu-id="7da72-133">-擁有者</span><span class="sxs-lookup"><span data-stu-id="7da72-133">-Owner</span></span>
<span data-ttu-id="7da72-134">事件擁有者。</span><span class="sxs-lookup"><span data-stu-id="7da72-134">Incident Owner.</span></span>

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

### <span data-ttu-id="7da72-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7da72-135">-ResourceGroupName</span></span>
<span data-ttu-id="7da72-136">資源組名。</span><span class="sxs-lookup"><span data-stu-id="7da72-136">Resource group name.</span></span>

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

### <span data-ttu-id="7da72-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7da72-137">-ResourceId</span></span>
<span data-ttu-id="7da72-138">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="7da72-138">Resource Id.</span></span>

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

### <span data-ttu-id="7da72-139">-嚴重性</span><span class="sxs-lookup"><span data-stu-id="7da72-139">-Severity</span></span>
<span data-ttu-id="7da72-140">事件嚴重性。</span><span class="sxs-lookup"><span data-stu-id="7da72-140">Incident Severity.</span></span>

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

### <span data-ttu-id="7da72-141">-狀態</span><span class="sxs-lookup"><span data-stu-id="7da72-141">-Status</span></span>
<span data-ttu-id="7da72-142">事件狀態。</span><span class="sxs-lookup"><span data-stu-id="7da72-142">Incident Status.</span></span>

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

### <span data-ttu-id="7da72-143">-標題</span><span class="sxs-lookup"><span data-stu-id="7da72-143">-Title</span></span>
<span data-ttu-id="7da72-144">事件標題。</span><span class="sxs-lookup"><span data-stu-id="7da72-144">Incident Title.</span></span>

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

### <span data-ttu-id="7da72-145">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7da72-145">-WorkspaceName</span></span>
<span data-ttu-id="7da72-146">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="7da72-146">Workspace Name.</span></span>

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

### <span data-ttu-id="7da72-147">-確認</span><span class="sxs-lookup"><span data-stu-id="7da72-147">-Confirm</span></span>
<span data-ttu-id="7da72-148">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7da72-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7da72-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7da72-149">-WhatIf</span></span>
<span data-ttu-id="7da72-150">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7da72-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7da72-151">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7da72-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7da72-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7da72-152">CommonParameters</span></span>
<span data-ttu-id="7da72-153">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7da72-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7da72-154">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7da72-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7da72-155">輸入</span><span class="sxs-lookup"><span data-stu-id="7da72-155">INPUTS</span></span>

### <span data-ttu-id="7da72-156">Microsoft.Azure.Commands.SecurityInsights.models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="7da72-156">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>

### <span data-ttu-id="7da72-157">System.String</span><span class="sxs-lookup"><span data-stu-id="7da72-157">System.String</span></span>

### <span data-ttu-id="7da72-158">System.Collections.Generic.IList'1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="7da72-158">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="7da72-159">Microsoft.Azure.Commands.SecurityInsights.models.Incidents.PSSentinelIncidentOwner</span><span class="sxs-lookup"><span data-stu-id="7da72-159">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span></span>

## <span data-ttu-id="7da72-160">輸出</span><span class="sxs-lookup"><span data-stu-id="7da72-160">OUTPUTS</span></span>

### <span data-ttu-id="7da72-161">Microsoft.Azure.Commands.SecurityInsights.models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="7da72-161">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>

## <span data-ttu-id="7da72-162">筆記</span><span class="sxs-lookup"><span data-stu-id="7da72-162">NOTES</span></span>

## <span data-ttu-id="7da72-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="7da72-163">RELATED LINKS</span></span>
