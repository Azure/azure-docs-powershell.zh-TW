---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
ms.openlocfilehash: 4612f1ef1dac22d87b6794e35f9541a39f6312ea
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138855"
---
# <span data-ttu-id="dd9fc-101">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="dd9fc-101">New-AzFrontDoorWafCustomRuleObject</span></span>

## <span data-ttu-id="dd9fc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dd9fc-102">SYNOPSIS</span></span>
<span data-ttu-id="dd9fc-103">建立 WAF 原則建立的 CustomRule 物件</span><span class="sxs-lookup"><span data-stu-id="dd9fc-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="dd9fc-104">句法</span><span class="sxs-lookup"><span data-stu-id="dd9fc-104">SYNTAX</span></span>

```
New-AzFrontDoorWafCustomRuleObject -Name <String> -RuleType <String> -MatchCondition <PSMatchCondition[]>
 -Action <String> -Priority <Int32> [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>]
 [-EnabledState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd9fc-105">說明</span><span class="sxs-lookup"><span data-stu-id="dd9fc-105">DESCRIPTION</span></span>
<span data-ttu-id="dd9fc-106">建立 WAF 原則建立的 CustomRule 物件</span><span class="sxs-lookup"><span data-stu-id="dd9fc-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="dd9fc-107">示例</span><span class="sxs-lookup"><span data-stu-id="dd9fc-107">EXAMPLES</span></span>

### <span data-ttu-id="dd9fc-108">範例1</span><span class="sxs-lookup"><span data-stu-id="dd9fc-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="dd9fc-109">建立 CustomRule 物件</span><span class="sxs-lookup"><span data-stu-id="dd9fc-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="dd9fc-110">參數</span><span class="sxs-lookup"><span data-stu-id="dd9fc-110">PARAMETERS</span></span>

### <span data-ttu-id="dd9fc-111">-動作</span><span class="sxs-lookup"><span data-stu-id="dd9fc-111">-Action</span></span>
<span data-ttu-id="dd9fc-112">動作類型。</span><span class="sxs-lookup"><span data-stu-id="dd9fc-112">Type of Actions.</span></span>
<span data-ttu-id="dd9fc-113">可能的值包括： "Allow"，"Block"，"Log"</span><span class="sxs-lookup"><span data-stu-id="dd9fc-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

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

### <span data-ttu-id="dd9fc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd9fc-114">-DefaultProfile</span></span>
<span data-ttu-id="dd9fc-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dd9fc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd9fc-116">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="dd9fc-116">-EnabledState</span></span>
<span data-ttu-id="dd9fc-117">已啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="dd9fc-117">Enabled State.</span></span> <span data-ttu-id="dd9fc-118">可能的值包括：「已啟用」、「已停用」。</span><span class="sxs-lookup"><span data-stu-id="dd9fc-118">Possible values include: 'Enabled', 'Disabled'.</span></span>

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

### <span data-ttu-id="dd9fc-119">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="dd9fc-119">-MatchCondition</span></span>
<span data-ttu-id="dd9fc-120">符合條件的清單。</span><span class="sxs-lookup"><span data-stu-id="dd9fc-120">List of match conditions.</span></span>

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

### <span data-ttu-id="dd9fc-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="dd9fc-121">-Name</span></span>
<span data-ttu-id="dd9fc-122">規則名稱</span><span class="sxs-lookup"><span data-stu-id="dd9fc-122">Name of the rule</span></span>

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

### <span data-ttu-id="dd9fc-123">-優先順序</span><span class="sxs-lookup"><span data-stu-id="dd9fc-123">-Priority</span></span>
<span data-ttu-id="dd9fc-124">描述規則的優先順序。</span><span class="sxs-lookup"><span data-stu-id="dd9fc-124">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="dd9fc-125">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="dd9fc-125">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="dd9fc-126">Rate 限制持續時間。</span><span class="sxs-lookup"><span data-stu-id="dd9fc-126">Rate limit duration.</span></span> <span data-ttu-id="dd9fc-127">預設值-1 分鐘</span><span class="sxs-lookup"><span data-stu-id="dd9fc-127">Default - 1 minute</span></span>

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

### <span data-ttu-id="dd9fc-128">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="dd9fc-128">-RateLimitThreshold</span></span>
<span data-ttu-id="dd9fc-129">Rate 限制閾值</span><span class="sxs-lookup"><span data-stu-id="dd9fc-129">Rate limit threshold</span></span>

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

### <span data-ttu-id="dd9fc-130">-RuleType</span><span class="sxs-lookup"><span data-stu-id="dd9fc-130">-RuleType</span></span>
<span data-ttu-id="dd9fc-131">規則的類型。</span><span class="sxs-lookup"><span data-stu-id="dd9fc-131">Type of the rule.</span></span>
<span data-ttu-id="dd9fc-132">可能的值包括： "MatchRule"、"RateLimitRule"</span><span class="sxs-lookup"><span data-stu-id="dd9fc-132">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="dd9fc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd9fc-133">CommonParameters</span></span>
<span data-ttu-id="dd9fc-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dd9fc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd9fc-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dd9fc-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd9fc-136">輸入</span><span class="sxs-lookup"><span data-stu-id="dd9fc-136">INPUTS</span></span>

### <span data-ttu-id="dd9fc-137">所有</span><span class="sxs-lookup"><span data-stu-id="dd9fc-137">None</span></span>

## <span data-ttu-id="dd9fc-138">輸出</span><span class="sxs-lookup"><span data-stu-id="dd9fc-138">OUTPUTS</span></span>

### <span data-ttu-id="dd9fc-139">PSCustomRule 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="dd9fc-139">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="dd9fc-140">筆記</span><span class="sxs-lookup"><span data-stu-id="dd9fc-140">NOTES</span></span>

## <span data-ttu-id="dd9fc-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="dd9fc-141">RELATED LINKS</span></span>

<span data-ttu-id="dd9fc-142">[新-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
[更新-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="dd9fc-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span></span>
