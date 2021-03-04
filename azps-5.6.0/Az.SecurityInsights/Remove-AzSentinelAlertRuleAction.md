---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/remove-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 0828961a534a6f98d52cdf8c4e2a134cc2975df4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904830"
---
# <span data-ttu-id="852ee-101">Remove-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="852ee-101">Remove-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="852ee-102">簡介</span><span class="sxs-lookup"><span data-stu-id="852ee-102">SYNOPSIS</span></span>
<span data-ttu-id="852ee-103">從分析移除自動化回應。</span><span class="sxs-lookup"><span data-stu-id="852ee-103">Remove an Automated Response from an Analytic.</span></span>

## <span data-ttu-id="852ee-104">語法</span><span class="sxs-lookup"><span data-stu-id="852ee-104">SYNTAX</span></span>

### <span data-ttu-id="852ee-105">ActionId (預設) </span><span class="sxs-lookup"><span data-stu-id="852ee-105">ActionId (Default)</span></span>
```
Remove-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="852ee-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="852ee-106">InputObject</span></span>
```
Remove-AzSentinelAlertRuleAction -InputObject <PSSentinelActionResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="852ee-107">描述</span><span class="sxs-lookup"><span data-stu-id="852ee-107">DESCRIPTION</span></span>
<span data-ttu-id="852ee-108">**Remove-AzSentinelAlertRuleAction** Cmdlet 會永久刪除指定工作區中警示規則的自動回應。</span><span class="sxs-lookup"><span data-stu-id="852ee-108">The **Remove-AzSentinelAlertRuleAction** cmdlet permanently deletes an Automated Response from the Alert Rule in a specified workspace.</span></span>
<span data-ttu-id="852ee-109">您可以使用管線運算子傳遞 **AlertRuleAction** 物件，或者您也可以指定所需的參數。</span><span class="sxs-lookup"><span data-stu-id="852ee-109">You can pass an **AlertRuleAction** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="852ee-110">您可以使用確認參數$ConfirmPreference Windows PowerShell 變數來控制 Cmdlet 是否提示您確認。</span><span class="sxs-lookup"><span data-stu-id="852ee-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="852ee-111">例子</span><span class="sxs-lookup"><span data-stu-id="852ee-111">EXAMPLES</span></span>

### <span data-ttu-id="852ee-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="852ee-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
```

<span data-ttu-id="852ee-113">此命令會從工作區移除警示規則。</span><span class="sxs-lookup"><span data-stu-id="852ee-113">This command removes the Alert Rule from the workspace.</span></span>

## <span data-ttu-id="852ee-114">參數</span><span class="sxs-lookup"><span data-stu-id="852ee-114">PARAMETERS</span></span>

### <span data-ttu-id="852ee-115">-ActionId</span><span class="sxs-lookup"><span data-stu-id="852ee-115">-ActionId</span></span>
<span data-ttu-id="852ee-116">動作識別碼。</span><span class="sxs-lookup"><span data-stu-id="852ee-116">Action Id.</span></span>

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

### <span data-ttu-id="852ee-117">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="852ee-117">-AlertRuleId</span></span>
<span data-ttu-id="852ee-118">警示規則識別碼。</span><span class="sxs-lookup"><span data-stu-id="852ee-118">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="852ee-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="852ee-119">-DefaultProfile</span></span>
<span data-ttu-id="852ee-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="852ee-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="852ee-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="852ee-121">-InputObject</span></span>
<span data-ttu-id="852ee-122">InputObject。</span><span class="sxs-lookup"><span data-stu-id="852ee-122">InputObject.</span></span>

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

### <span data-ttu-id="852ee-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="852ee-123">-PassThru</span></span>
<span data-ttu-id="852ee-124">PassThru</span><span class="sxs-lookup"><span data-stu-id="852ee-124">PassThru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="852ee-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="852ee-125">-ResourceGroupName</span></span>
<span data-ttu-id="852ee-126">資源組名。</span><span class="sxs-lookup"><span data-stu-id="852ee-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="852ee-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="852ee-127">-WorkspaceName</span></span>
<span data-ttu-id="852ee-128">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="852ee-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="852ee-129">-確認</span><span class="sxs-lookup"><span data-stu-id="852ee-129">-Confirm</span></span>
<span data-ttu-id="852ee-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="852ee-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="852ee-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="852ee-131">-WhatIf</span></span>
<span data-ttu-id="852ee-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="852ee-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="852ee-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="852ee-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="852ee-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="852ee-134">CommonParameters</span></span>
<span data-ttu-id="852ee-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="852ee-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="852ee-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="852ee-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="852ee-137">輸入</span><span class="sxs-lookup"><span data-stu-id="852ee-137">INPUTS</span></span>

### <span data-ttu-id="852ee-138">System.String</span><span class="sxs-lookup"><span data-stu-id="852ee-138">System.String</span></span>
### <span data-ttu-id="852ee-139">Microsoft.Azure.Commands.SecurityInsights.models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="852ee-139">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="852ee-140">輸出</span><span class="sxs-lookup"><span data-stu-id="852ee-140">OUTPUTS</span></span>

### <span data-ttu-id="852ee-141">Microsoft.Azure.Commands.SecurityInsights.models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="852ee-141">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="852ee-142">筆記</span><span class="sxs-lookup"><span data-stu-id="852ee-142">NOTES</span></span>

## <span data-ttu-id="852ee-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="852ee-143">RELATED LINKS</span></span>
