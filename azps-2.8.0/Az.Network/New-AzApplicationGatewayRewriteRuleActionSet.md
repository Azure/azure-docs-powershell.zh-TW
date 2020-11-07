---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleactionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
ms.openlocfilehash: 84be6aa60ede19e88b98ca9517fa3cbce3872c8b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789929"
---
# <span data-ttu-id="bd99d-101">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="bd99d-101">New-AzApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="bd99d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bd99d-102">SYNOPSIS</span></span>
<span data-ttu-id="bd99d-103">建立應用程式閘道的重寫規則動作集。</span><span class="sxs-lookup"><span data-stu-id="bd99d-103">Creates a rewrite rule action set for an application gateway.</span></span>

## <span data-ttu-id="bd99d-104">句法</span><span class="sxs-lookup"><span data-stu-id="bd99d-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleActionSet
 [-RequestHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-ResponseHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd99d-105">說明</span><span class="sxs-lookup"><span data-stu-id="bd99d-105">DESCRIPTION</span></span>
<span data-ttu-id="bd99d-106">**新的-AzApplicationGatewayRewriteRuleActionSet** Cmdlet 會建立 Azure 應用程式閘道的重寫規則動作集。</span><span class="sxs-lookup"><span data-stu-id="bd99d-106">**The New-AzApplicationGatewayRewriteRuleActionSet** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="bd99d-107">示例</span><span class="sxs-lookup"><span data-stu-id="bd99d-107">EXAMPLES</span></span>

### <span data-ttu-id="bd99d-108">範例1</span><span class="sxs-lookup"><span data-stu-id="bd99d-108">Example 1</span></span>
```powershell
PS C:\> $action = New-AzApplicationGatewayRewriteRuleActionSet -ResponseHeaderConfiguration $hc
```

<span data-ttu-id="bd99d-109">這個命令會建立重寫規則動作集，並將結果儲存在名為 $action 的變數中。</span><span class="sxs-lookup"><span data-stu-id="bd99d-109">This command creates a rewrite rule action set and stores the result in the variable named $action.</span></span>

## <span data-ttu-id="bd99d-110">參數</span><span class="sxs-lookup"><span data-stu-id="bd99d-110">PARAMETERS</span></span>

### <span data-ttu-id="bd99d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd99d-111">-DefaultProfile</span></span>
<span data-ttu-id="bd99d-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bd99d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd99d-113">-RequestHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="bd99d-113">-RequestHeaderConfiguration</span></span>
<span data-ttu-id="bd99d-114">要求標頭設定清單</span><span class="sxs-lookup"><span data-stu-id="bd99d-114">List of request header configurations</span></span>

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

### <span data-ttu-id="bd99d-115">-ResponseHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="bd99d-115">-ResponseHeaderConfiguration</span></span>
<span data-ttu-id="bd99d-116">回應標頭設定清單</span><span class="sxs-lookup"><span data-stu-id="bd99d-116">List of response header configurations</span></span>

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

### <span data-ttu-id="bd99d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd99d-117">CommonParameters</span></span>
<span data-ttu-id="bd99d-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bd99d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd99d-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bd99d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd99d-120">輸入</span><span class="sxs-lookup"><span data-stu-id="bd99d-120">INPUTS</span></span>

### <span data-ttu-id="bd99d-121">所有</span><span class="sxs-lookup"><span data-stu-id="bd99d-121">None</span></span>

## <span data-ttu-id="bd99d-122">輸出</span><span class="sxs-lookup"><span data-stu-id="bd99d-122">OUTPUTS</span></span>

### <span data-ttu-id="bd99d-123">PSApplicationGatewayRewriteRuleActionSet 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bd99d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="bd99d-124">筆記</span><span class="sxs-lookup"><span data-stu-id="bd99d-124">NOTES</span></span>

## <span data-ttu-id="bd99d-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="bd99d-125">RELATED LINKS</span></span>

[<span data-ttu-id="bd99d-126">附加 AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bd99d-126">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="bd99d-127">AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bd99d-127">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="bd99d-128">新-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bd99d-128">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="bd99d-129">移除-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bd99d-129">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="bd99d-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bd99d-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="bd99d-131">新-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="bd99d-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="bd99d-132">新-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="bd99d-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
