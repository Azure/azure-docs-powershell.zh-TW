---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: e2f477aa657bc4d21a650edffb7f014ae3c1ba62
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622068"
---
# <span data-ttu-id="a2b53-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="a2b53-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="a2b53-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a2b53-102">SYNOPSIS</span></span>
<span data-ttu-id="a2b53-103">取得應用程式閘道的 WAF 設定。</span><span class="sxs-lookup"><span data-stu-id="a2b53-103">Gets the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="a2b53-104">句法</span><span class="sxs-lookup"><span data-stu-id="a2b53-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2b53-105">說明</span><span class="sxs-lookup"><span data-stu-id="a2b53-105">DESCRIPTION</span></span>
<span data-ttu-id="a2b53-106">**AzApplicationGatewayWebApplicationFirewallConfiguration** Cmdlet 會取得 web 應用程式防火牆 (WAF 應用程式閘道的) 設定。</span><span class="sxs-lookup"><span data-stu-id="a2b53-106">The **Get-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet gets the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="a2b53-107">示例</span><span class="sxs-lookup"><span data-stu-id="a2b53-107">EXAMPLES</span></span>

### <span data-ttu-id="a2b53-108">範例1：取得應用程式閘道 web 應用程式防火牆設定</span><span class="sxs-lookup"><span data-stu-id="a2b53-108">Example 1: Get an application gateway web application firewall configuration</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

<span data-ttu-id="a2b53-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，然後將它儲存在 $AppGW 變數中。</span><span class="sxs-lookup"><span data-stu-id="a2b53-109">The first command gets the application gateway named ApplicationGateway01, and then stores it in the $AppGW variable.</span></span>
<span data-ttu-id="a2b53-110">第二個命令會在 $AppGW 中取得應用程式閘道的防火牆設定，然後將其儲存在 $FirewallConfig 中。</span><span class="sxs-lookup"><span data-stu-id="a2b53-110">The second command gets the firewall configuration of the application gateway in $AppGW, and then stores it in $FirewallConfig.</span></span>

## <span data-ttu-id="a2b53-111">參數</span><span class="sxs-lookup"><span data-stu-id="a2b53-111">PARAMETERS</span></span>

### <span data-ttu-id="a2b53-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a2b53-112">-ApplicationGateway</span></span>
<span data-ttu-id="a2b53-113">指定應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="a2b53-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="a2b53-114">您可以使用 Get-AzApplicationGateway Cmdlet 來取得應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="a2b53-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="a2b53-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2b53-115">-DefaultProfile</span></span>
<span data-ttu-id="a2b53-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a2b53-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2b53-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2b53-117">CommonParameters</span></span>
<span data-ttu-id="a2b53-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a2b53-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2b53-119">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a2b53-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2b53-120">輸入</span><span class="sxs-lookup"><span data-stu-id="a2b53-120">INPUTS</span></span>

### <span data-ttu-id="a2b53-121">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a2b53-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a2b53-122">輸出</span><span class="sxs-lookup"><span data-stu-id="a2b53-122">OUTPUTS</span></span>

### <span data-ttu-id="a2b53-123">PSApplicationGatewayWebApplicationFirewallConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a2b53-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="a2b53-124">筆記</span><span class="sxs-lookup"><span data-stu-id="a2b53-124">NOTES</span></span>

## <span data-ttu-id="a2b53-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="a2b53-125">RELATED LINKS</span></span>

[<span data-ttu-id="a2b53-126">AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a2b53-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="a2b53-127">新-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="a2b53-127">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="a2b53-128">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="a2b53-128">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


