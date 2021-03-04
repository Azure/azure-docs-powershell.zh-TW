---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/remove-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorRulesEngine.md
ms.openlocfilehash: 84bcc64127636adc318935d1a7fd97f7ce79d760
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917730"
---
# <span data-ttu-id="bc851-101">Remove-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="bc851-101">Remove-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="bc851-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bc851-102">SYNOPSIS</span></span>
<span data-ttu-id="bc851-103">從前門移除規則引擎</span><span class="sxs-lookup"><span data-stu-id="bc851-103">Remove Rules Engine from Front Door</span></span>

## <span data-ttu-id="bc851-104">語法</span><span class="sxs-lookup"><span data-stu-id="bc851-104">SYNTAX</span></span>

### <span data-ttu-id="bc851-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="bc851-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc851-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc851-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorRulesEngine -InputObject <PSRulesEngine> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc851-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc851-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorRulesEngine -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc851-108">描述</span><span class="sxs-lookup"><span data-stu-id="bc851-108">DESCRIPTION</span></span>
<span data-ttu-id="bc851-109">從前門移除規則引擎</span><span class="sxs-lookup"><span data-stu-id="bc851-109">Remove Rules Engine from Front Door</span></span>

## <span data-ttu-id="bc851-110">例子</span><span class="sxs-lookup"><span data-stu-id="bc851-110">EXAMPLES</span></span>

### <span data-ttu-id="bc851-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="bc851-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name $rulesEngine.Name -PassThru
True
```

<span data-ttu-id="bc851-112">移除規則引擎組配置。</span><span class="sxs-lookup"><span data-stu-id="bc851-112">Remove rules engine configuration.</span></span>

### <span data-ttu-id="bc851-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="bc851-113">Example 2</span></span>
```powershell
PS C:> Remove-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name nonexistentRulesEngine
Remove-AzFrontDoorRulesEngine : Rules Engine with name 'nonexistentRulesEngine' in Front Door 'frontDoorName' in the resource group 'resourceGroupName' does not exist.
At line:1 char:1
+ Remove-AzFrontDoorRulesEngine -ResourceGroupName resourceGroupName -Fro ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+ CategoryInfo          : CloseError: (:) [Remove-AzFrontDoorRulesEngine], PSArgumentException
+ FullyQualifiedErrorId : Microsoft.Azure.Commands.FrontDoor.Cmdlets.RemoveFrontDoorRulesEngine
```

<span data-ttu-id="bc851-114">移除不存在的規則引擎組式時的預期結果。</span><span class="sxs-lookup"><span data-stu-id="bc851-114">Expected outcome when removing a nonexistent rules engine configuration.</span></span>

## <span data-ttu-id="bc851-115">參數</span><span class="sxs-lookup"><span data-stu-id="bc851-115">PARAMETERS</span></span>

### <span data-ttu-id="bc851-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc851-116">-DefaultProfile</span></span>
<span data-ttu-id="bc851-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="bc851-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc851-118">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="bc851-118">-FrontDoorName</span></span>
<span data-ttu-id="bc851-119">前門名稱。</span><span class="sxs-lookup"><span data-stu-id="bc851-119">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc851-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bc851-120">-InputObject</span></span>
<span data-ttu-id="bc851-121">要更新的規則引擎物件。</span><span class="sxs-lookup"><span data-stu-id="bc851-121">The Rules Engine object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc851-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="bc851-122">-Name</span></span>
<span data-ttu-id="bc851-123">規則引擎名稱。</span><span class="sxs-lookup"><span data-stu-id="bc851-123">Rules engine name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc851-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bc851-124">-PassThru</span></span>
<span data-ttu-id="bc851-125">如果指定 (，則) 。</span><span class="sxs-lookup"><span data-stu-id="bc851-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="bc851-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc851-126">-ResourceGroupName</span></span>
<span data-ttu-id="bc851-127">要建立前門的資源組名。</span><span class="sxs-lookup"><span data-stu-id="bc851-127">The resource group name that the Front Door will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc851-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bc851-128">-ResourceId</span></span>
<span data-ttu-id="bc851-129">要更新之 RulesEngine 的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="bc851-129">Resource Id of the RulesEngine to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc851-130">-確認</span><span class="sxs-lookup"><span data-stu-id="bc851-130">-Confirm</span></span>
<span data-ttu-id="bc851-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="bc851-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc851-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc851-132">-WhatIf</span></span>
<span data-ttu-id="bc851-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bc851-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bc851-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bc851-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc851-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc851-135">CommonParameters</span></span>
<span data-ttu-id="bc851-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bc851-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc851-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bc851-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc851-138">輸入</span><span class="sxs-lookup"><span data-stu-id="bc851-138">INPUTS</span></span>

### <span data-ttu-id="bc851-139">Microsoft.Azure.Commands.FrontDoor.models.PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="bc851-139">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

### <span data-ttu-id="bc851-140">System.String</span><span class="sxs-lookup"><span data-stu-id="bc851-140">System.String</span></span>

## <span data-ttu-id="bc851-141">輸出</span><span class="sxs-lookup"><span data-stu-id="bc851-141">OUTPUTS</span></span>

### <span data-ttu-id="bc851-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bc851-142">System.Boolean</span></span>

## <span data-ttu-id="bc851-143">筆記</span><span class="sxs-lookup"><span data-stu-id="bc851-143">NOTES</span></span>

## <span data-ttu-id="bc851-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="bc851-144">RELATED LINKS</span></span>
