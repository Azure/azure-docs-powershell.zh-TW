---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: e3a92085c15116527e1b6c14d5403f68748f4f90
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98287216"
---
# <span data-ttu-id="9d4f0-101">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="9d4f0-101">Add-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="9d4f0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9d4f0-102">SYNOPSIS</span></span>
<span data-ttu-id="9d4f0-103">將信任的用戶端 CA 憑證鏈新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="9d4f0-103">Adds a trusted client CA certificate chain to an application gateway.</span></span>

## <span data-ttu-id="9d4f0-104">句法</span><span class="sxs-lookup"><span data-stu-id="9d4f0-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d4f0-105">說明</span><span class="sxs-lookup"><span data-stu-id="9d4f0-105">DESCRIPTION</span></span>
<span data-ttu-id="9d4f0-106">**AzApplicationGatewayTrustedClientCertificate** Cmdlet 會將信任的用戶端 CA 憑證鏈新增至 Azure 應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="9d4f0-106">The **Add-AzApplicationGatewayTrustedClientCertificate** cmdlet adds a trusted client CA certificate chain to an Azure application gateway.</span></span>

## <span data-ttu-id="9d4f0-107">示例</span><span class="sxs-lookup"><span data-stu-id="9d4f0-107">EXAMPLES</span></span>

### <span data-ttu-id="9d4f0-108">範例1</span><span class="sxs-lookup"><span data-stu-id="9d4f0-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedClient = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert" -CertificateFile "C:\clientCAChain.cer"
PS C:\> $AppGw = Add-AzApplicationGatewaySslProfile -Name $sslProfileName -ApplicationGateway $gw -TrustedClientCertificates $trustedClient
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="9d4f0-109">第一個命令會取得應用程式閘道，並將它儲存在 $gw 變數中。</span><span class="sxs-lookup"><span data-stu-id="9d4f0-109">The first command gets the application gateway and stores it in $gw variable.</span></span> <span data-ttu-id="9d4f0-110">第二個命令會建立新的信任用戶端 CA 憑證鏈，並將用戶端 CA 憑證的路徑做為輸入。</span><span class="sxs-lookup"><span data-stu-id="9d4f0-110">The second command creates a new trusted client CA certificate chain taking path of the client CA certificate as input.</span></span> <span data-ttu-id="9d4f0-111">第三個命令會使用信任的用戶端憑證來建立 SSL 設定檔。</span><span class="sxs-lookup"><span data-stu-id="9d4f0-111">The third command creates a SSL profile using trusted client certificate.</span></span> <span data-ttu-id="9d4f0-112">第四個命令會更新應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="9d4f0-112">The fourth command updates the Application Gateway.</span></span>

## <span data-ttu-id="9d4f0-113">參數</span><span class="sxs-lookup"><span data-stu-id="9d4f0-113">PARAMETERS</span></span>

### <span data-ttu-id="9d4f0-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9d4f0-114">-ApplicationGateway</span></span>
<span data-ttu-id="9d4f0-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9d4f0-115">The applicationGateway</span></span>

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

### <span data-ttu-id="9d4f0-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="9d4f0-116">-CertificateFile</span></span>
<span data-ttu-id="9d4f0-117">受信任的用戶端 CA 憑證鏈檔案的路徑</span><span class="sxs-lookup"><span data-stu-id="9d4f0-117">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="9d4f0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d4f0-118">-DefaultProfile</span></span>
<span data-ttu-id="9d4f0-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9d4f0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d4f0-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="9d4f0-120">-Name</span></span>
<span data-ttu-id="9d4f0-121">受信任的用戶端 CA 憑證鏈的名稱</span><span class="sxs-lookup"><span data-stu-id="9d4f0-121">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="9d4f0-122">-確認</span><span class="sxs-lookup"><span data-stu-id="9d4f0-122">-Confirm</span></span>
<span data-ttu-id="9d4f0-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9d4f0-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d4f0-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d4f0-124">-WhatIf</span></span>
<span data-ttu-id="9d4f0-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9d4f0-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d4f0-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9d4f0-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d4f0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d4f0-127">CommonParameters</span></span>
<span data-ttu-id="9d4f0-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9d4f0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d4f0-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9d4f0-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d4f0-130">輸入</span><span class="sxs-lookup"><span data-stu-id="9d4f0-130">INPUTS</span></span>

### <span data-ttu-id="9d4f0-131">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9d4f0-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9d4f0-132">輸出</span><span class="sxs-lookup"><span data-stu-id="9d4f0-132">OUTPUTS</span></span>

### <span data-ttu-id="9d4f0-133">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9d4f0-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9d4f0-134">筆記</span><span class="sxs-lookup"><span data-stu-id="9d4f0-134">NOTES</span></span>

## <span data-ttu-id="9d4f0-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="9d4f0-135">RELATED LINKS</span></span>

[<span data-ttu-id="9d4f0-136">新-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="9d4f0-136">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="9d4f0-137">AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="9d4f0-137">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="9d4f0-138">移除-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="9d4f0-138">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="9d4f0-139">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="9d4f0-139">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)