---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
ms.openlocfilehash: 4612f1ef1dac22d87b6794e35f9541a39f6312ea
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100403981"
---
# <span data-ttu-id="aa312-101">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="aa312-101">New-AzFrontDoorWafCustomRuleObject</span></span>

## <span data-ttu-id="aa312-102">簡介</span><span class="sxs-lookup"><span data-stu-id="aa312-102">SYNOPSIS</span></span>
<span data-ttu-id="aa312-103">建立自訂規則物件以建立 WAF 規則</span><span class="sxs-lookup"><span data-stu-id="aa312-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="aa312-104">語法</span><span class="sxs-lookup"><span data-stu-id="aa312-104">SYNTAX</span></span>

```
New-AzFrontDoorWafCustomRuleObject -Name <String> -RuleType <String> -MatchCondition <PSMatchCondition[]>
 -Action <String> -Priority <Int32> [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>]
 [-EnabledState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa312-105">描述</span><span class="sxs-lookup"><span data-stu-id="aa312-105">DESCRIPTION</span></span>
<span data-ttu-id="aa312-106">建立自訂規則物件以建立 WAF 策略</span><span class="sxs-lookup"><span data-stu-id="aa312-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="aa312-107">例子</span><span class="sxs-lookup"><span data-stu-id="aa312-107">EXAMPLES</span></span>

### <span data-ttu-id="aa312-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="aa312-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="aa312-109">建立 CustomRule 物件</span><span class="sxs-lookup"><span data-stu-id="aa312-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="aa312-110">參數</span><span class="sxs-lookup"><span data-stu-id="aa312-110">PARAMETERS</span></span>

### <span data-ttu-id="aa312-111">-動作</span><span class="sxs-lookup"><span data-stu-id="aa312-111">-Action</span></span>
<span data-ttu-id="aa312-112">動作類型。</span><span class="sxs-lookup"><span data-stu-id="aa312-112">Type of Actions.</span></span>
<span data-ttu-id="aa312-113">可能的值包括：'Allow'，'Block'， 'Log'</span><span class="sxs-lookup"><span data-stu-id="aa312-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

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

### <span data-ttu-id="aa312-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa312-114">-DefaultProfile</span></span>
<span data-ttu-id="aa312-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="aa312-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa312-116">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="aa312-116">-EnabledState</span></span>
<span data-ttu-id="aa312-117">啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="aa312-117">Enabled State.</span></span> <span data-ttu-id="aa312-118">可能的值包括：「已啟用」、」已停用」。</span><span class="sxs-lookup"><span data-stu-id="aa312-118">Possible values include: 'Enabled', 'Disabled'.</span></span>

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

### <span data-ttu-id="aa312-119">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="aa312-119">-MatchCondition</span></span>
<span data-ttu-id="aa312-120">符合條件的清單。</span><span class="sxs-lookup"><span data-stu-id="aa312-120">List of match conditions.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa312-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="aa312-121">-Name</span></span>
<span data-ttu-id="aa312-122">規則名稱</span><span class="sxs-lookup"><span data-stu-id="aa312-122">Name of the rule</span></span>

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

### <span data-ttu-id="aa312-123">-優先順序</span><span class="sxs-lookup"><span data-stu-id="aa312-123">-Priority</span></span>
<span data-ttu-id="aa312-124">說明規則的優先順序。</span><span class="sxs-lookup"><span data-stu-id="aa312-124">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="aa312-125">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="aa312-125">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="aa312-126">費率限制持續時間。</span><span class="sxs-lookup"><span data-stu-id="aa312-126">Rate limit duration.</span></span> <span data-ttu-id="aa312-127">預設 - 1 分鐘</span><span class="sxs-lookup"><span data-stu-id="aa312-127">Default - 1 minute</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa312-128">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="aa312-128">-RateLimitThreshold</span></span>
<span data-ttu-id="aa312-129">費率限制閥值</span><span class="sxs-lookup"><span data-stu-id="aa312-129">Rate limit threshold</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa312-130">-RuleType</span><span class="sxs-lookup"><span data-stu-id="aa312-130">-RuleType</span></span>
<span data-ttu-id="aa312-131">規則類型。</span><span class="sxs-lookup"><span data-stu-id="aa312-131">Type of the rule.</span></span>
<span data-ttu-id="aa312-132">可能的值包括：'MatchRule'， 'RateLimitRule'</span><span class="sxs-lookup"><span data-stu-id="aa312-132">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="aa312-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa312-133">CommonParameters</span></span>
<span data-ttu-id="aa312-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="aa312-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa312-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aa312-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa312-136">輸入</span><span class="sxs-lookup"><span data-stu-id="aa312-136">INPUTS</span></span>

### <span data-ttu-id="aa312-137">沒有</span><span class="sxs-lookup"><span data-stu-id="aa312-137">None</span></span>

## <span data-ttu-id="aa312-138">輸出</span><span class="sxs-lookup"><span data-stu-id="aa312-138">OUTPUTS</span></span>

### <span data-ttu-id="aa312-139">Microsoft.Azure.Commands.FrontDoor.models.PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="aa312-139">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="aa312-140">筆記</span><span class="sxs-lookup"><span data-stu-id="aa312-140">NOTES</span></span>

## <span data-ttu-id="aa312-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="aa312-141">RELATED LINKS</span></span>

<span data-ttu-id="aa312-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="aa312-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span></span>
