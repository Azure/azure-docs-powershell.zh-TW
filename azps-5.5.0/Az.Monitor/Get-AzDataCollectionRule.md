---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRule.md
ms.openlocfilehash: 8826dfdf8fe0152035319c576210088bcd5521e3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100129111"
---
# <span data-ttu-id="ed79c-101">Get-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="ed79c-101">Get-AzDataCollectionRule</span></span>

## <span data-ttu-id="ed79c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ed79c-102">SYNOPSIS</span></span>
<span data-ttu-id="ed79c-103">取得資料收集規則 (s) 。</span><span class="sxs-lookup"><span data-stu-id="ed79c-103">Gets data collection rule(s).</span></span>

## <span data-ttu-id="ed79c-104">句法</span><span class="sxs-lookup"><span data-stu-id="ed79c-104">SYNTAX</span></span>

### <span data-ttu-id="ed79c-105">BySubscription (預設) </span><span class="sxs-lookup"><span data-stu-id="ed79c-105">BySubscription (Default)</span></span>
```
Get-AzDataCollectionRule
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="ed79c-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ed79c-106">ByResourceGroup</span></span>
```
Get-AzDataCollectionRule
   -ResourceGroupName <string>
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="ed79c-107">ByName</span><span class="sxs-lookup"><span data-stu-id="ed79c-107">ByName</span></span>
```
Get-AzDataCollectionRule
   -ResourceGroupName <string>
   -RuleName <string>
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="ed79c-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ed79c-108">ByResourceId</span></span>
```
Get-AzDataCollectionRule
   -RuleId <string>
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

## <span data-ttu-id="ed79c-109">說明</span><span class="sxs-lookup"><span data-stu-id="ed79c-109">DESCRIPTION</span></span>
<span data-ttu-id="ed79c-110">**AzDataCollectionRule** Cmdlet 會取得一或多個資料收集規則。</span><span class="sxs-lookup"><span data-stu-id="ed79c-110">The **Get-AzDataCollectionRule** cmdlet gets one or more data collection rules.</span></span>

<span data-ttu-id="ed79c-111">資料收集規則 (DCR) 定義進入 Azure 監視器的資料，並指定要傳送或儲存資料的位置。</span><span class="sxs-lookup"><span data-stu-id="ed79c-111">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="ed79c-112">以下是完整的 [DCR 概述文章](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview)。</span><span class="sxs-lookup"><span data-stu-id="ed79c-112">Here is the complete [DCR overview article](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

## <span data-ttu-id="ed79c-113">示例</span><span class="sxs-lookup"><span data-stu-id="ed79c-113">EXAMPLES</span></span>

### <span data-ttu-id="ed79c-114">範例1：依訂閱識別碼取得資料收集規則</span><span class="sxs-lookup"><span data-stu-id="ed79c-114">Example 1: Get data collection rules by subscription ID</span></span>
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

<span data-ttu-id="ed79c-115">這個命令會列出目前訂閱的所有資料收集規則。</span><span class="sxs-lookup"><span data-stu-id="ed79c-115">This command lists all the data collection rules for the current subscription.</span></span>

### <span data-ttu-id="ed79c-116">範例2：取得指定資源群組的資料收集規則</span><span class="sxs-lookup"><span data-stu-id="ed79c-116">Example 2: Get data collection rules for the given resource group</span></span>
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

<span data-ttu-id="ed79c-117">這個命令會列出指定資源群組的資料收集規則。</span><span class="sxs-lookup"><span data-stu-id="ed79c-117">This command lists data collection rules for the given resource group.</span></span>

### <span data-ttu-id="ed79c-118">範例3：取得資料集合規則</span><span class="sxs-lookup"><span data-stu-id="ed79c-118">Example 3: Get a data collection rule</span></span>
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

<span data-ttu-id="ed79c-119">這個命令會列出一個 (清單，其中只有一個元素) 資料收集規則。</span><span class="sxs-lookup"><span data-stu-id="ed79c-119">This command lists one (a list with a single element) data collection rule.</span></span>

### <span data-ttu-id="ed79c-120">範例4：依規則識別碼取得資料收集規則</span><span class="sxs-lookup"><span data-stu-id="ed79c-120">Example 4: Get a data collection rule by Rule ID</span></span>
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

<span data-ttu-id="ed79c-121">這個命令會列出一個 (清單，其中只有一個元素) 資料收集規則。</span><span class="sxs-lookup"><span data-stu-id="ed79c-121">This command lists one (a list with a single element) data collection rule.</span></span>

## <span data-ttu-id="ed79c-122">參數</span><span class="sxs-lookup"><span data-stu-id="ed79c-122">PARAMETERS</span></span>

### <span data-ttu-id="ed79c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed79c-123">-DefaultProfile</span></span>
<span data-ttu-id="ed79c-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ed79c-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed79c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed79c-125">-ResourceGroupName</span></span>
<span data-ttu-id="ed79c-126">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="ed79c-126">The resource group name</span></span>

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

### <span data-ttu-id="ed79c-127">-RuleName</span><span class="sxs-lookup"><span data-stu-id="ed79c-127">-RuleName</span></span>
<span data-ttu-id="ed79c-128">資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed79c-128">The name of the resource.</span></span>

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

### <span data-ttu-id="ed79c-129">-RuleId</span><span class="sxs-lookup"><span data-stu-id="ed79c-129">-RuleId</span></span>
<span data-ttu-id="ed79c-130">資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ed79c-130">The ID of the resource.</span></span>

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

### <span data-ttu-id="ed79c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed79c-131">CommonParameters</span></span>
<span data-ttu-id="ed79c-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ed79c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed79c-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ed79c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed79c-134">輸入</span><span class="sxs-lookup"><span data-stu-id="ed79c-134">INPUTS</span></span>

### <span data-ttu-id="ed79c-135">System.object</span><span class="sxs-lookup"><span data-stu-id="ed79c-135">System.String</span></span>

## <span data-ttu-id="ed79c-136">輸出</span><span class="sxs-lookup"><span data-stu-id="ed79c-136">OUTPUTS</span></span>

### <span data-ttu-id="ed79c-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="ed79c-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="ed79c-138">筆記</span><span class="sxs-lookup"><span data-stu-id="ed79c-138">NOTES</span></span>

## <span data-ttu-id="ed79c-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="ed79c-139">RELATED LINKS</span></span>

<span data-ttu-id="ed79c-140">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md) 
[移除-AzDataCollectionRule](./Remove-AzDataCollectionRule.md) 
[新-AzDataCollectionRule](./New-AzDataCollectionRule.md) 
[更新-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="ed79c-140">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)
[Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md)
[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span></span>
