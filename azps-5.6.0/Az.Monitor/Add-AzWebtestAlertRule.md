---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: FBAE5F75-1E28-4F1C-A9ED-20075FFD4AC7
online version: https://docs.microsoft.com/powershell/module/az.monitor/add-azwebtestalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzWebtestAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzWebtestAlertRule.md
ms.openlocfilehash: 8f66117d4ae2909617a6215c1c154ba22d469b21
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908986"
---
# <span data-ttu-id="8172e-101">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="8172e-101">Add-AzWebtestAlertRule</span></span>

## <span data-ttu-id="8172e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8172e-102">SYNOPSIS</span></span>
<span data-ttu-id="8172e-103">新增或更新 Webtest 警示規則。</span><span class="sxs-lookup"><span data-stu-id="8172e-103">Adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="8172e-104">語法</span><span class="sxs-lookup"><span data-stu-id="8172e-104">SYNTAX</span></span>

```
Add-AzWebtestAlertRule -MetricName <String> -TargetResourceUri <String> -WindowSize <TimeSpan>
 -FailedLocationCount <Int32> [-MetricNamespace <String>] -Location <String> [-Description <String>]
 [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8172e-105">描述</span><span class="sxs-lookup"><span data-stu-id="8172e-105">DESCRIPTION</span></span>
<span data-ttu-id="8172e-106">**Add-AzWebtestAlertRule** Cmdlet 會新增或更新公制、事件或 Webtest 類型的警示規則。</span><span class="sxs-lookup"><span data-stu-id="8172e-106">The **Add-AzWebtestAlertRule** cmdlet adds or updates an alert rule of either metric, event, or webtest type.</span></span>
<span data-ttu-id="8172e-107">新增的規則與資源群組相關聯，而且有名稱。</span><span class="sxs-lookup"><span data-stu-id="8172e-107">The added rule is associated to a resource group and has a name.</span></span>
<span data-ttu-id="8172e-108">此 Cmdlet 實做 ShouldProcess 模式，即實際建立、修改或移除資源之前，可能會向使用者要求確認。</span><span class="sxs-lookup"><span data-stu-id="8172e-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="8172e-109">例子</span><span class="sxs-lookup"><span data-stu-id="8172e-109">EXAMPLES</span></span>

### <span data-ttu-id="8172e-110">範例 1：新增 Webtest 警示規則</span><span class="sxs-lookup"><span data-stu-id="8172e-110">Example 1: Add a webtest alert rule</span></span>
```
PS C:\>Add-AzWebtestAlertRule -Name "webtestRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -WindowSize 00:05:00 -MetricName "metric" -TargetResourceUri "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourcegroups/Default-Web-WestUS/providers/microsoft.insights/webtests/leowebtestr1-webtestr1" -Description "Nice Webtest rule" -Failed 3
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="8172e-111">此命令會新增或更新 WebTest 警示規則。</span><span class="sxs-lookup"><span data-stu-id="8172e-111">This command adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="8172e-112">參數</span><span class="sxs-lookup"><span data-stu-id="8172e-112">PARAMETERS</span></span>

### <span data-ttu-id="8172e-113">-動作</span><span class="sxs-lookup"><span data-stu-id="8172e-113">-Action</span></span>
<span data-ttu-id="8172e-114">指定以逗號分隔的動作清單。</span><span class="sxs-lookup"><span data-stu-id="8172e-114">Specifies a comma-separated list of actions.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8172e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8172e-115">-DefaultProfile</span></span>
<span data-ttu-id="8172e-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="8172e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8172e-117">-描述</span><span class="sxs-lookup"><span data-stu-id="8172e-117">-Description</span></span>
<span data-ttu-id="8172e-118">指定規則的描述。</span><span class="sxs-lookup"><span data-stu-id="8172e-118">Specifies a description of the rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8172e-119">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="8172e-119">-DisableRule</span></span>
<span data-ttu-id="8172e-120">停用規則。</span><span class="sxs-lookup"><span data-stu-id="8172e-120">Disables the rule.</span></span>
<span data-ttu-id="8172e-121">如果您未指定此參數，則規則會啟用。</span><span class="sxs-lookup"><span data-stu-id="8172e-121">If you do not specify this parameter, the rule is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8172e-122">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="8172e-122">-FailedLocationCount</span></span>
<span data-ttu-id="8172e-123">指定 Webtest 規則的失敗位置計數。</span><span class="sxs-lookup"><span data-stu-id="8172e-123">Specifies the failed location count for the webtest rules.</span></span>
<span data-ttu-id="8172e-124">這類似于其他類型的規則中的閾值。</span><span class="sxs-lookup"><span data-stu-id="8172e-124">This is similar to the threshold in the other types of rules.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8172e-125">-位置</span><span class="sxs-lookup"><span data-stu-id="8172e-125">-Location</span></span>
<span data-ttu-id="8172e-126">指定定義規則的位置。</span><span class="sxs-lookup"><span data-stu-id="8172e-126">Specifies the location where the rule is defined.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8172e-127">-MetricName</span><span class="sxs-lookup"><span data-stu-id="8172e-127">-MetricName</span></span>
<span data-ttu-id="8172e-128">指定度量的名稱。</span><span class="sxs-lookup"><span data-stu-id="8172e-128">Specifies the name of the metric.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8172e-129">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="8172e-129">-MetricNamespace</span></span>
<span data-ttu-id="8172e-130">指定規則的公制命名空間。</span><span class="sxs-lookup"><span data-stu-id="8172e-130">Specifies the metric namespace for rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8172e-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="8172e-131">-Name</span></span>
<span data-ttu-id="8172e-132">指定規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="8172e-132">Specifies the name of the rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8172e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8172e-133">-ResourceGroupName</span></span>
<span data-ttu-id="8172e-134">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8172e-134">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8172e-135">-TargetResourceUri</span><span class="sxs-lookup"><span data-stu-id="8172e-135">-TargetResourceUri</span></span>
<span data-ttu-id="8172e-136">指定 Webtest 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8172e-136">Specifies the resource ID of the webtest.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8172e-137">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="8172e-137">-WindowSize</span></span>
<span data-ttu-id="8172e-138">指定規則計算其資料的時段大小。</span><span class="sxs-lookup"><span data-stu-id="8172e-138">Specifies the time window size for the rule to compute its data.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8172e-139">-確認</span><span class="sxs-lookup"><span data-stu-id="8172e-139">-Confirm</span></span>
<span data-ttu-id="8172e-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8172e-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8172e-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8172e-141">-WhatIf</span></span>
<span data-ttu-id="8172e-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8172e-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8172e-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8172e-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8172e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8172e-144">CommonParameters</span></span>
<span data-ttu-id="8172e-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8172e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8172e-146">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8172e-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8172e-147">輸入</span><span class="sxs-lookup"><span data-stu-id="8172e-147">INPUTS</span></span>

### <span data-ttu-id="8172e-148">System.String</span><span class="sxs-lookup"><span data-stu-id="8172e-148">System.String</span></span>

### <span data-ttu-id="8172e-149">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="8172e-149">System.TimeSpan</span></span>

### <span data-ttu-id="8172e-150">System.Int32</span><span class="sxs-lookup"><span data-stu-id="8172e-150">System.Int32</span></span>

### <span data-ttu-id="8172e-151">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8172e-151">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="8172e-152">System.Collections.generic.List'1[[Microsoft.Azure.management.Monitor.management.models.RuleAction，Microsoft.Azure.PowerShell.Cmdlets.Monitor， Version=1.0.0.0， Culture=neutral， PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="8172e-152">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="8172e-153">輸出</span><span class="sxs-lookup"><span data-stu-id="8172e-153">OUTPUTS</span></span>

### <span data-ttu-id="8172e-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="8172e-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="8172e-155">筆記</span><span class="sxs-lookup"><span data-stu-id="8172e-155">NOTES</span></span>

## <span data-ttu-id="8172e-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="8172e-156">RELATED LINKS</span></span>

[<span data-ttu-id="8172e-157">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="8172e-157">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="8172e-158">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="8172e-158">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="8172e-159">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="8172e-159">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="8172e-160">New-AzAlertRuleWeb一體式</span><span class="sxs-lookup"><span data-stu-id="8172e-160">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


