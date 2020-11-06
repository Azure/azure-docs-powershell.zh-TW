---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurermkeyvaultnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureRmKeyVaultNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureRmKeyVaultNetworkRule.md
ms.openlocfilehash: c99b621a39df1be595ceb873d85f5a3d848abc88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446991"
---
# <span data-ttu-id="fd955-101">Add-AzureRmKeyVaultNetworkRule</span><span class="sxs-lookup"><span data-stu-id="fd955-101">Add-AzureRmKeyVaultNetworkRule</span></span>

## <span data-ttu-id="fd955-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fd955-102">SYNOPSIS</span></span>
<span data-ttu-id="fd955-103">新增規則，旨在根據用戶端的網際網路位址限制存取金鑰 vault。</span><span class="sxs-lookup"><span data-stu-id="fd955-103">Adds a rule meant to restrict access to a key vault based on the client's internet address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd955-104">句法</span><span class="sxs-lookup"><span data-stu-id="fd955-104">SYNTAX</span></span>

### <span data-ttu-id="fd955-105">ByVaultName (預設) </span><span class="sxs-lookup"><span data-stu-id="fd955-105">ByVaultName (Default)</span></span>
```
Add-AzureRmKeyVaultNetworkRule [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd955-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fd955-106">ByInputObject</span></span>
```
Add-AzureRmKeyVaultNetworkRule [-InputObject] <PSKeyVault> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd955-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fd955-107">ByResourceId</span></span>
```
Add-AzureRmKeyVaultNetworkRule [-ResourceId] <String> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd955-108">說明</span><span class="sxs-lookup"><span data-stu-id="fd955-108">DESCRIPTION</span></span>
<span data-ttu-id="fd955-109">**AzureRmKeyVaultNetworkRule** Cmdlet 會將金鑰保存庫的存取權授予或限制為一組呼叫者，由其 IP 位址或其所屬的虛擬網路所指定。</span><span class="sxs-lookup"><span data-stu-id="fd955-109">The **Add-AzureRmKeyVaultNetworkRule** cmdlet grants or restricts access to a key vault to a set of caller designated by their IP addresses or the virtual network to which they belong.</span></span> <span data-ttu-id="fd955-110">規則有可能會限制其他使用者、應用程式或安全性群組的存取權，這些使用者已透過存取原則授與許可權。</span><span class="sxs-lookup"><span data-stu-id="fd955-110">The rule has the potential to restrict access for other users, applications, or security groups which have been granted permissions via the access policy.</span></span>

## <span data-ttu-id="fd955-111">示例</span><span class="sxs-lookup"><span data-stu-id="fd955-111">EXAMPLES</span></span>

### <span data-ttu-id="fd955-112">範例1</span><span class="sxs-lookup"><span data-stu-id="fd955-112">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault 
PS C:\> $virtualNetwork = New-AzureRmVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzureRmVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Add-AzureRmKeyVaultNetworkRule -VaultName myvault -IpAddressRange "10.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId -PassThru

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

<span data-ttu-id="fd955-113">這個命令會在指定的電子倉庫中新增一個網路規則，以允許從 $myNetworkResId 識別的虛擬網路存取指定的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="fd955-113">This command adds a network rule to the specified vault, allowing access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span>

## <span data-ttu-id="fd955-114">參數</span><span class="sxs-lookup"><span data-stu-id="fd955-114">PARAMETERS</span></span>

### <span data-ttu-id="fd955-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd955-115">-DefaultProfile</span></span>
<span data-ttu-id="fd955-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fd955-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd955-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd955-117">-InputObject</span></span>
<span data-ttu-id="fd955-118">KeyVault 物件</span><span class="sxs-lookup"><span data-stu-id="fd955-118">KeyVault object</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd955-119">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="fd955-119">-IpAddressRange</span></span>
<span data-ttu-id="fd955-120">指定允許的網路 IP 位址範圍（網路規則）。</span><span class="sxs-lookup"><span data-stu-id="fd955-120">Specifies allowed network IP address range of network rule.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd955-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd955-121">-PassThru</span></span>
<span data-ttu-id="fd955-122">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="fd955-122">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="fd955-123">如果指定此參數，則會傳回更新的金鑰 vault 物件。</span><span class="sxs-lookup"><span data-stu-id="fd955-123">If this switch is specified, it returns the updated key vault object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd955-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd955-124">-ResourceGroupName</span></span>
<span data-ttu-id="fd955-125">指定與要修改之網路規則之 [主要電子倉庫] 相關聯之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fd955-125">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd955-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd955-126">-ResourceId</span></span>
<span data-ttu-id="fd955-127">KeyVault 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="fd955-127">KeyVault Resource Id</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd955-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fd955-128">-VaultName</span></span>
<span data-ttu-id="fd955-129">指定要修改其網路規則之金鑰保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="fd955-129">Specifies the name of a key vault whose network rule is being modified.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd955-130">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="fd955-130">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="fd955-131">指定網路規則的 [允許的虛擬網路資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="fd955-131">Specifies allowed virtual network resource identifier of network rule.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd955-132">-確認</span><span class="sxs-lookup"><span data-stu-id="fd955-132">-Confirm</span></span>
<span data-ttu-id="fd955-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fd955-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd955-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd955-134">-WhatIf</span></span>
<span data-ttu-id="fd955-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fd955-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd955-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fd955-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd955-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd955-137">CommonParameters</span></span>
<span data-ttu-id="fd955-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fd955-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd955-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fd955-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd955-140">輸入</span><span class="sxs-lookup"><span data-stu-id="fd955-140">INPUTS</span></span>

### <span data-ttu-id="fd955-141">PSKeyVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="fd955-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="fd955-142">輸出</span><span class="sxs-lookup"><span data-stu-id="fd955-142">OUTPUTS</span></span>

### <span data-ttu-id="fd955-143">PSKeyVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="fd955-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="fd955-144">筆記</span><span class="sxs-lookup"><span data-stu-id="fd955-144">NOTES</span></span>

## <span data-ttu-id="fd955-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="fd955-145">RELATED LINKS</span></span>
