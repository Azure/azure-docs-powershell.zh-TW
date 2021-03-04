---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
ms.openlocfilehash: 84148d675b5c6bc43a883ecd5c419b5019de49d6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917173"
---
# <span data-ttu-id="15df3-101">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="15df3-101">Get-AzKeyVault</span></span>

## <span data-ttu-id="15df3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="15df3-102">SYNOPSIS</span></span>
<span data-ttu-id="15df3-103">獲得金鑰庫。</span><span class="sxs-lookup"><span data-stu-id="15df3-103">Gets key vaults.</span></span>

## <span data-ttu-id="15df3-104">語法</span><span class="sxs-lookup"><span data-stu-id="15df3-104">SYNTAX</span></span>

### <span data-ttu-id="15df3-105">GetVaultByName (預設) </span><span class="sxs-lookup"><span data-stu-id="15df3-105">GetVaultByName (Default)</span></span>
```
Get-AzKeyVault [[-VaultName] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15df3-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="15df3-106">ByDeletedVault</span></span>
```
Get-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15df3-107">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="15df3-107">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15df3-108">描述</span><span class="sxs-lookup"><span data-stu-id="15df3-108">DESCRIPTION</span></span>
<span data-ttu-id="15df3-109">**Get-AzKeyVault** Cmdlet 會取得訂閱中金鑰庫的資訊。</span><span class="sxs-lookup"><span data-stu-id="15df3-109">The **Get-AzKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="15df3-110">您可以查看訂閱中所有金鑰庫實例，或根據資源群組或特定金鑰庫篩選結果。</span><span class="sxs-lookup"><span data-stu-id="15df3-110">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>
<span data-ttu-id="15df3-111">請注意，雖然當您取得單一金鑰庫時，此 Cmdlet 可選擇性指定資源群組，但您應這麼做以提升績效。</span><span class="sxs-lookup"><span data-stu-id="15df3-111">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="15df3-112">例子</span><span class="sxs-lookup"><span data-stu-id="15df3-112">EXAMPLES</span></span>

### <span data-ttu-id="15df3-113">範例 1：取得目前訂閱的所有金鑰庫</span><span class="sxs-lookup"><span data-stu-id="15df3-113">Example 1: Get all key vaults in your current subscription</span></span>
```powershell
PS C:\> Get-AzKeyVault

Vault Name          : myvault1
Resource Group Name : myrg
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.Ke
                      yVault/vaults/myvault1
Tags                :


Vault Name          : myvault2
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault2
Tags                :

Vault Name          : myvault3
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault3
Tags                :
```

<span data-ttu-id="15df3-114">此命令會獲得您目前訂閱的所有金鑰庫。</span><span class="sxs-lookup"><span data-stu-id="15df3-114">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="15df3-115">範例 2：取得特定的金鑰庫</span><span class="sxs-lookup"><span data-stu-id="15df3-115">Example 2: Get a specific key vault</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName 'myvault'

Vault Name                       : myvault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
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

Tags                             :
```

<span data-ttu-id="15df3-116">此命令會獲得您目前訂閱中名為 myvault 的金鑰庫。</span><span class="sxs-lookup"><span data-stu-id="15df3-116">This command gets the key vault named myvault in your current subscription.</span></span>

### <span data-ttu-id="15df3-117">範例 3：取得資源群組中的金鑰庫</span><span class="sxs-lookup"><span data-stu-id="15df3-117">Example 3: Get key vaults in a resource group</span></span>
```powershell
PS C:\> Get-AzKeyVault -ResourceGroupName 'myrg1'

Vault Name          : myvault2
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault2
Tags                :

Vault Name          : myvault3
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault3
Tags                :
```

<span data-ttu-id="15df3-118">此命令會獲得資源群組中名為 ContosoPayRollResourceGroup 的所有金鑰庫。</span><span class="sxs-lookup"><span data-stu-id="15df3-118">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="15df3-119">範例 4：取得目前訂閱中所有已刪除的金鑰庫</span><span class="sxs-lookup"><span data-stu-id="15df3-119">Example 4: Get all deleted key vaults in your current subscription</span></span>
```powershell
PS C:\> Get-AzKeyVault -InRemovedState

Vault Name           : myvault4
Location             : westus
Id                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/providers/Microsoft.KeyVault/locations/westu
                       s/deletedVaults/myvault4
Resource ID          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.K
                       eyVault/vaults/myvault4
Deletion Date        : 5/24/2018 9:33:24 PM
Scheduled Purge Date : 8/22/2018 9:33:24 PM
Tags                 :
```

<span data-ttu-id="15df3-120">此命令會獲得您目前訂閱中所有已刪除的金鑰庫。</span><span class="sxs-lookup"><span data-stu-id="15df3-120">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="15df3-121">範例 5：取得已刪除的金鑰庫</span><span class="sxs-lookup"><span data-stu-id="15df3-121">Example 5: Get a deleted key vault</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName 'myvault4'  -Location 'westus' -InRemovedState

Vault Name           : myvault4
Location             : westus
Id                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/providers/Microsoft.KeyVault/locations/westu
                       s/deletedVaults/myvault4
Resource ID          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.K
                       eyVault/vaults/myvault4
Deletion Date        : 5/24/2018 9:33:24 PM
Scheduled Purge Date : 8/22/2018 9:33:24 PM
Tags                 :
```

<span data-ttu-id="15df3-122">此命令會獲得您目前訂閱和西部地區名為 myvault4 的已刪除金鑰庫資訊。</span><span class="sxs-lookup"><span data-stu-id="15df3-122">This command gets the deleted key vault information named myvault4 in your current subscription and in westus region.</span></span>

### <span data-ttu-id="15df3-123">範例 6：使用篩選取得金鑰庫</span><span class="sxs-lookup"><span data-stu-id="15df3-123">Example 6: Get key vaults using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName 'myvault*'

Vault Name          : myvault2
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault2
Tags                :

Vault Name          : myvault3
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault3
Tags                :
```

<span data-ttu-id="15df3-124">此命令會獲得訂閱中以 "myvault" 開始的所有金鑰庫。</span><span class="sxs-lookup"><span data-stu-id="15df3-124">This command gets all the key vaults in the subscription that start with "myvault".</span></span>

## <span data-ttu-id="15df3-125">參數</span><span class="sxs-lookup"><span data-stu-id="15df3-125">PARAMETERS</span></span>

### <span data-ttu-id="15df3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15df3-126">-DefaultProfile</span></span>
<span data-ttu-id="15df3-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="15df3-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="15df3-128">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="15df3-128">-InRemovedState</span></span>
<span data-ttu-id="15df3-129">指定是否要在輸出中顯示先前刪除的儲存庫。</span><span class="sxs-lookup"><span data-stu-id="15df3-129">Specifies whether to show the previously deleted vaults in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault, ListAllDeletedVaultsInSubscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15df3-130">-位置</span><span class="sxs-lookup"><span data-stu-id="15df3-130">-Location</span></span>
<span data-ttu-id="15df3-131">已刪除的儲存庫位置。</span><span class="sxs-lookup"><span data-stu-id="15df3-131">The location of the deleted vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15df3-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15df3-132">-ResourceGroupName</span></span>
<span data-ttu-id="15df3-133">指定與要查詢之金鑰庫或索引鍵庫相關聯的資源組名。</span><span class="sxs-lookup"><span data-stu-id="15df3-133">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="15df3-134">-標記</span><span class="sxs-lookup"><span data-stu-id="15df3-134">-Tag</span></span>
<span data-ttu-id="15df3-135">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="15df3-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="15df3-136">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="15df3-136">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: GetVaultByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15df3-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="15df3-137">-VaultName</span></span>
<span data-ttu-id="15df3-138">指定金鑰庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="15df3-138">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="15df3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15df3-139">CommonParameters</span></span>
<span data-ttu-id="15df3-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="15df3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15df3-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="15df3-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15df3-142">輸入</span><span class="sxs-lookup"><span data-stu-id="15df3-142">INPUTS</span></span>

### <span data-ttu-id="15df3-143">System.String</span><span class="sxs-lookup"><span data-stu-id="15df3-143">System.String</span></span>

### <span data-ttu-id="15df3-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="15df3-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="15df3-145">輸出</span><span class="sxs-lookup"><span data-stu-id="15df3-145">OUTPUTS</span></span>

### <span data-ttu-id="15df3-146">Microsoft.Azure.Commands.KeyVault.models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="15df3-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="15df3-147">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="15df3-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="15df3-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="15df3-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

## <span data-ttu-id="15df3-149">筆記</span><span class="sxs-lookup"><span data-stu-id="15df3-149">NOTES</span></span>

## <span data-ttu-id="15df3-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="15df3-150">RELATED LINKS</span></span>

[<span data-ttu-id="15df3-151">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="15df3-151">New-AzKeyVault</span></span>](./New-AzKeyVault.md)

[<span data-ttu-id="15df3-152">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="15df3-152">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
