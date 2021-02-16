---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDataCollectionRule.md
ms.openlocfilehash: 864b3c8abe2411316edf155c49757c1082a863a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100134059"
---
# <span data-ttu-id="81296-101">Set-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="81296-101">Set-AzDataCollectionRule</span></span>

## <span data-ttu-id="81296-102">摘要</span><span class="sxs-lookup"><span data-stu-id="81296-102">SYNOPSIS</span></span>
<span data-ttu-id="81296-103">更新 (完整取代) 資料收集規則。</span><span class="sxs-lookup"><span data-stu-id="81296-103">Updates (full replacement) a data collection rule.</span></span>

## <span data-ttu-id="81296-104">句法</span><span class="sxs-lookup"><span data-stu-id="81296-104">SYNTAX</span></span>

### <span data-ttu-id="81296-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="81296-105">ByName (Default)</span></span>
```
Set-AzDataCollectionRule 
   -Location <string>
   -ResourceGroupName <string>
   -RuleName <string>
   -RuleFile <string>
   [-Description <string>]
   [-Tag <hashtable>]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

### <span data-ttu-id="81296-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="81296-106">ByResourceId</span></span>
```
Set-AzDataCollectionRule 
   -Location <string>
   -RuleId <string>
   -RuleFile <string>
   [-Description <string>]
   [-Tag <hashtable>]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

### <span data-ttu-id="81296-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="81296-107">ByInputObject</span></span>
```
Set-AzDataCollectionRule 
   -InputObject <PSDataCollectionRuleResource> 
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="81296-108">說明</span><span class="sxs-lookup"><span data-stu-id="81296-108">DESCRIPTION</span></span>
<span data-ttu-id="81296-109">**AzDataCollectionRule** Cmdlet 會取代現有的資料集合規則。</span><span class="sxs-lookup"><span data-stu-id="81296-109">The **Set-AzDataCollectionRule** cmdlet replaces an existing data collection rule.</span></span>

<span data-ttu-id="81296-110">資料收集規則 (DCR) 定義進入 Azure 監視器的資料，並指定要傳送或儲存資料的位置。</span><span class="sxs-lookup"><span data-stu-id="81296-110">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="81296-111">以下是完整的 [DCR 概述文章](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview)。</span><span class="sxs-lookup"><span data-stu-id="81296-111">Here is the complete [DCR overview article](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

<span data-ttu-id="81296-112">若要使用-RuleFile 參數，請構造包含三個屬性的 json 檔案： [資訊]、[目的地]、[dataFlows] (請參閱 #1) 的範例。</span><span class="sxs-lookup"><span data-stu-id="81296-112">To use the -RuleFile parameter, construct a json file containing three properties: dataSources, destinations, dataFlows (see Example #1).</span></span>

<span data-ttu-id="81296-113">您可以在這裡找到 [架構的詳細資料](https://docs.microsoft.com/en-us/rest/api/monitor/datacollectionrules/create)。</span><span class="sxs-lookup"><span data-stu-id="81296-113">You may find here the [schema detail](https://docs.microsoft.com/en-us/rest/api/monitor/datacollectionrules/create).</span></span>

<span data-ttu-id="81296-114">DCR 使用 Cmdlet ConvertTo-Json 序列化的輸出也支援 (範例 #2) 。</span><span class="sxs-lookup"><span data-stu-id="81296-114">The output of a DCR serialized with the cmdlet ConvertTo-Json is also supported (Example #2).</span></span>

## <span data-ttu-id="81296-115">示例</span><span class="sxs-lookup"><span data-stu-id="81296-115">EXAMPLES</span></span>

### <span data-ttu-id="81296-116">範例1：從 Rest API 更新資料收集規則，JSON</span><span class="sxs-lookup"><span data-stu-id="81296-116">Example 1: Update data collection rule, JSON from Rest API</span></span>
```powershell
PS C:\>Set-AzDataCollectionRule -Location 'East US 2 EUAP'
                                -ResourceGroupName 'testdcr' 
                                -RuleName 'newDcr' 
                                -RuleFile 'C:\samples\dcr1.json'
                                -Description 'Updated Description'

Description       : Updated Description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcr
Name              : newDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}

# Note: Content of C:\samples\dcr1.json
{
  "properties": {
    "dataSources": {
      "performanceCounters": [
        {
          "streams": [
            "Microsoft-InsightsMetrics"
          ],
          "scheduledTransferPeriod": "PT1M",
          "samplingFrequencyInSeconds": 10,
          "counterSpecifiers": [
            "\\Processor Information(_Total)\\% Processor Time"
          ],
          "name": "perfCounter01"
        }
      ]
    },
    "destinations": {
      "azureMonitorMetrics": {
        "name": "azureMonitorMetrics-default"
      }
    },
    "dataFlows": [
      {
        "streams": [
          "Microsoft-InsightsMetrics"
        ],
        "destinations": [
          "azureMonitorMetrics-default"
        ]
      }
    ]
  }
}
```

<span data-ttu-id="81296-117">這個命令會取代目前訂閱的現有資料集合規則。</span><span class="sxs-lookup"><span data-stu-id="81296-117">This command replaces an existing data collection rules for the current subscription.</span></span>

### <span data-ttu-id="81296-118">範例2：從 PSDataCollectionRuleResource 更新資料收集規則</span><span class="sxs-lookup"><span data-stu-id="81296-118">Example 2: Update data collection rule, JSON from PSDataCollectionRuleResource</span></span>
```powershell
PS C:\>Set-AzDataCollectionRule -Location 'East US 2 EUAP'
                                -RuleId '/subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcr' 
                                -RuleFile 'C:\samples\dcr2.json'
                                -Description 'Updated Description'

Description       : Updated Description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcr
Name              : newDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}

# Note: Content of C:\samples\dcr2.json
{
  "DataSources": {
    "PerformanceCounters": [
      {
        "Streams": [
          "Microsoft-InsightsMetrics"
        ],
        "ScheduledTransferPeriod": "PT1M",
        "SamplingFrequencyInSeconds": 10,
        "CounterSpecifiers": [
          "\\Processor Information(_Total)\\% Processor Time"
        ],
        "Name": "perfCounter01"
      }
    ]
  },
  "Destinations": {
    "AzureMonitorMetrics": {
      "Name": "azureMonitorMetrics-default"
    }
  },
  "DataFlows": [
    {
      "Streams": [
        "Microsoft-InsightsMetrics"
      ],
      "Destinations": [
        "azureMonitorMetrics-default"
      ]
    }
  ]
}
```

<span data-ttu-id="81296-119">這個命令會取代目前訂閱的現有資料集合規則。</span><span class="sxs-lookup"><span data-stu-id="81296-119">This command replaces an existing data collection rules for the current subscription.</span></span>

### <span data-ttu-id="81296-120">範例3：從物件更新資料收集規則</span><span class="sxs-lookup"><span data-stu-id="81296-120">Example 3: Update data collection rule from object</span></span>
```powershell
PS C:\>$dcr = Get-AzDataCollectionRule -ResourceGroupName "testdcr" -Name "newDcr"
PS C:\>$dcr.Description = 'This is a test'
PS C:\>$dcr | Set-AzDataCollectionRule

Description       : This is a test
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : {provState}
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcr
Name              : newDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

## <span data-ttu-id="81296-121">參數</span><span class="sxs-lookup"><span data-stu-id="81296-121">PARAMETERS</span></span>

### <span data-ttu-id="81296-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81296-122">-DefaultProfile</span></span>
<span data-ttu-id="81296-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="81296-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="81296-124">-位置</span><span class="sxs-lookup"><span data-stu-id="81296-124">-Location</span></span>
<span data-ttu-id="81296-125">資源位置</span><span class="sxs-lookup"><span data-stu-id="81296-125">The resource location</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81296-126">-RuleFile</span><span class="sxs-lookup"><span data-stu-id="81296-126">-RuleFile</span></span>
<span data-ttu-id="81296-127">JSON 檔路徑</span><span class="sxs-lookup"><span data-stu-id="81296-127">The JSON file path</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81296-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81296-128">-ResourceGroupName</span></span>
<span data-ttu-id="81296-129">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="81296-129">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81296-130">-RuleName</span><span class="sxs-lookup"><span data-stu-id="81296-130">-RuleName</span></span>
<span data-ttu-id="81296-131">資源名稱</span><span class="sxs-lookup"><span data-stu-id="81296-131">The resource name</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81296-132">-RuleId</span><span class="sxs-lookup"><span data-stu-id="81296-132">-RuleId</span></span>
<span data-ttu-id="81296-133">資源識別碼</span><span class="sxs-lookup"><span data-stu-id="81296-133">The resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81296-134">-描述</span><span class="sxs-lookup"><span data-stu-id="81296-134">-Description</span></span>
<span data-ttu-id="81296-135">資源描述</span><span class="sxs-lookup"><span data-stu-id="81296-135">The resource description</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81296-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="81296-136">-Tag</span></span>
<span data-ttu-id="81296-137">資源標記</span><span class="sxs-lookup"><span data-stu-id="81296-137">The resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81296-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81296-138">-InputObject</span></span>
<span data-ttu-id="81296-139">PSDataCollectionRuleResource 物件</span><span class="sxs-lookup"><span data-stu-id="81296-139">PSDataCollectionRuleResource Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="81296-140">-確認</span><span class="sxs-lookup"><span data-stu-id="81296-140">-Confirm</span></span>
<span data-ttu-id="81296-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="81296-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81296-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81296-142">-WhatIf</span></span>
<span data-ttu-id="81296-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="81296-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="81296-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="81296-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81296-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81296-145">CommonParameters</span></span>
<span data-ttu-id="81296-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="81296-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81296-147">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="81296-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81296-148">輸入</span><span class="sxs-lookup"><span data-stu-id="81296-148">INPUTS</span></span>

### <span data-ttu-id="81296-149">System.object</span><span class="sxs-lookup"><span data-stu-id="81296-149">System.String</span></span>

## <span data-ttu-id="81296-150">輸出</span><span class="sxs-lookup"><span data-stu-id="81296-150">OUTPUTS</span></span>

### <span data-ttu-id="81296-151">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="81296-151">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="81296-152">筆記</span><span class="sxs-lookup"><span data-stu-id="81296-152">NOTES</span></span>

## <span data-ttu-id="81296-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="81296-153">RELATED LINKS</span></span>

<span data-ttu-id="81296-154">[新-AzDataCollectionRule](./New-AzDataCollectionRule.md) 
[移除-AzDataCollectionRule](./Remove-AzDataCollectionRule.md) 
[AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
[更新-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="81296-154">[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)
[Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md)
[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span></span>