---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayrewriterulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
ms.openlocfilehash: 9f53ddd628b313a02cf15ce6d80097f0b916c6f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914741"
---
# <span data-ttu-id="d01af-101">New-AzApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="d01af-101">New-AzApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="d01af-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d01af-102">SYNOPSIS</span></span>
<span data-ttu-id="d01af-103">新增條件至應用程式閘道的 RewriteRule。</span><span class="sxs-lookup"><span data-stu-id="d01af-103">Adds a condition to the RewriteRule for an application gateway.</span></span>

## <span data-ttu-id="d01af-104">語法</span><span class="sxs-lookup"><span data-stu-id="d01af-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleCondition -Variable <String> [-Pattern <String>] [-IgnoreCase] [-Negate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d01af-105">描述</span><span class="sxs-lookup"><span data-stu-id="d01af-105">DESCRIPTION</span></span>
<span data-ttu-id="d01af-106">**AzApplicationGatewayRewriteRuleCondition** Cmdlet 會為 Azure 應用程式閘道建立重寫規則條件。</span><span class="sxs-lookup"><span data-stu-id="d01af-106">**The AzApplicationGatewayRewriteRuleCondition** cmdlet creates a rewrite rule condition for an Azure application gateway.</span></span>

## <span data-ttu-id="d01af-107">例子</span><span class="sxs-lookup"><span data-stu-id="d01af-107">EXAMPLES</span></span>

### <span data-ttu-id="d01af-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="d01af-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayRewriteRuleCondition -Variable "var_request_uri" -Pattern "http" -IgnoreCase
PS C:\> $condition

Variable   : var_request_uri
Pattern    : http
IgnoreCase : True
Negate     : False

PS C:\> $condition | Format-Table

Variable        Pattern IgnoreCase Negate
--------        ------- ---------- ------
var_request_uri http          True  False
```
<span data-ttu-id="d01af-109">此命令在重寫規則中建立條件，並儲存在名為 $condition 的變數中。</span><span class="sxs-lookup"><span data-stu-id="d01af-109">This command creates a condition in a rewrite rule and stores the result in the variable named $condition.</span></span>

## <span data-ttu-id="d01af-110">參數</span><span class="sxs-lookup"><span data-stu-id="d01af-110">PARAMETERS</span></span>

### <span data-ttu-id="d01af-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d01af-111">-DefaultProfile</span></span>
<span data-ttu-id="d01af-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d01af-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d01af-113">-IgnoreCase</span><span class="sxs-lookup"><span data-stu-id="d01af-113">-IgnoreCase</span></span>
<span data-ttu-id="d01af-114">設定此標號以忽略圖樣上的大小寫</span><span class="sxs-lookup"><span data-stu-id="d01af-114">Set this flag to ignore case on the pattern</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d01af-115">-Negate</span><span class="sxs-lookup"><span data-stu-id="d01af-115">-Negate</span></span>
<span data-ttu-id="d01af-116">設定此旗標以否定條件驗證</span><span class="sxs-lookup"><span data-stu-id="d01af-116">Set this flag to negate the condition validation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d01af-117">-模式</span><span class="sxs-lookup"><span data-stu-id="d01af-117">-Pattern</span></span>
<span data-ttu-id="d01af-118">在變數頁眉中尋找的模式</span><span class="sxs-lookup"><span data-stu-id="d01af-118">Pattern to look for in the Variable Header</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d01af-119">-Variable</span><span class="sxs-lookup"><span data-stu-id="d01af-119">-Variable</span></span>
<span data-ttu-id="d01af-120">要設定條件的頁眉名稱</span><span class="sxs-lookup"><span data-stu-id="d01af-120">Name of the Header to set condition on it</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d01af-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d01af-121">CommonParameters</span></span>
<span data-ttu-id="d01af-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d01af-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d01af-123">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="d01af-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d01af-124">輸入</span><span class="sxs-lookup"><span data-stu-id="d01af-124">INPUTS</span></span>

### <span data-ttu-id="d01af-125">沒有</span><span class="sxs-lookup"><span data-stu-id="d01af-125">None</span></span>

## <span data-ttu-id="d01af-126">輸出</span><span class="sxs-lookup"><span data-stu-id="d01af-126">OUTPUTS</span></span>

### <span data-ttu-id="d01af-127">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="d01af-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="d01af-128">筆記</span><span class="sxs-lookup"><span data-stu-id="d01af-128">NOTES</span></span>

## <span data-ttu-id="d01af-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="d01af-129">RELATED LINKS</span></span>
[<span data-ttu-id="d01af-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d01af-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d01af-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d01af-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d01af-132">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d01af-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d01af-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d01af-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d01af-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d01af-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d01af-135">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="d01af-135">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="d01af-136">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="d01af-136">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
