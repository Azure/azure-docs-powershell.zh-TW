---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
ms.openlocfilehash: 467fab7d2d7c344c3ffa2ca631addb538e790101
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911257"
---
# <span data-ttu-id="5e893-101">Remove-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="5e893-101">Remove-AzRmStorageContainer</span></span>

## <span data-ttu-id="5e893-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5e893-102">SYNOPSIS</span></span>
<span data-ttu-id="5e893-103">移除儲存 Blob 容器</span><span class="sxs-lookup"><span data-stu-id="5e893-103">Removes a Storage blob container</span></span>

## <span data-ttu-id="5e893-104">語法</span><span class="sxs-lookup"><span data-stu-id="5e893-104">SYNTAX</span></span>

### <span data-ttu-id="5e893-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="5e893-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e893-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="5e893-106">AccountObject</span></span>
```
Remove-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e893-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="5e893-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainer -InputObject <PSContainer> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e893-108">描述</span><span class="sxs-lookup"><span data-stu-id="5e893-108">DESCRIPTION</span></span>
<span data-ttu-id="5e893-109">**Remove-AzRmstorageContainer Cmdlet** 會移除儲存 Blob 容器</span><span class="sxs-lookup"><span data-stu-id="5e893-109">The **Remove-AzRmStorageContainer** cmdlet removes a Storage blob container</span></span>

## <span data-ttu-id="5e893-110">例子</span><span class="sxs-lookup"><span data-stu-id="5e893-110">EXAMPLES</span></span>

### <span data-ttu-id="5e893-111">範例 1：移除儲存空間 Blob 容器與儲存帳戶名稱和容器名稱</span><span class="sxs-lookup"><span data-stu-id="5e893-111">Example 1: Remove a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="5e893-112">此命令會移除包含儲存帳戶名稱和容器名稱的儲存 Blob 容器。</span><span class="sxs-lookup"><span data-stu-id="5e893-112">This command removes a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="5e893-113">範例 2：移除儲存空間 Blob 容器與儲存帳戶物件和容器名稱</span><span class="sxs-lookup"><span data-stu-id="5e893-113">Example 2: Remove a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="5e893-114">此命令會移除包含儲存帳戶物件和容器名稱的儲存 Blob 容器。</span><span class="sxs-lookup"><span data-stu-id="5e893-114">This command removes a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="5e893-115">範例 3：移除儲存帳戶中具有管線的所有儲存 Blob 容器</span><span class="sxs-lookup"><span data-stu-id="5e893-115">Example 3: Remove all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainer -Force
```

<span data-ttu-id="5e893-116">此命令會移除儲存帳戶中具有管線的所有儲存 Blob 容器。</span><span class="sxs-lookup"><span data-stu-id="5e893-116">This command removes all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="5e893-117">參數</span><span class="sxs-lookup"><span data-stu-id="5e893-117">PARAMETERS</span></span>

### <span data-ttu-id="5e893-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e893-118">-DefaultProfile</span></span>
<span data-ttu-id="5e893-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5e893-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e893-120">-強制</span><span class="sxs-lookup"><span data-stu-id="5e893-120">-Force</span></span>
<span data-ttu-id="5e893-121">強制移除容器及其中所有內容</span><span class="sxs-lookup"><span data-stu-id="5e893-121">Force to remove the container and all content in it</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e893-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e893-122">-InputObject</span></span>
<span data-ttu-id="5e893-123">儲存容器物件</span><span class="sxs-lookup"><span data-stu-id="5e893-123">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e893-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="5e893-124">-Name</span></span>
<span data-ttu-id="5e893-125">容器名稱</span><span class="sxs-lookup"><span data-stu-id="5e893-125">Container Name</span></span>

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

### <span data-ttu-id="5e893-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e893-126">-PassThru</span></span>
<span data-ttu-id="5e893-127">表示此 Cmdlet 會返回 **反映** 作業成功的布林值。</span><span class="sxs-lookup"><span data-stu-id="5e893-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="5e893-128">根據預設，此 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="5e893-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="5e893-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e893-129">-ResourceGroupName</span></span>
<span data-ttu-id="5e893-130">資源組名。</span><span class="sxs-lookup"><span data-stu-id="5e893-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="5e893-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="5e893-131">-StorageAccount</span></span>
<span data-ttu-id="5e893-132">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="5e893-132">Storage account object</span></span>

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

### <span data-ttu-id="5e893-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5e893-133">-StorageAccountName</span></span>
<span data-ttu-id="5e893-134">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="5e893-134">Storage Account Name.</span></span>

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

### <span data-ttu-id="5e893-135">-確認</span><span class="sxs-lookup"><span data-stu-id="5e893-135">-Confirm</span></span>
<span data-ttu-id="5e893-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5e893-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e893-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e893-137">-WhatIf</span></span>
<span data-ttu-id="5e893-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5e893-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5e893-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5e893-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e893-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e893-140">CommonParameters</span></span>
<span data-ttu-id="5e893-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5e893-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e893-142">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="5e893-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e893-143">輸入</span><span class="sxs-lookup"><span data-stu-id="5e893-143">INPUTS</span></span>

### <span data-ttu-id="5e893-144">System.String</span><span class="sxs-lookup"><span data-stu-id="5e893-144">System.String</span></span>

### <span data-ttu-id="5e893-145">Microsoft.Azure.Commands.management.storage.models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5e893-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="5e893-146">Microsoft.Azure.Commands.management.storage.models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="5e893-146">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="5e893-147">輸出</span><span class="sxs-lookup"><span data-stu-id="5e893-147">OUTPUTS</span></span>

### <span data-ttu-id="5e893-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5e893-148">System.Boolean</span></span>

## <span data-ttu-id="5e893-149">筆記</span><span class="sxs-lookup"><span data-stu-id="5e893-149">NOTES</span></span>

## <span data-ttu-id="5e893-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="5e893-150">RELATED LINKS</span></span>
