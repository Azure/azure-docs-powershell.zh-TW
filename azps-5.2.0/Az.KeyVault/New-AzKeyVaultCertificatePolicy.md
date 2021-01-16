---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 370662b1d24f9b5b71653506be7a3add5a3801f8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98283524"
---
# <span data-ttu-id="85f50-101">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="85f50-101">New-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="85f50-102">摘要</span><span class="sxs-lookup"><span data-stu-id="85f50-102">SYNOPSIS</span></span>
<span data-ttu-id="85f50-103">建立記憶體內部的憑證原則物件。</span><span class="sxs-lookup"><span data-stu-id="85f50-103">Creates an in-memory certificate policy object.</span></span>

## <span data-ttu-id="85f50-104">句法</span><span class="sxs-lookup"><span data-stu-id="85f50-104">SYNTAX</span></span>

### <span data-ttu-id="85f50-105">SubjectName (預設) </span><span class="sxs-lookup"><span data-stu-id="85f50-105">SubjectName (Default)</span></span>
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

### <span data-ttu-id="85f50-106">DNSNames</span><span class="sxs-lookup"><span data-stu-id="85f50-106">DNSNames</span></span>
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

## <span data-ttu-id="85f50-107">說明</span><span class="sxs-lookup"><span data-stu-id="85f50-107">DESCRIPTION</span></span>
<span data-ttu-id="85f50-108">**新的-AzKeyVaultCertificatePolicy** Cmdlet 會針對 Azure 金鑰保存庫建立記憶體內部憑證原則物件。</span><span class="sxs-lookup"><span data-stu-id="85f50-108">The **New-AzKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="85f50-109">示例</span><span class="sxs-lookup"><span data-stu-id="85f50-109">EXAMPLES</span></span>

### <span data-ttu-id="85f50-110">範例1：建立憑證原則</span><span class="sxs-lookup"><span data-stu-id="85f50-110">Example 1: Create a certificate policy</span></span>
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

<span data-ttu-id="85f50-111">這個命令會建立有效期為6個月的憑證原則，並重複使用金鑰來更新憑證。</span><span class="sxs-lookup"><span data-stu-id="85f50-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

### <span data-ttu-id="85f50-112">範例2</span><span class="sxs-lookup"><span data-stu-id="85f50-112">Example 2</span></span>

<span data-ttu-id="85f50-113">建立記憶體內部的憑證原則物件。</span><span class="sxs-lookup"><span data-stu-id="85f50-113">Creates an in-memory certificate policy object.</span></span> <span data-ttu-id="85f50-114"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="85f50-114">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzKeyVaultCertificatePolicy -IssuerName 'Self' -KeyType RSA -RenewAtNumberOfDaysBeforeExpiry <Int32> -SecretContentType application/x-pkcs12 -SubjectName 'CN=contoso.com' -ValidityInMonths 6
```

### <span data-ttu-id="85f50-115">範例3：建立 (或 SAN) 憑證的消費者替代名稱</span><span class="sxs-lookup"><span data-stu-id="85f50-115">Example 3: Create a Subject Alternate Name (or SAN) certificate</span></span>

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

<span data-ttu-id="85f50-116">這個範例會建立含3個 DNS 名稱的 SAN 憑證。</span><span class="sxs-lookup"><span data-stu-id="85f50-116">This example creates a SAN certificate with 3 DNS names.</span></span>

## <span data-ttu-id="85f50-117">參數</span><span class="sxs-lookup"><span data-stu-id="85f50-117">PARAMETERS</span></span>

### <span data-ttu-id="85f50-118">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="85f50-118">-CertificateTransparency</span></span>
<span data-ttu-id="85f50-119">指出是否已針對此憑證/頒發者啟用憑證透明;如果沒有指定，則預設值為 "true"</span><span class="sxs-lookup"><span data-stu-id="85f50-119">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

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

### <span data-ttu-id="85f50-120">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="85f50-120">-CertificateType</span></span>
<span data-ttu-id="85f50-121">指定發行人的憑證類型。</span><span class="sxs-lookup"><span data-stu-id="85f50-121">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="85f50-122">-曲線</span><span class="sxs-lookup"><span data-stu-id="85f50-122">-Curve</span></span>
<span data-ttu-id="85f50-123">指定憑證金鑰的橢圓曲線名稱。</span><span class="sxs-lookup"><span data-stu-id="85f50-123">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="85f50-124">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="85f50-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="85f50-125">P-256</span><span class="sxs-lookup"><span data-stu-id="85f50-125">P-256</span></span>
- <span data-ttu-id="85f50-126">P-384</span><span class="sxs-lookup"><span data-stu-id="85f50-126">P-384</span></span>
- <span data-ttu-id="85f50-127">P-521</span><span class="sxs-lookup"><span data-stu-id="85f50-127">P-521</span></span>
- <span data-ttu-id="85f50-128">P-256K</span><span class="sxs-lookup"><span data-stu-id="85f50-128">P-256K</span></span>
- <span data-ttu-id="85f50-129">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="85f50-129">SECP256K1</span></span>

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

### <span data-ttu-id="85f50-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85f50-130">-DefaultProfile</span></span>
<span data-ttu-id="85f50-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="85f50-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="85f50-132">-已停用</span><span class="sxs-lookup"><span data-stu-id="85f50-132">-Disabled</span></span>
<span data-ttu-id="85f50-133">表示憑證原則已停用。</span><span class="sxs-lookup"><span data-stu-id="85f50-133">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="85f50-134">-DnsName</span><span class="sxs-lookup"><span data-stu-id="85f50-134">-DnsName</span></span>
<span data-ttu-id="85f50-135">指定憑證中的 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="85f50-135">Specifies the DNS names in the certificate.</span></span> <span data-ttu-id="85f50-136">您可以將 (San) 的消費者備用名稱指定為 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="85f50-136">Subject Alternative Names (SANs) can be specified as DNS names.</span></span>

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

### <span data-ttu-id="85f50-137">-Eku</span><span class="sxs-lookup"><span data-stu-id="85f50-137">-Ekus</span></span>
<span data-ttu-id="85f50-138">指定憑證中 (Eku) 的增強型金鑰用法。</span><span class="sxs-lookup"><span data-stu-id="85f50-138">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="85f50-139">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="85f50-139">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="85f50-140">指定自動通知程式開始前的到期天數。</span><span class="sxs-lookup"><span data-stu-id="85f50-140">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="85f50-141">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="85f50-141">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="85f50-142">指定啟動通知自動程式開始的生命週期百分比。</span><span class="sxs-lookup"><span data-stu-id="85f50-142">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="85f50-143">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="85f50-143">-IssuerName</span></span>
<span data-ttu-id="85f50-144">指定憑證的頒發者名稱。</span><span class="sxs-lookup"><span data-stu-id="85f50-144">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="85f50-145">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="85f50-145">-KeyNotExportable</span></span>
<span data-ttu-id="85f50-146">表示金鑰無法匯出。</span><span class="sxs-lookup"><span data-stu-id="85f50-146">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="85f50-147">KeySize</span><span class="sxs-lookup"><span data-stu-id="85f50-147">-KeySize</span></span>
<span data-ttu-id="85f50-148">指定憑證的金鑰大小。</span><span class="sxs-lookup"><span data-stu-id="85f50-148">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="85f50-149">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="85f50-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="85f50-150">2048</span><span class="sxs-lookup"><span data-stu-id="85f50-150">2048</span></span>
- <span data-ttu-id="85f50-151">3072</span><span class="sxs-lookup"><span data-stu-id="85f50-151">3072</span></span>
- <span data-ttu-id="85f50-152">4096</span><span class="sxs-lookup"><span data-stu-id="85f50-152">4096</span></span>
- <span data-ttu-id="85f50-153">256</span><span class="sxs-lookup"><span data-stu-id="85f50-153">256</span></span>
- <span data-ttu-id="85f50-154">384</span><span class="sxs-lookup"><span data-stu-id="85f50-154">384</span></span>
- <span data-ttu-id="85f50-155">521</span><span class="sxs-lookup"><span data-stu-id="85f50-155">521</span></span>

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

### <span data-ttu-id="85f50-156">-KeyType</span><span class="sxs-lookup"><span data-stu-id="85f50-156">-KeyType</span></span>
<span data-ttu-id="85f50-157">指定支援憑證之金鑰的金鑰類型。</span><span class="sxs-lookup"><span data-stu-id="85f50-157">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="85f50-158">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="85f50-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="85f50-159">與眾不同</span><span class="sxs-lookup"><span data-stu-id="85f50-159">RSA</span></span>
- <span data-ttu-id="85f50-160">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="85f50-160">RSA-HSM</span></span>
- <span data-ttu-id="85f50-161">成員國</span><span class="sxs-lookup"><span data-stu-id="85f50-161">EC</span></span>
- <span data-ttu-id="85f50-162">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="85f50-162">EC-HSM</span></span>

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

### <span data-ttu-id="85f50-163">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="85f50-163">-KeyUsage</span></span>
<span data-ttu-id="85f50-164">指定憑證中的金鑰用法。</span><span class="sxs-lookup"><span data-stu-id="85f50-164">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="85f50-165">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="85f50-165">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="85f50-166">指定到期前的天數，在此之後，就會開始更新自動程式。</span><span class="sxs-lookup"><span data-stu-id="85f50-166">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="85f50-167">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="85f50-167">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="85f50-168">指定啟動證書自動程式開始前的生命週期百分比。</span><span class="sxs-lookup"><span data-stu-id="85f50-168">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="85f50-169">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="85f50-169">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="85f50-170">表示憑證在續約時重複使用金鑰。</span><span class="sxs-lookup"><span data-stu-id="85f50-170">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="85f50-171">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="85f50-171">-SecretContentType</span></span>
<span data-ttu-id="85f50-172">指定新的主要電子倉庫密碼的內容類型。</span><span class="sxs-lookup"><span data-stu-id="85f50-172">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="85f50-173">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="85f50-173">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="85f50-174">應用程式/x-pkcs12</span><span class="sxs-lookup"><span data-stu-id="85f50-174">application/x-pkcs12</span></span>
- <span data-ttu-id="85f50-175">應用程式/x pem-檔案</span><span class="sxs-lookup"><span data-stu-id="85f50-175">application/x-pem-file</span></span>

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

### <span data-ttu-id="85f50-176">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="85f50-176">-SubjectName</span></span>
<span data-ttu-id="85f50-177">指定憑證的受領人名稱。</span><span class="sxs-lookup"><span data-stu-id="85f50-177">Specifies the subject name of the certificate.</span></span> 

> [!NOTE]
> <span data-ttu-id="85f50-178">如果您必須使用逗號 (、) 或句點 (。 ) 在參數中的屬性內 `SubjectName` ，必須以引號括住屬性欄位。</span><span class="sxs-lookup"><span data-stu-id="85f50-178">If you must use a comma (,) or a period (.) within a property in the `SubjectName` parameter, you must enclose the property field in quotation marks.</span></span> <span data-ttu-id="85f50-179">例如，您可以使用 O = "Contoso，有限公司"。</span><span class="sxs-lookup"><span data-stu-id="85f50-179">For example, you may use O="Contoso, Ltd."</span></span> <span data-ttu-id="85f50-180">在 [組織名稱] 欄位中。</span><span class="sxs-lookup"><span data-stu-id="85f50-180">in the Organization Name field.</span></span>

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

### <span data-ttu-id="85f50-181">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="85f50-181">-ValidityInMonths</span></span>
<span data-ttu-id="85f50-182">指定憑證有效的月份數。</span><span class="sxs-lookup"><span data-stu-id="85f50-182">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="85f50-183">-確認</span><span class="sxs-lookup"><span data-stu-id="85f50-183">-Confirm</span></span>
<span data-ttu-id="85f50-184">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="85f50-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85f50-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85f50-185">-WhatIf</span></span>
<span data-ttu-id="85f50-186">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="85f50-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85f50-187">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="85f50-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85f50-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85f50-188">CommonParameters</span></span>
<span data-ttu-id="85f50-189">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="85f50-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85f50-190">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="85f50-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85f50-191">輸入</span><span class="sxs-lookup"><span data-stu-id="85f50-191">INPUTS</span></span>

### <span data-ttu-id="85f50-192">System.object</span><span class="sxs-lookup"><span data-stu-id="85f50-192">System.String</span></span>

### <span data-ttu-id="85f50-193">[System.object]。清單 ' 1 [CoreLib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="85f50-193">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="85f50-194">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="85f50-194">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="85f50-195">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="85f50-195">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="85f50-196">[System.object]。清單 ' 1 [X509Certificates. X509KeyUsageFlags，系統. X509Certificates，版本 = 4.2.1.0，Culture = 中性，PublicKeyToken = b03f5f7f11d50a3a]]。</span><span class="sxs-lookup"><span data-stu-id="85f50-196">System.Collections.Generic.List\`1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System.Security.Cryptography.X509Certificates, Version=4.2.1.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a]]</span></span>

## <span data-ttu-id="85f50-197">輸出</span><span class="sxs-lookup"><span data-stu-id="85f50-197">OUTPUTS</span></span>

### <span data-ttu-id="85f50-198">PSKeyVaultCertificatePolicy 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="85f50-198">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="85f50-199">筆記</span><span class="sxs-lookup"><span data-stu-id="85f50-199">NOTES</span></span>

## <span data-ttu-id="85f50-200">相關連結</span><span class="sxs-lookup"><span data-stu-id="85f50-200">RELATED LINKS</span></span>

[<span data-ttu-id="85f50-201">AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="85f50-201">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="85f50-202">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="85f50-202">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

