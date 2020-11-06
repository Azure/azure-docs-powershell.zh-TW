---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 84c6df195b0d24e5096748a4a5e3fd8360665831
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446785"
---
# <span data-ttu-id="5bcf4-101">Update-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5bcf4-101">Update-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="5bcf4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5bcf4-102">SYNOPSIS</span></span>
<span data-ttu-id="5bcf4-103">更新主要電子倉庫管理的 Azure 儲存空間帳戶的可編輯屬性。</span><span class="sxs-lookup"><span data-stu-id="5bcf4-103">Update editable attributes of a Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5bcf4-104">句法</span><span class="sxs-lookup"><span data-stu-id="5bcf4-104">SYNTAX</span></span>

```
Update-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-ActiveKeyName <String>] [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5bcf4-105">說明</span><span class="sxs-lookup"><span data-stu-id="5bcf4-105">DESCRIPTION</span></span>
<span data-ttu-id="5bcf4-106">更新主要電子倉庫管理的 Azure 儲存空間帳戶的可編輯屬性。</span><span class="sxs-lookup"><span data-stu-id="5bcf4-106">Update the editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="5bcf4-107">示例</span><span class="sxs-lookup"><span data-stu-id="5bcf4-107">EXAMPLES</span></span>

### <span data-ttu-id="5bcf4-108">範例1：在主要電子倉庫管理的 Azure 儲存空間帳戶上，將 active key 更新為 ' key2」。</span><span class="sxs-lookup"><span data-stu-id="5bcf4-108">Example 1:Update the active key to 'key2' on a Key Vault managed Azure Storage Account.</span></span>
```
PS C:\> Update-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -ActiveKeyName 'key2'
```

<span data-ttu-id="5bcf4-109">將主要電子倉庫管理的 Azure 儲存空間帳戶啟用金鑰更新為 ' key2」。</span><span class="sxs-lookup"><span data-stu-id="5bcf4-109">Updates the Key Vault managed Azure Storage Account active key to 'key2'.</span></span> <span data-ttu-id="5bcf4-110">在此更新之後，"key2" 將用於產生 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="5bcf4-110">'key2' will be used to generate SAS tokens after this update.</span></span>

## <span data-ttu-id="5bcf4-111">參數</span><span class="sxs-lookup"><span data-stu-id="5bcf4-111">PARAMETERS</span></span>

### <span data-ttu-id="5bcf4-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5bcf4-112">-AccountName</span></span>
<span data-ttu-id="5bcf4-113">主要保存庫管理的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="5bcf4-113">Key Vault managed storage account name.</span></span> <span data-ttu-id="5bcf4-114">Cmdlet 會從保存庫名稱、目前已選取的環境及 manged 儲存空間帳戶名稱構造受管理儲存空間帳戶名稱的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="5bcf4-114">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bcf4-115">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="5bcf4-115">-ActiveKeyName</span></span>
<span data-ttu-id="5bcf4-116">Active 項名稱。</span><span class="sxs-lookup"><span data-stu-id="5bcf4-116">Active key name.</span></span>
<span data-ttu-id="5bcf4-117">如果未指定，受管理儲存空間帳戶的作用中金鑰名稱的現有值會保持不變</span><span class="sxs-lookup"><span data-stu-id="5bcf4-117">If not specified, the existing value of managed storage account's active key name remains unchanged</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bcf4-118">-AutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="5bcf4-118">-AutoRegenerateKey</span></span>
<span data-ttu-id="5bcf4-119">自動重新產生金鑰。</span><span class="sxs-lookup"><span data-stu-id="5bcf4-119">Auto regenerate key.</span></span>
<span data-ttu-id="5bcf4-120">如果未指定，則受管理儲存帳戶的自動重新產生鍵的現有值會保持不變</span><span class="sxs-lookup"><span data-stu-id="5bcf4-120">If not specified, the existing value of auto regenerate key of managed storage account remains unchanged</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bcf4-121">-確認</span><span class="sxs-lookup"><span data-stu-id="5bcf4-121">-Confirm</span></span>
<span data-ttu-id="5bcf4-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5bcf4-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bcf4-123">-啟用</span><span class="sxs-lookup"><span data-stu-id="5bcf4-123">-Enable</span></span>
<span data-ttu-id="5bcf4-124">如果有的話，可以將受管理的儲存空間帳戶金鑰用於 sas 權杖產生（如果值為 true）。</span><span class="sxs-lookup"><span data-stu-id="5bcf4-124">If present, enables a use of a managed storage account key for sas token generation if value is true.</span></span> <span data-ttu-id="5bcf4-125">如果值為 false，則停用針對 sas 權杖產生使用受管理的儲存空間帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="5bcf4-125">Disables use of a managed storage account key for sas token generation if value is false.</span></span> <span data-ttu-id="5bcf4-126">如果未指定，儲存帳戶的啟用/停用狀態的現有值會保持不變。</span><span class="sxs-lookup"><span data-stu-id="5bcf4-126">If not specified, the existing value of the storage account's enabled/disabled state remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bcf4-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5bcf4-127">-PassThru</span></span>
<span data-ttu-id="5bcf4-128">Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="5bcf4-128">Cmdlet does not return object by default.</span></span> <span data-ttu-id="5bcf4-129">如果已指定此開關，請傳回受管理的儲存空間帳戶物件。</span><span class="sxs-lookup"><span data-stu-id="5bcf4-129">If this switch is specified, return managed storage account object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bcf4-130">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="5bcf4-130">-RegenerationPeriod</span></span>
<span data-ttu-id="5bcf4-131">[再生期間]。</span><span class="sxs-lookup"><span data-stu-id="5bcf4-131">Regeneration period.</span></span> <span data-ttu-id="5bcf4-132">如果啟用自動重新產生鍵，此值會指定要在已管理的儲存空間帳戶停用 keygets 自動重新產生並成為作用中金鑰之後的時間跨度。</span><span class="sxs-lookup"><span data-stu-id="5bcf4-132">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the active key.</span></span> <span data-ttu-id="5bcf4-133">如果未指定，受管理的儲存帳戶金鑰的現有值會保持不變</span><span class="sxs-lookup"><span data-stu-id="5bcf4-133">If not specified, the existing value of regeneration period of keys of managed storage account remains unchanged</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bcf4-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="5bcf4-134">-Tag</span></span>
<span data-ttu-id="5bcf4-135">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="5bcf4-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5bcf4-136">例如：</span><span class="sxs-lookup"><span data-stu-id="5bcf4-136">For example:</span></span>

<span data-ttu-id="5bcf4-137">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="5bcf4-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bcf4-138">-VaultName</span><span class="sxs-lookup"><span data-stu-id="5bcf4-138">-VaultName</span></span>
<span data-ttu-id="5bcf4-139">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="5bcf4-139">Vault name.</span></span>
<span data-ttu-id="5bcf4-140">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="5bcf4-140">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bcf4-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bcf4-141">-WhatIf</span></span>
<span data-ttu-id="5bcf4-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5bcf4-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bcf4-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5bcf4-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bcf4-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bcf4-144">-DefaultProfile</span></span>
<span data-ttu-id="5bcf4-145">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5bcf4-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5bcf4-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bcf4-146">CommonParameters</span></span>
<span data-ttu-id="5bcf4-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5bcf4-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bcf4-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5bcf4-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bcf4-149">輸入</span><span class="sxs-lookup"><span data-stu-id="5bcf4-149">INPUTS</span></span>

## <span data-ttu-id="5bcf4-150">輸出</span><span class="sxs-lookup"><span data-stu-id="5bcf4-150">OUTPUTS</span></span>

### <span data-ttu-id="5bcf4-151">ManagedStorageAccount 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="5bcf4-151">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="5bcf4-152">筆記</span><span class="sxs-lookup"><span data-stu-id="5bcf4-152">NOTES</span></span>

## <span data-ttu-id="5bcf4-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="5bcf4-153">RELATED LINKS</span></span>

[<span data-ttu-id="5bcf4-154">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5bcf4-154">AzureRM.KeyVault</span></span>](/powershell/module/azurerm.keyvault)
