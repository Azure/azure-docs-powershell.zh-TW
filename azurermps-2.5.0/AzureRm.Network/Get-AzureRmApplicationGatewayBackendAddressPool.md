---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4B2066B6-51D7-46D8-8A72-1A232B3E6589
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
ms.openlocfilehash: 4ce1f2d1c388b531ee960688ba8296ef1632ac25
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800901"
---
# <span data-ttu-id="49851-101">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="49851-101">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="49851-102">摘要</span><span class="sxs-lookup"><span data-stu-id="49851-102">SYNOPSIS</span></span>
<span data-ttu-id="49851-103">取得應用程式閘道的後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="49851-103">Gets a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49851-104">句法</span><span class="sxs-lookup"><span data-stu-id="49851-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayBackendAddressPool [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49851-105">說明</span><span class="sxs-lookup"><span data-stu-id="49851-105">DESCRIPTION</span></span>

## <span data-ttu-id="49851-106">示例</span><span class="sxs-lookup"><span data-stu-id="49851-106">EXAMPLES</span></span>

### <span data-ttu-id="49851-107">範例1：取得指定的後端伺服器池</span><span class="sxs-lookup"><span data-stu-id="49851-107">Example 1: Get a specified back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPool = Get-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -ApplicationGateway $AppGw
```

<span data-ttu-id="49851-108">第一個命令會在名為 ResourceGroup01 的資源群組中，取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="49851-108">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="49851-109">第二個命令會取得與名為 Pool01 $AppGw 相關聯的後端位址集區，並將它儲存在 $BackendPool 變數中。</span><span class="sxs-lookup"><span data-stu-id="49851-109">The second command gets the back-end address pool associated with $AppGw named Pool01 and stores it in the $BackendPool variable.</span></span>

### <span data-ttu-id="49851-110">範例2：取得後端伺服器池清單</span><span class="sxs-lookup"><span data-stu-id="49851-110">Example 2: Get a list of back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPools = Get-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw
```

<span data-ttu-id="49851-111">第一個命令會在名為 ResourceGroup01 的資源群組中，取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="49851-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="49851-112">第二個命令會取得與 $AppGw 相關聯的後端位址集區清單，並將清單儲存在 $BackendPools 變數中。</span><span class="sxs-lookup"><span data-stu-id="49851-112">The second command gets a list of the back-end address pools associated with $AppGw, and stores the list in the $BackendPools variable.</span></span>

## <span data-ttu-id="49851-113">參數</span><span class="sxs-lookup"><span data-stu-id="49851-113">PARAMETERS</span></span>

### <span data-ttu-id="49851-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="49851-114">-ApplicationGateway</span></span>
<span data-ttu-id="49851-115">**AzureRmApplicationGatewayBackendAddressPool** Cmdlet 會取得應用程式閘道的後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="49851-115">The **Get-AzureRmApplicationGatewayBackendAddressPool** cmdlet gets a back-end address pool for an application gateway.</span></span>

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

### <span data-ttu-id="49851-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49851-116">-DefaultProfile</span></span>
<span data-ttu-id="49851-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="49851-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49851-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="49851-118">-Name</span></span>
<span data-ttu-id="49851-119">指定此 Cmdlet 取得的後端位址集區名稱。</span><span class="sxs-lookup"><span data-stu-id="49851-119">Specifies the name of the back-end address pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="49851-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49851-120">CommonParameters</span></span>
<span data-ttu-id="49851-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="49851-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49851-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="49851-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49851-123">輸入</span><span class="sxs-lookup"><span data-stu-id="49851-123">INPUTS</span></span>

### <span data-ttu-id="49851-124">System.object</span><span class="sxs-lookup"><span data-stu-id="49851-124">System.String</span></span>

## <span data-ttu-id="49851-125">輸出</span><span class="sxs-lookup"><span data-stu-id="49851-125">OUTPUTS</span></span>

### <span data-ttu-id="49851-126">PSApplicationGatewayBackendAddressPool 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="49851-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="49851-127">筆記</span><span class="sxs-lookup"><span data-stu-id="49851-127">NOTES</span></span>

## <span data-ttu-id="49851-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="49851-128">RELATED LINKS</span></span>

[<span data-ttu-id="49851-129">附加 AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="49851-129">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="49851-130">新-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="49851-130">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="49851-131">移除-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="49851-131">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="49851-132">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="49851-132">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


