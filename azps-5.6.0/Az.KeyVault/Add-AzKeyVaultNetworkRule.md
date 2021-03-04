---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/add-azkeyvaultnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultNetworkRule.md
ms.openlocfilehash: dda32611087046a9e31f9e2d00edc8f648180fe5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903598"
---
# <span data-ttu-id="8469c-101">Add-AzKeyVaultNetworkRule</span><span class="sxs-lookup"><span data-stu-id="8469c-101">Add-AzKeyVaultNetworkRule</span></span>

## <span data-ttu-id="8469c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8469c-102">SYNOPSIS</span></span>
<span data-ttu-id="8469c-103">新增根據用戶端網際網路位址限制金鑰庫存取的規則。</span><span class="sxs-lookup"><span data-stu-id="8469c-103">Adds a rule meant to restrict access to a key vault based on the client's internet address.</span></span>

## <span data-ttu-id="8469c-104">語法</span><span class="sxs-lookup"><span data-stu-id="8469c-104">SYNTAX</span></span>

### <span data-ttu-id="8469c-105">ByVaultName (預設) </span><span class="sxs-lookup"><span data-stu-id="8469c-105">ByVaultName (Default)</span></span>
```
Add-AzKeyVaultNetworkRule [-VaultName] <String> [[-ResourceGroupName] <String>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8469c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8469c-106">ByInputObject</span></span>
```
Add-AzKeyVaultNetworkRule [-InputObject] <PSKeyVault> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8469c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8469c-107">ByResourceId</span></span>
```
Add-AzKeyVaultNetworkRule [-ResourceId] <String> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8469c-108">描述</span><span class="sxs-lookup"><span data-stu-id="8469c-108">DESCRIPTION</span></span>
<span data-ttu-id="8469c-109">**Add-AzKeyVaultNetworkRule** Cmdlet 會授予或限制一組由他們的 IP 位址或所屬的虛擬機器所指定的來電者存取金鑰庫。</span><span class="sxs-lookup"><span data-stu-id="8469c-109">The **Add-AzKeyVaultNetworkRule** cmdlet grants or restricts access to a key vault to a set of caller designated by their IP addresses or the virtual network to which they belong.</span></span> <span data-ttu-id="8469c-110">規則可能會限制已透過存取原則獲授予許可權的其他使用者、應用程式或安全性群組的存取權限。</span><span class="sxs-lookup"><span data-stu-id="8469c-110">The rule has the potential to restrict access for other users, applications, or security groups which have been granted permissions via the access policy.</span></span>

<span data-ttu-id="8469c-111">請注意，私人 IP `10.0.0.0-10.255.255.255` 位址 (內的任何 IP) 無法用來新增網路規則。</span><span class="sxs-lookup"><span data-stu-id="8469c-111">Please note that any IP range inside `10.0.0.0-10.255.255.255` (private IP addresses) cannot be used to add network rules.</span></span>

## <span data-ttu-id="8469c-112">例子</span><span class="sxs-lookup"><span data-stu-id="8469c-112">EXAMPLES</span></span>

### <span data-ttu-id="8469c-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="8469c-113">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault 
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Add-AzKeyVaultNetworkRule -VaultName myvault -IpAddressRange "10.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId -PassThru

Vault Name                       : myvault
Resource Group Name              : myRG
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myRG/providers
                                   /Microsoft.KeyVault/vaults/myvault
Vault URI                        : https://myvault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : True
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
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
                                   setissuers, recover
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update


Network Rule Set                 :
                                   Default Action                             : Allow
                                   Bypass                                     : AzureServices
                                   IP Rules                                   : 10.0.1.0/24
                                   Virtual Network Rules                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-
                                   xxxxxxxxxxxxx/resourcegroups/myRG/providers/microsoft.network/virtualnetworks/myvn
                                   et/subnets/frontendsubnet

Tags                             :
```

<span data-ttu-id="8469c-114">此命令會將網路規則新增到指定的儲存庫，允許從由使用者識別的$myNetworkResId。</span><span class="sxs-lookup"><span data-stu-id="8469c-114">This command adds a network rule to the specified vault, allowing access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span>

## <span data-ttu-id="8469c-115">參數</span><span class="sxs-lookup"><span data-stu-id="8469c-115">PARAMETERS</span></span>

### <span data-ttu-id="8469c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8469c-116">-DefaultProfile</span></span>
<span data-ttu-id="8469c-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8469c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8469c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8469c-118">-InputObject</span></span>
<span data-ttu-id="8469c-119">KeyVault 物件</span><span class="sxs-lookup"><span data-stu-id="8469c-119">KeyVault object</span></span>

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

### <span data-ttu-id="8469c-120">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="8469c-120">-IpAddressRange</span></span>
<span data-ttu-id="8469c-121">指定網路規則的允許網路 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="8469c-121">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="8469c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8469c-122">-PassThru</span></span>
<span data-ttu-id="8469c-123">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="8469c-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="8469c-124">如果指定此參數，會返回更新的金鑰庫物件。</span><span class="sxs-lookup"><span data-stu-id="8469c-124">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="8469c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8469c-125">-ResourceGroupName</span></span>
<span data-ttu-id="8469c-126">指定與正在修改其網路規則之金鑰庫相關聯的資源組名。</span><span class="sxs-lookup"><span data-stu-id="8469c-126">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="8469c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8469c-127">-ResourceId</span></span>
<span data-ttu-id="8469c-128">KeyVault 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="8469c-128">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="8469c-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8469c-129">-VaultName</span></span>
<span data-ttu-id="8469c-130">指定正在修改其網路規則的金鑰庫名稱。</span><span class="sxs-lookup"><span data-stu-id="8469c-130">Specifies the name of a key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="8469c-131">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="8469c-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="8469c-132">指定網路規則的允許虛擬網路資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8469c-132">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="8469c-133">-確認</span><span class="sxs-lookup"><span data-stu-id="8469c-133">-Confirm</span></span>
<span data-ttu-id="8469c-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8469c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8469c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8469c-135">-WhatIf</span></span>
<span data-ttu-id="8469c-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8469c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8469c-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8469c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8469c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8469c-138">CommonParameters</span></span>
<span data-ttu-id="8469c-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8469c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8469c-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8469c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8469c-141">輸入</span><span class="sxs-lookup"><span data-stu-id="8469c-141">INPUTS</span></span>

### <span data-ttu-id="8469c-142">Microsoft.Azure.Commands.KeyVault.models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="8469c-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="8469c-143">System.String</span><span class="sxs-lookup"><span data-stu-id="8469c-143">System.String</span></span>

## <span data-ttu-id="8469c-144">輸出</span><span class="sxs-lookup"><span data-stu-id="8469c-144">OUTPUTS</span></span>

### <span data-ttu-id="8469c-145">Microsoft.Azure.Commands.KeyVault.models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="8469c-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="8469c-146">筆記</span><span class="sxs-lookup"><span data-stu-id="8469c-146">NOTES</span></span>

## <span data-ttu-id="8469c-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="8469c-147">RELATED LINKS</span></span>
