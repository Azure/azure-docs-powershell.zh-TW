---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: a9b0d41ad700d0591e38fa339c38efb85cb00859
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98286948"
---
# <span data-ttu-id="0fe12-101">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="0fe12-101">New-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="0fe12-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0fe12-102">SYNOPSIS</span></span>
<span data-ttu-id="0fe12-103">建立應用程式閘道的 SSL 設定檔。</span><span class="sxs-lookup"><span data-stu-id="0fe12-103">Creates SSL profile for an application gateway.</span></span>

## <span data-ttu-id="0fe12-104">句法</span><span class="sxs-lookup"><span data-stu-id="0fe12-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslProfile -Name <String> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 [-ClientAuthConfiguration <PSApplicationGatewayClientAuthConfiguration>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0fe12-105">說明</span><span class="sxs-lookup"><span data-stu-id="0fe12-105">DESCRIPTION</span></span>
<span data-ttu-id="0fe12-106">**新的-AzApplicationGatewaySslProfile** Cmdlet 會為應用程式閘道建立 SSL 設定檔。</span><span class="sxs-lookup"><span data-stu-id="0fe12-106">The **New-AzApplicationGatewaySslProfile** cmdlet creates SSL profile for an application gateway.</span></span> <span data-ttu-id="0fe12-107">Ssl 設定檔是在 HTTPS 偵聽程式上設定。</span><span class="sxs-lookup"><span data-stu-id="0fe12-107">The ssl profile is configured on the HTTPS listeners.</span></span>

## <span data-ttu-id="0fe12-108">示例</span><span class="sxs-lookup"><span data-stu-id="0fe12-108">EXAMPLES</span></span>

### <span data-ttu-id="0fe12-109">範例1</span><span class="sxs-lookup"><span data-stu-id="0fe12-109">Example 1</span></span>
```powershell
PS C:\> $sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
PS C:\> $trustedClient01 = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert01" -CertificateFile "C:\clientCAChain1.cer"
PS C:\> $profile = New-AzApplicationGatewaySslProfile -Name $sslProfile01Name -SslPolicy $sslPolicy -TrustedClientCertificates $trustedClient01
```
<span data-ttu-id="0fe12-110">第一個命令會建立新的 SSL 原則，並將它儲存在 $sslPolicy 變數中。</span><span class="sxs-lookup"><span data-stu-id="0fe12-110">The first command creates a new SSL policy and stores it in the $sslPolicy variable.</span></span>
<span data-ttu-id="0fe12-111">第二個命令會建立信任的用戶端 CA 憑證鏈，並將它們儲存在 $ClientCert 01 變數中。</span><span class="sxs-lookup"><span data-stu-id="0fe12-111">The second command creates a trusted client CA certificate chains and stores them in the $ClientCert01 variable.</span></span>
<span data-ttu-id="0fe12-112">第三個命令會使用 SSL 原則和受信任的用戶端 CA 憑證鏈，建立新的 SSL 設定檔。</span><span class="sxs-lookup"><span data-stu-id="0fe12-112">The third command create a new SSL profile with the the ssl policy and trusted client CA certificate chain.</span></span>

## <span data-ttu-id="0fe12-113">參數</span><span class="sxs-lookup"><span data-stu-id="0fe12-113">PARAMETERS</span></span>

### <span data-ttu-id="0fe12-114">-ClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="0fe12-114">-ClientAuthConfiguration</span></span>
<span data-ttu-id="0fe12-115">用戶端驗證設定設定</span><span class="sxs-lookup"><span data-stu-id="0fe12-115">Client authentication configuration settings</span></span>

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

### <span data-ttu-id="0fe12-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fe12-116">-DefaultProfile</span></span>
<span data-ttu-id="0fe12-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0fe12-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fe12-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="0fe12-118">-Name</span></span>
<span data-ttu-id="0fe12-119">SSL 設定檔的名稱</span><span class="sxs-lookup"><span data-stu-id="0fe12-119">The name of the SSL profile</span></span>

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

### <span data-ttu-id="0fe12-120">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="0fe12-120">-SslPolicy</span></span>
<span data-ttu-id="0fe12-121">SSL 原則</span><span class="sxs-lookup"><span data-stu-id="0fe12-121">SSL policy</span></span>

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

### <span data-ttu-id="0fe12-122">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="0fe12-122">-TrustedClientCertificates</span></span>
<span data-ttu-id="0fe12-123">受信任的用戶端 CA 憑證鏈</span><span class="sxs-lookup"><span data-stu-id="0fe12-123">The trusted client CA certificate chains</span></span>

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

### <span data-ttu-id="0fe12-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fe12-124">CommonParameters</span></span>
<span data-ttu-id="0fe12-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0fe12-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fe12-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0fe12-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fe12-127">輸入</span><span class="sxs-lookup"><span data-stu-id="0fe12-127">INPUTS</span></span>

### <span data-ttu-id="0fe12-128">所有</span><span class="sxs-lookup"><span data-stu-id="0fe12-128">None</span></span>

## <span data-ttu-id="0fe12-129">輸出</span><span class="sxs-lookup"><span data-stu-id="0fe12-129">OUTPUTS</span></span>

### <span data-ttu-id="0fe12-130">PSApplicationGatewaySslProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0fe12-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="0fe12-131">筆記</span><span class="sxs-lookup"><span data-stu-id="0fe12-131">NOTES</span></span>

## <span data-ttu-id="0fe12-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="0fe12-132">RELATED LINKS</span></span>

[<span data-ttu-id="0fe12-133">附加 AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="0fe12-133">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="0fe12-134">AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="0fe12-134">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="0fe12-135">移除-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="0fe12-135">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="0fe12-136">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="0fe12-136">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)