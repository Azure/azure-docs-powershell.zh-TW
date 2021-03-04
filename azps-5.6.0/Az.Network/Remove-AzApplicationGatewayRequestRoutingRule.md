---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CC033DA8-FACC-44E2-82F9-E30FADBF8926
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: ac18c96353e247c721f95acf83e174e18a578b2c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911905"
---
# <span data-ttu-id="daf30-101">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="daf30-101">Remove-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="daf30-102">簡介</span><span class="sxs-lookup"><span data-stu-id="daf30-102">SYNOPSIS</span></span>
<span data-ttu-id="daf30-103">從應用程式閘道移除要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="daf30-103">Removes a request routing rule from an application gateway.</span></span>

## <span data-ttu-id="daf30-104">語法</span><span class="sxs-lookup"><span data-stu-id="daf30-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRequestRoutingRule -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="daf30-105">描述</span><span class="sxs-lookup"><span data-stu-id="daf30-105">DESCRIPTION</span></span>
<span data-ttu-id="daf30-106">**Remove-AzApplicationGatewayRequestRoutingRule** Cmdlet 會從 Azure 應用程式閘道移除要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="daf30-106">The **Remove-AzApplicationGatewayRequestRoutingRule** cmdlet removes a request routing rule from an Azure application gateway.</span></span>

## <span data-ttu-id="daf30-107">例子</span><span class="sxs-lookup"><span data-stu-id="daf30-107">EXAMPLES</span></span>

### <span data-ttu-id="daf30-108">範例 1：從應用程式閘道移除要求路由規則</span><span class="sxs-lookup"><span data-stu-id="daf30-108">Example 1: Remove a request routing rule from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule02"
```

<span data-ttu-id="daf30-109">第一個命令會獲得應用程式閘道，並儲存在$AppGw變數中。</span><span class="sxs-lookup"><span data-stu-id="daf30-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="daf30-110">第二個命令會從儲存在 $AppGw 的應用程式閘道移除名為 Rule02 的要求路由$AppGw。</span><span class="sxs-lookup"><span data-stu-id="daf30-110">The second command removes the request routing rule named Rule02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="daf30-111">參數</span><span class="sxs-lookup"><span data-stu-id="daf30-111">PARAMETERS</span></span>

### <span data-ttu-id="daf30-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="daf30-112">-ApplicationGateway</span></span>
<span data-ttu-id="daf30-113">指定要從中移除要求路由規則的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="daf30-113">Specifies the application gateway from which to remove a request routing rule.</span></span>

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

### <span data-ttu-id="daf30-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daf30-114">-DefaultProfile</span></span>
<span data-ttu-id="daf30-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="daf30-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="daf30-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="daf30-116">-Name</span></span>
<span data-ttu-id="daf30-117">指定此 Cmdlet 移除之要求路由規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="daf30-117">Specifies the name of the request routing rule for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="daf30-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daf30-118">CommonParameters</span></span>
<span data-ttu-id="daf30-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="daf30-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daf30-120">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="daf30-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daf30-121">輸入</span><span class="sxs-lookup"><span data-stu-id="daf30-121">INPUTS</span></span>

### <span data-ttu-id="daf30-122">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="daf30-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="daf30-123">輸出</span><span class="sxs-lookup"><span data-stu-id="daf30-123">OUTPUTS</span></span>

### <span data-ttu-id="daf30-124">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="daf30-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="daf30-125">筆記</span><span class="sxs-lookup"><span data-stu-id="daf30-125">NOTES</span></span>

## <span data-ttu-id="daf30-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="daf30-126">RELATED LINKS</span></span>

[<span data-ttu-id="daf30-127">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="daf30-127">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="daf30-128">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="daf30-128">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="daf30-129">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="daf30-129">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="daf30-130">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="daf30-130">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


