---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/powershell/module/az.keyvault/set-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 09e58a029d3011c2abcee035ee23640f801825b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906597"
---
# <span data-ttu-id="fff93-101">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="fff93-101">Set-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="fff93-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fff93-102">SYNOPSIS</span></span>
<span data-ttu-id="fff93-103">建立或更新金鑰庫中憑證的策略。</span><span class="sxs-lookup"><span data-stu-id="fff93-103">Creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="fff93-104">語法</span><span class="sxs-lookup"><span data-stu-id="fff93-104">SYNTAX</span></span>

### <span data-ttu-id="fff93-105">展開的RenewPercentage (預設) </span><span class="sxs-lookup"><span data-stu-id="fff93-105">ExpandedRenewPercentage (Default)</span></span>
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

### <span data-ttu-id="fff93-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="fff93-106">ByValue</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>] [-KeySize <Int32>]
 [-CertificateTransparency <Boolean>] [-PassThru] [-Curve <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fff93-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="fff93-107">ExpandedRenewNumber</span></span>
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

## <span data-ttu-id="fff93-108">描述</span><span class="sxs-lookup"><span data-stu-id="fff93-108">DESCRIPTION</span></span>
<span data-ttu-id="fff93-109">**Set-AzKeyVaultCertificatePolidlet** 會建立或更新金鑰庫中憑證的策略。</span><span class="sxs-lookup"><span data-stu-id="fff93-109">The **Set-AzKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="fff93-110">例子</span><span class="sxs-lookup"><span data-stu-id="fff93-110">EXAMPLES</span></span>

### <span data-ttu-id="fff93-111">範例 1：設定憑證策略</span><span class="sxs-lookup"><span data-stu-id="fff93-111">Example 1: Set a certificate policy</span></span>
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

<span data-ttu-id="fff93-112">此命令會設定 ContosoKV01 金鑰庫中的 TestCert01 憑證之策略。</span><span class="sxs-lookup"><span data-stu-id="fff93-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="fff93-113">參數</span><span class="sxs-lookup"><span data-stu-id="fff93-113">PARAMETERS</span></span>

### <span data-ttu-id="fff93-114">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="fff93-114">-CertificateTransparency</span></span>
<span data-ttu-id="fff93-115">指出此憑證/發行者是否已啟用憑證透明度;如果未指定，預設值為 "true"。</span><span class="sxs-lookup"><span data-stu-id="fff93-115">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'.</span></span>
<span data-ttu-id="fff93-116">`-IssuerName` 設定此屬性時必須指定此屬性。</span><span class="sxs-lookup"><span data-stu-id="fff93-116">`-IssuerName` needs to be specified when setting this property.</span></span>

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

### <span data-ttu-id="fff93-117">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="fff93-117">-CertificateType</span></span>
<span data-ttu-id="fff93-118">指定發行者憑證的類型。</span><span class="sxs-lookup"><span data-stu-id="fff93-118">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="fff93-119">-曲線</span><span class="sxs-lookup"><span data-stu-id="fff93-119">-Curve</span></span>
<span data-ttu-id="fff93-120">指定憑證金鑰的省略號曲線名稱。</span><span class="sxs-lookup"><span data-stu-id="fff93-120">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="fff93-121">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="fff93-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fff93-122">P-256</span><span class="sxs-lookup"><span data-stu-id="fff93-122">P-256</span></span>
- <span data-ttu-id="fff93-123">P-384</span><span class="sxs-lookup"><span data-stu-id="fff93-123">P-384</span></span>
- <span data-ttu-id="fff93-124">P-521</span><span class="sxs-lookup"><span data-stu-id="fff93-124">P-521</span></span>
- <span data-ttu-id="fff93-125">P-256K</span><span class="sxs-lookup"><span data-stu-id="fff93-125">P-256K</span></span>
- <span data-ttu-id="fff93-126">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="fff93-126">SECP256K1</span></span>

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

### <span data-ttu-id="fff93-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fff93-127">-DefaultProfile</span></span>
<span data-ttu-id="fff93-128">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="fff93-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fff93-129">-已停用</span><span class="sxs-lookup"><span data-stu-id="fff93-129">-Disabled</span></span>
<span data-ttu-id="fff93-130">表示憑證策略已停用。</span><span class="sxs-lookup"><span data-stu-id="fff93-130">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="fff93-131">-DnsName</span><span class="sxs-lookup"><span data-stu-id="fff93-131">-DnsName</span></span>
<span data-ttu-id="fff93-132">指定憑證的主體名稱。</span><span class="sxs-lookup"><span data-stu-id="fff93-132">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="fff93-133">-EKUs</span><span class="sxs-lookup"><span data-stu-id="fff93-133">-Ekus</span></span>
<span data-ttu-id="fff93-134">指定憑證中 (EKUS) 的增強金鑰使用量。</span><span class="sxs-lookup"><span data-stu-id="fff93-134">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="fff93-135">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="fff93-135">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="fff93-136">指定自動續約應開始到期前的天數。</span><span class="sxs-lookup"><span data-stu-id="fff93-136">Specifies the number of days before expiration when automatic renewal should start.</span></span>

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

### <span data-ttu-id="fff93-137">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="fff93-137">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="fff93-138">指定通知自動程式開始後的生命週期百分比。</span><span class="sxs-lookup"><span data-stu-id="fff93-138">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="fff93-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fff93-139">-InputObject</span></span>
<span data-ttu-id="fff93-140">指定憑證策略。</span><span class="sxs-lookup"><span data-stu-id="fff93-140">Specifies the certificate policy.</span></span>

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

### <span data-ttu-id="fff93-141">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="fff93-141">-IssuerName</span></span>
<span data-ttu-id="fff93-142">指定此憑證的發行者名稱。</span><span class="sxs-lookup"><span data-stu-id="fff93-142">Specifies the name of the issuer for this certificate.</span></span>

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

### <span data-ttu-id="fff93-143">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="fff93-143">-KeyNotExportable</span></span>
<span data-ttu-id="fff93-144">表示無法匯出金鑰。</span><span class="sxs-lookup"><span data-stu-id="fff93-144">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="fff93-145">-KeySize</span><span class="sxs-lookup"><span data-stu-id="fff93-145">-KeySize</span></span>
<span data-ttu-id="fff93-146">指定憑證的金鑰大小。</span><span class="sxs-lookup"><span data-stu-id="fff93-146">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="fff93-147">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="fff93-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fff93-148">2048</span><span class="sxs-lookup"><span data-stu-id="fff93-148">2048</span></span>
- <span data-ttu-id="fff93-149">3072</span><span class="sxs-lookup"><span data-stu-id="fff93-149">3072</span></span>
- <span data-ttu-id="fff93-150">4096</span><span class="sxs-lookup"><span data-stu-id="fff93-150">4096</span></span>
- <span data-ttu-id="fff93-151">256</span><span class="sxs-lookup"><span data-stu-id="fff93-151">256</span></span>
- <span data-ttu-id="fff93-152">384</span><span class="sxs-lookup"><span data-stu-id="fff93-152">384</span></span>
- <span data-ttu-id="fff93-153">521</span><span class="sxs-lookup"><span data-stu-id="fff93-153">521</span></span>

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

### <span data-ttu-id="fff93-154">-KeyType</span><span class="sxs-lookup"><span data-stu-id="fff93-154">-KeyType</span></span>
<span data-ttu-id="fff93-155">指定支援憑證之金鑰的金鑰類型。</span><span class="sxs-lookup"><span data-stu-id="fff93-155">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="fff93-156">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="fff93-156">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fff93-157">Rsa</span><span class="sxs-lookup"><span data-stu-id="fff93-157">RSA</span></span>
- <span data-ttu-id="fff93-158">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="fff93-158">RSA-HSM</span></span>
- <span data-ttu-id="fff93-159">電子商務</span><span class="sxs-lookup"><span data-stu-id="fff93-159">EC</span></span>
- <span data-ttu-id="fff93-160">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="fff93-160">EC-HSM</span></span>

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

### <span data-ttu-id="fff93-161">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="fff93-161">-KeyUsage</span></span>
<span data-ttu-id="fff93-162">指定憑證中的重要使用量。</span><span class="sxs-lookup"><span data-stu-id="fff93-162">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="fff93-163">-名稱</span><span class="sxs-lookup"><span data-stu-id="fff93-163">-Name</span></span>
<span data-ttu-id="fff93-164">指定憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="fff93-164">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="fff93-165">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fff93-165">-PassThru</span></span>
<span data-ttu-id="fff93-166">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="fff93-166">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fff93-167">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="fff93-167">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fff93-168">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="fff93-168">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="fff93-169">指定憑證續約的自動程式開始前的天數。</span><span class="sxs-lookup"><span data-stu-id="fff93-169">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="fff93-170">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="fff93-170">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="fff93-171">指定憑證續約的自動程式開始後的生命週期百分比。</span><span class="sxs-lookup"><span data-stu-id="fff93-171">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="fff93-172">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="fff93-172">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="fff93-173">表示憑證在續約期間重複使用金鑰。</span><span class="sxs-lookup"><span data-stu-id="fff93-173">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="fff93-174">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="fff93-174">-SecretContentType</span></span>
<span data-ttu-id="fff93-175">指定新金鑰庫機密的內容類型。</span><span class="sxs-lookup"><span data-stu-id="fff93-175">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="fff93-176">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="fff93-176">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fff93-177">application/x-pkcs12</span><span class="sxs-lookup"><span data-stu-id="fff93-177">application/x-pkcs12</span></span>
- <span data-ttu-id="fff93-178">application/x-pem-file</span><span class="sxs-lookup"><span data-stu-id="fff93-178">application/x-pem-file</span></span>

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

### <span data-ttu-id="fff93-179">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="fff93-179">-SubjectName</span></span>
<span data-ttu-id="fff93-180">指定憑證的主體名稱。</span><span class="sxs-lookup"><span data-stu-id="fff93-180">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="fff93-181">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="fff93-181">-ValidityInMonths</span></span>
<span data-ttu-id="fff93-182">指定憑證有效的月數。</span><span class="sxs-lookup"><span data-stu-id="fff93-182">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="fff93-183">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fff93-183">-VaultName</span></span>
<span data-ttu-id="fff93-184">指定金鑰庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="fff93-184">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="fff93-185">-確認</span><span class="sxs-lookup"><span data-stu-id="fff93-185">-Confirm</span></span>
<span data-ttu-id="fff93-186">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="fff93-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fff93-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fff93-187">-WhatIf</span></span>
<span data-ttu-id="fff93-188">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fff93-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fff93-189">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fff93-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fff93-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fff93-190">CommonParameters</span></span>
<span data-ttu-id="fff93-191">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fff93-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fff93-192">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fff93-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fff93-193">輸入</span><span class="sxs-lookup"><span data-stu-id="fff93-193">INPUTS</span></span>

### <span data-ttu-id="fff93-194">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="fff93-194">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="fff93-195">輸出</span><span class="sxs-lookup"><span data-stu-id="fff93-195">OUTPUTS</span></span>

### <span data-ttu-id="fff93-196">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="fff93-196">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="fff93-197">筆記</span><span class="sxs-lookup"><span data-stu-id="fff93-197">NOTES</span></span>

## <span data-ttu-id="fff93-198">相關連結</span><span class="sxs-lookup"><span data-stu-id="fff93-198">RELATED LINKS</span></span>

[<span data-ttu-id="fff93-199">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="fff93-199">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="fff93-200">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="fff93-200">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

