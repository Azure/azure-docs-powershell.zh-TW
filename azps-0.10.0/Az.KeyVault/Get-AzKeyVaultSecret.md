---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
ms.openlocfilehash: b14e97ba09cba70a9ec571b2fbf1273de7157930
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795547"
---
# <span data-ttu-id="29f1e-101">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="29f1e-101">Get-AzKeyVaultSecret</span></span>

## <span data-ttu-id="29f1e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="29f1e-102">SYNOPSIS</span></span>
<span data-ttu-id="29f1e-103">取得金鑰保存庫中的密碼。</span><span class="sxs-lookup"><span data-stu-id="29f1e-103">Gets the secrets in a key vault.</span></span>

## <span data-ttu-id="29f1e-104">句法</span><span class="sxs-lookup"><span data-stu-id="29f1e-104">SYNTAX</span></span>

### <span data-ttu-id="29f1e-105">ByVaultName (預設) </span><span class="sxs-lookup"><span data-stu-id="29f1e-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29f1e-106">BySecretName</span><span class="sxs-lookup"><span data-stu-id="29f1e-106">BySecretName</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29f1e-107">BySecretVersions</span><span class="sxs-lookup"><span data-stu-id="29f1e-107">BySecretVersions</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29f1e-108">ByDeletedSecrets</span><span class="sxs-lookup"><span data-stu-id="29f1e-108">ByDeletedSecrets</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29f1e-109">說明</span><span class="sxs-lookup"><span data-stu-id="29f1e-109">DESCRIPTION</span></span>
<span data-ttu-id="29f1e-110">**AzKeyVaultSecret** Cmdlet 會在金鑰保存庫中取得機密資訊。</span><span class="sxs-lookup"><span data-stu-id="29f1e-110">The **Get-AzKeyVaultSecret** cmdlet gets secrets in a key vault.</span></span>
<span data-ttu-id="29f1e-111">這個 Cmdlet 會在金鑰保存庫中取得特定機密或所有機密。</span><span class="sxs-lookup"><span data-stu-id="29f1e-111">This cmdlet gets a specific secret or all the secrets in a key vault.</span></span>

## <span data-ttu-id="29f1e-112">示例</span><span class="sxs-lookup"><span data-stu-id="29f1e-112">EXAMPLES</span></span>

### <span data-ttu-id="29f1e-113">範例1：取得金鑰保存庫中所有機密的最新版本</span><span class="sxs-lookup"><span data-stu-id="29f1e-113">Example 1: Get all current versions of all secrets in a key vault</span></span>
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso'
```

<span data-ttu-id="29f1e-114">這個命令會取得名為 Contoso 之金鑰保存庫中所有機密的目前版本。</span><span class="sxs-lookup"><span data-stu-id="29f1e-114">This command gets the current versions of all secrets in the key vault named Contoso.</span></span>

### <span data-ttu-id="29f1e-115">範例2：取得特定機密的所有版本</span><span class="sxs-lookup"><span data-stu-id="29f1e-115">Example 2: Get all versions of a specific secret</span></span>
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -IncludeVersions
```

<span data-ttu-id="29f1e-116">這個命令會取得名為 Contoso 之金鑰保存庫中名為 ITSecret 的所有版本。</span><span class="sxs-lookup"><span data-stu-id="29f1e-116">This command gets all versions of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="29f1e-117">範例3：取得特定機密的目前版本</span><span class="sxs-lookup"><span data-stu-id="29f1e-117">Example 3: Get the current version of a specific secret</span></span>
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
```

<span data-ttu-id="29f1e-118">這個命令會取得名為 Contoso 之金鑰保存庫中名為 ITSecret 的目前版本。</span><span class="sxs-lookup"><span data-stu-id="29f1e-118">This command gets the current version of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="29f1e-119">範例4：取得特定機密的特定版本</span><span class="sxs-lookup"><span data-stu-id="29f1e-119">Example 4: Get a specific version of a specific secret</span></span>
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -Version '6A12A286385949DB8B5F82AFEF85CAE9'
```

<span data-ttu-id="29f1e-120">這個命令會在名為 Contoso 的主要電子倉庫中取得名為 ITSecret 的特定密碼版本。</span><span class="sxs-lookup"><span data-stu-id="29f1e-120">This command gets a specific version of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="29f1e-121">範例5：取得特定機密之目前版本的純文字值</span><span class="sxs-lookup"><span data-stu-id="29f1e-121">Example 5: Get the plain text value of the current version of a specific secret</span></span>
```
PS C:\>$secret = Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
PS C:\> Write-Host "Secret Value is: " $secret.SecretValueText
```

<span data-ttu-id="29f1e-122">這些命令會取得名為 ITSecret 之密碼的目前版本，然後顯示該秘密的純文字值。</span><span class="sxs-lookup"><span data-stu-id="29f1e-122">These commands get the current version of a secret named ITSecret, and then displays the plain text value of that secret.</span></span>

### <span data-ttu-id="29f1e-123">範例6：取得已刪除但未針對此金鑰保存庫清除的所有機密。</span><span class="sxs-lookup"><span data-stu-id="29f1e-123">Example 6: Get all the secrets that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="29f1e-124">這個命令會在名為 Contoso 的金鑰保存庫中，取得先前已刪除但尚未清除的所有機密。</span><span class="sxs-lookup"><span data-stu-id="29f1e-124">This command gets all the secrets that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="29f1e-125">範例7：取得已刪除但未針對此金鑰保存庫清除的機密 ITSecret。</span><span class="sxs-lookup"><span data-stu-id="29f1e-125">Example 7: Gets the secret ITSecret that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -KeyName 'ITSecret' -InRemovedState
```

<span data-ttu-id="29f1e-126">這個命令會在名為 Contoso 的金鑰保存庫中，取得先前已刪除但尚未清除的機密 ITSecret。</span><span class="sxs-lookup"><span data-stu-id="29f1e-126">This command gets the secret ITSecret that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="29f1e-127">這個命令會傳回中繼資料，例如刪除日期，以及此刪除的機密的排程清除日期。</span><span class="sxs-lookup"><span data-stu-id="29f1e-127">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted secret.</span></span>

## <span data-ttu-id="29f1e-128">參數</span><span class="sxs-lookup"><span data-stu-id="29f1e-128">PARAMETERS</span></span>

### <span data-ttu-id="29f1e-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29f1e-129">-DefaultProfile</span></span>
<span data-ttu-id="29f1e-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="29f1e-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29f1e-131">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="29f1e-131">-IncludeVersions</span></span>
<span data-ttu-id="29f1e-132">表示此 Cmdlet 會取得所有版本的密碼。</span><span class="sxs-lookup"><span data-stu-id="29f1e-132">Indicates that this cmdlet gets all versions of a secret.</span></span>
<span data-ttu-id="29f1e-133">密碼的目前版本是清單中的第一個版本。</span><span class="sxs-lookup"><span data-stu-id="29f1e-133">The current version of a secret is the first one on the list.</span></span>
<span data-ttu-id="29f1e-134">如果您指定此參數，您也必須指定 *Name* 及 *VaultName* 參數。</span><span class="sxs-lookup"><span data-stu-id="29f1e-134">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>

<span data-ttu-id="29f1e-135">如果您沒有指定 *IncludeVersions* 參數，這個 Cmdlet 會以指定的 *名稱* 取得目前的機密版本。</span><span class="sxs-lookup"><span data-stu-id="29f1e-135">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the secret with the specified *Name*.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: BySecretVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29f1e-136">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="29f1e-136">-InRemovedState</span></span>
<span data-ttu-id="29f1e-137">指定是否要在輸出中顯示先前刪除的機密</span><span class="sxs-lookup"><span data-stu-id="29f1e-137">Specifies whether to show the previously deleted secrets in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedSecrets
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29f1e-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="29f1e-138">-Name</span></span>
<span data-ttu-id="29f1e-139">指定要取得之密碼的名稱。</span><span class="sxs-lookup"><span data-stu-id="29f1e-139">Specifies the name of the secret to get.</span></span>

```yaml
Type: String
Parameter Sets: BySecretName, BySecretVersions
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedSecrets
Aliases: SecretName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29f1e-140">-VaultName</span><span class="sxs-lookup"><span data-stu-id="29f1e-140">-VaultName</span></span>
<span data-ttu-id="29f1e-141">指定機密所屬之金鑰保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="29f1e-141">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="29f1e-142">這個 Cmdlet 會根據此參數指定的名稱和您目前的環境，來構造金鑰 vault (FQDN) 的完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="29f1e-142">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="29f1e-143">-版本</span><span class="sxs-lookup"><span data-stu-id="29f1e-143">-Version</span></span>
<span data-ttu-id="29f1e-144">指定機密版本。</span><span class="sxs-lookup"><span data-stu-id="29f1e-144">Specifies the secret version.</span></span>
<span data-ttu-id="29f1e-145">這個 Cmdlet 根據金鑰保存庫名稱、您目前選取的環境、密碼及機密版本來構造秘密的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="29f1e-145">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

```yaml
Type: String
Parameter Sets: BySecretName
Aliases: SecretVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29f1e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29f1e-146">CommonParameters</span></span>
<span data-ttu-id="29f1e-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="29f1e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29f1e-148">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="29f1e-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29f1e-149">輸入</span><span class="sxs-lookup"><span data-stu-id="29f1e-149">INPUTS</span></span>

### <span data-ttu-id="29f1e-150">字串</span><span class="sxs-lookup"><span data-stu-id="29f1e-150">String</span></span>

## <span data-ttu-id="29f1e-151">輸出</span><span class="sxs-lookup"><span data-stu-id="29f1e-151">OUTPUTS</span></span>

### <span data-ttu-id="29f1e-152">[KeyVault]<清單中的 [SecretIdentityItem]。 [KeyVault]><、[]、[>]、、、、、、、、DeletedSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="29f1e-152">List<Microsoft.Azure.Commands.KeyVault.Models.SecretIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.Secret, List<Microsoft.Azure.Commands.KeyVault.Models.DeletedSecretIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.DeletedSecret</span></span>

## <span data-ttu-id="29f1e-153">筆記</span><span class="sxs-lookup"><span data-stu-id="29f1e-153">NOTES</span></span>

## <span data-ttu-id="29f1e-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="29f1e-154">RELATED LINKS</span></span>

[<span data-ttu-id="29f1e-155">移除-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="29f1e-155">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="29f1e-156">復原-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="29f1e-156">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)

[<span data-ttu-id="29f1e-157">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="29f1e-157">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

