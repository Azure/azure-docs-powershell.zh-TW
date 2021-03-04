---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/remove-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRule.md
ms.openlocfilehash: 4dfa9417b2bce7473b3d2986f503c163cb6bf42f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907622"
---
# <span data-ttu-id="a664f-101">Remove-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="a664f-101">Remove-AzDataCollectionRule</span></span>

## <span data-ttu-id="a664f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a664f-102">SYNOPSIS</span></span>
<span data-ttu-id="a664f-103">刪除資料收集規則。</span><span class="sxs-lookup"><span data-stu-id="a664f-103">Delete a data collection rule.</span></span>

## <span data-ttu-id="a664f-104">語法</span><span class="sxs-lookup"><span data-stu-id="a664f-104">SYNTAX</span></span>

### <span data-ttu-id="a664f-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="a664f-105">ByName (Default)</span></span>
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

### <span data-ttu-id="a664f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a664f-106">ByInputObject</span></span>
```
Remove-AzDataCollectionRule
   -InputObject <PSDataCollectionRuleResource>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

### <span data-ttu-id="a664f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a664f-107">ByResourceId</span></span>
```
Remove-AzDataCollectionRule
   -RuleId <string>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="a664f-108">描述</span><span class="sxs-lookup"><span data-stu-id="a664f-108">DESCRIPTION</span></span>
<span data-ttu-id="a664f-109">**Remove-AzDataCollectionRule** Cmdlet 會刪除資料收集規則。</span><span class="sxs-lookup"><span data-stu-id="a664f-109">The **Remove-AzDataCollectionRule** cmdlet delete a data collection rule.</span></span>

<span data-ttu-id="a664f-110">資料收集規則 (DCR) 定義要進入 Azure 監視器的資料，並指定該資料的寄件位置或儲存位置。</span><span class="sxs-lookup"><span data-stu-id="a664f-110">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="a664f-111">以下是完整的 [DCR 概觀文章](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview)。</span><span class="sxs-lookup"><span data-stu-id="a664f-111">Here is the complete [DCR overview article](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

## <span data-ttu-id="a664f-112">例子</span><span class="sxs-lookup"><span data-stu-id="a664f-112">EXAMPLES</span></span>

### <span data-ttu-id="a664f-113">範例 1：刪除包含名稱和資源群組參數的資料收集規則</span><span class="sxs-lookup"><span data-stu-id="a664f-113">Example 1: Delete data collection rule with name and resource group parameters</span></span>
```
PS C:\>Remove-AzDataCollectionRule -ResourceGroupName "testgroup" -RuleName "testDcr"             
```

### <span data-ttu-id="a664f-114">範例 2：刪除包含名稱和資源群組的資料收集規則，並返回布林值</span><span class="sxs-lookup"><span data-stu-id="a664f-114">Example 2: Delete data collection rule with name and resource group return bool</span></span>
```
PS C:\>Remove-AzDataCollectionRule -ResourceGroupName "testgroup" -RuleName "testDcr" -PassThru

True
```

### <span data-ttu-id="a664f-115">範例 3：從 InputObject 刪除資料收集規則</span><span class="sxs-lookup"><span data-stu-id="a664f-115">Example 3: Delete data collection rule from InputObject</span></span>
```
PS C:\>Get-AzDataCollectionRule -ResourceGroupName "testdcr" -RuleName "dcrFromPipe95" | Remove-AzDataCollectionRule
```

### <span data-ttu-id="a664f-116">範例 4：從資源識別碼刪除資料收集規則</span><span class="sxs-lookup"><span data-stu-id="a664f-116">Example 4: Delete data collection rule from resource id</span></span>
```
PS C:\>Remove-AzDataCollectionRule -RuleId "/subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/{dcrName}"
```

## <span data-ttu-id="a664f-117">參數</span><span class="sxs-lookup"><span data-stu-id="a664f-117">PARAMETERS</span></span>

### <span data-ttu-id="a664f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a664f-118">-DefaultProfile</span></span>
<span data-ttu-id="a664f-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="a664f-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a664f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a664f-120">-ResourceGroupName</span></span>
<span data-ttu-id="a664f-121">資源組名</span><span class="sxs-lookup"><span data-stu-id="a664f-121">The resource group name</span></span>

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

### <span data-ttu-id="a664f-122">-RuleName</span><span class="sxs-lookup"><span data-stu-id="a664f-122">-RuleName</span></span>
<span data-ttu-id="a664f-123">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="a664f-123">The resource name.</span></span>

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

### <span data-ttu-id="a664f-124">-RuleId</span><span class="sxs-lookup"><span data-stu-id="a664f-124">-RuleId</span></span>
<span data-ttu-id="a664f-125">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a664f-125">The resource identifier.</span></span>

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

### <span data-ttu-id="a664f-126">-確認</span><span class="sxs-lookup"><span data-stu-id="a664f-126">-Confirm</span></span>
<span data-ttu-id="a664f-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a664f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a664f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a664f-128">-WhatIf</span></span>
<span data-ttu-id="a664f-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a664f-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a664f-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a664f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a664f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a664f-131">CommonParameters</span></span>
<span data-ttu-id="a664f-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a664f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a664f-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a664f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a664f-134">輸入</span><span class="sxs-lookup"><span data-stu-id="a664f-134">INPUTS</span></span>

### <span data-ttu-id="a664f-135">System.String</span><span class="sxs-lookup"><span data-stu-id="a664f-135">System.String</span></span>

## <span data-ttu-id="a664f-136">輸出</span><span class="sxs-lookup"><span data-stu-id="a664f-136">OUTPUTS</span></span>

### <span data-ttu-id="a664f-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="a664f-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="a664f-138">筆記</span><span class="sxs-lookup"><span data-stu-id="a664f-138">NOTES</span></span>

## <span data-ttu-id="a664f-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="a664f-139">RELATED LINKS</span></span>

<span data-ttu-id="a664f-140">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md) 
[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
[New-AzDataCollectionRule](./New-AzDataCollectionRule.md) 
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="a664f-140">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)
[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span></span>