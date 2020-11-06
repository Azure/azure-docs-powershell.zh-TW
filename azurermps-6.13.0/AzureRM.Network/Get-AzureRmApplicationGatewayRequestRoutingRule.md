---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 57A6DB40-43EC-402C-9784-06817ECD99B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 7a6d8bef710ddf41f805c6ced558e12781a23276
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452800"
---
# <span data-ttu-id="4365b-101">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4365b-101">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="4365b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4365b-102">SYNOPSIS</span></span>
<span data-ttu-id="4365b-103">取得應用程式閘道的要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="4365b-103">Gets the request routing rule of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4365b-104">句法</span><span class="sxs-lookup"><span data-stu-id="4365b-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayRequestRoutingRule [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4365b-105">說明</span><span class="sxs-lookup"><span data-stu-id="4365b-105">DESCRIPTION</span></span>
<span data-ttu-id="4365b-106">**AzureRmApplicationGatewayRequestRoutingRule** Cmdlet 會取得應用程式閘道的要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="4365b-106">The **Get-AzureRmApplicationGatewayRequestRoutingRule** cmdlet gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="4365b-107">示例</span><span class="sxs-lookup"><span data-stu-id="4365b-107">EXAMPLES</span></span>

### <span data-ttu-id="4365b-108">範例1：取得特定的要求路由規則</span><span class="sxs-lookup"><span data-stu-id="4365b-108">Example 1: Get a specific request routing rule</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzureRmApplicationGatewayRequestRoutingRule -"Rule01" -ApplicationGateway $AppGW
```

<span data-ttu-id="4365b-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將結果儲存在名為 $AppGW 的變數中。</span><span class="sxs-lookup"><span data-stu-id="4365b-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="4365b-110">第二個命令會從儲存在名為 $AppGW 的變數中，從應用程式閘道取得名為 Rule01 的要求路由規則。</span><span class="sxs-lookup"><span data-stu-id="4365b-110">The second command gets the request routing rule named Rule01 from the Application Gateway stored in the variable named $AppGW.</span></span>

### <span data-ttu-id="4365b-111">範例2：取得要求路由規則清單</span><span class="sxs-lookup"><span data-stu-id="4365b-111">Example 2: Get a list of request routing rules</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rules = Get-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGW
```

<span data-ttu-id="4365b-112">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將結果儲存在名為 $AppGW 的變數中。</span><span class="sxs-lookup"><span data-stu-id="4365b-112">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="4365b-113">第二個命令會從儲存在名為 $AppGW 的變數中的應用程式閘道取得要求路由規則清單。</span><span class="sxs-lookup"><span data-stu-id="4365b-113">The second command gets a list of request routing rules from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="4365b-114">參數</span><span class="sxs-lookup"><span data-stu-id="4365b-114">PARAMETERS</span></span>

### <span data-ttu-id="4365b-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4365b-115">-ApplicationGateway</span></span>
<span data-ttu-id="4365b-116">指定包含要求路由規則的應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="4365b-116">Specifies the application gateway object that contains request routing rule.</span></span>

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

### <span data-ttu-id="4365b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4365b-117">-DefaultProfile</span></span>
<span data-ttu-id="4365b-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4365b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4365b-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="4365b-119">-Name</span></span>
<span data-ttu-id="4365b-120">指定此 Cmdlet 取得的要求路由規則名稱。</span><span class="sxs-lookup"><span data-stu-id="4365b-120">Specifies the name of the request routing rule which this cmdlet gets.</span></span>

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

### <span data-ttu-id="4365b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4365b-121">CommonParameters</span></span>
<span data-ttu-id="4365b-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4365b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4365b-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4365b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4365b-124">輸入</span><span class="sxs-lookup"><span data-stu-id="4365b-124">INPUTS</span></span>

### <span data-ttu-id="4365b-125">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4365b-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="4365b-126">參數： ApplicationGateway (ByValue) </span><span class="sxs-lookup"><span data-stu-id="4365b-126">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="4365b-127">輸出</span><span class="sxs-lookup"><span data-stu-id="4365b-127">OUTPUTS</span></span>

### <span data-ttu-id="4365b-128">PSApplicationGatewayRequestRoutingRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4365b-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="4365b-129">筆記</span><span class="sxs-lookup"><span data-stu-id="4365b-129">NOTES</span></span>

## <span data-ttu-id="4365b-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="4365b-130">RELATED LINKS</span></span>

[<span data-ttu-id="4365b-131">附加 AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4365b-131">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="4365b-132">新-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4365b-132">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="4365b-133">移除-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4365b-133">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="4365b-134">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4365b-134">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


