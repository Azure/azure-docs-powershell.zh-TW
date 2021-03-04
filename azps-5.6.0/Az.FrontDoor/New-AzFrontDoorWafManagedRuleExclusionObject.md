---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleexclusionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
ms.openlocfilehash: 4f8764a40d536897ee71e36c1be1d691040e2ab9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906645"
---
# <span data-ttu-id="00ef7-101">New-AzFrontDoorWafManagedRuleExclusionObject</span><span class="sxs-lookup"><span data-stu-id="00ef7-101">New-AzFrontDoorWafManagedRuleExclusionObject</span></span>

## <span data-ttu-id="00ef7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="00ef7-102">SYNOPSIS</span></span>
<span data-ttu-id="00ef7-103">建立 WAF 受管理規則集、群組或規則的受管理規則排除物件。</span><span class="sxs-lookup"><span data-stu-id="00ef7-103">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="00ef7-104">語法</span><span class="sxs-lookup"><span data-stu-id="00ef7-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleExclusionObject -Variable <String> -Operator <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00ef7-105">描述</span><span class="sxs-lookup"><span data-stu-id="00ef7-105">DESCRIPTION</span></span>
<span data-ttu-id="00ef7-106">建立 WAF 受管理規則集、群組或規則的受管理規則排除物件。</span><span class="sxs-lookup"><span data-stu-id="00ef7-106">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="00ef7-107">例子</span><span class="sxs-lookup"><span data-stu-id="00ef7-107">EXAMPLES</span></span>

### <span data-ttu-id="00ef7-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="00ef7-108">Example 1</span></span>
```powershell
PS C:> New-AzFrontDoorWafManagedRuleExclusionObject -Variable QueryStringArgNames -Operator Equals -Selector "ParameterName"

MatchVariable       SelectorMatchOperator Selector
-------------       --------------------- --------
QueryStringArgNames Equals                ParameterName
```

## <span data-ttu-id="00ef7-109">參數</span><span class="sxs-lookup"><span data-stu-id="00ef7-109">PARAMETERS</span></span>

### <span data-ttu-id="00ef7-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00ef7-110">-DefaultProfile</span></span>
<span data-ttu-id="00ef7-111">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="00ef7-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00ef7-112">-運算子</span><span class="sxs-lookup"><span data-stu-id="00ef7-112">-Operator</span></span>
<span data-ttu-id="00ef7-113">在比對選取器時使用的運算子，EqualsAny 表示沒有選取器 (指定類型變數的所有相符) </span><span class="sxs-lookup"><span data-stu-id="00ef7-113">Operator to use when matching the selector, EqualsAny means no selector (all match variables of the specified type)</span></span>

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

### <span data-ttu-id="00ef7-114">-選取器</span><span class="sxs-lookup"><span data-stu-id="00ef7-114">-Selector</span></span>
<span data-ttu-id="00ef7-115">如果運算子不是 EqualsAny， (選擇器模式以使用運算子) </span><span class="sxs-lookup"><span data-stu-id="00ef7-115">Selector pattern to match using the operator (if the operator is not EqualsAny)</span></span>

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

### <span data-ttu-id="00ef7-116">-Variable</span><span class="sxs-lookup"><span data-stu-id="00ef7-116">-Variable</span></span>
<span data-ttu-id="00ef7-117">比對變數。</span><span class="sxs-lookup"><span data-stu-id="00ef7-117">Match variable.</span></span> <span data-ttu-id="00ef7-118">可能的值為 RequestHeaderNames、RequestCookieNames、QueryStringArgNames、RequestBodyPostArgNames。</span><span class="sxs-lookup"><span data-stu-id="00ef7-118">Possible values are RequestHeaderNames, RequestCookieNames, QueryStringArgNames, RequestBodyPostArgNames.</span></span>
<span data-ttu-id="00ef7-119">例如，QueryStringArgNames 是符合選取器與指定運算子之 GET 參數的排除專案。</span><span class="sxs-lookup"><span data-stu-id="00ef7-119">For example, QueryStringArgNames is an exclusion of GET parameters matching the selector with the given operator.</span></span>

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

### <span data-ttu-id="00ef7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00ef7-120">CommonParameters</span></span>
<span data-ttu-id="00ef7-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="00ef7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00ef7-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="00ef7-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00ef7-123">輸入</span><span class="sxs-lookup"><span data-stu-id="00ef7-123">INPUTS</span></span>

### <span data-ttu-id="00ef7-124">沒有</span><span class="sxs-lookup"><span data-stu-id="00ef7-124">None</span></span>

## <span data-ttu-id="00ef7-125">輸出</span><span class="sxs-lookup"><span data-stu-id="00ef7-125">OUTPUTS</span></span>

### <span data-ttu-id="00ef7-126">Microsoft.Azure.Commands.FrontDoor.models.PSManagedRuleExclusion</span><span class="sxs-lookup"><span data-stu-id="00ef7-126">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion</span></span>

## <span data-ttu-id="00ef7-127">筆記</span><span class="sxs-lookup"><span data-stu-id="00ef7-127">NOTES</span></span>

## <span data-ttu-id="00ef7-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="00ef7-128">RELATED LINKS</span></span>

<span data-ttu-id="00ef7-129">[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md) 
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="00ef7-129">[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
