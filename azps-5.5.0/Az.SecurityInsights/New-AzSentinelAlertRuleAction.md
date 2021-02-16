---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 57b1f21aae43bd8b52d6bd4f23a15a7f41c15495
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100139887"
---
# <span data-ttu-id="2240a-101">New-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="2240a-101">New-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="2240a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2240a-102">SYNOPSIS</span></span>
<span data-ttu-id="2240a-103">將自動回應新增至 Analatic。</span><span class="sxs-lookup"><span data-stu-id="2240a-103">Add an Automated Response to an Analatic.</span></span>

## <span data-ttu-id="2240a-104">句法</span><span class="sxs-lookup"><span data-stu-id="2240a-104">SYNTAX</span></span>

```
New-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-ActionId <String>] -LogicAppResourceId <String> -TriggerUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2240a-105">說明</span><span class="sxs-lookup"><span data-stu-id="2240a-105">DESCRIPTION</span></span>
<span data-ttu-id="2240a-106">**新的-AzSentinelAlertRuleAction** Cmdlet 會針對指定工作區中的報警規則建立自動回應。</span><span class="sxs-lookup"><span data-stu-id="2240a-106">The **New-AzSentinelAlertRuleAction** cmdlet creates an Automated Response for an Alert Rule in the specified workspace.</span></span>
<span data-ttu-id="2240a-107">您必須提供邏輯 App Resorce Id 與觸發 Uri，才能使用邏輯 App 模組找到。</span><span class="sxs-lookup"><span data-stu-id="2240a-107">You must provide the Logic App Resorce Id and Trigger Uri which can be found using the Logic App module.</span></span>
<span data-ttu-id="2240a-108">您可以使用 *Confirm* 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2240a-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="2240a-109">示例</span><span class="sxs-lookup"><span data-stu-id="2240a-109">EXAMPLES</span></span>

### <span data-ttu-id="2240a-110">範例1</span><span class="sxs-lookup"><span data-stu-id="2240a-110">Example 1</span></span>
```powershell
PS C:\>$LogicAppResourceId = Get-AzLogicApp -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword"
PS C:\>$LogicAppTriggerUri = Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword" -TriggerName "When_a_response_to_an_Azure_Sentinel_alert_is_triggered"
PS C:\>$AlertRuleAction = New-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="2240a-111">這個範例會使用邏輯 App 的屬性，為指定的警示規則建立 **AlertRuleAction** ，然後將其儲存在 $AlertRuleAction 變數中。</span><span class="sxs-lookup"><span data-stu-id="2240a-111">This example creates an **AlertRuleAction** for the specified Alert Rule using properties of the Logic App, and then stores it in the $AlertRuleAction variable.</span></span>

## <span data-ttu-id="2240a-112">參數</span><span class="sxs-lookup"><span data-stu-id="2240a-112">PARAMETERS</span></span>

### <span data-ttu-id="2240a-113">-ActionId</span><span class="sxs-lookup"><span data-stu-id="2240a-113">-ActionId</span></span>
<span data-ttu-id="2240a-114">[動作識別碼]。</span><span class="sxs-lookup"><span data-stu-id="2240a-114">Action Id.</span></span>

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

### <span data-ttu-id="2240a-115">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="2240a-115">-AlertRuleId</span></span>
<span data-ttu-id="2240a-116">[警示規則識別碼]。</span><span class="sxs-lookup"><span data-stu-id="2240a-116">Alert Rule Id.</span></span>

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

### <span data-ttu-id="2240a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2240a-117">-DefaultProfile</span></span>
<span data-ttu-id="2240a-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2240a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2240a-119">-LogicAppResourceId</span><span class="sxs-lookup"><span data-stu-id="2240a-119">-LogicAppResourceId</span></span>
<span data-ttu-id="2240a-120">動作邏輯 App 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2240a-120">Action Logic App Resource Id.</span></span>

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

### <span data-ttu-id="2240a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2240a-121">-ResourceGroupName</span></span>
<span data-ttu-id="2240a-122">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="2240a-122">Resource group name.</span></span>

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

### <span data-ttu-id="2240a-123">-TriggerUri</span><span class="sxs-lookup"><span data-stu-id="2240a-123">-TriggerUri</span></span>
<span data-ttu-id="2240a-124">動作邏輯 App 觸發程式 Uri。</span><span class="sxs-lookup"><span data-stu-id="2240a-124">Action Logic App Trigger Uri.</span></span>

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

### <span data-ttu-id="2240a-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2240a-125">-WorkspaceName</span></span>
<span data-ttu-id="2240a-126">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="2240a-126">Workspace Name.</span></span>

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

### <span data-ttu-id="2240a-127">-確認</span><span class="sxs-lookup"><span data-stu-id="2240a-127">-Confirm</span></span>
<span data-ttu-id="2240a-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2240a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2240a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2240a-129">-WhatIf</span></span>
<span data-ttu-id="2240a-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2240a-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2240a-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2240a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2240a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2240a-132">CommonParameters</span></span>
<span data-ttu-id="2240a-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2240a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2240a-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2240a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2240a-135">輸入</span><span class="sxs-lookup"><span data-stu-id="2240a-135">INPUTS</span></span>

### <span data-ttu-id="2240a-136">所有</span><span class="sxs-lookup"><span data-stu-id="2240a-136">None</span></span>
## <span data-ttu-id="2240a-137">輸出</span><span class="sxs-lookup"><span data-stu-id="2240a-137">OUTPUTS</span></span>

### <span data-ttu-id="2240a-138">PSSentinelActionResponse 中的 SecurityInsights.。</span><span class="sxs-lookup"><span data-stu-id="2240a-138">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="2240a-139">筆記</span><span class="sxs-lookup"><span data-stu-id="2240a-139">NOTES</span></span>

## <span data-ttu-id="2240a-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="2240a-140">RELATED LINKS</span></span>
