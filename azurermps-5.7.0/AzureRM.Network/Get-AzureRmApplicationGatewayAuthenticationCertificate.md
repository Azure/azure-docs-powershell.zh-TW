---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: bec9d197d039ea3934607ee291bdd6511ae6f4a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451432"
---
# <span data-ttu-id="f29ad-101">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f29ad-101">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="f29ad-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f29ad-102">SYNOPSIS</span></span>
<span data-ttu-id="f29ad-103">取得應用程式閘道的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="f29ad-103">Gets an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f29ad-104">句法</span><span class="sxs-lookup"><span data-stu-id="f29ad-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAuthenticationCertificate [-Name <String>]
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f29ad-105">說明</span><span class="sxs-lookup"><span data-stu-id="f29ad-105">DESCRIPTION</span></span>
<span data-ttu-id="f29ad-106">**AzureRmApplicationGatewayAuthenticationCertificate** Cmdlet 會取得 Azure 應用程式閘道的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="f29ad-106">The **Get-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="f29ad-107">示例</span><span class="sxs-lookup"><span data-stu-id="f29ad-107">EXAMPLES</span></span>

## <span data-ttu-id="f29ad-108">參數</span><span class="sxs-lookup"><span data-stu-id="f29ad-108">PARAMETERS</span></span>

### <span data-ttu-id="f29ad-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f29ad-109">-ApplicationGateway</span></span>
<span data-ttu-id="f29ad-110">指定此 Cmdlet 取得其驗證憑證之應用程式閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="f29ad-110">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="f29ad-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f29ad-111">-DefaultProfile</span></span>
<span data-ttu-id="f29ad-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f29ad-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f29ad-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="f29ad-113">-Name</span></span>
<span data-ttu-id="f29ad-114">指定此 Cmdlet 所取得之驗證憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="f29ad-114">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f29ad-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f29ad-115">CommonParameters</span></span>
<span data-ttu-id="f29ad-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f29ad-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f29ad-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f29ad-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f29ad-118">輸入</span><span class="sxs-lookup"><span data-stu-id="f29ad-118">INPUTS</span></span>

### <span data-ttu-id="f29ad-119">System.object</span><span class="sxs-lookup"><span data-stu-id="f29ad-119">System.String</span></span>

## <span data-ttu-id="f29ad-120">輸出</span><span class="sxs-lookup"><span data-stu-id="f29ad-120">OUTPUTS</span></span>

### <span data-ttu-id="f29ad-121">PSApplicationGatewayAuthenticationCertificate 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f29ad-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="f29ad-122">筆記</span><span class="sxs-lookup"><span data-stu-id="f29ad-122">NOTES</span></span>
* <span data-ttu-id="f29ad-123">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="f29ad-123">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="f29ad-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="f29ad-124">RELATED LINKS</span></span>

[<span data-ttu-id="f29ad-125">附加 AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f29ad-125">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="f29ad-126">新-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f29ad-126">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="f29ad-127">移除-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f29ad-127">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="f29ad-128">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f29ad-128">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


