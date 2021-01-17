---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRule.md
ms.openlocfilehash: 415a4156831d00672aba5709d3f915625adac106
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448532"
---
# <span data-ttu-id="98fa3-101">Remove-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="98fa3-101">Remove-AzSentinelAlertRule</span></span>

## <span data-ttu-id="98fa3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="98fa3-102">SYNOPSIS</span></span>
<span data-ttu-id="98fa3-103">刪除分析。</span><span class="sxs-lookup"><span data-stu-id="98fa3-103">Delete an Analytic.</span></span>

## <span data-ttu-id="98fa3-104">句法</span><span class="sxs-lookup"><span data-stu-id="98fa3-104">SYNTAX</span></span>

### <span data-ttu-id="98fa3-105">AlertRuleId (預設) </span><span class="sxs-lookup"><span data-stu-id="98fa3-105">AlertRuleId (Default)</span></span>
```
Remove-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98fa3-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="98fa3-106">InputObject</span></span>
```
Remove-AzSentinelAlertRule -InputObject <PSSentinelAlertRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98fa3-107">說明</span><span class="sxs-lookup"><span data-stu-id="98fa3-107">DESCRIPTION</span></span>
<span data-ttu-id="98fa3-108">**AzSentinelAlertRule** Cmdlet 會從指定的工作區永久刪除一個警報規則。</span><span class="sxs-lookup"><span data-stu-id="98fa3-108">The **Remove-AzSentinelAlertRule** cmdlet permanently deletes an Alert Rule from a specified workspace.</span></span>
<span data-ttu-id="98fa3-109">您可以使用管線運算子傳遞 **AlertRule** 物件，或者也可以指定所需的參數。</span><span class="sxs-lookup"><span data-stu-id="98fa3-109">You can pass an **AlertRule** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="98fa3-110">您可以使用 Confirm 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="98fa3-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="98fa3-111">示例</span><span class="sxs-lookup"><span data-stu-id="98fa3-111">EXAMPLES</span></span>

### <span data-ttu-id="98fa3-112">範例1</span><span class="sxs-lookup"><span data-stu-id="98fa3-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

<span data-ttu-id="98fa3-113">這個命令會從工作區移除警示規則。</span><span class="sxs-lookup"><span data-stu-id="98fa3-113">This command removes the Alert Rule from the workspace.</span></span>

## <span data-ttu-id="98fa3-114">參數</span><span class="sxs-lookup"><span data-stu-id="98fa3-114">PARAMETERS</span></span>

### <span data-ttu-id="98fa3-115">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="98fa3-115">-AlertRuleId</span></span>
<span data-ttu-id="98fa3-116">[警示規則識別碼]。</span><span class="sxs-lookup"><span data-stu-id="98fa3-116">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98fa3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98fa3-117">-DefaultProfile</span></span>
<span data-ttu-id="98fa3-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="98fa3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98fa3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98fa3-119">-InputObject</span></span>
<span data-ttu-id="98fa3-120">InputObject.</span><span class="sxs-lookup"><span data-stu-id="98fa3-120">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98fa3-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="98fa3-121">-PassThru</span></span>
<span data-ttu-id="98fa3-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="98fa3-122">PassThru</span></span>

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

### <span data-ttu-id="98fa3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98fa3-123">-ResourceGroupName</span></span>
<span data-ttu-id="98fa3-124">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="98fa3-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98fa3-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="98fa3-125">-WorkspaceName</span></span>
<span data-ttu-id="98fa3-126">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="98fa3-126">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98fa3-127">-確認</span><span class="sxs-lookup"><span data-stu-id="98fa3-127">-Confirm</span></span>
<span data-ttu-id="98fa3-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="98fa3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98fa3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98fa3-129">-WhatIf</span></span>
<span data-ttu-id="98fa3-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="98fa3-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98fa3-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="98fa3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98fa3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98fa3-132">CommonParameters</span></span>
<span data-ttu-id="98fa3-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="98fa3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98fa3-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="98fa3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98fa3-135">輸入</span><span class="sxs-lookup"><span data-stu-id="98fa3-135">INPUTS</span></span>

### <span data-ttu-id="98fa3-136">System.object</span><span class="sxs-lookup"><span data-stu-id="98fa3-136">System.String</span></span>
### <span data-ttu-id="98fa3-137">SecurityInsights AlertRules. PSSentinelAlertRule （）</span><span class="sxs-lookup"><span data-stu-id="98fa3-137">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="98fa3-138">輸出</span><span class="sxs-lookup"><span data-stu-id="98fa3-138">OUTPUTS</span></span>

### <span data-ttu-id="98fa3-139">SecurityInsights AlertRules. PSSentinelAlertRule （）</span><span class="sxs-lookup"><span data-stu-id="98fa3-139">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="98fa3-140">筆記</span><span class="sxs-lookup"><span data-stu-id="98fa3-140">NOTES</span></span>

## <span data-ttu-id="98fa3-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="98fa3-141">RELATED LINKS</span></span>
