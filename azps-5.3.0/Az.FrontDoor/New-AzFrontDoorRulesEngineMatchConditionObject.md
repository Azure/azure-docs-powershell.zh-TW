---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesenginematchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineMatchConditionObject.md
ms.openlocfilehash: 991d3233dd484025e699bba455b7d43e86f586e7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98438408"
---
# <span data-ttu-id="fc7d2-101">New-AzFrontDoorRulesEngineMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="fc7d2-101">New-AzFrontDoorRulesEngineMatchConditionObject</span></span>

## <span data-ttu-id="fc7d2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fc7d2-102">SYNOPSIS</span></span>
<span data-ttu-id="fc7d2-103">建立建立規則引擎規則的 PSRulesEngineMatchCondition 物件。</span><span class="sxs-lookup"><span data-stu-id="fc7d2-103">Create a PSRulesEngineMatchCondition object for creating a rules engine rule.</span></span>

## <span data-ttu-id="fc7d2-104">句法</span><span class="sxs-lookup"><span data-stu-id="fc7d2-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngineMatchConditionObject -MatchVariable <PSRulesEngineMatchVariable>
 -MatchValue <String[]> [-Selector <String>] [-Operator <PSRulesEngineOperator>] [-NegateCondition <Boolean>]
 [-Transform <PSTransform[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc7d2-105">說明</span><span class="sxs-lookup"><span data-stu-id="fc7d2-105">DESCRIPTION</span></span>
<span data-ttu-id="fc7d2-106">建立建立規則引擎規則的 PSRulesEngineMatchCondition 物件。</span><span class="sxs-lookup"><span data-stu-id="fc7d2-106">Create a PSRulesEngineMatchCondition object for creating a rules engine rule.</span></span>

## <span data-ttu-id="fc7d2-107">示例</span><span class="sxs-lookup"><span data-stu-id="fc7d2-107">EXAMPLES</span></span>

### <span data-ttu-id="fc7d2-108">範例1</span><span class="sxs-lookup"><span data-stu-id="fc7d2-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineMatchConditionObject -MatchVariable RequestHeader -Operator Equal -MatchValue allowoverride -Transform "LowerCase", "UpperCase"-Selector Rules-Engine-Route-Forward -NegateCondition $false

RulesEngineMatchVariable : RequestHeader
RulesEngineMatchValue    : {allowoverride}
Selector                 : Rules-Engine-Route-Forward
RulesEngineOperator      : Equal
NegateCondition          : False
Transform                : {Lowercase, Uppercase}
```

<span data-ttu-id="fc7d2-109">Greate 新的 PSRulesEngineMatchCondition 物件。</span><span class="sxs-lookup"><span data-stu-id="fc7d2-109">Greate a new PSRulesEngineMatchCondition object.</span></span>

## <span data-ttu-id="fc7d2-110">參數</span><span class="sxs-lookup"><span data-stu-id="fc7d2-110">PARAMETERS</span></span>

### <span data-ttu-id="fc7d2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc7d2-111">-DefaultProfile</span></span>
<span data-ttu-id="fc7d2-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fc7d2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc7d2-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="fc7d2-113">-MatchValue</span></span>
<span data-ttu-id="fc7d2-114">符合的值。</span><span class="sxs-lookup"><span data-stu-id="fc7d2-114">Match values to match against.</span></span>
<span data-ttu-id="fc7d2-115">運算子會套用到這裡的每個值，或語義。</span><span class="sxs-lookup"><span data-stu-id="fc7d2-115">The operator will apply to each value in here with OR semantics.</span></span>
<span data-ttu-id="fc7d2-116">如果有任何專案與指定運算子的變數相符，此符合條件就會視為相符。</span><span class="sxs-lookup"><span data-stu-id="fc7d2-116">If any of them match the variable with the given operator this match condition is considered a match.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc7d2-117">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="fc7d2-117">-MatchVariable</span></span>
<span data-ttu-id="fc7d2-118">[相符] 變數。</span><span class="sxs-lookup"><span data-stu-id="fc7d2-118">Match Variable.</span></span>
<span data-ttu-id="fc7d2-119">可能的值為 IsMobile、RemoteAddr、RequestMethod、QueryString、PostArg、RequestUri、RequestPath、RequestFileName、RequestfilenameExtension、RequestHeader、RequestBody、RequestScheme、、、</span><span class="sxs-lookup"><span data-stu-id="fc7d2-119">Possible values are IsMobile, RemoteAddr, RequestMethod, QueryString, PostArg, RequestUri, RequestPath, RequestFileName, RequestfilenameExtension, RequestHeader, RequestBody, RequestScheme</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchVariable
Parameter Sets: (All)
Aliases:
Accepted values: IsMobile, RemoteAddr, RequestMethod, QueryString, PostArgs, RequestUri, RequestPath, RequestFilename, RequestFilenameExtension, RequestHeader, RequestBody, RequestScheme

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc7d2-120">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="fc7d2-120">-NegateCondition</span></span>
<span data-ttu-id="fc7d2-121">描述此情況是否為否定條件</span><span class="sxs-lookup"><span data-stu-id="fc7d2-121">Describes if this is negate condition or not</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc7d2-122">-運算子</span><span class="sxs-lookup"><span data-stu-id="fc7d2-122">-Operator</span></span>
<span data-ttu-id="fc7d2-123">描述要套用至 match 條件的運算子。</span><span class="sxs-lookup"><span data-stu-id="fc7d2-123">Describes operator to apply to the match condition.</span></span>
<span data-ttu-id="fc7d2-124">可能的值為 Any、IPMatch、GeoMatch、等於號、Contains、小於、GreaterThan、LessThanOrEqual、GreaterThanOrEqual、BeginsWith、EndsWith、、、。</span><span class="sxs-lookup"><span data-stu-id="fc7d2-124">Possible values are Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineOperator
Parameter Sets: (All)
Aliases:
Accepted values: Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc7d2-125">-選取器</span><span class="sxs-lookup"><span data-stu-id="fc7d2-125">-Selector</span></span>
<span data-ttu-id="fc7d2-126">要相符的 RequestHeader 或 RequestBody 中的選擇器名稱</span><span class="sxs-lookup"><span data-stu-id="fc7d2-126">Name of selector in RequestHeader or RequestBody to be matched</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc7d2-127">-轉換</span><span class="sxs-lookup"><span data-stu-id="fc7d2-127">-Transform</span></span>
<span data-ttu-id="fc7d2-128">在匹配前套用的轉換清單。</span><span class="sxs-lookup"><span data-stu-id="fc7d2-128">List of what transforms are applied before matching.</span></span> <span data-ttu-id="fc7d2-129">可能的個別轉換值為小寫、大寫、Trim、UrlDecode、UrlEncode、RemoveNulls。</span><span class="sxs-lookup"><span data-stu-id="fc7d2-129">Possible individual transform values are Lowercase, Uppercase, Trim, UrlDecode, UrlEncode, RemoveNulls.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSTransform[]
Parameter Sets: (All)
Aliases:
Accepted values: Lowercase, Uppercase, Trim, UrlDecode, UrlEncode, RemoveNulls

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc7d2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc7d2-130">CommonParameters</span></span>
<span data-ttu-id="fc7d2-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fc7d2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc7d2-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fc7d2-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc7d2-133">輸入</span><span class="sxs-lookup"><span data-stu-id="fc7d2-133">INPUTS</span></span>

### <span data-ttu-id="fc7d2-134">所有</span><span class="sxs-lookup"><span data-stu-id="fc7d2-134">None</span></span>

## <span data-ttu-id="fc7d2-135">輸出</span><span class="sxs-lookup"><span data-stu-id="fc7d2-135">OUTPUTS</span></span>

### <span data-ttu-id="fc7d2-136">PSRulesEngineMatchCondition 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="fc7d2-136">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchCondition</span></span>

## <span data-ttu-id="fc7d2-137">筆記</span><span class="sxs-lookup"><span data-stu-id="fc7d2-137">NOTES</span></span>

## <span data-ttu-id="fc7d2-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="fc7d2-138">RELATED LINKS</span></span>
