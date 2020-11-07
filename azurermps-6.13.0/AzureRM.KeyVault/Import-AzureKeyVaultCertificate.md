---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: D4188DC6-A8AB-4B45-9781-94B74C338C63
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/import-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Import-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Import-AzureKeyVaultCertificate.md
ms.openlocfilehash: 5cc7846ae1d5eba5764c524e4edfb470a7cd562b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625288"
---
# <span data-ttu-id="0409b-101">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="0409b-101">Import-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="0409b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0409b-102">SYNOPSIS</span></span>
<span data-ttu-id="0409b-103">將憑證匯入到金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="0409b-103">Imports a certificate to a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0409b-104">句法</span><span class="sxs-lookup"><span data-stu-id="0409b-104">SYNTAX</span></span>

### <span data-ttu-id="0409b-105">ImportCertificateFromFile (預設) </span><span class="sxs-lookup"><span data-stu-id="0409b-105">ImportCertificateFromFile (Default)</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0409b-106">ImportWithPrivateKeyFromString</span><span class="sxs-lookup"><span data-stu-id="0409b-106">ImportWithPrivateKeyFromString</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -CertificateString <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0409b-107">ImportWithPrivateKeyFromCollection</span><span class="sxs-lookup"><span data-stu-id="0409b-107">ImportWithPrivateKeyFromCollection</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [-CertificateCollection] <X509Certificate2Collection> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0409b-108">說明</span><span class="sxs-lookup"><span data-stu-id="0409b-108">DESCRIPTION</span></span>
<span data-ttu-id="0409b-109">匯 **入-AzureKeyVaultCertificate** Cmdlet 會將證書匯入到金鑰保存庫中。</span><span class="sxs-lookup"><span data-stu-id="0409b-109">The **Import-AzureKeyVaultCertificate** cmdlet imports a certificate into a key vault.</span></span>
<span data-ttu-id="0409b-110">您可以使用下列其中一種方法，建立要匯入的憑證：</span><span class="sxs-lookup"><span data-stu-id="0409b-110">You can create the certificate to import by using one of the following methods:</span></span>
- <span data-ttu-id="0409b-111">使用 New-AzureKeyVaultCertificateSigningRequest Cmdlet 來建立證書簽署要求，並將它提交給憑證授權單位。</span><span class="sxs-lookup"><span data-stu-id="0409b-111">Use the New-AzureKeyVaultCertificateSigningRequest cmdlet to create a certificate signing request and submit it to a certificate authority.</span></span>
- <span data-ttu-id="0409b-112">使用現有的憑證套件檔案，例如 .pfx 或 p12 檔案，其中包含憑證和私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="0409b-112">Use an existing certificate package file, such as a .pfx or .p12 file, which contains both the certificate and private key.</span></span>

## <span data-ttu-id="0409b-113">示例</span><span class="sxs-lookup"><span data-stu-id="0409b-113">EXAMPLES</span></span>

### <span data-ttu-id="0409b-114">範例1：匯入主要電子倉庫憑證</span><span class="sxs-lookup"><span data-stu-id="0409b-114">Example 1: Import a key vault certificate</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS C:\> Import-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "ImportCert01" -FilePath "C:\Users\contosoUser\Desktop\import.pfx" -Password $Password

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

<span data-ttu-id="0409b-115">第一個命令使用 ConvertTo-SecureString Cmdlet 來建立安全密碼，然後將它儲存在 $Password 變數中。</span><span class="sxs-lookup"><span data-stu-id="0409b-115">The first command uses the ConvertTo-SecureString cmdlet to create a secure password, and then stores it in the $Password variable.</span></span>
<span data-ttu-id="0409b-116">第二個命令會將名為 ImportCert01 的憑證匯入到 CosotosoKV01 金鑰保存庫中。</span><span class="sxs-lookup"><span data-stu-id="0409b-116">The second command imports the certificate named ImportCert01 into the CosotosoKV01 key vault.</span></span>

## <span data-ttu-id="0409b-117">參數</span><span class="sxs-lookup"><span data-stu-id="0409b-117">PARAMETERS</span></span>

### <span data-ttu-id="0409b-118">-CertificateCollection</span><span class="sxs-lookup"><span data-stu-id="0409b-118">-CertificateCollection</span></span>
<span data-ttu-id="0409b-119">指定要新增到主要電子倉庫的憑證集合。</span><span class="sxs-lookup"><span data-stu-id="0409b-119">Specifies the certificate collection to add to a key vault.</span></span>

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

### <span data-ttu-id="0409b-120">-CertificateString</span><span class="sxs-lookup"><span data-stu-id="0409b-120">-CertificateString</span></span>
<span data-ttu-id="0409b-121">指定憑證字串。</span><span class="sxs-lookup"><span data-stu-id="0409b-121">Specifies a certificate string.</span></span>

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

### <span data-ttu-id="0409b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0409b-122">-DefaultProfile</span></span>
<span data-ttu-id="0409b-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="0409b-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0409b-124">-FilePath</span><span class="sxs-lookup"><span data-stu-id="0409b-124">-FilePath</span></span>
<span data-ttu-id="0409b-125">指定此 Cmdlet 所匯入的憑證檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="0409b-125">Specifies the path of the certificate file that this cmdlet imports.</span></span>

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

### <span data-ttu-id="0409b-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="0409b-126">-Name</span></span>
<span data-ttu-id="0409b-127">指定憑證名稱。</span><span class="sxs-lookup"><span data-stu-id="0409b-127">Specifies the certificate name.</span></span> <span data-ttu-id="0409b-128">這個 Cmdlet 會從主要的保存庫名稱、目前所選的環境及憑證名稱，構造憑證的完整功能變數名稱 (FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="0409b-128">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate from key vault name, currently selected environment, and certificate name.</span></span>

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

### <span data-ttu-id="0409b-129">-Password</span><span class="sxs-lookup"><span data-stu-id="0409b-129">-Password</span></span>
<span data-ttu-id="0409b-130">指定憑證檔的密碼。</span><span class="sxs-lookup"><span data-stu-id="0409b-130">Specifies the password for a certificate file.</span></span>

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

### <span data-ttu-id="0409b-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="0409b-131">-Tag</span></span>
<span data-ttu-id="0409b-132">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="0409b-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0409b-133">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="0409b-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0409b-134">-VaultName</span><span class="sxs-lookup"><span data-stu-id="0409b-134">-VaultName</span></span>
<span data-ttu-id="0409b-135">指定此 Cmdlet 要匯入憑證的主要保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="0409b-135">Specifies the key vault name into which this cmdlet imports certificates.</span></span>
<span data-ttu-id="0409b-136">這個 Cmdlet 會根據名稱和目前所選的環境，來構造金鑰 vault (FQDN) 的完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="0409b-136">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="0409b-137">-確認</span><span class="sxs-lookup"><span data-stu-id="0409b-137">-Confirm</span></span>
<span data-ttu-id="0409b-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0409b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0409b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0409b-139">-WhatIf</span></span>
<span data-ttu-id="0409b-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0409b-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0409b-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0409b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0409b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0409b-142">CommonParameters</span></span>
<span data-ttu-id="0409b-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0409b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0409b-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0409b-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0409b-145">輸入</span><span class="sxs-lookup"><span data-stu-id="0409b-145">INPUTS</span></span>

### <span data-ttu-id="0409b-146">System.object</span><span class="sxs-lookup"><span data-stu-id="0409b-146">System.String</span></span>

### <span data-ttu-id="0409b-147">X509Certificates. 密碼。 X509Certificate2Collection</span><span class="sxs-lookup"><span data-stu-id="0409b-147">System.Security.Cryptography.X509Certificates.X509Certificate2Collection</span></span>
<span data-ttu-id="0409b-148">參數： CertificateCollection (ByValue) </span><span class="sxs-lookup"><span data-stu-id="0409b-148">Parameters: CertificateCollection (ByValue)</span></span>

### <span data-ttu-id="0409b-149">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0409b-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0409b-150">輸出</span><span class="sxs-lookup"><span data-stu-id="0409b-150">OUTPUTS</span></span>

### <span data-ttu-id="0409b-151">PSKeyVaultCertificate 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="0409b-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="0409b-152">筆記</span><span class="sxs-lookup"><span data-stu-id="0409b-152">NOTES</span></span>

## <span data-ttu-id="0409b-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="0409b-153">RELATED LINKS</span></span>

[<span data-ttu-id="0409b-154">移除-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="0409b-154">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)
