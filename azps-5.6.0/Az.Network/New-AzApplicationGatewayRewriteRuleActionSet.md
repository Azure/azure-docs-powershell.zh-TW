---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayrewriteruleactionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
ms.openlocfilehash: 2c5fa5f4c12a44d1efc12e75dfa3901dce061f8e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916522"
---
# <span data-ttu-id="14317-101">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="14317-101">New-AzApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="14317-102">簡介</span><span class="sxs-lookup"><span data-stu-id="14317-102">SYNOPSIS</span></span>
<span data-ttu-id="14317-103">為應用程式閘道建立重寫規則動作集。</span><span class="sxs-lookup"><span data-stu-id="14317-103">Creates a rewrite rule action set for an application gateway.</span></span>

## <span data-ttu-id="14317-104">語法</span><span class="sxs-lookup"><span data-stu-id="14317-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleActionSet
 [-RequestHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-ResponseHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-UrlConfiguration [Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration]]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14317-105">描述</span><span class="sxs-lookup"><span data-stu-id="14317-105">DESCRIPTION</span></span>
<span data-ttu-id="14317-106">**New-AzApplicationGatewayRewriteRuleActionSet** Cmdlet 會為 Azure 應用程式閘道建立重寫規則動作集。</span><span class="sxs-lookup"><span data-stu-id="14317-106">**The New-AzApplicationGatewayRewriteRuleActionSet** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="14317-107">例子</span><span class="sxs-lookup"><span data-stu-id="14317-107">EXAMPLES</span></span>

### <span data-ttu-id="14317-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="14317-108">Example 1</span></span>
```powershell
PS C:\> $action = New-AzApplicationGatewayRewriteRuleActionSet -ResponseHeaderConfiguration $hc -UrlConfiguration $urlConfiguration
```

<span data-ttu-id="14317-109">此命令會建立重寫規則動作集，並儲存在名為 $action 的變數中。</span><span class="sxs-lookup"><span data-stu-id="14317-109">This command creates a rewrite rule action set and stores the result in the variable named $action.</span></span>

## <span data-ttu-id="14317-110">參數</span><span class="sxs-lookup"><span data-stu-id="14317-110">PARAMETERS</span></span>

### <span data-ttu-id="14317-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14317-111">-DefaultProfile</span></span>
<span data-ttu-id="14317-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="14317-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14317-113">-RequestHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="14317-113">-RequestHeaderConfiguration</span></span>
<span data-ttu-id="14317-114">要求標題組配置清單</span><span class="sxs-lookup"><span data-stu-id="14317-114">List of request header configurations</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14317-115">-ResponseHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="14317-115">-ResponseHeaderConfiguration</span></span>
<span data-ttu-id="14317-116">回應標頭組配置清單</span><span class="sxs-lookup"><span data-stu-id="14317-116">List of response header configurations</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14317-117">-UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="14317-117">-UrlConfiguration</span></span>
<span data-ttu-id="14317-118">動作集的 URL 設定</span><span class="sxs-lookup"><span data-stu-id="14317-118">Url Configuration for action set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14317-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14317-119">CommonParameters</span></span>
<span data-ttu-id="14317-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="14317-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14317-121">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="14317-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14317-122">輸入</span><span class="sxs-lookup"><span data-stu-id="14317-122">INPUTS</span></span>

### <span data-ttu-id="14317-123">沒有</span><span class="sxs-lookup"><span data-stu-id="14317-123">None</span></span>

## <span data-ttu-id="14317-124">輸出</span><span class="sxs-lookup"><span data-stu-id="14317-124">OUTPUTS</span></span>

### <span data-ttu-id="14317-125">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="14317-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="14317-126">筆記</span><span class="sxs-lookup"><span data-stu-id="14317-126">NOTES</span></span>

## <span data-ttu-id="14317-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="14317-127">RELATED LINKS</span></span>

[<span data-ttu-id="14317-128">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="14317-128">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="14317-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="14317-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="14317-130">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="14317-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="14317-131">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="14317-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="14317-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="14317-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="14317-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="14317-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="14317-134">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="14317-134">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)

[<span data-ttu-id="14317-135">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="14317-135">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleUrlConfiguration.md)