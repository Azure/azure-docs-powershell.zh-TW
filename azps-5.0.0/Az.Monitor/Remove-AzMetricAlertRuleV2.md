---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
ms.openlocfilehash: d2b34063f5ece370d52b8a4c3c0dab35cff77c54
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141348"
---
# <span data-ttu-id="26e28-101">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="26e28-101">Remove-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="26e28-102">摘要</span><span class="sxs-lookup"><span data-stu-id="26e28-102">SYNOPSIS</span></span>
<span data-ttu-id="26e28-103">移除 V2 (非傳統) 標準警示規則。</span><span class="sxs-lookup"><span data-stu-id="26e28-103">Removes a V2 (non-classic) metric alert rule.</span></span>

## <span data-ttu-id="26e28-104">句法</span><span class="sxs-lookup"><span data-stu-id="26e28-104">SYNTAX</span></span>

### <span data-ttu-id="26e28-105">ByMetricRuleResourceName (預設) </span><span class="sxs-lookup"><span data-stu-id="26e28-105">ByMetricRuleResourceName (Default)</span></span>
```
Remove-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26e28-106">ByMetricRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="26e28-106">ByMetricRuleResourceId</span></span>
```
Remove-AzMetricAlertRuleV2 -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26e28-107">ByRuleObject</span><span class="sxs-lookup"><span data-stu-id="26e28-107">ByRuleObject</span></span>
```
Remove-AzMetricAlertRuleV2 -InputObject <PSMetricAlertRuleV2> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26e28-108">說明</span><span class="sxs-lookup"><span data-stu-id="26e28-108">DESCRIPTION</span></span>
<span data-ttu-id="26e28-109">**AzMetricAlertRuleV2** Cmdlet 會移除警示規則。</span><span class="sxs-lookup"><span data-stu-id="26e28-109">The **Remove-AzMetricAlertRuleV2** cmdlet removes an alert rule.</span></span> <span data-ttu-id="26e28-110">這個 Cmdlet 會實現 ShouldProcess 模式，亦即，在實際建立、修改或移除資源之前，它可能會要求使用者進行確認。</span><span class="sxs-lookup"><span data-stu-id="26e28-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="26e28-111">示例</span><span class="sxs-lookup"><span data-stu-id="26e28-111">EXAMPLES</span></span>

### <span data-ttu-id="26e28-112">範例1：依名稱移除警示規則</span><span class="sxs-lookup"><span data-stu-id="26e28-112">Example 1: Remove an alert rule by name</span></span>

```powershell
PS C:\> Remove-AzMetricAlertRuleV2 -ResourceGroupName xxxxRG -Name PsSdk -PassThru
True
```

<span data-ttu-id="26e28-113">這個命令會移除名為 PsSdk 的警示規則</span><span class="sxs-lookup"><span data-stu-id="26e28-113">This command removes the alert rule named PsSdk</span></span>

### <span data-ttu-id="26e28-114">範例2：依識別碼移除警示規則</span><span class="sxs-lookup"><span data-stu-id="26e28-114">Example 2: Remove an alert rule by ID</span></span>

```powershell
PS C:\>Remove-AzMetricAlertRuleV2 -ResourceId /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule
```

<span data-ttu-id="26e28-115">這個命令會移除含資源識別碼的警示規則 `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span><span class="sxs-lookup"><span data-stu-id="26e28-115">This command removes the alert rule with resource ID `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span></span>

### <span data-ttu-id="26e28-116">範例3：取得並移除提醒</span><span class="sxs-lookup"><span data-stu-id="26e28-116">Example 3: Get an alert and remove it</span></span>

```powershell
PS c:\>Get-AzMetricAlertRuleV2 -ResourceGroupName alertstest -Name sampleAlertRule |Remove-AzMetricAlertRuleV2
```

<span data-ttu-id="26e28-117">這個命令會取得警報並將它移除。</span><span class="sxs-lookup"><span data-stu-id="26e28-117">This command gets an alert and removes it.</span></span>

## <span data-ttu-id="26e28-118">參數</span><span class="sxs-lookup"><span data-stu-id="26e28-118">PARAMETERS</span></span>

### <span data-ttu-id="26e28-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="26e28-119">-AsJob</span></span>
<span data-ttu-id="26e28-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="26e28-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="26e28-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26e28-121">-DefaultProfile</span></span>
<span data-ttu-id="26e28-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="26e28-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26e28-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26e28-123">-InputObject</span></span>
<span data-ttu-id="26e28-124">公制規則物件</span><span class="sxs-lookup"><span data-stu-id="26e28-124">The Metric rule object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2
Parameter Sets: ByRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26e28-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="26e28-125">-Name</span></span>
<span data-ttu-id="26e28-126">公制警報規則的名稱</span><span class="sxs-lookup"><span data-stu-id="26e28-126">The name of metric alert rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByMetricRuleResourceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26e28-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26e28-127">-PassThru</span></span>
<span data-ttu-id="26e28-128">成功刪除時，傳回 true。</span><span class="sxs-lookup"><span data-stu-id="26e28-128">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="26e28-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26e28-129">-ResourceGroupName</span></span>
<span data-ttu-id="26e28-130">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26e28-130">The ResourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: ByMetricRuleResourceName
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26e28-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26e28-131">-ResourceId</span></span>
<span data-ttu-id="26e28-132">RuleResourceId</span><span class="sxs-lookup"><span data-stu-id="26e28-132">The RuleResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByMetricRuleResourceId
Aliases: RuleResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26e28-133">-確認</span><span class="sxs-lookup"><span data-stu-id="26e28-133">-Confirm</span></span>
<span data-ttu-id="26e28-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="26e28-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26e28-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26e28-135">-WhatIf</span></span>
<span data-ttu-id="26e28-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="26e28-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26e28-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="26e28-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26e28-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26e28-138">CommonParameters</span></span>
<span data-ttu-id="26e28-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="26e28-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26e28-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="26e28-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26e28-141">輸入</span><span class="sxs-lookup"><span data-stu-id="26e28-141">INPUTS</span></span>

### <span data-ttu-id="26e28-142">System.object</span><span class="sxs-lookup"><span data-stu-id="26e28-142">System.String</span></span>

### <span data-ttu-id="26e28-143">PSMetricAlertRuleV2 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="26e28-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="26e28-144">輸出</span><span class="sxs-lookup"><span data-stu-id="26e28-144">OUTPUTS</span></span>

### <span data-ttu-id="26e28-145">System.object</span><span class="sxs-lookup"><span data-stu-id="26e28-145">System.Boolean</span></span>

## <span data-ttu-id="26e28-146">筆記</span><span class="sxs-lookup"><span data-stu-id="26e28-146">NOTES</span></span>

## <span data-ttu-id="26e28-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="26e28-147">RELATED LINKS</span></span>
