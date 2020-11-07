---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 8e4f547d615a88957ffbf133dd725e2453ef7a11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624831"
---
# <span data-ttu-id="81c33-101">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="81c33-101">Stop-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="81c33-102">摘要</span><span class="sxs-lookup"><span data-stu-id="81c33-102">SYNOPSIS</span></span>
<span data-ttu-id="81c33-103">停止資料工廠中的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="81c33-103">Stops a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81c33-104">句法</span><span class="sxs-lookup"><span data-stu-id="81c33-104">SYNTAX</span></span>

### <span data-ttu-id="81c33-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="81c33-105">ByFactoryName (Default)</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81c33-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="81c33-106">ByInputObject</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81c33-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="81c33-107">ByResourceId</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81c33-108">說明</span><span class="sxs-lookup"><span data-stu-id="81c33-108">DESCRIPTION</span></span>
<span data-ttu-id="81c33-109">**AzureRmDataFactoryV2Trigger** Cmdlet 會在資料工廠中停止觸發程式。</span><span class="sxs-lookup"><span data-stu-id="81c33-109">The **Stop-AzureRmDataFactoryV2Trigger** cmdlet stops a trigger in a data factory.</span></span> <span data-ttu-id="81c33-110">如果觸發程式處於「已啟動」狀態，則該 Cmdlet 會停止觸發程式，而且不會再叫管線。</span><span class="sxs-lookup"><span data-stu-id="81c33-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="81c33-111">如果觸發程式已處於「已停止」狀態，則此 Cmdlet 沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="81c33-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span> <span data-ttu-id="81c33-112">如果指定了 Force 參數，則在停止觸發程式前，不會提示 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="81c33-112">If the Force parameter is specified, the cmdlet doesn't prompt before stopping the trigger.</span></span>

## <span data-ttu-id="81c33-113">示例</span><span class="sxs-lookup"><span data-stu-id="81c33-113">EXAMPLES</span></span>

### <span data-ttu-id="81c33-114">範例1：停止觸發程式</span><span class="sxs-lookup"><span data-stu-id="81c33-114">Example 1: Stop a trigger</span></span>
```
Stop-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to stop trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="81c33-115">停止資料工廠 "WikiADF" 中名為 "ScheduledTrigger" 的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="81c33-115">Stops a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="81c33-116">參數</span><span class="sxs-lookup"><span data-stu-id="81c33-116">PARAMETERS</span></span>

### <span data-ttu-id="81c33-117">-確認</span><span class="sxs-lookup"><span data-stu-id="81c33-117">-Confirm</span></span>
<span data-ttu-id="81c33-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="81c33-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81c33-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="81c33-119">-DataFactoryName</span></span>
<span data-ttu-id="81c33-120">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="81c33-120">The data factory name.</span></span>

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

### <span data-ttu-id="81c33-121">-Force</span><span class="sxs-lookup"><span data-stu-id="81c33-121">-Force</span></span>
<span data-ttu-id="81c33-122">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="81c33-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="81c33-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="81c33-123">-Name</span></span>
<span data-ttu-id="81c33-124">觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="81c33-124">The trigger name.</span></span>

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

### <span data-ttu-id="81c33-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81c33-125">-ResourceGroupName</span></span>
<span data-ttu-id="81c33-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="81c33-126">The resource group name.</span></span>

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

### <span data-ttu-id="81c33-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81c33-127">-ResourceId</span></span>
<span data-ttu-id="81c33-128">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="81c33-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="81c33-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81c33-129">-InputObject</span></span>
<span data-ttu-id="81c33-130">觸發要啟動的物件。</span><span class="sxs-lookup"><span data-stu-id="81c33-130">Trigger object to start.</span></span>

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

### <span data-ttu-id="81c33-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81c33-131">-WhatIf</span></span>
<span data-ttu-id="81c33-132">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="81c33-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="81c33-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81c33-133">-DefaultProfile</span></span>
<span data-ttu-id="81c33-134">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="81c33-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81c33-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81c33-135">CommonParameters</span></span>
<span data-ttu-id="81c33-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="81c33-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81c33-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="81c33-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81c33-138">輸入</span><span class="sxs-lookup"><span data-stu-id="81c33-138">INPUTS</span></span>

### <span data-ttu-id="81c33-139">System.object</span><span class="sxs-lookup"><span data-stu-id="81c33-139">System.String</span></span>
<span data-ttu-id="81c33-140">PSTrigger 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="81c33-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="81c33-141">輸出</span><span class="sxs-lookup"><span data-stu-id="81c33-141">OUTPUTS</span></span>

### <span data-ttu-id="81c33-142">[System.object]。清單 ' 1 [DataFactoryV2. PSTrigger，DataFactoryV2，版本 = 0.1.9.0，Culture = 中性，PublicKeyToken = null]]。）））</span><span class="sxs-lookup"><span data-stu-id="81c33-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="81c33-143">PSTrigger 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="81c33-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="81c33-144">筆記</span><span class="sxs-lookup"><span data-stu-id="81c33-144">NOTES</span></span>

## <span data-ttu-id="81c33-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="81c33-145">RELATED LINKS</span></span>

[<span data-ttu-id="81c33-146">AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="81c33-146">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="81c33-147">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="81c33-147">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="81c33-148">開始-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="81c33-148">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="81c33-149">移除-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="81c33-149">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
