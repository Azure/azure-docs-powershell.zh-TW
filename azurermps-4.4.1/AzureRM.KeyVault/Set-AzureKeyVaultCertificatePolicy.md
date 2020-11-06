---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: 94f8b6e136925956faf4402b583d80f6a675cca3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455759"
---
# <span data-ttu-id="9a1f0-101">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="9a1f0-101">Set-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="9a1f0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9a1f0-102">SYNOPSIS</span></span>
<span data-ttu-id="9a1f0-103">在金鑰保存庫中建立或更新憑證的原則。</span><span class="sxs-lookup"><span data-stu-id="9a1f0-103">Creates or updates the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a1f0-104">句法</span><span class="sxs-lookup"><span data-stu-id="9a1f0-104">SYNTAX</span></span>

### <span data-ttu-id="9a1f0-105">展開 (預設) </span><span class="sxs-lookup"><span data-stu-id="9a1f0-105">Expanded (Default)</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-SecretContentType <String>]
 [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsNames <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>]
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [-KeyNotExportable] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9a1f0-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="9a1f0-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [[-CertificatePolicy] <KeyVaultCertificatePolicy>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a1f0-107">說明</span><span class="sxs-lookup"><span data-stu-id="9a1f0-107">DESCRIPTION</span></span>
<span data-ttu-id="9a1f0-108">**AzureKeyVaultCertificatePolicy** Cmdlet 會建立或更新金鑰保存庫中的憑證原則。</span><span class="sxs-lookup"><span data-stu-id="9a1f0-108">The **Set-AzureKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="9a1f0-109">示例</span><span class="sxs-lookup"><span data-stu-id="9a1f0-109">EXAMPLES</span></span>

### <span data-ttu-id="9a1f0-110">範例1：設定憑證原則</span><span class="sxs-lookup"><span data-stu-id="9a1f0-110">Example 1: Set a certificate policy</span></span>
```
PS C:\>Set-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True
```

<span data-ttu-id="9a1f0-111">這個命令會在 ContosoKV01 金鑰保存庫中設定 TestCert01 憑證的原則。</span><span class="sxs-lookup"><span data-stu-id="9a1f0-111">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="9a1f0-112">參數</span><span class="sxs-lookup"><span data-stu-id="9a1f0-112">PARAMETERS</span></span>

### <span data-ttu-id="9a1f0-113">-CertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="9a1f0-113">-CertificatePolicy</span></span>
<span data-ttu-id="9a1f0-114">指定憑證原則。</span><span class="sxs-lookup"><span data-stu-id="9a1f0-114">Specifies the certificate policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy
Parameter Sets: ByValue
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a1f0-115">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="9a1f0-115">-CertificateType</span></span>
<span data-ttu-id="9a1f0-116">指定發行人的憑證類型。</span><span class="sxs-lookup"><span data-stu-id="9a1f0-116">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a1f0-117">-已停用</span><span class="sxs-lookup"><span data-stu-id="9a1f0-117">-Disabled</span></span>
<span data-ttu-id="9a1f0-118">表示憑證原則已停用。</span><span class="sxs-lookup"><span data-stu-id="9a1f0-118">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a1f0-119">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="9a1f0-119">-DnsNames</span></span>
<span data-ttu-id="9a1f0-120">指定憑證中的 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="9a1f0-120">Specifies the DNS names in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a1f0-121">-Eku</span><span class="sxs-lookup"><span data-stu-id="9a1f0-121">-Ekus</span></span>
<span data-ttu-id="9a1f0-122">指定憑證中 (Eku) 的增強型金鑰用法。</span><span class="sxs-lookup"><span data-stu-id="9a1f0-122">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a1f0-123">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="9a1f0-123">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="9a1f0-124">指定自動通知程式開始前的到期天數。</span><span class="sxs-lookup"><span data-stu-id="9a1f0-124">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="9a1f0-125">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="9a1f0-125">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="9a1f0-126">指定啟動通知自動程式開始的生命週期百分比。</span><span class="sxs-lookup"><span data-stu-id="9a1f0-126">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="9a1f0-127">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="9a1f0-127">-IssuerName</span></span>
<span data-ttu-id="9a1f0-128">指定此憑證的頒發者名稱。</span><span class="sxs-lookup"><span data-stu-id="9a1f0-128">Specifies the name of the issuer for this certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a1f0-129">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="9a1f0-129">-KeyNotExportable</span></span>
<span data-ttu-id="9a1f0-130">表示金鑰無法匯出。</span><span class="sxs-lookup"><span data-stu-id="9a1f0-130">Indicates that the key is not exportable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a1f0-131">-KeyType</span><span class="sxs-lookup"><span data-stu-id="9a1f0-131">-KeyType</span></span>
<span data-ttu-id="9a1f0-132">指定支援憑證之金鑰的金鑰類型。</span><span class="sxs-lookup"><span data-stu-id="9a1f0-132">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="9a1f0-133">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="9a1f0-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9a1f0-134">與眾不同</span><span class="sxs-lookup"><span data-stu-id="9a1f0-134">RSA</span></span>
- <span data-ttu-id="9a1f0-135">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="9a1f0-135">RSA-HSM</span></span>

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

### <span data-ttu-id="9a1f0-136">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="9a1f0-136">-KeyUsage</span></span>
<span data-ttu-id="9a1f0-137">指定憑證中的金鑰用法。</span><span class="sxs-lookup"><span data-stu-id="9a1f0-137">Specifies the key usages in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a1f0-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="9a1f0-138">-Name</span></span>
<span data-ttu-id="9a1f0-139">指定憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="9a1f0-139">Specifies the name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a1f0-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a1f0-140">-PassThru</span></span>
<span data-ttu-id="9a1f0-141">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="9a1f0-141">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9a1f0-142">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="9a1f0-142">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9a1f0-143">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="9a1f0-143">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="9a1f0-144">指定到期前的天數，在此之後，就會開始更新自動程式。</span><span class="sxs-lookup"><span data-stu-id="9a1f0-144">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a1f0-145">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="9a1f0-145">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="9a1f0-146">指定啟動證書自動程式開始前的生命週期百分比。</span><span class="sxs-lookup"><span data-stu-id="9a1f0-146">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a1f0-147">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="9a1f0-147">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="9a1f0-148">表示憑證在續約時重複使用金鑰。</span><span class="sxs-lookup"><span data-stu-id="9a1f0-148">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a1f0-149">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="9a1f0-149">-SecretContentType</span></span>
<span data-ttu-id="9a1f0-150">指定新的主要電子倉庫密碼的內容類型。</span><span class="sxs-lookup"><span data-stu-id="9a1f0-150">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="9a1f0-151">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="9a1f0-151">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9a1f0-152">應用程式/x-pkcs12</span><span class="sxs-lookup"><span data-stu-id="9a1f0-152">application/x-pkcs12</span></span>
- <span data-ttu-id="9a1f0-153">應用程式/x pem-檔案</span><span class="sxs-lookup"><span data-stu-id="9a1f0-153">application/x-pem-file</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a1f0-154">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="9a1f0-154">-SubjectName</span></span>
<span data-ttu-id="9a1f0-155">指定憑證的受領人名稱。</span><span class="sxs-lookup"><span data-stu-id="9a1f0-155">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a1f0-156">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="9a1f0-156">-ValidityInMonths</span></span>
<span data-ttu-id="9a1f0-157">指定憑證有效的月份數。</span><span class="sxs-lookup"><span data-stu-id="9a1f0-157">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a1f0-158">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9a1f0-158">-VaultName</span></span>
<span data-ttu-id="9a1f0-159">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="9a1f0-159">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a1f0-160">-確認</span><span class="sxs-lookup"><span data-stu-id="9a1f0-160">-Confirm</span></span>
<span data-ttu-id="9a1f0-161">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9a1f0-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a1f0-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a1f0-162">-WhatIf</span></span>
<span data-ttu-id="9a1f0-163">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9a1f0-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a1f0-164">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9a1f0-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a1f0-165">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a1f0-165">-DefaultProfile</span></span>
<span data-ttu-id="9a1f0-166">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9a1f0-166">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a1f0-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a1f0-167">CommonParameters</span></span>
<span data-ttu-id="9a1f0-168">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9a1f0-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a1f0-169">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9a1f0-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a1f0-170">輸入</span><span class="sxs-lookup"><span data-stu-id="9a1f0-170">INPUTS</span></span>

## <span data-ttu-id="9a1f0-171">輸出</span><span class="sxs-lookup"><span data-stu-id="9a1f0-171">OUTPUTS</span></span>

### <span data-ttu-id="9a1f0-172">KeyVaultCertificatePolicy 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="9a1f0-172">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="9a1f0-173">筆記</span><span class="sxs-lookup"><span data-stu-id="9a1f0-173">NOTES</span></span>

## <span data-ttu-id="9a1f0-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="9a1f0-174">RELATED LINKS</span></span>

[<span data-ttu-id="9a1f0-175">AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="9a1f0-175">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="9a1f0-176">新-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="9a1f0-176">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

