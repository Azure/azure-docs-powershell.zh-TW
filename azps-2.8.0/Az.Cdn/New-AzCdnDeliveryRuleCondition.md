---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryrulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
ms.openlocfilehash: 830b561a3d46e23f083d77dcac627b28f7dbb94e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613524"
---
# <span data-ttu-id="296b1-101">New-AzCdnDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="296b1-101">New-AzCdnDeliveryRuleCondition</span></span>

## <span data-ttu-id="296b1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="296b1-102">SYNOPSIS</span></span>
<span data-ttu-id="296b1-103">建立傳遞規則條件。</span><span class="sxs-lookup"><span data-stu-id="296b1-103">Creates a delivery rule condition.</span></span>

## <span data-ttu-id="296b1-104">句法</span><span class="sxs-lookup"><span data-stu-id="296b1-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRuleCondition -MatchVariable <String> -Operator <String> -MatchValue <String[]>
 [-Transform <String>] [-NegateCondition] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="296b1-105">說明</span><span class="sxs-lookup"><span data-stu-id="296b1-105">DESCRIPTION</span></span>
<span data-ttu-id="296b1-106">**新的-AzCdnDeliveryRule** Cmdlet 會建立 CDN 端點建立的傳遞規則。</span><span class="sxs-lookup"><span data-stu-id="296b1-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="296b1-107">示例</span><span class="sxs-lookup"><span data-stu-id="296b1-107">EXAMPLES</span></span>

### <span data-ttu-id="296b1-108">範例1</span><span class="sxs-lookup"><span data-stu-id="296b1-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleCondition -MatchVariable UrlPath -Operator Equal -MatchValue "abc"

MatchVariable   : UrlPath
Operator        : Equal
Selector        :
MatchValue      : {abc}
NegateCondition : False
Transfroms      :
```

<span data-ttu-id="296b1-109">建立簡單的條件。</span><span class="sxs-lookup"><span data-stu-id="296b1-109">Create a simple condition.</span></span>

## <span data-ttu-id="296b1-110">參數</span><span class="sxs-lookup"><span data-stu-id="296b1-110">PARAMETERS</span></span>

### <span data-ttu-id="296b1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="296b1-111">-DefaultProfile</span></span>
<span data-ttu-id="296b1-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="296b1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="296b1-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="296b1-113">-MatchValue</span></span>
<span data-ttu-id="296b1-114">可能符合值的清單。</span><span class="sxs-lookup"><span data-stu-id="296b1-114">List of possible match values.</span></span>

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

### <span data-ttu-id="296b1-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="296b1-115">-MatchVariable</span></span>
<span data-ttu-id="296b1-116">符合條件的變數。</span><span class="sxs-lookup"><span data-stu-id="296b1-116">Match variable of the condition.</span></span>

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

### <span data-ttu-id="296b1-117">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="296b1-117">-NegateCondition</span></span>
<span data-ttu-id="296b1-118">描述此條件的結果是否應該取反。</span><span class="sxs-lookup"><span data-stu-id="296b1-118">Describes if the result of this condition should be negated.</span></span>

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

### <span data-ttu-id="296b1-119">-運算子</span><span class="sxs-lookup"><span data-stu-id="296b1-119">-Operator</span></span>
<span data-ttu-id="296b1-120">描述要相符的運算子</span><span class="sxs-lookup"><span data-stu-id="296b1-120">Describes operator to be matched</span></span>

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

### <span data-ttu-id="296b1-121">-轉換</span><span class="sxs-lookup"><span data-stu-id="296b1-121">-Transform</span></span>
<span data-ttu-id="296b1-122">在匹配前要套用的轉換。</span><span class="sxs-lookup"><span data-stu-id="296b1-122">Transform to apply before matching.</span></span>
<span data-ttu-id="296b1-123">可能的值為小寫和大寫</span><span class="sxs-lookup"><span data-stu-id="296b1-123">Possible values are Lowercase and Uppercase</span></span>

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

### <span data-ttu-id="296b1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="296b1-124">CommonParameters</span></span>
<span data-ttu-id="296b1-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="296b1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="296b1-126">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="296b1-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="296b1-127">輸入</span><span class="sxs-lookup"><span data-stu-id="296b1-127">INPUTS</span></span>

### <span data-ttu-id="296b1-128">所有</span><span class="sxs-lookup"><span data-stu-id="296b1-128">None</span></span>

## <span data-ttu-id="296b1-129">輸出</span><span class="sxs-lookup"><span data-stu-id="296b1-129">OUTPUTS</span></span>

### <span data-ttu-id="296b1-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="296b1-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span></span>

## <span data-ttu-id="296b1-131">筆記</span><span class="sxs-lookup"><span data-stu-id="296b1-131">NOTES</span></span>

## <span data-ttu-id="296b1-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="296b1-132">RELATED LINKS</span></span>
