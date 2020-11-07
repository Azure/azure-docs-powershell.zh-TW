---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 23b337779da46169be29e3dd6fef55fc70f4f035
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795463"
---
# <span data-ttu-id="39b30-101">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="39b30-101">Set-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="39b30-102">摘要</span><span class="sxs-lookup"><span data-stu-id="39b30-102">SYNOPSIS</span></span>
<span data-ttu-id="39b30-103">更新應用程式閘道的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="39b30-103">Updates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="39b30-104">句法</span><span class="sxs-lookup"><span data-stu-id="39b30-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="39b30-105">說明</span><span class="sxs-lookup"><span data-stu-id="39b30-105">DESCRIPTION</span></span>
<span data-ttu-id="39b30-106">**AzApplicationGatewayAuthenticationCertificate** Cmdlet 會更新 Azure 應用程式閘道的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="39b30-106">The **Set-AzApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="39b30-107">示例</span><span class="sxs-lookup"><span data-stu-id="39b30-107">EXAMPLES</span></span>

### <span data-ttu-id="39b30-108">sr-1</span><span class="sxs-lookup"><span data-stu-id="39b30-108">1:</span></span>
```

```

## <span data-ttu-id="39b30-109">參數</span><span class="sxs-lookup"><span data-stu-id="39b30-109">PARAMETERS</span></span>

### <span data-ttu-id="39b30-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="39b30-110">-ApplicationGateway</span></span>
<span data-ttu-id="39b30-111">指定此 Cmdlet 更新驗證憑證之應用程式閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="39b30-111">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="39b30-112">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="39b30-112">-CertificateFile</span></span>
<span data-ttu-id="39b30-113">指定此 Cmdlet 更新憑證的驗證憑證檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="39b30-113">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="39b30-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39b30-114">-DefaultProfile</span></span>
<span data-ttu-id="39b30-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="39b30-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39b30-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="39b30-116">-Name</span></span>
<span data-ttu-id="39b30-117">指定此 Cmdlet 更新之驗證憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="39b30-117">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="39b30-118">-確認</span><span class="sxs-lookup"><span data-stu-id="39b30-118">-Confirm</span></span>
<span data-ttu-id="39b30-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="39b30-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39b30-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39b30-120">-WhatIf</span></span>
<span data-ttu-id="39b30-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="39b30-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39b30-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="39b30-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39b30-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39b30-123">CommonParameters</span></span>
<span data-ttu-id="39b30-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="39b30-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39b30-125">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="39b30-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39b30-126">輸入</span><span class="sxs-lookup"><span data-stu-id="39b30-126">INPUTS</span></span>

### <span data-ttu-id="39b30-127">System.object</span><span class="sxs-lookup"><span data-stu-id="39b30-127">System.String</span></span>

## <span data-ttu-id="39b30-128">輸出</span><span class="sxs-lookup"><span data-stu-id="39b30-128">OUTPUTS</span></span>

### <span data-ttu-id="39b30-129">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="39b30-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="39b30-130">筆記</span><span class="sxs-lookup"><span data-stu-id="39b30-130">NOTES</span></span>
* <span data-ttu-id="39b30-131">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="39b30-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="39b30-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="39b30-132">RELATED LINKS</span></span>

[<span data-ttu-id="39b30-133">附加 AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="39b30-133">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="39b30-134">AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="39b30-134">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="39b30-135">新-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="39b30-135">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="39b30-136">移除-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="39b30-136">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)


