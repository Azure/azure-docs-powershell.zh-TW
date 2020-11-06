---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EC4C642-1D23-4699-AE00-6E180C38271E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 7dddb6a5b38414d658cc405820327c0d6df43a6c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622174"
---
# <span data-ttu-id="0e2b1-101">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0e2b1-101">Add-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="0e2b1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0e2b1-102">SYNOPSIS</span></span>
<span data-ttu-id="0e2b1-103">將 SSL 憑證新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="0e2b1-103">Adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="0e2b1-104">句法</span><span class="sxs-lookup"><span data-stu-id="0e2b1-104">SYNTAX</span></span>

```
Add-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e2b1-105">說明</span><span class="sxs-lookup"><span data-stu-id="0e2b1-105">DESCRIPTION</span></span>
<span data-ttu-id="0e2b1-106">**載入 AzApplicationGatewaySslCertificate** Cmdlet 會將 SSL 憑證新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="0e2b1-106">The **Add-AzApplicationGatewaySslCertificate** cmdlet adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="0e2b1-107">示例</span><span class="sxs-lookup"><span data-stu-id="0e2b1-107">EXAMPLES</span></span>

### <span data-ttu-id="0e2b1-108">範例1：使用 pfx 將 SSL 憑證新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="0e2b1-108">Example 1: Add an SSL certificate using pfx to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="0e2b1-109">這個命令會取得名為 ApplicationGateway01 的應用程式閘道，然後將名為 Cert01 的 SSL 憑證新增至它。</span><span class="sxs-lookup"><span data-stu-id="0e2b1-109">This command gets an application gateway named ApplicationGateway01 and then adds an SSL certificate named Cert01 to it.</span></span>

### <span data-ttu-id="0e2b1-110">範例2：使用 KeyVault 機密新增 SSL 憑證 (版本不足的 secretId) 到應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="0e2b1-110">Example 2: Add an SSL certificate using KeyVault Secret (version-less secretId) to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="0e2b1-111">在中取得機密並加以參照， `Add-AzApplicationGatewaySslCertificate` 即可將名稱新增到應用程式閘道 `Cert01` 。</span><span class="sxs-lookup"><span data-stu-id="0e2b1-111">Get the secret and reference it in the `Add-AzApplicationGatewaySslCertificate` to add it to the Application Gateway with name `Cert01`.</span></span>
<span data-ttu-id="0e2b1-112">注意：在這裡提供版本較少的 secretId，應用程式閘道會以定期間隔與 KeyVault 同步處理憑證。</span><span class="sxs-lookup"><span data-stu-id="0e2b1-112">Note: As version-less secretId is provided here, Application Gateway will sync the certificate in regular intervals with the KeyVault.</span></span>

### <span data-ttu-id="0e2b1-113">範例3：使用 KeyVault (版本控制 secretId) 將 SSL 憑證新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="0e2b1-113">Example 3: Add an SSL certificate using KeyVault Secret (versioned secretId) to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="0e2b1-114">在中取得機密並加以參照， `Add-AzApplicationGatewaySslCertificate` 即可將名稱新增到應用程式閘道 `Cert01` 。</span><span class="sxs-lookup"><span data-stu-id="0e2b1-114">Get the secret and reference it in the `Add-AzApplicationGatewaySslCertificate` to add it to the Application Gateway with name `Cert01`.</span></span>
<span data-ttu-id="0e2b1-115">注意：如果應用程式閘道需要使用 KeyVault 同步處理憑證，請提供版本較少的 secretId。</span><span class="sxs-lookup"><span data-stu-id="0e2b1-115">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="0e2b1-116">參數</span><span class="sxs-lookup"><span data-stu-id="0e2b1-116">PARAMETERS</span></span>

### <span data-ttu-id="0e2b1-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0e2b1-117">-ApplicationGateway</span></span>
<span data-ttu-id="0e2b1-118">指定此 Cmdlet 新增 SSL 憑證之應用程式閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e2b1-118">Specifies the name of application gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="0e2b1-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="0e2b1-119">-CertificateFile</span></span>
<span data-ttu-id="0e2b1-120">指定此 Cmdlet 所新增之 SSL 憑證的 .pfx 檔案。</span><span class="sxs-lookup"><span data-stu-id="0e2b1-120">Specifies the .pfx file of an SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="0e2b1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e2b1-121">-DefaultProfile</span></span>
<span data-ttu-id="0e2b1-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0e2b1-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e2b1-123">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="0e2b1-123">-KeyVaultSecretId</span></span>
<span data-ttu-id="0e2b1-124">SecretId KeyVault 密碼的 (uri) 。</span><span class="sxs-lookup"><span data-stu-id="0e2b1-124">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="0e2b1-125">當需要使用特定的機密版本時，請使用這個選項。</span><span class="sxs-lookup"><span data-stu-id="0e2b1-125">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="0e2b1-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="0e2b1-126">-Name</span></span>
<span data-ttu-id="0e2b1-127">指定此 Cmdlet 所新增之 SSL 憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e2b1-127">Specifies the name of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="0e2b1-128">-Password</span><span class="sxs-lookup"><span data-stu-id="0e2b1-128">-Password</span></span>
<span data-ttu-id="0e2b1-129">指定此 Cmdlet 所新增之 SSL 憑證的密碼。</span><span class="sxs-lookup"><span data-stu-id="0e2b1-129">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="0e2b1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e2b1-130">CommonParameters</span></span>
<span data-ttu-id="0e2b1-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0e2b1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e2b1-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0e2b1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e2b1-133">輸入</span><span class="sxs-lookup"><span data-stu-id="0e2b1-133">INPUTS</span></span>

### <span data-ttu-id="0e2b1-134">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0e2b1-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0e2b1-135">輸出</span><span class="sxs-lookup"><span data-stu-id="0e2b1-135">OUTPUTS</span></span>

### <span data-ttu-id="0e2b1-136">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0e2b1-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0e2b1-137">筆記</span><span class="sxs-lookup"><span data-stu-id="0e2b1-137">NOTES</span></span>

## <span data-ttu-id="0e2b1-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="0e2b1-138">RELATED LINKS</span></span>

[<span data-ttu-id="0e2b1-139">AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0e2b1-139">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="0e2b1-140">新-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0e2b1-140">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="0e2b1-141">移除-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0e2b1-141">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="0e2b1-142">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0e2b1-142">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


