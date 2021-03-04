---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 919B3755-81D4-43FB-AE8C-B071329A61D9
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: aa6dbacb85263d8f0169f913c07e56a9dbd1c7ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912782"
---
# <span data-ttu-id="5ece4-101">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5ece4-101">Get-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="5ece4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5ece4-102">SYNOPSIS</span></span>
<span data-ttu-id="5ece4-103">獲得應用程式閘道的 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="5ece4-103">Gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="5ece4-104">語法</span><span class="sxs-lookup"><span data-stu-id="5ece4-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ece4-105">描述</span><span class="sxs-lookup"><span data-stu-id="5ece4-105">DESCRIPTION</span></span>
<span data-ttu-id="5ece4-106">**Get-AzApplicationGatewaySslCertificate** Cmdlet 會取得應用程式閘道的 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="5ece4-106">The **Get-AzApplicationGatewaySslCertificate** cmdlet gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="5ece4-107">例子</span><span class="sxs-lookup"><span data-stu-id="5ece4-107">EXAMPLES</span></span>

### <span data-ttu-id="5ece4-108">範例 1：取得特定的 SSL 憑證</span><span class="sxs-lookup"><span data-stu-id="5ece4-108">Example 1: Get a specific SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Get-AzApplicationGatewaySslCertificate -Name "Cert01" -ApplicationGateway $AppGW
```

<span data-ttu-id="5ece4-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並儲存在名為 applicationGateway01 的$AppGW。</span><span class="sxs-lookup"><span data-stu-id="5ece4-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="5ece4-110">第二個命令會從儲存在名為 Cert01 之變數的應用程式閘道中，獲得名為 Cert01 的 SSL 憑證$AppGW。</span><span class="sxs-lookup"><span data-stu-id="5ece4-110">The second command gets the SSL certificate named Cert01 from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="5ece4-111">該命令將憑證儲存在名為 $Cert 的變數中。</span><span class="sxs-lookup"><span data-stu-id="5ece4-111">The command stores the certificate in the variable named $Cert.</span></span>

### <span data-ttu-id="5ece4-112">範例 2：取得 SSL 憑證清單</span><span class="sxs-lookup"><span data-stu-id="5ece4-112">Example 2: Get a list of SSL certificates</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Certs = Get-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW
```

<span data-ttu-id="5ece4-113">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並儲存在名為 applicationGateway01 的$AppGW。</span><span class="sxs-lookup"><span data-stu-id="5ece4-113">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="5ece4-114">第二個命令會從儲存在名為 $AppGW 之變數的應用程式閘道中，獲得 SSL 憑證$AppGW。</span><span class="sxs-lookup"><span data-stu-id="5ece4-114">This second command gets a list of SSL certificates from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="5ece4-115">命令接著會將結果儲存在名為 $Certs 的變數中。</span><span class="sxs-lookup"><span data-stu-id="5ece4-115">The command then stores the results in the variable named $Certs.</span></span>

## <span data-ttu-id="5ece4-116">參數</span><span class="sxs-lookup"><span data-stu-id="5ece4-116">PARAMETERS</span></span>

### <span data-ttu-id="5ece4-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ece4-117">-ApplicationGateway</span></span>
<span data-ttu-id="5ece4-118">指定包含 SSL 憑證的應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="5ece4-118">Specifies the application gateway object that contains the SSL certificate.</span></span>

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

### <span data-ttu-id="5ece4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ece4-119">-DefaultProfile</span></span>
<span data-ttu-id="5ece4-120">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5ece4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ece4-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="5ece4-121">-Name</span></span>
<span data-ttu-id="5ece4-122">指定此 Cmdlet 所獲取的 SSL 憑證資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="5ece4-122">Specifies the name of SSL certificate pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5ece4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ece4-123">CommonParameters</span></span>
<span data-ttu-id="5ece4-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5ece4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ece4-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5ece4-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ece4-126">輸入</span><span class="sxs-lookup"><span data-stu-id="5ece4-126">INPUTS</span></span>

### <span data-ttu-id="5ece4-127">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ece4-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5ece4-128">輸出</span><span class="sxs-lookup"><span data-stu-id="5ece4-128">OUTPUTS</span></span>

### <span data-ttu-id="5ece4-129">Microsoft.Azure.Commands.Network.models.PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5ece4-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="5ece4-130">筆記</span><span class="sxs-lookup"><span data-stu-id="5ece4-130">NOTES</span></span>

## <span data-ttu-id="5ece4-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="5ece4-131">RELATED LINKS</span></span>

[<span data-ttu-id="5ece4-132">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5ece4-132">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="5ece4-133">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5ece4-133">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="5ece4-134">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5ece4-134">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="5ece4-135">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5ece4-135">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


