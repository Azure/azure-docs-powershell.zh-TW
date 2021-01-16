---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
ms.openlocfilehash: fa53affab7fe530defcf23f169458ee6813722a1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274992"
---
# <span data-ttu-id="83cc8-101">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="83cc8-101">Get-AzKeyVaultKey</span></span>

## <span data-ttu-id="83cc8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="83cc8-102">SYNOPSIS</span></span>
<span data-ttu-id="83cc8-103">取得金鑰保存庫金鑰。</span><span class="sxs-lookup"><span data-stu-id="83cc8-103">Gets Key Vault keys.</span></span>

## <span data-ttu-id="83cc8-104">句法</span><span class="sxs-lookup"><span data-stu-id="83cc8-104">SYNTAX</span></span>

### <span data-ttu-id="83cc8-105">ByVaultName (預設) </span><span class="sxs-lookup"><span data-stu-id="83cc8-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83cc8-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="83cc8-106">ByKeyName</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83cc8-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="83cc8-107">ByKeyVersions</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83cc8-108">HsmByKeyName</span><span class="sxs-lookup"><span data-stu-id="83cc8-108">HsmByKeyName</span></span>
```
Get-AzKeyVaultKey -HsmName <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83cc8-109">HsmByVaultName</span><span class="sxs-lookup"><span data-stu-id="83cc8-109">HsmByVaultName</span></span>
```
Get-AzKeyVaultKey -HsmName <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83cc8-110">HsmByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="83cc8-110">HsmByKeyVersions</span></span>
```
Get-AzKeyVaultKey -HsmName <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83cc8-111">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="83cc8-111">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83cc8-112">ByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="83cc8-112">ByInputObjectKeyName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83cc8-113">ByInputObjectKeyVersions</span><span class="sxs-lookup"><span data-stu-id="83cc8-113">ByInputObjectKeyVersions</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83cc8-114">HsmByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="83cc8-114">HsmByInputObjectVaultName</span></span>
```
Get-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83cc8-115">HsmByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="83cc8-115">HsmByInputObjectKeyName</span></span>
```
Get-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83cc8-116">HsmByInputObjectKeyVersions</span><span class="sxs-lookup"><span data-stu-id="83cc8-116">HsmByInputObjectKeyVersions</span></span>
```
Get-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83cc8-117">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="83cc8-117">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83cc8-118">ByResourceIdKeyName</span><span class="sxs-lookup"><span data-stu-id="83cc8-118">ByResourceIdKeyName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83cc8-119">ByResourceIdKeyVersions</span><span class="sxs-lookup"><span data-stu-id="83cc8-119">ByResourceIdKeyVersions</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83cc8-120">HsmByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="83cc8-120">HsmByResourceIdVaultName</span></span>
```
Get-AzKeyVaultKey -HsmResourceId <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83cc8-121">HsmByResourceIdKeyName</span><span class="sxs-lookup"><span data-stu-id="83cc8-121">HsmByResourceIdKeyName</span></span>
```
Get-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83cc8-122">HsmByResourceIdKeyVersions</span><span class="sxs-lookup"><span data-stu-id="83cc8-122">HsmByResourceIdKeyVersions</span></span>
```
Get-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83cc8-123">說明</span><span class="sxs-lookup"><span data-stu-id="83cc8-123">DESCRIPTION</span></span>
<span data-ttu-id="83cc8-124">**AzKeyVaultKey** Cmdlet 會取得 Azure 金鑰保存庫金鑰。</span><span class="sxs-lookup"><span data-stu-id="83cc8-124">The **Get-AzKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="83cc8-125">這個 Cmdlet 會取得特定的 **KeyVault KeyBundle** 或主要保存庫或依據版本中所有 **KeyBundle** 物件的清單。</span><span class="sxs-lookup"><span data-stu-id="83cc8-125">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="83cc8-126">示例</span><span class="sxs-lookup"><span data-stu-id="83cc8-126">EXAMPLES</span></span>

### <span data-ttu-id="83cc8-127">範例1：取得金鑰保存庫中的所有按鍵</span><span class="sxs-lookup"><span data-stu-id="83cc8-127">Example 1: Get all the keys in a key vault</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso'

Vault Name     : contoso
Name           : test1
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test1
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :

Vault Name     : contoso
Name           : test2
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test2
Enabled        : True
Expires        : 11/24/2018 6:09:44 PM
Not Before     : 5/24/2018 5:59:44 PM
Created        : 5/24/2018 6:09:44 PM
Updated        : 5/24/2018 6:09:44 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="83cc8-128">這個命令會取得名為 Contoso 的主要電子倉庫中的所有金鑰。</span><span class="sxs-lookup"><span data-stu-id="83cc8-128">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="83cc8-129">範例2：取得目前的金鑰版本</span><span class="sxs-lookup"><span data-stu-id="83cc8-129">Example 2: Get the current version of a key</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test1'

Vault Name     : contoso
Name           : test1
Version        : 7fe415d5518240c1a6fce89986b8d334
Id             : https://contoso.vault.azure.net:443/keys/test1/7fe415d5518240c1a6fce89986b8d334
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="83cc8-130">這個命令會取得名為 Contoso 之金鑰保存庫中名為 test1 的目前版本的金鑰。</span><span class="sxs-lookup"><span data-stu-id="83cc8-130">This command gets the current version of the key named test1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="83cc8-131">範例3：取得金鑰的所有版本</span><span class="sxs-lookup"><span data-stu-id="83cc8-131">Example 3: Get all versions of a key</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test1' -IncludeVersions

Vault Name     : contoso
Name           : test1
Version        : 7fe415d5518240c1a6fce89986b8d334
Id             : https://contoso.vault.azure.net:443/keys/test1/7fe415d5518240c1a6fce89986b8d334
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :

Vault Name     : contoso
Name           : test1
Version        : e4e95940e669407fbdb4298bc21a3e1d
Id             : https://contoso.vault.azure.net:443/keys/test1/e4e95940e669407fbdb4298bc21a3e1d
Enabled        : False
Expires        : 11/24/2018 6:08:08 PM
Not Before     : 5/24/2018 5:58:08 PM
Created        : 5/24/2018 6:08:08 PM
Updated        : 5/24/2018 6:08:08 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="83cc8-132">這個命令會取得所有版本在名為 Contoso 的主要保存庫中名為 ITPfx 的金鑰。</span><span class="sxs-lookup"><span data-stu-id="83cc8-132">This command gets all versions the key named ITPfx in the key vault named Contoso.</span></span>

### <span data-ttu-id="83cc8-133">範例4：取得特定的金鑰版本</span><span class="sxs-lookup"><span data-stu-id="83cc8-133">Example 4: Get a specific version of a key</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test1' -Version 'e4e95940e669407fbdb4298bc21a3e1d'

Vault Name     : contoso
Name           : test1
Version        : e4e95940e669407fbdb4298bc21a3e1d
Id             : https://contoso.vault.azure.net:443/keys/test1/e4e95940e669407fbdb4298bc21a3e1d
Enabled        : False
Expires        : 11/24/2018 6:08:08 PM
Not Before     : 5/24/2018 5:58:08 PM
Created        : 5/24/2018 6:08:08 PM
Updated        : 5/24/2018 6:08:08 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="83cc8-134">這個命令會在名為 Contoso 的主要保存庫中，取得名為 test1 的特定金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="83cc8-134">This command gets a specific version of the key named test1 in the key vault named Contoso.</span></span>
<span data-ttu-id="83cc8-135">執行此命令之後，您可以流覽 $Key 物件來檢查索引鍵的各種屬性。</span><span class="sxs-lookup"><span data-stu-id="83cc8-135">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="83cc8-136">範例5：取得已刪除但未針對此金鑰保存庫清除的所有按鍵</span><span class="sxs-lookup"><span data-stu-id="83cc8-136">Example 5: Get all the keys that have been deleted but not purged for this key vault</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -InRemovedState

Vault Name           : contoso
Name                 : test3
Id                   : https://contoso.vault.azure.net:443/keys/test3
Deleted Date         : 5/24/2018 8:32:42 PM
Scheduled Purge Date : 8/22/2018 8:32:42 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 5/24/2018 8:32:27 PM
Updated              : 5/24/2018 8:32:27 PM
Purge Disabled       : False
Tags                 :
```

<span data-ttu-id="83cc8-137">這個命令會在名為 Contoso 的金鑰保存庫中，取得先前已刪除但尚未清除的所有索引鍵。</span><span class="sxs-lookup"><span data-stu-id="83cc8-137">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="83cc8-138">範例6：取得已刪除但未針對此金鑰保存庫清除的金鑰 ITPfx。</span><span class="sxs-lookup"><span data-stu-id="83cc8-138">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test3' -InRemovedState

Vault Name           : contoso
Name                 : test3
Id                   : https://contoso.vault.azure.net:443/keys/test3/1af807cc331a49d0b52b7c75e1b2366e
Deleted Date         : 5/24/2018 8:32:42 PM
Scheduled Purge Date : 8/22/2018 8:32:42 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 5/24/2018 8:32:27 PM
Updated              : 5/24/2018 8:32:27 PM
Purge Disabled       : False
Tags                 :
```

<span data-ttu-id="83cc8-139">這個命令會在名為 Contoso 的金鑰保存庫中，取得先前已刪除但尚未清除的金鑰 test3。</span><span class="sxs-lookup"><span data-stu-id="83cc8-139">This command gets the key test3 that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="83cc8-140">這個命令會傳回中繼資料，例如刪除日期，以及此刪除金鑰的排程清除日期。</span><span class="sxs-lookup"><span data-stu-id="83cc8-140">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

### <span data-ttu-id="83cc8-141">範例7：使用篩選取得金鑰保存庫中的所有金鑰</span><span class="sxs-lookup"><span data-stu-id="83cc8-141">Example 7: Get all the keys in a key vault using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName "test*"

Vault Name     : contoso
Name           : test1
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test1
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :

Vault Name     : contoso
Name           : test2
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test2
Enabled        : True
Expires        : 11/24/2018 6:09:44 PM
Not Before     : 5/24/2018 5:59:44 PM
Created        : 5/24/2018 6:09:44 PM
Updated        : 5/24/2018 6:09:44 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="83cc8-142">這個命令會取得名為 Contoso 的主要電子倉庫中，以「test」開頭的所有索引鍵。</span><span class="sxs-lookup"><span data-stu-id="83cc8-142">This command gets all the keys in the key vault named Contoso that start with "test".</span></span>

### <span data-ttu-id="83cc8-143">範例8：下載公開金鑰做為 pem 檔案</span><span class="sxs-lookup"><span data-stu-id="83cc8-143">Example 8: Download a public key as a .pem file</span></span>

```powershell
PS C:\> $path = "D:\public.pem"
PS C:\> Get-AzKeyVaultKey -VaultName $vaultName -KeyName $keyName -OutFile $path
```

<span data-ttu-id="83cc8-144">您可以透過指定參數來下載 RSA 金鑰的公開金鑰 `-OutFile` 。</span><span class="sxs-lookup"><span data-stu-id="83cc8-144">You can download the public key of a RSA key by specifying the `-OutFile` parameter.</span></span>
<span data-ttu-id="83cc8-145">這是將受 HSM 保護的金鑰匯入 Azure 金鑰保存庫的一個步驟。</span><span class="sxs-lookup"><span data-stu-id="83cc8-145">This is one step of importing HSM-protected keys to Azure Key Vault.</span></span> <span data-ttu-id="83cc8-146">請參閱 https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span><span class="sxs-lookup"><span data-stu-id="83cc8-146">See https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span></span>

## <span data-ttu-id="83cc8-147">參數</span><span class="sxs-lookup"><span data-stu-id="83cc8-147">PARAMETERS</span></span>

### <span data-ttu-id="83cc8-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83cc8-148">-DefaultProfile</span></span>
<span data-ttu-id="83cc8-149">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="83cc8-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83cc8-150">-HsmName</span><span class="sxs-lookup"><span data-stu-id="83cc8-150">-HsmName</span></span>
<span data-ttu-id="83cc8-151">HSM 名稱。</span><span class="sxs-lookup"><span data-stu-id="83cc8-151">HSM name.</span></span> <span data-ttu-id="83cc8-152">Cmdlet 根據名稱和目前所選的環境來構造受管理的 HSM 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="83cc8-152">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByKeyName, HsmByVaultName, HsmByKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83cc8-153">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="83cc8-153">-HsmObject</span></span>
<span data-ttu-id="83cc8-154">HSM 物件。</span><span class="sxs-lookup"><span data-stu-id="83cc8-154">HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: HsmByInputObjectVaultName, HsmByInputObjectKeyName, HsmByInputObjectKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83cc8-155">-HsmResourceId</span><span class="sxs-lookup"><span data-stu-id="83cc8-155">-HsmResourceId</span></span>
<span data-ttu-id="83cc8-156">HSM 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="83cc8-156">HSM Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByResourceIdVaultName, HsmByResourceIdKeyName, HsmByResourceIdKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83cc8-157">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="83cc8-157">-IncludeVersions</span></span>
<span data-ttu-id="83cc8-158">表示此 Cmdlet 會取得所有版本的金鑰。</span><span class="sxs-lookup"><span data-stu-id="83cc8-158">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="83cc8-159">索引鍵的目前版本是清單中的第一個版本。</span><span class="sxs-lookup"><span data-stu-id="83cc8-159">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="83cc8-160">如果您指定此參數，您也必須指定 *Name* 及 *VaultName* 參數。</span><span class="sxs-lookup"><span data-stu-id="83cc8-160">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="83cc8-161">如果您沒有指定 *IncludeVersions* 參數，這個 Cmdlet 會取得具有指定 *名稱* 的目前金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="83cc8-161">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByKeyVersions, HsmByKeyVersions, ByInputObjectKeyVersions, HsmByInputObjectKeyVersions, ByResourceIdKeyVersions, HsmByResourceIdKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83cc8-162">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83cc8-162">-InputObject</span></span>
<span data-ttu-id="83cc8-163">KeyVault 物件。</span><span class="sxs-lookup"><span data-stu-id="83cc8-163">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObjectVaultName, ByInputObjectKeyName, ByInputObjectKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83cc8-164">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="83cc8-164">-InRemovedState</span></span>
<span data-ttu-id="83cc8-165">指定是否要在輸出中顯示先前刪除的索引鍵</span><span class="sxs-lookup"><span data-stu-id="83cc8-165">Specifies whether to show the previously deleted keys in the output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByVaultName, HsmByVaultName, ByInputObjectVaultName, HsmByInputObjectVaultName, ByResourceIdVaultName, HsmByResourceIdVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83cc8-166">-名稱</span><span class="sxs-lookup"><span data-stu-id="83cc8-166">-Name</span></span>
<span data-ttu-id="83cc8-167">指定要取得的金鑰捆綁的名稱。</span><span class="sxs-lookup"><span data-stu-id="83cc8-167">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, HsmByVaultName, ByInputObjectVaultName, HsmByInputObjectVaultName, ByResourceIdVaultName, HsmByResourceIdVaultName
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByKeyVersions, HsmByKeyName, HsmByKeyVersions, ByInputObjectKeyName, ByInputObjectKeyVersions, HsmByInputObjectKeyName, HsmByInputObjectKeyVersions, ByResourceIdKeyName, ByResourceIdKeyVersions, HsmByResourceIdKeyName, HsmByResourceIdKeyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="83cc8-168">-OutFile</span><span class="sxs-lookup"><span data-stu-id="83cc8-168">-OutFile</span></span>
<span data-ttu-id="83cc8-169">指定此 Cmdlet 儲存金鑰的輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="83cc8-169">Specifies the output file for which this cmdlet saves the key.</span></span> <span data-ttu-id="83cc8-170">公開金鑰預設會以 PEM 格式儲存。</span><span class="sxs-lookup"><span data-stu-id="83cc8-170">The public key is saved in PEM format by default.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83cc8-171">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="83cc8-171">-ResourceId</span></span>
<span data-ttu-id="83cc8-172">KeyVault 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="83cc8-172">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdVaultName, ByResourceIdKeyName, ByResourceIdKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83cc8-173">-VaultName</span><span class="sxs-lookup"><span data-stu-id="83cc8-173">-VaultName</span></span>
<span data-ttu-id="83cc8-174">指定由此 Cmdlet 取得金鑰之金鑰電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="83cc8-174">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="83cc8-175">這個 Cmdlet 會根據此參數指定的名稱和您所選的環境，來構造金鑰 vault (FQDN) 的完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="83cc8-175">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByKeyName, ByKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83cc8-176">-版本</span><span class="sxs-lookup"><span data-stu-id="83cc8-176">-Version</span></span>
<span data-ttu-id="83cc8-177">指定金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="83cc8-177">Specifies the key version.</span></span>
<span data-ttu-id="83cc8-178">這個 Cmdlet 根據金鑰保存庫名稱、您目前選取的環境、金鑰名稱及金鑰版本來構造金鑰的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="83cc8-178">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName, HsmByKeyName, ByInputObjectKeyName, HsmByInputObjectKeyName, ByResourceIdKeyName, HsmByResourceIdKeyName
Aliases: KeyVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83cc8-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83cc8-179">CommonParameters</span></span>
<span data-ttu-id="83cc8-180">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="83cc8-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83cc8-181">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="83cc8-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83cc8-182">輸入</span><span class="sxs-lookup"><span data-stu-id="83cc8-182">INPUTS</span></span>

### <span data-ttu-id="83cc8-183">PSKeyVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="83cc8-183">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="83cc8-184">System.object</span><span class="sxs-lookup"><span data-stu-id="83cc8-184">System.String</span></span>

## <span data-ttu-id="83cc8-185">輸出</span><span class="sxs-lookup"><span data-stu-id="83cc8-185">OUTPUTS</span></span>

### <span data-ttu-id="83cc8-186">PSKeyVaultKeyIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="83cc8-186">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="83cc8-187">PSKeyVaultKey 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="83cc8-187">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

### <span data-ttu-id="83cc8-188">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="83cc8-188">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="83cc8-189">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="83cc8-189">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="83cc8-190">筆記</span><span class="sxs-lookup"><span data-stu-id="83cc8-190">NOTES</span></span>

## <span data-ttu-id="83cc8-191">相關連結</span><span class="sxs-lookup"><span data-stu-id="83cc8-191">RELATED LINKS</span></span>

[<span data-ttu-id="83cc8-192">附加 AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="83cc8-192">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="83cc8-193">移除-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="83cc8-193">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="83cc8-194">復原-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="83cc8-194">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

[<span data-ttu-id="83cc8-195">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="83cc8-195">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

