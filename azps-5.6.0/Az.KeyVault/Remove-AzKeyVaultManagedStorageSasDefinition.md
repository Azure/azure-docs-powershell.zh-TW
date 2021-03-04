---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 844802c01b9b3bff7f59b795d5ba7712b9a7f4c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917722"
---
# <span data-ttu-id="d1aba-101">Remove-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="d1aba-101">Remove-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="d1aba-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d1aba-102">SYNOPSIS</span></span>
<span data-ttu-id="d1aba-103">移除金鑰保存庫管理的 Azure 儲存體 SAS 定義。</span><span class="sxs-lookup"><span data-stu-id="d1aba-103">Removes a Key Vault managed Azure Storage SAS definitions.</span></span>

## <span data-ttu-id="d1aba-104">語法</span><span class="sxs-lookup"><span data-stu-id="d1aba-104">SYNTAX</span></span>

### <span data-ttu-id="d1aba-105">ByDefinitionName (預設) </span><span class="sxs-lookup"><span data-stu-id="d1aba-105">ByDefinitionName (Default)</span></span>
```
Remove-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1aba-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d1aba-106">ByInputObject</span></span>
```
Remove-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageSasDefinitionIdentityItem>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1aba-107">描述</span><span class="sxs-lookup"><span data-stu-id="d1aba-107">DESCRIPTION</span></span>
<span data-ttu-id="d1aba-108">移除金鑰保存庫管理的 Azure 儲存體 SAS 定義。</span><span class="sxs-lookup"><span data-stu-id="d1aba-108">Removes a Key Vault managed Azure Storage SAS definitions.</span></span> <span data-ttu-id="d1aba-109">這也會移除用來根據此 SAS 定義取得 SAS 權杖的秘訣。</span><span class="sxs-lookup"><span data-stu-id="d1aba-109">This also removes the secret used to get the SAS token per this SAS definition.</span></span>

## <span data-ttu-id="d1aba-110">例子</span><span class="sxs-lookup"><span data-stu-id="d1aba-110">EXAMPLES</span></span>

### <span data-ttu-id="d1aba-111">範例 1：移除金鑰保存庫管理的 Azure 儲存體 SAS 定義。</span><span class="sxs-lookup"><span data-stu-id="d1aba-111">Example 1: Remove a Key Vault managed Azure Storage SAS definition.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -PassThru

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/mysasdef
Vault Name  : myvault
AccountName : mystorageaccount
Name        : mysasdef
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="d1aba-112">移除與保存庫 'myvault' 中帳戶 'mystorageaccount' 相關聯的金鑰保存庫受管理的儲存空間 SAS 定義 'mysasdef'。</span><span class="sxs-lookup"><span data-stu-id="d1aba-112">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

### <span data-ttu-id="d1aba-113">範例 2：移除金鑰保存庫管理的 Azure 儲存體 SAS 定義，而不讓使用者確認。</span><span class="sxs-lookup"><span data-stu-id="d1aba-113">Example 2: Remove a Key Vault managed Azure Storage SAS definition without user confirmation.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -PassThru -Force

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/mysasdef
Vault Name  : myvault
AccountName : mystorageaccount
Name        : mysasdef
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="d1aba-114">移除與保存庫 'myvault' 中帳戶 'mystorageaccount' 相關聯的金鑰保存庫受管理的儲存空間 SAS 定義 'mysasdef'。</span><span class="sxs-lookup"><span data-stu-id="d1aba-114">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

## <span data-ttu-id="d1aba-115">參數</span><span class="sxs-lookup"><span data-stu-id="d1aba-115">PARAMETERS</span></span>

### <span data-ttu-id="d1aba-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d1aba-116">-AccountName</span></span>
<span data-ttu-id="d1aba-117">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="d1aba-117">Storage account name.</span></span>
<span data-ttu-id="d1aba-118">Cmdlet 會從保存庫名稱、目前選取的環境和儲存帳戶名稱建構受管理儲存帳戶名稱的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="d1aba-118">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1aba-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1aba-119">-DefaultProfile</span></span>
<span data-ttu-id="d1aba-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="d1aba-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d1aba-121">-強制</span><span class="sxs-lookup"><span data-stu-id="d1aba-121">-Force</span></span>
<span data-ttu-id="d1aba-122">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="d1aba-122">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1aba-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1aba-123">-InputObject</span></span>
<span data-ttu-id="d1aba-124">ManagedStorageSasDefinition 物件。</span><span class="sxs-lookup"><span data-stu-id="d1aba-124">ManagedStorageSasDefinition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1aba-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="d1aba-125">-Name</span></span>
<span data-ttu-id="d1aba-126">儲存空間 sas 定義名稱。</span><span class="sxs-lookup"><span data-stu-id="d1aba-126">Storage sas definition name.</span></span>
<span data-ttu-id="d1aba-127">Cmdlet 會從保存庫名稱、目前選取的環境、儲存帳戶名稱和 sas 定義名稱建構儲存空間 sas 定義的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="d1aba-127">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1aba-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1aba-128">-PassThru</span></span>
<span data-ttu-id="d1aba-129">Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="d1aba-129">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="d1aba-130">如果指定此參數，Cmdlet 會返回已刪除的受管理儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="d1aba-130">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1aba-131">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d1aba-131">-VaultName</span></span>
<span data-ttu-id="d1aba-132">儲存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="d1aba-132">Vault name.</span></span>
<span data-ttu-id="d1aba-133">Cmdlet 會根據名稱和目前選取的環境來建構庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="d1aba-133">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1aba-134">-確認</span><span class="sxs-lookup"><span data-stu-id="d1aba-134">-Confirm</span></span>
<span data-ttu-id="d1aba-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d1aba-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1aba-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1aba-136">-WhatIf</span></span>
<span data-ttu-id="d1aba-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d1aba-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1aba-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d1aba-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1aba-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1aba-139">CommonParameters</span></span>
<span data-ttu-id="d1aba-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d1aba-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1aba-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d1aba-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1aba-142">輸入</span><span class="sxs-lookup"><span data-stu-id="d1aba-142">INPUTS</span></span>

### <span data-ttu-id="d1aba-143">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="d1aba-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="d1aba-144">輸出</span><span class="sxs-lookup"><span data-stu-id="d1aba-144">OUTPUTS</span></span>

### <span data-ttu-id="d1aba-145">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="d1aba-145">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="d1aba-146">筆記</span><span class="sxs-lookup"><span data-stu-id="d1aba-146">NOTES</span></span>

## <span data-ttu-id="d1aba-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="d1aba-147">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

