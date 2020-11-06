---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: b16ceeb2409c2709286b970f857fcb9079bf067a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447775"
---
# <span data-ttu-id="a6e6c-101">Update-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a6e6c-101">Update-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="a6e6c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a6e6c-102">SYNOPSIS</span></span>
<span data-ttu-id="a6e6c-103">更新主要電子倉庫管理的 Azure 儲存空間帳戶的可編輯屬性。</span><span class="sxs-lookup"><span data-stu-id="a6e6c-103">Update editable attributes of a Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6e6c-104">句法</span><span class="sxs-lookup"><span data-stu-id="a6e6c-104">SYNTAX</span></span>

```
Update-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-ActiveKeyName <String>] [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a6e6c-105">說明</span><span class="sxs-lookup"><span data-stu-id="a6e6c-105">DESCRIPTION</span></span>
<span data-ttu-id="a6e6c-106">更新主要電子倉庫管理的 Azure 儲存空間帳戶的可編輯屬性。</span><span class="sxs-lookup"><span data-stu-id="a6e6c-106">Update the editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="a6e6c-107">示例</span><span class="sxs-lookup"><span data-stu-id="a6e6c-107">EXAMPLES</span></span>

### <span data-ttu-id="a6e6c-108">範例1：在主要電子倉庫管理的 Azure 儲存空間帳戶上，將 active key 更新為 ' key2」。</span><span class="sxs-lookup"><span data-stu-id="a6e6c-108">Example 1:Update the active key to 'key2' on a Key Vault managed Azure Storage Account.</span></span>
```
PS C:\> Update-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -ActiveKeyName 'key2'
```

<span data-ttu-id="a6e6c-109">將主要電子倉庫管理的 Azure 儲存空間帳戶啟用金鑰更新為 ' key2」。</span><span class="sxs-lookup"><span data-stu-id="a6e6c-109">Updates the Key Vault managed Azure Storage Account active key to 'key2'.</span></span> <span data-ttu-id="a6e6c-110">在此更新之後，"key2" 將用於產生 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="a6e6c-110">'key2' will be used to generate SAS tokens after this update.</span></span>

## <span data-ttu-id="a6e6c-111">參數</span><span class="sxs-lookup"><span data-stu-id="a6e6c-111">PARAMETERS</span></span>

### <span data-ttu-id="a6e6c-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a6e6c-112">-AccountName</span></span>
<span data-ttu-id="a6e6c-113">主要保存庫管理的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="a6e6c-113">Key Vault managed storage account name.</span></span> <span data-ttu-id="a6e6c-114">Cmdlet 會從保存庫名稱、目前已選取的環境及 manged 儲存空間帳戶名稱構造受管理儲存空間帳戶名稱的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="a6e6c-114">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6e6c-115">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="a6e6c-115">-ActiveKeyName</span></span>
<span data-ttu-id="a6e6c-116">Active 項名稱。</span><span class="sxs-lookup"><span data-stu-id="a6e6c-116">Active key name.</span></span>
<span data-ttu-id="a6e6c-117">如果未指定，受管理儲存空間帳戶的作用中金鑰名稱的現有值會保持不變</span><span class="sxs-lookup"><span data-stu-id="a6e6c-117">If not specified, the existing value of managed storage account's active key name remains unchanged</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6e6c-118">-AutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="a6e6c-118">-AutoRegenerateKey</span></span>
<span data-ttu-id="a6e6c-119">自動重新產生金鑰。</span><span class="sxs-lookup"><span data-stu-id="a6e6c-119">Auto regenerate key.</span></span>
<span data-ttu-id="a6e6c-120">如果未指定，則受管理儲存帳戶的自動重新產生鍵的現有值會保持不變</span><span class="sxs-lookup"><span data-stu-id="a6e6c-120">If not specified, the existing value of auto regenerate key of managed storage account remains unchanged</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6e6c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6e6c-121">-DefaultProfile</span></span>
<span data-ttu-id="a6e6c-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a6e6c-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a6e6c-123">-啟用</span><span class="sxs-lookup"><span data-stu-id="a6e6c-123">-Enable</span></span>
<span data-ttu-id="a6e6c-124">如果有的話，可以將受管理的儲存空間帳戶金鑰用於 sas 權杖產生（如果值為 true）。</span><span class="sxs-lookup"><span data-stu-id="a6e6c-124">If present, enables a use of a managed storage account key for sas token generation if value is true.</span></span> <span data-ttu-id="a6e6c-125">如果值為 false，則停用針對 sas 權杖產生使用受管理的儲存空間帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="a6e6c-125">Disables use of a managed storage account key for sas token generation if value is false.</span></span> <span data-ttu-id="a6e6c-126">如果未指定，儲存帳戶的啟用/停用狀態的現有值會保持不變。</span><span class="sxs-lookup"><span data-stu-id="a6e6c-126">If not specified, the existing value of the storage account's enabled/disabled state remains unchanged.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6e6c-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6e6c-127">-PassThru</span></span>
<span data-ttu-id="a6e6c-128">Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="a6e6c-128">Cmdlet does not return object by default.</span></span> <span data-ttu-id="a6e6c-129">如果已指定此開關，請傳回受管理的儲存空間帳戶物件。</span><span class="sxs-lookup"><span data-stu-id="a6e6c-129">If this switch is specified, return managed storage account object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6e6c-130">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="a6e6c-130">-RegenerationPeriod</span></span>
<span data-ttu-id="a6e6c-131">[再生期間]。</span><span class="sxs-lookup"><span data-stu-id="a6e6c-131">Regeneration period.</span></span> <span data-ttu-id="a6e6c-132">如果啟用自動重新產生鍵，此值會指定要在已管理的儲存空間帳戶停用 keygets 自動重新產生並成為作用中金鑰之後的時間跨度。</span><span class="sxs-lookup"><span data-stu-id="a6e6c-132">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the active key.</span></span> <span data-ttu-id="a6e6c-133">如果未指定，受管理的儲存帳戶金鑰的現有值會保持不變</span><span class="sxs-lookup"><span data-stu-id="a6e6c-133">If not specified, the existing value of regeneration period of keys of managed storage account remains unchanged</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6e6c-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="a6e6c-134">-Tag</span></span>
<span data-ttu-id="a6e6c-135">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="a6e6c-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a6e6c-136">例如：</span><span class="sxs-lookup"><span data-stu-id="a6e6c-136">For example:</span></span>

<span data-ttu-id="a6e6c-137">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="a6e6c-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6e6c-138">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a6e6c-138">-VaultName</span></span>
<span data-ttu-id="a6e6c-139">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="a6e6c-139">Vault name.</span></span>
<span data-ttu-id="a6e6c-140">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="a6e6c-140">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="a6e6c-141">-確認</span><span class="sxs-lookup"><span data-stu-id="a6e6c-141">-Confirm</span></span>
<span data-ttu-id="a6e6c-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a6e6c-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6e6c-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6e6c-143">-WhatIf</span></span>
<span data-ttu-id="a6e6c-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a6e6c-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6e6c-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a6e6c-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6e6c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6e6c-146">CommonParameters</span></span>
<span data-ttu-id="a6e6c-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a6e6c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6e6c-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a6e6c-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6e6c-149">輸入</span><span class="sxs-lookup"><span data-stu-id="a6e6c-149">INPUTS</span></span>

### <span data-ttu-id="a6e6c-150">所有</span><span class="sxs-lookup"><span data-stu-id="a6e6c-150">None</span></span>
<span data-ttu-id="a6e6c-151">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="a6e6c-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a6e6c-152">輸出</span><span class="sxs-lookup"><span data-stu-id="a6e6c-152">OUTPUTS</span></span>

### <span data-ttu-id="a6e6c-153">ManagedStorageAccount 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="a6e6c-153">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="a6e6c-154">筆記</span><span class="sxs-lookup"><span data-stu-id="a6e6c-154">NOTES</span></span>

## <span data-ttu-id="a6e6c-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="a6e6c-155">RELATED LINKS</span></span>

[<span data-ttu-id="a6e6c-156">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a6e6c-156">AzureRM.KeyVault</span></span>](/powershell/module/azurerm.keyvault)
