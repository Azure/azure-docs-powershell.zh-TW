---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
ms.openlocfilehash: d7a4563a32da28215dbb9b6dab2b911a500183a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793093"
---
# <span data-ttu-id="10dff-101">Remove-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="10dff-101">Remove-AzRmStorageContainer</span></span>

## <span data-ttu-id="10dff-102">摘要</span><span class="sxs-lookup"><span data-stu-id="10dff-102">SYNOPSIS</span></span>
<span data-ttu-id="10dff-103">移除儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="10dff-103">Removes a Storage blob container</span></span>

## <span data-ttu-id="10dff-104">句法</span><span class="sxs-lookup"><span data-stu-id="10dff-104">SYNTAX</span></span>

### <span data-ttu-id="10dff-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="10dff-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10dff-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="10dff-106">AccountObject</span></span>
```
Remove-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10dff-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="10dff-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainer -InputObject <PSContainer> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10dff-108">說明</span><span class="sxs-lookup"><span data-stu-id="10dff-108">DESCRIPTION</span></span>
<span data-ttu-id="10dff-109">**AzRmStorageContainer** Cmdlet 會移除存儲 blob 容器</span><span class="sxs-lookup"><span data-stu-id="10dff-109">The **Remove-AzRmStorageContainer** cmdlet removes a Storage blob container</span></span>

## <span data-ttu-id="10dff-110">示例</span><span class="sxs-lookup"><span data-stu-id="10dff-110">EXAMPLES</span></span>

### <span data-ttu-id="10dff-111">範例1：移除含儲存空間帳戶名稱和容器名稱的儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="10dff-111">Example 1: Remove a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="10dff-112">這個命令會移除儲存空間帳戶名稱和容器名稱的儲存 blob 容器。</span><span class="sxs-lookup"><span data-stu-id="10dff-112">This command removes a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="10dff-113">範例2：移除含儲存空間帳戶物件和容器名稱的儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="10dff-113">Example 2: Remove a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="10dff-114">這個命令會移除含儲存空間帳戶物件和容器名稱的儲存 blob 容器。</span><span class="sxs-lookup"><span data-stu-id="10dff-114">This command removes a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="10dff-115">範例3：移除包含管線的儲存空間帳戶中的所有儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="10dff-115">Example 3: Remove all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainer -Force
```

<span data-ttu-id="10dff-116">這個命令會移除含管線的儲存空間帳戶中的所有儲存 blob 容器。</span><span class="sxs-lookup"><span data-stu-id="10dff-116">This command removes all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="10dff-117">參數</span><span class="sxs-lookup"><span data-stu-id="10dff-117">PARAMETERS</span></span>

### <span data-ttu-id="10dff-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10dff-118">-DefaultProfile</span></span>
<span data-ttu-id="10dff-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="10dff-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10dff-120">-Force</span><span class="sxs-lookup"><span data-stu-id="10dff-120">-Force</span></span>
<span data-ttu-id="10dff-121">強制移除容器及其中的所有內容</span><span class="sxs-lookup"><span data-stu-id="10dff-121">Force to remove the container and all content in it</span></span>

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

### <span data-ttu-id="10dff-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10dff-122">-InputObject</span></span>
<span data-ttu-id="10dff-123">儲存容器物件</span><span class="sxs-lookup"><span data-stu-id="10dff-123">Storage container object</span></span>

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

### <span data-ttu-id="10dff-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="10dff-124">-Name</span></span>
<span data-ttu-id="10dff-125">容器名稱</span><span class="sxs-lookup"><span data-stu-id="10dff-125">Container Name</span></span>

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

### <span data-ttu-id="10dff-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="10dff-126">-PassThru</span></span>
<span data-ttu-id="10dff-127">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="10dff-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="10dff-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10dff-128">-ResourceGroupName</span></span>
<span data-ttu-id="10dff-129">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="10dff-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="10dff-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="10dff-130">-StorageAccount</span></span>
<span data-ttu-id="10dff-131">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="10dff-131">Storage account object</span></span>

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

### <span data-ttu-id="10dff-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="10dff-132">-StorageAccountName</span></span>
<span data-ttu-id="10dff-133">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="10dff-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="10dff-134">-確認</span><span class="sxs-lookup"><span data-stu-id="10dff-134">-Confirm</span></span>
<span data-ttu-id="10dff-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="10dff-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10dff-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10dff-136">-WhatIf</span></span>
<span data-ttu-id="10dff-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="10dff-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="10dff-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="10dff-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10dff-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10dff-139">CommonParameters</span></span>
<span data-ttu-id="10dff-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="10dff-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10dff-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="10dff-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10dff-142">輸入</span><span class="sxs-lookup"><span data-stu-id="10dff-142">INPUTS</span></span>

### <span data-ttu-id="10dff-143">System.object</span><span class="sxs-lookup"><span data-stu-id="10dff-143">System.String</span></span>

### <span data-ttu-id="10dff-144">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="10dff-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="10dff-145">PSContainer 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="10dff-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="10dff-146">輸出</span><span class="sxs-lookup"><span data-stu-id="10dff-146">OUTPUTS</span></span>

### <span data-ttu-id="10dff-147">System.object</span><span class="sxs-lookup"><span data-stu-id="10dff-147">System.Boolean</span></span>

## <span data-ttu-id="10dff-148">筆記</span><span class="sxs-lookup"><span data-stu-id="10dff-148">NOTES</span></span>

## <span data-ttu-id="10dff-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="10dff-149">RELATED LINKS</span></span>
