---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
ms.openlocfilehash: 05248a299b907c74f43edddb7caf18697794dc08
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906666"
---
# <span data-ttu-id="3a415-101">New-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="3a415-101">New-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="3a415-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3a415-102">SYNOPSIS</span></span>
<span data-ttu-id="3a415-103">為指定的前門建立新規則引擎組。</span><span class="sxs-lookup"><span data-stu-id="3a415-103">Create a new rules engine configuration for a specified front door.</span></span> 

## <span data-ttu-id="3a415-104">語法</span><span class="sxs-lookup"><span data-stu-id="3a415-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 [-Rule <PSRulesEngineRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3a415-105">描述</span><span class="sxs-lookup"><span data-stu-id="3a415-105">DESCRIPTION</span></span>
<span data-ttu-id="3a415-106">為指定的前門建立新規則引擎組。</span><span class="sxs-lookup"><span data-stu-id="3a415-106">Create a new rules engine configuration for a specified front door.</span></span> 

<span data-ttu-id="3a415-107">使用 Cmdlet "New-AzFrontDoorRulesEngineRule" 來建構規則引擎規則，以傳遞至此 Cmdlet 的 "-Rules" 參數。</span><span class="sxs-lookup"><span data-stu-id="3a415-107">Use cmdlet "New-AzFrontDoorRulesEngineRule" to construct rules engine rules to pass into the "-Rules" parameter of this cmdlet.</span></span>

## <span data-ttu-id="3a415-108">例子</span><span class="sxs-lookup"><span data-stu-id="3a415-108">EXAMPLES</span></span>

### <span data-ttu-id="3a415-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="3a415-109">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name myRulesEngine -Rule $rulesEngineRule1

Name          RulesEngineRules
----          ----------------
myRulesEngine {rules1}
```

<span data-ttu-id="3a415-110">為指定的前門建立新規則引擎組。</span><span class="sxs-lookup"><span data-stu-id="3a415-110">Create a new rules engine configuration for specified front door.</span></span>

## <span data-ttu-id="3a415-111">參數</span><span class="sxs-lookup"><span data-stu-id="3a415-111">PARAMETERS</span></span>

### <span data-ttu-id="3a415-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a415-112">-DefaultProfile</span></span>
<span data-ttu-id="3a415-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3a415-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a415-114">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="3a415-114">-FrontDoorName</span></span>
<span data-ttu-id="3a415-115">前門名稱。</span><span class="sxs-lookup"><span data-stu-id="3a415-115">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a415-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="3a415-116">-Name</span></span>
<span data-ttu-id="3a415-117">規則引擎名稱。</span><span class="sxs-lookup"><span data-stu-id="3a415-117">Rules engine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a415-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a415-118">-ResourceGroupName</span></span>
<span data-ttu-id="3a415-119">要建立前門的資源組名。</span><span class="sxs-lookup"><span data-stu-id="3a415-119">The resource group name that the Front Door will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a415-120">-規則</span><span class="sxs-lookup"><span data-stu-id="3a415-120">-Rule</span></span>
<span data-ttu-id="3a415-121">定義特定規則引擎群組原則的規則清單。</span><span class="sxs-lookup"><span data-stu-id="3a415-121">A list of rules that define a particular Rules Engine Configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a415-122">-確認</span><span class="sxs-lookup"><span data-stu-id="3a415-122">-Confirm</span></span>
<span data-ttu-id="3a415-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3a415-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a415-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a415-124">-WhatIf</span></span>
<span data-ttu-id="3a415-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3a415-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3a415-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3a415-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a415-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a415-127">CommonParameters</span></span>
<span data-ttu-id="3a415-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3a415-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a415-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3a415-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a415-130">輸入</span><span class="sxs-lookup"><span data-stu-id="3a415-130">INPUTS</span></span>

### <span data-ttu-id="3a415-131">沒有</span><span class="sxs-lookup"><span data-stu-id="3a415-131">None</span></span>

## <span data-ttu-id="3a415-132">輸出</span><span class="sxs-lookup"><span data-stu-id="3a415-132">OUTPUTS</span></span>

### <span data-ttu-id="3a415-133">Microsoft.Azure.Commands.FrontDoor.models.PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="3a415-133">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="3a415-134">筆記</span><span class="sxs-lookup"><span data-stu-id="3a415-134">NOTES</span></span>

## <span data-ttu-id="3a415-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="3a415-135">RELATED LINKS</span></span>
