---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 03eb85c423b06642a15db616b1ba1e0343c94963
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100133575"
---
# <span data-ttu-id="cd8da-101">Update-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="cd8da-101">Update-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="cd8da-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cd8da-102">SYNOPSIS</span></span>
<span data-ttu-id="cd8da-103">更新自動回應 (警示規則動作) 。</span><span class="sxs-lookup"><span data-stu-id="cd8da-103">Update an Automated Response (Alert Rule Action).</span></span>

## <span data-ttu-id="cd8da-104">句法</span><span class="sxs-lookup"><span data-stu-id="cd8da-104">SYNTAX</span></span>

### <span data-ttu-id="cd8da-105">ActionId (預設) </span><span class="sxs-lookup"><span data-stu-id="cd8da-105">ActionId (Default)</span></span>
```
Update-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> -LogicAppResourceId <String> -TriggerUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd8da-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="cd8da-106">InputObject</span></span>
```
Update-AzSentinelAlertRuleAction -LogicAppResourceId <String> -TriggerUri <String>
 -InputObject <PSSentinelActionResponse> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cd8da-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd8da-107">ResourceId</span></span>
```
Update-AzSentinelAlertRuleAction -LogicAppResourceId <String> -TriggerUri <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd8da-108">說明</span><span class="sxs-lookup"><span data-stu-id="cd8da-108">DESCRIPTION</span></span>
<span data-ttu-id="cd8da-109">**更新-AzSentinelAlertRuleAction** Cmdlet 會更新指定工作區中的書簽。</span><span class="sxs-lookup"><span data-stu-id="cd8da-109">The **Update-AzSentinelAlertRuleAction** cmdlet updates the bookmark in the specified workspace.</span></span>
<span data-ttu-id="cd8da-110">您可以將 **AlertRuleAction** 物件傳遞為參數或使用管線運算子，或者也可以指定 *AlertRuleId* 和 *ActionId* 參數。</span><span class="sxs-lookup"><span data-stu-id="cd8da-110">You can pass an **AlertRuleAction** object as a parameter or by using the pipeline operator, or alternatively you can specify the *AlertRuleId* and *ActionId* parameters.</span></span>
<span data-ttu-id="cd8da-111">您可以使用 *Confirm* 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cd8da-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="cd8da-112">示例</span><span class="sxs-lookup"><span data-stu-id="cd8da-112">EXAMPLES</span></span>

### <span data-ttu-id="cd8da-113">範例1</span><span class="sxs-lookup"><span data-stu-id="cd8da-113">Example 1</span></span>
```powershell
PS C:\>$LogicAppResourceId = Get-AzLogicApp -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword"
PS C:\>$LogicAppTriggerUri = Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword" -TriggerName "When_a_response_to_an_Azure_Sentinel_alert_is_triggered"
PS C:\> Update-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId" -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="cd8da-114">這個範例會更新以新屬性取代現有 *動作* 的 **AlertRuleAction** 。</span><span class="sxs-lookup"><span data-stu-id="cd8da-114">This example updates an **AlertRuleAction** replacing an existing *Action* with new properties.</span></span>

### <span data-ttu-id="cd8da-115">範例2</span><span class="sxs-lookup"><span data-stu-id="cd8da-115">Example 2</span></span>
```powershell
PS C:\> $AlertRuleAction = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
PS C:\> Update-AzSentinelAlertRuleAction -InputObject $AlertRuleAction -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="cd8da-116">這個範例會使用 InputObject 來更新含有新屬性的現有 *動作* 來更新 **AlertRuleAction** 。</span><span class="sxs-lookup"><span data-stu-id="cd8da-116">This example updates an **AlertRuleAction** using an InputObject replacing an existing *Action* with new properties.</span></span>

## <span data-ttu-id="cd8da-117">參數</span><span class="sxs-lookup"><span data-stu-id="cd8da-117">PARAMETERS</span></span>

### <span data-ttu-id="cd8da-118">-ActionId</span><span class="sxs-lookup"><span data-stu-id="cd8da-118">-ActionId</span></span>
<span data-ttu-id="cd8da-119">[動作識別碼]。</span><span class="sxs-lookup"><span data-stu-id="cd8da-119">Action Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd8da-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="cd8da-120">-AlertRuleId</span></span>
<span data-ttu-id="cd8da-121">[警示規則識別碼]。</span><span class="sxs-lookup"><span data-stu-id="cd8da-121">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd8da-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd8da-122">-DefaultProfile</span></span>
<span data-ttu-id="cd8da-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cd8da-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd8da-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd8da-124">-InputObject</span></span>
<span data-ttu-id="cd8da-125">InputObject.</span><span class="sxs-lookup"><span data-stu-id="cd8da-125">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd8da-126">-LogicAppResourceId</span><span class="sxs-lookup"><span data-stu-id="cd8da-126">-LogicAppResourceId</span></span>
<span data-ttu-id="cd8da-127">動作邏輯 App 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="cd8da-127">Action Logic App Resource Id.</span></span>

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

### <span data-ttu-id="cd8da-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd8da-128">-ResourceGroupName</span></span>
<span data-ttu-id="cd8da-129">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="cd8da-129">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd8da-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd8da-130">-ResourceId</span></span>
<span data-ttu-id="cd8da-131">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="cd8da-131">Resource Id.</span></span>

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

### <span data-ttu-id="cd8da-132">-TriggerUri</span><span class="sxs-lookup"><span data-stu-id="cd8da-132">-TriggerUri</span></span>
<span data-ttu-id="cd8da-133">動作邏輯 App 觸發程式 Uri。</span><span class="sxs-lookup"><span data-stu-id="cd8da-133">Action Logic App Trigger Uri.</span></span>

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

### <span data-ttu-id="cd8da-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cd8da-134">-WorkspaceName</span></span>
<span data-ttu-id="cd8da-135">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="cd8da-135">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd8da-136">-確認</span><span class="sxs-lookup"><span data-stu-id="cd8da-136">-Confirm</span></span>
<span data-ttu-id="cd8da-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cd8da-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd8da-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd8da-138">-WhatIf</span></span>
<span data-ttu-id="cd8da-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cd8da-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd8da-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd8da-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd8da-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd8da-141">CommonParameters</span></span>
<span data-ttu-id="cd8da-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cd8da-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd8da-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cd8da-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd8da-144">輸入</span><span class="sxs-lookup"><span data-stu-id="cd8da-144">INPUTS</span></span>

### <span data-ttu-id="cd8da-145">SecurityInsights AlertRules. PSSentinelAlertRule （）</span><span class="sxs-lookup"><span data-stu-id="cd8da-145">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

### <span data-ttu-id="cd8da-146">PSSentinelActionResponse 中的 SecurityInsights.。</span><span class="sxs-lookup"><span data-stu-id="cd8da-146">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>

### <span data-ttu-id="cd8da-147">System.object</span><span class="sxs-lookup"><span data-stu-id="cd8da-147">System.String</span></span>

## <span data-ttu-id="cd8da-148">輸出</span><span class="sxs-lookup"><span data-stu-id="cd8da-148">OUTPUTS</span></span>

### <span data-ttu-id="cd8da-149">PSSentinelActionResponse 中的 SecurityInsights.。</span><span class="sxs-lookup"><span data-stu-id="cd8da-149">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>

## <span data-ttu-id="cd8da-150">筆記</span><span class="sxs-lookup"><span data-stu-id="cd8da-150">NOTES</span></span>

## <span data-ttu-id="cd8da-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="cd8da-151">RELATED LINKS</span></span>
