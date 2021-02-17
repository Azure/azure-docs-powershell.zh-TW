---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
ms.openlocfilehash: e0601285bf2adc7204cd5a946e07d032579e080b
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404712"
---
# <span data-ttu-id="98697-101">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="98697-101">Get-AzKeyVaultKey</span></span>

## <span data-ttu-id="98697-102">簡介</span><span class="sxs-lookup"><span data-stu-id="98697-102">SYNOPSIS</span></span>
<span data-ttu-id="98697-103">獲得金鑰庫金鑰。</span><span class="sxs-lookup"><span data-stu-id="98697-103">Gets Key Vault keys.</span></span>

## <span data-ttu-id="98697-104">語法</span><span class="sxs-lookup"><span data-stu-id="98697-104">SYNTAX</span></span>

### <span data-ttu-id="98697-105">ByVaultName (預設) </span><span class="sxs-lookup"><span data-stu-id="98697-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98697-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="98697-106">ByKeyName</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98697-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="98697-107">ByKeyVersions</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98697-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="98697-108">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98697-109">ByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="98697-109">ByInputObjectKeyName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98697-110">ByInputObjectKeyVersions</span><span class="sxs-lookup"><span data-stu-id="98697-110">ByInputObjectKeyVersions</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98697-111">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="98697-111">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98697-112">ByResourceIdKeyName</span><span class="sxs-lookup"><span data-stu-id="98697-112">ByResourceIdKeyName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98697-113">ByResourceIdKeyVersions</span><span class="sxs-lookup"><span data-stu-id="98697-113">ByResourceIdKeyVersions</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98697-114">描述</span><span class="sxs-lookup"><span data-stu-id="98697-114">DESCRIPTION</span></span>
<span data-ttu-id="98697-115">**Get-AzKeyVaultKey** Cmdlet 會取得 Azure 金鑰庫金鑰。</span><span class="sxs-lookup"><span data-stu-id="98697-115">The **Get-AzKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="98697-116">此 Cmdlet 會獲得特定的 **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** 或金鑰庫或版本的所有 **KeyBundle** 物件清單。</span><span class="sxs-lookup"><span data-stu-id="98697-116">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="98697-117">例子</span><span class="sxs-lookup"><span data-stu-id="98697-117">EXAMPLES</span></span>

### <span data-ttu-id="98697-118">範例 1：取得金鑰庫中的所有金鑰</span><span class="sxs-lookup"><span data-stu-id="98697-118">Example 1: Get all the keys in a key vault</span></span>
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

<span data-ttu-id="98697-119">此命令會獲得名稱為 Contoso 之金鑰庫中的所有金鑰。</span><span class="sxs-lookup"><span data-stu-id="98697-119">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="98697-120">範例 2：取得金鑰的目前版本</span><span class="sxs-lookup"><span data-stu-id="98697-120">Example 2: Get the current version of a key</span></span>
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

<span data-ttu-id="98697-121">此命令會獲得名稱為 Contoso 之金鑰庫中名為 test1 的金鑰的目前版本。</span><span class="sxs-lookup"><span data-stu-id="98697-121">This command gets the current version of the key named test1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="98697-122">範例 3：取得金鑰的所有版本</span><span class="sxs-lookup"><span data-stu-id="98697-122">Example 3: Get all versions of a key</span></span>
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

<span data-ttu-id="98697-123">此命令會獲得名稱為 Contoso 之金鑰庫中名為 ITPfx 的所有版本。</span><span class="sxs-lookup"><span data-stu-id="98697-123">This command gets all versions the key named ITPfx in the key vaultnamed Contoso.</span></span>

### <span data-ttu-id="98697-124">範例 4：取得特定版本的金鑰</span><span class="sxs-lookup"><span data-stu-id="98697-124">Example 4: Get a specific version of a key</span></span>
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

<span data-ttu-id="98697-125">此命令在名為 Contoso 的金鑰庫中，會獲得名為 test1 的特定金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="98697-125">This command gets a specific version of the key named test1 in the key vault named Contoso.</span></span>
<span data-ttu-id="98697-126">執行此命令之後，您可以流覽物件以檢查$Key屬性。</span><span class="sxs-lookup"><span data-stu-id="98697-126">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="98697-127">範例 5：取得此金鑰庫的所有已刪除但並未清除的金鑰。</span><span class="sxs-lookup"><span data-stu-id="98697-127">Example 5: Get all the keys that have been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="98697-128">此命令會獲得先前在名稱為 Contoso 的金鑰庫中刪除但並未清除的所有金鑰。</span><span class="sxs-lookup"><span data-stu-id="98697-128">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="98697-129">範例 6：針對此金鑰庫，獲得已刪除但並未清除的金鑰 ITPfx。</span><span class="sxs-lookup"><span data-stu-id="98697-129">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="98697-130">此命令會獲得先前在名稱為 Contoso 的金鑰庫中刪除但並未清除的金鑰 test3。</span><span class="sxs-lookup"><span data-stu-id="98697-130">This command gets the key test3 that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="98697-131">此命令會返回中繼資料，例如刪除日期，以及此刪除金鑰的排程清除日期。</span><span class="sxs-lookup"><span data-stu-id="98697-131">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

### <span data-ttu-id="98697-132">範例 7：使用篩選功能取得金鑰庫中的所有金鑰</span><span class="sxs-lookup"><span data-stu-id="98697-132">Example 7: Get all the keys in a key vault using filtering</span></span>
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

<span data-ttu-id="98697-133">此命令會獲得名稱為 Contoso 的金鑰庫中以「測試」做為開始的所有金鑰。</span><span class="sxs-lookup"><span data-stu-id="98697-133">This command gets all the keys in the key vault named Contoso that start with "test".</span></span>

### <span data-ttu-id="98697-134">範例 8：將公開金鑰下載為 .pem 檔案</span><span class="sxs-lookup"><span data-stu-id="98697-134">Example 8: Download a public key as a .pem file</span></span>

```powershell
PS C:\> $path = "D:\public.pem"
PS C:\> Get-AzKeyVaultKey -VaultName $vaultName -KeyName $keyName -OutFile $path
```

<span data-ttu-id="98697-135">您可以指定參數來下載 RSA 金鑰的 `-OutFile` 公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="98697-135">You can download the public key of a RSA key by specifying the `-OutFile` parameter.</span></span>
<span data-ttu-id="98697-136">這是將受 HSM 保護的金鑰導入 Azure 金鑰庫的步驟之一。</span><span class="sxs-lookup"><span data-stu-id="98697-136">This is one step of importing HSM-protected keys to Azure Key Vault.</span></span> <span data-ttu-id="98697-137">看到 https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span><span class="sxs-lookup"><span data-stu-id="98697-137">See https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span></span>

## <span data-ttu-id="98697-138">參數</span><span class="sxs-lookup"><span data-stu-id="98697-138">PARAMETERS</span></span>

### <span data-ttu-id="98697-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98697-139">-DefaultProfile</span></span>
<span data-ttu-id="98697-140">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="98697-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98697-141">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="98697-141">-IncludeVersions</span></span>
<span data-ttu-id="98697-142">表示此 Cmdlet 會獲得所有版本的金鑰。</span><span class="sxs-lookup"><span data-stu-id="98697-142">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="98697-143">目前版本的金鑰是清單中的第一個版本。</span><span class="sxs-lookup"><span data-stu-id="98697-143">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="98697-144">如果您指定此參數，您也必須指定 *Name* 和 *VaultName* 參數。</span><span class="sxs-lookup"><span data-stu-id="98697-144">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="98697-145">如果您未指定 *IncludeVersions* 參數，此 Cmdlet 會以指定的名稱獲得目前版本的 *金鑰*。</span><span class="sxs-lookup"><span data-stu-id="98697-145">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByKeyVersions, ByInputObjectKeyVersions, ByResourceIdKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98697-146">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98697-146">-InputObject</span></span>
<span data-ttu-id="98697-147">KeyVault 物件。</span><span class="sxs-lookup"><span data-stu-id="98697-147">KeyVault object.</span></span>

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

### <span data-ttu-id="98697-148">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="98697-148">-InRemovedState</span></span>
<span data-ttu-id="98697-149">指定是否要在輸出中顯示先前刪除的按鍵</span><span class="sxs-lookup"><span data-stu-id="98697-149">Specifies whether to show the previously deleted keys in the output</span></span>

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

### <span data-ttu-id="98697-150">-名稱</span><span class="sxs-lookup"><span data-stu-id="98697-150">-Name</span></span>
<span data-ttu-id="98697-151">指定要取得之金鑰組合的名稱。</span><span class="sxs-lookup"><span data-stu-id="98697-151">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByKeyVersions, ByInputObjectKeyName, ByInputObjectKeyVersions, ByResourceIdKeyName, ByResourceIdKeyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98697-152">-OutFile</span><span class="sxs-lookup"><span data-stu-id="98697-152">-OutFile</span></span>
<span data-ttu-id="98697-153">指定此 Cmdlet 會針對該金鑰進行保存的輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="98697-153">Specifies the output file for which this cmdlet saves the key.</span></span> <span data-ttu-id="98697-154">根據預設，公用鍵會以 PEM 格式儲存。</span><span class="sxs-lookup"><span data-stu-id="98697-154">The public key is saved in PEM format by default.</span></span>

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

### <span data-ttu-id="98697-155">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98697-155">-ResourceId</span></span>
<span data-ttu-id="98697-156">KeyVault 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="98697-156">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="98697-157">-VaultName</span><span class="sxs-lookup"><span data-stu-id="98697-157">-VaultName</span></span>
<span data-ttu-id="98697-158">指定此 Cmdlet 從其中獲得金鑰的金鑰庫名稱。</span><span class="sxs-lookup"><span data-stu-id="98697-158">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="98697-159">此 Cmdlet 會根據此參數指定的名稱 (所選環境，建構金鑰庫的 FQDN) 完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="98697-159">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

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

### <span data-ttu-id="98697-160">-版本</span><span class="sxs-lookup"><span data-stu-id="98697-160">-Version</span></span>
<span data-ttu-id="98697-161">指定金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="98697-161">Specifies the key version.</span></span>
<span data-ttu-id="98697-162">此 Cmdlet 會根據金鑰庫名稱、您目前選取的環境、金鑰名稱和金鑰版本來建構金鑰的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="98697-162">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByInputObjectKeyName, ByResourceIdKeyName
Aliases: KeyVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98697-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98697-163">CommonParameters</span></span>
<span data-ttu-id="98697-164">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="98697-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98697-165">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="98697-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98697-166">輸入</span><span class="sxs-lookup"><span data-stu-id="98697-166">INPUTS</span></span>

### <span data-ttu-id="98697-167">Microsoft.Azure.Commands.KeyVault.models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="98697-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="98697-168">System.String</span><span class="sxs-lookup"><span data-stu-id="98697-168">System.String</span></span>

## <span data-ttu-id="98697-169">輸出</span><span class="sxs-lookup"><span data-stu-id="98697-169">OUTPUTS</span></span>

### <span data-ttu-id="98697-170">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="98697-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="98697-171">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="98697-171">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

### <span data-ttu-id="98697-172">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="98697-172">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="98697-173">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="98697-173">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="98697-174">筆記</span><span class="sxs-lookup"><span data-stu-id="98697-174">NOTES</span></span>

## <span data-ttu-id="98697-175">相關連結</span><span class="sxs-lookup"><span data-stu-id="98697-175">RELATED LINKS</span></span>

[<span data-ttu-id="98697-176">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="98697-176">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="98697-177">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="98697-177">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="98697-178">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="98697-178">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)


