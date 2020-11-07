---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: d49e04f4a791f6cbf5d609d6553fddcc26dc34e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624834"
---
# <span data-ttu-id="315dc-101">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="315dc-101">Start-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="315dc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="315dc-102">SYNOPSIS</span></span>
<span data-ttu-id="315dc-103">在資料工廠中啟動觸發程式。</span><span class="sxs-lookup"><span data-stu-id="315dc-103">Starts a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="315dc-104">句法</span><span class="sxs-lookup"><span data-stu-id="315dc-104">SYNTAX</span></span>

### <span data-ttu-id="315dc-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="315dc-105">ByFactoryName (Default)</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="315dc-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="315dc-106">ByInputObject</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="315dc-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="315dc-107">ByResourceId</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="315dc-108">說明</span><span class="sxs-lookup"><span data-stu-id="315dc-108">DESCRIPTION</span></span>
<span data-ttu-id="315dc-109">AzureRmDataFactoryV2Trigger Cmdlet 會在資料工廠中啟動觸發 **程式** 。</span><span class="sxs-lookup"><span data-stu-id="315dc-109">The **Start-AzureRmDataFactoryV2Trigger** cmdlet starts a trigger in a data factory.</span></span> <span data-ttu-id="315dc-110">如果觸發程式處於「已停止」狀態，則該 Cmdlet 會啟動觸發程式，而且最終會根據其定義來調用管線。</span><span class="sxs-lookup"><span data-stu-id="315dc-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="315dc-111">如果觸發程式已處於「已啟動」狀態，則此 Cmdlet 不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="315dc-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span> <span data-ttu-id="315dc-112">如果指定了 Force 參數，則在啟動觸發程式前，不會提示 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="315dc-112">If the Force parameter is specified, the cmdlet doesn't prompt before starting the trigger.</span></span>

## <span data-ttu-id="315dc-113">示例</span><span class="sxs-lookup"><span data-stu-id="315dc-113">EXAMPLES</span></span>

### <span data-ttu-id="315dc-114">範例1：啟動觸發程式</span><span class="sxs-lookup"><span data-stu-id="315dc-114">Example 1: Start a trigger</span></span>
```
Start-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to start trigger 'ScheduledTrigger' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="315dc-115">在資料工廠 "WikiADF" 中啟動名為 "ScheduledTrigger" 的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="315dc-115">Starts a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="315dc-116">參數</span><span class="sxs-lookup"><span data-stu-id="315dc-116">PARAMETERS</span></span>

### <span data-ttu-id="315dc-117">-確認</span><span class="sxs-lookup"><span data-stu-id="315dc-117">-Confirm</span></span>
<span data-ttu-id="315dc-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="315dc-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="315dc-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="315dc-119">-DataFactoryName</span></span>
<span data-ttu-id="315dc-120">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="315dc-120">The data factory name.</span></span>

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

### <span data-ttu-id="315dc-121">-Force</span><span class="sxs-lookup"><span data-stu-id="315dc-121">-Force</span></span>
<span data-ttu-id="315dc-122">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="315dc-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="315dc-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="315dc-123">-Name</span></span>
<span data-ttu-id="315dc-124">觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="315dc-124">The trigger name.</span></span>

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

### <span data-ttu-id="315dc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="315dc-125">-ResourceGroupName</span></span>
<span data-ttu-id="315dc-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="315dc-126">The resource group name.</span></span>

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

### <span data-ttu-id="315dc-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="315dc-127">-ResourceId</span></span>
<span data-ttu-id="315dc-128">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="315dc-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="315dc-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="315dc-129">-InputObject</span></span>
<span data-ttu-id="315dc-130">觸發要啟動的物件。</span><span class="sxs-lookup"><span data-stu-id="315dc-130">Trigger object to start.</span></span>

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

### <span data-ttu-id="315dc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="315dc-131">-WhatIf</span></span>
<span data-ttu-id="315dc-132">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="315dc-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="315dc-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="315dc-133">-DefaultProfile</span></span>
<span data-ttu-id="315dc-134">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="315dc-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="315dc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="315dc-135">CommonParameters</span></span>
<span data-ttu-id="315dc-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="315dc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="315dc-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="315dc-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="315dc-138">輸入</span><span class="sxs-lookup"><span data-stu-id="315dc-138">INPUTS</span></span>

### <span data-ttu-id="315dc-139">System.object</span><span class="sxs-lookup"><span data-stu-id="315dc-139">System.String</span></span>
<span data-ttu-id="315dc-140">PSTrigger 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="315dc-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="315dc-141">輸出</span><span class="sxs-lookup"><span data-stu-id="315dc-141">OUTPUTS</span></span>

### <span data-ttu-id="315dc-142">[System.object]。清單 ' 1 [DataFactoryV2. PSTrigger，DataFactoryV2，版本 = 0.1.9.0，Culture = 中性，PublicKeyToken = null]]。）））</span><span class="sxs-lookup"><span data-stu-id="315dc-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="315dc-143">PSTrigger 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="315dc-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="315dc-144">筆記</span><span class="sxs-lookup"><span data-stu-id="315dc-144">NOTES</span></span>

## <span data-ttu-id="315dc-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="315dc-145">RELATED LINKS</span></span>

[<span data-ttu-id="315dc-146">AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="315dc-146">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="315dc-147">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="315dc-147">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="315dc-148">停止 AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="315dc-148">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="315dc-149">移除-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="315dc-149">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
