---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/update-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageEncryptionScope.md
ms.openlocfilehash: 153165406fd02561dbece79e18558065ff34c8f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907238"
---
# <span data-ttu-id="ccff4-101">Update-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="ccff4-101">Update-AzStorageEncryptionScope</span></span>

## <span data-ttu-id="ccff4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ccff4-102">SYNOPSIS</span></span>
<span data-ttu-id="ccff4-103">修改儲存空間帳戶的加密範圍。</span><span class="sxs-lookup"><span data-stu-id="ccff4-103">Modify an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="ccff4-104">語法</span><span class="sxs-lookup"><span data-stu-id="ccff4-104">SYNTAX</span></span>

### <span data-ttu-id="ccff4-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="ccff4-105">AccountName (Default)</span></span>
```
Update-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-StorageEncryption] [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccff4-106">AccountNameKeyVault</span><span class="sxs-lookup"><span data-stu-id="ccff4-106">AccountNameKeyVault</span></span>
```
Update-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-KeyvaultEncryption] -KeyUri <String> [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccff4-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="ccff4-107">AccountObject</span></span>
```
Update-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-StorageEncryption] [-State <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ccff4-108">AccountObjectKeyVault</span><span class="sxs-lookup"><span data-stu-id="ccff4-108">AccountObjectKeyVault</span></span>
```
Update-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-KeyvaultEncryption] -KeyUri <String> [-State <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccff4-109">EncryptionScopeObject</span><span class="sxs-lookup"><span data-stu-id="ccff4-109">EncryptionScopeObject</span></span>
```
Update-AzStorageEncryptionScope -InputObject <PSEncryptionScope> [-StorageEncryption] [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccff4-110">EncryptionScopeObjectKeyVault</span><span class="sxs-lookup"><span data-stu-id="ccff4-110">EncryptionScopeObjectKeyVault</span></span>
```
Update-AzStorageEncryptionScope -InputObject <PSEncryptionScope> [-KeyvaultEncryption] -KeyUri <String>
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccff4-111">描述</span><span class="sxs-lookup"><span data-stu-id="ccff4-111">DESCRIPTION</span></span>
<span data-ttu-id="ccff4-112">**Update-AzStorageEncryptionScope** Cmdlet 會修改儲存帳戶的加密範圍。</span><span class="sxs-lookup"><span data-stu-id="ccff4-112">The **Update-AzStorageEncryptionScope** cmdlet modifies an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="ccff4-113">例子</span><span class="sxs-lookup"><span data-stu-id="ccff4-113">EXAMPLES</span></span>

### <span data-ttu-id="ccff4-114">範例 1：停用加密範圍</span><span class="sxs-lookup"><span data-stu-id="ccff4-114">Example 1: Disable an encryption scope</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -State Disabled 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri RequireInfrastructureEncryption                                         
----      -----    ------            -------------- -------------------------------                                         
testscope Disabled Microsoft.Storage
```

<span data-ttu-id="ccff4-115">此命令會停用加密範圍。</span><span class="sxs-lookup"><span data-stu-id="ccff4-115">This command disables an encryption scope.</span></span>

### <span data-ttu-id="ccff4-116">範例 2：啟用加密範圍</span><span class="sxs-lookup"><span data-stu-id="ccff4-116">Example 2: Enable an encryption scope</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -State Enabled 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri RequireInfrastructureEncryption                                                                           
----      -----    ------            -------------- -------------------------------                                                                          
testscope Enabled  Microsoft.Storage
```

<span data-ttu-id="ccff4-117">此命令啟用加密範圍。</span><span class="sxs-lookup"><span data-stu-id="ccff4-117">This command enables an encryption scope.</span></span>

### <span data-ttu-id="ccff4-118">範例 3：更新加密範圍以使用儲存加密</span><span class="sxs-lookup"><span data-stu-id="ccff4-118">Example 3: Update an encryption scope to use Storage Encryption</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -StorageEncryption

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri RequireInfrastructureEncryption                                          
----      -----    ------            -------------- -------------------------------                                         
testscope Enabled  Microsoft.Storage
```

<span data-ttu-id="ccff4-119">此命令會更新加密範圍以使用儲存加密。</span><span class="sxs-lookup"><span data-stu-id="ccff4-119">This command updates an encryption scope to use Storage Encryption.</span></span>

### <span data-ttu-id="ccff4-120">範例 4：更新加密範圍以使用 Keyvault Encryption</span><span class="sxs-lookup"><span data-stu-id="ccff4-120">Example 4: Update an encryption scope to use Keyvault Encryption</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EncryptionScopeName testscope -KeyvaultEncryption -KeyUri "https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                                                          RequireInfrastructureEncryption 
----      -----    ------             --------------                                                                          -------------------------------
testscope Enabled  Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57   
```

<span data-ttu-id="ccff4-121">此命令會提高使用 Keyvault 加密的加密範圍。</span><span class="sxs-lookup"><span data-stu-id="ccff4-121">This command updtaes an encryption scope to use Keyvault Encryption.</span></span>
<span data-ttu-id="ccff4-122">儲存帳戶身分識別需要取得 keyvault 金鑰的 wrapkey、unwrapkey 許可權。</span><span class="sxs-lookup"><span data-stu-id="ccff4-122">The Storage account Identity need have get,wrapkey,unwrapkey permissions to the keyvault key.</span></span>

## <span data-ttu-id="ccff4-123">參數</span><span class="sxs-lookup"><span data-stu-id="ccff4-123">PARAMETERS</span></span>

### <span data-ttu-id="ccff4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccff4-124">-DefaultProfile</span></span>
<span data-ttu-id="ccff4-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ccff4-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccff4-126">-EncryptionScopeName</span><span class="sxs-lookup"><span data-stu-id="ccff4-126">-EncryptionScopeName</span></span>
<span data-ttu-id="ccff4-127">Azure 儲存體 EncryptionScope 名稱</span><span class="sxs-lookup"><span data-stu-id="ccff4-127">Azure Storage EncryptionScope name</span></span>

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

### <span data-ttu-id="ccff4-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ccff4-128">-InputObject</span></span>
<span data-ttu-id="ccff4-129">EncryptionScope 物件</span><span class="sxs-lookup"><span data-stu-id="ccff4-129">EncryptionScope object</span></span>

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

### <span data-ttu-id="ccff4-130">-KeyUri</span><span class="sxs-lookup"><span data-stu-id="ccff4-130">-KeyUri</span></span>
<span data-ttu-id="ccff4-131">金鑰 Uri</span><span class="sxs-lookup"><span data-stu-id="ccff4-131">The key Uri</span></span>

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

### <span data-ttu-id="ccff4-132">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="ccff4-132">-KeyvaultEncryption</span></span>
<span data-ttu-id="ccff4-133">使用 KeySource 建立加密範圍做為 Microsoft.Keyvault</span><span class="sxs-lookup"><span data-stu-id="ccff4-133">Create encryption scope with keySource as Microsoft.Keyvault</span></span>

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

### <span data-ttu-id="ccff4-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccff4-134">-ResourceGroupName</span></span>
<span data-ttu-id="ccff4-135">資源組名。</span><span class="sxs-lookup"><span data-stu-id="ccff4-135">Resource Group Name.</span></span>

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

### <span data-ttu-id="ccff4-136">-State</span><span class="sxs-lookup"><span data-stu-id="ccff4-136">-State</span></span>
<span data-ttu-id="ccff4-137">更新加密範圍狀態，可能的值包括：「已啟用」、」已停用」。</span><span class="sxs-lookup"><span data-stu-id="ccff4-137">Update encryption scope State, Possible values include: 'Enabled', 'Disabled'.</span></span>

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

### <span data-ttu-id="ccff4-138">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="ccff4-138">-StorageAccount</span></span>
<span data-ttu-id="ccff4-139">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="ccff4-139">Storage account object</span></span>

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

### <span data-ttu-id="ccff4-140">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ccff4-140">-StorageAccountName</span></span>
<span data-ttu-id="ccff4-141">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="ccff4-141">Storage Account Name.</span></span>

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

### <span data-ttu-id="ccff4-142">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="ccff4-142">-StorageEncryption</span></span>
<span data-ttu-id="ccff4-143">使用 KeySource 建立加密範圍做為 Microsoft.Storage。</span><span class="sxs-lookup"><span data-stu-id="ccff4-143">Create encryption scope with keySource as Microsoft.Storage.</span></span>

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

### <span data-ttu-id="ccff4-144">-確認</span><span class="sxs-lookup"><span data-stu-id="ccff4-144">-Confirm</span></span>
<span data-ttu-id="ccff4-145">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ccff4-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccff4-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccff4-146">-WhatIf</span></span>
<span data-ttu-id="ccff4-147">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ccff4-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccff4-148">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ccff4-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccff4-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccff4-149">CommonParameters</span></span>
<span data-ttu-id="ccff4-150">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ccff4-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccff4-151">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ccff4-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccff4-152">輸入</span><span class="sxs-lookup"><span data-stu-id="ccff4-152">INPUTS</span></span>

### <span data-ttu-id="ccff4-153">Microsoft.Azure.Commands.management.storage.models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ccff4-153">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="ccff4-154">輸出</span><span class="sxs-lookup"><span data-stu-id="ccff4-154">OUTPUTS</span></span>

### <span data-ttu-id="ccff4-155">Microsoft.Azure.Commands.management.storage.models.PSEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="ccff4-155">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span></span>

## <span data-ttu-id="ccff4-156">筆記</span><span class="sxs-lookup"><span data-stu-id="ccff4-156">NOTES</span></span>

## <span data-ttu-id="ccff4-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="ccff4-157">RELATED LINKS</span></span>
