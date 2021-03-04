---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/update-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzDataCollectionRule.md
ms.openlocfilehash: 2e4aba9a2572b5612070d860dcbe20cda2366a02
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912802"
---
# <span data-ttu-id="6bd0e-101">Update-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="6bd0e-101">Update-AzDataCollectionRule</span></span>

## <span data-ttu-id="6bd0e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6bd0e-102">SYNOPSIS</span></span>
<span data-ttu-id="6bd0e-103">更新資料收集規則標記屬性。</span><span class="sxs-lookup"><span data-stu-id="6bd0e-103">Updates a data collection rule tags property.</span></span>

## <span data-ttu-id="6bd0e-104">語法</span><span class="sxs-lookup"><span data-stu-id="6bd0e-104">SYNTAX</span></span>

### <span data-ttu-id="6bd0e-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="6bd0e-105">ByName (Default)</span></span>
```
Update-AzDataCollectionRule 
      -ResourceGroupName <string> 
      -RuleName <string> 
      [-Tag <hashtable>] 
      [-DefaultProfile <IAzureContextContainer>] 
      [-WhatIf] 
      [-Confirm]
      [<CommonParameters>]
```

### <span data-ttu-id="6bd0e-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6bd0e-106">ByResourceId</span></span>
```
Update-AzDataCollectionRule 
      -RuleId <string> 
      [-Tag <hashtable>] 
      [-DefaultProfile <IAzureContextContainer>] 
      [-WhatIf] 
      [-Confirm]
      [<CommonParameters>]
```

### <span data-ttu-id="6bd0e-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6bd0e-107">ByInputObject</span></span>
```
Update-AzDataCollectionRule 
      -InputObject <PSDataCollectionRuleResource> 
      [-Tag <hashtable>] 
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

## <span data-ttu-id="6bd0e-108">描述</span><span class="sxs-lookup"><span data-stu-id="6bd0e-108">DESCRIPTION</span></span>
<span data-ttu-id="6bd0e-109">**Update-AzDataCollectionRule** Cmdlet 會更新資料收集規則 Tags 屬性。</span><span class="sxs-lookup"><span data-stu-id="6bd0e-109">The **Update-AzDataCollectionRule** cmdlet updates a data collection rule Tags property.</span></span>

<span data-ttu-id="6bd0e-110">資料收集規則 (DCR) 定義要進入 Azure 監視器的資料，並指定該資料的寄件位置或儲存位置。</span><span class="sxs-lookup"><span data-stu-id="6bd0e-110">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="6bd0e-111">以下是完整的 [DCR 概觀文章](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview)。</span><span class="sxs-lookup"><span data-stu-id="6bd0e-111">Here is the complete [DCR overview article](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

## <span data-ttu-id="6bd0e-112">例子</span><span class="sxs-lookup"><span data-stu-id="6bd0e-112">EXAMPLES</span></span>

### <span data-ttu-id="6bd0e-113">範例 1：更新資料收集規則標記</span><span class="sxs-lookup"><span data-stu-id="6bd0e-113">Example 1: Update data collection rule tags</span></span>
```
PS C:\>Update-AzDataCollectionRule -RuleName 'newDcr'
                                   -ResourceGroupName 'testdcr'
                                   -Tag @{"tag1"="value1"; "tag2"="value2"}

Description       : 
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
```

<span data-ttu-id="6bd0e-114">此命令會更新給定資料收集規則的標記屬性。</span><span class="sxs-lookup"><span data-stu-id="6bd0e-114">This command updates the tags property for the given data collection rule.</span></span>

### <span data-ttu-id="6bd0e-115">範例 2：更新資料收集規則標記</span><span class="sxs-lookup"><span data-stu-id="6bd0e-115">Example 2: Update data collection rule tags</span></span>
```
PS C:\>Update-AzDataCollectionRule -RuleId '/subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcr'
                                   -Tag @{"tag1"="value1"; "tag2"="value2"}

Description       : 
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
```

<span data-ttu-id="6bd0e-116">此命令會更新給定資料收集規則的標記屬性。</span><span class="sxs-lookup"><span data-stu-id="6bd0e-116">This command updates the tags property for the given data collection rule.</span></span>

### <span data-ttu-id="6bd0e-117">範例 3：更新資料收集規則標記</span><span class="sxs-lookup"><span data-stu-id="6bd0e-117">Example 3: Update data collection rule tags</span></span>
```
PS C:\>$dcr = Get-AzDataCollectionRule -ResourceGroupName "testdcr" -Name "newDcr"
PS C:\>$dcr | Update-AzDataCollectionRule -Tag @{"tag1"="value1"; "tag2"="value2"}

Description       : 
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

<span data-ttu-id="6bd0e-118">此命令會更新給定資料收集規則的標記屬性。</span><span class="sxs-lookup"><span data-stu-id="6bd0e-118">This command updates the tags property for the given data collection rule.</span></span>

## <span data-ttu-id="6bd0e-119">參數</span><span class="sxs-lookup"><span data-stu-id="6bd0e-119">PARAMETERS</span></span>

### <span data-ttu-id="6bd0e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bd0e-120">-DefaultProfile</span></span>
<span data-ttu-id="6bd0e-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="6bd0e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6bd0e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bd0e-122">-ResourceGroupName</span></span>
<span data-ttu-id="6bd0e-123">資源組名</span><span class="sxs-lookup"><span data-stu-id="6bd0e-123">The resource group name</span></span>

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

### <span data-ttu-id="6bd0e-124">-RuleName</span><span class="sxs-lookup"><span data-stu-id="6bd0e-124">-RuleName</span></span>
<span data-ttu-id="6bd0e-125">資源名稱</span><span class="sxs-lookup"><span data-stu-id="6bd0e-125">The resource name</span></span>

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

### <span data-ttu-id="6bd0e-126">-RuleId</span><span class="sxs-lookup"><span data-stu-id="6bd0e-126">-RuleId</span></span>
<span data-ttu-id="6bd0e-127">資料收集規則的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="6bd0e-127">The resource ID of the data collection rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="6bd0e-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6bd0e-128">-InputObject</span></span>
<span data-ttu-id="6bd0e-129">PSDataCollectionRuleResource 物件</span><span class="sxs-lookup"><span data-stu-id="6bd0e-129">PSDataCollectionRuleResource Object</span></span>

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

### <span data-ttu-id="6bd0e-130">-標記</span><span class="sxs-lookup"><span data-stu-id="6bd0e-130">-Tag</span></span>
<span data-ttu-id="6bd0e-131">資料收集規則的標記屬性</span><span class="sxs-lookup"><span data-stu-id="6bd0e-131">The tags property of the data collection rule</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: Falose
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bd0e-132">-確認</span><span class="sxs-lookup"><span data-stu-id="6bd0e-132">-Confirm</span></span>
<span data-ttu-id="6bd0e-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6bd0e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bd0e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bd0e-134">-WhatIf</span></span>
<span data-ttu-id="6bd0e-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6bd0e-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6bd0e-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6bd0e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bd0e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bd0e-137">CommonParameters</span></span>
<span data-ttu-id="6bd0e-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6bd0e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bd0e-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6bd0e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bd0e-140">輸入</span><span class="sxs-lookup"><span data-stu-id="6bd0e-140">INPUTS</span></span>

### <span data-ttu-id="6bd0e-141">System.String</span><span class="sxs-lookup"><span data-stu-id="6bd0e-141">System.String</span></span>

## <span data-ttu-id="6bd0e-142">輸出</span><span class="sxs-lookup"><span data-stu-id="6bd0e-142">OUTPUTS</span></span>

### <span data-ttu-id="6bd0e-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="6bd0e-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="6bd0e-144">筆記</span><span class="sxs-lookup"><span data-stu-id="6bd0e-144">NOTES</span></span>

## <span data-ttu-id="6bd0e-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="6bd0e-145">RELATED LINKS</span></span>

<span data-ttu-id="6bd0e-146">[New-AzDataCollectionRule](./New-AzDataCollectionRule.md) 
[Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md) 
[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="6bd0e-146">[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)
[Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md)
[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)</span></span>