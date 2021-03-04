---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageEncryptionScope.md
ms.openlocfilehash: ab2750bff8ccc3f53761671455bc50fe3ec154d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915069"
---
# <span data-ttu-id="cd470-101">New-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="cd470-101">New-AzStorageEncryptionScope</span></span>

## <span data-ttu-id="cd470-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cd470-102">SYNOPSIS</span></span>
<span data-ttu-id="cd470-103">建立儲存空間帳戶的加密範圍。</span><span class="sxs-lookup"><span data-stu-id="cd470-103">Creates an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="cd470-104">語法</span><span class="sxs-lookup"><span data-stu-id="cd470-104">SYNTAX</span></span>

### <span data-ttu-id="cd470-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="cd470-105">AccountName (Default)</span></span>
```
New-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-StorageEncryption] [-RequireInfrastructureEncryption]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd470-106">AccountNameKeyVault</span><span class="sxs-lookup"><span data-stu-id="cd470-106">AccountNameKeyVault</span></span>
```
New-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-KeyvaultEncryption] -KeyUri <String> [-RequireInfrastructureEncryption]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd470-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="cd470-107">AccountObject</span></span>
```
New-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-StorageEncryption] [-RequireInfrastructureEncryption] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd470-108">AccountObjectKeyVault</span><span class="sxs-lookup"><span data-stu-id="cd470-108">AccountObjectKeyVault</span></span>
```
New-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-KeyvaultEncryption] -KeyUri <String> [-RequireInfrastructureEncryption]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd470-109">描述</span><span class="sxs-lookup"><span data-stu-id="cd470-109">DESCRIPTION</span></span>
<span data-ttu-id="cd470-110">**New-AzStorageEncryptionScope** Cmdlet 會為儲存空間帳戶建立加密範圍。</span><span class="sxs-lookup"><span data-stu-id="cd470-110">The **New-AzStorageEncryptionScope** cmdlet creates an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="cd470-111">例子</span><span class="sxs-lookup"><span data-stu-id="cd470-111">EXAMPLES</span></span>

### <span data-ttu-id="cd470-112">範例 1：使用儲存加密建立加密範圍</span><span class="sxs-lookup"><span data-stu-id="cd470-112">Example 1: Create an encryption scope with Storage Encryption</span></span>
```
PS C:\> New-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -StorageEncryption

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri RequireInfrastructureEncryption                                         
----      -----    ------            -------------- -------------------------------                                         
testscope Enabled  Microsoft.Storage
```

<span data-ttu-id="cd470-113">此命令會使用儲存加密建立加密範圍。</span><span class="sxs-lookup"><span data-stu-id="cd470-113">This command creates an encryption scope with Storage Encryption.</span></span>

### <span data-ttu-id="cd470-114">範例 2：使用 Keyvault Encryption 和 RequireInfracryptEncryption 建立加密範圍</span><span class="sxs-lookup"><span data-stu-id="cd470-114">Example 2: Create an encryption scope with Keyvault Encryption, and RequireInfrastructureEncryption</span></span>
```
PS C:\> New-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" `
    -EncryptionScopeName testscope -KeyvaultEncryption -KeyUri "https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57" `
    -RequireInfrastructureEncryption 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name         State   Source           KeyVaultKeyUri                                                                          RequireInfrastructureEncryption                                       
----         -----   ------             --------------                                                                        -------------------------------                                     
testscope Enabled  Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57  True 
```

<span data-ttu-id="cd470-115">此命令會使用 Keyvault Encryption 和 RequireInfracryptEncryption 建立加密範圍。</span><span class="sxs-lookup"><span data-stu-id="cd470-115">This command creates an encryption scope with Keyvault Encryption and RequireInfrastructureEncryption.</span></span>
<span data-ttu-id="cd470-116">儲存帳戶身分識別需要取得 keyvault 金鑰的 wrapkey、unwrapkey 許可權。</span><span class="sxs-lookup"><span data-stu-id="cd470-116">The Storage account Identity need have get,wrapkey,unwrapkey permissions to the keyvault key.</span></span>

## <span data-ttu-id="cd470-117">參數</span><span class="sxs-lookup"><span data-stu-id="cd470-117">PARAMETERS</span></span>

### <span data-ttu-id="cd470-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd470-118">-DefaultProfile</span></span>
<span data-ttu-id="cd470-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cd470-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd470-120">-EncryptionScopeName</span><span class="sxs-lookup"><span data-stu-id="cd470-120">-EncryptionScopeName</span></span>
<span data-ttu-id="cd470-121">Azure 儲存體 EncryptionScope 名稱</span><span class="sxs-lookup"><span data-stu-id="cd470-121">Azure Storage EncryptionScope name</span></span>

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

### <span data-ttu-id="cd470-122">-KeyUri</span><span class="sxs-lookup"><span data-stu-id="cd470-122">-KeyUri</span></span>
<span data-ttu-id="cd470-123">金鑰 Uri</span><span class="sxs-lookup"><span data-stu-id="cd470-123">The key Uri</span></span>

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

### <span data-ttu-id="cd470-124">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="cd470-124">-KeyvaultEncryption</span></span>
<span data-ttu-id="cd470-125">使用 KeySource 建立加密範圍做為 Microsoft.Keyvault</span><span class="sxs-lookup"><span data-stu-id="cd470-125">Create encryption scope with keySource as Microsoft.Keyvault</span></span>

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

### <span data-ttu-id="cd470-126">-RequireInfracryptEncryption</span><span class="sxs-lookup"><span data-stu-id="cd470-126">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="cd470-127">加密範圍會針對靜態資料，使用平臺管理金鑰來使用次要加密層。</span><span class="sxs-lookup"><span data-stu-id="cd470-127">The encryption scope will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="cd470-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd470-128">-ResourceGroupName</span></span>
<span data-ttu-id="cd470-129">資源組名。</span><span class="sxs-lookup"><span data-stu-id="cd470-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="cd470-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd470-130">-StorageAccount</span></span>
<span data-ttu-id="cd470-131">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="cd470-131">Storage account object</span></span>

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

### <span data-ttu-id="cd470-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cd470-132">-StorageAccountName</span></span>
<span data-ttu-id="cd470-133">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="cd470-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="cd470-134">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="cd470-134">-StorageEncryption</span></span>
<span data-ttu-id="cd470-135">使用 KeySource 建立加密範圍做為 Microsoft.Storage。</span><span class="sxs-lookup"><span data-stu-id="cd470-135">Create encryption scope with keySource as Microsoft.Storage.</span></span>

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

### <span data-ttu-id="cd470-136">-確認</span><span class="sxs-lookup"><span data-stu-id="cd470-136">-Confirm</span></span>
<span data-ttu-id="cd470-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="cd470-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd470-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd470-138">-WhatIf</span></span>
<span data-ttu-id="cd470-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cd470-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd470-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd470-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd470-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd470-141">CommonParameters</span></span>
<span data-ttu-id="cd470-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cd470-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd470-143">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="cd470-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd470-144">輸入</span><span class="sxs-lookup"><span data-stu-id="cd470-144">INPUTS</span></span>

### <span data-ttu-id="cd470-145">Microsoft.Azure.Commands.management.storage.models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd470-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="cd470-146">輸出</span><span class="sxs-lookup"><span data-stu-id="cd470-146">OUTPUTS</span></span>

### <span data-ttu-id="cd470-147">Microsoft.Azure.Commands.management.storage.models.PSEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="cd470-147">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span></span>

## <span data-ttu-id="cd470-148">筆記</span><span class="sxs-lookup"><span data-stu-id="cd470-148">NOTES</span></span>

## <span data-ttu-id="cd470-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="cd470-149">RELATED LINKS</span></span>
