---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: ff384b456d6cbaac3fa0c28f01038a60b211dfca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612133"
---
# <span data-ttu-id="fd6ac-101">Get-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="fd6ac-101">Get-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="fd6ac-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fd6ac-102">SYNOPSIS</span></span>
<span data-ttu-id="fd6ac-103">取得主要電子倉庫管理的儲存 SAS 定義。</span><span class="sxs-lookup"><span data-stu-id="fd6ac-103">Gets Key Vault managed Storage SAS Definitions.</span></span>

## <span data-ttu-id="fd6ac-104">句法</span><span class="sxs-lookup"><span data-stu-id="fd6ac-104">SYNTAX</span></span>

### <span data-ttu-id="fd6ac-105">ByDefinitionName (預設) </span><span class="sxs-lookup"><span data-stu-id="fd6ac-105">ByDefinitionName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [[-Name] <String>]
 [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd6ac-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fd6ac-106">ByInputObject</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-Name] <String>] [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd6ac-107">說明</span><span class="sxs-lookup"><span data-stu-id="fd6ac-107">DESCRIPTION</span></span>
<span data-ttu-id="fd6ac-108">如果已指定定義的名稱，則會取得主要 Vault 管理的儲存 SAS 定義。</span><span class="sxs-lookup"><span data-stu-id="fd6ac-108">Gets a Key Vault managed Storage SAS Definition if the name of the definition is specified.</span></span> <span data-ttu-id="fd6ac-109">如果未指定定義名稱，則會列出與保存庫中指定的主要儲存庫管理儲存空間帳戶相關聯的所有 SAS 定義。</span><span class="sxs-lookup"><span data-stu-id="fd6ac-109">If the definition name is not specified, then all the SAS definitions associated with the specified Key Vault managed Storage Account in the vault are listed.</span></span>

## <span data-ttu-id="fd6ac-110">示例</span><span class="sxs-lookup"><span data-stu-id="fd6ac-110">EXAMPLES</span></span>

### <span data-ttu-id="fd6ac-111">範例1：列出所有主要 Vault 管理的儲存 SAS 定義</span><span class="sxs-lookup"><span data-stu-id="fd6ac-111">Example 1: List all Key Vault managed Storage SAS Definitions</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount'

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="fd6ac-112">列出所有與主要 Vault 管理的儲存帳戶 ' mystorageaccount」（由保存庫 ' myvault」所管理）關聯的所有 SAS 定義</span><span class="sxs-lookup"><span data-stu-id="fd6ac-112">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'</span></span>

### <span data-ttu-id="fd6ac-113">範例2：取得重要的 Vault 管理儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="fd6ac-113">Example 2: Get a Key Vault managed Storage Account</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'accountsas'

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas
Secret Id   : https://myvault.vault.azure.net/secrets/mystorageaccount-accountsas
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas
Parameter   :
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="fd6ac-114">取得與主要電子倉庫管理儲存空間帳戶 "mystorageaccount" （由保存庫 ' myvault」所管理）相關聯的 SAS 定義 ' accountsas」的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="fd6ac-114">Gets the details of SAS Definition 'accountsas' associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'.</span></span>

### <span data-ttu-id="fd6ac-115">範例3：使用篩選列出所有主要儲存空間管理的儲存空間 SAS 定義</span><span class="sxs-lookup"><span data-stu-id="fd6ac-115">Example 3: List all Key Vault managed Storage SAS Definitions using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name "account*"

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas1
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas1
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas2
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas2
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="fd6ac-116">列出所有與主要電子倉庫管理的儲存帳戶 ' mystorageaccount」（由以 "Account" 開頭的保存庫 "myvault" 所管理）相關的所有 SAS 定義。</span><span class="sxs-lookup"><span data-stu-id="fd6ac-116">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault' that start with "account".</span></span>

## <span data-ttu-id="fd6ac-117">參數</span><span class="sxs-lookup"><span data-stu-id="fd6ac-117">PARAMETERS</span></span>

### <span data-ttu-id="fd6ac-118">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fd6ac-118">-AccountName</span></span>
<span data-ttu-id="fd6ac-119">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="fd6ac-119">Vault name.</span></span>
<span data-ttu-id="fd6ac-120">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="fd6ac-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="fd6ac-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd6ac-121">-DefaultProfile</span></span>
<span data-ttu-id="fd6ac-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="fd6ac-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd6ac-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd6ac-123">-InputObject</span></span>
<span data-ttu-id="fd6ac-124">ManagedStorageAccount 物件。</span><span class="sxs-lookup"><span data-stu-id="fd6ac-124">ManagedStorageAccount object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd6ac-125">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="fd6ac-125">-InRemovedState</span></span>
<span data-ttu-id="fd6ac-126">指定是否要在輸出中顯示先前刪除的儲存空間 sas 定義。</span><span class="sxs-lookup"><span data-stu-id="fd6ac-126">Specifies whether to show the previously deleted storage sas definitions in the output.</span></span>

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

### <span data-ttu-id="fd6ac-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="fd6ac-127">-Name</span></span>
<span data-ttu-id="fd6ac-128">儲存區 sas 定義名稱。</span><span class="sxs-lookup"><span data-stu-id="fd6ac-128">Storage sas definition name.</span></span>
<span data-ttu-id="fd6ac-129">Cmdlet 會從保存庫名稱、目前所選的環境、儲存空間帳戶名稱和 sas 定義名稱來構造儲存 sas 定義的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="fd6ac-129">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd6ac-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fd6ac-130">-VaultName</span></span>
<span data-ttu-id="fd6ac-131">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="fd6ac-131">Vault name.</span></span>
<span data-ttu-id="fd6ac-132">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="fd6ac-132">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="fd6ac-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd6ac-133">CommonParameters</span></span>
<span data-ttu-id="fd6ac-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fd6ac-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd6ac-135">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fd6ac-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd6ac-136">輸入</span><span class="sxs-lookup"><span data-stu-id="fd6ac-136">INPUTS</span></span>

### <span data-ttu-id="fd6ac-137">PSKeyVaultManagedStorageAccountIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="fd6ac-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="fd6ac-138">輸出</span><span class="sxs-lookup"><span data-stu-id="fd6ac-138">OUTPUTS</span></span>

### <span data-ttu-id="fd6ac-139">PSKeyVaultManagedStorageSasDefinitionIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="fd6ac-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

### <span data-ttu-id="fd6ac-140">PSKeyVaultManagedStorageSasDefinition 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="fd6ac-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

### <span data-ttu-id="fd6ac-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="fd6ac-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span></span>

### <span data-ttu-id="fd6ac-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="fd6ac-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="fd6ac-143">筆記</span><span class="sxs-lookup"><span data-stu-id="fd6ac-143">NOTES</span></span>

## <span data-ttu-id="fd6ac-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="fd6ac-144">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

