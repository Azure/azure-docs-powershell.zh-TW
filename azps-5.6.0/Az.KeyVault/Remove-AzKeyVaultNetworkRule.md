---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultNetworkRule.md
ms.openlocfilehash: 6949de15168043e9ede9e8a023f6f5fcec333557
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902049"
---
# <span data-ttu-id="127a9-101">Remove-AzKeyVaultNetworkRule</span><span class="sxs-lookup"><span data-stu-id="127a9-101">Remove-AzKeyVaultNetworkRule</span></span>

## <span data-ttu-id="127a9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="127a9-102">SYNOPSIS</span></span>
<span data-ttu-id="127a9-103">從金鑰庫移除網路規則。</span><span class="sxs-lookup"><span data-stu-id="127a9-103">Removes a network rule from a key vault.</span></span>

## <span data-ttu-id="127a9-104">語法</span><span class="sxs-lookup"><span data-stu-id="127a9-104">SYNTAX</span></span>

### <span data-ttu-id="127a9-105">ByVaultName (預設) </span><span class="sxs-lookup"><span data-stu-id="127a9-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultNetworkRule [-VaultName] <String> [[-ResourceGroupName] <String>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="127a9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="127a9-106">ByInputObject</span></span>
```
Remove-AzKeyVaultNetworkRule [-InputObject] <PSKeyVault> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="127a9-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="127a9-107">ByResourceId</span></span>
```
Remove-AzKeyVaultNetworkRule [-ResourceId] <String> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="127a9-108">描述</span><span class="sxs-lookup"><span data-stu-id="127a9-108">DESCRIPTION</span></span>
<span data-ttu-id="127a9-109">從金鑰庫移除網路規則。</span><span class="sxs-lookup"><span data-stu-id="127a9-109">Removes a network rule from a key vault.</span></span>

## <span data-ttu-id="127a9-110">例子</span><span class="sxs-lookup"><span data-stu-id="127a9-110">EXAMPLES</span></span>

### <span data-ttu-id="127a9-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="127a9-111">Example 1</span></span>
```powershell
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNetName -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Remove-AzKeyVaultNetworkRule -VaultName myVault -IpAddressRange "10.0.0.1/26" -VirtualNetworkResourceId $myNetworkResId -PassThru

Vault Name                       : myVault
Resource Group Name              : myrg
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
                                   IP Rules                                   :
                                   Virtual Network Rules                      :

Tags                             :
```

<span data-ttu-id="127a9-112">如果找到符合指定 IP 位址和虛擬網路資源識別碼的規則，此命令會從指定的儲存庫移除網路規則。</span><span class="sxs-lookup"><span data-stu-id="127a9-112">This command removes a network rule from the specified vault, provided a rule is found matching the specified IP address and the virtual network resource identifier.</span></span>

## <span data-ttu-id="127a9-113">參數</span><span class="sxs-lookup"><span data-stu-id="127a9-113">PARAMETERS</span></span>

### <span data-ttu-id="127a9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="127a9-114">-DefaultProfile</span></span>
<span data-ttu-id="127a9-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="127a9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="127a9-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="127a9-116">-InputObject</span></span>
<span data-ttu-id="127a9-117">KeyVault 物件</span><span class="sxs-lookup"><span data-stu-id="127a9-117">KeyVault object</span></span>

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

### <span data-ttu-id="127a9-118">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="127a9-118">-IpAddressRange</span></span>
<span data-ttu-id="127a9-119">指定網路規則的允許網路 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="127a9-119">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="127a9-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="127a9-120">-PassThru</span></span>
<span data-ttu-id="127a9-121">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="127a9-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="127a9-122">如果指定此參數，會返回更新的金鑰庫物件。</span><span class="sxs-lookup"><span data-stu-id="127a9-122">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="127a9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="127a9-123">-ResourceGroupName</span></span>
<span data-ttu-id="127a9-124">指定與正在修改其網路規則之金鑰庫相關聯的資源組名。</span><span class="sxs-lookup"><span data-stu-id="127a9-124">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="127a9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="127a9-125">-ResourceId</span></span>
<span data-ttu-id="127a9-126">KeyVault 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="127a9-126">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="127a9-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="127a9-127">-VaultName</span></span>
<span data-ttu-id="127a9-128">指定正在修改其網路規則的金鑰庫名稱。</span><span class="sxs-lookup"><span data-stu-id="127a9-128">Specifies the name of a key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="127a9-129">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="127a9-129">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="127a9-130">指定網路規則的允許虛擬網路資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="127a9-130">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="127a9-131">-確認</span><span class="sxs-lookup"><span data-stu-id="127a9-131">-Confirm</span></span>
<span data-ttu-id="127a9-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="127a9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="127a9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="127a9-133">-WhatIf</span></span>
<span data-ttu-id="127a9-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="127a9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="127a9-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="127a9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="127a9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="127a9-136">CommonParameters</span></span>
<span data-ttu-id="127a9-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="127a9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="127a9-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="127a9-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="127a9-139">輸入</span><span class="sxs-lookup"><span data-stu-id="127a9-139">INPUTS</span></span>

### <span data-ttu-id="127a9-140">Microsoft.Azure.Commands.KeyVault.models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="127a9-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="127a9-141">System.String</span><span class="sxs-lookup"><span data-stu-id="127a9-141">System.String</span></span>

## <span data-ttu-id="127a9-142">輸出</span><span class="sxs-lookup"><span data-stu-id="127a9-142">OUTPUTS</span></span>

### <span data-ttu-id="127a9-143">Microsoft.Azure.Commands.KeyVault.models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="127a9-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="127a9-144">筆記</span><span class="sxs-lookup"><span data-stu-id="127a9-144">NOTES</span></span>

## <span data-ttu-id="127a9-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="127a9-145">RELATED LINKS</span></span>
