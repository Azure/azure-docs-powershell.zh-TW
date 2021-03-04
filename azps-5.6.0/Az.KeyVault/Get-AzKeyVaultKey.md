---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
ms.openlocfilehash: 81276c0896d6cb6685d3ce3ee71bb72cb39b690a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902878"
---
# <span data-ttu-id="85837-101">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="85837-101">Get-AzKeyVaultKey</span></span>

## <span data-ttu-id="85837-102">簡介</span><span class="sxs-lookup"><span data-stu-id="85837-102">SYNOPSIS</span></span>
<span data-ttu-id="85837-103">獲得金鑰庫金鑰。</span><span class="sxs-lookup"><span data-stu-id="85837-103">Gets Key Vault keys.</span></span>

## <span data-ttu-id="85837-104">語法</span><span class="sxs-lookup"><span data-stu-id="85837-104">SYNTAX</span></span>

### <span data-ttu-id="85837-105">ByVaultName (預設) </span><span class="sxs-lookup"><span data-stu-id="85837-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85837-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="85837-106">ByKeyName</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85837-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="85837-107">ByKeyVersions</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85837-108">HsmByKeyName</span><span class="sxs-lookup"><span data-stu-id="85837-108">HsmByKeyName</span></span>
```
Get-AzKeyVaultKey -HsmName <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85837-109">HsmByVaultName</span><span class="sxs-lookup"><span data-stu-id="85837-109">HsmByVaultName</span></span>
```
Get-AzKeyVaultKey -HsmName <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85837-110">HsmByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="85837-110">HsmByKeyVersions</span></span>
```
Get-AzKeyVaultKey -HsmName <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85837-111">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="85837-111">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85837-112">ByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="85837-112">ByInputObjectKeyName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85837-113">ByInputObjectKeyVersions</span><span class="sxs-lookup"><span data-stu-id="85837-113">ByInputObjectKeyVersions</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85837-114">HsmByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="85837-114">HsmByInputObjectVaultName</span></span>
```
Get-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85837-115">HsmByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="85837-115">HsmByInputObjectKeyName</span></span>
```
Get-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85837-116">HsmByInputObjectKeyVersions</span><span class="sxs-lookup"><span data-stu-id="85837-116">HsmByInputObjectKeyVersions</span></span>
```
Get-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85837-117">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="85837-117">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultKey -ResourceId <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85837-118">ByResourceIdKeyName</span><span class="sxs-lookup"><span data-stu-id="85837-118">ByResourceIdKeyName</span></span>
```
Get-AzKeyVaultKey -ResourceId <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85837-119">ByResourceIdKeyVersions</span><span class="sxs-lookup"><span data-stu-id="85837-119">ByResourceIdKeyVersions</span></span>
```
Get-AzKeyVaultKey -ResourceId <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85837-120">HsmByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="85837-120">HsmByResourceIdVaultName</span></span>
```
Get-AzKeyVaultKey -HsmResourceId <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85837-121">HsmByResourceIdKeyName</span><span class="sxs-lookup"><span data-stu-id="85837-121">HsmByResourceIdKeyName</span></span>
```
Get-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85837-122">HsmByResourceIdKeyVersions</span><span class="sxs-lookup"><span data-stu-id="85837-122">HsmByResourceIdKeyVersions</span></span>
```
Get-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85837-123">描述</span><span class="sxs-lookup"><span data-stu-id="85837-123">DESCRIPTION</span></span>
<span data-ttu-id="85837-124">**Get-AzKeyVaultKey** Cmdlet 會取得 Azure 金鑰庫金鑰。</span><span class="sxs-lookup"><span data-stu-id="85837-124">The **Get-AzKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="85837-125">此 Cmdlet 會獲得特定的 **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** 或金鑰庫或版本中所有 **KeyBundle** 物件的清單。</span><span class="sxs-lookup"><span data-stu-id="85837-125">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="85837-126">例子</span><span class="sxs-lookup"><span data-stu-id="85837-126">EXAMPLES</span></span>

### <span data-ttu-id="85837-127">範例 1：取得金鑰庫中的所有金鑰</span><span class="sxs-lookup"><span data-stu-id="85837-127">Example 1: Get all the keys in a key vault</span></span>
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

<span data-ttu-id="85837-128">此命令會獲得名稱為 Contoso 之金鑰庫中的所有金鑰。</span><span class="sxs-lookup"><span data-stu-id="85837-128">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="85837-129">範例 2：取得金鑰的目前版本</span><span class="sxs-lookup"><span data-stu-id="85837-129">Example 2: Get the current version of a key</span></span>
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

<span data-ttu-id="85837-130">此命令在名稱為 Contoso 的金鑰庫中，會獲得名為 test1 的金鑰的目前版本。</span><span class="sxs-lookup"><span data-stu-id="85837-130">This command gets the current version of the key named test1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="85837-131">範例 3：取得金鑰的所有版本</span><span class="sxs-lookup"><span data-stu-id="85837-131">Example 3: Get all versions of a key</span></span>
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

<span data-ttu-id="85837-132">此命令會獲得名稱為 Contoso 之金鑰庫中名為 ITPfx 的所有版本。</span><span class="sxs-lookup"><span data-stu-id="85837-132">This command gets all versions the key named ITPfx in the key vault named Contoso.</span></span>

### <span data-ttu-id="85837-133">範例 4：取得金鑰的特定版本</span><span class="sxs-lookup"><span data-stu-id="85837-133">Example 4: Get a specific version of a key</span></span>
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

<span data-ttu-id="85837-134">此命令在名為 Contoso 的金鑰庫中，會獲得名為 test1 的特定金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="85837-134">This command gets a specific version of the key named test1 in the key vault named Contoso.</span></span>
<span data-ttu-id="85837-135">執行此命令之後，您可以流覽物件以檢查$Key屬性。</span><span class="sxs-lookup"><span data-stu-id="85837-135">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="85837-136">範例 5：取得此金鑰庫的所有已刪除但並未清除的金鑰</span><span class="sxs-lookup"><span data-stu-id="85837-136">Example 5: Get all the keys that have been deleted but not purged for this key vault</span></span>
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

<span data-ttu-id="85837-137">此命令會獲得先前在名稱為 Contoso 的金鑰庫中刪除但並未清除的所有金鑰。</span><span class="sxs-lookup"><span data-stu-id="85837-137">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="85837-138">範例 6：針對此金鑰庫，獲得已被刪除但並未清除的金鑰 ITPfx。</span><span class="sxs-lookup"><span data-stu-id="85837-138">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="85837-139">此命令會獲得先前在名稱為 Contoso 的金鑰庫中刪除但並未清除的金鑰 test3。</span><span class="sxs-lookup"><span data-stu-id="85837-139">This command gets the key test3 that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="85837-140">此命令會返回中繼資料，例如刪除日期，以及此刪除金鑰的排程清除日期。</span><span class="sxs-lookup"><span data-stu-id="85837-140">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

### <span data-ttu-id="85837-141">範例 7：使用篩選功能取得金鑰庫中的所有金鑰</span><span class="sxs-lookup"><span data-stu-id="85837-141">Example 7: Get all the keys in a key vault using filtering</span></span>
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

<span data-ttu-id="85837-142">此命令會獲得名稱為 Contoso 的金鑰庫中以「測試」做為開始的所有金鑰。</span><span class="sxs-lookup"><span data-stu-id="85837-142">This command gets all the keys in the key vault named Contoso that start with "test".</span></span>

### <span data-ttu-id="85837-143">範例 8：將公開金鑰下載為 .pem 檔案</span><span class="sxs-lookup"><span data-stu-id="85837-143">Example 8: Download a public key as a .pem file</span></span>

```powershell
PS C:\> $path = "D:\public.pem"
PS C:\> Get-AzKeyVaultKey -VaultName $vaultName -KeyName $keyName -OutFile $path
```

<span data-ttu-id="85837-144">您可以指定參數來下載 RSA 金鑰的 `-OutFile` 公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="85837-144">You can download the public key of a RSA key by specifying the `-OutFile` parameter.</span></span>
<span data-ttu-id="85837-145">這是將受 HSM 保護的金鑰導入 Azure 金鑰庫的其中一個步驟。</span><span class="sxs-lookup"><span data-stu-id="85837-145">This is one step of importing HSM-protected keys to Azure Key Vault.</span></span> <span data-ttu-id="85837-146">看到 https://docs.microsoft.com/azure/key-vault/keys/hsm-protected-keys</span><span class="sxs-lookup"><span data-stu-id="85837-146">See https://docs.microsoft.com/azure/key-vault/keys/hsm-protected-keys</span></span>

## <span data-ttu-id="85837-147">參數</span><span class="sxs-lookup"><span data-stu-id="85837-147">PARAMETERS</span></span>

### <span data-ttu-id="85837-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85837-148">-DefaultProfile</span></span>
<span data-ttu-id="85837-149">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="85837-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="85837-150">-HsmName</span><span class="sxs-lookup"><span data-stu-id="85837-150">-HsmName</span></span>
<span data-ttu-id="85837-151">HSM 名稱。</span><span class="sxs-lookup"><span data-stu-id="85837-151">HSM name.</span></span> <span data-ttu-id="85837-152">Cmdlet 會根據名稱和目前選取的環境，建構受管理 HSM 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="85837-152">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="85837-153">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="85837-153">-HsmObject</span></span>
<span data-ttu-id="85837-154">HSM 物件。</span><span class="sxs-lookup"><span data-stu-id="85837-154">HSM object.</span></span>

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

### <span data-ttu-id="85837-155">-HsmResourceId</span><span class="sxs-lookup"><span data-stu-id="85837-155">-HsmResourceId</span></span>
<span data-ttu-id="85837-156">HSM 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="85837-156">HSM Resource Id.</span></span>

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

### <span data-ttu-id="85837-157">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="85837-157">-IncludeVersions</span></span>
<span data-ttu-id="85837-158">表示此 Cmdlet 會獲得所有版本的金鑰。</span><span class="sxs-lookup"><span data-stu-id="85837-158">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="85837-159">目前版本的金鑰是清單中的第一個。</span><span class="sxs-lookup"><span data-stu-id="85837-159">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="85837-160">如果您指定此參數，您也必須指定 *Name* 和 *VaultName* 參數。</span><span class="sxs-lookup"><span data-stu-id="85837-160">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="85837-161">如果您未指定 *IncludeVersions* 參數，此 Cmdlet 會以指定的名稱獲得目前版本的 *金鑰*。</span><span class="sxs-lookup"><span data-stu-id="85837-161">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

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

### <span data-ttu-id="85837-162">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85837-162">-InputObject</span></span>
<span data-ttu-id="85837-163">KeyVault 物件。</span><span class="sxs-lookup"><span data-stu-id="85837-163">KeyVault object.</span></span>

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

### <span data-ttu-id="85837-164">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="85837-164">-InRemovedState</span></span>
<span data-ttu-id="85837-165">指定是否要在輸出中顯示先前刪除的按鍵</span><span class="sxs-lookup"><span data-stu-id="85837-165">Specifies whether to show the previously deleted keys in the output</span></span>

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

### <span data-ttu-id="85837-166">-名稱</span><span class="sxs-lookup"><span data-stu-id="85837-166">-Name</span></span>
<span data-ttu-id="85837-167">指定要取得之金鑰組合的名稱。</span><span class="sxs-lookup"><span data-stu-id="85837-167">Specifies the name of the key bundle to get.</span></span>

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

### <span data-ttu-id="85837-168">-OutFile</span><span class="sxs-lookup"><span data-stu-id="85837-168">-OutFile</span></span>
<span data-ttu-id="85837-169">指定此 Cmdlet 會針對該金鑰進行保存的輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="85837-169">Specifies the output file for which this cmdlet saves the key.</span></span> <span data-ttu-id="85837-170">根據預設，公用鍵會以 PEM 格式儲存。</span><span class="sxs-lookup"><span data-stu-id="85837-170">The public key is saved in PEM format by default.</span></span>

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

### <span data-ttu-id="85837-171">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85837-171">-ResourceId</span></span>
<span data-ttu-id="85837-172">KeyVault 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="85837-172">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdVaultName, ByResourceIdKeyName, ByResourceIdKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85837-173">-VaultName</span><span class="sxs-lookup"><span data-stu-id="85837-173">-VaultName</span></span>
<span data-ttu-id="85837-174">指定此 Cmdlet 從其中獲得金鑰的金鑰庫名稱。</span><span class="sxs-lookup"><span data-stu-id="85837-174">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="85837-175">此 Cmdlet 會根據此參數指定的名稱 (所選環境，建構金鑰庫的 FQDN) 完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="85837-175">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

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

### <span data-ttu-id="85837-176">-版本</span><span class="sxs-lookup"><span data-stu-id="85837-176">-Version</span></span>
<span data-ttu-id="85837-177">指定金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="85837-177">Specifies the key version.</span></span>
<span data-ttu-id="85837-178">此 Cmdlet 會根據金鑰庫名稱、您目前選取的環境、金鑰名稱和金鑰版本來建構金鑰的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="85837-178">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

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

### <span data-ttu-id="85837-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85837-179">CommonParameters</span></span>
<span data-ttu-id="85837-180">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="85837-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85837-181">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="85837-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85837-182">輸入</span><span class="sxs-lookup"><span data-stu-id="85837-182">INPUTS</span></span>

### <span data-ttu-id="85837-183">Microsoft.Azure.Commands.KeyVault.models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="85837-183">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="85837-184">System.String</span><span class="sxs-lookup"><span data-stu-id="85837-184">System.String</span></span>

## <span data-ttu-id="85837-185">輸出</span><span class="sxs-lookup"><span data-stu-id="85837-185">OUTPUTS</span></span>

### <span data-ttu-id="85837-186">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="85837-186">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="85837-187">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="85837-187">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

### <span data-ttu-id="85837-188">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="85837-188">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="85837-189">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="85837-189">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="85837-190">筆記</span><span class="sxs-lookup"><span data-stu-id="85837-190">NOTES</span></span>

## <span data-ttu-id="85837-191">相關連結</span><span class="sxs-lookup"><span data-stu-id="85837-191">RELATED LINKS</span></span>

[<span data-ttu-id="85837-192">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="85837-192">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="85837-193">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="85837-193">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="85837-194">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="85837-194">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

[<span data-ttu-id="85837-195">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="85837-195">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

