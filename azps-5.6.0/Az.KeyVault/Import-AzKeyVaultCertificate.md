---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: D4188DC6-A8AB-4B45-9781-94B74C338C63
online version: https://docs.microsoft.com/powershell/module/az.keyvault/import-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultCertificate.md
ms.openlocfilehash: 507bcce6607566c733ee4cd52f72f7e7910ac90f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914806"
---
# <span data-ttu-id="00389-101">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="00389-101">Import-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="00389-102">簡介</span><span class="sxs-lookup"><span data-stu-id="00389-102">SYNOPSIS</span></span>
<span data-ttu-id="00389-103">將憑證導入到金鑰庫。</span><span class="sxs-lookup"><span data-stu-id="00389-103">Imports a certificate to a key vault.</span></span>

## <span data-ttu-id="00389-104">語法</span><span class="sxs-lookup"><span data-stu-id="00389-104">SYNTAX</span></span>

### <span data-ttu-id="00389-105">ImportCertificateFromFile (預設) </span><span class="sxs-lookup"><span data-stu-id="00389-105">ImportCertificateFromFile (Default)</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="00389-106">ImportWithPrivateKeyFromString</span><span class="sxs-lookup"><span data-stu-id="00389-106">ImportWithPrivateKeyFromString</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> -CertificateString <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="00389-107">ImportWithPrivateKeyFromCollection</span><span class="sxs-lookup"><span data-stu-id="00389-107">ImportWithPrivateKeyFromCollection</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [-CertificateCollection] <X509Certificate2Collection> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00389-108">描述</span><span class="sxs-lookup"><span data-stu-id="00389-108">DESCRIPTION</span></span>
<span data-ttu-id="00389-109">**Import-AzKeyVaultCertificate** Cmdlet 將憑證導入金鑰庫。</span><span class="sxs-lookup"><span data-stu-id="00389-109">The **Import-AzKeyVaultCertificate** cmdlet imports a certificate into a key vault.</span></span>
<span data-ttu-id="00389-110">您可以使用下列其中一種方法建立要匯出的憑證：</span><span class="sxs-lookup"><span data-stu-id="00389-110">You can create the certificate to import by using one of the following methods:</span></span>
- <span data-ttu-id="00389-111">用於 `Add-AzKeyVaultCertificate` 建立憑證簽署要求，並提交給憑證授權單位。</span><span class="sxs-lookup"><span data-stu-id="00389-111">Use `Add-AzKeyVaultCertificate` to create a certificate signing request and submit it to a certificate authority.</span></span> <span data-ttu-id="00389-112">看到 https://docs.microsoft.com/azure/key-vault/certificates/create-certificate-signing-request</span><span class="sxs-lookup"><span data-stu-id="00389-112">See https://docs.microsoft.com/azure/key-vault/certificates/create-certificate-signing-request</span></span>
- <span data-ttu-id="00389-113">使用同時包含憑證和私密金鑰的現有憑證套件檔案，例如 .pfx 或 .p12 檔案。</span><span class="sxs-lookup"><span data-stu-id="00389-113">Use an existing certificate package file, such as a .pfx or .p12 file, which contains both the certificate and private key.</span></span>

## <span data-ttu-id="00389-114">例子</span><span class="sxs-lookup"><span data-stu-id="00389-114">EXAMPLES</span></span>

### <span data-ttu-id="00389-115">範例 1：匯出金鑰庫憑證</span><span class="sxs-lookup"><span data-stu-id="00389-115">Example 1: Import a key vault certificate</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS C:\> Import-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "ImportCert01" -FilePath "C:\Users\contosoUser\Desktop\import.pfx" -Password $Password

Name        : importCert01
Certificate : [Subject]
                CN=contoso.com

              [Issuer]
                CN=contoso.com

              [Serial Number]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

              [Not Before]
                2/8/2016 3:11:45 PM

              [Not After]
                8/8/2016 4:21:45 PM

              [Thumbprint]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

Thumbprint  : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Tags        :
Enabled     : True
Created     : 2/8/2016 11:50:43 PM
Updated     : 2/8/2016 11:50:43 PM
```

<span data-ttu-id="00389-116">第一個命令使用 ConvertTo-SecureString Cmdlet 建立安全的密碼，然後將它儲存在$Password變數中。</span><span class="sxs-lookup"><span data-stu-id="00389-116">The first command uses the ConvertTo-SecureString cmdlet to create a secure password, and then stores it in the $Password variable.</span></span>
<span data-ttu-id="00389-117">第二個命令將名稱為 ImportCert01 的憑證導入到 CosotosoKV01 金鑰庫。</span><span class="sxs-lookup"><span data-stu-id="00389-117">The second command imports the certificate named ImportCert01 into the CosotosoKV01 key vault.</span></span>

## <span data-ttu-id="00389-118">參數</span><span class="sxs-lookup"><span data-stu-id="00389-118">PARAMETERS</span></span>

### <span data-ttu-id="00389-119">-CertificateCollection</span><span class="sxs-lookup"><span data-stu-id="00389-119">-CertificateCollection</span></span>
<span data-ttu-id="00389-120">指定要新加入金鑰庫的憑證集合。</span><span class="sxs-lookup"><span data-stu-id="00389-120">Specifies the certificate collection to add to a key vault.</span></span>

```yaml
Type: System.Security.Cryptography.X509Certificates.X509Certificate2Collection
Parameter Sets: ImportWithPrivateKeyFromCollection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00389-121">-CertificateString</span><span class="sxs-lookup"><span data-stu-id="00389-121">-CertificateString</span></span>
<span data-ttu-id="00389-122">指定憑證字串。</span><span class="sxs-lookup"><span data-stu-id="00389-122">Specifies a certificate string.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportWithPrivateKeyFromString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00389-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00389-123">-DefaultProfile</span></span>
<span data-ttu-id="00389-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="00389-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="00389-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="00389-125">-FilePath</span></span>
<span data-ttu-id="00389-126">指定此 Cmdlet 所導入之憑證檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="00389-126">Specifies the path of the certificate file that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportCertificateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00389-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="00389-127">-Name</span></span>
<span data-ttu-id="00389-128">指定憑證名稱。</span><span class="sxs-lookup"><span data-stu-id="00389-128">Specifies the certificate name.</span></span> <span data-ttu-id="00389-129">此 Cmdlet 會從金鑰庫名稱、目前選取的環境 (憑證名稱) 完整功能變數名稱的 FQDN 名稱。</span><span class="sxs-lookup"><span data-stu-id="00389-129">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate from key vault name, currently selected environment, and certificate name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00389-130">-密碼</span><span class="sxs-lookup"><span data-stu-id="00389-130">-Password</span></span>
<span data-ttu-id="00389-131">指定憑證檔案的密碼。</span><span class="sxs-lookup"><span data-stu-id="00389-131">Specifies the password for a certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ImportCertificateFromFile, ImportWithPrivateKeyFromString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00389-132">-標記</span><span class="sxs-lookup"><span data-stu-id="00389-132">-Tag</span></span>
<span data-ttu-id="00389-133">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="00389-133">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="00389-134">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="00389-134">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00389-135">-VaultName</span><span class="sxs-lookup"><span data-stu-id="00389-135">-VaultName</span></span>
<span data-ttu-id="00389-136">指定此 Cmdlet 所輸入憑證的金鑰庫名稱。</span><span class="sxs-lookup"><span data-stu-id="00389-136">Specifies the key vault name into which this cmdlet imports certificates.</span></span>
<span data-ttu-id="00389-137">此 Cmdlet 會根據名稱 (目前選取的環境) 金鑰庫的 FQDN) 建構完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="00389-137">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="00389-138">-確認</span><span class="sxs-lookup"><span data-stu-id="00389-138">-Confirm</span></span>
<span data-ttu-id="00389-139">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="00389-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00389-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00389-140">-WhatIf</span></span>
<span data-ttu-id="00389-141">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="00389-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00389-142">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="00389-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00389-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00389-143">CommonParameters</span></span>
<span data-ttu-id="00389-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="00389-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00389-145">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="00389-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00389-146">輸入</span><span class="sxs-lookup"><span data-stu-id="00389-146">INPUTS</span></span>

### <span data-ttu-id="00389-147">System.String</span><span class="sxs-lookup"><span data-stu-id="00389-147">System.String</span></span>

### <span data-ttu-id="00389-148">System.Security.Cryptography.X509Certificates.X509Certificate2Collection</span><span class="sxs-lookup"><span data-stu-id="00389-148">System.Security.Cryptography.X509Certificates.X509Certificate2Collection</span></span>

### <span data-ttu-id="00389-149">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="00389-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="00389-150">輸出</span><span class="sxs-lookup"><span data-stu-id="00389-150">OUTPUTS</span></span>

### <span data-ttu-id="00389-151">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="00389-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="00389-152">筆記</span><span class="sxs-lookup"><span data-stu-id="00389-152">NOTES</span></span>

## <span data-ttu-id="00389-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="00389-153">RELATED LINKS</span></span>

[<span data-ttu-id="00389-154">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="00389-154">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="00389-155">在 Key Vault 中建立及合併CSR</span><span class="sxs-lookup"><span data-stu-id="00389-155">Creating and merging CSR in Key Vault</span></span>](https://docs.microsoft.com/azure/key-vault/certificates/create-certificate-signing-request)