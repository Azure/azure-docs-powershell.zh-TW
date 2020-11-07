---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 3c70fcd0e04b566ff1cd3297525d3ed2c9ed95ba
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802233"
---
# <span data-ttu-id="3a1b3-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="3a1b3-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="3a1b3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3a1b3-102">SYNOPSIS</span></span>
<span data-ttu-id="3a1b3-103">更新應用程式閘道的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="3a1b3-103">Updates an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a1b3-104">句法</span><span class="sxs-lookup"><span data-stu-id="3a1b3-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3a1b3-105">說明</span><span class="sxs-lookup"><span data-stu-id="3a1b3-105">DESCRIPTION</span></span>
<span data-ttu-id="3a1b3-106">**AzureRmApplicationGatewayAuthenticationCertificate** Cmdlet 會更新 Azure 應用程式閘道的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="3a1b3-106">The **Set-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="3a1b3-107">示例</span><span class="sxs-lookup"><span data-stu-id="3a1b3-107">EXAMPLES</span></span>

### <span data-ttu-id="3a1b3-108">sr-1</span><span class="sxs-lookup"><span data-stu-id="3a1b3-108">1:</span></span>
```

```

## <span data-ttu-id="3a1b3-109">參數</span><span class="sxs-lookup"><span data-stu-id="3a1b3-109">PARAMETERS</span></span>

### <span data-ttu-id="3a1b3-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3a1b3-110">-ApplicationGateway</span></span>
<span data-ttu-id="3a1b3-111">指定此 Cmdlet 更新驗證憑證之應用程式閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a1b3-111">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="3a1b3-112">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="3a1b3-112">-CertificateFile</span></span>
<span data-ttu-id="3a1b3-113">指定此 Cmdlet 更新憑證的驗證憑證檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="3a1b3-113">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="3a1b3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a1b3-114">-DefaultProfile</span></span>
<span data-ttu-id="3a1b3-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3a1b3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a1b3-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="3a1b3-116">-Name</span></span>
<span data-ttu-id="3a1b3-117">指定此 Cmdlet 更新之驗證憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a1b3-117">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="3a1b3-118">-確認</span><span class="sxs-lookup"><span data-stu-id="3a1b3-118">-Confirm</span></span>
<span data-ttu-id="3a1b3-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3a1b3-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a1b3-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a1b3-120">-WhatIf</span></span>
<span data-ttu-id="3a1b3-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3a1b3-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a1b3-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3a1b3-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a1b3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a1b3-123">CommonParameters</span></span>
<span data-ttu-id="3a1b3-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3a1b3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a1b3-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3a1b3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a1b3-126">輸入</span><span class="sxs-lookup"><span data-stu-id="3a1b3-126">INPUTS</span></span>

### <span data-ttu-id="3a1b3-127">System.object</span><span class="sxs-lookup"><span data-stu-id="3a1b3-127">System.String</span></span>

## <span data-ttu-id="3a1b3-128">輸出</span><span class="sxs-lookup"><span data-stu-id="3a1b3-128">OUTPUTS</span></span>

### <span data-ttu-id="3a1b3-129">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3a1b3-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3a1b3-130">筆記</span><span class="sxs-lookup"><span data-stu-id="3a1b3-130">NOTES</span></span>
* <span data-ttu-id="3a1b3-131">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="3a1b3-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="3a1b3-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="3a1b3-132">RELATED LINKS</span></span>

[<span data-ttu-id="3a1b3-133">附加 AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="3a1b3-133">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="3a1b3-134">AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="3a1b3-134">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="3a1b3-135">新-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="3a1b3-135">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="3a1b3-136">移除-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="3a1b3-136">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)


