---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: d657c769a32d7c042a12a56571343885c526eea7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909546"
---
# <span data-ttu-id="a7a44-101">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a7a44-101">Add-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="a7a44-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a7a44-102">SYNOPSIS</span></span>
<span data-ttu-id="a7a44-103">新增重寫規則集至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="a7a44-103">Adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="a7a44-104">語法</span><span class="sxs-lookup"><span data-stu-id="a7a44-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7a44-105">描述</span><span class="sxs-lookup"><span data-stu-id="a7a44-105">DESCRIPTION</span></span>
<span data-ttu-id="a7a44-106">**Add-AzApplicationGatewayRewriteRuleSet** Cmdlet 會新增重寫規則集至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="a7a44-106">The **Add-AzApplicationGatewayRewriteRuleSet** cmdlet adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="a7a44-107">例子</span><span class="sxs-lookup"><span data-stu-id="a7a44-107">EXAMPLES</span></span>

### <span data-ttu-id="a7a44-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="a7a44-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="a7a44-109">第一個命令會獲得應用程式閘道，並儲存在$AppGw變數。</span><span class="sxs-lookup"><span data-stu-id="a7a44-109">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a7a44-110">第二個命令會將重寫規則集新增到應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="a7a44-110">The second command adds the rewrite rule set to the application gateway.</span></span>

## <span data-ttu-id="a7a44-111">參數</span><span class="sxs-lookup"><span data-stu-id="a7a44-111">PARAMETERS</span></span>

### <span data-ttu-id="a7a44-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a7a44-112">-ApplicationGateway</span></span>
<span data-ttu-id="a7a44-113">應用程式Gateway</span><span class="sxs-lookup"><span data-stu-id="a7a44-113">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7a44-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7a44-114">-DefaultProfile</span></span>
<span data-ttu-id="a7a44-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a7a44-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7a44-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="a7a44-116">-Name</span></span>
<span data-ttu-id="a7a44-117">RewriteRuleSet 的名稱</span><span class="sxs-lookup"><span data-stu-id="a7a44-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="a7a44-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="a7a44-118">-RewriteRule</span></span>
<span data-ttu-id="a7a44-119">重寫規則清單</span><span class="sxs-lookup"><span data-stu-id="a7a44-119">List of rewrite rules</span></span>

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

### <span data-ttu-id="a7a44-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7a44-120">CommonParameters</span></span>
<span data-ttu-id="a7a44-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a7a44-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7a44-122">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a7a44-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7a44-123">輸入</span><span class="sxs-lookup"><span data-stu-id="a7a44-123">INPUTS</span></span>

### <span data-ttu-id="a7a44-124">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a7a44-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a7a44-125">輸出</span><span class="sxs-lookup"><span data-stu-id="a7a44-125">OUTPUTS</span></span>

### <span data-ttu-id="a7a44-126">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a7a44-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a7a44-127">筆記</span><span class="sxs-lookup"><span data-stu-id="a7a44-127">NOTES</span></span>

## <span data-ttu-id="a7a44-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="a7a44-128">RELATED LINKS</span></span>

[<span data-ttu-id="a7a44-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a7a44-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a7a44-130">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a7a44-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a7a44-131">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a7a44-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a7a44-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a7a44-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="a7a44-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="a7a44-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="a7a44-134">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="a7a44-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="a7a44-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="a7a44-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
