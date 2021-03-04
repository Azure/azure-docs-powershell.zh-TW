---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorwafmatchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafMatchConditionObject.md
ms.openlocfilehash: e67841073d6c7342e0bb88c52809a9c45d92f82f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906633"
---
# <span data-ttu-id="a333b-101">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="a333b-101">New-AzFrontDoorWafMatchConditionObject</span></span>

## <span data-ttu-id="a333b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a333b-102">SYNOPSIS</span></span>
<span data-ttu-id="a333b-103">建立 MatchCondition 物件以建立 WAF 策略</span><span class="sxs-lookup"><span data-stu-id="a333b-103">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="a333b-104">語法</span><span class="sxs-lookup"><span data-stu-id="a333b-104">SYNTAX</span></span>

```
New-AzFrontDoorWafMatchConditionObject -MatchVariable <String> -OperatorProperty <String>
 [-MatchValue <String[]>] [-Selector <String>] [-NegateCondition <Boolean>] [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a333b-105">描述</span><span class="sxs-lookup"><span data-stu-id="a333b-105">DESCRIPTION</span></span>
<span data-ttu-id="a333b-106">建立 MatchCondition 物件以建立 WAF 策略</span><span class="sxs-lookup"><span data-stu-id="a333b-106">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="a333b-107">例子</span><span class="sxs-lookup"><span data-stu-id="a333b-107">EXAMPLES</span></span>

### <span data-ttu-id="a333b-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="a333b-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "Windows"


MatchVariable OperatorProperty MatchValue Selector   NegateCondition Transform
------------- ---------------- ---------- --------   --------------- ---------
RequestHeader Contains         {Windows}  User-Agent           False
```

### <span data-ttu-id="a333b-109">範例 2</span><span class="sxs-lookup"><span data-stu-id="a333b-109">Example 2</span></span>
```powershell
PS C:\> New-AzFrontDoorWafMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "WINDOWS" -Transform Uppercase


MatchVariable OperatorProperty MatchValue Selector   NegateCondition Transform
------------- ---------------- ---------- --------   --------------- ---------
RequestHeader Contains         {WINDOWS}  User-Agent           False {Uppercase}
```

<span data-ttu-id="a333b-110">建立 MatchCondition 物件</span><span class="sxs-lookup"><span data-stu-id="a333b-110">Create a MatchCondition object</span></span>

## <span data-ttu-id="a333b-111">參數</span><span class="sxs-lookup"><span data-stu-id="a333b-111">PARAMETERS</span></span>

### <span data-ttu-id="a333b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a333b-112">-DefaultProfile</span></span>
<span data-ttu-id="a333b-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a333b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a333b-114">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="a333b-114">-MatchValue</span></span>
<span data-ttu-id="a333b-115">比對值。</span><span class="sxs-lookup"><span data-stu-id="a333b-115">Match value.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a333b-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="a333b-116">-MatchVariable</span></span>
<span data-ttu-id="a333b-117">Match Variable。</span><span class="sxs-lookup"><span data-stu-id="a333b-117">Match Variable.</span></span>
<span data-ttu-id="a333b-118">可能的值包括：'RemoteAddr'， 'RequestMethod'， 'QueryString'， 'PostArgs'， 'RequestUri'， 'RequestHeader'， 'RequestBody'， 'SocketAddr'</span><span class="sxs-lookup"><span data-stu-id="a333b-118">Possible values include: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestBody', 'SocketAddr'</span></span>

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

### <span data-ttu-id="a333b-119">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="a333b-119">-NegateCondition</span></span>
<span data-ttu-id="a333b-120">說明此為負條件或預設值為 False</span><span class="sxs-lookup"><span data-stu-id="a333b-120">Describes if this is negate condition or not Default value is false</span></span>

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

### <span data-ttu-id="a333b-121">-OperatorProperty</span><span class="sxs-lookup"><span data-stu-id="a333b-121">-OperatorProperty</span></span>
<span data-ttu-id="a333b-122">描述要相符的運算子。</span><span class="sxs-lookup"><span data-stu-id="a333b-122">Describes operator to be matched.</span></span>
<span data-ttu-id="a333b-123">可能的值包括：'Any'， 'IPMatch'， 'GeoMatch'， 'Equal'， 'Contains'， 'LessQual'， 'GreaterQual'， 'lessQualOrEqual'， 'Greater。OrEqual'， 'BeginsWith'， 'EndsWith'， 'RegEx'</span><span class="sxs-lookup"><span data-stu-id="a333b-123">Possible values include: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith', 'RegEx'</span></span>

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

### <span data-ttu-id="a333b-124">-選取器</span><span class="sxs-lookup"><span data-stu-id="a333b-124">-Selector</span></span>
<span data-ttu-id="a333b-125">RequestHeader 或 RequestBody 中要相符的選取器名稱</span><span class="sxs-lookup"><span data-stu-id="a333b-125">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="a333b-126">-轉換</span><span class="sxs-lookup"><span data-stu-id="a333b-126">-Transform</span></span>
<span data-ttu-id="a333b-127">要申請的轉換。</span><span class="sxs-lookup"><span data-stu-id="a333b-127">Transforms to apply.</span></span> <span data-ttu-id="a333b-128">可能的值包括：'小寫'、'大寫'、'修剪」、'UrlDecode'、'UrlEncode'、'RemoveNulls'。</span><span class="sxs-lookup"><span data-stu-id="a333b-128">Possible values include: 'Lowercase', 'Uppercase', 'Trim', 'UrlDecode', 'UrlEncode', 'RemoveNulls'.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a333b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a333b-129">CommonParameters</span></span>
<span data-ttu-id="a333b-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a333b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a333b-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a333b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a333b-132">輸入</span><span class="sxs-lookup"><span data-stu-id="a333b-132">INPUTS</span></span>

### <span data-ttu-id="a333b-133">沒有</span><span class="sxs-lookup"><span data-stu-id="a333b-133">None</span></span>

## <span data-ttu-id="a333b-134">輸出</span><span class="sxs-lookup"><span data-stu-id="a333b-134">OUTPUTS</span></span>

### <span data-ttu-id="a333b-135">Microsoft.Azure.Commands.FrontDoor.models.PSMatchCondition</span><span class="sxs-lookup"><span data-stu-id="a333b-135">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span></span>

## <span data-ttu-id="a333b-136">筆記</span><span class="sxs-lookup"><span data-stu-id="a333b-136">NOTES</span></span>

## <span data-ttu-id="a333b-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="a333b-137">RELATED LINKS</span></span>

[<span data-ttu-id="a333b-138">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="a333b-138">New-AzFrontDoorWafCustomRuleObject</span></span>](./New-AzFrontDoorWafCustomRuleObject.md)
