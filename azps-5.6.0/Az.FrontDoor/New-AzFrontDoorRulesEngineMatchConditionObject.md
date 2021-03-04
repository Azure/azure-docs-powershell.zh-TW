---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorrulesenginematchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineMatchConditionObject.md
ms.openlocfilehash: 4f35b20b7c17a0cd809cb5964fbecfa429b581bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906661"
---
# <span data-ttu-id="1f558-101">New-AzFrontDoorRulesEngineMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="1f558-101">New-AzFrontDoorRulesEngineMatchConditionObject</span></span>

## <span data-ttu-id="1f558-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1f558-102">SYNOPSIS</span></span>
<span data-ttu-id="1f558-103">建立 PSRulesEngineMatchCondition 物件以建立規則引擎規則。</span><span class="sxs-lookup"><span data-stu-id="1f558-103">Create a PSRulesEngineMatchCondition object for creating a rules engine rule.</span></span>

## <span data-ttu-id="1f558-104">語法</span><span class="sxs-lookup"><span data-stu-id="1f558-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngineMatchConditionObject -MatchVariable <PSRulesEngineMatchVariable>
 -MatchValue <String[]> [-Selector <String>] [-Operator <PSRulesEngineOperator>] [-NegateCondition <Boolean>]
 [-Transform <PSTransform[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f558-105">描述</span><span class="sxs-lookup"><span data-stu-id="1f558-105">DESCRIPTION</span></span>
<span data-ttu-id="1f558-106">建立 PSRulesEngineMatchCondition 物件以建立規則引擎規則。</span><span class="sxs-lookup"><span data-stu-id="1f558-106">Create a PSRulesEngineMatchCondition object for creating a rules engine rule.</span></span>

## <span data-ttu-id="1f558-107">例子</span><span class="sxs-lookup"><span data-stu-id="1f558-107">EXAMPLES</span></span>

### <span data-ttu-id="1f558-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="1f558-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineMatchConditionObject -MatchVariable RequestHeader -Operator Equal -MatchValue allowoverride -Transform "LowerCase", "UpperCase"-Selector Rules-Engine-Route-Forward -NegateCondition $false

RulesEngineMatchVariable : RequestHeader
RulesEngineMatchValue    : {allowoverride}
Selector                 : Rules-Engine-Route-Forward
RulesEngineOperator      : Equal
NegateCondition          : False
Transform                : {Lowercase, Uppercase}
```

<span data-ttu-id="1f558-109">改善新的 PSRulesEngineMatchCondition 物件。</span><span class="sxs-lookup"><span data-stu-id="1f558-109">Greate a new PSRulesEngineMatchCondition object.</span></span>

## <span data-ttu-id="1f558-110">參數</span><span class="sxs-lookup"><span data-stu-id="1f558-110">PARAMETERS</span></span>

### <span data-ttu-id="1f558-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f558-111">-DefaultProfile</span></span>
<span data-ttu-id="1f558-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1f558-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f558-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="1f558-113">-MatchValue</span></span>
<span data-ttu-id="1f558-114">比對要比對的值。</span><span class="sxs-lookup"><span data-stu-id="1f558-114">Match values to match against.</span></span>
<span data-ttu-id="1f558-115">運算子會以 OR 語義來適用于這裡的每個值。</span><span class="sxs-lookup"><span data-stu-id="1f558-115">The operator will apply to each value in here with OR semantics.</span></span>
<span data-ttu-id="1f558-116">如果其中任何一個符合變數與給定運算子，則此比對條件會視為相符。</span><span class="sxs-lookup"><span data-stu-id="1f558-116">If any of them match the variable with the given operator this match condition is considered a match.</span></span>

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

### <span data-ttu-id="1f558-117">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="1f558-117">-MatchVariable</span></span>
<span data-ttu-id="1f558-118">Match Variable。</span><span class="sxs-lookup"><span data-stu-id="1f558-118">Match Variable.</span></span>
<span data-ttu-id="1f558-119">可能的值為 IsMobile、RemoteAddr、RequestMethod、QueryString、PostArg、RequestUri、RequestPath、RequestFileName、RequestfilenameExtension、RequestHeader、RequestBody、RequestS方程式</span><span class="sxs-lookup"><span data-stu-id="1f558-119">Possible values are IsMobile, RemoteAddr, RequestMethod, QueryString, PostArg, RequestUri, RequestPath, RequestFileName, RequestfilenameExtension, RequestHeader, RequestBody, RequestScheme</span></span>

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

### <span data-ttu-id="1f558-120">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="1f558-120">-NegateCondition</span></span>
<span data-ttu-id="1f558-121">說明這是否為否定條件</span><span class="sxs-lookup"><span data-stu-id="1f558-121">Describes if this is negate condition or not</span></span>

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

### <span data-ttu-id="1f558-122">-運算子</span><span class="sxs-lookup"><span data-stu-id="1f558-122">-Operator</span></span>
<span data-ttu-id="1f558-123">描述要適用于比對條件的運算子。</span><span class="sxs-lookup"><span data-stu-id="1f558-123">Describes operator to apply to the match condition.</span></span>
<span data-ttu-id="1f558-124">可能的值為 Any、IPMatch、GeoMatch、Equal、Contains、LessQual、GreaterQualEqual、LessQualOrEqual、GreaterQualOrEqual、BeginsWith、EndsWith。</span><span class="sxs-lookup"><span data-stu-id="1f558-124">Possible values are Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith.</span></span>

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

### <span data-ttu-id="1f558-125">-選取器</span><span class="sxs-lookup"><span data-stu-id="1f558-125">-Selector</span></span>
<span data-ttu-id="1f558-126">RequestHeader 或 RequestBody 中要相符的選取器名稱</span><span class="sxs-lookup"><span data-stu-id="1f558-126">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="1f558-127">-轉換</span><span class="sxs-lookup"><span data-stu-id="1f558-127">-Transform</span></span>
<span data-ttu-id="1f558-128">在比對之前套用哪些轉換的清單。</span><span class="sxs-lookup"><span data-stu-id="1f558-128">List of what transforms are applied before matching.</span></span> <span data-ttu-id="1f558-129">可能的個別轉換值為小寫、大寫、修剪、UrlDecode、UrlEncode、RemoveNulls。</span><span class="sxs-lookup"><span data-stu-id="1f558-129">Possible individual transform values are Lowercase, Uppercase, Trim, UrlDecode, UrlEncode, RemoveNulls.</span></span>

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

### <span data-ttu-id="1f558-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f558-130">CommonParameters</span></span>
<span data-ttu-id="1f558-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1f558-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f558-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1f558-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f558-133">輸入</span><span class="sxs-lookup"><span data-stu-id="1f558-133">INPUTS</span></span>

### <span data-ttu-id="1f558-134">沒有</span><span class="sxs-lookup"><span data-stu-id="1f558-134">None</span></span>

## <span data-ttu-id="1f558-135">輸出</span><span class="sxs-lookup"><span data-stu-id="1f558-135">OUTPUTS</span></span>

### <span data-ttu-id="1f558-136">Microsoft.Azure.Commands.FrontDoor.models.PSRulesEngineMatchCondition</span><span class="sxs-lookup"><span data-stu-id="1f558-136">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchCondition</span></span>

## <span data-ttu-id="1f558-137">筆記</span><span class="sxs-lookup"><span data-stu-id="1f558-137">NOTES</span></span>

## <span data-ttu-id="1f558-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="1f558-138">RELATED LINKS</span></span>
