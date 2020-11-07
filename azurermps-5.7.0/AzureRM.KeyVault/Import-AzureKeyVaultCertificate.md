---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: D4188DC6-A8AB-4B45-9781-94B74C338C63
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/import-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Import-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Import-AzureKeyVaultCertificate.md
ms.openlocfilehash: 37befa1434d18241b2f4721523de0ab48bebfd0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626444"
---
# <span data-ttu-id="2c3bb-101">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="2c3bb-101">Import-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="2c3bb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2c3bb-102">SYNOPSIS</span></span>
<span data-ttu-id="2c3bb-103">將憑證匯入到金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="2c3bb-103">Imports a certificate to a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c3bb-104">句法</span><span class="sxs-lookup"><span data-stu-id="2c3bb-104">SYNTAX</span></span>

### <span data-ttu-id="2c3bb-105">ImportCertificateFromFile (預設) </span><span class="sxs-lookup"><span data-stu-id="2c3bb-105">ImportCertificateFromFile (Default)</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2c3bb-106">ImportWithPrivateKeyFromString</span><span class="sxs-lookup"><span data-stu-id="2c3bb-106">ImportWithPrivateKeyFromString</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -CertificateString <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2c3bb-107">ImportWithPrivateKeyFromCollection</span><span class="sxs-lookup"><span data-stu-id="2c3bb-107">ImportWithPrivateKeyFromCollection</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [-CertificateCollection] <X509Certificate2Collection> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c3bb-108">說明</span><span class="sxs-lookup"><span data-stu-id="2c3bb-108">DESCRIPTION</span></span>
<span data-ttu-id="2c3bb-109">匯 **入-AzureKeyVaultCertificate** Cmdlet 會將證書匯入到金鑰保存庫中。</span><span class="sxs-lookup"><span data-stu-id="2c3bb-109">The **Import-AzureKeyVaultCertificate** cmdlet imports a certificate into a key vault.</span></span>

<span data-ttu-id="2c3bb-110">您可以使用下列其中一種方法，建立要匯入的憑證：</span><span class="sxs-lookup"><span data-stu-id="2c3bb-110">You can create the certificate to import by using one of the following methods:</span></span>

- <span data-ttu-id="2c3bb-111">使用 New-AzureKeyVaultCertificateSigningRequest Cmdlet 來建立證書簽署要求，並將它提交給憑證授權單位。</span><span class="sxs-lookup"><span data-stu-id="2c3bb-111">Use the New-AzureKeyVaultCertificateSigningRequest cmdlet to create a certificate signing request and submit it to a certificate authority.</span></span>
- <span data-ttu-id="2c3bb-112">使用現有的憑證套件檔案，例如 .pfx 或 p12 檔案，其中包含憑證和私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="2c3bb-112">Use an existing certificate package file, such as a .pfx or .p12 file, which contains both the certificate and private key.</span></span>

## <span data-ttu-id="2c3bb-113">示例</span><span class="sxs-lookup"><span data-stu-id="2c3bb-113">EXAMPLES</span></span>

### <span data-ttu-id="2c3bb-114">範例1：匯入主要電子倉庫憑證</span><span class="sxs-lookup"><span data-stu-id="2c3bb-114">Example 1: Import a key vault certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS C:\> Import-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "ImportCert01" -FilePath "C:\Users\contosoUser\Desktop\import.pfx" -Password $Password
Name        : importCert01
Certificate : [Subject]
                CN=contoso.com

              [Issuer]
                CN=contoso.com

              [Serial Number]
                05979C5A2F0741D5A3B6F97673E8A118

              [Not Before]
                2/8/2016 3:11:45 PM

              [Not After]
                8/8/2016 4:21:45 PM

              [Thumbprint]
                3E9B6848AD1834284157D68B060F748037F663C8

Thumbprint  : 3E9B6848AD1834284157D68B060F748037F663C8
Tags        :
Enabled     : True
Created     : 2/8/2016 11:50:43 PM
Updated     : 2/8/2016 11:50:43 PM
```

<span data-ttu-id="2c3bb-115">第一個命令使用 ConvertTo-SecureString Cmdlet 來建立安全密碼，然後將它儲存在 $Password 變數中。</span><span class="sxs-lookup"><span data-stu-id="2c3bb-115">The first command uses the ConvertTo-SecureString cmdlet to create a secure password, and then stores it in the $Password variable.</span></span>

<span data-ttu-id="2c3bb-116">第二個命令會將名為 ImportCert01 的憑證匯入到 CosotosoKV01 金鑰保存庫中。</span><span class="sxs-lookup"><span data-stu-id="2c3bb-116">The second command imports the certificate named ImportCert01 into the CosotosoKV01 key vault.</span></span>

## <span data-ttu-id="2c3bb-117">參數</span><span class="sxs-lookup"><span data-stu-id="2c3bb-117">PARAMETERS</span></span>

### <span data-ttu-id="2c3bb-118">-CertificateCollection</span><span class="sxs-lookup"><span data-stu-id="2c3bb-118">-CertificateCollection</span></span>
<span data-ttu-id="2c3bb-119">指定要新增到主要電子倉庫的憑證集合。</span><span class="sxs-lookup"><span data-stu-id="2c3bb-119">Specifies the certificate collection to add to a key vault.</span></span>

```yaml
Type: X509Certificate2Collection
Parameter Sets: ImportWithPrivateKeyFromCollection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c3bb-120">-CertificateString</span><span class="sxs-lookup"><span data-stu-id="2c3bb-120">-CertificateString</span></span>
<span data-ttu-id="2c3bb-121">指定憑證字串。</span><span class="sxs-lookup"><span data-stu-id="2c3bb-121">Specifies a certificate string.</span></span>

```yaml
Type: String
Parameter Sets: ImportWithPrivateKeyFromString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c3bb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c3bb-122">-DefaultProfile</span></span>
<span data-ttu-id="2c3bb-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2c3bb-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c3bb-124">-FilePath</span><span class="sxs-lookup"><span data-stu-id="2c3bb-124">-FilePath</span></span>
<span data-ttu-id="2c3bb-125">指定此 Cmdlet 所匯入的憑證檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="2c3bb-125">Specifies the path of the certificate file that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: ImportCertificateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c3bb-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="2c3bb-126">-Name</span></span>
<span data-ttu-id="2c3bb-127">指定憑證名稱。</span><span class="sxs-lookup"><span data-stu-id="2c3bb-127">Specifies the certificate name.</span></span> <span data-ttu-id="2c3bb-128">這個 Cmdlet 會從主要的保存庫名稱、目前所選的環境及憑證名稱，構造憑證的完整功能變數名稱 (FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="2c3bb-128">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate from key vault name, currently selected environment, and certificate name.</span></span>

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

### <span data-ttu-id="2c3bb-129">-Password</span><span class="sxs-lookup"><span data-stu-id="2c3bb-129">-Password</span></span>
<span data-ttu-id="2c3bb-130">指定憑證檔的密碼。</span><span class="sxs-lookup"><span data-stu-id="2c3bb-130">Specifies the password for a certificate file.</span></span>

```yaml
Type: SecureString
Parameter Sets: ImportCertificateFromFile, ImportWithPrivateKeyFromString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c3bb-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="2c3bb-131">-Tag</span></span>
<span data-ttu-id="2c3bb-132">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="2c3bb-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2c3bb-133">例如：</span><span class="sxs-lookup"><span data-stu-id="2c3bb-133">For example:</span></span>

<span data-ttu-id="2c3bb-134">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="2c3bb-134">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c3bb-135">-VaultName</span><span class="sxs-lookup"><span data-stu-id="2c3bb-135">-VaultName</span></span>
<span data-ttu-id="2c3bb-136">指定此 Cmdlet 要匯入憑證的主要保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="2c3bb-136">Specifies the key vault name into which this cmdlet imports certificates.</span></span>
<span data-ttu-id="2c3bb-137">這個 Cmdlet 會根據名稱和目前所選的環境，來構造金鑰 vault (FQDN) 的完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="2c3bb-137">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="2c3bb-138">-確認</span><span class="sxs-lookup"><span data-stu-id="2c3bb-138">-Confirm</span></span>
<span data-ttu-id="2c3bb-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2c3bb-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c3bb-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c3bb-140">-WhatIf</span></span>
<span data-ttu-id="2c3bb-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2c3bb-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c3bb-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2c3bb-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c3bb-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c3bb-143">CommonParameters</span></span>
<span data-ttu-id="2c3bb-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2c3bb-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c3bb-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2c3bb-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c3bb-146">輸入</span><span class="sxs-lookup"><span data-stu-id="2c3bb-146">INPUTS</span></span>

### <span data-ttu-id="2c3bb-147">所有</span><span class="sxs-lookup"><span data-stu-id="2c3bb-147">None</span></span>
<span data-ttu-id="2c3bb-148">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="2c3bb-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2c3bb-149">輸出</span><span class="sxs-lookup"><span data-stu-id="2c3bb-149">OUTPUTS</span></span>

### <span data-ttu-id="2c3bb-150">PSKeyVaultCertificate 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="2c3bb-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="2c3bb-151">筆記</span><span class="sxs-lookup"><span data-stu-id="2c3bb-151">NOTES</span></span>

## <span data-ttu-id="2c3bb-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="2c3bb-152">RELATED LINKS</span></span>

[<span data-ttu-id="2c3bb-153">移除-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="2c3bb-153">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)
