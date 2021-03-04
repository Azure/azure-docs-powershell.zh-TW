---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/undo-azkeyvaultremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultRemoval.md
ms.openlocfilehash: ff7dea63b4731b4a2a6becfc31d0b312345978bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908173"
---
# <span data-ttu-id="9293e-101">Undo-AzKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="9293e-101">Undo-AzKeyVaultRemoval</span></span>

## <span data-ttu-id="9293e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9293e-102">SYNOPSIS</span></span>
<span data-ttu-id="9293e-103">將已刪除的金鑰庫復原為使用中狀態。</span><span class="sxs-lookup"><span data-stu-id="9293e-103">Recovers a deleted key vault into an active state.</span></span>

## <span data-ttu-id="9293e-104">語法</span><span class="sxs-lookup"><span data-stu-id="9293e-104">SYNTAX</span></span>

### <span data-ttu-id="9293e-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="9293e-105">Default (Default)</span></span>
```
Undo-AzKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9293e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="9293e-106">InputObject</span></span>
```
Undo-AzKeyVaultRemoval [-InputObject] <PSDeletedKeyVault> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9293e-107">描述</span><span class="sxs-lookup"><span data-stu-id="9293e-107">DESCRIPTION</span></span>
<span data-ttu-id="9293e-108">**Undo-AzKeyVaultRemoval** Cmdlet 會復原先前刪除的金鑰庫。</span><span class="sxs-lookup"><span data-stu-id="9293e-108">The **Undo-AzKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="9293e-109">復原後，復原的儲存庫將會為使用中狀態</span><span class="sxs-lookup"><span data-stu-id="9293e-109">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="9293e-110">例子</span><span class="sxs-lookup"><span data-stu-id="9293e-110">EXAMPLES</span></span>

### <span data-ttu-id="9293e-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="9293e-111">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultRemoval -VaultName 'MyKeyVault' -ResourceGroupName 'MyResourceGroup' -Location 'eastus2' -Tag @{"x"= "y"}

Vault Name                       : MyKeyVault
Resource Group Name              : MyResourceGroup
Location                         : eastus2
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers
                                   /Microsoft.KeyVault/vaults/mykeyvault
Vault URI                        : https://mykeyvault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : True
Enabled For Disk Encryption?     : True
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

Tags                             :
                                   Name  Value
                                   ====  =====
                                   x     y
```

<span data-ttu-id="9293e-112">此命令將復原先前從 eastus2 地區和 'MyResourceGroup' 資源群組刪除的金鑰庫 'MyKeyVault'，進入作用中且可使用的狀態。</span><span class="sxs-lookup"><span data-stu-id="9293e-112">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="9293e-113">它也以新的標記取代標記。</span><span class="sxs-lookup"><span data-stu-id="9293e-113">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="9293e-114">參數</span><span class="sxs-lookup"><span data-stu-id="9293e-114">PARAMETERS</span></span>

### <span data-ttu-id="9293e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9293e-115">-DefaultProfile</span></span>
<span data-ttu-id="9293e-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="9293e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9293e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9293e-117">-InputObject</span></span>
<span data-ttu-id="9293e-118">已刪除的庫物件</span><span class="sxs-lookup"><span data-stu-id="9293e-118">Deleted vault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9293e-119">-位置</span><span class="sxs-lookup"><span data-stu-id="9293e-119">-Location</span></span>
<span data-ttu-id="9293e-120">指定已刪除的庫原始 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="9293e-120">Specifies the deleted vault original Azure region.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9293e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9293e-121">-ResourceGroupName</span></span>
<span data-ttu-id="9293e-122">指定要建立金鑰庫之現有資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9293e-122">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9293e-123">-標記</span><span class="sxs-lookup"><span data-stu-id="9293e-123">-Tag</span></span>
<span data-ttu-id="9293e-124">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="9293e-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9293e-125">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="9293e-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9293e-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9293e-126">-VaultName</span></span>
<span data-ttu-id="9293e-127">儲存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="9293e-127">Vault name.</span></span>
<span data-ttu-id="9293e-128">Cmdlet 會根據名稱和目前選取的環境來建構庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="9293e-128">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9293e-129">-確認</span><span class="sxs-lookup"><span data-stu-id="9293e-129">-Confirm</span></span>
<span data-ttu-id="9293e-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9293e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9293e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9293e-131">-WhatIf</span></span>
<span data-ttu-id="9293e-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9293e-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9293e-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9293e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9293e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9293e-134">CommonParameters</span></span>
<span data-ttu-id="9293e-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9293e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9293e-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9293e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9293e-137">輸入</span><span class="sxs-lookup"><span data-stu-id="9293e-137">INPUTS</span></span>

### <span data-ttu-id="9293e-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="9293e-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

## <span data-ttu-id="9293e-139">輸出</span><span class="sxs-lookup"><span data-stu-id="9293e-139">OUTPUTS</span></span>

### <span data-ttu-id="9293e-140">Microsoft.Azure.Commands.KeyVault.models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="9293e-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="9293e-141">筆記</span><span class="sxs-lookup"><span data-stu-id="9293e-141">NOTES</span></span>

## <span data-ttu-id="9293e-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="9293e-142">RELATED LINKS</span></span>

[<span data-ttu-id="9293e-143">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="9293e-143">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)

[<span data-ttu-id="9293e-144">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="9293e-144">New-AzKeyVault</span></span>](./New-AzKeyVault.md)

[<span data-ttu-id="9293e-145">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="9293e-145">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)
