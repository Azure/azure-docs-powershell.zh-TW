---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 0fa72c48693335dd3df6ab3c1cf8040c5343cc84
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958603"
---
# <span data-ttu-id="42fc5-101">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="42fc5-101">Set-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="42fc5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="42fc5-102">SYNOPSIS</span></span>
<span data-ttu-id="42fc5-103">更新應用程式閘道的 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="42fc5-103">Updates an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="42fc5-104">句法</span><span class="sxs-lookup"><span data-stu-id="42fc5-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42fc5-105">說明</span><span class="sxs-lookup"><span data-stu-id="42fc5-105">DESCRIPTION</span></span>
<span data-ttu-id="42fc5-106">**AzApplicationGatewaySslCertificate** Cmdlet 會更新應用程式閘道的 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="42fc5-106">The **Set-AzApplicationGatewaySslCertificate** cmdlet updates an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="42fc5-107">示例</span><span class="sxs-lookup"><span data-stu-id="42fc5-107">EXAMPLES</span></span>

### <span data-ttu-id="42fc5-108">範例1：更新應用程式閘道上的現有 SSL 憑證</span><span class="sxs-lookup"><span data-stu-id="42fc5-108">Example 1: Update an existing SSL certificate on Application Gateway</span></span>
```
PS C:\> $appGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="42fc5-109">針對名為 ApplicationGateway01 的應用程式閘道，更新現有的 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="42fc5-109">Update an existing SSL certificate for the application gateway named ApplicationGateway01.</span></span>

### <span data-ttu-id="42fc5-110">範例2：使用 KeyVault 機密更新現有 SSL 憑證 (版本較低的 secretId) 應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="42fc5-110">Example 2: Update an existing SSL certificate using KeyVault Secret (version-less secretId) on Application Gateway</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="42fc5-111">使用來取得密碼並更新現有的 SSL 憑證 `Set-AzApplicationGatewaySslCertificate` 。</span><span class="sxs-lookup"><span data-stu-id="42fc5-111">Get the secret and update an existing SSL Certificate using `Set-AzApplicationGatewaySslCertificate`.</span></span>

### <span data-ttu-id="42fc5-112">範例3：在應用程式閘道使用 KeyVault Secret 更新現有的 SSL 憑證</span><span class="sxs-lookup"><span data-stu-id="42fc5-112">Example 3: Update an existing SSL certificate using KeyVault Secret on Application Gateway</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="42fc5-113">使用來取得密碼並更新現有的 SSL 憑證 `Set-AzApplicationGatewaySslCertificate` 。</span><span class="sxs-lookup"><span data-stu-id="42fc5-113">Get the secret and update an existing SSL Certificate using `Set-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="42fc5-114">注意：如果應用程式閘道需要使用 KeyVault 同步處理憑證，請提供版本較少的 secretId。</span><span class="sxs-lookup"><span data-stu-id="42fc5-114">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="42fc5-115">參數</span><span class="sxs-lookup"><span data-stu-id="42fc5-115">PARAMETERS</span></span>

### <span data-ttu-id="42fc5-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="42fc5-116">-ApplicationGateway</span></span>
<span data-ttu-id="42fc5-117">指定與安全通訊端層 (SSL) 憑證相關聯的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="42fc5-117">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

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

### <span data-ttu-id="42fc5-118">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="42fc5-118">-CertificateFile</span></span>
<span data-ttu-id="42fc5-119">指定 SSL 憑證的路徑。</span><span class="sxs-lookup"><span data-stu-id="42fc5-119">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="42fc5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42fc5-120">-DefaultProfile</span></span>
<span data-ttu-id="42fc5-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="42fc5-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42fc5-122">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="42fc5-122">-KeyVaultSecretId</span></span>
<span data-ttu-id="42fc5-123">SecretId KeyVault 密碼的 (uri) 。</span><span class="sxs-lookup"><span data-stu-id="42fc5-123">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="42fc5-124">當需要使用特定的機密版本時，請使用這個選項。</span><span class="sxs-lookup"><span data-stu-id="42fc5-124">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="42fc5-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="42fc5-125">-Name</span></span>
<span data-ttu-id="42fc5-126">指定 SSL 憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="42fc5-126">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="42fc5-127">-Password</span><span class="sxs-lookup"><span data-stu-id="42fc5-127">-Password</span></span>
<span data-ttu-id="42fc5-128">指定 SSL 憑證的密碼。</span><span class="sxs-lookup"><span data-stu-id="42fc5-128">Specifies the password of the SSL certificate.</span></span>

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

### <span data-ttu-id="42fc5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42fc5-129">CommonParameters</span></span>
<span data-ttu-id="42fc5-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="42fc5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42fc5-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="42fc5-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42fc5-132">輸入</span><span class="sxs-lookup"><span data-stu-id="42fc5-132">INPUTS</span></span>

### <span data-ttu-id="42fc5-133">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="42fc5-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="42fc5-134">輸出</span><span class="sxs-lookup"><span data-stu-id="42fc5-134">OUTPUTS</span></span>

### <span data-ttu-id="42fc5-135">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="42fc5-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="42fc5-136">筆記</span><span class="sxs-lookup"><span data-stu-id="42fc5-136">NOTES</span></span>

## <span data-ttu-id="42fc5-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="42fc5-137">RELATED LINKS</span></span>

[<span data-ttu-id="42fc5-138">附加 AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="42fc5-138">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="42fc5-139">AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="42fc5-139">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="42fc5-140">新-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="42fc5-140">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="42fc5-141">移除-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="42fc5-141">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)


