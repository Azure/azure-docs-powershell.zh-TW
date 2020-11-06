---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: 381ce302a8404c0bb643db0fc82e392fe53d956a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446786"
---
# <span data-ttu-id="57e6c-101">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="57e6c-101">New-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="57e6c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="57e6c-102">SYNOPSIS</span></span>
<span data-ttu-id="57e6c-103">建立記憶體內部的憑證原則物件。</span><span class="sxs-lookup"><span data-stu-id="57e6c-103">Creates an in-memory certificate policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57e6c-104">句法</span><span class="sxs-lookup"><span data-stu-id="57e6c-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificatePolicy [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-SubjectName <String>] [-DnsNames <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] -IssuerName <String>
 [-CertificateType <String>] [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>]
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57e6c-105">說明</span><span class="sxs-lookup"><span data-stu-id="57e6c-105">DESCRIPTION</span></span>
<span data-ttu-id="57e6c-106">**新的-AzureKeyVaultCertificatePolicy** Cmdlet 會針對 Azure 金鑰保存庫建立記憶體內部憑證原則物件。</span><span class="sxs-lookup"><span data-stu-id="57e6c-106">The **New-AzureKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="57e6c-107">示例</span><span class="sxs-lookup"><span data-stu-id="57e6c-107">EXAMPLES</span></span>

### <span data-ttu-id="57e6c-108">範例1：建立憑證原則</span><span class="sxs-lookup"><span data-stu-id="57e6c-108">Example 1: Create a certificate policy</span></span>
```
PS C:\>New-AzureKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
```

<span data-ttu-id="57e6c-109">這個命令會建立有效期為6個月的憑證原則，並重複使用金鑰來更新憑證。</span><span class="sxs-lookup"><span data-stu-id="57e6c-109">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="57e6c-110">參數</span><span class="sxs-lookup"><span data-stu-id="57e6c-110">PARAMETERS</span></span>

### <span data-ttu-id="57e6c-111">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="57e6c-111">-CertificateType</span></span>
<span data-ttu-id="57e6c-112">指定發行人的憑證類型。</span><span class="sxs-lookup"><span data-stu-id="57e6c-112">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="57e6c-113">-已停用</span><span class="sxs-lookup"><span data-stu-id="57e6c-113">-Disabled</span></span>
<span data-ttu-id="57e6c-114">表示憑證原則已停用。</span><span class="sxs-lookup"><span data-stu-id="57e6c-114">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="57e6c-115">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="57e6c-115">-DnsNames</span></span>
<span data-ttu-id="57e6c-116">指定憑證中的 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="57e6c-116">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="57e6c-117">-Eku</span><span class="sxs-lookup"><span data-stu-id="57e6c-117">-Ekus</span></span>
<span data-ttu-id="57e6c-118">指定憑證中 (Eku) 的增強型金鑰用法。</span><span class="sxs-lookup"><span data-stu-id="57e6c-118">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="57e6c-119">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="57e6c-119">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="57e6c-120">指定自動通知程式開始前的到期天數。</span><span class="sxs-lookup"><span data-stu-id="57e6c-120">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="57e6c-121">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="57e6c-121">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="57e6c-122">指定啟動通知自動程式開始的生命週期百分比。</span><span class="sxs-lookup"><span data-stu-id="57e6c-122">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="57e6c-123">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="57e6c-123">-IssuerName</span></span>
<span data-ttu-id="57e6c-124">指定憑證的頒發者名稱。</span><span class="sxs-lookup"><span data-stu-id="57e6c-124">Specifies the name of the issuer for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57e6c-125">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="57e6c-125">-KeyNotExportable</span></span>
<span data-ttu-id="57e6c-126">表示金鑰無法匯出。</span><span class="sxs-lookup"><span data-stu-id="57e6c-126">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="57e6c-127">-KeyType</span><span class="sxs-lookup"><span data-stu-id="57e6c-127">-KeyType</span></span>
<span data-ttu-id="57e6c-128">指定支援憑證之金鑰的金鑰類型。</span><span class="sxs-lookup"><span data-stu-id="57e6c-128">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="57e6c-129">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="57e6c-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="57e6c-130">與眾不同</span><span class="sxs-lookup"><span data-stu-id="57e6c-130">RSA</span></span>
- <span data-ttu-id="57e6c-131">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="57e6c-131">RSA-HSM</span></span>

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

### <span data-ttu-id="57e6c-132">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="57e6c-132">-KeyUsage</span></span>
<span data-ttu-id="57e6c-133">指定憑證中的金鑰用法。</span><span class="sxs-lookup"><span data-stu-id="57e6c-133">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="57e6c-134">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="57e6c-134">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="57e6c-135">指定到期前的天數，在此之後，就會開始更新自動程式。</span><span class="sxs-lookup"><span data-stu-id="57e6c-135">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="57e6c-136">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="57e6c-136">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="57e6c-137">指定啟動證書自動程式開始前的生命週期百分比。</span><span class="sxs-lookup"><span data-stu-id="57e6c-137">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="57e6c-138">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="57e6c-138">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="57e6c-139">表示憑證在續約時重複使用金鑰。</span><span class="sxs-lookup"><span data-stu-id="57e6c-139">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="57e6c-140">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="57e6c-140">-SecretContentType</span></span>
<span data-ttu-id="57e6c-141">指定新的主要電子倉庫密碼的內容類型。</span><span class="sxs-lookup"><span data-stu-id="57e6c-141">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="57e6c-142">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="57e6c-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="57e6c-143">應用程式/x-pkcs12</span><span class="sxs-lookup"><span data-stu-id="57e6c-143">application/x-pkcs12</span></span>
- <span data-ttu-id="57e6c-144">應用程式/x pem-檔案</span><span class="sxs-lookup"><span data-stu-id="57e6c-144">application/x-pem-file</span></span>

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

### <span data-ttu-id="57e6c-145">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="57e6c-145">-SubjectName</span></span>
<span data-ttu-id="57e6c-146">指定憑證的受領人名稱。</span><span class="sxs-lookup"><span data-stu-id="57e6c-146">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="57e6c-147">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="57e6c-147">-ValidityInMonths</span></span>
<span data-ttu-id="57e6c-148">指定憑證有效的月份數。</span><span class="sxs-lookup"><span data-stu-id="57e6c-148">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="57e6c-149">-確認</span><span class="sxs-lookup"><span data-stu-id="57e6c-149">-Confirm</span></span>
<span data-ttu-id="57e6c-150">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="57e6c-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57e6c-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57e6c-151">-WhatIf</span></span>
<span data-ttu-id="57e6c-152">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="57e6c-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57e6c-153">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="57e6c-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57e6c-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57e6c-154">-DefaultProfile</span></span>
<span data-ttu-id="57e6c-155">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="57e6c-155">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57e6c-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57e6c-156">CommonParameters</span></span>
<span data-ttu-id="57e6c-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="57e6c-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57e6c-158">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="57e6c-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57e6c-159">輸入</span><span class="sxs-lookup"><span data-stu-id="57e6c-159">INPUTS</span></span>

## <span data-ttu-id="57e6c-160">輸出</span><span class="sxs-lookup"><span data-stu-id="57e6c-160">OUTPUTS</span></span>

### <span data-ttu-id="57e6c-161">KeyVaultCertificatePolicy 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="57e6c-161">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="57e6c-162">筆記</span><span class="sxs-lookup"><span data-stu-id="57e6c-162">NOTES</span></span>

## <span data-ttu-id="57e6c-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="57e6c-163">RELATED LINKS</span></span>

[<span data-ttu-id="57e6c-164">AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="57e6c-164">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="57e6c-165">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="57e6c-165">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

