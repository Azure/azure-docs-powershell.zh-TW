---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultRemoval.md
ms.openlocfilehash: 98a3a023564c2c61f1398856e8a089276aeae7bc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434947"
---
# <span data-ttu-id="81312-101">Undo-AzKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="81312-101">Undo-AzKeyVaultRemoval</span></span>

## <span data-ttu-id="81312-102">摘要</span><span class="sxs-lookup"><span data-stu-id="81312-102">SYNOPSIS</span></span>
<span data-ttu-id="81312-103">將已刪除的金鑰電子倉庫恢復成作用中狀態。</span><span class="sxs-lookup"><span data-stu-id="81312-103">Recovers a deleted key vault into an active state.</span></span>

## <span data-ttu-id="81312-104">句法</span><span class="sxs-lookup"><span data-stu-id="81312-104">SYNTAX</span></span>

### <span data-ttu-id="81312-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="81312-105">Default (Default)</span></span>
```
Undo-AzKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81312-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="81312-106">InputObject</span></span>
```
Undo-AzKeyVaultRemoval [-InputObject] <PSDeletedKeyVault> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81312-107">說明</span><span class="sxs-lookup"><span data-stu-id="81312-107">DESCRIPTION</span></span>
<span data-ttu-id="81312-108">**Undo AzKeyVaultRemoval** Cmdlet 會復原先前刪除的主要保存庫。</span><span class="sxs-lookup"><span data-stu-id="81312-108">The **Undo-AzKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="81312-109">復原後的電子倉庫將在恢復後生效</span><span class="sxs-lookup"><span data-stu-id="81312-109">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="81312-110">示例</span><span class="sxs-lookup"><span data-stu-id="81312-110">EXAMPLES</span></span>

### <span data-ttu-id="81312-111">範例1</span><span class="sxs-lookup"><span data-stu-id="81312-111">Example 1</span></span>
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

<span data-ttu-id="81312-112">這個命令會將先前從 eastus2 區域和 "MyResourceGroup" 資源群組中刪除的主要保存庫 ' MyKeyVault ' 復原為作用中且可用的狀態。</span><span class="sxs-lookup"><span data-stu-id="81312-112">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="81312-113">它也會將標記取代為 [新增標籤]。</span><span class="sxs-lookup"><span data-stu-id="81312-113">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="81312-114">參數</span><span class="sxs-lookup"><span data-stu-id="81312-114">PARAMETERS</span></span>

### <span data-ttu-id="81312-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81312-115">-DefaultProfile</span></span>
<span data-ttu-id="81312-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="81312-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="81312-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81312-117">-InputObject</span></span>
<span data-ttu-id="81312-118">已刪除的保存庫物件</span><span class="sxs-lookup"><span data-stu-id="81312-118">Deleted vault object</span></span>

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

### <span data-ttu-id="81312-119">-位置</span><span class="sxs-lookup"><span data-stu-id="81312-119">-Location</span></span>
<span data-ttu-id="81312-120">指定已刪除的保存庫原始 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="81312-120">Specifies the deleted vault original Azure region.</span></span>

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

### <span data-ttu-id="81312-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81312-121">-ResourceGroupName</span></span>
<span data-ttu-id="81312-122">指定要在其中建立金鑰保存庫的現有資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="81312-122">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="81312-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="81312-123">-Tag</span></span>
<span data-ttu-id="81312-124">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="81312-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="81312-125">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="81312-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="81312-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="81312-126">-VaultName</span></span>
<span data-ttu-id="81312-127">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="81312-127">Vault name.</span></span>
<span data-ttu-id="81312-128">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="81312-128">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="81312-129">-確認</span><span class="sxs-lookup"><span data-stu-id="81312-129">-Confirm</span></span>
<span data-ttu-id="81312-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="81312-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81312-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81312-131">-WhatIf</span></span>
<span data-ttu-id="81312-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="81312-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="81312-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="81312-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81312-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81312-134">CommonParameters</span></span>
<span data-ttu-id="81312-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="81312-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81312-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="81312-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81312-137">輸入</span><span class="sxs-lookup"><span data-stu-id="81312-137">INPUTS</span></span>

### <span data-ttu-id="81312-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="81312-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

## <span data-ttu-id="81312-139">輸出</span><span class="sxs-lookup"><span data-stu-id="81312-139">OUTPUTS</span></span>

### <span data-ttu-id="81312-140">PSKeyVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="81312-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="81312-141">筆記</span><span class="sxs-lookup"><span data-stu-id="81312-141">NOTES</span></span>

## <span data-ttu-id="81312-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="81312-142">RELATED LINKS</span></span>

[<span data-ttu-id="81312-143">移除-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="81312-143">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)

[<span data-ttu-id="81312-144">新-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="81312-144">New-AzKeyVault</span></span>](./New-AzKeyVault.md)

[<span data-ttu-id="81312-145">AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="81312-145">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)
