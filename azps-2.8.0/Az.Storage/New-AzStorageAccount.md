---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: c8ac7139c44adc8bd748eef9a6c762a71c3a777f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793067"
---
# <span data-ttu-id="c8b25-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c8b25-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="c8b25-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c8b25-102">SYNOPSIS</span></span>
<span data-ttu-id="c8b25-103">建立儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="c8b25-103">Creates a Storage account.</span></span>

## <span data-ttu-id="c8b25-104">句法</span><span class="sxs-lookup"><span data-stu-id="c8b25-104">SYNTAX</span></span>

```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8b25-105">說明</span><span class="sxs-lookup"><span data-stu-id="c8b25-105">DESCRIPTION</span></span>
<span data-ttu-id="c8b25-106">**新的-AzStorageAccount** Cmdlet 會建立 Azure 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="c8b25-106">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="c8b25-107">示例</span><span class="sxs-lookup"><span data-stu-id="c8b25-107">EXAMPLES</span></span>

### <span data-ttu-id="c8b25-108">範例1：建立儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="c8b25-108">Example 1: Create a Storage account</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="c8b25-109">這個命令會為 [資源] 群組名稱 MyResourceGroup 建立儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="c8b25-109">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="c8b25-110">範例2：使用 BlobStorage 類型和熱 AccessTier 建立 Blob 儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="c8b25-110">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="c8b25-111">這個命令會建立一個 BlobStorage 類型和熱 AccessTier 的 Blob 儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="c8b25-111">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="c8b25-112">範例3：使用類型 StorageV2 建立儲存空間帳戶，並產生並指派 Azure KeyVault 的身分識別。</span><span class="sxs-lookup"><span data-stu-id="c8b25-112">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="c8b25-113">這個命令會建立 StorageV2 類型的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="c8b25-113">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="c8b25-114">它也會產生並指派可用於透過 Azure KeyVault 管理帳戶金鑰的身分識別。</span><span class="sxs-lookup"><span data-stu-id="c8b25-114">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="c8b25-115">範例4：從 JSON 建立 NetworkRuleSet 的儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="c8b25-115">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="c8b25-116">這個命令會建立具有 JSON NetworkRuleSet 屬性的儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="c8b25-116">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="c8b25-117">範例5：建立已啟用階層命名空間的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="c8b25-117">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="c8b25-118">這個命令會建立已啟用階層命名空間的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="c8b25-118">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

### <span data-ttu-id="c8b25-119">範例6：建立擁有 Azure 檔案 AAD DS 驗證的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="c8b25-119">Example 6: Create a Storage account with Azure Files AAD DS Authentication.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true
```

<span data-ttu-id="c8b25-120">這個命令會建立擁有 Azure 檔案 AAD DS 驗證的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="c8b25-120">This command creates a Storage account with Azure Files AAD DS Authentication.</span></span>

## <span data-ttu-id="c8b25-121">參數</span><span class="sxs-lookup"><span data-stu-id="c8b25-121">PARAMETERS</span></span>

### <span data-ttu-id="c8b25-122">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="c8b25-122">-AccessTier</span></span>
<span data-ttu-id="c8b25-123">指定此 Cmdlet 所建立之儲存空間帳戶的存取層。</span><span class="sxs-lookup"><span data-stu-id="c8b25-123">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="c8b25-124">此參數可接受的值為： [熱] 和 [超酷]。</span><span class="sxs-lookup"><span data-stu-id="c8b25-124">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="c8b25-125">如果您為 *Kind* 參數指定 BlobStorage 值，您必須指定 *AccessTier* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="c8b25-125">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="c8b25-126">如果您指定此 *類型* 參數的 Storage 值，請勿指定 *AccessTier* 參數。</span><span class="sxs-lookup"><span data-stu-id="c8b25-126">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="c8b25-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8b25-127">-AsJob</span></span>
<span data-ttu-id="c8b25-128">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c8b25-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c8b25-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c8b25-129">-AssignIdentity</span></span>
<span data-ttu-id="c8b25-130">針對此儲存空間帳戶產生並指派新的儲存空間帳戶身分識別，以搭配 Azure KeyVault 等金鑰管理服務使用。</span><span class="sxs-lookup"><span data-stu-id="c8b25-130">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="c8b25-131">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="c8b25-131">-CustomDomainName</span></span>
<span data-ttu-id="c8b25-132">指定儲存空間帳戶之自訂網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="c8b25-132">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="c8b25-133">預設值為 [儲存]。</span><span class="sxs-lookup"><span data-stu-id="c8b25-133">The default value is Storage.</span></span>

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

### <span data-ttu-id="c8b25-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8b25-134">-DefaultProfile</span></span>
<span data-ttu-id="c8b25-135">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c8b25-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8b25-136">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="c8b25-136">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="c8b25-137">針對儲存空間帳戶啟用 Azure Active Directory 網域服務驗證。</span><span class="sxs-lookup"><span data-stu-id="c8b25-137">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="c8b25-138">-EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="c8b25-138">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="c8b25-139">指示儲存空間帳戶是否啟用階層命名空間。</span><span class="sxs-lookup"><span data-stu-id="c8b25-139">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

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

### <span data-ttu-id="c8b25-140">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="c8b25-140">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="c8b25-141">指出儲存空間帳戶是否只啟用 HTTPS 流量。</span><span class="sxs-lookup"><span data-stu-id="c8b25-141">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="c8b25-142">類型</span><span class="sxs-lookup"><span data-stu-id="c8b25-142">-Kind</span></span>
<span data-ttu-id="c8b25-143">指定這個 Cmdlet 所建立的儲存空間帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="c8b25-143">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="c8b25-144">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c8b25-144">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c8b25-145">容量.</span><span class="sxs-lookup"><span data-stu-id="c8b25-145">Storage.</span></span> <span data-ttu-id="c8b25-146">支援 Blob、表格、佇列、檔案和磁片儲存的一般用途儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="c8b25-146">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="c8b25-147">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="c8b25-147">StorageV2.</span></span> <span data-ttu-id="c8b25-148">一般用途版本 2 (GPv2) 儲存空間帳戶（支援 Blob、表格、佇列、檔案和磁片），以及資料分層等高級功能。</span><span class="sxs-lookup"><span data-stu-id="c8b25-148">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="c8b25-149">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="c8b25-149">BlobStorage.</span></span> <span data-ttu-id="c8b25-150">僅支援以 Blob 儲存的 blob 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="c8b25-150">Blob Storage account which supports storage of Blobs only.</span></span>
- <span data-ttu-id="c8b25-151">BlockBlobStorage.</span><span class="sxs-lookup"><span data-stu-id="c8b25-151">BlockBlobStorage.</span></span> <span data-ttu-id="c8b25-152">僅支援區塊 Blob 儲存的封鎖 Blob 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="c8b25-152">Block Blob Storage account which supports storage of Block Blobs only.</span></span>
- <span data-ttu-id="c8b25-153">FileStorage.</span><span class="sxs-lookup"><span data-stu-id="c8b25-153">FileStorage.</span></span> <span data-ttu-id="c8b25-154">僅支援儲存檔案的檔案儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="c8b25-154">File Storage account which supports storage of Files only.</span></span>
<span data-ttu-id="c8b25-155">預設值為 StorageV2。</span><span class="sxs-lookup"><span data-stu-id="c8b25-155">The default value is StorageV2.</span></span>

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

### <span data-ttu-id="c8b25-156">-位置</span><span class="sxs-lookup"><span data-stu-id="c8b25-156">-Location</span></span>
<span data-ttu-id="c8b25-157">指定要建立的儲存空間帳戶位置。</span><span class="sxs-lookup"><span data-stu-id="c8b25-157">Specifies the location of the Storage account to create.</span></span>

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

### <span data-ttu-id="c8b25-158">-名稱</span><span class="sxs-lookup"><span data-stu-id="c8b25-158">-Name</span></span>
<span data-ttu-id="c8b25-159">指定要建立的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="c8b25-159">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="c8b25-160">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="c8b25-160">-NetworkRuleSet</span></span>
<span data-ttu-id="c8b25-161">NetworkRuleSet 是用來定義防火牆和虛擬網路的一組設定規則，以及設定網路屬性的值，例如允許繞過規則的服務，以及如何處理不符合任何已定義規則的要求。</span><span class="sxs-lookup"><span data-stu-id="c8b25-161">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="c8b25-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8b25-162">-ResourceGroupName</span></span>
<span data-ttu-id="c8b25-163">指定要新增儲存空間帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c8b25-163">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="c8b25-164">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c8b25-164">-SkuName</span></span>
<span data-ttu-id="c8b25-165">指定此 Cmdlet 所建立之儲存空間帳戶的 SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="c8b25-165">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="c8b25-166">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c8b25-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c8b25-167">Standard_LRS]。</span><span class="sxs-lookup"><span data-stu-id="c8b25-167">Standard_LRS.</span></span> <span data-ttu-id="c8b25-168">本機冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="c8b25-168">Locally-redundant storage.</span></span>
- <span data-ttu-id="c8b25-169">Standard_ZRS]。</span><span class="sxs-lookup"><span data-stu-id="c8b25-169">Standard_ZRS.</span></span> <span data-ttu-id="c8b25-170">區域冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="c8b25-170">Zone-redundant storage.</span></span>
- <span data-ttu-id="c8b25-171">Standard_GRS]。</span><span class="sxs-lookup"><span data-stu-id="c8b25-171">Standard_GRS.</span></span> <span data-ttu-id="c8b25-172">地域冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="c8b25-172">Geo-redundant storage.</span></span>
- <span data-ttu-id="c8b25-173">Standard_RAGRS]。</span><span class="sxs-lookup"><span data-stu-id="c8b25-173">Standard_RAGRS.</span></span> <span data-ttu-id="c8b25-174">讀取 access 地域冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="c8b25-174">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="c8b25-175">Premium_LRS]。</span><span class="sxs-lookup"><span data-stu-id="c8b25-175">Premium_LRS.</span></span> <span data-ttu-id="c8b25-176">[特優] 本機-冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="c8b25-176">Premium locally-redundant storage.</span></span>
- <span data-ttu-id="c8b25-177">Premium_ZRS]。</span><span class="sxs-lookup"><span data-stu-id="c8b25-177">Premium_ZRS.</span></span> <span data-ttu-id="c8b25-178">[特優區域-冗余儲存空間]。</span><span class="sxs-lookup"><span data-stu-id="c8b25-178">Premium zone-redundant storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS, Premium_ZRS

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8b25-179">-Tag</span><span class="sxs-lookup"><span data-stu-id="c8b25-179">-Tag</span></span>
<span data-ttu-id="c8b25-180">在伺服器上將雜湊表的格式設定為標記的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="c8b25-180">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="c8b25-181">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="c8b25-181">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c8b25-182">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="c8b25-182">-UseSubDomain</span></span>
<span data-ttu-id="c8b25-183">指示是否要啟用間接 CName 驗證。</span><span class="sxs-lookup"><span data-stu-id="c8b25-183">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="c8b25-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8b25-184">CommonParameters</span></span>
<span data-ttu-id="c8b25-185">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c8b25-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8b25-186">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c8b25-186">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8b25-187">輸入</span><span class="sxs-lookup"><span data-stu-id="c8b25-187">INPUTS</span></span>

### <span data-ttu-id="c8b25-188">System.object</span><span class="sxs-lookup"><span data-stu-id="c8b25-188">System.String</span></span>

## <span data-ttu-id="c8b25-189">輸出</span><span class="sxs-lookup"><span data-stu-id="c8b25-189">OUTPUTS</span></span>

### <span data-ttu-id="c8b25-190">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="c8b25-190">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="c8b25-191">筆記</span><span class="sxs-lookup"><span data-stu-id="c8b25-191">NOTES</span></span>

## <span data-ttu-id="c8b25-192">相關連結</span><span class="sxs-lookup"><span data-stu-id="c8b25-192">RELATED LINKS</span></span>

[<span data-ttu-id="c8b25-193">AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c8b25-193">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="c8b25-194">移除-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c8b25-194">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="c8b25-195">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c8b25-195">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)
