---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 9859c6f17f393a5ca691c34e3ee144e24ab59fa8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624303"
---
# <span data-ttu-id="0ddd7-101">Remove-AzureKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="0ddd7-101">Remove-AzureKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="0ddd7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0ddd7-102">SYNOPSIS</span></span>
<span data-ttu-id="0ddd7-103">移除金鑰保存庫管理的 Azure 儲存體 SAS 定義。</span><span class="sxs-lookup"><span data-stu-id="0ddd7-103">Removes a Key Vault managed Azure Storage SAS definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ddd7-104">句法</span><span class="sxs-lookup"><span data-stu-id="0ddd7-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ddd7-105">說明</span><span class="sxs-lookup"><span data-stu-id="0ddd7-105">DESCRIPTION</span></span>
<span data-ttu-id="0ddd7-106">移除金鑰保存庫管理的 Azure 儲存體 SAS 定義。</span><span class="sxs-lookup"><span data-stu-id="0ddd7-106">Removes a Key Vault managed Azure Storage SAS definitions.</span></span> <span data-ttu-id="0ddd7-107">這也會移除用於根據此 SAS 定義取得 SAS 權杖的機密。</span><span class="sxs-lookup"><span data-stu-id="0ddd7-107">This also removes the secret used to get the SAS token per this SAS definition.</span></span>

## <span data-ttu-id="0ddd7-108">示例</span><span class="sxs-lookup"><span data-stu-id="0ddd7-108">EXAMPLES</span></span>

### <span data-ttu-id="0ddd7-109">範例1：移除主要電子倉庫管理的 Azure 儲存區 SAS 定義。</span><span class="sxs-lookup"><span data-stu-id="0ddd7-109">Example 1: Remove a Key Vault managed Azure Storage SAS definition.</span></span>
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef'
```

<span data-ttu-id="0ddd7-110">移除與保存庫 "myvault" 中的帳戶 "mystorageaccount" 相關聯的主要保存庫管理的儲存 SAS 定義 "mysasdef"。</span><span class="sxs-lookup"><span data-stu-id="0ddd7-110">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

### <span data-ttu-id="0ddd7-111">範例2：移除主要電子倉庫管理的 Azure 儲存體 SAS 定義，不需使用者確認。</span><span class="sxs-lookup"><span data-stu-id="0ddd7-111">Example 2: Remove a Key Vault managed Azure Storage SAS definition without user confirmation.</span></span>
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -Force -Confirm:$False
```

<span data-ttu-id="0ddd7-112">移除與保存庫 "myvault" 中的帳戶 "mystorageaccount" 相關聯的主要保存庫管理的儲存 SAS 定義 "mysasdef"。</span><span class="sxs-lookup"><span data-stu-id="0ddd7-112">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

## <span data-ttu-id="0ddd7-113">參數</span><span class="sxs-lookup"><span data-stu-id="0ddd7-113">PARAMETERS</span></span>

### <span data-ttu-id="0ddd7-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0ddd7-114">-AccountName</span></span>
<span data-ttu-id="0ddd7-115">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="0ddd7-115">Storage account name.</span></span>
<span data-ttu-id="0ddd7-116">Cmdlet 會從保存庫名稱、目前已選取的環境和儲存空間帳戶名稱構造受管理儲存空間帳戶名稱的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="0ddd7-116">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ddd7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ddd7-117">-DefaultProfile</span></span>
<span data-ttu-id="0ddd7-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="0ddd7-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ddd7-119">-Force</span><span class="sxs-lookup"><span data-stu-id="0ddd7-119">-Force</span></span>
<span data-ttu-id="0ddd7-120">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="0ddd7-120">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ddd7-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="0ddd7-121">-Name</span></span>
<span data-ttu-id="0ddd7-122">儲存區 sas 定義名稱。</span><span class="sxs-lookup"><span data-stu-id="0ddd7-122">Storage sas definition name.</span></span>
<span data-ttu-id="0ddd7-123">Cmdlet 會從保存庫名稱、目前所選的環境、儲存空間帳戶名稱和 sas 定義名稱來構造儲存 sas 定義的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="0ddd7-123">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ddd7-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0ddd7-124">-PassThru</span></span>
<span data-ttu-id="0ddd7-125">Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="0ddd7-125">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="0ddd7-126">如果指定此開關，則 Cmdlet 會傳回已刪除的受管理儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="0ddd7-126">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ddd7-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="0ddd7-127">-VaultName</span></span>
<span data-ttu-id="0ddd7-128">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="0ddd7-128">Vault name.</span></span>
<span data-ttu-id="0ddd7-129">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="0ddd7-129">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ddd7-130">-確認</span><span class="sxs-lookup"><span data-stu-id="0ddd7-130">-Confirm</span></span>
<span data-ttu-id="0ddd7-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0ddd7-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ddd7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ddd7-132">-WhatIf</span></span>
<span data-ttu-id="0ddd7-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0ddd7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ddd7-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0ddd7-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ddd7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ddd7-135">CommonParameters</span></span>
<span data-ttu-id="0ddd7-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0ddd7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ddd7-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0ddd7-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ddd7-138">輸入</span><span class="sxs-lookup"><span data-stu-id="0ddd7-138">INPUTS</span></span>

### <span data-ttu-id="0ddd7-139">System.object</span><span class="sxs-lookup"><span data-stu-id="0ddd7-139">System.String</span></span>

## <span data-ttu-id="0ddd7-140">輸出</span><span class="sxs-lookup"><span data-stu-id="0ddd7-140">OUTPUTS</span></span>

### <span data-ttu-id="0ddd7-141">ManagedStorageSasDefinition 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="0ddd7-141">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinition</span></span>

## <span data-ttu-id="0ddd7-142">筆記</span><span class="sxs-lookup"><span data-stu-id="0ddd7-142">NOTES</span></span>

## <span data-ttu-id="0ddd7-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="0ddd7-143">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

