---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 01f1dc89257088c053cdd6003384c31c708d6b04
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94288255"
---
# <span data-ttu-id="c206e-101">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c206e-101">Remove-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="c206e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c206e-102">SYNOPSIS</span></span>
<span data-ttu-id="c206e-103">從應用程式閘道移除重寫規則集。</span><span class="sxs-lookup"><span data-stu-id="c206e-103">Removes a rewrite rule set from an application gateway.</span></span>

## <span data-ttu-id="c206e-104">句法</span><span class="sxs-lookup"><span data-stu-id="c206e-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRewriteRuleSet -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c206e-105">說明</span><span class="sxs-lookup"><span data-stu-id="c206e-105">DESCRIPTION</span></span>
<span data-ttu-id="c206e-106">**AzApplicationGatewayRewriteRuleSet** Cmdlet 會從 Azure 應用程式閘道移除重新寫入規則集。</span><span class="sxs-lookup"><span data-stu-id="c206e-106">The **Remove-AzApplicationGatewayRewriteRuleSet** cmdlet removes a rewrite rule set from an Azure application gateway.</span></span>

## <span data-ttu-id="c206e-107">示例</span><span class="sxs-lookup"><span data-stu-id="c206e-107">EXAMPLES</span></span>

### <span data-ttu-id="c206e-108">範例1</span><span class="sxs-lookup"><span data-stu-id="c206e-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "RuleSet02"
```

<span data-ttu-id="c206e-109">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="c206e-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c206e-110">第二個命令會從儲存在 $AppGw 的應用程式閘道中，移除名為 RuleSet02 的重新寫入規則集。</span><span class="sxs-lookup"><span data-stu-id="c206e-110">The second command removes the rewrite rule set named RuleSet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="c206e-111">參數</span><span class="sxs-lookup"><span data-stu-id="c206e-111">PARAMETERS</span></span>

### <span data-ttu-id="c206e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c206e-112">-ApplicationGateway</span></span>
<span data-ttu-id="c206e-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c206e-113">The applicationGateway</span></span>

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

### <span data-ttu-id="c206e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c206e-114">-DefaultProfile</span></span>
<span data-ttu-id="c206e-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c206e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c206e-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="c206e-116">-Name</span></span>
<span data-ttu-id="c206e-117">應用程式閘道 RewriteRuleSet 的名稱</span><span class="sxs-lookup"><span data-stu-id="c206e-117">The name of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="c206e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c206e-118">CommonParameters</span></span>
<span data-ttu-id="c206e-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c206e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c206e-120">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c206e-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c206e-121">輸入</span><span class="sxs-lookup"><span data-stu-id="c206e-121">INPUTS</span></span>

### <span data-ttu-id="c206e-122">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c206e-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c206e-123">輸出</span><span class="sxs-lookup"><span data-stu-id="c206e-123">OUTPUTS</span></span>

### <span data-ttu-id="c206e-124">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c206e-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c206e-125">筆記</span><span class="sxs-lookup"><span data-stu-id="c206e-125">NOTES</span></span>

## <span data-ttu-id="c206e-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="c206e-126">RELATED LINKS</span></span>

[<span data-ttu-id="c206e-127">附加 AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c206e-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="c206e-128">AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c206e-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="c206e-129">新-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c206e-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="c206e-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c206e-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="c206e-131">新-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="c206e-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="c206e-132">新-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="c206e-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="c206e-133">新-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="c206e-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
