---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
ms.openlocfilehash: 0b5e34fe3d7fe4c680ac20da53a32e1e5bad36fa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137225"
---
# <span data-ttu-id="0710c-101">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0710c-101">Set-AzStorageAccount</span></span>

## <span data-ttu-id="0710c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0710c-102">SYNOPSIS</span></span>
<span data-ttu-id="0710c-103">修改儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="0710c-103">Modifies a Storage account.</span></span>

## <span data-ttu-id="0710c-104">句法</span><span class="sxs-lookup"><span data-stu-id="0710c-104">SYNTAX</span></span>

### <span data-ttu-id="0710c-105">StorageEncryption (預設) </span><span class="sxs-lookup"><span data-stu-id="0710c-105">StorageEncryption (Default)</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0710c-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="0710c-106">KeyvaultEncryption</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> [-KeyVersion <String>]
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0710c-107">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="0710c-107">ActiveDirectoryDomainServicesForFile</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-UpgradeToStorageV2] [-EnableLargeFileShare] -EnableActiveDirectoryDomainServicesForFile <Boolean>
 [-ActiveDirectoryDomainName <String>] [-ActiveDirectoryNetBiosDomainName <String>]
 [-ActiveDirectoryForestName <String>] [-ActiveDirectoryDomainGuid <String>]
 [-ActiveDirectoryDomainSid <String>] [-ActiveDirectoryAzureStorageSid <String>]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0710c-108">說明</span><span class="sxs-lookup"><span data-stu-id="0710c-108">DESCRIPTION</span></span>
<span data-ttu-id="0710c-109">**AzStorageAccount** Cmdlet 會修改 Azure 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="0710c-109">The **Set-AzStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="0710c-110">您可以使用此 Cmdlet 來修改帳戶類型、更新客戶網域，或在儲存空間帳戶上設定標籤。</span><span class="sxs-lookup"><span data-stu-id="0710c-110">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="0710c-111">示例</span><span class="sxs-lookup"><span data-stu-id="0710c-111">EXAMPLES</span></span>

### <span data-ttu-id="0710c-112">範例1：設定儲存帳戶類型</span><span class="sxs-lookup"><span data-stu-id="0710c-112">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="0710c-113">這個命令會將儲存帳戶類型設定為 [Standard_RAGRS]。</span><span class="sxs-lookup"><span data-stu-id="0710c-113">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="0710c-114">範例2：針對儲存帳戶設定自訂網域</span><span class="sxs-lookup"><span data-stu-id="0710c-114">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="0710c-115">這個命令會針對儲存空間帳戶設定自訂網域。</span><span class="sxs-lookup"><span data-stu-id="0710c-115">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="0710c-116">範例3：設定存取層的值</span><span class="sxs-lookup"><span data-stu-id="0710c-116">Example 3: Set the access tier value</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AccessTier Cool
```

<span data-ttu-id="0710c-117">該命令會將 [存取層] 值設定為 [冷卻]。</span><span class="sxs-lookup"><span data-stu-id="0710c-117">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="0710c-118">範例4：設定自訂網域和標籤</span><span class="sxs-lookup"><span data-stu-id="0710c-118">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="0710c-119">此命令會針對儲存空間帳戶設定自訂網域和標籤。</span><span class="sxs-lookup"><span data-stu-id="0710c-119">The command sets the custom domain and tags for a Storage account.</span></span>

### <span data-ttu-id="0710c-120">範例5：將加密 KeySource 設定為 Keyvault</span><span class="sxs-lookup"><span data-stu-id="0710c-120">Example 5: Set Encryption KeySource to Keyvault</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AssignIdentity
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"

PS C:\>$keyVault = New-AzKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get

PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="0710c-121">這個命令會將加密 KeySource 設定為新的已建立 Keyvault。</span><span class="sxs-lookup"><span data-stu-id="0710c-121">This command set Encryption KeySource with a new created Keyvault.</span></span>

### <span data-ttu-id="0710c-122">範例6：將加密 KeySource 設定為 "Microsoft. Storage"</span><span class="sxs-lookup"><span data-stu-id="0710c-122">Example 6: Set Encryption KeySource to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -StorageEncryption
```

<span data-ttu-id="0710c-123">這個命令會將加密 KeySource 設定為 "Microsoft. Storage"</span><span class="sxs-lookup"><span data-stu-id="0710c-123">This command set Encryption KeySource to "Microsoft.Storage"</span></span>

### <span data-ttu-id="0710c-124">範例7：使用 JSON 設定儲存空間帳戶的 NetworkRuleSet 屬性</span><span class="sxs-lookup"><span data-stu-id="0710c-124">Example 7: Set NetworkRuleSet property of a Storage account with JSON</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="allow"})
```

<span data-ttu-id="0710c-125">這個命令會使用 JSON 設定儲存空間帳戶的 NetworkRuleSet 屬性</span><span class="sxs-lookup"><span data-stu-id="0710c-125">This command sets NetworkRuleSet property of a Storage account with JSON</span></span>

### <span data-ttu-id="0710c-126">範例8：從儲存空間帳戶取得 NetworkRuleSet 屬性，並將其設定為其他儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="0710c-126">Example 8: Get NetworkRuleSet property from a Storage account, and set it to another Storage account</span></span>
```
PS C:\> $networkRuleSet = (Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount").NetworkRuleSet 
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount2" -NetworkRuleSet $networkRuleSet
```

<span data-ttu-id="0710c-127">這個第一個命令會從儲存空間帳戶取得 NetworkRuleSet 屬性，而第二個命令會將它設為其他儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="0710c-127">This first command gets NetworkRuleSet property from a Storage account, and the second command sets it to another Storage account</span></span> 

### <span data-ttu-id="0710c-128">範例9：將具有類型 "Storage" 或 "BlobStorage" 的儲存空間帳戶升級為 "StorageV2" 類型的儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="0710c-128">Example 9: Upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account</span></span>
```
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -UpgradeToStorageV2
```

<span data-ttu-id="0710c-129">此命令會將類型為「Storage」或 "BlobStorage" 的儲存空間帳戶升級為 "StorageV2" 類型的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="0710c-129">The command upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account.</span></span>

### <span data-ttu-id="0710c-130">範例10：透過啟用 Azure Files AAD DS 驗證來更新儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="0710c-130">Example 10: Update a Storage account by enable Azure Files AAD DS Authentication.</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -EnableAzureActiveDirectoryDomainServicesForFile $true PS

PS C:\> $account.AzureFilesIdentityBasedAuth.DirectoryServiceOptions
AADDS
```

<span data-ttu-id="0710c-131">此命令會透過啟用 Azure 檔案 AAD DS 驗證來更新儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="0710c-131">The command update a Storage account by enable Azure Files AAD DS Authentication.</span></span>

### <span data-ttu-id="0710c-132">範例11：使用 [啟用檔案] Active Directory 網域服務驗證，然後顯示 [以檔案身分識別] 驗證設定來更新儲存帳戶</span><span class="sxs-lookup"><span data-stu-id="0710c-132">Example 11: Update a Storage account by enable Files Active Directory Domain Service Authentication, and then show the File Identity Based authentication setting</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
        
PS C:\> $account.AzureFilesIdentityBasedAuth.DirectoryServiceOptions
AD

PS C:\> $account.AzureFilesIdentityBasedAuth.ActiveDirectoryProperties

DomainName        : mydomain.com
NetBiosDomainName : mydomain.com
ForestName        : mydomain.com
DomainGuid        : 12345678-1234-1234-1234-123456789012
DomainSid         : S-1-5-21-1234567890-1234567890-1234567890
AzureStorageSid   : S-1-5-21-1234567890-1234567890-1234567890-1234
```

<span data-ttu-id="0710c-133">此命令會透過啟用 Azure 檔案 Active Directory 網域服務驗證來更新儲存空間帳戶，然後顯示以檔案身分識別的驗證設定</span><span class="sxs-lookup"><span data-stu-id="0710c-133">The command updates a Storage account by enable Azure Files Active Directory Domain Service Authentication, and then shows the File Identity Based authentication setting</span></span>

### <span data-ttu-id="0710c-134">範例12：設定 MinimumTlsVersion 和 AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="0710c-134">Example 12: Set MinimumTlsVersion and AllowBlobPublicAccess</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False
```

<span data-ttu-id="0710c-135">此命令會設定 MinimumTlsVersion 和 AllowBlobPublicAccess，然後顯示帳戶的2個屬性</span><span class="sxs-lookup"><span data-stu-id="0710c-135">The command sets MinimumTlsVersion  and AllowBlobPublicAccess, and then show the the 2 properties of the account</span></span> 

## <span data-ttu-id="0710c-136">參數</span><span class="sxs-lookup"><span data-stu-id="0710c-136">PARAMETERS</span></span>

### <span data-ttu-id="0710c-137">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="0710c-137">-AccessTier</span></span>
<span data-ttu-id="0710c-138">指定此 Cmdlet 修改之儲存空間帳戶的存取層。</span><span class="sxs-lookup"><span data-stu-id="0710c-138">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="0710c-139">此參數可接受的值為： [熱] 和 [超酷]。</span><span class="sxs-lookup"><span data-stu-id="0710c-139">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="0710c-140">如果您變更了存取層，可能會導致額外的費用。</span><span class="sxs-lookup"><span data-stu-id="0710c-140">If you change the access tier, it may result in additional charges.</span></span> <span data-ttu-id="0710c-141">如需詳細資訊，請參閱 [Azure Blob 儲存體：熱及冷卻存儲層](http://go.microsoft.com/fwlink/?LinkId=786482)。</span><span class="sxs-lookup"><span data-stu-id="0710c-141">For more information, see [Azure Blob Storage: Hot and cool storage tiers](http://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="0710c-142">如果儲存空間帳戶的類型是 StorageV2 或 BlobStorage，您可以指定 *AccessTier* 參數。</span><span class="sxs-lookup"><span data-stu-id="0710c-142">If the Storage account has Kind as StorageV2 or BlobStorage, you can specify the *AccessTier* parameter.</span></span> <span data-ttu-id="0710c-143">如果儲存空間帳戶的類型是 [儲存空間]，請勿指定 *AccessTier* 參數。</span><span class="sxs-lookup"><span data-stu-id="0710c-143">If the Storage account has Kind as Storage, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0710c-144">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="0710c-144">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="0710c-145">指定 Azure 儲存空間 (SID) 的安全性識別碼。</span><span class="sxs-lookup"><span data-stu-id="0710c-145">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="0710c-146">此參數必須在-EnableActiveDirectoryDomainServicesForFile 設定為 true 時設定。</span><span class="sxs-lookup"><span data-stu-id="0710c-146">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0710c-147">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="0710c-147">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="0710c-148">指定網域 GUID。</span><span class="sxs-lookup"><span data-stu-id="0710c-148">Specifies the domain GUID.</span></span> <span data-ttu-id="0710c-149">此參數必須在-EnableActiveDirectoryDomainServicesForFile 設定為 true 時設定。</span><span class="sxs-lookup"><span data-stu-id="0710c-149">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0710c-150">-ActiveDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="0710c-150">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="0710c-151">指定 AD DNS 伺服器擁有權威的主域。</span><span class="sxs-lookup"><span data-stu-id="0710c-151">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="0710c-152">此參數必須在-EnableActiveDirectoryDomainServicesForFile 設定為 true 時設定。</span><span class="sxs-lookup"><span data-stu-id="0710c-152">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0710c-153">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="0710c-153">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="0710c-154">指定 (SID) 的安全性識別碼。</span><span class="sxs-lookup"><span data-stu-id="0710c-154">Specifies the security identifier (SID).</span></span> <span data-ttu-id="0710c-155">此參數必須在-EnableActiveDirectoryDomainServicesForFile 設定為 true 時設定。</span><span class="sxs-lookup"><span data-stu-id="0710c-155">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0710c-156">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="0710c-156">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="0710c-157">指定要取得的 Active Directory 林。</span><span class="sxs-lookup"><span data-stu-id="0710c-157">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="0710c-158">此參數必須在-EnableActiveDirectoryDomainServicesForFile 設定為 true 時設定。</span><span class="sxs-lookup"><span data-stu-id="0710c-158">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0710c-159">-ActiveDirectoryNetBiosDomainName</span><span class="sxs-lookup"><span data-stu-id="0710c-159">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="0710c-160">指定 NetBIOS 功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="0710c-160">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="0710c-161">此參數必須在-EnableActiveDirectoryDomainServicesForFile 設定為 true 時設定。</span><span class="sxs-lookup"><span data-stu-id="0710c-161">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0710c-162">-AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="0710c-162">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="0710c-163">允許或不允許公開存取儲存空間帳戶中的所有 blob 或容器。</span><span class="sxs-lookup"><span data-stu-id="0710c-163">Allow or disallow public access to all blobs or containers in the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0710c-164">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0710c-164">-AsJob</span></span>
<span data-ttu-id="0710c-165">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0710c-165">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0710c-166">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="0710c-166">-AssignIdentity</span></span>
<span data-ttu-id="0710c-167">針對此儲存空間帳戶產生並指派新的儲存空間帳戶身分識別，以搭配 Azure KeyVault 等金鑰管理服務使用。</span><span class="sxs-lookup"><span data-stu-id="0710c-167">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="0710c-168">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="0710c-168">-CustomDomainName</span></span>
<span data-ttu-id="0710c-169">指定自訂網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="0710c-169">Specifies the name of the custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0710c-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0710c-170">-DefaultProfile</span></span>
<span data-ttu-id="0710c-171">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0710c-171">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0710c-172">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="0710c-172">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="0710c-173">針對儲存空間帳戶啟用 Azure Files Active Directory 網域服務驗證。</span><span class="sxs-lookup"><span data-stu-id="0710c-173">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0710c-174">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="0710c-174">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="0710c-175">針對儲存空間帳戶啟用 Azure Files Active Directory 網域服務驗證。</span><span class="sxs-lookup"><span data-stu-id="0710c-175">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: StorageEncryption, KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0710c-176">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="0710c-176">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="0710c-177">指出儲存空間帳戶是否只啟用 HTTPS 流量。</span><span class="sxs-lookup"><span data-stu-id="0710c-177">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0710c-178">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="0710c-178">-EnableLargeFileShare</span></span>
<span data-ttu-id="0710c-179">指示儲存空間帳戶是否可支援超過5個 TiB 容量的大型檔案共用。</span><span class="sxs-lookup"><span data-stu-id="0710c-179">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="0710c-180">一旦啟用帳戶，就無法停用此功能。</span><span class="sxs-lookup"><span data-stu-id="0710c-180">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="0710c-181">目前僅支援 LRS 和 ZRS 複製類型，因此不可能將帳戶轉換成地域冗余帳戶。</span><span class="sxs-lookup"><span data-stu-id="0710c-181">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="0710c-182">深入瞭解 https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="0710c-182">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="0710c-183">-Force</span><span class="sxs-lookup"><span data-stu-id="0710c-183">-Force</span></span>
<span data-ttu-id="0710c-184">強制將變更寫入儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="0710c-184">Forces the change to be written to the Storage account.</span></span>

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

### <span data-ttu-id="0710c-185">-KeyName</span><span class="sxs-lookup"><span data-stu-id="0710c-185">-KeyName</span></span>
<span data-ttu-id="0710c-186">如果使用-KeyvaultEncryption 啟用金鑰保存庫的加密，請使用這個選項指定 Keyname 屬性。</span><span class="sxs-lookup"><span data-stu-id="0710c-186">If using -KeyvaultEncryption to enable encryption with Key Vault, specify the Keyname property with this option.</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0710c-187">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="0710c-187">-KeyvaultEncryption</span></span>
<span data-ttu-id="0710c-188">指示在使用儲存服務加密時，是否要針對加密金鑰使用 Microsoft KeyVault。</span><span class="sxs-lookup"><span data-stu-id="0710c-188">Indicates whether or not to use Microsoft KeyVault for the encryption keys when using Storage Service Encryption.</span></span> <span data-ttu-id="0710c-189">如果 KeyName、KeyVersion 和 KeyVaultUri 全都設定，KeySource 將會設定為 Microsoft。 Keyvault 是否已設定此參數。</span><span class="sxs-lookup"><span data-stu-id="0710c-189">If KeyName, KeyVersion, and KeyVaultUri are all set, KeySource will be set to Microsoft.Keyvault whether this parameter is set or not.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0710c-190">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="0710c-190">-KeyVaultUri</span></span>
<span data-ttu-id="0710c-191">透過指定-KeyvaultEncryption 參數使用金鑰保險存儲加密時，請使用這個選項來指定主要電子倉庫的 URI。</span><span class="sxs-lookup"><span data-stu-id="0710c-191">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0710c-192">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="0710c-192">-KeyVersion</span></span>
<span data-ttu-id="0710c-193">透過指定-KeyvaultEncryption 參數使用金鑰 Vault 加密時，請使用這個選項來指定金鑰版本的 URI。</span><span class="sxs-lookup"><span data-stu-id="0710c-193">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Version.</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0710c-194">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="0710c-194">-MinimumTlsVersion</span></span>
<span data-ttu-id="0710c-195">針對儲存空間要求所允許的最小 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="0710c-195">The minimum TLS version to be permitted on requests to storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TLS1_0, TLS1_1, TLS1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0710c-196">-名稱</span><span class="sxs-lookup"><span data-stu-id="0710c-196">-Name</span></span>
<span data-ttu-id="0710c-197">指定要修改的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="0710c-197">Specifies the name of the Storage account to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0710c-198">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="0710c-198">-NetworkRuleSet</span></span>
<span data-ttu-id="0710c-199">NetworkRuleSet 是用來定義防火牆和虛擬網路的一組設定規則，以及設定網路屬性的值，例如允許繞過規則的服務，以及如何處理不符合任何已定義規則的要求。</span><span class="sxs-lookup"><span data-stu-id="0710c-199">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0710c-200">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0710c-200">-ResourceGroupName</span></span>
<span data-ttu-id="0710c-201">指定要修改儲存空間帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0710c-201">Specifies the name of the resource group in which to modify the Storage account.</span></span>

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

### <span data-ttu-id="0710c-202">-SkuName</span><span class="sxs-lookup"><span data-stu-id="0710c-202">-SkuName</span></span>
<span data-ttu-id="0710c-203">指定儲存空間帳戶的 SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="0710c-203">Specifies the SKU name of the Storage account.</span></span>
<span data-ttu-id="0710c-204">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="0710c-204">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0710c-205">Standard_LRS 本機冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="0710c-205">Standard_LRS - Locally-redundant storage.</span></span>
- <span data-ttu-id="0710c-206">Standard_ZRS 區域冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="0710c-206">Standard_ZRS - Zone-redundant storage.</span></span>
- <span data-ttu-id="0710c-207">Standard_GRS 地域冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="0710c-207">Standard_GRS - Geo-redundant storage.</span></span>
- <span data-ttu-id="0710c-208">Standard_RAGRS 讀取 access 地域冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="0710c-208">Standard_RAGRS - Read access geo-redundant storage.</span></span>
- <span data-ttu-id="0710c-209">Premium_LRS-Premium 本機冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="0710c-209">Premium_LRS - Premium locally-redundant storage.</span></span>
- <span data-ttu-id="0710c-210">Standard_GZRS 地域冗余區域-冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="0710c-210">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="0710c-211">Standard_RAGZRS 讀取 access 地域冗余區域-冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="0710c-211">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>
<span data-ttu-id="0710c-212">您無法將 Standard_ZRS 和 Premium_LRS 類型變更為其他帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="0710c-212">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="0710c-213">您無法將其他帳戶類型變更為 [Standard_ZRS] 或 [Premium_LRS]。</span><span class="sxs-lookup"><span data-stu-id="0710c-213">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS, Standard_GZRS, Standard_RAGZRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0710c-214">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="0710c-214">-StorageEncryption</span></span>
<span data-ttu-id="0710c-215">指出是否要將儲存帳戶加密設定為使用 Microsoft 管理的金鑰。</span><span class="sxs-lookup"><span data-stu-id="0710c-215">Indicates whether or not to set the Storage account encryption to use Microsoft-managed keys.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: StorageEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0710c-216">-Tag</span><span class="sxs-lookup"><span data-stu-id="0710c-216">-Tag</span></span>
<span data-ttu-id="0710c-217">在伺服器上將雜湊表的格式設定為標記的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="0710c-217">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="0710c-218">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="0710c-218">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0710c-219">-UpgradeToStorageV2</span><span class="sxs-lookup"><span data-stu-id="0710c-219">-UpgradeToStorageV2</span></span>
<span data-ttu-id="0710c-220">從 Storage 或 BlobStorage 升級儲存帳戶類型至 StorageV2。</span><span class="sxs-lookup"><span data-stu-id="0710c-220">Upgrade Storage account Kind from  Storage or BlobStorage to StorageV2.</span></span>

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

### <span data-ttu-id="0710c-221">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="0710c-221">-UseSubDomain</span></span>
<span data-ttu-id="0710c-222">指示是否要啟用間接 CName 驗證。</span><span class="sxs-lookup"><span data-stu-id="0710c-222">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="0710c-223">-確認</span><span class="sxs-lookup"><span data-stu-id="0710c-223">-Confirm</span></span>
<span data-ttu-id="0710c-224">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0710c-224">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0710c-225">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0710c-225">-WhatIf</span></span>
<span data-ttu-id="0710c-226">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0710c-226">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0710c-227">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0710c-227">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0710c-228">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0710c-228">CommonParameters</span></span>
<span data-ttu-id="0710c-229">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0710c-229">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0710c-230">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0710c-230">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0710c-231">輸入</span><span class="sxs-lookup"><span data-stu-id="0710c-231">INPUTS</span></span>

### <span data-ttu-id="0710c-232">System.object</span><span class="sxs-lookup"><span data-stu-id="0710c-232">System.String</span></span>

### <span data-ttu-id="0710c-233">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0710c-233">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0710c-234">輸出</span><span class="sxs-lookup"><span data-stu-id="0710c-234">OUTPUTS</span></span>

### <span data-ttu-id="0710c-235">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="0710c-235">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="0710c-236">筆記</span><span class="sxs-lookup"><span data-stu-id="0710c-236">NOTES</span></span>

## <span data-ttu-id="0710c-237">相關連結</span><span class="sxs-lookup"><span data-stu-id="0710c-237">RELATED LINKS</span></span>

[<span data-ttu-id="0710c-238">AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0710c-238">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="0710c-239">新-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0710c-239">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="0710c-240">移除-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0710c-240">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)
