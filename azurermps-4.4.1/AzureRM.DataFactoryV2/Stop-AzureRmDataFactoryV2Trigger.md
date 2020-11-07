---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2Trigger.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 3054824876ccaff24f319ae14c704cd975e79434
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625220"
---
# <span data-ttu-id="31ff4-101">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="31ff4-101">Stop-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="31ff4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="31ff4-102">SYNOPSIS</span></span>

<span data-ttu-id="31ff4-103">停止資料工廠中的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="31ff4-103">Stops a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31ff4-104">句法</span><span class="sxs-lookup"><span data-stu-id="31ff4-104">SYNTAX</span></span>

### <span data-ttu-id="31ff4-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="31ff4-105">ByFactoryName (Default)</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="31ff4-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="31ff4-106">ByInputObject</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="31ff4-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="31ff4-107">ByResourceId</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="31ff4-108">說明</span><span class="sxs-lookup"><span data-stu-id="31ff4-108">DESCRIPTION</span></span>

<span data-ttu-id="31ff4-109">**AzureRmDataFactoryV2Trigger** Cmdlet 會在資料工廠中停止觸發程式。</span><span class="sxs-lookup"><span data-stu-id="31ff4-109">The **Stop-AzureRmDataFactoryV2Trigger** cmdlet stops a trigger in a data factory.</span></span> <span data-ttu-id="31ff4-110">如果觸發程式處於「已啟動」狀態，則該 Cmdlet 會停止觸發程式，而且不會再叫管線。</span><span class="sxs-lookup"><span data-stu-id="31ff4-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="31ff4-111">如果觸發程式已處於「已停止」狀態，則此 Cmdlet 沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="31ff4-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span> <span data-ttu-id="31ff4-112">如果指定了 Force 參數，則在停止觸發程式前，不會提示 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="31ff4-112">If the Force parameter is specified, the cmdlet doesn't prompt before stopping the trigger.</span></span>


## <span data-ttu-id="31ff4-113">示例</span><span class="sxs-lookup"><span data-stu-id="31ff4-113">EXAMPLES</span></span>

### <span data-ttu-id="31ff4-114">範例1：停止觸發程式</span><span class="sxs-lookup"><span data-stu-id="31ff4-114">Example 1: Stop a trigger</span></span>

```
Stop-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to stop trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="31ff4-115">停止資料工廠 "WikiADF" 中名為 "ScheduledTrigger" 的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="31ff4-115">Stops a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>


## <span data-ttu-id="31ff4-116">參數</span><span class="sxs-lookup"><span data-stu-id="31ff4-116">PARAMETERS</span></span>

### <span data-ttu-id="31ff4-117">-確認</span><span class="sxs-lookup"><span data-stu-id="31ff4-117">-Confirm</span></span>
<span data-ttu-id="31ff4-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="31ff4-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ff4-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="31ff4-119">-DataFactoryName</span></span>
<span data-ttu-id="31ff4-120">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="31ff4-120">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31ff4-121">-Force</span><span class="sxs-lookup"><span data-stu-id="31ff4-121">-Force</span></span>
<span data-ttu-id="31ff4-122">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="31ff4-122">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ff4-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="31ff4-123">-Name</span></span>
<span data-ttu-id="31ff4-124">觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="31ff4-124">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31ff4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31ff4-125">-ResourceGroupName</span></span>
<span data-ttu-id="31ff4-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="31ff4-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31ff4-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31ff4-127">-ResourceId</span></span>
<span data-ttu-id="31ff4-128">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="31ff4-128">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31ff4-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31ff4-129">-InputObject</span></span>
<span data-ttu-id="31ff4-130">觸發要啟動的物件。</span><span class="sxs-lookup"><span data-stu-id="31ff4-130">Trigger object to start.</span></span>

```yaml
Type: PSTrigger
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31ff4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31ff4-131">-WhatIf</span></span>
<span data-ttu-id="31ff4-132">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="31ff4-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="31ff4-133">輸入</span><span class="sxs-lookup"><span data-stu-id="31ff4-133">INPUTS</span></span>

### <span data-ttu-id="31ff4-134">System.object</span><span class="sxs-lookup"><span data-stu-id="31ff4-134">System.String</span></span>
<span data-ttu-id="31ff4-135">PSTrigger 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="31ff4-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>


## <span data-ttu-id="31ff4-136">輸出</span><span class="sxs-lookup"><span data-stu-id="31ff4-136">OUTPUTS</span></span>

### <span data-ttu-id="31ff4-137">[System.object]。清單 ' 1 [DataFactoryV2. PSTrigger，DataFactoryV2，版本 = 0.1.9.0，Culture = 中性，PublicKeyToken = null]]。）））</span><span class="sxs-lookup"><span data-stu-id="31ff4-137">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="31ff4-138">PSTrigger 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="31ff4-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>


## <span data-ttu-id="31ff4-139">筆記</span><span class="sxs-lookup"><span data-stu-id="31ff4-139">NOTES</span></span>

## <span data-ttu-id="31ff4-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="31ff4-140">RELATED LINKS</span></span>
[<span data-ttu-id="31ff4-141">AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="31ff4-141">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="31ff4-142">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="31ff4-142">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="31ff4-143">開始-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="31ff4-143">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="31ff4-144">移除-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="31ff4-144">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
