---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageEncryptionScope.md
ms.openlocfilehash: 011bdd96d69ae73ca62145b85f6e636751f8eb9f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100134443"
---
# <span data-ttu-id="440a3-101">New-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="440a3-101">New-AzStorageEncryptionScope</span></span>

## <span data-ttu-id="440a3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="440a3-102">SYNOPSIS</span></span>
<span data-ttu-id="440a3-103">建立儲存空間帳戶的加密範圍。</span><span class="sxs-lookup"><span data-stu-id="440a3-103">Creates an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="440a3-104">句法</span><span class="sxs-lookup"><span data-stu-id="440a3-104">SYNTAX</span></span>

### <span data-ttu-id="440a3-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="440a3-105">AccountName (Default)</span></span>
```
New-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-StorageEncryption] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="440a3-106">AccountNameKeyVault</span><span class="sxs-lookup"><span data-stu-id="440a3-106">AccountNameKeyVault</span></span>
```
New-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-KeyvaultEncryption] -KeyUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="440a3-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="440a3-107">AccountObject</span></span>
```
New-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-StorageEncryption] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="440a3-108">AccountObjectKeyVault</span><span class="sxs-lookup"><span data-stu-id="440a3-108">AccountObjectKeyVault</span></span>
```
New-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-KeyvaultEncryption] -KeyUri <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="440a3-109">說明</span><span class="sxs-lookup"><span data-stu-id="440a3-109">DESCRIPTION</span></span>
<span data-ttu-id="440a3-110">**新的-AzStorageEncryptionScope** Cmdlet 會為儲存空間帳戶建立加密範圍。</span><span class="sxs-lookup"><span data-stu-id="440a3-110">The **New-AzStorageEncryptionScope** cmdlet creates an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="440a3-111">示例</span><span class="sxs-lookup"><span data-stu-id="440a3-111">EXAMPLES</span></span>

### <span data-ttu-id="440a3-112">範例1：使用儲存加密建立加密範圍</span><span class="sxs-lookup"><span data-stu-id="440a3-112">Example 1: Create an encryption scope with Storage Encryption</span></span>
```
PS C:\> New-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -StorageEncryption

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri                                         
----      -----    ------            --------------                                         
testscope Enabled  Microsoft.Storage
```

<span data-ttu-id="440a3-113">這個命令會建立含儲存加密的加密範圍。</span><span class="sxs-lookup"><span data-stu-id="440a3-113">This command creates an encryption scope with Storage Encryption.</span></span>

### <span data-ttu-id="440a3-114">範例2：使用 Keyvault 加密建立加密範圍</span><span class="sxs-lookup"><span data-stu-id="440a3-114">Example 2: Create an encryption scope with Keyvault Encryption</span></span>
```
PS C:\> New-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EncryptionScopeName testscope -KeyvaultEncryption -KeyUri "https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Enabled  Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57
```

<span data-ttu-id="440a3-115">這個命令會使用 Keyvault 加密來建立加密範圍。</span><span class="sxs-lookup"><span data-stu-id="440a3-115">This command creates an encryption scope with Keyvault Encryption.</span></span>
<span data-ttu-id="440a3-116">儲存帳戶身分識別需要擁有 keyvault 金鑰的 [取得]、[wrapkey]、[unwrapkey] 許可權。</span><span class="sxs-lookup"><span data-stu-id="440a3-116">The Storage account Identity need have get,wrapkey,unwrapkey permissions to the keyvault key.</span></span>

## <span data-ttu-id="440a3-117">參數</span><span class="sxs-lookup"><span data-stu-id="440a3-117">PARAMETERS</span></span>

### <span data-ttu-id="440a3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="440a3-118">-DefaultProfile</span></span>
<span data-ttu-id="440a3-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="440a3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="440a3-120">-EncryptionScopeName</span><span class="sxs-lookup"><span data-stu-id="440a3-120">-EncryptionScopeName</span></span>
<span data-ttu-id="440a3-121">Azure 儲存空間 EncryptionScope 名稱</span><span class="sxs-lookup"><span data-stu-id="440a3-121">Azure Storage EncryptionScope name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="440a3-122">-KeyUri</span><span class="sxs-lookup"><span data-stu-id="440a3-122">-KeyUri</span></span>
<span data-ttu-id="440a3-123">金鑰 Uri</span><span class="sxs-lookup"><span data-stu-id="440a3-123">The key Uri</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameKeyVault, AccountObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="440a3-124">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="440a3-124">-KeyvaultEncryption</span></span>
<span data-ttu-id="440a3-125">使用 keySource 做為 Microsoft. Keyvault 建立加密範圍</span><span class="sxs-lookup"><span data-stu-id="440a3-125">Create encryption scope with keySource as Microsoft.Keyvault</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameKeyVault, AccountObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="440a3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="440a3-126">-ResourceGroupName</span></span>
<span data-ttu-id="440a3-127">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="440a3-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="440a3-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="440a3-128">-StorageAccount</span></span>
<span data-ttu-id="440a3-129">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="440a3-129">Storage account object</span></span>

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

### <span data-ttu-id="440a3-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="440a3-130">-StorageAccountName</span></span>
<span data-ttu-id="440a3-131">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="440a3-131">Storage Account Name.</span></span>

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

### <span data-ttu-id="440a3-132">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="440a3-132">-StorageEncryption</span></span>
<span data-ttu-id="440a3-133">使用 keySource 建立加密範圍，以儲存為 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="440a3-133">Create encryption scope with keySource as Microsoft.Storage.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="440a3-134">-確認</span><span class="sxs-lookup"><span data-stu-id="440a3-134">-Confirm</span></span>
<span data-ttu-id="440a3-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="440a3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="440a3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="440a3-136">-WhatIf</span></span>
<span data-ttu-id="440a3-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="440a3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="440a3-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="440a3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="440a3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="440a3-139">CommonParameters</span></span>
<span data-ttu-id="440a3-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="440a3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="440a3-141">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="440a3-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="440a3-142">輸入</span><span class="sxs-lookup"><span data-stu-id="440a3-142">INPUTS</span></span>

### <span data-ttu-id="440a3-143">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="440a3-143">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="440a3-144">輸出</span><span class="sxs-lookup"><span data-stu-id="440a3-144">OUTPUTS</span></span>

### <span data-ttu-id="440a3-145">PSEncryptionScope 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="440a3-145">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span></span>

## <span data-ttu-id="440a3-146">筆記</span><span class="sxs-lookup"><span data-stu-id="440a3-146">NOTES</span></span>

## <span data-ttu-id="440a3-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="440a3-147">RELATED LINKS</span></span>
