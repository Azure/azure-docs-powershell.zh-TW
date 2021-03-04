---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 364C41D0-A5DB-4AEF-853A-FE5A11AD9155
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: cab20e2b92343549b5138f14f88505c70624effb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913494"
---
# <span data-ttu-id="62b6d-101">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="62b6d-101">Get-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="62b6d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="62b6d-102">SYNOPSIS</span></span>
<span data-ttu-id="62b6d-103">獲得應用程式閘道的前端 IP 組式。</span><span class="sxs-lookup"><span data-stu-id="62b6d-103">Gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="62b6d-104">語法</span><span class="sxs-lookup"><span data-stu-id="62b6d-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendIPConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62b6d-105">描述</span><span class="sxs-lookup"><span data-stu-id="62b6d-105">DESCRIPTION</span></span>
<span data-ttu-id="62b6d-106">**Get-AzApplicationGatewayFrontendIPConfig** Cmdlet 會取得應用程式閘道的前端 IP 組式。</span><span class="sxs-lookup"><span data-stu-id="62b6d-106">The **Get-AzApplicationGatewayFrontendIPConfig** cmdlet gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="62b6d-107">例子</span><span class="sxs-lookup"><span data-stu-id="62b6d-107">EXAMPLES</span></span>

### <span data-ttu-id="62b6d-108">範例 1：取得指定的前端 IP 組式</span><span class="sxs-lookup"><span data-stu-id="62b6d-108">Example 1: Get a specified front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIP= Get-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -ApplicationGateway $AppGw
```

<span data-ttu-id="62b6d-109">第一個命令會從名為 ResourceGroup01 的資源群組中，獲得名為 ApplicationGateway01 的應用程式閘道，並儲存在$AppGw變數。第二個命令會從 $AppGw 取名為 FrontEndIP01 的前端 IP 組$FrontEndIP變數。</span><span class="sxs-lookup"><span data-stu-id="62b6d-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the front-end IP configuration named FrontEndIP01 from $AppGw and stores it in the $FrontEndIP variable.</span></span>

### <span data-ttu-id="62b6d-110">範例 2：取得前端 IP 組式清單</span><span class="sxs-lookup"><span data-stu-id="62b6d-110">Example 2: Get a list of front-end IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIPs= Get-AzApplicationGatewayFrontendIPConfig  -ApplicationGateway $AppGw
```

<span data-ttu-id="62b6d-111">第一個命令會從名為 ResourceGroup01 的資源群組中，獲得名為 ApplicationGateway01 的應用程式閘道，並儲存在$AppGw變數。第二個命令會從清單中獲得前端 IP $AppGw，並儲存在 $FrontEndIPs 變數中。</span><span class="sxs-lookup"><span data-stu-id="62b6d-111">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets a list of the front-end IP configurations from $AppGw and stores it in the $FrontEndIPs variable.</span></span>

## <span data-ttu-id="62b6d-112">參數</span><span class="sxs-lookup"><span data-stu-id="62b6d-112">PARAMETERS</span></span>

### <span data-ttu-id="62b6d-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="62b6d-113">-ApplicationGateway</span></span>
<span data-ttu-id="62b6d-114">指定包含前端 IP 設定檔的應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="62b6d-114">Specifies the application gateway object that contains the front-end IP configuration.</span></span>

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

### <span data-ttu-id="62b6d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62b6d-115">-DefaultProfile</span></span>
<span data-ttu-id="62b6d-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="62b6d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62b6d-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="62b6d-117">-Name</span></span>
<span data-ttu-id="62b6d-118">指定此 Cmdlet 所獲得前端 IP 群組原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="62b6d-118">Specifies the name of the front-end IP configuration that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62b6d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62b6d-119">CommonParameters</span></span>
<span data-ttu-id="62b6d-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="62b6d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62b6d-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62b6d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62b6d-122">輸入</span><span class="sxs-lookup"><span data-stu-id="62b6d-122">INPUTS</span></span>

### <span data-ttu-id="62b6d-123">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="62b6d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="62b6d-124">輸出</span><span class="sxs-lookup"><span data-stu-id="62b6d-124">OUTPUTS</span></span>

### <span data-ttu-id="62b6d-125">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="62b6d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="62b6d-126">筆記</span><span class="sxs-lookup"><span data-stu-id="62b6d-126">NOTES</span></span>

## <span data-ttu-id="62b6d-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="62b6d-127">RELATED LINKS</span></span>

[<span data-ttu-id="62b6d-128">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="62b6d-128">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="62b6d-129">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="62b6d-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="62b6d-130">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="62b6d-130">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="62b6d-131">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="62b6d-131">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


