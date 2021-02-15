---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
ms.openlocfilehash: babd3d8a42ddbd740c8189a41de76c78170ecae5
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398813"
---
# <span data-ttu-id="f7d70-101">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="f7d70-101">Get-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="f7d70-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f7d70-102">SYNOPSIS</span></span>
<span data-ttu-id="f7d70-103">從金鑰庫獲得憑證。</span><span class="sxs-lookup"><span data-stu-id="f7d70-103">Gets a certificate from a key vault.</span></span>

## <span data-ttu-id="f7d70-104">語法</span><span class="sxs-lookup"><span data-stu-id="f7d70-104">SYNTAX</span></span>

### <span data-ttu-id="f7d70-105">ByVaultName (預設) </span><span class="sxs-lookup"><span data-stu-id="f7d70-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f7d70-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="f7d70-106">ByCertificateName</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7d70-107">ByCertificateVersions</span><span class="sxs-lookup"><span data-stu-id="f7d70-107">ByCertificateVersions</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7d70-108">ByDeletedCertificates</span><span class="sxs-lookup"><span data-stu-id="f7d70-108">ByDeletedCertificates</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7d70-109">描述</span><span class="sxs-lookup"><span data-stu-id="f7d70-109">DESCRIPTION</span></span>
<span data-ttu-id="f7d70-110">**Get-AzKeyVaultCertificate** Cmdlet 會從 Azure 金鑰庫的金鑰庫取得指定的憑證或憑證版本。</span><span class="sxs-lookup"><span data-stu-id="f7d70-110">The **Get-AzKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="f7d70-111">例子</span><span class="sxs-lookup"><span data-stu-id="f7d70-111">EXAMPLES</span></span>

### <span data-ttu-id="f7d70-112">範例 1：取得憑證</span><span class="sxs-lookup"><span data-stu-id="f7d70-112">Example 1: Get a certificate</span></span>
```
PS C:\>Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
Name        : testCert01
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
Created     : 2/8/2016 11:21:45 PM
Updated     : 2/8/2016 11:21:45 PM
```

<span data-ttu-id="f7d70-113">此命令會從名為 ContosoKV01 的金鑰庫獲得名為 TestCert01 的憑證。</span><span class="sxs-lookup"><span data-stu-id="f7d70-113">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="f7d70-114">範例 2：取得此金鑰庫的所有憑證已被刪除，但並未清除。</span><span class="sxs-lookup"><span data-stu-id="f7d70-114">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultCertificate -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="f7d70-115">此命令會獲得先前在名稱為 Contoso 的金鑰庫中刪除但並未清除的所有憑證。</span><span class="sxs-lookup"><span data-stu-id="f7d70-115">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="f7d70-116">範例 3：針對此金鑰庫，獲得已被刪除但並未清除的憑證 MyCert。</span><span class="sxs-lookup"><span data-stu-id="f7d70-116">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="f7d70-117">此命令會獲得名稱為 "MyCert" 的憑證，該憑證先前已在名為 Contoso 的金鑰庫中刪除，但並未清除。</span><span class="sxs-lookup"><span data-stu-id="f7d70-117">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="f7d70-118">此命令會返回中繼資料，例如刪除日期，以及此已刪除憑證的排程清除日期。</span><span class="sxs-lookup"><span data-stu-id="f7d70-118">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

## <span data-ttu-id="f7d70-119">參數</span><span class="sxs-lookup"><span data-stu-id="f7d70-119">PARAMETERS</span></span>

### <span data-ttu-id="f7d70-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7d70-120">-DefaultProfile</span></span>
<span data-ttu-id="f7d70-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="f7d70-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7d70-122">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="f7d70-122">-IncludeVersions</span></span>
<span data-ttu-id="f7d70-123">表示此作業會獲得憑證的所有版本。</span><span class="sxs-lookup"><span data-stu-id="f7d70-123">Indicates that this operation gets all versions of the certificate.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByCertificateVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7d70-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="f7d70-124">-InRemovedState</span></span>
<span data-ttu-id="f7d70-125">指定是否要在輸出中納入先前刪除的憑證</span><span class="sxs-lookup"><span data-stu-id="f7d70-125">Specifies whether to include previously deleted certificates in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedCertificates
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7d70-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="f7d70-126">-Name</span></span>
<span data-ttu-id="f7d70-127">指定要取得之憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="f7d70-127">Specifies the name of the certificate to get.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateName, ByCertificateVersions
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedCertificates
Aliases: CertificateName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7d70-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f7d70-128">-VaultName</span></span>
<span data-ttu-id="f7d70-129">指定金鑰庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="f7d70-129">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="f7d70-130">-版本</span><span class="sxs-lookup"><span data-stu-id="f7d70-130">-Version</span></span>
<span data-ttu-id="f7d70-131">指定憑證的版本。</span><span class="sxs-lookup"><span data-stu-id="f7d70-131">Specifies the version of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateName
Aliases: CertificateVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7d70-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7d70-132">CommonParameters</span></span>
<span data-ttu-id="f7d70-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f7d70-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7d70-134">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f7d70-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7d70-135">輸入</span><span class="sxs-lookup"><span data-stu-id="f7d70-135">INPUTS</span></span>

### <span data-ttu-id="f7d70-136">沒有</span><span class="sxs-lookup"><span data-stu-id="f7d70-136">None</span></span>
<span data-ttu-id="f7d70-137">此 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="f7d70-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f7d70-138">輸出</span><span class="sxs-lookup"><span data-stu-id="f7d70-138">OUTPUTS</span></span>

### <span data-ttu-id="f7d70-139">System.Collections.generic.List'1[Microsoft.Azure.Commands.KeyVault.models.CertificateIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="f7d70-139">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.CertificateIdentityItem]</span></span>

### <span data-ttu-id="f7d70-140">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="f7d70-140">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span></span>

## <span data-ttu-id="f7d70-141">筆記</span><span class="sxs-lookup"><span data-stu-id="f7d70-141">NOTES</span></span>

## <span data-ttu-id="f7d70-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="f7d70-142">RELATED LINKS</span></span>

[<span data-ttu-id="f7d70-143">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="f7d70-143">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="f7d70-144">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="f7d70-144">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="f7d70-145">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="f7d70-145">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

