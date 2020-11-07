---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultNetworkRuleSet.md
ms.openlocfilehash: f20099fbd9dd2aa7a9fd6774892d29fbde7ce34b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787241"
---
# <span data-ttu-id="16f19-101">Update-AzKeyVaultNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="16f19-101">Update-AzKeyVaultNetworkRuleSet</span></span>

## <span data-ttu-id="16f19-102">摘要</span><span class="sxs-lookup"><span data-stu-id="16f19-102">SYNOPSIS</span></span>
<span data-ttu-id="16f19-103">更新主要電子倉庫上的網路規則集。</span><span class="sxs-lookup"><span data-stu-id="16f19-103">Updates the network rule set on a key vault.</span></span>

## <span data-ttu-id="16f19-104">句法</span><span class="sxs-lookup"><span data-stu-id="16f19-104">SYNTAX</span></span>

### <span data-ttu-id="16f19-105">ByVaultName (預設) </span><span class="sxs-lookup"><span data-stu-id="16f19-105">ByVaultName (Default)</span></span>
```
Update-AzKeyVaultNetworkRuleSet [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16f19-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="16f19-106">ByInputObject</span></span>
```
Update-AzKeyVaultNetworkRuleSet [-InputObject] <PSKeyVault>
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16f19-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="16f19-107">ByResourceId</span></span>
```
Update-AzKeyVaultNetworkRuleSet [-ResourceId] <String>
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16f19-108">說明</span><span class="sxs-lookup"><span data-stu-id="16f19-108">DESCRIPTION</span></span>
<span data-ttu-id="16f19-109">**更新-AzKeyVaultNetworkRuleSet** 命令會更新在指定的 [主要電子倉庫] 中生效的網路規則。</span><span class="sxs-lookup"><span data-stu-id="16f19-109">The **Update-AzKeyVaultNetworkRuleSet** command updates the network rules in effect on the specified key vault.</span></span> 

## <span data-ttu-id="16f19-110">示例</span><span class="sxs-lookup"><span data-stu-id="16f19-110">EXAMPLES</span></span>

### <span data-ttu-id="16f19-111">範例1</span><span class="sxs-lookup"><span data-stu-id="16f19-111">Example 1</span></span>
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

<span data-ttu-id="16f19-112">這個命令會針對指定的 IP 範圍和虛擬網路，在名為「myVault」的保存庫中，更新網路規則集，以允許避開 Azure 服務的網路規則。</span><span class="sxs-lookup"><span data-stu-id="16f19-112">This command updates the network ruleset on the vault named 'myVault' for the specified IP range and the virtual network, allowing bypassing of the network rule for Azure services.</span></span>

## <span data-ttu-id="16f19-113">參數</span><span class="sxs-lookup"><span data-stu-id="16f19-113">PARAMETERS</span></span>

### <span data-ttu-id="16f19-114">-略過</span><span class="sxs-lookup"><span data-stu-id="16f19-114">-Bypass</span></span>
<span data-ttu-id="16f19-115">指定 [繞過網路規則]。</span><span class="sxs-lookup"><span data-stu-id="16f19-115">Specifies bypass of network rule.</span></span>

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

### <span data-ttu-id="16f19-116">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="16f19-116">-DefaultAction</span></span>
<span data-ttu-id="16f19-117">指定網路規則的預設動作。</span><span class="sxs-lookup"><span data-stu-id="16f19-117">Specifies default action of network rule.</span></span>

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

### <span data-ttu-id="16f19-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16f19-118">-DefaultProfile</span></span>
<span data-ttu-id="16f19-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="16f19-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16f19-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16f19-120">-InputObject</span></span>
<span data-ttu-id="16f19-121">KeyVault 物件</span><span class="sxs-lookup"><span data-stu-id="16f19-121">KeyVault object</span></span>

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

### <span data-ttu-id="16f19-122">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="16f19-122">-IpAddressRange</span></span>
<span data-ttu-id="16f19-123">指定允許的網路 IP 位址範圍（網路規則）。</span><span class="sxs-lookup"><span data-stu-id="16f19-123">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="16f19-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16f19-124">-PassThru</span></span>
<span data-ttu-id="16f19-125">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="16f19-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="16f19-126">如果指定此參數，則會傳回更新的金鑰 vault 物件。</span><span class="sxs-lookup"><span data-stu-id="16f19-126">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="16f19-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16f19-127">-ResourceGroupName</span></span>
<span data-ttu-id="16f19-128">指定與要修改之網路規則之 [主要電子倉庫] 相關聯之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="16f19-128">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="16f19-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16f19-129">-ResourceId</span></span>
<span data-ttu-id="16f19-130">KeyVault 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="16f19-130">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="16f19-131">-VaultName</span><span class="sxs-lookup"><span data-stu-id="16f19-131">-VaultName</span></span>
<span data-ttu-id="16f19-132">指定要修改其網路規則之金鑰保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="16f19-132">Specifies the name of a key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="16f19-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="16f19-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="16f19-134">指定網路規則的 [允許的虛擬網路資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="16f19-134">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="16f19-135">-確認</span><span class="sxs-lookup"><span data-stu-id="16f19-135">-Confirm</span></span>
<span data-ttu-id="16f19-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="16f19-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16f19-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16f19-137">-WhatIf</span></span>
<span data-ttu-id="16f19-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="16f19-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16f19-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="16f19-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16f19-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16f19-140">CommonParameters</span></span>
<span data-ttu-id="16f19-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="16f19-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16f19-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="16f19-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16f19-143">輸入</span><span class="sxs-lookup"><span data-stu-id="16f19-143">INPUTS</span></span>

### <span data-ttu-id="16f19-144">PSKeyVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="16f19-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="16f19-145">System.object</span><span class="sxs-lookup"><span data-stu-id="16f19-145">System.String</span></span>

### <span data-ttu-id="16f19-146">KeyVault 為 Nullable "1 [PSKeyVaultNetworkRuleDefaultActionEnum，KeyVault，版本 = 1.0.0.0，Culture = 中性，PublicKeyToken = null]] （區域性 = 非特定語言）</span><span class="sxs-lookup"><span data-stu-id="16f19-146">System.Nullable\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleDefaultActionEnum, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="16f19-147">KeyVault 為 Nullable "1 [PSKeyVaultNetworkRuleBypassEnum，KeyVault，版本 = 1.0.0.0，Culture = 中性，PublicKeyToken = null]] （區域性 = 非特定語言）</span><span class="sxs-lookup"><span data-stu-id="16f19-147">System.Nullable\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleBypassEnum, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="16f19-148">輸出</span><span class="sxs-lookup"><span data-stu-id="16f19-148">OUTPUTS</span></span>

### <span data-ttu-id="16f19-149">PSKeyVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="16f19-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="16f19-150">筆記</span><span class="sxs-lookup"><span data-stu-id="16f19-150">NOTES</span></span>

## <span data-ttu-id="16f19-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="16f19-151">RELATED LINKS</span></span>
