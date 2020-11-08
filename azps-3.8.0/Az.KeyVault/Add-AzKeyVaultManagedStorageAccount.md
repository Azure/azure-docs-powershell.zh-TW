---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 90f6347346c0967e29917ffe56e7ba13f7e705de
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93798697"
---
# <span data-ttu-id="524ad-101">Add-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="524ad-101">Add-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="524ad-102">摘要</span><span class="sxs-lookup"><span data-stu-id="524ad-102">SYNOPSIS</span></span>
<span data-ttu-id="524ad-103">將現有的 Azure 儲存空間帳戶新增到指定的 [金鑰保存庫]，以便由主要 Vault 服務來管理其金鑰。</span><span class="sxs-lookup"><span data-stu-id="524ad-103">Adds an existing Azure Storage Account to the specified key vault for its keys to be managed by the Key Vault service.</span></span>

## <span data-ttu-id="524ad-104">句法</span><span class="sxs-lookup"><span data-stu-id="524ad-104">SYNTAX</span></span>

```
Add-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-AccountResourceId] <String>
 [-ActiveKeyName] <String> [-DisableAutoRegenerateKey] [-RegenerationPeriod <TimeSpan>] [-Disable]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="524ad-105">說明</span><span class="sxs-lookup"><span data-stu-id="524ad-105">DESCRIPTION</span></span>
<span data-ttu-id="524ad-106">針對儲存帳戶金鑰的金鑰保存庫設定現有的 Azure 儲存空間帳戶，由主要保存庫管理。</span><span class="sxs-lookup"><span data-stu-id="524ad-106">Sets up an existing Azure Storage Account with Key Vault for Storage Account keys to be managed by Key Vault.</span></span> <span data-ttu-id="524ad-107">儲存空間帳戶必須已經存在。</span><span class="sxs-lookup"><span data-stu-id="524ad-107">The Storage Account must already exist.</span></span> <span data-ttu-id="524ad-108">存儲金鑰永遠不會暴露給來電者。</span><span class="sxs-lookup"><span data-stu-id="524ad-108">The Storage Keys are never exposed to caller.</span></span>
<span data-ttu-id="524ad-109">金鑰 Vault 自動再生，然後根據再生期間來切換使用中的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="524ad-109">Key Vault auto regenerates and switches the active key based on the regeneration period.</span></span> <span data-ttu-id="524ad-110">如需此功能的概要，請參閱 [Azure 金鑰 Vault 管理的儲存空間帳戶-PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-overview-storage-keys-powershell) 。</span><span class="sxs-lookup"><span data-stu-id="524ad-110">See [Azure Key Vault managed storage account - PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-overview-storage-keys-powershell) for an overview of this feature.</span></span>

## <span data-ttu-id="524ad-111">示例</span><span class="sxs-lookup"><span data-stu-id="524ad-111">EXAMPLES</span></span>

### <span data-ttu-id="524ad-112">範例1：使用金鑰保存庫設定 Azure 儲存空間帳戶來管理其金鑰</span><span class="sxs-lookup"><span data-stu-id="524ad-112">Example 1: Set an Azure Storage Account with Key Vault to manage its keys</span></span>
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

<span data-ttu-id="524ad-113">針對金鑰保存庫設定儲存空間帳戶，以便由主要電子倉庫管理其金鑰。</span><span class="sxs-lookup"><span data-stu-id="524ad-113">Sets a Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="524ad-114">[作用中金鑰] 設定為 "key1"。</span><span class="sxs-lookup"><span data-stu-id="524ad-114">The active key set is 'key1'.</span></span> <span data-ttu-id="524ad-115">此金鑰將用來產生 sas 權杖。</span><span class="sxs-lookup"><span data-stu-id="524ad-115">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="524ad-116">[主要電子倉庫] 會在此命令時間之後的 [再生期間] 重新產生「key2」金鑰，並將它設為作用中的按鍵。</span><span class="sxs-lookup"><span data-stu-id="524ad-116">Key Vault will regenerate 'key2' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="524ad-117">這個自動重新產生程式將會在 [key1] 與 "key2" 之間繼續，而間隔為90天。</span><span class="sxs-lookup"><span data-stu-id="524ad-117">This auto regeneration process will continue between 'key1' and 'key2' with a gap of 90 days.</span></span>

### <span data-ttu-id="524ad-118">範例2：使用金鑰保存庫設定傳統 Azure 儲存空間帳戶來管理其金鑰</span><span class="sxs-lookup"><span data-stu-id="524ad-118">Example 2: Set a Classic Azure Storage Account with Key Vault to manage its keys</span></span>
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

<span data-ttu-id="524ad-119">使用 [金鑰保存庫] 來設定傳統儲存空間帳戶，以由主要電子倉庫管理其金鑰。</span><span class="sxs-lookup"><span data-stu-id="524ad-119">Sets a Classic Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="524ad-120">[作用中金鑰] 設定為 [Primary]。</span><span class="sxs-lookup"><span data-stu-id="524ad-120">The active key set is 'Primary'.</span></span> <span data-ttu-id="524ad-121">此金鑰將用來產生 sas 權杖。</span><span class="sxs-lookup"><span data-stu-id="524ad-121">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="524ad-122">[主要電子倉庫] 會在此命令時間之後的 [再生期間] 重新產生 [次要] 金鑰，並將它設為作用中的按鍵。</span><span class="sxs-lookup"><span data-stu-id="524ad-122">Key Vault will regenerate 'Secondary' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="524ad-123">這個自動重新產生程式將會在「主要」和「次要」之間繼續，而間隔則是90天。</span><span class="sxs-lookup"><span data-stu-id="524ad-123">This auto regeneration process will continue between 'Primary' and 'Secondary' with a gap of 90 days.</span></span>

## <span data-ttu-id="524ad-124">參數</span><span class="sxs-lookup"><span data-stu-id="524ad-124">PARAMETERS</span></span>

### <span data-ttu-id="524ad-125">-AccountName</span><span class="sxs-lookup"><span data-stu-id="524ad-125">-AccountName</span></span>
<span data-ttu-id="524ad-126">主要保存庫管理的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="524ad-126">Key Vault managed storage account name.</span></span> <span data-ttu-id="524ad-127">Cmdlet 會從保存庫名稱、目前已選取的環境及 manged 儲存空間帳戶名稱構造受管理儲存空間帳戶名稱的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="524ad-127">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="524ad-128">-AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="524ad-128">-AccountResourceId</span></span>
<span data-ttu-id="524ad-129">儲存空間帳戶的 Azure 資源 id。</span><span class="sxs-lookup"><span data-stu-id="524ad-129">Azure resource id of the storage account.</span></span>

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

### <span data-ttu-id="524ad-130">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="524ad-130">-ActiveKeyName</span></span>
<span data-ttu-id="524ad-131">必須用來產生 sas 權杖的儲存空間帳戶金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="524ad-131">Name of the storage account key that must be used for generating sas tokens.</span></span>

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

### <span data-ttu-id="524ad-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="524ad-132">-DefaultProfile</span></span>
<span data-ttu-id="524ad-133">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="524ad-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="524ad-134">-停用</span><span class="sxs-lookup"><span data-stu-id="524ad-134">-Disable</span></span>
<span data-ttu-id="524ad-135">停用受管理的儲存帳戶金鑰來產生 sas 權杖。</span><span class="sxs-lookup"><span data-stu-id="524ad-135">Disables the use of managed storage account's key for generation of sas tokens.</span></span>

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

### <span data-ttu-id="524ad-136">-DisableAutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="524ad-136">-DisableAutoRegenerateKey</span></span>
<span data-ttu-id="524ad-137">自動重新產生金鑰。</span><span class="sxs-lookup"><span data-stu-id="524ad-137">Auto regenerate key.</span></span> <span data-ttu-id="524ad-138">如果是 true，則受管理的儲存空間帳戶的非作用中金鑰會自動重新產生，並在再生期間成為新的作用中索引鍵。</span><span class="sxs-lookup"><span data-stu-id="524ad-138">If true, then the managed storage account's inactive key gets auto regenerated and becomes the new active key after the regeneration period.</span></span> <span data-ttu-id="524ad-139">如果是 false，系統就不會自動重新產生受管理的儲存空間帳戶的金鑰。</span><span class="sxs-lookup"><span data-stu-id="524ad-139">If false, then the keys of managed storage account are not auto regenerated.</span></span>

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

### <span data-ttu-id="524ad-140">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="524ad-140">-RegenerationPeriod</span></span>
<span data-ttu-id="524ad-141">[再生期間]。</span><span class="sxs-lookup"><span data-stu-id="524ad-141">Regeneration period.</span></span> <span data-ttu-id="524ad-142">如果已啟用自動重新產生鍵，此值會指定管理儲存空間帳戶停用 keygets 自動重新產生並成為新的作用中金鑰之後的時間跨度。</span><span class="sxs-lookup"><span data-stu-id="524ad-142">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the new active key.</span></span>

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

### <span data-ttu-id="524ad-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="524ad-143">-Tag</span></span>
<span data-ttu-id="524ad-144">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="524ad-144">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="524ad-145">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="524ad-145">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="524ad-146">-VaultName</span><span class="sxs-lookup"><span data-stu-id="524ad-146">-VaultName</span></span>
<span data-ttu-id="524ad-147">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="524ad-147">Vault name.</span></span>
<span data-ttu-id="524ad-148">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="524ad-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="524ad-149">-確認</span><span class="sxs-lookup"><span data-stu-id="524ad-149">-Confirm</span></span>
<span data-ttu-id="524ad-150">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="524ad-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="524ad-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="524ad-151">-WhatIf</span></span>
<span data-ttu-id="524ad-152">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="524ad-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="524ad-153">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="524ad-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="524ad-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="524ad-154">CommonParameters</span></span>
<span data-ttu-id="524ad-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="524ad-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="524ad-156">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="524ad-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="524ad-157">輸入</span><span class="sxs-lookup"><span data-stu-id="524ad-157">INPUTS</span></span>

### <span data-ttu-id="524ad-158">System.object</span><span class="sxs-lookup"><span data-stu-id="524ad-158">System.String</span></span>

### <span data-ttu-id="524ad-159">CoreLib "1 [System. Timespan.zero，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="524ad-159">System.Nullable\`1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="524ad-160">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="524ad-160">System.Collections.Hashtable</span></span>

## <span data-ttu-id="524ad-161">輸出</span><span class="sxs-lookup"><span data-stu-id="524ad-161">OUTPUTS</span></span>

### <span data-ttu-id="524ad-162">PSKeyVaultManagedStorageAccount 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="524ad-162">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="524ad-163">筆記</span><span class="sxs-lookup"><span data-stu-id="524ad-163">NOTES</span></span>

## <span data-ttu-id="524ad-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="524ad-164">RELATED LINKS</span></span>

[<span data-ttu-id="524ad-165">Az. KeyVault</span><span class="sxs-lookup"><span data-stu-id="524ad-165">Az.KeyVault</span></span>](/powershell/module/az.keyvault)