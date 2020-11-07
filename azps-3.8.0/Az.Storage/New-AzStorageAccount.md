---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: c88e56a485f9e42daf229667ab4c07d7a7464578
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959088"
---
# <span data-ttu-id="ee8a0-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ee8a0-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="ee8a0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ee8a0-102">SYNOPSIS</span></span>
<span data-ttu-id="ee8a0-103">建立儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-103">Creates a Storage account.</span></span>

## <span data-ttu-id="ee8a0-104">句法</span><span class="sxs-lookup"><span data-stu-id="ee8a0-104">SYNTAX</span></span>

```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-AsJob] [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee8a0-105">說明</span><span class="sxs-lookup"><span data-stu-id="ee8a0-105">DESCRIPTION</span></span>
<span data-ttu-id="ee8a0-106">**新的-AzStorageAccount** Cmdlet 會建立 Azure 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-106">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="ee8a0-107">示例</span><span class="sxs-lookup"><span data-stu-id="ee8a0-107">EXAMPLES</span></span>

### <span data-ttu-id="ee8a0-108">範例1：建立儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="ee8a0-108">Example 1: Create a Storage account</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="ee8a0-109">這個命令會為 [資源] 群組名稱 MyResourceGroup 建立儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-109">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="ee8a0-110">範例2：使用 BlobStorage 類型和熱 AccessTier 建立 Blob 儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="ee8a0-110">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="ee8a0-111">這個命令會建立一個 BlobStorage 類型和熱 AccessTier 的 Blob 儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="ee8a0-111">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="ee8a0-112">範例3：使用類型 StorageV2 建立儲存空間帳戶，並產生並指派 Azure KeyVault 的身分識別。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-112">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="ee8a0-113">這個命令會建立 StorageV2 類型的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-113">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="ee8a0-114">它也會產生並指派可用於透過 Azure KeyVault 管理帳戶金鑰的身分識別。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-114">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="ee8a0-115">範例4：從 JSON 建立 NetworkRuleSet 的儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="ee8a0-115">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="ee8a0-116">這個命令會建立具有 JSON NetworkRuleSet 屬性的儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="ee8a0-116">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="ee8a0-117">範例5：建立已啟用階層命名空間的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-117">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="ee8a0-118">這個命令會建立已啟用階層命名空間的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-118">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

### <span data-ttu-id="ee8a0-119">範例6：建立擁有 Azure 檔案 AAD DS 驗證的儲存空間帳戶，並啟用大型檔案共用。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-119">Example 6: Create a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

<span data-ttu-id="ee8a0-120">這個命令會建立擁有 Azure 檔案 AAD DS 驗證的儲存空間帳戶，並啟用大型檔案共用。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-120">This command creates a Storage account with Azure Files AAD DS Authentication, and enable large file share..</span></span>

### <span data-ttu-id="ee8a0-121">範例8：使用 [佇列] 和 [資料表服務] 建立儲存空間帳戶使用帳戶範圍的加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-121">Example 8: Create a Storage account with Queue and Table Service use account-scoped encryption key.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EncryptionKeyTypeForTable Account -EncryptionKeyTypeForQueue Account

PS C:\>$account = get-AzStorageAccount -ResourceGroupName $rgname -StorageAccountName $accountName

PS C:\>$account.Encryption.Services.Queue

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\>$account.Encryption.Services.Table

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account
```

<span data-ttu-id="ee8a0-122">這個命令會建立包含佇列和資料表服務的儲存空間帳戶使用帳戶範圍的加密金鑰，所以佇列和資料表將會使用與 Blob 和檔案服務相同的加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-122">This command creates a Storage account with Queue and Table Service use account-scoped encryption key, so Queue and Table will use same encryption key with Blob and File service.</span></span> <span data-ttu-id="ee8a0-123">然後取得儲存空間帳戶屬性，並查看佇列和資料表服務的加密 keytype。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-123">Then get the Storage account properties, and view the encryption keytype of Queue and Table Service.</span></span>

## <span data-ttu-id="ee8a0-124">參數</span><span class="sxs-lookup"><span data-stu-id="ee8a0-124">PARAMETERS</span></span>

### <span data-ttu-id="ee8a0-125">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="ee8a0-125">-AccessTier</span></span>
<span data-ttu-id="ee8a0-126">指定此 Cmdlet 所建立之儲存空間帳戶的存取層。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-126">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="ee8a0-127">此參數可接受的值為： [熱] 和 [超酷]。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-127">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="ee8a0-128">如果您為 *Kind* 參數指定 BlobStorage 值，您必須指定 *AccessTier* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-128">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="ee8a0-129">如果您指定此 *類型* 參數的 Storage 值，請勿指定 *AccessTier* 參數。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-129">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="ee8a0-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ee8a0-130">-AsJob</span></span>
<span data-ttu-id="ee8a0-131">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ee8a0-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ee8a0-132">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="ee8a0-132">-AssignIdentity</span></span>
<span data-ttu-id="ee8a0-133">針對此儲存空間帳戶產生並指派新的儲存空間帳戶身分識別，以搭配 Azure KeyVault 等金鑰管理服務使用。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-133">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="ee8a0-134">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="ee8a0-134">-CustomDomainName</span></span>
<span data-ttu-id="ee8a0-135">指定儲存空間帳戶之自訂網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-135">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="ee8a0-136">預設值為 [儲存]。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-136">The default value is Storage.</span></span>

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

### <span data-ttu-id="ee8a0-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee8a0-137">-DefaultProfile</span></span>
<span data-ttu-id="ee8a0-138">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee8a0-139">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="ee8a0-139">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="ee8a0-140">針對儲存空間帳戶啟用 Azure Active Directory 網域服務驗證。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-140">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="ee8a0-141">-EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="ee8a0-141">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="ee8a0-142">指示儲存空間帳戶是否啟用階層命名空間。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-142">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

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

### <span data-ttu-id="ee8a0-143">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="ee8a0-143">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="ee8a0-144">指出儲存空間帳戶是否只啟用 HTTPS 流量。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-144">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="ee8a0-145">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="ee8a0-145">-EnableLargeFileShare</span></span>
<span data-ttu-id="ee8a0-146">指示儲存空間帳戶是否可支援超過5個 TiB 容量的大型檔案共用。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-146">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="ee8a0-147">一旦啟用帳戶，就無法停用此功能。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-147">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="ee8a0-148">目前僅支援 LRS 和 ZRS 複製類型，因此不可能將帳戶轉換成地域冗余帳戶。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-148">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="ee8a0-149">深入瞭解 https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="ee8a0-149">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="ee8a0-150">-EncryptionKeyTypeForQueue</span><span class="sxs-lookup"><span data-stu-id="ee8a0-150">-EncryptionKeyTypeForQueue</span></span>
<span data-ttu-id="ee8a0-151">設定佇列的加密 KeyType。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-151">Set the Encryption KeyType for Queue.</span></span> <span data-ttu-id="ee8a0-152">預設值為 [服務]。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-152">The default value is Service.</span></span>
<span data-ttu-id="ee8a0-153">-帳戶：將使用帳戶範圍的加密金鑰來加密佇列。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-153">-Account: Queue will be encrypted with account-scoped encryption key.</span></span> <span data-ttu-id="ee8a0-154">-服務：將永遠使用 Service-Managed 金鑰來加密佇列。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-154">-Service: Queue will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="ee8a0-155">-EncryptionKeyTypeForTable</span><span class="sxs-lookup"><span data-stu-id="ee8a0-155">-EncryptionKeyTypeForTable</span></span>
<span data-ttu-id="ee8a0-156">設定資料表的加密 KeyType。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-156">Set the Encryption KeyType for Table.</span></span> <span data-ttu-id="ee8a0-157">預設值為 [服務]。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-157">The default value is Service.</span></span>
- <span data-ttu-id="ee8a0-158">帳戶：表格將使用帳戶範圍的加密金鑰加密。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-158">Account: Table will be encrypted with account-scoped encryption key.</span></span> 
- <span data-ttu-id="ee8a0-159">服務：表格將一直使用 Service-Managed 金鑰進行加密。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-159">Service: Table will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="ee8a0-160">類型</span><span class="sxs-lookup"><span data-stu-id="ee8a0-160">-Kind</span></span>
<span data-ttu-id="ee8a0-161">指定這個 Cmdlet 所建立的儲存空間帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-161">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="ee8a0-162">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ee8a0-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ee8a0-163">容量.</span><span class="sxs-lookup"><span data-stu-id="ee8a0-163">Storage.</span></span> <span data-ttu-id="ee8a0-164">支援 Blob、表格、佇列、檔案和磁片儲存的一般用途儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-164">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="ee8a0-165">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="ee8a0-165">StorageV2.</span></span> <span data-ttu-id="ee8a0-166">一般用途版本 2 (GPv2) 儲存空間帳戶（支援 Blob、表格、佇列、檔案和磁片），以及資料分層等高級功能。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-166">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="ee8a0-167">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="ee8a0-167">BlobStorage.</span></span> <span data-ttu-id="ee8a0-168">僅支援以 Blob 儲存的 blob 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-168">Blob Storage account which supports storage of Blobs only.</span></span>
- <span data-ttu-id="ee8a0-169">BlockBlobStorage.</span><span class="sxs-lookup"><span data-stu-id="ee8a0-169">BlockBlobStorage.</span></span> <span data-ttu-id="ee8a0-170">僅支援區塊 Blob 儲存的封鎖 Blob 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-170">Block Blob Storage account which supports storage of Block Blobs only.</span></span>
- <span data-ttu-id="ee8a0-171">FileStorage.</span><span class="sxs-lookup"><span data-stu-id="ee8a0-171">FileStorage.</span></span> <span data-ttu-id="ee8a0-172">僅支援儲存檔案的檔案儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-172">File Storage account which supports storage of Files only.</span></span>
<span data-ttu-id="ee8a0-173">預設值為 StorageV2。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-173">The default value is StorageV2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage, BlockBlobStorage, FileStorage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee8a0-174">-位置</span><span class="sxs-lookup"><span data-stu-id="ee8a0-174">-Location</span></span>
<span data-ttu-id="ee8a0-175">指定要建立的儲存空間帳戶位置。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-175">Specifies the location of the Storage account to create.</span></span>

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

### <span data-ttu-id="ee8a0-176">-名稱</span><span class="sxs-lookup"><span data-stu-id="ee8a0-176">-Name</span></span>
<span data-ttu-id="ee8a0-177">指定要建立的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-177">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="ee8a0-178">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ee8a0-178">-NetworkRuleSet</span></span>
<span data-ttu-id="ee8a0-179">NetworkRuleSet 是用來定義防火牆和虛擬網路的一組設定規則，以及設定網路屬性的值，例如允許繞過規則的服務，以及如何處理不符合任何已定義規則的要求。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-179">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="ee8a0-180">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee8a0-180">-ResourceGroupName</span></span>
<span data-ttu-id="ee8a0-181">指定要新增儲存空間帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-181">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="ee8a0-182">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ee8a0-182">-SkuName</span></span>
<span data-ttu-id="ee8a0-183">指定此 Cmdlet 所建立之儲存空間帳戶的 SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-183">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="ee8a0-184">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ee8a0-184">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ee8a0-185">Standard_LRS]。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-185">Standard_LRS.</span></span> <span data-ttu-id="ee8a0-186">本機冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-186">Locally-redundant storage.</span></span>
- <span data-ttu-id="ee8a0-187">Standard_ZRS]。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-187">Standard_ZRS.</span></span> <span data-ttu-id="ee8a0-188">區域冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-188">Zone-redundant storage.</span></span>
- <span data-ttu-id="ee8a0-189">Standard_GRS]。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-189">Standard_GRS.</span></span> <span data-ttu-id="ee8a0-190">地域冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-190">Geo-redundant storage.</span></span>
- <span data-ttu-id="ee8a0-191">Standard_RAGRS]。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-191">Standard_RAGRS.</span></span> <span data-ttu-id="ee8a0-192">讀取 access 地域冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-192">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="ee8a0-193">Premium_LRS]。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-193">Premium_LRS.</span></span> <span data-ttu-id="ee8a0-194">[特優] 本機-冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-194">Premium locally-redundant storage.</span></span>
- <span data-ttu-id="ee8a0-195">Premium_ZRS]。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-195">Premium_ZRS.</span></span> <span data-ttu-id="ee8a0-196">[特優區域-冗余儲存空間]。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-196">Premium zone-redundant storage.</span></span>
- <span data-ttu-id="ee8a0-197">Standard_GZRS 地域冗余區域-冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-197">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="ee8a0-198">Standard_RAGZRS 讀取 access 地域冗余區域-冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-198">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>

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

### <span data-ttu-id="ee8a0-199">-Tag</span><span class="sxs-lookup"><span data-stu-id="ee8a0-199">-Tag</span></span>
<span data-ttu-id="ee8a0-200">在伺服器上將雜湊表的格式設定為標記的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-200">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="ee8a0-201">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="ee8a0-201">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ee8a0-202">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="ee8a0-202">-UseSubDomain</span></span>
<span data-ttu-id="ee8a0-203">指示是否要啟用間接 CName 驗證。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-203">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="ee8a0-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee8a0-204">CommonParameters</span></span>
<span data-ttu-id="ee8a0-205">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee8a0-206">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-206">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee8a0-207">輸入</span><span class="sxs-lookup"><span data-stu-id="ee8a0-207">INPUTS</span></span>

### <span data-ttu-id="ee8a0-208">System.object</span><span class="sxs-lookup"><span data-stu-id="ee8a0-208">System.String</span></span>

## <span data-ttu-id="ee8a0-209">輸出</span><span class="sxs-lookup"><span data-stu-id="ee8a0-209">OUTPUTS</span></span>

### <span data-ttu-id="ee8a0-210">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="ee8a0-210">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="ee8a0-211">筆記</span><span class="sxs-lookup"><span data-stu-id="ee8a0-211">NOTES</span></span>

## <span data-ttu-id="ee8a0-212">相關連結</span><span class="sxs-lookup"><span data-stu-id="ee8a0-212">RELATED LINKS</span></span>

[<span data-ttu-id="ee8a0-213">AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ee8a0-213">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="ee8a0-214">移除-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ee8a0-214">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="ee8a0-215">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ee8a0-215">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)
