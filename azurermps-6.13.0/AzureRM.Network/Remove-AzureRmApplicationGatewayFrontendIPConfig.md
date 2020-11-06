---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 289B761C-1A1D-46D2-8755-B6B6A4758EFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 94cb9e07bc5d4b8d59e543c39ddada5386ebcb27
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446941"
---
# <span data-ttu-id="ab2e4-101">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ab2e4-101">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="ab2e4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ab2e4-102">SYNOPSIS</span></span>
<span data-ttu-id="ab2e4-103">從應用程式閘道移除前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="ab2e4-103">Removes a front-end IP configuration from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab2e4-104">句法</span><span class="sxs-lookup"><span data-stu-id="ab2e4-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayFrontendIPConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab2e4-105">說明</span><span class="sxs-lookup"><span data-stu-id="ab2e4-105">DESCRIPTION</span></span>
<span data-ttu-id="ab2e4-106">**AzureRmApplicationGatewayFrontendIPConfig** Cmdlet 會將前端 IP 從 Azure 應用程式閘道中移除。</span><span class="sxs-lookup"><span data-stu-id="ab2e4-106">The **Remove-AzureRmApplicationGatewayFrontendIPConfig** cmdlet removes frontend IP from an Azure application gateway.</span></span>

## <span data-ttu-id="ab2e4-107">示例</span><span class="sxs-lookup"><span data-stu-id="ab2e4-107">EXAMPLES</span></span>

### <span data-ttu-id="ab2e4-108">範例1：移除前端 IP 設定</span><span class="sxs-lookup"><span data-stu-id="ab2e4-108">Example 1: Remove a front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIP02"
```

<span data-ttu-id="ab2e4-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="ab2e4-109">The first command gets an application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ab2e4-110">第二個命令會從儲存在 $AppGw 的應用程式閘道中，移除名為 FrontEndIP02 的前端 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="ab2e4-110">The second command removes the front-end IP configuration named FrontEndIP02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="ab2e4-111">參數</span><span class="sxs-lookup"><span data-stu-id="ab2e4-111">PARAMETERS</span></span>

### <span data-ttu-id="ab2e4-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ab2e4-112">-ApplicationGateway</span></span>
<span data-ttu-id="ab2e4-113">指定要移除前端 IP 設定的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="ab2e4-113">Specifies an application gateway from which to remove a front-end IP configuration.</span></span>

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

### <span data-ttu-id="ab2e4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab2e4-114">-DefaultProfile</span></span>
<span data-ttu-id="ab2e4-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ab2e4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab2e4-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="ab2e4-116">-Name</span></span>
<span data-ttu-id="ab2e4-117">指定要移除的前端 IP 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="ab2e4-117">Specifies the name of a front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="ab2e4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab2e4-118">CommonParameters</span></span>
<span data-ttu-id="ab2e4-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ab2e4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab2e4-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ab2e4-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab2e4-121">輸入</span><span class="sxs-lookup"><span data-stu-id="ab2e4-121">INPUTS</span></span>

### <span data-ttu-id="ab2e4-122">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ab2e4-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="ab2e4-123">參數： ApplicationGateway (ByValue) </span><span class="sxs-lookup"><span data-stu-id="ab2e4-123">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="ab2e4-124">輸出</span><span class="sxs-lookup"><span data-stu-id="ab2e4-124">OUTPUTS</span></span>

### <span data-ttu-id="ab2e4-125">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ab2e4-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ab2e4-126">筆記</span><span class="sxs-lookup"><span data-stu-id="ab2e4-126">NOTES</span></span>

## <span data-ttu-id="ab2e4-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="ab2e4-127">RELATED LINKS</span></span>

[<span data-ttu-id="ab2e4-128">附加 AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ab2e4-128">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="ab2e4-129">AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ab2e4-129">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="ab2e4-130">新-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ab2e4-130">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="ab2e4-131">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ab2e4-131">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Set-AzureRmApplicationGatewayFrontendIPConfig.md)


