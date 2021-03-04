---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/powershell/module/az.keyvault/new-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: af35cef768c668663b68cfd4a21e473109883aec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914782"
---
# <span data-ttu-id="f9ee7-101">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f9ee7-101">New-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="f9ee7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f9ee7-102">SYNOPSIS</span></span>
<span data-ttu-id="f9ee7-103">建立記憶體內憑證策略物件。</span><span class="sxs-lookup"><span data-stu-id="f9ee7-103">Creates an in-memory certificate policy object.</span></span>

## <span data-ttu-id="f9ee7-104">語法</span><span class="sxs-lookup"><span data-stu-id="f9ee7-104">SYNTAX</span></span>

### <span data-ttu-id="f9ee7-105">SubjectName (預設) </span><span class="sxs-lookup"><span data-stu-id="f9ee7-105">SubjectName (Default)</span></span>
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

### <span data-ttu-id="f9ee7-106">DNSNames</span><span class="sxs-lookup"><span data-stu-id="f9ee7-106">DNSNames</span></span>
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

## <span data-ttu-id="f9ee7-107">描述</span><span class="sxs-lookup"><span data-stu-id="f9ee7-107">DESCRIPTION</span></span>
<span data-ttu-id="f9ee7-108">**New-AzKeyVaultCertificatePolidlet** 會為 Azure Key Vault 建立記憶體內憑證策略物件。</span><span class="sxs-lookup"><span data-stu-id="f9ee7-108">The **New-AzKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="f9ee7-109">例子</span><span class="sxs-lookup"><span data-stu-id="f9ee7-109">EXAMPLES</span></span>

### <span data-ttu-id="f9ee7-110">範例 1：建立憑證策略</span><span class="sxs-lookup"><span data-stu-id="f9ee7-110">Example 1: Create a certificate policy</span></span>
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

<span data-ttu-id="f9ee7-111">此命令會建立有效六個月的憑證策略，並重複使用金鑰以更新憑證。</span><span class="sxs-lookup"><span data-stu-id="f9ee7-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

### <span data-ttu-id="f9ee7-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="f9ee7-112">Example 2</span></span>

<span data-ttu-id="f9ee7-113">建立記憶體內憑證策略物件。</span><span class="sxs-lookup"><span data-stu-id="f9ee7-113">Creates an in-memory certificate policy object.</span></span> <span data-ttu-id="f9ee7-114"> (自動) </span><span class="sxs-lookup"><span data-stu-id="f9ee7-114">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzKeyVaultCertificatePolicy -IssuerName 'Self' -KeyType RSA -RenewAtNumberOfDaysBeforeExpiry <Int32> -SecretContentType application/x-pkcs12 -SubjectName 'CN=contoso.com' -ValidityInMonths 6
```

### <span data-ttu-id="f9ee7-115">範例 3：建立主題替代 (或 SAN) 憑證</span><span class="sxs-lookup"><span data-stu-id="f9ee7-115">Example 3: Create a Subject Alternate Name (or SAN) certificate</span></span>

```powershell
PS C:\> New-AzKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -DnsName "contoso.com","support.contoso.com","docs.contoso.com" -IssuerName "Self"

SecretContentType               : application/x-pkcs12
Kty                             : RSA
KeySize                         : 2048
Curve                           :
Exportable                      :
ReuseKeyOnRenewal               : False
SubjectName                     : CN=contoso.com
DnsNames                        : {contoso.com, support.contoso.com, docs.contoso.com}
KeyUsage                        :
Ekus                            :
ValidityInMonths                :
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

<span data-ttu-id="f9ee7-116">此範例會建立一個包含 3 個 DNS 名稱的 SAN 憑證。</span><span class="sxs-lookup"><span data-stu-id="f9ee7-116">This example creates a SAN certificate with 3 DNS names.</span></span>

## <span data-ttu-id="f9ee7-117">參數</span><span class="sxs-lookup"><span data-stu-id="f9ee7-117">PARAMETERS</span></span>

### <span data-ttu-id="f9ee7-118">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="f9ee7-118">-CertificateTransparency</span></span>
<span data-ttu-id="f9ee7-119">指出此憑證/發行者是否已啟用憑證透明度;如果未指定，預設值為 "true"</span><span class="sxs-lookup"><span data-stu-id="f9ee7-119">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

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

### <span data-ttu-id="f9ee7-120">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="f9ee7-120">-CertificateType</span></span>
<span data-ttu-id="f9ee7-121">指定發行者憑證的類型。</span><span class="sxs-lookup"><span data-stu-id="f9ee7-121">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="f9ee7-122">-曲線</span><span class="sxs-lookup"><span data-stu-id="f9ee7-122">-Curve</span></span>
<span data-ttu-id="f9ee7-123">指定憑證金鑰的省略號曲線名稱。</span><span class="sxs-lookup"><span data-stu-id="f9ee7-123">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="f9ee7-124">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="f9ee7-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f9ee7-125">P-256</span><span class="sxs-lookup"><span data-stu-id="f9ee7-125">P-256</span></span>
- <span data-ttu-id="f9ee7-126">P-384</span><span class="sxs-lookup"><span data-stu-id="f9ee7-126">P-384</span></span>
- <span data-ttu-id="f9ee7-127">P-521</span><span class="sxs-lookup"><span data-stu-id="f9ee7-127">P-521</span></span>
- <span data-ttu-id="f9ee7-128">P-256K</span><span class="sxs-lookup"><span data-stu-id="f9ee7-128">P-256K</span></span>
- <span data-ttu-id="f9ee7-129">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="f9ee7-129">SECP256K1</span></span>

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

### <span data-ttu-id="f9ee7-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9ee7-130">-DefaultProfile</span></span>
<span data-ttu-id="f9ee7-131">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="f9ee7-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f9ee7-132">-已停用</span><span class="sxs-lookup"><span data-stu-id="f9ee7-132">-Disabled</span></span>
<span data-ttu-id="f9ee7-133">表示憑證策略已停用。</span><span class="sxs-lookup"><span data-stu-id="f9ee7-133">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="f9ee7-134">-DnsName</span><span class="sxs-lookup"><span data-stu-id="f9ee7-134">-DnsName</span></span>
<span data-ttu-id="f9ee7-135">指定憑證中的 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="f9ee7-135">Specifies the DNS names in the certificate.</span></span> <span data-ttu-id="f9ee7-136">主題替代名稱 (SAN) 可指定為 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="f9ee7-136">Subject Alternative Names (SANs) can be specified as DNS names.</span></span>

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

### <span data-ttu-id="f9ee7-137">-EKUs</span><span class="sxs-lookup"><span data-stu-id="f9ee7-137">-Ekus</span></span>
<span data-ttu-id="f9ee7-138">指定憑證中 (EKUS) 的增強金鑰使用量。</span><span class="sxs-lookup"><span data-stu-id="f9ee7-138">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="f9ee7-139">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="f9ee7-139">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="f9ee7-140">指定自動通知程式開始前幾天。</span><span class="sxs-lookup"><span data-stu-id="f9ee7-140">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="f9ee7-141">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="f9ee7-141">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="f9ee7-142">指定通知自動程式開始後的生命週期百分比。</span><span class="sxs-lookup"><span data-stu-id="f9ee7-142">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="f9ee7-143">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="f9ee7-143">-IssuerName</span></span>
<span data-ttu-id="f9ee7-144">指定憑證的發行者名稱。</span><span class="sxs-lookup"><span data-stu-id="f9ee7-144">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="f9ee7-145">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="f9ee7-145">-KeyNotExportable</span></span>
<span data-ttu-id="f9ee7-146">表示無法匯出金鑰。</span><span class="sxs-lookup"><span data-stu-id="f9ee7-146">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="f9ee7-147">-KeySize</span><span class="sxs-lookup"><span data-stu-id="f9ee7-147">-KeySize</span></span>
<span data-ttu-id="f9ee7-148">指定憑證的金鑰大小。</span><span class="sxs-lookup"><span data-stu-id="f9ee7-148">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="f9ee7-149">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="f9ee7-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f9ee7-150">2048</span><span class="sxs-lookup"><span data-stu-id="f9ee7-150">2048</span></span>
- <span data-ttu-id="f9ee7-151">3072</span><span class="sxs-lookup"><span data-stu-id="f9ee7-151">3072</span></span>
- <span data-ttu-id="f9ee7-152">4096</span><span class="sxs-lookup"><span data-stu-id="f9ee7-152">4096</span></span>
- <span data-ttu-id="f9ee7-153">256</span><span class="sxs-lookup"><span data-stu-id="f9ee7-153">256</span></span>
- <span data-ttu-id="f9ee7-154">384</span><span class="sxs-lookup"><span data-stu-id="f9ee7-154">384</span></span>
- <span data-ttu-id="f9ee7-155">521</span><span class="sxs-lookup"><span data-stu-id="f9ee7-155">521</span></span>

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

### <span data-ttu-id="f9ee7-156">-KeyType</span><span class="sxs-lookup"><span data-stu-id="f9ee7-156">-KeyType</span></span>
<span data-ttu-id="f9ee7-157">指定支援憑證之金鑰的金鑰類型。</span><span class="sxs-lookup"><span data-stu-id="f9ee7-157">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="f9ee7-158">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="f9ee7-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f9ee7-159">Rsa</span><span class="sxs-lookup"><span data-stu-id="f9ee7-159">RSA</span></span>
- <span data-ttu-id="f9ee7-160">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="f9ee7-160">RSA-HSM</span></span>
- <span data-ttu-id="f9ee7-161">電子商務</span><span class="sxs-lookup"><span data-stu-id="f9ee7-161">EC</span></span>
- <span data-ttu-id="f9ee7-162">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="f9ee7-162">EC-HSM</span></span>

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

### <span data-ttu-id="f9ee7-163">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="f9ee7-163">-KeyUsage</span></span>
<span data-ttu-id="f9ee7-164">指定憑證中的重要使用量。</span><span class="sxs-lookup"><span data-stu-id="f9ee7-164">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="f9ee7-165">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="f9ee7-165">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="f9ee7-166">指定憑證續約的自動程式開始前的天數。</span><span class="sxs-lookup"><span data-stu-id="f9ee7-166">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="f9ee7-167">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="f9ee7-167">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="f9ee7-168">指定憑證續約的自動程式開始後的生命週期百分比。</span><span class="sxs-lookup"><span data-stu-id="f9ee7-168">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="f9ee7-169">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="f9ee7-169">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="f9ee7-170">表示憑證在續約期間重複使用金鑰。</span><span class="sxs-lookup"><span data-stu-id="f9ee7-170">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="f9ee7-171">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="f9ee7-171">-SecretContentType</span></span>
<span data-ttu-id="f9ee7-172">指定新金鑰庫機密的內容類型。</span><span class="sxs-lookup"><span data-stu-id="f9ee7-172">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="f9ee7-173">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="f9ee7-173">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f9ee7-174">application/x-pkcs12</span><span class="sxs-lookup"><span data-stu-id="f9ee7-174">application/x-pkcs12</span></span>
- <span data-ttu-id="f9ee7-175">application/x-pem-file</span><span class="sxs-lookup"><span data-stu-id="f9ee7-175">application/x-pem-file</span></span>

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

### <span data-ttu-id="f9ee7-176">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="f9ee7-176">-SubjectName</span></span>
<span data-ttu-id="f9ee7-177">指定憑證的主體名稱。</span><span class="sxs-lookup"><span data-stu-id="f9ee7-177">Specifies the subject name of the certificate.</span></span> 

> [!NOTE]
> <span data-ttu-id="f9ee7-178">如果您必須在參數的屬性內使用逗號 (、) 或句號 (.) ，則必須以引號括住 `SubjectName` 屬性欄位。</span><span class="sxs-lookup"><span data-stu-id="f9ee7-178">If you must use a comma (,) or a period (.) within a property in the `SubjectName` parameter, you must enclose the property field in quotation marks.</span></span> <span data-ttu-id="f9ee7-179">例如，您可以使用 O="Contoso， Ltd."</span><span class="sxs-lookup"><span data-stu-id="f9ee7-179">For example, you may use O="Contoso, Ltd."</span></span> <span data-ttu-id="f9ee7-180">在組織名稱欄位中。</span><span class="sxs-lookup"><span data-stu-id="f9ee7-180">in the Organization Name field.</span></span>

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

### <span data-ttu-id="f9ee7-181">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="f9ee7-181">-ValidityInMonths</span></span>
<span data-ttu-id="f9ee7-182">指定憑證有效的月數。</span><span class="sxs-lookup"><span data-stu-id="f9ee7-182">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="f9ee7-183">-確認</span><span class="sxs-lookup"><span data-stu-id="f9ee7-183">-Confirm</span></span>
<span data-ttu-id="f9ee7-184">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f9ee7-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9ee7-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9ee7-185">-WhatIf</span></span>
<span data-ttu-id="f9ee7-186">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f9ee7-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9ee7-187">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f9ee7-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9ee7-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9ee7-188">CommonParameters</span></span>
<span data-ttu-id="f9ee7-189">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f9ee7-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9ee7-190">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f9ee7-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9ee7-191">輸入</span><span class="sxs-lookup"><span data-stu-id="f9ee7-191">INPUTS</span></span>

### <span data-ttu-id="f9ee7-192">System.String</span><span class="sxs-lookup"><span data-stu-id="f9ee7-192">System.String</span></span>

### <span data-ttu-id="f9ee7-193">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f9ee7-193">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f9ee7-194">System.Nullable'1[[System.Int32， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f9ee7-194">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f9ee7-195">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f9ee7-195">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="f9ee7-196">System.Collections.Generic.List'1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags， System.Security.Cryptography.X509Certificates， Version=4.2.1.0， Culture=neutral， PublicKeyToken=b03f5f7f11d50a3a]]</span><span class="sxs-lookup"><span data-stu-id="f9ee7-196">System.Collections.Generic.List\`1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System.Security.Cryptography.X509Certificates, Version=4.2.1.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a]]</span></span>

## <span data-ttu-id="f9ee7-197">輸出</span><span class="sxs-lookup"><span data-stu-id="f9ee7-197">OUTPUTS</span></span>

### <span data-ttu-id="f9ee7-198">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f9ee7-198">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="f9ee7-199">筆記</span><span class="sxs-lookup"><span data-stu-id="f9ee7-199">NOTES</span></span>

## <span data-ttu-id="f9ee7-200">相關連結</span><span class="sxs-lookup"><span data-stu-id="f9ee7-200">RELATED LINKS</span></span>

[<span data-ttu-id="f9ee7-201">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f9ee7-201">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="f9ee7-202">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f9ee7-202">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

