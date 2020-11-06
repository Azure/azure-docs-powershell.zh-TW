---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: d8f2fcb875503b6d6a8063007926690ef682bdc8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455127"
---
# <span data-ttu-id="a356e-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="a356e-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="a356e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a356e-102">SYNOPSIS</span></span>
<span data-ttu-id="a356e-103">更新應用程式閘道的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="a356e-103">Updates an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a356e-104">句法</span><span class="sxs-lookup"><span data-stu-id="a356e-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a356e-105">說明</span><span class="sxs-lookup"><span data-stu-id="a356e-105">DESCRIPTION</span></span>
<span data-ttu-id="a356e-106">**AzureRmApplicationGatewayAuthenticationCertificate** Cmdlet 會更新 Azure 應用程式閘道的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="a356e-106">The **Set-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="a356e-107">示例</span><span class="sxs-lookup"><span data-stu-id="a356e-107">EXAMPLES</span></span>

## <span data-ttu-id="a356e-108">參數</span><span class="sxs-lookup"><span data-stu-id="a356e-108">PARAMETERS</span></span>

### <span data-ttu-id="a356e-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a356e-109">-ApplicationGateway</span></span>
<span data-ttu-id="a356e-110">指定此 Cmdlet 更新驗證憑證之應用程式閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="a356e-110">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="a356e-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="a356e-111">-CertificateFile</span></span>
<span data-ttu-id="a356e-112">指定此 Cmdlet 更新憑證的驗證憑證檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="a356e-112">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a356e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a356e-113">-DefaultProfile</span></span>
<span data-ttu-id="a356e-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a356e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a356e-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="a356e-115">-Name</span></span>
<span data-ttu-id="a356e-116">指定此 Cmdlet 更新之驗證憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="a356e-116">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a356e-117">-確認</span><span class="sxs-lookup"><span data-stu-id="a356e-117">-Confirm</span></span>
<span data-ttu-id="a356e-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a356e-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a356e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a356e-119">-WhatIf</span></span>
<span data-ttu-id="a356e-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a356e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a356e-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a356e-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a356e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a356e-122">CommonParameters</span></span>
<span data-ttu-id="a356e-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a356e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a356e-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a356e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a356e-125">輸入</span><span class="sxs-lookup"><span data-stu-id="a356e-125">INPUTS</span></span>

### <span data-ttu-id="a356e-126">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a356e-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="a356e-127">參數： ApplicationGateway (ByValue) </span><span class="sxs-lookup"><span data-stu-id="a356e-127">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="a356e-128">輸出</span><span class="sxs-lookup"><span data-stu-id="a356e-128">OUTPUTS</span></span>

### <span data-ttu-id="a356e-129">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a356e-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a356e-130">筆記</span><span class="sxs-lookup"><span data-stu-id="a356e-130">NOTES</span></span>
* <span data-ttu-id="a356e-131">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="a356e-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="a356e-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="a356e-132">RELATED LINKS</span></span>

[<span data-ttu-id="a356e-133">附加 AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="a356e-133">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="a356e-134">AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="a356e-134">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="a356e-135">新-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="a356e-135">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="a356e-136">移除-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="a356e-136">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)


