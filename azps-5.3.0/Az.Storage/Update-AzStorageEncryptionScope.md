---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageEncryptionScope.md
ms.openlocfilehash: 6c8f07cbdb70b84d235afa7ce953da0bac477f55
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98285999"
---
# <span data-ttu-id="708e8-101">Update-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="708e8-101">Update-AzStorageEncryptionScope</span></span>

## <span data-ttu-id="708e8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="708e8-102">SYNOPSIS</span></span>
<span data-ttu-id="708e8-103">修改儲存空間帳戶的加密範圍。</span><span class="sxs-lookup"><span data-stu-id="708e8-103">Modify an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="708e8-104">句法</span><span class="sxs-lookup"><span data-stu-id="708e8-104">SYNTAX</span></span>

### <span data-ttu-id="708e8-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="708e8-105">AccountName (Default)</span></span>
```
Update-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-StorageEncryption] [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="708e8-106">AccountNameKeyVault</span><span class="sxs-lookup"><span data-stu-id="708e8-106">AccountNameKeyVault</span></span>
```
Update-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-KeyvaultEncryption] -KeyUri <String> [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="708e8-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="708e8-107">AccountObject</span></span>
```
Update-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-StorageEncryption] [-State <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="708e8-108">AccountObjectKeyVault</span><span class="sxs-lookup"><span data-stu-id="708e8-108">AccountObjectKeyVault</span></span>
```
Update-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-KeyvaultEncryption] -KeyUri <String> [-State <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="708e8-109">EncryptionScopeObject</span><span class="sxs-lookup"><span data-stu-id="708e8-109">EncryptionScopeObject</span></span>
```
Update-AzStorageEncryptionScope -InputObject <PSEncryptionScope> [-StorageEncryption] [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="708e8-110">EncryptionScopeObjectKeyVault</span><span class="sxs-lookup"><span data-stu-id="708e8-110">EncryptionScopeObjectKeyVault</span></span>
```
Update-AzStorageEncryptionScope -InputObject <PSEncryptionScope> [-KeyvaultEncryption] -KeyUri <String>
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="708e8-111">說明</span><span class="sxs-lookup"><span data-stu-id="708e8-111">DESCRIPTION</span></span>
<span data-ttu-id="708e8-112">**AzStorageEncryptionScope** Cmdlet 會修改儲存空間帳戶的加密範圍。</span><span class="sxs-lookup"><span data-stu-id="708e8-112">The **Update-AzStorageEncryptionScope** cmdlet modifies an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="708e8-113">示例</span><span class="sxs-lookup"><span data-stu-id="708e8-113">EXAMPLES</span></span>

### <span data-ttu-id="708e8-114">範例1：停用加密範圍</span><span class="sxs-lookup"><span data-stu-id="708e8-114">Example 1: Disable an encryption scope</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -State Disabled 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri                                                                          
----      -----    ------            --------------                                                                          
testscope Disabled Microsoft.Storage
```

<span data-ttu-id="708e8-115">這個命令會停用加密範圍。</span><span class="sxs-lookup"><span data-stu-id="708e8-115">This command disables an encryption scope.</span></span>

### <span data-ttu-id="708e8-116">範例2：啟用加密範圍</span><span class="sxs-lookup"><span data-stu-id="708e8-116">Example 2: Enable an encryption scope</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -State Enabled 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri                                                                          
----      -----    ------            --------------                                                                          
testscope Enabled  Microsoft.Storage
```

<span data-ttu-id="708e8-117">這個命令會啟用加密範圍。</span><span class="sxs-lookup"><span data-stu-id="708e8-117">This command enables an encryption scope.</span></span>

### <span data-ttu-id="708e8-118">範例3：更新加密範圍以使用儲存加密</span><span class="sxs-lookup"><span data-stu-id="708e8-118">Example 3: Update an encryption scope to use Storage Encryption</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -StorageEncryption

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri                                         
----      -----    ------            --------------                                         
testscope Enabled  Microsoft.Storage
```

<span data-ttu-id="708e8-119">這個命令會更新加密範圍，以使用儲存加密。</span><span class="sxs-lookup"><span data-stu-id="708e8-119">This command updates an encryption scope to use Storage Encryption.</span></span>

### <span data-ttu-id="708e8-120">範例4：更新加密範圍以使用 Keyvault 加密</span><span class="sxs-lookup"><span data-stu-id="708e8-120">Example 4: Update an encryption scope to use Keyvault Encryption</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EncryptionScopeName testscope -KeyvaultEncryption -KeyUri "https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Enabled  Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57
```

<span data-ttu-id="708e8-121">這個命令 updtaes 要使用 Keyvault 加密的加密範圍。</span><span class="sxs-lookup"><span data-stu-id="708e8-121">This command updtaes an encryption scope to use Keyvault Encryption.</span></span>
<span data-ttu-id="708e8-122">儲存帳戶身分識別需要擁有 keyvault 金鑰的 [取得]、[wrapkey]、[unwrapkey] 許可權。</span><span class="sxs-lookup"><span data-stu-id="708e8-122">The Storage account Identity need have get,wrapkey,unwrapkey permissions to the keyvault key.</span></span>

## <span data-ttu-id="708e8-123">參數</span><span class="sxs-lookup"><span data-stu-id="708e8-123">PARAMETERS</span></span>

### <span data-ttu-id="708e8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="708e8-124">-DefaultProfile</span></span>
<span data-ttu-id="708e8-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="708e8-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="708e8-126">-EncryptionScopeName</span><span class="sxs-lookup"><span data-stu-id="708e8-126">-EncryptionScopeName</span></span>
<span data-ttu-id="708e8-127">Azure 儲存空間 EncryptionScope 名稱</span><span class="sxs-lookup"><span data-stu-id="708e8-127">Azure Storage EncryptionScope name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameKeyVault, AccountObject, AccountObjectKeyVault
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="708e8-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="708e8-128">-InputObject</span></span>
<span data-ttu-id="708e8-129">EncryptionScope 物件</span><span class="sxs-lookup"><span data-stu-id="708e8-129">EncryptionScope object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope
Parameter Sets: EncryptionScopeObject, EncryptionScopeObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="708e8-130">-KeyUri</span><span class="sxs-lookup"><span data-stu-id="708e8-130">-KeyUri</span></span>
<span data-ttu-id="708e8-131">金鑰 Uri</span><span class="sxs-lookup"><span data-stu-id="708e8-131">The key Uri</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameKeyVault, AccountObjectKeyVault, EncryptionScopeObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="708e8-132">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="708e8-132">-KeyvaultEncryption</span></span>
<span data-ttu-id="708e8-133">使用 keySource 做為 Microsoft. Keyvault 建立加密範圍</span><span class="sxs-lookup"><span data-stu-id="708e8-133">Create encryption scope with keySource as Microsoft.Keyvault</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameKeyVault, AccountObjectKeyVault, EncryptionScopeObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="708e8-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="708e8-134">-ResourceGroupName</span></span>
<span data-ttu-id="708e8-135">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="708e8-135">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameKeyVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="708e8-136">-State</span><span class="sxs-lookup"><span data-stu-id="708e8-136">-State</span></span>
<span data-ttu-id="708e8-137">更新加密範圍狀態，可能的值包括： ' 已啟用」、「已停用」。</span><span class="sxs-lookup"><span data-stu-id="708e8-137">Update encryption scope State, Possible values include: 'Enabled', 'Disabled'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="708e8-138">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="708e8-138">-StorageAccount</span></span>
<span data-ttu-id="708e8-139">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="708e8-139">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject, AccountObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="708e8-140">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="708e8-140">-StorageAccountName</span></span>
<span data-ttu-id="708e8-141">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="708e8-141">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameKeyVault
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="708e8-142">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="708e8-142">-StorageEncryption</span></span>
<span data-ttu-id="708e8-143">使用 keySource 建立加密範圍，以儲存為 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="708e8-143">Create encryption scope with keySource as Microsoft.Storage.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountName, AccountObject, EncryptionScopeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="708e8-144">-確認</span><span class="sxs-lookup"><span data-stu-id="708e8-144">-Confirm</span></span>
<span data-ttu-id="708e8-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="708e8-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="708e8-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="708e8-146">-WhatIf</span></span>
<span data-ttu-id="708e8-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="708e8-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="708e8-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="708e8-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="708e8-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="708e8-149">CommonParameters</span></span>
<span data-ttu-id="708e8-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="708e8-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="708e8-151">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="708e8-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="708e8-152">輸入</span><span class="sxs-lookup"><span data-stu-id="708e8-152">INPUTS</span></span>

### <span data-ttu-id="708e8-153">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="708e8-153">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="708e8-154">輸出</span><span class="sxs-lookup"><span data-stu-id="708e8-154">OUTPUTS</span></span>

### <span data-ttu-id="708e8-155">PSEncryptionScope 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="708e8-155">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span></span>

## <span data-ttu-id="708e8-156">筆記</span><span class="sxs-lookup"><span data-stu-id="708e8-156">NOTES</span></span>

## <span data-ttu-id="708e8-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="708e8-157">RELATED LINKS</span></span>
