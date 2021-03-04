---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/undo-azkeyvaultmanagedstorageaccountremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageAccountRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageAccountRemoval.md
ms.openlocfilehash: 289adecd07837134fed9279758cf1142d30183a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916734"
---
# <span data-ttu-id="ce53e-101">Undo-AzKeyVaultManagedStorageAccountRemoval</span><span class="sxs-lookup"><span data-stu-id="ce53e-101">Undo-AzKeyVaultManagedStorageAccountRemoval</span></span>

## <span data-ttu-id="ce53e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ce53e-102">SYNOPSIS</span></span>
<span data-ttu-id="ce53e-103">復原先前已刪除的 KeyVault 管理儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="ce53e-103">Recovers a previously deleted KeyVault-managed storage account.</span></span>

## <span data-ttu-id="ce53e-104">語法</span><span class="sxs-lookup"><span data-stu-id="ce53e-104">SYNTAX</span></span>

### <span data-ttu-id="ce53e-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="ce53e-105">Default (Default)</span></span>
```
Undo-AzKeyVaultManagedStorageAccountRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce53e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ce53e-106">InputObject</span></span>
```
Undo-AzKeyVaultManagedStorageAccountRemoval [-InputObject] <PSDeletedKeyVaultManagedStorageAccountIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce53e-107">描述</span><span class="sxs-lookup"><span data-stu-id="ce53e-107">DESCRIPTION</span></span>
<span data-ttu-id="ce53e-108">復原 **-AzKeyVaultManagedStorageAccountRemoval** 命令會復原先前已刪除的受管理儲存空間帳戶，但此保存庫必須啟用柔刪除，且復原期間會嘗試復原。</span><span class="sxs-lookup"><span data-stu-id="ce53e-108">The **Undo-AzKeyVaultManagedStorageAccountRemoval** command recovers a previously deleted managed storage account, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="ce53e-109">例子</span><span class="sxs-lookup"><span data-stu-id="ce53e-109">EXAMPLES</span></span>

### <span data-ttu-id="ce53e-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="ce53e-110">Example 1</span></span>
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

<span data-ttu-id="ce53e-111">此命令順序會決定指定的儲存空間帳戶是否存在於保存庫中的已刪除狀態;後續的命令會復原已刪除的儲存空間帳戶，讓該帳戶恢復為使用中狀態。</span><span class="sxs-lookup"><span data-stu-id="ce53e-111">This sequence of commands determines whether the specified storage account exists in the vault in a deleted state; the subsequent command recovers the deleted storage account, bringing it back into an active state.</span></span>

## <span data-ttu-id="ce53e-112">參數</span><span class="sxs-lookup"><span data-stu-id="ce53e-112">PARAMETERS</span></span>

### <span data-ttu-id="ce53e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce53e-113">-DefaultProfile</span></span>
<span data-ttu-id="ce53e-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ce53e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce53e-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce53e-115">-InputObject</span></span>
<span data-ttu-id="ce53e-116">已刪除 Managed Storage Account 物件</span><span class="sxs-lookup"><span data-stu-id="ce53e-116">Deleted Managed Storage Account object</span></span>

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

### <span data-ttu-id="ce53e-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="ce53e-117">-Name</span></span>
<span data-ttu-id="ce53e-118">KeyVault 管理儲存帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="ce53e-118">Name of the KeyVault managed storage account.</span></span>
<span data-ttu-id="ce53e-119">Cmdlet 會從保存庫名稱、目前選取的環境及受管理的儲存帳戶名稱建構目標 FQDN。</span><span class="sxs-lookup"><span data-stu-id="ce53e-119">Cmdlet constructs the FQDN of the target from vault name, currently selected environment and the name of the managed storage account.</span></span>

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

### <span data-ttu-id="ce53e-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ce53e-120">-VaultName</span></span>
<span data-ttu-id="ce53e-121">儲存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="ce53e-121">Vault name.</span></span>
<span data-ttu-id="ce53e-122">Cmdlet 會根據名稱和目前選取的環境來建構庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="ce53e-122">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="ce53e-123">-確認</span><span class="sxs-lookup"><span data-stu-id="ce53e-123">-Confirm</span></span>
<span data-ttu-id="ce53e-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ce53e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce53e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce53e-125">-WhatIf</span></span>
<span data-ttu-id="ce53e-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ce53e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce53e-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce53e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce53e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce53e-128">CommonParameters</span></span>
<span data-ttu-id="ce53e-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ce53e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce53e-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ce53e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce53e-131">輸入</span><span class="sxs-lookup"><span data-stu-id="ce53e-131">INPUTS</span></span>

### <span data-ttu-id="ce53e-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="ce53e-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="ce53e-133">輸出</span><span class="sxs-lookup"><span data-stu-id="ce53e-133">OUTPUTS</span></span>

### <span data-ttu-id="ce53e-134">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ce53e-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="ce53e-135">筆記</span><span class="sxs-lookup"><span data-stu-id="ce53e-135">NOTES</span></span>

## <span data-ttu-id="ce53e-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="ce53e-136">RELATED LINKS</span></span>
