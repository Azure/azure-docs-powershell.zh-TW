---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
ms.openlocfilehash: a934b1d96b260a6615acfbe02b15c80e6d3bfae5
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411444"
---
# <span data-ttu-id="1932d-101">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1932d-101">Get-AzKeyVaultKey</span></span>

## <span data-ttu-id="1932d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1932d-102">SYNOPSIS</span></span>
<span data-ttu-id="1932d-103">獲得金鑰庫金鑰。</span><span class="sxs-lookup"><span data-stu-id="1932d-103">Gets Key Vault keys.</span></span>

## <span data-ttu-id="1932d-104">語法</span><span class="sxs-lookup"><span data-stu-id="1932d-104">SYNTAX</span></span>

### <span data-ttu-id="1932d-105">ByVaultName (預設) </span><span class="sxs-lookup"><span data-stu-id="1932d-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1932d-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="1932d-106">ByKeyName</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1932d-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="1932d-107">ByKeyVersions</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1932d-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="1932d-108">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1932d-109">ByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="1932d-109">ByInputObjectKeyName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1932d-110">ByInputObjectKeyVersions</span><span class="sxs-lookup"><span data-stu-id="1932d-110">ByInputObjectKeyVersions</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1932d-111">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="1932d-111">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1932d-112">ByResourceIdKeyName</span><span class="sxs-lookup"><span data-stu-id="1932d-112">ByResourceIdKeyName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1932d-113">ByResourceIdKeyVersions</span><span class="sxs-lookup"><span data-stu-id="1932d-113">ByResourceIdKeyVersions</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1932d-114">描述</span><span class="sxs-lookup"><span data-stu-id="1932d-114">DESCRIPTION</span></span>
<span data-ttu-id="1932d-115">**Get-AzKeyVaultKey** Cmdlet 會取得 Azure 金鑰庫金鑰。</span><span class="sxs-lookup"><span data-stu-id="1932d-115">The **Get-AzKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="1932d-116">此 Cmdlet 會獲得特定的 **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** 或金鑰庫或版本的所有 **KeyBundle** 物件清單。</span><span class="sxs-lookup"><span data-stu-id="1932d-116">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="1932d-117">例子</span><span class="sxs-lookup"><span data-stu-id="1932d-117">EXAMPLES</span></span>

### <span data-ttu-id="1932d-118">範例 1：取得金鑰庫中的所有金鑰</span><span class="sxs-lookup"><span data-stu-id="1932d-118">Example 1: Get all the keys in a key vault</span></span>
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

<span data-ttu-id="1932d-119">此命令會獲得名稱為 Contoso 之金鑰庫中的所有金鑰。</span><span class="sxs-lookup"><span data-stu-id="1932d-119">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="1932d-120">範例 2：取得金鑰的目前版本</span><span class="sxs-lookup"><span data-stu-id="1932d-120">Example 2: Get the current version of a key</span></span>
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

<span data-ttu-id="1932d-121">此命令會獲得名稱為 Contoso 之金鑰庫中名為 test1 的金鑰的目前版本。</span><span class="sxs-lookup"><span data-stu-id="1932d-121">This command gets the current version of the key named test1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="1932d-122">範例 3：取得金鑰的所有版本</span><span class="sxs-lookup"><span data-stu-id="1932d-122">Example 3: Get all versions of a key</span></span>
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

<span data-ttu-id="1932d-123">此命令會獲得名稱為 Contoso 之金鑰庫中名為 ITPfx 的所有版本。</span><span class="sxs-lookup"><span data-stu-id="1932d-123">This command gets all versions the key named ITPfx in the key vaultnamed Contoso.</span></span>

### <span data-ttu-id="1932d-124">範例 4：取得金鑰的特定版本</span><span class="sxs-lookup"><span data-stu-id="1932d-124">Example 4: Get a specific version of a key</span></span>
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

<span data-ttu-id="1932d-125">此命令在名為 Contoso 的金鑰庫中，會獲得名為 test1 的特定金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="1932d-125">This command gets a specific version of the key named test1 in the key vault named Contoso.</span></span>
<span data-ttu-id="1932d-126">執行此命令之後，您可以流覽物件以檢查$Key屬性。</span><span class="sxs-lookup"><span data-stu-id="1932d-126">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="1932d-127">範例 5：取得此金鑰庫的所有已刪除但並未清除的金鑰。</span><span class="sxs-lookup"><span data-stu-id="1932d-127">Example 5: Get all the keys that have been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="1932d-128">此命令會獲得先前在名稱為 Contoso 的金鑰庫中刪除但並未清除的所有金鑰。</span><span class="sxs-lookup"><span data-stu-id="1932d-128">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="1932d-129">範例 6：針對此金鑰庫，獲得已刪除但並未清除的金鑰 ITPfx。</span><span class="sxs-lookup"><span data-stu-id="1932d-129">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="1932d-130">此命令會獲得先前在名稱為 Contoso 的金鑰庫中刪除但並未清除的金鑰 test3。</span><span class="sxs-lookup"><span data-stu-id="1932d-130">This command gets the key test3 that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="1932d-131">此命令會返回中繼資料，例如刪除日期，以及此刪除金鑰的排程清除日期。</span><span class="sxs-lookup"><span data-stu-id="1932d-131">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

### <span data-ttu-id="1932d-132">範例 7：使用篩選功能取得金鑰庫中的所有金鑰</span><span class="sxs-lookup"><span data-stu-id="1932d-132">Example 7: Get all the keys in a key vault using filtering</span></span>
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

<span data-ttu-id="1932d-133">此命令會獲得名稱為 Contoso 的金鑰庫中以「測試」做為開始的所有金鑰。</span><span class="sxs-lookup"><span data-stu-id="1932d-133">This command gets all the keys in the key vault named Contoso that start with "test".</span></span>

## <span data-ttu-id="1932d-134">參數</span><span class="sxs-lookup"><span data-stu-id="1932d-134">PARAMETERS</span></span>

### <span data-ttu-id="1932d-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1932d-135">-DefaultProfile</span></span>
<span data-ttu-id="1932d-136">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="1932d-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1932d-137">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="1932d-137">-IncludeVersions</span></span>
<span data-ttu-id="1932d-138">表示此 Cmdlet 會獲得所有版本的金鑰。</span><span class="sxs-lookup"><span data-stu-id="1932d-138">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="1932d-139">目前版本的金鑰是清單中的第一個版本。</span><span class="sxs-lookup"><span data-stu-id="1932d-139">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="1932d-140">如果您指定此參數，您也必須指定 *Name* 和 *VaultName* 參數。</span><span class="sxs-lookup"><span data-stu-id="1932d-140">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="1932d-141">如果您未指定 *IncludeVersions* 參數，此 Cmdlet 會以指定的名稱獲得目前版本的 *金鑰*。</span><span class="sxs-lookup"><span data-stu-id="1932d-141">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

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

### <span data-ttu-id="1932d-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1932d-142">-InputObject</span></span>
<span data-ttu-id="1932d-143">KeyVault 物件。</span><span class="sxs-lookup"><span data-stu-id="1932d-143">KeyVault object.</span></span>

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

### <span data-ttu-id="1932d-144">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="1932d-144">-InRemovedState</span></span>
<span data-ttu-id="1932d-145">指定是否要在輸出中顯示先前刪除的按鍵</span><span class="sxs-lookup"><span data-stu-id="1932d-145">Specifies whether to show the previously deleted keys in the output</span></span>

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

### <span data-ttu-id="1932d-146">-名稱</span><span class="sxs-lookup"><span data-stu-id="1932d-146">-Name</span></span>
<span data-ttu-id="1932d-147">指定要取得之金鑰組合的名稱。</span><span class="sxs-lookup"><span data-stu-id="1932d-147">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByKeyVersions, ByInputObjectKeyName, ByInputObjectKeyVersions, ByResourceIdKeyName, ByResourceIdKeyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="1932d-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1932d-148">-ResourceId</span></span>
<span data-ttu-id="1932d-149">KeyVault 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1932d-149">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="1932d-150">-VaultName</span><span class="sxs-lookup"><span data-stu-id="1932d-150">-VaultName</span></span>
<span data-ttu-id="1932d-151">指定此 Cmdlet 從其中獲得金鑰的金鑰庫名稱。</span><span class="sxs-lookup"><span data-stu-id="1932d-151">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="1932d-152">此 Cmdlet 會根據此參數指定的名稱 (所選環境，建構金鑰庫的 FQDN) 完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="1932d-152">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

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

### <span data-ttu-id="1932d-153">-版本</span><span class="sxs-lookup"><span data-stu-id="1932d-153">-Version</span></span>
<span data-ttu-id="1932d-154">指定金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="1932d-154">Specifies the key version.</span></span>
<span data-ttu-id="1932d-155">此 Cmdlet 會根據金鑰庫名稱、您目前選取的環境、金鑰名稱和金鑰版本來建構金鑰的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="1932d-155">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

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

### <span data-ttu-id="1932d-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1932d-156">CommonParameters</span></span>
<span data-ttu-id="1932d-157">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1932d-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1932d-158">詳細資訊[請參閱about_CommonParameters。](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1932d-158">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1932d-159">輸入</span><span class="sxs-lookup"><span data-stu-id="1932d-159">INPUTS</span></span>

### <span data-ttu-id="1932d-160">Microsoft.Azure.Commands.KeyVault.models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="1932d-160">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="1932d-161">System.String</span><span class="sxs-lookup"><span data-stu-id="1932d-161">System.String</span></span>

## <span data-ttu-id="1932d-162">輸出</span><span class="sxs-lookup"><span data-stu-id="1932d-162">OUTPUTS</span></span>

### <span data-ttu-id="1932d-163">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="1932d-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="1932d-164">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1932d-164">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

### <span data-ttu-id="1932d-165">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="1932d-165">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="1932d-166">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1932d-166">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="1932d-167">筆記</span><span class="sxs-lookup"><span data-stu-id="1932d-167">NOTES</span></span>

## <span data-ttu-id="1932d-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="1932d-168">RELATED LINKS</span></span>

[<span data-ttu-id="1932d-169">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1932d-169">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="1932d-170">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1932d-170">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="1932d-171">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="1932d-171">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)


