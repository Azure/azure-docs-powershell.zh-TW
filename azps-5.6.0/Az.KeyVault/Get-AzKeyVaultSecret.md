---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
ms.openlocfilehash: 361425e7bee88300a196c9ed7ac33fe4db171b8d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914809"
---
# <span data-ttu-id="77682-101">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="77682-101">Get-AzKeyVaultSecret</span></span>

## <span data-ttu-id="77682-102">簡介</span><span class="sxs-lookup"><span data-stu-id="77682-102">SYNOPSIS</span></span>
<span data-ttu-id="77682-103">在金鑰庫中獲取秘訣。</span><span class="sxs-lookup"><span data-stu-id="77682-103">Gets the secrets in a key vault.</span></span>

## <span data-ttu-id="77682-104">語法</span><span class="sxs-lookup"><span data-stu-id="77682-104">SYNTAX</span></span>

### <span data-ttu-id="77682-105">ByVaultName (預設) </span><span class="sxs-lookup"><span data-stu-id="77682-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77682-106">BySecretName</span><span class="sxs-lookup"><span data-stu-id="77682-106">BySecretName</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Version] <String> [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77682-107">BySecretVersions</span><span class="sxs-lookup"><span data-stu-id="77682-107">BySecretVersions</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77682-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="77682-108">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77682-109">ByInputObjectSecretName</span><span class="sxs-lookup"><span data-stu-id="77682-109">ByInputObjectSecretName</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String> [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77682-110">ByInputObjectSecretVersions</span><span class="sxs-lookup"><span data-stu-id="77682-110">ByInputObjectSecretVersions</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77682-111">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="77682-111">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77682-112">ByResourceIdSecretName</span><span class="sxs-lookup"><span data-stu-id="77682-112">ByResourceIdSecretName</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-Version] <String> [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77682-113">ByResourceIdSecretVersions</span><span class="sxs-lookup"><span data-stu-id="77682-113">ByResourceIdSecretVersions</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77682-114">描述</span><span class="sxs-lookup"><span data-stu-id="77682-114">DESCRIPTION</span></span>
<span data-ttu-id="77682-115">**Get-AzKeyVaultSecret** Cmdlet 會取得金鑰庫中的機密。</span><span class="sxs-lookup"><span data-stu-id="77682-115">The **Get-AzKeyVaultSecret** cmdlet gets secrets in a key vault.</span></span>
<span data-ttu-id="77682-116">此 Cmdlet 會獲得金鑰庫中的特定機密或所有機密。</span><span class="sxs-lookup"><span data-stu-id="77682-116">This cmdlet gets a specific secret or all the secrets in a key vault.</span></span>

## <span data-ttu-id="77682-117">例子</span><span class="sxs-lookup"><span data-stu-id="77682-117">EXAMPLES</span></span>

### <span data-ttu-id="77682-118">範例 1：取得金鑰庫中所有機密的所有目前版本</span><span class="sxs-lookup"><span data-stu-id="77682-118">Example 1: Get all current versions of all secrets in a key vault</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso'

Vault Name   : contoso
Name         : secret1
Version      :
Id           : https://contoso.vault.azure.net:443/secrets/secret1
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :

Vault Name   : contoso
Name         : secret2
Version      :
Id           : https://contoso.vault.azure.net:443/secrets/secret2
Enabled      : True
Expires      :
Not Before   :
Created      : 4/11/2018 11:45:06 PM
Updated      : 4/11/2018 11:45:06 PM
Content Type :
Tags         :
```

<span data-ttu-id="77682-119">此命令會獲得名稱為 Contoso 之金鑰庫中所有機密的最新版本。</span><span class="sxs-lookup"><span data-stu-id="77682-119">This command gets the current versions of all secrets in the key vault named Contoso.</span></span>

### <span data-ttu-id="77682-120">範例 2：取得特定機密的所有版本</span><span class="sxs-lookup"><span data-stu-id="77682-120">Example 2: Get all versions of a specific secret</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'secret1' -IncludeVersions

Vault Name   : contoso
Name         : secret1
Version      : 7128133570f84a71b48d7d0550deb74c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/7128133570f84a71b48d7d0550deb74c
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :

Vault Name   : contoso
Name         : secret1
Version      : 5d1a74ba2c454439886fb8509b6cab3c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/5d1a74ba2c454439886fb8509b6cab3c
Enabled      : True
Expires      :
Not Before   :
Created      : 4/5/2018 11:44:50 PM
Updated      : 4/5/2018 11:44:50 PM
Content Type :
Tags         :
```

<span data-ttu-id="77682-121">此命令會獲得名稱為 Contoso 之金鑰庫之機密的所有版本。</span><span class="sxs-lookup"><span data-stu-id="77682-121">This command gets all versions of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="77682-122">範例 3：取得特定機密的目前版本</span><span class="sxs-lookup"><span data-stu-id="77682-122">Example 3: Get the current version of a specific secret</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'secret1'

Vault Name   : contoso
Name         : secret1
Version      : 7128133570f84a71b48d7d0550deb74c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/7128133570f84a71b48d7d0550deb74c
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :
```

<span data-ttu-id="77682-123">此命令會獲得名稱為 Contoso 之金鑰庫之機密的目前版本。</span><span class="sxs-lookup"><span data-stu-id="77682-123">This command gets the current version of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="77682-124">範例 4：取得特定機密的特定版本</span><span class="sxs-lookup"><span data-stu-id="77682-124">Example 4: Get a specific version of a specific secret</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'secret1' -Version '5d1a74ba2c454439886fb8509b6cab3c'

Vault Name   : contoso
Name         : secret1
Version      : 5d1a74ba2c454439886fb8509b6cab3c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/5d1a74ba2c454439886fb8509b6cab3c
Enabled      : True
Expires      :
Not Before   :
Created      : 4/5/2018 11:44:50 PM
Updated      : 4/5/2018 11:44:50 PM
Content Type :
Tags         :
```

<span data-ttu-id="77682-125">此命令在名稱為 Contoso 的金鑰庫內，會獲得名為 secret1 的特定版本。</span><span class="sxs-lookup"><span data-stu-id="77682-125">This command gets a specific version of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="77682-126">範例 5：取得特定機密目前版本的純文字值</span><span class="sxs-lookup"><span data-stu-id="77682-126">Example 5: Get the plain text value of the current version of a specific secret</span></span>
```powershell
PS C:\> $secretText = Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -AsPlainText
```

<span data-ttu-id="77682-127">Cmdlet 會以字串形式在已使用時 `-AsPlainText` ，將密碼做為字串。</span><span class="sxs-lookup"><span data-stu-id="77682-127">The cmdlet returns the secret as a string when `-AsPlainText` is applied.</span></span>

### <span data-ttu-id="77682-128">範例 6：取得此金鑰庫的所有已被刪除但並未清除的機密。</span><span class="sxs-lookup"><span data-stu-id="77682-128">Example 6: Get all the secrets that have been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -InRemovedState

Vault Name           : contoso
Name                 : secret1
Id                   : https://contoso.vault.azure.net:443/secrets/secret1
Deleted Date         : 4/4/2018 8:51:58 PM
Scheduled Purge Date : 7/3/2018 8:51:58 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/4/2018 8:51:03 PM
Updated              : 4/4/2018 8:51:03 PM
Content Type         :
Tags                 :

Vault Name           : contoso
Name                 : secret2
Id                   : https://contoso.vault.azure.net:443/secrets/secret2
Deleted Date         : 5/7/2018 7:56:34 PM
Scheduled Purge Date : 8/5/2018 7:56:34 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/6/2018 8:39:15 PM
Updated              : 4/6/2018 10:11:24 PM
Content Type         :
Tags                 :
```

<span data-ttu-id="77682-129">此命令會獲得先前在名稱為 Contoso 的金鑰庫中刪除但並未清除的所有機密。</span><span class="sxs-lookup"><span data-stu-id="77682-129">This command gets all the secrets that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="77682-130">範例 7：針對此金鑰庫，獲得已被刪除但並未清除的機密 ITSecret。</span><span class="sxs-lookup"><span data-stu-id="77682-130">Example 7: Gets the secret ITSecret that has been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'secret1' -InRemovedState

Vault Name           : contoso
Name                 : secret1
Version              : 689d23346e9c42a2a64f4e3d75094dcc
Id                   : https://contoso.vault.azure.net:443/secrets/secret1/689d23346e9c42a2a64f4e3d75094dcc
Deleted Date         : 4/4/2018 8:51:58 PM
Scheduled Purge Date : 7/3/2018 8:51:58 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/4/2018 8:51:03 PM
Updated              : 4/4/2018 8:51:03 PM
Content Type         :
Tags                 :
```

<span data-ttu-id="77682-131">此命令會獲得先前在名稱為 Contoso 的金鑰庫中刪除但並未清除的機密'機密 1。」</span><span class="sxs-lookup"><span data-stu-id="77682-131">This command gets the secret 'secret1' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="77682-132">此命令會返回中繼資料，例如刪除日期，以及此已刪除之機密的排程清除日期。</span><span class="sxs-lookup"><span data-stu-id="77682-132">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted secret.</span></span>

### <span data-ttu-id="77682-133">範例 8：使用篩選在金鑰庫中取得所有機密的所有目前版本</span><span class="sxs-lookup"><span data-stu-id="77682-133">Example 8: Get all current versions of all secrets in a key vault using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name "secret*"

Vault Name   : contoso
Name         : secret1
Version      :
Id           : https://contoso.vault.azure.net:443/secrets/secret1
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :

Vault Name   : contoso
Name         : secret2
Version      :
Id           : https://contoso.vault.azure.net:443/secrets/secret2
Enabled      : True
Expires      :
Not Before   :
Created      : 4/11/2018 11:45:06 PM
Updated      : 4/11/2018 11:45:06 PM
Content Type :
Tags         :
```

<span data-ttu-id="77682-134">此命令會獲得名稱為 Contoso 之金鑰庫中所有機密的最新版本，以「機密」做為開始。</span><span class="sxs-lookup"><span data-stu-id="77682-134">This command gets the current versions of all secrets in the key vault named Contoso that start with "secret".</span></span>

## <span data-ttu-id="77682-135">參數</span><span class="sxs-lookup"><span data-stu-id="77682-135">PARAMETERS</span></span>

### <span data-ttu-id="77682-136">-AsPtext</span><span class="sxs-lookup"><span data-stu-id="77682-136">-AsPlainText</span></span>
<span data-ttu-id="77682-137">設定之後，Cmdlet 會將安全字串中的機密轉換為解密純文字字串做為輸出。</span><span class="sxs-lookup"><span data-stu-id="77682-137">When set, the cmdlet will convert secret in secure string to the decrypted plaintext string as output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByVaultName, BySecretName, ByInputObjectVaultName, ByInputObjectSecretName, ByResourceIdVaultName, ByResourceIdSecretName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77682-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77682-138">-DefaultProfile</span></span>
<span data-ttu-id="77682-139">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="77682-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77682-140">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="77682-140">-IncludeVersions</span></span>
<span data-ttu-id="77682-141">表示此 Cmdlet 會獲得所有版本的機密。</span><span class="sxs-lookup"><span data-stu-id="77682-141">Indicates that this cmdlet gets all versions of a secret.</span></span>
<span data-ttu-id="77682-142">目前版本的機密是清單中的第一個版本。</span><span class="sxs-lookup"><span data-stu-id="77682-142">The current version of a secret is the first one on the list.</span></span>
<span data-ttu-id="77682-143">如果您指定此參數，您也必須指定 *Name* 和 *VaultName* 參數。</span><span class="sxs-lookup"><span data-stu-id="77682-143">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="77682-144">如果您未指定 *IncludeVersions* 參數，此 Cmdlet 會以指定的名稱獲得目前版本的 *機密*。</span><span class="sxs-lookup"><span data-stu-id="77682-144">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the secret with the specified *Name*.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BySecretVersions, ByInputObjectSecretVersions, ByResourceIdSecretVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77682-145">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77682-145">-InputObject</span></span>
<span data-ttu-id="77682-146">KeyVault 物件。</span><span class="sxs-lookup"><span data-stu-id="77682-146">KeyVault Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObjectVaultName, ByInputObjectSecretName, ByInputObjectSecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77682-147">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="77682-147">-InRemovedState</span></span>
<span data-ttu-id="77682-148">指定是否要在輸出中顯示先前刪除的秘訣</span><span class="sxs-lookup"><span data-stu-id="77682-148">Specifies whether to show the previously deleted secrets in the output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77682-149">-名稱</span><span class="sxs-lookup"><span data-stu-id="77682-149">-Name</span></span>
<span data-ttu-id="77682-150">指定要取得之機密的名稱。</span><span class="sxs-lookup"><span data-stu-id="77682-150">Specifies the name of the secret to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases: SecretName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: BySecretName, BySecretVersions, ByInputObjectSecretName, ByInputObjectSecretVersions, ByResourceIdSecretName, ByResourceIdSecretVersions
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="77682-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77682-151">-ResourceId</span></span>
<span data-ttu-id="77682-152">KeyVault 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="77682-152">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdVaultName, ByResourceIdSecretName, ByResourceIdSecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77682-153">-VaultName</span><span class="sxs-lookup"><span data-stu-id="77682-153">-VaultName</span></span>
<span data-ttu-id="77682-154">指定該機密所屬的金鑰庫名稱。</span><span class="sxs-lookup"><span data-stu-id="77682-154">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="77682-155">此 Cmdlet 會根據此參數指定的名稱 (您目前的環境，建構金鑰庫的 FQDN) 完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="77682-155">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, BySecretName, BySecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77682-156">-版本</span><span class="sxs-lookup"><span data-stu-id="77682-156">-Version</span></span>
<span data-ttu-id="77682-157">指定機密版本。</span><span class="sxs-lookup"><span data-stu-id="77682-157">Specifies the secret version.</span></span>
<span data-ttu-id="77682-158">此 Cmdlet 會依據金鑰庫名稱、您目前選取的環境、機密名稱和金鑰版本來建構機密的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="77682-158">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

```yaml
Type: System.String
Parameter Sets: BySecretName, ByInputObjectSecretName, ByResourceIdSecretName
Aliases: SecretVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77682-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77682-159">CommonParameters</span></span>
<span data-ttu-id="77682-160">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="77682-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77682-161">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="77682-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77682-162">輸入</span><span class="sxs-lookup"><span data-stu-id="77682-162">INPUTS</span></span>

### <span data-ttu-id="77682-163">Microsoft.Azure.Commands.KeyVault.models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="77682-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="77682-164">System.String</span><span class="sxs-lookup"><span data-stu-id="77682-164">System.String</span></span>

## <span data-ttu-id="77682-165">輸出</span><span class="sxs-lookup"><span data-stu-id="77682-165">OUTPUTS</span></span>

### <span data-ttu-id="77682-166">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="77682-166">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

### <span data-ttu-id="77682-167">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="77682-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

### <span data-ttu-id="77682-168">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="77682-168">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

### <span data-ttu-id="77682-169">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="77682-169">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="77682-170">筆記</span><span class="sxs-lookup"><span data-stu-id="77682-170">NOTES</span></span>

## <span data-ttu-id="77682-171">相關連結</span><span class="sxs-lookup"><span data-stu-id="77682-171">RELATED LINKS</span></span>

[<span data-ttu-id="77682-172">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="77682-172">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="77682-173">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="77682-173">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)

[<span data-ttu-id="77682-174">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="77682-174">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

