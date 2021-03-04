---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDataCollectionRule.md
ms.openlocfilehash: b14d834e005f8a81666fd98b40d276825f04c0e8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910073"
---
# <span data-ttu-id="3eda4-101">New-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="3eda4-101">New-AzDataCollectionRule</span></span>

## <span data-ttu-id="3eda4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3eda4-102">SYNOPSIS</span></span>
<span data-ttu-id="3eda4-103">建立資料收集規則。</span><span class="sxs-lookup"><span data-stu-id="3eda4-103">Create a data collection rule.</span></span>

## <span data-ttu-id="3eda4-104">語法</span><span class="sxs-lookup"><span data-stu-id="3eda4-104">SYNTAX</span></span>

### <span data-ttu-id="3eda4-105">ByFile (預設) </span><span class="sxs-lookup"><span data-stu-id="3eda4-105">ByFile (Default)</span></span>
```
New-AzDataCollectionRule
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

## <span data-ttu-id="3eda4-106">描述</span><span class="sxs-lookup"><span data-stu-id="3eda4-106">DESCRIPTION</span></span>
<span data-ttu-id="3eda4-107">**New-AzDataCollectionRule** Cmdlet 會建立資料收集規則。</span><span class="sxs-lookup"><span data-stu-id="3eda4-107">The **New-AzDataCollectionRule** cmdlet creates a data collection rule.</span></span>

<span data-ttu-id="3eda4-108">資料收集規則 (DCR) 定義要進入 Azure 監視器的資料，並指定該資料的寄件位置或儲存位置。</span><span class="sxs-lookup"><span data-stu-id="3eda4-108">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="3eda4-109">以下是完整的 [DCR 概觀文章](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview)。</span><span class="sxs-lookup"><span data-stu-id="3eda4-109">Here is the complete [DCR overview article](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

<span data-ttu-id="3eda4-110">若要使用 -RuleFile 參數，請建構包含三個屬性的 json 檔案：dataSources、目的地、dataFlows (請參閱範例#1) </span><span class="sxs-lookup"><span data-stu-id="3eda4-110">To use the -RuleFile parameter, construct a json file containing three properties: dataSources, destinations, dataFlows (see Example #1)</span></span>

<span data-ttu-id="3eda4-111">您可以在此找到架構 [的詳細資料](https://docs.microsoft.com/rest/api/monitor/datacollectionrules/create)。</span><span class="sxs-lookup"><span data-stu-id="3eda4-111">You may find here the [schema detail](https://docs.microsoft.com/rest/api/monitor/datacollectionrules/create).</span></span>

<span data-ttu-id="3eda4-112">也支援以 Cmdlet ConvertTo-Json序列化的 DCR 輸出 (請參閱範例#2) 。</span><span class="sxs-lookup"><span data-stu-id="3eda4-112">The output of a DCR serialized with the cmdlet ConvertTo-Json is also supported (see Example #2).</span></span>

## <span data-ttu-id="3eda4-113">例子</span><span class="sxs-lookup"><span data-stu-id="3eda4-113">EXAMPLES</span></span>

### <span data-ttu-id="3eda4-114">範例 1：建立資料收集規則，從 Rest API 建立 JSON</span><span class="sxs-lookup"><span data-stu-id="3eda4-114">Example 1: Create data collection rule, JSON from Rest API</span></span>
```powershell
PS C:\>New-AzDataCollectionRule -Location 'East US 2 EUAP' -ResourceGroupName 'testdcr'
                                -RuleName 'newDcrEx1' -RuleFile 'C:\samples\dcrEx1.json'
                                -Description 'Dcr description'
                                -Tag @{"tag1"="value1"; "tag2"="value2"}

Description       : Dcr description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcrEx1
Name              : newDcrEx1
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}

# Note: Content of C:\samples\dcrEx1.json
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

<span data-ttu-id="3eda4-115">此命令會針對目前的訂閱建立資料收集規則。</span><span class="sxs-lookup"><span data-stu-id="3eda4-115">This command creates a data collection rules for the current subscription.</span></span>

### <span data-ttu-id="3eda4-116">範例 2：建立資料收集規則，來自 PSDataCollectionRuleResource 的 JSON</span><span class="sxs-lookup"><span data-stu-id="3eda4-116">Example 2: Create data collection rule, JSON from PSDataCollectionRuleResource</span></span>
```powershell
PS C:\>New-AzDataCollectionRule -Location 'East US 2 EUAP' -ResourceGroupName 'testdcr'
                                -RuleName 'newDcrEx2' -RuleFile 'C:\samples\dcrEx2.json'
                                -Description 'Dcr description'
                                -Tag @{"tag1"="value1"; "tag2"="value2"}

Description       : Dcr description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcrEx2
Name              : newDcrEx2
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}

# Note: Content of C:\samples\dcrEx2.json
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

<span data-ttu-id="3eda4-117">此命令會針對目前的訂閱建立資料收集規則。</span><span class="sxs-lookup"><span data-stu-id="3eda4-117">This command creates a data collection rules for the current subscription.</span></span>

## <span data-ttu-id="3eda4-118">參數</span><span class="sxs-lookup"><span data-stu-id="3eda4-118">PARAMETERS</span></span>

### <span data-ttu-id="3eda4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eda4-119">-DefaultProfile</span></span>
<span data-ttu-id="3eda4-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="3eda4-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3eda4-121">-位置</span><span class="sxs-lookup"><span data-stu-id="3eda4-121">-Location</span></span>
<span data-ttu-id="3eda4-122">資源位置</span><span class="sxs-lookup"><span data-stu-id="3eda4-122">The resource location</span></span>

```yaml
Type: System.String
Parameter Sets: ByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eda4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3eda4-123">-ResourceGroupName</span></span>
<span data-ttu-id="3eda4-124">資源組名</span><span class="sxs-lookup"><span data-stu-id="3eda4-124">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eda4-125">-RuleName</span><span class="sxs-lookup"><span data-stu-id="3eda4-125">-RuleName</span></span>
<span data-ttu-id="3eda4-126">資源名稱</span><span class="sxs-lookup"><span data-stu-id="3eda4-126">The resource name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFile
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eda4-127">-RuleFile</span><span class="sxs-lookup"><span data-stu-id="3eda4-127">-RuleFile</span></span>
<span data-ttu-id="3eda4-128">JSON 檔案路徑</span><span class="sxs-lookup"><span data-stu-id="3eda4-128">The JSON file path</span></span>

```yaml
Type: System.String
Parameter Sets: ByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eda4-129">-描述</span><span class="sxs-lookup"><span data-stu-id="3eda4-129">-Description</span></span>
<span data-ttu-id="3eda4-130">資源描述</span><span class="sxs-lookup"><span data-stu-id="3eda4-130">The resource description</span></span>

```yaml
Type: System.String
Parameter Sets: ByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eda4-131">-標記</span><span class="sxs-lookup"><span data-stu-id="3eda4-131">-Tag</span></span>
<span data-ttu-id="3eda4-132">資源標記</span><span class="sxs-lookup"><span data-stu-id="3eda4-132">The resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eda4-133">-確認</span><span class="sxs-lookup"><span data-stu-id="3eda4-133">-Confirm</span></span>
<span data-ttu-id="3eda4-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3eda4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3eda4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3eda4-135">-WhatIf</span></span>
<span data-ttu-id="3eda4-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3eda4-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3eda4-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3eda4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3eda4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eda4-138">CommonParameters</span></span>
<span data-ttu-id="3eda4-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3eda4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eda4-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3eda4-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eda4-141">輸入</span><span class="sxs-lookup"><span data-stu-id="3eda4-141">INPUTS</span></span>

### <span data-ttu-id="3eda4-142">System.String</span><span class="sxs-lookup"><span data-stu-id="3eda4-142">System.String</span></span>

## <span data-ttu-id="3eda4-143">輸出</span><span class="sxs-lookup"><span data-stu-id="3eda4-143">OUTPUTS</span></span>

### <span data-ttu-id="3eda4-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="3eda4-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="3eda4-145">筆記</span><span class="sxs-lookup"><span data-stu-id="3eda4-145">NOTES</span></span>

## <span data-ttu-id="3eda4-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="3eda4-146">RELATED LINKS</span></span>

<span data-ttu-id="3eda4-147">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md) 
[Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md) 
[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="3eda4-147">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)
[Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md)
[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span></span>