---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultmanagedstoragesasdefinitionremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageSasDefinitionRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageSasDefinitionRemoval.md
ms.openlocfilehash: bb44bc8f5e4537691d1e5d5493a29111ceaf42a3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436490"
---
# <span data-ttu-id="c3e9b-101">Undo-AzKeyVaultManagedStorageSasDefinitionRemoval</span><span class="sxs-lookup"><span data-stu-id="c3e9b-101">Undo-AzKeyVaultManagedStorageSasDefinitionRemoval</span></span>

## <span data-ttu-id="c3e9b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c3e9b-102">SYNOPSIS</span></span>
<span data-ttu-id="c3e9b-103">恢復先前刪除的 KeyVault 管理儲存 SAS 定義。</span><span class="sxs-lookup"><span data-stu-id="c3e9b-103">Recovers a previously deleted KeyVault-managed storage SAS definition.</span></span>

## <span data-ttu-id="c3e9b-104">句法</span><span class="sxs-lookup"><span data-stu-id="c3e9b-104">SYNTAX</span></span>

### <span data-ttu-id="c3e9b-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="c3e9b-105">Default (Default)</span></span>
```
Undo-AzKeyVaultManagedStorageSasDefinitionRemoval [-VaultName] <String> [-AccountName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3e9b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c3e9b-106">InputObject</span></span>
```
Undo-AzKeyVaultManagedStorageSasDefinitionRemoval [-AccountName] <String>
 [-InputObject] <PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3e9b-107">說明</span><span class="sxs-lookup"><span data-stu-id="c3e9b-107">DESCRIPTION</span></span>
<span data-ttu-id="c3e9b-108">**復原-AzKeyVaultManagedStorageSasDefinitionRemoval** 命令會復原先前刪除的受管理儲存 SAS 定義，前提是已針對此電子倉庫啟用虛刪除，且在復原間隔期間嘗試進行復原。</span><span class="sxs-lookup"><span data-stu-id="c3e9b-108">The **Undo-AzKeyVaultManagedStorageSasDefinitionRemoval** command recovers a previously deleted managed storage SAS definition, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="c3e9b-109">示例</span><span class="sxs-lookup"><span data-stu-id="c3e9b-109">EXAMPLES</span></span>

### <span data-ttu-id="c3e9b-110">範例1</span><span class="sxs-lookup"><span data-stu-id="c3e9b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName myVault -AccountName myAccount -Name mySasName -InRemovedState
PS C:\> Undo-AzKeyVaultManagedStorageSasDefinitionRemoval -VaultName myVault -AccountName myAccount -Name mySasName

Id          : https://myvault.vault.azure.net:443/storage/myaccount/sas/mysasname
Secret Id   : https://myvault.vault.azure.net/secrets/myaccount-mysasname
Vault Name  : myVault
AccountName : myAccount
Name        : mySasName
Parameter   :
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="c3e9b-111">這個命令順序決定了保存庫中指定的儲存 SAS 定義是否存在於已刪除的狀態;後續命令會復原已刪除的 sas 定義，使其回到作用中狀態。</span><span class="sxs-lookup"><span data-stu-id="c3e9b-111">This sequence of commands determines whether the specified storage SAS definition exists in the vault in a deleted state; the subsequent command recovers the deleted sas definition, bringing it back into an active state.</span></span>

## <span data-ttu-id="c3e9b-112">參數</span><span class="sxs-lookup"><span data-stu-id="c3e9b-112">PARAMETERS</span></span>

### <span data-ttu-id="c3e9b-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c3e9b-113">-AccountName</span></span>
<span data-ttu-id="c3e9b-114">KeyVault 管理的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="c3e9b-114">KeyVault-managed storage account name.</span></span>
<span data-ttu-id="c3e9b-115">Cmdlet 會從保存庫名稱、目前已選取的環境和受管理的儲存空間帳戶名稱構造受管理的儲存 SAS 定義的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="c3e9b-115">Cmdlet constructs the FQDN of a managed storage SAS definition from vault name, currently-selected environment and managed storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e9b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3e9b-116">-DefaultProfile</span></span>
<span data-ttu-id="c3e9b-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c3e9b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3e9b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3e9b-118">-InputObject</span></span>
<span data-ttu-id="c3e9b-119">已刪除的受管理儲存容量 SAS 定義物件</span><span class="sxs-lookup"><span data-stu-id="c3e9b-119">Deleted managed storage SAS definition object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3e9b-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="c3e9b-120">-Name</span></span>
<span data-ttu-id="c3e9b-121">KeyVault 管理的儲存 SAS 定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="c3e9b-121">Name of the KeyVault-managed storage SAS definition.</span></span>
<span data-ttu-id="c3e9b-122">Cmdlet 會從保存庫名稱、目前已選取的環境、受管理的儲存空間帳戶名稱和 SAS 定義的名稱來構造目標的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="c3e9b-122">Cmdlet constructs the FQDN of the target from vault name, currently-selected environment, the name of the managed storage account and the name of the SAS definition.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e9b-123">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c3e9b-123">-VaultName</span></span>
<span data-ttu-id="c3e9b-124">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="c3e9b-124">Vault name.</span></span>
<span data-ttu-id="c3e9b-125">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="c3e9b-125">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="c3e9b-126">-確認</span><span class="sxs-lookup"><span data-stu-id="c3e9b-126">-Confirm</span></span>
<span data-ttu-id="c3e9b-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c3e9b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3e9b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3e9b-128">-WhatIf</span></span>
<span data-ttu-id="c3e9b-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c3e9b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3e9b-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c3e9b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3e9b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3e9b-131">CommonParameters</span></span>
<span data-ttu-id="c3e9b-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c3e9b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3e9b-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c3e9b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3e9b-134">輸入</span><span class="sxs-lookup"><span data-stu-id="c3e9b-134">INPUTS</span></span>

### <span data-ttu-id="c3e9b-135">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="c3e9b-135">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="c3e9b-136">輸出</span><span class="sxs-lookup"><span data-stu-id="c3e9b-136">OUTPUTS</span></span>

### <span data-ttu-id="c3e9b-137">PSKeyVaultManagedStorageSasDefinition 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="c3e9b-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="c3e9b-138">筆記</span><span class="sxs-lookup"><span data-stu-id="c3e9b-138">NOTES</span></span>

## <span data-ttu-id="c3e9b-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="c3e9b-139">RELATED LINKS</span></span>
