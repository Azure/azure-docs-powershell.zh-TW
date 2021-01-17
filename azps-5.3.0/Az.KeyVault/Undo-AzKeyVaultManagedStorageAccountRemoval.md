---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultmanagedstorageaccountremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageAccountRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageAccountRemoval.md
ms.openlocfilehash: 3d854d6b820f6c2e23d99e3397173ec45d5b7697
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449093"
---
# <span data-ttu-id="e9de7-101">Undo-AzKeyVaultManagedStorageAccountRemoval</span><span class="sxs-lookup"><span data-stu-id="e9de7-101">Undo-AzKeyVaultManagedStorageAccountRemoval</span></span>

## <span data-ttu-id="e9de7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e9de7-102">SYNOPSIS</span></span>
<span data-ttu-id="e9de7-103">恢復先前刪除的 KeyVault 管理儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="e9de7-103">Recovers a previously deleted KeyVault-managed storage account.</span></span>

## <span data-ttu-id="e9de7-104">句法</span><span class="sxs-lookup"><span data-stu-id="e9de7-104">SYNTAX</span></span>

### <span data-ttu-id="e9de7-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="e9de7-105">Default (Default)</span></span>
```
Undo-AzKeyVaultManagedStorageAccountRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9de7-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="e9de7-106">InputObject</span></span>
```
Undo-AzKeyVaultManagedStorageAccountRemoval [-InputObject] <PSDeletedKeyVaultManagedStorageAccountIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9de7-107">說明</span><span class="sxs-lookup"><span data-stu-id="e9de7-107">DESCRIPTION</span></span>
<span data-ttu-id="e9de7-108">**復原-AzKeyVaultManagedStorageAccountRemoval** 命令會復原先前刪除的受管理儲存空間帳戶，但前提是已針對此保存庫啟用 [虛刪除]，且在恢復時間間隔期間嘗試進行復原。</span><span class="sxs-lookup"><span data-stu-id="e9de7-108">The **Undo-AzKeyVaultManagedStorageAccountRemoval** command recovers a previously deleted managed storage account, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="e9de7-109">示例</span><span class="sxs-lookup"><span data-stu-id="e9de7-109">EXAMPLES</span></span>

### <span data-ttu-id="e9de7-110">範例1</span><span class="sxs-lookup"><span data-stu-id="e9de7-110">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName myVault -Name myAccount -InRemovedState
PS C:\> Undo-AzKeyVaultManagedStorageAccountRemoval -VaultName myVault -Name myAccount

Id                  : https://myvault.vault.azure.net:443/storage/myaccount
Vault Name          : myVault
AccountName         : myAccount
Account Resource Id : /subscriptions/8bc48661-1801-4b7a-8ca1-6a3cadfb4870/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/myaccount
Active Key Name     : key2
Auto Regenerate Key : False
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="e9de7-111">這個命令順序會判斷保存庫中是否存在已刪除狀態的指定儲存空間帳戶;後續命令會復原已刪除的儲存空間帳戶，使其回到作用中狀態。</span><span class="sxs-lookup"><span data-stu-id="e9de7-111">This sequence of commands determines whether the specified storage account exists in the vault in a deleted state; the subsequent command recovers the deleted storage account, bringing it back into an active state.</span></span>

## <span data-ttu-id="e9de7-112">參數</span><span class="sxs-lookup"><span data-stu-id="e9de7-112">PARAMETERS</span></span>

### <span data-ttu-id="e9de7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9de7-113">-DefaultProfile</span></span>
<span data-ttu-id="e9de7-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e9de7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9de7-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9de7-115">-InputObject</span></span>
<span data-ttu-id="e9de7-116">已刪除的受管理儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="e9de7-116">Deleted Managed Storage Account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9de7-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="e9de7-117">-Name</span></span>
<span data-ttu-id="e9de7-118">KeyVault 受管理儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="e9de7-118">Name of the KeyVault managed storage account.</span></span>
<span data-ttu-id="e9de7-119">Cmdlet 會從保存庫名稱、目前所選的環境和受管理的儲存空間帳戶名稱構造目標的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="e9de7-119">Cmdlet constructs the FQDN of the target from vault name, currently selected environment and the name of the managed storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9de7-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e9de7-120">-VaultName</span></span>
<span data-ttu-id="e9de7-121">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="e9de7-121">Vault name.</span></span>
<span data-ttu-id="e9de7-122">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="e9de7-122">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="e9de7-123">-確認</span><span class="sxs-lookup"><span data-stu-id="e9de7-123">-Confirm</span></span>
<span data-ttu-id="e9de7-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e9de7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9de7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9de7-125">-WhatIf</span></span>
<span data-ttu-id="e9de7-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e9de7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9de7-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e9de7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9de7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9de7-128">CommonParameters</span></span>
<span data-ttu-id="e9de7-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e9de7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9de7-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e9de7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9de7-131">輸入</span><span class="sxs-lookup"><span data-stu-id="e9de7-131">INPUTS</span></span>

### <span data-ttu-id="e9de7-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="e9de7-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="e9de7-133">輸出</span><span class="sxs-lookup"><span data-stu-id="e9de7-133">OUTPUTS</span></span>

### <span data-ttu-id="e9de7-134">PSKeyVaultManagedStorageAccount 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="e9de7-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="e9de7-135">筆記</span><span class="sxs-lookup"><span data-stu-id="e9de7-135">NOTES</span></span>

## <span data-ttu-id="e9de7-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="e9de7-136">RELATED LINKS</span></span>
