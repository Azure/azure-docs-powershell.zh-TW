---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/stop-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 7356f6f0235f73207582303b46459d28dffbe6fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905142"
---
# <span data-ttu-id="4480f-101">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="4480f-101">Stop-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="4480f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4480f-102">SYNOPSIS</span></span>
<span data-ttu-id="4480f-103">在資料工廠中停止觸發。</span><span class="sxs-lookup"><span data-stu-id="4480f-103">Stops a trigger in a data factory.</span></span>

## <span data-ttu-id="4480f-104">語法</span><span class="sxs-lookup"><span data-stu-id="4480f-104">SYNTAX</span></span>

### <span data-ttu-id="4480f-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="4480f-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4480f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4480f-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4480f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4480f-107">ByResourceId</span></span>
```
Stop-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4480f-108">描述</span><span class="sxs-lookup"><span data-stu-id="4480f-108">DESCRIPTION</span></span>
<span data-ttu-id="4480f-109">**Stop-AzDataFactoryV2Trigger** Cmdlet 會停止資料工廠中的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="4480f-109">The **Stop-AzDataFactoryV2Trigger** cmdlet stops a trigger in a data factory.</span></span> <span data-ttu-id="4480f-110">如果觸發程式位於 'Started' 狀態，Cmdlet 會停止觸發程式，不再會啟動管線。</span><span class="sxs-lookup"><span data-stu-id="4480f-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="4480f-111">如果觸發人已經進入 '已停止' 狀態，此 Cmdlet 沒有作用。</span><span class="sxs-lookup"><span data-stu-id="4480f-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span> <span data-ttu-id="4480f-112">如果已指定 Force 參數，Cmdlet 不會在停止觸發之前提示。</span><span class="sxs-lookup"><span data-stu-id="4480f-112">If the Force parameter is specified, the cmdlet doesn't prompt before stopping the trigger.</span></span>

## <span data-ttu-id="4480f-113">例子</span><span class="sxs-lookup"><span data-stu-id="4480f-113">EXAMPLES</span></span>

### <span data-ttu-id="4480f-114">範例 1：停止觸發</span><span class="sxs-lookup"><span data-stu-id="4480f-114">Example 1: Stop a trigger</span></span>
```
Stop-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to stop trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="4480f-115">在資料工廠 「WikiADF」中停止名為「ScheduledTri用」的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="4480f-115">Stops a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="4480f-116">參數</span><span class="sxs-lookup"><span data-stu-id="4480f-116">PARAMETERS</span></span>

### <span data-ttu-id="4480f-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4480f-117">-DataFactoryName</span></span>
<span data-ttu-id="4480f-118">資料出廠名稱。</span><span class="sxs-lookup"><span data-stu-id="4480f-118">The data factory name.</span></span>

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

### <span data-ttu-id="4480f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4480f-119">-DefaultProfile</span></span>
<span data-ttu-id="4480f-120">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4480f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4480f-121">-強制</span><span class="sxs-lookup"><span data-stu-id="4480f-121">-Force</span></span>
<span data-ttu-id="4480f-122">執行 Cmdlet 而不提示確認。</span><span class="sxs-lookup"><span data-stu-id="4480f-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="4480f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4480f-123">-InputObject</span></span>
<span data-ttu-id="4480f-124">觸發物件以開始。</span><span class="sxs-lookup"><span data-stu-id="4480f-124">Trigger object to start.</span></span>

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

### <span data-ttu-id="4480f-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="4480f-125">-Name</span></span>
<span data-ttu-id="4480f-126">觸發者名稱。</span><span class="sxs-lookup"><span data-stu-id="4480f-126">The trigger name.</span></span>

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

### <span data-ttu-id="4480f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4480f-127">-ResourceGroupName</span></span>
<span data-ttu-id="4480f-128">資源組名。</span><span class="sxs-lookup"><span data-stu-id="4480f-128">The resource group name.</span></span>

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

### <span data-ttu-id="4480f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4480f-129">-ResourceId</span></span>
<span data-ttu-id="4480f-130">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4480f-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="4480f-131">-確認</span><span class="sxs-lookup"><span data-stu-id="4480f-131">-Confirm</span></span>
<span data-ttu-id="4480f-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4480f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4480f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4480f-133">-WhatIf</span></span>
<span data-ttu-id="4480f-134">顯示如果 Cmdlet 執行，但不執行 Cmdlet 會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4480f-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="4480f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4480f-135">CommonParameters</span></span>
<span data-ttu-id="4480f-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4480f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4480f-137">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="4480f-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4480f-138">輸入</span><span class="sxs-lookup"><span data-stu-id="4480f-138">INPUTS</span></span>

### <span data-ttu-id="4480f-139">System.String</span><span class="sxs-lookup"><span data-stu-id="4480f-139">System.String</span></span>

### <span data-ttu-id="4480f-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="4480f-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="4480f-141">輸出</span><span class="sxs-lookup"><span data-stu-id="4480f-141">OUTPUTS</span></span>

### <span data-ttu-id="4480f-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="4480f-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="4480f-143">筆記</span><span class="sxs-lookup"><span data-stu-id="4480f-143">NOTES</span></span>

## <span data-ttu-id="4480f-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="4480f-144">RELATED LINKS</span></span>

[<span data-ttu-id="4480f-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="4480f-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="4480f-146">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="4480f-146">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="4480f-147">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="4480f-147">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="4480f-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="4480f-148">Remove-AzDataFactoryV2Trigger</span></span>]()
