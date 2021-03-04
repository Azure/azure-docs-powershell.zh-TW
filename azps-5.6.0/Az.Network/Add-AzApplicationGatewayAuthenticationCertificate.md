---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: ba0d82ab04f8e0c990c7bbf15facb3ee725f7609
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905937"
---
# <span data-ttu-id="72138-101">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="72138-101">Add-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="72138-102">簡介</span><span class="sxs-lookup"><span data-stu-id="72138-102">SYNOPSIS</span></span>
<span data-ttu-id="72138-103">新增驗證憑證至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="72138-103">Adds an authentication certificate to an application gateway.</span></span>

## <span data-ttu-id="72138-104">語法</span><span class="sxs-lookup"><span data-stu-id="72138-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72138-105">描述</span><span class="sxs-lookup"><span data-stu-id="72138-105">DESCRIPTION</span></span>
<span data-ttu-id="72138-106">**Add-AzApplicationGatewayAuthenticationCertificate** Cmdlet 會新增驗證憑證至 Azure 應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="72138-106">The **Add-AzApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="72138-107">例子</span><span class="sxs-lookup"><span data-stu-id="72138-107">EXAMPLES</span></span>

### <span data-ttu-id="72138-108">範例 1：新增驗證憑證至應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="72138-108">Example 1: Add authentication certificate to an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01" -CertificateFile "C:\cert.cer"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="72138-109">第一個命令會獲得名為 appGwName 的應用程式閘道，並儲存在$appgw變數。</span><span class="sxs-lookup"><span data-stu-id="72138-109">The first command gets an application gateway named appGwName and stores it in $appgw variable.</span></span>
<span data-ttu-id="72138-110">第二個命令會將名為 cert01 的驗證憑證新增到應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="72138-110">The second command adds authentication certificate named cert01 to the application gateway.</span></span>
<span data-ttu-id="72138-111">第三個命令會更新應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="72138-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="72138-112">參數</span><span class="sxs-lookup"><span data-stu-id="72138-112">PARAMETERS</span></span>

### <span data-ttu-id="72138-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="72138-113">-ApplicationGateway</span></span>
<span data-ttu-id="72138-114">指定此 Cmdlet 新增驗證憑證的應用程式閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="72138-114">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="72138-115">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="72138-115">-CertificateFile</span></span>
<span data-ttu-id="72138-116">指定此 Cmdlet 新增之驗證憑證的路徑。</span><span class="sxs-lookup"><span data-stu-id="72138-116">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="72138-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72138-117">-DefaultProfile</span></span>
<span data-ttu-id="72138-118">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="72138-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72138-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="72138-119">-Name</span></span>
<span data-ttu-id="72138-120">指定此 Cmdlet 新增到應用程式閘道的憑證名稱。</span><span class="sxs-lookup"><span data-stu-id="72138-120">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="72138-121">-確認</span><span class="sxs-lookup"><span data-stu-id="72138-121">-Confirm</span></span>
<span data-ttu-id="72138-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="72138-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72138-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72138-123">-WhatIf</span></span>
<span data-ttu-id="72138-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="72138-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72138-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="72138-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72138-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72138-126">CommonParameters</span></span>
<span data-ttu-id="72138-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="72138-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72138-128">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="72138-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72138-129">輸入</span><span class="sxs-lookup"><span data-stu-id="72138-129">INPUTS</span></span>

### <span data-ttu-id="72138-130">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="72138-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="72138-131">輸出</span><span class="sxs-lookup"><span data-stu-id="72138-131">OUTPUTS</span></span>

### <span data-ttu-id="72138-132">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="72138-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="72138-133">筆記</span><span class="sxs-lookup"><span data-stu-id="72138-133">NOTES</span></span>
* <span data-ttu-id="72138-134">關鍵字：azure、azurerm、arm、資源、管理、管理員、網路、網路</span><span class="sxs-lookup"><span data-stu-id="72138-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="72138-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="72138-135">RELATED LINKS</span></span>

[<span data-ttu-id="72138-136">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="72138-136">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="72138-137">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="72138-137">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="72138-138">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="72138-138">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="72138-139">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="72138-139">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


