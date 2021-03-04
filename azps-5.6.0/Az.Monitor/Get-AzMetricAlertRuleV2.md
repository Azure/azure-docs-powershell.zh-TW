---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricAlertRuleV2.md
ms.openlocfilehash: 135451f5e44d8e92511b84766d5be66be3cd7e9a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908909"
---
# <span data-ttu-id="19c65-101">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="19c65-101">Get-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="19c65-102">簡介</span><span class="sxs-lookup"><span data-stu-id="19c65-102">SYNOPSIS</span></span>
<span data-ttu-id="19c65-103">使用非 (標準) 規則來使用 V2</span><span class="sxs-lookup"><span data-stu-id="19c65-103">Gets V2 (non-classic) metric alert rules</span></span>

## <span data-ttu-id="19c65-104">語法</span><span class="sxs-lookup"><span data-stu-id="19c65-104">SYNTAX</span></span>

### <span data-ttu-id="19c65-105">ByResourceGroupName (預設) </span><span class="sxs-lookup"><span data-stu-id="19c65-105">ByResourceGroupName (Default)</span></span>
```
Get-AzMetricAlertRuleV2 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="19c65-106">ByRuleName</span><span class="sxs-lookup"><span data-stu-id="19c65-106">ByRuleName</span></span>
```
Get-AzMetricAlertRuleV2 -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="19c65-107">ByRuleId</span><span class="sxs-lookup"><span data-stu-id="19c65-107">ByRuleId</span></span>
```
Get-AzMetricAlertRuleV2 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19c65-108">描述</span><span class="sxs-lookup"><span data-stu-id="19c65-108">DESCRIPTION</span></span>
<span data-ttu-id="19c65-109">**Get-AzMetricAlertRuleV2** Cmdlet 會依名稱或 URI 或指定資源群組或訂閱的所有計量警示規則，取得公制警示規則。</span><span class="sxs-lookup"><span data-stu-id="19c65-109">The **Get-AzMetricAlertRuleV2** cmdlet gets a metric alert rule by its name or URI, or all metric alert rules from a specified resource group or subscription.</span></span>

## <span data-ttu-id="19c65-110">例子</span><span class="sxs-lookup"><span data-stu-id="19c65-110">EXAMPLES</span></span>

### <span data-ttu-id="19c65-111">範例 1：取得目前訂閱的所有計量警示規則</span><span class="sxs-lookup"><span data-stu-id="19c65-111">Example 1: Get all metric alert rules in current subscription</span></span>
```powershell
PS C:\>Get-AzMetricAlertRuleV2
TargetResourceId     : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricResourceGroup/providers/Microsoft.KeyVault/vaults/GenevaRPKeyVault
Criteria             : {Metric1}
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/sampleresourcegroup/providers/microsoft.insights/actiongroups/scnewactiongroup}
ResourceGroup        : metricResourceGroup
Description          : fdafda
Severity             : 3
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricResourceGroup/providers/Microsoft.KeyVault/vaults/GenevaRPKeyVault}
EvaluationFrequency  : 00:01:00
WindowSize           : 00:05:00
TargetResourceType   :
TargetResourceRegion :
AutoMitigate         :
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricResourceGroup/providers/microsoft.insights/metricAlerts/Rule1
Name                 : Rule1
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 : {}

Criteria             : {Metric1}
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/sampleresourcegroup/providers/microsoft.insights/actiongroups/scnewactiongroup}
ResourceGroup        : SampleResourceGroup
Description          : Testing 1 minute granuarity
Severity             : 3
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/Microsoft.Compute/virtualMachines/SCCMDemo4}
EvaluationFrequency  : 00:01:00
WindowSize           : 00:01:00
TargetResourceType   : Microsoft.Compute/virtualMachines
TargetResourceRegion : eastus
AutoMitigate         : True
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/microsoft.insights/metricAlerts/Rule2
Name                 : Rule2
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 : {}
```

<span data-ttu-id="19c65-112">此命令會獲得目前訂閱中所有公制警示規則。</span><span class="sxs-lookup"><span data-stu-id="19c65-112">This command gets all the metric alert rules in the current subscription.</span></span>

### <span data-ttu-id="19c65-113">範例 2：在資源群組中取得所有計量警示規則</span><span class="sxs-lookup"><span data-stu-id="19c65-113">Example 2: Get all metric alert rules in a resource group</span></span>

```powershell
PS C:\>Get-AzMetricAlertRuleV2 -ResourceGroupName metricAlertsRG
Criteria             : {Metric1}
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/pr
                       oviders/microsoft.insights/actiongroups/emails}
ResourceGroup        : metricAlertsRG
Description          : Test Classic VM alert - CPU Usage
Severity             : 3
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertsRG/providers/Micr
                       osoft.ClassicCompute/virtualMachines/VM1}
EvaluationFrequency  : 00:01:00
WindowSize           : 00:05:00
TargetResourceType   : Microsoft.ClassicCompute/virtualMachines
TargetResourceRegion : southcentralus
AutoMitigate         : True
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertsRG/providers/micro
                       soft.insights/metricAlerts/Test%20Classic%20VM%20alert%20-%20CPU%20Usage
Name                 : Test Classic VM alert - CPU Usage
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 : {}
```

<span data-ttu-id="19c65-114">此命令會獲得資源群組中名為 metricAlertsRG 的所有計量警示規則。</span><span class="sxs-lookup"><span data-stu-id="19c65-114">This command gets all the metric alert rules in the resource group named metricAlertsRG.</span></span>

### <span data-ttu-id="19c65-115">範例 3：依名稱取得公制警示規則</span><span class="sxs-lookup"><span data-stu-id="19c65-115">Example 3: Get a metric alert rule by name</span></span>

```powershell
PS C:\> Get-AzMetricAlertRuleV2 -ResourceGroupName metricAlertsRG -Name PS3182019

Criteria             : {metric1}
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/demo}
ResourceGroup        : metricAlertsRG
Description          : This is description 
Severity             : 1
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertsRG/providers/Microsoft.Compute/virtualMachines/VM1,
                       /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertsRG/providers/Microsoft.Compute/virtualMachines/VM2}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   : Microsoft.Compute/virtualMachines
TargetResourceRegion : eastus
AutoMitigate         :
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertsRG/providers/Microsoft.Insights/metricAlerts/PS3182019
Name                 : PS3182019
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="19c65-116">此命令在名為 metricAlertsRG 的資源群組中，會獲得名為 PS3182019 的公制警示規則。</span><span class="sxs-lookup"><span data-stu-id="19c65-116">This command gets the metric alert rule named PS3182019 in the resource group named metricAlertsRG.</span></span>

### <span data-ttu-id="19c65-117">範例 4：依 ruleID 取得公制警示規則</span><span class="sxs-lookup"><span data-stu-id="19c65-117">Example 4: Get a metric alert rule by ruleID</span></span>

```powershell
PS C:\>Get-AzMetricAlertRuleV2 -ResourceId /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/microsoft.insights/metricAlerts/MyMetricAlertRule
TargetResourceId     : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/microsoft.insights/components/alertstestFunction
Criteria             : {Metric1}
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/emails}
ResourceGroup        : SampleResourceGroup
Description          : Test Description
Severity             : 3
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/microsoft.insights/components/alertstestFunction}
EvaluationFrequency  : 00:01:00
WindowSize           : 00:05:00
TargetResourceType   : 
TargetResourceRegion : 
AutoMitigate         : 
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/SampleResourceGroup/providers/microsoft.insights/metricAlerts/MyMetricAlertRule
Name                 : MyMetricAlertRule
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="19c65-118">此命令會獲得具有給定資源識別碼的公制警示規則。</span><span class="sxs-lookup"><span data-stu-id="19c65-118">This command gets the metric alert rule with the given resource ID.</span></span>

## <span data-ttu-id="19c65-119">參數</span><span class="sxs-lookup"><span data-stu-id="19c65-119">PARAMETERS</span></span>

### <span data-ttu-id="19c65-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19c65-120">-DefaultProfile</span></span>
<span data-ttu-id="19c65-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="19c65-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19c65-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="19c65-122">-Name</span></span>
<span data-ttu-id="19c65-123">公制警示規則的名稱</span><span class="sxs-lookup"><span data-stu-id="19c65-123">The Name of metric alert rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c65-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19c65-124">-ResourceGroupName</span></span>
<span data-ttu-id="19c65-125">The ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19c65-125">The ResourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupName
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c65-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="19c65-126">-ResourceId</span></span>
<span data-ttu-id="19c65-127">公制警示規則的規則識別碼</span><span class="sxs-lookup"><span data-stu-id="19c65-127">The Rule Id of metric alert rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19c65-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19c65-128">CommonParameters</span></span>
<span data-ttu-id="19c65-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="19c65-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19c65-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19c65-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19c65-131">輸入</span><span class="sxs-lookup"><span data-stu-id="19c65-131">INPUTS</span></span>

### <span data-ttu-id="19c65-132">System.String</span><span class="sxs-lookup"><span data-stu-id="19c65-132">System.String</span></span>

## <span data-ttu-id="19c65-133">輸出</span><span class="sxs-lookup"><span data-stu-id="19c65-133">OUTPUTS</span></span>

### <span data-ttu-id="19c65-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="19c65-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="19c65-135">筆記</span><span class="sxs-lookup"><span data-stu-id="19c65-135">NOTES</span></span>

## <span data-ttu-id="19c65-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="19c65-136">RELATED LINKS</span></span>
