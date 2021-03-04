---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: ac4da06b2f90f9d7bb5c3cbccbde98c8c65db481
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909541"
---
# <span data-ttu-id="70358-101">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="70358-101">Add-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="70358-102">簡介</span><span class="sxs-lookup"><span data-stu-id="70358-102">SYNOPSIS</span></span>
<span data-ttu-id="70358-103">新增信任的用戶端 CA 憑證鏈至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="70358-103">Adds a trusted client CA certificate chain to an application gateway.</span></span>

## <span data-ttu-id="70358-104">語法</span><span class="sxs-lookup"><span data-stu-id="70358-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70358-105">描述</span><span class="sxs-lookup"><span data-stu-id="70358-105">DESCRIPTION</span></span>
<span data-ttu-id="70358-106">**Add-AzApplicationGatewayTrustedClientCertificate** Cmdlet 會將信任的用戶端 CA 憑證鏈新增到 Azure 應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="70358-106">The **Add-AzApplicationGatewayTrustedClientCertificate** cmdlet adds a trusted client CA certificate chain to an Azure application gateway.</span></span>

## <span data-ttu-id="70358-107">例子</span><span class="sxs-lookup"><span data-stu-id="70358-107">EXAMPLES</span></span>

### <span data-ttu-id="70358-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="70358-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedClient = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert" -CertificateFile "C:\clientCAChain.cer"
PS C:\> $AppGw = Add-AzApplicationGatewaySslProfile -Name $sslProfileName -ApplicationGateway $gw -TrustedClientCertificates $trustedClient
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="70358-109">第一個命令會獲得應用程式閘道，並儲存在$gw變數中。</span><span class="sxs-lookup"><span data-stu-id="70358-109">The first command gets the application gateway and stores it in $gw variable.</span></span> <span data-ttu-id="70358-110">第二個命令會建立一個新的信任的用戶端 CA 憑證鏈，以用戶端 CA 憑證的路徑做為輸入。</span><span class="sxs-lookup"><span data-stu-id="70358-110">The second command creates a new trusted client CA certificate chain taking path of the client CA certificate as input.</span></span> <span data-ttu-id="70358-111">第三個命令會使用信任的用戶端憑證建立 SSL 設定檔。</span><span class="sxs-lookup"><span data-stu-id="70358-111">The third command creates a SSL profile using trusted client certificate.</span></span> <span data-ttu-id="70358-112">第四個命令會更新應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="70358-112">The fourth command updates the Application Gateway.</span></span>

## <span data-ttu-id="70358-113">參數</span><span class="sxs-lookup"><span data-stu-id="70358-113">PARAMETERS</span></span>

### <span data-ttu-id="70358-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="70358-114">-ApplicationGateway</span></span>
<span data-ttu-id="70358-115">應用程式Gateway</span><span class="sxs-lookup"><span data-stu-id="70358-115">The applicationGateway</span></span>

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

### <span data-ttu-id="70358-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="70358-116">-CertificateFile</span></span>
<span data-ttu-id="70358-117">信任的用戶端 CA 憑證鏈檔案的路徑</span><span class="sxs-lookup"><span data-stu-id="70358-117">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="70358-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70358-118">-DefaultProfile</span></span>
<span data-ttu-id="70358-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="70358-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70358-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="70358-120">-Name</span></span>
<span data-ttu-id="70358-121">信任的用戶端 CA 憑證鏈的名稱</span><span class="sxs-lookup"><span data-stu-id="70358-121">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="70358-122">-確認</span><span class="sxs-lookup"><span data-stu-id="70358-122">-Confirm</span></span>
<span data-ttu-id="70358-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="70358-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70358-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70358-124">-WhatIf</span></span>
<span data-ttu-id="70358-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="70358-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70358-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="70358-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70358-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70358-127">CommonParameters</span></span>
<span data-ttu-id="70358-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="70358-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70358-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="70358-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70358-130">輸入</span><span class="sxs-lookup"><span data-stu-id="70358-130">INPUTS</span></span>

### <span data-ttu-id="70358-131">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="70358-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="70358-132">輸出</span><span class="sxs-lookup"><span data-stu-id="70358-132">OUTPUTS</span></span>

### <span data-ttu-id="70358-133">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="70358-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="70358-134">筆記</span><span class="sxs-lookup"><span data-stu-id="70358-134">NOTES</span></span>

## <span data-ttu-id="70358-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="70358-135">RELATED LINKS</span></span>

[<span data-ttu-id="70358-136">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="70358-136">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="70358-137">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="70358-137">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="70358-138">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="70358-138">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="70358-139">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="70358-139">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)