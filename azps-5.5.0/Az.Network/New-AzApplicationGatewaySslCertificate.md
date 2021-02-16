---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 31d9c5d5c627f4d3451c47584b09760655e77342
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100135862"
---
# <span data-ttu-id="cd791-101">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cd791-101">New-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="cd791-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cd791-102">SYNOPSIS</span></span>
<span data-ttu-id="cd791-103">建立 Azure 應用程式閘道的 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="cd791-103">Creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="cd791-104">句法</span><span class="sxs-lookup"><span data-stu-id="cd791-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslCertificate -Name <String> [-CertificateFile <String>] [-Password <SecureString>]
 [-KeyVaultSecretId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd791-105">說明</span><span class="sxs-lookup"><span data-stu-id="cd791-105">DESCRIPTION</span></span>
<span data-ttu-id="cd791-106">**新的 AzApplicationGatewaySslCertificate** Cmdlet 會建立 Azure 應用程式閘道的 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="cd791-106">The **New-AzApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="cd791-107">示例</span><span class="sxs-lookup"><span data-stu-id="cd791-107">EXAMPLES</span></span>

### <span data-ttu-id="cd791-108">範例1：建立 Azure 應用程式閘道的 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="cd791-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\> $password = ConvertTo-SecureString $passwordPlainString -AsPlainText -Force
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="cd791-109">這個命令會建立名為 Cert01 的 SSL 憑證，以用於預設的應用程式閘道，並將結果儲存在名為 $Cert 的變數中。</span><span class="sxs-lookup"><span data-stu-id="cd791-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

### <span data-ttu-id="cd791-110">範例2：使用 KeyVault 機密建立 SSL 憑證 (版本較少的 secretId) 並新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="cd791-110">Example 2: Create an SSL certificate using KeyVault Secret (version-less secretId) and add to an application gateway.</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="cd791-111">取得密碼並使用建立 SSL 憑證 `New-AzApplicationGatewaySslCertificate` 。</span><span class="sxs-lookup"><span data-stu-id="cd791-111">Get the secret and create an SSL Certificate using `New-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="cd791-112">注意：在這裡提供版本較少的 secretId，應用程式閘道會以定期間隔與 KeyVault 同步處理憑證。</span><span class="sxs-lookup"><span data-stu-id="cd791-112">Note: As version-less secretId is provided here, Application Gateway will sync the certificate in regular intervals with the KeyVault.</span></span>

### <span data-ttu-id="cd791-113">範例3：使用 KeyVault 機密建立 SSL 憑證並新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="cd791-113">Example 3: Create an SSL certificate using KeyVault Secret and add to an Application Gateway.</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="cd791-114">取得密碼並使用建立 SSL 憑證 `New-AzApplicationGatewaySslCertificate` 。</span><span class="sxs-lookup"><span data-stu-id="cd791-114">Get the secret and create an SSL Certificate using `New-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="cd791-115">注意：如果應用程式閘道需要使用 KeyVault 同步處理憑證，請提供版本較少的 secretId。</span><span class="sxs-lookup"><span data-stu-id="cd791-115">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="cd791-116">參數</span><span class="sxs-lookup"><span data-stu-id="cd791-116">PARAMETERS</span></span>

### <span data-ttu-id="cd791-117">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="cd791-117">-CertificateFile</span></span>
<span data-ttu-id="cd791-118">指定此 Cmdlet 建立之 SSL 憑證之 .pfx 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="cd791-118">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="cd791-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd791-119">-DefaultProfile</span></span>
<span data-ttu-id="cd791-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cd791-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd791-121">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="cd791-121">-KeyVaultSecretId</span></span>
<span data-ttu-id="cd791-122">SecretId KeyVault 密碼的 (uri) 。</span><span class="sxs-lookup"><span data-stu-id="cd791-122">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="cd791-123">當需要使用特定的機密版本時，請使用這個選項。</span><span class="sxs-lookup"><span data-stu-id="cd791-123">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="cd791-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="cd791-124">-Name</span></span>
<span data-ttu-id="cd791-125">指定此 Cmdlet 所建立之 SSL 憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="cd791-125">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="cd791-126">-Password</span><span class="sxs-lookup"><span data-stu-id="cd791-126">-Password</span></span>
<span data-ttu-id="cd791-127">指定此 Cmdlet 所建立之 SSL 的密碼。</span><span class="sxs-lookup"><span data-stu-id="cd791-127">Specifies the password of the SSL that this cmdlet creates.</span></span>

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

### <span data-ttu-id="cd791-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd791-128">CommonParameters</span></span>
<span data-ttu-id="cd791-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cd791-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd791-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cd791-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd791-131">輸入</span><span class="sxs-lookup"><span data-stu-id="cd791-131">INPUTS</span></span>

### <span data-ttu-id="cd791-132">所有</span><span class="sxs-lookup"><span data-stu-id="cd791-132">None</span></span>

## <span data-ttu-id="cd791-133">輸出</span><span class="sxs-lookup"><span data-stu-id="cd791-133">OUTPUTS</span></span>

### <span data-ttu-id="cd791-134">PSApplicationGatewaySslCertificate 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="cd791-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="cd791-135">筆記</span><span class="sxs-lookup"><span data-stu-id="cd791-135">NOTES</span></span>

## <span data-ttu-id="cd791-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="cd791-136">RELATED LINKS</span></span>

[<span data-ttu-id="cd791-137">附加 AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cd791-137">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="cd791-138">AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cd791-138">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="cd791-139">移除-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cd791-139">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="cd791-140">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cd791-140">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


