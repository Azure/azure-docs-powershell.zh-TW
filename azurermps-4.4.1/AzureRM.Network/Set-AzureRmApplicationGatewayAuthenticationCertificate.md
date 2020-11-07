---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: a71ba6f6d9b45e0016589d5629f029998f33963f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626592"
---
# <span data-ttu-id="14f7a-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="14f7a-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="14f7a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="14f7a-102">SYNOPSIS</span></span>
<span data-ttu-id="14f7a-103">更新應用程式閘道的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="14f7a-103">Updates an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14f7a-104">句法</span><span class="sxs-lookup"><span data-stu-id="14f7a-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="14f7a-105">說明</span><span class="sxs-lookup"><span data-stu-id="14f7a-105">DESCRIPTION</span></span>
<span data-ttu-id="14f7a-106">**AzureRmApplicationGatewayAuthenticationCertificate** Cmdlet 會更新 Azure 應用程式閘道的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="14f7a-106">The **Set-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="14f7a-107">示例</span><span class="sxs-lookup"><span data-stu-id="14f7a-107">EXAMPLES</span></span>

## <span data-ttu-id="14f7a-108">參數</span><span class="sxs-lookup"><span data-stu-id="14f7a-108">PARAMETERS</span></span>

### <span data-ttu-id="14f7a-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14f7a-109">-ApplicationGateway</span></span>
<span data-ttu-id="14f7a-110">指定此 Cmdlet 更新驗證憑證之應用程式閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="14f7a-110">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="14f7a-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="14f7a-111">-CertificateFile</span></span>
<span data-ttu-id="14f7a-112">指定此 Cmdlet 更新憑證的驗證憑證檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="14f7a-112">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="14f7a-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="14f7a-113">-Name</span></span>
<span data-ttu-id="14f7a-114">指定此 Cmdlet 更新之驗證憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="14f7a-114">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="14f7a-115">-確認</span><span class="sxs-lookup"><span data-stu-id="14f7a-115">-Confirm</span></span>
<span data-ttu-id="14f7a-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="14f7a-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14f7a-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14f7a-117">-WhatIf</span></span>
<span data-ttu-id="14f7a-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="14f7a-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14f7a-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="14f7a-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14f7a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14f7a-120">-DefaultProfile</span></span>
<span data-ttu-id="14f7a-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="14f7a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14f7a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14f7a-122">CommonParameters</span></span>
<span data-ttu-id="14f7a-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="14f7a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14f7a-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="14f7a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14f7a-125">輸入</span><span class="sxs-lookup"><span data-stu-id="14f7a-125">INPUTS</span></span>

### <span data-ttu-id="14f7a-126">System.object</span><span class="sxs-lookup"><span data-stu-id="14f7a-126">System.String</span></span>

## <span data-ttu-id="14f7a-127">輸出</span><span class="sxs-lookup"><span data-stu-id="14f7a-127">OUTPUTS</span></span>

### <span data-ttu-id="14f7a-128">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="14f7a-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="14f7a-129">筆記</span><span class="sxs-lookup"><span data-stu-id="14f7a-129">NOTES</span></span>
* <span data-ttu-id="14f7a-130">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="14f7a-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="14f7a-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="14f7a-131">RELATED LINKS</span></span>

[<span data-ttu-id="14f7a-132">附加 AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="14f7a-132">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="14f7a-133">AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="14f7a-133">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="14f7a-134">新-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="14f7a-134">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="14f7a-135">移除-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="14f7a-135">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)


