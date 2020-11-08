---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleexclusionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
ms.openlocfilehash: 1f59a7366106c59f6dc5e5af3a32368594a00537
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138850"
---
# <span data-ttu-id="a7b60-101">New-AzFrontDoorWafManagedRuleExclusionObject</span><span class="sxs-lookup"><span data-stu-id="a7b60-101">New-AzFrontDoorWafManagedRuleExclusionObject</span></span>

## <span data-ttu-id="a7b60-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a7b60-102">SYNOPSIS</span></span>
<span data-ttu-id="a7b60-103">針對 WAF 受管理的規則集、群組或規則，建立受管理規則的排除物件。</span><span class="sxs-lookup"><span data-stu-id="a7b60-103">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="a7b60-104">句法</span><span class="sxs-lookup"><span data-stu-id="a7b60-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleExclusionObject -Variable <String> -Operator <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7b60-105">說明</span><span class="sxs-lookup"><span data-stu-id="a7b60-105">DESCRIPTION</span></span>
<span data-ttu-id="a7b60-106">針對 WAF 受管理的規則集、群組或規則，建立受管理規則的排除物件。</span><span class="sxs-lookup"><span data-stu-id="a7b60-106">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="a7b60-107">示例</span><span class="sxs-lookup"><span data-stu-id="a7b60-107">EXAMPLES</span></span>

### <span data-ttu-id="a7b60-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a7b60-108">Example 1</span></span>
```powershell
PS C:> New-AzFrontDoorWafManagedRuleExclusionObject -Variable QueryStringArgNames -Operator Equals -Selector "ParameterName"

MatchVariable       SelectorMatchOperator Selector
-------------       --------------------- --------
QueryStringArgNames Equals                ParameterName
```

## <span data-ttu-id="a7b60-109">參數</span><span class="sxs-lookup"><span data-stu-id="a7b60-109">PARAMETERS</span></span>

### <span data-ttu-id="a7b60-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7b60-110">-DefaultProfile</span></span>
<span data-ttu-id="a7b60-111">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a7b60-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7b60-112">-運算子</span><span class="sxs-lookup"><span data-stu-id="a7b60-112">-Operator</span></span>
<span data-ttu-id="a7b60-113">要在與選取器相符時使用的運算子，EqualsAny 表示指定類型的所有相符變數都沒有選取器 () </span><span class="sxs-lookup"><span data-stu-id="a7b60-113">Operator to use when matching the selector, EqualsAny means no selector (all match variables of the specified type)</span></span>

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

### <span data-ttu-id="a7b60-114">-選取器</span><span class="sxs-lookup"><span data-stu-id="a7b60-114">-Selector</span></span>
<span data-ttu-id="a7b60-115">如果沒有 EqualsAny 運算子，則使用運算子時要搭配的選取模式 () </span><span class="sxs-lookup"><span data-stu-id="a7b60-115">Selector pattern to match using the operator (if the operator is not EqualsAny)</span></span>

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

### <span data-ttu-id="a7b60-116">變數</span><span class="sxs-lookup"><span data-stu-id="a7b60-116">-Variable</span></span>
<span data-ttu-id="a7b60-117">[相符] 變數。</span><span class="sxs-lookup"><span data-stu-id="a7b60-117">Match variable.</span></span> <span data-ttu-id="a7b60-118">可能的值為 RequestHeaderNames、RequestCookieNames、QueryStringArgNames、RequestBodyPostArgNames。</span><span class="sxs-lookup"><span data-stu-id="a7b60-118">Possible values are RequestHeaderNames, RequestCookieNames, QueryStringArgNames, RequestBodyPostArgNames.</span></span>
<span data-ttu-id="a7b60-119">例如，QueryStringArgNames 是一種排除與選取器搭配指定運算子的取得參數。</span><span class="sxs-lookup"><span data-stu-id="a7b60-119">For example, QueryStringArgNames is an exclusion of GET parameters matching the selector with the given operator.</span></span>

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

### <span data-ttu-id="a7b60-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7b60-120">CommonParameters</span></span>
<span data-ttu-id="a7b60-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a7b60-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7b60-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a7b60-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7b60-123">輸入</span><span class="sxs-lookup"><span data-stu-id="a7b60-123">INPUTS</span></span>

### <span data-ttu-id="a7b60-124">所有</span><span class="sxs-lookup"><span data-stu-id="a7b60-124">None</span></span>

## <span data-ttu-id="a7b60-125">輸出</span><span class="sxs-lookup"><span data-stu-id="a7b60-125">OUTPUTS</span></span>

### <span data-ttu-id="a7b60-126">PSManagedRuleExclusion 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="a7b60-126">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion</span></span>

## <span data-ttu-id="a7b60-127">筆記</span><span class="sxs-lookup"><span data-stu-id="a7b60-127">NOTES</span></span>

## <span data-ttu-id="a7b60-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="a7b60-128">RELATED LINKS</span></span>

<span data-ttu-id="a7b60-129">[新-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
[新-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md) 
[新-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="a7b60-129">[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>