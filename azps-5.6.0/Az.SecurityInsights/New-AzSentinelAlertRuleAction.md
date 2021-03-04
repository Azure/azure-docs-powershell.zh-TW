---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/new-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRuleAction.md
ms.openlocfilehash: ed4d1b5d833ce73a9b0a19e38a05192d11a0d8f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908013"
---
# <span data-ttu-id="56129-101">New-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="56129-101">New-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="56129-102">簡介</span><span class="sxs-lookup"><span data-stu-id="56129-102">SYNOPSIS</span></span>
<span data-ttu-id="56129-103">新增自動回復至 Analal。。</span><span class="sxs-lookup"><span data-stu-id="56129-103">Add an Automated Response to an Analatic.</span></span>

## <span data-ttu-id="56129-104">語法</span><span class="sxs-lookup"><span data-stu-id="56129-104">SYNTAX</span></span>

```
New-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-ActionId <String>] -LogicAppResourceId <String> -TriggerUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56129-105">描述</span><span class="sxs-lookup"><span data-stu-id="56129-105">DESCRIPTION</span></span>
<span data-ttu-id="56129-106">**New-AzSentinelAlertRuleAction** Cmdlet 會建立指定工作區中警示規則的自動回應。</span><span class="sxs-lookup"><span data-stu-id="56129-106">The **New-AzSentinelAlertRuleAction** cmdlet creates an Automated Response for an Alert Rule in the specified workspace.</span></span>
<span data-ttu-id="56129-107">您必須提供邏輯應用程式重新連接識別碼和觸發 Uri，您可以使用邏輯應用程式模組找到。</span><span class="sxs-lookup"><span data-stu-id="56129-107">You must provide the Logic App Resorce Id and Trigger Uri which can be found using the Logic App module.</span></span>
<span data-ttu-id="56129-108">您可以使用確認 *參數$ConfirmPreference* Windows PowerShell 變數來控制 Cmdlet 是否提示您確認。</span><span class="sxs-lookup"><span data-stu-id="56129-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="56129-109">例子</span><span class="sxs-lookup"><span data-stu-id="56129-109">EXAMPLES</span></span>

### <span data-ttu-id="56129-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="56129-110">Example 1</span></span>
```powershell
PS C:\>$LogicAppResourceId = Get-AzLogicApp -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword"
PS C:\>$LogicAppTriggerUri = Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword" -TriggerName "When_a_response_to_an_Azure_Sentinel_alert_is_triggered"
PS C:\>$AlertRuleAction = New-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="56129-111">此範例會使用邏輯應用程式的屬性，為指定的警示規則建立 **AlertRuleAction，** 然後將它儲存在 $AlertRuleAction 變數中。</span><span class="sxs-lookup"><span data-stu-id="56129-111">This example creates an **AlertRuleAction** for the specified Alert Rule using properties of the Logic App, and then stores it in the $AlertRuleAction variable.</span></span>

## <span data-ttu-id="56129-112">參數</span><span class="sxs-lookup"><span data-stu-id="56129-112">PARAMETERS</span></span>

### <span data-ttu-id="56129-113">-ActionId</span><span class="sxs-lookup"><span data-stu-id="56129-113">-ActionId</span></span>
<span data-ttu-id="56129-114">動作識別碼。</span><span class="sxs-lookup"><span data-stu-id="56129-114">Action Id.</span></span>

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

### <span data-ttu-id="56129-115">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="56129-115">-AlertRuleId</span></span>
<span data-ttu-id="56129-116">警示規則識別碼。</span><span class="sxs-lookup"><span data-stu-id="56129-116">Alert Rule Id.</span></span>

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

### <span data-ttu-id="56129-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56129-117">-DefaultProfile</span></span>
<span data-ttu-id="56129-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="56129-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56129-119">-LogicAppResourceId</span><span class="sxs-lookup"><span data-stu-id="56129-119">-LogicAppResourceId</span></span>
<span data-ttu-id="56129-120">動作邏輯應用程式資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="56129-120">Action Logic App Resource Id.</span></span>

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

### <span data-ttu-id="56129-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56129-121">-ResourceGroupName</span></span>
<span data-ttu-id="56129-122">資源組名。</span><span class="sxs-lookup"><span data-stu-id="56129-122">Resource group name.</span></span>

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

### <span data-ttu-id="56129-123">-TriggerUri</span><span class="sxs-lookup"><span data-stu-id="56129-123">-TriggerUri</span></span>
<span data-ttu-id="56129-124">動作邏輯應用程式觸發 Uri。</span><span class="sxs-lookup"><span data-stu-id="56129-124">Action Logic App Trigger Uri.</span></span>

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

### <span data-ttu-id="56129-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="56129-125">-WorkspaceName</span></span>
<span data-ttu-id="56129-126">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="56129-126">Workspace Name.</span></span>

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

### <span data-ttu-id="56129-127">-確認</span><span class="sxs-lookup"><span data-stu-id="56129-127">-Confirm</span></span>
<span data-ttu-id="56129-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="56129-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56129-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56129-129">-WhatIf</span></span>
<span data-ttu-id="56129-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="56129-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="56129-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="56129-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56129-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56129-132">CommonParameters</span></span>
<span data-ttu-id="56129-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="56129-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56129-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56129-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56129-135">輸入</span><span class="sxs-lookup"><span data-stu-id="56129-135">INPUTS</span></span>

### <span data-ttu-id="56129-136">沒有</span><span class="sxs-lookup"><span data-stu-id="56129-136">None</span></span>
## <span data-ttu-id="56129-137">輸出</span><span class="sxs-lookup"><span data-stu-id="56129-137">OUTPUTS</span></span>

### <span data-ttu-id="56129-138">Microsoft.Azure.Commands.SecurityInsights.models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="56129-138">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="56129-139">筆記</span><span class="sxs-lookup"><span data-stu-id="56129-139">NOTES</span></span>

## <span data-ttu-id="56129-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="56129-140">RELATED LINKS</span></span>
