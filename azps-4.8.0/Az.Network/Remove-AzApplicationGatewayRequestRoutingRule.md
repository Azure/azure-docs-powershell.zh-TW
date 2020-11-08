---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CC033DA8-FACC-44E2-82F9-E30FADBF8926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: c1c630c39039d39b1957ccab78bb96d8f085176c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970327"
---
# <span data-ttu-id="23486-101">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="23486-101">Remove-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="23486-102">摘要</span><span class="sxs-lookup"><span data-stu-id="23486-102">SYNOPSIS</span></span>
<span data-ttu-id="23486-103">從應用程式閘道移除要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="23486-103">Removes a request routing rule from an application gateway.</span></span>

## <span data-ttu-id="23486-104">句法</span><span class="sxs-lookup"><span data-stu-id="23486-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRequestRoutingRule -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23486-105">說明</span><span class="sxs-lookup"><span data-stu-id="23486-105">DESCRIPTION</span></span>
<span data-ttu-id="23486-106">**AzApplicationGatewayRequestRoutingRule** Cmdlet 會從 Azure 應用程式閘道移除要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="23486-106">The **Remove-AzApplicationGatewayRequestRoutingRule** cmdlet removes a request routing rule from an Azure application gateway.</span></span>

## <span data-ttu-id="23486-107">示例</span><span class="sxs-lookup"><span data-stu-id="23486-107">EXAMPLES</span></span>

### <span data-ttu-id="23486-108">範例1：從應用程式閘道移除要求路由規則</span><span class="sxs-lookup"><span data-stu-id="23486-108">Example 1: Remove a request routing rule from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule02"
```

<span data-ttu-id="23486-109">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="23486-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="23486-110">第二個命令會從 $AppGw 中儲存的應用程式閘道，移除名為 Rule02 的要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="23486-110">The second command removes the request routing rule named Rule02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="23486-111">參數</span><span class="sxs-lookup"><span data-stu-id="23486-111">PARAMETERS</span></span>

### <span data-ttu-id="23486-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="23486-112">-ApplicationGateway</span></span>
<span data-ttu-id="23486-113">指定要移除要求路由規則的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="23486-113">Specifies the application gateway from which to remove a request routing rule.</span></span>

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

### <span data-ttu-id="23486-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23486-114">-DefaultProfile</span></span>
<span data-ttu-id="23486-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="23486-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23486-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="23486-116">-Name</span></span>
<span data-ttu-id="23486-117">指定此 Cmdlet 移除之要求路由規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="23486-117">Specifies the name of the request routing rule for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="23486-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23486-118">CommonParameters</span></span>
<span data-ttu-id="23486-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="23486-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23486-120">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="23486-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23486-121">輸入</span><span class="sxs-lookup"><span data-stu-id="23486-121">INPUTS</span></span>

### <span data-ttu-id="23486-122">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="23486-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="23486-123">輸出</span><span class="sxs-lookup"><span data-stu-id="23486-123">OUTPUTS</span></span>

### <span data-ttu-id="23486-124">PSApplicationGatewayRequestRoutingRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="23486-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="23486-125">筆記</span><span class="sxs-lookup"><span data-stu-id="23486-125">NOTES</span></span>

## <span data-ttu-id="23486-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="23486-126">RELATED LINKS</span></span>

[<span data-ttu-id="23486-127">附加 AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="23486-127">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="23486-128">AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="23486-128">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="23486-129">新-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="23486-129">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="23486-130">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="23486-130">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


