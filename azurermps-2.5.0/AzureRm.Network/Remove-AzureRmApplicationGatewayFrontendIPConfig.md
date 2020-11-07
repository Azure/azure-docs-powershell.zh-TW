---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 289B761C-1A1D-46D2-8755-B6B6A4758EFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
ms.openlocfilehash: ead8884b3594edc6377fc4c646c01e51dbe13439
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802305"
---
# <span data-ttu-id="2cf6c-101">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="2cf6c-101">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="2cf6c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2cf6c-102">SYNOPSIS</span></span>
<span data-ttu-id="2cf6c-103">從應用程式閘道移除前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="2cf6c-103">Removes a front-end IP configuration from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2cf6c-104">句法</span><span class="sxs-lookup"><span data-stu-id="2cf6c-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayFrontendIPConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cf6c-105">說明</span><span class="sxs-lookup"><span data-stu-id="2cf6c-105">DESCRIPTION</span></span>
<span data-ttu-id="2cf6c-106">**AzureRmApplicationGatewayFrontendIPConfig** Cmdlet 會將前端 IP 從 Azure 應用程式閘道中移除。</span><span class="sxs-lookup"><span data-stu-id="2cf6c-106">The **Remove-AzureRmApplicationGatewayFrontendIPConfig** cmdlet removes frontend IP from an Azure application gateway.</span></span>

## <span data-ttu-id="2cf6c-107">示例</span><span class="sxs-lookup"><span data-stu-id="2cf6c-107">EXAMPLES</span></span>

### <span data-ttu-id="2cf6c-108">範例1：移除前端 IP 設定</span><span class="sxs-lookup"><span data-stu-id="2cf6c-108">Example 1: Remove a front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIP02"
```

<span data-ttu-id="2cf6c-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="2cf6c-109">The first command gets an application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="2cf6c-110">第二個命令會從儲存在 $AppGw 的應用程式閘道中，移除名為 FrontEndIP02 的前端 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="2cf6c-110">The second command removes the front-end IP configuration named FrontEndIP02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="2cf6c-111">參數</span><span class="sxs-lookup"><span data-stu-id="2cf6c-111">PARAMETERS</span></span>

### <span data-ttu-id="2cf6c-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2cf6c-112">-ApplicationGateway</span></span>
<span data-ttu-id="2cf6c-113">指定要移除前端 IP 設定的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="2cf6c-113">Specifies an application gateway from which to remove a front-end IP configuration.</span></span>

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

### <span data-ttu-id="2cf6c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cf6c-114">-DefaultProfile</span></span>
<span data-ttu-id="2cf6c-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2cf6c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cf6c-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="2cf6c-116">-Name</span></span>
<span data-ttu-id="2cf6c-117">指定要移除的前端 IP 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="2cf6c-117">Specifies the name of a front-end IP configuration to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cf6c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cf6c-118">CommonParameters</span></span>
<span data-ttu-id="2cf6c-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2cf6c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cf6c-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2cf6c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cf6c-121">輸入</span><span class="sxs-lookup"><span data-stu-id="2cf6c-121">INPUTS</span></span>

### <span data-ttu-id="2cf6c-122">System.object</span><span class="sxs-lookup"><span data-stu-id="2cf6c-122">System.String</span></span>

## <span data-ttu-id="2cf6c-123">輸出</span><span class="sxs-lookup"><span data-stu-id="2cf6c-123">OUTPUTS</span></span>

### <span data-ttu-id="2cf6c-124">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2cf6c-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2cf6c-125">筆記</span><span class="sxs-lookup"><span data-stu-id="2cf6c-125">NOTES</span></span>

## <span data-ttu-id="2cf6c-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="2cf6c-126">RELATED LINKS</span></span>

[<span data-ttu-id="2cf6c-127">附加 AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="2cf6c-127">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="2cf6c-128">AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="2cf6c-128">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="2cf6c-129">新-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="2cf6c-129">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="2cf6c-130">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="2cf6c-130">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Set-AzureRmApplicationGatewayFrontendIPConfig.md)


