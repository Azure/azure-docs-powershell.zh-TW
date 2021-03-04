---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F01CB88A-49E7-41D8-B4E7-F1A4DCDC6B84
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
ms.openlocfilehash: cf869a0de5847b1930879dbd610749746370791b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912785"
---
# <span data-ttu-id="f83bb-101">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="f83bb-101">Get-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="f83bb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f83bb-102">SYNOPSIS</span></span>
<span data-ttu-id="f83bb-103">獲得應用程式閘道的 SKU。</span><span class="sxs-lookup"><span data-stu-id="f83bb-103">Gets the SKU of an application gateway.</span></span>

## <span data-ttu-id="f83bb-104">語法</span><span class="sxs-lookup"><span data-stu-id="f83bb-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f83bb-105">描述</span><span class="sxs-lookup"><span data-stu-id="f83bb-105">DESCRIPTION</span></span>
<span data-ttu-id="f83bb-106">**Get-AzApplicationGatewaySku** Cmdlet 會取得應用程式閘道 (SKU) 庫存單位。</span><span class="sxs-lookup"><span data-stu-id="f83bb-106">The **Get-AzApplicationGatewaySku** cmdlet gets the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="f83bb-107">例子</span><span class="sxs-lookup"><span data-stu-id="f83bb-107">EXAMPLES</span></span>

### <span data-ttu-id="f83bb-108">範例 1：取得應用程式閘道 SKU</span><span class="sxs-lookup"><span data-stu-id="f83bb-108">Example 1: Get an application gateway SKU</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SKU = Get-AzApplicationGatewaySku -ApplicationGateway $AppGW
```

<span data-ttu-id="f83bb-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並儲存在名為 applicationGateway01 的$AppGW。</span><span class="sxs-lookup"><span data-stu-id="f83bb-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="f83bb-110">第二個命令會取得名為 ApplicationGateway01 的應用程式閘道 SKU，並儲存在名為 applicationGateway01 的變數$SKU。</span><span class="sxs-lookup"><span data-stu-id="f83bb-110">The second command gets the SKU of an application gateway named ApplicationGateway01 and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="f83bb-111">參數</span><span class="sxs-lookup"><span data-stu-id="f83bb-111">PARAMETERS</span></span>

### <span data-ttu-id="f83bb-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f83bb-112">-ApplicationGateway</span></span>
<span data-ttu-id="f83bb-113">指定應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="f83bb-113">Specifies the application gateway object.</span></span>

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

### <span data-ttu-id="f83bb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f83bb-114">-DefaultProfile</span></span>
<span data-ttu-id="f83bb-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f83bb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f83bb-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f83bb-116">CommonParameters</span></span>
<span data-ttu-id="f83bb-117">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f83bb-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f83bb-118">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f83bb-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f83bb-119">輸入</span><span class="sxs-lookup"><span data-stu-id="f83bb-119">INPUTS</span></span>

### <span data-ttu-id="f83bb-120">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f83bb-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f83bb-121">輸出</span><span class="sxs-lookup"><span data-stu-id="f83bb-121">OUTPUTS</span></span>

### <span data-ttu-id="f83bb-122">Microsoft.Azure.Commands.Network.models.PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="f83bb-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="f83bb-123">筆記</span><span class="sxs-lookup"><span data-stu-id="f83bb-123">NOTES</span></span>

## <span data-ttu-id="f83bb-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="f83bb-124">RELATED LINKS</span></span>

[<span data-ttu-id="f83bb-125">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="f83bb-125">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="f83bb-126">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="f83bb-126">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


