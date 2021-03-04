---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: 0a5ccfaec396f4dc79c877da38112a5bfa575e09
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912538"
---
# <span data-ttu-id="75c8c-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="75c8c-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="75c8c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="75c8c-102">SYNOPSIS</span></span>
<span data-ttu-id="75c8c-103">建立儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="75c8c-103">Creates a Storage account.</span></span>

## <span data-ttu-id="75c8c-104">語法</span><span class="sxs-lookup"><span data-stu-id="75c8c-104">SYNTAX</span></span>

### <span data-ttu-id="75c8c-105">AzureActiveDirectoryDomainServicesForFile (預設) </span><span class="sxs-lookup"><span data-stu-id="75c8c-105">AzureActiveDirectoryDomainServicesForFile (Default)</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>] [-PublishInternetEndpoint <Boolean>] [-AsJob]
 [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>] [-RequireInfrastructureEncryption]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AllowSharedKeyAccess <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [<CommonParameters>]
```

### <span data-ttu-id="75c8c-106">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="75c8c-106">ActiveDirectoryDomainServicesForFile</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>]
 [-PublishInternetEndpoint <Boolean>] [-EnableActiveDirectoryDomainServicesForFile <Boolean>]
 [-ActiveDirectoryDomainName <String>] [-ActiveDirectoryNetBiosDomainName <String>]
 [-ActiveDirectoryForestName <String>] [-ActiveDirectoryDomainGuid <String>]
 [-ActiveDirectoryDomainSid <String>] [-ActiveDirectoryAzureStorageSid <String>] [-AsJob]
 [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>] [-RequireInfrastructureEncryption]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AllowSharedKeyAccess <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [<CommonParameters>]
```

## <span data-ttu-id="75c8c-107">描述</span><span class="sxs-lookup"><span data-stu-id="75c8c-107">DESCRIPTION</span></span>
<span data-ttu-id="75c8c-108">**New-AzStorageAccount** Cmdlet 會建立 Azure 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="75c8c-108">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="75c8c-109">例子</span><span class="sxs-lookup"><span data-stu-id="75c8c-109">EXAMPLES</span></span>

### <span data-ttu-id="75c8c-110">範例 1：建立儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="75c8c-110">Example 1: Create a Storage account</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="75c8c-111">此命令會為資源組名 MyResourceGroup 建立儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="75c8c-111">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="75c8c-112">範例 2：使用 BlobStorage Kind 和 hot AccessTier 建立 Blob 儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="75c8c-112">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="75c8c-113">此命令會建立 Blob 儲存空間帳戶，該帳戶具有 BlobStorage 類型與熱 AccessTier</span><span class="sxs-lookup"><span data-stu-id="75c8c-113">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="75c8c-114">範例 3：使用 Kind StorageV2 建立儲存空間帳戶，以及產生和指派 Azure KeyVault 的身分識別。</span><span class="sxs-lookup"><span data-stu-id="75c8c-114">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="75c8c-115">此命令會使用 Kind StorageV2 建立儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="75c8c-115">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="75c8c-116">它也會產生並指派身分識別，可用來透過 Azure KeyVault 管理帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="75c8c-116">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="75c8c-117">範例 4：從 JSON 使用 NetworkRuleSet 建立儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="75c8c-117">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="75c8c-118">此命令會建立一個儲存空間帳戶，該帳戶具有來自 JSON 的 NetworkRuleSet 屬性</span><span class="sxs-lookup"><span data-stu-id="75c8c-118">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="75c8c-119">範例 5：建立已啟用階層命名空間的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="75c8c-119">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="75c8c-120">此命令會建立已啟用階層命名空間的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="75c8c-120">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

### <span data-ttu-id="75c8c-121">範例 6：使用 Azure 檔案 AAD DS 驗證建立儲存空間帳戶，並啟用大型檔案共用。</span><span class="sxs-lookup"><span data-stu-id="75c8c-121">Example 6: Create a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

<span data-ttu-id="75c8c-122">此命令會使用 Azure 檔案 AAD DS 驗證建立儲存空間帳戶，並啟用大型檔案共用。</span><span class="sxs-lookup"><span data-stu-id="75c8c-122">This command creates a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>

### <span data-ttu-id="75c8c-123">範例 7：使用啟用檔案 Active Directory 網域服務驗證來建立儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="75c8c-123">Example 7: Create a Storage account with enable Files Active Directory Domain Service Authentication.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
```

<span data-ttu-id="75c8c-124">此命令會建立可啟用檔案 Active Directory 網域服務驗證的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="75c8c-124">This command creates a Storage account withenable Files Active Directory Domain Service Authentication.</span></span>

### <span data-ttu-id="75c8c-125">範例 8：使用佇列和資料表服務建立儲存空間帳戶，使用帳戶範圍加密金鑰，以及需要基礎結構加密。</span><span class="sxs-lookup"><span data-stu-id="75c8c-125">Example 8: Create a Storage account with Queue and Table Service use account-scoped encryption key, and Require Infrastructure Encryption.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EncryptionKeyTypeForTable Account -EncryptionKeyTypeForQueue Account -RequireInfrastructureEncryption

PS C:\>$account = get-AzStorageAccount -ResourceGroupName $rgname -StorageAccountName $accountName

PS C:\>$account.Encryption.Services.Queue

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\>$account.Encryption.Services.Table

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\> $account.Encryption.RequireInfrastructureEncryption
True
```

<span data-ttu-id="75c8c-126">此命令會建立一個儲存帳戶，其中佇列和資料表服務會使用帳戶範圍加密金鑰和需要基礎結構加密，因此佇列和資料表會與 Blob 和檔案服務使用相同的加密金鑰，而服務會針對其餘的資料，使用平臺管理金鑰來使用次要加密層。</span><span class="sxs-lookup"><span data-stu-id="75c8c-126">This command creates a Storage account with Queue and Table Service use account-scoped encryption key and Require Infrastructure Encryption, so Queue and Table will use same encryption key with Blob and File service, and the service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>
<span data-ttu-id="75c8c-127">然後取得儲存空間帳戶屬性，並查看 Queue 和 Table Service 的加密金鑰類型，以及 RequireInfracryptEncryption 值。</span><span class="sxs-lookup"><span data-stu-id="75c8c-127">Then get the Storage account properties, and view the encryption keytype of Queue and Table Service, and RequireInfrastructureEncryption value.</span></span>

### <span data-ttu-id="75c8c-128">範例 9：建立帳戶 MinimumTlsVersion 和 AllowBlobPublicAccess，並停用 SharedKey Access</span><span class="sxs-lookup"><span data-stu-id="75c8c-128">Example 9: Create account MinimumTlsVersion  and AllowBlobPublicAccess, and disable SharedKey Access</span></span>
```
PS C:\> $account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2 -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false -AllowSharedKeyAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False

PS C:\> $a.AllowSharedKeyAccess
False
```

<span data-ttu-id="75c8c-129">命令會使用 MinimumTlsVersion、AllowBlobPublicAccess 來建立帳戶，並停用該帳戶的 SharedKey 存取，然後顯示所建立帳戶的 3 個屬性</span><span class="sxs-lookup"><span data-stu-id="75c8c-129">The command create account with MinimumTlsVersion, AllowBlobPublicAccess, and disable SharedKey access to the account, and then show the the 3 properties of the created account</span></span> 

### <span data-ttu-id="75c8c-130">範例 10：使用 RoutingPreference 設定建立儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="75c8c-130">Example 10: Create a Storage account with RoutingPreference setting</span></span>
```powershell
PS C:\>$account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -PublishMicrosoftEndpoint $true -PublishInternetEndpoint $true -RoutingChoice MicrosoftRouting

PS C:\>$account.RoutingPreference

RoutingChoice    PublishMicrosoftEndpoints PublishInternetEndpoints
-------------    ------------------------- ------------------------
MicrosoftRouting                     True                     True

PS C:\>$account.PrimaryEndpoints

Blob               : https://mystorageaccount.blob.core.windows.net/
Queue              : https://mystorageaccount.queue.core.windows.net/
Table              : https://mystorageaccount.table.core.windows.net/
File               : https://mystorageaccount.file.core.windows.net/
Web                : https://mystorageaccount.z2.web.core.windows.net/
Dfs                : https://mystorageaccount.dfs.core.windows.net/
MicrosoftEndpoints : {"Blob":"https://mystorageaccount-microsoftrouting.blob.core.windows.net/","Queue":"https://mystorageaccount-microsoftrouting.queue.core.windows.net/","Table":"https://mystorageaccount-microsoftrouting.table.core.windows.net/","File":"ht
                     tps://mystorageaccount-microsoftrouting.file.core.windows.net/","Web":"https://mystorageaccount-microsoftrouting.z2.web.core.windows.net/","Dfs":"https://mystorageaccount-microsoftrouting.dfs.core.windows.net/"}
InternetEndpoints  : {"Blob":"https://mystorageaccount-internetrouting.blob.core.windows.net/","File":"https://mystorageaccount-internetrouting.file.core.windows.net/","Web":"https://mystorageaccount-internetrouting.z2.web.core.windows.net/","Dfs":"https://w
                     eirp3-internetrouting.dfs.core.windows.net/"}
```

<span data-ttu-id="75c8c-131">此命令會建立具有 RoutingPreference 設定儲存空間帳戶：PublishMicrosoftEndpoint 和 PublishInternetEndpoint 為 True，而 RoutingChoice 為 MicrosoftRouting。</span><span class="sxs-lookup"><span data-stu-id="75c8c-131">This command creates a Storage account with RoutingPreference setting: PublishMicrosoftEndpoint and PublishInternetEndpoint as true, and RoutingChoice as MicrosoftRouting.</span></span>

## <span data-ttu-id="75c8c-132">參數</span><span class="sxs-lookup"><span data-stu-id="75c8c-132">PARAMETERS</span></span>

### <span data-ttu-id="75c8c-133">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="75c8c-133">-AccessTier</span></span>
<span data-ttu-id="75c8c-134">指定此 Cmdlet 所建立之儲存空間帳戶的存取層級。</span><span class="sxs-lookup"><span data-stu-id="75c8c-134">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="75c8c-135">此參數可接受的值為：Hot 和 Cool。</span><span class="sxs-lookup"><span data-stu-id="75c8c-135">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="75c8c-136">如果您為 Kind 參數指定 BlobStorage值，則必須指定 *AccessTier 參數* 的值。</span><span class="sxs-lookup"><span data-stu-id="75c8c-136">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="75c8c-137">如果您指定此類型參數的儲存 *空間值，* 請勿指定 *AccessTier* 參數。</span><span class="sxs-lookup"><span data-stu-id="75c8c-137">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="75c8c-138">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="75c8c-138">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="75c8c-139">指定 Azure 儲存空間 (SID) 安全性識別碼。</span><span class="sxs-lookup"><span data-stu-id="75c8c-139">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="75c8c-140">當 -EnableActiveDirectoryDomainServicesForFile 設為 True 時，必須設定此參數。</span><span class="sxs-lookup"><span data-stu-id="75c8c-140">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="75c8c-141">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="75c8c-141">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="75c8c-142">指定網域 GUID。</span><span class="sxs-lookup"><span data-stu-id="75c8c-142">Specifies the domain GUID.</span></span> <span data-ttu-id="75c8c-143">當 -EnableActiveDirectoryDomainServicesForFile 設為 True 時，必須設定此參數。</span><span class="sxs-lookup"><span data-stu-id="75c8c-143">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="75c8c-144">-ActiveDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="75c8c-144">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="75c8c-145">指定 AD DNS 伺服器授權的主要網域。</span><span class="sxs-lookup"><span data-stu-id="75c8c-145">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="75c8c-146">當 -EnableActiveDirectoryDomainServicesForFile 設為 True 時，必須設定此參數。</span><span class="sxs-lookup"><span data-stu-id="75c8c-146">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="75c8c-147">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="75c8c-147">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="75c8c-148">指定 SID 中 (安全性) 。</span><span class="sxs-lookup"><span data-stu-id="75c8c-148">Specifies the security identifier (SID).</span></span> <span data-ttu-id="75c8c-149">當 -EnableActiveDirectoryDomainServicesForFile 設為 True 時，必須設定此參數。</span><span class="sxs-lookup"><span data-stu-id="75c8c-149">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="75c8c-150">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="75c8c-150">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="75c8c-151">指定要取得的 Active Directory 樹目錄樹。</span><span class="sxs-lookup"><span data-stu-id="75c8c-151">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="75c8c-152">當 -EnableActiveDirectoryDomainServicesForFile 設為 True 時，必須設定此參數。</span><span class="sxs-lookup"><span data-stu-id="75c8c-152">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="75c8c-153">-ActiveDirectoryNetBiosDomainName</span><span class="sxs-lookup"><span data-stu-id="75c8c-153">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="75c8c-154">指定 NetBIOS 功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="75c8c-154">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="75c8c-155">當 -EnableActiveDirectoryDomainServicesForFile 設為 True 時，必須設定此參數。</span><span class="sxs-lookup"><span data-stu-id="75c8c-155">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="75c8c-156">-AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="75c8c-156">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="75c8c-157">允許公用存取儲存帳戶中的所有 Blob 或容器。</span><span class="sxs-lookup"><span data-stu-id="75c8c-157">Allow public access to all blobs or containers in the storage account.</span></span> <span data-ttu-id="75c8c-158">此屬性的預設解譯為 True。</span><span class="sxs-lookup"><span data-stu-id="75c8c-158">The default interpretation is true for this property.</span></span>

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

### <span data-ttu-id="75c8c-159">-AllowSharedKeyAccess</span><span class="sxs-lookup"><span data-stu-id="75c8c-159">-AllowSharedKeyAccess</span></span>
<span data-ttu-id="75c8c-160">指出儲存空間帳戶是否允許透過共用金鑰使用帳戶便捷鍵獲得授權。</span><span class="sxs-lookup"><span data-stu-id="75c8c-160">Indicates whether the storage account permits requests to be authorized with the account access key via Shared Key.</span></span> <span data-ttu-id="75c8c-161">如果為 False，則所有要求 ，包括共用存取簽章，都必須使用 Azure Active Directory (Azure AD) 。</span><span class="sxs-lookup"><span data-stu-id="75c8c-161">If false, then all requests, including shared access signatures, must be authorized with Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="75c8c-162">預設值為 Null，相當於 True。</span><span class="sxs-lookup"><span data-stu-id="75c8c-162">The default value is null, which is equivalent to true.</span></span>

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

### <span data-ttu-id="75c8c-163">-AsJob</span><span class="sxs-lookup"><span data-stu-id="75c8c-163">-AsJob</span></span>
<span data-ttu-id="75c8c-164">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="75c8c-164">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="75c8c-165">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="75c8c-165">-AssignIdentity</span></span>
<span data-ttu-id="75c8c-166">為此儲存空間帳戶產生並指派新的儲存帳戶身分識別，以用於 Azure KeyVault 等重要管理服務。</span><span class="sxs-lookup"><span data-stu-id="75c8c-166">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="75c8c-167">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="75c8c-167">-CustomDomainName</span></span>
<span data-ttu-id="75c8c-168">指定儲存空間帳戶的自訂網功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="75c8c-168">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="75c8c-169">預設值為儲存空間。</span><span class="sxs-lookup"><span data-stu-id="75c8c-169">The default value is Storage.</span></span>

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

### <span data-ttu-id="75c8c-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75c8c-170">-DefaultProfile</span></span>
<span data-ttu-id="75c8c-171">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="75c8c-171">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75c8c-172">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="75c8c-172">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="75c8c-173">針對儲存帳戶啟用 Azure 檔案 Active Directory 網域服務驗證。</span><span class="sxs-lookup"><span data-stu-id="75c8c-173">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c8c-174">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="75c8c-174">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="75c8c-175">針對儲存帳戶啟用 Azure 檔案 Azure Active Directory 網域服務驗證。</span><span class="sxs-lookup"><span data-stu-id="75c8c-175">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AzureActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c8c-176">-EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="75c8c-176">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="75c8c-177">指出儲存空間帳戶是否啟用階層命名空間。</span><span class="sxs-lookup"><span data-stu-id="75c8c-177">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

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

### <span data-ttu-id="75c8c-178">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="75c8c-178">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="75c8c-179">指出儲存空間帳戶是否僅啟用 HTTPS 流量。</span><span class="sxs-lookup"><span data-stu-id="75c8c-179">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="75c8c-180">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="75c8c-180">-EnableLargeFileShare</span></span>
<span data-ttu-id="75c8c-181">指出儲存空間帳戶是否可支援容量超過 5 TiB 的大型檔案共用。</span><span class="sxs-lookup"><span data-stu-id="75c8c-181">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="75c8c-182">帳戶啟用後，就無法停用此功能。</span><span class="sxs-lookup"><span data-stu-id="75c8c-182">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="75c8c-183">目前僅支援 LRS 和 ZRS 複製類型，因此無法將帳戶轉換為異地重複帳戶。</span><span class="sxs-lookup"><span data-stu-id="75c8c-183">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="75c8c-184">若要深入瞭解，請于 https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="75c8c-184">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="75c8c-185">-EncryptionKeyTypeForQueue</span><span class="sxs-lookup"><span data-stu-id="75c8c-185">-EncryptionKeyTypeForQueue</span></span>
<span data-ttu-id="75c8c-186">設定佇列的加密金鑰類型。</span><span class="sxs-lookup"><span data-stu-id="75c8c-186">Set the Encryption KeyType for Queue.</span></span> <span data-ttu-id="75c8c-187">預設值為服務。</span><span class="sxs-lookup"><span data-stu-id="75c8c-187">The default value is Service.</span></span>
<span data-ttu-id="75c8c-188">-帳戶：佇列會使用帳戶範圍加密金鑰加密。</span><span class="sxs-lookup"><span data-stu-id="75c8c-188">-Account: Queue will be encrypted with account-scoped encryption key.</span></span> <span data-ttu-id="75c8c-189">-服務：佇列一定會使用金鑰加密Service-Managed加密。</span><span class="sxs-lookup"><span data-stu-id="75c8c-189">-Service: Queue will always be encrypted with Service-Managed keys.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Service, Account

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c8c-190">-EncryptionKeyTypeForTable</span><span class="sxs-lookup"><span data-stu-id="75c8c-190">-EncryptionKeyTypeForTable</span></span>
<span data-ttu-id="75c8c-191">設定資料表的加密金鑰類型。</span><span class="sxs-lookup"><span data-stu-id="75c8c-191">Set the Encryption KeyType for Table.</span></span> <span data-ttu-id="75c8c-192">預設值為服務。</span><span class="sxs-lookup"><span data-stu-id="75c8c-192">The default value is Service.</span></span>
- <span data-ttu-id="75c8c-193">帳戶：資料表會使用帳戶範圍加密金鑰加密。</span><span class="sxs-lookup"><span data-stu-id="75c8c-193">Account: Table will be encrypted with account-scoped encryption key.</span></span> 
- <span data-ttu-id="75c8c-194">服務：資料表一定會使用Service-Managed加密。</span><span class="sxs-lookup"><span data-stu-id="75c8c-194">Service: Table will always be encrypted with Service-Managed keys.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Service, Account

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c8c-195">-Kind</span><span class="sxs-lookup"><span data-stu-id="75c8c-195">-Kind</span></span>
<span data-ttu-id="75c8c-196">指定此 Cmdlet 所建立儲存空間帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="75c8c-196">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="75c8c-197">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="75c8c-197">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="75c8c-198">存儲。</span><span class="sxs-lookup"><span data-stu-id="75c8c-198">Storage.</span></span> <span data-ttu-id="75c8c-199">支援 Blob、資料表、佇列、檔案和磁片的儲存空間的一般用途儲存帳戶。</span><span class="sxs-lookup"><span data-stu-id="75c8c-199">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="75c8c-200">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="75c8c-200">StorageV2.</span></span> <span data-ttu-id="75c8c-201">一般用途版本 2 (GPv2) 儲存空間帳戶，支援 Blob、資料表、佇列、檔案和磁片，以及資料分層等進位功能。</span><span class="sxs-lookup"><span data-stu-id="75c8c-201">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="75c8c-202">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="75c8c-202">BlobStorage.</span></span> <span data-ttu-id="75c8c-203">僅支援 Blob 儲存空間的 Blob 儲存體帳戶。</span><span class="sxs-lookup"><span data-stu-id="75c8c-203">Blob Storage account which supports storage of Blobs only.</span></span>
- <span data-ttu-id="75c8c-204">BlockBlobStorage.</span><span class="sxs-lookup"><span data-stu-id="75c8c-204">BlockBlobStorage.</span></span> <span data-ttu-id="75c8c-205">封鎖只支援封鎖 Blob 儲存空間的 Blob 儲存體帳戶。</span><span class="sxs-lookup"><span data-stu-id="75c8c-205">Block Blob Storage account which supports storage of Block Blobs only.</span></span>
- <span data-ttu-id="75c8c-206">FileStorage.</span><span class="sxs-lookup"><span data-stu-id="75c8c-206">FileStorage.</span></span> <span data-ttu-id="75c8c-207">僅支援儲存檔案的檔案儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="75c8c-207">File Storage account which supports storage of Files only.</span></span>
<span data-ttu-id="75c8c-208">預設值為 StorageV2。</span><span class="sxs-lookup"><span data-stu-id="75c8c-208">The default value is StorageV2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage, BlockBlobStorage, FileStorage

Required: False
Position: Named
Default value: StorageV2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c8c-209">-位置</span><span class="sxs-lookup"><span data-stu-id="75c8c-209">-Location</span></span>
<span data-ttu-id="75c8c-210">指定要建立儲存空間帳戶的位置。</span><span class="sxs-lookup"><span data-stu-id="75c8c-210">Specifies the location of the Storage account to create.</span></span>

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

### <span data-ttu-id="75c8c-211">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="75c8c-211">-MinimumTlsVersion</span></span>
<span data-ttu-id="75c8c-212">儲存空間要求允許的最小 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="75c8c-212">The minimum TLS version to be permitted on requests to storage.</span></span> <span data-ttu-id="75c8c-213">此屬性的預設解譯為 TLS 1.0。</span><span class="sxs-lookup"><span data-stu-id="75c8c-213">The default interpretation is TLS 1.0 for this property.</span></span>

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

### <span data-ttu-id="75c8c-214">-名稱</span><span class="sxs-lookup"><span data-stu-id="75c8c-214">-Name</span></span>
<span data-ttu-id="75c8c-215">指定要建立之儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="75c8c-215">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="75c8c-216">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="75c8c-216">-NetworkRuleSet</span></span>
<span data-ttu-id="75c8c-217">NetworkRuleSet 可用來定義一組防火牆和虛擬網路的組組設定規則，以及設定網路屬性值 ，例如允許忽略規則的服務，以及如何處理與任何已定義規則不相符的要求。</span><span class="sxs-lookup"><span data-stu-id="75c8c-217">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="75c8c-218">-PublishInternetEndpoint</span><span class="sxs-lookup"><span data-stu-id="75c8c-218">-PublishInternetEndpoint</span></span>
<span data-ttu-id="75c8c-219">指出是否要發佈網際網路路由儲存端點</span><span class="sxs-lookup"><span data-stu-id="75c8c-219">Indicates whether internet  routing storage endpoints are to be published</span></span>

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

### <span data-ttu-id="75c8c-220">-PublishMicrosoftEndpoint</span><span class="sxs-lookup"><span data-stu-id="75c8c-220">-PublishMicrosoftEndpoint</span></span>
<span data-ttu-id="75c8c-221">指出是否要發佈 Microsoft 路由儲存端點</span><span class="sxs-lookup"><span data-stu-id="75c8c-221">Indicates whether microsoft routing storage endpoints are to be published</span></span>

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

### <span data-ttu-id="75c8c-222">-RequireInfracryptEncryption</span><span class="sxs-lookup"><span data-stu-id="75c8c-222">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="75c8c-223">服務會針對靜態資料，使用平臺管理金鑰來使用次要加密層。</span><span class="sxs-lookup"><span data-stu-id="75c8c-223">The service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="75c8c-224">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75c8c-224">-ResourceGroupName</span></span>
<span data-ttu-id="75c8c-225">指定要新增儲存空間帳戶的資源組名。</span><span class="sxs-lookup"><span data-stu-id="75c8c-225">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="75c8c-226">-RoutingChoice</span><span class="sxs-lookup"><span data-stu-id="75c8c-226">-RoutingChoice</span></span>
<span data-ttu-id="75c8c-227">路由選擇會定義使用者選擇的網路路由類型。</span><span class="sxs-lookup"><span data-stu-id="75c8c-227">Routing Choice defines the kind of network routing opted by the user.</span></span> <span data-ttu-id="75c8c-228">可能的值包括：'MicrosoftRouting'，'InternetRouting'</span><span class="sxs-lookup"><span data-stu-id="75c8c-228">Possible values include: 'MicrosoftRouting', 'InternetRouting'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MicrosoftRouting, InternetRouting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c8c-229">-SKUName</span><span class="sxs-lookup"><span data-stu-id="75c8c-229">-SkuName</span></span>
<span data-ttu-id="75c8c-230">指定此 Cmdlet 所建立之儲存空間帳戶的 SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="75c8c-230">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="75c8c-231">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="75c8c-231">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="75c8c-232">Standard_LRS。</span><span class="sxs-lookup"><span data-stu-id="75c8c-232">Standard_LRS.</span></span> <span data-ttu-id="75c8c-233">本地多餘的儲存空間。</span><span class="sxs-lookup"><span data-stu-id="75c8c-233">Locally-redundant storage.</span></span>
- <span data-ttu-id="75c8c-234">Standard_ZRS。</span><span class="sxs-lookup"><span data-stu-id="75c8c-234">Standard_ZRS.</span></span> <span data-ttu-id="75c8c-235">區域多餘的儲存空間。</span><span class="sxs-lookup"><span data-stu-id="75c8c-235">Zone-redundant storage.</span></span>
- <span data-ttu-id="75c8c-236">Standard_GRS。</span><span class="sxs-lookup"><span data-stu-id="75c8c-236">Standard_GRS.</span></span> <span data-ttu-id="75c8c-237">異地重複儲存空間。</span><span class="sxs-lookup"><span data-stu-id="75c8c-237">Geo-redundant storage.</span></span>
- <span data-ttu-id="75c8c-238">Standard_RAGRS。</span><span class="sxs-lookup"><span data-stu-id="75c8c-238">Standard_RAGRS.</span></span> <span data-ttu-id="75c8c-239">讀取存取異地重複儲存空間。</span><span class="sxs-lookup"><span data-stu-id="75c8c-239">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="75c8c-240">Premium_LRS。</span><span class="sxs-lookup"><span data-stu-id="75c8c-240">Premium_LRS.</span></span> <span data-ttu-id="75c8c-241">進一無二的儲存空間。</span><span class="sxs-lookup"><span data-stu-id="75c8c-241">Premium locally-redundant storage.</span></span>
- <span data-ttu-id="75c8c-242">Premium_ZRS。</span><span class="sxs-lookup"><span data-stu-id="75c8c-242">Premium_ZRS.</span></span> <span data-ttu-id="75c8c-243">進一無二的區域重複儲存空間。</span><span class="sxs-lookup"><span data-stu-id="75c8c-243">Premium zone-redundant storage.</span></span>
- <span data-ttu-id="75c8c-244">Standard_GZRS - 異地重複區域 -多餘的儲存空間。</span><span class="sxs-lookup"><span data-stu-id="75c8c-244">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="75c8c-245">Standard_RAGZRS - 讀取存取異地重複區域-多餘的儲存空間。</span><span class="sxs-lookup"><span data-stu-id="75c8c-245">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS, Premium_ZRS, Standard_GZRS, Standard_RAGZRS

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75c8c-246">-標記</span><span class="sxs-lookup"><span data-stu-id="75c8c-246">-Tag</span></span>
<span data-ttu-id="75c8c-247">以雜湊表格形式設定為伺服器上標記的索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="75c8c-247">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="75c8c-248">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="75c8c-248">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="75c8c-249">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="75c8c-249">-UseSubDomain</span></span>
<span data-ttu-id="75c8c-250">指出是否要啟用間接 CName 驗證。</span><span class="sxs-lookup"><span data-stu-id="75c8c-250">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="75c8c-251">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75c8c-251">CommonParameters</span></span>
<span data-ttu-id="75c8c-252">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="75c8c-252">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75c8c-253">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="75c8c-253">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75c8c-254">輸入</span><span class="sxs-lookup"><span data-stu-id="75c8c-254">INPUTS</span></span>

### <span data-ttu-id="75c8c-255">System.String</span><span class="sxs-lookup"><span data-stu-id="75c8c-255">System.String</span></span>

## <span data-ttu-id="75c8c-256">輸出</span><span class="sxs-lookup"><span data-stu-id="75c8c-256">OUTPUTS</span></span>

### <span data-ttu-id="75c8c-257">Microsoft.Azure.Commands.management.storage.models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="75c8c-257">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="75c8c-258">筆記</span><span class="sxs-lookup"><span data-stu-id="75c8c-258">NOTES</span></span>

## <span data-ttu-id="75c8c-259">相關連結</span><span class="sxs-lookup"><span data-stu-id="75c8c-259">RELATED LINKS</span></span>

[<span data-ttu-id="75c8c-260">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="75c8c-260">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="75c8c-261">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="75c8c-261">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="75c8c-262">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="75c8c-262">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)
