---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 919B3755-81D4-43FB-AE8C-B071329A61D9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: 990225622cc6aa72e78a3aa396ba333191469630
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623597"
---
# <span data-ttu-id="4874a-101">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4874a-101">Get-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="4874a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4874a-102">SYNOPSIS</span></span>
<span data-ttu-id="4874a-103">取得應用程式閘道的 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="4874a-103">Gets an SSL certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4874a-104">句法</span><span class="sxs-lookup"><span data-stu-id="4874a-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4874a-105">說明</span><span class="sxs-lookup"><span data-stu-id="4874a-105">DESCRIPTION</span></span>
<span data-ttu-id="4874a-106">**AzureRmApplicationGatewaySslCertificate** Cmdlet 會為應用程式閘道取得 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="4874a-106">The **Get-AzureRmApplicationGatewaySslCertificate** cmdlet gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="4874a-107">示例</span><span class="sxs-lookup"><span data-stu-id="4874a-107">EXAMPLES</span></span>

### <span data-ttu-id="4874a-108">範例1：取得特定的 SSL 憑證</span><span class="sxs-lookup"><span data-stu-id="4874a-108">Example 1: Get a specific SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Get-AzureRmApplicationGatewaySslCertificate -Name "Cert01" -ApplicationGateway $AppGW
```

<span data-ttu-id="4874a-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將結果儲存在名為 $AppGW 的變數中。</span><span class="sxs-lookup"><span data-stu-id="4874a-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="4874a-110">第二個命令會從儲存在名為 $AppGW 的變數中的應用程式閘道取得名為 Cert01 的 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="4874a-110">The second command gets the SSL certificate named Cert01 from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="4874a-111">該命令會將憑證儲存在名為 $Cert 的變數中。</span><span class="sxs-lookup"><span data-stu-id="4874a-111">The command stores the certificate in the variable named $Cert.</span></span>

### <span data-ttu-id="4874a-112">範例2：取得 SSL 憑證清單</span><span class="sxs-lookup"><span data-stu-id="4874a-112">Example 2: Get a list of SSL certificates</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Certs = Get-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW
```

<span data-ttu-id="4874a-113">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將結果儲存在名為 $AppGW 的變數中。</span><span class="sxs-lookup"><span data-stu-id="4874a-113">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="4874a-114">這個第二個命令會從儲存在名為 $AppGW 的變數中的應用程式閘道取得 SSL 憑證清單。</span><span class="sxs-lookup"><span data-stu-id="4874a-114">This second command gets a list of SSL certificates from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="4874a-115">然後，該命令會將結果儲存在名為 $Certs 的變數中。</span><span class="sxs-lookup"><span data-stu-id="4874a-115">The command then stores the results in the variable named $Certs.</span></span>

## <span data-ttu-id="4874a-116">參數</span><span class="sxs-lookup"><span data-stu-id="4874a-116">PARAMETERS</span></span>

### <span data-ttu-id="4874a-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4874a-117">-ApplicationGateway</span></span>
<span data-ttu-id="4874a-118">指定包含 SSL 憑證的應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="4874a-118">Specifies the application gateway object that contains the SSL certificate.</span></span>

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

### <span data-ttu-id="4874a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4874a-119">-DefaultProfile</span></span>
<span data-ttu-id="4874a-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4874a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4874a-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="4874a-121">-Name</span></span>
<span data-ttu-id="4874a-122">指定此 Cmdlet 所取得之 SSL 憑證池的名稱。</span><span class="sxs-lookup"><span data-stu-id="4874a-122">Specifies the name of SSL certificate pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4874a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4874a-123">CommonParameters</span></span>
<span data-ttu-id="4874a-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4874a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4874a-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4874a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4874a-126">輸入</span><span class="sxs-lookup"><span data-stu-id="4874a-126">INPUTS</span></span>

### <span data-ttu-id="4874a-127">System.object</span><span class="sxs-lookup"><span data-stu-id="4874a-127">System.String</span></span>

## <span data-ttu-id="4874a-128">輸出</span><span class="sxs-lookup"><span data-stu-id="4874a-128">OUTPUTS</span></span>

### <span data-ttu-id="4874a-129">PSApplicationGatewaySslCertificate 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4874a-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="4874a-130">筆記</span><span class="sxs-lookup"><span data-stu-id="4874a-130">NOTES</span></span>

## <span data-ttu-id="4874a-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="4874a-131">RELATED LINKS</span></span>

[<span data-ttu-id="4874a-132">附加 AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4874a-132">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="4874a-133">新-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4874a-133">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="4874a-134">移除-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4874a-134">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="4874a-135">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4874a-135">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)

