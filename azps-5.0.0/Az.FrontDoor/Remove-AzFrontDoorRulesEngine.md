---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorRulesEngine.md
ms.openlocfilehash: e0df270a2cfc409025434a4e9ca64a2234e6e7c1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94136886"
---
# <span data-ttu-id="c3c63-101">Remove-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="c3c63-101">Remove-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="c3c63-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c3c63-102">SYNOPSIS</span></span>
<span data-ttu-id="c3c63-103">從前門移除規則引擎</span><span class="sxs-lookup"><span data-stu-id="c3c63-103">Remove Rules Engine from Front Door</span></span>

## <span data-ttu-id="c3c63-104">句法</span><span class="sxs-lookup"><span data-stu-id="c3c63-104">SYNTAX</span></span>

### <span data-ttu-id="c3c63-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c3c63-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3c63-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3c63-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorRulesEngine -InputObject <PSRulesEngine> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3c63-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3c63-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorRulesEngine -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3c63-108">說明</span><span class="sxs-lookup"><span data-stu-id="c3c63-108">DESCRIPTION</span></span>
<span data-ttu-id="c3c63-109">從前門移除規則引擎</span><span class="sxs-lookup"><span data-stu-id="c3c63-109">Remove Rules Engine from Front Door</span></span>

## <span data-ttu-id="c3c63-110">示例</span><span class="sxs-lookup"><span data-stu-id="c3c63-110">EXAMPLES</span></span>

### <span data-ttu-id="c3c63-111">範例1</span><span class="sxs-lookup"><span data-stu-id="c3c63-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name $rulesEngine.Name -PassThru
True
```

<span data-ttu-id="c3c63-112">移除規則引擎設定。</span><span class="sxs-lookup"><span data-stu-id="c3c63-112">Remove rules engine configuration.</span></span>

### <span data-ttu-id="c3c63-113">範例2</span><span class="sxs-lookup"><span data-stu-id="c3c63-113">Example 2</span></span>
```powershell
PS C:> Remove-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name nonexistentRulesEngine
Remove-AzFrontDoorRulesEngine : Rules Engine with name 'nonexistentRulesEngine' in Front Door 'frontDoorName' in the resource group 'resourceGroupName' does not exist.
At line:1 char:1
+ Remove-AzFrontDoorRulesEngine -ResourceGroupName resourceGroupName -Fro ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+ CategoryInfo          : CloseError: (:) [Remove-AzFrontDoorRulesEngine], PSArgumentException
+ FullyQualifiedErrorId : Microsoft.Azure.Commands.FrontDoor.Cmdlets.RemoveFrontDoorRulesEngine
```

<span data-ttu-id="c3c63-114">移除不存在的規則引擎配置時預期的結果。</span><span class="sxs-lookup"><span data-stu-id="c3c63-114">Expected outcome when removing a nonexistent rules engine configuration.</span></span>

## <span data-ttu-id="c3c63-115">參數</span><span class="sxs-lookup"><span data-stu-id="c3c63-115">PARAMETERS</span></span>

### <span data-ttu-id="c3c63-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3c63-116">-DefaultProfile</span></span>
<span data-ttu-id="c3c63-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c3c63-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3c63-118">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="c3c63-118">-FrontDoorName</span></span>
<span data-ttu-id="c3c63-119">前門名稱。</span><span class="sxs-lookup"><span data-stu-id="c3c63-119">Front Door name.</span></span>

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

### <span data-ttu-id="c3c63-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3c63-120">-InputObject</span></span>
<span data-ttu-id="c3c63-121">要更新的規則引擎物件。</span><span class="sxs-lookup"><span data-stu-id="c3c63-121">The Rules Engine object to update.</span></span>

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

### <span data-ttu-id="c3c63-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="c3c63-122">-Name</span></span>
<span data-ttu-id="c3c63-123">規則引擎名稱。</span><span class="sxs-lookup"><span data-stu-id="c3c63-123">Rules engine name.</span></span>

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

### <span data-ttu-id="c3c63-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c3c63-124">-PassThru</span></span>
<span data-ttu-id="c3c63-125">如果指定) ，則傳回物件 (。</span><span class="sxs-lookup"><span data-stu-id="c3c63-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="c3c63-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3c63-126">-ResourceGroupName</span></span>
<span data-ttu-id="c3c63-127">在其中建立前蓋的資源群組名稱。</span><span class="sxs-lookup"><span data-stu-id="c3c63-127">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="c3c63-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3c63-128">-ResourceId</span></span>
<span data-ttu-id="c3c63-129">要更新之 RulesEngine 的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c3c63-129">Resource Id of the RulesEngine to update</span></span>

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

### <span data-ttu-id="c3c63-130">-確認</span><span class="sxs-lookup"><span data-stu-id="c3c63-130">-Confirm</span></span>
<span data-ttu-id="c3c63-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c3c63-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3c63-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3c63-132">-WhatIf</span></span>
<span data-ttu-id="c3c63-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c3c63-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c3c63-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c3c63-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3c63-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3c63-135">CommonParameters</span></span>
<span data-ttu-id="c3c63-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c3c63-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3c63-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c3c63-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3c63-138">輸入</span><span class="sxs-lookup"><span data-stu-id="c3c63-138">INPUTS</span></span>

### <span data-ttu-id="c3c63-139">PSRulesEngine 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="c3c63-139">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

### <span data-ttu-id="c3c63-140">System.object</span><span class="sxs-lookup"><span data-stu-id="c3c63-140">System.String</span></span>

## <span data-ttu-id="c3c63-141">輸出</span><span class="sxs-lookup"><span data-stu-id="c3c63-141">OUTPUTS</span></span>

### <span data-ttu-id="c3c63-142">System.object</span><span class="sxs-lookup"><span data-stu-id="c3c63-142">System.Boolean</span></span>

## <span data-ttu-id="c3c63-143">筆記</span><span class="sxs-lookup"><span data-stu-id="c3c63-143">NOTES</span></span>

## <span data-ttu-id="c3c63-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="c3c63-144">RELATED LINKS</span></span>