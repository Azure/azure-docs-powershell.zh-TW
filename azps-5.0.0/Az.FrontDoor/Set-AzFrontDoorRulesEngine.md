---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/set-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoorRulesEngine.md
ms.openlocfilehash: cf98121f535f60c7d1ddc3b29e33f10fd8f29842
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94136884"
---
# <span data-ttu-id="58f1f-101">Set-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="58f1f-101">Set-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="58f1f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="58f1f-102">SYNOPSIS</span></span>
<span data-ttu-id="58f1f-103">更新規則引擎。</span><span class="sxs-lookup"><span data-stu-id="58f1f-103">Update a Rules Engine.</span></span>

## <span data-ttu-id="58f1f-104">句法</span><span class="sxs-lookup"><span data-stu-id="58f1f-104">SYNTAX</span></span>

### <span data-ttu-id="58f1f-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="58f1f-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 [-Rule <PSRulesEngineRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="58f1f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="58f1f-106">ByObjectParameterSet</span></span>
```
Set-AzFrontDoorRulesEngine -InputObject <PSRulesEngine> [-Rule <PSRulesEngineRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58f1f-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="58f1f-107">ByResourceIdParameterSet</span></span>
```
Set-AzFrontDoorRulesEngine -ResourceId <String> [-Rule <PSRulesEngineRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58f1f-108">說明</span><span class="sxs-lookup"><span data-stu-id="58f1f-108">DESCRIPTION</span></span>
<span data-ttu-id="58f1f-109">更新規則引擎。</span><span class="sxs-lookup"><span data-stu-id="58f1f-109">Update a Rules Engine.</span></span>

## <span data-ttu-id="58f1f-110">示例</span><span class="sxs-lookup"><span data-stu-id="58f1f-110">EXAMPLES</span></span>

### <span data-ttu-id="58f1f-111">範例1</span><span class="sxs-lookup"><span data-stu-id="58f1f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name myRulesEngine

Name          RulesEngineRules
----          ----------------
myRulesEngine {rules1}

PS C:\> $rulesEngineRule2 = New-AzFrontDoorRulesEngineRuleObject -Name rules2 -Priority 3 -Action $rulesEngineAction
PS C:\AFD\azure-powershell\artifacts\Debug\Az.FrontDoor> Set-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name myRulesEngine -Rule $rulesEngineRule1, $rulesEngineRule2

Name          RulesEngineRules
----          ----------------
myRulesEngine {rules1, rules2}
```

<span data-ttu-id="58f1f-112">取得現有的規則引擎設定，並將另一個規則引擎規則新增到其中。</span><span class="sxs-lookup"><span data-stu-id="58f1f-112">Get an existing rules engine configuration and add another rules engine rule to it.</span></span>

## <span data-ttu-id="58f1f-113">參數</span><span class="sxs-lookup"><span data-stu-id="58f1f-113">PARAMETERS</span></span>

### <span data-ttu-id="58f1f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58f1f-114">-DefaultProfile</span></span>
<span data-ttu-id="58f1f-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="58f1f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58f1f-116">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="58f1f-116">-FrontDoorName</span></span>
<span data-ttu-id="58f1f-117">前門名稱。</span><span class="sxs-lookup"><span data-stu-id="58f1f-117">Front Door name.</span></span>

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

### <span data-ttu-id="58f1f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58f1f-118">-InputObject</span></span>
<span data-ttu-id="58f1f-119">要更新的規則引擎物件。</span><span class="sxs-lookup"><span data-stu-id="58f1f-119">The Rules Engine object to update.</span></span>

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

### <span data-ttu-id="58f1f-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="58f1f-120">-Name</span></span>
<span data-ttu-id="58f1f-121">規則引擎名稱。</span><span class="sxs-lookup"><span data-stu-id="58f1f-121">Rules engine name.</span></span>

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

### <span data-ttu-id="58f1f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58f1f-122">-ResourceGroupName</span></span>
<span data-ttu-id="58f1f-123">在其中建立前蓋的資源群組名稱。</span><span class="sxs-lookup"><span data-stu-id="58f1f-123">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="58f1f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58f1f-124">-ResourceId</span></span>
<span data-ttu-id="58f1f-125">要更新之 RulesEngine 的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="58f1f-125">Resource Id of the RulesEngine to update</span></span>

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

### <span data-ttu-id="58f1f-126">-規則</span><span class="sxs-lookup"><span data-stu-id="58f1f-126">-Rule</span></span>
<span data-ttu-id="58f1f-127">定義特定規則引擎配置的規則清單。</span><span class="sxs-lookup"><span data-stu-id="58f1f-127">A list of rules that define a particular Rules Engine Configuration.</span></span>

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

### <span data-ttu-id="58f1f-128">-確認</span><span class="sxs-lookup"><span data-stu-id="58f1f-128">-Confirm</span></span>
<span data-ttu-id="58f1f-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="58f1f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58f1f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58f1f-130">-WhatIf</span></span>
<span data-ttu-id="58f1f-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="58f1f-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="58f1f-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="58f1f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58f1f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58f1f-133">CommonParameters</span></span>
<span data-ttu-id="58f1f-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="58f1f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58f1f-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="58f1f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58f1f-136">輸入</span><span class="sxs-lookup"><span data-stu-id="58f1f-136">INPUTS</span></span>

### <span data-ttu-id="58f1f-137">PSRulesEngine 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="58f1f-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

### <span data-ttu-id="58f1f-138">System.object</span><span class="sxs-lookup"><span data-stu-id="58f1f-138">System.String</span></span>

## <span data-ttu-id="58f1f-139">輸出</span><span class="sxs-lookup"><span data-stu-id="58f1f-139">OUTPUTS</span></span>

### <span data-ttu-id="58f1f-140">PSRulesEngine 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="58f1f-140">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="58f1f-141">筆記</span><span class="sxs-lookup"><span data-stu-id="58f1f-141">NOTES</span></span>

## <span data-ttu-id="58f1f-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="58f1f-142">RELATED LINKS</span></span>