---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRule.md
ms.openlocfilehash: 24b5d7dc4209edfbd9bb3080bc87fc18a14977b0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100134067"
---
# <span data-ttu-id="e5a8b-101">Remove-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="e5a8b-101">Remove-AzDataCollectionRule</span></span>

## <span data-ttu-id="e5a8b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e5a8b-102">SYNOPSIS</span></span>
<span data-ttu-id="e5a8b-103">刪除資料收集規則。</span><span class="sxs-lookup"><span data-stu-id="e5a8b-103">Delete a data collection rule.</span></span>

## <span data-ttu-id="e5a8b-104">句法</span><span class="sxs-lookup"><span data-stu-id="e5a8b-104">SYNTAX</span></span>

### <span data-ttu-id="e5a8b-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="e5a8b-105">ByName (Default)</span></span>
```
Remove-AzDataCollectionRule
   -ResourceGroupName <string> 
   -RuleName <string> 
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

### <span data-ttu-id="e5a8b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e5a8b-106">ByInputObject</span></span>
```
Remove-AzDataCollectionRule
   -InputObject <PSDataCollectionRuleResource>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

### <span data-ttu-id="e5a8b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e5a8b-107">ByResourceId</span></span>
```
Remove-AzDataCollectionRule
   -RuleId <string>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="e5a8b-108">說明</span><span class="sxs-lookup"><span data-stu-id="e5a8b-108">DESCRIPTION</span></span>
<span data-ttu-id="e5a8b-109">**AzDataCollectionRule** Cmdlet 會刪除資料收集規則。</span><span class="sxs-lookup"><span data-stu-id="e5a8b-109">The **Remove-AzDataCollectionRule** cmdlet delete a data collection rule.</span></span>

<span data-ttu-id="e5a8b-110">資料收集規則 (DCR) 定義進入 Azure 監視器的資料，並指定要傳送或儲存資料的位置。</span><span class="sxs-lookup"><span data-stu-id="e5a8b-110">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="e5a8b-111">以下是完整的 [DCR 概述文章](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview)。</span><span class="sxs-lookup"><span data-stu-id="e5a8b-111">Here is the complete [DCR overview article](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

## <span data-ttu-id="e5a8b-112">示例</span><span class="sxs-lookup"><span data-stu-id="e5a8b-112">EXAMPLES</span></span>

### <span data-ttu-id="e5a8b-113">範例1：刪除具有名稱和資源群組參數的資料收集規則</span><span class="sxs-lookup"><span data-stu-id="e5a8b-113">Example 1: Delete data collection rule with name and resource group parameters</span></span>
```
PS C:\>Remove-AzDataCollectionRule -ResourceGroupName "testgroup" -RuleName "testDcr"             
```

### <span data-ttu-id="e5a8b-114">範例2：刪除名稱與資源群組的資料收集規則傳回 bool</span><span class="sxs-lookup"><span data-stu-id="e5a8b-114">Example 2: Delete data collection rule with name and resource group return bool</span></span>
```
PS C:\>Remove-AzDataCollectionRule -ResourceGroupName "testgroup" -RuleName "testDcr" -PassThru

True
```

### <span data-ttu-id="e5a8b-115">範例3：從 InputObject 刪除資料收集規則</span><span class="sxs-lookup"><span data-stu-id="e5a8b-115">Example 3: Delete data collection rule from InputObject</span></span>
```
PS C:\>Get-AzDataCollectionRule -ResourceGroupName "testdcr" -RuleName "dcrFromPipe95" | Remove-AzDataCollectionRule
```

### <span data-ttu-id="e5a8b-116">範例4：從資源識別碼刪除資料收集規則</span><span class="sxs-lookup"><span data-stu-id="e5a8b-116">Example 4: Delete data collection rule from resource id</span></span>
```
PS C:\>Remove-AzDataCollectionRule -RuleId "/subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/{dcrName}"
```

## <span data-ttu-id="e5a8b-117">參數</span><span class="sxs-lookup"><span data-stu-id="e5a8b-117">PARAMETERS</span></span>

### <span data-ttu-id="e5a8b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5a8b-118">-DefaultProfile</span></span>
<span data-ttu-id="e5a8b-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e5a8b-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5a8b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5a8b-120">-ResourceGroupName</span></span>
<span data-ttu-id="e5a8b-121">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="e5a8b-121">The resource group name</span></span>

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

### <span data-ttu-id="e5a8b-122">-RuleName</span><span class="sxs-lookup"><span data-stu-id="e5a8b-122">-RuleName</span></span>
<span data-ttu-id="e5a8b-123">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="e5a8b-123">The resource name.</span></span>

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

### <span data-ttu-id="e5a8b-124">-RuleId</span><span class="sxs-lookup"><span data-stu-id="e5a8b-124">-RuleId</span></span>
<span data-ttu-id="e5a8b-125">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e5a8b-125">The resource identifier.</span></span>

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

### <span data-ttu-id="e5a8b-126">-確認</span><span class="sxs-lookup"><span data-stu-id="e5a8b-126">-Confirm</span></span>
<span data-ttu-id="e5a8b-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e5a8b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5a8b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5a8b-128">-WhatIf</span></span>
<span data-ttu-id="e5a8b-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e5a8b-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e5a8b-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5a8b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5a8b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5a8b-131">CommonParameters</span></span>
<span data-ttu-id="e5a8b-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e5a8b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5a8b-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e5a8b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5a8b-134">輸入</span><span class="sxs-lookup"><span data-stu-id="e5a8b-134">INPUTS</span></span>

### <span data-ttu-id="e5a8b-135">System.object</span><span class="sxs-lookup"><span data-stu-id="e5a8b-135">System.String</span></span>

## <span data-ttu-id="e5a8b-136">輸出</span><span class="sxs-lookup"><span data-stu-id="e5a8b-136">OUTPUTS</span></span>

### <span data-ttu-id="e5a8b-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="e5a8b-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="e5a8b-138">筆記</span><span class="sxs-lookup"><span data-stu-id="e5a8b-138">NOTES</span></span>

## <span data-ttu-id="e5a8b-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5a8b-139">RELATED LINKS</span></span>

<span data-ttu-id="e5a8b-140">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md) 
[AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
[新-AzDataCollectionRule](./New-AzDataCollectionRule.md) 
[更新-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="e5a8b-140">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)
[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span></span>