---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: 022c27b3eec589e395e1044f165ee9f8f17d1cad
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129748"
---
# <span data-ttu-id="352ac-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="352ac-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="352ac-102">摘要</span><span class="sxs-lookup"><span data-stu-id="352ac-102">SYNOPSIS</span></span>
<span data-ttu-id="352ac-103">建立儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="352ac-103">Creates a Storage account.</span></span>

## <span data-ttu-id="352ac-104">句法</span><span class="sxs-lookup"><span data-stu-id="352ac-104">SYNTAX</span></span>

### <span data-ttu-id="352ac-105">AzureActiveDirectoryDomainServicesForFile (預設) </span><span class="sxs-lookup"><span data-stu-id="352ac-105">AzureActiveDirectoryDomainServicesForFile (Default)</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-AsJob] [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>]
 [-RequireInfrastructureEncryption] [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="352ac-106">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="352ac-106">ActiveDirectoryDomainServicesForFile</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableLargeFileShare]
 [-EnableActiveDirectoryDomainServicesForFile <Boolean>] [-ActiveDirectoryDomainName <String>]
 [-ActiveDirectoryNetBiosDomainName <String>] [-ActiveDirectoryForestName <String>]
 [-ActiveDirectoryDomainGuid <String>] [-ActiveDirectoryDomainSid <String>]
 [-ActiveDirectoryAzureStorageSid <String>] [-AsJob] [-EncryptionKeyTypeForTable <String>]
 [-EncryptionKeyTypeForQueue <String>] [-RequireInfrastructureEncryption] [-AllowBlobPublicAccess <Boolean>]
 [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="352ac-107">說明</span><span class="sxs-lookup"><span data-stu-id="352ac-107">DESCRIPTION</span></span>
<span data-ttu-id="352ac-108">**新的-AzStorageAccount** Cmdlet 會建立 Azure 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="352ac-108">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="352ac-109">示例</span><span class="sxs-lookup"><span data-stu-id="352ac-109">EXAMPLES</span></span>

### <span data-ttu-id="352ac-110">範例1：建立儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="352ac-110">Example 1: Create a Storage account</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="352ac-111">這個命令會為 [資源] 群組名稱 MyResourceGroup 建立儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="352ac-111">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="352ac-112">範例2：使用 BlobStorage 類型和熱 AccessTier 建立 Blob 儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="352ac-112">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="352ac-113">這個命令會建立一個 BlobStorage 類型和熱 AccessTier 的 Blob 儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="352ac-113">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="352ac-114">範例3：使用類型 StorageV2 建立儲存空間帳戶，並產生並指派 Azure KeyVault 的身分識別。</span><span class="sxs-lookup"><span data-stu-id="352ac-114">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="352ac-115">這個命令會建立 StorageV2 類型的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="352ac-115">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="352ac-116">它也會產生並指派可用於透過 Azure KeyVault 管理帳戶金鑰的身分識別。</span><span class="sxs-lookup"><span data-stu-id="352ac-116">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="352ac-117">範例4：從 JSON 建立 NetworkRuleSet 的儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="352ac-117">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="352ac-118">這個命令會建立具有 JSON NetworkRuleSet 屬性的儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="352ac-118">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="352ac-119">範例5：建立已啟用階層命名空間的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="352ac-119">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="352ac-120">這個命令會建立已啟用階層命名空間的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="352ac-120">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

### <span data-ttu-id="352ac-121">範例6：建立擁有 Azure 檔案 AAD DS 驗證的儲存空間帳戶，並啟用大型檔案共用。</span><span class="sxs-lookup"><span data-stu-id="352ac-121">Example 6: Create a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

<span data-ttu-id="352ac-122">這個命令會建立擁有 Azure 檔案 AAD DS 驗證的儲存空間帳戶，並啟用大型檔案共用。</span><span class="sxs-lookup"><span data-stu-id="352ac-122">This command creates a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>

### <span data-ttu-id="352ac-123">範例7：使用啟用檔案建立儲存空間帳戶 Active Directory 網域服務驗證。</span><span class="sxs-lookup"><span data-stu-id="352ac-123">Example 7: Create a Storage account with enable Files Active Directory Domain Service Authentication.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
```

<span data-ttu-id="352ac-124">這個命令會建立儲存帳戶 withenable 檔案 Active Directory 網域服務驗證。</span><span class="sxs-lookup"><span data-stu-id="352ac-124">This command creates a Storage account withenable Files Active Directory Domain Service Authentication.</span></span>

### <span data-ttu-id="352ac-125">範例8：使用 [佇列] 和 [資料表服務] 建立儲存空間帳戶使用帳戶範圍的加密金鑰，並需要基礎結構加密。</span><span class="sxs-lookup"><span data-stu-id="352ac-125">Example 8: Create a Storage account with Queue and Table Service use account-scoped encryption key, and Require Infrastructure Encryption.</span></span>
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

<span data-ttu-id="352ac-126">這個命令會使用 [佇列] 和 [資料表服務] 來建立儲存空間帳戶，且需要基礎結構加密，因此佇列和資料表將會使用與 Blob 和檔案服務相同的加密金鑰，因此服務將在 rest 上使用平臺管理金鑰來套用次要加密層級。</span><span class="sxs-lookup"><span data-stu-id="352ac-126">This command creates a Storage account with Queue and Table Service use account-scoped encryption key and Require Infrastructure Encryption, so Queue and Table will use same encryption key with Blob and File service, and the service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>
<span data-ttu-id="352ac-127">然後取得 [儲存空間] 帳戶的屬性，並查看 [佇列] 和 [資料表] 服務的加密 keytype，以及 RequireInfrastructureEncryption [值]。</span><span class="sxs-lookup"><span data-stu-id="352ac-127">Then get the Storage account properties, and view the encryption keytype of Queue and Table Service, and RequireInfrastructureEncryption value.</span></span>

### <span data-ttu-id="352ac-128">範例9：建立帳戶 MinimumTlsVersion 和 AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="352ac-128">Example 9: Create account MinimumTlsVersion  and AllowBlobPublicAccess</span></span>
```
PS C:\> $account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2 -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False
```

<span data-ttu-id="352ac-129">命令會使用 MinimumTlsVersion 和 AllowBlobPublicAccess 建立帳戶，然後顯示已建立帳戶的2個屬性</span><span class="sxs-lookup"><span data-stu-id="352ac-129">The command create account with MinimumTlsVersion  and AllowBlobPublicAccess, and then show the the 2 properties of the created account</span></span> 

## <span data-ttu-id="352ac-130">參數</span><span class="sxs-lookup"><span data-stu-id="352ac-130">PARAMETERS</span></span>

### <span data-ttu-id="352ac-131">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="352ac-131">-AccessTier</span></span>
<span data-ttu-id="352ac-132">指定此 Cmdlet 所建立之儲存空間帳戶的存取層。</span><span class="sxs-lookup"><span data-stu-id="352ac-132">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="352ac-133">此參數可接受的值為： [熱] 和 [超酷]。</span><span class="sxs-lookup"><span data-stu-id="352ac-133">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="352ac-134">如果您為 *Kind* 參數指定 BlobStorage 值，您必須指定 *AccessTier* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="352ac-134">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="352ac-135">如果您指定此 *類型* 參數的 Storage 值，請勿指定 *AccessTier* 參數。</span><span class="sxs-lookup"><span data-stu-id="352ac-135">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="352ac-136">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="352ac-136">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="352ac-137">指定 Azure 儲存空間 (SID) 的安全性識別碼。</span><span class="sxs-lookup"><span data-stu-id="352ac-137">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="352ac-138">此參數必須在-EnableActiveDirectoryDomainServicesForFile 設定為 true 時設定。</span><span class="sxs-lookup"><span data-stu-id="352ac-138">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="352ac-139">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="352ac-139">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="352ac-140">指定網域 GUID。</span><span class="sxs-lookup"><span data-stu-id="352ac-140">Specifies the domain GUID.</span></span> <span data-ttu-id="352ac-141">此參數必須在-EnableActiveDirectoryDomainServicesForFile 設定為 true 時設定。</span><span class="sxs-lookup"><span data-stu-id="352ac-141">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="352ac-142">-ActiveDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="352ac-142">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="352ac-143">指定 AD DNS 伺服器擁有權威的主域。</span><span class="sxs-lookup"><span data-stu-id="352ac-143">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="352ac-144">此參數必須在-EnableActiveDirectoryDomainServicesForFile 設定為 true 時設定。</span><span class="sxs-lookup"><span data-stu-id="352ac-144">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="352ac-145">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="352ac-145">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="352ac-146">指定 (SID) 的安全性識別碼。</span><span class="sxs-lookup"><span data-stu-id="352ac-146">Specifies the security identifier (SID).</span></span> <span data-ttu-id="352ac-147">此參數必須在-EnableActiveDirectoryDomainServicesForFile 設定為 true 時設定。</span><span class="sxs-lookup"><span data-stu-id="352ac-147">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="352ac-148">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="352ac-148">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="352ac-149">指定要取得的 Active Directory 林。</span><span class="sxs-lookup"><span data-stu-id="352ac-149">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="352ac-150">此參數必須在-EnableActiveDirectoryDomainServicesForFile 設定為 true 時設定。</span><span class="sxs-lookup"><span data-stu-id="352ac-150">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="352ac-151">-ActiveDirectoryNetBiosDomainName</span><span class="sxs-lookup"><span data-stu-id="352ac-151">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="352ac-152">指定 NetBIOS 功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="352ac-152">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="352ac-153">此參數必須在-EnableActiveDirectoryDomainServicesForFile 設定為 true 時設定。</span><span class="sxs-lookup"><span data-stu-id="352ac-153">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="352ac-154">-AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="352ac-154">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="352ac-155">允許公用存取儲存空間帳戶中的所有 blob 或容器。</span><span class="sxs-lookup"><span data-stu-id="352ac-155">Allow public access to all blobs or containers in the storage account.</span></span> <span data-ttu-id="352ac-156">這個屬性的預設轉譯為 true。</span><span class="sxs-lookup"><span data-stu-id="352ac-156">The default interpretation is true for this property.</span></span>

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

### <span data-ttu-id="352ac-157">-AsJob</span><span class="sxs-lookup"><span data-stu-id="352ac-157">-AsJob</span></span>
<span data-ttu-id="352ac-158">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="352ac-158">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="352ac-159">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="352ac-159">-AssignIdentity</span></span>
<span data-ttu-id="352ac-160">針對此儲存空間帳戶產生並指派新的儲存空間帳戶身分識別，以搭配 Azure KeyVault 等金鑰管理服務使用。</span><span class="sxs-lookup"><span data-stu-id="352ac-160">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="352ac-161">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="352ac-161">-CustomDomainName</span></span>
<span data-ttu-id="352ac-162">指定儲存空間帳戶之自訂網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="352ac-162">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="352ac-163">預設值為 [儲存]。</span><span class="sxs-lookup"><span data-stu-id="352ac-163">The default value is Storage.</span></span>

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

### <span data-ttu-id="352ac-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="352ac-164">-DefaultProfile</span></span>
<span data-ttu-id="352ac-165">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="352ac-165">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="352ac-166">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="352ac-166">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="352ac-167">針對儲存空間帳戶啟用 Azure Files Active Directory 網域服務驗證。</span><span class="sxs-lookup"><span data-stu-id="352ac-167">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="352ac-168">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="352ac-168">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="352ac-169">針對儲存空間帳戶啟用 Azure Active Directory 網域服務驗證。</span><span class="sxs-lookup"><span data-stu-id="352ac-169">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="352ac-170">-EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="352ac-170">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="352ac-171">指示儲存空間帳戶是否啟用階層命名空間。</span><span class="sxs-lookup"><span data-stu-id="352ac-171">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

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

### <span data-ttu-id="352ac-172">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="352ac-172">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="352ac-173">指出儲存空間帳戶是否只啟用 HTTPS 流量。</span><span class="sxs-lookup"><span data-stu-id="352ac-173">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="352ac-174">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="352ac-174">-EnableLargeFileShare</span></span>
<span data-ttu-id="352ac-175">指示儲存空間帳戶是否可支援超過5個 TiB 容量的大型檔案共用。</span><span class="sxs-lookup"><span data-stu-id="352ac-175">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="352ac-176">一旦啟用帳戶，就無法停用此功能。</span><span class="sxs-lookup"><span data-stu-id="352ac-176">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="352ac-177">目前僅支援 LRS 和 ZRS 複製類型，因此不可能將帳戶轉換成地域冗余帳戶。</span><span class="sxs-lookup"><span data-stu-id="352ac-177">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="352ac-178">深入瞭解 https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="352ac-178">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="352ac-179">-EncryptionKeyTypeForQueue</span><span class="sxs-lookup"><span data-stu-id="352ac-179">-EncryptionKeyTypeForQueue</span></span>
<span data-ttu-id="352ac-180">設定佇列的加密 KeyType。</span><span class="sxs-lookup"><span data-stu-id="352ac-180">Set the Encryption KeyType for Queue.</span></span> <span data-ttu-id="352ac-181">預設值為 [服務]。</span><span class="sxs-lookup"><span data-stu-id="352ac-181">The default value is Service.</span></span>
<span data-ttu-id="352ac-182">-帳戶：將使用帳戶範圍的加密金鑰來加密佇列。</span><span class="sxs-lookup"><span data-stu-id="352ac-182">-Account: Queue will be encrypted with account-scoped encryption key.</span></span> <span data-ttu-id="352ac-183">-服務：將永遠使用 Service-Managed 金鑰來加密佇列。</span><span class="sxs-lookup"><span data-stu-id="352ac-183">-Service: Queue will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="352ac-184">-EncryptionKeyTypeForTable</span><span class="sxs-lookup"><span data-stu-id="352ac-184">-EncryptionKeyTypeForTable</span></span>
<span data-ttu-id="352ac-185">設定資料表的加密 KeyType。</span><span class="sxs-lookup"><span data-stu-id="352ac-185">Set the Encryption KeyType for Table.</span></span> <span data-ttu-id="352ac-186">預設值為 [服務]。</span><span class="sxs-lookup"><span data-stu-id="352ac-186">The default value is Service.</span></span>
- <span data-ttu-id="352ac-187">帳戶：表格將使用帳戶範圍的加密金鑰加密。</span><span class="sxs-lookup"><span data-stu-id="352ac-187">Account: Table will be encrypted with account-scoped encryption key.</span></span> 
- <span data-ttu-id="352ac-188">服務：表格將一直使用 Service-Managed 金鑰進行加密。</span><span class="sxs-lookup"><span data-stu-id="352ac-188">Service: Table will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="352ac-189">類型</span><span class="sxs-lookup"><span data-stu-id="352ac-189">-Kind</span></span>
<span data-ttu-id="352ac-190">指定這個 Cmdlet 所建立的儲存空間帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="352ac-190">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="352ac-191">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="352ac-191">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="352ac-192">容量.</span><span class="sxs-lookup"><span data-stu-id="352ac-192">Storage.</span></span> <span data-ttu-id="352ac-193">支援 Blob、表格、佇列、檔案和磁片儲存的一般用途儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="352ac-193">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="352ac-194">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="352ac-194">StorageV2.</span></span> <span data-ttu-id="352ac-195">一般用途版本 2 (GPv2) 儲存空間帳戶（支援 Blob、表格、佇列、檔案和磁片），以及資料分層等高級功能。</span><span class="sxs-lookup"><span data-stu-id="352ac-195">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="352ac-196">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="352ac-196">BlobStorage.</span></span> <span data-ttu-id="352ac-197">僅支援以 Blob 儲存的 blob 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="352ac-197">Blob Storage account which supports storage of Blobs only.</span></span>
- <span data-ttu-id="352ac-198">BlockBlobStorage.</span><span class="sxs-lookup"><span data-stu-id="352ac-198">BlockBlobStorage.</span></span> <span data-ttu-id="352ac-199">僅支援區塊 Blob 儲存的封鎖 Blob 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="352ac-199">Block Blob Storage account which supports storage of Block Blobs only.</span></span>
- <span data-ttu-id="352ac-200">FileStorage.</span><span class="sxs-lookup"><span data-stu-id="352ac-200">FileStorage.</span></span> <span data-ttu-id="352ac-201">僅支援儲存檔案的檔案儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="352ac-201">File Storage account which supports storage of Files only.</span></span>
<span data-ttu-id="352ac-202">預設值為 StorageV2。</span><span class="sxs-lookup"><span data-stu-id="352ac-202">The default value is StorageV2.</span></span>

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

### <span data-ttu-id="352ac-203">-位置</span><span class="sxs-lookup"><span data-stu-id="352ac-203">-Location</span></span>
<span data-ttu-id="352ac-204">指定要建立的儲存空間帳戶位置。</span><span class="sxs-lookup"><span data-stu-id="352ac-204">Specifies the location of the Storage account to create.</span></span>

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

### <span data-ttu-id="352ac-205">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="352ac-205">-MinimumTlsVersion</span></span>
<span data-ttu-id="352ac-206">針對儲存空間要求所允許的最小 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="352ac-206">The minimum TLS version to be permitted on requests to storage.</span></span> <span data-ttu-id="352ac-207">這個屬性的預設轉譯是 TLS 1.0。</span><span class="sxs-lookup"><span data-stu-id="352ac-207">The default interpretation is TLS 1.0 for this property.</span></span>

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

### <span data-ttu-id="352ac-208">-名稱</span><span class="sxs-lookup"><span data-stu-id="352ac-208">-Name</span></span>
<span data-ttu-id="352ac-209">指定要建立的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="352ac-209">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="352ac-210">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="352ac-210">-NetworkRuleSet</span></span>
<span data-ttu-id="352ac-211">NetworkRuleSet 是用來定義防火牆和虛擬網路的一組設定規則，以及設定網路屬性的值，例如允許繞過規則的服務，以及如何處理不符合任何已定義規則的要求。</span><span class="sxs-lookup"><span data-stu-id="352ac-211">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="352ac-212">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="352ac-212">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="352ac-213">此服務將使用平臺管理金鑰來在 rest 上套用資料的次要加密層級。</span><span class="sxs-lookup"><span data-stu-id="352ac-213">The service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="352ac-214">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="352ac-214">-ResourceGroupName</span></span>
<span data-ttu-id="352ac-215">指定要新增儲存空間帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="352ac-215">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="352ac-216">-SkuName</span><span class="sxs-lookup"><span data-stu-id="352ac-216">-SkuName</span></span>
<span data-ttu-id="352ac-217">指定此 Cmdlet 所建立之儲存空間帳戶的 SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="352ac-217">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="352ac-218">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="352ac-218">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="352ac-219">Standard_LRS]。</span><span class="sxs-lookup"><span data-stu-id="352ac-219">Standard_LRS.</span></span> <span data-ttu-id="352ac-220">本機冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="352ac-220">Locally-redundant storage.</span></span>
- <span data-ttu-id="352ac-221">Standard_ZRS]。</span><span class="sxs-lookup"><span data-stu-id="352ac-221">Standard_ZRS.</span></span> <span data-ttu-id="352ac-222">區域冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="352ac-222">Zone-redundant storage.</span></span>
- <span data-ttu-id="352ac-223">Standard_GRS]。</span><span class="sxs-lookup"><span data-stu-id="352ac-223">Standard_GRS.</span></span> <span data-ttu-id="352ac-224">地域冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="352ac-224">Geo-redundant storage.</span></span>
- <span data-ttu-id="352ac-225">Standard_RAGRS]。</span><span class="sxs-lookup"><span data-stu-id="352ac-225">Standard_RAGRS.</span></span> <span data-ttu-id="352ac-226">讀取 access 地域冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="352ac-226">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="352ac-227">Premium_LRS]。</span><span class="sxs-lookup"><span data-stu-id="352ac-227">Premium_LRS.</span></span> <span data-ttu-id="352ac-228">[特優] 本機-冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="352ac-228">Premium locally-redundant storage.</span></span>
- <span data-ttu-id="352ac-229">Premium_ZRS]。</span><span class="sxs-lookup"><span data-stu-id="352ac-229">Premium_ZRS.</span></span> <span data-ttu-id="352ac-230">[特優區域-冗余儲存空間]。</span><span class="sxs-lookup"><span data-stu-id="352ac-230">Premium zone-redundant storage.</span></span>
- <span data-ttu-id="352ac-231">Standard_GZRS 地域冗余區域-冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="352ac-231">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="352ac-232">Standard_RAGZRS 讀取 access 地域冗余區域-冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="352ac-232">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>

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

### <span data-ttu-id="352ac-233">-Tag</span><span class="sxs-lookup"><span data-stu-id="352ac-233">-Tag</span></span>
<span data-ttu-id="352ac-234">在伺服器上將雜湊表的格式設定為標記的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="352ac-234">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="352ac-235">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="352ac-235">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="352ac-236">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="352ac-236">-UseSubDomain</span></span>
<span data-ttu-id="352ac-237">指示是否要啟用間接 CName 驗證。</span><span class="sxs-lookup"><span data-stu-id="352ac-237">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="352ac-238">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="352ac-238">CommonParameters</span></span>
<span data-ttu-id="352ac-239">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="352ac-239">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="352ac-240">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="352ac-240">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="352ac-241">輸入</span><span class="sxs-lookup"><span data-stu-id="352ac-241">INPUTS</span></span>

### <span data-ttu-id="352ac-242">System.object</span><span class="sxs-lookup"><span data-stu-id="352ac-242">System.String</span></span>

## <span data-ttu-id="352ac-243">輸出</span><span class="sxs-lookup"><span data-stu-id="352ac-243">OUTPUTS</span></span>

### <span data-ttu-id="352ac-244">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="352ac-244">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="352ac-245">筆記</span><span class="sxs-lookup"><span data-stu-id="352ac-245">NOTES</span></span>

## <span data-ttu-id="352ac-246">相關連結</span><span class="sxs-lookup"><span data-stu-id="352ac-246">RELATED LINKS</span></span>

[<span data-ttu-id="352ac-247">AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="352ac-247">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="352ac-248">移除-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="352ac-248">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="352ac-249">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="352ac-249">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)
