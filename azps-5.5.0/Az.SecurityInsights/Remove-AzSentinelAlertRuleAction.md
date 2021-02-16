---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 48566fde735deb5693783f9e71f047f73d5f9336
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100139870"
---
# <span data-ttu-id="fbe39-101">Remove-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="fbe39-101">Remove-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="fbe39-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fbe39-102">SYNOPSIS</span></span>
<span data-ttu-id="fbe39-103">移除分析的自動回應。</span><span class="sxs-lookup"><span data-stu-id="fbe39-103">Remove an Automated Response from an Analytic.</span></span>

## <span data-ttu-id="fbe39-104">句法</span><span class="sxs-lookup"><span data-stu-id="fbe39-104">SYNTAX</span></span>

### <span data-ttu-id="fbe39-105">ActionId (預設) </span><span class="sxs-lookup"><span data-stu-id="fbe39-105">ActionId (Default)</span></span>
```
Remove-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fbe39-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="fbe39-106">InputObject</span></span>
```
Remove-AzSentinelAlertRuleAction -InputObject <PSSentinelActionResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbe39-107">說明</span><span class="sxs-lookup"><span data-stu-id="fbe39-107">DESCRIPTION</span></span>
<span data-ttu-id="fbe39-108">**AzSentinelAlertRuleAction** Cmdlet 會永久刪除指定工作區中警示規則的自動回應。</span><span class="sxs-lookup"><span data-stu-id="fbe39-108">The **Remove-AzSentinelAlertRuleAction** cmdlet permanently deletes an Automated Response from the Alert Rule in a specified workspace.</span></span>
<span data-ttu-id="fbe39-109">您可以使用管線運算子傳遞 **AlertRuleAction** 物件，或者也可以指定所需的參數。</span><span class="sxs-lookup"><span data-stu-id="fbe39-109">You can pass an **AlertRuleAction** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="fbe39-110">您可以使用 Confirm 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fbe39-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="fbe39-111">示例</span><span class="sxs-lookup"><span data-stu-id="fbe39-111">EXAMPLES</span></span>

### <span data-ttu-id="fbe39-112">範例1</span><span class="sxs-lookup"><span data-stu-id="fbe39-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
```

<span data-ttu-id="fbe39-113">這個命令會從工作區移除警示規則。</span><span class="sxs-lookup"><span data-stu-id="fbe39-113">This command removes the Alert Rule from the workspace.</span></span>

## <span data-ttu-id="fbe39-114">參數</span><span class="sxs-lookup"><span data-stu-id="fbe39-114">PARAMETERS</span></span>

### <span data-ttu-id="fbe39-115">-ActionId</span><span class="sxs-lookup"><span data-stu-id="fbe39-115">-ActionId</span></span>
<span data-ttu-id="fbe39-116">[動作識別碼]。</span><span class="sxs-lookup"><span data-stu-id="fbe39-116">Action Id.</span></span>

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

### <span data-ttu-id="fbe39-117">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="fbe39-117">-AlertRuleId</span></span>
<span data-ttu-id="fbe39-118">[警示規則識別碼]。</span><span class="sxs-lookup"><span data-stu-id="fbe39-118">Alert Rule Id.</span></span>

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

### <span data-ttu-id="fbe39-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbe39-119">-DefaultProfile</span></span>
<span data-ttu-id="fbe39-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fbe39-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbe39-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fbe39-121">-InputObject</span></span>
<span data-ttu-id="fbe39-122">InputObject.</span><span class="sxs-lookup"><span data-stu-id="fbe39-122">InputObject.</span></span>

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

### <span data-ttu-id="fbe39-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fbe39-123">-PassThru</span></span>
<span data-ttu-id="fbe39-124">PassThru</span><span class="sxs-lookup"><span data-stu-id="fbe39-124">PassThru</span></span>

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

### <span data-ttu-id="fbe39-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbe39-125">-ResourceGroupName</span></span>
<span data-ttu-id="fbe39-126">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="fbe39-126">Resource group name.</span></span>

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

### <span data-ttu-id="fbe39-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fbe39-127">-WorkspaceName</span></span>
<span data-ttu-id="fbe39-128">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="fbe39-128">Workspace Name.</span></span>

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

### <span data-ttu-id="fbe39-129">-確認</span><span class="sxs-lookup"><span data-stu-id="fbe39-129">-Confirm</span></span>
<span data-ttu-id="fbe39-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fbe39-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbe39-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbe39-131">-WhatIf</span></span>
<span data-ttu-id="fbe39-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fbe39-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbe39-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fbe39-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbe39-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbe39-134">CommonParameters</span></span>
<span data-ttu-id="fbe39-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fbe39-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbe39-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fbe39-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbe39-137">輸入</span><span class="sxs-lookup"><span data-stu-id="fbe39-137">INPUTS</span></span>

### <span data-ttu-id="fbe39-138">System.object</span><span class="sxs-lookup"><span data-stu-id="fbe39-138">System.String</span></span>
### <span data-ttu-id="fbe39-139">PSSentinelActionResponse 中的 SecurityInsights.。</span><span class="sxs-lookup"><span data-stu-id="fbe39-139">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="fbe39-140">輸出</span><span class="sxs-lookup"><span data-stu-id="fbe39-140">OUTPUTS</span></span>

### <span data-ttu-id="fbe39-141">PSSentinelActionResponse 中的 SecurityInsights.。</span><span class="sxs-lookup"><span data-stu-id="fbe39-141">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="fbe39-142">筆記</span><span class="sxs-lookup"><span data-stu-id="fbe39-142">NOTES</span></span>

## <span data-ttu-id="fbe39-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="fbe39-143">RELATED LINKS</span></span>
