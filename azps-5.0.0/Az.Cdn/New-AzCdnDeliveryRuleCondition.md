---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryrulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
ms.openlocfilehash: 7d7d15fdbaac3de1a212c13fb35dee134dde5381
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285864"
---
# <span data-ttu-id="e8526-101">New-AzCdnDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="e8526-101">New-AzCdnDeliveryRuleCondition</span></span>

## <span data-ttu-id="e8526-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8526-102">SYNOPSIS</span></span>
<span data-ttu-id="e8526-103">建立傳遞規則條件。</span><span class="sxs-lookup"><span data-stu-id="e8526-103">Creates a delivery rule condition.</span></span>

## <span data-ttu-id="e8526-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8526-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRuleCondition -MatchVariable <String> -Operator <String> [-Selector <String>]
 -MatchValue <String[]> [-Transform <String>] [-NegateCondition] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e8526-105">說明</span><span class="sxs-lookup"><span data-stu-id="e8526-105">DESCRIPTION</span></span>
<span data-ttu-id="e8526-106">**新的-AzCdnDeliveryRule** Cmdlet 會建立 CDN 端點建立的傳遞規則。</span><span class="sxs-lookup"><span data-stu-id="e8526-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="e8526-107">示例</span><span class="sxs-lookup"><span data-stu-id="e8526-107">EXAMPLES</span></span>

### <span data-ttu-id="e8526-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e8526-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleCondition -MatchVariable UrlPath -Operator Equal -MatchValue "abc"

MatchVariable   : UrlPath
Operator        : Equal
Selector        :
MatchValue      : {abc}
NegateCondition : False
Transfroms      :
```

<span data-ttu-id="e8526-109">建立簡單的條件。</span><span class="sxs-lookup"><span data-stu-id="e8526-109">Create a simple condition.</span></span>

## <span data-ttu-id="e8526-110">參數</span><span class="sxs-lookup"><span data-stu-id="e8526-110">PARAMETERS</span></span>

### <span data-ttu-id="e8526-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8526-111">-DefaultProfile</span></span>
<span data-ttu-id="e8526-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8526-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8526-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="e8526-113">-MatchValue</span></span>
<span data-ttu-id="e8526-114">可能符合值的清單。</span><span class="sxs-lookup"><span data-stu-id="e8526-114">List of possible match values.</span></span>

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

### <span data-ttu-id="e8526-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="e8526-115">-MatchVariable</span></span>
<span data-ttu-id="e8526-116">符合條件的變數。</span><span class="sxs-lookup"><span data-stu-id="e8526-116">Match variable of the condition.</span></span>

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

### <span data-ttu-id="e8526-117">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="e8526-117">-NegateCondition</span></span>
<span data-ttu-id="e8526-118">描述此條件的結果是否應該取反。</span><span class="sxs-lookup"><span data-stu-id="e8526-118">Describes if the result of this condition should be negated.</span></span>

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

### <span data-ttu-id="e8526-119">-運算子</span><span class="sxs-lookup"><span data-stu-id="e8526-119">-Operator</span></span>
<span data-ttu-id="e8526-120">描述要相符的運算子</span><span class="sxs-lookup"><span data-stu-id="e8526-120">Describes operator to be matched</span></span>

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

### <span data-ttu-id="e8526-121">-選取器</span><span class="sxs-lookup"><span data-stu-id="e8526-121">-Selector</span></span>
<span data-ttu-id="e8526-122">要相符的選擇器名稱</span><span class="sxs-lookup"><span data-stu-id="e8526-122">Name of Selector to be matched</span></span>

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

### <span data-ttu-id="e8526-123">-轉換</span><span class="sxs-lookup"><span data-stu-id="e8526-123">-Transform</span></span>
<span data-ttu-id="e8526-124">在匹配前要套用的轉換。</span><span class="sxs-lookup"><span data-stu-id="e8526-124">Transform to apply before matching.</span></span>
<span data-ttu-id="e8526-125">可能的值為小寫和大寫</span><span class="sxs-lookup"><span data-stu-id="e8526-125">Possible values are Lowercase and Uppercase</span></span>

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

### <span data-ttu-id="e8526-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8526-126">CommonParameters</span></span>
<span data-ttu-id="e8526-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8526-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8526-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e8526-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8526-129">輸入</span><span class="sxs-lookup"><span data-stu-id="e8526-129">INPUTS</span></span>

### <span data-ttu-id="e8526-130">所有</span><span class="sxs-lookup"><span data-stu-id="e8526-130">None</span></span>

## <span data-ttu-id="e8526-131">輸出</span><span class="sxs-lookup"><span data-stu-id="e8526-131">OUTPUTS</span></span>

### <span data-ttu-id="e8526-132">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="e8526-132">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span></span>

## <span data-ttu-id="e8526-133">筆記</span><span class="sxs-lookup"><span data-stu-id="e8526-133">NOTES</span></span>

## <span data-ttu-id="e8526-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8526-134">RELATED LINKS</span></span>
