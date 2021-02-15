---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
ms.openlocfilehash: 901061390c68853832bad14965620abad21817e8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100137795"
---
# <span data-ttu-id="238cd-101">New-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="238cd-101">New-AzRmStorageContainer</span></span>

## <span data-ttu-id="238cd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="238cd-102">SYNOPSIS</span></span>
<span data-ttu-id="238cd-103">建立儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="238cd-103">Creates a Storage blob container</span></span>

## <span data-ttu-id="238cd-104">句法</span><span class="sxs-lookup"><span data-stu-id="238cd-104">SYNTAX</span></span>

### <span data-ttu-id="238cd-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="238cd-105">AccountName (Default)</span></span>
```
New-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="238cd-106">AccountNameEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="238cd-106">AccountNameEncryptionScope</span></span>
```
New-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -DefaultEncryptionScope <String> -PreventEncryptionScopeOverride <Boolean> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="238cd-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="238cd-107">AccountObject</span></span>
```
New-AzRmStorageContainer -StorageAccount <PSStorageAccount> -Name <String> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="238cd-108">AccountObjectEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="238cd-108">AccountObjectEncryptionScope</span></span>
```
New-AzRmStorageContainer -StorageAccount <PSStorageAccount> -Name <String> -DefaultEncryptionScope <String>
 -PreventEncryptionScopeOverride <Boolean> [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="238cd-109">說明</span><span class="sxs-lookup"><span data-stu-id="238cd-109">DESCRIPTION</span></span>
<span data-ttu-id="238cd-110">**新的-AzRmStorageContainer** Cmdlet 會建立儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="238cd-110">The **New-AzRmStorageContainer** cmdlet creates a Storage blob container</span></span>

## <span data-ttu-id="238cd-111">示例</span><span class="sxs-lookup"><span data-stu-id="238cd-111">EXAMPLES</span></span>

### <span data-ttu-id="238cd-112">範例1：使用儲存空間帳戶名稱和容器名稱（含中繼資料）建立儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="238cd-112">Example 1: Create a Storage blob container with Storage account name and container name, with metadata</span></span>
```
PS C:\>New-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Metadata @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="238cd-113">這個命令會建立含中繼資料之儲存空間帳戶名稱和容器名稱的儲存 blob 容器。</span><span class="sxs-lookup"><span data-stu-id="238cd-113">This command creates a Storage blob container with Storage account name and container name, with metadata.</span></span>

### <span data-ttu-id="238cd-114">範例2：使用儲存空間帳戶物件和容器名稱建立儲存 blob 容器，並以 Blob 公用存取</span><span class="sxs-lookup"><span data-stu-id="238cd-114">Example 2: Create a Storage blob container with Storage account object and container name, with public access as Blob</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>New-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess Blob
```

<span data-ttu-id="238cd-115">這個命令會建立含儲存空間帳戶物件和容器名稱的儲存 blob 容器，並以 Blob 公開存取權。</span><span class="sxs-lookup"><span data-stu-id="238cd-115">This command creates a Storage blob container with Storage account object and container name, with public access as Blob.</span></span>

### <span data-ttu-id="238cd-116">範例3：使用 EncryptionScope 設定來建立儲存容器</span><span class="sxs-lookup"><span data-stu-id="238cd-116">Example 3: Create a storage container with EncryptionScope setting</span></span>
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

<span data-ttu-id="238cd-117">這個命令會建立一個含有 defalt encryptionScope 的儲存容器，並封鎖來自容器預設的加密範圍。</span><span class="sxs-lookup"><span data-stu-id="238cd-117">This command creates a storage container with a defalt encryptionScope, and blocks override of encryption scope from the container default.</span></span>
<span data-ttu-id="238cd-118">然後顯示相關的容器屬性。</span><span class="sxs-lookup"><span data-stu-id="238cd-118">Then show the related container properties.</span></span>

## <span data-ttu-id="238cd-119">參數</span><span class="sxs-lookup"><span data-stu-id="238cd-119">PARAMETERS</span></span>

### <span data-ttu-id="238cd-120">-DefaultEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="238cd-120">-DefaultEncryptionScope</span></span>
<span data-ttu-id="238cd-121">預設是使用指定的加密範圍進行所有寫入的容器。</span><span class="sxs-lookup"><span data-stu-id="238cd-121">Default the container to use specified encryption scope for all writes.</span></span>

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

### <span data-ttu-id="238cd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="238cd-122">-DefaultProfile</span></span>
<span data-ttu-id="238cd-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="238cd-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="238cd-124">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="238cd-124">-Metadata</span></span>
<span data-ttu-id="238cd-125">容器中繼資料</span><span class="sxs-lookup"><span data-stu-id="238cd-125">Container Metadata</span></span>

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

### <span data-ttu-id="238cd-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="238cd-126">-Name</span></span>
<span data-ttu-id="238cd-127">容器名稱</span><span class="sxs-lookup"><span data-stu-id="238cd-127">Container Name</span></span>

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

### <span data-ttu-id="238cd-128">-PreventEncryptionScopeOverride</span><span class="sxs-lookup"><span data-stu-id="238cd-128">-PreventEncryptionScopeOverride</span></span>
<span data-ttu-id="238cd-129">從容器預設的封鎖覆蓋加密範圍。</span><span class="sxs-lookup"><span data-stu-id="238cd-129">Block override of encryption scope from the container default.</span></span>

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

### <span data-ttu-id="238cd-130">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="238cd-130">-PublicAccess</span></span>
<span data-ttu-id="238cd-131">容器 PublicAccess</span><span class="sxs-lookup"><span data-stu-id="238cd-131">Container PublicAccess</span></span>

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

### <span data-ttu-id="238cd-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="238cd-132">-ResourceGroupName</span></span>
<span data-ttu-id="238cd-133">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="238cd-133">Resource Group Name.</span></span>

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

### <span data-ttu-id="238cd-134">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="238cd-134">-StorageAccount</span></span>
<span data-ttu-id="238cd-135">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="238cd-135">Storage account object</span></span>

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

### <span data-ttu-id="238cd-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="238cd-136">-StorageAccountName</span></span>
<span data-ttu-id="238cd-137">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="238cd-137">Storage Account Name.</span></span>

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

### <span data-ttu-id="238cd-138">-確認</span><span class="sxs-lookup"><span data-stu-id="238cd-138">-Confirm</span></span>
<span data-ttu-id="238cd-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="238cd-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="238cd-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="238cd-140">-WhatIf</span></span>
<span data-ttu-id="238cd-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="238cd-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="238cd-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="238cd-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="238cd-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="238cd-143">CommonParameters</span></span>
<span data-ttu-id="238cd-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="238cd-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="238cd-145">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="238cd-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="238cd-146">輸入</span><span class="sxs-lookup"><span data-stu-id="238cd-146">INPUTS</span></span>

### <span data-ttu-id="238cd-147">System.object</span><span class="sxs-lookup"><span data-stu-id="238cd-147">System.String</span></span>

### <span data-ttu-id="238cd-148">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="238cd-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="238cd-149">輸出</span><span class="sxs-lookup"><span data-stu-id="238cd-149">OUTPUTS</span></span>

### <span data-ttu-id="238cd-150">PSContainer 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="238cd-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="238cd-151">筆記</span><span class="sxs-lookup"><span data-stu-id="238cd-151">NOTES</span></span>

## <span data-ttu-id="238cd-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="238cd-152">RELATED LINKS</span></span>
