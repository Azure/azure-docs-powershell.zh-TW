---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/new-azurermstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
ms.openlocfilehash: 2ceb395805607809593054880415dccac7e1e28c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450160"
---
# <span data-ttu-id="14375-101">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="14375-101">New-AzureRmStorageAccount</span></span>

## <span data-ttu-id="14375-102">摘要</span><span class="sxs-lookup"><span data-stu-id="14375-102">SYNOPSIS</span></span>
<span data-ttu-id="14375-103">建立儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="14375-103">Creates a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14375-104">句法</span><span class="sxs-lookup"><span data-stu-id="14375-104">SYNTAX</span></span>

```
New-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String>
 [-Location] <String> [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>]
 [-UseSubDomain <Boolean>] [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14375-105">說明</span><span class="sxs-lookup"><span data-stu-id="14375-105">DESCRIPTION</span></span>
<span data-ttu-id="14375-106">**新的-AzureRmStorageAccount** Cmdlet 會建立 Azure 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="14375-106">The **New-AzureRmStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="14375-107">示例</span><span class="sxs-lookup"><span data-stu-id="14375-107">EXAMPLES</span></span>

### <span data-ttu-id="14375-108">範例1：建立儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="14375-108">Example 1: Create a Storage account</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="14375-109">這個命令會為 [資源] 群組名稱 MyResourceGroup 建立儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="14375-109">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="14375-110">範例2：使用 BlobStorage 類型和熱 AccessTier 建立 Blob 儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="14375-110">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="14375-111">這個命令會建立一個 BlobStorage 類型和熱 AccessTier 的 Blob 儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="14375-111">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="14375-112">範例3：使用類型 StorageV2 建立儲存空間帳戶，並產生並指派 Azure KeyVault 的身分識別。</span><span class="sxs-lookup"><span data-stu-id="14375-112">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="14375-113">這個命令會建立 StorageV2 類型的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="14375-113">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="14375-114">它也會產生並指派可用於透過 Azure KeyVault 管理帳戶金鑰的身分識別。</span><span class="sxs-lookup"><span data-stu-id="14375-114">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="14375-115">範例4：從 JSON 建立 NetworkRuleSet 的儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="14375-115">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="14375-116">這個命令會建立具有 JSON NetworkRuleSet 屬性的儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="14375-116">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

## <span data-ttu-id="14375-117">參數</span><span class="sxs-lookup"><span data-stu-id="14375-117">PARAMETERS</span></span>

### <span data-ttu-id="14375-118">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="14375-118">-AccessTier</span></span>
<span data-ttu-id="14375-119">指定此 Cmdlet 所建立之儲存空間帳戶的存取層。</span><span class="sxs-lookup"><span data-stu-id="14375-119">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="14375-120">此參數可接受的值為： [熱] 和 [超酷]。</span><span class="sxs-lookup"><span data-stu-id="14375-120">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="14375-121">如果您為 *Kind* 參數指定 BlobStorage 值，您必須指定 *AccessTier* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="14375-121">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="14375-122">如果您指定此 *類型* 參數的 Storage 值，請勿指定 *AccessTier* 參數。</span><span class="sxs-lookup"><span data-stu-id="14375-122">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="14375-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14375-123">-AsJob</span></span>
<span data-ttu-id="14375-124">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="14375-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="14375-125">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="14375-125">-AssignIdentity</span></span>
<span data-ttu-id="14375-126">針對此儲存空間帳戶產生並指派新的儲存空間帳戶身分識別，以搭配 Azure KeyVault 等金鑰管理服務使用。</span><span class="sxs-lookup"><span data-stu-id="14375-126">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="14375-127">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="14375-127">-CustomDomainName</span></span>
<span data-ttu-id="14375-128">指定儲存空間帳戶之自訂網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="14375-128">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="14375-129">預設值為 [儲存]。</span><span class="sxs-lookup"><span data-stu-id="14375-129">The default value is Storage.</span></span>

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

### <span data-ttu-id="14375-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14375-130">-DefaultProfile</span></span>
<span data-ttu-id="14375-131">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="14375-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14375-132">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="14375-132">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="14375-133">指出儲存空間帳戶是否只啟用 HTTPS 流量。</span><span class="sxs-lookup"><span data-stu-id="14375-133">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14375-134">類型</span><span class="sxs-lookup"><span data-stu-id="14375-134">-Kind</span></span>
<span data-ttu-id="14375-135">指定這個 Cmdlet 所建立的儲存空間帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="14375-135">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="14375-136">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="14375-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="14375-137">容量.</span><span class="sxs-lookup"><span data-stu-id="14375-137">Storage.</span></span> <span data-ttu-id="14375-138">支援 Blob、表格、佇列、檔案和磁片儲存的一般用途儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="14375-138">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="14375-139">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="14375-139">StorageV2.</span></span> <span data-ttu-id="14375-140">一般用途版本 2 (GPv2) 儲存空間帳戶（支援 Blob、表格、佇列、檔案和磁片），以及資料分層等高級功能。</span><span class="sxs-lookup"><span data-stu-id="14375-140">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="14375-141">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="14375-141">BlobStorage.</span></span> <span data-ttu-id="14375-142">僅支援以 Blob 儲存的 blob 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="14375-142">Blob Storage account which supports storage of Blobs only.</span></span>
<span data-ttu-id="14375-143">預設值為 [儲存]。</span><span class="sxs-lookup"><span data-stu-id="14375-143">The default value is Storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14375-144">-位置</span><span class="sxs-lookup"><span data-stu-id="14375-144">-Location</span></span>
<span data-ttu-id="14375-145">指定要建立的儲存空間帳戶位置。</span><span class="sxs-lookup"><span data-stu-id="14375-145">Specifies the location of the Storage account to create.</span></span>

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

### <span data-ttu-id="14375-146">-名稱</span><span class="sxs-lookup"><span data-stu-id="14375-146">-Name</span></span>
<span data-ttu-id="14375-147">指定要建立的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="14375-147">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="14375-148">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="14375-148">-NetworkRuleSet</span></span>
<span data-ttu-id="14375-149">NetworkRuleSet 是用來定義防火牆和虛擬網路的一組設定規則，以及設定網路屬性的值，例如允許繞過規則的服務，以及如何處理不符合任何已定義規則的要求。</span><span class="sxs-lookup"><span data-stu-id="14375-149">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="14375-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14375-150">-ResourceGroupName</span></span>
<span data-ttu-id="14375-151">指定要新增儲存空間帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="14375-151">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="14375-152">-SkuName</span><span class="sxs-lookup"><span data-stu-id="14375-152">-SkuName</span></span>
<span data-ttu-id="14375-153">指定此 Cmdlet 所建立之儲存空間帳戶的 SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="14375-153">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="14375-154">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="14375-154">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="14375-155">Standard_LRS]。</span><span class="sxs-lookup"><span data-stu-id="14375-155">Standard_LRS.</span></span> <span data-ttu-id="14375-156">本機冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="14375-156">Locally-redundant storage.</span></span>
- <span data-ttu-id="14375-157">Standard_ZRS]。</span><span class="sxs-lookup"><span data-stu-id="14375-157">Standard_ZRS.</span></span> <span data-ttu-id="14375-158">區域冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="14375-158">Zone-redundant storage.</span></span>
- <span data-ttu-id="14375-159">Standard_GRS]。</span><span class="sxs-lookup"><span data-stu-id="14375-159">Standard_GRS.</span></span> <span data-ttu-id="14375-160">地域冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="14375-160">Geo-redundant storage.</span></span>
- <span data-ttu-id="14375-161">Standard_RAGRS]。</span><span class="sxs-lookup"><span data-stu-id="14375-161">Standard_RAGRS.</span></span> <span data-ttu-id="14375-162">讀取 access 地域冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="14375-162">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="14375-163">Premium_LRS]。</span><span class="sxs-lookup"><span data-stu-id="14375-163">Premium_LRS.</span></span> <span data-ttu-id="14375-164">[特優] 本機-冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="14375-164">Premium locally-redundant storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14375-165">-Tag</span><span class="sxs-lookup"><span data-stu-id="14375-165">-Tag</span></span>
<span data-ttu-id="14375-166">在伺服器上將雜湊表的格式設定為標記的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="14375-166">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="14375-167">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="14375-167">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="14375-168">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="14375-168">-UseSubDomain</span></span>
<span data-ttu-id="14375-169">指示是否要啟用間接 CName 驗證。</span><span class="sxs-lookup"><span data-stu-id="14375-169">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="14375-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14375-170">CommonParameters</span></span>
<span data-ttu-id="14375-171">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="14375-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14375-172">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="14375-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14375-173">輸入</span><span class="sxs-lookup"><span data-stu-id="14375-173">INPUTS</span></span>

### <span data-ttu-id="14375-174">System.object</span><span class="sxs-lookup"><span data-stu-id="14375-174">System.String</span></span>

### <span data-ttu-id="14375-175">System.object</span><span class="sxs-lookup"><span data-stu-id="14375-175">System.Boolean</span></span>

## <span data-ttu-id="14375-176">輸出</span><span class="sxs-lookup"><span data-stu-id="14375-176">OUTPUTS</span></span>

### <span data-ttu-id="14375-177">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="14375-177">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="14375-178">筆記</span><span class="sxs-lookup"><span data-stu-id="14375-178">NOTES</span></span>

## <span data-ttu-id="14375-179">相關連結</span><span class="sxs-lookup"><span data-stu-id="14375-179">RELATED LINKS</span></span>

[<span data-ttu-id="14375-180">AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="14375-180">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="14375-181">移除-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="14375-181">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)

[<span data-ttu-id="14375-182">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="14375-182">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)
