---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
ms.openlocfilehash: 6c40a54dd230bc4c7e45f97b4fa6f969940e1673
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612358"
---
# <span data-ttu-id="c9b5f-101">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="c9b5f-101">New-AzFrontDoorWafCustomRuleObject</span></span>

## <span data-ttu-id="c9b5f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c9b5f-102">SYNOPSIS</span></span>
<span data-ttu-id="c9b5f-103">建立 WAF 原則建立的 CustomRule 物件</span><span class="sxs-lookup"><span data-stu-id="c9b5f-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="c9b5f-104">句法</span><span class="sxs-lookup"><span data-stu-id="c9b5f-104">SYNTAX</span></span>

```
New-AzFrontDoorWafCustomRuleObject -Name <String> -RuleType <String> -MatchCondition <PSMatchCondition[]>
 -Action <String> -Priority <Int32> [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9b5f-105">說明</span><span class="sxs-lookup"><span data-stu-id="c9b5f-105">DESCRIPTION</span></span>
<span data-ttu-id="c9b5f-106">建立 WAF 原則建立的 CustomRule 物件</span><span class="sxs-lookup"><span data-stu-id="c9b5f-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="c9b5f-107">示例</span><span class="sxs-lookup"><span data-stu-id="c9b5f-107">EXAMPLES</span></span>

### <span data-ttu-id="c9b5f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="c9b5f-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="c9b5f-109">建立 CustomRule 物件</span><span class="sxs-lookup"><span data-stu-id="c9b5f-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="c9b5f-110">參數</span><span class="sxs-lookup"><span data-stu-id="c9b5f-110">PARAMETERS</span></span>

### <span data-ttu-id="c9b5f-111">-動作</span><span class="sxs-lookup"><span data-stu-id="c9b5f-111">-Action</span></span>
<span data-ttu-id="c9b5f-112">動作類型。</span><span class="sxs-lookup"><span data-stu-id="c9b5f-112">Type of Actions.</span></span>
<span data-ttu-id="c9b5f-113">可能的值包括： "Allow"，"Block"，"Log"</span><span class="sxs-lookup"><span data-stu-id="c9b5f-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

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

### <span data-ttu-id="c9b5f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9b5f-114">-DefaultProfile</span></span>
<span data-ttu-id="c9b5f-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c9b5f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9b5f-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="c9b5f-116">-MatchCondition</span></span>
<span data-ttu-id="c9b5f-117">符合條件的清單。</span><span class="sxs-lookup"><span data-stu-id="c9b5f-117">List of match conditions.</span></span>

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

### <span data-ttu-id="c9b5f-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="c9b5f-118">-Name</span></span>
<span data-ttu-id="c9b5f-119">規則名稱</span><span class="sxs-lookup"><span data-stu-id="c9b5f-119">Name of the rule</span></span>

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

### <span data-ttu-id="c9b5f-120">-優先順序</span><span class="sxs-lookup"><span data-stu-id="c9b5f-120">-Priority</span></span>
<span data-ttu-id="c9b5f-121">描述規則的優先順序。</span><span class="sxs-lookup"><span data-stu-id="c9b5f-121">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="c9b5f-122">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="c9b5f-122">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="c9b5f-123">Rate 限制持續時間。</span><span class="sxs-lookup"><span data-stu-id="c9b5f-123">Rate limit duration.</span></span> <span data-ttu-id="c9b5f-124">預設值-1 分鐘</span><span class="sxs-lookup"><span data-stu-id="c9b5f-124">Default - 1 minute</span></span>

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

### <span data-ttu-id="c9b5f-125">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="c9b5f-125">-RateLimitThreshold</span></span>
<span data-ttu-id="c9b5f-126">Rate 限制閾值</span><span class="sxs-lookup"><span data-stu-id="c9b5f-126">Rate limit threshold</span></span>

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

### <span data-ttu-id="c9b5f-127">-RuleType</span><span class="sxs-lookup"><span data-stu-id="c9b5f-127">-RuleType</span></span>
<span data-ttu-id="c9b5f-128">規則的類型。</span><span class="sxs-lookup"><span data-stu-id="c9b5f-128">Type of the rule.</span></span>
<span data-ttu-id="c9b5f-129">可能的值包括： "MatchRule"、"RateLimitRule"</span><span class="sxs-lookup"><span data-stu-id="c9b5f-129">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="c9b5f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9b5f-130">CommonParameters</span></span>
<span data-ttu-id="c9b5f-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c9b5f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9b5f-132">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c9b5f-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9b5f-133">輸入</span><span class="sxs-lookup"><span data-stu-id="c9b5f-133">INPUTS</span></span>

### <span data-ttu-id="c9b5f-134">所有</span><span class="sxs-lookup"><span data-stu-id="c9b5f-134">None</span></span>

## <span data-ttu-id="c9b5f-135">輸出</span><span class="sxs-lookup"><span data-stu-id="c9b5f-135">OUTPUTS</span></span>

### <span data-ttu-id="c9b5f-136">PSCustomRule 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="c9b5f-136">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="c9b5f-137">筆記</span><span class="sxs-lookup"><span data-stu-id="c9b5f-137">NOTES</span></span>

## <span data-ttu-id="c9b5f-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="c9b5f-138">RELATED LINKS</span></span>

<span data-ttu-id="c9b5f-139">[新-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
[Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="c9b5f-139">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md)</span></span>
