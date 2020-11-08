---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
ms.openlocfilehash: f41e15a01a667576ee8f045d94bcb6b6dfee1e7b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969669"
---
# <span data-ttu-id="0728a-101">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="0728a-101">Get-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="0728a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0728a-102">SYNOPSIS</span></span>
<span data-ttu-id="0728a-103">從金鑰保存庫取得憑證。</span><span class="sxs-lookup"><span data-stu-id="0728a-103">Gets a certificate from a key vault.</span></span>

## <span data-ttu-id="0728a-104">句法</span><span class="sxs-lookup"><span data-stu-id="0728a-104">SYNTAX</span></span>

### <span data-ttu-id="0728a-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="0728a-105">ByName (Default)</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0728a-106">ByCertificateNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="0728a-106">ByCertificateNameAndVersion</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0728a-107">ByCertificateAllVersions</span><span class="sxs-lookup"><span data-stu-id="0728a-107">ByCertificateAllVersions</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0728a-108">ByNameInputObject</span><span class="sxs-lookup"><span data-stu-id="0728a-108">ByNameInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0728a-109">ByCertificateNameAndVersionInputObject</span><span class="sxs-lookup"><span data-stu-id="0728a-109">ByCertificateNameAndVersionInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0728a-110">ByCertificateAllVersionsInputObject</span><span class="sxs-lookup"><span data-stu-id="0728a-110">ByCertificateAllVersionsInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0728a-111">ByNameResourceId</span><span class="sxs-lookup"><span data-stu-id="0728a-111">ByNameResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0728a-112">ByCertificateNameAndVersionResourceId</span><span class="sxs-lookup"><span data-stu-id="0728a-112">ByCertificateNameAndVersionResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0728a-113">ByCertificateAllVersionsResourceId</span><span class="sxs-lookup"><span data-stu-id="0728a-113">ByCertificateAllVersionsResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0728a-114">說明</span><span class="sxs-lookup"><span data-stu-id="0728a-114">DESCRIPTION</span></span>
<span data-ttu-id="0728a-115">**AzKeyVaultCertificate** Cmdlet 會從 Azure 金鑰保存庫中的金鑰保存庫取得指定的憑證或憑證版本。</span><span class="sxs-lookup"><span data-stu-id="0728a-115">The **Get-AzKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="0728a-116">示例</span><span class="sxs-lookup"><span data-stu-id="0728a-116">EXAMPLES</span></span>

### <span data-ttu-id="0728a-117">範例1：取得憑證</span><span class="sxs-lookup"><span data-stu-id="0728a-117">Example 1: Get a certificate</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
Name        : testCert01
Certificate : [Subject] 
                CN=contoso.com

              [Issuer] 
                CN=contoso.com

              [Serial Number] 
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

              [Not Before] 
                2/8/2016 3:11:45 PM

              [Not After] 
                8/8/2016 4:21:45 PM

              [Thumbprint] 
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId       : https://contoso.vault.azure.net:443/keys/TestCert01/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
SecretId    : https://contoso.vault.azure.net:443/secrets/TestCert01/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Thumbprint  : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:21:45 PM
Updated     : 2/8/2016 11:21:45 PM
```

### <span data-ttu-id="0728a-118">範例2：取得 cert 並將它另存為 pfx</span><span class="sxs-lookup"><span data-stu-id="0728a-118">Example 2: Get cert and save it as pfx</span></span>
<span data-ttu-id="0728a-119">這個命令會從名為 ContosoKV01 的主要電子倉庫中取得名為 TestCert01 的憑證。</span><span class="sxs-lookup"><span data-stu-id="0728a-119">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span> <span data-ttu-id="0728a-120">若要將憑證下載為 pfx 檔案，請執行下列命令。</span><span class="sxs-lookup"><span data-stu-id="0728a-120">To download the certificate as pfx file, run following command.</span></span> <span data-ttu-id="0728a-121">這些命令會存取 SecretId，然後將內容儲存為 pfx 檔案。</span><span class="sxs-lookup"><span data-stu-id="0728a-121">These commands access SecretId and then save the content as a pfx file.</span></span>

```powershell
$cert = Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
$secret = Get-AzKeyVaultSecret -VaultName $vaultName -Name $cert.Name

$secretByte = [Convert]::FromBase64String($secret.SecretValueText)
$x509Cert = new-object System.Security.Cryptography.X509Certificates.X509Certificate2
$x509Cert.Import($secretByte, "", "Exportable,PersistKeySet")
$type = [System.Security.Cryptography.X509Certificates.X509ContentType]::Pfx
$pfxFileByte = $x509Cert.Export($type, $password)

# Write to a file
[System.IO.File]::WriteAllBytes("KeyVault.pfx", $pfxFileByte)
```

### <span data-ttu-id="0728a-122">範例3：取得已刪除但未針對此金鑰保存庫清除的所有憑證。</span><span class="sxs-lookup"><span data-stu-id="0728a-122">Example 3: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificate -VaultName 'contoso' -InRemovedState

DeletedDate        : 5/24/2018 6:08:32 PM
Enabled            : True
Expires            : 11/24/2018 6:08:13 PM
NotBefore          : 5/24/2018 5:58:13 PM
Created            : 5/24/2018 6:08:13 PM
Updated            : 5/24/2018 6:08:13 PM
Tags               :
VaultName          : contoso
Name               : test1
Version            :
Id                 : https://contoso.vault.azure.net:443/certificates/test1

ScheduledPurgeDate : 8/22/2018 6:10:47 PM
DeletedDate        : 5/24/2018 6:10:47 PM
Enabled            : True
Expires            : 11/24/2018 6:09:44 PM
NotBefore          : 5/24/2018 5:59:44 PM
Created            : 5/24/2018 6:09:44 PM
Updated            : 5/24/2018 6:09:44 PM
Tags               :
VaultName          : contoso
Name               : test2
Version            :
Id                 : https://contoso.vault.azure.net:443/certificates/test2
```

<span data-ttu-id="0728a-123">這個命令會在名為 Contoso 的金鑰保存庫中，取得先前已刪除但尚未清除的所有憑證。</span><span class="sxs-lookup"><span data-stu-id="0728a-123">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="0728a-124">範例4：取得已刪除但未針對此金鑰保存庫清除的憑證 MyCert。</span><span class="sxs-lookup"><span data-stu-id="0728a-124">Example 4: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificate -VaultName 'contoso' -Name 'test1' -InRemovedState

Certificate        : [Subject]
                       CN=contoso.com

                     [Issuer]
                       CN=contoso.com

                     [Serial Number]
                       XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                     [Not Before]
                       5/24/2018 10:58:13 AM

                     [Not After]
                       11/24/2018 10:08:13 AM

                     [Thumbprint]
                       XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId              : https://contoso.vault.azure.net:443/keys/test1/7fe415d5518240c1a6fce89986b8d334
SecretId           : https://contoso.vault.azure.net:443/secrets/test1/7fe415d5518240c1a6fce89986b8d334
Thumbprint         : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel      : Recoverable+Purgeable
ScheduledPurgeDate : 8/22/2018 6:08:32 PM
DeletedDate        : 5/24/2018 6:08:32 PM
Enabled            : True
Expires            : 11/24/2018 6:08:13 PM
NotBefore          : 5/24/2018 5:58:13 PM
Created            : 5/24/2018 6:08:13 PM
Updated            : 5/24/2018 6:08:13 PM
Tags               :
VaultName          : contoso
Name               : test1
Version            : 7fe415d5518240c1a6fce89986b8d334
Id                 : https://contoso.vault.azure.net:443/certificates/test1/7fe415d5518240c1a6fce89986b8d334
```

<span data-ttu-id="0728a-125">這個命令會在名為 Contoso 的金鑰保存庫中，取得名為「MyCert」的憑證，但尚未清除。</span><span class="sxs-lookup"><span data-stu-id="0728a-125">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="0728a-126">這個命令會傳回中繼資料，例如刪除日期，以及此刪除的憑證的排程清除日期。</span><span class="sxs-lookup"><span data-stu-id="0728a-126">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

### <span data-ttu-id="0728a-127">範例5：使用篩選列出憑證</span><span class="sxs-lookup"><span data-stu-id="0728a-127">Example 5: List certificates using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "test*"

Enabled   : True
Expires   : 8/5/2019 2:39:25 AM
NotBefore : 2/5/2019 2:29:25 AM
Created   : 2/5/2019 2:39:25 AM
Updated   : 2/5/2019 2:39:25 AM
Tags      :
VaultName : ContosoKV01
Name      : test1
Version   :
Id        : https://ContosoKV01.vault.azure.net:443/certificates/test1

Enabled   : True
Expires   : 8/5/2019 2:39:25 AM
NotBefore : 2/5/2019 2:29:25 AM
Created   : 2/5/2019 2:39:25 AM
Updated   : 2/5/2019 2:39:25 AM
Tags      :
VaultName : ContosoKV01
Name      : test2
Version   :
Id        : https://ContosoKV01.vault.azure.net:443/certificates/test2

This command gets all certificates starting with "test" from the key vault named ContosoKV01.
```

## <span data-ttu-id="0728a-128">參數</span><span class="sxs-lookup"><span data-stu-id="0728a-128">PARAMETERS</span></span>

### <span data-ttu-id="0728a-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0728a-129">-DefaultProfile</span></span>
<span data-ttu-id="0728a-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="0728a-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0728a-131">-IncludePending</span><span class="sxs-lookup"><span data-stu-id="0728a-131">-IncludePending</span></span>
<span data-ttu-id="0728a-132">指定是否要在輸出中包含擱置中的憑證</span><span class="sxs-lookup"><span data-stu-id="0728a-132">Specifies whether to include pending certificates in the output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByName, ByNameInputObject, ByNameResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0728a-133">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="0728a-133">-IncludeVersions</span></span>
<span data-ttu-id="0728a-134">表示此操作會取得所有版本的憑證。</span><span class="sxs-lookup"><span data-stu-id="0728a-134">Indicates that this operation gets all versions of the certificate.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByCertificateAllVersions, ByCertificateAllVersionsInputObject, ByCertificateAllVersionsResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0728a-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0728a-135">-InputObject</span></span>
<span data-ttu-id="0728a-136">KeyVault 物件。</span><span class="sxs-lookup"><span data-stu-id="0728a-136">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByNameInputObject, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0728a-137">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="0728a-137">-InRemovedState</span></span>
<span data-ttu-id="0728a-138">指定是否要在輸出中包含先前刪除的憑證</span><span class="sxs-lookup"><span data-stu-id="0728a-138">Specifies whether to include previously deleted certificates in the output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByName, ByNameInputObject, ByNameResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0728a-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="0728a-139">-Name</span></span>
<span data-ttu-id="0728a-140">指定要取得的憑證名稱。</span><span class="sxs-lookup"><span data-stu-id="0728a-140">Specifies the name of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByNameInputObject, ByNameResourceId
Aliases: CertificateName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateAllVersions, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject, ByCertificateNameAndVersionResourceId, ByCertificateAllVersionsResourceId
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0728a-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0728a-141">-ResourceId</span></span>
<span data-ttu-id="0728a-142">KeyVault 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0728a-142">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameResourceId, ByCertificateNameAndVersionResourceId, ByCertificateAllVersionsResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0728a-143">-VaultName</span><span class="sxs-lookup"><span data-stu-id="0728a-143">-VaultName</span></span>
<span data-ttu-id="0728a-144">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="0728a-144">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByCertificateNameAndVersion, ByCertificateAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0728a-145">-版本</span><span class="sxs-lookup"><span data-stu-id="0728a-145">-Version</span></span>
<span data-ttu-id="0728a-146">指定憑證版本。</span><span class="sxs-lookup"><span data-stu-id="0728a-146">Specifies the version of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateNameAndVersionInputObject, ByCertificateNameAndVersionResourceId
Aliases: CertificateVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0728a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0728a-147">CommonParameters</span></span>
<span data-ttu-id="0728a-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0728a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0728a-149">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0728a-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0728a-150">輸入</span><span class="sxs-lookup"><span data-stu-id="0728a-150">INPUTS</span></span>

### <span data-ttu-id="0728a-151">PSKeyVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="0728a-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="0728a-152">System.object</span><span class="sxs-lookup"><span data-stu-id="0728a-152">System.String</span></span>

## <span data-ttu-id="0728a-153">輸出</span><span class="sxs-lookup"><span data-stu-id="0728a-153">OUTPUTS</span></span>

### <span data-ttu-id="0728a-154">PSKeyVaultCertificateIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="0728a-154">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

### <span data-ttu-id="0728a-155">PSKeyVaultCertificate 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="0728a-155">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

### <span data-ttu-id="0728a-156">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="0728a-156">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span></span>

### <span data-ttu-id="0728a-157">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="0728a-157">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="0728a-158">筆記</span><span class="sxs-lookup"><span data-stu-id="0728a-158">NOTES</span></span>

## <span data-ttu-id="0728a-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="0728a-159">RELATED LINKS</span></span>

[<span data-ttu-id="0728a-160">附加 AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="0728a-160">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="0728a-161">匯入-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="0728a-161">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="0728a-162">移除-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="0728a-162">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="0728a-163">復原-AzKeyVaultSecretCertificate</span><span class="sxs-lookup"><span data-stu-id="0728a-163">Undo-AzKeyVaultSecretCertificate</span></span>](./Undo-AzKeyVaultSecretCertificate.md)
