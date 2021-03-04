---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 099abbe1f8c2a536cebff59f1c21b664bb284e8b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911629"
---
# <span data-ttu-id="316af-101">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="316af-101">Remove-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="316af-102">簡介</span><span class="sxs-lookup"><span data-stu-id="316af-102">SYNOPSIS</span></span>
<span data-ttu-id="316af-103">從應用程式閘道移除重寫規則集。</span><span class="sxs-lookup"><span data-stu-id="316af-103">Removes a rewrite rule set from an application gateway.</span></span>

## <span data-ttu-id="316af-104">語法</span><span class="sxs-lookup"><span data-stu-id="316af-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRewriteRuleSet -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="316af-105">描述</span><span class="sxs-lookup"><span data-stu-id="316af-105">DESCRIPTION</span></span>
<span data-ttu-id="316af-106">**Remove-AzApplicationGatewayRewriteRuleSet** Cmdlet 會從 Azure 應用程式閘道移除重寫規則集。</span><span class="sxs-lookup"><span data-stu-id="316af-106">The **Remove-AzApplicationGatewayRewriteRuleSet** cmdlet removes a rewrite rule set from an Azure application gateway.</span></span>

## <span data-ttu-id="316af-107">例子</span><span class="sxs-lookup"><span data-stu-id="316af-107">EXAMPLES</span></span>

### <span data-ttu-id="316af-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="316af-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "RuleSet02"
```

<span data-ttu-id="316af-109">第一個命令會獲得應用程式閘道，並儲存在$AppGw變數中。</span><span class="sxs-lookup"><span data-stu-id="316af-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="316af-110">第二個命令會從儲存在 $AppGw 的應用程式閘道移除名為 RuleSet02 的重寫規則$AppGw。</span><span class="sxs-lookup"><span data-stu-id="316af-110">The second command removes the rewrite rule set named RuleSet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="316af-111">參數</span><span class="sxs-lookup"><span data-stu-id="316af-111">PARAMETERS</span></span>

### <span data-ttu-id="316af-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="316af-112">-ApplicationGateway</span></span>
<span data-ttu-id="316af-113">應用程式Gateway</span><span class="sxs-lookup"><span data-stu-id="316af-113">The applicationGateway</span></span>

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

### <span data-ttu-id="316af-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="316af-114">-DefaultProfile</span></span>
<span data-ttu-id="316af-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="316af-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="316af-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="316af-116">-Name</span></span>
<span data-ttu-id="316af-117">應用程式閘道 RewriteRuleSet 的名稱</span><span class="sxs-lookup"><span data-stu-id="316af-117">The name of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="316af-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="316af-118">CommonParameters</span></span>
<span data-ttu-id="316af-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="316af-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="316af-120">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="316af-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="316af-121">輸入</span><span class="sxs-lookup"><span data-stu-id="316af-121">INPUTS</span></span>

### <span data-ttu-id="316af-122">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="316af-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="316af-123">輸出</span><span class="sxs-lookup"><span data-stu-id="316af-123">OUTPUTS</span></span>

### <span data-ttu-id="316af-124">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="316af-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="316af-125">筆記</span><span class="sxs-lookup"><span data-stu-id="316af-125">NOTES</span></span>

## <span data-ttu-id="316af-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="316af-126">RELATED LINKS</span></span>

[<span data-ttu-id="316af-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="316af-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="316af-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="316af-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="316af-129">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="316af-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="316af-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="316af-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="316af-131">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="316af-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="316af-132">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="316af-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="316af-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="316af-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
