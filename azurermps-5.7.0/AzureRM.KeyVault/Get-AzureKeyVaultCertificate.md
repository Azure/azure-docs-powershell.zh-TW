---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificate.md
ms.openlocfilehash: 87b030229eb2a1f4bb91122aaec8a119134d27fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447789"
---
# <span data-ttu-id="02a17-101">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="02a17-101">Get-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="02a17-102">摘要</span><span class="sxs-lookup"><span data-stu-id="02a17-102">SYNOPSIS</span></span>
<span data-ttu-id="02a17-103">從金鑰保存庫取得憑證。</span><span class="sxs-lookup"><span data-stu-id="02a17-103">Gets a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02a17-104">句法</span><span class="sxs-lookup"><span data-stu-id="02a17-104">SYNTAX</span></span>

### <span data-ttu-id="02a17-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="02a17-105">ByName (Default)</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02a17-106">ByCertificateNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="02a17-106">ByCertificateNameAndVersion</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02a17-107">ByCertificateAllVersions</span><span class="sxs-lookup"><span data-stu-id="02a17-107">ByCertificateAllVersions</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02a17-108">ByNameInputObject</span><span class="sxs-lookup"><span data-stu-id="02a17-108">ByNameInputObject</span></span>
```
Get-AzureKeyVaultCertificate [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02a17-109">ByCertificateNameAndVersionInputObject</span><span class="sxs-lookup"><span data-stu-id="02a17-109">ByCertificateNameAndVersionInputObject</span></span>
```
Get-AzureKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02a17-110">ByCertificateAllVersionsInputObject</span><span class="sxs-lookup"><span data-stu-id="02a17-110">ByCertificateAllVersionsInputObject</span></span>
```
Get-AzureKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02a17-111">說明</span><span class="sxs-lookup"><span data-stu-id="02a17-111">DESCRIPTION</span></span>
<span data-ttu-id="02a17-112">**AzureKeyVaultCertificate** Cmdlet 會從 Azure 金鑰保存庫中的金鑰保存庫取得指定的憑證或憑證版本。</span><span class="sxs-lookup"><span data-stu-id="02a17-112">The **Get-AzureKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="02a17-113">示例</span><span class="sxs-lookup"><span data-stu-id="02a17-113">EXAMPLES</span></span>

### <span data-ttu-id="02a17-114">範例1：取得憑證</span><span class="sxs-lookup"><span data-stu-id="02a17-114">Example 1: Get a certificate</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
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

<span data-ttu-id="02a17-115">這個命令會從名為 ContosoKV01 的主要電子倉庫中取得名為 TestCert01 的憑證。</span><span class="sxs-lookup"><span data-stu-id="02a17-115">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="02a17-116">範例2：取得已刪除但未針對此金鑰保存庫清除的所有憑證。</span><span class="sxs-lookup"><span data-stu-id="02a17-116">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="02a17-117">這個命令會在名為 Contoso 的金鑰保存庫中，取得先前已刪除但尚未清除的所有憑證。</span><span class="sxs-lookup"><span data-stu-id="02a17-117">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="02a17-118">範例3：取得已刪除但未針對此金鑰保存庫清除的憑證 MyCert。</span><span class="sxs-lookup"><span data-stu-id="02a17-118">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="02a17-119">這個命令會在名為 Contoso 的金鑰保存庫中，取得名為「MyCert」的憑證，但尚未清除。</span><span class="sxs-lookup"><span data-stu-id="02a17-119">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="02a17-120">這個命令會傳回中繼資料，例如刪除日期，以及此刪除的憑證的排程清除日期。</span><span class="sxs-lookup"><span data-stu-id="02a17-120">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

## <span data-ttu-id="02a17-121">參數</span><span class="sxs-lookup"><span data-stu-id="02a17-121">PARAMETERS</span></span>

### <span data-ttu-id="02a17-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02a17-122">-DefaultProfile</span></span>
<span data-ttu-id="02a17-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="02a17-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="02a17-124">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="02a17-124">-IncludeVersions</span></span>
<span data-ttu-id="02a17-125">表示此操作會取得所有版本的憑證。</span><span class="sxs-lookup"><span data-stu-id="02a17-125">Indicates that this operation gets all versions of the certificate.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByCertificateAllVersions, ByCertificateAllVersionsInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02a17-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02a17-126">-InputObject</span></span>
<span data-ttu-id="02a17-127">KeyVault 物件。</span><span class="sxs-lookup"><span data-stu-id="02a17-127">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByNameInputObject, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02a17-128">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="02a17-128">-InRemovedState</span></span>
<span data-ttu-id="02a17-129">指定是否要在輸出中包含先前刪除的憑證</span><span class="sxs-lookup"><span data-stu-id="02a17-129">Specifies whether to include previously deleted certificates in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByName, ByNameInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02a17-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="02a17-130">-Name</span></span>
<span data-ttu-id="02a17-131">指定要取得的憑證名稱。</span><span class="sxs-lookup"><span data-stu-id="02a17-131">Specifies the name of the certificate to get.</span></span>

```yaml
Type: String
Parameter Sets: ByName, ByNameInputObject
Aliases: CertificateName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateAllVersions, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02a17-132">-VaultName</span><span class="sxs-lookup"><span data-stu-id="02a17-132">-VaultName</span></span>
<span data-ttu-id="02a17-133">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="02a17-133">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: ByName, ByCertificateNameAndVersion, ByCertificateAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02a17-134">-版本</span><span class="sxs-lookup"><span data-stu-id="02a17-134">-Version</span></span>
<span data-ttu-id="02a17-135">指定憑證版本。</span><span class="sxs-lookup"><span data-stu-id="02a17-135">Specifies the version of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateNameAndVersionInputObject
Aliases: CertificateVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02a17-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02a17-136">CommonParameters</span></span>
<span data-ttu-id="02a17-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="02a17-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02a17-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="02a17-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02a17-139">輸入</span><span class="sxs-lookup"><span data-stu-id="02a17-139">INPUTS</span></span>

### <span data-ttu-id="02a17-140">所有</span><span class="sxs-lookup"><span data-stu-id="02a17-140">None</span></span>
<span data-ttu-id="02a17-141">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="02a17-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="02a17-142">輸出</span><span class="sxs-lookup"><span data-stu-id="02a17-142">OUTPUTS</span></span>

### <span data-ttu-id="02a17-143">[System.object]. 清單 ' 1 [KeyVault]。 PSKeyVaultCertificateIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="02a17-143">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem]</span></span>

### <span data-ttu-id="02a17-144">PSKeyVaultCertificate 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="02a17-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="02a17-145">筆記</span><span class="sxs-lookup"><span data-stu-id="02a17-145">NOTES</span></span>

## <span data-ttu-id="02a17-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="02a17-146">RELATED LINKS</span></span>

[<span data-ttu-id="02a17-147">附加 AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="02a17-147">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="02a17-148">匯入-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="02a17-148">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="02a17-149">移除-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="02a17-149">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="02a17-150">復原-AzureKeyVaultSecretCertificate</span><span class="sxs-lookup"><span data-stu-id="02a17-150">Undo-AzureKeyVaultSecretCertificate</span></span>](./Undo-AzureKeyVaultSecretCertificate.md)
