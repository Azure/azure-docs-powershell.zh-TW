---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: d3b8a57fcd170a2a1f1e4e4c539cff8a60885260
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912746"
---
# <span data-ttu-id="505b4-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="505b4-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="505b4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="505b4-102">SYNOPSIS</span></span>
<span data-ttu-id="505b4-103">獲得應用程式閘道的 WAF 組塊。</span><span class="sxs-lookup"><span data-stu-id="505b4-103">Gets the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="505b4-104">語法</span><span class="sxs-lookup"><span data-stu-id="505b4-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="505b4-105">描述</span><span class="sxs-lookup"><span data-stu-id="505b4-105">DESCRIPTION</span></span>
<span data-ttu-id="505b4-106">**Get-AzApplicationGatewayWebApplicationFirewallConfiguration** Cmdlet 會取得 Web 應用程式防火牆 (WAF) 應用程式閘道的組式。</span><span class="sxs-lookup"><span data-stu-id="505b4-106">The **Get-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet gets the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="505b4-107">例子</span><span class="sxs-lookup"><span data-stu-id="505b4-107">EXAMPLES</span></span>

### <span data-ttu-id="505b4-108">範例 1：取得應用程式閘道 Web 應用程式防火牆組</span><span class="sxs-lookup"><span data-stu-id="505b4-108">Example 1: Get an application gateway web application firewall configuration</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

<span data-ttu-id="505b4-109">第一個命令會獲得名為 ApplicationGateway01 的應用程式閘道，然後將它儲存在$AppGW變數。</span><span class="sxs-lookup"><span data-stu-id="505b4-109">The first command gets the application gateway named ApplicationGateway01, and then stores it in the $AppGW variable.</span></span>
<span data-ttu-id="505b4-110">第二個命令會獲得應用程式閘道在 $AppGW 中的防火牆$FirewallConfig。</span><span class="sxs-lookup"><span data-stu-id="505b4-110">The second command gets the firewall configuration of the application gateway in $AppGW, and then stores it in $FirewallConfig.</span></span>

## <span data-ttu-id="505b4-111">參數</span><span class="sxs-lookup"><span data-stu-id="505b4-111">PARAMETERS</span></span>

### <span data-ttu-id="505b4-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="505b4-112">-ApplicationGateway</span></span>
<span data-ttu-id="505b4-113">指定應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="505b4-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="505b4-114">您可以使用 Get-AzApplicationGateway Cmdlet 取得應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="505b4-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="505b4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="505b4-115">-DefaultProfile</span></span>
<span data-ttu-id="505b4-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="505b4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="505b4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="505b4-117">CommonParameters</span></span>
<span data-ttu-id="505b4-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="505b4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="505b4-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="505b4-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="505b4-120">輸入</span><span class="sxs-lookup"><span data-stu-id="505b4-120">INPUTS</span></span>

### <span data-ttu-id="505b4-121">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="505b4-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="505b4-122">輸出</span><span class="sxs-lookup"><span data-stu-id="505b4-122">OUTPUTS</span></span>

### <span data-ttu-id="505b4-123">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="505b4-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="505b4-124">筆記</span><span class="sxs-lookup"><span data-stu-id="505b4-124">NOTES</span></span>

## <span data-ttu-id="505b4-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="505b4-125">RELATED LINKS</span></span>

[<span data-ttu-id="505b4-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="505b4-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="505b4-127">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="505b4-127">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="505b4-128">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="505b4-128">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


