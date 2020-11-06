---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CC033DA8-FACC-44E2-82F9-E30FADBF8926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: a4c1710ebbdfad1afb428bb09cccf27865c5e56e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448333"
---
# <span data-ttu-id="e6301-101">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e6301-101">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="e6301-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e6301-102">SYNOPSIS</span></span>
<span data-ttu-id="e6301-103">從應用程式閘道移除要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="e6301-103">Removes a request routing rule from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6301-104">句法</span><span class="sxs-lookup"><span data-stu-id="e6301-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6301-105">說明</span><span class="sxs-lookup"><span data-stu-id="e6301-105">DESCRIPTION</span></span>
<span data-ttu-id="e6301-106">**AzureRmApplicationGatewayRequestRoutingRule** Cmdlet 會從 Azure 應用程式閘道移除要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="e6301-106">The **Remove-AzureRmApplicationGatewayRequestRoutingRule** cmdlet removes a request routing rule from an Azure application gateway.</span></span>

## <span data-ttu-id="e6301-107">示例</span><span class="sxs-lookup"><span data-stu-id="e6301-107">EXAMPLES</span></span>

### <span data-ttu-id="e6301-108">範例1：從應用程式閘道移除要求路由規則</span><span class="sxs-lookup"><span data-stu-id="e6301-108">Example 1: Remove a request routing rule from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule02"
```

<span data-ttu-id="e6301-109">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="e6301-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e6301-110">第二個命令會從 $AppGw 中儲存的應用程式閘道，移除名為 Rule02 的要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="e6301-110">The second command removes the request routing rule named Rule02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="e6301-111">參數</span><span class="sxs-lookup"><span data-stu-id="e6301-111">PARAMETERS</span></span>

### <span data-ttu-id="e6301-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e6301-112">-ApplicationGateway</span></span>
<span data-ttu-id="e6301-113">指定要移除要求路由規則的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="e6301-113">Specifies the application gateway from which to remove a request routing rule.</span></span>

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

### <span data-ttu-id="e6301-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6301-114">-DefaultProfile</span></span>
<span data-ttu-id="e6301-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e6301-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6301-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="e6301-116">-Name</span></span>
<span data-ttu-id="e6301-117">指定此 Cmdlet 移除之要求路由規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="e6301-117">Specifies the name of the request routing rule for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="e6301-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6301-118">CommonParameters</span></span>
<span data-ttu-id="e6301-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e6301-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6301-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e6301-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6301-121">輸入</span><span class="sxs-lookup"><span data-stu-id="e6301-121">INPUTS</span></span>

### <span data-ttu-id="e6301-122">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e6301-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="e6301-123">參數： ApplicationGateway (ByValue) </span><span class="sxs-lookup"><span data-stu-id="e6301-123">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="e6301-124">輸出</span><span class="sxs-lookup"><span data-stu-id="e6301-124">OUTPUTS</span></span>

### <span data-ttu-id="e6301-125">PSApplicationGatewayRequestRoutingRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e6301-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="e6301-126">筆記</span><span class="sxs-lookup"><span data-stu-id="e6301-126">NOTES</span></span>

## <span data-ttu-id="e6301-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="e6301-127">RELATED LINKS</span></span>

[<span data-ttu-id="e6301-128">附加 AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e6301-128">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="e6301-129">AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e6301-129">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="e6301-130">新-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e6301-130">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="e6301-131">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e6301-131">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


