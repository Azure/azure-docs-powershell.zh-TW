---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
ms.openlocfilehash: a11e962e2af6beaa3f3004cec104530f7603bb3a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127678"
---
# <span data-ttu-id="90b31-101">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="90b31-101">New-AzKeyVault</span></span>

## <span data-ttu-id="90b31-102">摘要</span><span class="sxs-lookup"><span data-stu-id="90b31-102">SYNOPSIS</span></span>
<span data-ttu-id="90b31-103">建立金鑰電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="90b31-103">Creates a key vault.</span></span>

## <span data-ttu-id="90b31-104">句法</span><span class="sxs-lookup"><span data-stu-id="90b31-104">SYNTAX</span></span>

```
New-AzKeyVault [-Name] <String> [-ResourceGroupName] <String> [-Location] <String> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-DisableSoftDelete] [-EnablePurgeProtection]
 [-EnableRbacAuthorization] [-SoftDeleteRetentionInDays <Int32>] [-Sku <SkuName>] [-Tag <Hashtable>]
 [-NetworkRuleSet <PSKeyVaultNetworkRuleSet>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="90b31-105">說明</span><span class="sxs-lookup"><span data-stu-id="90b31-105">DESCRIPTION</span></span>
<span data-ttu-id="90b31-106">**新的-AzKeyVault** Cmdlet 會在指定的資源群組中建立金鑰 vault。</span><span class="sxs-lookup"><span data-stu-id="90b31-106">The **New-AzKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="90b31-107">這個 Cmdlet 也會授與目前登入的使用者在金鑰保存庫中新增、移除或列出金鑰及密碼的許可權。</span><span class="sxs-lookup"><span data-stu-id="90b31-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>
<span data-ttu-id="90b31-108">注意：如果您看到錯誤，表示您在嘗試建立新的金鑰保存庫時 **未登錄訂閱使用命名空間 ' KeyVault '** ，請執行 **Register-AzResourceProvider-ProviderNamespace "microsoft. KeyVault"** ，然後重新執行 **新的 AzKeyVault** 命令。</span><span class="sxs-lookup"><span data-stu-id="90b31-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzKeyVault** command.</span></span> <span data-ttu-id="90b31-109">如需詳細資訊，請參閱註冊 AzResourceProvider。</span><span class="sxs-lookup"><span data-stu-id="90b31-109">For more information, see Register-AzResourceProvider.</span></span>

## <span data-ttu-id="90b31-110">示例</span><span class="sxs-lookup"><span data-stu-id="90b31-110">EXAMPLES</span></span>

### <span data-ttu-id="90b31-111">範例1：建立標準的金鑰 vault</span><span class="sxs-lookup"><span data-stu-id="90b31-111">Example 1: Create a Standard key vault</span></span>
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

<span data-ttu-id="90b31-112">這個命令會在 Azure region （美國）中，建立一個名為 Contoso03Vault 的主要電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="90b31-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="90b31-113">該命令會將主要電子倉庫新增到名為 Group14 的資源群組中。</span><span class="sxs-lookup"><span data-stu-id="90b31-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="90b31-114">因為命令不會指定 *SKU* 參數的值，所以它會建立標準的金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="90b31-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="90b31-115">範例2：建立 Premium 金鑰電子倉庫</span><span class="sxs-lookup"><span data-stu-id="90b31-115">Example 2: Create a Premium key vault</span></span>
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

<span data-ttu-id="90b31-116">這個命令會建立一個金鑰 vault，就像前一個範例一樣。</span><span class="sxs-lookup"><span data-stu-id="90b31-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="90b31-117">不過，它會為 *SKU* 參數指定 premium 的值，以建立 Premium 金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="90b31-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

### <span data-ttu-id="90b31-118">範例3</span><span class="sxs-lookup"><span data-stu-id="90b31-118">Example 3</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "110.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "110.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> $ruleSet = New-AzKeyVaultNetworkRuleSetObject -DefaultAction Allow -Bypass AzureServices -IpAddressRange "110.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId
PS C:\> New-AzKeyVault -ResourceGroupName "myRg" -VaultName "myVault" -NetworkRuleSet $ruleSet
```

<span data-ttu-id="90b31-119">建立主要電子倉庫並指定網路規則，以允許從 $myNetworkResId 識別的虛擬網路存取指定的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="90b31-119">Creating a key vault and specifies network rules to allow access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span> <span data-ttu-id="90b31-120">如需詳細資訊，請參閱 `New-AzKeyVaultNetworkRuleSetObject` 。</span><span class="sxs-lookup"><span data-stu-id="90b31-120">See `New-AzKeyVaultNetworkRuleSetObject` for more information.</span></span>

## <span data-ttu-id="90b31-121">參數</span><span class="sxs-lookup"><span data-stu-id="90b31-121">PARAMETERS</span></span>

### <span data-ttu-id="90b31-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90b31-122">-DefaultProfile</span></span>
<span data-ttu-id="90b31-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="90b31-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90b31-124">-DisableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="90b31-124">-DisableSoftDelete</span></span>
<span data-ttu-id="90b31-125">如果已指定，將停用此金鑰保存庫的 [虛刪除] 功能。</span><span class="sxs-lookup"><span data-stu-id="90b31-125">If specified, 'soft delete' functionality is disabled for this key vault.</span></span>

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

### <span data-ttu-id="90b31-126">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="90b31-126">-EnabledForDeployment</span></span>
<span data-ttu-id="90b31-127">當在資源建立期間參照此金鑰保存庫時，可使用 Microsoft. 計算資源提供者來從此金鑰保存庫中取得機密資訊，例如建立虛擬機器時。</span><span class="sxs-lookup"><span data-stu-id="90b31-127">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="90b31-128">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="90b31-128">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="90b31-129">讓 Azure 磁片加密服務從此金鑰保存庫取得機密和解除解包金鑰。</span><span class="sxs-lookup"><span data-stu-id="90b31-129">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="90b31-130">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="90b31-130">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="90b31-131">在範本部署中參照此金鑰保存庫時，允許 Azure 資源管理員從該金鑰保存庫取得機密。</span><span class="sxs-lookup"><span data-stu-id="90b31-131">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="90b31-132">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="90b31-132">-EnablePurgeProtection</span></span>
<span data-ttu-id="90b31-133">如果已指定，就會針對此保存庫啟用 [防止立即刪除] 功能;還需啟用 [虛刪除]。</span><span class="sxs-lookup"><span data-stu-id="90b31-133">If specified, protection against immediate deletion is enabled for this vault; requires soft delete to be enabled as well.</span></span>

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

### <span data-ttu-id="90b31-134">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="90b31-134">-EnableRbacAuthorization</span></span>
<span data-ttu-id="90b31-135">如果已指定，則可透過角色的存取控制 (RBAC) 授權資料動作，然後會忽略在保存庫屬性中指定的存取原則。</span><span class="sxs-lookup"><span data-stu-id="90b31-135">If specified, enables to authorize data actions by Role Based Access Control (RBAC), and then the access policies specified in vault properties will be ignored.</span></span> <span data-ttu-id="90b31-136">請注意，管理動作總是使用 RBAC 進行授權。</span><span class="sxs-lookup"><span data-stu-id="90b31-136">Note that management actions are always authorized with RBAC.</span></span>

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

### <span data-ttu-id="90b31-137">-位置</span><span class="sxs-lookup"><span data-stu-id="90b31-137">-Location</span></span>
<span data-ttu-id="90b31-138">指定要在其中建立金鑰保存庫的 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="90b31-138">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="90b31-139">使用命令 [AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) 查看您的選擇。</span><span class="sxs-lookup"><span data-stu-id="90b31-139">Use the command [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) to see your choices.</span></span>

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

### <span data-ttu-id="90b31-140">-名稱</span><span class="sxs-lookup"><span data-stu-id="90b31-140">-Name</span></span>
<span data-ttu-id="90b31-141">指定要建立之金鑰保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="90b31-141">Specifies a name of the key vault to create.</span></span> <span data-ttu-id="90b31-142">名稱可以是字母、數位或連字號的任何組合。</span><span class="sxs-lookup"><span data-stu-id="90b31-142">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="90b31-143">名稱必須以字母或數位開頭和結尾。</span><span class="sxs-lookup"><span data-stu-id="90b31-143">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="90b31-144">名稱必須是通用唯一的。</span><span class="sxs-lookup"><span data-stu-id="90b31-144">The name must be universally unique.</span></span>

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

### <span data-ttu-id="90b31-145">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="90b31-145">-NetworkRuleSet</span></span>
<span data-ttu-id="90b31-146">指定電子倉庫的網路規則集。</span><span class="sxs-lookup"><span data-stu-id="90b31-146">Specifies the network rule set of the vault.</span></span> <span data-ttu-id="90b31-147">它會控制來自特定網路位置的主要電子倉庫的協助工具。</span><span class="sxs-lookup"><span data-stu-id="90b31-147">It governs the accessibility of the key vault from specific network locations.</span></span> <span data-ttu-id="90b31-148">建立者] `New-AzKeyVaultNetworkRuleSetObject` 。</span><span class="sxs-lookup"><span data-stu-id="90b31-148">Created by `New-AzKeyVaultNetworkRuleSetObject`.</span></span>

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

### <span data-ttu-id="90b31-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90b31-149">-ResourceGroupName</span></span>
<span data-ttu-id="90b31-150">指定要在其中建立金鑰保存庫的現有資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="90b31-150">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="90b31-151">-Sku</span><span class="sxs-lookup"><span data-stu-id="90b31-151">-Sku</span></span>
<span data-ttu-id="90b31-152">指定主要電子倉庫實例的 SKU。</span><span class="sxs-lookup"><span data-stu-id="90b31-152">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="90b31-153">如需有關每個 SKU 可用功能的詳細資訊，請參閱 Azure 金鑰 Vault 定價網站 (https://go.microsoft.com/fwlink/?linkid=512521) 。</span><span class="sxs-lookup"><span data-stu-id="90b31-153">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

```yaml
Type: Microsoft.Azure.Management.KeyVault.Models.SkuName
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90b31-154">-SoftDeleteRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="90b31-154">-SoftDeleteRetentionInDays</span></span>
<span data-ttu-id="90b31-155">指定保留刪除的資源的時間長度，以及要花多少時間，才能清除電子倉庫或刪除狀態中的物件。</span><span class="sxs-lookup"><span data-stu-id="90b31-155">Specifies how long deleted resources are retained, and how long until a vault or an object in the deleted state can be purged.</span></span> <span data-ttu-id="90b31-156">預設值為90天。</span><span class="sxs-lookup"><span data-stu-id="90b31-156">The default is 90 days.</span></span>

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

### <span data-ttu-id="90b31-157">-Tag</span><span class="sxs-lookup"><span data-stu-id="90b31-157">-Tag</span></span>
<span data-ttu-id="90b31-158">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="90b31-158">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="90b31-159">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="90b31-159">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="90b31-160">-確認</span><span class="sxs-lookup"><span data-stu-id="90b31-160">-Confirm</span></span>
<span data-ttu-id="90b31-161">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="90b31-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90b31-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90b31-162">-WhatIf</span></span>
<span data-ttu-id="90b31-163">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="90b31-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90b31-164">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="90b31-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90b31-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90b31-165">CommonParameters</span></span>
<span data-ttu-id="90b31-166">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="90b31-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90b31-167">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="90b31-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90b31-168">輸入</span><span class="sxs-lookup"><span data-stu-id="90b31-168">INPUTS</span></span>

### <span data-ttu-id="90b31-169">System.object</span><span class="sxs-lookup"><span data-stu-id="90b31-169">System.String</span></span>

### <span data-ttu-id="90b31-170">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="90b31-170">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="90b31-171">SkuName 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="90b31-171">Microsoft.Azure.Management.KeyVault.Models.SkuName</span></span>

### <span data-ttu-id="90b31-172">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="90b31-172">System.Collections.Hashtable</span></span>

## <span data-ttu-id="90b31-173">輸出</span><span class="sxs-lookup"><span data-stu-id="90b31-173">OUTPUTS</span></span>

### <span data-ttu-id="90b31-174">PSKeyVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="90b31-174">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="90b31-175">筆記</span><span class="sxs-lookup"><span data-stu-id="90b31-175">NOTES</span></span>

## <span data-ttu-id="90b31-176">相關連結</span><span class="sxs-lookup"><span data-stu-id="90b31-176">RELATED LINKS</span></span>

[<span data-ttu-id="90b31-177">AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="90b31-177">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="90b31-178">移除-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="90b31-178">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
