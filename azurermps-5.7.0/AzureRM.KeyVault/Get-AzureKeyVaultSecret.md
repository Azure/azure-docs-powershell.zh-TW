---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultSecret.md
ms.openlocfilehash: f2507d441dc04fd01217dde685deb667211f4034
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457160"
---
# <span data-ttu-id="b59dc-101">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b59dc-101">Get-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="b59dc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b59dc-102">SYNOPSIS</span></span>
<span data-ttu-id="b59dc-103">取得金鑰保存庫中的密碼。</span><span class="sxs-lookup"><span data-stu-id="b59dc-103">Gets the secrets in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b59dc-104">句法</span><span class="sxs-lookup"><span data-stu-id="b59dc-104">SYNTAX</span></span>

### <span data-ttu-id="b59dc-105">ByVaultName (預設) </span><span class="sxs-lookup"><span data-stu-id="b59dc-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b59dc-106">BySecretName</span><span class="sxs-lookup"><span data-stu-id="b59dc-106">BySecretName</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b59dc-107">BySecretVersions</span><span class="sxs-lookup"><span data-stu-id="b59dc-107">BySecretVersions</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b59dc-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="b59dc-108">ByInputObjectVaultName</span></span>
```
Get-AzureKeyVaultSecret [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b59dc-109">ByInputObjectSecretName</span><span class="sxs-lookup"><span data-stu-id="b59dc-109">ByInputObjectSecretName</span></span>
```
Get-AzureKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b59dc-110">ByInputObjectSecretVersions</span><span class="sxs-lookup"><span data-stu-id="b59dc-110">ByInputObjectSecretVersions</span></span>
```
Get-AzureKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b59dc-111">說明</span><span class="sxs-lookup"><span data-stu-id="b59dc-111">DESCRIPTION</span></span>
<span data-ttu-id="b59dc-112">**AzureKeyVaultSecret** Cmdlet 會在金鑰保存庫中取得機密資訊。</span><span class="sxs-lookup"><span data-stu-id="b59dc-112">The **Get-AzureKeyVaultSecret** cmdlet gets secrets in a key vault.</span></span>
<span data-ttu-id="b59dc-113">這個 Cmdlet 會在金鑰保存庫中取得特定機密或所有機密。</span><span class="sxs-lookup"><span data-stu-id="b59dc-113">This cmdlet gets a specific secret or all the secrets in a key vault.</span></span>

## <span data-ttu-id="b59dc-114">示例</span><span class="sxs-lookup"><span data-stu-id="b59dc-114">EXAMPLES</span></span>

### <span data-ttu-id="b59dc-115">範例1：取得金鑰保存庫中所有機密的最新版本</span><span class="sxs-lookup"><span data-stu-id="b59dc-115">Example 1: Get all current versions of all secrets in a key vault</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso'
```

<span data-ttu-id="b59dc-116">這個命令會取得名為 Contoso 之金鑰保存庫中所有機密的目前版本。</span><span class="sxs-lookup"><span data-stu-id="b59dc-116">This command gets the current versions of all secrets in the key vault named Contoso.</span></span>

### <span data-ttu-id="b59dc-117">範例2：取得特定機密的所有版本</span><span class="sxs-lookup"><span data-stu-id="b59dc-117">Example 2: Get all versions of a specific secret</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -IncludeVersions
```

<span data-ttu-id="b59dc-118">這個命令會取得名為 Contoso 之金鑰保存庫中名為 ITSecret 的所有版本。</span><span class="sxs-lookup"><span data-stu-id="b59dc-118">This command gets all versions of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="b59dc-119">範例3：取得特定機密的目前版本</span><span class="sxs-lookup"><span data-stu-id="b59dc-119">Example 3: Get the current version of a specific secret</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
```

<span data-ttu-id="b59dc-120">這個命令會取得名為 Contoso 之金鑰保存庫中名為 ITSecret 的目前版本。</span><span class="sxs-lookup"><span data-stu-id="b59dc-120">This command gets the current version of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="b59dc-121">範例4：取得特定機密的特定版本</span><span class="sxs-lookup"><span data-stu-id="b59dc-121">Example 4: Get a specific version of a specific secret</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -Version '6A12A286385949DB8B5F82AFEF85CAE9'
```

<span data-ttu-id="b59dc-122">這個命令會在名為 Contoso 的主要電子倉庫中取得名為 ITSecret 的特定密碼版本。</span><span class="sxs-lookup"><span data-stu-id="b59dc-122">This command gets a specific version of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="b59dc-123">範例5：取得特定機密之目前版本的純文字值</span><span class="sxs-lookup"><span data-stu-id="b59dc-123">Example 5: Get the plain text value of the current version of a specific secret</span></span>
```
PS C:\>$secret = Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
PS C:\> Write-Host "Secret Value is: " $secret.SecretValueText
```

<span data-ttu-id="b59dc-124">這些命令會取得名為 ITSecret 之密碼的目前版本，然後顯示該秘密的純文字值。</span><span class="sxs-lookup"><span data-stu-id="b59dc-124">These commands get the current version of a secret named ITSecret, and then displays the plain text value of that secret.</span></span>

### <span data-ttu-id="b59dc-125">範例6：取得已刪除但未針對此金鑰保存庫清除的所有機密。</span><span class="sxs-lookup"><span data-stu-id="b59dc-125">Example 6: Get all the secrets that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="b59dc-126">這個命令會在名為 Contoso 的金鑰保存庫中，取得先前已刪除但尚未清除的所有機密。</span><span class="sxs-lookup"><span data-stu-id="b59dc-126">This command gets all the secrets that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="b59dc-127">範例7：取得已刪除但未針對此金鑰保存庫清除的機密 ITSecret。</span><span class="sxs-lookup"><span data-stu-id="b59dc-127">Example 7: Gets the secret ITSecret that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -KeyName 'ITSecret' -InRemovedState
```

<span data-ttu-id="b59dc-128">這個命令會在名為 Contoso 的金鑰保存庫中，取得先前已刪除但尚未清除的機密 ITSecret。</span><span class="sxs-lookup"><span data-stu-id="b59dc-128">This command gets the secret ITSecret that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="b59dc-129">這個命令會傳回中繼資料，例如刪除日期，以及此刪除的機密的排程清除日期。</span><span class="sxs-lookup"><span data-stu-id="b59dc-129">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted secret.</span></span>

## <span data-ttu-id="b59dc-130">參數</span><span class="sxs-lookup"><span data-stu-id="b59dc-130">PARAMETERS</span></span>

### <span data-ttu-id="b59dc-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b59dc-131">-DefaultProfile</span></span>
<span data-ttu-id="b59dc-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b59dc-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b59dc-133">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="b59dc-133">-IncludeVersions</span></span>
<span data-ttu-id="b59dc-134">表示此 Cmdlet 會取得所有版本的密碼。</span><span class="sxs-lookup"><span data-stu-id="b59dc-134">Indicates that this cmdlet gets all versions of a secret.</span></span>
<span data-ttu-id="b59dc-135">密碼的目前版本是清單中的第一個版本。</span><span class="sxs-lookup"><span data-stu-id="b59dc-135">The current version of a secret is the first one on the list.</span></span>
<span data-ttu-id="b59dc-136">如果您指定此參數，您也必須指定 *Name* 及 *VaultName* 參數。</span><span class="sxs-lookup"><span data-stu-id="b59dc-136">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>

<span data-ttu-id="b59dc-137">如果您沒有指定 *IncludeVersions* 參數，這個 Cmdlet 會以指定的 *名稱* 取得目前的機密版本。</span><span class="sxs-lookup"><span data-stu-id="b59dc-137">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the secret with the specified *Name*.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: BySecretVersions, ByInputObjectSecretVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b59dc-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b59dc-138">-InputObject</span></span>
<span data-ttu-id="b59dc-139">KeyVault 物件。</span><span class="sxs-lookup"><span data-stu-id="b59dc-139">KeyVault Object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObjectVaultName, ByInputObjectSecretName, ByInputObjectSecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b59dc-140">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="b59dc-140">-InRemovedState</span></span>
<span data-ttu-id="b59dc-141">指定是否要在輸出中顯示先前刪除的機密</span><span class="sxs-lookup"><span data-stu-id="b59dc-141">Specifies whether to show the previously deleted secrets in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByVaultName, ByInputObjectVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b59dc-142">-名稱</span><span class="sxs-lookup"><span data-stu-id="b59dc-142">-Name</span></span>
<span data-ttu-id="b59dc-143">指定要取得之密碼的名稱。</span><span class="sxs-lookup"><span data-stu-id="b59dc-143">Specifies the name of the secret to get.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName, ByInputObjectVaultName
Aliases: SecretName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: BySecretName, BySecretVersions, ByInputObjectSecretName, ByInputObjectSecretVersions
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b59dc-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b59dc-144">-VaultName</span></span>
<span data-ttu-id="b59dc-145">指定機密所屬之金鑰保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="b59dc-145">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="b59dc-146">這個 Cmdlet 會根據此參數指定的名稱和您目前的環境，來構造金鑰 vault (FQDN) 的完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="b59dc-146">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName, BySecretName, BySecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b59dc-147">-版本</span><span class="sxs-lookup"><span data-stu-id="b59dc-147">-Version</span></span>
<span data-ttu-id="b59dc-148">指定機密版本。</span><span class="sxs-lookup"><span data-stu-id="b59dc-148">Specifies the secret version.</span></span>
<span data-ttu-id="b59dc-149">這個 Cmdlet 根據金鑰保存庫名稱、您目前選取的環境、密碼及機密版本來構造秘密的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="b59dc-149">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

```yaml
Type: String
Parameter Sets: BySecretName, ByInputObjectSecretName
Aliases: SecretVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b59dc-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b59dc-150">CommonParameters</span></span>
<span data-ttu-id="b59dc-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b59dc-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b59dc-152">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b59dc-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b59dc-153">輸入</span><span class="sxs-lookup"><span data-stu-id="b59dc-153">INPUTS</span></span>

### <span data-ttu-id="b59dc-154">字串</span><span class="sxs-lookup"><span data-stu-id="b59dc-154">String</span></span>

## <span data-ttu-id="b59dc-155">輸出</span><span class="sxs-lookup"><span data-stu-id="b59dc-155">OUTPUTS</span></span>

### <span data-ttu-id="b59dc-156">清單<PSKeyVaultSecretIdentityItem>，KeyVault.. PSKeyVaultSecret、List<Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem>、Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret。</span><span class="sxs-lookup"><span data-stu-id="b59dc-156">List<Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret, List<Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="b59dc-157">筆記</span><span class="sxs-lookup"><span data-stu-id="b59dc-157">NOTES</span></span>

## <span data-ttu-id="b59dc-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="b59dc-158">RELATED LINKS</span></span>

[<span data-ttu-id="b59dc-159">移除-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b59dc-159">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="b59dc-160">復原-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="b59dc-160">Undo-AzureKeyVaultSecretRemoval</span></span>](./Undo-AzureKeyVaultSecretRemoval.md)

[<span data-ttu-id="b59dc-161">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b59dc-161">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

