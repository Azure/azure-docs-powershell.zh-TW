---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengineruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineRuleObject.md
ms.openlocfilehash: c02fa092532f70567405f314dc8943e4e2ce51f6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435107"
---
# <span data-ttu-id="b1a63-101">New-AzFrontDoorRulesEngineRuleObject</span><span class="sxs-lookup"><span data-stu-id="b1a63-101">New-AzFrontDoorRulesEngineRuleObject</span></span>

## <span data-ttu-id="b1a63-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b1a63-102">SYNOPSIS</span></span>
<span data-ttu-id="b1a63-103">建立規則引擎建立的 PSRulesEngineRule 物件。</span><span class="sxs-lookup"><span data-stu-id="b1a63-103">Create a PSRulesEngineRule object for Rules Engine creation.</span></span>

## <span data-ttu-id="b1a63-104">句法</span><span class="sxs-lookup"><span data-stu-id="b1a63-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngineRuleObject -Name <String> -Priority <Int32> -Action <PSRulesEngineAction>
 [-MatchProcessingBehavior <PSMatchProcessingBehavior>] [-MatchCondition <PSRulesEngineMatchCondition[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1a63-105">說明</span><span class="sxs-lookup"><span data-stu-id="b1a63-105">DESCRIPTION</span></span>
<span data-ttu-id="b1a63-106">建立規則引擎建立的 PSRulesEngineRule 物件。</span><span class="sxs-lookup"><span data-stu-id="b1a63-106">Create a PSRulesEngineRule object for Rules Engine creation.</span></span>

<span data-ttu-id="b1a63-107">使用 Cmdlet "New-AzFrontDoorRulesEngineActionObject" 建立 PSRulesEngineAction 物件，以傳送到 "-Action" 參數。</span><span class="sxs-lookup"><span data-stu-id="b1a63-107">Use cmdlet "New-AzFrontDoorRulesEngineActionObject" to create PSRulesEngineAction object to pass into the "-Action" parameter.</span></span>
<span data-ttu-id="b1a63-108">使用 Cmdlet "New-AzFrontDoorRulesEngineMatchConditionObject" 建立 PSRulesEngineMatchCondition 物件，以傳送到 "-MatchCondition" 參數。</span><span class="sxs-lookup"><span data-stu-id="b1a63-108">Use cmdlet "New-AzFrontDoorRulesEngineMatchConditionObject" to create PSRulesEngineMatchCondition object to pass into the "-MatchCondition" parameter.</span></span>

## <span data-ttu-id="b1a63-109">示例</span><span class="sxs-lookup"><span data-stu-id="b1a63-109">EXAMPLES</span></span>

### <span data-ttu-id="b1a63-110">範例1</span><span class="sxs-lookup"><span data-stu-id="b1a63-110">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority 0 -Action $rulesEngineAction -MatchProcessingBehavior Stop -MatchCondition $rulesEngineMatchCondition

Name                    : rules1
Priority                : 0
MatchProcessingBehavior : Stop
MatchCondition          : {Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchCondition}
Action                  : Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineAction


PS C:\> $rulesEngineRule1.Action

RequestHeaderActions           ResponseHeaderActions RouteConfigurationOverride
--------------------           --------------------- --------------------------
{headeraction1, headeraction2} {}                    Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingConfigurati�

PS C:\> $rulesEngineRule1.MatchCondition[0]

RulesEngineMatchVariable : RequestHeader
RulesEngineMatchValue    : {allowoverride}
Selector                 : Rules-Engine-Route-Forward
RulesEngineOperator      : Equal
NegateCondition          : False
Transforms               : {Lowercase, Uppercase}
```

<span data-ttu-id="b1a63-111">建立新的 PSRulesEngineRule 物件，並示範如何查看子欄位。</span><span class="sxs-lookup"><span data-stu-id="b1a63-111">Create new PSRulesEngineRule object and demonstrate how to see the subfields.</span></span>

### <span data-ttu-id="b1a63-112">範例2</span><span class="sxs-lookup"><span data-stu-id="b1a63-112">Example 2</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority -1
New-AzFrontDoorRulesEngineRuleObject : Cannot validate argument on parameter 'Priority'. The -1 argument is less than the minimum allowed range of 0. Supply an argument that is greater than or equal to 0 and then try the command again.
At line:1 char:81
+ ... ule1 = New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority -1
+                                                                        ~~
+ CategoryInfo          : InvalidData: (:) [New-AzFrontDoorRulesEngineRuleObject], ParameterBindingValidationException
+ FullyQualifiedErrorId : ParameterArgumentValidationError,Microsoft.Azure.Commands.FrontDoor.Cmdlets.NewFrontDoorRulesEngineRuleObject
```

<span data-ttu-id="b1a63-113">傳遞不正確 [優先順序] 值時，預期會出現輸出。</span><span class="sxs-lookup"><span data-stu-id="b1a63-113">Expect output when passing in invalid priority value.</span></span>

## <span data-ttu-id="b1a63-114">參數</span><span class="sxs-lookup"><span data-stu-id="b1a63-114">PARAMETERS</span></span>

### <span data-ttu-id="b1a63-115">-動作</span><span class="sxs-lookup"><span data-stu-id="b1a63-115">-Action</span></span>
<span data-ttu-id="b1a63-116">在符合所有符合條件的情況下，在要求和回應上執行的動作。</span><span class="sxs-lookup"><span data-stu-id="b1a63-116">Actions to perform on the request and response if all of the match conditions are met.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineAction
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1a63-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1a63-117">-DefaultProfile</span></span>
<span data-ttu-id="b1a63-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b1a63-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1a63-119">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="b1a63-119">-MatchCondition</span></span>
<span data-ttu-id="b1a63-120">必須符合才能執行此規則之動作之符合條件的清單。</span><span class="sxs-lookup"><span data-stu-id="b1a63-120">A list of match conditions that must meet in order for the actions of this rule to run.</span></span> <span data-ttu-id="b1a63-121">沒有任何相符的條件，就表示動作將會一直執行。</span><span class="sxs-lookup"><span data-stu-id="b1a63-121">Having no match conditions means the actions will always run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchCondition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1a63-122">-MatchProcessingBehavior</span><span class="sxs-lookup"><span data-stu-id="b1a63-122">-MatchProcessingBehavior</span></span>
<span data-ttu-id="b1a63-123">如果這個規則符合規則，則規則引擎會繼續執行剩餘的規則或停止。</span><span class="sxs-lookup"><span data-stu-id="b1a63-123">If this rule is a match should the rules engine continue running the remaining rules or stop.</span></span>
<span data-ttu-id="b1a63-124">可能的值會繼續並停止。</span><span class="sxs-lookup"><span data-stu-id="b1a63-124">Possible values are Continue and Stop.</span></span>
<span data-ttu-id="b1a63-125">如果不存在，則預設為 [繼續]。</span><span class="sxs-lookup"><span data-stu-id="b1a63-125">If not present, defaults to Continue.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMatchProcessingBehavior
Parameter Sets: (All)
Aliases:
Accepted values: Continue, Stop

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1a63-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="b1a63-126">-Name</span></span>
<span data-ttu-id="b1a63-127">要參照此特定規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1a63-127">A name to refer to this specific rule.</span></span>

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

### <span data-ttu-id="b1a63-128">-優先順序</span><span class="sxs-lookup"><span data-stu-id="b1a63-128">-Priority</span></span>
<span data-ttu-id="b1a63-129">指派給這個規則的優先順序。</span><span class="sxs-lookup"><span data-stu-id="b1a63-129">A priority assigned to this rule.</span></span>
<span data-ttu-id="b1a63-130">不能是負數。</span><span class="sxs-lookup"><span data-stu-id="b1a63-130">Cannot be negative.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1a63-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1a63-131">CommonParameters</span></span>
<span data-ttu-id="b1a63-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b1a63-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1a63-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b1a63-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1a63-134">輸入</span><span class="sxs-lookup"><span data-stu-id="b1a63-134">INPUTS</span></span>

### <span data-ttu-id="b1a63-135">所有</span><span class="sxs-lookup"><span data-stu-id="b1a63-135">None</span></span>

## <span data-ttu-id="b1a63-136">輸出</span><span class="sxs-lookup"><span data-stu-id="b1a63-136">OUTPUTS</span></span>

### <span data-ttu-id="b1a63-137">PSRulesEngineRule 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="b1a63-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineRule</span></span>

## <span data-ttu-id="b1a63-138">筆記</span><span class="sxs-lookup"><span data-stu-id="b1a63-138">NOTES</span></span>

## <span data-ttu-id="b1a63-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="b1a63-139">RELATED LINKS</span></span>
