---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/update-azkeyvaultnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultNetworkRuleSet.md
ms.openlocfilehash: d71712067b546e4147dff49b15dcf6466550131c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908142"
---
# <span data-ttu-id="383d4-101">Update-AzKeyVaultNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="383d4-101">Update-AzKeyVaultNetworkRuleSet</span></span>

## <span data-ttu-id="383d4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="383d4-102">SYNOPSIS</span></span>
<span data-ttu-id="383d4-103">更新金鑰庫上的網路規則集。</span><span class="sxs-lookup"><span data-stu-id="383d4-103">Updates the network rule set on a key vault.</span></span>

## <span data-ttu-id="383d4-104">語法</span><span class="sxs-lookup"><span data-stu-id="383d4-104">SYNTAX</span></span>

### <span data-ttu-id="383d4-105">ByVaultName (預設) </span><span class="sxs-lookup"><span data-stu-id="383d4-105">ByVaultName (Default)</span></span>
```
Update-AzKeyVaultNetworkRuleSet [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="383d4-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="383d4-106">ByInputObject</span></span>
```
Update-AzKeyVaultNetworkRuleSet [-InputObject] <PSKeyVault>
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="383d4-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="383d4-107">ByResourceId</span></span>
```
Update-AzKeyVaultNetworkRuleSet [-ResourceId] <String>
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="383d4-108">描述</span><span class="sxs-lookup"><span data-stu-id="383d4-108">DESCRIPTION</span></span>
<span data-ttu-id="383d4-109">**Update-AzKeyVaultNetworkRuleSet 命令** 會更新指定金鑰庫上生效的網路規則。</span><span class="sxs-lookup"><span data-stu-id="383d4-109">The **Update-AzKeyVaultNetworkRuleSet** command updates the network rules in effect on the specified key vault.</span></span> 

## <span data-ttu-id="383d4-110">例子</span><span class="sxs-lookup"><span data-stu-id="383d4-110">EXAMPLES</span></span>

### <span data-ttu-id="383d4-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="383d4-111">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault 
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Update-AzKeyVaultNetworkRuleSet -VaultName 'myVault' -ResourceGroupName myRG -Bypass AzureServices -IpAddressRange "10.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId -PassThru

Vault Name                       : myVault
Resource Group Name              : myRG
Location                         : West US
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/myvault
Vault URI                        : https://myvault.vault.azure.net/
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


Network Rule Set                 :
                                   Default Action                             : Allow
                                   Bypass                                     : AzureServices
                                   IP Rules                                   : 10.0.1.0/24
                                   Virtual Network Rules                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-
                                   xxxxxxxxxxxxx/resourcegroups/myrg/providers/microsoft.network/virtualnetworks/myvn
                                   et/subnets/frontendsubnet

Tags                             :
```

<span data-ttu-id="383d4-112">此命令會更新指定 IP 範圍和虛擬網路名稱為 "myVault" 的儲存庫上的網路規則集，允許忽略 Azure 服務的網路規則。</span><span class="sxs-lookup"><span data-stu-id="383d4-112">This command updates the network ruleset on the vault named 'myVault' for the specified IP range and the virtual network, allowing bypassing of the network rule for Azure services.</span></span>

### <span data-ttu-id="383d4-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="383d4-113">Example 2</span></span>

<span data-ttu-id="383d4-114">更新金鑰庫上的網路規則集。</span><span class="sxs-lookup"><span data-stu-id="383d4-114">Updates the network rule set on a key vault.</span></span> <span data-ttu-id="383d4-115"> (自動) </span><span class="sxs-lookup"><span data-stu-id="383d4-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Update-AzKeyVaultNetworkRuleSet -DefaultAction Allow -VaultName 'myVault'
```

## <span data-ttu-id="383d4-116">參數</span><span class="sxs-lookup"><span data-stu-id="383d4-116">PARAMETERS</span></span>

### <span data-ttu-id="383d4-117">-旁路</span><span class="sxs-lookup"><span data-stu-id="383d4-117">-Bypass</span></span>
<span data-ttu-id="383d4-118">指定忽略網路規則。</span><span class="sxs-lookup"><span data-stu-id="383d4-118">Specifies bypass of network rule.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleBypassEnum]
Parameter Sets: (All)
Aliases:
Accepted values: None, AzureServices

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="383d4-119">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="383d4-119">-DefaultAction</span></span>
<span data-ttu-id="383d4-120">指定網路規則的預設動作。</span><span class="sxs-lookup"><span data-stu-id="383d4-120">Specifies default action of network rule.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleDefaultActionEnum]
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="383d4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="383d4-121">-DefaultProfile</span></span>
<span data-ttu-id="383d4-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="383d4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="383d4-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="383d4-123">-InputObject</span></span>
<span data-ttu-id="383d4-124">KeyVault 物件</span><span class="sxs-lookup"><span data-stu-id="383d4-124">KeyVault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="383d4-125">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="383d4-125">-IpAddressRange</span></span>
<span data-ttu-id="383d4-126">指定網路規則的允許網路 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="383d4-126">Specifies allowed network IP address range of network rule.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="383d4-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="383d4-127">-PassThru</span></span>
<span data-ttu-id="383d4-128">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="383d4-128">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="383d4-129">如果指定此參數，會返回更新的金鑰庫物件。</span><span class="sxs-lookup"><span data-stu-id="383d4-129">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="383d4-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="383d4-130">-ResourceGroupName</span></span>
<span data-ttu-id="383d4-131">指定與正在修改其網路規則之金鑰庫相關聯的資源組名。</span><span class="sxs-lookup"><span data-stu-id="383d4-131">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="383d4-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="383d4-132">-ResourceId</span></span>
<span data-ttu-id="383d4-133">KeyVault 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="383d4-133">KeyVault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="383d4-134">-VaultName</span><span class="sxs-lookup"><span data-stu-id="383d4-134">-VaultName</span></span>
<span data-ttu-id="383d4-135">指定正在修改其網路規則的金鑰庫名稱。</span><span class="sxs-lookup"><span data-stu-id="383d4-135">Specifies the name of a key vault whose network rule is being modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="383d4-136">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="383d4-136">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="383d4-137">指定網路規則的允許虛擬網路資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="383d4-137">Specifies allowed virtual network resource identifier of network rule.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="383d4-138">-確認</span><span class="sxs-lookup"><span data-stu-id="383d4-138">-Confirm</span></span>
<span data-ttu-id="383d4-139">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="383d4-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="383d4-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="383d4-140">-WhatIf</span></span>
<span data-ttu-id="383d4-141">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="383d4-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="383d4-142">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="383d4-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="383d4-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="383d4-143">CommonParameters</span></span>
<span data-ttu-id="383d4-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="383d4-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="383d4-145">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="383d4-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="383d4-146">輸入</span><span class="sxs-lookup"><span data-stu-id="383d4-146">INPUTS</span></span>

### <span data-ttu-id="383d4-147">Microsoft.Azure.Commands.KeyVault.models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="383d4-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="383d4-148">System.String</span><span class="sxs-lookup"><span data-stu-id="383d4-148">System.String</span></span>

### <span data-ttu-id="383d4-149">System.Nullable'1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleDefaultActionEnum, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="383d4-149">System.Nullable\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleDefaultActionEnum, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="383d4-150">System.Nullable'1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleBypassEnum, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="383d4-150">System.Nullable\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleBypassEnum, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="383d4-151">輸出</span><span class="sxs-lookup"><span data-stu-id="383d4-151">OUTPUTS</span></span>

### <span data-ttu-id="383d4-152">Microsoft.Azure.Commands.KeyVault.models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="383d4-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="383d4-153">筆記</span><span class="sxs-lookup"><span data-stu-id="383d4-153">NOTES</span></span>

## <span data-ttu-id="383d4-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="383d4-154">RELATED LINKS</span></span>
