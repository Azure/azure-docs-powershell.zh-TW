---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
ms.openlocfilehash: 40514bdd6ed8d37679d3002f80146e622a0614e9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794683"
---
# <span data-ttu-id="d011e-101">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="d011e-101">Get-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="d011e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d011e-102">SYNOPSIS</span></span>
<span data-ttu-id="d011e-103">從金鑰保存庫取得憑證。</span><span class="sxs-lookup"><span data-stu-id="d011e-103">Gets a certificate from a key vault.</span></span>

## <span data-ttu-id="d011e-104">句法</span><span class="sxs-lookup"><span data-stu-id="d011e-104">SYNTAX</span></span>

### <span data-ttu-id="d011e-105">ByVaultName (預設) </span><span class="sxs-lookup"><span data-stu-id="d011e-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d011e-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="d011e-106">ByCertificateName</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d011e-107">ByCertificateVersions</span><span class="sxs-lookup"><span data-stu-id="d011e-107">ByCertificateVersions</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d011e-108">ByDeletedCertificates</span><span class="sxs-lookup"><span data-stu-id="d011e-108">ByDeletedCertificates</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d011e-109">說明</span><span class="sxs-lookup"><span data-stu-id="d011e-109">DESCRIPTION</span></span>
<span data-ttu-id="d011e-110">**AzKeyVaultCertificate** Cmdlet 會從 Azure 金鑰保存庫中的金鑰保存庫取得指定的憑證或憑證版本。</span><span class="sxs-lookup"><span data-stu-id="d011e-110">The **Get-AzKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="d011e-111">示例</span><span class="sxs-lookup"><span data-stu-id="d011e-111">EXAMPLES</span></span>

### <span data-ttu-id="d011e-112">範例1：取得憑證</span><span class="sxs-lookup"><span data-stu-id="d011e-112">Example 1: Get a certificate</span></span>
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

<span data-ttu-id="d011e-113">這個命令會從名為 ContosoKV01 的主要電子倉庫中取得名為 TestCert01 的憑證。</span><span class="sxs-lookup"><span data-stu-id="d011e-113">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="d011e-114">範例2：取得已刪除但未針對此金鑰保存庫清除的所有憑證。</span><span class="sxs-lookup"><span data-stu-id="d011e-114">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultCertificate -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="d011e-115">這個命令會在名為 Contoso 的金鑰保存庫中，取得先前已刪除但尚未清除的所有憑證。</span><span class="sxs-lookup"><span data-stu-id="d011e-115">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="d011e-116">範例3：取得已刪除但未針對此金鑰保存庫清除的憑證 MyCert。</span><span class="sxs-lookup"><span data-stu-id="d011e-116">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="d011e-117">這個命令會在名為 Contoso 的金鑰保存庫中，取得名為「MyCert」的憑證，但尚未清除。</span><span class="sxs-lookup"><span data-stu-id="d011e-117">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="d011e-118">這個命令會傳回中繼資料，例如刪除日期，以及此刪除的憑證的排程清除日期。</span><span class="sxs-lookup"><span data-stu-id="d011e-118">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

## <span data-ttu-id="d011e-119">參數</span><span class="sxs-lookup"><span data-stu-id="d011e-119">PARAMETERS</span></span>

### <span data-ttu-id="d011e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d011e-120">-DefaultProfile</span></span>
<span data-ttu-id="d011e-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d011e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d011e-122">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="d011e-122">-IncludeVersions</span></span>
<span data-ttu-id="d011e-123">表示此操作會取得所有版本的憑證。</span><span class="sxs-lookup"><span data-stu-id="d011e-123">Indicates that this operation gets all versions of the certificate.</span></span>

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

### <span data-ttu-id="d011e-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="d011e-124">-InRemovedState</span></span>
<span data-ttu-id="d011e-125">指定是否要在輸出中包含先前刪除的憑證</span><span class="sxs-lookup"><span data-stu-id="d011e-125">Specifies whether to include previously deleted certificates in the output</span></span>

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

### <span data-ttu-id="d011e-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="d011e-126">-Name</span></span>
<span data-ttu-id="d011e-127">指定要取得的憑證名稱。</span><span class="sxs-lookup"><span data-stu-id="d011e-127">Specifies the name of the certificate to get.</span></span>

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

### <span data-ttu-id="d011e-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d011e-128">-VaultName</span></span>
<span data-ttu-id="d011e-129">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="d011e-129">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="d011e-130">-版本</span><span class="sxs-lookup"><span data-stu-id="d011e-130">-Version</span></span>
<span data-ttu-id="d011e-131">指定憑證版本。</span><span class="sxs-lookup"><span data-stu-id="d011e-131">Specifies the version of a certificate.</span></span>

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

### <span data-ttu-id="d011e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d011e-132">CommonParameters</span></span>
<span data-ttu-id="d011e-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d011e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d011e-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d011e-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d011e-135">輸入</span><span class="sxs-lookup"><span data-stu-id="d011e-135">INPUTS</span></span>

### <span data-ttu-id="d011e-136">所有</span><span class="sxs-lookup"><span data-stu-id="d011e-136">None</span></span>
<span data-ttu-id="d011e-137">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="d011e-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d011e-138">輸出</span><span class="sxs-lookup"><span data-stu-id="d011e-138">OUTPUTS</span></span>

### <span data-ttu-id="d011e-139">[System.object]. 清單 ' 1 [KeyVault]。 CertificateIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="d011e-139">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.CertificateIdentityItem]</span></span>

### <span data-ttu-id="d011e-140">KeyVaultCertificate 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="d011e-140">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span></span>

## <span data-ttu-id="d011e-141">筆記</span><span class="sxs-lookup"><span data-stu-id="d011e-141">NOTES</span></span>

## <span data-ttu-id="d011e-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="d011e-142">RELATED LINKS</span></span>

[<span data-ttu-id="d011e-143">附加 AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="d011e-143">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="d011e-144">匯入-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="d011e-144">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="d011e-145">移除-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="d011e-145">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="d011e-146">復原-AzKeyVaultSecretCertificate</span><span class="sxs-lookup"><span data-stu-id="d011e-146">Undo-AzKeyVaultSecretCertificate</span></span>](./Undo-AzKeyVaultSecretCertificate.md)
