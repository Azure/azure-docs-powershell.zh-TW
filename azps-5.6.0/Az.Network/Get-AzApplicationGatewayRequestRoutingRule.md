---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 57A6DB40-43EC-402C-9784-06817ECD99B8
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 04c7ef7dd041ce26802f23117edab79353816283
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912789"
---
# <span data-ttu-id="d26dd-101">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d26dd-101">Get-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="d26dd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d26dd-102">SYNOPSIS</span></span>
<span data-ttu-id="d26dd-103">獲得應用程式閘道的要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="d26dd-103">Gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="d26dd-104">語法</span><span class="sxs-lookup"><span data-stu-id="d26dd-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRequestRoutingRule [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d26dd-105">描述</span><span class="sxs-lookup"><span data-stu-id="d26dd-105">DESCRIPTION</span></span>
<span data-ttu-id="d26dd-106">**Get-AzApplicationGatewayRequestRoutingRule** Cmdlet 會取得應用程式閘道的要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="d26dd-106">The **Get-AzApplicationGatewayRequestRoutingRule** cmdlet gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="d26dd-107">例子</span><span class="sxs-lookup"><span data-stu-id="d26dd-107">EXAMPLES</span></span>

### <span data-ttu-id="d26dd-108">範例 1：取得特定要求路由規則</span><span class="sxs-lookup"><span data-stu-id="d26dd-108">Example 1: Get a specific request routing rule</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRequestRoutingRule -"Rule01" -ApplicationGateway $AppGW
```

<span data-ttu-id="d26dd-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並儲存在名為 applicationGateway01 的$AppGW。</span><span class="sxs-lookup"><span data-stu-id="d26dd-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="d26dd-110">第二個命令會從儲存在$AppGW變數的應用程式閘道中，獲得名為 Rule01 的要求路由$AppGW。</span><span class="sxs-lookup"><span data-stu-id="d26dd-110">The second command gets the request routing rule named Rule01 from the Application Gateway stored in the variable named $AppGW.</span></span>

### <span data-ttu-id="d26dd-111">範例 2：取得要求路由規則清單</span><span class="sxs-lookup"><span data-stu-id="d26dd-111">Example 2: Get a list of request routing rules</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rules = Get-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGW
```

<span data-ttu-id="d26dd-112">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並儲存在名為 applicationGateway01 的$AppGW。</span><span class="sxs-lookup"><span data-stu-id="d26dd-112">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="d26dd-113">第二個命令會從儲存在名為 $AppGW 的變數中的應用程式閘道中，獲得要求路由規則$AppGW。</span><span class="sxs-lookup"><span data-stu-id="d26dd-113">The second command gets a list of request routing rules from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="d26dd-114">參數</span><span class="sxs-lookup"><span data-stu-id="d26dd-114">PARAMETERS</span></span>

### <span data-ttu-id="d26dd-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d26dd-115">-ApplicationGateway</span></span>
<span data-ttu-id="d26dd-116">指定包含要求路由規則的應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="d26dd-116">Specifies the application gateway object that contains request routing rule.</span></span>

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

### <span data-ttu-id="d26dd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d26dd-117">-DefaultProfile</span></span>
<span data-ttu-id="d26dd-118">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d26dd-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d26dd-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="d26dd-119">-Name</span></span>
<span data-ttu-id="d26dd-120">指定此 Cmdlet 所獲得之要求路由規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="d26dd-120">Specifies the name of the request routing rule which this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d26dd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d26dd-121">CommonParameters</span></span>
<span data-ttu-id="d26dd-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d26dd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d26dd-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d26dd-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d26dd-124">輸入</span><span class="sxs-lookup"><span data-stu-id="d26dd-124">INPUTS</span></span>

### <span data-ttu-id="d26dd-125">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d26dd-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d26dd-126">輸出</span><span class="sxs-lookup"><span data-stu-id="d26dd-126">OUTPUTS</span></span>

### <span data-ttu-id="d26dd-127">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d26dd-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="d26dd-128">筆記</span><span class="sxs-lookup"><span data-stu-id="d26dd-128">NOTES</span></span>

## <span data-ttu-id="d26dd-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="d26dd-129">RELATED LINKS</span></span>

[<span data-ttu-id="d26dd-130">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d26dd-130">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="d26dd-131">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d26dd-131">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="d26dd-132">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d26dd-132">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="d26dd-133">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d26dd-133">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


