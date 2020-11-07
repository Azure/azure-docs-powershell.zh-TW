---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 77a87d80e656098eeb9450b0ed612d82a8b9e7fa
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794446"
---
# <span data-ttu-id="ccd74-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="ccd74-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="ccd74-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ccd74-102">SYNOPSIS</span></span>
<span data-ttu-id="ccd74-103">取得應用程式閘道的 WAF 設定。</span><span class="sxs-lookup"><span data-stu-id="ccd74-103">Gets the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="ccd74-104">句法</span><span class="sxs-lookup"><span data-stu-id="ccd74-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ccd74-105">說明</span><span class="sxs-lookup"><span data-stu-id="ccd74-105">DESCRIPTION</span></span>
<span data-ttu-id="ccd74-106">**AzApplicationGatewayWebApplicationFirewallConfiguration** Cmdlet 會取得 web 應用程式防火牆 (WAF 應用程式閘道的) 設定。</span><span class="sxs-lookup"><span data-stu-id="ccd74-106">The **Get-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet gets the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="ccd74-107">示例</span><span class="sxs-lookup"><span data-stu-id="ccd74-107">EXAMPLES</span></span>

### <span data-ttu-id="ccd74-108">範例1：取得應用程式閘道 web 應用程式防火牆設定</span><span class="sxs-lookup"><span data-stu-id="ccd74-108">Example 1: Get an application gateway web application firewall configuration</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

<span data-ttu-id="ccd74-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，然後將它儲存在 $AppGW 變數中。</span><span class="sxs-lookup"><span data-stu-id="ccd74-109">The first command gets the application gateway named ApplicationGateway01, and then stores it in the $AppGW variable.</span></span>

<span data-ttu-id="ccd74-110">第二個命令會在 $AppGW 中取得應用程式閘道的防火牆設定，然後將其儲存在 $FirewallConfig 中。</span><span class="sxs-lookup"><span data-stu-id="ccd74-110">The second command gets the firewall configuration of the application gateway in $AppGW, and then stores it in $FirewallConfig.</span></span>

## <span data-ttu-id="ccd74-111">參數</span><span class="sxs-lookup"><span data-stu-id="ccd74-111">PARAMETERS</span></span>

### <span data-ttu-id="ccd74-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ccd74-112">-ApplicationGateway</span></span>
<span data-ttu-id="ccd74-113">指定應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="ccd74-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="ccd74-114">您可以使用 Get-AzApplicationGateway Cmdlet 來取得應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="ccd74-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ccd74-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccd74-115">-DefaultProfile</span></span>
<span data-ttu-id="ccd74-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ccd74-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccd74-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccd74-117">CommonParameters</span></span>
<span data-ttu-id="ccd74-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ccd74-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccd74-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ccd74-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccd74-120">輸入</span><span class="sxs-lookup"><span data-stu-id="ccd74-120">INPUTS</span></span>

### <span data-ttu-id="ccd74-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ccd74-121">PSApplicationGateway</span></span>
<span data-ttu-id="ccd74-122">形參 "ApplicationGateway" 接受管線中 "PSApplicationGateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="ccd74-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="ccd74-123">輸出</span><span class="sxs-lookup"><span data-stu-id="ccd74-123">OUTPUTS</span></span>

### <span data-ttu-id="ccd74-124">PSApplicationGatewayWebApplicationFirewallConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ccd74-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="ccd74-125">筆記</span><span class="sxs-lookup"><span data-stu-id="ccd74-125">NOTES</span></span>

## <span data-ttu-id="ccd74-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="ccd74-126">RELATED LINKS</span></span>

[<span data-ttu-id="ccd74-127">AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ccd74-127">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="ccd74-128">新-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="ccd74-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="ccd74-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="ccd74-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


