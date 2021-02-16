---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
ms.openlocfilehash: d5426decba60df0e18e331c01481ae4f99d5c27c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100138431"
---
# <span data-ttu-id="e0954-101">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="e0954-101">Remove-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="e0954-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e0954-102">SYNOPSIS</span></span>
<span data-ttu-id="e0954-103">從資料工廠移除觸發程式。</span><span class="sxs-lookup"><span data-stu-id="e0954-103">Removes a trigger from a data factory.</span></span>

## <span data-ttu-id="e0954-104">句法</span><span class="sxs-lookup"><span data-stu-id="e0954-104">SYNTAX</span></span>

### <span data-ttu-id="e0954-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="e0954-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0954-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e0954-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0954-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e0954-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0954-108">說明</span><span class="sxs-lookup"><span data-stu-id="e0954-108">DESCRIPTION</span></span>
<span data-ttu-id="e0954-109">AzDataFactoryV2Trigger Cmdlet 會從資料工廠中移除觸發 **程式** 。</span><span class="sxs-lookup"><span data-stu-id="e0954-109">The **Remove-AzDataFactoryV2Trigger** cmdlet removes a trigger from a data factory.</span></span> <span data-ttu-id="e0954-110">如果指定了 _Force_ 參數，則在移除觸發程式之前，Cmdlet 不會提示。</span><span class="sxs-lookup"><span data-stu-id="e0954-110">If the _Force_ parameter is specified, the cmdlet doesn't prompt before removing the trigger.</span></span>

## <span data-ttu-id="e0954-111">示例</span><span class="sxs-lookup"><span data-stu-id="e0954-111">EXAMPLES</span></span>

### <span data-ttu-id="e0954-112">範例1：移除觸發程式</span><span class="sxs-lookup"><span data-stu-id="e0954-112">Example 1: Remove a trigger</span></span>
```
Remove-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger"

Confirm
Are you sure you want to remove trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="e0954-113">從資料工廠 "WikiADF" 移除名為 "ScheduledTrigger" 的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="e0954-113">Remove a trigger called "ScheduledTrigger" from the data factory "WikiADF".</span></span>

## <span data-ttu-id="e0954-114">參數</span><span class="sxs-lookup"><span data-stu-id="e0954-114">PARAMETERS</span></span>

### <span data-ttu-id="e0954-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e0954-115">-DataFactoryName</span></span>
<span data-ttu-id="e0954-116">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="e0954-116">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0954-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0954-117">-DefaultProfile</span></span>
<span data-ttu-id="e0954-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e0954-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0954-119">-Force</span><span class="sxs-lookup"><span data-stu-id="e0954-119">-Force</span></span>
<span data-ttu-id="e0954-120">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e0954-120">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0954-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0954-121">-InputObject</span></span>
<span data-ttu-id="e0954-122">要移除的觸發程式物件。</span><span class="sxs-lookup"><span data-stu-id="e0954-122">The Trigger object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0954-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="e0954-123">-Name</span></span>
<span data-ttu-id="e0954-124">觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="e0954-124">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0954-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0954-125">-ResourceGroupName</span></span>
<span data-ttu-id="e0954-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0954-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0954-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0954-127">-ResourceId</span></span>
<span data-ttu-id="e0954-128">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e0954-128">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0954-129">-確認</span><span class="sxs-lookup"><span data-stu-id="e0954-129">-Confirm</span></span>
<span data-ttu-id="e0954-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e0954-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0954-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0954-131">-WhatIf</span></span>
<span data-ttu-id="e0954-132">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e0954-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0954-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0954-133">CommonParameters</span></span>
<span data-ttu-id="e0954-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e0954-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0954-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e0954-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0954-136">輸入</span><span class="sxs-lookup"><span data-stu-id="e0954-136">INPUTS</span></span>

### <span data-ttu-id="e0954-137">PSTrigger 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="e0954-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

### <span data-ttu-id="e0954-138">System.object</span><span class="sxs-lookup"><span data-stu-id="e0954-138">System.String</span></span>

## <span data-ttu-id="e0954-139">輸出</span><span class="sxs-lookup"><span data-stu-id="e0954-139">OUTPUTS</span></span>

### <span data-ttu-id="e0954-140">System.object</span><span class="sxs-lookup"><span data-stu-id="e0954-140">System.Boolean</span></span>

## <span data-ttu-id="e0954-141">筆記</span><span class="sxs-lookup"><span data-stu-id="e0954-141">NOTES</span></span>

## <span data-ttu-id="e0954-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="e0954-142">RELATED LINKS</span></span>

[<span data-ttu-id="e0954-143">AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="e0954-143">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="e0954-144">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="e0954-144">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="e0954-145">開始-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="e0954-145">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="e0954-146">停止 AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="e0954-146">Stop-AzDataFactoryV2Trigger</span></span>]()

