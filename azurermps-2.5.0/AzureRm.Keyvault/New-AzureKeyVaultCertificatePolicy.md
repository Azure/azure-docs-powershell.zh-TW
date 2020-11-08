---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificatepolicy
schema: 2.0.0
ms.openlocfilehash: b10dd0e034db53af35c930ce1c4588dee2576c75
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800498"
---
# <span data-ttu-id="971c0-101">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="971c0-101">New-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="971c0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="971c0-102">SYNOPSIS</span></span>
<span data-ttu-id="971c0-103">建立記憶體內部的憑證原則物件。</span><span class="sxs-lookup"><span data-stu-id="971c0-103">Creates an in-memory certificate policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="971c0-104">句法</span><span class="sxs-lookup"><span data-stu-id="971c0-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificatePolicy [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-SubjectName <String>] [-DnsNames <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] -IssuerName <String>
 [-CertificateType <String>] [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>]
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="971c0-105">說明</span><span class="sxs-lookup"><span data-stu-id="971c0-105">DESCRIPTION</span></span>
<span data-ttu-id="971c0-106">**新的-AzureKeyVaultCertificatePolicy** Cmdlet 會針對 Azure 金鑰保存庫建立記憶體內部憑證原則物件。</span><span class="sxs-lookup"><span data-stu-id="971c0-106">The **New-AzureKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="971c0-107">示例</span><span class="sxs-lookup"><span data-stu-id="971c0-107">EXAMPLES</span></span>

### <span data-ttu-id="971c0-108">範例1：建立憑證原則</span><span class="sxs-lookup"><span data-stu-id="971c0-108">Example 1: Create a certificate policy</span></span>
```
PS C:\>New-AzureKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
```

<span data-ttu-id="971c0-109">這個命令會建立有效期為6個月的憑證原則，並重複使用金鑰來更新憑證。</span><span class="sxs-lookup"><span data-stu-id="971c0-109">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="971c0-110">參數</span><span class="sxs-lookup"><span data-stu-id="971c0-110">PARAMETERS</span></span>

### <span data-ttu-id="971c0-111">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="971c0-111">-CertificateType</span></span>
<span data-ttu-id="971c0-112">指定發行人的憑證類型。</span><span class="sxs-lookup"><span data-stu-id="971c0-112">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="971c0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="971c0-113">-DefaultProfile</span></span>
<span data-ttu-id="971c0-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="971c0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="971c0-115">-已停用</span><span class="sxs-lookup"><span data-stu-id="971c0-115">-Disabled</span></span>
<span data-ttu-id="971c0-116">表示憑證原則已停用。</span><span class="sxs-lookup"><span data-stu-id="971c0-116">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="971c0-117">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="971c0-117">-DnsNames</span></span>
<span data-ttu-id="971c0-118">指定憑證中的 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="971c0-118">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="971c0-119">-Eku</span><span class="sxs-lookup"><span data-stu-id="971c0-119">-Ekus</span></span>
<span data-ttu-id="971c0-120">指定憑證中 (Eku) 的增強型金鑰用法。</span><span class="sxs-lookup"><span data-stu-id="971c0-120">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="971c0-121">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="971c0-121">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="971c0-122">指定自動通知程式開始前的到期天數。</span><span class="sxs-lookup"><span data-stu-id="971c0-122">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="971c0-123">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="971c0-123">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="971c0-124">指定啟動通知自動程式開始的生命週期百分比。</span><span class="sxs-lookup"><span data-stu-id="971c0-124">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="971c0-125">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="971c0-125">-IssuerName</span></span>
<span data-ttu-id="971c0-126">指定憑證的頒發者名稱。</span><span class="sxs-lookup"><span data-stu-id="971c0-126">Specifies the name of the issuer for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="971c0-127">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="971c0-127">-KeyNotExportable</span></span>
<span data-ttu-id="971c0-128">表示金鑰無法匯出。</span><span class="sxs-lookup"><span data-stu-id="971c0-128">Indicates that the key is not exportable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="971c0-129">-KeyType</span><span class="sxs-lookup"><span data-stu-id="971c0-129">-KeyType</span></span>
<span data-ttu-id="971c0-130">指定支援憑證之金鑰的金鑰類型。</span><span class="sxs-lookup"><span data-stu-id="971c0-130">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="971c0-131">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="971c0-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="971c0-132">與眾不同</span><span class="sxs-lookup"><span data-stu-id="971c0-132">RSA</span></span>
- <span data-ttu-id="971c0-133">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="971c0-133">RSA-HSM</span></span>

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

### <span data-ttu-id="971c0-134">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="971c0-134">-KeyUsage</span></span>
<span data-ttu-id="971c0-135">指定憑證中的金鑰用法。</span><span class="sxs-lookup"><span data-stu-id="971c0-135">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="971c0-136">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="971c0-136">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="971c0-137">指定到期前的天數，在此之後，就會開始更新自動程式。</span><span class="sxs-lookup"><span data-stu-id="971c0-137">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="971c0-138">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="971c0-138">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="971c0-139">指定啟動證書自動程式開始前的生命週期百分比。</span><span class="sxs-lookup"><span data-stu-id="971c0-139">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="971c0-140">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="971c0-140">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="971c0-141">表示憑證在續約時重複使用金鑰。</span><span class="sxs-lookup"><span data-stu-id="971c0-141">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="971c0-142">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="971c0-142">-SecretContentType</span></span>
<span data-ttu-id="971c0-143">指定新的主要電子倉庫密碼的內容類型。</span><span class="sxs-lookup"><span data-stu-id="971c0-143">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="971c0-144">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="971c0-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="971c0-145">應用程式/x-pkcs12</span><span class="sxs-lookup"><span data-stu-id="971c0-145">application/x-pkcs12</span></span>
- <span data-ttu-id="971c0-146">應用程式/x pem-檔案</span><span class="sxs-lookup"><span data-stu-id="971c0-146">application/x-pem-file</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="971c0-147">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="971c0-147">-SubjectName</span></span>
<span data-ttu-id="971c0-148">指定憑證的受領人名稱。</span><span class="sxs-lookup"><span data-stu-id="971c0-148">Specifies the subject name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="971c0-149">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="971c0-149">-ValidityInMonths</span></span>
<span data-ttu-id="971c0-150">指定憑證有效的月份數。</span><span class="sxs-lookup"><span data-stu-id="971c0-150">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="971c0-151">-確認</span><span class="sxs-lookup"><span data-stu-id="971c0-151">-Confirm</span></span>
<span data-ttu-id="971c0-152">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="971c0-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="971c0-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="971c0-153">-WhatIf</span></span>
<span data-ttu-id="971c0-154">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="971c0-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="971c0-155">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="971c0-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="971c0-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="971c0-156">CommonParameters</span></span>
<span data-ttu-id="971c0-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="971c0-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="971c0-158">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="971c0-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="971c0-159">輸入</span><span class="sxs-lookup"><span data-stu-id="971c0-159">INPUTS</span></span>

## <span data-ttu-id="971c0-160">輸出</span><span class="sxs-lookup"><span data-stu-id="971c0-160">OUTPUTS</span></span>

### <span data-ttu-id="971c0-161">KeyVaultCertificatePolicy 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="971c0-161">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="971c0-162">筆記</span><span class="sxs-lookup"><span data-stu-id="971c0-162">NOTES</span></span>

## <span data-ttu-id="971c0-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="971c0-163">RELATED LINKS</span></span>

[<span data-ttu-id="971c0-164">AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="971c0-164">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="971c0-165">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="971c0-165">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)
