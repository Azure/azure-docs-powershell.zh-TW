---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
ms.openlocfilehash: 4bd6db0cf8dce4270e14337ee1168002618e3dc3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93799905"
---
# <span data-ttu-id="6762b-101">Add-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6762b-101">Add-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="6762b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6762b-102">SYNOPSIS</span></span>
<span data-ttu-id="6762b-103">將現有的 Azure 儲存空間帳戶新增到指定的 [金鑰保存庫]，以便由主要 Vault 服務來管理其金鑰。</span><span class="sxs-lookup"><span data-stu-id="6762b-103">Adds an existing Azure Storage Account to the specified key vault for its keys to be managed by the Key Vault service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6762b-104">句法</span><span class="sxs-lookup"><span data-stu-id="6762b-104">SYNTAX</span></span>

```
Add-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-AccountResourceId] <String> [-ActiveKeyName] <String> [-DisableAutoRegenerateKey]
 [-RegenerationPeriod <TimeSpan>] [-Disable] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6762b-105">說明</span><span class="sxs-lookup"><span data-stu-id="6762b-105">DESCRIPTION</span></span>
<span data-ttu-id="6762b-106">針對儲存帳戶金鑰的金鑰保存庫設定現有的 Azure 儲存空間帳戶，由主要保存庫管理。</span><span class="sxs-lookup"><span data-stu-id="6762b-106">Sets up an existing Azure Storage Account with Key Vault for Storage Account keys to be managed by Key Vault.</span></span> <span data-ttu-id="6762b-107">儲存空間帳戶必須已經存在。</span><span class="sxs-lookup"><span data-stu-id="6762b-107">The Storage Account must already exist.</span></span> <span data-ttu-id="6762b-108">存儲金鑰永遠不會暴露給來電者。</span><span class="sxs-lookup"><span data-stu-id="6762b-108">The Storage Keys are never exposed to caller.</span></span>
<span data-ttu-id="6762b-109">金鑰 Vault 自動再生，然後根據再生期間來切換使用中的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="6762b-109">Key Vault auto regenerates and switches the active key based on the regeneration period.</span></span>

## <span data-ttu-id="6762b-110">示例</span><span class="sxs-lookup"><span data-stu-id="6762b-110">EXAMPLES</span></span>

### <span data-ttu-id="6762b-111">範例1：使用金鑰保存庫設定 Azure 儲存空間帳戶來管理其金鑰</span><span class="sxs-lookup"><span data-stu-id="6762b-111">Example 1: Set an Azure Storage Account with Key Vault to manage its keys</span></span>
```
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -ResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount' -ActiveKeyName 'key1' -RegenerationPeriod $regenerationPeriod
```

<span data-ttu-id="6762b-112">針對金鑰保存庫設定儲存空間帳戶，以便由主要電子倉庫管理其金鑰。</span><span class="sxs-lookup"><span data-stu-id="6762b-112">Sets a Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="6762b-113">[作用中金鑰] 設定為 "key1"。</span><span class="sxs-lookup"><span data-stu-id="6762b-113">The active key set is 'key1'.</span></span> <span data-ttu-id="6762b-114">此金鑰將用來產生 sas 權杖。</span><span class="sxs-lookup"><span data-stu-id="6762b-114">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="6762b-115">[主要電子倉庫] 會在此命令時間之後的 [再生期間] 重新產生「key2」金鑰，並將它設為作用中的按鍵。</span><span class="sxs-lookup"><span data-stu-id="6762b-115">Key Vault will regenerate 'key2' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="6762b-116">這個自動重新產生程式將會在 [key1] 與 "key2" 之間繼續，而間隔為90天。</span><span class="sxs-lookup"><span data-stu-id="6762b-116">This auto regeneration process will continue between 'key1' and 'key2' with a gap of 90 days.</span></span>

### <span data-ttu-id="6762b-117">範例2：使用金鑰保存庫設定傳統 Azure 儲存空間帳戶來管理其金鑰</span><span class="sxs-lookup"><span data-stu-id="6762b-117">Example 2: Set a Classic Azure Storage Account with Key Vault to manage its keys</span></span>
```
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -ResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount' -ActiveKeyName 'Primary' -RegenerationPeriod $regenerationPeriod
```

<span data-ttu-id="6762b-118">使用 [金鑰保存庫] 來設定傳統儲存空間帳戶，以由主要電子倉庫管理其金鑰。</span><span class="sxs-lookup"><span data-stu-id="6762b-118">Sets a Classic Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="6762b-119">[作用中金鑰] 設定為 [Primary]。</span><span class="sxs-lookup"><span data-stu-id="6762b-119">The active key set is 'Primary'.</span></span> <span data-ttu-id="6762b-120">此金鑰將用來產生 sas 權杖。</span><span class="sxs-lookup"><span data-stu-id="6762b-120">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="6762b-121">[主要電子倉庫] 會在此命令時間之後的 [再生期間] 重新產生 [次要] 金鑰，並將它設為作用中的按鍵。</span><span class="sxs-lookup"><span data-stu-id="6762b-121">Key Vault will regenerate 'Secondary' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="6762b-122">這個自動重新產生程式將會在「主要」和「次要」之間繼續，而間隔則是90天。</span><span class="sxs-lookup"><span data-stu-id="6762b-122">This auto regeneration process will continue between 'Primary' and 'Secondary' with a gap of 90 days.</span></span>

## <span data-ttu-id="6762b-123">參數</span><span class="sxs-lookup"><span data-stu-id="6762b-123">PARAMETERS</span></span>

### <span data-ttu-id="6762b-124">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6762b-124">-AccountName</span></span>
<span data-ttu-id="6762b-125">主要保存庫管理的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="6762b-125">Key Vault managed storage account name.</span></span> <span data-ttu-id="6762b-126">Cmdlet 會從保存庫名稱、目前已選取的環境及 manged 儲存空間帳戶名稱構造受管理儲存空間帳戶名稱的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="6762b-126">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="6762b-127">-AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="6762b-127">-AccountResourceId</span></span>
<span data-ttu-id="6762b-128">儲存空間帳戶的 Azure 資源 id。</span><span class="sxs-lookup"><span data-stu-id="6762b-128">Azure resource id of the storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountResourceId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6762b-129">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="6762b-129">-ActiveKeyName</span></span>
<span data-ttu-id="6762b-130">必須用來產生 sas 權杖的儲存空間帳戶金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="6762b-130">Name of the storage account key that must be used for generating sas tokens.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6762b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6762b-131">-DefaultProfile</span></span>
<span data-ttu-id="6762b-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="6762b-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6762b-133">-停用</span><span class="sxs-lookup"><span data-stu-id="6762b-133">-Disable</span></span>
<span data-ttu-id="6762b-134">停用受管理的儲存帳戶金鑰來產生 sas 權杖。</span><span class="sxs-lookup"><span data-stu-id="6762b-134">Disables the use of managed storage account's key for generation of sas tokens.</span></span>

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

### <span data-ttu-id="6762b-135">-DisableAutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="6762b-135">-DisableAutoRegenerateKey</span></span>
<span data-ttu-id="6762b-136">自動重新產生金鑰。</span><span class="sxs-lookup"><span data-stu-id="6762b-136">Auto regenerate key.</span></span> <span data-ttu-id="6762b-137">如果是 true，則受管理的儲存空間帳戶的非作用中金鑰會自動重新產生，並在再生期間成為新的作用中索引鍵。</span><span class="sxs-lookup"><span data-stu-id="6762b-137">If true, then the managed storage account's inactive key gets auto regenerated and becomes the new active key after the regeneration period.</span></span> <span data-ttu-id="6762b-138">如果是 false，系統就不會自動重新產生受管理的儲存空間帳戶的金鑰。</span><span class="sxs-lookup"><span data-stu-id="6762b-138">If false, then the keys of managed storage account are not auto regenerated.</span></span>

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

### <span data-ttu-id="6762b-139">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="6762b-139">-RegenerationPeriod</span></span>
<span data-ttu-id="6762b-140">[再生期間]。</span><span class="sxs-lookup"><span data-stu-id="6762b-140">Regeneration period.</span></span> <span data-ttu-id="6762b-141">如果已啟用自動重新產生鍵，此值會指定管理儲存空間帳戶停用 keygets 自動重新產生並成為新的作用中金鑰之後的時間跨度。</span><span class="sxs-lookup"><span data-stu-id="6762b-141">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the new active key.</span></span>

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

### <span data-ttu-id="6762b-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="6762b-142">-Tag</span></span>
<span data-ttu-id="6762b-143">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="6762b-143">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6762b-144">例如：</span><span class="sxs-lookup"><span data-stu-id="6762b-144">For example:</span></span>

<span data-ttu-id="6762b-145">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="6762b-145">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6762b-146">-VaultName</span><span class="sxs-lookup"><span data-stu-id="6762b-146">-VaultName</span></span>
<span data-ttu-id="6762b-147">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="6762b-147">Vault name.</span></span>
<span data-ttu-id="6762b-148">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="6762b-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="6762b-149">-確認</span><span class="sxs-lookup"><span data-stu-id="6762b-149">-Confirm</span></span>
<span data-ttu-id="6762b-150">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6762b-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6762b-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6762b-151">-WhatIf</span></span>
<span data-ttu-id="6762b-152">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6762b-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6762b-153">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6762b-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6762b-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6762b-154">CommonParameters</span></span>
<span data-ttu-id="6762b-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6762b-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6762b-156">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6762b-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6762b-157">輸入</span><span class="sxs-lookup"><span data-stu-id="6762b-157">INPUTS</span></span>

## <span data-ttu-id="6762b-158">輸出</span><span class="sxs-lookup"><span data-stu-id="6762b-158">OUTPUTS</span></span>

### <span data-ttu-id="6762b-159">ManagedStorageAccount 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="6762b-159">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="6762b-160">筆記</span><span class="sxs-lookup"><span data-stu-id="6762b-160">NOTES</span></span>

## <span data-ttu-id="6762b-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="6762b-161">RELATED LINKS</span></span>

[<span data-ttu-id="6762b-162">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6762b-162">AzureRM.KeyVault</span></span>](/powershell/module/azurerm.keyvault)
