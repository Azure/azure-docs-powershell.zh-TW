---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
ms.openlocfilehash: ccd2762449e24f881a3308c0d11476a1e4626fed
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402400"
---
# <span data-ttu-id="6bcbd-101">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="6bcbd-101">Get-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="6bcbd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6bcbd-102">SYNOPSIS</span></span>
<span data-ttu-id="6bcbd-103">從金鑰庫獲得憑證。</span><span class="sxs-lookup"><span data-stu-id="6bcbd-103">Gets a certificate from a key vault.</span></span>

## <span data-ttu-id="6bcbd-104">語法</span><span class="sxs-lookup"><span data-stu-id="6bcbd-104">SYNTAX</span></span>

### <span data-ttu-id="6bcbd-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="6bcbd-105">ByName (Default)</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6bcbd-106">ByCertificateNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="6bcbd-106">ByCertificateNameAndVersion</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6bcbd-107">ByCertificateAllVersions</span><span class="sxs-lookup"><span data-stu-id="6bcbd-107">ByCertificateAllVersions</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6bcbd-108">ByNameInputObject</span><span class="sxs-lookup"><span data-stu-id="6bcbd-108">ByNameInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6bcbd-109">ByCertificateNameAndVersionInputObject</span><span class="sxs-lookup"><span data-stu-id="6bcbd-109">ByCertificateNameAndVersionInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6bcbd-110">ByCertificateAllVersionsInputObject</span><span class="sxs-lookup"><span data-stu-id="6bcbd-110">ByCertificateAllVersionsInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6bcbd-111">ByNameResourceId</span><span class="sxs-lookup"><span data-stu-id="6bcbd-111">ByNameResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6bcbd-112">ByCertificateNameAndVersionResourceId</span><span class="sxs-lookup"><span data-stu-id="6bcbd-112">ByCertificateNameAndVersionResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6bcbd-113">ByCertificateAllVersionsResourceId</span><span class="sxs-lookup"><span data-stu-id="6bcbd-113">ByCertificateAllVersionsResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6bcbd-114">描述</span><span class="sxs-lookup"><span data-stu-id="6bcbd-114">DESCRIPTION</span></span>
<span data-ttu-id="6bcbd-115">**Get-AzKeyVaultCertificate** Cmdlet 會從 Azure 金鑰庫的金鑰庫取得指定的憑證或憑證版本。</span><span class="sxs-lookup"><span data-stu-id="6bcbd-115">The **Get-AzKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="6bcbd-116">例子</span><span class="sxs-lookup"><span data-stu-id="6bcbd-116">EXAMPLES</span></span>

### <span data-ttu-id="6bcbd-117">範例 1：取得憑證</span><span class="sxs-lookup"><span data-stu-id="6bcbd-117">Example 1: Get a certificate</span></span>
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

Thumbprint  : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:21:45 PM
Updated     : 2/8/2016 11:21:45 PM
```

<span data-ttu-id="6bcbd-118">此命令會從名為 ContosoKV01 的金鑰庫獲得名為 TestCert01 的憑證。</span><span class="sxs-lookup"><span data-stu-id="6bcbd-118">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="6bcbd-119">範例 2：取得此金鑰庫的所有憑證已被刪除，但並未清除。</span><span class="sxs-lookup"><span data-stu-id="6bcbd-119">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="6bcbd-120">此命令會獲得先前在名稱為 Contoso 的金鑰庫中刪除但並未清除的所有憑證。</span><span class="sxs-lookup"><span data-stu-id="6bcbd-120">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="6bcbd-121">範例 3：針對此金鑰庫，獲得已被刪除但並未清除的憑證 MyCert。</span><span class="sxs-lookup"><span data-stu-id="6bcbd-121">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="6bcbd-122">此命令會獲得名稱為 "MyCert" 的憑證，該憑證先前已在名為 Contoso 的金鑰庫中刪除，但並未清除。</span><span class="sxs-lookup"><span data-stu-id="6bcbd-122">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="6bcbd-123">此命令會返回中繼資料，例如刪除日期，以及此已刪除憑證的排程清除日期。</span><span class="sxs-lookup"><span data-stu-id="6bcbd-123">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

### <span data-ttu-id="6bcbd-124">範例 4：使用篩選列出憑證</span><span class="sxs-lookup"><span data-stu-id="6bcbd-124">Example 4: List certificates using filtering</span></span>
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

## <span data-ttu-id="6bcbd-125">參數</span><span class="sxs-lookup"><span data-stu-id="6bcbd-125">PARAMETERS</span></span>

### <span data-ttu-id="6bcbd-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bcbd-126">-DefaultProfile</span></span>
<span data-ttu-id="6bcbd-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="6bcbd-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6bcbd-128">-IncludePending</span><span class="sxs-lookup"><span data-stu-id="6bcbd-128">-IncludePending</span></span>
<span data-ttu-id="6bcbd-129">指定是否要在輸出中納入擱置中的憑證</span><span class="sxs-lookup"><span data-stu-id="6bcbd-129">Specifies whether to include pending certificates in the output</span></span>

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

### <span data-ttu-id="6bcbd-130">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="6bcbd-130">-IncludeVersions</span></span>
<span data-ttu-id="6bcbd-131">表示此作業會獲得憑證的所有版本。</span><span class="sxs-lookup"><span data-stu-id="6bcbd-131">Indicates that this operation gets all versions of the certificate.</span></span>

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

### <span data-ttu-id="6bcbd-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6bcbd-132">-InputObject</span></span>
<span data-ttu-id="6bcbd-133">KeyVault 物件。</span><span class="sxs-lookup"><span data-stu-id="6bcbd-133">KeyVault object.</span></span>

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

### <span data-ttu-id="6bcbd-134">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="6bcbd-134">-InRemovedState</span></span>
<span data-ttu-id="6bcbd-135">指定是否要在輸出中納入先前刪除的憑證</span><span class="sxs-lookup"><span data-stu-id="6bcbd-135">Specifies whether to include previously deleted certificates in the output</span></span>

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

### <span data-ttu-id="6bcbd-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="6bcbd-136">-Name</span></span>
<span data-ttu-id="6bcbd-137">指定要取得之憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="6bcbd-137">Specifies the name of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByNameInputObject, ByNameResourceId
Aliases: CertificateName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateAllVersions, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject, ByCertificateNameAndVersionResourceId, ByCertificateAllVersionsResourceId
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="6bcbd-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6bcbd-138">-ResourceId</span></span>
<span data-ttu-id="6bcbd-139">KeyVault 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="6bcbd-139">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="6bcbd-140">-VaultName</span><span class="sxs-lookup"><span data-stu-id="6bcbd-140">-VaultName</span></span>
<span data-ttu-id="6bcbd-141">指定金鑰庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="6bcbd-141">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="6bcbd-142">-版本</span><span class="sxs-lookup"><span data-stu-id="6bcbd-142">-Version</span></span>
<span data-ttu-id="6bcbd-143">指定憑證的版本。</span><span class="sxs-lookup"><span data-stu-id="6bcbd-143">Specifies the version of a certificate.</span></span>

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

### <span data-ttu-id="6bcbd-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bcbd-144">CommonParameters</span></span>
<span data-ttu-id="6bcbd-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6bcbd-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bcbd-146">詳細資訊[請參閱about_CommonParameters。](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6bcbd-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bcbd-147">輸入</span><span class="sxs-lookup"><span data-stu-id="6bcbd-147">INPUTS</span></span>

### <span data-ttu-id="6bcbd-148">Microsoft.Azure.Commands.KeyVault.models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="6bcbd-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="6bcbd-149">System.String</span><span class="sxs-lookup"><span data-stu-id="6bcbd-149">System.String</span></span>

## <span data-ttu-id="6bcbd-150">輸出</span><span class="sxs-lookup"><span data-stu-id="6bcbd-150">OUTPUTS</span></span>

### <span data-ttu-id="6bcbd-151">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="6bcbd-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

### <span data-ttu-id="6bcbd-152">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="6bcbd-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

### <span data-ttu-id="6bcbd-153">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="6bcbd-153">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span></span>

### <span data-ttu-id="6bcbd-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="6bcbd-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="6bcbd-155">筆記</span><span class="sxs-lookup"><span data-stu-id="6bcbd-155">NOTES</span></span>

## <span data-ttu-id="6bcbd-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="6bcbd-156">RELATED LINKS</span></span>

[<span data-ttu-id="6bcbd-157">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="6bcbd-157">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="6bcbd-158">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="6bcbd-158">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="6bcbd-159">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="6bcbd-159">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

