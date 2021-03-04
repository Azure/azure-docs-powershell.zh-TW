---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 4e58ee2c2f9b7854234913f0cf6ce7c6923f3345
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906549"
---
# <span data-ttu-id="b1f3e-101">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="b1f3e-101">New-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="b1f3e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b1f3e-102">SYNOPSIS</span></span>
<span data-ttu-id="b1f3e-103">建立應用程式閘道的 SSL 設定檔。</span><span class="sxs-lookup"><span data-stu-id="b1f3e-103">Creates SSL profile for an application gateway.</span></span>

## <span data-ttu-id="b1f3e-104">語法</span><span class="sxs-lookup"><span data-stu-id="b1f3e-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslProfile -Name <String> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 [-ClientAuthConfiguration <PSApplicationGatewayClientAuthConfiguration>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1f3e-105">描述</span><span class="sxs-lookup"><span data-stu-id="b1f3e-105">DESCRIPTION</span></span>
<span data-ttu-id="b1f3e-106">**New-AzApplicationGatewaySslProfile** Cmdlet 會建立應用程式閘道的 SSL 設定檔。</span><span class="sxs-lookup"><span data-stu-id="b1f3e-106">The **New-AzApplicationGatewaySslProfile** cmdlet creates SSL profile for an application gateway.</span></span> <span data-ttu-id="b1f3e-107">SSL 設定檔是在 HTTPS 聆聽程式上所配置。</span><span class="sxs-lookup"><span data-stu-id="b1f3e-107">The ssl profile is configured on the HTTPS listeners.</span></span>

## <span data-ttu-id="b1f3e-108">例子</span><span class="sxs-lookup"><span data-stu-id="b1f3e-108">EXAMPLES</span></span>

### <span data-ttu-id="b1f3e-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="b1f3e-109">Example 1</span></span>
```powershell
PS C:\> $sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
PS C:\> $trustedClient01 = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert01" -CertificateFile "C:\clientCAChain1.cer"
PS C:\> $profile = New-AzApplicationGatewaySslProfile -Name $sslProfile01Name -SslPolicy $sslPolicy -TrustedClientCertificates $trustedClient01
```
<span data-ttu-id="b1f3e-110">第一個命令會建立新的 SSL 策略，並儲存在$sslPolicy變數中。</span><span class="sxs-lookup"><span data-stu-id="b1f3e-110">The first command creates a new SSL policy and stores it in the $sslPolicy variable.</span></span>
<span data-ttu-id="b1f3e-111">第二個命令會建立信任的用戶端 CA 憑證鏈，並儲存在 $ClientCert 01 變數中。</span><span class="sxs-lookup"><span data-stu-id="b1f3e-111">The second command creates a trusted client CA certificate chains and stores them in the $ClientCert01 variable.</span></span>
<span data-ttu-id="b1f3e-112">第三個命令會使用 ssl 策略和信任的用戶端 CA 憑證鏈來建立新的 SSL 設定檔。</span><span class="sxs-lookup"><span data-stu-id="b1f3e-112">The third command create a new SSL profile with the the ssl policy and trusted client CA certificate chain.</span></span>

## <span data-ttu-id="b1f3e-113">參數</span><span class="sxs-lookup"><span data-stu-id="b1f3e-113">PARAMETERS</span></span>

### <span data-ttu-id="b1f3e-114">-ClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="b1f3e-114">-ClientAuthConfiguration</span></span>
<span data-ttu-id="b1f3e-115">用戶端驗證設定設定</span><span class="sxs-lookup"><span data-stu-id="b1f3e-115">Client authentication configuration settings</span></span>

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

### <span data-ttu-id="b1f3e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1f3e-116">-DefaultProfile</span></span>
<span data-ttu-id="b1f3e-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b1f3e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1f3e-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="b1f3e-118">-Name</span></span>
<span data-ttu-id="b1f3e-119">SSL 設定檔的名稱</span><span class="sxs-lookup"><span data-stu-id="b1f3e-119">The name of the SSL profile</span></span>

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

### <span data-ttu-id="b1f3e-120">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="b1f3e-120">-SslPolicy</span></span>
<span data-ttu-id="b1f3e-121">SSL 政策</span><span class="sxs-lookup"><span data-stu-id="b1f3e-121">SSL policy</span></span>

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

### <span data-ttu-id="b1f3e-122">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="b1f3e-122">-TrustedClientCertificates</span></span>
<span data-ttu-id="b1f3e-123">信任的用戶端 CA 憑證鏈</span><span class="sxs-lookup"><span data-stu-id="b1f3e-123">The trusted client CA certificate chains</span></span>

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

### <span data-ttu-id="b1f3e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1f3e-124">CommonParameters</span></span>
<span data-ttu-id="b1f3e-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b1f3e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1f3e-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b1f3e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1f3e-127">輸入</span><span class="sxs-lookup"><span data-stu-id="b1f3e-127">INPUTS</span></span>

### <span data-ttu-id="b1f3e-128">沒有</span><span class="sxs-lookup"><span data-stu-id="b1f3e-128">None</span></span>

## <span data-ttu-id="b1f3e-129">輸出</span><span class="sxs-lookup"><span data-stu-id="b1f3e-129">OUTPUTS</span></span>

### <span data-ttu-id="b1f3e-130">Microsoft.Azure.Commands.Network.models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="b1f3e-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="b1f3e-131">筆記</span><span class="sxs-lookup"><span data-stu-id="b1f3e-131">NOTES</span></span>

## <span data-ttu-id="b1f3e-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="b1f3e-132">RELATED LINKS</span></span>

[<span data-ttu-id="b1f3e-133">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="b1f3e-133">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="b1f3e-134">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="b1f3e-134">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="b1f3e-135">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="b1f3e-135">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="b1f3e-136">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="b1f3e-136">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)