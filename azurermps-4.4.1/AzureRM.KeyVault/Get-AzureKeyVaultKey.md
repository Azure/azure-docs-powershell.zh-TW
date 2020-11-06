---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://go.microsoft.com/fwlink/?LinkId=690297
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultKey.md
ms.openlocfilehash: 48d050623ea75bed1aee1b78a26bf81bf3305e06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446802"
---
# <span data-ttu-id="c6f5b-101">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c6f5b-101">Get-AzureKeyVaultKey</span></span>

## <span data-ttu-id="c6f5b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c6f5b-102">SYNOPSIS</span></span>
<span data-ttu-id="c6f5b-103">取得金鑰保存庫金鑰。</span><span class="sxs-lookup"><span data-stu-id="c6f5b-103">Gets Key Vault keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6f5b-104">句法</span><span class="sxs-lookup"><span data-stu-id="c6f5b-104">SYNTAX</span></span>

### <span data-ttu-id="c6f5b-105">ByVaultName (預設) </span><span class="sxs-lookup"><span data-stu-id="c6f5b-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6f5b-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="c6f5b-106">ByKeyName</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6f5b-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="c6f5b-107">ByKeyVersions</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6f5b-108">ByDeletedKey</span><span class="sxs-lookup"><span data-stu-id="c6f5b-108">ByDeletedKey</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6f5b-109">說明</span><span class="sxs-lookup"><span data-stu-id="c6f5b-109">DESCRIPTION</span></span>
<span data-ttu-id="c6f5b-110">**AzureKeyVaultKey** Cmdlet 會取得 Azure 金鑰保存庫金鑰。</span><span class="sxs-lookup"><span data-stu-id="c6f5b-110">The **Get-AzureKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="c6f5b-111">這個 Cmdlet 會取得特定的 **KeyVault KeyBundle** 或主要保存庫或依據版本中所有 **KeyBundle** 物件的清單。</span><span class="sxs-lookup"><span data-stu-id="c6f5b-111">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="c6f5b-112">示例</span><span class="sxs-lookup"><span data-stu-id="c6f5b-112">EXAMPLES</span></span>

### <span data-ttu-id="c6f5b-113">範例1：取得金鑰保存庫中的所有按鍵</span><span class="sxs-lookup"><span data-stu-id="c6f5b-113">Example 1: Get all the keys in a key vault</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso'
```

<span data-ttu-id="c6f5b-114">這個命令會取得名為 Contoso 的主要電子倉庫中的所有金鑰。</span><span class="sxs-lookup"><span data-stu-id="c6f5b-114">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="c6f5b-115">範例2：取得目前的金鑰版本</span><span class="sxs-lookup"><span data-stu-id="c6f5b-115">Example 2: Get the current version of a key</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx'
```

<span data-ttu-id="c6f5b-116">這個命令會取得名為 Contoso 的主要保存庫中名為 ITPfx 之金鑰的目前版本。</span><span class="sxs-lookup"><span data-stu-id="c6f5b-116">This command gets the current version of the key named ITPfx in the key vault named Contoso.</span></span>

### <span data-ttu-id="c6f5b-117">範例3：取得金鑰的所有版本</span><span class="sxs-lookup"><span data-stu-id="c6f5b-117">Example 3: Get all versions of a key</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -IncludeVersions
```

<span data-ttu-id="c6f5b-118">這個命令會取得所有版本金鑰 vaultnamed Contoso 中名為 ITPfx 的金鑰。</span><span class="sxs-lookup"><span data-stu-id="c6f5b-118">This command gets all versions the key named ITPfx in the key vaultnamed Contoso.</span></span>

### <span data-ttu-id="c6f5b-119">範例4：取得特定的金鑰版本</span><span class="sxs-lookup"><span data-stu-id="c6f5b-119">Example 4: Get a specific version of a key</span></span>
```
PS C:\>$Key = Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -Version '5A12A276385949DB8B5F82AFEE85CAED'
```

<span data-ttu-id="c6f5b-120">這個命令會在名為 Contoso 的主要保存庫中，取得名為 ITPfx 的特定金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="c6f5b-120">This command gets a specific version of the key named ITPfx in the key vault named Contoso.</span></span>
<span data-ttu-id="c6f5b-121">執行此命令之後，您可以流覽 $Key 物件來檢查索引鍵的各種屬性。</span><span class="sxs-lookup"><span data-stu-id="c6f5b-121">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="c6f5b-122">範例5：取得已刪除但未針對此金鑰保存庫清除的所有索引鍵。</span><span class="sxs-lookup"><span data-stu-id="c6f5b-122">Example 5: Get all the keys that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="c6f5b-123">這個命令會在名為 Contoso 的金鑰保存庫中，取得先前已刪除但尚未清除的所有索引鍵。</span><span class="sxs-lookup"><span data-stu-id="c6f5b-123">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="c6f5b-124">範例6：取得已刪除但未針對此金鑰保存庫清除的金鑰 ITPfx。</span><span class="sxs-lookup"><span data-stu-id="c6f5b-124">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -InRemovedState
```

<span data-ttu-id="c6f5b-125">這個命令會在名為 Contoso 的金鑰保存庫中，取得先前已刪除但尚未清除的金鑰 ITPfx。</span><span class="sxs-lookup"><span data-stu-id="c6f5b-125">This command gets the key ITPfx that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="c6f5b-126">這個命令會傳回中繼資料，例如刪除日期，以及此刪除金鑰的排程清除日期。</span><span class="sxs-lookup"><span data-stu-id="c6f5b-126">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

## <span data-ttu-id="c6f5b-127">參數</span><span class="sxs-lookup"><span data-stu-id="c6f5b-127">PARAMETERS</span></span>

### <span data-ttu-id="c6f5b-128">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="c6f5b-128">-IncludeVersions</span></span>
<span data-ttu-id="c6f5b-129">表示此 Cmdlet 會取得所有版本的金鑰。</span><span class="sxs-lookup"><span data-stu-id="c6f5b-129">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="c6f5b-130">索引鍵的目前版本是清單中的第一個版本。</span><span class="sxs-lookup"><span data-stu-id="c6f5b-130">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="c6f5b-131">如果您指定此參數，您也必須指定 *Name* 及 *VaultName* 參數。</span><span class="sxs-lookup"><span data-stu-id="c6f5b-131">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>

<span data-ttu-id="c6f5b-132">如果您沒有指定 *IncludeVersions* 參數，這個 Cmdlet 會取得具有指定 *名稱* 的目前金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="c6f5b-132">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByKeyVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6f5b-133">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="c6f5b-133">-InRemovedState</span></span>
<span data-ttu-id="c6f5b-134">指定是否要在輸出中顯示先前刪除的金鑰。</span><span class="sxs-lookup"><span data-stu-id="c6f5b-134">Specifies whether to show the previously deleted keys in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedKey
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6f5b-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="c6f5b-135">-Name</span></span>
<span data-ttu-id="c6f5b-136">指定要取得的金鑰捆綁的名稱。</span><span class="sxs-lookup"><span data-stu-id="c6f5b-136">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByKeyVersions
Aliases: KeyName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedKey
Aliases: KeyName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6f5b-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c6f5b-137">-VaultName</span></span>
<span data-ttu-id="c6f5b-138">指定由此 Cmdlet 取得金鑰之金鑰電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="c6f5b-138">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="c6f5b-139">這個 Cmdlet 會根據此參數指定的名稱和您所選的環境，來構造金鑰 vault (FQDN) 的完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="c6f5b-139">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6f5b-140">-版本</span><span class="sxs-lookup"><span data-stu-id="c6f5b-140">-Version</span></span>
<span data-ttu-id="c6f5b-141">指定金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="c6f5b-141">Specifies the key version.</span></span>
<span data-ttu-id="c6f5b-142">這個 Cmdlet 根據金鑰保存庫名稱、您目前選取的環境、金鑰名稱及金鑰版本來構造金鑰的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="c6f5b-142">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases: KeyVersion

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6f5b-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6f5b-143">-DefaultProfile</span></span>
<span data-ttu-id="c6f5b-144">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c6f5b-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6f5b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6f5b-145">CommonParameters</span></span>
<span data-ttu-id="c6f5b-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c6f5b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6f5b-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c6f5b-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6f5b-148">輸入</span><span class="sxs-lookup"><span data-stu-id="c6f5b-148">INPUTS</span></span>

### <span data-ttu-id="c6f5b-149">字串</span><span class="sxs-lookup"><span data-stu-id="c6f5b-149">String</span></span>

## <span data-ttu-id="c6f5b-150">輸出</span><span class="sxs-lookup"><span data-stu-id="c6f5b-150">OUTPUTS</span></span>

### <span data-ttu-id="c6f5b-151">[KeyVault]<清單中的 [> KeyIdentityItem]。 KeyVault. KeyBundle、List><、、、KeyVault、、、、、、、、</span><span class="sxs-lookup"><span data-stu-id="c6f5b-151">List<Microsoft.Azure.Commands.KeyVault.Models.KeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyBundle, List<Microsoft.Azure.Commands.KeyVault.Models.DeletedKeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.DeletedKeyBundle</span></span>

## <span data-ttu-id="c6f5b-152">筆記</span><span class="sxs-lookup"><span data-stu-id="c6f5b-152">NOTES</span></span>

## <span data-ttu-id="c6f5b-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="c6f5b-153">RELATED LINKS</span></span>

[<span data-ttu-id="c6f5b-154">附加 AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c6f5b-154">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="c6f5b-155">移除-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c6f5b-155">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="c6f5b-156">復原-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="c6f5b-156">Undo-AzureKeyVaultKeyRemoval</span></span>](./Undo-AzureKeyVaultKeyRemoval.md)

[<span data-ttu-id="c6f5b-157">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="c6f5b-157">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)

