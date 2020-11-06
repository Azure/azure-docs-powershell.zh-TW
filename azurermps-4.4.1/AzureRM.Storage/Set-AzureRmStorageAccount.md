---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Set-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Set-AzureRmStorageAccount.md
ms.openlocfilehash: 5ca65c09746f6bb9a050c14fe10987702465b484
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449475"
---
# <span data-ttu-id="9620c-101">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9620c-101">Set-AzureRmStorageAccount</span></span>

## <span data-ttu-id="9620c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9620c-102">SYNOPSIS</span></span>
<span data-ttu-id="9620c-103">修改儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="9620c-103">Modifies a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9620c-104">句法</span><span class="sxs-lookup"><span data-stu-id="9620c-104">SYNTAX</span></span>

### <span data-ttu-id="9620c-105">StorageEncryption (預設) </span><span class="sxs-lookup"><span data-stu-id="9620c-105">StorageEncryption (Default)</span></span>
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [[-SkuName] <String>]
 [[-AccessTier] <String>] [[-CustomDomainName] <String>] [[-UseSubDomain] <Boolean>]
 [[-EnableEncryptionService] <EncryptionSupportServiceEnum>]
 [[-DisableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9620c-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="9620c-106">KeyvaultEncryption</span></span>
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [[-SkuName] <String>]
 [[-AccessTier] <String>] [[-CustomDomainName] <String>] [[-UseSubDomain] <Boolean>]
 [[-EnableEncryptionService] <EncryptionSupportServiceEnum>]
 [[-DisableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9620c-107">說明</span><span class="sxs-lookup"><span data-stu-id="9620c-107">DESCRIPTION</span></span>
<span data-ttu-id="9620c-108">**AzureRmStorageAccount** Cmdlet 會修改 Azure 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="9620c-108">The **Set-AzureRmStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="9620c-109">您可以使用此 Cmdlet 來修改帳戶類型、更新客戶網域，或在儲存空間帳戶上設定標籤。</span><span class="sxs-lookup"><span data-stu-id="9620c-109">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="9620c-110">示例</span><span class="sxs-lookup"><span data-stu-id="9620c-110">EXAMPLES</span></span>

### <span data-ttu-id="9620c-111">範例1：設定儲存帳戶類型</span><span class="sxs-lookup"><span data-stu-id="9620c-111">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="9620c-112">這個命令會將儲存帳戶類型設定為 [Standard_RAGRS]。</span><span class="sxs-lookup"><span data-stu-id="9620c-112">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="9620c-113">範例2：針對儲存帳戶設定自訂網域</span><span class="sxs-lookup"><span data-stu-id="9620c-113">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="9620c-114">這個命令會針對儲存空間帳戶設定自訂網域。</span><span class="sxs-lookup"><span data-stu-id="9620c-114">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="9620c-115">範例3：在 Blob 和檔案服務上啟用加密</span><span class="sxs-lookup"><span data-stu-id="9620c-115">Example 3: Enable encryption on Blob and File Services</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -EnableEncryptionService "Blob,File"
```

<span data-ttu-id="9620c-116">這個命令會在 Blob 和檔案上啟用儲存空間帳戶的儲存服務加密。</span><span class="sxs-lookup"><span data-stu-id="9620c-116">This command enables Storage Service encryption on Blob and File for a Storage account.</span></span>

### <span data-ttu-id="9620c-117">範例4：設定存取層的值</span><span class="sxs-lookup"><span data-stu-id="9620c-117">Example 4: Set the access tier value</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -AccessTier Cool
```

<span data-ttu-id="9620c-118">該命令會將 [存取層] 值設定為 [冷卻]。</span><span class="sxs-lookup"><span data-stu-id="9620c-118">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="9620c-119">範例4：設定自訂網域和標籤</span><span class="sxs-lookup"><span data-stu-id="9620c-119">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="9620c-120">該命令會將 [存取層] 值設定為 [冷卻]。</span><span class="sxs-lookup"><span data-stu-id="9620c-120">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="9620c-121">範例5：使用 Keyvault 在 Blob 服務上啟用加密</span><span class="sxs-lookup"><span data-stu-id="9620c-121">Example 5: Enable encryption on Blob Services with Keyvault</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -AssignIdentity
PS C:\>$account = Get-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount"

PS C:\>$keyVault = New-AzureRmKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzureKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey

PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -EnableEncryptionService "Blob" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="9620c-122">這個命令會在 Blob 上以新建立的 Keyvault 啟用儲存服務加密。</span><span class="sxs-lookup"><span data-stu-id="9620c-122">This command enables Storage Service encryption on Blob with a new created Keyvault.</span></span>

### <span data-ttu-id="9620c-123">範例6：停用 KeySource 設定為 "Microsoft. Storage" 的檔案服務加密</span><span class="sxs-lookup"><span data-stu-id="9620c-123">Example 6: Disable encryption on File Services with KeySource set to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -DisableEncryptionService File  -StorageEncryption
```

<span data-ttu-id="9620c-124">這個命令會在 KeySource 設定為 "Microsoft. Storage" 的檔案服務上停用加密</span><span class="sxs-lookup"><span data-stu-id="9620c-124">This command disables encryption on File Services with KeySource set to "Microsoft.Storage"</span></span>

## <span data-ttu-id="9620c-125">參數</span><span class="sxs-lookup"><span data-stu-id="9620c-125">PARAMETERS</span></span>

### <span data-ttu-id="9620c-126">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="9620c-126">-AccessTier</span></span>
<span data-ttu-id="9620c-127">指定此 Cmdlet 修改之儲存空間帳戶的存取層。</span><span class="sxs-lookup"><span data-stu-id="9620c-127">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="9620c-128">此參數可接受的值為： [熱] 和 [超酷]。</span><span class="sxs-lookup"><span data-stu-id="9620c-128">The acceptable values for this parameter are: Hot and Cool.</span></span>

<span data-ttu-id="9620c-129">如果您變更了存取層，可能會導致額外的費用。</span><span class="sxs-lookup"><span data-stu-id="9620c-129">If you change the access tier, it may result in additional charges.</span></span>
<span data-ttu-id="9620c-130">如需詳細資訊，請參閱 Azure Blob 儲存體：熱及冷卻儲存層 https://go.microsoft.com/fwlink/?LinkId=786482 (https://go.microsoft.com/fwlink/?LinkId=786482) 。</span><span class="sxs-lookup"><span data-stu-id="9620c-130">For more information, see Azure Blob Storage: Hot and cool storage tiershttps://go.microsoft.com/fwlink/?LinkId=786482 (https://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="9620c-131">如果儲存空間帳戶的類型是 [儲存空間]，請勿指定此參數。</span><span class="sxs-lookup"><span data-stu-id="9620c-131">If the kind of Storage account is Storage, do not specify this parameter.</span></span>

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

### <span data-ttu-id="9620c-132">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="9620c-132">-AssignIdentity</span></span>
<span data-ttu-id="9620c-133">針對此儲存空間帳戶產生並指派新的儲存空間帳戶身分識別，以搭配 Azure KeyVault 等金鑰管理服務使用。</span><span class="sxs-lookup"><span data-stu-id="9620c-133">Generate and assign a new Storage Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="9620c-134">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="9620c-134">-CustomDomainName</span></span>
<span data-ttu-id="9620c-135">指定自訂網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="9620c-135">Specifies the name of the custom domain.</span></span>

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

### <span data-ttu-id="9620c-136">-DisableEncryptionService</span><span class="sxs-lookup"><span data-stu-id="9620c-136">-DisableEncryptionService</span></span>
<span data-ttu-id="9620c-137">指示此 Cmdlet 是否停用儲存服務上的儲存服務加密。</span><span class="sxs-lookup"><span data-stu-id="9620c-137">Indicates whether this cmdlet disables Storage Service encryption on the Storage Service.</span></span>
<span data-ttu-id="9620c-138">支援 azure Blob 和 Azure 檔案服務。</span><span class="sxs-lookup"><span data-stu-id="9620c-138">Azure Blob and Azure File Services are supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Storage.StorageAccountBaseCmdlet+EncryptionSupportServiceEnum]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9620c-139">-EnableEncryptionService</span><span class="sxs-lookup"><span data-stu-id="9620c-139">-EnableEncryptionService</span></span>
<span data-ttu-id="9620c-140">指示此 Cmdlet 是否在儲存服務上啟用儲存服務加密。</span><span class="sxs-lookup"><span data-stu-id="9620c-140">Indicates whether this cmdlet enables Storage Service encryption on the Storage Service.</span></span>
<span data-ttu-id="9620c-141">支援 azure Blob 和 Azure 檔案服務。</span><span class="sxs-lookup"><span data-stu-id="9620c-141">Azure Blob and Azure File Services are supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Storage.StorageAccountBaseCmdlet+EncryptionSupportServiceEnum]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9620c-142">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="9620c-142">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="9620c-143">指出儲存空間帳戶是否只啟用 HTTPs 流量。</span><span class="sxs-lookup"><span data-stu-id="9620c-143">Indicates whether or not the Storage Account only enable https traffic.</span></span>

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

### <span data-ttu-id="9620c-144">-Force</span><span class="sxs-lookup"><span data-stu-id="9620c-144">-Force</span></span>
<span data-ttu-id="9620c-145">如果您變更了存取層，可能會導致額外的費用。</span><span class="sxs-lookup"><span data-stu-id="9620c-145">If you change the access tier, it may result in additional charges.</span></span>
<span data-ttu-id="9620c-146">如需詳細資訊，請參閱 Azure Blob 儲存體：熱及冷卻儲存層 https://go.microsoft.com/fwlink/?LinkId=786482 (https://go.microsoft.com/fwlink/?LinkId=786482) 。</span><span class="sxs-lookup"><span data-stu-id="9620c-146">For more information, see Azure Blob Storage: Hot and cool storage tiershttps://go.microsoft.com/fwlink/?LinkId=786482 (https://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="9620c-147">如果儲存空間帳戶的類型是 [儲存空間]，請勿指定此參數。</span><span class="sxs-lookup"><span data-stu-id="9620c-147">If the kind of Storage account is Storage, do not specify this parameter.</span></span>

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

### <span data-ttu-id="9620c-148">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="9620c-148">-InformationAction</span></span>
<span data-ttu-id="9620c-149">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="9620c-149">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9620c-150">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="9620c-150">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9620c-151">持續</span><span class="sxs-lookup"><span data-stu-id="9620c-151">Continue</span></span>
- <span data-ttu-id="9620c-152">理會</span><span class="sxs-lookup"><span data-stu-id="9620c-152">Ignore</span></span>
- <span data-ttu-id="9620c-153">看</span><span class="sxs-lookup"><span data-stu-id="9620c-153">Inquire</span></span>
- <span data-ttu-id="9620c-154">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9620c-154">SilentlyContinue</span></span>
- <span data-ttu-id="9620c-155">停止</span><span class="sxs-lookup"><span data-stu-id="9620c-155">Stop</span></span>
- <span data-ttu-id="9620c-156">封存</span><span class="sxs-lookup"><span data-stu-id="9620c-156">Suspend</span></span>

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

### <span data-ttu-id="9620c-157">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9620c-157">-InformationVariable</span></span>
<span data-ttu-id="9620c-158">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="9620c-158">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9620c-159">-KeyName</span><span class="sxs-lookup"><span data-stu-id="9620c-159">-KeyName</span></span>
<span data-ttu-id="9620c-160">儲存帳戶加密 keySource KeyVault KeyName</span><span class="sxs-lookup"><span data-stu-id="9620c-160">Storage Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="9620c-161">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="9620c-161">-KeyvaultEncryption</span></span>
<span data-ttu-id="9620c-162">是否將儲存帳戶加密 KeySource 設定為 Keyvault。</span><span class="sxs-lookup"><span data-stu-id="9620c-162">Whether to set Storage Account Encryption KeySource to Microsoft.Keyvault or not.</span></span> <span data-ttu-id="9620c-163">如果您指定 KeyName、KeyVersion 和 KeyvaultUri，儲存帳戶加密 keySource 也會設定為 Microsoft。 Keyvault 天氣此參數已設定。</span><span class="sxs-lookup"><span data-stu-id="9620c-163">If you specify KeyName, KeyVersion and KeyvaultUri, Storage Account encryption keySource will also be set to Microsoft.Keyvault weather this parameter is set or not.</span></span>
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

### <span data-ttu-id="9620c-164">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="9620c-164">-KeyVaultUri</span></span>
<span data-ttu-id="9620c-165">儲存帳戶加密 keySource KeyVault KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="9620c-165">Storage Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="9620c-166">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="9620c-166">-KeyVersion</span></span>
<span data-ttu-id="9620c-167">儲存帳戶加密 keySource KeyVault KeyVersion</span><span class="sxs-lookup"><span data-stu-id="9620c-167">Storage Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="9620c-168">-名稱</span><span class="sxs-lookup"><span data-stu-id="9620c-168">-Name</span></span>
<span data-ttu-id="9620c-169">指定要修改的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="9620c-169">Specifies the name of the Storage account to Modify.</span></span>

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

### <span data-ttu-id="9620c-170">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="9620c-170">-NetworkRuleSet</span></span>
<span data-ttu-id="9620c-171">儲存空間帳戶 NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="9620c-171">Storage Account NetworkRuleSet</span></span>

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

### <span data-ttu-id="9620c-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9620c-172">-ResourceGroupName</span></span>
<span data-ttu-id="9620c-173">指定要修改儲存空間帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9620c-173">Specifies the name of the resource group in which to modify the Storage account.</span></span>

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

### <span data-ttu-id="9620c-174">-SkuName</span><span class="sxs-lookup"><span data-stu-id="9620c-174">-SkuName</span></span>
<span data-ttu-id="9620c-175">指定儲存空間帳戶的 SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="9620c-175">Specifies the SKU name of the storage account.</span></span>
<span data-ttu-id="9620c-176">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="9620c-176">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9620c-177">Standard_LRS]。</span><span class="sxs-lookup"><span data-stu-id="9620c-177">Standard_LRS.</span></span>
<span data-ttu-id="9620c-178">本機冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="9620c-178">Locally-redundant storage.</span></span> 
- <span data-ttu-id="9620c-179">Standard_ZRS]。</span><span class="sxs-lookup"><span data-stu-id="9620c-179">Standard_ZRS.</span></span>
<span data-ttu-id="9620c-180">區域冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="9620c-180">Zone-redundant storage.</span></span>
- <span data-ttu-id="9620c-181">Standard_GRS]。</span><span class="sxs-lookup"><span data-stu-id="9620c-181">Standard_GRS.</span></span>
<span data-ttu-id="9620c-182">地域冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="9620c-182">Geo-redundant storage.</span></span> 
- <span data-ttu-id="9620c-183">Standard_RAGRS]。</span><span class="sxs-lookup"><span data-stu-id="9620c-183">Standard_RAGRS.</span></span>
<span data-ttu-id="9620c-184">讀取 access 地域冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="9620c-184">Read access geo-redundant storage.</span></span> 
- <span data-ttu-id="9620c-185">Premium_LRS]。</span><span class="sxs-lookup"><span data-stu-id="9620c-185">Premium_LRS.</span></span>
<span data-ttu-id="9620c-186">[特優] 本機-冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="9620c-186">Premium locally-redundant storage.</span></span>

<span data-ttu-id="9620c-187">您無法將 Standard_ZRS 和 Premium_LRS 類型變更為其他帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="9620c-187">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="9620c-188">您無法將其他帳戶類型變更為 [Standard_ZRS] 或 [Premium_LRS]。</span><span class="sxs-lookup"><span data-stu-id="9620c-188">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9620c-189">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="9620c-189">-StorageEncryption</span></span>
<span data-ttu-id="9620c-190">是否將儲存帳戶加密 KeySource 到 Microsoft. 儲存。</span><span class="sxs-lookup"><span data-stu-id="9620c-190">Whether to set Storage Account Encryption KeySource to Microsoft.Storage or not.</span></span>

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

### <span data-ttu-id="9620c-191">-Tag</span><span class="sxs-lookup"><span data-stu-id="9620c-191">-Tag</span></span>
<span data-ttu-id="9620c-192">如果您為 New-AzureRmStorageAccount Cmdlet 的 *Kind* 參數指定了 BlobStorage 值，您必須指定 *AccessTier* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="9620c-192">If you specify a value of BlobStorage for the *Kind* parameter of the New-AzureRmStorageAccount cmdlet, you must specify a value for the *AccessTier* parameter.</span></span>

<span data-ttu-id="9620c-193">如果您指定此 *類型* 參數的 Storage 值，請勿指定 *AccessTier* 參數。</span><span class="sxs-lookup"><span data-stu-id="9620c-193">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9620c-194">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="9620c-194">-UseSubDomain</span></span>
<span data-ttu-id="9620c-195">指示是否要啟用間接 CName 驗證。</span><span class="sxs-lookup"><span data-stu-id="9620c-195">Indicates whether to enable indirect CName validation.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9620c-196">-確認</span><span class="sxs-lookup"><span data-stu-id="9620c-196">-Confirm</span></span>
<span data-ttu-id="9620c-197">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9620c-197">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9620c-198">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9620c-198">-WhatIf</span></span>
<span data-ttu-id="9620c-199">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9620c-199">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9620c-200">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9620c-200">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9620c-201">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9620c-201">-DefaultProfile</span></span>
<span data-ttu-id="9620c-202">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9620c-202">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9620c-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9620c-203">CommonParameters</span></span>
<span data-ttu-id="9620c-204">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9620c-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9620c-205">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9620c-205">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9620c-206">輸入</span><span class="sxs-lookup"><span data-stu-id="9620c-206">INPUTS</span></span>

## <span data-ttu-id="9620c-207">輸出</span><span class="sxs-lookup"><span data-stu-id="9620c-207">OUTPUTS</span></span>

## <span data-ttu-id="9620c-208">筆記</span><span class="sxs-lookup"><span data-stu-id="9620c-208">NOTES</span></span>

## <span data-ttu-id="9620c-209">相關連結</span><span class="sxs-lookup"><span data-stu-id="9620c-209">RELATED LINKS</span></span>

[<span data-ttu-id="9620c-210">AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9620c-210">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="9620c-211">新-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9620c-211">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="9620c-212">移除-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9620c-212">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)

