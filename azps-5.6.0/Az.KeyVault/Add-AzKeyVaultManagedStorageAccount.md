---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/add-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 05c744050cc377eda01e309fb30122f83b9a8f5f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916409"
---
# <span data-ttu-id="d084a-101">Add-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d084a-101">Add-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="d084a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d084a-102">SYNOPSIS</span></span>
<span data-ttu-id="d084a-103">將現有的 Azure 儲存空間帳戶新增到指定的金鑰保存庫，讓金鑰保存庫服務管理其金鑰。</span><span class="sxs-lookup"><span data-stu-id="d084a-103">Adds an existing Azure Storage Account to the specified key vault for its keys to be managed by the Key Vault service.</span></span>

## <span data-ttu-id="d084a-104">語法</span><span class="sxs-lookup"><span data-stu-id="d084a-104">SYNTAX</span></span>

```
Add-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-AccountResourceId] <String>
 [-ActiveKeyName] <String> [-DisableAutoRegenerateKey] [-RegenerationPeriod <TimeSpan>] [-Disable]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d084a-105">描述</span><span class="sxs-lookup"><span data-stu-id="d084a-105">DESCRIPTION</span></span>
<span data-ttu-id="d084a-106">使用金鑰保存庫設定現有的 Azure 儲存空間帳戶，以儲存帳戶金鑰由金鑰保存庫管理。</span><span class="sxs-lookup"><span data-stu-id="d084a-106">Sets up an existing Azure Storage Account with Key Vault for Storage Account keys to be managed by Key Vault.</span></span> <span data-ttu-id="d084a-107">儲存空間帳戶必須已存在。</span><span class="sxs-lookup"><span data-stu-id="d084a-107">The Storage Account must already exist.</span></span> <span data-ttu-id="d084a-108">儲存金鑰永遠不會向來電者公開。</span><span class="sxs-lookup"><span data-stu-id="d084a-108">The Storage Keys are never exposed to caller.</span></span>
<span data-ttu-id="d084a-109">Key Vault 會自動重新產生，並依據週期切換使用中金鑰。</span><span class="sxs-lookup"><span data-stu-id="d084a-109">Key Vault auto regenerates and switches the active key based on the regeneration period.</span></span> <span data-ttu-id="d084a-110">請參閱 [Azure 金鑰保存庫受管理的儲存空間帳戶 - PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-overview-storage-keys-powershell) 以概觀瞭解此功能。</span><span class="sxs-lookup"><span data-stu-id="d084a-110">See [Azure Key Vault managed storage account - PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-overview-storage-keys-powershell) for an overview of this feature.</span></span>

## <span data-ttu-id="d084a-111">例子</span><span class="sxs-lookup"><span data-stu-id="d084a-111">EXAMPLES</span></span>

### <span data-ttu-id="d084a-112">範例 1：設定 Azure 儲存空間帳戶與金鑰保存庫以管理其金鑰</span><span class="sxs-lookup"><span data-stu-id="d084a-112">Example 1: Set an Azure Storage Account with Key Vault to manage its keys</span></span>
```powershell
PS C:\> $storage = Get-AzStorageAccount -ResourceGroupName "mystorageResourceGroup" -StorageAccountName "mystorage"
PS C:\> $servicePrincipal = Get-AzADServicePrincipal -ServicePrincipalName cfa8b339-82a2-471a-a3c9-0fc0be7a4093
PS C:\> New-AzRoleAssignment -ObjectId $servicePrincipal.Id -RoleDefinitionName 'Storage Account Key Operator Service Role' -Scope $storage.Id
PS C:\> $userPrincipalId = $(Get-AzADUser -SearchString "developer@contoso.com").Id
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName $keyVaultName -ObjectId $userPrincipalId -PermissionsToStorage get, set
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -AccountResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount' -ActiveKeyName 'key1' -RegenerationPeriod $regenerationPeriod

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key1
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="d084a-113">使用金鑰保存庫設定儲存空間帳戶，以讓金鑰保存庫管理其金鑰。</span><span class="sxs-lookup"><span data-stu-id="d084a-113">Sets a Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="d084a-114">使用中鍵組為'key1'。</span><span class="sxs-lookup"><span data-stu-id="d084a-114">The active key set is 'key1'.</span></span> <span data-ttu-id="d084a-115">此金鑰將用來產生 sas 權杖。</span><span class="sxs-lookup"><span data-stu-id="d084a-115">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="d084a-116">從此命令開始到更新期間之後，Key Vault 會重新產生 'key2' 鍵，並設定為使用中金鑰。</span><span class="sxs-lookup"><span data-stu-id="d084a-116">Key Vault will regenerate 'key2' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="d084a-117">此自動進位程式會持續在有 90 天差距的 'key1' 和 'key2' 之間。</span><span class="sxs-lookup"><span data-stu-id="d084a-117">This auto regeneration process will continue between 'key1' and 'key2' with a gap of 90 days.</span></span>

### <span data-ttu-id="d084a-118">範例 2：設定具有金鑰保存庫的傳統 Azure 儲存空間帳戶以管理其金鑰</span><span class="sxs-lookup"><span data-stu-id="d084a-118">Example 2: Set a Classic Azure Storage Account with Key Vault to manage its keys</span></span>
```powershell
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -AccountResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount' -ActiveKeyName 'Primary' -RegenerationPeriod $regenerationPeriod

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myvault/providers/Microsoft.Cl
                      assicStorage/storageAccounts/mystorageaccount
Active Key Name     : Primary
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="d084a-119">設定具有金鑰保存庫的傳統儲存空間帳戶，以讓金鑰保存庫管理其金鑰。</span><span class="sxs-lookup"><span data-stu-id="d084a-119">Sets a Classic Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="d084a-120">使用中鍵組是 'Primary'。</span><span class="sxs-lookup"><span data-stu-id="d084a-120">The active key set is 'Primary'.</span></span> <span data-ttu-id="d084a-121">此金鑰將用來產生 sas 權杖。</span><span class="sxs-lookup"><span data-stu-id="d084a-121">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="d084a-122">從此命令開始，金鑰庫將在更新期間之後重新產生次要金鑰，並設定為使用中金鑰。</span><span class="sxs-lookup"><span data-stu-id="d084a-122">Key Vault will regenerate 'Secondary' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="d084a-123">此自動回收程式會持續在主要和次要之間，差距為 90 天。</span><span class="sxs-lookup"><span data-stu-id="d084a-123">This auto regeneration process will continue between 'Primary' and 'Secondary' with a gap of 90 days.</span></span>

## <span data-ttu-id="d084a-124">參數</span><span class="sxs-lookup"><span data-stu-id="d084a-124">PARAMETERS</span></span>

### <span data-ttu-id="d084a-125">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d084a-125">-AccountName</span></span>
<span data-ttu-id="d084a-126">金鑰保存庫受管理的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="d084a-126">Key Vault managed storage account name.</span></span> <span data-ttu-id="d084a-127">Cmdlet 會從保存庫名稱、目前選取的環境和偽造的儲存帳戶名稱建構受管理儲存帳戶名稱的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="d084a-127">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="d084a-128">-AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="d084a-128">-AccountResourceId</span></span>
<span data-ttu-id="d084a-129">儲存帳戶的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d084a-129">Azure resource id of the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountResourceId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d084a-130">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="d084a-130">-ActiveKeyName</span></span>
<span data-ttu-id="d084a-131">您必須用來產生 sas 權杖的儲存空間帳戶金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="d084a-131">Name of the storage account key that must be used for generating sas tokens.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d084a-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d084a-132">-DefaultProfile</span></span>
<span data-ttu-id="d084a-133">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="d084a-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d084a-134">-停用</span><span class="sxs-lookup"><span data-stu-id="d084a-134">-Disable</span></span>
<span data-ttu-id="d084a-135">停用受管理的儲存空間帳戶金鑰用於產生 sas 權杖。</span><span class="sxs-lookup"><span data-stu-id="d084a-135">Disables the use of managed storage account's key for generation of sas tokens.</span></span>

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

### <span data-ttu-id="d084a-136">-DisableAutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="d084a-136">-DisableAutoRegenerateKey</span></span>
<span data-ttu-id="d084a-137">自動重新產生金鑰。</span><span class="sxs-lookup"><span data-stu-id="d084a-137">Auto regenerate key.</span></span> <span data-ttu-id="d084a-138">如果為 True，則受管理的儲存空間帳戶的非使用中金鑰會自動重新產生，成為更新週期後的新使用中金鑰。</span><span class="sxs-lookup"><span data-stu-id="d084a-138">If true, then the managed storage account's inactive key gets auto regenerated and becomes the new active key after the regeneration period.</span></span> <span data-ttu-id="d084a-139">如果為 False，則系統不會自動重新產生受管理儲存帳戶的金鑰。</span><span class="sxs-lookup"><span data-stu-id="d084a-139">If false, then the keys of managed storage account are not auto regenerated.</span></span>

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

### <span data-ttu-id="d084a-140">-更新更新</span><span class="sxs-lookup"><span data-stu-id="d084a-140">-RegenerationPeriod</span></span>
<span data-ttu-id="d084a-141">週期週期。</span><span class="sxs-lookup"><span data-stu-id="d084a-141">Regeneration period.</span></span> <span data-ttu-id="d084a-142">如果已啟用自動重新產生金鑰，此值會指定受管理儲存帳戶的非使用中金鑰自動重新產生，成為新的使用中金鑰的時間窗格。</span><span class="sxs-lookup"><span data-stu-id="d084a-142">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the new active key.</span></span>

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

### <span data-ttu-id="d084a-143">-標記</span><span class="sxs-lookup"><span data-stu-id="d084a-143">-Tag</span></span>
<span data-ttu-id="d084a-144">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="d084a-144">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d084a-145">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="d084a-145">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d084a-146">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d084a-146">-VaultName</span></span>
<span data-ttu-id="d084a-147">儲存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="d084a-147">Vault name.</span></span>
<span data-ttu-id="d084a-148">Cmdlet 會根據名稱和目前選取的環境來建構庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="d084a-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="d084a-149">-確認</span><span class="sxs-lookup"><span data-stu-id="d084a-149">-Confirm</span></span>
<span data-ttu-id="d084a-150">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d084a-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d084a-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d084a-151">-WhatIf</span></span>
<span data-ttu-id="d084a-152">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d084a-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d084a-153">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d084a-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d084a-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d084a-154">CommonParameters</span></span>
<span data-ttu-id="d084a-155">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d084a-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d084a-156">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d084a-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d084a-157">輸入</span><span class="sxs-lookup"><span data-stu-id="d084a-157">INPUTS</span></span>

### <span data-ttu-id="d084a-158">System.String</span><span class="sxs-lookup"><span data-stu-id="d084a-158">System.String</span></span>

### <span data-ttu-id="d084a-159">System.Nullable'1[[System.TimeSpan， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d084a-159">System.Nullable\`1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d084a-160">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="d084a-160">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d084a-161">輸出</span><span class="sxs-lookup"><span data-stu-id="d084a-161">OUTPUTS</span></span>

### <span data-ttu-id="d084a-162">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d084a-162">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="d084a-163">筆記</span><span class="sxs-lookup"><span data-stu-id="d084a-163">NOTES</span></span>

## <span data-ttu-id="d084a-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="d084a-164">RELATED LINKS</span></span>

[<span data-ttu-id="d084a-165">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d084a-165">Az.KeyVault</span></span>](/powershell/module/az.keyvault)
