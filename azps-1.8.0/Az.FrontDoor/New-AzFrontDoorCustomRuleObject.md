---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorCustomRuleObject.md
ms.openlocfilehash: 19f8215f8feaa1765da871f0fa38cc0120d842ea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787822"
---
# <span data-ttu-id="4238e-101">New-AzFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="4238e-101">New-AzFrontDoorCustomRuleObject</span></span>

## <span data-ttu-id="4238e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4238e-102">SYNOPSIS</span></span>
<span data-ttu-id="4238e-103">建立 WAF 原則建立的 CustomRule 物件</span><span class="sxs-lookup"><span data-stu-id="4238e-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="4238e-104">句法</span><span class="sxs-lookup"><span data-stu-id="4238e-104">SYNTAX</span></span>

```
New-AzFrontDoorCustomRuleObject -Name <String> -RuleType <PSCustomRuleType>
 -MatchCondition <PSMatchCondition[]> -Action <PSAction> -Priority <Int32>
 [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4238e-105">說明</span><span class="sxs-lookup"><span data-stu-id="4238e-105">DESCRIPTION</span></span>
<span data-ttu-id="4238e-106">建立 WAF 原則建立的 CustomRule 物件</span><span class="sxs-lookup"><span data-stu-id="4238e-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="4238e-107">示例</span><span class="sxs-lookup"><span data-stu-id="4238e-107">EXAMPLES</span></span>

### <span data-ttu-id="4238e-108">範例1</span><span class="sxs-lookup"><span data-stu-id="4238e-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="4238e-109">建立 CustomRule 物件</span><span class="sxs-lookup"><span data-stu-id="4238e-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="4238e-110">參數</span><span class="sxs-lookup"><span data-stu-id="4238e-110">PARAMETERS</span></span>

### <span data-ttu-id="4238e-111">-動作</span><span class="sxs-lookup"><span data-stu-id="4238e-111">-Action</span></span>
<span data-ttu-id="4238e-112">動作類型。</span><span class="sxs-lookup"><span data-stu-id="4238e-112">Type of Actions.</span></span>
<span data-ttu-id="4238e-113">可能的值包括： "Allow"，"Block"，"Log"</span><span class="sxs-lookup"><span data-stu-id="4238e-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAction
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log, Redirect

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4238e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4238e-114">-DefaultProfile</span></span>
<span data-ttu-id="4238e-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4238e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4238e-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="4238e-116">-MatchCondition</span></span>
<span data-ttu-id="4238e-117">符合條件的清單。</span><span class="sxs-lookup"><span data-stu-id="4238e-117">List of match conditions.</span></span>

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

### <span data-ttu-id="4238e-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="4238e-118">-Name</span></span>
<span data-ttu-id="4238e-119">規則名稱</span><span class="sxs-lookup"><span data-stu-id="4238e-119">Name of the rule</span></span>

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

### <span data-ttu-id="4238e-120">-優先順序</span><span class="sxs-lookup"><span data-stu-id="4238e-120">-Priority</span></span>
<span data-ttu-id="4238e-121">描述規則的優先順序。</span><span class="sxs-lookup"><span data-stu-id="4238e-121">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="4238e-122">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="4238e-122">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="4238e-123">Rate 限制持續時間。</span><span class="sxs-lookup"><span data-stu-id="4238e-123">Rate limit duration.</span></span> <span data-ttu-id="4238e-124">預設值-1 分鐘</span><span class="sxs-lookup"><span data-stu-id="4238e-124">Default - 1 minute</span></span>

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

### <span data-ttu-id="4238e-125">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="4238e-125">-RateLimitThreshold</span></span>
<span data-ttu-id="4238e-126">Rate 限制 thresold</span><span class="sxs-lookup"><span data-stu-id="4238e-126">Rate limit thresold</span></span>

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

### <span data-ttu-id="4238e-127">-RuleType</span><span class="sxs-lookup"><span data-stu-id="4238e-127">-RuleType</span></span>
<span data-ttu-id="4238e-128">規則的類型。</span><span class="sxs-lookup"><span data-stu-id="4238e-128">Type of the rule.</span></span>
<span data-ttu-id="4238e-129">可能的值包括： "MatchRule"、"RateLimitRule"</span><span class="sxs-lookup"><span data-stu-id="4238e-129">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRuleType
Parameter Sets: (All)
Aliases:
Accepted values: RateLimitRule, MatchRule

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4238e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4238e-130">CommonParameters</span></span>
<span data-ttu-id="4238e-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4238e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4238e-132">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4238e-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4238e-133">輸入</span><span class="sxs-lookup"><span data-stu-id="4238e-133">INPUTS</span></span>

### <span data-ttu-id="4238e-134">所有</span><span class="sxs-lookup"><span data-stu-id="4238e-134">None</span></span>

## <span data-ttu-id="4238e-135">輸出</span><span class="sxs-lookup"><span data-stu-id="4238e-135">OUTPUTS</span></span>

### <span data-ttu-id="4238e-136">PSCustomRule 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="4238e-136">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="4238e-137">筆記</span><span class="sxs-lookup"><span data-stu-id="4238e-137">NOTES</span></span>

## <span data-ttu-id="4238e-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="4238e-138">RELATED LINKS</span></span>

<span data-ttu-id="4238e-139">[新-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
[Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="4238e-139">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md)</span></span>
