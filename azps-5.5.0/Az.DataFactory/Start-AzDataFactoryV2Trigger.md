---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/start-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 2a47676324f2955d02c2d50ff83d564ea150d818
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100132130"
---
# <span data-ttu-id="eedaf-101">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="eedaf-101">Start-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="eedaf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eedaf-102">SYNOPSIS</span></span>
<span data-ttu-id="eedaf-103">在資料工廠中啟動觸發程式。</span><span class="sxs-lookup"><span data-stu-id="eedaf-103">Starts a trigger in a data factory.</span></span>

## <span data-ttu-id="eedaf-104">句法</span><span class="sxs-lookup"><span data-stu-id="eedaf-104">SYNTAX</span></span>

### <span data-ttu-id="eedaf-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="eedaf-105">ByFactoryName (Default)</span></span>
```
Start-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eedaf-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="eedaf-106">ByInputObject</span></span>
```
Start-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eedaf-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="eedaf-107">ByResourceId</span></span>
```
Start-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eedaf-108">說明</span><span class="sxs-lookup"><span data-stu-id="eedaf-108">DESCRIPTION</span></span>
<span data-ttu-id="eedaf-109">AzDataFactoryV2Trigger Cmdlet 會在資料工廠中啟動觸發 **程式** 。</span><span class="sxs-lookup"><span data-stu-id="eedaf-109">The **Start-AzDataFactoryV2Trigger** cmdlet starts a trigger in a data factory.</span></span> <span data-ttu-id="eedaf-110">如果觸發程式處於「已停止」狀態，則該 Cmdlet 會啟動觸發程式，而且最終會根據其定義來調用管線。</span><span class="sxs-lookup"><span data-stu-id="eedaf-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="eedaf-111">如果觸發程式已處於「已啟動」狀態，則此 Cmdlet 不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="eedaf-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span> <span data-ttu-id="eedaf-112">如果指定了 Force 參數，則在啟動觸發程式前，不會提示 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eedaf-112">If the Force parameter is specified, the cmdlet doesn't prompt before starting the trigger.</span></span>

## <span data-ttu-id="eedaf-113">示例</span><span class="sxs-lookup"><span data-stu-id="eedaf-113">EXAMPLES</span></span>

### <span data-ttu-id="eedaf-114">範例1：啟動觸發程式</span><span class="sxs-lookup"><span data-stu-id="eedaf-114">Example 1: Start a trigger</span></span>
```
Start-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to start trigger 'ScheduledTrigger' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="eedaf-115">在資料工廠 "WikiADF" 中啟動名為 "ScheduledTrigger" 的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="eedaf-115">Starts a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="eedaf-116">參數</span><span class="sxs-lookup"><span data-stu-id="eedaf-116">PARAMETERS</span></span>

### <span data-ttu-id="eedaf-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="eedaf-117">-DataFactoryName</span></span>
<span data-ttu-id="eedaf-118">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="eedaf-118">The data factory name.</span></span>

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

### <span data-ttu-id="eedaf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eedaf-119">-DefaultProfile</span></span>
<span data-ttu-id="eedaf-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="eedaf-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eedaf-121">-Force</span><span class="sxs-lookup"><span data-stu-id="eedaf-121">-Force</span></span>
<span data-ttu-id="eedaf-122">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eedaf-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="eedaf-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eedaf-123">-InputObject</span></span>
<span data-ttu-id="eedaf-124">觸發要啟動的物件。</span><span class="sxs-lookup"><span data-stu-id="eedaf-124">Trigger object to start.</span></span>

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

### <span data-ttu-id="eedaf-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="eedaf-125">-Name</span></span>
<span data-ttu-id="eedaf-126">觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="eedaf-126">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eedaf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eedaf-127">-ResourceGroupName</span></span>
<span data-ttu-id="eedaf-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="eedaf-128">The resource group name.</span></span>

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

### <span data-ttu-id="eedaf-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eedaf-129">-ResourceId</span></span>
<span data-ttu-id="eedaf-130">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="eedaf-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="eedaf-131">-確認</span><span class="sxs-lookup"><span data-stu-id="eedaf-131">-Confirm</span></span>
<span data-ttu-id="eedaf-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="eedaf-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eedaf-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eedaf-133">-WhatIf</span></span>
<span data-ttu-id="eedaf-134">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eedaf-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="eedaf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eedaf-135">CommonParameters</span></span>
<span data-ttu-id="eedaf-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eedaf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eedaf-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="eedaf-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eedaf-138">輸入</span><span class="sxs-lookup"><span data-stu-id="eedaf-138">INPUTS</span></span>

### <span data-ttu-id="eedaf-139">System.object</span><span class="sxs-lookup"><span data-stu-id="eedaf-139">System.String</span></span>

### <span data-ttu-id="eedaf-140">PSTrigger 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="eedaf-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="eedaf-141">輸出</span><span class="sxs-lookup"><span data-stu-id="eedaf-141">OUTPUTS</span></span>

### <span data-ttu-id="eedaf-142">PSTrigger 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="eedaf-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="eedaf-143">筆記</span><span class="sxs-lookup"><span data-stu-id="eedaf-143">NOTES</span></span>

## <span data-ttu-id="eedaf-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="eedaf-144">RELATED LINKS</span></span>

[<span data-ttu-id="eedaf-145">AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="eedaf-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="eedaf-146">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="eedaf-146">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="eedaf-147">停止 AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="eedaf-147">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="eedaf-148">移除-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="eedaf-148">Remove-AzDataFactoryV2Trigger</span></span>]()
