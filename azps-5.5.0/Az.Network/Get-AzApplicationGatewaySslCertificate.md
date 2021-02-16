---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 919B3755-81D4-43FB-AE8C-B071329A61D9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 3e7010309c6aed367e3771971a8b1c2841548fe0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100132642"
---
# <span data-ttu-id="bcbf1-101">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="bcbf1-101">Get-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="bcbf1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bcbf1-102">SYNOPSIS</span></span>
<span data-ttu-id="bcbf1-103">取得應用程式閘道的 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="bcbf1-103">Gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="bcbf1-104">句法</span><span class="sxs-lookup"><span data-stu-id="bcbf1-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bcbf1-105">說明</span><span class="sxs-lookup"><span data-stu-id="bcbf1-105">DESCRIPTION</span></span>
<span data-ttu-id="bcbf1-106">**AzApplicationGatewaySslCertificate** Cmdlet 會為應用程式閘道取得 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="bcbf1-106">The **Get-AzApplicationGatewaySslCertificate** cmdlet gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="bcbf1-107">示例</span><span class="sxs-lookup"><span data-stu-id="bcbf1-107">EXAMPLES</span></span>

### <span data-ttu-id="bcbf1-108">範例1：取得特定的 SSL 憑證</span><span class="sxs-lookup"><span data-stu-id="bcbf1-108">Example 1: Get a specific SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Get-AzApplicationGatewaySslCertificate -Name "Cert01" -ApplicationGateway $AppGW
```

<span data-ttu-id="bcbf1-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將結果儲存在名為 $AppGW 的變數中。</span><span class="sxs-lookup"><span data-stu-id="bcbf1-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="bcbf1-110">第二個命令會從儲存在名為 $AppGW 的變數中的應用程式閘道取得名為 Cert01 的 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="bcbf1-110">The second command gets the SSL certificate named Cert01 from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="bcbf1-111">該命令會將憑證儲存在名為 $Cert 的變數中。</span><span class="sxs-lookup"><span data-stu-id="bcbf1-111">The command stores the certificate in the variable named $Cert.</span></span>

### <span data-ttu-id="bcbf1-112">範例2：取得 SSL 憑證清單</span><span class="sxs-lookup"><span data-stu-id="bcbf1-112">Example 2: Get a list of SSL certificates</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Certs = Get-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW
```

<span data-ttu-id="bcbf1-113">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將結果儲存在名為 $AppGW 的變數中。</span><span class="sxs-lookup"><span data-stu-id="bcbf1-113">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="bcbf1-114">這個第二個命令會從儲存在名為 $AppGW 的變數中的應用程式閘道取得 SSL 憑證清單。</span><span class="sxs-lookup"><span data-stu-id="bcbf1-114">This second command gets a list of SSL certificates from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="bcbf1-115">然後，該命令會將結果儲存在名為 $Certs 的變數中。</span><span class="sxs-lookup"><span data-stu-id="bcbf1-115">The command then stores the results in the variable named $Certs.</span></span>

## <span data-ttu-id="bcbf1-116">參數</span><span class="sxs-lookup"><span data-stu-id="bcbf1-116">PARAMETERS</span></span>

### <span data-ttu-id="bcbf1-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bcbf1-117">-ApplicationGateway</span></span>
<span data-ttu-id="bcbf1-118">指定包含 SSL 憑證的應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="bcbf1-118">Specifies the application gateway object that contains the SSL certificate.</span></span>

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

### <span data-ttu-id="bcbf1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcbf1-119">-DefaultProfile</span></span>
<span data-ttu-id="bcbf1-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bcbf1-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcbf1-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="bcbf1-121">-Name</span></span>
<span data-ttu-id="bcbf1-122">指定此 Cmdlet 所取得之 SSL 憑證池的名稱。</span><span class="sxs-lookup"><span data-stu-id="bcbf1-122">Specifies the name of SSL certificate pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="bcbf1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcbf1-123">CommonParameters</span></span>
<span data-ttu-id="bcbf1-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bcbf1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcbf1-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bcbf1-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcbf1-126">輸入</span><span class="sxs-lookup"><span data-stu-id="bcbf1-126">INPUTS</span></span>

### <span data-ttu-id="bcbf1-127">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bcbf1-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bcbf1-128">輸出</span><span class="sxs-lookup"><span data-stu-id="bcbf1-128">OUTPUTS</span></span>

### <span data-ttu-id="bcbf1-129">PSApplicationGatewaySslCertificate 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bcbf1-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="bcbf1-130">筆記</span><span class="sxs-lookup"><span data-stu-id="bcbf1-130">NOTES</span></span>

## <span data-ttu-id="bcbf1-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="bcbf1-131">RELATED LINKS</span></span>

[<span data-ttu-id="bcbf1-132">附加 AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="bcbf1-132">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="bcbf1-133">新-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="bcbf1-133">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="bcbf1-134">移除-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="bcbf1-134">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="bcbf1-135">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="bcbf1-135">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


