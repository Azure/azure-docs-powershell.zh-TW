---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: d57f672ef440515e69535503f006e08b4c924646
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794653"
---
# <span data-ttu-id="915fe-101">Remove-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="915fe-101">Remove-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="915fe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="915fe-102">SYNOPSIS</span></span>
<span data-ttu-id="915fe-103">移除主要電子倉庫管理的 Azure 儲存空間帳戶和所有相關的 SAS 定義。</span><span class="sxs-lookup"><span data-stu-id="915fe-103">Removes a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>

## <span data-ttu-id="915fe-104">句法</span><span class="sxs-lookup"><span data-stu-id="915fe-104">SYNTAX</span></span>

```
Remove-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="915fe-105">說明</span><span class="sxs-lookup"><span data-stu-id="915fe-105">DESCRIPTION</span></span>
<span data-ttu-id="915fe-106">解除與 [主要電子倉庫] 的 Azure 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="915fe-106">Disassociates an Azure Storage Account from Key Vault.</span></span> <span data-ttu-id="915fe-107">這不會移除 Azure 儲存空間帳戶，但會將帳戶金鑰從 Azure 金鑰保存庫管理。</span><span class="sxs-lookup"><span data-stu-id="915fe-107">This does not remove an Azure Storage Account but removes the account keys from being managed by Azure Key Vault.</span></span> <span data-ttu-id="915fe-108">同時也會移除所有相關聯的主要電子倉庫管理的儲存 SAS 定義。</span><span class="sxs-lookup"><span data-stu-id="915fe-108">All associated Key Vault managed Storage SAS definitions are also removed.</span></span>

## <span data-ttu-id="915fe-109">示例</span><span class="sxs-lookup"><span data-stu-id="915fe-109">EXAMPLES</span></span>

### <span data-ttu-id="915fe-110">範例1：移除主要電子倉庫管理的 Azure 儲存空間帳戶和所有相關的 SAS 定義。</span><span class="sxs-lookup"><span data-stu-id="915fe-110">Example 1: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>
```
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount'
```

<span data-ttu-id="915fe-111">解除 Azure 儲存空間帳戶 "mystorageaccount" 與主要保存庫「myvault」的對應，並停止金鑰保存庫的管理其金鑰。</span><span class="sxs-lookup"><span data-stu-id="915fe-111">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="915fe-112">將不會移除帳戶 [mystorageaccount]。</span><span class="sxs-lookup"><span data-stu-id="915fe-112">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="915fe-113">將會移除與此帳戶相關聯的所有主要電子倉庫管理的儲存空間 SAS 定義。</span><span class="sxs-lookup"><span data-stu-id="915fe-113">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="915fe-114">範例2：移除主要電子倉庫管理的 Azure 儲存空間帳戶和所有相關的 SAS 定義，而不需使用者確認。</span><span class="sxs-lookup"><span data-stu-id="915fe-114">Example 2: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions without user confirmation.</span></span>
```
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Force -Confirm:$False
```

<span data-ttu-id="915fe-115">解除 Azure 儲存空間帳戶 "mystorageaccount" 與主要保存庫「myvault」的對應，並停止金鑰保存庫的管理其金鑰。</span><span class="sxs-lookup"><span data-stu-id="915fe-115">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="915fe-116">將不會移除帳戶 [mystorageaccount]。</span><span class="sxs-lookup"><span data-stu-id="915fe-116">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="915fe-117">將會移除與此帳戶相關聯的所有主要電子倉庫管理的儲存空間 SAS 定義。</span><span class="sxs-lookup"><span data-stu-id="915fe-117">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

## <span data-ttu-id="915fe-118">參數</span><span class="sxs-lookup"><span data-stu-id="915fe-118">PARAMETERS</span></span>

### <span data-ttu-id="915fe-119">-AccountName</span><span class="sxs-lookup"><span data-stu-id="915fe-119">-AccountName</span></span>
<span data-ttu-id="915fe-120">主要保存庫管理的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="915fe-120">Key Vault managed storage account name.</span></span> <span data-ttu-id="915fe-121">Cmdlet 會從保存庫名稱、目前已選取的環境及 manged 儲存空間帳戶名稱構造受管理儲存空間帳戶名稱的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="915fe-121">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="915fe-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="915fe-122">-DefaultProfile</span></span>
<span data-ttu-id="915fe-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="915fe-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="915fe-124">-Force</span><span class="sxs-lookup"><span data-stu-id="915fe-124">-Force</span></span>
<span data-ttu-id="915fe-125">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="915fe-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="915fe-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="915fe-126">-PassThru</span></span>
<span data-ttu-id="915fe-127">Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="915fe-127">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="915fe-128">如果指定此開關，則 Cmdlet 會傳回已刪除的受管理儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="915fe-128">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="915fe-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="915fe-129">-VaultName</span></span>
<span data-ttu-id="915fe-130">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="915fe-130">Vault name.</span></span>
<span data-ttu-id="915fe-131">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="915fe-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="915fe-132">-確認</span><span class="sxs-lookup"><span data-stu-id="915fe-132">-Confirm</span></span>
<span data-ttu-id="915fe-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="915fe-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="915fe-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="915fe-134">-WhatIf</span></span>
<span data-ttu-id="915fe-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="915fe-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="915fe-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="915fe-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="915fe-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="915fe-137">CommonParameters</span></span>
<span data-ttu-id="915fe-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="915fe-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="915fe-139">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="915fe-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="915fe-140">輸入</span><span class="sxs-lookup"><span data-stu-id="915fe-140">INPUTS</span></span>

### <span data-ttu-id="915fe-141">System.object</span><span class="sxs-lookup"><span data-stu-id="915fe-141">System.String</span></span>

## <span data-ttu-id="915fe-142">輸出</span><span class="sxs-lookup"><span data-stu-id="915fe-142">OUTPUTS</span></span>

### <span data-ttu-id="915fe-143">ManagedStorageAccount 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="915fe-143">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="915fe-144">筆記</span><span class="sxs-lookup"><span data-stu-id="915fe-144">NOTES</span></span>

## <span data-ttu-id="915fe-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="915fe-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

