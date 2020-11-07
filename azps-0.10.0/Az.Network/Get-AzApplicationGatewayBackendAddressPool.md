---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4B2066B6-51D7-46D8-8A72-1A232B3E6589
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: b10863cf5e4af09ded0e98dbed76aff37dc48677
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794481"
---
# <span data-ttu-id="e2723-101">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e2723-101">Get-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="e2723-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e2723-102">SYNOPSIS</span></span>
<span data-ttu-id="e2723-103">取得應用程式閘道的後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="e2723-103">Gets a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="e2723-104">句法</span><span class="sxs-lookup"><span data-stu-id="e2723-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendAddressPool [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2723-105">說明</span><span class="sxs-lookup"><span data-stu-id="e2723-105">DESCRIPTION</span></span>

## <span data-ttu-id="e2723-106">示例</span><span class="sxs-lookup"><span data-stu-id="e2723-106">EXAMPLES</span></span>

### <span data-ttu-id="e2723-107">範例1：取得指定的後端伺服器池</span><span class="sxs-lookup"><span data-stu-id="e2723-107">Example 1: Get a specified back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPool = Get-AzApplicationGatewayBackendAddressPool -Name "Pool01" -ApplicationGateway $AppGw
```

<span data-ttu-id="e2723-108">第一個命令會在名為 ResourceGroup01 的資源群組中，取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="e2723-108">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e2723-109">第二個命令會取得與名為 Pool01 $AppGw 相關聯的後端位址集區，並將它儲存在 $BackendPool 變數中。</span><span class="sxs-lookup"><span data-stu-id="e2723-109">The second command gets the back-end address pool associated with $AppGw named Pool01 and stores it in the $BackendPool variable.</span></span>

### <span data-ttu-id="e2723-110">範例2：取得後端伺服器池清單</span><span class="sxs-lookup"><span data-stu-id="e2723-110">Example 2: Get a list of back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPools = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw
```

<span data-ttu-id="e2723-111">第一個命令會在名為 ResourceGroup01 的資源群組中，取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="e2723-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e2723-112">第二個命令會取得與 $AppGw 相關聯的後端位址集區清單，並將清單儲存在 $BackendPools 變數中。</span><span class="sxs-lookup"><span data-stu-id="e2723-112">The second command gets a list of the back-end address pools associated with $AppGw, and stores the list in the $BackendPools variable.</span></span>

## <span data-ttu-id="e2723-113">參數</span><span class="sxs-lookup"><span data-stu-id="e2723-113">PARAMETERS</span></span>

### <span data-ttu-id="e2723-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e2723-114">-ApplicationGateway</span></span>
<span data-ttu-id="e2723-115">**AzApplicationGatewayBackendAddressPool** Cmdlet 會取得應用程式閘道的後端位址集區。</span><span class="sxs-lookup"><span data-stu-id="e2723-115">The **Get-AzApplicationGatewayBackendAddressPool** cmdlet gets a back-end address pool for an application gateway.</span></span>

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

### <span data-ttu-id="e2723-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2723-116">-DefaultProfile</span></span>
<span data-ttu-id="e2723-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e2723-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2723-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="e2723-118">-Name</span></span>
<span data-ttu-id="e2723-119">指定此 Cmdlet 取得的後端位址集區名稱。</span><span class="sxs-lookup"><span data-stu-id="e2723-119">Specifies the name of the back-end address pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e2723-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2723-120">CommonParameters</span></span>
<span data-ttu-id="e2723-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e2723-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2723-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e2723-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2723-123">輸入</span><span class="sxs-lookup"><span data-stu-id="e2723-123">INPUTS</span></span>

### <span data-ttu-id="e2723-124">System.object</span><span class="sxs-lookup"><span data-stu-id="e2723-124">System.String</span></span>

## <span data-ttu-id="e2723-125">輸出</span><span class="sxs-lookup"><span data-stu-id="e2723-125">OUTPUTS</span></span>

### <span data-ttu-id="e2723-126">PSApplicationGatewayBackendAddressPool 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e2723-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="e2723-127">筆記</span><span class="sxs-lookup"><span data-stu-id="e2723-127">NOTES</span></span>

## <span data-ttu-id="e2723-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="e2723-128">RELATED LINKS</span></span>

[<span data-ttu-id="e2723-129">附加 AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e2723-129">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="e2723-130">新-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e2723-130">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="e2723-131">移除-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e2723-131">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="e2723-132">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e2723-132">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


