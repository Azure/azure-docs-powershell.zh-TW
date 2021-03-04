---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorrulesengineruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineRuleObject.md
ms.openlocfilehash: 7bef36412f8b1b5977e94b32d0645ccdaa8d0324
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906657"
---
# <span data-ttu-id="e7cb9-101">New-AzFrontDoorRulesEngineRuleObject</span><span class="sxs-lookup"><span data-stu-id="e7cb9-101">New-AzFrontDoorRulesEngineRuleObject</span></span>

## <span data-ttu-id="e7cb9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e7cb9-102">SYNOPSIS</span></span>
<span data-ttu-id="e7cb9-103">建立 PSRulesEngineRule 物件以建立規則引擎。</span><span class="sxs-lookup"><span data-stu-id="e7cb9-103">Create a PSRulesEngineRule object for Rules Engine creation.</span></span>

## <span data-ttu-id="e7cb9-104">語法</span><span class="sxs-lookup"><span data-stu-id="e7cb9-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngineRuleObject -Name <String> -Priority <Int32> -Action <PSRulesEngineAction>
 [-MatchProcessingBehavior <PSMatchProcessingBehavior>] [-MatchCondition <PSRulesEngineMatchCondition[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7cb9-105">描述</span><span class="sxs-lookup"><span data-stu-id="e7cb9-105">DESCRIPTION</span></span>
<span data-ttu-id="e7cb9-106">建立 PSRulesEngineRule 物件以建立規則引擎。</span><span class="sxs-lookup"><span data-stu-id="e7cb9-106">Create a PSRulesEngineRule object for Rules Engine creation.</span></span>

<span data-ttu-id="e7cb9-107">使用 Cmdlet "New-AzFrontDoorRulesEngineActionObject" 建立 PSRulesEngineAction 物件，以進入 "-Action" 參數。</span><span class="sxs-lookup"><span data-stu-id="e7cb9-107">Use cmdlet "New-AzFrontDoorRulesEngineActionObject" to create PSRulesEngineAction object to pass into the "-Action" parameter.</span></span>
<span data-ttu-id="e7cb9-108">使用 Cmdlet "New-AzFrontDoorRulesEngineMatchConditionObject" 來建立 PSRulesEngineMatchCondition 物件，以進入 "-MatchCondition" 參數。</span><span class="sxs-lookup"><span data-stu-id="e7cb9-108">Use cmdlet "New-AzFrontDoorRulesEngineMatchConditionObject" to create PSRulesEngineMatchCondition object to pass into the "-MatchCondition" parameter.</span></span>

## <span data-ttu-id="e7cb9-109">例子</span><span class="sxs-lookup"><span data-stu-id="e7cb9-109">EXAMPLES</span></span>

### <span data-ttu-id="e7cb9-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="e7cb9-110">Example 1</span></span>
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

<span data-ttu-id="e7cb9-111">建立新的 PSRulesEngineRule 物件，並示範如何查看子欄位。</span><span class="sxs-lookup"><span data-stu-id="e7cb9-111">Create new PSRulesEngineRule object and demonstrate how to see the subfields.</span></span>

### <span data-ttu-id="e7cb9-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="e7cb9-112">Example 2</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority -1
New-AzFrontDoorRulesEngineRuleObject : Cannot validate argument on parameter 'Priority'. The -1 argument is less than the minimum allowed range of 0. Supply an argument that is greater than or equal to 0 and then try the command again.
At line:1 char:81
+ ... ule1 = New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority -1
+                                                                        ~~
+ CategoryInfo          : InvalidData: (:) [New-AzFrontDoorRulesEngineRuleObject], ParameterBindingValidationException
+ FullyQualifiedErrorId : ParameterArgumentValidationError,Microsoft.Azure.Commands.FrontDoor.Cmdlets.NewFrontDoorRulesEngineRuleObject
```

<span data-ttu-id="e7cb9-113">傳遞不正確優先順序值時，預期輸出。</span><span class="sxs-lookup"><span data-stu-id="e7cb9-113">Expect output when passing in invalid priority value.</span></span>

## <span data-ttu-id="e7cb9-114">參數</span><span class="sxs-lookup"><span data-stu-id="e7cb9-114">PARAMETERS</span></span>

### <span data-ttu-id="e7cb9-115">-動作</span><span class="sxs-lookup"><span data-stu-id="e7cb9-115">-Action</span></span>
<span data-ttu-id="e7cb9-116">如果符合所有符合的條件，針對要求和回應執行的動作。</span><span class="sxs-lookup"><span data-stu-id="e7cb9-116">Actions to perform on the request and response if all of the match conditions are met.</span></span>

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

### <span data-ttu-id="e7cb9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7cb9-117">-DefaultProfile</span></span>
<span data-ttu-id="e7cb9-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e7cb9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7cb9-119">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="e7cb9-119">-MatchCondition</span></span>
<span data-ttu-id="e7cb9-120">必須符合的相符條件清單，才能執行此規則的動作。</span><span class="sxs-lookup"><span data-stu-id="e7cb9-120">A list of match conditions that must meet in order for the actions of this rule to run.</span></span> <span data-ttu-id="e7cb9-121">沒有符合條件表示動作一定會執行。</span><span class="sxs-lookup"><span data-stu-id="e7cb9-121">Having no match conditions means the actions will always run.</span></span>

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

### <span data-ttu-id="e7cb9-122">-MatchProcessingBehavior</span><span class="sxs-lookup"><span data-stu-id="e7cb9-122">-MatchProcessingBehavior</span></span>
<span data-ttu-id="e7cb9-123">如果此規則符合規則，則規則引擎會繼續執行其餘的規則或停止。</span><span class="sxs-lookup"><span data-stu-id="e7cb9-123">If this rule is a match should the rules engine continue running the remaining rules or stop.</span></span>
<span data-ttu-id="e7cb9-124">可能的值為繼續和停止。</span><span class="sxs-lookup"><span data-stu-id="e7cb9-124">Possible values are Continue and Stop.</span></span>
<span data-ttu-id="e7cb9-125">如果沒有，預設為繼續。</span><span class="sxs-lookup"><span data-stu-id="e7cb9-125">If not present, defaults to Continue.</span></span>

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

### <span data-ttu-id="e7cb9-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="e7cb9-126">-Name</span></span>
<span data-ttu-id="e7cb9-127">這是要參照此特定規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7cb9-127">A name to refer to this specific rule.</span></span>

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

### <span data-ttu-id="e7cb9-128">-優先順序</span><span class="sxs-lookup"><span data-stu-id="e7cb9-128">-Priority</span></span>
<span data-ttu-id="e7cb9-129">指派給此規則的優先順序。</span><span class="sxs-lookup"><span data-stu-id="e7cb9-129">A priority assigned to this rule.</span></span>
<span data-ttu-id="e7cb9-130">不能是負數。</span><span class="sxs-lookup"><span data-stu-id="e7cb9-130">Cannot be negative.</span></span>

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

### <span data-ttu-id="e7cb9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7cb9-131">CommonParameters</span></span>
<span data-ttu-id="e7cb9-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e7cb9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7cb9-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7cb9-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7cb9-134">輸入</span><span class="sxs-lookup"><span data-stu-id="e7cb9-134">INPUTS</span></span>

### <span data-ttu-id="e7cb9-135">沒有</span><span class="sxs-lookup"><span data-stu-id="e7cb9-135">None</span></span>

## <span data-ttu-id="e7cb9-136">輸出</span><span class="sxs-lookup"><span data-stu-id="e7cb9-136">OUTPUTS</span></span>

### <span data-ttu-id="e7cb9-137">Microsoft.Azure.Commands.FrontDoor.models.PSRulesEngineRule</span><span class="sxs-lookup"><span data-stu-id="e7cb9-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineRule</span></span>

## <span data-ttu-id="e7cb9-138">筆記</span><span class="sxs-lookup"><span data-stu-id="e7cb9-138">NOTES</span></span>

## <span data-ttu-id="e7cb9-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="e7cb9-139">RELATED LINKS</span></span>
