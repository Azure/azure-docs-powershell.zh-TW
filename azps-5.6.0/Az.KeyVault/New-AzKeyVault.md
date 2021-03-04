---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/powershell/module/az.keyvault/new-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
ms.openlocfilehash: 6af82533540bd93b90847c51b9aaf0bd603dc727
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914798"
---
# <span data-ttu-id="11c75-101">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="11c75-101">New-AzKeyVault</span></span>

## <span data-ttu-id="11c75-102">簡介</span><span class="sxs-lookup"><span data-stu-id="11c75-102">SYNOPSIS</span></span>
<span data-ttu-id="11c75-103">建立金鑰庫。</span><span class="sxs-lookup"><span data-stu-id="11c75-103">Creates a key vault.</span></span>

## <span data-ttu-id="11c75-104">語法</span><span class="sxs-lookup"><span data-stu-id="11c75-104">SYNTAX</span></span>

```
New-AzKeyVault [-Name] <String> [-ResourceGroupName] <String> [-Location] <String> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnablePurgeProtection]
 [-EnableRbacAuthorization] [-SoftDeleteRetentionInDays <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-NetworkRuleSet <PSKeyVaultNetworkRuleSet>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="11c75-105">描述</span><span class="sxs-lookup"><span data-stu-id="11c75-105">DESCRIPTION</span></span>
<span data-ttu-id="11c75-106">**New-AzKeyVault** Cmdlet 會建立指定資源群組中的金鑰庫。</span><span class="sxs-lookup"><span data-stu-id="11c75-106">The **New-AzKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="11c75-107">此 Cmdlet 也會將許可權授予目前登入的使用者，以新增、移除或列出金鑰庫中的金鑰和機密。</span><span class="sxs-lookup"><span data-stu-id="11c75-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>
<span data-ttu-id="11c75-108">注意：如果您看到錯誤：當您嘗試建立新金鑰庫時，訂閱未註冊使用命名空間 **'Microsoft.KeyVault'，** 請執行 **Register-AzResourceProvider -ProviderNamespace "Microsoft.KeyVault"，** 然後重新執行 **New-AzKeyVault** 命令。</span><span class="sxs-lookup"><span data-stu-id="11c75-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzKeyVault** command.</span></span> <span data-ttu-id="11c75-109">詳細資訊請參閱 Register-AzResourceProvider。</span><span class="sxs-lookup"><span data-stu-id="11c75-109">For more information, see Register-AzResourceProvider.</span></span>

## <span data-ttu-id="11c75-110">例子</span><span class="sxs-lookup"><span data-stu-id="11c75-110">EXAMPLES</span></span>

### <span data-ttu-id="11c75-111">範例 1：建立標準金鑰庫</span><span class="sxs-lookup"><span data-stu-id="11c75-111">Example 1: Create a Standard key vault</span></span>
```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'

Vault Name                       : contoso03vault
Resource Group Name              : group14
Location                         : East US
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/group14/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : False
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             :
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : get, create, delete, list, update,
                                   import, backup, restore, recover
                                   Permissions to Secrets                     : get, list, set, delete, backup,
                                   restore, recover
                                   Permissions to Certificates                : get, delete, list, create, import,
                                   update, deleteissuers, getissuers, listissuers, managecontacts, manageissuers,
                                   setissuers, recover, backup, restore
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update, recover, backup, restore

Tags                             :
```

<span data-ttu-id="11c75-112">此命令會在美國東部 Azure 地區建立名為 Contoso03Vault 的金鑰庫。</span><span class="sxs-lookup"><span data-stu-id="11c75-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="11c75-113">該命令會將金鑰庫新增到名為 Group14 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="11c75-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="11c75-114">由於命令不會為 *SKU* 參數指定值，因此會建立標準金鑰庫。</span><span class="sxs-lookup"><span data-stu-id="11c75-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="11c75-115">範例 2：建立進一步金鑰庫</span><span class="sxs-lookup"><span data-stu-id="11c75-115">Example 2: Create a Premium key vault</span></span>
```powershell
PS C:\>New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -Sku 'Premium'

Vault Name                       : contoso03vault
Resource Group Name              : group14
Location                         : East US
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/group14/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Premium
Enabled For Deployment?          : False
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             :
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : get, create, delete, list, update,
                                   import, backup, restore, recover
                                   Permissions to Secrets                     : get, list, set, delete, backup,
                                   restore, recover
                                   Permissions to Certificates                : get, delete, list, create, import,
                                   update, deleteissuers, getissuers, listissuers, managecontacts, manageissuers,
                                   setissuers, recover, backup, restore
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update, recover, backup, restore

Tags                             :
```

<span data-ttu-id="11c75-116">此命令會建立金鑰庫，就像上一個範例一樣。</span><span class="sxs-lookup"><span data-stu-id="11c75-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="11c75-117">不過，它會指定 *SKU* 參數的 Premium 值，以建立進位金鑰庫。</span><span class="sxs-lookup"><span data-stu-id="11c75-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

### <span data-ttu-id="11c75-118">範例 3</span><span class="sxs-lookup"><span data-stu-id="11c75-118">Example 3</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "110.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "110.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> $ruleSet = New-AzKeyVaultNetworkRuleSetObject -DefaultAction Allow -Bypass AzureServices -IpAddressRange "110.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId
PS C:\> New-AzKeyVault -ResourceGroupName "myRg" -VaultName "myVault" -NetworkRuleSet $ruleSet
```

<span data-ttu-id="11c75-119">建立金鑰庫並指定網路規則，以允許從由使用者識別的$myNetworkResId。</span><span class="sxs-lookup"><span data-stu-id="11c75-119">Creating a key vault and specifies network rules to allow access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span> <span data-ttu-id="11c75-120">請參閱 `New-AzKeyVaultNetworkRuleSetObject` 詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="11c75-120">See `New-AzKeyVaultNetworkRuleSetObject` for more information.</span></span>

## <span data-ttu-id="11c75-121">參數</span><span class="sxs-lookup"><span data-stu-id="11c75-121">PARAMETERS</span></span>

### <span data-ttu-id="11c75-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11c75-122">-DefaultProfile</span></span>
<span data-ttu-id="11c75-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="11c75-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11c75-124">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="11c75-124">-EnabledForDeployment</span></span>
<span data-ttu-id="11c75-125">當資源建立中參照此金鑰庫時 ，例如建立虛擬機器時，可讓 Microsoft.Compute 資源提供者從這個金鑰庫中取回秘訣。</span><span class="sxs-lookup"><span data-stu-id="11c75-125">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11c75-126">-EnabledForCryptEncryption</span><span class="sxs-lookup"><span data-stu-id="11c75-126">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="11c75-127">啟用 Azure 磁片加密服務，以取得金鑰庫中的金鑰和解包金鑰。</span><span class="sxs-lookup"><span data-stu-id="11c75-127">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11c75-128">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="11c75-128">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="11c75-129">當範本部署中參照此金鑰庫時，可讓 Azure Resource Manager 從此金鑰庫取得秘訣。</span><span class="sxs-lookup"><span data-stu-id="11c75-129">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11c75-130">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="11c75-130">-EnablePurgeProtection</span></span>
<span data-ttu-id="11c75-131">如果指定，此儲存庫會啟用防止立即刪除的保護;也需要啟用柔刪除。</span><span class="sxs-lookup"><span data-stu-id="11c75-131">If specified, protection against immediate deletion is enabled for this vault; requires soft delete to be enabled as well.</span></span>

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

### <span data-ttu-id="11c75-132">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="11c75-132">-EnableRbacAuthorization</span></span>
<span data-ttu-id="11c75-133">如果指定，啟用由角色型存取控制 (RBAC) 授權資料動作，然後會忽略在 Vault 屬性中指定的存取策略。</span><span class="sxs-lookup"><span data-stu-id="11c75-133">If specified, enables to authorize data actions by Role Based Access Control (RBAC), and then the access policies specified in vault properties will be ignored.</span></span> <span data-ttu-id="11c75-134">請注意，管理動作一直獲得 RBAC 的授權。</span><span class="sxs-lookup"><span data-stu-id="11c75-134">Note that management actions are always authorized with RBAC.</span></span>

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

### <span data-ttu-id="11c75-135">-位置</span><span class="sxs-lookup"><span data-stu-id="11c75-135">-Location</span></span>
<span data-ttu-id="11c75-136">指定要建立金鑰庫的 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="11c75-136">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="11c75-137">使用 [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) 命令來查看您的選擇。</span><span class="sxs-lookup"><span data-stu-id="11c75-137">Use the command [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) to see your choices.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11c75-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="11c75-138">-Name</span></span>
<span data-ttu-id="11c75-139">指定要建立之金鑰庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="11c75-139">Specifies a name of the key vault to create.</span></span> <span data-ttu-id="11c75-140">名稱可以是字母、數位或連字號的任何組合。</span><span class="sxs-lookup"><span data-stu-id="11c75-140">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="11c75-141">名稱必須以字母或數位做為開頭和結尾。</span><span class="sxs-lookup"><span data-stu-id="11c75-141">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="11c75-142">名稱必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="11c75-142">The name must be universally unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VaultName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11c75-143">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="11c75-143">-NetworkRuleSet</span></span>
<span data-ttu-id="11c75-144">指定儲存庫的網路規則集。</span><span class="sxs-lookup"><span data-stu-id="11c75-144">Specifies the network rule set of the vault.</span></span> <span data-ttu-id="11c75-145">它規範特定網路位置之金鑰庫的協助工具。</span><span class="sxs-lookup"><span data-stu-id="11c75-145">It governs the accessibility of the key vault from specific network locations.</span></span> <span data-ttu-id="11c75-146">建立者 `New-AzKeyVaultNetworkRuleSetObject` 。</span><span class="sxs-lookup"><span data-stu-id="11c75-146">Created by `New-AzKeyVaultNetworkRuleSetObject`.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11c75-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11c75-147">-ResourceGroupName</span></span>
<span data-ttu-id="11c75-148">指定要建立金鑰庫之現有資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="11c75-148">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11c75-149">-SKU</span><span class="sxs-lookup"><span data-stu-id="11c75-149">-Sku</span></span>
<span data-ttu-id="11c75-150">指定金鑰庫實例的 SKU。</span><span class="sxs-lookup"><span data-stu-id="11c75-150">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="11c75-151">有關每個 SKU 提供哪些功能的詳細資訊，請參閱 Azure 金鑰庫定價網站 https://go.microsoft.com/fwlink/?linkid=512521) (。</span><span class="sxs-lookup"><span data-stu-id="11c75-151">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11c75-152">-SoftDeleteRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="11c75-152">-SoftDeleteRetentionInDays</span></span>
<span data-ttu-id="11c75-153">指定已刪除的資源會保留多久，以及保存庫或已刪除狀態的物件可以清除多久。</span><span class="sxs-lookup"><span data-stu-id="11c75-153">Specifies how long deleted resources are retained, and how long until a vault or an object in the deleted state can be purged.</span></span> <span data-ttu-id="11c75-154">預設值為 90 天。</span><span class="sxs-lookup"><span data-stu-id="11c75-154">The default is 90 days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11c75-155">-標記</span><span class="sxs-lookup"><span data-stu-id="11c75-155">-Tag</span></span>
<span data-ttu-id="11c75-156">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="11c75-156">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="11c75-157">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="11c75-157">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="11c75-158">-確認</span><span class="sxs-lookup"><span data-stu-id="11c75-158">-Confirm</span></span>
<span data-ttu-id="11c75-159">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="11c75-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11c75-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11c75-160">-WhatIf</span></span>
<span data-ttu-id="11c75-161">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="11c75-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11c75-162">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11c75-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11c75-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11c75-163">CommonParameters</span></span>
<span data-ttu-id="11c75-164">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="11c75-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11c75-165">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11c75-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11c75-166">輸入</span><span class="sxs-lookup"><span data-stu-id="11c75-166">INPUTS</span></span>

### <span data-ttu-id="11c75-167">System.String</span><span class="sxs-lookup"><span data-stu-id="11c75-167">System.String</span></span>

### <span data-ttu-id="11c75-168">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="11c75-168">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="11c75-169">Microsoft.Azure.management.KeyVault.models.SkuName</span><span class="sxs-lookup"><span data-stu-id="11c75-169">Microsoft.Azure.Management.KeyVault.Models.SkuName</span></span>

### <span data-ttu-id="11c75-170">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="11c75-170">System.Collections.Hashtable</span></span>

## <span data-ttu-id="11c75-171">輸出</span><span class="sxs-lookup"><span data-stu-id="11c75-171">OUTPUTS</span></span>

### <span data-ttu-id="11c75-172">Microsoft.Azure.Commands.KeyVault.models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="11c75-172">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="11c75-173">筆記</span><span class="sxs-lookup"><span data-stu-id="11c75-173">NOTES</span></span>

## <span data-ttu-id="11c75-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="11c75-174">RELATED LINKS</span></span>

[<span data-ttu-id="11c75-175">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="11c75-175">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="11c75-176">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="11c75-176">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
