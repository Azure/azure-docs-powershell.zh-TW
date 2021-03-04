---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/set-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: b95f47de7fbdcf6b5ed7892cb8deb8656559da27
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911941"
---
# <span data-ttu-id="c0164-101">Set-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="c0164-101">Set-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="c0164-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c0164-102">SYNOPSIS</span></span>
<span data-ttu-id="c0164-103">使用具有金鑰保存庫管理之 Azure (帳戶的金鑰保存庫定義設定共用存取簽章與 SAS) 定義。</span><span class="sxs-lookup"><span data-stu-id="c0164-103">Sets a Shared Access Signature (SAS) definition with Key Vault for a given Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="c0164-104">語法</span><span class="sxs-lookup"><span data-stu-id="c0164-104">SYNTAX</span></span>

### <span data-ttu-id="c0164-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="c0164-105">Default (Default)</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>] -ValidityPeriod <TimeSpan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0164-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c0164-106">ByInputObject</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-Name] <String> [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>]
 -ValidityPeriod <TimeSpan> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c0164-107">描述</span><span class="sxs-lookup"><span data-stu-id="c0164-107">DESCRIPTION</span></span>
<span data-ttu-id="c0164-108">使用具具金鑰保存庫管理的 Azure (帳戶) SAS 的共用存取簽章定義。</span><span class="sxs-lookup"><span data-stu-id="c0164-108">Sets a Shared Access Signature (SAS) definition with a given Key Vault managed Azure Storage Account.</span></span> <span data-ttu-id="c0164-109">這也設定了一個秘訣，可用來根據此 SAS 定義取得 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="c0164-109">This also sets a secret which can be used to get the SAS token per this SAS definition.</span></span>
<span data-ttu-id="c0164-110">使用這些參數和金鑰保存庫受管理的 Azure 儲存帳戶的活動金鑰產生 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="c0164-110">SAS token is generated using these parameters and the active key of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="c0164-111">例子</span><span class="sxs-lookup"><span data-stu-id="c0164-111">EXAMPLES</span></span>

### <span data-ttu-id="c0164-112">範例 1：設定帳戶類型的 SAS 定義，並依據它取得目前的 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="c0164-112">Example 1: Set an account-type SAS definition, and obtain a current SAS token based on it</span></span>
```powershell
PS C:\> $sa = Get-AzStorageAccount -Name mysa -ResourceGroupName myrg
PS C:\> $kv = Get-AzKeyVault -VaultName mykv
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName $kv.VaultName -AccountName $sa.StorageAccountName -AccountResourceId $sa.Id -ActiveKeyName key1 -RegenerationPeriod ([System.Timespan]::FromDays(180))
PS C:\> $sctx = New-AzStorageContext -StorageAccountName $sa.StorageAccountName -Protocol Https -StorageAccountKey Key1
PS C:\> $start = [System.DateTime]::Now.AddDays(-1)
PS C:\> $end = [System.DateTime]::Now.AddMonths(1)
PS C:\> $at = New-AzStorageAccountSasToken -Service blob,file,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -StartTime $start -ExpiryTime $end -Context $sctx
PS C:\> $sas = Set-AzKeyVaultManagedStorageSasDefinition -AccountName $sa.StorageAccountName -VaultName $kv.VaultName -Name accountsas -TemplateUri $at -SasType 'account' -ValidityPeriod ([System.Timespan]::FromDays(30))
PS C:\> Get-AzKeyVaultSecret -VaultName $kv.VaultName -Name $sas.Sid.Substring($sas.Sid.LastIndexOf('/')+1)
```

<span data-ttu-id="c0164-113">在保存庫中的 KeyVault 管理儲存空間帳戶 'mysa' 上設定帳戶 SAS 定義 'accountas'。</span><span class="sxs-lookup"><span data-stu-id="c0164-113">Sets an account SAS definition 'accountsas' on a KeyVault-managed storage account 'mysa' in vault 'mykv'.</span></span> <span data-ttu-id="c0164-114">具體來說，上述順序會執行下列操作：</span><span class="sxs-lookup"><span data-stu-id="c0164-114">Specifically, the sequence above performs the following:</span></span>
  - <span data-ttu-id="c0164-115">獲得 (儲存空間) 帳戶</span><span class="sxs-lookup"><span data-stu-id="c0164-115">gets a (pre-existing) storage account</span></span>
  - <span data-ttu-id="c0164-116">獲得 (現有金鑰) 庫</span><span class="sxs-lookup"><span data-stu-id="c0164-116">gets a (pre-existing) key vault</span></span>
  - <span data-ttu-id="c0164-117">將 KeyVault 管理的儲存空間帳戶新增到保存庫，將 Key1 設定為使用中金鑰，並且有 180 天的回收期</span><span class="sxs-lookup"><span data-stu-id="c0164-117">adds a KeyVault-managed storage account to the vault, setting Key1 as the active key, and with a regeneration period of 180 days</span></span>
  - <span data-ttu-id="c0164-118">使用 Key1 設定指定儲存空間帳戶的儲存內容</span><span class="sxs-lookup"><span data-stu-id="c0164-118">sets a storage context for the specified storage account, with Key1</span></span>
  - <span data-ttu-id="c0164-119">建立服務 Blob、檔案、資料表和佇列的帳戶 SAS 權杖，用於資源類型服務、容器和物件，並擁有擁有權限，可超過 HTTPs 並包含指定的開始與結束日期</span><span class="sxs-lookup"><span data-stu-id="c0164-119">creates an account SAS token for services Blob, File, Table and Queue, for resource types Service, Container and Object, with all permissions, over https and with the specified start and end dates</span></span>
  - <span data-ttu-id="c0164-120">在保存庫中設定 KeyVault 管理的儲存空間 SAS 定義，範本 uri 是上述的 SAS 權杖，且為 SAS 類型的'帳戶'，且有效 30 天</span><span class="sxs-lookup"><span data-stu-id="c0164-120">sets a KeyVault-managed storage SAS definition in the vault, with the template uri as the SAS token created above, of SAS type 'account' and valid for 30 days</span></span>
  - <span data-ttu-id="c0164-121">從對應至 SAS 定義的 KeyVault 機密中，取得實際存取權杖</span><span class="sxs-lookup"><span data-stu-id="c0164-121">retrieves the actual access token from the KeyVault secret corresponding to the SAS definition</span></span>

## <span data-ttu-id="c0164-122">參數</span><span class="sxs-lookup"><span data-stu-id="c0164-122">PARAMETERS</span></span>

### <span data-ttu-id="c0164-123">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c0164-123">-AccountName</span></span>
<span data-ttu-id="c0164-124">金鑰保存庫受管理的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="c0164-124">Key Vault managed storage account name.</span></span> <span data-ttu-id="c0164-125">Cmdlet 會從保存庫名稱、目前選取的環境和偽造的儲存帳戶名稱建構受管理儲存帳戶名稱的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="c0164-125">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0164-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0164-126">-DefaultProfile</span></span>
<span data-ttu-id="c0164-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="c0164-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0164-128">-停用</span><span class="sxs-lookup"><span data-stu-id="c0164-128">-Disable</span></span>
<span data-ttu-id="c0164-129">停用 sas 定義用於產生 sas token。</span><span class="sxs-lookup"><span data-stu-id="c0164-129">Disables the use of sas definition for generation of sas token.</span></span>

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

### <span data-ttu-id="c0164-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0164-130">-InputObject</span></span>
<span data-ttu-id="c0164-131">ManagedStorageAccount 物件。</span><span class="sxs-lookup"><span data-stu-id="c0164-131">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="c0164-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="c0164-132">-Name</span></span>
<span data-ttu-id="c0164-133">儲存空間 sas 定義名稱。</span><span class="sxs-lookup"><span data-stu-id="c0164-133">Storage sas definition name.</span></span> <span data-ttu-id="c0164-134">Cmdlet 會從保存庫名稱、目前選取的環境、儲存帳戶名稱和 sas 定義名稱建構儲存空間 sas 定義的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="c0164-134">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0164-135">-SasType</span><span class="sxs-lookup"><span data-stu-id="c0164-135">-SasType</span></span>
<span data-ttu-id="c0164-136">儲存空間 SAS 類型。</span><span class="sxs-lookup"><span data-stu-id="c0164-136">Storage SAS type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0164-137">-標記</span><span class="sxs-lookup"><span data-stu-id="c0164-137">-Tag</span></span>
<span data-ttu-id="c0164-138">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="c0164-138">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c0164-139">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="c0164-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0164-140">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="c0164-140">-TemplateUri</span></span>
<span data-ttu-id="c0164-141">儲存體 SAS 定義範本 uri。</span><span class="sxs-lookup"><span data-stu-id="c0164-141">Storage SAS definition template uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0164-142">-ValidityPeriod</span><span class="sxs-lookup"><span data-stu-id="c0164-142">-ValidityPeriod</span></span>
<span data-ttu-id="c0164-143">將用來設定自產生 sas 權杖起到期時間的有效期間</span><span class="sxs-lookup"><span data-stu-id="c0164-143">Validity period that will get used to set the expiry time of sas token from the time it gets generated</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0164-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c0164-144">-VaultName</span></span>
<span data-ttu-id="c0164-145">儲存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="c0164-145">Vault name.</span></span>
<span data-ttu-id="c0164-146">Cmdlet 會根據名稱和目前選取的環境來建構庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="c0164-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0164-147">-確認</span><span class="sxs-lookup"><span data-stu-id="c0164-147">-Confirm</span></span>
<span data-ttu-id="c0164-148">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c0164-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0164-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0164-149">-WhatIf</span></span>
<span data-ttu-id="c0164-150">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c0164-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0164-151">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c0164-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0164-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0164-152">CommonParameters</span></span>
<span data-ttu-id="c0164-153">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c0164-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0164-154">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0164-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0164-155">輸入</span><span class="sxs-lookup"><span data-stu-id="c0164-155">INPUTS</span></span>

### <span data-ttu-id="c0164-156">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="c0164-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="c0164-157">輸出</span><span class="sxs-lookup"><span data-stu-id="c0164-157">OUTPUTS</span></span>

### <span data-ttu-id="c0164-158">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="c0164-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="c0164-159">筆記</span><span class="sxs-lookup"><span data-stu-id="c0164-159">NOTES</span></span>

## <span data-ttu-id="c0164-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="c0164-160">RELATED LINKS</span></span>

[<span data-ttu-id="c0164-161">Azure？RM.â€Keyââ€Vault</span><span class="sxs-lookup"><span data-stu-id="c0164-161">Azureâ€‹RM.â€‹Keyâ€‹Vault</span></span>](/powershell/module/az.keyvault/)
