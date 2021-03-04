---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 84465161d726108749e09d4a928e22aea8050c92
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917686"
---
# <span data-ttu-id="e5d01-101">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e5d01-101">New-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="e5d01-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e5d01-102">SYNOPSIS</span></span>
<span data-ttu-id="e5d01-103">為 Azure 應用程式閘道建立 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="e5d01-103">Creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="e5d01-104">語法</span><span class="sxs-lookup"><span data-stu-id="e5d01-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslCertificate -Name <String> [-CertificateFile <String>] [-Password <SecureString>]
 [-KeyVaultSecretId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5d01-105">描述</span><span class="sxs-lookup"><span data-stu-id="e5d01-105">DESCRIPTION</span></span>
<span data-ttu-id="e5d01-106">**New-AzApplicationGatewaySslCertificate** Cmdlet 會為 Azure 應用程式閘道建立 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="e5d01-106">The **New-AzApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="e5d01-107">例子</span><span class="sxs-lookup"><span data-stu-id="e5d01-107">EXAMPLES</span></span>

### <span data-ttu-id="e5d01-108">範例 1：建立 Azure 應用程式閘道的 SSL 憑證。</span><span class="sxs-lookup"><span data-stu-id="e5d01-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\> $password = ConvertTo-SecureString $passwordPlainString -AsPlainText -Force
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="e5d01-109">此命令會為預設應用程式閘道建立名為 Cert01 的 SSL 憑證，並儲存在名為 $Cert 的變數中。</span><span class="sxs-lookup"><span data-stu-id="e5d01-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

### <span data-ttu-id="e5d01-110">範例 2：使用 KeyVault Secret (version-less secretId) 建立 SSL 憑證，並新增到應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="e5d01-110">Example 2: Create an SSL certificate using KeyVault Secret (version-less secretId) and add to an application gateway.</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="e5d01-111">取得秘訣，然後使用 建立 SSL 憑證 `New-AzApplicationGatewaySslCertificate` 。</span><span class="sxs-lookup"><span data-stu-id="e5d01-111">Get the secret and create an SSL Certificate using `New-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="e5d01-112">注意：由於此處提供版本較少的 secretId，應用程式閘道會定期與 KeyVault 同步處理憑證。</span><span class="sxs-lookup"><span data-stu-id="e5d01-112">Note: As version-less secretId is provided here, Application Gateway will sync the certificate in regular intervals with the KeyVault.</span></span>

### <span data-ttu-id="e5d01-113">範例 3：使用 KeyVault Secret 建立 SSL 憑證，並新增到應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="e5d01-113">Example 3: Create an SSL certificate using KeyVault Secret and add to an Application Gateway.</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="e5d01-114">取得秘訣，然後使用 建立 SSL 憑證 `New-AzApplicationGatewaySslCertificate` 。</span><span class="sxs-lookup"><span data-stu-id="e5d01-114">Get the secret and create an SSL Certificate using `New-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="e5d01-115">注意：如果需要應用程式閘道將憑證與 KeyVault 同步處理，請提供版本較少的 secretId。</span><span class="sxs-lookup"><span data-stu-id="e5d01-115">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="e5d01-116">參數</span><span class="sxs-lookup"><span data-stu-id="e5d01-116">PARAMETERS</span></span>

### <span data-ttu-id="e5d01-117">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="e5d01-117">-CertificateFile</span></span>
<span data-ttu-id="e5d01-118">指定此 Cmdlet 所建立之 SSL 憑證的 .pfx 檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="e5d01-118">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="e5d01-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5d01-119">-DefaultProfile</span></span>
<span data-ttu-id="e5d01-120">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e5d01-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5d01-121">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="e5d01-121">-KeyVaultSecretId</span></span>
<span data-ttu-id="e5d01-122">SecretId (KeyVault) 的 uri 密碼。</span><span class="sxs-lookup"><span data-stu-id="e5d01-122">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="e5d01-123">當需要使用特定版本的機密時，請使用此選項。</span><span class="sxs-lookup"><span data-stu-id="e5d01-123">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="e5d01-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="e5d01-124">-Name</span></span>
<span data-ttu-id="e5d01-125">指定此 Cmdlet 所建立之 SSL 憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5d01-125">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="e5d01-126">-密碼</span><span class="sxs-lookup"><span data-stu-id="e5d01-126">-Password</span></span>
<span data-ttu-id="e5d01-127">指定此 Cmdlet 所建立之 SSL 的密碼。</span><span class="sxs-lookup"><span data-stu-id="e5d01-127">Specifies the password of the SSL that this cmdlet creates.</span></span>

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

### <span data-ttu-id="e5d01-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5d01-128">CommonParameters</span></span>
<span data-ttu-id="e5d01-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e5d01-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5d01-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="e5d01-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5d01-131">輸入</span><span class="sxs-lookup"><span data-stu-id="e5d01-131">INPUTS</span></span>

### <span data-ttu-id="e5d01-132">沒有</span><span class="sxs-lookup"><span data-stu-id="e5d01-132">None</span></span>

## <span data-ttu-id="e5d01-133">輸出</span><span class="sxs-lookup"><span data-stu-id="e5d01-133">OUTPUTS</span></span>

### <span data-ttu-id="e5d01-134">Microsoft.Azure.Commands.Network.models.PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e5d01-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="e5d01-135">筆記</span><span class="sxs-lookup"><span data-stu-id="e5d01-135">NOTES</span></span>

## <span data-ttu-id="e5d01-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5d01-136">RELATED LINKS</span></span>

[<span data-ttu-id="e5d01-137">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e5d01-137">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e5d01-138">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e5d01-138">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e5d01-139">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e5d01-139">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e5d01-140">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e5d01-140">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


