---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 5af778b84981b5b15acaa688bd8ad1702e5ab7e3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136237"
---
# <span data-ttu-id="b936f-101">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b936f-101">Set-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="b936f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b936f-102">SYNOPSIS</span></span>
<span data-ttu-id="b936f-103">更新應用程式閘道的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="b936f-103">Updates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="b936f-104">句法</span><span class="sxs-lookup"><span data-stu-id="b936f-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b936f-105">說明</span><span class="sxs-lookup"><span data-stu-id="b936f-105">DESCRIPTION</span></span>
<span data-ttu-id="b936f-106">**AzApplicationGatewayAuthenticationCertificate** Cmdlet 會更新 Azure 應用程式閘道的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="b936f-106">The **Set-AzApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="b936f-107">示例</span><span class="sxs-lookup"><span data-stu-id="b936f-107">EXAMPLES</span></span>

### <span data-ttu-id="b936f-108">範例1：更新驗證憑證</span><span class="sxs-lookup"><span data-stu-id="b936f-108">Example 1: Update an authentication certificate</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01" -CertificateFile "C:\cert2.cer"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="b936f-109">第一個命令會取得名為 appGwName 的應用程式閘道，並將結果儲存在 $appgw 變數中。</span><span class="sxs-lookup"><span data-stu-id="b936f-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="b936f-110">第二個命令會更新應用程式閘道中名為 cert01 的驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="b936f-110">The second command updates the authentication certificate named cert01 in the application gateway.</span></span>
<span data-ttu-id="b936f-111">第三個命令會更新應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="b936f-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="b936f-112">參數</span><span class="sxs-lookup"><span data-stu-id="b936f-112">PARAMETERS</span></span>

### <span data-ttu-id="b936f-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b936f-113">-ApplicationGateway</span></span>
<span data-ttu-id="b936f-114">指定此 Cmdlet 更新驗證憑證之應用程式閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="b936f-114">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="b936f-115">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="b936f-115">-CertificateFile</span></span>
<span data-ttu-id="b936f-116">指定此 Cmdlet 更新憑證的驗證憑證檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="b936f-116">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="b936f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b936f-117">-DefaultProfile</span></span>
<span data-ttu-id="b936f-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b936f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b936f-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="b936f-119">-Name</span></span>
<span data-ttu-id="b936f-120">指定此 Cmdlet 更新之驗證憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="b936f-120">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="b936f-121">-確認</span><span class="sxs-lookup"><span data-stu-id="b936f-121">-Confirm</span></span>
<span data-ttu-id="b936f-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b936f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b936f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b936f-123">-WhatIf</span></span>
<span data-ttu-id="b936f-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b936f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b936f-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b936f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b936f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b936f-126">CommonParameters</span></span>
<span data-ttu-id="b936f-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b936f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b936f-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b936f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b936f-129">輸入</span><span class="sxs-lookup"><span data-stu-id="b936f-129">INPUTS</span></span>

### <span data-ttu-id="b936f-130">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b936f-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b936f-131">輸出</span><span class="sxs-lookup"><span data-stu-id="b936f-131">OUTPUTS</span></span>

### <span data-ttu-id="b936f-132">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b936f-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b936f-133">筆記</span><span class="sxs-lookup"><span data-stu-id="b936f-133">NOTES</span></span>
* <span data-ttu-id="b936f-134">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路</span><span class="sxs-lookup"><span data-stu-id="b936f-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="b936f-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="b936f-135">RELATED LINKS</span></span>

[<span data-ttu-id="b936f-136">附加 AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b936f-136">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b936f-137">AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b936f-137">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b936f-138">新-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b936f-138">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b936f-139">移除-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b936f-139">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)


