---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultmanagedstorageaccountremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultManagedStorageAccountRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultManagedStorageAccountRemoval.md
ms.openlocfilehash: a8e8bb9a4a006c30275f1de959181ad640a04f88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626095"
---
# <span data-ttu-id="e9447-101">Undo-AzureKeyVaultManagedStorageAccountRemoval</span><span class="sxs-lookup"><span data-stu-id="e9447-101">Undo-AzureKeyVaultManagedStorageAccountRemoval</span></span>

## <span data-ttu-id="e9447-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e9447-102">SYNOPSIS</span></span>
<span data-ttu-id="e9447-103">恢復先前刪除的 KeyVault 管理儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="e9447-103">Recovers a previously deleted KeyVault-managed storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9447-104">句法</span><span class="sxs-lookup"><span data-stu-id="e9447-104">SYNTAX</span></span>

### <span data-ttu-id="e9447-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="e9447-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultManagedStorageAccountRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9447-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="e9447-106">InputObject</span></span>
```
Undo-AzureKeyVaultManagedStorageAccountRemoval
 [-InputObject] <PSDeletedKeyVaultManagedStorageAccountIdentityItem> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9447-107">說明</span><span class="sxs-lookup"><span data-stu-id="e9447-107">DESCRIPTION</span></span>
<span data-ttu-id="e9447-108">**復原-AzureKeyVaultManagedStorageAccountRemoval** 命令會復原先前刪除的受管理儲存空間帳戶，但前提是已針對此保存庫啟用 [虛刪除]，且在恢復時間間隔期間嘗試進行復原。</span><span class="sxs-lookup"><span data-stu-id="e9447-108">The **Undo-AzureKeyVaultManagedStorageAccountRemoval** command recovers a previously deleted managed storage account, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="e9447-109">示例</span><span class="sxs-lookup"><span data-stu-id="e9447-109">EXAMPLES</span></span>

### <span data-ttu-id="e9447-110">範例1</span><span class="sxs-lookup"><span data-stu-id="e9447-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName myVault -Name myAccount -InRemovedState
PS C:\> Undo-AzureKeyVaultManagedStorageAccountRemoval -VaultName myVault -Name myAccount

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

<span data-ttu-id="e9447-111">這個命令順序會判斷保存庫中是否存在已刪除狀態的指定儲存空間帳戶;後續命令會復原已刪除的儲存空間帳戶，使其回到作用中狀態。</span><span class="sxs-lookup"><span data-stu-id="e9447-111">This sequence of commands determines whether the specified storage account exists in the vault in a deleted state; the subsequent command recovers the deleted storage account, bringing it back into an active state.</span></span>

## <span data-ttu-id="e9447-112">參數</span><span class="sxs-lookup"><span data-stu-id="e9447-112">PARAMETERS</span></span>

### <span data-ttu-id="e9447-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9447-113">-DefaultProfile</span></span>
<span data-ttu-id="e9447-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e9447-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9447-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9447-115">-InputObject</span></span>
<span data-ttu-id="e9447-116">已刪除的受管理儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="e9447-116">Deleted Managed Storage Account object</span></span>

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

### <span data-ttu-id="e9447-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="e9447-117">-Name</span></span>
<span data-ttu-id="e9447-118">KeyVault 受管理儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="e9447-118">Name of the KeyVault managed storage account.</span></span>
<span data-ttu-id="e9447-119">Cmdlet 會從保存庫名稱、目前所選的環境和受管理的儲存空間帳戶名稱構造目標的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="e9447-119">Cmdlet constructs the FQDN of the target from vault name, currently selected environment and the name of the managed storage account.</span></span>

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

### <span data-ttu-id="e9447-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e9447-120">-VaultName</span></span>
<span data-ttu-id="e9447-121">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="e9447-121">Vault name.</span></span>
<span data-ttu-id="e9447-122">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="e9447-122">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="e9447-123">-確認</span><span class="sxs-lookup"><span data-stu-id="e9447-123">-Confirm</span></span>
<span data-ttu-id="e9447-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e9447-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9447-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9447-125">-WhatIf</span></span>
<span data-ttu-id="e9447-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e9447-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9447-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e9447-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9447-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9447-128">CommonParameters</span></span>
<span data-ttu-id="e9447-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e9447-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9447-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e9447-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9447-131">輸入</span><span class="sxs-lookup"><span data-stu-id="e9447-131">INPUTS</span></span>

### <span data-ttu-id="e9447-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="e9447-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>
<span data-ttu-id="e9447-133">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="e9447-133">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="e9447-134">輸出</span><span class="sxs-lookup"><span data-stu-id="e9447-134">OUTPUTS</span></span>

### <span data-ttu-id="e9447-135">PSKeyVaultManagedStorageAccount 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="e9447-135">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="e9447-136">筆記</span><span class="sxs-lookup"><span data-stu-id="e9447-136">NOTES</span></span>

## <span data-ttu-id="e9447-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="e9447-137">RELATED LINKS</span></span>
