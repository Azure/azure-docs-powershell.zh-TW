---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultmanagedstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
ms.openlocfilehash: b603cff68d2343a683718ca53e900aa5b667dc14
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141637"
---
# <span data-ttu-id="029e0-101">Update-AzKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="029e0-101">Update-AzKeyVaultManagedStorageAccountKey</span></span>

## <span data-ttu-id="029e0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="029e0-102">SYNOPSIS</span></span>
<span data-ttu-id="029e0-103">重新生成主要電子倉庫管理的 Azure 儲存空間帳戶的指定金鑰。</span><span class="sxs-lookup"><span data-stu-id="029e0-103">Regenerates the specified key of Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="029e0-104">句法</span><span class="sxs-lookup"><span data-stu-id="029e0-104">SYNTAX</span></span>

### <span data-ttu-id="029e0-105">ByDefinitionName (預設) </span><span class="sxs-lookup"><span data-stu-id="029e0-105">ByDefinitionName (Default)</span></span>
```
Update-AzKeyVaultManagedStorageAccountKey [-VaultName] <String> [-AccountName] <String> [-KeyName] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="029e0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="029e0-106">ByInputObject</span></span>
```
Update-AzKeyVaultManagedStorageAccountKey [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-KeyName] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="029e0-107">說明</span><span class="sxs-lookup"><span data-stu-id="029e0-107">DESCRIPTION</span></span>
<span data-ttu-id="029e0-108">重新產生主要電子倉庫管理 Azure 儲存空間帳戶的指定金鑰，並將金鑰設定為作用中的金鑰。</span><span class="sxs-lookup"><span data-stu-id="029e0-108">Regenerates the specified key of Key Vault managed Azure Storage Account and sets the key as the active key.</span></span> <span data-ttu-id="029e0-109">主要電子倉庫將呼叫 Azure 資源管理員以重新產生金鑰。</span><span class="sxs-lookup"><span data-stu-id="029e0-109">Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span></span> <span data-ttu-id="029e0-110">呼叫者必須擁有許可權，才能在指定的 Azure 儲存空間帳戶上重新產生金鑰。</span><span class="sxs-lookup"><span data-stu-id="029e0-110">The caller must posses permissions to regenerate keys on given Azure Storage Account.</span></span>

## <span data-ttu-id="029e0-111">示例</span><span class="sxs-lookup"><span data-stu-id="029e0-111">EXAMPLES</span></span>

### <span data-ttu-id="029e0-112">範例1：重新產生按鍵</span><span class="sxs-lookup"><span data-stu-id="029e0-112">Example 1: Regenerate a key</span></span>
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

<span data-ttu-id="029e0-113">重新產生帳戶 "mystorageaccount" 的 "key1"，並將 "key1" 設為可用的主要保存庫管理的 Azure 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="029e0-113">Regenerates 'key1' of account 'mystorageaccount' and sets 'key1' as the active of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="029e0-114">參數</span><span class="sxs-lookup"><span data-stu-id="029e0-114">PARAMETERS</span></span>

### <span data-ttu-id="029e0-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="029e0-115">-AccountName</span></span>
<span data-ttu-id="029e0-116">主要保存庫管理的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="029e0-116">Key Vault managed storage account name.</span></span> <span data-ttu-id="029e0-117">Cmdlet 會從保存庫名稱、目前已選取的環境及 manged 儲存空間帳戶名稱構造受管理儲存空間帳戶名稱的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="029e0-117">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="029e0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="029e0-118">-DefaultProfile</span></span>
<span data-ttu-id="029e0-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="029e0-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="029e0-120">-Force</span><span class="sxs-lookup"><span data-stu-id="029e0-120">-Force</span></span>
<span data-ttu-id="029e0-121">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="029e0-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="029e0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="029e0-122">-InputObject</span></span>
<span data-ttu-id="029e0-123">ManagedStorageAccount 物件。</span><span class="sxs-lookup"><span data-stu-id="029e0-123">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="029e0-124">-KeyName</span><span class="sxs-lookup"><span data-stu-id="029e0-124">-KeyName</span></span>
<span data-ttu-id="029e0-125">要重新產生並生效的儲存空間帳戶金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="029e0-125">Name of storage account key to regenerate and make active.</span></span>

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

### <span data-ttu-id="029e0-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="029e0-126">-PassThru</span></span>
<span data-ttu-id="029e0-127">Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="029e0-127">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="029e0-128">如果指定此開關，則 Cmdlet 會傳回已刪除的受管理儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="029e0-128">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="029e0-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="029e0-129">-VaultName</span></span>
<span data-ttu-id="029e0-130">保存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="029e0-130">Vault name.</span></span>
<span data-ttu-id="029e0-131">Cmdlet 根據名稱和目前所選的環境來構造電子倉庫的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="029e0-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="029e0-132">-確認</span><span class="sxs-lookup"><span data-stu-id="029e0-132">-Confirm</span></span>
<span data-ttu-id="029e0-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="029e0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="029e0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="029e0-134">-WhatIf</span></span>
<span data-ttu-id="029e0-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="029e0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="029e0-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="029e0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="029e0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="029e0-137">CommonParameters</span></span>
<span data-ttu-id="029e0-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="029e0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="029e0-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="029e0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="029e0-140">輸入</span><span class="sxs-lookup"><span data-stu-id="029e0-140">INPUTS</span></span>

### <span data-ttu-id="029e0-141">PSKeyVaultManagedStorageAccountIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="029e0-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="029e0-142">輸出</span><span class="sxs-lookup"><span data-stu-id="029e0-142">OUTPUTS</span></span>

### <span data-ttu-id="029e0-143">PSKeyVaultManagedStorageAccount 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="029e0-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="029e0-144">筆記</span><span class="sxs-lookup"><span data-stu-id="029e0-144">NOTES</span></span>

## <span data-ttu-id="029e0-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="029e0-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

