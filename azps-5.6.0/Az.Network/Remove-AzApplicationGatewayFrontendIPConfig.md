---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 289B761C-1A1D-46D2-8755-B6B6A4758EFC
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 0c226cf7dabbc170e137f1a809cee0afe3c7e76f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912349"
---
# <span data-ttu-id="ed36f-101">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ed36f-101">Remove-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="ed36f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ed36f-102">SYNOPSIS</span></span>
<span data-ttu-id="ed36f-103">從應用程式閘道移除前端 IP 組式。</span><span class="sxs-lookup"><span data-stu-id="ed36f-103">Removes a front-end IP configuration from an application gateway.</span></span>

## <span data-ttu-id="ed36f-104">語法</span><span class="sxs-lookup"><span data-stu-id="ed36f-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendIPConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed36f-105">描述</span><span class="sxs-lookup"><span data-stu-id="ed36f-105">DESCRIPTION</span></span>
<span data-ttu-id="ed36f-106">**Remove-AzApplicationGatewayFrontendIPConfig** Cmdlet 會從 Azure 應用程式閘道移除前端 IP。</span><span class="sxs-lookup"><span data-stu-id="ed36f-106">The **Remove-AzApplicationGatewayFrontendIPConfig** cmdlet removes frontend IP from an Azure application gateway.</span></span>

## <span data-ttu-id="ed36f-107">例子</span><span class="sxs-lookup"><span data-stu-id="ed36f-107">EXAMPLES</span></span>

### <span data-ttu-id="ed36f-108">範例 1：移除前端 IP 組</span><span class="sxs-lookup"><span data-stu-id="ed36f-108">Example 1: Remove a front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIP02"
```

<span data-ttu-id="ed36f-109">第一個命令會獲得名為 ApplicationGateway01 的應用程式閘道，並儲存在$AppGw變數中。</span><span class="sxs-lookup"><span data-stu-id="ed36f-109">The first command gets an application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ed36f-110">第二個命令會從儲存在 $AppGw 的應用程式閘道移除名為 FrontEndIP02 的前端 IP $AppGw。</span><span class="sxs-lookup"><span data-stu-id="ed36f-110">The second command removes the front-end IP configuration named FrontEndIP02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="ed36f-111">參數</span><span class="sxs-lookup"><span data-stu-id="ed36f-111">PARAMETERS</span></span>

### <span data-ttu-id="ed36f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ed36f-112">-ApplicationGateway</span></span>
<span data-ttu-id="ed36f-113">指定要從中移除前端 IP 設定檔的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="ed36f-113">Specifies an application gateway from which to remove a front-end IP configuration.</span></span>

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

### <span data-ttu-id="ed36f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed36f-114">-DefaultProfile</span></span>
<span data-ttu-id="ed36f-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ed36f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed36f-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="ed36f-116">-Name</span></span>
<span data-ttu-id="ed36f-117">指定要移除的前端 IP 組名。</span><span class="sxs-lookup"><span data-stu-id="ed36f-117">Specifies the name of a front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="ed36f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed36f-118">CommonParameters</span></span>
<span data-ttu-id="ed36f-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ed36f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed36f-120">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed36f-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed36f-121">輸入</span><span class="sxs-lookup"><span data-stu-id="ed36f-121">INPUTS</span></span>

### <span data-ttu-id="ed36f-122">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ed36f-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ed36f-123">輸出</span><span class="sxs-lookup"><span data-stu-id="ed36f-123">OUTPUTS</span></span>

### <span data-ttu-id="ed36f-124">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ed36f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ed36f-125">筆記</span><span class="sxs-lookup"><span data-stu-id="ed36f-125">NOTES</span></span>

## <span data-ttu-id="ed36f-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="ed36f-126">RELATED LINKS</span></span>

[<span data-ttu-id="ed36f-127">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ed36f-127">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="ed36f-128">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ed36f-128">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="ed36f-129">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ed36f-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="ed36f-130">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ed36f-130">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


