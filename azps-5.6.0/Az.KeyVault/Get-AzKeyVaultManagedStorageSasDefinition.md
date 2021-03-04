---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: acb0e2811f184f7c3162635b87849a35ce9156ac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914822"
---
# <span data-ttu-id="28df7-101">Get-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="28df7-101">Get-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="28df7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="28df7-102">SYNOPSIS</span></span>
<span data-ttu-id="28df7-103">獲得金鑰保存庫管理的儲存空間 SAS 定義。</span><span class="sxs-lookup"><span data-stu-id="28df7-103">Gets Key Vault managed Storage SAS Definitions.</span></span>

## <span data-ttu-id="28df7-104">語法</span><span class="sxs-lookup"><span data-stu-id="28df7-104">SYNTAX</span></span>

### <span data-ttu-id="28df7-105">ByDefinitionName (預設) </span><span class="sxs-lookup"><span data-stu-id="28df7-105">ByDefinitionName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [[-Name] <String>]
 [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28df7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="28df7-106">ByInputObject</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-Name] <String>] [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28df7-107">描述</span><span class="sxs-lookup"><span data-stu-id="28df7-107">DESCRIPTION</span></span>
<span data-ttu-id="28df7-108">如果指定定義的名稱，則獲得金鑰保存庫受管理的儲存空間 SAS 定義。</span><span class="sxs-lookup"><span data-stu-id="28df7-108">Gets a Key Vault managed Storage SAS Definition if the name of the definition is specified.</span></span> <span data-ttu-id="28df7-109">如果未指定定義名稱，會列出與保存庫中指定之金鑰保存庫受管理儲存帳戶相關聯的所有 SAS 定義。</span><span class="sxs-lookup"><span data-stu-id="28df7-109">If the definition name is not specified, then all the SAS definitions associated with the specified Key Vault managed Storage Account in the vault are listed.</span></span>

## <span data-ttu-id="28df7-110">例子</span><span class="sxs-lookup"><span data-stu-id="28df7-110">EXAMPLES</span></span>

### <span data-ttu-id="28df7-111">範例 1：列出所有金鑰保存庫受管理的儲存空間 SAS 定義</span><span class="sxs-lookup"><span data-stu-id="28df7-111">Example 1: List all Key Vault managed Storage SAS Definitions</span></span>
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

<span data-ttu-id="28df7-112">列出與金鑰保存庫管理的儲存帳戶 "mystorageaccount" 由保存庫 "myvault" 管理的所有 SAS 定義</span><span class="sxs-lookup"><span data-stu-id="28df7-112">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'</span></span>

### <span data-ttu-id="28df7-113">範例 2：取得金鑰保存庫管理的儲存帳戶</span><span class="sxs-lookup"><span data-stu-id="28df7-113">Example 2: Get a Key Vault managed Storage Account</span></span>
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

<span data-ttu-id="28df7-114">獲得由保存庫 "myvault" 管理之金鑰保存庫管理的儲存帳戶 'mystorageaccount' 相關聯的 SAS 定義 'accountas' 詳細資料。</span><span class="sxs-lookup"><span data-stu-id="28df7-114">Gets the details of SAS Definition 'accountsas' associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'.</span></span>

### <span data-ttu-id="28df7-115">範例 3：使用篩選列出所有金鑰保存庫受管理的儲存空間 SAS 定義</span><span class="sxs-lookup"><span data-stu-id="28df7-115">Example 3: List all Key Vault managed Storage SAS Definitions using filtering</span></span>
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

<span data-ttu-id="28df7-116">列出與金鑰保存庫管理的儲存帳戶「mystorageaccount」相關聯的所有 SAS 定義，這些帳戶是由保存庫「myvault」所管理，以「帳戶」做為開始。</span><span class="sxs-lookup"><span data-stu-id="28df7-116">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault' that start with "account".</span></span>

## <span data-ttu-id="28df7-117">參數</span><span class="sxs-lookup"><span data-stu-id="28df7-117">PARAMETERS</span></span>

### <span data-ttu-id="28df7-118">-AccountName</span><span class="sxs-lookup"><span data-stu-id="28df7-118">-AccountName</span></span>
<span data-ttu-id="28df7-119">儲存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="28df7-119">Vault name.</span></span>
<span data-ttu-id="28df7-120">Cmdlet 會根據名稱和目前選取的環境來建構庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="28df7-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="28df7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28df7-121">-DefaultProfile</span></span>
<span data-ttu-id="28df7-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="28df7-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="28df7-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28df7-123">-InputObject</span></span>
<span data-ttu-id="28df7-124">ManagedStorageAccount 物件。</span><span class="sxs-lookup"><span data-stu-id="28df7-124">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="28df7-125">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="28df7-125">-InRemovedState</span></span>
<span data-ttu-id="28df7-126">指定是否要在輸出中顯示先前刪除的儲存空間 sas 定義。</span><span class="sxs-lookup"><span data-stu-id="28df7-126">Specifies whether to show the previously deleted storage sas definitions in the output.</span></span>

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

### <span data-ttu-id="28df7-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="28df7-127">-Name</span></span>
<span data-ttu-id="28df7-128">儲存空間 sas 定義名稱。</span><span class="sxs-lookup"><span data-stu-id="28df7-128">Storage sas definition name.</span></span>
<span data-ttu-id="28df7-129">Cmdlet 會從保存庫名稱、目前選取的環境、儲存帳戶名稱和 sas 定義名稱建構儲存空間 sas 定義的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="28df7-129">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

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

### <span data-ttu-id="28df7-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="28df7-130">-VaultName</span></span>
<span data-ttu-id="28df7-131">儲存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="28df7-131">Vault name.</span></span>
<span data-ttu-id="28df7-132">Cmdlet 會根據名稱和目前選取的環境來建構庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="28df7-132">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="28df7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28df7-133">CommonParameters</span></span>
<span data-ttu-id="28df7-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="28df7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28df7-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="28df7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28df7-136">輸入</span><span class="sxs-lookup"><span data-stu-id="28df7-136">INPUTS</span></span>

### <span data-ttu-id="28df7-137">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="28df7-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="28df7-138">輸出</span><span class="sxs-lookup"><span data-stu-id="28df7-138">OUTPUTS</span></span>

### <span data-ttu-id="28df7-139">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="28df7-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

### <span data-ttu-id="28df7-140">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="28df7-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

### <span data-ttu-id="28df7-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="28df7-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span></span>

### <span data-ttu-id="28df7-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="28df7-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="28df7-143">筆記</span><span class="sxs-lookup"><span data-stu-id="28df7-143">NOTES</span></span>

## <span data-ttu-id="28df7-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="28df7-144">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

