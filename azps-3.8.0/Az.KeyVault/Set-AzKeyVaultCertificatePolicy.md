---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 5a6b88ce85b8b9296d9666955a93d1240b631634
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958484"
---
# <span data-ttu-id="89ea7-101">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="89ea7-101">Set-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="89ea7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="89ea7-102">SYNOPSIS</span></span>
<span data-ttu-id="89ea7-103">在金鑰保存庫中建立或更新憑證的原則。</span><span class="sxs-lookup"><span data-stu-id="89ea7-103">Creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="89ea7-104">句法</span><span class="sxs-lookup"><span data-stu-id="89ea7-104">SYNTAX</span></span>

### <span data-ttu-id="89ea7-105">ExpandedRenewPercentage (預設) </span><span class="sxs-lookup"><span data-stu-id="89ea7-105">ExpandedRenewPercentage (Default)</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-RenewAtPercentageLifetime <Int32>]
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeySize <Int32>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-Curve <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89ea7-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="89ea7-106">ByValue</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>] [-KeySize <Int32>]
 [-CertificateTransparency <Boolean>] [-PassThru] [-Curve <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89ea7-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="89ea7-107">ExpandedRenewNumber</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> -RenewAtNumberOfDaysBeforeExpiry <Int32>
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeySize <Int32>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-Curve <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89ea7-108">說明</span><span class="sxs-lookup"><span data-stu-id="89ea7-108">DESCRIPTION</span></span>
<span data-ttu-id="89ea7-109">**AzKeyVaultCertificatePolicy** Cmdlet 會建立或更新金鑰保存庫中的憑證原則。</span><span class="sxs-lookup"><span data-stu-id="89ea7-109">The **Set-AzKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="89ea7-110">示例</span><span class="sxs-lookup"><span data-stu-id="89ea7-110">EXAMPLES</span></span>

### <span data-ttu-id="89ea7-111">範例1：設定憑證原則</span><span class="sxs-lookup"><span data-stu-id="89ea7-111">Example 1: Set a certificate policy</span></span>
```powershell
PS C:\> Set-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True -PassThru

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

<span data-ttu-id="89ea7-112">這個命令會在 ContosoKV01 金鑰保存庫中設定 TestCert01 憑證的原則。</span><span class="sxs-lookup"><span data-stu-id="89ea7-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="89ea7-113">參數</span><span class="sxs-lookup"><span data-stu-id="89ea7-113">PARAMETERS</span></span>

### <span data-ttu-id="89ea7-114">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="89ea7-114">-CertificateTransparency</span></span>
<span data-ttu-id="89ea7-115">指出是否已針對此憑證/頒發者啟用憑證透明;如果沒有指定，則預設值為 "true"</span><span class="sxs-lookup"><span data-stu-id="89ea7-115">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89ea7-116">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="89ea7-116">-CertificateType</span></span>
<span data-ttu-id="89ea7-117">指定發行人的憑證類型。</span><span class="sxs-lookup"><span data-stu-id="89ea7-117">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89ea7-118">-曲線</span><span class="sxs-lookup"><span data-stu-id="89ea7-118">-Curve</span></span>
<span data-ttu-id="89ea7-119">指定憑證金鑰的橢圓曲線名稱。</span><span class="sxs-lookup"><span data-stu-id="89ea7-119">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="89ea7-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="89ea7-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="89ea7-121">P-256</span><span class="sxs-lookup"><span data-stu-id="89ea7-121">P-256</span></span>
- <span data-ttu-id="89ea7-122">P-384</span><span class="sxs-lookup"><span data-stu-id="89ea7-122">P-384</span></span>
- <span data-ttu-id="89ea7-123">P-521</span><span class="sxs-lookup"><span data-stu-id="89ea7-123">P-521</span></span>
- <span data-ttu-id="89ea7-124">P-256K</span><span class="sxs-lookup"><span data-stu-id="89ea7-124">P-256K</span></span>
- <span data-ttu-id="89ea7-125">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="89ea7-125">SECP256K1</span></span>

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

### <span data-ttu-id="89ea7-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89ea7-126">-DefaultProfile</span></span>
<span data-ttu-id="89ea7-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="89ea7-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="89ea7-128">-已停用</span><span class="sxs-lookup"><span data-stu-id="89ea7-128">-Disabled</span></span>
<span data-ttu-id="89ea7-129">表示憑證原則已停用。</span><span class="sxs-lookup"><span data-stu-id="89ea7-129">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89ea7-130">-DnsName</span><span class="sxs-lookup"><span data-stu-id="89ea7-130">-DnsName</span></span>
<span data-ttu-id="89ea7-131">指定憑證的受領人名稱。</span><span class="sxs-lookup"><span data-stu-id="89ea7-131">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases: DnsNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89ea7-132">-Eku</span><span class="sxs-lookup"><span data-stu-id="89ea7-132">-Ekus</span></span>
<span data-ttu-id="89ea7-133">指定憑證中 (Eku) 的增強型金鑰用法。</span><span class="sxs-lookup"><span data-stu-id="89ea7-133">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89ea7-134">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="89ea7-134">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="89ea7-135">指定自動續約開始時到期前的天數。</span><span class="sxs-lookup"><span data-stu-id="89ea7-135">Specifies the number of days before expiration when automatic renewal should start.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89ea7-136">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="89ea7-136">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="89ea7-137">指定啟動通知自動程式開始的生命週期百分比。</span><span class="sxs-lookup"><span data-stu-id="89ea7-137">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89ea7-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89ea7-138">-InputObject</span></span>
<span data-ttu-id="89ea7-139">指定憑證原則。</span><span class="sxs-lookup"><span data-stu-id="89ea7-139">Specifies the certificate policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy
Parameter Sets: ByValue
Aliases: CertificatePolicy

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89ea7-140">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="89ea7-140">-IssuerName</span></span>
<span data-ttu-id="89ea7-141">指定此憑證的頒發者名稱。</span><span class="sxs-lookup"><span data-stu-id="89ea7-141">Specifies the name of the issuer for this certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89ea7-142">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="89ea7-142">-KeyNotExportable</span></span>
<span data-ttu-id="89ea7-143">表示金鑰無法匯出。</span><span class="sxs-lookup"><span data-stu-id="89ea7-143">Indicates that the key is not exportable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89ea7-144">KeySize</span><span class="sxs-lookup"><span data-stu-id="89ea7-144">-KeySize</span></span>
<span data-ttu-id="89ea7-145">指定憑證的金鑰大小。</span><span class="sxs-lookup"><span data-stu-id="89ea7-145">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="89ea7-146">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="89ea7-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="89ea7-147">2048</span><span class="sxs-lookup"><span data-stu-id="89ea7-147">2048</span></span>
- <span data-ttu-id="89ea7-148">3072</span><span class="sxs-lookup"><span data-stu-id="89ea7-148">3072</span></span>
- <span data-ttu-id="89ea7-149">4096</span><span class="sxs-lookup"><span data-stu-id="89ea7-149">4096</span></span>
- <span data-ttu-id="89ea7-150">256</span><span class="sxs-lookup"><span data-stu-id="89ea7-150">256</span></span>
- <span data-ttu-id="89ea7-151">384</span><span class="sxs-lookup"><span data-stu-id="89ea7-151">384</span></span>
- <span data-ttu-id="89ea7-152">521</span><span class="sxs-lookup"><span data-stu-id="89ea7-152">521</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:
Accepted values: 2048, 3072, 4096, 256, 384, 521

Required: False
Position: Named
Default value: 2048
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89ea7-153">-KeyType</span><span class="sxs-lookup"><span data-stu-id="89ea7-153">-KeyType</span></span>
<span data-ttu-id="89ea7-154">指定支援憑證之金鑰的金鑰類型。</span><span class="sxs-lookup"><span data-stu-id="89ea7-154">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="89ea7-155">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="89ea7-155">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="89ea7-156">與眾不同</span><span class="sxs-lookup"><span data-stu-id="89ea7-156">RSA</span></span>
- <span data-ttu-id="89ea7-157">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="89ea7-157">RSA-HSM</span></span>
- <span data-ttu-id="89ea7-158">成員國</span><span class="sxs-lookup"><span data-stu-id="89ea7-158">EC</span></span>
- <span data-ttu-id="89ea7-159">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="89ea7-159">EC-HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM, EC, EC-HSM

Required: False
Position: Named
Default value: RSA
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89ea7-160">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="89ea7-160">-KeyUsage</span></span>
<span data-ttu-id="89ea7-161">指定憑證中的金鑰用法。</span><span class="sxs-lookup"><span data-stu-id="89ea7-161">Specifies the key usages in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:
Accepted values: None, EncipherOnly, CrlSign, KeyCertSign, KeyAgreement, DataEncipherment, KeyEncipherment, NonRepudiation, DigitalSignature, DecipherOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89ea7-162">-名稱</span><span class="sxs-lookup"><span data-stu-id="89ea7-162">-Name</span></span>
<span data-ttu-id="89ea7-163">指定憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="89ea7-163">Specifies the name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89ea7-164">-PassThru</span><span class="sxs-lookup"><span data-stu-id="89ea7-164">-PassThru</span></span>
<span data-ttu-id="89ea7-165">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="89ea7-165">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="89ea7-166">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="89ea7-166">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89ea7-167">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="89ea7-167">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="89ea7-168">指定到期前的天數，在此之後，就會開始更新自動程式。</span><span class="sxs-lookup"><span data-stu-id="89ea7-168">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ExpandedRenewNumber
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89ea7-169">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="89ea7-169">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="89ea7-170">指定啟動證書自動程式開始前的生命週期百分比。</span><span class="sxs-lookup"><span data-stu-id="89ea7-170">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ExpandedRenewPercentage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89ea7-171">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="89ea7-171">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="89ea7-172">表示憑證在續約時重複使用金鑰。</span><span class="sxs-lookup"><span data-stu-id="89ea7-172">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89ea7-173">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="89ea7-173">-SecretContentType</span></span>
<span data-ttu-id="89ea7-174">指定新的主要電子倉庫密碼的內容類型。</span><span class="sxs-lookup"><span data-stu-id="89ea7-174">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="89ea7-175">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="89ea7-175">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="89ea7-176">應用程式/x-pkcs12</span><span class="sxs-lookup"><span data-stu-id="89ea7-176">application/x-pkcs12</span></span>
- <span data-ttu-id="89ea7-177">應用程式/x pem-檔案</span><span class="sxs-lookup"><span data-stu-id="89ea7-177">application/x-pem-file</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89ea7-178">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="89ea7-178">-SubjectName</span></span>
<span data-ttu-id="89ea7-179">指定憑證的受領人名稱。</span><span class="sxs-lookup"><span data-stu-id="89ea7-179">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89ea7-180">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="89ea7-180">-ValidityInMonths</span></span>
<span data-ttu-id="89ea7-181">指定憑證有效的月份數。</span><span class="sxs-lookup"><span data-stu-id="89ea7-181">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89ea7-182">-VaultName</span><span class="sxs-lookup"><span data-stu-id="89ea7-182">-VaultName</span></span>
<span data-ttu-id="89ea7-183">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="89ea7-183">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89ea7-184">-確認</span><span class="sxs-lookup"><span data-stu-id="89ea7-184">-Confirm</span></span>
<span data-ttu-id="89ea7-185">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="89ea7-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89ea7-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89ea7-186">-WhatIf</span></span>
<span data-ttu-id="89ea7-187">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="89ea7-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89ea7-188">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="89ea7-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89ea7-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89ea7-189">CommonParameters</span></span>
<span data-ttu-id="89ea7-190">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="89ea7-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89ea7-191">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="89ea7-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89ea7-192">輸入</span><span class="sxs-lookup"><span data-stu-id="89ea7-192">INPUTS</span></span>

### <span data-ttu-id="89ea7-193">PSKeyVaultCertificatePolicy 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="89ea7-193">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="89ea7-194">輸出</span><span class="sxs-lookup"><span data-stu-id="89ea7-194">OUTPUTS</span></span>

### <span data-ttu-id="89ea7-195">PSKeyVaultCertificatePolicy 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="89ea7-195">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="89ea7-196">筆記</span><span class="sxs-lookup"><span data-stu-id="89ea7-196">NOTES</span></span>

## <span data-ttu-id="89ea7-197">相關連結</span><span class="sxs-lookup"><span data-stu-id="89ea7-197">RELATED LINKS</span></span>

[<span data-ttu-id="89ea7-198">AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="89ea7-198">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="89ea7-199">新-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="89ea7-199">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

