---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 289B761C-1A1D-46D2-8755-B6B6A4758EFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 72cc21b697b2dbdc05ad7106fca5687203aec870
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789205"
---
# <span data-ttu-id="7748a-101">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="7748a-101">Remove-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="7748a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7748a-102">SYNOPSIS</span></span>
<span data-ttu-id="7748a-103">從應用程式閘道移除前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="7748a-103">Removes a front-end IP configuration from an application gateway.</span></span>

## <span data-ttu-id="7748a-104">句法</span><span class="sxs-lookup"><span data-stu-id="7748a-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendIPConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7748a-105">說明</span><span class="sxs-lookup"><span data-stu-id="7748a-105">DESCRIPTION</span></span>
<span data-ttu-id="7748a-106">**AzApplicationGatewayFrontendIPConfig** Cmdlet 會將前端 IP 從 Azure 應用程式閘道中移除。</span><span class="sxs-lookup"><span data-stu-id="7748a-106">The **Remove-AzApplicationGatewayFrontendIPConfig** cmdlet removes frontend IP from an Azure application gateway.</span></span>

## <span data-ttu-id="7748a-107">示例</span><span class="sxs-lookup"><span data-stu-id="7748a-107">EXAMPLES</span></span>

### <span data-ttu-id="7748a-108">範例1：移除前端 IP 設定</span><span class="sxs-lookup"><span data-stu-id="7748a-108">Example 1: Remove a front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIP02"
```

<span data-ttu-id="7748a-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="7748a-109">The first command gets an application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7748a-110">第二個命令會從儲存在 $AppGw 的應用程式閘道中，移除名為 FrontEndIP02 的前端 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="7748a-110">The second command removes the front-end IP configuration named FrontEndIP02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="7748a-111">參數</span><span class="sxs-lookup"><span data-stu-id="7748a-111">PARAMETERS</span></span>

### <span data-ttu-id="7748a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7748a-112">-ApplicationGateway</span></span>
<span data-ttu-id="7748a-113">指定要移除前端 IP 設定的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="7748a-113">Specifies an application gateway from which to remove a front-end IP configuration.</span></span>

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

### <span data-ttu-id="7748a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7748a-114">-DefaultProfile</span></span>
<span data-ttu-id="7748a-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7748a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7748a-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="7748a-116">-Name</span></span>
<span data-ttu-id="7748a-117">指定要移除的前端 IP 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="7748a-117">Specifies the name of a front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="7748a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7748a-118">CommonParameters</span></span>
<span data-ttu-id="7748a-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7748a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7748a-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7748a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7748a-121">輸入</span><span class="sxs-lookup"><span data-stu-id="7748a-121">INPUTS</span></span>

### <span data-ttu-id="7748a-122">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7748a-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7748a-123">輸出</span><span class="sxs-lookup"><span data-stu-id="7748a-123">OUTPUTS</span></span>

### <span data-ttu-id="7748a-124">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7748a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7748a-125">筆記</span><span class="sxs-lookup"><span data-stu-id="7748a-125">NOTES</span></span>

## <span data-ttu-id="7748a-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="7748a-126">RELATED LINKS</span></span>

[<span data-ttu-id="7748a-127">附加 AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="7748a-127">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="7748a-128">AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="7748a-128">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="7748a-129">新-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="7748a-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="7748a-130">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="7748a-130">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)

