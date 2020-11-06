---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 44411d8f763e217d5513440a90f713c92c6d6398
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451428"
---
# <span data-ttu-id="5ef16-101">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="5ef16-101">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="5ef16-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5ef16-102">SYNOPSIS</span></span>
<span data-ttu-id="5ef16-103">取得應用程式閘道的 WAF 設定。</span><span class="sxs-lookup"><span data-stu-id="5ef16-103">Gets the WAF configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ef16-104">句法</span><span class="sxs-lookup"><span data-stu-id="5ef16-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ef16-105">說明</span><span class="sxs-lookup"><span data-stu-id="5ef16-105">DESCRIPTION</span></span>
<span data-ttu-id="5ef16-106">**AzureRmApplicationGatewayWebApplicationFirewallConfiguration** Cmdlet 會取得 web 應用程式防火牆 (WAF 應用程式閘道的) 設定。</span><span class="sxs-lookup"><span data-stu-id="5ef16-106">The **Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet gets the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="5ef16-107">示例</span><span class="sxs-lookup"><span data-stu-id="5ef16-107">EXAMPLES</span></span>

### <span data-ttu-id="5ef16-108">範例1：取得應用程式閘道 web 應用程式防火牆設定</span><span class="sxs-lookup"><span data-stu-id="5ef16-108">Example 1: Get an application gateway web application firewall configuration</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

<span data-ttu-id="5ef16-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，然後將它儲存在 $AppGW 變數中。</span><span class="sxs-lookup"><span data-stu-id="5ef16-109">The first command gets the application gateway named ApplicationGateway01, and then stores it in the $AppGW variable.</span></span>

<span data-ttu-id="5ef16-110">第二個命令會在 $AppGW 中取得應用程式閘道的防火牆設定，然後將其儲存在 $FirewallConfig 中。</span><span class="sxs-lookup"><span data-stu-id="5ef16-110">The second command gets the firewall configuration of the application gateway in $AppGW, and then stores it in $FirewallConfig.</span></span>

## <span data-ttu-id="5ef16-111">參數</span><span class="sxs-lookup"><span data-stu-id="5ef16-111">PARAMETERS</span></span>

### <span data-ttu-id="5ef16-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ef16-112">-ApplicationGateway</span></span>
<span data-ttu-id="5ef16-113">指定應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="5ef16-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="5ef16-114">您可以使用 Get-AzureRmApplicationGateway Cmdlet 來取得應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="5ef16-114">You can use the Get-AzureRmApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="5ef16-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ef16-115">-DefaultProfile</span></span>
<span data-ttu-id="5ef16-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5ef16-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ef16-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ef16-117">CommonParameters</span></span>
<span data-ttu-id="5ef16-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5ef16-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ef16-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5ef16-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ef16-120">輸入</span><span class="sxs-lookup"><span data-stu-id="5ef16-120">INPUTS</span></span>

### <span data-ttu-id="5ef16-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ef16-121">PSApplicationGateway</span></span>
<span data-ttu-id="5ef16-122">形參 "ApplicationGateway" 接受管線中 "PSApplicationGateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="5ef16-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="5ef16-123">輸出</span><span class="sxs-lookup"><span data-stu-id="5ef16-123">OUTPUTS</span></span>

### <span data-ttu-id="5ef16-124">PSApplicationGatewayWebApplicationFirewallConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5ef16-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="5ef16-125">筆記</span><span class="sxs-lookup"><span data-stu-id="5ef16-125">NOTES</span></span>

## <span data-ttu-id="5ef16-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="5ef16-126">RELATED LINKS</span></span>

[<span data-ttu-id="5ef16-127">AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ef16-127">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="5ef16-128">新-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="5ef16-128">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="5ef16-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="5ef16-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)


