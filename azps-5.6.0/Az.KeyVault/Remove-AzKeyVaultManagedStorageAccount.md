---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: ab126ee6bfc6a19f4a3a9997a75a01277437e42d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902050"
---
# <span data-ttu-id="277c3-101">Remove-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="277c3-101">Remove-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="277c3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="277c3-102">SYNOPSIS</span></span>
<span data-ttu-id="277c3-103">移除金鑰保存庫管理的 Azure 儲存體帳戶及所有相關聯的 SAS 定義。</span><span class="sxs-lookup"><span data-stu-id="277c3-103">Removes a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>

## <span data-ttu-id="277c3-104">語法</span><span class="sxs-lookup"><span data-stu-id="277c3-104">SYNTAX</span></span>

### <span data-ttu-id="277c3-105">ByDefinitionName (預設) </span><span class="sxs-lookup"><span data-stu-id="277c3-105">ByDefinitionName (Default)</span></span>
```
Remove-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="277c3-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="277c3-106">ByInputObject</span></span>
```
Remove-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-InRemovedState] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="277c3-107">描述</span><span class="sxs-lookup"><span data-stu-id="277c3-107">DESCRIPTION</span></span>
<span data-ttu-id="277c3-108">解除關聯 Azure 儲存空間帳戶與金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="277c3-108">Disassociates an Azure Storage Account from Key Vault.</span></span> <span data-ttu-id="277c3-109">這不會移除 Azure 儲存空間帳戶，但會從 Azure 金鑰保存庫管理帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="277c3-109">This does not remove an Azure Storage Account but removes the account keys from being managed by Azure Key Vault.</span></span> <span data-ttu-id="277c3-110">也會移除所有關聯的金鑰保存庫受管理的儲存空間 SAS 定義。</span><span class="sxs-lookup"><span data-stu-id="277c3-110">All associated Key Vault managed Storage SAS definitions are also removed.</span></span>

## <span data-ttu-id="277c3-111">例子</span><span class="sxs-lookup"><span data-stu-id="277c3-111">EXAMPLES</span></span>

### <span data-ttu-id="277c3-112">範例 1：移除金鑰保存庫管理的 Azure 儲存體帳戶及所有相關聯的 SAS 定義。</span><span class="sxs-lookup"><span data-stu-id="277c3-112">Example 1: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -PassThru

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

<span data-ttu-id="277c3-113">將 Azure 儲存空間帳戶的'mystorageaccount」從金鑰保存庫的'myvault'解除關聯，並停止金鑰保存庫管理其金鑰。</span><span class="sxs-lookup"><span data-stu-id="277c3-113">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="277c3-114">不會移除帳戶的'mystorageaccount'。</span><span class="sxs-lookup"><span data-stu-id="277c3-114">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="277c3-115">將會移除與此帳戶相關聯的所有金鑰保存庫受管理的儲存空間 SAS 定義。</span><span class="sxs-lookup"><span data-stu-id="277c3-115">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="277c3-116">範例 2：移除金鑰保存庫管理的 Azure 儲存空間帳戶，以及所有關聯的 SAS 定義，而不需要使用者確認。</span><span class="sxs-lookup"><span data-stu-id="277c3-116">Example 2: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions without user confirmation.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -PassThru -Force

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

<span data-ttu-id="277c3-117">將 Azure 儲存空間帳戶的'mystorageaccount」從金鑰保存庫的'myvault'解除關聯，並停止金鑰保存庫管理其金鑰。</span><span class="sxs-lookup"><span data-stu-id="277c3-117">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="277c3-118">不會移除帳戶的'mystorageaccount'。</span><span class="sxs-lookup"><span data-stu-id="277c3-118">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="277c3-119">將會移除與此帳戶相關聯的所有金鑰保存庫受管理的儲存空間 SAS 定義。</span><span class="sxs-lookup"><span data-stu-id="277c3-119">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="277c3-120">範例 3：從啟用 (的保存) 永久刪除金鑰保存庫管理的 Azure 儲存帳戶及所有相關聯的 SAS 定義。</span><span class="sxs-lookup"><span data-stu-id="277c3-120">Example 3: Permanently delete (purge) a Key Vault managed Azure Storage Account and all associated SAS definitions from a soft-delete-enabled vault.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' 
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
```

<span data-ttu-id="277c3-121">此範例假設此儲存庫已啟用柔刪除功能。</span><span class="sxs-lookup"><span data-stu-id="277c3-121">The example assumes that soft-delete is enabled for this vault.</span></span> <span data-ttu-id="277c3-122">檢查庫中實體的 Vault 屬性或 RecoveryLevel 屬性，確認是否有這種情況。</span><span class="sxs-lookup"><span data-stu-id="277c3-122">Verify whether that is the case by examining the vault properties, or the RecoveryLevel attribute of an entity in the vault.</span></span>
<span data-ttu-id="277c3-123">第一個 Cmdlet 會解除關聯 Azure 儲存空間帳戶的金鑰保存庫的 'mystorageaccount'，並停止金鑰保存庫管理其金鑰。</span><span class="sxs-lookup"><span data-stu-id="277c3-123">The first cmdlet disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="277c3-124">不會移除帳戶的'mystorageaccount'。</span><span class="sxs-lookup"><span data-stu-id="277c3-124">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="277c3-125">將會移除與此帳戶相關聯的所有金鑰保存庫受管理的儲存空間 SAS 定義。</span><span class="sxs-lookup"><span data-stu-id="277c3-125">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>
<span data-ttu-id="277c3-126">第二個 Cmdlet 會驗證儲存空間帳戶已被刪除，但可復原的狀態。</span><span class="sxs-lookup"><span data-stu-id="277c3-126">The second cmdlet verifies that the storage account is in a deleted, but recoverable state.</span></span> <span data-ttu-id="277c3-127">達到此狀態可能需要一些時間，請在嘗試之前允許 ~30 人。</span><span class="sxs-lookup"><span data-stu-id="277c3-127">Reaching this state may require some time, please allow ~30s before attempting.</span></span>
<span data-ttu-id="277c3-128">第三個 Cmdlet 會永久移除儲存空間帳戶 - 無法再復原。</span><span class="sxs-lookup"><span data-stu-id="277c3-128">The third cmdlet permanently removes the storage account - recovery will no longer be possible.</span></span>

## <span data-ttu-id="277c3-129">參數</span><span class="sxs-lookup"><span data-stu-id="277c3-129">PARAMETERS</span></span>

### <span data-ttu-id="277c3-130">-AccountName</span><span class="sxs-lookup"><span data-stu-id="277c3-130">-AccountName</span></span>
<span data-ttu-id="277c3-131">金鑰保存庫受管理的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="277c3-131">Key Vault managed storage account name.</span></span> <span data-ttu-id="277c3-132">Cmdlet 會從保存庫名稱、目前選取的環境和偽造的儲存帳戶名稱建構受管理儲存帳戶名稱的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="277c3-132">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="277c3-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="277c3-133">-DefaultProfile</span></span>
<span data-ttu-id="277c3-134">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="277c3-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="277c3-135">-強制</span><span class="sxs-lookup"><span data-stu-id="277c3-135">-Force</span></span>
<span data-ttu-id="277c3-136">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="277c3-136">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="277c3-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="277c3-137">-InputObject</span></span>
<span data-ttu-id="277c3-138">ManagedStorageAccount 物件。</span><span class="sxs-lookup"><span data-stu-id="277c3-138">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="277c3-139">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="277c3-139">-InRemovedState</span></span>
<span data-ttu-id="277c3-140">永久移除先前刪除的受管理儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="277c3-140">Permanently remove the previously deleted managed storage account.</span></span>

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

### <span data-ttu-id="277c3-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="277c3-141">-PassThru</span></span>
<span data-ttu-id="277c3-142">Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="277c3-142">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="277c3-143">如果指定此參數，Cmdlet 會返回已刪除的受管理儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="277c3-143">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="277c3-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="277c3-144">-VaultName</span></span>
<span data-ttu-id="277c3-145">儲存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="277c3-145">Vault name.</span></span>
<span data-ttu-id="277c3-146">Cmdlet 會根據名稱和目前選取的環境來建構庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="277c3-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="277c3-147">-確認</span><span class="sxs-lookup"><span data-stu-id="277c3-147">-Confirm</span></span>
<span data-ttu-id="277c3-148">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="277c3-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="277c3-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="277c3-149">-WhatIf</span></span>
<span data-ttu-id="277c3-150">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="277c3-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="277c3-151">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="277c3-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="277c3-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="277c3-152">CommonParameters</span></span>
<span data-ttu-id="277c3-153">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="277c3-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="277c3-154">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="277c3-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="277c3-155">輸入</span><span class="sxs-lookup"><span data-stu-id="277c3-155">INPUTS</span></span>

### <span data-ttu-id="277c3-156">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="277c3-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="277c3-157">輸出</span><span class="sxs-lookup"><span data-stu-id="277c3-157">OUTPUTS</span></span>

### <span data-ttu-id="277c3-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="277c3-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="277c3-159">筆記</span><span class="sxs-lookup"><span data-stu-id="277c3-159">NOTES</span></span>

## <span data-ttu-id="277c3-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="277c3-160">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

