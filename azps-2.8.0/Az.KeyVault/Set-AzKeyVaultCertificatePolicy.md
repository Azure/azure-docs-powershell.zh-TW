---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: e6ae1be8599869631698ddd886fa09184abfb867
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612090"
---
# <span data-ttu-id="14d27-101">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="14d27-101">Set-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="14d27-102">摘要</span><span class="sxs-lookup"><span data-stu-id="14d27-102">SYNOPSIS</span></span>
<span data-ttu-id="14d27-103">在金鑰保存庫中建立或更新憑證的原則。</span><span class="sxs-lookup"><span data-stu-id="14d27-103">Creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="14d27-104">句法</span><span class="sxs-lookup"><span data-stu-id="14d27-104">SYNTAX</span></span>

### <span data-ttu-id="14d27-105">ExpandedRenewPercentage (預設) </span><span class="sxs-lookup"><span data-stu-id="14d27-105">ExpandedRenewPercentage (Default)</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-RenewAtPercentageLifetime <Int32>]
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeySize <Int32>] [-KeyType <String>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14d27-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="14d27-106">ByValue</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeySize <Int32>] [-KeyType <String>] [-CertificateTransparency <Boolean>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14d27-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="14d27-107">ExpandedRenewNumber</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> -RenewAtNumberOfDaysBeforeExpiry <Int32>
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeySize <Int32>] [-KeyType <String>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14d27-108">說明</span><span class="sxs-lookup"><span data-stu-id="14d27-108">DESCRIPTION</span></span>
<span data-ttu-id="14d27-109">**AzKeyVaultCertificatePolicy** Cmdlet 會建立或更新金鑰保存庫中的憑證原則。</span><span class="sxs-lookup"><span data-stu-id="14d27-109">The **Set-AzKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="14d27-110">示例</span><span class="sxs-lookup"><span data-stu-id="14d27-110">EXAMPLES</span></span>

### <span data-ttu-id="14d27-111">範例1：設定憑證原則</span><span class="sxs-lookup"><span data-stu-id="14d27-111">Example 1: Set a certificate policy</span></span>
```powershell
PS C:\> Set-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True -PassThru

SecretContentType               : application/x-pkcs12
Kty                             :
KeySize                         : 2048
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

<span data-ttu-id="14d27-112">這個命令會在 ContosoKV01 金鑰保存庫中設定 TestCert01 憑證的原則。</span><span class="sxs-lookup"><span data-stu-id="14d27-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="14d27-113">參數</span><span class="sxs-lookup"><span data-stu-id="14d27-113">PARAMETERS</span></span>

### <span data-ttu-id="14d27-114">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="14d27-114">-CertificateTransparency</span></span>
<span data-ttu-id="14d27-115">指出是否已針對此憑證/頒發者啟用憑證透明;如果沒有指定，則預設值為 "true"</span><span class="sxs-lookup"><span data-stu-id="14d27-115">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

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

### <span data-ttu-id="14d27-116">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="14d27-116">-CertificateType</span></span>
<span data-ttu-id="14d27-117">指定發行人的憑證類型。</span><span class="sxs-lookup"><span data-stu-id="14d27-117">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="14d27-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14d27-118">-DefaultProfile</span></span>
<span data-ttu-id="14d27-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="14d27-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14d27-120">-已停用</span><span class="sxs-lookup"><span data-stu-id="14d27-120">-Disabled</span></span>
<span data-ttu-id="14d27-121">表示憑證原則已停用。</span><span class="sxs-lookup"><span data-stu-id="14d27-121">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="14d27-122">-DnsName</span><span class="sxs-lookup"><span data-stu-id="14d27-122">-DnsName</span></span>
<span data-ttu-id="14d27-123">指定憑證的受領人名稱。</span><span class="sxs-lookup"><span data-stu-id="14d27-123">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="14d27-124">-Eku</span><span class="sxs-lookup"><span data-stu-id="14d27-124">-Ekus</span></span>
<span data-ttu-id="14d27-125">指定憑證中 (Eku) 的增強型金鑰用法。</span><span class="sxs-lookup"><span data-stu-id="14d27-125">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="14d27-126">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="14d27-126">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="14d27-127">指定自動續約開始時到期前的天數。</span><span class="sxs-lookup"><span data-stu-id="14d27-127">Specifies the number of days before expiration when automatic renewal should start.</span></span>

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

### <span data-ttu-id="14d27-128">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="14d27-128">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="14d27-129">指定啟動通知自動程式開始的生命週期百分比。</span><span class="sxs-lookup"><span data-stu-id="14d27-129">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="14d27-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14d27-130">-InputObject</span></span>
<span data-ttu-id="14d27-131">指定憑證原則。</span><span class="sxs-lookup"><span data-stu-id="14d27-131">Specifies the certificate policy.</span></span>

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

### <span data-ttu-id="14d27-132">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="14d27-132">-IssuerName</span></span>
<span data-ttu-id="14d27-133">指定此憑證的頒發者名稱。</span><span class="sxs-lookup"><span data-stu-id="14d27-133">Specifies the name of the issuer for this certificate.</span></span>

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

### <span data-ttu-id="14d27-134">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="14d27-134">-KeyNotExportable</span></span>
<span data-ttu-id="14d27-135">表示金鑰無法匯出。</span><span class="sxs-lookup"><span data-stu-id="14d27-135">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="14d27-136">KeySize</span><span class="sxs-lookup"><span data-stu-id="14d27-136">-KeySize</span></span>
<span data-ttu-id="14d27-137">指定憑證的金鑰大小。</span><span class="sxs-lookup"><span data-stu-id="14d27-137">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="14d27-138">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="14d27-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="14d27-139">2048</span><span class="sxs-lookup"><span data-stu-id="14d27-139">2048</span></span>
- <span data-ttu-id="14d27-140">3072</span><span class="sxs-lookup"><span data-stu-id="14d27-140">3072</span></span>
- <span data-ttu-id="14d27-141">4096</span><span class="sxs-lookup"><span data-stu-id="14d27-141">4096</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:
Accepted values: 2048, 3072, 4096

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14d27-142">-KeyType</span><span class="sxs-lookup"><span data-stu-id="14d27-142">-KeyType</span></span>
<span data-ttu-id="14d27-143">指定支援憑證之金鑰的金鑰類型。</span><span class="sxs-lookup"><span data-stu-id="14d27-143">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="14d27-144">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="14d27-144">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="14d27-145">與眾不同</span><span class="sxs-lookup"><span data-stu-id="14d27-145">RSA</span></span>
- <span data-ttu-id="14d27-146">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="14d27-146">RSA-HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14d27-147">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="14d27-147">-KeyUsage</span></span>
<span data-ttu-id="14d27-148">指定憑證中的金鑰用法。</span><span class="sxs-lookup"><span data-stu-id="14d27-148">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="14d27-149">-名稱</span><span class="sxs-lookup"><span data-stu-id="14d27-149">-Name</span></span>
<span data-ttu-id="14d27-150">指定憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="14d27-150">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="14d27-151">-PassThru</span><span class="sxs-lookup"><span data-stu-id="14d27-151">-PassThru</span></span>
<span data-ttu-id="14d27-152">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="14d27-152">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="14d27-153">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="14d27-153">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="14d27-154">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="14d27-154">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="14d27-155">指定到期前的天數，在此之後，就會開始更新自動程式。</span><span class="sxs-lookup"><span data-stu-id="14d27-155">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="14d27-156">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="14d27-156">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="14d27-157">指定啟動證書自動程式開始前的生命週期百分比。</span><span class="sxs-lookup"><span data-stu-id="14d27-157">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="14d27-158">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="14d27-158">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="14d27-159">表示憑證在續約時重複使用金鑰。</span><span class="sxs-lookup"><span data-stu-id="14d27-159">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="14d27-160">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="14d27-160">-SecretContentType</span></span>
<span data-ttu-id="14d27-161">指定新的主要電子倉庫密碼的內容類型。</span><span class="sxs-lookup"><span data-stu-id="14d27-161">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="14d27-162">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="14d27-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="14d27-163">應用程式/x-pkcs12</span><span class="sxs-lookup"><span data-stu-id="14d27-163">application/x-pkcs12</span></span>
- <span data-ttu-id="14d27-164">應用程式/x pem-檔案</span><span class="sxs-lookup"><span data-stu-id="14d27-164">application/x-pem-file</span></span>

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

### <span data-ttu-id="14d27-165">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="14d27-165">-SubjectName</span></span>
<span data-ttu-id="14d27-166">指定憑證的受領人名稱。</span><span class="sxs-lookup"><span data-stu-id="14d27-166">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="14d27-167">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="14d27-167">-ValidityInMonths</span></span>
<span data-ttu-id="14d27-168">指定憑證有效的月份數。</span><span class="sxs-lookup"><span data-stu-id="14d27-168">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="14d27-169">-VaultName</span><span class="sxs-lookup"><span data-stu-id="14d27-169">-VaultName</span></span>
<span data-ttu-id="14d27-170">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="14d27-170">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="14d27-171">-確認</span><span class="sxs-lookup"><span data-stu-id="14d27-171">-Confirm</span></span>
<span data-ttu-id="14d27-172">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="14d27-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14d27-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14d27-173">-WhatIf</span></span>
<span data-ttu-id="14d27-174">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="14d27-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14d27-175">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="14d27-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14d27-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14d27-176">CommonParameters</span></span>
<span data-ttu-id="14d27-177">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="14d27-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14d27-178">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="14d27-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14d27-179">輸入</span><span class="sxs-lookup"><span data-stu-id="14d27-179">INPUTS</span></span>

### <span data-ttu-id="14d27-180">PSKeyVaultCertificatePolicy 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="14d27-180">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="14d27-181">輸出</span><span class="sxs-lookup"><span data-stu-id="14d27-181">OUTPUTS</span></span>

### <span data-ttu-id="14d27-182">PSKeyVaultCertificatePolicy 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="14d27-182">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="14d27-183">筆記</span><span class="sxs-lookup"><span data-stu-id="14d27-183">NOTES</span></span>

## <span data-ttu-id="14d27-184">相關連結</span><span class="sxs-lookup"><span data-stu-id="14d27-184">RELATED LINKS</span></span>

[<span data-ttu-id="14d27-185">AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="14d27-185">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="14d27-186">新-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="14d27-186">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)
