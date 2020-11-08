---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 687752d74e13030cd954736132dba845c2c55127
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137679"
---
# <span data-ttu-id="fe2ce-101">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="fe2ce-101">Add-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="fe2ce-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fe2ce-102">SYNOPSIS</span></span>
<span data-ttu-id="fe2ce-103">將驗證憑證新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="fe2ce-103">Adds an authentication certificate to an application gateway.</span></span>

## <span data-ttu-id="fe2ce-104">句法</span><span class="sxs-lookup"><span data-stu-id="fe2ce-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe2ce-105">說明</span><span class="sxs-lookup"><span data-stu-id="fe2ce-105">DESCRIPTION</span></span>
<span data-ttu-id="fe2ce-106">**載入 AzApplicationGatewayAuthenticationCertificate** Cmdlet 會將驗證憑證新增至 Azure 應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="fe2ce-106">The **Add-AzApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="fe2ce-107">示例</span><span class="sxs-lookup"><span data-stu-id="fe2ce-107">EXAMPLES</span></span>

### <span data-ttu-id="fe2ce-108">範例1：將驗證憑證新增至應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="fe2ce-108">Example 1: Add authentication certificate to an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01" -CertificateFile "C:\cert.cer"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="fe2ce-109">第一個命令會取得名為 appGwName 的應用程式閘道，並將其儲存在 $appgw 變數中。</span><span class="sxs-lookup"><span data-stu-id="fe2ce-109">The first command gets an application gateway named appGwName and stores it in $appgw variable.</span></span>
<span data-ttu-id="fe2ce-110">第二個命令會將名為 cert01 的驗證憑證新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="fe2ce-110">The second command adds authentication certificate named cert01 to the application gateway.</span></span>
<span data-ttu-id="fe2ce-111">第三個命令會更新應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="fe2ce-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="fe2ce-112">參數</span><span class="sxs-lookup"><span data-stu-id="fe2ce-112">PARAMETERS</span></span>

### <span data-ttu-id="fe2ce-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fe2ce-113">-ApplicationGateway</span></span>
<span data-ttu-id="fe2ce-114">指定此 Cmdlet 新增驗證憑證之應用程式閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="fe2ce-114">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="fe2ce-115">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="fe2ce-115">-CertificateFile</span></span>
<span data-ttu-id="fe2ce-116">指定此 Cmdlet 所新增之驗證憑證的路徑。</span><span class="sxs-lookup"><span data-stu-id="fe2ce-116">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="fe2ce-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe2ce-117">-DefaultProfile</span></span>
<span data-ttu-id="fe2ce-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fe2ce-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe2ce-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="fe2ce-119">-Name</span></span>
<span data-ttu-id="fe2ce-120">指定此 Cmdlet 新增至應用程式閘道之憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="fe2ce-120">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="fe2ce-121">-確認</span><span class="sxs-lookup"><span data-stu-id="fe2ce-121">-Confirm</span></span>
<span data-ttu-id="fe2ce-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fe2ce-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe2ce-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe2ce-123">-WhatIf</span></span>
<span data-ttu-id="fe2ce-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fe2ce-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe2ce-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fe2ce-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe2ce-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe2ce-126">CommonParameters</span></span>
<span data-ttu-id="fe2ce-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fe2ce-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe2ce-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fe2ce-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe2ce-129">輸入</span><span class="sxs-lookup"><span data-stu-id="fe2ce-129">INPUTS</span></span>

### <span data-ttu-id="fe2ce-130">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fe2ce-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fe2ce-131">輸出</span><span class="sxs-lookup"><span data-stu-id="fe2ce-131">OUTPUTS</span></span>

### <span data-ttu-id="fe2ce-132">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fe2ce-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fe2ce-133">筆記</span><span class="sxs-lookup"><span data-stu-id="fe2ce-133">NOTES</span></span>
* <span data-ttu-id="fe2ce-134">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="fe2ce-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="fe2ce-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="fe2ce-135">RELATED LINKS</span></span>

[<span data-ttu-id="fe2ce-136">AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="fe2ce-136">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="fe2ce-137">新-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="fe2ce-137">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="fe2ce-138">移除-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="fe2ce-138">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="fe2ce-139">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="fe2ce-139">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


