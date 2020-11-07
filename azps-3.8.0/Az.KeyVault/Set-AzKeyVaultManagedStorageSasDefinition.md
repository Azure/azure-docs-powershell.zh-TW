---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 8ecd136243f48c52f2ee1d4077b0eccb4a610e76
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959737"
---
# <span data-ttu-id="2ed0b-101">Set-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="2ed0b-101">Set-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="2ed0b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2ed0b-102">SYNOPSIS</span></span>
<span data-ttu-id="2ed0b-103">針對特定的主要電子倉庫管理的 Azure 儲存空間帳戶，使用金鑰保存庫 (SAS) 定義來設定共用存取簽章。</span><span class="sxs-lookup"><span data-stu-id="2ed0b-103">Sets a Shared Access Signature (SAS) definition with Key Vault for a given Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="2ed0b-104">句法</span><span class="sxs-lookup"><span data-stu-id="2ed0b-104">SYNTAX</span></span>

### <span data-ttu-id="2ed0b-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="2ed0b-105">Default (Default)</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>] -ValidityPeriod <TimeSpan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ed0b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2ed0b-106">ByInputObject</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-Name] <String> [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>]
 -ValidityPeriod <TimeSpan> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2ed0b-107">說明</span><span class="sxs-lookup"><span data-stu-id="2ed0b-107">DESCRIPTION</span></span>
<span data-ttu-id="2ed0b-108">使用指定的主要電子倉庫管理的 Azure 儲存空間帳戶，設定共用存取簽章 (SAS) 定義。</span><span class="sxs-lookup"><span data-stu-id="2ed0b-108">Sets a Shared Access Signature (SAS) definition with a given Key Vault managed Azure Storage Account.</span></span> <span data-ttu-id="2ed0b-109">這也會設定一個機密，您可以用來針對每個 SAS 定義取得 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="2ed0b-109">This also sets a secret which can be used to get the SAS token per this SAS definition.</span></span>
<span data-ttu-id="2ed0b-110">SAS 權杖是使用這些參數以及主要電子倉庫管理的 Azure 儲存空間帳戶的活動金鑰產生。</span><span class="sxs-lookup"><span data-stu-id="2ed0b-110">SAS token is generated using these parameters and the active key of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="2ed0b-111">示例</span><span class="sxs-lookup"><span data-stu-id="2ed0b-111">EXAMPLES</span></span>

### <span data-ttu-id="2ed0b-112">範例1：設定帳戶類型 SAS 定義，並根據它取得目前的 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="2ed0b-112">Example 1 : Set an account-type SAS definition, and obtain a current SAS token based on it</span></span>
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

<span data-ttu-id="2ed0b-113">在 vault "mykv" 中，針對 KeyVault 管理的儲存空間帳戶 ' mysa ' 設定帳戶 SAS 定義 ' accountsas '。</span><span class="sxs-lookup"><span data-stu-id="2ed0b-113">Sets an account SAS definition 'accountsas' on a KeyVault-managed storage account 'mysa' in vault 'mykv'.</span></span> <span data-ttu-id="2ed0b-114">具體來說，上述順序會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="2ed0b-114">Specifically, the sequence above performs the following:</span></span>
  - <span data-ttu-id="2ed0b-115">取得 (預先存在的) 儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="2ed0b-115">gets a (pre-existing) storage account</span></span>
  - <span data-ttu-id="2ed0b-116">取得 (預先存在的) 金鑰保存庫</span><span class="sxs-lookup"><span data-stu-id="2ed0b-116">gets a (pre-existing) key vault</span></span>
  - <span data-ttu-id="2ed0b-117">將 KeyVault 管理的儲存空間帳戶新增到保存庫、將 Key1 設定為使用中的金鑰，以及在180天內再生期間</span><span class="sxs-lookup"><span data-stu-id="2ed0b-117">adds a KeyVault-managed storage account to the vault, setting Key1 as the active key, and with a regeneration period of 180 days</span></span>
  - <span data-ttu-id="2ed0b-118">針對指定的儲存空間帳戶（含 Key1）設定儲存內容</span><span class="sxs-lookup"><span data-stu-id="2ed0b-118">sets a storage context for the specified storage account, with Key1</span></span>
  - <span data-ttu-id="2ed0b-119">為服務 Blob、檔案、資料表和佇列（針對資源類型服務、容器及物件）建立帳戶 SAS 權杖，並在 HTTPs 中使用指定的開始和結束日期</span><span class="sxs-lookup"><span data-stu-id="2ed0b-119">creates an account SAS token for services Blob, File, Table and Queue, for resource types Service, Container and Object, with all permissions, over https and with the specified start and end dates</span></span>
  - <span data-ttu-id="2ed0b-120">在保存庫中設定 KeyVault 管理的儲存 SAS 定義，並將範本 uri 做為在上述建立的 SAS 權杖，即 SAS 類型 ' 帳戶」，且有效期為30天</span><span class="sxs-lookup"><span data-stu-id="2ed0b-120">sets a KeyVault-managed storage SAS definition in the vault, with the template uri as the SAS token created above, of SAS type 'account' and valid for 30 days</span></span>
  - <span data-ttu-id="2ed0b-121">從與 SAS 定義相對應的 KeyVault 機密檢索實際存取權杖</span><span class="sxs-lookup"><span data-stu-id="2ed0b-121">retrieves the actual access token from the KeyVault secret corresponding to the SAS definition</span></span>

## <span data-ttu-id="2ed0b-122">參數</span><span class="sxs-lookup"><span data-stu-id="2ed0b-122">PARAMETERS</span></span>

### <span data-ttu-id="2ed0b-123">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2ed0b-123">-AccountName</span></span>
<span data-ttu-id="2ed0b-124">主要保存庫管理的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="2ed0b-124">Key Vault managed storage account name.</span></span> <span data-ttu-id="2ed0b-125">Cmdlet 會從保存庫名稱、目前已選取的環境及 manged 儲存空間帳戶名稱構造受管理儲存空間帳戶名稱的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="2ed0b-125">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="2ed0b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ed0b-126">-DefaultProfile</span></span>
<span data-ttu-id="2ed0b-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2ed0b-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2ed0b-128">-停用</span><span class="sxs-lookup"><span data-stu-id="2ed0b-128">-Disable</span></span>
<span data-ttu-id="2ed0b-129">停用 sas 定義來產生 sas 權杖。</span><span class="sxs-lookup"><span data-stu-id="2ed0b-129">Disables the use of sas definition for generation of sas token.</span></span>

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

### <span data-ttu-id="2ed0b-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ed0b-130">-InputObject</span></span>
<span data-ttu-id="2ed0b-131">ManagedStorageAccount 物件。</span><span class="sxs-lookup"><span data-stu-id="2ed0b-131">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="2ed0b-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="2ed0b-132">-Name</span></span>
<span data-ttu-id="2ed0b-133">儲存區 sas 定義名稱。</span><span class="sxs-lookup"><span data-stu-id="2ed0b-133">Storage sas definition name.</span></span> <span data-ttu-id="2ed0b-134">Cmdlet 會從保存庫名稱、目前所選的環境、儲存空間帳戶名稱和 sas 定義名稱來構造儲存 sas 定義的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="2ed0b-134">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

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

### <span data-ttu-id="2ed0b-135">-SasType</span><span class="sxs-lookup"><span data-stu-id="2ed0b-135">-SasType</span></span>
<span data-ttu-id="2ed0b-136">儲存 SAS 類型。</span><span class="sxs-lookup"><span data-stu-id="2ed0b-136">Storage SAS type.</span></span>

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

### <span data-ttu-id="2ed0b-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="2ed0b-137">-Tag</span></span>
<span data-ttu-id="2ed0b-138">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="2ed0b-138">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2ed0b-139">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="2ed0b-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2ed0b-140">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="2ed0b-140">-TemplateUri</span></span>
<span data-ttu-id="2ed0b-141">儲存 SAS 定義範本 uri。</span><span class="sxs-lookup"><span data-stu-id="2ed0b-141">Storage SAS definition template uri.</span></span>

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

### <span data-ttu-id="2ed0b-142">-ValidityPeriod</span><span class="sxs-lookup"><span data-stu-id="2ed0b-142">-ValidityPeriod</span></span>
<span data-ttu-id="2ed0b-143">將用來從產生 sas 權杖的時間設定其到期時間的有效期間</span><span class="sxs-lookup"><span data-stu-id="2ed0b-143">Validity period that will get used to set the expiry time of sas token from the time it gets generated</span></span>

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

### <span data-ttu-id="2ed0b-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="2ed0b-144">-VaultName</span></span>
<span data-ttu-id="2ed0b-145">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="2ed0b-145">Vault name.</span></span>
<span data-ttu-id="2ed0b-146">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="2ed0b-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="2ed0b-147">-確認</span><span class="sxs-lookup"><span data-stu-id="2ed0b-147">-Confirm</span></span>
<span data-ttu-id="2ed0b-148">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2ed0b-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ed0b-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ed0b-149">-WhatIf</span></span>
<span data-ttu-id="2ed0b-150">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2ed0b-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ed0b-151">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2ed0b-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ed0b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ed0b-152">CommonParameters</span></span>
<span data-ttu-id="2ed0b-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2ed0b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ed0b-154">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2ed0b-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ed0b-155">輸入</span><span class="sxs-lookup"><span data-stu-id="2ed0b-155">INPUTS</span></span>

### <span data-ttu-id="2ed0b-156">PSKeyVaultManagedStorageAccountIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="2ed0b-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="2ed0b-157">輸出</span><span class="sxs-lookup"><span data-stu-id="2ed0b-157">OUTPUTS</span></span>

### <span data-ttu-id="2ed0b-158">PSKeyVaultManagedStorageSasDefinition 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="2ed0b-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="2ed0b-159">筆記</span><span class="sxs-lookup"><span data-stu-id="2ed0b-159">NOTES</span></span>

## <span data-ttu-id="2ed0b-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="2ed0b-160">RELATED LINKS</span></span>

[<span data-ttu-id="2ed0b-161">Azureâ€‹ RM。€‹ Keyâ€‹ Vault</span><span class="sxs-lookup"><span data-stu-id="2ed0b-161">Azureâ€‹RM.â€‹Keyâ€‹Vault</span></span>](/powershell/module/az.keyvault/)
