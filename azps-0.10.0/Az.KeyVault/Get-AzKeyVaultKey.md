---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
ms.openlocfilehash: a0d79aa0d1699f6e6645f86475732c235447342f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794672"
---
# <span data-ttu-id="3964f-101">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3964f-101">Get-AzKeyVaultKey</span></span>

## <span data-ttu-id="3964f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3964f-102">SYNOPSIS</span></span>
<span data-ttu-id="3964f-103">取得金鑰保存庫金鑰。</span><span class="sxs-lookup"><span data-stu-id="3964f-103">Gets Key Vault keys.</span></span>

## <span data-ttu-id="3964f-104">句法</span><span class="sxs-lookup"><span data-stu-id="3964f-104">SYNTAX</span></span>

### <span data-ttu-id="3964f-105">ByVaultName (預設) </span><span class="sxs-lookup"><span data-stu-id="3964f-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3964f-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="3964f-106">ByKeyName</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3964f-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="3964f-107">ByKeyVersions</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3964f-108">ByDeletedKey</span><span class="sxs-lookup"><span data-stu-id="3964f-108">ByDeletedKey</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3964f-109">說明</span><span class="sxs-lookup"><span data-stu-id="3964f-109">DESCRIPTION</span></span>
<span data-ttu-id="3964f-110">**AzKeyVaultKey** Cmdlet 會取得 Azure 金鑰保存庫金鑰。</span><span class="sxs-lookup"><span data-stu-id="3964f-110">The **Get-AzKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="3964f-111">這個 Cmdlet 會取得特定的 **KeyVault KeyBundle** 或主要保存庫或依據版本中所有 **KeyBundle** 物件的清單。</span><span class="sxs-lookup"><span data-stu-id="3964f-111">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="3964f-112">示例</span><span class="sxs-lookup"><span data-stu-id="3964f-112">EXAMPLES</span></span>

### <span data-ttu-id="3964f-113">範例1：取得金鑰保存庫中的所有按鍵</span><span class="sxs-lookup"><span data-stu-id="3964f-113">Example 1: Get all the keys in a key vault</span></span>
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso'
```

<span data-ttu-id="3964f-114">這個命令會取得名為 Contoso 的主要電子倉庫中的所有金鑰。</span><span class="sxs-lookup"><span data-stu-id="3964f-114">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="3964f-115">範例2：取得目前的金鑰版本</span><span class="sxs-lookup"><span data-stu-id="3964f-115">Example 2: Get the current version of a key</span></span>
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx'
```

<span data-ttu-id="3964f-116">這個命令會取得名為 Contoso 的主要保存庫中名為 ITPfx 之金鑰的目前版本。</span><span class="sxs-lookup"><span data-stu-id="3964f-116">This command gets the current version of the key named ITPfx in the key vault named Contoso.</span></span>

### <span data-ttu-id="3964f-117">範例3：取得金鑰的所有版本</span><span class="sxs-lookup"><span data-stu-id="3964f-117">Example 3: Get all versions of a key</span></span>
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -IncludeVersions
```

<span data-ttu-id="3964f-118">這個命令會取得所有版本金鑰 vaultnamed Contoso 中名為 ITPfx 的金鑰。</span><span class="sxs-lookup"><span data-stu-id="3964f-118">This command gets all versions the key named ITPfx in the key vaultnamed Contoso.</span></span>

### <span data-ttu-id="3964f-119">範例4：取得特定的金鑰版本</span><span class="sxs-lookup"><span data-stu-id="3964f-119">Example 4: Get a specific version of a key</span></span>
```
PS C:\>$Key = Get-AzKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -Version '5A12A276385949DB8B5F82AFEE85CAED'
```

<span data-ttu-id="3964f-120">這個命令會在名為 Contoso 的主要保存庫中，取得名為 ITPfx 的特定金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="3964f-120">This command gets a specific version of the key named ITPfx in the key vault named Contoso.</span></span>
<span data-ttu-id="3964f-121">執行此命令之後，您可以流覽 $Key 物件來檢查索引鍵的各種屬性。</span><span class="sxs-lookup"><span data-stu-id="3964f-121">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="3964f-122">範例5：取得已刪除但未針對此金鑰保存庫清除的所有索引鍵。</span><span class="sxs-lookup"><span data-stu-id="3964f-122">Example 5: Get all the keys that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="3964f-123">這個命令會在名為 Contoso 的金鑰保存庫中，取得先前已刪除但尚未清除的所有索引鍵。</span><span class="sxs-lookup"><span data-stu-id="3964f-123">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="3964f-124">範例6：取得已刪除但未針對此金鑰保存庫清除的金鑰 ITPfx。</span><span class="sxs-lookup"><span data-stu-id="3964f-124">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -InRemovedState
```

<span data-ttu-id="3964f-125">這個命令會在名為 Contoso 的金鑰保存庫中，取得先前已刪除但尚未清除的金鑰 ITPfx。</span><span class="sxs-lookup"><span data-stu-id="3964f-125">This command gets the key ITPfx that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="3964f-126">這個命令會傳回中繼資料，例如刪除日期，以及此刪除金鑰的排程清除日期。</span><span class="sxs-lookup"><span data-stu-id="3964f-126">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

## <span data-ttu-id="3964f-127">參數</span><span class="sxs-lookup"><span data-stu-id="3964f-127">PARAMETERS</span></span>

### <span data-ttu-id="3964f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3964f-128">-DefaultProfile</span></span>
<span data-ttu-id="3964f-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="3964f-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3964f-130">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="3964f-130">-IncludeVersions</span></span>
<span data-ttu-id="3964f-131">表示此 Cmdlet 會取得所有版本的金鑰。</span><span class="sxs-lookup"><span data-stu-id="3964f-131">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="3964f-132">索引鍵的目前版本是清單中的第一個版本。</span><span class="sxs-lookup"><span data-stu-id="3964f-132">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="3964f-133">如果您指定此參數，您也必須指定 *Name* 及 *VaultName* 參數。</span><span class="sxs-lookup"><span data-stu-id="3964f-133">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>

<span data-ttu-id="3964f-134">如果您沒有指定 *IncludeVersions* 參數，這個 Cmdlet 會取得具有指定 *名稱* 的目前金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="3964f-134">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByKeyVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3964f-135">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="3964f-135">-InRemovedState</span></span>
<span data-ttu-id="3964f-136">指定是否要在輸出中顯示先前刪除的索引鍵</span><span class="sxs-lookup"><span data-stu-id="3964f-136">Specifies whether to show the previously deleted keys in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedKey
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3964f-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="3964f-137">-Name</span></span>
<span data-ttu-id="3964f-138">指定要取得的金鑰捆綁的名稱。</span><span class="sxs-lookup"><span data-stu-id="3964f-138">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: String
Parameter Sets: ByKeyName, ByKeyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedKey
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3964f-139">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3964f-139">-VaultName</span></span>
<span data-ttu-id="3964f-140">指定由此 Cmdlet 取得金鑰之金鑰電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="3964f-140">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="3964f-141">這個 Cmdlet 會根據此參數指定的名稱和您所選的環境，來構造金鑰 vault (FQDN) 的完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="3964f-141">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

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

### <span data-ttu-id="3964f-142">-版本</span><span class="sxs-lookup"><span data-stu-id="3964f-142">-Version</span></span>
<span data-ttu-id="3964f-143">指定金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="3964f-143">Specifies the key version.</span></span>
<span data-ttu-id="3964f-144">這個 Cmdlet 根據金鑰保存庫名稱、您目前選取的環境、金鑰名稱及金鑰版本來構造金鑰的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="3964f-144">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: String
Parameter Sets: ByKeyName
Aliases: KeyVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3964f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3964f-145">CommonParameters</span></span>
<span data-ttu-id="3964f-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3964f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3964f-147">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3964f-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3964f-148">輸入</span><span class="sxs-lookup"><span data-stu-id="3964f-148">INPUTS</span></span>

### <span data-ttu-id="3964f-149">字串</span><span class="sxs-lookup"><span data-stu-id="3964f-149">String</span></span>

## <span data-ttu-id="3964f-150">輸出</span><span class="sxs-lookup"><span data-stu-id="3964f-150">OUTPUTS</span></span>

### <span data-ttu-id="3964f-151">[KeyVault]<清單中的 [> KeyIdentityItem]。 KeyVault. KeyBundle、List><、、、KeyVault、、、、、、、、</span><span class="sxs-lookup"><span data-stu-id="3964f-151">List<Microsoft.Azure.Commands.KeyVault.Models.KeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyBundle, List<Microsoft.Azure.Commands.KeyVault.Models.DeletedKeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.DeletedKeyBundle</span></span>

## <span data-ttu-id="3964f-152">筆記</span><span class="sxs-lookup"><span data-stu-id="3964f-152">NOTES</span></span>

## <span data-ttu-id="3964f-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="3964f-153">RELATED LINKS</span></span>

[<span data-ttu-id="3964f-154">附加 AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3964f-154">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="3964f-155">移除-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3964f-155">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="3964f-156">復原-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="3964f-156">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

[<span data-ttu-id="3964f-157">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="3964f-157">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

