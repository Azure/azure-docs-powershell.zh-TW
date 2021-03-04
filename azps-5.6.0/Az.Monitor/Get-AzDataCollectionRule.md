---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRule.md
ms.openlocfilehash: 6c1ea4cd7abbf50fb00a5f7fe1b04b7112b8f6c2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908945"
---
# <span data-ttu-id="91f50-101">Get-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="91f50-101">Get-AzDataCollectionRule</span></span>

## <span data-ttu-id="91f50-102">簡介</span><span class="sxs-lookup"><span data-stu-id="91f50-102">SYNOPSIS</span></span>
<span data-ttu-id="91f50-103">在資料 (規則) 。</span><span class="sxs-lookup"><span data-stu-id="91f50-103">Gets data collection rule(s).</span></span>

## <span data-ttu-id="91f50-104">語法</span><span class="sxs-lookup"><span data-stu-id="91f50-104">SYNTAX</span></span>

### <span data-ttu-id="91f50-105">BySubscription (預設) </span><span class="sxs-lookup"><span data-stu-id="91f50-105">BySubscription (Default)</span></span>
```
Get-AzDataCollectionRule
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="91f50-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="91f50-106">ByResourceGroup</span></span>
```
Get-AzDataCollectionRule
   -ResourceGroupName <string>
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="91f50-107">ByName</span><span class="sxs-lookup"><span data-stu-id="91f50-107">ByName</span></span>
```
Get-AzDataCollectionRule
   -ResourceGroupName <string>
   -RuleName <string>
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="91f50-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="91f50-108">ByResourceId</span></span>
```
Get-AzDataCollectionRule
   -RuleId <string>
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

## <span data-ttu-id="91f50-109">描述</span><span class="sxs-lookup"><span data-stu-id="91f50-109">DESCRIPTION</span></span>
<span data-ttu-id="91f50-110">**Get-AzDataCollectionRule** Cmdlet 會取得一或多個資料收集規則。</span><span class="sxs-lookup"><span data-stu-id="91f50-110">The **Get-AzDataCollectionRule** cmdlet gets one or more data collection rules.</span></span>

<span data-ttu-id="91f50-111">資料收集規則 (DCR) 定義要進入 Azure 監視器的資料，並指定該資料的寄件位置或儲存位置。</span><span class="sxs-lookup"><span data-stu-id="91f50-111">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="91f50-112">以下是完整的 [DCR 概觀文章](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview)。</span><span class="sxs-lookup"><span data-stu-id="91f50-112">Here is the complete [DCR overview article](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

## <span data-ttu-id="91f50-113">例子</span><span class="sxs-lookup"><span data-stu-id="91f50-113">EXAMPLES</span></span>

### <span data-ttu-id="91f50-114">範例 1：根據訂閱識別碼取得資料收集規則</span><span class="sxs-lookup"><span data-stu-id="91f50-114">Example 1: Get data collection rules by subscription ID</span></span>
```
PS C:\>Get-AzDataCollectionRule

Description       : DCR description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr
Name              : testDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="91f50-115">此命令會列出目前訂閱的所有資料收集規則。</span><span class="sxs-lookup"><span data-stu-id="91f50-115">This command lists all the data collection rules for the current subscription.</span></span>

### <span data-ttu-id="91f50-116">範例 2：取得給定資源群組的資料收集規則</span><span class="sxs-lookup"><span data-stu-id="91f50-116">Example 2: Get data collection rules for the given resource group</span></span>
```
PS C:\>Get-AzDataCollectionRule -ResourceGroup "testgroup"

Description       : DCR description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr
Name              : testDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="91f50-117">此命令會列出給定資源群組的資料收集規則。</span><span class="sxs-lookup"><span data-stu-id="91f50-117">This command lists data collection rules for the given resource group.</span></span>

### <span data-ttu-id="91f50-118">範例 3：取得資料收集規則</span><span class="sxs-lookup"><span data-stu-id="91f50-118">Example 3: Get a data collection rule</span></span>
```
PS C:\>Get-AzDataCollectionRule -ResourceGroup "testgroup" -RuleName "testDcr"

Description       : DCR description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr
Name              : testDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="91f50-119">此命令會列出一 (一個清單，其中一個元素) 資料收集規則。</span><span class="sxs-lookup"><span data-stu-id="91f50-119">This command lists one (a list with a single element) data collection rule.</span></span>

### <span data-ttu-id="91f50-120">範例 4：依規則識別碼取得資料收集規則</span><span class="sxs-lookup"><span data-stu-id="91f50-120">Example 4: Get a data collection rule by Rule ID</span></span>
```
PS C:\>Get-AzDataCollectionRule -RuleId "/subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr"

Description       : DCR description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr
Name              : testDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="91f50-121">此命令會列出一 (一個清單，其中一個元素) 資料收集規則。</span><span class="sxs-lookup"><span data-stu-id="91f50-121">This command lists one (a list with a single element) data collection rule.</span></span>

## <span data-ttu-id="91f50-122">參數</span><span class="sxs-lookup"><span data-stu-id="91f50-122">PARAMETERS</span></span>

### <span data-ttu-id="91f50-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91f50-123">-DefaultProfile</span></span>
<span data-ttu-id="91f50-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="91f50-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91f50-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91f50-125">-ResourceGroupName</span></span>
<span data-ttu-id="91f50-126">資源組名</span><span class="sxs-lookup"><span data-stu-id="91f50-126">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91f50-127">-RuleName</span><span class="sxs-lookup"><span data-stu-id="91f50-127">-RuleName</span></span>
<span data-ttu-id="91f50-128">資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="91f50-128">The name of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91f50-129">-RuleId</span><span class="sxs-lookup"><span data-stu-id="91f50-129">-RuleId</span></span>
<span data-ttu-id="91f50-130">資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="91f50-130">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91f50-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91f50-131">CommonParameters</span></span>
<span data-ttu-id="91f50-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="91f50-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91f50-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="91f50-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91f50-134">輸入</span><span class="sxs-lookup"><span data-stu-id="91f50-134">INPUTS</span></span>

### <span data-ttu-id="91f50-135">System.String</span><span class="sxs-lookup"><span data-stu-id="91f50-135">System.String</span></span>

## <span data-ttu-id="91f50-136">輸出</span><span class="sxs-lookup"><span data-stu-id="91f50-136">OUTPUTS</span></span>

### <span data-ttu-id="91f50-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="91f50-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="91f50-138">筆記</span><span class="sxs-lookup"><span data-stu-id="91f50-138">NOTES</span></span>

## <span data-ttu-id="91f50-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="91f50-139">RELATED LINKS</span></span>

<span data-ttu-id="91f50-140">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md) 
[Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md) 
[New-AzDataCollectionRule](./New-AzDataCollectionRule.md) 
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="91f50-140">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)
[Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md)
[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span></span>
