---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/start-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 2a47676324f2955d02c2d50ff83d564ea150d818
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128776"
---
# <span data-ttu-id="414a6-101">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="414a6-101">Start-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="414a6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="414a6-102">SYNOPSIS</span></span>
<span data-ttu-id="414a6-103">在資料工廠中啟動觸發程式。</span><span class="sxs-lookup"><span data-stu-id="414a6-103">Starts a trigger in a data factory.</span></span>

## <span data-ttu-id="414a6-104">句法</span><span class="sxs-lookup"><span data-stu-id="414a6-104">SYNTAX</span></span>

### <span data-ttu-id="414a6-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="414a6-105">ByFactoryName (Default)</span></span>
```
Start-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="414a6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="414a6-106">ByInputObject</span></span>
```
Start-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="414a6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="414a6-107">ByResourceId</span></span>
```
Start-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="414a6-108">說明</span><span class="sxs-lookup"><span data-stu-id="414a6-108">DESCRIPTION</span></span>
<span data-ttu-id="414a6-109">AzDataFactoryV2Trigger Cmdlet 會在資料工廠中啟動觸發 **程式** 。</span><span class="sxs-lookup"><span data-stu-id="414a6-109">The **Start-AzDataFactoryV2Trigger** cmdlet starts a trigger in a data factory.</span></span> <span data-ttu-id="414a6-110">如果觸發程式處於「已停止」狀態，則該 Cmdlet 會啟動觸發程式，而且最終會根據其定義來調用管線。</span><span class="sxs-lookup"><span data-stu-id="414a6-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="414a6-111">如果觸發程式已處於「已啟動」狀態，則此 Cmdlet 不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="414a6-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span> <span data-ttu-id="414a6-112">如果指定了 Force 參數，則在啟動觸發程式前，不會提示 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="414a6-112">If the Force parameter is specified, the cmdlet doesn't prompt before starting the trigger.</span></span>

## <span data-ttu-id="414a6-113">示例</span><span class="sxs-lookup"><span data-stu-id="414a6-113">EXAMPLES</span></span>

### <span data-ttu-id="414a6-114">範例1：啟動觸發程式</span><span class="sxs-lookup"><span data-stu-id="414a6-114">Example 1: Start a trigger</span></span>
```
Start-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to start trigger 'ScheduledTrigger' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="414a6-115">在資料工廠 "WikiADF" 中啟動名為 "ScheduledTrigger" 的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="414a6-115">Starts a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="414a6-116">參數</span><span class="sxs-lookup"><span data-stu-id="414a6-116">PARAMETERS</span></span>

### <span data-ttu-id="414a6-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="414a6-117">-DataFactoryName</span></span>
<span data-ttu-id="414a6-118">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="414a6-118">The data factory name.</span></span>

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

### <span data-ttu-id="414a6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="414a6-119">-DefaultProfile</span></span>
<span data-ttu-id="414a6-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="414a6-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="414a6-121">-Force</span><span class="sxs-lookup"><span data-stu-id="414a6-121">-Force</span></span>
<span data-ttu-id="414a6-122">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="414a6-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="414a6-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="414a6-123">-InputObject</span></span>
<span data-ttu-id="414a6-124">觸發要啟動的物件。</span><span class="sxs-lookup"><span data-stu-id="414a6-124">Trigger object to start.</span></span>

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

### <span data-ttu-id="414a6-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="414a6-125">-Name</span></span>
<span data-ttu-id="414a6-126">觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="414a6-126">The trigger name.</span></span>

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

### <span data-ttu-id="414a6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="414a6-127">-ResourceGroupName</span></span>
<span data-ttu-id="414a6-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="414a6-128">The resource group name.</span></span>

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

### <span data-ttu-id="414a6-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="414a6-129">-ResourceId</span></span>
<span data-ttu-id="414a6-130">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="414a6-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="414a6-131">-確認</span><span class="sxs-lookup"><span data-stu-id="414a6-131">-Confirm</span></span>
<span data-ttu-id="414a6-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="414a6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="414a6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="414a6-133">-WhatIf</span></span>
<span data-ttu-id="414a6-134">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="414a6-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="414a6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="414a6-135">CommonParameters</span></span>
<span data-ttu-id="414a6-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="414a6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="414a6-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="414a6-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="414a6-138">輸入</span><span class="sxs-lookup"><span data-stu-id="414a6-138">INPUTS</span></span>

### <span data-ttu-id="414a6-139">System.object</span><span class="sxs-lookup"><span data-stu-id="414a6-139">System.String</span></span>

### <span data-ttu-id="414a6-140">PSTrigger 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="414a6-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="414a6-141">輸出</span><span class="sxs-lookup"><span data-stu-id="414a6-141">OUTPUTS</span></span>

### <span data-ttu-id="414a6-142">PSTrigger 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="414a6-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="414a6-143">筆記</span><span class="sxs-lookup"><span data-stu-id="414a6-143">NOTES</span></span>

## <span data-ttu-id="414a6-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="414a6-144">RELATED LINKS</span></span>

[<span data-ttu-id="414a6-145">AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="414a6-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="414a6-146">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="414a6-146">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="414a6-147">停止 AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="414a6-147">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="414a6-148">移除-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="414a6-148">Remove-AzDataFactoryV2Trigger</span></span>]()
