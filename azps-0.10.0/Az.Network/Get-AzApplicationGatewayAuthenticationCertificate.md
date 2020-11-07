---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 465567242c0ff13ea695c767cf1dda7f04f54174
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794484"
---
# <span data-ttu-id="3d687-101">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="3d687-101">Get-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="3d687-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3d687-102">SYNOPSIS</span></span>
<span data-ttu-id="3d687-103">取得應用程式閘道的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="3d687-103">Gets an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="3d687-104">句法</span><span class="sxs-lookup"><span data-stu-id="3d687-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAuthenticationCertificate [-Name <String>]
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d687-105">說明</span><span class="sxs-lookup"><span data-stu-id="3d687-105">DESCRIPTION</span></span>
<span data-ttu-id="3d687-106">**AzApplicationGatewayAuthenticationCertificate** Cmdlet 會取得 Azure 應用程式閘道的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="3d687-106">The **Get-AzApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="3d687-107">示例</span><span class="sxs-lookup"><span data-stu-id="3d687-107">EXAMPLES</span></span>

### <span data-ttu-id="3d687-108">sr-1</span><span class="sxs-lookup"><span data-stu-id="3d687-108">1:</span></span>
```

```

## <span data-ttu-id="3d687-109">參數</span><span class="sxs-lookup"><span data-stu-id="3d687-109">PARAMETERS</span></span>

### <span data-ttu-id="3d687-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3d687-110">-ApplicationGateway</span></span>
<span data-ttu-id="3d687-111">指定此 Cmdlet 取得其驗證憑證之應用程式閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d687-111">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="3d687-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d687-112">-DefaultProfile</span></span>
<span data-ttu-id="3d687-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3d687-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d687-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="3d687-114">-Name</span></span>
<span data-ttu-id="3d687-115">指定此 Cmdlet 所取得之驗證憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d687-115">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3d687-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d687-116">CommonParameters</span></span>
<span data-ttu-id="3d687-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3d687-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d687-118">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3d687-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d687-119">輸入</span><span class="sxs-lookup"><span data-stu-id="3d687-119">INPUTS</span></span>

### <span data-ttu-id="3d687-120">System.object</span><span class="sxs-lookup"><span data-stu-id="3d687-120">System.String</span></span>

## <span data-ttu-id="3d687-121">輸出</span><span class="sxs-lookup"><span data-stu-id="3d687-121">OUTPUTS</span></span>

### <span data-ttu-id="3d687-122">PSApplicationGatewayAuthenticationCertificate 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3d687-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="3d687-123">筆記</span><span class="sxs-lookup"><span data-stu-id="3d687-123">NOTES</span></span>
* <span data-ttu-id="3d687-124">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="3d687-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="3d687-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="3d687-125">RELATED LINKS</span></span>

[<span data-ttu-id="3d687-126">附加 AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="3d687-126">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="3d687-127">新-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="3d687-127">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="3d687-128">移除-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="3d687-128">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="3d687-129">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="3d687-129">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


