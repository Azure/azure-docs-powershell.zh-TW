---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificatepolicy
schema: 2.0.0
ms.openlocfilehash: 7a9356952f2ea8b4113f5df0fe364e9647e2c733
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801301"
---
# <span data-ttu-id="e398d-101">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="e398d-101">Set-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="e398d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e398d-102">SYNOPSIS</span></span>
<span data-ttu-id="e398d-103">在金鑰保存庫中建立或更新憑證的原則。</span><span class="sxs-lookup"><span data-stu-id="e398d-103">Creates or updates the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e398d-104">句法</span><span class="sxs-lookup"><span data-stu-id="e398d-104">SYNTAX</span></span>

### <span data-ttu-id="e398d-105">展開 (預設) </span><span class="sxs-lookup"><span data-stu-id="e398d-105">Expanded (Default)</span></span>
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

### <span data-ttu-id="e398d-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="e398d-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [[-CertificatePolicy] <KeyVaultCertificatePolicy>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e398d-107">說明</span><span class="sxs-lookup"><span data-stu-id="e398d-107">DESCRIPTION</span></span>
<span data-ttu-id="e398d-108">**AzureKeyVaultCertificatePolicy** Cmdlet 會建立或更新金鑰保存庫中的憑證原則。</span><span class="sxs-lookup"><span data-stu-id="e398d-108">The **Set-AzureKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="e398d-109">示例</span><span class="sxs-lookup"><span data-stu-id="e398d-109">EXAMPLES</span></span>

### <span data-ttu-id="e398d-110">範例1：設定憑證原則</span><span class="sxs-lookup"><span data-stu-id="e398d-110">Example 1: Set a certificate policy</span></span>
```
PS C:\>Set-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True
```

<span data-ttu-id="e398d-111">這個命令會在 ContosoKV01 金鑰保存庫中設定 TestCert01 憑證的原則。</span><span class="sxs-lookup"><span data-stu-id="e398d-111">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="e398d-112">參數</span><span class="sxs-lookup"><span data-stu-id="e398d-112">PARAMETERS</span></span>

### <span data-ttu-id="e398d-113">-CertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="e398d-113">-CertificatePolicy</span></span>
<span data-ttu-id="e398d-114">指定憑證原則。</span><span class="sxs-lookup"><span data-stu-id="e398d-114">Specifies the certificate policy.</span></span>

```yaml
Type: KeyVaultCertificatePolicy
Parameter Sets: ByValue
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e398d-115">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="e398d-115">-CertificateType</span></span>
<span data-ttu-id="e398d-116">指定發行人的憑證類型。</span><span class="sxs-lookup"><span data-stu-id="e398d-116">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e398d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e398d-117">-DefaultProfile</span></span>
<span data-ttu-id="e398d-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e398d-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e398d-119">-已停用</span><span class="sxs-lookup"><span data-stu-id="e398d-119">-Disabled</span></span>
<span data-ttu-id="e398d-120">表示憑證原則已停用。</span><span class="sxs-lookup"><span data-stu-id="e398d-120">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e398d-121">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="e398d-121">-DnsNames</span></span>
<span data-ttu-id="e398d-122">指定憑證中的 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="e398d-122">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="e398d-123">-Eku</span><span class="sxs-lookup"><span data-stu-id="e398d-123">-Ekus</span></span>
<span data-ttu-id="e398d-124">指定憑證中 (Eku) 的增強型金鑰用法。</span><span class="sxs-lookup"><span data-stu-id="e398d-124">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="e398d-125">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="e398d-125">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="e398d-126">指定自動通知程式開始前的到期天數。</span><span class="sxs-lookup"><span data-stu-id="e398d-126">Specifies how many days before expiry the automatic notification process begins.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e398d-127">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="e398d-127">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="e398d-128">指定啟動通知自動程式開始的生命週期百分比。</span><span class="sxs-lookup"><span data-stu-id="e398d-128">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e398d-129">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="e398d-129">-IssuerName</span></span>
<span data-ttu-id="e398d-130">指定此憑證的頒發者名稱。</span><span class="sxs-lookup"><span data-stu-id="e398d-130">Specifies the name of the issuer for this certificate.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e398d-131">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="e398d-131">-KeyNotExportable</span></span>
<span data-ttu-id="e398d-132">表示金鑰無法匯出。</span><span class="sxs-lookup"><span data-stu-id="e398d-132">Indicates that the key is not exportable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e398d-133">-KeyType</span><span class="sxs-lookup"><span data-stu-id="e398d-133">-KeyType</span></span>
<span data-ttu-id="e398d-134">指定支援憑證之金鑰的金鑰類型。</span><span class="sxs-lookup"><span data-stu-id="e398d-134">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="e398d-135">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="e398d-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e398d-136">與眾不同</span><span class="sxs-lookup"><span data-stu-id="e398d-136">RSA</span></span>
- <span data-ttu-id="e398d-137">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="e398d-137">RSA-HSM</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: RSA, RSA-HSM

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e398d-138">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="e398d-138">-KeyUsage</span></span>
<span data-ttu-id="e398d-139">指定憑證中的金鑰用法。</span><span class="sxs-lookup"><span data-stu-id="e398d-139">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="e398d-140">-名稱</span><span class="sxs-lookup"><span data-stu-id="e398d-140">-Name</span></span>
<span data-ttu-id="e398d-141">指定憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="e398d-141">Specifies the name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e398d-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e398d-142">-PassThru</span></span>
<span data-ttu-id="e398d-143">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="e398d-143">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e398d-144">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="e398d-144">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e398d-145">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="e398d-145">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="e398d-146">指定到期前的天數，在此之後，就會開始更新自動程式。</span><span class="sxs-lookup"><span data-stu-id="e398d-146">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e398d-147">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="e398d-147">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="e398d-148">指定啟動證書自動程式開始前的生命週期百分比。</span><span class="sxs-lookup"><span data-stu-id="e398d-148">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e398d-149">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="e398d-149">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="e398d-150">表示憑證在續約時重複使用金鑰。</span><span class="sxs-lookup"><span data-stu-id="e398d-150">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: Boolean
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e398d-151">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="e398d-151">-SecretContentType</span></span>
<span data-ttu-id="e398d-152">指定新的主要電子倉庫密碼的內容類型。</span><span class="sxs-lookup"><span data-stu-id="e398d-152">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="e398d-153">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="e398d-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e398d-154">應用程式/x-pkcs12</span><span class="sxs-lookup"><span data-stu-id="e398d-154">application/x-pkcs12</span></span>
- <span data-ttu-id="e398d-155">應用程式/x pem-檔案</span><span class="sxs-lookup"><span data-stu-id="e398d-155">application/x-pem-file</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases: 
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e398d-156">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="e398d-156">-SubjectName</span></span>
<span data-ttu-id="e398d-157">指定憑證的受領人名稱。</span><span class="sxs-lookup"><span data-stu-id="e398d-157">Specifies the subject name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e398d-158">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="e398d-158">-ValidityInMonths</span></span>
<span data-ttu-id="e398d-159">指定憑證有效的月份數。</span><span class="sxs-lookup"><span data-stu-id="e398d-159">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: Int32
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e398d-160">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e398d-160">-VaultName</span></span>
<span data-ttu-id="e398d-161">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="e398d-161">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e398d-162">-確認</span><span class="sxs-lookup"><span data-stu-id="e398d-162">-Confirm</span></span>
<span data-ttu-id="e398d-163">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e398d-163">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e398d-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e398d-164">-WhatIf</span></span>
<span data-ttu-id="e398d-165">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e398d-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e398d-166">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e398d-166">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e398d-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e398d-167">CommonParameters</span></span>
<span data-ttu-id="e398d-168">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e398d-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e398d-169">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e398d-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e398d-170">輸入</span><span class="sxs-lookup"><span data-stu-id="e398d-170">INPUTS</span></span>

## <span data-ttu-id="e398d-171">輸出</span><span class="sxs-lookup"><span data-stu-id="e398d-171">OUTPUTS</span></span>

### <span data-ttu-id="e398d-172">KeyVaultCertificatePolicy 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="e398d-172">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="e398d-173">筆記</span><span class="sxs-lookup"><span data-stu-id="e398d-173">NOTES</span></span>

## <span data-ttu-id="e398d-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="e398d-174">RELATED LINKS</span></span>

[<span data-ttu-id="e398d-175">AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="e398d-175">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="e398d-176">新-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="e398d-176">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)
