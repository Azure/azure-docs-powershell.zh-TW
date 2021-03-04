---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EC4C642-1D23-4699-AE00-6E180C38271E
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 4dde5ab085dede4520b26a4fbeb3255cc62c0fe8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909545"
---
# <span data-ttu-id="fc0a6-101">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="fc0a6-101">Add-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="fc0a6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fc0a6-102">SYNOPSIS</span></span>
<span data-ttu-id="fc0a6-103">新增 SSL 憑證至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="fc0a6-103">Adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="fc0a6-104">語法</span><span class="sxs-lookup"><span data-stu-id="fc0a6-104">SYNTAX</span></span>

```
Add-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc0a6-105">描述</span><span class="sxs-lookup"><span data-stu-id="fc0a6-105">DESCRIPTION</span></span>
<span data-ttu-id="fc0a6-106">**Add-AzApplicationGatewaySslCertificate** Cmdlet 會新增 SSL 憑證至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="fc0a6-106">The **Add-AzApplicationGatewaySslCertificate** cmdlet adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="fc0a6-107">例子</span><span class="sxs-lookup"><span data-stu-id="fc0a6-107">EXAMPLES</span></span>

### <span data-ttu-id="fc0a6-108">範例 1：使用 pfx 新增 SSL 憑證至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="fc0a6-108">Example 1: Add an SSL certificate using pfx to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString $passwordPlainString -AsPlainText -Force
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="fc0a6-109">此命令會獲得名為 ApplicationGateway01 的應用程式閘道，然後將名為 Cert01 的 SSL 憑證新增到它。</span><span class="sxs-lookup"><span data-stu-id="fc0a6-109">This command gets an application gateway named ApplicationGateway01 and then adds an SSL certificate named Cert01 to it.</span></span>

### <span data-ttu-id="fc0a6-110">範例 2：使用 KeyVault Secret (version-less secretId) 新增 SSL 憑證至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="fc0a6-110">Example 2: Add an SSL certificate using KeyVault Secret (version-less secretId) to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultCertificate -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.SecretId.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="fc0a6-111">取得機密，並參照到 ， `Add-AzApplicationGatewaySslCertificate` 以將其新增到應用程式閘道，並加上名稱 `Cert01` 。</span><span class="sxs-lookup"><span data-stu-id="fc0a6-111">Get the secret and reference it in the `Add-AzApplicationGatewaySslCertificate` to add it to the Application Gateway with name `Cert01`.</span></span>
<span data-ttu-id="fc0a6-112">注意：由於此處提供版本較少的 secretId，應用程式閘道會定期與 KeyVault 同步處理憑證。</span><span class="sxs-lookup"><span data-stu-id="fc0a6-112">Note: As version-less secretId is provided here, Application Gateway will sync the certificate in regular intervals with the KeyVault.</span></span>

### <span data-ttu-id="fc0a6-113">範例 3：使用 KeyVault Secret (versioned secretId) 新增 SSL 憑證至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="fc0a6-113">Example 3: Add an SSL certificate using KeyVault Secret (versioned secretId) to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultCertificate -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="fc0a6-114">取得機密，並參照到 ， `Add-AzApplicationGatewaySslCertificate` 以將其新增到應用程式閘道，並加上名稱 `Cert01` 。</span><span class="sxs-lookup"><span data-stu-id="fc0a6-114">Get the secret and reference it in the `Add-AzApplicationGatewaySslCertificate` to add it to the Application Gateway with name `Cert01`.</span></span>
<span data-ttu-id="fc0a6-115">注意：如果需要應用程式閘道將憑證與 KeyVault 同步處理，請提供版本較少的 secretId。</span><span class="sxs-lookup"><span data-stu-id="fc0a6-115">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="fc0a6-116">參數</span><span class="sxs-lookup"><span data-stu-id="fc0a6-116">PARAMETERS</span></span>

### <span data-ttu-id="fc0a6-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fc0a6-117">-ApplicationGateway</span></span>
<span data-ttu-id="fc0a6-118">指定此 Cmdlet 新增 SSL 憑證的應用程式閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="fc0a6-118">Specifies the name of application gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="fc0a6-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="fc0a6-119">-CertificateFile</span></span>
<span data-ttu-id="fc0a6-120">指定此 Cmdlet 新增之 SSL 憑證的 .pfx 檔案。</span><span class="sxs-lookup"><span data-stu-id="fc0a6-120">Specifies the .pfx file of an SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="fc0a6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc0a6-121">-DefaultProfile</span></span>
<span data-ttu-id="fc0a6-122">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fc0a6-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc0a6-123">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="fc0a6-123">-KeyVaultSecretId</span></span>
<span data-ttu-id="fc0a6-124">SecretId (KeyVault) 的 uri 密碼。</span><span class="sxs-lookup"><span data-stu-id="fc0a6-124">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="fc0a6-125">當需要使用特定版本的機密時，請使用此選項。</span><span class="sxs-lookup"><span data-stu-id="fc0a6-125">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="fc0a6-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="fc0a6-126">-Name</span></span>
<span data-ttu-id="fc0a6-127">指定此 Cmdlet 新增的 SSL 憑證名稱。</span><span class="sxs-lookup"><span data-stu-id="fc0a6-127">Specifies the name of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="fc0a6-128">-密碼</span><span class="sxs-lookup"><span data-stu-id="fc0a6-128">-Password</span></span>
<span data-ttu-id="fc0a6-129">指定此 Cmdlet 新增的 SSL 憑證密碼。</span><span class="sxs-lookup"><span data-stu-id="fc0a6-129">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="fc0a6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc0a6-130">CommonParameters</span></span>
<span data-ttu-id="fc0a6-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fc0a6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc0a6-132">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="fc0a6-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc0a6-133">輸入</span><span class="sxs-lookup"><span data-stu-id="fc0a6-133">INPUTS</span></span>

### <span data-ttu-id="fc0a6-134">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fc0a6-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fc0a6-135">輸出</span><span class="sxs-lookup"><span data-stu-id="fc0a6-135">OUTPUTS</span></span>

### <span data-ttu-id="fc0a6-136">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fc0a6-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fc0a6-137">筆記</span><span class="sxs-lookup"><span data-stu-id="fc0a6-137">NOTES</span></span>

## <span data-ttu-id="fc0a6-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="fc0a6-138">RELATED LINKS</span></span>

[<span data-ttu-id="fc0a6-139">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="fc0a6-139">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="fc0a6-140">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="fc0a6-140">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="fc0a6-141">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="fc0a6-141">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="fc0a6-142">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="fc0a6-142">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


