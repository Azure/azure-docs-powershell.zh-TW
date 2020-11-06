---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: c5f96c2e4840d35ac79e78c6778cb66ddc034180
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449112"
---
# <span data-ttu-id="1e1d2-101">Remove-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1e1d2-101">Remove-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="1e1d2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1e1d2-102">SYNOPSIS</span></span>
<span data-ttu-id="1e1d2-103">移除主要電子倉庫管理的 Azure 儲存空間帳戶和所有相關的 SAS 定義。</span><span class="sxs-lookup"><span data-stu-id="1e1d2-103">Removes a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e1d2-104">句法</span><span class="sxs-lookup"><span data-stu-id="1e1d2-104">SYNTAX</span></span>

### <span data-ttu-id="1e1d2-105">ByDefinitionName (預設) </span><span class="sxs-lookup"><span data-stu-id="1e1d2-105">ByDefinitionName (Default)</span></span>
```
Remove-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-InRemovedState]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e1d2-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1e1d2-106">ByInputObject</span></span>
```
Remove-AzureKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-InRemovedState] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1e1d2-107">說明</span><span class="sxs-lookup"><span data-stu-id="1e1d2-107">DESCRIPTION</span></span>
<span data-ttu-id="1e1d2-108">解除與 [主要電子倉庫] 的 Azure 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="1e1d2-108">Disassociates an Azure Storage Account from Key Vault.</span></span> <span data-ttu-id="1e1d2-109">這不會移除 Azure 儲存空間帳戶，但會將帳戶金鑰從 Azure 金鑰保存庫管理。</span><span class="sxs-lookup"><span data-stu-id="1e1d2-109">This does not remove an Azure Storage Account but removes the account keys from being managed by Azure Key Vault.</span></span> <span data-ttu-id="1e1d2-110">同時也會移除所有相關聯的主要電子倉庫管理的儲存 SAS 定義。</span><span class="sxs-lookup"><span data-stu-id="1e1d2-110">All associated Key Vault managed Storage SAS definitions are also removed.</span></span>

## <span data-ttu-id="1e1d2-111">示例</span><span class="sxs-lookup"><span data-stu-id="1e1d2-111">EXAMPLES</span></span>

### <span data-ttu-id="1e1d2-112">範例1：移除主要電子倉庫管理的 Azure 儲存空間帳戶和所有相關的 SAS 定義。</span><span class="sxs-lookup"><span data-stu-id="1e1d2-112">Example 1: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -PassThru

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="1e1d2-113">解除 Azure 儲存空間帳戶 "mystorageaccount" 與主要保存庫「myvault」的對應，並停止金鑰保存庫的管理其金鑰。</span><span class="sxs-lookup"><span data-stu-id="1e1d2-113">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="1e1d2-114">將不會移除帳戶 [mystorageaccount]。</span><span class="sxs-lookup"><span data-stu-id="1e1d2-114">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="1e1d2-115">將會移除與此帳戶相關聯的所有主要電子倉庫管理的儲存空間 SAS 定義。</span><span class="sxs-lookup"><span data-stu-id="1e1d2-115">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="1e1d2-116">範例2：移除主要電子倉庫管理的 Azure 儲存空間帳戶和所有相關的 SAS 定義，而不需使用者確認。</span><span class="sxs-lookup"><span data-stu-id="1e1d2-116">Example 2: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions without user confirmation.</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -PassThru -Force

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="1e1d2-117">解除 Azure 儲存空間帳戶 "mystorageaccount" 與主要保存庫「myvault」的對應，並停止金鑰保存庫的管理其金鑰。</span><span class="sxs-lookup"><span data-stu-id="1e1d2-117">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="1e1d2-118">將不會移除帳戶 [mystorageaccount]。</span><span class="sxs-lookup"><span data-stu-id="1e1d2-118">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="1e1d2-119">將會移除與此帳戶相關聯的所有主要電子倉庫管理的儲存空間 SAS 定義。</span><span class="sxs-lookup"><span data-stu-id="1e1d2-119">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="1e1d2-120">範例3：永久刪除 (清除) 主要 Vault 管理 Azure 儲存空間帳戶，以及從虛刪除的電子倉庫中所有相關的 SAS 定義。</span><span class="sxs-lookup"><span data-stu-id="1e1d2-120">Example 3: Permanently delete (purge) a Key Vault managed Azure Storage Account and all associated SAS definitions from a soft-delete-enabled vault.</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' 
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
```

<span data-ttu-id="1e1d2-121">此範例假設已針對此電子倉庫啟用 [虛刪除]。</span><span class="sxs-lookup"><span data-stu-id="1e1d2-121">The example assumes that soft-delete is enabled for this vault.</span></span> <span data-ttu-id="1e1d2-122">檢查保存庫的屬性或保存庫中某個實體的 RecoveryLevel 屬性，以驗證該案例是否為事例。</span><span class="sxs-lookup"><span data-stu-id="1e1d2-122">Verify whether that is the case by examining the vault properties, or the RecoveryLevel attribute of an entity in the vault.</span></span>
<span data-ttu-id="1e1d2-123">第一個 Cmdlet 解除 Azure 儲存空間帳戶 ' mystorageaccount」與主要保存庫 ' myvault」的對應，並停止金鑰保存庫的管理其金鑰。</span><span class="sxs-lookup"><span data-stu-id="1e1d2-123">The first cmdlet disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="1e1d2-124">將不會移除帳戶 [mystorageaccount]。</span><span class="sxs-lookup"><span data-stu-id="1e1d2-124">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="1e1d2-125">將會移除與此帳戶相關聯的所有主要電子倉庫管理的儲存空間 SAS 定義。</span><span class="sxs-lookup"><span data-stu-id="1e1d2-125">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>
<span data-ttu-id="1e1d2-126">第二個 Cmdlet 會驗證儲存空間帳戶是否處於已刪除，但可復原的狀態。</span><span class="sxs-lookup"><span data-stu-id="1e1d2-126">The second cmdlet verifies that the storage account is in a deleted, but recoverable state.</span></span> <span data-ttu-id="1e1d2-127">達到此狀態可能需要一些時間，請在嘗試之前先允許 ~ 30s。</span><span class="sxs-lookup"><span data-stu-id="1e1d2-127">Reaching this state may require some time, please allow ~30s before attempting.</span></span>
<span data-ttu-id="1e1d2-128">第三個 Cmdlet 會永久移除 [儲存空間帳戶]-將不再可能恢復。</span><span class="sxs-lookup"><span data-stu-id="1e1d2-128">The third cmdlet permanently removes the storage account - recovery will no longer be possible.</span></span>

## <span data-ttu-id="1e1d2-129">參數</span><span class="sxs-lookup"><span data-stu-id="1e1d2-129">PARAMETERS</span></span>

### <span data-ttu-id="1e1d2-130">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1e1d2-130">-AccountName</span></span>
<span data-ttu-id="1e1d2-131">主要保存庫管理的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="1e1d2-131">Key Vault managed storage account name.</span></span> <span data-ttu-id="1e1d2-132">Cmdlet 會從保存庫名稱、目前已選取的環境及 manged 儲存空間帳戶名稱構造受管理儲存空間帳戶名稱的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="1e1d2-132">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e1d2-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e1d2-133">-DefaultProfile</span></span>
<span data-ttu-id="1e1d2-134">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="1e1d2-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e1d2-135">-Force</span><span class="sxs-lookup"><span data-stu-id="1e1d2-135">-Force</span></span>
<span data-ttu-id="1e1d2-136">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="1e1d2-136">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1e1d2-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e1d2-137">-InputObject</span></span>
<span data-ttu-id="1e1d2-138">ManagedStorageAccount 物件。</span><span class="sxs-lookup"><span data-stu-id="1e1d2-138">ManagedStorageAccount object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e1d2-139">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="1e1d2-139">-InRemovedState</span></span>
<span data-ttu-id="1e1d2-140">永久移除先前刪除的受管理儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="1e1d2-140">Permanently remove the previously deleted managed storage account.</span></span>

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

### <span data-ttu-id="1e1d2-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1e1d2-141">-PassThru</span></span>
<span data-ttu-id="1e1d2-142">Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="1e1d2-142">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="1e1d2-143">如果指定此開關，則 Cmdlet 會傳回已刪除的受管理儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="1e1d2-143">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="1e1d2-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="1e1d2-144">-VaultName</span></span>
<span data-ttu-id="1e1d2-145">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="1e1d2-145">Vault name.</span></span>
<span data-ttu-id="1e1d2-146">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="1e1d2-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e1d2-147">-確認</span><span class="sxs-lookup"><span data-stu-id="1e1d2-147">-Confirm</span></span>
<span data-ttu-id="1e1d2-148">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1e1d2-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e1d2-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e1d2-149">-WhatIf</span></span>
<span data-ttu-id="1e1d2-150">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1e1d2-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e1d2-151">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1e1d2-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e1d2-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e1d2-152">CommonParameters</span></span>
<span data-ttu-id="1e1d2-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1e1d2-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e1d2-154">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1e1d2-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e1d2-155">輸入</span><span class="sxs-lookup"><span data-stu-id="1e1d2-155">INPUTS</span></span>

### <span data-ttu-id="1e1d2-156">PSKeyVaultManagedStorageAccountIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="1e1d2-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>
<span data-ttu-id="1e1d2-157">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="1e1d2-157">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="1e1d2-158">輸出</span><span class="sxs-lookup"><span data-stu-id="1e1d2-158">OUTPUTS</span></span>

### <span data-ttu-id="1e1d2-159">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1e1d2-159">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="1e1d2-160">筆記</span><span class="sxs-lookup"><span data-stu-id="1e1d2-160">NOTES</span></span>

## <span data-ttu-id="1e1d2-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="1e1d2-161">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)
