---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2Trigger.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 610aabd21fa1a3e7ae19430c4ce5d79d89f7ab3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457619"
---
# <span data-ttu-id="07d84-101">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="07d84-101">Start-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="07d84-102">摘要</span><span class="sxs-lookup"><span data-stu-id="07d84-102">SYNOPSIS</span></span>

<span data-ttu-id="07d84-103">在資料工廠中啟動觸發程式。</span><span class="sxs-lookup"><span data-stu-id="07d84-103">Starts a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07d84-104">句法</span><span class="sxs-lookup"><span data-stu-id="07d84-104">SYNTAX</span></span>

### <span data-ttu-id="07d84-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="07d84-105">ByFactoryName (Default)</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="07d84-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="07d84-106">ByInputObject</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="07d84-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="07d84-107">ByResourceId</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="07d84-108">說明</span><span class="sxs-lookup"><span data-stu-id="07d84-108">DESCRIPTION</span></span>

<span data-ttu-id="07d84-109">AzureRmDataFactoryV2Trigger Cmdlet 會在資料工廠中啟動觸發 **程式** 。</span><span class="sxs-lookup"><span data-stu-id="07d84-109">The **Start-AzureRmDataFactoryV2Trigger** cmdlet starts a trigger in a data factory.</span></span> <span data-ttu-id="07d84-110">如果觸發程式處於「已停止」狀態，則該 Cmdlet 會啟動觸發程式，而且最終會根據其定義來調用管線。</span><span class="sxs-lookup"><span data-stu-id="07d84-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="07d84-111">如果觸發程式已處於「已啟動」狀態，則此 Cmdlet 不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="07d84-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span> <span data-ttu-id="07d84-112">如果指定了 Force 參數，則在啟動觸發程式前，不會提示 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="07d84-112">If the Force parameter is specified, the cmdlet doesn't prompt before starting the trigger.</span></span>


## <span data-ttu-id="07d84-113">示例</span><span class="sxs-lookup"><span data-stu-id="07d84-113">EXAMPLES</span></span>

### <span data-ttu-id="07d84-114">範例1：啟動觸發程式</span><span class="sxs-lookup"><span data-stu-id="07d84-114">Example 1: Start a trigger</span></span>

```
Start-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to start trigger 'ScheduledTrigger' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="07d84-115">在資料工廠 "WikiADF" 中啟動名為 "ScheduledTrigger" 的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="07d84-115">Starts a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>


## <span data-ttu-id="07d84-116">參數</span><span class="sxs-lookup"><span data-stu-id="07d84-116">PARAMETERS</span></span>

### <span data-ttu-id="07d84-117">-確認</span><span class="sxs-lookup"><span data-stu-id="07d84-117">-Confirm</span></span>
<span data-ttu-id="07d84-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="07d84-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07d84-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="07d84-119">-DataFactoryName</span></span>
<span data-ttu-id="07d84-120">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="07d84-120">The data factory name.</span></span>

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

### <span data-ttu-id="07d84-121">-Force</span><span class="sxs-lookup"><span data-stu-id="07d84-121">-Force</span></span>
<span data-ttu-id="07d84-122">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="07d84-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="07d84-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="07d84-123">-Name</span></span>
<span data-ttu-id="07d84-124">觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="07d84-124">The trigger name.</span></span>

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

### <span data-ttu-id="07d84-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07d84-125">-ResourceGroupName</span></span>
<span data-ttu-id="07d84-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="07d84-126">The resource group name.</span></span>

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

### <span data-ttu-id="07d84-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07d84-127">-ResourceId</span></span>
<span data-ttu-id="07d84-128">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="07d84-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="07d84-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07d84-129">-InputObject</span></span>
<span data-ttu-id="07d84-130">觸發要啟動的物件。</span><span class="sxs-lookup"><span data-stu-id="07d84-130">Trigger object to start.</span></span>

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

### <span data-ttu-id="07d84-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07d84-131">-WhatIf</span></span>
<span data-ttu-id="07d84-132">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="07d84-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="07d84-133">輸入</span><span class="sxs-lookup"><span data-stu-id="07d84-133">INPUTS</span></span>

### <span data-ttu-id="07d84-134">System.object</span><span class="sxs-lookup"><span data-stu-id="07d84-134">System.String</span></span>
<span data-ttu-id="07d84-135">PSTrigger 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="07d84-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>


## <span data-ttu-id="07d84-136">輸出</span><span class="sxs-lookup"><span data-stu-id="07d84-136">OUTPUTS</span></span>

### <span data-ttu-id="07d84-137">[System.object]。清單 ' 1 [DataFactoryV2. PSTrigger，DataFactoryV2，版本 = 0.1.9.0，Culture = 中性，PublicKeyToken = null]]。）））</span><span class="sxs-lookup"><span data-stu-id="07d84-137">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="07d84-138">PSTrigger 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="07d84-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>


## <span data-ttu-id="07d84-139">筆記</span><span class="sxs-lookup"><span data-stu-id="07d84-139">NOTES</span></span>

## <span data-ttu-id="07d84-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="07d84-140">RELATED LINKS</span></span>
[<span data-ttu-id="07d84-141">AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="07d84-141">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="07d84-142">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="07d84-142">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="07d84-143">停止 AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="07d84-143">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="07d84-144">移除-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="07d84-144">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
