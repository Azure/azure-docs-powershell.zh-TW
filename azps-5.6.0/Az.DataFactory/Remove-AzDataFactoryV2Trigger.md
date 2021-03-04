---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
ms.openlocfilehash: df23225193b0b7fe057b13b5114bb3ce227d584e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916631"
---
# <span data-ttu-id="16b75-101">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="16b75-101">Remove-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="16b75-102">簡介</span><span class="sxs-lookup"><span data-stu-id="16b75-102">SYNOPSIS</span></span>
<span data-ttu-id="16b75-103">從資料工廠移除觸發項。</span><span class="sxs-lookup"><span data-stu-id="16b75-103">Removes a trigger from a data factory.</span></span>

## <span data-ttu-id="16b75-104">語法</span><span class="sxs-lookup"><span data-stu-id="16b75-104">SYNTAX</span></span>

### <span data-ttu-id="16b75-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="16b75-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16b75-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="16b75-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16b75-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="16b75-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16b75-108">描述</span><span class="sxs-lookup"><span data-stu-id="16b75-108">DESCRIPTION</span></span>
<span data-ttu-id="16b75-109">**Remove-AzDataFactoryV2Trigger Cmdlet** 會從資料工廠移除觸發程式。</span><span class="sxs-lookup"><span data-stu-id="16b75-109">The **Remove-AzDataFactoryV2Trigger** cmdlet removes a trigger from a data factory.</span></span> <span data-ttu-id="16b75-110">如果 _已指定 Force_ 參數，Cmdlet 不會在移除觸發之前提示。</span><span class="sxs-lookup"><span data-stu-id="16b75-110">If the _Force_ parameter is specified, the cmdlet doesn't prompt before removing the trigger.</span></span>

## <span data-ttu-id="16b75-111">例子</span><span class="sxs-lookup"><span data-stu-id="16b75-111">EXAMPLES</span></span>

### <span data-ttu-id="16b75-112">範例 1：移除觸發項</span><span class="sxs-lookup"><span data-stu-id="16b75-112">Example 1: Remove a trigger</span></span>
```
Remove-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger"

Confirm
Are you sure you want to remove trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="16b75-113">從資料工廠的 「WikiADF」移除名為「ScheduledTri用」的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="16b75-113">Remove a trigger called "ScheduledTrigger" from the data factory "WikiADF".</span></span>

## <span data-ttu-id="16b75-114">參數</span><span class="sxs-lookup"><span data-stu-id="16b75-114">PARAMETERS</span></span>

### <span data-ttu-id="16b75-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="16b75-115">-DataFactoryName</span></span>
<span data-ttu-id="16b75-116">資料出廠名稱。</span><span class="sxs-lookup"><span data-stu-id="16b75-116">The data factory name.</span></span>

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

### <span data-ttu-id="16b75-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16b75-117">-DefaultProfile</span></span>
<span data-ttu-id="16b75-118">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="16b75-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16b75-119">-強制</span><span class="sxs-lookup"><span data-stu-id="16b75-119">-Force</span></span>
<span data-ttu-id="16b75-120">執行 Cmdlet 而不提示確認。</span><span class="sxs-lookup"><span data-stu-id="16b75-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="16b75-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16b75-121">-InputObject</span></span>
<span data-ttu-id="16b75-122">要移除的觸發物件。</span><span class="sxs-lookup"><span data-stu-id="16b75-122">The Trigger object to remove.</span></span>

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

### <span data-ttu-id="16b75-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="16b75-123">-Name</span></span>
<span data-ttu-id="16b75-124">觸發者名稱。</span><span class="sxs-lookup"><span data-stu-id="16b75-124">The trigger name.</span></span>

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

### <span data-ttu-id="16b75-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16b75-125">-ResourceGroupName</span></span>
<span data-ttu-id="16b75-126">資源組名。</span><span class="sxs-lookup"><span data-stu-id="16b75-126">The resource group name.</span></span>

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

### <span data-ttu-id="16b75-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16b75-127">-ResourceId</span></span>
<span data-ttu-id="16b75-128">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="16b75-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="16b75-129">-確認</span><span class="sxs-lookup"><span data-stu-id="16b75-129">-Confirm</span></span>
<span data-ttu-id="16b75-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="16b75-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16b75-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16b75-131">-WhatIf</span></span>
<span data-ttu-id="16b75-132">顯示如果 Cmdlet 執行，但不執行 Cmdlet 會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="16b75-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="16b75-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16b75-133">CommonParameters</span></span>
<span data-ttu-id="16b75-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="16b75-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16b75-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="16b75-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16b75-136">輸入</span><span class="sxs-lookup"><span data-stu-id="16b75-136">INPUTS</span></span>

### <span data-ttu-id="16b75-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="16b75-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

### <span data-ttu-id="16b75-138">System.String</span><span class="sxs-lookup"><span data-stu-id="16b75-138">System.String</span></span>

## <span data-ttu-id="16b75-139">輸出</span><span class="sxs-lookup"><span data-stu-id="16b75-139">OUTPUTS</span></span>

### <span data-ttu-id="16b75-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="16b75-140">System.Boolean</span></span>

## <span data-ttu-id="16b75-141">筆記</span><span class="sxs-lookup"><span data-stu-id="16b75-141">NOTES</span></span>

## <span data-ttu-id="16b75-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="16b75-142">RELATED LINKS</span></span>

[<span data-ttu-id="16b75-143">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="16b75-143">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="16b75-144">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="16b75-144">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="16b75-145">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="16b75-145">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="16b75-146">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="16b75-146">Stop-AzDataFactoryV2Trigger</span></span>]()

