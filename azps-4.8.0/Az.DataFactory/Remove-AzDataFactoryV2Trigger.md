---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
ms.openlocfilehash: d5426decba60df0e18e331c01481ae4f99d5c27c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126545"
---
# <span data-ttu-id="78bfc-101">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="78bfc-101">Remove-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="78bfc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="78bfc-102">SYNOPSIS</span></span>
<span data-ttu-id="78bfc-103">從資料工廠移除觸發程式。</span><span class="sxs-lookup"><span data-stu-id="78bfc-103">Removes a trigger from a data factory.</span></span>

## <span data-ttu-id="78bfc-104">句法</span><span class="sxs-lookup"><span data-stu-id="78bfc-104">SYNTAX</span></span>

### <span data-ttu-id="78bfc-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="78bfc-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78bfc-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="78bfc-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78bfc-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="78bfc-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78bfc-108">說明</span><span class="sxs-lookup"><span data-stu-id="78bfc-108">DESCRIPTION</span></span>
<span data-ttu-id="78bfc-109">AzDataFactoryV2Trigger Cmdlet 會從資料工廠中移除觸發 **程式** 。</span><span class="sxs-lookup"><span data-stu-id="78bfc-109">The **Remove-AzDataFactoryV2Trigger** cmdlet removes a trigger from a data factory.</span></span> <span data-ttu-id="78bfc-110">如果指定了 _Force_ 參數，則在移除觸發程式之前，Cmdlet 不會提示。</span><span class="sxs-lookup"><span data-stu-id="78bfc-110">If the _Force_ parameter is specified, the cmdlet doesn't prompt before removing the trigger.</span></span>

## <span data-ttu-id="78bfc-111">示例</span><span class="sxs-lookup"><span data-stu-id="78bfc-111">EXAMPLES</span></span>

### <span data-ttu-id="78bfc-112">範例1：移除觸發程式</span><span class="sxs-lookup"><span data-stu-id="78bfc-112">Example 1: Remove a trigger</span></span>
```
Remove-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger"

Confirm
Are you sure you want to remove trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="78bfc-113">從資料工廠 "WikiADF" 移除名為 "ScheduledTrigger" 的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="78bfc-113">Remove a trigger called "ScheduledTrigger" from the data factory "WikiADF".</span></span>

## <span data-ttu-id="78bfc-114">參數</span><span class="sxs-lookup"><span data-stu-id="78bfc-114">PARAMETERS</span></span>

### <span data-ttu-id="78bfc-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="78bfc-115">-DataFactoryName</span></span>
<span data-ttu-id="78bfc-116">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="78bfc-116">The data factory name.</span></span>

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

### <span data-ttu-id="78bfc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78bfc-117">-DefaultProfile</span></span>
<span data-ttu-id="78bfc-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="78bfc-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78bfc-119">-Force</span><span class="sxs-lookup"><span data-stu-id="78bfc-119">-Force</span></span>
<span data-ttu-id="78bfc-120">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="78bfc-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="78bfc-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78bfc-121">-InputObject</span></span>
<span data-ttu-id="78bfc-122">要移除的觸發程式物件。</span><span class="sxs-lookup"><span data-stu-id="78bfc-122">The Trigger object to remove.</span></span>

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

### <span data-ttu-id="78bfc-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="78bfc-123">-Name</span></span>
<span data-ttu-id="78bfc-124">觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="78bfc-124">The trigger name.</span></span>

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

### <span data-ttu-id="78bfc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78bfc-125">-ResourceGroupName</span></span>
<span data-ttu-id="78bfc-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="78bfc-126">The resource group name.</span></span>

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

### <span data-ttu-id="78bfc-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78bfc-127">-ResourceId</span></span>
<span data-ttu-id="78bfc-128">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="78bfc-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="78bfc-129">-確認</span><span class="sxs-lookup"><span data-stu-id="78bfc-129">-Confirm</span></span>
<span data-ttu-id="78bfc-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="78bfc-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78bfc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78bfc-131">-WhatIf</span></span>
<span data-ttu-id="78bfc-132">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="78bfc-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="78bfc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78bfc-133">CommonParameters</span></span>
<span data-ttu-id="78bfc-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="78bfc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78bfc-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="78bfc-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78bfc-136">輸入</span><span class="sxs-lookup"><span data-stu-id="78bfc-136">INPUTS</span></span>

### <span data-ttu-id="78bfc-137">PSTrigger 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="78bfc-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

### <span data-ttu-id="78bfc-138">System.object</span><span class="sxs-lookup"><span data-stu-id="78bfc-138">System.String</span></span>

## <span data-ttu-id="78bfc-139">輸出</span><span class="sxs-lookup"><span data-stu-id="78bfc-139">OUTPUTS</span></span>

### <span data-ttu-id="78bfc-140">System.object</span><span class="sxs-lookup"><span data-stu-id="78bfc-140">System.Boolean</span></span>

## <span data-ttu-id="78bfc-141">筆記</span><span class="sxs-lookup"><span data-stu-id="78bfc-141">NOTES</span></span>

## <span data-ttu-id="78bfc-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="78bfc-142">RELATED LINKS</span></span>

[<span data-ttu-id="78bfc-143">AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="78bfc-143">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="78bfc-144">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="78bfc-144">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="78bfc-145">開始-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="78bfc-145">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="78bfc-146">停止 AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="78bfc-146">Stop-AzDataFactoryV2Trigger</span></span>]()

