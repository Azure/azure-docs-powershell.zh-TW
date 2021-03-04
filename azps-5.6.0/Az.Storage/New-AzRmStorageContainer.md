---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
ms.openlocfilehash: c85b482ff077263d20ae770e6ec6d91b497153e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912982"
---
# <span data-ttu-id="05415-101">New-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="05415-101">New-AzRmStorageContainer</span></span>

## <span data-ttu-id="05415-102">簡介</span><span class="sxs-lookup"><span data-stu-id="05415-102">SYNOPSIS</span></span>
<span data-ttu-id="05415-103">建立儲存 Blob 容器</span><span class="sxs-lookup"><span data-stu-id="05415-103">Creates a Storage blob container</span></span>

## <span data-ttu-id="05415-104">語法</span><span class="sxs-lookup"><span data-stu-id="05415-104">SYNTAX</span></span>

### <span data-ttu-id="05415-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="05415-105">AccountName (Default)</span></span>
```
New-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05415-106">AccountNameEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="05415-106">AccountNameEncryptionScope</span></span>
```
New-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -DefaultEncryptionScope <String> -PreventEncryptionScopeOverride <Boolean> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05415-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="05415-107">AccountObject</span></span>
```
New-AzRmStorageContainer -StorageAccount <PSStorageAccount> -Name <String> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05415-108">AccountObjectEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="05415-108">AccountObjectEncryptionScope</span></span>
```
New-AzRmStorageContainer -StorageAccount <PSStorageAccount> -Name <String> -DefaultEncryptionScope <String>
 -PreventEncryptionScopeOverride <Boolean> [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05415-109">描述</span><span class="sxs-lookup"><span data-stu-id="05415-109">DESCRIPTION</span></span>
<span data-ttu-id="05415-110">**New-AzRmStorageContainer Cmdlet** 會建立儲存 Blob 容器</span><span class="sxs-lookup"><span data-stu-id="05415-110">The **New-AzRmStorageContainer** cmdlet creates a Storage blob container</span></span>

## <span data-ttu-id="05415-111">例子</span><span class="sxs-lookup"><span data-stu-id="05415-111">EXAMPLES</span></span>

### <span data-ttu-id="05415-112">範例 1：使用儲存帳戶名稱和容器名稱建立包含中繼資料的儲存 Blob 容器</span><span class="sxs-lookup"><span data-stu-id="05415-112">Example 1: Create a Storage blob container with Storage account name and container name, with metadata</span></span>
```
PS C:\>New-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Metadata @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="05415-113">此命令會建立包含儲存帳戶名稱和容器名稱以及中繼資料的儲存 Blob 容器。</span><span class="sxs-lookup"><span data-stu-id="05415-113">This command creates a Storage blob container with Storage account name and container name, with metadata.</span></span>

### <span data-ttu-id="05415-114">範例 2：使用儲存帳戶物件和容器名稱建立具有公用存取為 Blob 的儲存 Blob 容器</span><span class="sxs-lookup"><span data-stu-id="05415-114">Example 2: Create a Storage blob container with Storage account object and container name, with public access as Blob</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>New-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess Blob
```

<span data-ttu-id="05415-115">此命令會建立包含儲存帳戶物件和容器名稱的儲存 Blob 容器，且公用存取為 Blob。</span><span class="sxs-lookup"><span data-stu-id="05415-115">This command creates a Storage blob container with Storage account object and container name, with public access as Blob.</span></span>

### <span data-ttu-id="05415-116">範例 3：使用 EncryptionScope 設定建立儲存容器</span><span class="sxs-lookup"><span data-stu-id="05415-116">Example 3: Create a storage container with EncryptionScope setting</span></span>
```
PS C:\> $c = New-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name testcontainer -DefaultEncryptionScope "testscope" -PreventEncryptionScopeOverride $true

PS C:\> $c

   ResourceGroupName: myResourceGroup, StorageAccountName: myStorageAccount

Name          PublicAccess LastModified HasLegalHold HasImmutabilityPolicy
----          ------------ ------------ ------------ ---------------------
testcontainer                           False        False                

PS C:\> $c.DefaultEncryptionScope
testscope

PS C:\> $c.DenyEncryptionScopeOverride
True
```

<span data-ttu-id="05415-117">此命令會使用 Defalt encryptionScope 建立儲存容器，並且從容器預設值中區塊加密範圍的覆蓋。</span><span class="sxs-lookup"><span data-stu-id="05415-117">This command creates a storage container with a defalt encryptionScope, and blocks override of encryption scope from the container default.</span></span>
<span data-ttu-id="05415-118">然後顯示相關的容器屬性。</span><span class="sxs-lookup"><span data-stu-id="05415-118">Then show the related container properties.</span></span>

## <span data-ttu-id="05415-119">參數</span><span class="sxs-lookup"><span data-stu-id="05415-119">PARAMETERS</span></span>

### <span data-ttu-id="05415-120">-DefaultEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="05415-120">-DefaultEncryptionScope</span></span>
<span data-ttu-id="05415-121">將容器預設為針對所有寫入使用指定的加密範圍。</span><span class="sxs-lookup"><span data-stu-id="05415-121">Default the container to use specified encryption scope for all writes.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameEncryptionScope, AccountObjectEncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05415-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05415-122">-DefaultProfile</span></span>
<span data-ttu-id="05415-123">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="05415-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05415-124">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="05415-124">-Metadata</span></span>
<span data-ttu-id="05415-125">容器中繼資料</span><span class="sxs-lookup"><span data-stu-id="05415-125">Container Metadata</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05415-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="05415-126">-Name</span></span>
<span data-ttu-id="05415-127">容器名稱</span><span class="sxs-lookup"><span data-stu-id="05415-127">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05415-128">-PreventEncryptionScopeOverride</span><span class="sxs-lookup"><span data-stu-id="05415-128">-PreventEncryptionScopeOverride</span></span>
<span data-ttu-id="05415-129">從容器預設封鎖加密範圍的重寫。</span><span class="sxs-lookup"><span data-stu-id="05415-129">Block override of encryption scope from the container default.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AccountNameEncryptionScope, AccountObjectEncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05415-130">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="05415-130">-PublicAccess</span></span>
<span data-ttu-id="05415-131">Container PublicAccess</span><span class="sxs-lookup"><span data-stu-id="05415-131">Container PublicAccess</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSPublicAccess
Parameter Sets: (All)
Aliases:
Accepted values: Container, Blob, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05415-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05415-132">-ResourceGroupName</span></span>
<span data-ttu-id="05415-133">資源組名。</span><span class="sxs-lookup"><span data-stu-id="05415-133">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameEncryptionScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05415-134">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="05415-134">-StorageAccount</span></span>
<span data-ttu-id="05415-135">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="05415-135">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject, AccountObjectEncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05415-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="05415-136">-StorageAccountName</span></span>
<span data-ttu-id="05415-137">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="05415-137">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameEncryptionScope
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05415-138">-確認</span><span class="sxs-lookup"><span data-stu-id="05415-138">-Confirm</span></span>
<span data-ttu-id="05415-139">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="05415-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05415-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05415-140">-WhatIf</span></span>
<span data-ttu-id="05415-141">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="05415-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="05415-142">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="05415-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05415-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05415-143">CommonParameters</span></span>
<span data-ttu-id="05415-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="05415-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05415-145">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="05415-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05415-146">輸入</span><span class="sxs-lookup"><span data-stu-id="05415-146">INPUTS</span></span>

### <span data-ttu-id="05415-147">System.String</span><span class="sxs-lookup"><span data-stu-id="05415-147">System.String</span></span>

### <span data-ttu-id="05415-148">Microsoft.Azure.Commands.management.storage.models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="05415-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="05415-149">輸出</span><span class="sxs-lookup"><span data-stu-id="05415-149">OUTPUTS</span></span>

### <span data-ttu-id="05415-150">Microsoft.Azure.Commands.management.storage.models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="05415-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="05415-151">筆記</span><span class="sxs-lookup"><span data-stu-id="05415-151">NOTES</span></span>

## <span data-ttu-id="05415-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="05415-152">RELATED LINKS</span></span>
