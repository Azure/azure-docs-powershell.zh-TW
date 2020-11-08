---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
ms.openlocfilehash: 0de3582d9a5cbdaba8555cf53bd9038d3eaf15b2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127681"
---
# <span data-ttu-id="0802b-101">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0802b-101">Get-AzKeyVaultKey</span></span>

## <span data-ttu-id="0802b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0802b-102">SYNOPSIS</span></span>
<span data-ttu-id="0802b-103">取得金鑰保存庫金鑰。</span><span class="sxs-lookup"><span data-stu-id="0802b-103">Gets Key Vault keys.</span></span>

## <span data-ttu-id="0802b-104">句法</span><span class="sxs-lookup"><span data-stu-id="0802b-104">SYNTAX</span></span>

### <span data-ttu-id="0802b-105">ByVaultName (預設) </span><span class="sxs-lookup"><span data-stu-id="0802b-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0802b-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="0802b-106">ByKeyName</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0802b-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="0802b-107">ByKeyVersions</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0802b-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="0802b-108">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0802b-109">ByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="0802b-109">ByInputObjectKeyName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0802b-110">ByInputObjectKeyVersions</span><span class="sxs-lookup"><span data-stu-id="0802b-110">ByInputObjectKeyVersions</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0802b-111">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="0802b-111">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0802b-112">ByResourceIdKeyName</span><span class="sxs-lookup"><span data-stu-id="0802b-112">ByResourceIdKeyName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0802b-113">ByResourceIdKeyVersions</span><span class="sxs-lookup"><span data-stu-id="0802b-113">ByResourceIdKeyVersions</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0802b-114">說明</span><span class="sxs-lookup"><span data-stu-id="0802b-114">DESCRIPTION</span></span>
<span data-ttu-id="0802b-115">**AzKeyVaultKey** Cmdlet 會取得 Azure 金鑰保存庫金鑰。</span><span class="sxs-lookup"><span data-stu-id="0802b-115">The **Get-AzKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="0802b-116">這個 Cmdlet 會取得特定的 **KeyVault KeyBundle** 或主要保存庫或依據版本中所有 **KeyBundle** 物件的清單。</span><span class="sxs-lookup"><span data-stu-id="0802b-116">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="0802b-117">示例</span><span class="sxs-lookup"><span data-stu-id="0802b-117">EXAMPLES</span></span>

### <span data-ttu-id="0802b-118">範例1：取得金鑰保存庫中的所有按鍵</span><span class="sxs-lookup"><span data-stu-id="0802b-118">Example 1: Get all the keys in a key vault</span></span>
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

<span data-ttu-id="0802b-119">這個命令會取得名為 Contoso 的主要電子倉庫中的所有金鑰。</span><span class="sxs-lookup"><span data-stu-id="0802b-119">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="0802b-120">範例2：取得目前的金鑰版本</span><span class="sxs-lookup"><span data-stu-id="0802b-120">Example 2: Get the current version of a key</span></span>
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

<span data-ttu-id="0802b-121">這個命令會取得名為 Contoso 之金鑰保存庫中名為 test1 的目前版本的金鑰。</span><span class="sxs-lookup"><span data-stu-id="0802b-121">This command gets the current version of the key named test1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="0802b-122">範例3：取得金鑰的所有版本</span><span class="sxs-lookup"><span data-stu-id="0802b-122">Example 3: Get all versions of a key</span></span>
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

<span data-ttu-id="0802b-123">這個命令會取得所有版本金鑰 vaultnamed Contoso 中名為 ITPfx 的金鑰。</span><span class="sxs-lookup"><span data-stu-id="0802b-123">This command gets all versions the key named ITPfx in the key vaultnamed Contoso.</span></span>

### <span data-ttu-id="0802b-124">範例4：取得特定的金鑰版本</span><span class="sxs-lookup"><span data-stu-id="0802b-124">Example 4: Get a specific version of a key</span></span>
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

<span data-ttu-id="0802b-125">這個命令會在名為 Contoso 的主要保存庫中，取得名為 test1 的特定金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="0802b-125">This command gets a specific version of the key named test1 in the key vault named Contoso.</span></span>
<span data-ttu-id="0802b-126">執行此命令之後，您可以流覽 $Key 物件來檢查索引鍵的各種屬性。</span><span class="sxs-lookup"><span data-stu-id="0802b-126">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="0802b-127">範例5：取得已刪除但未針對此金鑰保存庫清除的所有索引鍵。</span><span class="sxs-lookup"><span data-stu-id="0802b-127">Example 5: Get all the keys that have been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="0802b-128">這個命令會在名為 Contoso 的金鑰保存庫中，取得先前已刪除但尚未清除的所有索引鍵。</span><span class="sxs-lookup"><span data-stu-id="0802b-128">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="0802b-129">範例6：取得已刪除但未針對此金鑰保存庫清除的金鑰 ITPfx。</span><span class="sxs-lookup"><span data-stu-id="0802b-129">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="0802b-130">這個命令會在名為 Contoso 的金鑰保存庫中，取得先前已刪除但尚未清除的金鑰 test3。</span><span class="sxs-lookup"><span data-stu-id="0802b-130">This command gets the key test3 that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="0802b-131">這個命令會傳回中繼資料，例如刪除日期，以及此刪除金鑰的排程清除日期。</span><span class="sxs-lookup"><span data-stu-id="0802b-131">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

### <span data-ttu-id="0802b-132">範例7：使用篩選取得金鑰保存庫中的所有金鑰</span><span class="sxs-lookup"><span data-stu-id="0802b-132">Example 7: Get all the keys in a key vault using filtering</span></span>
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

<span data-ttu-id="0802b-133">這個命令會取得名為 Contoso 的主要電子倉庫中，以「test」開頭的所有索引鍵。</span><span class="sxs-lookup"><span data-stu-id="0802b-133">This command gets all the keys in the key vault named Contoso that start with "test".</span></span>

### <span data-ttu-id="0802b-134">範例8：下載公開金鑰做為 pem 檔案</span><span class="sxs-lookup"><span data-stu-id="0802b-134">Example 8: Download a public key as a .pem file</span></span>

```powershell
PS C:\> $path = "D:\public.pem"
PS C:\> Get-AzKeyVaultKey -VaultName $vaultName -KeyName $keyName -OutFile $path
```

<span data-ttu-id="0802b-135">您可以透過指定參數來下載 RSA 金鑰的公開金鑰 `-OutFile` 。</span><span class="sxs-lookup"><span data-stu-id="0802b-135">You can download the public key of a RSA key by specifying the `-OutFile` parameter.</span></span>
<span data-ttu-id="0802b-136">這是將受 HSM 保護的金鑰匯入 Azure 金鑰保存庫的一個步驟。</span><span class="sxs-lookup"><span data-stu-id="0802b-136">This is one step of importing HSM-protected keys to Azure Key Vault.</span></span> <span data-ttu-id="0802b-137">請參閱 https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span><span class="sxs-lookup"><span data-stu-id="0802b-137">See https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span></span>

## <span data-ttu-id="0802b-138">參數</span><span class="sxs-lookup"><span data-stu-id="0802b-138">PARAMETERS</span></span>

### <span data-ttu-id="0802b-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0802b-139">-DefaultProfile</span></span>
<span data-ttu-id="0802b-140">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="0802b-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0802b-141">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="0802b-141">-IncludeVersions</span></span>
<span data-ttu-id="0802b-142">表示此 Cmdlet 會取得所有版本的金鑰。</span><span class="sxs-lookup"><span data-stu-id="0802b-142">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="0802b-143">索引鍵的目前版本是清單中的第一個版本。</span><span class="sxs-lookup"><span data-stu-id="0802b-143">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="0802b-144">如果您指定此參數，您也必須指定 *Name* 及 *VaultName* 參數。</span><span class="sxs-lookup"><span data-stu-id="0802b-144">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="0802b-145">如果您沒有指定 *IncludeVersions* 參數，這個 Cmdlet 會取得具有指定 *名稱* 的目前金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="0802b-145">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

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

### <span data-ttu-id="0802b-146">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0802b-146">-InputObject</span></span>
<span data-ttu-id="0802b-147">KeyVault 物件。</span><span class="sxs-lookup"><span data-stu-id="0802b-147">KeyVault object.</span></span>

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

### <span data-ttu-id="0802b-148">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="0802b-148">-InRemovedState</span></span>
<span data-ttu-id="0802b-149">指定是否要在輸出中顯示先前刪除的索引鍵</span><span class="sxs-lookup"><span data-stu-id="0802b-149">Specifies whether to show the previously deleted keys in the output</span></span>

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

### <span data-ttu-id="0802b-150">-名稱</span><span class="sxs-lookup"><span data-stu-id="0802b-150">-Name</span></span>
<span data-ttu-id="0802b-151">指定要取得的金鑰捆綁的名稱。</span><span class="sxs-lookup"><span data-stu-id="0802b-151">Specifies the name of the key bundle to get.</span></span>

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

### <span data-ttu-id="0802b-152">-OutFile</span><span class="sxs-lookup"><span data-stu-id="0802b-152">-OutFile</span></span>
<span data-ttu-id="0802b-153">指定此 Cmdlet 儲存金鑰的輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="0802b-153">Specifies the output file for which this cmdlet saves the key.</span></span> <span data-ttu-id="0802b-154">公開金鑰預設會以 PEM 格式儲存。</span><span class="sxs-lookup"><span data-stu-id="0802b-154">The public key is saved in PEM format by default.</span></span>

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

### <span data-ttu-id="0802b-155">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0802b-155">-ResourceId</span></span>
<span data-ttu-id="0802b-156">KeyVault 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0802b-156">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="0802b-157">-VaultName</span><span class="sxs-lookup"><span data-stu-id="0802b-157">-VaultName</span></span>
<span data-ttu-id="0802b-158">指定由此 Cmdlet 取得金鑰之金鑰電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="0802b-158">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="0802b-159">這個 Cmdlet 會根據此參數指定的名稱和您所選的環境，來構造金鑰 vault (FQDN) 的完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="0802b-159">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

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

### <span data-ttu-id="0802b-160">-版本</span><span class="sxs-lookup"><span data-stu-id="0802b-160">-Version</span></span>
<span data-ttu-id="0802b-161">指定金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="0802b-161">Specifies the key version.</span></span>
<span data-ttu-id="0802b-162">這個 Cmdlet 根據金鑰保存庫名稱、您目前選取的環境、金鑰名稱及金鑰版本來構造金鑰的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="0802b-162">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

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

### <span data-ttu-id="0802b-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0802b-163">CommonParameters</span></span>
<span data-ttu-id="0802b-164">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0802b-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0802b-165">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0802b-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0802b-166">輸入</span><span class="sxs-lookup"><span data-stu-id="0802b-166">INPUTS</span></span>

### <span data-ttu-id="0802b-167">PSKeyVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="0802b-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="0802b-168">System.object</span><span class="sxs-lookup"><span data-stu-id="0802b-168">System.String</span></span>

## <span data-ttu-id="0802b-169">輸出</span><span class="sxs-lookup"><span data-stu-id="0802b-169">OUTPUTS</span></span>

### <span data-ttu-id="0802b-170">PSKeyVaultKeyIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="0802b-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="0802b-171">PSKeyVaultKey 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="0802b-171">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

### <span data-ttu-id="0802b-172">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="0802b-172">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="0802b-173">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0802b-173">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="0802b-174">筆記</span><span class="sxs-lookup"><span data-stu-id="0802b-174">NOTES</span></span>

## <span data-ttu-id="0802b-175">相關連結</span><span class="sxs-lookup"><span data-stu-id="0802b-175">RELATED LINKS</span></span>

[<span data-ttu-id="0802b-176">附加 AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0802b-176">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="0802b-177">移除-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0802b-177">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="0802b-178">復原-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="0802b-178">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

[<span data-ttu-id="0802b-179">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="0802b-179">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

