---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/new-azcdndeliveryrulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
ms.openlocfilehash: 6367910117ff00219c3194a06bb51754913df063
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916578"
---
# <span data-ttu-id="6d26e-101">New-AzCdnDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="6d26e-101">New-AzCdnDeliveryRuleCondition</span></span>

## <span data-ttu-id="6d26e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6d26e-102">SYNOPSIS</span></span>
<span data-ttu-id="6d26e-103">建立傳遞規則條件。</span><span class="sxs-lookup"><span data-stu-id="6d26e-103">Creates a delivery rule condition.</span></span>

## <span data-ttu-id="6d26e-104">語法</span><span class="sxs-lookup"><span data-stu-id="6d26e-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRuleCondition -MatchVariable <String> -Operator <String> [-Selector <String>]
 -MatchValue <String[]> [-Transform <String>] [-NegateCondition] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6d26e-105">描述</span><span class="sxs-lookup"><span data-stu-id="6d26e-105">DESCRIPTION</span></span>
<span data-ttu-id="6d26e-106">**New-AzCdnDeliveryRule** Cmdlet 會建立 CDN 端點的建立傳遞規則。</span><span class="sxs-lookup"><span data-stu-id="6d26e-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="6d26e-107">例子</span><span class="sxs-lookup"><span data-stu-id="6d26e-107">EXAMPLES</span></span>

### <span data-ttu-id="6d26e-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="6d26e-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleCondition -MatchVariable UrlPath -Operator Equal -MatchValue "abc"

MatchVariable   : UrlPath
Operator        : Equal
Selector        :
MatchValue      : {abc}
NegateCondition : False
Transfroms      :
```

<span data-ttu-id="6d26e-109">建立簡單的條件。</span><span class="sxs-lookup"><span data-stu-id="6d26e-109">Create a simple condition.</span></span>

## <span data-ttu-id="6d26e-110">參數</span><span class="sxs-lookup"><span data-stu-id="6d26e-110">PARAMETERS</span></span>

### <span data-ttu-id="6d26e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d26e-111">-DefaultProfile</span></span>
<span data-ttu-id="6d26e-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6d26e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d26e-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="6d26e-113">-MatchValue</span></span>
<span data-ttu-id="6d26e-114">可能的相符值清單。</span><span class="sxs-lookup"><span data-stu-id="6d26e-114">List of possible match values.</span></span>

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

### <span data-ttu-id="6d26e-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="6d26e-115">-MatchVariable</span></span>
<span data-ttu-id="6d26e-116">條件之比對變數。</span><span class="sxs-lookup"><span data-stu-id="6d26e-116">Match variable of the condition.</span></span>

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

### <span data-ttu-id="6d26e-117">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="6d26e-117">-NegateCondition</span></span>
<span data-ttu-id="6d26e-118">描述此條件的結果是否應負數。</span><span class="sxs-lookup"><span data-stu-id="6d26e-118">Describes if the result of this condition should be negated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d26e-119">-運算子</span><span class="sxs-lookup"><span data-stu-id="6d26e-119">-Operator</span></span>
<span data-ttu-id="6d26e-120">描述要比對的運算子</span><span class="sxs-lookup"><span data-stu-id="6d26e-120">Describes operator to be matched</span></span>

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

### <span data-ttu-id="6d26e-121">-選取器</span><span class="sxs-lookup"><span data-stu-id="6d26e-121">-Selector</span></span>
<span data-ttu-id="6d26e-122">要比對的選取器名稱</span><span class="sxs-lookup"><span data-stu-id="6d26e-122">Name of Selector to be matched</span></span>

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

### <span data-ttu-id="6d26e-123">-轉換</span><span class="sxs-lookup"><span data-stu-id="6d26e-123">-Transform</span></span>
<span data-ttu-id="6d26e-124">轉換以在比對前套用。</span><span class="sxs-lookup"><span data-stu-id="6d26e-124">Transform to apply before matching.</span></span>
<span data-ttu-id="6d26e-125">可能的值是小寫和大寫</span><span class="sxs-lookup"><span data-stu-id="6d26e-125">Possible values are Lowercase and Uppercase</span></span>

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

### <span data-ttu-id="6d26e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d26e-126">CommonParameters</span></span>
<span data-ttu-id="6d26e-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6d26e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d26e-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6d26e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d26e-129">輸入</span><span class="sxs-lookup"><span data-stu-id="6d26e-129">INPUTS</span></span>

### <span data-ttu-id="6d26e-130">沒有</span><span class="sxs-lookup"><span data-stu-id="6d26e-130">None</span></span>

## <span data-ttu-id="6d26e-131">輸出</span><span class="sxs-lookup"><span data-stu-id="6d26e-131">OUTPUTS</span></span>

### <span data-ttu-id="6d26e-132">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSD力RuleCondition</span><span class="sxs-lookup"><span data-stu-id="6d26e-132">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span></span>

## <span data-ttu-id="6d26e-133">筆記</span><span class="sxs-lookup"><span data-stu-id="6d26e-133">NOTES</span></span>

## <span data-ttu-id="6d26e-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="6d26e-134">RELATED LINKS</span></span>
