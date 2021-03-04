---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/update-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 3feb6a9cfa06e06a4759c34e3c0b2cd624559d2c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902834"
---
# <span data-ttu-id="73505-101">Update-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="73505-101">Update-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="73505-102">簡介</span><span class="sxs-lookup"><span data-stu-id="73505-102">SYNOPSIS</span></span>
<span data-ttu-id="73505-103">更新自動回應 (警示規則動作) 。</span><span class="sxs-lookup"><span data-stu-id="73505-103">Update an Automated Response (Alert Rule Action).</span></span>

## <span data-ttu-id="73505-104">語法</span><span class="sxs-lookup"><span data-stu-id="73505-104">SYNTAX</span></span>

### <span data-ttu-id="73505-105">ActionId (預設) </span><span class="sxs-lookup"><span data-stu-id="73505-105">ActionId (Default)</span></span>
```
Update-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> -LogicAppResourceId <String> -TriggerUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73505-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="73505-106">InputObject</span></span>
```
Update-AzSentinelAlertRuleAction -LogicAppResourceId <String> -TriggerUri <String>
 -InputObject <PSSentinelActionResponse> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="73505-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="73505-107">ResourceId</span></span>
```
Update-AzSentinelAlertRuleAction -LogicAppResourceId <String> -TriggerUri <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73505-108">描述</span><span class="sxs-lookup"><span data-stu-id="73505-108">DESCRIPTION</span></span>
<span data-ttu-id="73505-109">**Update-AzSentinelAlertRuleAction** Cmdlet 會更新指定工作區中的書簽。</span><span class="sxs-lookup"><span data-stu-id="73505-109">The **Update-AzSentinelAlertRuleAction** cmdlet updates the bookmark in the specified workspace.</span></span>
<span data-ttu-id="73505-110">您可以傳遞 **AlertRuleAction** 物件做為參數，或是使用管線運算子，或者您也可以指定 *AlertRuleId* 和 *ActionId* 參數。</span><span class="sxs-lookup"><span data-stu-id="73505-110">You can pass an **AlertRuleAction** object as a parameter or by using the pipeline operator, or alternatively you can specify the *AlertRuleId* and *ActionId* parameters.</span></span>
<span data-ttu-id="73505-111">您可以使用確認 *參數$ConfirmPreference* Windows PowerShell 變數來控制 Cmdlet 是否提示您確認。</span><span class="sxs-lookup"><span data-stu-id="73505-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="73505-112">例子</span><span class="sxs-lookup"><span data-stu-id="73505-112">EXAMPLES</span></span>

### <span data-ttu-id="73505-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="73505-113">Example 1</span></span>
```powershell
PS C:\>$LogicAppResourceId = Get-AzLogicApp -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword"
PS C:\>$LogicAppTriggerUri = Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword" -TriggerName "When_a_response_to_an_Azure_Sentinel_alert_is_triggered"
PS C:\> Update-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId" -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="73505-114">此範例會更新 **AlertRuleAction** 以新 *屬性取代現有的動作* 。</span><span class="sxs-lookup"><span data-stu-id="73505-114">This example updates an **AlertRuleAction** replacing an existing *Action* with new properties.</span></span>

### <span data-ttu-id="73505-115">範例 2</span><span class="sxs-lookup"><span data-stu-id="73505-115">Example 2</span></span>
```powershell
PS C:\> $AlertRuleAction = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
PS C:\> Update-AzSentinelAlertRuleAction -InputObject $AlertRuleAction -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="73505-116">此範例會使用 InputObject 更新 **AlertRuleAction，** 以新的屬性取代現有的 *動作* 。</span><span class="sxs-lookup"><span data-stu-id="73505-116">This example updates an **AlertRuleAction** using an InputObject replacing an existing *Action* with new properties.</span></span>

## <span data-ttu-id="73505-117">參數</span><span class="sxs-lookup"><span data-stu-id="73505-117">PARAMETERS</span></span>

### <span data-ttu-id="73505-118">-ActionId</span><span class="sxs-lookup"><span data-stu-id="73505-118">-ActionId</span></span>
<span data-ttu-id="73505-119">動作識別碼。</span><span class="sxs-lookup"><span data-stu-id="73505-119">Action Id.</span></span>

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

### <span data-ttu-id="73505-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="73505-120">-AlertRuleId</span></span>
<span data-ttu-id="73505-121">警示規則識別碼。</span><span class="sxs-lookup"><span data-stu-id="73505-121">Alert Rule Id.</span></span>

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

### <span data-ttu-id="73505-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73505-122">-DefaultProfile</span></span>
<span data-ttu-id="73505-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="73505-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73505-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73505-124">-InputObject</span></span>
<span data-ttu-id="73505-125">InputObject。</span><span class="sxs-lookup"><span data-stu-id="73505-125">InputObject.</span></span>

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

### <span data-ttu-id="73505-126">-LogicAppResourceId</span><span class="sxs-lookup"><span data-stu-id="73505-126">-LogicAppResourceId</span></span>
<span data-ttu-id="73505-127">動作邏輯應用程式資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="73505-127">Action Logic App Resource Id.</span></span>

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

### <span data-ttu-id="73505-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73505-128">-ResourceGroupName</span></span>
<span data-ttu-id="73505-129">資源組名。</span><span class="sxs-lookup"><span data-stu-id="73505-129">Resource group name.</span></span>

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

### <span data-ttu-id="73505-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73505-130">-ResourceId</span></span>
<span data-ttu-id="73505-131">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="73505-131">Resource Id.</span></span>

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

### <span data-ttu-id="73505-132">-TriggerUri</span><span class="sxs-lookup"><span data-stu-id="73505-132">-TriggerUri</span></span>
<span data-ttu-id="73505-133">動作邏輯應用程式觸發 Uri。</span><span class="sxs-lookup"><span data-stu-id="73505-133">Action Logic App Trigger Uri.</span></span>

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

### <span data-ttu-id="73505-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="73505-134">-WorkspaceName</span></span>
<span data-ttu-id="73505-135">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="73505-135">Workspace Name.</span></span>

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

### <span data-ttu-id="73505-136">-確認</span><span class="sxs-lookup"><span data-stu-id="73505-136">-Confirm</span></span>
<span data-ttu-id="73505-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="73505-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73505-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73505-138">-WhatIf</span></span>
<span data-ttu-id="73505-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="73505-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73505-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="73505-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73505-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73505-141">CommonParameters</span></span>
<span data-ttu-id="73505-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="73505-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73505-143">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73505-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73505-144">輸入</span><span class="sxs-lookup"><span data-stu-id="73505-144">INPUTS</span></span>

### <span data-ttu-id="73505-145">Microsoft.Azure.Commands.SecurityInsights.models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="73505-145">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

### <span data-ttu-id="73505-146">Microsoft.Azure.Commands.SecurityInsights.models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="73505-146">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>

### <span data-ttu-id="73505-147">System.String</span><span class="sxs-lookup"><span data-stu-id="73505-147">System.String</span></span>

## <span data-ttu-id="73505-148">輸出</span><span class="sxs-lookup"><span data-stu-id="73505-148">OUTPUTS</span></span>

### <span data-ttu-id="73505-149">Microsoft.Azure.Commands.SecurityInsights.models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="73505-149">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>

## <span data-ttu-id="73505-150">筆記</span><span class="sxs-lookup"><span data-stu-id="73505-150">NOTES</span></span>

## <span data-ttu-id="73505-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="73505-151">RELATED LINKS</span></span>
