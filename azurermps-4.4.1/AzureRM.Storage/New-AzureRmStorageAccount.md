---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
ms.openlocfilehash: 50384630658f7626ee02ca1dee223e82bf122ef1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626470"
---
# <span data-ttu-id="2e371-101">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2e371-101">New-AzureRmStorageAccount</span></span>

## <span data-ttu-id="2e371-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2e371-102">SYNOPSIS</span></span>
<span data-ttu-id="2e371-103">建立儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="2e371-103">Creates a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e371-104">句法</span><span class="sxs-lookup"><span data-stu-id="2e371-104">SYNTAX</span></span>

```
New-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String>
 [-Location] <String> [[-Kind] <String>] [[-AccessTier] <String>] [[-CustomDomainName] <String>]
 [[-UseSubDomain] <Boolean>] [[-EnableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2e371-105">說明</span><span class="sxs-lookup"><span data-stu-id="2e371-105">DESCRIPTION</span></span>
<span data-ttu-id="2e371-106">**新的-AzureRmStorageAccount** Cmdlet 會建立 Azure 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="2e371-106">The **New-AzureRmStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="2e371-107">示例</span><span class="sxs-lookup"><span data-stu-id="2e371-107">EXAMPLES</span></span>

### <span data-ttu-id="2e371-108">範例1：建立儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="2e371-108">Example 1: Create a Storage Account</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "US West" -SkuName "Standard_GRS"
```

<span data-ttu-id="2e371-109">這個命令會為 [資源] 群組名稱 MyResourceGroup 建立儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="2e371-109">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="2e371-110">範例2：建立使用儲存服務加密的 Blob 儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="2e371-110">Example 2: Create a Blob Storage account that uses Storage Service Encryption</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "US West" -SkuName "Standard_GRS" -EnableEncryptionService Blob -Kind "BlobStorage" -AccessTier Hot
```

<span data-ttu-id="2e371-111">這個命令會建立使用熱存取類型的 Blob 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="2e371-111">This command creates a Blob Storage account that uses the hot access type.</span></span>
<span data-ttu-id="2e371-112">帳戶已啟用 Blob 服務的儲存服務加密。</span><span class="sxs-lookup"><span data-stu-id="2e371-112">The account has enabled Storage Service encryption on Blob Service.</span></span>

### <span data-ttu-id="2e371-113">範例3：建立可在 Blob 和檔案服務上啟用儲存服務加密的儲存空間帳戶，並為 Azure KeyVault 產生並指派身分識別。</span><span class="sxs-lookup"><span data-stu-id="2e371-113">Example 3: Create a Storage Account that Enables Storage Service Encryption on Blob and File Services, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "US West" -SkuName "Standard_GRS" -EnableEncryptionService "Blob,File" -AssignIdentity
```

<span data-ttu-id="2e371-114">這個命令會建立可在 Blob 和檔案服務上啟用儲存服務加密的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="2e371-114">This command creates a Storage account that enabled Storage Service encryption on Blob and File Services.</span></span>  <span data-ttu-id="2e371-115">它也會產生並指派可用於透過 Azure KeyVault 管理帳戶金鑰的身分識別。</span><span class="sxs-lookup"><span data-stu-id="2e371-115">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

## <span data-ttu-id="2e371-116">參數</span><span class="sxs-lookup"><span data-stu-id="2e371-116">PARAMETERS</span></span>

### <span data-ttu-id="2e371-117">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="2e371-117">-AccessTier</span></span>
<span data-ttu-id="2e371-118">指定此 Cmdlet 所建立之儲存空間帳戶的存取層。</span><span class="sxs-lookup"><span data-stu-id="2e371-118">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="2e371-119">此參數可接受的值為： [熱] 和 [超酷]。</span><span class="sxs-lookup"><span data-stu-id="2e371-119">The acceptable values for this parameter are: Hot and Cool.</span></span>

<span data-ttu-id="2e371-120">如果您為 *Kind* 參數指定 BlobStorage 值，您必須指定 *AccessTier* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="2e371-120">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span>

<span data-ttu-id="2e371-121">如果您指定此 *類型* 參數的 Storage 值，請勿指定 *AccessTier* 參數。</span><span class="sxs-lookup"><span data-stu-id="2e371-121">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e371-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="2e371-122">-AssignIdentity</span></span>
<span data-ttu-id="2e371-123">針對此儲存空間帳戶產生並指派新的儲存空間帳戶身分識別，以搭配 Azure KeyVault 等金鑰管理服務使用。</span><span class="sxs-lookup"><span data-stu-id="2e371-123">Generate and assign a new Storage Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="2e371-124">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="2e371-124">-CustomDomainName</span></span>
<span data-ttu-id="2e371-125">指定儲存空間帳戶之自訂網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="2e371-125">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="2e371-126">預設值為 [儲存]。</span><span class="sxs-lookup"><span data-stu-id="2e371-126">The default value is Storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e371-127">-EnableEncryptionService</span><span class="sxs-lookup"><span data-stu-id="2e371-127">-EnableEncryptionService</span></span>
<span data-ttu-id="2e371-128">指示此 Cmdlet 是否在儲存服務上啟用儲存服務加密。</span><span class="sxs-lookup"><span data-stu-id="2e371-128">Indicates whether this cmdlet enables Storage Service encryption on the Storage Service.</span></span>
<span data-ttu-id="2e371-129">支援 azure Blob 和 Azure 檔案服務。</span><span class="sxs-lookup"><span data-stu-id="2e371-129">Azure Blob and Azure File Services are supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Storage.StorageAccountBaseCmdlet+EncryptionSupportServiceEnum]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e371-130">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="2e371-130">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="2e371-131">指出儲存空間帳戶是否只啟用 HTTPs 流量。</span><span class="sxs-lookup"><span data-stu-id="2e371-131">Indicates whether or not the Storage Account only enable https traffic.</span></span>

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

### <span data-ttu-id="2e371-132">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2e371-132">-InformationAction</span></span>
<span data-ttu-id="2e371-133">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="2e371-133">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2e371-134">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="2e371-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2e371-135">持續</span><span class="sxs-lookup"><span data-stu-id="2e371-135">Continue</span></span>
- <span data-ttu-id="2e371-136">理會</span><span class="sxs-lookup"><span data-stu-id="2e371-136">Ignore</span></span>
- <span data-ttu-id="2e371-137">看</span><span class="sxs-lookup"><span data-stu-id="2e371-137">Inquire</span></span>
- <span data-ttu-id="2e371-138">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2e371-138">SilentlyContinue</span></span>
- <span data-ttu-id="2e371-139">停止</span><span class="sxs-lookup"><span data-stu-id="2e371-139">Stop</span></span>
- <span data-ttu-id="2e371-140">封存</span><span class="sxs-lookup"><span data-stu-id="2e371-140">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e371-141">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2e371-141">-InformationVariable</span></span>
<span data-ttu-id="2e371-142">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="2e371-142">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e371-143">類型</span><span class="sxs-lookup"><span data-stu-id="2e371-143">-Kind</span></span>
<span data-ttu-id="2e371-144">指定這個 Cmdlet 所建立的儲存空間帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="2e371-144">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="2e371-145">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="2e371-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2e371-146">容量.</span><span class="sxs-lookup"><span data-stu-id="2e371-146">Storage.</span></span>
<span data-ttu-id="2e371-147">支援 Blob、表格、佇列、檔案和磁片儲存的一般用途儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="2e371-147">General purpose storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
 
- <span data-ttu-id="2e371-148">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="2e371-148">BlobStorage.</span></span>
<span data-ttu-id="2e371-149">僅支援以 Blob 儲存的 blob 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="2e371-149">Blob storage account which supports storage of Blobs only.</span></span>
 

<span data-ttu-id="2e371-150">預設值為 [儲存]。</span><span class="sxs-lookup"><span data-stu-id="2e371-150">The default value is Storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e371-151">-位置</span><span class="sxs-lookup"><span data-stu-id="2e371-151">-Location</span></span>
<span data-ttu-id="2e371-152">指定要建立的儲存空間帳戶位置。</span><span class="sxs-lookup"><span data-stu-id="2e371-152">Specifies the location of the Storage account to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e371-153">-名稱</span><span class="sxs-lookup"><span data-stu-id="2e371-153">-Name</span></span>
<span data-ttu-id="2e371-154">指定要建立的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="2e371-154">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="2e371-155">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="2e371-155">-NetworkRuleSet</span></span>
<span data-ttu-id="2e371-156">儲存空間帳戶 NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="2e371-156">Storage Account NetworkRuleSet</span></span>

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

### <span data-ttu-id="2e371-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e371-157">-ResourceGroupName</span></span>
<span data-ttu-id="2e371-158">指定要新增儲存空間帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2e371-158">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="2e371-159">-SkuName</span><span class="sxs-lookup"><span data-stu-id="2e371-159">-SkuName</span></span>
<span data-ttu-id="2e371-160">指定此 Cmdlet 所建立之儲存空間帳戶的 SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="2e371-160">Specifies the SKU name of the storage account that this cmdlet creates.</span></span>
<span data-ttu-id="2e371-161">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="2e371-161">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2e371-162">Standard_LRS]。</span><span class="sxs-lookup"><span data-stu-id="2e371-162">Standard_LRS.</span></span>
<span data-ttu-id="2e371-163">本機冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="2e371-163">Locally-redundant storage.</span></span> 
- <span data-ttu-id="2e371-164">Standard_ZRS]。</span><span class="sxs-lookup"><span data-stu-id="2e371-164">Standard_ZRS.</span></span>
<span data-ttu-id="2e371-165">區域冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="2e371-165">Zone-redundant storage.</span></span>
- <span data-ttu-id="2e371-166">Standard_GRS]。</span><span class="sxs-lookup"><span data-stu-id="2e371-166">Standard_GRS.</span></span>
<span data-ttu-id="2e371-167">地域冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="2e371-167">Geo-redundant storage.</span></span> 
- <span data-ttu-id="2e371-168">Standard_RAGRS]。</span><span class="sxs-lookup"><span data-stu-id="2e371-168">Standard_RAGRS.</span></span>
<span data-ttu-id="2e371-169">讀取 access 地域冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="2e371-169">Read access geo-redundant storage.</span></span> 
- <span data-ttu-id="2e371-170">Premium_LRS]。</span><span class="sxs-lookup"><span data-stu-id="2e371-170">Premium_LRS.</span></span>
<span data-ttu-id="2e371-171">[特優] 本機-冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="2e371-171">Premium locally-redundant storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e371-172">-Tag</span><span class="sxs-lookup"><span data-stu-id="2e371-172">-Tag</span></span>
<span data-ttu-id="2e371-173">如果您為 *Kind* 參數指定 BlobStorage 值，您必須指定 *AccessTier* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="2e371-173">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span>

<span data-ttu-id="2e371-174">如果您指定此 *類型* 參數的 Storage 值，請勿指定 *AccessTier* 參數。</span><span class="sxs-lookup"><span data-stu-id="2e371-174">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e371-175">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="2e371-175">-UseSubDomain</span></span>
<span data-ttu-id="2e371-176">指示是否要啟用間接 CName 驗證。</span><span class="sxs-lookup"><span data-stu-id="2e371-176">Indicates whether to enable indirect CName validation.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e371-177">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e371-177">-DefaultProfile</span></span>
<span data-ttu-id="2e371-178">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2e371-178">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e371-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e371-179">CommonParameters</span></span>
<span data-ttu-id="2e371-180">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2e371-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e371-181">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2e371-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e371-182">輸入</span><span class="sxs-lookup"><span data-stu-id="2e371-182">INPUTS</span></span>

## <span data-ttu-id="2e371-183">輸出</span><span class="sxs-lookup"><span data-stu-id="2e371-183">OUTPUTS</span></span>

## <span data-ttu-id="2e371-184">筆記</span><span class="sxs-lookup"><span data-stu-id="2e371-184">NOTES</span></span>

## <span data-ttu-id="2e371-185">相關連結</span><span class="sxs-lookup"><span data-stu-id="2e371-185">RELATED LINKS</span></span>

[<span data-ttu-id="2e371-186">AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2e371-186">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="2e371-187">移除-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2e371-187">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)

[<span data-ttu-id="2e371-188">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2e371-188">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


