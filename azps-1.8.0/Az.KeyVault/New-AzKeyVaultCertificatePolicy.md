---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: e5b03660c37dff6333479c19d7de039d368fd4ee
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787362"
---
# <span data-ttu-id="ab129-101">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="ab129-101">New-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="ab129-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ab129-102">SYNOPSIS</span></span>
<span data-ttu-id="ab129-103">建立記憶體內部的憑證原則物件。</span><span class="sxs-lookup"><span data-stu-id="ab129-103">Creates an in-memory certificate policy object.</span></span>

## <span data-ttu-id="ab129-104">句法</span><span class="sxs-lookup"><span data-stu-id="ab129-104">SYNTAX</span></span>

### <span data-ttu-id="ab129-105">SubjectName (預設) </span><span class="sxs-lookup"><span data-stu-id="ab129-105">SubjectName (Default)</span></span>
```
New-AzKeyVaultCertificatePolicy [-IssuerName] <String> [-SubjectName] <String>
 [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>]
 [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ab129-106">DNSNames</span><span class="sxs-lookup"><span data-stu-id="ab129-106">DNSNames</span></span>
```
New-AzKeyVaultCertificatePolicy [-IssuerName] <String> [[-SubjectName] <String>]
 [-DnsName] <System.Collections.Generic.List`1[System.String]> [-RenewAtNumberOfDaysBeforeExpiry <Int32>]
 [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ab129-107">說明</span><span class="sxs-lookup"><span data-stu-id="ab129-107">DESCRIPTION</span></span>
<span data-ttu-id="ab129-108">**新的-AzKeyVaultCertificatePolicy** Cmdlet 會針對 Azure 金鑰保存庫建立記憶體內部憑證原則物件。</span><span class="sxs-lookup"><span data-stu-id="ab129-108">The **New-AzKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="ab129-109">示例</span><span class="sxs-lookup"><span data-stu-id="ab129-109">EXAMPLES</span></span>

### <span data-ttu-id="ab129-110">範例1：建立憑證原則</span><span class="sxs-lookup"><span data-stu-id="ab129-110">Example 1: Create a certificate policy</span></span>
```powershell
PS C:\> New-AzKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal

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

<span data-ttu-id="ab129-111">這個命令會建立有效期為6個月的憑證原則，並重複使用金鑰來更新憑證。</span><span class="sxs-lookup"><span data-stu-id="ab129-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="ab129-112">參數</span><span class="sxs-lookup"><span data-stu-id="ab129-112">PARAMETERS</span></span>

### <span data-ttu-id="ab129-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="ab129-113">-CertificateType</span></span>
<span data-ttu-id="ab129-114">指定發行人的憑證類型。</span><span class="sxs-lookup"><span data-stu-id="ab129-114">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="ab129-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab129-115">-DefaultProfile</span></span>
<span data-ttu-id="ab129-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ab129-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab129-117">-已停用</span><span class="sxs-lookup"><span data-stu-id="ab129-117">-Disabled</span></span>
<span data-ttu-id="ab129-118">表示憑證原則已停用。</span><span class="sxs-lookup"><span data-stu-id="ab129-118">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="ab129-119">-DnsName</span><span class="sxs-lookup"><span data-stu-id="ab129-119">-DnsName</span></span>
<span data-ttu-id="ab129-120">指定憑證中的 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="ab129-120">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="ab129-121">-Eku</span><span class="sxs-lookup"><span data-stu-id="ab129-121">-Ekus</span></span>
<span data-ttu-id="ab129-122">指定憑證中 (Eku) 的增強型金鑰用法。</span><span class="sxs-lookup"><span data-stu-id="ab129-122">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="ab129-123">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="ab129-123">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="ab129-124">指定自動通知程式開始前的到期天數。</span><span class="sxs-lookup"><span data-stu-id="ab129-124">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="ab129-125">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="ab129-125">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="ab129-126">指定啟動通知自動程式開始的生命週期百分比。</span><span class="sxs-lookup"><span data-stu-id="ab129-126">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="ab129-127">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="ab129-127">-IssuerName</span></span>
<span data-ttu-id="ab129-128">指定憑證的頒發者名稱。</span><span class="sxs-lookup"><span data-stu-id="ab129-128">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="ab129-129">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="ab129-129">-KeyNotExportable</span></span>
<span data-ttu-id="ab129-130">表示金鑰無法匯出。</span><span class="sxs-lookup"><span data-stu-id="ab129-130">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="ab129-131">-KeyType</span><span class="sxs-lookup"><span data-stu-id="ab129-131">-KeyType</span></span>
<span data-ttu-id="ab129-132">指定支援憑證之金鑰的金鑰類型。</span><span class="sxs-lookup"><span data-stu-id="ab129-132">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="ab129-133">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ab129-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ab129-134">與眾不同</span><span class="sxs-lookup"><span data-stu-id="ab129-134">RSA</span></span>
- <span data-ttu-id="ab129-135">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="ab129-135">RSA-HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab129-136">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="ab129-136">-KeyUsage</span></span>
<span data-ttu-id="ab129-137">指定憑證中的金鑰用法。</span><span class="sxs-lookup"><span data-stu-id="ab129-137">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="ab129-138">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="ab129-138">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="ab129-139">指定到期前的天數，在此之後，就會開始更新自動程式。</span><span class="sxs-lookup"><span data-stu-id="ab129-139">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="ab129-140">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="ab129-140">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="ab129-141">指定啟動證書自動程式開始前的生命週期百分比。</span><span class="sxs-lookup"><span data-stu-id="ab129-141">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="ab129-142">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="ab129-142">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="ab129-143">表示憑證在續約時重複使用金鑰。</span><span class="sxs-lookup"><span data-stu-id="ab129-143">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="ab129-144">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="ab129-144">-SecretContentType</span></span>
<span data-ttu-id="ab129-145">指定新的主要電子倉庫密碼的內容類型。</span><span class="sxs-lookup"><span data-stu-id="ab129-145">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="ab129-146">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ab129-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ab129-147">應用程式/x-pkcs12</span><span class="sxs-lookup"><span data-stu-id="ab129-147">application/x-pkcs12</span></span>
- <span data-ttu-id="ab129-148">應用程式/x pem-檔案</span><span class="sxs-lookup"><span data-stu-id="ab129-148">application/x-pem-file</span></span>

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

### <span data-ttu-id="ab129-149">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="ab129-149">-SubjectName</span></span>
<span data-ttu-id="ab129-150">指定憑證的受領人名稱。</span><span class="sxs-lookup"><span data-stu-id="ab129-150">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="ab129-151">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="ab129-151">-ValidityInMonths</span></span>
<span data-ttu-id="ab129-152">指定憑證有效的月份數。</span><span class="sxs-lookup"><span data-stu-id="ab129-152">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="ab129-153">-確認</span><span class="sxs-lookup"><span data-stu-id="ab129-153">-Confirm</span></span>
<span data-ttu-id="ab129-154">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ab129-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab129-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab129-155">-WhatIf</span></span>
<span data-ttu-id="ab129-156">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ab129-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab129-157">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ab129-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab129-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab129-158">CommonParameters</span></span>
<span data-ttu-id="ab129-159">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ab129-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab129-160">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ab129-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab129-161">輸入</span><span class="sxs-lookup"><span data-stu-id="ab129-161">INPUTS</span></span>

### <span data-ttu-id="ab129-162">System.object</span><span class="sxs-lookup"><span data-stu-id="ab129-162">System.String</span></span>

### <span data-ttu-id="ab129-163">[System.object]。清單 ' 1 [CoreLib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ab129-163">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ab129-164">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ab129-164">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ab129-165">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="ab129-165">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="ab129-166">[System.object]。清單 ' 1 [X509Certificates. X509KeyUsageFlags，系統. X509Certificates，版本 = 4.2.1.0，Culture = 中性，PublicKeyToken = b03f5f7f11d50a3a]]。</span><span class="sxs-lookup"><span data-stu-id="ab129-166">System.Collections.Generic.List\`1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System.Security.Cryptography.X509Certificates, Version=4.2.1.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a]]</span></span>

## <span data-ttu-id="ab129-167">輸出</span><span class="sxs-lookup"><span data-stu-id="ab129-167">OUTPUTS</span></span>

### <span data-ttu-id="ab129-168">PSKeyVaultCertificatePolicy 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="ab129-168">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="ab129-169">筆記</span><span class="sxs-lookup"><span data-stu-id="ab129-169">NOTES</span></span>

## <span data-ttu-id="ab129-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="ab129-170">RELATED LINKS</span></span>

[<span data-ttu-id="ab129-171">AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="ab129-171">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="ab129-172">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="ab129-172">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)
