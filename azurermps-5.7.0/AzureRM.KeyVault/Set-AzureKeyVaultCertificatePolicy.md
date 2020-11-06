---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: e960aa211b53c79087e67e2bd86504e597a718d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456199"
---
# <span data-ttu-id="5a140-101">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="5a140-101">Set-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="5a140-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5a140-102">SYNOPSIS</span></span>
<span data-ttu-id="5a140-103">在金鑰保存庫中建立或更新憑證的原則。</span><span class="sxs-lookup"><span data-stu-id="5a140-103">Creates or updates the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a140-104">句法</span><span class="sxs-lookup"><span data-stu-id="5a140-104">SYNTAX</span></span>

### <span data-ttu-id="5a140-105">ExpandedRenewPercentage (預設) </span><span class="sxs-lookup"><span data-stu-id="5a140-105">ExpandedRenewPercentage (Default)</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-RenewAtPercentageLifetime <Int32>]
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a140-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="5a140-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a140-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="5a140-107">ExpandedRenewNumber</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 -RenewAtNumberOfDaysBeforeExpiry <Int32> [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>]
 [-Disabled] [-SubjectName <String>] [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a140-108">說明</span><span class="sxs-lookup"><span data-stu-id="5a140-108">DESCRIPTION</span></span>
<span data-ttu-id="5a140-109">**AzureKeyVaultCertificatePolicy** Cmdlet 會建立或更新金鑰保存庫中的憑證原則。</span><span class="sxs-lookup"><span data-stu-id="5a140-109">The **Set-AzureKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="5a140-110">示例</span><span class="sxs-lookup"><span data-stu-id="5a140-110">EXAMPLES</span></span>

### <span data-ttu-id="5a140-111">範例1：設定憑證原則</span><span class="sxs-lookup"><span data-stu-id="5a140-111">Example 1: Set a certificate policy</span></span>
```
PS C:\>Set-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True
```

<span data-ttu-id="5a140-112">這個命令會在 ContosoKV01 金鑰保存庫中設定 TestCert01 憑證的原則。</span><span class="sxs-lookup"><span data-stu-id="5a140-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="5a140-113">參數</span><span class="sxs-lookup"><span data-stu-id="5a140-113">PARAMETERS</span></span>

### <span data-ttu-id="5a140-114">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="5a140-114">-CertificateType</span></span>
<span data-ttu-id="5a140-115">指定發行人的憑證類型。</span><span class="sxs-lookup"><span data-stu-id="5a140-115">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a140-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a140-116">-DefaultProfile</span></span>
<span data-ttu-id="5a140-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="5a140-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a140-118">-已停用</span><span class="sxs-lookup"><span data-stu-id="5a140-118">-Disabled</span></span>
<span data-ttu-id="5a140-119">表示憑證原則已停用。</span><span class="sxs-lookup"><span data-stu-id="5a140-119">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a140-120">-DnsName</span><span class="sxs-lookup"><span data-stu-id="5a140-120">-DnsName</span></span>
<span data-ttu-id="5a140-121">指定憑證的受領人名稱。</span><span class="sxs-lookup"><span data-stu-id="5a140-121">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases: DnsNames

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a140-122">-Eku</span><span class="sxs-lookup"><span data-stu-id="5a140-122">-Ekus</span></span>
<span data-ttu-id="5a140-123">指定憑證中 (Eku) 的增強型金鑰用法。</span><span class="sxs-lookup"><span data-stu-id="5a140-123">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a140-124">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="5a140-124">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="5a140-125">指定自動續約開始時到期前的天數。</span><span class="sxs-lookup"><span data-stu-id="5a140-125">Specifies the number of days before expiration when automatic renewal should start.</span></span>

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

### <span data-ttu-id="5a140-126">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="5a140-126">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="5a140-127">指定啟動通知自動程式開始的生命週期百分比。</span><span class="sxs-lookup"><span data-stu-id="5a140-127">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="5a140-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a140-128">-InputObject</span></span>
<span data-ttu-id="5a140-129">指定憑證原則。</span><span class="sxs-lookup"><span data-stu-id="5a140-129">Specifies the certificate policy.</span></span>

```yaml
Type: PSKeyVaultCertificatePolicy
Parameter Sets: ByValue
Aliases: CertificatePolicy

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a140-130">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="5a140-130">-IssuerName</span></span>
<span data-ttu-id="5a140-131">指定此憑證的頒發者名稱。</span><span class="sxs-lookup"><span data-stu-id="5a140-131">Specifies the name of the issuer for this certificate.</span></span>

```yaml
Type: String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a140-132">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="5a140-132">-KeyNotExportable</span></span>
<span data-ttu-id="5a140-133">表示金鑰無法匯出。</span><span class="sxs-lookup"><span data-stu-id="5a140-133">Indicates that the key is not exportable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a140-134">-KeyType</span><span class="sxs-lookup"><span data-stu-id="5a140-134">-KeyType</span></span>
<span data-ttu-id="5a140-135">指定支援憑證之金鑰的金鑰類型。</span><span class="sxs-lookup"><span data-stu-id="5a140-135">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="5a140-136">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="5a140-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5a140-137">與眾不同</span><span class="sxs-lookup"><span data-stu-id="5a140-137">RSA</span></span>
- <span data-ttu-id="5a140-138">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="5a140-138">RSA-HSM</span></span>

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

### <span data-ttu-id="5a140-139">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="5a140-139">-KeyUsage</span></span>
<span data-ttu-id="5a140-140">指定憑證中的金鑰用法。</span><span class="sxs-lookup"><span data-stu-id="5a140-140">Specifies the key usages in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a140-141">-名稱</span><span class="sxs-lookup"><span data-stu-id="5a140-141">-Name</span></span>
<span data-ttu-id="5a140-142">指定憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="5a140-142">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="5a140-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a140-143">-PassThru</span></span>
<span data-ttu-id="5a140-144">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="5a140-144">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5a140-145">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="5a140-145">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5a140-146">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="5a140-146">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="5a140-147">指定到期前的天數，在此之後，就會開始更新自動程式。</span><span class="sxs-lookup"><span data-stu-id="5a140-147">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: ExpandedRenewNumber
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a140-148">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="5a140-148">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="5a140-149">指定啟動證書自動程式開始前的生命週期百分比。</span><span class="sxs-lookup"><span data-stu-id="5a140-149">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: ExpandedRenewPercentage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a140-150">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="5a140-150">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="5a140-151">表示憑證在續約時重複使用金鑰。</span><span class="sxs-lookup"><span data-stu-id="5a140-151">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: Boolean
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a140-152">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="5a140-152">-SecretContentType</span></span>
<span data-ttu-id="5a140-153">指定新的主要電子倉庫密碼的內容類型。</span><span class="sxs-lookup"><span data-stu-id="5a140-153">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="5a140-154">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="5a140-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5a140-155">應用程式/x-pkcs12</span><span class="sxs-lookup"><span data-stu-id="5a140-155">application/x-pkcs12</span></span>
- <span data-ttu-id="5a140-156">應用程式/x pem-檔案</span><span class="sxs-lookup"><span data-stu-id="5a140-156">application/x-pem-file</span></span>

```yaml
Type: String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a140-157">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="5a140-157">-SubjectName</span></span>
<span data-ttu-id="5a140-158">指定憑證的受領人名稱。</span><span class="sxs-lookup"><span data-stu-id="5a140-158">Specifies the subject name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a140-159">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="5a140-159">-ValidityInMonths</span></span>
<span data-ttu-id="5a140-160">指定憑證有效的月份數。</span><span class="sxs-lookup"><span data-stu-id="5a140-160">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: Int32
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a140-161">-VaultName</span><span class="sxs-lookup"><span data-stu-id="5a140-161">-VaultName</span></span>
<span data-ttu-id="5a140-162">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="5a140-162">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="5a140-163">-確認</span><span class="sxs-lookup"><span data-stu-id="5a140-163">-Confirm</span></span>
<span data-ttu-id="5a140-164">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5a140-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a140-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a140-165">-WhatIf</span></span>
<span data-ttu-id="5a140-166">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5a140-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a140-167">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5a140-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a140-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a140-168">CommonParameters</span></span>
<span data-ttu-id="5a140-169">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5a140-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a140-170">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5a140-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a140-171">輸入</span><span class="sxs-lookup"><span data-stu-id="5a140-171">INPUTS</span></span>

### <span data-ttu-id="5a140-172">所有</span><span class="sxs-lookup"><span data-stu-id="5a140-172">None</span></span>
<span data-ttu-id="5a140-173">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="5a140-173">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5a140-174">輸出</span><span class="sxs-lookup"><span data-stu-id="5a140-174">OUTPUTS</span></span>

### <span data-ttu-id="5a140-175">PSKeyVaultCertificatePolicy 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="5a140-175">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="5a140-176">筆記</span><span class="sxs-lookup"><span data-stu-id="5a140-176">NOTES</span></span>

## <span data-ttu-id="5a140-177">相關連結</span><span class="sxs-lookup"><span data-stu-id="5a140-177">RELATED LINKS</span></span>

[<span data-ttu-id="5a140-178">AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="5a140-178">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="5a140-179">新-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="5a140-179">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

