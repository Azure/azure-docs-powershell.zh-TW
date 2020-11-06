---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 771097c11aceabb9bd2011c6024e469a37a39f4e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444951"
---
# <span data-ttu-id="744ba-101">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="744ba-101">Remove-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="744ba-102">摘要</span><span class="sxs-lookup"><span data-stu-id="744ba-102">SYNOPSIS</span></span>
<span data-ttu-id="744ba-103">從資料工廠移除觸發程式。</span><span class="sxs-lookup"><span data-stu-id="744ba-103">Removes a trigger from a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="744ba-104">句法</span><span class="sxs-lookup"><span data-stu-id="744ba-104">SYNTAX</span></span>

### <span data-ttu-id="744ba-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="744ba-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="744ba-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="744ba-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="744ba-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="744ba-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="744ba-108">說明</span><span class="sxs-lookup"><span data-stu-id="744ba-108">DESCRIPTION</span></span>
<span data-ttu-id="744ba-109">AzureRmDataFactoryV2Trigger Cmdlet 會從資料工廠中移除觸發 **程式** 。</span><span class="sxs-lookup"><span data-stu-id="744ba-109">The **Remove-AzureRmDataFactoryV2Trigger** cmdlet removes a trigger from a data factory.</span></span> <span data-ttu-id="744ba-110">如果指定了 _Force_ 參數，則在移除觸發程式之前，Cmdlet 不會提示。</span><span class="sxs-lookup"><span data-stu-id="744ba-110">If the _Force_ parameter is specified, the cmdlet doesn't prompt before removing the trigger.</span></span>

## <span data-ttu-id="744ba-111">示例</span><span class="sxs-lookup"><span data-stu-id="744ba-111">EXAMPLES</span></span>

### <span data-ttu-id="744ba-112">範例1：移除觸發程式</span><span class="sxs-lookup"><span data-stu-id="744ba-112">Example 1: Remove a trigger</span></span>
```
Remove-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger"

Confirm
Are you sure you want to remove trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="744ba-113">從資料工廠 "WikiADF" 移除名為 "ScheduledTrigger" 的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="744ba-113">Remove a trigger called "ScheduledTrigger" from the data factory "WikiADF".</span></span>

## <span data-ttu-id="744ba-114">參數</span><span class="sxs-lookup"><span data-stu-id="744ba-114">PARAMETERS</span></span>

### <span data-ttu-id="744ba-115">-確認</span><span class="sxs-lookup"><span data-stu-id="744ba-115">-Confirm</span></span>
<span data-ttu-id="744ba-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="744ba-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="744ba-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="744ba-117">-DataFactoryName</span></span>
<span data-ttu-id="744ba-118">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="744ba-118">The data factory name.</span></span>

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

### <span data-ttu-id="744ba-119">-Force</span><span class="sxs-lookup"><span data-stu-id="744ba-119">-Force</span></span>
<span data-ttu-id="744ba-120">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="744ba-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="744ba-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="744ba-121">-Name</span></span>
<span data-ttu-id="744ba-122">觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="744ba-122">The trigger name.</span></span>

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

### <span data-ttu-id="744ba-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="744ba-123">-ResourceGroupName</span></span>
<span data-ttu-id="744ba-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="744ba-124">The resource group name.</span></span>

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

### <span data-ttu-id="744ba-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="744ba-125">-ResourceId</span></span>
<span data-ttu-id="744ba-126">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="744ba-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="744ba-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="744ba-127">-InputObject</span></span>
<span data-ttu-id="744ba-128">要移除的觸發程式物件。</span><span class="sxs-lookup"><span data-stu-id="744ba-128">The Trigger object to remove.</span></span>

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

### <span data-ttu-id="744ba-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="744ba-129">-WhatIf</span></span>
<span data-ttu-id="744ba-130">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="744ba-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="744ba-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="744ba-131">-DefaultProfile</span></span>
<span data-ttu-id="744ba-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="744ba-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="744ba-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="744ba-133">CommonParameters</span></span>
<span data-ttu-id="744ba-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="744ba-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="744ba-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="744ba-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="744ba-136">輸入</span><span class="sxs-lookup"><span data-stu-id="744ba-136">INPUTS</span></span>

### <span data-ttu-id="744ba-137">PSTrigger 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="744ba-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>
<span data-ttu-id="744ba-138">System.object</span><span class="sxs-lookup"><span data-stu-id="744ba-138">System.String</span></span>

## <span data-ttu-id="744ba-139">輸出</span><span class="sxs-lookup"><span data-stu-id="744ba-139">OUTPUTS</span></span>

### <span data-ttu-id="744ba-140">System.object</span><span class="sxs-lookup"><span data-stu-id="744ba-140">System.Object</span></span>

## <span data-ttu-id="744ba-141">筆記</span><span class="sxs-lookup"><span data-stu-id="744ba-141">NOTES</span></span>

## <span data-ttu-id="744ba-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="744ba-142">RELATED LINKS</span></span>

[<span data-ttu-id="744ba-143">AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="744ba-143">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="744ba-144">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="744ba-144">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="744ba-145">開始-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="744ba-145">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="744ba-146">停止 AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="744ba-146">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

