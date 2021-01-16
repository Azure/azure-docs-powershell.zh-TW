---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 8930041959712b7533651262a39409e884ffb177
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98282283"
---
# <span data-ttu-id="0c92c-101">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="0c92c-101">Add-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="0c92c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0c92c-102">SYNOPSIS</span></span>
<span data-ttu-id="0c92c-103">將 SSL 設定檔新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="0c92c-103">Adds SSL profile to an application gateway.</span></span>

## <span data-ttu-id="0c92c-104">句法</span><span class="sxs-lookup"><span data-stu-id="0c92c-104">SYNTAX</span></span>

```
Add-AzApplicationGatewaySslProfile -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SslPolicy <PSApplicationGatewaySslPolicy>]
 [-ClientAuthConfiguration <PSApplicationGatewayClientAuthConfiguration>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c92c-105">說明</span><span class="sxs-lookup"><span data-stu-id="0c92c-105">DESCRIPTION</span></span>
<span data-ttu-id="0c92c-106">**載入 AzApplicationGatewaySslProfile** Cmdlet 會將 SSL 設定檔新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="0c92c-106">The **Add-AzApplicationGatewaySslProfile** cmdlet adds a SSL profile to an application gateway.</span></span> <span data-ttu-id="0c92c-107">SSL 設定檔會套用至 HTTPS 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="0c92c-107">The SSL profile is applied to HTTPS Listeners.</span></span>

## <span data-ttu-id="0c92c-108">示例</span><span class="sxs-lookup"><span data-stu-id="0c92c-108">EXAMPLES</span></span>

### <span data-ttu-id="0c92c-109">範例1</span><span class="sxs-lookup"><span data-stu-id="0c92c-109">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
PS C:\> $trustedClient01 = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert01" -CertificateFile "C:\clientCAChain1.cer"
PS C:\> $trustedClient02 = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert02" -CertificateFile "C:\clientCAChain2.cer"
PS C:\> $AppGw = Add-AzApplicationGatewaySslProfile -Name $sslProfile01Name -ApplicationGateway $AppGw -SslPolicy $sslPolicy -TrustedClientCertificates $trustedClient01,$trustedClient02
```

<span data-ttu-id="0c92c-110">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="0c92c-110">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="0c92c-111">第二個命令會建立新的 SSL 原則，並將它儲存在 $sslPolicy 變數中。</span><span class="sxs-lookup"><span data-stu-id="0c92c-111">The second command creates a new SSL policy and stores it in the $sslPolicy variable.</span></span>
<span data-ttu-id="0c92c-112">第三個和第四個命令會建立兩個新的信任用戶端 CA 憑證鏈，並將它們儲存在 $ClientCert 01 和 $ClientCert 02 變數中。</span><span class="sxs-lookup"><span data-stu-id="0c92c-112">The third and fourth command creates two new trusted client CA certificate chains and stores them in the $ClientCert01 and $ClientCert02 variables.</span></span>
<span data-ttu-id="0c92c-113">第五個命令會將 SSL 設定檔與 ssl 原則和受信任的用戶端 CA 憑證鏈一起新增至應用程式閘道 $AppGw。</span><span class="sxs-lookup"><span data-stu-id="0c92c-113">The fifth command adds the SSL profile with the the ssl policy and trusted client CA certificate chains to the application gateway $AppGw.</span></span>

## <span data-ttu-id="0c92c-114">參數</span><span class="sxs-lookup"><span data-stu-id="0c92c-114">PARAMETERS</span></span>

### <span data-ttu-id="0c92c-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0c92c-115">-ApplicationGateway</span></span>
<span data-ttu-id="0c92c-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0c92c-116">The applicationGateway</span></span>

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

### <span data-ttu-id="0c92c-117">-ClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="0c92c-117">-ClientAuthConfiguration</span></span>
<span data-ttu-id="0c92c-118">用戶端驗證設定設定</span><span class="sxs-lookup"><span data-stu-id="0c92c-118">Client authentication configuration settings</span></span>

```yaml
Type: PSApplicationGatewayClientAuthConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c92c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c92c-119">-DefaultProfile</span></span>
<span data-ttu-id="0c92c-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0c92c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c92c-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="0c92c-121">-Name</span></span>
<span data-ttu-id="0c92c-122">SSL 設定檔的名稱</span><span class="sxs-lookup"><span data-stu-id="0c92c-122">The name of the SSL profile</span></span>

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

### <span data-ttu-id="0c92c-123">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="0c92c-123">-SslPolicy</span></span>
<span data-ttu-id="0c92c-124">SSL 原則</span><span class="sxs-lookup"><span data-stu-id="0c92c-124">SSL policy</span></span>

```yaml
Type: PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c92c-125">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="0c92c-125">-TrustedClientCertificates</span></span>
<span data-ttu-id="0c92c-126">受信任的用戶端 CA 憑證鏈</span><span class="sxs-lookup"><span data-stu-id="0c92c-126">The trusted client CA certificate chains</span></span>

```yaml
Type: PSApplicationGatewayTrustedClientCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c92c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c92c-127">CommonParameters</span></span>
<span data-ttu-id="0c92c-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0c92c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c92c-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0c92c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c92c-130">輸入</span><span class="sxs-lookup"><span data-stu-id="0c92c-130">INPUTS</span></span>

### <span data-ttu-id="0c92c-131">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0c92c-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0c92c-132">輸出</span><span class="sxs-lookup"><span data-stu-id="0c92c-132">OUTPUTS</span></span>

### <span data-ttu-id="0c92c-133">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0c92c-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0c92c-134">筆記</span><span class="sxs-lookup"><span data-stu-id="0c92c-134">NOTES</span></span>

## <span data-ttu-id="0c92c-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="0c92c-135">RELATED LINKS</span></span>

[<span data-ttu-id="0c92c-136">新-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="0c92c-136">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="0c92c-137">AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="0c92c-137">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="0c92c-138">移除-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="0c92c-138">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="0c92c-139">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="0c92c-139">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)