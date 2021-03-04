---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/update-azkeyvaultmanagedstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
ms.openlocfilehash: 80ff79e71498cc76479592b65207da09fabed6a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908157"
---
# <span data-ttu-id="19001-101">Update-AzKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="19001-101">Update-AzKeyVaultManagedStorageAccountKey</span></span>

## <span data-ttu-id="19001-102">簡介</span><span class="sxs-lookup"><span data-stu-id="19001-102">SYNOPSIS</span></span>
<span data-ttu-id="19001-103">重新產生金鑰保存庫受管理的 Azure 儲存帳戶的指定金鑰。</span><span class="sxs-lookup"><span data-stu-id="19001-103">Regenerates the specified key of Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="19001-104">語法</span><span class="sxs-lookup"><span data-stu-id="19001-104">SYNTAX</span></span>

### <span data-ttu-id="19001-105">ByDefinitionName (預設) </span><span class="sxs-lookup"><span data-stu-id="19001-105">ByDefinitionName (Default)</span></span>
```
Update-AzKeyVaultManagedStorageAccountKey [-VaultName] <String> [-AccountName] <String> [-KeyName] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19001-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="19001-106">ByInputObject</span></span>
```
Update-AzKeyVaultManagedStorageAccountKey [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-KeyName] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="19001-107">描述</span><span class="sxs-lookup"><span data-stu-id="19001-107">DESCRIPTION</span></span>
<span data-ttu-id="19001-108">重新產生金鑰保存庫受管理的 Azure 儲存體帳戶的指定金鑰，並設定該金鑰為使用中金鑰。</span><span class="sxs-lookup"><span data-stu-id="19001-108">Regenerates the specified key of Key Vault managed Azure Storage Account and sets the key as the active key.</span></span> <span data-ttu-id="19001-109">Key Vault 會代理呼叫給 Azure Resource Manager，以重新產生金鑰。</span><span class="sxs-lookup"><span data-stu-id="19001-109">Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span></span> <span data-ttu-id="19001-110">來電者必須擁有許可權，才能重新產生特定 Azure 儲存帳戶中的金鑰。</span><span class="sxs-lookup"><span data-stu-id="19001-110">The caller must posses permissions to regenerate keys on given Azure Storage Account.</span></span>

## <span data-ttu-id="19001-111">例子</span><span class="sxs-lookup"><span data-stu-id="19001-111">EXAMPLES</span></span>

### <span data-ttu-id="19001-112">範例 1：重新產生金鑰</span><span class="sxs-lookup"><span data-stu-id="19001-112">Example 1: Regenerate a key</span></span>
```powershell
PS C:\> Update-AzKeyVaultManagedStorageAccountKey -VaultName 'myvault' -AccountName 'mystorageaccount' -KeyName 'key1'

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key1
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="19001-113">重新產生帳戶'mystorageaccount'的'key1'，並設定'key1'為金鑰保存庫管理 Azure 儲存帳戶的使用中。</span><span class="sxs-lookup"><span data-stu-id="19001-113">Regenerates 'key1' of account 'mystorageaccount' and sets 'key1' as the active of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="19001-114">參數</span><span class="sxs-lookup"><span data-stu-id="19001-114">PARAMETERS</span></span>

### <span data-ttu-id="19001-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="19001-115">-AccountName</span></span>
<span data-ttu-id="19001-116">金鑰保存庫受管理的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="19001-116">Key Vault managed storage account name.</span></span> <span data-ttu-id="19001-117">Cmdlet 會從保存庫名稱、目前選取的環境和偽造的儲存帳戶名稱建構受管理儲存帳戶名稱的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="19001-117">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19001-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19001-118">-DefaultProfile</span></span>
<span data-ttu-id="19001-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="19001-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19001-120">-強制</span><span class="sxs-lookup"><span data-stu-id="19001-120">-Force</span></span>
<span data-ttu-id="19001-121">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="19001-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="19001-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19001-122">-InputObject</span></span>
<span data-ttu-id="19001-123">ManagedStorageAccount 物件。</span><span class="sxs-lookup"><span data-stu-id="19001-123">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="19001-124">-KeyName</span><span class="sxs-lookup"><span data-stu-id="19001-124">-KeyName</span></span>
<span data-ttu-id="19001-125">要重新產生且成為使用中之儲存空間帳戶金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="19001-125">Name of storage account key to regenerate and make active.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19001-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19001-126">-PassThru</span></span>
<span data-ttu-id="19001-127">Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="19001-127">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="19001-128">如果指定此參數，Cmdlet 會返回已刪除的受管理儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="19001-128">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="19001-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="19001-129">-VaultName</span></span>
<span data-ttu-id="19001-130">儲存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="19001-130">Vault name.</span></span>
<span data-ttu-id="19001-131">Cmdlet 會根據名稱和目前選取的環境來建構庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="19001-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="19001-132">-確認</span><span class="sxs-lookup"><span data-stu-id="19001-132">-Confirm</span></span>
<span data-ttu-id="19001-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="19001-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19001-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19001-134">-WhatIf</span></span>
<span data-ttu-id="19001-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="19001-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19001-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="19001-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19001-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19001-137">CommonParameters</span></span>
<span data-ttu-id="19001-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="19001-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19001-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19001-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19001-140">輸入</span><span class="sxs-lookup"><span data-stu-id="19001-140">INPUTS</span></span>

### <span data-ttu-id="19001-141">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="19001-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="19001-142">輸出</span><span class="sxs-lookup"><span data-stu-id="19001-142">OUTPUTS</span></span>

### <span data-ttu-id="19001-143">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="19001-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="19001-144">筆記</span><span class="sxs-lookup"><span data-stu-id="19001-144">NOTES</span></span>

## <span data-ttu-id="19001-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="19001-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

