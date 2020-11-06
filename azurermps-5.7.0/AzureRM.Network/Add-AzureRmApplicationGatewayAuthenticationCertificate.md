---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 317fd5bf8306416ad4cbef3d1fb64d56d556ed1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449320"
---
# <span data-ttu-id="9f7a0-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="9f7a0-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="9f7a0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9f7a0-102">SYNOPSIS</span></span>
<span data-ttu-id="9f7a0-103">將驗證憑證新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="9f7a0-103">Adds an authentication certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f7a0-104">句法</span><span class="sxs-lookup"><span data-stu-id="9f7a0-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9f7a0-105">說明</span><span class="sxs-lookup"><span data-stu-id="9f7a0-105">DESCRIPTION</span></span>
<span data-ttu-id="9f7a0-106">**載入 AzureRmApplicationGatewayAuthenticationCertificate** Cmdlet 會將驗證憑證新增至 Azure 應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="9f7a0-106">The **Add-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="9f7a0-107">示例</span><span class="sxs-lookup"><span data-stu-id="9f7a0-107">EXAMPLES</span></span>

## <span data-ttu-id="9f7a0-108">參數</span><span class="sxs-lookup"><span data-stu-id="9f7a0-108">PARAMETERS</span></span>

### <span data-ttu-id="9f7a0-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9f7a0-109">-ApplicationGateway</span></span>
<span data-ttu-id="9f7a0-110">指定此 Cmdlet 新增驗證憑證之應用程式閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="9f7a0-110">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="9f7a0-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="9f7a0-111">-CertificateFile</span></span>
<span data-ttu-id="9f7a0-112">指定此 Cmdlet 所新增之驗證憑證的路徑。</span><span class="sxs-lookup"><span data-stu-id="9f7a0-112">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="9f7a0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f7a0-113">-DefaultProfile</span></span>
<span data-ttu-id="9f7a0-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9f7a0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f7a0-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="9f7a0-115">-Name</span></span>
<span data-ttu-id="9f7a0-116">指定此 Cmdlet 新增至應用程式閘道之憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="9f7a0-116">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="9f7a0-117">-確認</span><span class="sxs-lookup"><span data-stu-id="9f7a0-117">-Confirm</span></span>
<span data-ttu-id="9f7a0-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9f7a0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f7a0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f7a0-119">-WhatIf</span></span>
<span data-ttu-id="9f7a0-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9f7a0-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f7a0-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9f7a0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f7a0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f7a0-122">CommonParameters</span></span>
<span data-ttu-id="9f7a0-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9f7a0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f7a0-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9f7a0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f7a0-125">輸入</span><span class="sxs-lookup"><span data-stu-id="9f7a0-125">INPUTS</span></span>

### <span data-ttu-id="9f7a0-126">System.object</span><span class="sxs-lookup"><span data-stu-id="9f7a0-126">System.String</span></span>

## <span data-ttu-id="9f7a0-127">輸出</span><span class="sxs-lookup"><span data-stu-id="9f7a0-127">OUTPUTS</span></span>

### <span data-ttu-id="9f7a0-128">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9f7a0-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9f7a0-129">筆記</span><span class="sxs-lookup"><span data-stu-id="9f7a0-129">NOTES</span></span>
* <span data-ttu-id="9f7a0-130">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="9f7a0-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="9f7a0-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="9f7a0-131">RELATED LINKS</span></span>

[<span data-ttu-id="9f7a0-132">AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="9f7a0-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="9f7a0-133">新-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="9f7a0-133">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="9f7a0-134">移除-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="9f7a0-134">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="9f7a0-135">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="9f7a0-135">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)

