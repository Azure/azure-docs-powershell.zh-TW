---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4B2066B6-51D7-46D8-8A72-1A232B3E6589
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 6ca7bc3e5d1af477c7d6750f674272ff64d54889
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970945"
---
# <span data-ttu-id="7b8f5-101">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7b8f5-101">Get-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="7b8f5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7b8f5-102">SYNOPSIS</span></span>
<span data-ttu-id="7b8f5-103">取得應用程式閘道的後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="7b8f5-103">Gets a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="7b8f5-104">句法</span><span class="sxs-lookup"><span data-stu-id="7b8f5-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendAddressPool [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b8f5-105">說明</span><span class="sxs-lookup"><span data-stu-id="7b8f5-105">DESCRIPTION</span></span>
<span data-ttu-id="7b8f5-106">**AzApplicationGatewayBackendAddressPool** Cmdlet 會從應用程式閘道取得一或多個後端位址集區配置。</span><span class="sxs-lookup"><span data-stu-id="7b8f5-106">The **Get-AzApplicationGatewayBackendAddressPool** cmdlet gets one or more backend address pool configurations from an application gateway.</span></span>

## <span data-ttu-id="7b8f5-107">示例</span><span class="sxs-lookup"><span data-stu-id="7b8f5-107">EXAMPLES</span></span>

### <span data-ttu-id="7b8f5-108">範例1：取得指定的後端伺服器池</span><span class="sxs-lookup"><span data-stu-id="7b8f5-108">Example 1: Get a specified back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPool = Get-AzApplicationGatewayBackendAddressPool -Name "Pool01" -ApplicationGateway $AppGw
```

<span data-ttu-id="7b8f5-109">第一個命令會在名為 ResourceGroup01 的資源群組中，取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="7b8f5-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7b8f5-110">第二個命令會取得與名為 Pool01 $AppGw 相關聯的後端位址集區，並將它儲存在 $BackendPool 變數中。</span><span class="sxs-lookup"><span data-stu-id="7b8f5-110">The second command gets the back-end address pool associated with $AppGw named Pool01 and stores it in the $BackendPool variable.</span></span>

### <span data-ttu-id="7b8f5-111">範例2：取得後端伺服器池清單</span><span class="sxs-lookup"><span data-stu-id="7b8f5-111">Example 2: Get a list of back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPools = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw
```

<span data-ttu-id="7b8f5-112">第一個命令會在名為 ResourceGroup01 的資源群組中，取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="7b8f5-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7b8f5-113">第二個命令會取得與 $AppGw 相關聯的後端位址集區清單，並將清單儲存在 $BackendPools 變數中。</span><span class="sxs-lookup"><span data-stu-id="7b8f5-113">The second command gets a list of the back-end address pools associated with $AppGw, and stores the list in the $BackendPools variable.</span></span>

## <span data-ttu-id="7b8f5-114">參數</span><span class="sxs-lookup"><span data-stu-id="7b8f5-114">PARAMETERS</span></span>

### <span data-ttu-id="7b8f5-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7b8f5-115">-ApplicationGateway</span></span>
<span data-ttu-id="7b8f5-116">**AzApplicationGatewayBackendAddressPool** Cmdlet 會取得應用程式閘道的後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="7b8f5-116">The **Get-AzApplicationGatewayBackendAddressPool** cmdlet gets a back-end address pool for an application gateway.</span></span>

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

### <span data-ttu-id="7b8f5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b8f5-117">-DefaultProfile</span></span>
<span data-ttu-id="7b8f5-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7b8f5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b8f5-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="7b8f5-119">-Name</span></span>
<span data-ttu-id="7b8f5-120">指定此 Cmdlet 取得的後端位址集區名稱。</span><span class="sxs-lookup"><span data-stu-id="7b8f5-120">Specifies the name of the back-end address pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7b8f5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b8f5-121">CommonParameters</span></span>
<span data-ttu-id="7b8f5-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7b8f5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b8f5-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7b8f5-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b8f5-124">輸入</span><span class="sxs-lookup"><span data-stu-id="7b8f5-124">INPUTS</span></span>

### <span data-ttu-id="7b8f5-125">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7b8f5-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7b8f5-126">輸出</span><span class="sxs-lookup"><span data-stu-id="7b8f5-126">OUTPUTS</span></span>

### <span data-ttu-id="7b8f5-127">PSApplicationGatewayBackendAddressPool 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7b8f5-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="7b8f5-128">筆記</span><span class="sxs-lookup"><span data-stu-id="7b8f5-128">NOTES</span></span>

## <span data-ttu-id="7b8f5-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="7b8f5-129">RELATED LINKS</span></span>

[<span data-ttu-id="7b8f5-130">附加 AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7b8f5-130">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="7b8f5-131">新-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7b8f5-131">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="7b8f5-132">移除-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7b8f5-132">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="7b8f5-133">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7b8f5-133">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


