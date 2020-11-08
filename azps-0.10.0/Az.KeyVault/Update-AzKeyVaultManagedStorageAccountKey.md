---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/update-AzKeyvaultmanagedstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
ms.openlocfilehash: d73e9b02940f98db6734f851219399a2ba6c74a2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795515"
---
# <span data-ttu-id="a2b88-101">Update-AzKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="a2b88-101">Update-AzKeyVaultManagedStorageAccountKey</span></span>

## <span data-ttu-id="a2b88-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a2b88-102">SYNOPSIS</span></span>
<span data-ttu-id="a2b88-103">重新生成主要電子倉庫管理的 Azure 儲存空間帳戶的指定金鑰。</span><span class="sxs-lookup"><span data-stu-id="a2b88-103">Regenerates the specified key of Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="a2b88-104">句法</span><span class="sxs-lookup"><span data-stu-id="a2b88-104">SYNTAX</span></span>

```
Update-AzKeyVaultManagedStorageAccountKey [-VaultName] <String> [-AccountName] <String> [-KeyName] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2b88-105">說明</span><span class="sxs-lookup"><span data-stu-id="a2b88-105">DESCRIPTION</span></span>
<span data-ttu-id="a2b88-106">重新產生主要電子倉庫管理 Azure 儲存空間帳戶的指定金鑰，並將金鑰設定為作用中的金鑰。</span><span class="sxs-lookup"><span data-stu-id="a2b88-106">Regenerates the specified key of Key Vault managed Azure Storage Account and sets the key as the active key.</span></span> <span data-ttu-id="a2b88-107">主要電子倉庫將呼叫 Azure 資源管理員以重新產生金鑰。</span><span class="sxs-lookup"><span data-stu-id="a2b88-107">Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span></span> <span data-ttu-id="a2b88-108">呼叫者必須擁有許可權，才能在指定的 Azure 儲存空間帳戶上重新產生金鑰。</span><span class="sxs-lookup"><span data-stu-id="a2b88-108">The caller must posses permissions to regenerate keys on given Azure Storage Account.</span></span>

## <span data-ttu-id="a2b88-109">示例</span><span class="sxs-lookup"><span data-stu-id="a2b88-109">EXAMPLES</span></span>

### <span data-ttu-id="a2b88-110">範例1：重新產生按鍵</span><span class="sxs-lookup"><span data-stu-id="a2b88-110">Example 1: Regenerate a key</span></span>
```
PS C:\> Update-AzKeyVaultManagedStorageAccountKey -VaultName 'myvault' -AccountName 'mystorageaccount' -KeyName 'key1'
```

<span data-ttu-id="a2b88-111">重新產生帳戶 "mystorageaccount" 的 "key1"，並將 "key1" 設為可用的主要保存庫管理的 Azure 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="a2b88-111">Regenerates 'key1' of account 'mystorageaccount' and sets 'key1' as the active of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="a2b88-112">參數</span><span class="sxs-lookup"><span data-stu-id="a2b88-112">PARAMETERS</span></span>

### <span data-ttu-id="a2b88-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a2b88-113">-AccountName</span></span>
<span data-ttu-id="a2b88-114">主要保存庫管理的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="a2b88-114">Key Vault managed storage account name.</span></span> <span data-ttu-id="a2b88-115">Cmdlet 會從保存庫名稱、目前已選取的環境及 manged 儲存空間帳戶名稱構造受管理儲存空間帳戶名稱的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="a2b88-115">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="a2b88-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2b88-116">-DefaultProfile</span></span>
<span data-ttu-id="a2b88-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a2b88-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a2b88-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a2b88-118">-Force</span></span>
<span data-ttu-id="a2b88-119">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="a2b88-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a2b88-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="a2b88-120">-KeyName</span></span>
<span data-ttu-id="a2b88-121">要重新產生並生效的儲存空間帳戶金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="a2b88-121">Name of storage account key to regenerate and make active.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2b88-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a2b88-122">-PassThru</span></span>
<span data-ttu-id="a2b88-123">Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="a2b88-123">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="a2b88-124">如果指定此開關，則 Cmdlet 會傳回已刪除的受管理儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="a2b88-124">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="a2b88-125">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a2b88-125">-VaultName</span></span>
<span data-ttu-id="a2b88-126">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="a2b88-126">Vault name.</span></span>
<span data-ttu-id="a2b88-127">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="a2b88-127">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="a2b88-128">-確認</span><span class="sxs-lookup"><span data-stu-id="a2b88-128">-Confirm</span></span>
<span data-ttu-id="a2b88-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a2b88-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2b88-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2b88-130">-WhatIf</span></span>
<span data-ttu-id="a2b88-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a2b88-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2b88-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a2b88-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2b88-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2b88-133">CommonParameters</span></span>
<span data-ttu-id="a2b88-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a2b88-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2b88-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a2b88-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2b88-136">輸入</span><span class="sxs-lookup"><span data-stu-id="a2b88-136">INPUTS</span></span>

### <span data-ttu-id="a2b88-137">System.object</span><span class="sxs-lookup"><span data-stu-id="a2b88-137">System.String</span></span>

## <span data-ttu-id="a2b88-138">輸出</span><span class="sxs-lookup"><span data-stu-id="a2b88-138">OUTPUTS</span></span>

### <span data-ttu-id="a2b88-139">ManagedStorageAccount 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="a2b88-139">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="a2b88-140">筆記</span><span class="sxs-lookup"><span data-stu-id="a2b88-140">NOTES</span></span>

## <span data-ttu-id="a2b88-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="a2b88-141">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)
