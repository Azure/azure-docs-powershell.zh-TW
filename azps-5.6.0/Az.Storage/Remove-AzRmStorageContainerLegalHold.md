---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azrmstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerLegalHold.md
ms.openlocfilehash: 9788acb95be63d9e76525cbeaf7904cd260baae0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911250"
---
# <span data-ttu-id="d2469-101">Remove-AzRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="d2469-101">Remove-AzRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="d2469-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d2469-102">SYNOPSIS</span></span>
<span data-ttu-id="d2469-103">移除儲存 Blob 容器中的法律保留標記</span><span class="sxs-lookup"><span data-stu-id="d2469-103">Removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="d2469-104">語法</span><span class="sxs-lookup"><span data-stu-id="d2469-104">SYNTAX</span></span>

### <span data-ttu-id="d2469-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="d2469-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Name <String> -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d2469-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="d2469-106">AccountObject</span></span>
```
Remove-AzRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2469-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="d2469-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2469-108">描述</span><span class="sxs-lookup"><span data-stu-id="d2469-108">DESCRIPTION</span></span>
<span data-ttu-id="d2469-109">**Remove-AzRmStorageContainerLegalHold** Cmdlet 會移除儲存 Blob 容器中的法律保留標記</span><span class="sxs-lookup"><span data-stu-id="d2469-109">The **Remove-AzRmStorageContainerLegalHold** cmdlet removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="d2469-110">例子</span><span class="sxs-lookup"><span data-stu-id="d2469-110">EXAMPLES</span></span>

### <span data-ttu-id="d2469-111">範例 1：移除儲存 Blob 容器中具有儲存帳戶名稱和容器名稱的法律保留標記</span><span class="sxs-lookup"><span data-stu-id="d2469-111">Example 1: Remove legal hold tags from a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1
```

<span data-ttu-id="d2469-112">此命令會移除儲存 Blob 容器中具有儲存帳戶名稱和容器名稱的法律保留標記。</span><span class="sxs-lookup"><span data-stu-id="d2469-112">This command removes legal hold tags from a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="d2469-113">範例 2：移除儲存 Blob 容器中具有儲存帳戶物件和容器名稱的法律保留標記</span><span class="sxs-lookup"><span data-stu-id="d2469-113">Example 2: Remove legal hold tags from a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1,tag2
```

<span data-ttu-id="d2469-114">此命令會移除儲存 Blob 容器中具有儲存帳戶物件和容器名稱的法律保留標記。</span><span class="sxs-lookup"><span data-stu-id="d2469-114">This command removes legal hold tags from a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="d2469-115">範例 3：移除儲存帳戶中具有管線之所有儲存 Blob 容器的法律保留標記</span><span class="sxs-lookup"><span data-stu-id="d2469-115">Example 3: Remove legal hold tags from all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainerLegalHold -Tag  tag1
```

<span data-ttu-id="d2469-116">此命令會從具有管線的儲存空間帳戶內的所有儲存 Blob 容器移除法律保留標記。</span><span class="sxs-lookup"><span data-stu-id="d2469-116">This command removes legal hold tags from all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="d2469-117">參數</span><span class="sxs-lookup"><span data-stu-id="d2469-117">PARAMETERS</span></span>

### <span data-ttu-id="d2469-118">-Container</span><span class="sxs-lookup"><span data-stu-id="d2469-118">-Container</span></span>
<span data-ttu-id="d2469-119">儲存容器物件</span><span class="sxs-lookup"><span data-stu-id="d2469-119">Storage container object</span></span>

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

### <span data-ttu-id="d2469-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2469-120">-DefaultProfile</span></span>
<span data-ttu-id="d2469-121">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d2469-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2469-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="d2469-122">-Name</span></span>
<span data-ttu-id="d2469-123">容器名稱</span><span class="sxs-lookup"><span data-stu-id="d2469-123">Container Name</span></span>

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

### <span data-ttu-id="d2469-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2469-124">-ResourceGroupName</span></span>
<span data-ttu-id="d2469-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="d2469-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="d2469-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="d2469-126">-StorageAccount</span></span>
<span data-ttu-id="d2469-127">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="d2469-127">Storage account object</span></span>

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

### <span data-ttu-id="d2469-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d2469-128">-StorageAccountName</span></span>
<span data-ttu-id="d2469-129">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="d2469-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="d2469-130">-標記</span><span class="sxs-lookup"><span data-stu-id="d2469-130">-Tag</span></span>
<span data-ttu-id="d2469-131">Container LegalHold 標記</span><span class="sxs-lookup"><span data-stu-id="d2469-131">Container LegalHold Tags</span></span>

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

### <span data-ttu-id="d2469-132">-確認</span><span class="sxs-lookup"><span data-stu-id="d2469-132">-Confirm</span></span>
<span data-ttu-id="d2469-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d2469-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2469-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2469-134">-WhatIf</span></span>
<span data-ttu-id="d2469-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d2469-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d2469-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d2469-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2469-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2469-137">CommonParameters</span></span>
<span data-ttu-id="d2469-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d2469-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2469-139">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="d2469-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2469-140">輸入</span><span class="sxs-lookup"><span data-stu-id="d2469-140">INPUTS</span></span>

### <span data-ttu-id="d2469-141">System.String</span><span class="sxs-lookup"><span data-stu-id="d2469-141">System.String</span></span>

### <span data-ttu-id="d2469-142">Microsoft.Azure.Commands.management.storage.models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d2469-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="d2469-143">Microsoft.Azure.Commands.management.storage.models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="d2469-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="d2469-144">輸出</span><span class="sxs-lookup"><span data-stu-id="d2469-144">OUTPUTS</span></span>

### <span data-ttu-id="d2469-145">Microsoft.Azure.Commands.management.storage.models.PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="d2469-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="d2469-146">筆記</span><span class="sxs-lookup"><span data-stu-id="d2469-146">NOTES</span></span>

## <span data-ttu-id="d2469-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="d2469-147">RELATED LINKS</span></span>
