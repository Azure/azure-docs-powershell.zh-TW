---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 392c8aa5259419851d3cb85967ddf85afa3c94de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98438175"
---
# <span data-ttu-id="61201-101">Remove-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="61201-101">Remove-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="61201-102">摘要</span><span class="sxs-lookup"><span data-stu-id="61201-102">SYNOPSIS</span></span>
<span data-ttu-id="61201-103">移除金鑰保存庫管理的 Azure 儲存體 SAS 定義。</span><span class="sxs-lookup"><span data-stu-id="61201-103">Removes a Key Vault managed Azure Storage SAS definitions.</span></span>

## <span data-ttu-id="61201-104">句法</span><span class="sxs-lookup"><span data-stu-id="61201-104">SYNTAX</span></span>

### <span data-ttu-id="61201-105">ByDefinitionName (預設) </span><span class="sxs-lookup"><span data-stu-id="61201-105">ByDefinitionName (Default)</span></span>
```
Remove-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61201-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="61201-106">ByInputObject</span></span>
```
Remove-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageSasDefinitionIdentityItem>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61201-107">說明</span><span class="sxs-lookup"><span data-stu-id="61201-107">DESCRIPTION</span></span>
<span data-ttu-id="61201-108">移除金鑰保存庫管理的 Azure 儲存體 SAS 定義。</span><span class="sxs-lookup"><span data-stu-id="61201-108">Removes a Key Vault managed Azure Storage SAS definitions.</span></span> <span data-ttu-id="61201-109">這也會移除用於根據此 SAS 定義取得 SAS 權杖的機密。</span><span class="sxs-lookup"><span data-stu-id="61201-109">This also removes the secret used to get the SAS token per this SAS definition.</span></span>

## <span data-ttu-id="61201-110">示例</span><span class="sxs-lookup"><span data-stu-id="61201-110">EXAMPLES</span></span>

### <span data-ttu-id="61201-111">範例1：移除主要電子倉庫管理的 Azure 儲存區 SAS 定義。</span><span class="sxs-lookup"><span data-stu-id="61201-111">Example 1: Remove a Key Vault managed Azure Storage SAS definition.</span></span>
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

<span data-ttu-id="61201-112">移除與保存庫 "myvault" 中的帳戶 "mystorageaccount" 相關聯的主要保存庫管理的儲存 SAS 定義 "mysasdef"。</span><span class="sxs-lookup"><span data-stu-id="61201-112">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

### <span data-ttu-id="61201-113">範例2：移除主要電子倉庫管理的 Azure 儲存體 SAS 定義，不需使用者確認。</span><span class="sxs-lookup"><span data-stu-id="61201-113">Example 2: Remove a Key Vault managed Azure Storage SAS definition without user confirmation.</span></span>
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

<span data-ttu-id="61201-114">移除與保存庫 "myvault" 中的帳戶 "mystorageaccount" 相關聯的主要保存庫管理的儲存 SAS 定義 "mysasdef"。</span><span class="sxs-lookup"><span data-stu-id="61201-114">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

## <span data-ttu-id="61201-115">參數</span><span class="sxs-lookup"><span data-stu-id="61201-115">PARAMETERS</span></span>

### <span data-ttu-id="61201-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="61201-116">-AccountName</span></span>
<span data-ttu-id="61201-117">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="61201-117">Storage account name.</span></span>
<span data-ttu-id="61201-118">Cmdlet 會從保存庫名稱、目前已選取的環境和儲存空間帳戶名稱構造受管理儲存空間帳戶名稱的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="61201-118">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and storage account name.</span></span>

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

### <span data-ttu-id="61201-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61201-119">-DefaultProfile</span></span>
<span data-ttu-id="61201-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="61201-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61201-121">-Force</span><span class="sxs-lookup"><span data-stu-id="61201-121">-Force</span></span>
<span data-ttu-id="61201-122">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="61201-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="61201-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61201-123">-InputObject</span></span>
<span data-ttu-id="61201-124">ManagedStorageSasDefinition 物件。</span><span class="sxs-lookup"><span data-stu-id="61201-124">ManagedStorageSasDefinition object.</span></span>

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

### <span data-ttu-id="61201-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="61201-125">-Name</span></span>
<span data-ttu-id="61201-126">儲存區 sas 定義名稱。</span><span class="sxs-lookup"><span data-stu-id="61201-126">Storage sas definition name.</span></span>
<span data-ttu-id="61201-127">Cmdlet 會從保存庫名稱、目前所選的環境、儲存空間帳戶名稱和 sas 定義名稱來構造儲存 sas 定義的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="61201-127">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

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

### <span data-ttu-id="61201-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="61201-128">-PassThru</span></span>
<span data-ttu-id="61201-129">Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="61201-129">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="61201-130">如果指定此開關，則 Cmdlet 會傳回已刪除的受管理儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="61201-130">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="61201-131">-VaultName</span><span class="sxs-lookup"><span data-stu-id="61201-131">-VaultName</span></span>
<span data-ttu-id="61201-132">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="61201-132">Vault name.</span></span>
<span data-ttu-id="61201-133">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="61201-133">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="61201-134">-確認</span><span class="sxs-lookup"><span data-stu-id="61201-134">-Confirm</span></span>
<span data-ttu-id="61201-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="61201-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61201-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61201-136">-WhatIf</span></span>
<span data-ttu-id="61201-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="61201-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61201-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="61201-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61201-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61201-139">CommonParameters</span></span>
<span data-ttu-id="61201-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="61201-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61201-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="61201-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61201-142">輸入</span><span class="sxs-lookup"><span data-stu-id="61201-142">INPUTS</span></span>

### <span data-ttu-id="61201-143">PSKeyVaultManagedStorageSasDefinitionIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="61201-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="61201-144">輸出</span><span class="sxs-lookup"><span data-stu-id="61201-144">OUTPUTS</span></span>

### <span data-ttu-id="61201-145">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="61201-145">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="61201-146">筆記</span><span class="sxs-lookup"><span data-stu-id="61201-146">NOTES</span></span>

## <span data-ttu-id="61201-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="61201-147">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

