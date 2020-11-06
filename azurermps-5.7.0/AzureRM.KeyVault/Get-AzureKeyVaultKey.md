---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultKey.md
ms.openlocfilehash: eaddfaa6be725d588c8856031a34e1bdefcc3892
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452235"
---
# <span data-ttu-id="b756b-101">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b756b-101">Get-AzureKeyVaultKey</span></span>

## <span data-ttu-id="b756b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b756b-102">SYNOPSIS</span></span>
<span data-ttu-id="b756b-103">取得金鑰保存庫金鑰。</span><span class="sxs-lookup"><span data-stu-id="b756b-103">Gets Key Vault keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b756b-104">句法</span><span class="sxs-lookup"><span data-stu-id="b756b-104">SYNTAX</span></span>

### <span data-ttu-id="b756b-105">ByVaultName (預設) </span><span class="sxs-lookup"><span data-stu-id="b756b-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b756b-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="b756b-106">ByKeyName</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b756b-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="b756b-107">ByKeyVersions</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b756b-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="b756b-108">ByInputObjectVaultName</span></span>
```
Get-AzureKeyVaultKey [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b756b-109">ByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="b756b-109">ByInputObjectKeyName</span></span>
```
Get-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b756b-110">ByKInputObjecteyVersions</span><span class="sxs-lookup"><span data-stu-id="b756b-110">ByKInputObjecteyVersions</span></span>
```
Get-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b756b-111">說明</span><span class="sxs-lookup"><span data-stu-id="b756b-111">DESCRIPTION</span></span>
<span data-ttu-id="b756b-112">**AzureKeyVaultKey** Cmdlet 會取得 Azure 金鑰保存庫金鑰。</span><span class="sxs-lookup"><span data-stu-id="b756b-112">The **Get-AzureKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="b756b-113">這個 Cmdlet 會取得特定的 **KeyVault KeyBundle** 或主要保存庫或依據版本中所有 **KeyBundle** 物件的清單。</span><span class="sxs-lookup"><span data-stu-id="b756b-113">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="b756b-114">示例</span><span class="sxs-lookup"><span data-stu-id="b756b-114">EXAMPLES</span></span>

### <span data-ttu-id="b756b-115">範例1：取得金鑰保存庫中的所有按鍵</span><span class="sxs-lookup"><span data-stu-id="b756b-115">Example 1: Get all the keys in a key vault</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso'
```

<span data-ttu-id="b756b-116">這個命令會取得名為 Contoso 的主要電子倉庫中的所有金鑰。</span><span class="sxs-lookup"><span data-stu-id="b756b-116">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="b756b-117">範例2：取得目前的金鑰版本</span><span class="sxs-lookup"><span data-stu-id="b756b-117">Example 2: Get the current version of a key</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx'
```

<span data-ttu-id="b756b-118">這個命令會取得名為 Contoso 的主要保存庫中名為 ITPfx 之金鑰的目前版本。</span><span class="sxs-lookup"><span data-stu-id="b756b-118">This command gets the current version of the key named ITPfx in the key vault named Contoso.</span></span>

### <span data-ttu-id="b756b-119">範例3：取得金鑰的所有版本</span><span class="sxs-lookup"><span data-stu-id="b756b-119">Example 3: Get all versions of a key</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -IncludeVersions
```

<span data-ttu-id="b756b-120">這個命令會取得所有版本金鑰 vaultnamed Contoso 中名為 ITPfx 的金鑰。</span><span class="sxs-lookup"><span data-stu-id="b756b-120">This command gets all versions the key named ITPfx in the key vaultnamed Contoso.</span></span>

### <span data-ttu-id="b756b-121">範例4：取得特定的金鑰版本</span><span class="sxs-lookup"><span data-stu-id="b756b-121">Example 4: Get a specific version of a key</span></span>
```
PS C:\>$Key = Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -Version '5A12A276385949DB8B5F82AFEE85CAED'
```

<span data-ttu-id="b756b-122">這個命令會在名為 Contoso 的主要保存庫中，取得名為 ITPfx 的特定金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="b756b-122">This command gets a specific version of the key named ITPfx in the key vault named Contoso.</span></span>
<span data-ttu-id="b756b-123">執行此命令之後，您可以流覽 $Key 物件來檢查索引鍵的各種屬性。</span><span class="sxs-lookup"><span data-stu-id="b756b-123">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="b756b-124">範例5：取得已刪除但未針對此金鑰保存庫清除的所有索引鍵。</span><span class="sxs-lookup"><span data-stu-id="b756b-124">Example 5: Get all the keys that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="b756b-125">這個命令會在名為 Contoso 的金鑰保存庫中，取得先前已刪除但尚未清除的所有索引鍵。</span><span class="sxs-lookup"><span data-stu-id="b756b-125">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="b756b-126">範例6：取得已刪除但未針對此金鑰保存庫清除的金鑰 ITPfx。</span><span class="sxs-lookup"><span data-stu-id="b756b-126">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -InRemovedState
```

<span data-ttu-id="b756b-127">這個命令會在名為 Contoso 的金鑰保存庫中，取得先前已刪除但尚未清除的金鑰 ITPfx。</span><span class="sxs-lookup"><span data-stu-id="b756b-127">This command gets the key ITPfx that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="b756b-128">這個命令會傳回中繼資料，例如刪除日期，以及此刪除金鑰的排程清除日期。</span><span class="sxs-lookup"><span data-stu-id="b756b-128">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

## <span data-ttu-id="b756b-129">參數</span><span class="sxs-lookup"><span data-stu-id="b756b-129">PARAMETERS</span></span>

### <span data-ttu-id="b756b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b756b-130">-DefaultProfile</span></span>
<span data-ttu-id="b756b-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b756b-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b756b-132">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="b756b-132">-IncludeVersions</span></span>
<span data-ttu-id="b756b-133">表示此 Cmdlet 會取得所有版本的金鑰。</span><span class="sxs-lookup"><span data-stu-id="b756b-133">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="b756b-134">索引鍵的目前版本是清單中的第一個版本。</span><span class="sxs-lookup"><span data-stu-id="b756b-134">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="b756b-135">如果您指定此參數，您也必須指定 *Name* 及 *VaultName* 參數。</span><span class="sxs-lookup"><span data-stu-id="b756b-135">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>

<span data-ttu-id="b756b-136">如果您沒有指定 *IncludeVersions* 參數，這個 Cmdlet 會取得具有指定 *名稱* 的目前金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="b756b-136">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByKeyVersions, ByKInputObjecteyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b756b-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b756b-137">-InputObject</span></span>
<span data-ttu-id="b756b-138">KeyVault 物件。</span><span class="sxs-lookup"><span data-stu-id="b756b-138">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObjectVaultName, ByInputObjectKeyName, ByKInputObjecteyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b756b-139">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="b756b-139">-InRemovedState</span></span>
<span data-ttu-id="b756b-140">指定是否要在輸出中顯示先前刪除的索引鍵</span><span class="sxs-lookup"><span data-stu-id="b756b-140">Specifies whether to show the previously deleted keys in the output</span></span>

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

### <span data-ttu-id="b756b-141">-名稱</span><span class="sxs-lookup"><span data-stu-id="b756b-141">-Name</span></span>
<span data-ttu-id="b756b-142">指定要取得的金鑰捆綁的名稱。</span><span class="sxs-lookup"><span data-stu-id="b756b-142">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName, ByInputObjectVaultName
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByKeyName, ByKeyVersions, ByInputObjectKeyName, ByKInputObjecteyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b756b-143">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b756b-143">-VaultName</span></span>
<span data-ttu-id="b756b-144">指定由此 Cmdlet 取得金鑰之金鑰電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="b756b-144">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="b756b-145">這個 Cmdlet 會根據此參數指定的名稱和您所選的環境，來構造金鑰 vault (FQDN) 的完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="b756b-145">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName, ByKeyName, ByKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b756b-146">-版本</span><span class="sxs-lookup"><span data-stu-id="b756b-146">-Version</span></span>
<span data-ttu-id="b756b-147">指定金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="b756b-147">Specifies the key version.</span></span>
<span data-ttu-id="b756b-148">這個 Cmdlet 根據金鑰保存庫名稱、您目前選取的環境、金鑰名稱及金鑰版本來構造金鑰的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="b756b-148">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: String
Parameter Sets: ByKeyName, ByInputObjectKeyName
Aliases: KeyVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b756b-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b756b-149">CommonParameters</span></span>
<span data-ttu-id="b756b-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b756b-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b756b-151">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b756b-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b756b-152">輸入</span><span class="sxs-lookup"><span data-stu-id="b756b-152">INPUTS</span></span>

### <span data-ttu-id="b756b-153">字串</span><span class="sxs-lookup"><span data-stu-id="b756b-153">String</span></span>

## <span data-ttu-id="b756b-154">輸出</span><span class="sxs-lookup"><span data-stu-id="b756b-154">OUTPUTS</span></span>

### <span data-ttu-id="b756b-155">清單<PSKeyVaultKeyIdentityItem>，KeyVault.. PSKeyVaultKey、List<Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem>、Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey。</span><span class="sxs-lookup"><span data-stu-id="b756b-155">List<Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey, List<Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="b756b-156">筆記</span><span class="sxs-lookup"><span data-stu-id="b756b-156">NOTES</span></span>

## <span data-ttu-id="b756b-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="b756b-157">RELATED LINKS</span></span>

[<span data-ttu-id="b756b-158">附加 AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b756b-158">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="b756b-159">移除-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b756b-159">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="b756b-160">復原-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="b756b-160">Undo-AzureKeyVaultKeyRemoval</span></span>](./Undo-AzureKeyVaultKeyRemoval.md)

[<span data-ttu-id="b756b-161">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="b756b-161">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)

