---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: f1b944e2673c9682a0194c4996fa4d2b34fae97b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901961"
---
# <span data-ttu-id="6465b-101">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6465b-101">Set-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="6465b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6465b-102">SYNOPSIS</span></span>
<span data-ttu-id="6465b-103">更新應用程式閘道的 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="6465b-103">Updates an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="6465b-104">語法</span><span class="sxs-lookup"><span data-stu-id="6465b-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6465b-105">描述</span><span class="sxs-lookup"><span data-stu-id="6465b-105">DESCRIPTION</span></span>
<span data-ttu-id="6465b-106">**Set-AzApplicationGatewaySslCertificate** Cmdlet 會更新應用程式閘道的 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="6465b-106">The **Set-AzApplicationGatewaySslCertificate** cmdlet updates an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="6465b-107">例子</span><span class="sxs-lookup"><span data-stu-id="6465b-107">EXAMPLES</span></span>

### <span data-ttu-id="6465b-108">範例 1：更新應用程式閘道上現有的 SSL 憑證</span><span class="sxs-lookup"><span data-stu-id="6465b-108">Example 1: Update an existing SSL certificate on Application Gateway</span></span>
```
PS C:\> $appGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString $passwordPlainString -AsPlainText -Force
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="6465b-109">更新名為 ApplicationGateway01 之應用程式閘道的現有 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="6465b-109">Update an existing SSL certificate for the application gateway named ApplicationGateway01.</span></span>

### <span data-ttu-id="6465b-110">範例 2：在應用程式閘道上使用 KeyVault Secret (version-less secretId) 現有的 SSL 憑證</span><span class="sxs-lookup"><span data-stu-id="6465b-110">Example 2: Update an existing SSL certificate using KeyVault Secret (version-less secretId) on Application Gateway</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="6465b-111">取得金鑰，然後使用更新現有的 SSL 憑證 `Set-AzApplicationGatewaySslCertificate` 。</span><span class="sxs-lookup"><span data-stu-id="6465b-111">Get the secret and update an existing SSL Certificate using `Set-AzApplicationGatewaySslCertificate`.</span></span>

### <span data-ttu-id="6465b-112">範例 3：在應用程式閘道使用 KeyVault Secret 更新現有的 SSL 憑證</span><span class="sxs-lookup"><span data-stu-id="6465b-112">Example 3: Update an existing SSL certificate using KeyVault Secret on Application Gateway</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="6465b-113">取得金鑰，然後使用更新現有的 SSL 憑證 `Set-AzApplicationGatewaySslCertificate` 。</span><span class="sxs-lookup"><span data-stu-id="6465b-113">Get the secret and update an existing SSL Certificate using `Set-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="6465b-114">注意：如果需要應用程式閘道將憑證與 KeyVault 同步處理，請提供版本較少的 secretId。</span><span class="sxs-lookup"><span data-stu-id="6465b-114">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="6465b-115">參數</span><span class="sxs-lookup"><span data-stu-id="6465b-115">PARAMETERS</span></span>

### <span data-ttu-id="6465b-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6465b-116">-ApplicationGateway</span></span>
<span data-ttu-id="6465b-117">指定與安全通訊端層與 SSL (關聯的) 閘道。</span><span class="sxs-lookup"><span data-stu-id="6465b-117">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

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

### <span data-ttu-id="6465b-118">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="6465b-118">-CertificateFile</span></span>
<span data-ttu-id="6465b-119">指定 SSL 憑證的路徑。</span><span class="sxs-lookup"><span data-stu-id="6465b-119">Specifies the path of the SSL certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6465b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6465b-120">-DefaultProfile</span></span>
<span data-ttu-id="6465b-121">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6465b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6465b-122">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="6465b-122">-KeyVaultSecretId</span></span>
<span data-ttu-id="6465b-123">SecretId (KeyVault) 的 uri 密碼。</span><span class="sxs-lookup"><span data-stu-id="6465b-123">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="6465b-124">當需要使用特定版本的機密時，請使用此選項。</span><span class="sxs-lookup"><span data-stu-id="6465b-124">Use this option when a specific version of secret needs to be used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6465b-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="6465b-125">-Name</span></span>
<span data-ttu-id="6465b-126">指定 SSL 憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="6465b-126">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="6465b-127">-密碼</span><span class="sxs-lookup"><span data-stu-id="6465b-127">-Password</span></span>
<span data-ttu-id="6465b-128">指定 SSL 憑證的密碼。</span><span class="sxs-lookup"><span data-stu-id="6465b-128">Specifies the password of the SSL certificate.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6465b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6465b-129">CommonParameters</span></span>
<span data-ttu-id="6465b-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6465b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6465b-131">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="6465b-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6465b-132">輸入</span><span class="sxs-lookup"><span data-stu-id="6465b-132">INPUTS</span></span>

### <span data-ttu-id="6465b-133">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6465b-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6465b-134">輸出</span><span class="sxs-lookup"><span data-stu-id="6465b-134">OUTPUTS</span></span>

### <span data-ttu-id="6465b-135">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6465b-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6465b-136">筆記</span><span class="sxs-lookup"><span data-stu-id="6465b-136">NOTES</span></span>

## <span data-ttu-id="6465b-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="6465b-137">RELATED LINKS</span></span>

[<span data-ttu-id="6465b-138">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6465b-138">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="6465b-139">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6465b-139">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="6465b-140">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6465b-140">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="6465b-141">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6465b-141">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)


