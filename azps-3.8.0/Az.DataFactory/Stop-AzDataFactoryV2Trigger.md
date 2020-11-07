---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 80e9ed345b9d1b80dd75be2036826559ac3bbb9a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93798737"
---
# <span data-ttu-id="b5256-101">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="b5256-101">Stop-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="b5256-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b5256-102">SYNOPSIS</span></span>
<span data-ttu-id="b5256-103">停止資料工廠中的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="b5256-103">Stops a trigger in a data factory.</span></span>

## <span data-ttu-id="b5256-104">句法</span><span class="sxs-lookup"><span data-stu-id="b5256-104">SYNTAX</span></span>

### <span data-ttu-id="b5256-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="b5256-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5256-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b5256-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5256-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b5256-107">ByResourceId</span></span>
```
Stop-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5256-108">說明</span><span class="sxs-lookup"><span data-stu-id="b5256-108">DESCRIPTION</span></span>
<span data-ttu-id="b5256-109">**AzDataFactoryV2Trigger** Cmdlet 會在資料工廠中停止觸發程式。</span><span class="sxs-lookup"><span data-stu-id="b5256-109">The **Stop-AzDataFactoryV2Trigger** cmdlet stops a trigger in a data factory.</span></span> <span data-ttu-id="b5256-110">如果觸發程式處於「已啟動」狀態，則該 Cmdlet 會停止觸發程式，而且不會再叫管線。</span><span class="sxs-lookup"><span data-stu-id="b5256-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="b5256-111">如果觸發程式已處於「已停止」狀態，則此 Cmdlet 沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="b5256-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span> <span data-ttu-id="b5256-112">如果指定了 Force 參數，則在停止觸發程式前，不會提示 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b5256-112">If the Force parameter is specified, the cmdlet doesn't prompt before stopping the trigger.</span></span>

## <span data-ttu-id="b5256-113">示例</span><span class="sxs-lookup"><span data-stu-id="b5256-113">EXAMPLES</span></span>

### <span data-ttu-id="b5256-114">範例1：停止觸發程式</span><span class="sxs-lookup"><span data-stu-id="b5256-114">Example 1: Stop a trigger</span></span>
```
Stop-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to stop trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="b5256-115">停止資料工廠 "WikiADF" 中名為 "ScheduledTrigger" 的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="b5256-115">Stops a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="b5256-116">參數</span><span class="sxs-lookup"><span data-stu-id="b5256-116">PARAMETERS</span></span>

### <span data-ttu-id="b5256-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b5256-117">-DataFactoryName</span></span>
<span data-ttu-id="b5256-118">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="b5256-118">The data factory name.</span></span>

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

### <span data-ttu-id="b5256-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5256-119">-DefaultProfile</span></span>
<span data-ttu-id="b5256-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b5256-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5256-121">-Force</span><span class="sxs-lookup"><span data-stu-id="b5256-121">-Force</span></span>
<span data-ttu-id="b5256-122">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b5256-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="b5256-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5256-123">-InputObject</span></span>
<span data-ttu-id="b5256-124">觸發要啟動的物件。</span><span class="sxs-lookup"><span data-stu-id="b5256-124">Trigger object to start.</span></span>

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

### <span data-ttu-id="b5256-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="b5256-125">-Name</span></span>
<span data-ttu-id="b5256-126">觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="b5256-126">The trigger name.</span></span>

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

### <span data-ttu-id="b5256-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5256-127">-ResourceGroupName</span></span>
<span data-ttu-id="b5256-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b5256-128">The resource group name.</span></span>

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

### <span data-ttu-id="b5256-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5256-129">-ResourceId</span></span>
<span data-ttu-id="b5256-130">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b5256-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="b5256-131">-確認</span><span class="sxs-lookup"><span data-stu-id="b5256-131">-Confirm</span></span>
<span data-ttu-id="b5256-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b5256-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5256-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5256-133">-WhatIf</span></span>
<span data-ttu-id="b5256-134">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b5256-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="b5256-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5256-135">CommonParameters</span></span>
<span data-ttu-id="b5256-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b5256-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5256-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b5256-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5256-138">輸入</span><span class="sxs-lookup"><span data-stu-id="b5256-138">INPUTS</span></span>

### <span data-ttu-id="b5256-139">System.object</span><span class="sxs-lookup"><span data-stu-id="b5256-139">System.String</span></span>

### <span data-ttu-id="b5256-140">PSTrigger 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="b5256-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="b5256-141">輸出</span><span class="sxs-lookup"><span data-stu-id="b5256-141">OUTPUTS</span></span>

### <span data-ttu-id="b5256-142">PSTrigger 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="b5256-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="b5256-143">筆記</span><span class="sxs-lookup"><span data-stu-id="b5256-143">NOTES</span></span>

## <span data-ttu-id="b5256-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="b5256-144">RELATED LINKS</span></span>

[<span data-ttu-id="b5256-145">AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="b5256-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="b5256-146">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="b5256-146">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="b5256-147">開始-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="b5256-147">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="b5256-148">移除-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="b5256-148">Remove-AzDataFactoryV2Trigger</span></span>]()
