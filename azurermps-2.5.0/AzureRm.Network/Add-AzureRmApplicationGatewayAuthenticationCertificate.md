---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 4d664018592f05203c684a896f0a0701940301a6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801293"
---
# <span data-ttu-id="ef868-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ef868-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="ef868-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ef868-102">SYNOPSIS</span></span>
<span data-ttu-id="ef868-103">將驗證憑證新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="ef868-103">Adds an authentication certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef868-104">句法</span><span class="sxs-lookup"><span data-stu-id="ef868-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ef868-105">說明</span><span class="sxs-lookup"><span data-stu-id="ef868-105">DESCRIPTION</span></span>
<span data-ttu-id="ef868-106">**載入 AzureRmApplicationGatewayAuthenticationCertificate** Cmdlet 會將驗證憑證新增至 Azure 應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="ef868-106">The **Add-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="ef868-107">示例</span><span class="sxs-lookup"><span data-stu-id="ef868-107">EXAMPLES</span></span>

### <span data-ttu-id="ef868-108">sr-1</span><span class="sxs-lookup"><span data-stu-id="ef868-108">1:</span></span>
```

```

## <span data-ttu-id="ef868-109">參數</span><span class="sxs-lookup"><span data-stu-id="ef868-109">PARAMETERS</span></span>

### <span data-ttu-id="ef868-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ef868-110">-ApplicationGateway</span></span>
<span data-ttu-id="ef868-111">指定此 Cmdlet 新增驗證憑證之應用程式閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="ef868-111">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="ef868-112">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="ef868-112">-CertificateFile</span></span>
<span data-ttu-id="ef868-113">指定此 Cmdlet 所新增之驗證憑證的路徑。</span><span class="sxs-lookup"><span data-stu-id="ef868-113">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef868-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef868-114">-DefaultProfile</span></span>
<span data-ttu-id="ef868-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ef868-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef868-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="ef868-116">-Name</span></span>
<span data-ttu-id="ef868-117">指定此 Cmdlet 新增至應用程式閘道之憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="ef868-117">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef868-118">-確認</span><span class="sxs-lookup"><span data-stu-id="ef868-118">-Confirm</span></span>
<span data-ttu-id="ef868-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ef868-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef868-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef868-120">-WhatIf</span></span>
<span data-ttu-id="ef868-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ef868-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef868-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ef868-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef868-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef868-123">CommonParameters</span></span>
<span data-ttu-id="ef868-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ef868-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef868-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ef868-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef868-126">輸入</span><span class="sxs-lookup"><span data-stu-id="ef868-126">INPUTS</span></span>

### <span data-ttu-id="ef868-127">System.object</span><span class="sxs-lookup"><span data-stu-id="ef868-127">System.String</span></span>

## <span data-ttu-id="ef868-128">輸出</span><span class="sxs-lookup"><span data-stu-id="ef868-128">OUTPUTS</span></span>

### <span data-ttu-id="ef868-129">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ef868-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ef868-130">筆記</span><span class="sxs-lookup"><span data-stu-id="ef868-130">NOTES</span></span>
* <span data-ttu-id="ef868-131">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="ef868-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="ef868-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="ef868-132">RELATED LINKS</span></span>

[<span data-ttu-id="ef868-133">AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ef868-133">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ef868-134">新-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ef868-134">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ef868-135">移除-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ef868-135">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ef868-136">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ef868-136">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


