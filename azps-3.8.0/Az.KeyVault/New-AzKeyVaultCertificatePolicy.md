---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: b0d690358fb5598b1a88ecb7fe169c8ef3d2718f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966327"
---
# <span data-ttu-id="13c53-101">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="13c53-101">New-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="13c53-102">摘要</span><span class="sxs-lookup"><span data-stu-id="13c53-102">SYNOPSIS</span></span>
<span data-ttu-id="13c53-103">建立記憶體內部的憑證原則物件。</span><span class="sxs-lookup"><span data-stu-id="13c53-103">Creates an in-memory certificate policy object.</span></span>

## <span data-ttu-id="13c53-104">句法</span><span class="sxs-lookup"><span data-stu-id="13c53-104">SYNTAX</span></span>

### <span data-ttu-id="13c53-105">SubjectName (預設) </span><span class="sxs-lookup"><span data-stu-id="13c53-105">SubjectName (Default)</span></span>
```
New-AzKeyVaultCertificatePolicy [-IssuerName] <String> [-SubjectName] <String>
 [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>]
 [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeySize <Int32>] [-KeyNotExportable] [-CertificateTransparency <Boolean>]
 [-Curve <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13c53-106">DNSNames</span><span class="sxs-lookup"><span data-stu-id="13c53-106">DNSNames</span></span>
```
New-AzKeyVaultCertificatePolicy [-IssuerName] <String> [[-SubjectName] <String>]
 [-DnsName] <System.Collections.Generic.List`1[System.String]> [-RenewAtNumberOfDaysBeforeExpiry <Int32>]
 [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeySize <Int32>] [-KeyNotExportable] [-CertificateTransparency <Boolean>]
 [-Curve <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13c53-107">說明</span><span class="sxs-lookup"><span data-stu-id="13c53-107">DESCRIPTION</span></span>
<span data-ttu-id="13c53-108">**新的-AzKeyVaultCertificatePolicy** Cmdlet 會針對 Azure 金鑰保存庫建立記憶體內部憑證原則物件。</span><span class="sxs-lookup"><span data-stu-id="13c53-108">The **New-AzKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="13c53-109">示例</span><span class="sxs-lookup"><span data-stu-id="13c53-109">EXAMPLES</span></span>

### <span data-ttu-id="13c53-110">範例1：建立憑證原則</span><span class="sxs-lookup"><span data-stu-id="13c53-110">Example 1: Create a certificate policy</span></span>
```powershell
PS C:\> New-AzKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal

SecretContentType               : application/x-pkcs12
Kty                             :
KeySize                         : 2048
Curve                           :
Exportable                      :
ReuseKeyOnRenewal               : True
SubjectName                     : CN=contoso.com
DnsNames                        :
KeyUsage                        :
Ekus                            :
ValidityInMonths                : 6
IssuerName                      : Self
CertificateType                 :
RenewAtNumberOfDaysBeforeExpiry :
RenewAtPercentageLifetime       :
EmailAtNumberOfDaysBeforeExpiry :
EmailAtPercentageLifetime       :
CertificateTransparency         :
Enabled                         : True
Created                         :
Updated                         :
```

<span data-ttu-id="13c53-111">這個命令會建立有效期為6個月的憑證原則，並重複使用金鑰來更新憑證。</span><span class="sxs-lookup"><span data-stu-id="13c53-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="13c53-112">參數</span><span class="sxs-lookup"><span data-stu-id="13c53-112">PARAMETERS</span></span>

### <span data-ttu-id="13c53-113">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="13c53-113">-CertificateTransparency</span></span>
<span data-ttu-id="13c53-114">指出是否已針對此憑證/頒發者啟用憑證透明;如果沒有指定，則預設值為 "true"</span><span class="sxs-lookup"><span data-stu-id="13c53-114">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13c53-115">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="13c53-115">-CertificateType</span></span>
<span data-ttu-id="13c53-116">指定發行人的憑證類型。</span><span class="sxs-lookup"><span data-stu-id="13c53-116">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13c53-117">-曲線</span><span class="sxs-lookup"><span data-stu-id="13c53-117">-Curve</span></span>
<span data-ttu-id="13c53-118">指定憑證金鑰的橢圓曲線名稱。</span><span class="sxs-lookup"><span data-stu-id="13c53-118">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="13c53-119">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="13c53-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="13c53-120">P-256</span><span class="sxs-lookup"><span data-stu-id="13c53-120">P-256</span></span>
- <span data-ttu-id="13c53-121">P-384</span><span class="sxs-lookup"><span data-stu-id="13c53-121">P-384</span></span>
- <span data-ttu-id="13c53-122">P-521</span><span class="sxs-lookup"><span data-stu-id="13c53-122">P-521</span></span>
- <span data-ttu-id="13c53-123">P-256K</span><span class="sxs-lookup"><span data-stu-id="13c53-123">P-256K</span></span>
- <span data-ttu-id="13c53-124">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="13c53-124">SECP256K1</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: P-256, P-384, P-521, P-256K, SECP256K1

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13c53-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13c53-125">-DefaultProfile</span></span>
<span data-ttu-id="13c53-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="13c53-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="13c53-127">-已停用</span><span class="sxs-lookup"><span data-stu-id="13c53-127">-Disabled</span></span>
<span data-ttu-id="13c53-128">表示憑證原則已停用。</span><span class="sxs-lookup"><span data-stu-id="13c53-128">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13c53-129">-DnsName</span><span class="sxs-lookup"><span data-stu-id="13c53-129">-DnsName</span></span>
<span data-ttu-id="13c53-130">指定憑證中的 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="13c53-130">Specifies the DNS names in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: DNSNames
Aliases: DnsNames

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13c53-131">-Eku</span><span class="sxs-lookup"><span data-stu-id="13c53-131">-Ekus</span></span>
<span data-ttu-id="13c53-132">指定憑證中 (Eku) 的增強型金鑰用法。</span><span class="sxs-lookup"><span data-stu-id="13c53-132">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13c53-133">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="13c53-133">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="13c53-134">指定自動通知程式開始前的到期天數。</span><span class="sxs-lookup"><span data-stu-id="13c53-134">Specifies how many days before expiry the automatic notification process begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13c53-135">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="13c53-135">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="13c53-136">指定啟動通知自動程式開始的生命週期百分比。</span><span class="sxs-lookup"><span data-stu-id="13c53-136">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13c53-137">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="13c53-137">-IssuerName</span></span>
<span data-ttu-id="13c53-138">指定憑證的頒發者名稱。</span><span class="sxs-lookup"><span data-stu-id="13c53-138">Specifies the name of the issuer for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13c53-139">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="13c53-139">-KeyNotExportable</span></span>
<span data-ttu-id="13c53-140">表示金鑰無法匯出。</span><span class="sxs-lookup"><span data-stu-id="13c53-140">Indicates that the key is not exportable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13c53-141">KeySize</span><span class="sxs-lookup"><span data-stu-id="13c53-141">-KeySize</span></span>
<span data-ttu-id="13c53-142">指定憑證的金鑰大小。</span><span class="sxs-lookup"><span data-stu-id="13c53-142">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="13c53-143">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="13c53-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="13c53-144">2048</span><span class="sxs-lookup"><span data-stu-id="13c53-144">2048</span></span>
- <span data-ttu-id="13c53-145">3072</span><span class="sxs-lookup"><span data-stu-id="13c53-145">3072</span></span>
- <span data-ttu-id="13c53-146">4096</span><span class="sxs-lookup"><span data-stu-id="13c53-146">4096</span></span>
- <span data-ttu-id="13c53-147">256</span><span class="sxs-lookup"><span data-stu-id="13c53-147">256</span></span>
- <span data-ttu-id="13c53-148">384</span><span class="sxs-lookup"><span data-stu-id="13c53-148">384</span></span>
- <span data-ttu-id="13c53-149">521</span><span class="sxs-lookup"><span data-stu-id="13c53-149">521</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:
Accepted values: 2048, 3072, 4096, 256, 384, 521

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13c53-150">-KeyType</span><span class="sxs-lookup"><span data-stu-id="13c53-150">-KeyType</span></span>
<span data-ttu-id="13c53-151">指定支援憑證之金鑰的金鑰類型。</span><span class="sxs-lookup"><span data-stu-id="13c53-151">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="13c53-152">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="13c53-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="13c53-153">與眾不同</span><span class="sxs-lookup"><span data-stu-id="13c53-153">RSA</span></span>
- <span data-ttu-id="13c53-154">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="13c53-154">RSA-HSM</span></span>
- <span data-ttu-id="13c53-155">成員國</span><span class="sxs-lookup"><span data-stu-id="13c53-155">EC</span></span>
- <span data-ttu-id="13c53-156">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="13c53-156">EC-HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM, EC, EC-HSM

Required: False
Position: Named
Default value: RSA
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13c53-157">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="13c53-157">-KeyUsage</span></span>
<span data-ttu-id="13c53-158">指定憑證中的金鑰用法。</span><span class="sxs-lookup"><span data-stu-id="13c53-158">Specifies the key usages in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]
Parameter Sets: (All)
Aliases:
Accepted values: None, EncipherOnly, CrlSign, KeyCertSign, KeyAgreement, DataEncipherment, KeyEncipherment, NonRepudiation, DigitalSignature, DecipherOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13c53-159">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="13c53-159">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="13c53-160">指定到期前的天數，在此之後，就會開始更新自動程式。</span><span class="sxs-lookup"><span data-stu-id="13c53-160">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13c53-161">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="13c53-161">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="13c53-162">指定啟動證書自動程式開始前的生命週期百分比。</span><span class="sxs-lookup"><span data-stu-id="13c53-162">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13c53-163">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="13c53-163">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="13c53-164">表示憑證在續約時重複使用金鑰。</span><span class="sxs-lookup"><span data-stu-id="13c53-164">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13c53-165">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="13c53-165">-SecretContentType</span></span>
<span data-ttu-id="13c53-166">指定新的主要電子倉庫密碼的內容類型。</span><span class="sxs-lookup"><span data-stu-id="13c53-166">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="13c53-167">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="13c53-167">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="13c53-168">應用程式/x-pkcs12</span><span class="sxs-lookup"><span data-stu-id="13c53-168">application/x-pkcs12</span></span>
- <span data-ttu-id="13c53-169">應用程式/x pem-檔案</span><span class="sxs-lookup"><span data-stu-id="13c53-169">application/x-pem-file</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13c53-170">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="13c53-170">-SubjectName</span></span>
<span data-ttu-id="13c53-171">指定憑證的受領人名稱。</span><span class="sxs-lookup"><span data-stu-id="13c53-171">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: SubjectName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DNSNames
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13c53-172">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="13c53-172">-ValidityInMonths</span></span>
<span data-ttu-id="13c53-173">指定憑證有效的月份數。</span><span class="sxs-lookup"><span data-stu-id="13c53-173">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13c53-174">-確認</span><span class="sxs-lookup"><span data-stu-id="13c53-174">-Confirm</span></span>
<span data-ttu-id="13c53-175">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="13c53-175">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13c53-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13c53-176">-WhatIf</span></span>
<span data-ttu-id="13c53-177">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="13c53-177">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13c53-178">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="13c53-178">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13c53-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13c53-179">CommonParameters</span></span>
<span data-ttu-id="13c53-180">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="13c53-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13c53-181">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="13c53-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13c53-182">輸入</span><span class="sxs-lookup"><span data-stu-id="13c53-182">INPUTS</span></span>

### <span data-ttu-id="13c53-183">System.object</span><span class="sxs-lookup"><span data-stu-id="13c53-183">System.String</span></span>

### <span data-ttu-id="13c53-184">[System.object]。清單 ' 1 [CoreLib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="13c53-184">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="13c53-185">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="13c53-185">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="13c53-186">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="13c53-186">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="13c53-187">[System.object]。清單 ' 1 [X509Certificates. X509KeyUsageFlags，系統. X509Certificates，版本 = 4.2.1.0，Culture = 中性，PublicKeyToken = b03f5f7f11d50a3a]]。</span><span class="sxs-lookup"><span data-stu-id="13c53-187">System.Collections.Generic.List\`1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System.Security.Cryptography.X509Certificates, Version=4.2.1.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a]]</span></span>

## <span data-ttu-id="13c53-188">輸出</span><span class="sxs-lookup"><span data-stu-id="13c53-188">OUTPUTS</span></span>

### <span data-ttu-id="13c53-189">PSKeyVaultCertificatePolicy 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="13c53-189">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="13c53-190">筆記</span><span class="sxs-lookup"><span data-stu-id="13c53-190">NOTES</span></span>

## <span data-ttu-id="13c53-191">相關連結</span><span class="sxs-lookup"><span data-stu-id="13c53-191">RELATED LINKS</span></span>

[<span data-ttu-id="13c53-192">AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="13c53-192">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="13c53-193">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="13c53-193">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

