---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 1ed5c90d4c53769d53cd645b2e5bced7bdec4ce8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621829"
---
# <span data-ttu-id="a4ed0-101">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a4ed0-101">New-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="a4ed0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a4ed0-102">SYNOPSIS</span></span>
<span data-ttu-id="a4ed0-103">建立應用程式閘道的要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="a4ed0-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="a4ed0-104">句法</span><span class="sxs-lookup"><span data-stu-id="a4ed0-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleSet -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4ed0-105">說明</span><span class="sxs-lookup"><span data-stu-id="a4ed0-105">DESCRIPTION</span></span>
<span data-ttu-id="a4ed0-106">**新的-AzApplicationGatewayRewriteRuleSet** Cmdlet 會建立 Azure 應用程式閘道的重寫規則集。</span><span class="sxs-lookup"><span data-stu-id="a4ed0-106">**The New-AzApplicationGatewayRewriteRuleSet** cmdlet creates a rewrite rule set for an Azure application gateway.</span></span>

## <span data-ttu-id="a4ed0-107">示例</span><span class="sxs-lookup"><span data-stu-id="a4ed0-107">EXAMPLES</span></span>

### <span data-ttu-id="a4ed0-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a4ed0-108">Example 1</span></span>
```powershell
PS C:\> $ruleset = New-AzApplicationGatewayRewriteRuleSet -Name ruleset1 -RewriteRule $rule
```

<span data-ttu-id="a4ed0-109">這個命令會建立名為 ruleset1 的重新寫入規則集，並將結果儲存在名為 $ruleset 的變數中。</span><span class="sxs-lookup"><span data-stu-id="a4ed0-109">This command creates a rewrite rule set named ruleset1 and stores the result in the variable named $ruleset.</span></span>

## <span data-ttu-id="a4ed0-110">參數</span><span class="sxs-lookup"><span data-stu-id="a4ed0-110">PARAMETERS</span></span>

### <span data-ttu-id="a4ed0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4ed0-111">-DefaultProfile</span></span>
<span data-ttu-id="a4ed0-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a4ed0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4ed0-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="a4ed0-113">-Name</span></span>
<span data-ttu-id="a4ed0-114">RewriteRuleSet 的名稱</span><span class="sxs-lookup"><span data-stu-id="a4ed0-114">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="a4ed0-115">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="a4ed0-115">-RewriteRule</span></span>
<span data-ttu-id="a4ed0-116">重新寫入規則的清單</span><span class="sxs-lookup"><span data-stu-id="a4ed0-116">List of rewrite rules</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4ed0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4ed0-117">CommonParameters</span></span>
<span data-ttu-id="a4ed0-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a4ed0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4ed0-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a4ed0-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4ed0-120">輸入</span><span class="sxs-lookup"><span data-stu-id="a4ed0-120">INPUTS</span></span>

### <span data-ttu-id="a4ed0-121">所有</span><span class="sxs-lookup"><span data-stu-id="a4ed0-121">None</span></span>

## <span data-ttu-id="a4ed0-122">輸出</span><span class="sxs-lookup"><span data-stu-id="a4ed0-122">OUTPUTS</span></span>

### <span data-ttu-id="a4ed0-123">PSApplicationGatewayRewriteRuleSet 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a4ed0-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="a4ed0-124">筆記</span><span class="sxs-lookup"><span data-stu-id="a4ed0-124">NOTES</span></span>

## <span data-ttu-id="a4ed0-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="a4ed0-125">RELATED LINKS</span></span>

[<span data-ttu-id="a4ed0-126">附加 AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a4ed0-126">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a4ed0-127">AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a4ed0-127">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a4ed0-128">移除-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a4ed0-128">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a4ed0-129">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a4ed0-129">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a4ed0-130">新-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="a4ed0-130">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="a4ed0-131">新-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="a4ed0-131">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="a4ed0-132">新-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="a4ed0-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)