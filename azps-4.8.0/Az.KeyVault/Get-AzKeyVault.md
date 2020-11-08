---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
ms.openlocfilehash: cb1c4f901c598ec20af13e87707966704b285c64
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969672"
---
# <span data-ttu-id="8d3ab-101">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="8d3ab-101">Get-AzKeyVault</span></span>

## <span data-ttu-id="8d3ab-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8d3ab-102">SYNOPSIS</span></span>
<span data-ttu-id="8d3ab-103">取得金鑰電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="8d3ab-103">Gets key vaults.</span></span>

## <span data-ttu-id="8d3ab-104">句法</span><span class="sxs-lookup"><span data-stu-id="8d3ab-104">SYNTAX</span></span>

### <span data-ttu-id="8d3ab-105">GetVaultByName (預設) </span><span class="sxs-lookup"><span data-stu-id="8d3ab-105">GetVaultByName (Default)</span></span>
```
Get-AzKeyVault [[-VaultName] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d3ab-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="8d3ab-106">ByDeletedVault</span></span>
```
Get-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d3ab-107">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="8d3ab-107">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d3ab-108">說明</span><span class="sxs-lookup"><span data-stu-id="8d3ab-108">DESCRIPTION</span></span>
<span data-ttu-id="8d3ab-109">**AzKeyVault** Cmdlet 會取得訂閱中主要電子倉庫的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8d3ab-109">The **Get-AzKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="8d3ab-110">您可以查看訂閱中的所有主要電子倉庫實例，或依據資源群組或特定的金鑰電子倉庫來篩選結果。</span><span class="sxs-lookup"><span data-stu-id="8d3ab-110">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>
<span data-ttu-id="8d3ab-111">請注意，雖然在您取得單一金鑰 vault 時，可以為這個 Cmdlet 指定 [資源群組]，但您應該這麼做，以取得較佳的效能。</span><span class="sxs-lookup"><span data-stu-id="8d3ab-111">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="8d3ab-112">示例</span><span class="sxs-lookup"><span data-stu-id="8d3ab-112">EXAMPLES</span></span>

### <span data-ttu-id="8d3ab-113">範例1：取得目前訂閱中的所有主要電子倉庫</span><span class="sxs-lookup"><span data-stu-id="8d3ab-113">Example 1: Get all key vaults in your current subscription</span></span>
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

<span data-ttu-id="8d3ab-114">這個命令會在您目前的訂閱中取得所有的主要電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="8d3ab-114">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="8d3ab-115">範例2：取得特定的金鑰電子倉庫</span><span class="sxs-lookup"><span data-stu-id="8d3ab-115">Example 2: Get a specific key vault</span></span>
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

<span data-ttu-id="8d3ab-116">這個命令會在您目前的訂閱中取得名為 myvault 的金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="8d3ab-116">This command gets the key vault named myvault in your current subscription.</span></span>

### <span data-ttu-id="8d3ab-117">範例3：在資源群組中取得金鑰電子倉庫</span><span class="sxs-lookup"><span data-stu-id="8d3ab-117">Example 3: Get key vaults in a resource group</span></span>
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

<span data-ttu-id="8d3ab-118">這個命令會取得名為 ContosoPayRollResourceGroup 的資源群組中的所有主要電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="8d3ab-118">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="8d3ab-119">範例4：在您目前的訂閱中取得所有已刪除的金鑰電子倉庫</span><span class="sxs-lookup"><span data-stu-id="8d3ab-119">Example 4: Get all deleted key vaults in your current subscription</span></span>
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

<span data-ttu-id="8d3ab-120">這個命令會在您目前的訂閱中取得所有已刪除的金鑰電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="8d3ab-120">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="8d3ab-121">範例5：取得刪除的主要電子倉庫</span><span class="sxs-lookup"><span data-stu-id="8d3ab-121">Example 5: Get a deleted key vault</span></span>
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

<span data-ttu-id="8d3ab-122">這個命令會在您目前的訂閱和 westus 區域中取得名為 myvault4 的已刪除主要電子倉庫資訊。</span><span class="sxs-lookup"><span data-stu-id="8d3ab-122">This command gets the deleted key vault information named myvault4 in your current subscription and in westus region.</span></span>

### <span data-ttu-id="8d3ab-123">範例6：使用篩選來取得金鑰電子倉庫</span><span class="sxs-lookup"><span data-stu-id="8d3ab-123">Example 6: Get key vaults using filtering</span></span>
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

<span data-ttu-id="8d3ab-124">這個命令會取得訂閱中以 "myvault" 為開頭的所有主要電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="8d3ab-124">This command gets all the key vaults in the subscription that start with "myvault".</span></span>

## <span data-ttu-id="8d3ab-125">參數</span><span class="sxs-lookup"><span data-stu-id="8d3ab-125">PARAMETERS</span></span>

### <span data-ttu-id="8d3ab-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d3ab-126">-DefaultProfile</span></span>
<span data-ttu-id="8d3ab-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="8d3ab-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8d3ab-128">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="8d3ab-128">-InRemovedState</span></span>
<span data-ttu-id="8d3ab-129">指定是否要在輸出中顯示先前刪除的電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="8d3ab-129">Specifies whether to show the previously deleted vaults in the output.</span></span>

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

### <span data-ttu-id="8d3ab-130">-位置</span><span class="sxs-lookup"><span data-stu-id="8d3ab-130">-Location</span></span>
<span data-ttu-id="8d3ab-131">已刪除的電子倉庫的位置。</span><span class="sxs-lookup"><span data-stu-id="8d3ab-131">The location of the deleted vault.</span></span>

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

### <span data-ttu-id="8d3ab-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d3ab-132">-ResourceGroupName</span></span>
<span data-ttu-id="8d3ab-133">指定與要查詢之主要電子倉庫或主要電子倉庫相關聯之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d3ab-133">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d3ab-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="8d3ab-134">-Tag</span></span>
<span data-ttu-id="8d3ab-135">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="8d3ab-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8d3ab-136">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="8d3ab-136">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8d3ab-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8d3ab-137">-VaultName</span></span>
<span data-ttu-id="8d3ab-138">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d3ab-138">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d3ab-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d3ab-139">CommonParameters</span></span>
<span data-ttu-id="8d3ab-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8d3ab-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d3ab-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8d3ab-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d3ab-142">輸入</span><span class="sxs-lookup"><span data-stu-id="8d3ab-142">INPUTS</span></span>

### <span data-ttu-id="8d3ab-143">System.object</span><span class="sxs-lookup"><span data-stu-id="8d3ab-143">System.String</span></span>

### <span data-ttu-id="8d3ab-144">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8d3ab-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8d3ab-145">輸出</span><span class="sxs-lookup"><span data-stu-id="8d3ab-145">OUTPUTS</span></span>

### <span data-ttu-id="8d3ab-146">PSKeyVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="8d3ab-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="8d3ab-147">PSKeyVaultIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="8d3ab-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="8d3ab-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="8d3ab-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

## <span data-ttu-id="8d3ab-149">筆記</span><span class="sxs-lookup"><span data-stu-id="8d3ab-149">NOTES</span></span>

## <span data-ttu-id="8d3ab-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="8d3ab-150">RELATED LINKS</span></span>

[<span data-ttu-id="8d3ab-151">新-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="8d3ab-151">New-AzKeyVault</span></span>](./New-AzKeyVault.md)

[<span data-ttu-id="8d3ab-152">移除-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="8d3ab-152">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)