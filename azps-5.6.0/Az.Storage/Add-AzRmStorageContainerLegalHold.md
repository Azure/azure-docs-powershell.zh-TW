---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/add-azrmstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzRmStorageContainerLegalHold.md
ms.openlocfilehash: 8b0608a350f73de4280380abf7fd213d48742022
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907970"
---
# <span data-ttu-id="ce88f-101">Add-AzRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="ce88f-101">Add-AzRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="ce88f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ce88f-102">SYNOPSIS</span></span>
<span data-ttu-id="ce88f-103">新增法律保留標記至儲存 Blob 容器</span><span class="sxs-lookup"><span data-stu-id="ce88f-103">Adds legal hold tags to a Storage blob container</span></span>

## <span data-ttu-id="ce88f-104">語法</span><span class="sxs-lookup"><span data-stu-id="ce88f-104">SYNTAX</span></span>

### <span data-ttu-id="ce88f-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="ce88f-105">AccountName (Default)</span></span>
```
Add-AzRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce88f-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="ce88f-106">AccountObject</span></span>
```
Add-AzRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce88f-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="ce88f-107">ContainerObject</span></span>
```
Add-AzRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce88f-108">描述</span><span class="sxs-lookup"><span data-stu-id="ce88f-108">DESCRIPTION</span></span>
<span data-ttu-id="ce88f-109">**Add-AzRmStorageContainerLegalHold** Cmdlet 會將法律保留標記新增到儲存 Blob 容器</span><span class="sxs-lookup"><span data-stu-id="ce88f-109">The **Add-AzRmStorageContainerLegalHold** cmdlet adds legal hold tags to a Storage blob container</span></span>

## <span data-ttu-id="ce88f-110">例子</span><span class="sxs-lookup"><span data-stu-id="ce88f-110">EXAMPLES</span></span>

### <span data-ttu-id="ce88f-111">範例 1：新增具有儲存帳戶名稱和容器名稱之儲存空間 Blob 容器的法律保留標記</span><span class="sxs-lookup"><span data-stu-id="ce88f-111">Example 1: Add legal hold tags to a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Add-AzRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1,tag2
```

<span data-ttu-id="ce88f-112">此命令會新增具有儲存帳戶名稱和容器名稱之儲存空間 Blob 容器的法律保留標記。</span><span class="sxs-lookup"><span data-stu-id="ce88f-112">This command adds legal hold tags to a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="ce88f-113">範例 2：新增具有儲存帳戶物件和容器名稱之儲存空間 Blob 容器的法律保留標記</span><span class="sxs-lookup"><span data-stu-id="ce88f-113">Example 2: Add legal hold tags to a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Add-AzRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1
```

<span data-ttu-id="ce88f-114">此命令會新增具有儲存帳戶物件和容器名稱之儲存空間 Blob 容器的法律保留標記。</span><span class="sxs-lookup"><span data-stu-id="ce88f-114">This command adds legal hold tags to a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="ce88f-115">範例 3：在具有管線的儲存空間帳戶中，將法律保留標記新增到所有儲存 Blob 容器</span><span class="sxs-lookup"><span data-stu-id="ce88f-115">Example 3: Add legal hold tags to all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Add-AzRmStorageContainerLegalHold -Tag  tag1,tag2,tag3
```

<span data-ttu-id="ce88f-116">此命令會將法律保留標記新增到具有管線的儲存空間帳戶內的所有儲存 Blob 容器。</span><span class="sxs-lookup"><span data-stu-id="ce88f-116">This command adds legal hold tags to all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="ce88f-117">參數</span><span class="sxs-lookup"><span data-stu-id="ce88f-117">PARAMETERS</span></span>

### <span data-ttu-id="ce88f-118">-Container</span><span class="sxs-lookup"><span data-stu-id="ce88f-118">-Container</span></span>
<span data-ttu-id="ce88f-119">儲存容器物件</span><span class="sxs-lookup"><span data-stu-id="ce88f-119">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce88f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce88f-120">-DefaultProfile</span></span>
<span data-ttu-id="ce88f-121">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ce88f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce88f-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="ce88f-122">-Name</span></span>
<span data-ttu-id="ce88f-123">容器名稱</span><span class="sxs-lookup"><span data-stu-id="ce88f-123">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce88f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce88f-124">-ResourceGroupName</span></span>
<span data-ttu-id="ce88f-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="ce88f-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce88f-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="ce88f-126">-StorageAccount</span></span>
<span data-ttu-id="ce88f-127">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="ce88f-127">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce88f-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ce88f-128">-StorageAccountName</span></span>
<span data-ttu-id="ce88f-129">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="ce88f-129">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce88f-130">-標記</span><span class="sxs-lookup"><span data-stu-id="ce88f-130">-Tag</span></span>
<span data-ttu-id="ce88f-131">Container LegalHold 標記</span><span class="sxs-lookup"><span data-stu-id="ce88f-131">Container LegalHold Tags</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce88f-132">-確認</span><span class="sxs-lookup"><span data-stu-id="ce88f-132">-Confirm</span></span>
<span data-ttu-id="ce88f-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ce88f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce88f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce88f-134">-WhatIf</span></span>
<span data-ttu-id="ce88f-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ce88f-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ce88f-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce88f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce88f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce88f-137">CommonParameters</span></span>
<span data-ttu-id="ce88f-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ce88f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce88f-139">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ce88f-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce88f-140">輸入</span><span class="sxs-lookup"><span data-stu-id="ce88f-140">INPUTS</span></span>

### <span data-ttu-id="ce88f-141">System.String</span><span class="sxs-lookup"><span data-stu-id="ce88f-141">System.String</span></span>

### <span data-ttu-id="ce88f-142">Microsoft.Azure.Commands.management.storage.models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ce88f-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="ce88f-143">Microsoft.Azure.Commands.management.storage.models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="ce88f-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="ce88f-144">輸出</span><span class="sxs-lookup"><span data-stu-id="ce88f-144">OUTPUTS</span></span>

### <span data-ttu-id="ce88f-145">Microsoft.Azure.Commands.management.storage.models.PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="ce88f-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="ce88f-146">筆記</span><span class="sxs-lookup"><span data-stu-id="ce88f-146">NOTES</span></span>

## <span data-ttu-id="ce88f-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="ce88f-147">RELATED LINKS</span></span>
