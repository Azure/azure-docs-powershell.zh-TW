---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
ms.openlocfilehash: af2baec6b25b770c30f5f3207e6ed6b6a4b423f7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971432"
---
# <span data-ttu-id="77b0a-101">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="77b0a-101">Get-AzKeyVaultSecret</span></span>

## <span data-ttu-id="77b0a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="77b0a-102">SYNOPSIS</span></span>
<span data-ttu-id="77b0a-103">取得金鑰保存庫中的密碼。</span><span class="sxs-lookup"><span data-stu-id="77b0a-103">Gets the secrets in a key vault.</span></span>

## <span data-ttu-id="77b0a-104">句法</span><span class="sxs-lookup"><span data-stu-id="77b0a-104">SYNTAX</span></span>

### <span data-ttu-id="77b0a-105">ByVaultName (預設) </span><span class="sxs-lookup"><span data-stu-id="77b0a-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77b0a-106">BySecretName</span><span class="sxs-lookup"><span data-stu-id="77b0a-106">BySecretName</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77b0a-107">BySecretVersions</span><span class="sxs-lookup"><span data-stu-id="77b0a-107">BySecretVersions</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77b0a-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="77b0a-108">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77b0a-109">ByInputObjectSecretName</span><span class="sxs-lookup"><span data-stu-id="77b0a-109">ByInputObjectSecretName</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77b0a-110">ByInputObjectSecretVersions</span><span class="sxs-lookup"><span data-stu-id="77b0a-110">ByInputObjectSecretVersions</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77b0a-111">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="77b0a-111">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77b0a-112">ByResourceIdSecretName</span><span class="sxs-lookup"><span data-stu-id="77b0a-112">ByResourceIdSecretName</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77b0a-113">ByResourceIdSecretVersions</span><span class="sxs-lookup"><span data-stu-id="77b0a-113">ByResourceIdSecretVersions</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77b0a-114">說明</span><span class="sxs-lookup"><span data-stu-id="77b0a-114">DESCRIPTION</span></span>
<span data-ttu-id="77b0a-115">**AzKeyVaultSecret** Cmdlet 會在金鑰保存庫中取得機密資訊。</span><span class="sxs-lookup"><span data-stu-id="77b0a-115">The **Get-AzKeyVaultSecret** cmdlet gets secrets in a key vault.</span></span>
<span data-ttu-id="77b0a-116">這個 Cmdlet 會在金鑰保存庫中取得特定機密或所有機密。</span><span class="sxs-lookup"><span data-stu-id="77b0a-116">This cmdlet gets a specific secret or all the secrets in a key vault.</span></span>

## <span data-ttu-id="77b0a-117">示例</span><span class="sxs-lookup"><span data-stu-id="77b0a-117">EXAMPLES</span></span>

### <span data-ttu-id="77b0a-118">範例1：取得金鑰保存庫中所有機密的最新版本</span><span class="sxs-lookup"><span data-stu-id="77b0a-118">Example 1: Get all current versions of all secrets in a key vault</span></span>
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

<span data-ttu-id="77b0a-119">這個命令會取得名為 Contoso 之金鑰保存庫中所有機密的目前版本。</span><span class="sxs-lookup"><span data-stu-id="77b0a-119">This command gets the current versions of all secrets in the key vault named Contoso.</span></span>

### <span data-ttu-id="77b0a-120">範例2：取得特定機密的所有版本</span><span class="sxs-lookup"><span data-stu-id="77b0a-120">Example 2: Get all versions of a specific secret</span></span>
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

<span data-ttu-id="77b0a-121">這個命令會取得名為 Contoso 之金鑰保存庫中名為 secret1 的所有版本。</span><span class="sxs-lookup"><span data-stu-id="77b0a-121">This command gets all versions of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="77b0a-122">範例3：取得特定機密的目前版本</span><span class="sxs-lookup"><span data-stu-id="77b0a-122">Example 3: Get the current version of a specific secret</span></span>
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

<span data-ttu-id="77b0a-123">這個命令會取得名為 Contoso 之金鑰保存庫中名為 secret1 的目前版本。</span><span class="sxs-lookup"><span data-stu-id="77b0a-123">This command gets the current version of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="77b0a-124">範例4：取得特定機密的特定版本</span><span class="sxs-lookup"><span data-stu-id="77b0a-124">Example 4: Get a specific version of a specific secret</span></span>
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

<span data-ttu-id="77b0a-125">這個命令會在名為 Contoso 的主要電子倉庫中取得名為 secret1 的特定密碼版本。</span><span class="sxs-lookup"><span data-stu-id="77b0a-125">This command gets a specific version of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="77b0a-126">範例5：取得特定機密之目前版本的純文字值</span><span class="sxs-lookup"><span data-stu-id="77b0a-126">Example 5: Get the plain text value of the current version of a specific secret</span></span>
```powershell
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
PS C:\> Write-Host "Secret Value is:" $secret.SecretValueText

Secret Value is: P@ssw0rd
```

<span data-ttu-id="77b0a-127">這些命令會取得名為 ITSecret 之密碼的目前版本，然後顯示該秘密的純文字值。</span><span class="sxs-lookup"><span data-stu-id="77b0a-127">These commands get the current version of a secret named ITSecret, and then displays the plain text value of that secret.</span></span>

### <span data-ttu-id="77b0a-128">範例6：取得已刪除但未針對此金鑰保存庫清除的所有機密。</span><span class="sxs-lookup"><span data-stu-id="77b0a-128">Example 6: Get all the secrets that have been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="77b0a-129">這個命令會在名為 Contoso 的金鑰保存庫中，取得先前已刪除但尚未清除的所有機密。</span><span class="sxs-lookup"><span data-stu-id="77b0a-129">This command gets all the secrets that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="77b0a-130">範例7：取得已刪除但未針對此金鑰保存庫清除的機密 ITSecret。</span><span class="sxs-lookup"><span data-stu-id="77b0a-130">Example 7: Gets the secret ITSecret that has been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="77b0a-131">這個命令會在名為 Contoso 的金鑰保存庫中，取得先前已刪除但尚未清除的機密 ' secret1」。</span><span class="sxs-lookup"><span data-stu-id="77b0a-131">This command gets the secret 'secret1' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="77b0a-132">這個命令會傳回中繼資料，例如刪除日期，以及此刪除的機密的排程清除日期。</span><span class="sxs-lookup"><span data-stu-id="77b0a-132">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted secret.</span></span>

### <span data-ttu-id="77b0a-133">範例8：使用篩選在金鑰保存庫中取得所有機密的最新版本</span><span class="sxs-lookup"><span data-stu-id="77b0a-133">Example 8: Get all current versions of all secrets in a key vault using filtering</span></span>
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

<span data-ttu-id="77b0a-134">這個命令會在名為 Contoso 的主要電子倉庫中，取得以 "secret" 開頭的所有機密的目前版本。</span><span class="sxs-lookup"><span data-stu-id="77b0a-134">This command gets the current versions of all secrets in the key vault named Contoso that start with "secret".</span></span>

## <span data-ttu-id="77b0a-135">參數</span><span class="sxs-lookup"><span data-stu-id="77b0a-135">PARAMETERS</span></span>

### <span data-ttu-id="77b0a-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77b0a-136">-DefaultProfile</span></span>
<span data-ttu-id="77b0a-137">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="77b0a-137">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77b0a-138">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="77b0a-138">-IncludeVersions</span></span>
<span data-ttu-id="77b0a-139">表示此 Cmdlet 會取得所有版本的密碼。</span><span class="sxs-lookup"><span data-stu-id="77b0a-139">Indicates that this cmdlet gets all versions of a secret.</span></span>
<span data-ttu-id="77b0a-140">密碼的目前版本是清單中的第一個版本。</span><span class="sxs-lookup"><span data-stu-id="77b0a-140">The current version of a secret is the first one on the list.</span></span>
<span data-ttu-id="77b0a-141">如果您指定此參數，您也必須指定 *Name* 及 *VaultName* 參數。</span><span class="sxs-lookup"><span data-stu-id="77b0a-141">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="77b0a-142">如果您沒有指定 *IncludeVersions* 參數，這個 Cmdlet 會以指定的 *名稱* 取得目前的機密版本。</span><span class="sxs-lookup"><span data-stu-id="77b0a-142">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the secret with the specified *Name*.</span></span>

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

### <span data-ttu-id="77b0a-143">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77b0a-143">-InputObject</span></span>
<span data-ttu-id="77b0a-144">KeyVault 物件。</span><span class="sxs-lookup"><span data-stu-id="77b0a-144">KeyVault Object.</span></span>

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

### <span data-ttu-id="77b0a-145">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="77b0a-145">-InRemovedState</span></span>
<span data-ttu-id="77b0a-146">指定是否要在輸出中顯示先前刪除的機密</span><span class="sxs-lookup"><span data-stu-id="77b0a-146">Specifies whether to show the previously deleted secrets in the output</span></span>

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

### <span data-ttu-id="77b0a-147">-名稱</span><span class="sxs-lookup"><span data-stu-id="77b0a-147">-Name</span></span>
<span data-ttu-id="77b0a-148">指定要取得之密碼的名稱。</span><span class="sxs-lookup"><span data-stu-id="77b0a-148">Specifies the name of the secret to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases: SecretName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: BySecretName, BySecretVersions, ByInputObjectSecretName, ByInputObjectSecretVersions, ByResourceIdSecretName, ByResourceIdSecretVersions
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77b0a-149">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77b0a-149">-ResourceId</span></span>
<span data-ttu-id="77b0a-150">KeyVault 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="77b0a-150">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="77b0a-151">-VaultName</span><span class="sxs-lookup"><span data-stu-id="77b0a-151">-VaultName</span></span>
<span data-ttu-id="77b0a-152">指定機密所屬之金鑰保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="77b0a-152">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="77b0a-153">這個 Cmdlet 會根據此參數指定的名稱和您目前的環境，來構造金鑰 vault (FQDN) 的完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="77b0a-153">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="77b0a-154">-版本</span><span class="sxs-lookup"><span data-stu-id="77b0a-154">-Version</span></span>
<span data-ttu-id="77b0a-155">指定機密版本。</span><span class="sxs-lookup"><span data-stu-id="77b0a-155">Specifies the secret version.</span></span>
<span data-ttu-id="77b0a-156">這個 Cmdlet 根據金鑰保存庫名稱、您目前選取的環境、密碼及機密版本來構造秘密的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="77b0a-156">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

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

### <span data-ttu-id="77b0a-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77b0a-157">CommonParameters</span></span>
<span data-ttu-id="77b0a-158">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="77b0a-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77b0a-159">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="77b0a-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77b0a-160">輸入</span><span class="sxs-lookup"><span data-stu-id="77b0a-160">INPUTS</span></span>

### <span data-ttu-id="77b0a-161">PSKeyVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="77b0a-161">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="77b0a-162">System.object</span><span class="sxs-lookup"><span data-stu-id="77b0a-162">System.String</span></span>

## <span data-ttu-id="77b0a-163">輸出</span><span class="sxs-lookup"><span data-stu-id="77b0a-163">OUTPUTS</span></span>

### <span data-ttu-id="77b0a-164">PSKeyVaultSecretIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="77b0a-164">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

### <span data-ttu-id="77b0a-165">PSKeyVaultSecret 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="77b0a-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

### <span data-ttu-id="77b0a-166">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="77b0a-166">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

### <span data-ttu-id="77b0a-167">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="77b0a-167">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="77b0a-168">筆記</span><span class="sxs-lookup"><span data-stu-id="77b0a-168">NOTES</span></span>

## <span data-ttu-id="77b0a-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="77b0a-169">RELATED LINKS</span></span>

[<span data-ttu-id="77b0a-170">移除-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="77b0a-170">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="77b0a-171">復原-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="77b0a-171">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)

[<span data-ttu-id="77b0a-172">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="77b0a-172">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)
