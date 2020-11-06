---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 919B3755-81D4-43FB-AE8C-B071329A61D9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: e957ef203d0bf90393e523cca41b949a9d99acc5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452795"
---
# <span data-ttu-id="815a6-101">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="815a6-101">Get-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="815a6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="815a6-102">SYNOPSIS</span></span>
<span data-ttu-id="815a6-103">取得應用程式閘道的 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="815a6-103">Gets an SSL certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="815a6-104">句法</span><span class="sxs-lookup"><span data-stu-id="815a6-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="815a6-105">說明</span><span class="sxs-lookup"><span data-stu-id="815a6-105">DESCRIPTION</span></span>
<span data-ttu-id="815a6-106">**AzureRmApplicationGatewaySslCertificate** Cmdlet 會為應用程式閘道取得 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="815a6-106">The **Get-AzureRmApplicationGatewaySslCertificate** cmdlet gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="815a6-107">示例</span><span class="sxs-lookup"><span data-stu-id="815a6-107">EXAMPLES</span></span>

### <span data-ttu-id="815a6-108">範例1：取得特定的 SSL 憑證</span><span class="sxs-lookup"><span data-stu-id="815a6-108">Example 1: Get a specific SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Get-AzureRmApplicationGatewaySslCertificate -Name "Cert01" -ApplicationGateway $AppGW
```

<span data-ttu-id="815a6-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將結果儲存在名為 $AppGW 的變數中。</span><span class="sxs-lookup"><span data-stu-id="815a6-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="815a6-110">第二個命令會從儲存在名為 $AppGW 的變數中的應用程式閘道取得名為 Cert01 的 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="815a6-110">The second command gets the SSL certificate named Cert01 from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="815a6-111">該命令會將憑證儲存在名為 $Cert 的變數中。</span><span class="sxs-lookup"><span data-stu-id="815a6-111">The command stores the certificate in the variable named $Cert.</span></span>

### <span data-ttu-id="815a6-112">範例2：取得 SSL 憑證清單</span><span class="sxs-lookup"><span data-stu-id="815a6-112">Example 2: Get a list of SSL certificates</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Certs = Get-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW
```

<span data-ttu-id="815a6-113">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將結果儲存在名為 $AppGW 的變數中。</span><span class="sxs-lookup"><span data-stu-id="815a6-113">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="815a6-114">這個第二個命令會從儲存在名為 $AppGW 的變數中的應用程式閘道取得 SSL 憑證清單。</span><span class="sxs-lookup"><span data-stu-id="815a6-114">This second command gets a list of SSL certificates from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="815a6-115">然後，該命令會將結果儲存在名為 $Certs 的變數中。</span><span class="sxs-lookup"><span data-stu-id="815a6-115">The command then stores the results in the variable named $Certs.</span></span>

## <span data-ttu-id="815a6-116">參數</span><span class="sxs-lookup"><span data-stu-id="815a6-116">PARAMETERS</span></span>

### <span data-ttu-id="815a6-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="815a6-117">-ApplicationGateway</span></span>
<span data-ttu-id="815a6-118">指定包含 SSL 憑證的應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="815a6-118">Specifies the application gateway object that contains the SSL certificate.</span></span>

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

### <span data-ttu-id="815a6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="815a6-119">-DefaultProfile</span></span>
<span data-ttu-id="815a6-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="815a6-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="815a6-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="815a6-121">-Name</span></span>
<span data-ttu-id="815a6-122">指定此 Cmdlet 所取得之 SSL 憑證池的名稱。</span><span class="sxs-lookup"><span data-stu-id="815a6-122">Specifies the name of SSL certificate pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="815a6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="815a6-123">CommonParameters</span></span>
<span data-ttu-id="815a6-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="815a6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="815a6-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="815a6-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="815a6-126">輸入</span><span class="sxs-lookup"><span data-stu-id="815a6-126">INPUTS</span></span>

### <span data-ttu-id="815a6-127">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="815a6-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="815a6-128">參數： ApplicationGateway (ByValue) </span><span class="sxs-lookup"><span data-stu-id="815a6-128">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="815a6-129">輸出</span><span class="sxs-lookup"><span data-stu-id="815a6-129">OUTPUTS</span></span>

### <span data-ttu-id="815a6-130">PSApplicationGatewaySslCertificate 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="815a6-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="815a6-131">筆記</span><span class="sxs-lookup"><span data-stu-id="815a6-131">NOTES</span></span>

## <span data-ttu-id="815a6-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="815a6-132">RELATED LINKS</span></span>

[<span data-ttu-id="815a6-133">附加 AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="815a6-133">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="815a6-134">新-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="815a6-134">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="815a6-135">移除-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="815a6-135">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="815a6-136">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="815a6-136">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


