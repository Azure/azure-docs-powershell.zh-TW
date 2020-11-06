---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorCustomRuleObject.md
ms.openlocfilehash: a5a1494bd217147a4e6f4c94a85140313429898f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443832"
---
# <span data-ttu-id="bafc4-101">New-AzureRmFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="bafc4-101">New-AzureRmFrontDoorCustomRuleObject</span></span>

## <span data-ttu-id="bafc4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bafc4-102">SYNOPSIS</span></span>
<span data-ttu-id="bafc4-103">建立 WAF 原則建立的 CustomRule 物件</span><span class="sxs-lookup"><span data-stu-id="bafc4-103">Create CustomRule Object for WAF policy creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bafc4-104">句法</span><span class="sxs-lookup"><span data-stu-id="bafc4-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorCustomRuleObject -Name <String> -RuleType <PSCustomRuleType>
 -MatchCondition <PSMatchCondition[]> -Action <PSAction> -Priority <Int32>
 [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>] [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bafc4-105">說明</span><span class="sxs-lookup"><span data-stu-id="bafc4-105">DESCRIPTION</span></span>
<span data-ttu-id="bafc4-106">建立 WAF 原則建立的 CustomRule 物件</span><span class="sxs-lookup"><span data-stu-id="bafc4-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="bafc4-107">示例</span><span class="sxs-lookup"><span data-stu-id="bafc4-107">EXAMPLES</span></span>

### <span data-ttu-id="bafc4-108">範例1</span><span class="sxs-lookup"><span data-stu-id="bafc4-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

RuleType                   : MatchRule
Action                     : Block
MatchConditions            : {Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition}
Priority                   : 2
RateLimitDurationInMinutes : 1
RateLimitThreshold         :
Name                       : Rule1
Etag                       :
Transforms                 :
```

<span data-ttu-id="bafc4-109">建立 CustomRule 物件</span><span class="sxs-lookup"><span data-stu-id="bafc4-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="bafc4-110">參數</span><span class="sxs-lookup"><span data-stu-id="bafc4-110">PARAMETERS</span></span>

### <span data-ttu-id="bafc4-111">-動作</span><span class="sxs-lookup"><span data-stu-id="bafc4-111">-Action</span></span>
<span data-ttu-id="bafc4-112">動作類型。</span><span class="sxs-lookup"><span data-stu-id="bafc4-112">Type of Actions.</span></span>
<span data-ttu-id="bafc4-113">可能的值包括： "Allow"，"Block"，"Log"</span><span class="sxs-lookup"><span data-stu-id="bafc4-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAction
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bafc4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bafc4-114">-DefaultProfile</span></span>
<span data-ttu-id="bafc4-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bafc4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bafc4-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="bafc4-116">-MatchCondition</span></span>
<span data-ttu-id="bafc4-117">符合條件的清單。</span><span class="sxs-lookup"><span data-stu-id="bafc4-117">List of match conditions.</span></span>

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

### <span data-ttu-id="bafc4-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="bafc4-118">-Name</span></span>
<span data-ttu-id="bafc4-119">規則名稱</span><span class="sxs-lookup"><span data-stu-id="bafc4-119">Name of the rule</span></span>

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

### <span data-ttu-id="bafc4-120">-優先順序</span><span class="sxs-lookup"><span data-stu-id="bafc4-120">-Priority</span></span>
<span data-ttu-id="bafc4-121">描述規則的優先順序。</span><span class="sxs-lookup"><span data-stu-id="bafc4-121">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="bafc4-122">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="bafc4-122">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="bafc4-123">Rate 限制持續時間。</span><span class="sxs-lookup"><span data-stu-id="bafc4-123">Rate limit duration.</span></span> <span data-ttu-id="bafc4-124">預設值-1 分鐘</span><span class="sxs-lookup"><span data-stu-id="bafc4-124">Default - 1 minute</span></span>

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

### <span data-ttu-id="bafc4-125">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="bafc4-125">-RateLimitThreshold</span></span>
<span data-ttu-id="bafc4-126">Rate 限制 thresold</span><span class="sxs-lookup"><span data-stu-id="bafc4-126">Rate limit thresold</span></span>

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

### <span data-ttu-id="bafc4-127">-RuleType</span><span class="sxs-lookup"><span data-stu-id="bafc4-127">-RuleType</span></span>
<span data-ttu-id="bafc4-128">規則的類型。</span><span class="sxs-lookup"><span data-stu-id="bafc4-128">Type of the rule.</span></span>
<span data-ttu-id="bafc4-129">可能的值包括： "MatchRule"、"RateLimitRule"</span><span class="sxs-lookup"><span data-stu-id="bafc4-129">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="bafc4-130">-轉換</span><span class="sxs-lookup"><span data-stu-id="bafc4-130">-Transform</span></span>
<span data-ttu-id="bafc4-131">轉換清單</span><span class="sxs-lookup"><span data-stu-id="bafc4-131">List of transforms</span></span>

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

### <span data-ttu-id="bafc4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bafc4-132">CommonParameters</span></span>
<span data-ttu-id="bafc4-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bafc4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bafc4-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bafc4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bafc4-135">輸入</span><span class="sxs-lookup"><span data-stu-id="bafc4-135">INPUTS</span></span>

### <span data-ttu-id="bafc4-136">所有</span><span class="sxs-lookup"><span data-stu-id="bafc4-136">None</span></span>

## <span data-ttu-id="bafc4-137">輸出</span><span class="sxs-lookup"><span data-stu-id="bafc4-137">OUTPUTS</span></span>

### <span data-ttu-id="bafc4-138">PSCustomRule 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="bafc4-138">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="bafc4-139">筆記</span><span class="sxs-lookup"><span data-stu-id="bafc4-139">NOTES</span></span>

## <span data-ttu-id="bafc4-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="bafc4-140">RELATED LINKS</span></span>

<span data-ttu-id="bafc4-141">[新-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="bafc4-141">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)</span></span>
