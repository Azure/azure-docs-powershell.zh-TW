---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricAlertRuleV2.md
ms.openlocfilehash: f792452202a33b23bde2153ba781456d7c8c7094
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93786721"
---
# <span data-ttu-id="7e5c8-101">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="7e5c8-101">Get-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="7e5c8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7e5c8-102">SYNOPSIS</span></span>
<span data-ttu-id="7e5c8-103">取得 V2 (非傳統) 標準警示規則</span><span class="sxs-lookup"><span data-stu-id="7e5c8-103">Gets V2 (non-classic) metric alert rules</span></span>

## <span data-ttu-id="7e5c8-104">句法</span><span class="sxs-lookup"><span data-stu-id="7e5c8-104">SYNTAX</span></span>

### <span data-ttu-id="7e5c8-105">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e5c8-105">ByResourceGroupName</span></span>
```
Get-AzMetricAlertRuleV2 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7e5c8-106">ByRuleName</span><span class="sxs-lookup"><span data-stu-id="7e5c8-106">ByRuleName</span></span>
```
Get-AzMetricAlertRuleV2 -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7e5c8-107">ByRuleId</span><span class="sxs-lookup"><span data-stu-id="7e5c8-107">ByRuleId</span></span>
```
Get-AzMetricAlertRuleV2 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e5c8-108">說明</span><span class="sxs-lookup"><span data-stu-id="7e5c8-108">DESCRIPTION</span></span>
<span data-ttu-id="7e5c8-109">AzMetricAlertRuleV2 Cmdlet 會根據其名稱或 URI，或從指定的資源群組或訂閱取得所有度量警報規則，來 **取得** 度量警報規則。</span><span class="sxs-lookup"><span data-stu-id="7e5c8-109">The **Get-AzMetricAlertRuleV2** cmdlet gets a metric alert rule by its name or URI, or all metric alert rules from a specified resource group or subscription.</span></span>

## <span data-ttu-id="7e5c8-110">示例</span><span class="sxs-lookup"><span data-stu-id="7e5c8-110">EXAMPLES</span></span>
### <span data-ttu-id="7e5c8-111">範例1：取得目前訂閱中的所有度量警報規則</span><span class="sxs-lookup"><span data-stu-id="7e5c8-111">Example 1: Get all metric alert rules in current subscription</span></span>
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

<span data-ttu-id="7e5c8-112">這個命令會取得目前訂閱中的所有度量警報規則。</span><span class="sxs-lookup"><span data-stu-id="7e5c8-112">This command gets all the metric alert rules in the current subscription.</span></span>


### <span data-ttu-id="7e5c8-113">範例2：取得資源群組中的所有度量警報規則</span><span class="sxs-lookup"><span data-stu-id="7e5c8-113">Example 2: Get all metric alert rules in a resource group</span></span>

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
<span data-ttu-id="7e5c8-114">這個命令會取得名為 metricAlertsRG 的資源群組中的所有度量警報規則。</span><span class="sxs-lookup"><span data-stu-id="7e5c8-114">This command gets all the metric alert rules in the resource group named metricAlertsRG.</span></span>

### <span data-ttu-id="7e5c8-115">範例3：依名稱取得度量警示規則</span><span class="sxs-lookup"><span data-stu-id="7e5c8-115">Example 3: Get a metric alert rule by name</span></span>

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

<span data-ttu-id="7e5c8-116">這個命令會在名為 metricAlertsRG 的資源群組中，取得名為 PS3182019 的度量警示規則。</span><span class="sxs-lookup"><span data-stu-id="7e5c8-116">This command gets the metric alert rule named PS3182019 in the resource group named metricAlertsRG.</span></span>

### <span data-ttu-id="7e5c8-117">範例4：透過 ruleID 取得度量警示規則</span><span class="sxs-lookup"><span data-stu-id="7e5c8-117">Example 4: Get a metric alert rule by ruleID</span></span>

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

<span data-ttu-id="7e5c8-118">這個命令會取得具有指定資源識別碼的度量警報規則。</span><span class="sxs-lookup"><span data-stu-id="7e5c8-118">This command gets the metric alert rule with the given resource ID.</span></span>

## <span data-ttu-id="7e5c8-119">參數</span><span class="sxs-lookup"><span data-stu-id="7e5c8-119">PARAMETERS</span></span>

### <span data-ttu-id="7e5c8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e5c8-120">-DefaultProfile</span></span>
<span data-ttu-id="7e5c8-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7e5c8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e5c8-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="7e5c8-122">-Name</span></span>
<span data-ttu-id="7e5c8-123">公制警報規則的名稱</span><span class="sxs-lookup"><span data-stu-id="7e5c8-123">The Name of metric alert rule</span></span>

```yaml
Type: String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e5c8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e5c8-124">-ResourceGroupName</span></span>
<span data-ttu-id="7e5c8-125">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e5c8-125">The ResourceGroupName</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupName
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByRuleName
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e5c8-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e5c8-126">-ResourceId</span></span>
<span data-ttu-id="7e5c8-127">公制警示規則的規則識別碼</span><span class="sxs-lookup"><span data-stu-id="7e5c8-127">The Rule Id of metric alert rule</span></span>

```yaml
Type: String
Parameter Sets: ByRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e5c8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e5c8-128">CommonParameters</span></span>
<span data-ttu-id="7e5c8-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7e5c8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7e5c8-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7e5c8-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e5c8-131">輸入</span><span class="sxs-lookup"><span data-stu-id="7e5c8-131">INPUTS</span></span>

### <span data-ttu-id="7e5c8-132">System.object</span><span class="sxs-lookup"><span data-stu-id="7e5c8-132">System.String</span></span>

## <span data-ttu-id="7e5c8-133">輸出</span><span class="sxs-lookup"><span data-stu-id="7e5c8-133">OUTPUTS</span></span>

### <span data-ttu-id="7e5c8-134">PSMetricAlertRuleV2 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="7e5c8-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="7e5c8-135">筆記</span><span class="sxs-lookup"><span data-stu-id="7e5c8-135">NOTES</span></span>

## <span data-ttu-id="7e5c8-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="7e5c8-136">RELATED LINKS</span></span>
