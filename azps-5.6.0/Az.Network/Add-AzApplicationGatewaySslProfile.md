---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 469b490b0f0c2bd37f7f58265108278322cbca60
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909542"
---
# <span data-ttu-id="dea42-101">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="dea42-101">Add-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="dea42-102">簡介</span><span class="sxs-lookup"><span data-stu-id="dea42-102">SYNOPSIS</span></span>
<span data-ttu-id="dea42-103">新增 SSL 設定檔至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="dea42-103">Adds SSL profile to an application gateway.</span></span>

## <span data-ttu-id="dea42-104">語法</span><span class="sxs-lookup"><span data-stu-id="dea42-104">SYNTAX</span></span>

```
Add-AzApplicationGatewaySslProfile -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SslPolicy <PSApplicationGatewaySslPolicy>]
 [-ClientAuthConfiguration <PSApplicationGatewayClientAuthConfiguration>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dea42-105">描述</span><span class="sxs-lookup"><span data-stu-id="dea42-105">DESCRIPTION</span></span>
<span data-ttu-id="dea42-106">**Add-AzApplicationGatewaySslProfile** Cmdlet 會新增 SSL 設定檔至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="dea42-106">The **Add-AzApplicationGatewaySslProfile** cmdlet adds a SSL profile to an application gateway.</span></span> <span data-ttu-id="dea42-107">SSL 設定檔會適用于 HTTPS 聆聽者。</span><span class="sxs-lookup"><span data-stu-id="dea42-107">The SSL profile is applied to HTTPS Listeners.</span></span>

## <span data-ttu-id="dea42-108">例子</span><span class="sxs-lookup"><span data-stu-id="dea42-108">EXAMPLES</span></span>

### <span data-ttu-id="dea42-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="dea42-109">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
PS C:\> $trustedClient01 = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert01" -CertificateFile "C:\clientCAChain1.cer"
PS C:\> $trustedClient02 = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert02" -CertificateFile "C:\clientCAChain2.cer"
PS C:\> $AppGw = Add-AzApplicationGatewaySslProfile -Name $sslProfile01Name -ApplicationGateway $AppGw -SslPolicy $sslPolicy -TrustedClientCertificates $trustedClient01,$trustedClient02
```

<span data-ttu-id="dea42-110">第一個命令會獲得應用程式閘道，並儲存在$AppGw變數。</span><span class="sxs-lookup"><span data-stu-id="dea42-110">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="dea42-111">第二個命令會建立新的 SSL 策略，並儲存在$sslPolicy變數中。</span><span class="sxs-lookup"><span data-stu-id="dea42-111">The second command creates a new SSL policy and stores it in the $sslPolicy variable.</span></span>
<span data-ttu-id="dea42-112">第三個和第四個命令會建立兩個新的信任的用戶端 CA 憑證鏈，並儲存在 $ClientCert 01 和 $ClientCert 02 變數中。</span><span class="sxs-lookup"><span data-stu-id="dea42-112">The third and fourth command creates two new trusted client CA certificate chains and stores them in the $ClientCert01 and $ClientCert02 variables.</span></span>
<span data-ttu-id="dea42-113">第五個命令會使用 ssl 策略和信任的用戶端 CA 憑證鏈新增 SSL 設定檔至應用程式閘道$AppGw。</span><span class="sxs-lookup"><span data-stu-id="dea42-113">The fifth command adds the SSL profile with the the ssl policy and trusted client CA certificate chains to the application gateway $AppGw.</span></span>

## <span data-ttu-id="dea42-114">參數</span><span class="sxs-lookup"><span data-stu-id="dea42-114">PARAMETERS</span></span>

### <span data-ttu-id="dea42-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dea42-115">-ApplicationGateway</span></span>
<span data-ttu-id="dea42-116">應用程式Gateway</span><span class="sxs-lookup"><span data-stu-id="dea42-116">The applicationGateway</span></span>

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

### <span data-ttu-id="dea42-117">-ClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="dea42-117">-ClientAuthConfiguration</span></span>
<span data-ttu-id="dea42-118">用戶端驗證設定設定</span><span class="sxs-lookup"><span data-stu-id="dea42-118">Client authentication configuration settings</span></span>

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

### <span data-ttu-id="dea42-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dea42-119">-DefaultProfile</span></span>
<span data-ttu-id="dea42-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="dea42-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dea42-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="dea42-121">-Name</span></span>
<span data-ttu-id="dea42-122">SSL 設定檔的名稱</span><span class="sxs-lookup"><span data-stu-id="dea42-122">The name of the SSL profile</span></span>

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

### <span data-ttu-id="dea42-123">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="dea42-123">-SslPolicy</span></span>
<span data-ttu-id="dea42-124">SSL 政策</span><span class="sxs-lookup"><span data-stu-id="dea42-124">SSL policy</span></span>

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

### <span data-ttu-id="dea42-125">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="dea42-125">-TrustedClientCertificates</span></span>
<span data-ttu-id="dea42-126">信任的用戶端 CA 憑證鏈</span><span class="sxs-lookup"><span data-stu-id="dea42-126">The trusted client CA certificate chains</span></span>

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

### <span data-ttu-id="dea42-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dea42-127">CommonParameters</span></span>
<span data-ttu-id="dea42-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="dea42-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dea42-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dea42-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dea42-130">輸入</span><span class="sxs-lookup"><span data-stu-id="dea42-130">INPUTS</span></span>

### <span data-ttu-id="dea42-131">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dea42-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dea42-132">輸出</span><span class="sxs-lookup"><span data-stu-id="dea42-132">OUTPUTS</span></span>

### <span data-ttu-id="dea42-133">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dea42-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dea42-134">筆記</span><span class="sxs-lookup"><span data-stu-id="dea42-134">NOTES</span></span>

## <span data-ttu-id="dea42-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="dea42-135">RELATED LINKS</span></span>

[<span data-ttu-id="dea42-136">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="dea42-136">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="dea42-137">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="dea42-137">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="dea42-138">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="dea42-138">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="dea42-139">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="dea42-139">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)