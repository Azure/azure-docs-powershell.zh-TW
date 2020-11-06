---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: b7686b57175958ec2ce4bd1466ca111cce219e05
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614530"
---
# <span data-ttu-id="a1010-101">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a1010-101">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="a1010-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a1010-102">SYNOPSIS</span></span>
<span data-ttu-id="a1010-103">移除儲存 blob 容器的 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a1010-103">Removes ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="a1010-104">句法</span><span class="sxs-lookup"><span data-stu-id="a1010-104">SYNTAX</span></span>

### <span data-ttu-id="a1010-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="a1010-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a1010-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="a1010-106">AccountObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1010-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="a1010-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -Etag <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1010-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="a1010-108">ImmutabilityPolicyObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1010-109">說明</span><span class="sxs-lookup"><span data-stu-id="a1010-109">DESCRIPTION</span></span>
<span data-ttu-id="a1010-110">**AzRmStorageContainerImmutabilityPolicy** Cmdlet 會移除存儲 blob 容器的 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="a1010-110">The **Remove-AzRmStorageContainerImmutabilityPolicy** cmdlet removes ImmutabilityPolicy of a Storage blob containers.</span></span>

## <span data-ttu-id="a1010-111">示例</span><span class="sxs-lookup"><span data-stu-id="a1010-111">EXAMPLES</span></span>

### <span data-ttu-id="a1010-112">範例1：移除含儲存空間帳戶名稱和容器名稱的儲存 blob 容器 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a1010-112">Example 1: Remove ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="a1010-113">這個命令會移除含有儲存空間帳戶名稱和容器名稱的儲存 blob 容器 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="a1010-113">This command removes ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="a1010-114">範例2：移除含儲存空間帳戶物件的儲存 blob 容器 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a1010-114">Example 2: Remove ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="a1010-115">這個命令會以儲存空間帳戶物件移除儲存 blob 容器的 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="a1010-115">This command removes ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="a1010-116">範例3：使用容器物件移除 ImmutabilityPolicyof 儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="a1010-116">Example 3: Remove ImmutabilityPolicyof a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag
```

<span data-ttu-id="a1010-117">這個命令會移除含儲存容器物件之儲存 blob 容器的 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="a1010-117">This command removes ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="a1010-118">範例4：移除含 ImmutabilityPolicy 物件的儲存 blob 容器 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a1010-118">Example 4: Remove ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Remove-AzRmStorageContainerImmutabilityPolicy
```

<span data-ttu-id="a1010-119">這個命令會移除含 ImmutabilityPolicy 物件的儲存 blob 容器 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="a1010-119">This command removes ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span>

## <span data-ttu-id="a1010-120">參數</span><span class="sxs-lookup"><span data-stu-id="a1010-120">PARAMETERS</span></span>

### <span data-ttu-id="a1010-121">-容器</span><span class="sxs-lookup"><span data-stu-id="a1010-121">-Container</span></span>
<span data-ttu-id="a1010-122">儲存容器物件</span><span class="sxs-lookup"><span data-stu-id="a1010-122">Storage container object</span></span>

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

### <span data-ttu-id="a1010-123">-容器</span><span class="sxs-lookup"><span data-stu-id="a1010-123">-ContainerName</span></span>
<span data-ttu-id="a1010-124">容器名稱</span><span class="sxs-lookup"><span data-stu-id="a1010-124">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1010-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1010-125">-DefaultProfile</span></span>
<span data-ttu-id="a1010-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a1010-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1010-127">-Etag</span><span class="sxs-lookup"><span data-stu-id="a1010-127">-Etag</span></span>
<span data-ttu-id="a1010-128">永久性原則 etag。</span><span class="sxs-lookup"><span data-stu-id="a1010-128">Immutability policy etag.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1010-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1010-129">-InputObject</span></span>
<span data-ttu-id="a1010-130">要移除的 ImmutabilityPolicy 物件</span><span class="sxs-lookup"><span data-stu-id="a1010-130">ImmutabilityPolicy Object to Remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1010-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1010-131">-ResourceGroupName</span></span>
<span data-ttu-id="a1010-132">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="a1010-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="a1010-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="a1010-133">-StorageAccount</span></span>
<span data-ttu-id="a1010-134">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="a1010-134">Storage account object</span></span>

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

### <span data-ttu-id="a1010-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a1010-135">-StorageAccountName</span></span>
<span data-ttu-id="a1010-136">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="a1010-136">Storage Account Name.</span></span>

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

### <span data-ttu-id="a1010-137">-確認</span><span class="sxs-lookup"><span data-stu-id="a1010-137">-Confirm</span></span>
<span data-ttu-id="a1010-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a1010-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1010-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1010-139">-WhatIf</span></span>
<span data-ttu-id="a1010-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a1010-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1010-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a1010-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1010-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1010-142">CommonParameters</span></span>
<span data-ttu-id="a1010-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a1010-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1010-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a1010-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1010-145">輸入</span><span class="sxs-lookup"><span data-stu-id="a1010-145">INPUTS</span></span>

### <span data-ttu-id="a1010-146">System.object</span><span class="sxs-lookup"><span data-stu-id="a1010-146">System.String</span></span>

### <span data-ttu-id="a1010-147">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="a1010-147">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="a1010-148">PSContainer 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="a1010-148">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="a1010-149">PSImmutabilityPolicy 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="a1010-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="a1010-150">輸出</span><span class="sxs-lookup"><span data-stu-id="a1010-150">OUTPUTS</span></span>

### <span data-ttu-id="a1010-151">PSImmutabilityPolicy 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="a1010-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="a1010-152">筆記</span><span class="sxs-lookup"><span data-stu-id="a1010-152">NOTES</span></span>

## <span data-ttu-id="a1010-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="a1010-153">RELATED LINKS</span></span>
