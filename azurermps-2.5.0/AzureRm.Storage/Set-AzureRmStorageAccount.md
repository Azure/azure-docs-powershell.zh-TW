---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/set-azurermstorageaccount
schema: 2.0.0
ms.openlocfilehash: a6f16c4ef9012f7aaf5216e0cfb24edf65ce9f4d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800630"
---
# <span data-ttu-id="ead37-101">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ead37-101">Set-AzureRmStorageAccount</span></span>

## <span data-ttu-id="ead37-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ead37-102">SYNOPSIS</span></span>
<span data-ttu-id="ead37-103">修改儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="ead37-103">Modifies a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ead37-104">句法</span><span class="sxs-lookup"><span data-stu-id="ead37-104">SYNTAX</span></span>

### <span data-ttu-id="ead37-105">StorageEncryption (預設) </span><span class="sxs-lookup"><span data-stu-id="ead37-105">StorageEncryption (Default)</span></span>
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ead37-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="ead37-106">KeyvaultEncryption</span></span>
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ead37-107">說明</span><span class="sxs-lookup"><span data-stu-id="ead37-107">DESCRIPTION</span></span>
<span data-ttu-id="ead37-108">**AzureRmStorageAccount** Cmdlet 會修改 Azure 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="ead37-108">The **Set-AzureRmStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="ead37-109">您可以使用此 Cmdlet 來修改帳戶類型、更新客戶網域，或在儲存空間帳戶上設定標籤。</span><span class="sxs-lookup"><span data-stu-id="ead37-109">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="ead37-110">示例</span><span class="sxs-lookup"><span data-stu-id="ead37-110">EXAMPLES</span></span>

### <span data-ttu-id="ead37-111">範例1：設定儲存帳戶類型</span><span class="sxs-lookup"><span data-stu-id="ead37-111">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="ead37-112">這個命令會將儲存帳戶類型設定為 [Standard_RAGRS]。</span><span class="sxs-lookup"><span data-stu-id="ead37-112">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="ead37-113">範例2：針對儲存帳戶設定自訂網域</span><span class="sxs-lookup"><span data-stu-id="ead37-113">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="ead37-114">這個命令會針對儲存空間帳戶設定自訂網域。</span><span class="sxs-lookup"><span data-stu-id="ead37-114">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="ead37-115">範例3：設定存取層的值</span><span class="sxs-lookup"><span data-stu-id="ead37-115">Example 3: Set the access tier value</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AccessTier Cool
```

<span data-ttu-id="ead37-116">該命令會將 [存取層] 值設定為 [冷卻]。</span><span class="sxs-lookup"><span data-stu-id="ead37-116">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="ead37-117">範例4：設定自訂網域和標籤</span><span class="sxs-lookup"><span data-stu-id="ead37-117">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="ead37-118">此命令會針對儲存空間帳戶設定自訂網域和標籤。</span><span class="sxs-lookup"><span data-stu-id="ead37-118">The command sets the custom domain and tags for a Storage account.</span></span>

### <span data-ttu-id="ead37-119">範例5：將加密 KeySource 設定為 Keyvault</span><span class="sxs-lookup"><span data-stu-id="ead37-119">Example 5: Set Encryption KeySource to Keyvault</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AssignIdentity
PS C:\>$account = Get-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"

PS C:\>$keyVault = New-AzureRmKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzureKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get

PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="ead37-120">這個命令會將加密 KeySource 設定為新的已建立 Keyvault。</span><span class="sxs-lookup"><span data-stu-id="ead37-120">This command set Encryption KeySource with a new created Keyvault.</span></span>

### <span data-ttu-id="ead37-121">範例6：將加密 KeySource 設定為 "Microsoft. Storage"</span><span class="sxs-lookup"><span data-stu-id="ead37-121">Example 6: Set Encryption KeySource to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -StorageEncryption
```

<span data-ttu-id="ead37-122">這個命令會將加密 KeySource 設定為 "Microsoft. Storage"</span><span class="sxs-lookup"><span data-stu-id="ead37-122">This command set Encryption KeySource to "Microsoft.Storage"</span></span>

### <span data-ttu-id="ead37-123">範例7：使用 JSON 設定儲存空間帳戶的 NetworkRuleSet 屬性</span><span class="sxs-lookup"><span data-stu-id="ead37-123">Example 7: Set NetworkRuleSet property of a Storage account with JSON</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="allow"})
```

<span data-ttu-id="ead37-124">這個命令會使用 JSON 設定儲存空間帳戶的 NetworkRuleSet 屬性</span><span class="sxs-lookup"><span data-stu-id="ead37-124">This command sets NetworkRuleSet property of a Storage account with JSON</span></span>

### <span data-ttu-id="ead37-125">範例8：從儲存空間帳戶取得 NetworkRuleSet 屬性，並將其設定為其他儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="ead37-125">Example 8: Get NetworkRuleSet property from a Storage account, and set it to another Storage account</span></span>
```
PS C:\> $networkRuleSet = (Get-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount").NetworkRuleSet 
PS C:\> Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount2" -NetworkRuleSet $networkRuleSet
```

<span data-ttu-id="ead37-126">這個第一個命令會從儲存空間帳戶取得 NetworkRuleSet 屬性，而第二個命令會將它設為其他儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="ead37-126">This first command gets NetworkRuleSet property from a Storage account, and the second command sets it to another Storage account</span></span> 

### <span data-ttu-id="ead37-127">範例9：將具有類型 "Storage" 或 "BlobStorage" 的儲存空間帳戶升級為 "StorageV2" 類型的儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="ead37-127">Example 9: Upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account</span></span>
```
PS C:\> Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -UpgradeToStorageV2
```

<span data-ttu-id="ead37-128">此命令會將類型為「Storage」或 "BlobStorage" 的儲存空間帳戶升級為 "StorageV2" 類型的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="ead37-128">The command upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account.</span></span>

## <span data-ttu-id="ead37-129">參數</span><span class="sxs-lookup"><span data-stu-id="ead37-129">PARAMETERS</span></span>

### <span data-ttu-id="ead37-130">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="ead37-130">-AccessTier</span></span>
<span data-ttu-id="ead37-131">指定此 Cmdlet 修改之儲存空間帳戶的存取層。</span><span class="sxs-lookup"><span data-stu-id="ead37-131">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="ead37-132">此參數可接受的值為： [熱] 和 [超酷]。</span><span class="sxs-lookup"><span data-stu-id="ead37-132">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="ead37-133">如果您變更了存取層，可能會導致額外的費用。</span><span class="sxs-lookup"><span data-stu-id="ead37-133">If you change the access tier, it may result in additional charges.</span></span> <span data-ttu-id="ead37-134">如需詳細資訊，請參閱 [Azure Blob 儲存體：熱及冷卻存儲層](https://go.microsoft.com/fwlink/?LinkId=786482)。</span><span class="sxs-lookup"><span data-stu-id="ead37-134">For more information, see [Azure Blob Storage: Hot and cool storage tiers](https://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="ead37-135">如果儲存空間帳戶的類型是 StorageV2 或 BlobStorage，您可以指定 *AccessTier* 參數。</span><span class="sxs-lookup"><span data-stu-id="ead37-135">If the Storage account has Kind as StorageV2 or BlobStorage, you can specify the *AccessTier* parameter.</span></span> <span data-ttu-id="ead37-136">如果儲存空間帳戶的類型是 [儲存空間]，請勿指定 *AccessTier* 參數。</span><span class="sxs-lookup"><span data-stu-id="ead37-136">If the Storage account has Kind as Storage, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="ead37-137">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ead37-137">-AsJob</span></span>
<span data-ttu-id="ead37-138">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ead37-138">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ead37-139">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="ead37-139">-AssignIdentity</span></span>
<span data-ttu-id="ead37-140">針對此儲存空間帳戶產生並指派新的儲存空間帳戶身分識別，以搭配 Azure KeyVault 等金鑰管理服務使用。</span><span class="sxs-lookup"><span data-stu-id="ead37-140">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="ead37-141">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="ead37-141">-CustomDomainName</span></span>
<span data-ttu-id="ead37-142">指定自訂網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="ead37-142">Specifies the name of the custom domain.</span></span>

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

### <span data-ttu-id="ead37-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ead37-143">-DefaultProfile</span></span>
<span data-ttu-id="ead37-144">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ead37-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ead37-145">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="ead37-145">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="ead37-146">指出儲存空間帳戶是否只啟用 HTTPS 流量。</span><span class="sxs-lookup"><span data-stu-id="ead37-146">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="ead37-147">-Force</span><span class="sxs-lookup"><span data-stu-id="ead37-147">-Force</span></span>
<span data-ttu-id="ead37-148">強制將變更寫入儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="ead37-148">Forces the change to be written to the Storage account.</span></span>

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

### <span data-ttu-id="ead37-149">-KeyName</span><span class="sxs-lookup"><span data-stu-id="ead37-149">-KeyName</span></span>
<span data-ttu-id="ead37-150">如果使用-KeyvaultEncryption 啟用金鑰保存庫的加密，請使用這個選項指定 Keyname 屬性。</span><span class="sxs-lookup"><span data-stu-id="ead37-150">If using -KeyvaultEncryption to enable encryption with Key Vault, specify the Keyname property with this option.</span></span>

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

### <span data-ttu-id="ead37-151">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="ead37-151">-KeyvaultEncryption</span></span>
<span data-ttu-id="ead37-152">指示在使用儲存服務加密時，是否要針對加密金鑰使用 Microsoft KeyVault。</span><span class="sxs-lookup"><span data-stu-id="ead37-152">Indicates whether or not to use Microsoft KeyVault for the encryption keys when using Storage Service Encryption.</span></span> <span data-ttu-id="ead37-153">如果 KeyName、KeyVersion 和 KeyVaultUri 全都設定，KeySource 將會設定為 Microsoft。 Keyvault 是否已設定此參數。</span><span class="sxs-lookup"><span data-stu-id="ead37-153">If KeyName, KeyVersion, and KeyVaultUri are all set, KeySource will be set to Microsoft.Keyvault whether this parameter is set or not.</span></span> 

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

### <span data-ttu-id="ead37-154">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="ead37-154">-KeyVaultUri</span></span>
<span data-ttu-id="ead37-155">透過指定-KeyvaultEncryption 參數使用金鑰保險存儲加密時，請使用這個選項來指定主要電子倉庫的 URI。</span><span class="sxs-lookup"><span data-stu-id="ead37-155">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Vault.</span></span>

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

### <span data-ttu-id="ead37-156">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="ead37-156">-KeyVersion</span></span>
<span data-ttu-id="ead37-157">透過指定-KeyvaultEncryption 參數使用金鑰 Vault 加密時，請使用這個選項來指定金鑰版本的 URI。</span><span class="sxs-lookup"><span data-stu-id="ead37-157">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Version.</span></span>

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

### <span data-ttu-id="ead37-158">-名稱</span><span class="sxs-lookup"><span data-stu-id="ead37-158">-Name</span></span>
<span data-ttu-id="ead37-159">指定要修改的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="ead37-159">Specifies the name of the Storage account to modify.</span></span>

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

### <span data-ttu-id="ead37-160">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ead37-160">-NetworkRuleSet</span></span>
<span data-ttu-id="ead37-161">NetworkRuleSet 是用來定義防火牆和虛擬網路的一組設定規則，以及設定網路屬性的值，例如允許繞過規則的服務，以及如何處理不符合任何已定義規則的要求。</span><span class="sxs-lookup"><span data-stu-id="ead37-161">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="ead37-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ead37-162">-ResourceGroupName</span></span>
<span data-ttu-id="ead37-163">指定要修改儲存空間帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ead37-163">Specifies the name of the resource group in which to modify the Storage account.</span></span>

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

### <span data-ttu-id="ead37-164">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ead37-164">-SkuName</span></span>
<span data-ttu-id="ead37-165">指定儲存空間帳戶的 SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="ead37-165">Specifies the SKU name of the Storage account.</span></span>
<span data-ttu-id="ead37-166">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ead37-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ead37-167">Standard_LRS 本機冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="ead37-167">Standard_LRS - Locally-redundant storage.</span></span>
- <span data-ttu-id="ead37-168">Standard_ZRS 區域冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="ead37-168">Standard_ZRS - Zone-redundant storage.</span></span>
- <span data-ttu-id="ead37-169">Standard_GRS 地域冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="ead37-169">Standard_GRS - Geo-redundant storage.</span></span>
- <span data-ttu-id="ead37-170">Standard_RAGRS 讀取 access 地域冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="ead37-170">Standard_RAGRS - Read access geo-redundant storage.</span></span>
- <span data-ttu-id="ead37-171">Premium_LRS-Premium 本機冗余儲存空間。</span><span class="sxs-lookup"><span data-stu-id="ead37-171">Premium_LRS - Premium locally-redundant storage.</span></span>
<span data-ttu-id="ead37-172">您無法將 Standard_ZRS 和 Premium_LRS 類型變更為其他帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="ead37-172">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="ead37-173">您無法將其他帳戶類型變更為 [Standard_ZRS] 或 [Premium_LRS]。</span><span class="sxs-lookup"><span data-stu-id="ead37-173">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ead37-174">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="ead37-174">-StorageEncryption</span></span>
<span data-ttu-id="ead37-175">指出是否要將儲存帳戶加密設定為使用 Microsoft 管理的金鑰。</span><span class="sxs-lookup"><span data-stu-id="ead37-175">Indicates whether or not to set the Storage account encryption to use Microsoft-managed keys.</span></span>

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

### <span data-ttu-id="ead37-176">-Tag</span><span class="sxs-lookup"><span data-stu-id="ead37-176">-Tag</span></span>
<span data-ttu-id="ead37-177">在伺服器上將雜湊表的格式設定為標記的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="ead37-177">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="ead37-178">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="ead37-178">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ead37-179">-UpgradeToStorageV2</span><span class="sxs-lookup"><span data-stu-id="ead37-179">-UpgradeToStorageV2</span></span>
<span data-ttu-id="ead37-180">從 Storage 或 BlobStorage 升級儲存帳戶類型至 StorageV2。</span><span class="sxs-lookup"><span data-stu-id="ead37-180">Upgrade Storage account Kind from  Storage or BlobStorage to StorageV2.</span></span>

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

### <span data-ttu-id="ead37-181">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="ead37-181">-UseSubDomain</span></span>
<span data-ttu-id="ead37-182">指示是否要啟用間接 CName 驗證。</span><span class="sxs-lookup"><span data-stu-id="ead37-182">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="ead37-183">-確認</span><span class="sxs-lookup"><span data-stu-id="ead37-183">-Confirm</span></span>
<span data-ttu-id="ead37-184">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ead37-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ead37-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ead37-185">-WhatIf</span></span>
<span data-ttu-id="ead37-186">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ead37-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ead37-187">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ead37-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ead37-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ead37-188">CommonParameters</span></span>
<span data-ttu-id="ead37-189">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ead37-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ead37-190">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ead37-190">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ead37-191">輸入</span><span class="sxs-lookup"><span data-stu-id="ead37-191">INPUTS</span></span>

### <span data-ttu-id="ead37-192">System.object</span><span class="sxs-lookup"><span data-stu-id="ead37-192">System.String</span></span>

### <span data-ttu-id="ead37-193">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ead37-193">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ead37-194">System.object</span><span class="sxs-lookup"><span data-stu-id="ead37-194">System.Boolean</span></span>

## <span data-ttu-id="ead37-195">輸出</span><span class="sxs-lookup"><span data-stu-id="ead37-195">OUTPUTS</span></span>

### <span data-ttu-id="ead37-196">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="ead37-196">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="ead37-197">筆記</span><span class="sxs-lookup"><span data-stu-id="ead37-197">NOTES</span></span>

## <span data-ttu-id="ead37-198">相關連結</span><span class="sxs-lookup"><span data-stu-id="ead37-198">RELATED LINKS</span></span>

[<span data-ttu-id="ead37-199">AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ead37-199">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="ead37-200">新-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ead37-200">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="ead37-201">移除-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ead37-201">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)
