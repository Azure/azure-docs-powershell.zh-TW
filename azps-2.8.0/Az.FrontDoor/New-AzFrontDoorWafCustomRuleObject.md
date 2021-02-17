---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
ms.openlocfilehash: c59e0f90ae8b6d7839c7bb845b56e31a42b2d033
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412787"
---
# <span data-ttu-id="e59cc-101">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="e59cc-101">New-AzFrontDoorWafCustomRuleObject</span></span>

## <span data-ttu-id="e59cc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e59cc-102">SYNOPSIS</span></span>
<span data-ttu-id="e59cc-103">建立自訂規則物件以建立 WAF 策略</span><span class="sxs-lookup"><span data-stu-id="e59cc-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="e59cc-104">語法</span><span class="sxs-lookup"><span data-stu-id="e59cc-104">SYNTAX</span></span>

```
New-AzFrontDoorWafCustomRuleObject -Name <String> -RuleType <String> -MatchCondition <PSMatchCondition[]>
 -Action <String> -Priority <Int32> [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e59cc-105">描述</span><span class="sxs-lookup"><span data-stu-id="e59cc-105">DESCRIPTION</span></span>
<span data-ttu-id="e59cc-106">建立自訂規則物件以建立 WAF 規則</span><span class="sxs-lookup"><span data-stu-id="e59cc-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="e59cc-107">例子</span><span class="sxs-lookup"><span data-stu-id="e59cc-107">EXAMPLES</span></span>

### <span data-ttu-id="e59cc-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="e59cc-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="e59cc-109">建立 CustomRule 物件</span><span class="sxs-lookup"><span data-stu-id="e59cc-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="e59cc-110">參數</span><span class="sxs-lookup"><span data-stu-id="e59cc-110">PARAMETERS</span></span>

### <span data-ttu-id="e59cc-111">-動作</span><span class="sxs-lookup"><span data-stu-id="e59cc-111">-Action</span></span>
<span data-ttu-id="e59cc-112">動作類型。</span><span class="sxs-lookup"><span data-stu-id="e59cc-112">Type of Actions.</span></span>
<span data-ttu-id="e59cc-113">可能的值包括：'Allow'，'Block'， 'Log'</span><span class="sxs-lookup"><span data-stu-id="e59cc-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

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

### <span data-ttu-id="e59cc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e59cc-114">-DefaultProfile</span></span>
<span data-ttu-id="e59cc-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e59cc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e59cc-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="e59cc-116">-MatchCondition</span></span>
<span data-ttu-id="e59cc-117">符合條件的清單。</span><span class="sxs-lookup"><span data-stu-id="e59cc-117">List of match conditions.</span></span>

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

### <span data-ttu-id="e59cc-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="e59cc-118">-Name</span></span>
<span data-ttu-id="e59cc-119">規則名稱</span><span class="sxs-lookup"><span data-stu-id="e59cc-119">Name of the rule</span></span>

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

### <span data-ttu-id="e59cc-120">-優先順序</span><span class="sxs-lookup"><span data-stu-id="e59cc-120">-Priority</span></span>
<span data-ttu-id="e59cc-121">說明規則的優先順序。</span><span class="sxs-lookup"><span data-stu-id="e59cc-121">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="e59cc-122">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="e59cc-122">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="e59cc-123">費率限制持續時間。</span><span class="sxs-lookup"><span data-stu-id="e59cc-123">Rate limit duration.</span></span> <span data-ttu-id="e59cc-124">預設 - 1 分鐘</span><span class="sxs-lookup"><span data-stu-id="e59cc-124">Default - 1 minute</span></span>

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

### <span data-ttu-id="e59cc-125">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="e59cc-125">-RateLimitThreshold</span></span>
<span data-ttu-id="e59cc-126">費率限制閥值</span><span class="sxs-lookup"><span data-stu-id="e59cc-126">Rate limit threshold</span></span>

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

### <span data-ttu-id="e59cc-127">-RuleType</span><span class="sxs-lookup"><span data-stu-id="e59cc-127">-RuleType</span></span>
<span data-ttu-id="e59cc-128">規則類型。</span><span class="sxs-lookup"><span data-stu-id="e59cc-128">Type of the rule.</span></span>
<span data-ttu-id="e59cc-129">可能的值包括：'MatchRule'， 'RateLimitRule'</span><span class="sxs-lookup"><span data-stu-id="e59cc-129">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="e59cc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e59cc-130">CommonParameters</span></span>
<span data-ttu-id="e59cc-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e59cc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e59cc-132">詳細資訊[請參閱about_CommonParameters。](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e59cc-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e59cc-133">輸入</span><span class="sxs-lookup"><span data-stu-id="e59cc-133">INPUTS</span></span>

### <span data-ttu-id="e59cc-134">沒有</span><span class="sxs-lookup"><span data-stu-id="e59cc-134">None</span></span>

## <span data-ttu-id="e59cc-135">輸出</span><span class="sxs-lookup"><span data-stu-id="e59cc-135">OUTPUTS</span></span>

### <span data-ttu-id="e59cc-136">Microsoft.Azure.Commands.FrontDoor.models.PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="e59cc-136">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="e59cc-137">筆記</span><span class="sxs-lookup"><span data-stu-id="e59cc-137">NOTES</span></span>

## <span data-ttu-id="e59cc-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="e59cc-138">RELATED LINKS</span></span>

<span data-ttu-id="e59cc-139">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="e59cc-139">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span></span>
