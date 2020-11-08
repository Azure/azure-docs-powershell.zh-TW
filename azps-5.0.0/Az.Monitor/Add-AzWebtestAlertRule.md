---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: FBAE5F75-1E28-4F1C-A9ED-20075FFD4AC7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azwebtestalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzWebtestAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzWebtestAlertRule.md
ms.openlocfilehash: 043bb0e0b3c5fac61407eaca3d20c82ebe483037
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141502"
---
# <span data-ttu-id="8e7ab-101">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="8e7ab-101">Add-AzWebtestAlertRule</span></span>

## <span data-ttu-id="8e7ab-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8e7ab-102">SYNOPSIS</span></span>
<span data-ttu-id="8e7ab-103">新增或更新 webtest 提醒規則。</span><span class="sxs-lookup"><span data-stu-id="8e7ab-103">Adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="8e7ab-104">句法</span><span class="sxs-lookup"><span data-stu-id="8e7ab-104">SYNTAX</span></span>

```
Add-AzWebtestAlertRule -MetricName <String> -TargetResourceUri <String> -WindowSize <TimeSpan>
 -FailedLocationCount <Int32> [-MetricNamespace <String>] -Location <String> [-Description <String>]
 [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e7ab-105">說明</span><span class="sxs-lookup"><span data-stu-id="8e7ab-105">DESCRIPTION</span></span>
<span data-ttu-id="8e7ab-106">**AzWebtestAlertRule** Cmdlet 會新增或更新公制、event 或 webtest 類型的警示規則。</span><span class="sxs-lookup"><span data-stu-id="8e7ab-106">The **Add-AzWebtestAlertRule** cmdlet adds or updates an alert rule of either metric, event, or webtest type.</span></span>
<span data-ttu-id="8e7ab-107">新增的規則會與資源群組相關聯，且具有名稱。</span><span class="sxs-lookup"><span data-stu-id="8e7ab-107">The added rule is associated to a resource group and has a name.</span></span>
<span data-ttu-id="8e7ab-108">這個 Cmdlet 會實現 ShouldProcess 模式，亦即，在實際建立、修改或移除資源之前，它可能會要求使用者進行確認。</span><span class="sxs-lookup"><span data-stu-id="8e7ab-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="8e7ab-109">示例</span><span class="sxs-lookup"><span data-stu-id="8e7ab-109">EXAMPLES</span></span>

### <span data-ttu-id="8e7ab-110">範例1：新增 webtest 警示規則</span><span class="sxs-lookup"><span data-stu-id="8e7ab-110">Example 1: Add a webtest alert rule</span></span>
```
PS C:\>Add-AzWebtestAlertRule -Name "webtestRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -WindowSize 00:05:00 -MetricName "metric" -TargetResourceUri "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourcegroups/Default-Web-WestUS/providers/microsoft.insights/webtests/leowebtestr1-webtestr1" -Description "Nice Webtest rule" -Failed 3
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="8e7ab-111">這個命令會新增或更新 webtest 警示規則。</span><span class="sxs-lookup"><span data-stu-id="8e7ab-111">This command adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="8e7ab-112">參數</span><span class="sxs-lookup"><span data-stu-id="8e7ab-112">PARAMETERS</span></span>

### <span data-ttu-id="8e7ab-113">-動作</span><span class="sxs-lookup"><span data-stu-id="8e7ab-113">-Action</span></span>
<span data-ttu-id="8e7ab-114">指定以逗號分隔的動作清單。</span><span class="sxs-lookup"><span data-stu-id="8e7ab-114">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="8e7ab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e7ab-115">-DefaultProfile</span></span>
<span data-ttu-id="8e7ab-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="8e7ab-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e7ab-117">-描述</span><span class="sxs-lookup"><span data-stu-id="8e7ab-117">-Description</span></span>
<span data-ttu-id="8e7ab-118">指定規則的描述。</span><span class="sxs-lookup"><span data-stu-id="8e7ab-118">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="8e7ab-119">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="8e7ab-119">-DisableRule</span></span>
<span data-ttu-id="8e7ab-120">停用規則。</span><span class="sxs-lookup"><span data-stu-id="8e7ab-120">Disables the rule.</span></span>
<span data-ttu-id="8e7ab-121">如果您沒有指定此參數，則會啟用規則。</span><span class="sxs-lookup"><span data-stu-id="8e7ab-121">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="8e7ab-122">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="8e7ab-122">-FailedLocationCount</span></span>
<span data-ttu-id="8e7ab-123">指定 webtest 規則的失敗位置計數。</span><span class="sxs-lookup"><span data-stu-id="8e7ab-123">Specifies the failed location count for the webtest rules.</span></span>
<span data-ttu-id="8e7ab-124">這與其他規則類型中的閾值類似。</span><span class="sxs-lookup"><span data-stu-id="8e7ab-124">This is similar to the threshold in the other types of rules.</span></span>

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

### <span data-ttu-id="8e7ab-125">-位置</span><span class="sxs-lookup"><span data-stu-id="8e7ab-125">-Location</span></span>
<span data-ttu-id="8e7ab-126">指定定義規則的位置。</span><span class="sxs-lookup"><span data-stu-id="8e7ab-126">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="8e7ab-127">-MetricName</span><span class="sxs-lookup"><span data-stu-id="8e7ab-127">-MetricName</span></span>
<span data-ttu-id="8e7ab-128">指定度量值的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e7ab-128">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="8e7ab-129">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="8e7ab-129">-MetricNamespace</span></span>
<span data-ttu-id="8e7ab-130">指定規則的度量命名空間。</span><span class="sxs-lookup"><span data-stu-id="8e7ab-130">Specifies the metric namespace for rule.</span></span>

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

### <span data-ttu-id="8e7ab-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="8e7ab-131">-Name</span></span>
<span data-ttu-id="8e7ab-132">指定規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e7ab-132">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="8e7ab-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e7ab-133">-ResourceGroupName</span></span>
<span data-ttu-id="8e7ab-134">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e7ab-134">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="8e7ab-135">-TargetResourceUri</span><span class="sxs-lookup"><span data-stu-id="8e7ab-135">-TargetResourceUri</span></span>
<span data-ttu-id="8e7ab-136">指定 webtest 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8e7ab-136">Specifies the resource ID of the webtest.</span></span>

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

### <span data-ttu-id="8e7ab-137">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="8e7ab-137">-WindowSize</span></span>
<span data-ttu-id="8e7ab-138">指定規則計算其資料的時間視窗大小。</span><span class="sxs-lookup"><span data-stu-id="8e7ab-138">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="8e7ab-139">-確認</span><span class="sxs-lookup"><span data-stu-id="8e7ab-139">-Confirm</span></span>
<span data-ttu-id="8e7ab-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8e7ab-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e7ab-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e7ab-141">-WhatIf</span></span>
<span data-ttu-id="8e7ab-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8e7ab-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e7ab-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8e7ab-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e7ab-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e7ab-144">CommonParameters</span></span>
<span data-ttu-id="8e7ab-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8e7ab-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e7ab-146">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8e7ab-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e7ab-147">輸入</span><span class="sxs-lookup"><span data-stu-id="8e7ab-147">INPUTS</span></span>

### <span data-ttu-id="8e7ab-148">System.object</span><span class="sxs-lookup"><span data-stu-id="8e7ab-148">System.String</span></span>

### <span data-ttu-id="8e7ab-149">System.object</span><span class="sxs-lookup"><span data-stu-id="8e7ab-149">System.TimeSpan</span></span>

### <span data-ttu-id="8e7ab-150">System.object</span><span class="sxs-lookup"><span data-stu-id="8e7ab-150">System.Int32</span></span>

### <span data-ttu-id="8e7ab-151">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="8e7ab-151">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="8e7ab-152">[System.object]。清單 ' 1 [[Microsoft...... 監視器、版本 = 1.0.0.0、Culture = 中性、PublicKeyToken = null]」。）））</span><span class="sxs-lookup"><span data-stu-id="8e7ab-152">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="8e7ab-153">輸出</span><span class="sxs-lookup"><span data-stu-id="8e7ab-153">OUTPUTS</span></span>

### <span data-ttu-id="8e7ab-154">PSAddAlertRuleOperationResponse 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="8e7ab-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="8e7ab-155">筆記</span><span class="sxs-lookup"><span data-stu-id="8e7ab-155">NOTES</span></span>

## <span data-ttu-id="8e7ab-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="8e7ab-156">RELATED LINKS</span></span>

[<span data-ttu-id="8e7ab-157">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="8e7ab-157">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="8e7ab-158">附加 AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="8e7ab-158">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="8e7ab-159">AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="8e7ab-159">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="8e7ab-160">新-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="8e7ab-160">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


