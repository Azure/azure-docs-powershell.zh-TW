---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/undo-azkeyvaultmanagedstoragesasdefinitionremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageSasDefinitionRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultManagedStorageSasDefinitionRemoval.md
ms.openlocfilehash: a8f90c2314ad645a8de3a72abc92928759e3b828
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904102"
---
# <span data-ttu-id="36e32-101">Undo-AzKeyVaultManagedStorageSasDefinitionRemoval</span><span class="sxs-lookup"><span data-stu-id="36e32-101">Undo-AzKeyVaultManagedStorageSasDefinitionRemoval</span></span>

## <span data-ttu-id="36e32-102">簡介</span><span class="sxs-lookup"><span data-stu-id="36e32-102">SYNOPSIS</span></span>
<span data-ttu-id="36e32-103">復原先前已刪除的 KeyVault 管理儲存空間 SAS 定義。</span><span class="sxs-lookup"><span data-stu-id="36e32-103">Recovers a previously deleted KeyVault-managed storage SAS definition.</span></span>

## <span data-ttu-id="36e32-104">語法</span><span class="sxs-lookup"><span data-stu-id="36e32-104">SYNTAX</span></span>

### <span data-ttu-id="36e32-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="36e32-105">Default (Default)</span></span>
```
Undo-AzKeyVaultManagedStorageSasDefinitionRemoval [-VaultName] <String> [-AccountName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36e32-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="36e32-106">InputObject</span></span>
```
Undo-AzKeyVaultManagedStorageSasDefinitionRemoval [-AccountName] <String>
 [-InputObject] <PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36e32-107">描述</span><span class="sxs-lookup"><span data-stu-id="36e32-107">DESCRIPTION</span></span>
<span data-ttu-id="36e32-108">復原 **-AzKeyVaultManagedStorageSasDefinitionRemoval** 命令會復原先前已刪除的受管理儲存空間 SAS 定義，但此保存庫必須啟用柔刪除，且復原間隔期間會嘗試復原。</span><span class="sxs-lookup"><span data-stu-id="36e32-108">The **Undo-AzKeyVaultManagedStorageSasDefinitionRemoval** command recovers a previously deleted managed storage SAS definition, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="36e32-109">例子</span><span class="sxs-lookup"><span data-stu-id="36e32-109">EXAMPLES</span></span>

### <span data-ttu-id="36e32-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="36e32-110">Example 1</span></span>
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

<span data-ttu-id="36e32-111">此命令順序會決定指定的儲存空間 SAS 定義是否存在於保存庫中的已刪除狀態;後續命令會復原已刪除的 sas 定義，讓該定義恢復為使用中狀態。</span><span class="sxs-lookup"><span data-stu-id="36e32-111">This sequence of commands determines whether the specified storage SAS definition exists in the vault in a deleted state; the subsequent command recovers the deleted sas definition, bringing it back into an active state.</span></span>

## <span data-ttu-id="36e32-112">參數</span><span class="sxs-lookup"><span data-stu-id="36e32-112">PARAMETERS</span></span>

### <span data-ttu-id="36e32-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="36e32-113">-AccountName</span></span>
<span data-ttu-id="36e32-114">KeyVault 管理的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="36e32-114">KeyVault-managed storage account name.</span></span>
<span data-ttu-id="36e32-115">Cmdlet 會從保存庫名稱、目前選取的環境及受管理的儲存帳戶名稱，建構受管理的儲存空間 SAS 定義的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="36e32-115">Cmdlet constructs the FQDN of a managed storage SAS definition from vault name, currently-selected environment and managed storage account name.</span></span>

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

### <span data-ttu-id="36e32-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36e32-116">-DefaultProfile</span></span>
<span data-ttu-id="36e32-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="36e32-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36e32-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36e32-118">-InputObject</span></span>
<span data-ttu-id="36e32-119">已刪除受管理的儲存空間 SAS 定義物件</span><span class="sxs-lookup"><span data-stu-id="36e32-119">Deleted managed storage SAS definition object</span></span>

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

### <span data-ttu-id="36e32-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="36e32-120">-Name</span></span>
<span data-ttu-id="36e32-121">KeyVault 管理的儲存空間 SAS 定義名稱。</span><span class="sxs-lookup"><span data-stu-id="36e32-121">Name of the KeyVault-managed storage SAS definition.</span></span>
<span data-ttu-id="36e32-122">Cmdlet 會從保存庫名稱、目前選取的環境、受管理儲存帳戶的名稱以及 SAS 定義的名稱建構目標 FQDN。</span><span class="sxs-lookup"><span data-stu-id="36e32-122">Cmdlet constructs the FQDN of the target from vault name, currently-selected environment, the name of the managed storage account and the name of the SAS definition.</span></span>

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

### <span data-ttu-id="36e32-123">-VaultName</span><span class="sxs-lookup"><span data-stu-id="36e32-123">-VaultName</span></span>
<span data-ttu-id="36e32-124">儲存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="36e32-124">Vault name.</span></span>
<span data-ttu-id="36e32-125">Cmdlet 會根據名稱和目前選取的環境來建構庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="36e32-125">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="36e32-126">-確認</span><span class="sxs-lookup"><span data-stu-id="36e32-126">-Confirm</span></span>
<span data-ttu-id="36e32-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="36e32-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36e32-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36e32-128">-WhatIf</span></span>
<span data-ttu-id="36e32-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="36e32-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36e32-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="36e32-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36e32-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36e32-131">CommonParameters</span></span>
<span data-ttu-id="36e32-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="36e32-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36e32-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36e32-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36e32-134">輸入</span><span class="sxs-lookup"><span data-stu-id="36e32-134">INPUTS</span></span>

### <span data-ttu-id="36e32-135">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="36e32-135">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="36e32-136">輸出</span><span class="sxs-lookup"><span data-stu-id="36e32-136">OUTPUTS</span></span>

### <span data-ttu-id="36e32-137">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="36e32-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="36e32-138">筆記</span><span class="sxs-lookup"><span data-stu-id="36e32-138">NOTES</span></span>

## <span data-ttu-id="36e32-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="36e32-139">RELATED LINKS</span></span>
