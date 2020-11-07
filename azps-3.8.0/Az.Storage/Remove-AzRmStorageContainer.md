---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
ms.openlocfilehash: 333df1432ed892e75e0b798f1412cb7b0327a334
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966125"
---
# <span data-ttu-id="e5dcc-101">Remove-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="e5dcc-101">Remove-AzRmStorageContainer</span></span>

## <span data-ttu-id="e5dcc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e5dcc-102">SYNOPSIS</span></span>
<span data-ttu-id="e5dcc-103">移除儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="e5dcc-103">Removes a Storage blob container</span></span>

## <span data-ttu-id="e5dcc-104">句法</span><span class="sxs-lookup"><span data-stu-id="e5dcc-104">SYNTAX</span></span>

### <span data-ttu-id="e5dcc-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="e5dcc-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5dcc-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="e5dcc-106">AccountObject</span></span>
```
Remove-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5dcc-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="e5dcc-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainer -InputObject <PSContainer> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5dcc-108">說明</span><span class="sxs-lookup"><span data-stu-id="e5dcc-108">DESCRIPTION</span></span>
<span data-ttu-id="e5dcc-109">**AzRmStorageContainer** Cmdlet 會移除存儲 blob 容器</span><span class="sxs-lookup"><span data-stu-id="e5dcc-109">The **Remove-AzRmStorageContainer** cmdlet removes a Storage blob container</span></span>

## <span data-ttu-id="e5dcc-110">示例</span><span class="sxs-lookup"><span data-stu-id="e5dcc-110">EXAMPLES</span></span>

### <span data-ttu-id="e5dcc-111">範例1：移除含儲存空間帳戶名稱和容器名稱的儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="e5dcc-111">Example 1: Remove a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="e5dcc-112">這個命令會移除儲存空間帳戶名稱和容器名稱的儲存 blob 容器。</span><span class="sxs-lookup"><span data-stu-id="e5dcc-112">This command removes a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="e5dcc-113">範例2：移除含儲存空間帳戶物件和容器名稱的儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="e5dcc-113">Example 2: Remove a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="e5dcc-114">這個命令會移除含儲存空間帳戶物件和容器名稱的儲存 blob 容器。</span><span class="sxs-lookup"><span data-stu-id="e5dcc-114">This command removes a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="e5dcc-115">範例3：移除包含管線的儲存空間帳戶中的所有儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="e5dcc-115">Example 3: Remove all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainer -Force
```

<span data-ttu-id="e5dcc-116">這個命令會移除含管線的儲存空間帳戶中的所有儲存 blob 容器。</span><span class="sxs-lookup"><span data-stu-id="e5dcc-116">This command removes all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="e5dcc-117">參數</span><span class="sxs-lookup"><span data-stu-id="e5dcc-117">PARAMETERS</span></span>

### <span data-ttu-id="e5dcc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5dcc-118">-DefaultProfile</span></span>
<span data-ttu-id="e5dcc-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e5dcc-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5dcc-120">-Force</span><span class="sxs-lookup"><span data-stu-id="e5dcc-120">-Force</span></span>
<span data-ttu-id="e5dcc-121">強制移除容器及其中的所有內容</span><span class="sxs-lookup"><span data-stu-id="e5dcc-121">Force to remove the container and all content in it</span></span>

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

### <span data-ttu-id="e5dcc-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5dcc-122">-InputObject</span></span>
<span data-ttu-id="e5dcc-123">儲存容器物件</span><span class="sxs-lookup"><span data-stu-id="e5dcc-123">Storage container object</span></span>

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

### <span data-ttu-id="e5dcc-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="e5dcc-124">-Name</span></span>
<span data-ttu-id="e5dcc-125">容器名稱</span><span class="sxs-lookup"><span data-stu-id="e5dcc-125">Container Name</span></span>

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

### <span data-ttu-id="e5dcc-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5dcc-126">-PassThru</span></span>
<span data-ttu-id="e5dcc-127">表示此 Cmdlet 會傳回反映操作成功的 **布林值** 。</span><span class="sxs-lookup"><span data-stu-id="e5dcc-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="e5dcc-128">根據預設，這個 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="e5dcc-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="e5dcc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5dcc-129">-ResourceGroupName</span></span>
<span data-ttu-id="e5dcc-130">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="e5dcc-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="e5dcc-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="e5dcc-131">-StorageAccount</span></span>
<span data-ttu-id="e5dcc-132">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="e5dcc-132">Storage account object</span></span>

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

### <span data-ttu-id="e5dcc-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e5dcc-133">-StorageAccountName</span></span>
<span data-ttu-id="e5dcc-134">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="e5dcc-134">Storage Account Name.</span></span>

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

### <span data-ttu-id="e5dcc-135">-確認</span><span class="sxs-lookup"><span data-stu-id="e5dcc-135">-Confirm</span></span>
<span data-ttu-id="e5dcc-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e5dcc-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5dcc-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5dcc-137">-WhatIf</span></span>
<span data-ttu-id="e5dcc-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e5dcc-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e5dcc-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5dcc-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5dcc-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5dcc-140">CommonParameters</span></span>
<span data-ttu-id="e5dcc-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e5dcc-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5dcc-142">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e5dcc-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5dcc-143">輸入</span><span class="sxs-lookup"><span data-stu-id="e5dcc-143">INPUTS</span></span>

### <span data-ttu-id="e5dcc-144">System.object</span><span class="sxs-lookup"><span data-stu-id="e5dcc-144">System.String</span></span>

### <span data-ttu-id="e5dcc-145">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="e5dcc-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="e5dcc-146">PSContainer 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="e5dcc-146">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="e5dcc-147">輸出</span><span class="sxs-lookup"><span data-stu-id="e5dcc-147">OUTPUTS</span></span>

### <span data-ttu-id="e5dcc-148">System.object</span><span class="sxs-lookup"><span data-stu-id="e5dcc-148">System.Boolean</span></span>

## <span data-ttu-id="e5dcc-149">筆記</span><span class="sxs-lookup"><span data-stu-id="e5dcc-149">NOTES</span></span>

## <span data-ttu-id="e5dcc-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5dcc-150">RELATED LINKS</span></span>
