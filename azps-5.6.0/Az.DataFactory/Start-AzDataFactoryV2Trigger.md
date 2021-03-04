---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/start-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2Trigger.md
ms.openlocfilehash: d9ce325979a40315341a0e43049bd2c5bb512622
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905145"
---
# <span data-ttu-id="5386d-101">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5386d-101">Start-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="5386d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5386d-102">SYNOPSIS</span></span>
<span data-ttu-id="5386d-103">在資料工廠中啟動觸發程式。</span><span class="sxs-lookup"><span data-stu-id="5386d-103">Starts a trigger in a data factory.</span></span>

## <span data-ttu-id="5386d-104">語法</span><span class="sxs-lookup"><span data-stu-id="5386d-104">SYNTAX</span></span>

### <span data-ttu-id="5386d-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="5386d-105">ByFactoryName (Default)</span></span>
```
Start-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5386d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5386d-106">ByInputObject</span></span>
```
Start-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5386d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5386d-107">ByResourceId</span></span>
```
Start-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5386d-108">描述</span><span class="sxs-lookup"><span data-stu-id="5386d-108">DESCRIPTION</span></span>
<span data-ttu-id="5386d-109">**Start-AzDataFactoryV2Trigger Cmdlet** 在資料工廠中啟動觸發程式。</span><span class="sxs-lookup"><span data-stu-id="5386d-109">The **Start-AzDataFactoryV2Trigger** cmdlet starts a trigger in a data factory.</span></span> <span data-ttu-id="5386d-110">如果觸發程式為 '已停止' 狀態，Cmdlet 會啟動觸發程式，最後會根據定義來叫用管線。</span><span class="sxs-lookup"><span data-stu-id="5386d-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="5386d-111">如果觸發已進入 '開始' 狀態，此 Cmdlet 將無效。</span><span class="sxs-lookup"><span data-stu-id="5386d-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span> <span data-ttu-id="5386d-112">如果已指定 Force 參數，Cmdlet 不會在啟動觸發之前提示。</span><span class="sxs-lookup"><span data-stu-id="5386d-112">If the Force parameter is specified, the cmdlet doesn't prompt before starting the trigger.</span></span>

## <span data-ttu-id="5386d-113">例子</span><span class="sxs-lookup"><span data-stu-id="5386d-113">EXAMPLES</span></span>

### <span data-ttu-id="5386d-114">範例 1：啟動觸發</span><span class="sxs-lookup"><span data-stu-id="5386d-114">Example 1: Start a trigger</span></span>
```
Start-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to start trigger 'ScheduledTrigger' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="5386d-115">在資料工廠的 「WikiADF」中啟動名為「ScheduledTri用」的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="5386d-115">Starts a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="5386d-116">參數</span><span class="sxs-lookup"><span data-stu-id="5386d-116">PARAMETERS</span></span>

### <span data-ttu-id="5386d-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5386d-117">-DataFactoryName</span></span>
<span data-ttu-id="5386d-118">資料出廠名稱。</span><span class="sxs-lookup"><span data-stu-id="5386d-118">The data factory name.</span></span>

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

### <span data-ttu-id="5386d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5386d-119">-DefaultProfile</span></span>
<span data-ttu-id="5386d-120">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5386d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5386d-121">-強制</span><span class="sxs-lookup"><span data-stu-id="5386d-121">-Force</span></span>
<span data-ttu-id="5386d-122">執行 Cmdlet 而不提示確認。</span><span class="sxs-lookup"><span data-stu-id="5386d-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="5386d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5386d-123">-InputObject</span></span>
<span data-ttu-id="5386d-124">觸發物件以開始。</span><span class="sxs-lookup"><span data-stu-id="5386d-124">Trigger object to start.</span></span>

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

### <span data-ttu-id="5386d-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="5386d-125">-Name</span></span>
<span data-ttu-id="5386d-126">觸發者名稱。</span><span class="sxs-lookup"><span data-stu-id="5386d-126">The trigger name.</span></span>

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

### <span data-ttu-id="5386d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5386d-127">-ResourceGroupName</span></span>
<span data-ttu-id="5386d-128">資源組名。</span><span class="sxs-lookup"><span data-stu-id="5386d-128">The resource group name.</span></span>

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

### <span data-ttu-id="5386d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5386d-129">-ResourceId</span></span>
<span data-ttu-id="5386d-130">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5386d-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="5386d-131">-確認</span><span class="sxs-lookup"><span data-stu-id="5386d-131">-Confirm</span></span>
<span data-ttu-id="5386d-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5386d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5386d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5386d-133">-WhatIf</span></span>
<span data-ttu-id="5386d-134">顯示如果 Cmdlet 執行，但不執行 Cmdlet 會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5386d-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="5386d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5386d-135">CommonParameters</span></span>
<span data-ttu-id="5386d-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5386d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5386d-137">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="5386d-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5386d-138">輸入</span><span class="sxs-lookup"><span data-stu-id="5386d-138">INPUTS</span></span>

### <span data-ttu-id="5386d-139">System.String</span><span class="sxs-lookup"><span data-stu-id="5386d-139">System.String</span></span>

### <span data-ttu-id="5386d-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="5386d-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="5386d-141">輸出</span><span class="sxs-lookup"><span data-stu-id="5386d-141">OUTPUTS</span></span>

### <span data-ttu-id="5386d-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="5386d-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="5386d-143">筆記</span><span class="sxs-lookup"><span data-stu-id="5386d-143">NOTES</span></span>

## <span data-ttu-id="5386d-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="5386d-144">RELATED LINKS</span></span>

[<span data-ttu-id="5386d-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5386d-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="5386d-146">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5386d-146">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="5386d-147">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5386d-147">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="5386d-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5386d-148">Remove-AzDataFactoryV2Trigger</span></span>]()
