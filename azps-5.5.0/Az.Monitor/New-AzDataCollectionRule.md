---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDataCollectionRule.md
ms.openlocfilehash: cdde294c3af4684146d265e2024f6948660312bb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100140623"
---
# <span data-ttu-id="6d242-101">New-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="6d242-101">New-AzDataCollectionRule</span></span>

## <span data-ttu-id="6d242-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6d242-102">SYNOPSIS</span></span>
<span data-ttu-id="6d242-103">建立資料收集規則。</span><span class="sxs-lookup"><span data-stu-id="6d242-103">Create a data collection rule.</span></span>

## <span data-ttu-id="6d242-104">句法</span><span class="sxs-lookup"><span data-stu-id="6d242-104">SYNTAX</span></span>

### <span data-ttu-id="6d242-105">ByFile (預設) </span><span class="sxs-lookup"><span data-stu-id="6d242-105">ByFile (Default)</span></span>
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

## <span data-ttu-id="6d242-106">說明</span><span class="sxs-lookup"><span data-stu-id="6d242-106">DESCRIPTION</span></span>
<span data-ttu-id="6d242-107">**新的-AzDataCollectionRule** Cmdlet 會建立資料收集規則。</span><span class="sxs-lookup"><span data-stu-id="6d242-107">The **New-AzDataCollectionRule** cmdlet creates a data collection rule.</span></span>

<span data-ttu-id="6d242-108">資料收集規則 (DCR) 定義進入 Azure 監視器的資料，並指定要傳送或儲存資料的位置。</span><span class="sxs-lookup"><span data-stu-id="6d242-108">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="6d242-109">以下是完整的 [DCR 概述文章](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview)。</span><span class="sxs-lookup"><span data-stu-id="6d242-109">Here is the complete [DCR overview article](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

<span data-ttu-id="6d242-110">若要使用-RuleFile 參數，請構造包含三個屬性的 json 檔案： [資訊]、[目的地]、[dataFlows] (請參閱 #1) 範例</span><span class="sxs-lookup"><span data-stu-id="6d242-110">To use the -RuleFile parameter, construct a json file containing three properties: dataSources, destinations, dataFlows (see Example #1)</span></span>

<span data-ttu-id="6d242-111">您可以在這裡找到 [架構的詳細資料](https://docs.microsoft.com/en-us/rest/api/monitor/datacollectionrules/create)。</span><span class="sxs-lookup"><span data-stu-id="6d242-111">You may find here the [schema detail](https://docs.microsoft.com/en-us/rest/api/monitor/datacollectionrules/create).</span></span>

<span data-ttu-id="6d242-112">同時還支援使用 Cmdlet ConvertTo-Json 進行序列化的 DCR 輸出 (請參閱 #2) 範例。</span><span class="sxs-lookup"><span data-stu-id="6d242-112">The output of a DCR serialized with the cmdlet ConvertTo-Json is also supported (see Example #2).</span></span>

## <span data-ttu-id="6d242-113">示例</span><span class="sxs-lookup"><span data-stu-id="6d242-113">EXAMPLES</span></span>

### <span data-ttu-id="6d242-114">範例1：從 Rest API 建立資料收集規則、JSON</span><span class="sxs-lookup"><span data-stu-id="6d242-114">Example 1: Create data collection rule, JSON from Rest API</span></span>
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

<span data-ttu-id="6d242-115">這個命令會建立目前訂閱的資料收集規則。</span><span class="sxs-lookup"><span data-stu-id="6d242-115">This command creates a data collection rules for the current subscription.</span></span>

### <span data-ttu-id="6d242-116">範例2：從 PSDataCollectionRuleResource 建立資料收集規則</span><span class="sxs-lookup"><span data-stu-id="6d242-116">Example 2: Create data collection rule, JSON from PSDataCollectionRuleResource</span></span>
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

<span data-ttu-id="6d242-117">這個命令會建立目前訂閱的資料收集規則。</span><span class="sxs-lookup"><span data-stu-id="6d242-117">This command creates a data collection rules for the current subscription.</span></span>

## <span data-ttu-id="6d242-118">參數</span><span class="sxs-lookup"><span data-stu-id="6d242-118">PARAMETERS</span></span>

### <span data-ttu-id="6d242-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d242-119">-DefaultProfile</span></span>
<span data-ttu-id="6d242-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="6d242-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6d242-121">-位置</span><span class="sxs-lookup"><span data-stu-id="6d242-121">-Location</span></span>
<span data-ttu-id="6d242-122">資源位置</span><span class="sxs-lookup"><span data-stu-id="6d242-122">The resource location</span></span>

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

### <span data-ttu-id="6d242-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d242-123">-ResourceGroupName</span></span>
<span data-ttu-id="6d242-124">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="6d242-124">The resource group name</span></span>

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

### <span data-ttu-id="6d242-125">-RuleName</span><span class="sxs-lookup"><span data-stu-id="6d242-125">-RuleName</span></span>
<span data-ttu-id="6d242-126">資源名稱</span><span class="sxs-lookup"><span data-stu-id="6d242-126">The resource name</span></span>

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

### <span data-ttu-id="6d242-127">-RuleFile</span><span class="sxs-lookup"><span data-stu-id="6d242-127">-RuleFile</span></span>
<span data-ttu-id="6d242-128">JSON 檔路徑</span><span class="sxs-lookup"><span data-stu-id="6d242-128">The JSON file path</span></span>

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

### <span data-ttu-id="6d242-129">-描述</span><span class="sxs-lookup"><span data-stu-id="6d242-129">-Description</span></span>
<span data-ttu-id="6d242-130">資源描述</span><span class="sxs-lookup"><span data-stu-id="6d242-130">The resource description</span></span>

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

### <span data-ttu-id="6d242-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="6d242-131">-Tag</span></span>
<span data-ttu-id="6d242-132">資源標記</span><span class="sxs-lookup"><span data-stu-id="6d242-132">The resource tags</span></span>

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

### <span data-ttu-id="6d242-133">-確認</span><span class="sxs-lookup"><span data-stu-id="6d242-133">-Confirm</span></span>
<span data-ttu-id="6d242-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6d242-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d242-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d242-135">-WhatIf</span></span>
<span data-ttu-id="6d242-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6d242-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6d242-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6d242-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d242-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d242-138">CommonParameters</span></span>
<span data-ttu-id="6d242-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6d242-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d242-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6d242-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d242-141">輸入</span><span class="sxs-lookup"><span data-stu-id="6d242-141">INPUTS</span></span>

### <span data-ttu-id="6d242-142">System.object</span><span class="sxs-lookup"><span data-stu-id="6d242-142">System.String</span></span>

## <span data-ttu-id="6d242-143">輸出</span><span class="sxs-lookup"><span data-stu-id="6d242-143">OUTPUTS</span></span>

### <span data-ttu-id="6d242-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="6d242-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="6d242-145">筆記</span><span class="sxs-lookup"><span data-stu-id="6d242-145">NOTES</span></span>

## <span data-ttu-id="6d242-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="6d242-146">RELATED LINKS</span></span>

<span data-ttu-id="6d242-147">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md) 
[移除-AzDataCollectionRule](./Remove-AzDataCollectionRule.md) 
[AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
[更新-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="6d242-147">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)
[Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md)
[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span></span>