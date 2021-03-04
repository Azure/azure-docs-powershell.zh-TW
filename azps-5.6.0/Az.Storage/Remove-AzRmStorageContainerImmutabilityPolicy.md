---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: d94b84455f18a2823612ae1592e9cb337a4be3c7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906461"
---
# <span data-ttu-id="31b23-101">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="31b23-101">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="31b23-102">簡介</span><span class="sxs-lookup"><span data-stu-id="31b23-102">SYNOPSIS</span></span>
<span data-ttu-id="31b23-103">移除具有解除鎖定之策略的儲存 Blob 容器的可更新性</span><span class="sxs-lookup"><span data-stu-id="31b23-103">Removes ImmutabilityPolicy of a Storage blob container with an unlocked policy</span></span>

## <span data-ttu-id="31b23-104">語法</span><span class="sxs-lookup"><span data-stu-id="31b23-104">SYNTAX</span></span>

### <span data-ttu-id="31b23-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="31b23-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="31b23-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="31b23-106">AccountObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31b23-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="31b23-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -Etag <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31b23-108">可移動性PolicyObject</span><span class="sxs-lookup"><span data-stu-id="31b23-108">ImmutabilityPolicyObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31b23-109">描述</span><span class="sxs-lookup"><span data-stu-id="31b23-109">DESCRIPTION</span></span>
<span data-ttu-id="31b23-110">**Remove-AzRmStorageContainerImmutabilityPolidlet** 會移除具有解除鎖定之策略之儲存 Blob 容器的一切資訊。</span><span class="sxs-lookup"><span data-stu-id="31b23-110">The **Remove-AzRmStorageContainerImmutabilityPolicy** cmdlet removes ImmutabilityPolicy of a Storage blob container with an unlocked policy.</span></span>

## <span data-ttu-id="31b23-111">例子</span><span class="sxs-lookup"><span data-stu-id="31b23-111">EXAMPLES</span></span>

### <span data-ttu-id="31b23-112">範例 1：使用儲存帳戶名稱和容器名稱移除儲存 Blob 容器的未鎖定的 UnlockutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="31b23-112">Example 1: Remove unlocked ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="31b23-113">此命令會移除具有儲存帳戶名稱和容器名稱的儲存 Blob 容器未鎖定的 UnlockutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="31b23-113">This command removes unlocked ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="31b23-114">範例 2：移除儲存 Blob 容器的未鎖定的 UnlockutabilityPolicy，以及儲存帳戶物件</span><span class="sxs-lookup"><span data-stu-id="31b23-114">Example 2: Remove unlocked ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="31b23-115">此命令會移除已解除鎖定的 Storage Blob 容器與儲存空間帳戶物件中的一項作業。</span><span class="sxs-lookup"><span data-stu-id="31b23-115">This command removes unlocked ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="31b23-116">範例 3：移除已解除鎖定的 Storage Blob 容器的 UnlockutabilityPolicy，與容器物件</span><span class="sxs-lookup"><span data-stu-id="31b23-116">Example 3: Remove unlocked ImmutabilityPolicy of a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag
```

<span data-ttu-id="31b23-117">此命令會移除儲存 Blob 容器與儲存容器物件的未鎖定的 Blob 選項。</span><span class="sxs-lookup"><span data-stu-id="31b23-117">This command removes unlocked ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="31b23-118">範例 4：移除已解除鎖定的 Storage Blob 容器的 UnlockutabilityPolicy，With UnlockutabilityPolicy 物件</span><span class="sxs-lookup"><span data-stu-id="31b23-118">Example 4: Remove unlocked ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Remove-AzRmStorageContainerImmutabilityPolicy
```

<span data-ttu-id="31b23-119">此命令會移除已解除鎖定的 Storage Blob 容器的 UnlockutabilityPolicy，以及一個包含一個ObutabilityPolicy 物件。</span><span class="sxs-lookup"><span data-stu-id="31b23-119">This command removes unlocked ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span>

## <span data-ttu-id="31b23-120">參數</span><span class="sxs-lookup"><span data-stu-id="31b23-120">PARAMETERS</span></span>

### <span data-ttu-id="31b23-121">-Container</span><span class="sxs-lookup"><span data-stu-id="31b23-121">-Container</span></span>
<span data-ttu-id="31b23-122">儲存容器物件</span><span class="sxs-lookup"><span data-stu-id="31b23-122">Storage container object</span></span>

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

### <span data-ttu-id="31b23-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="31b23-123">-ContainerName</span></span>
<span data-ttu-id="31b23-124">容器名稱</span><span class="sxs-lookup"><span data-stu-id="31b23-124">Container Name</span></span>

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

### <span data-ttu-id="31b23-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31b23-125">-DefaultProfile</span></span>
<span data-ttu-id="31b23-126">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="31b23-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31b23-127">-Etag</span><span class="sxs-lookup"><span data-stu-id="31b23-127">-Etag</span></span>
<span data-ttu-id="31b23-128">可移動性政策 etag。</span><span class="sxs-lookup"><span data-stu-id="31b23-128">Immutability policy etag.</span></span>

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

### <span data-ttu-id="31b23-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31b23-129">-InputObject</span></span>
<span data-ttu-id="31b23-130">解除鎖定的可移動性Policy 物件以移除</span><span class="sxs-lookup"><span data-stu-id="31b23-130">Unlocked ImmutabilityPolicy Object to Remove</span></span>

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

### <span data-ttu-id="31b23-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31b23-131">-ResourceGroupName</span></span>
<span data-ttu-id="31b23-132">資源組名。</span><span class="sxs-lookup"><span data-stu-id="31b23-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="31b23-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="31b23-133">-StorageAccount</span></span>
<span data-ttu-id="31b23-134">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="31b23-134">Storage account object</span></span>

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

### <span data-ttu-id="31b23-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="31b23-135">-StorageAccountName</span></span>
<span data-ttu-id="31b23-136">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="31b23-136">Storage Account Name.</span></span>

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

### <span data-ttu-id="31b23-137">-確認</span><span class="sxs-lookup"><span data-stu-id="31b23-137">-Confirm</span></span>
<span data-ttu-id="31b23-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="31b23-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31b23-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31b23-139">-WhatIf</span></span>
<span data-ttu-id="31b23-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="31b23-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31b23-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="31b23-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31b23-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31b23-142">CommonParameters</span></span>
<span data-ttu-id="31b23-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="31b23-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31b23-144">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="31b23-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31b23-145">輸入</span><span class="sxs-lookup"><span data-stu-id="31b23-145">INPUTS</span></span>

### <span data-ttu-id="31b23-146">System.String</span><span class="sxs-lookup"><span data-stu-id="31b23-146">System.String</span></span>

### <span data-ttu-id="31b23-147">Microsoft.Azure.Commands.management.storage.models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="31b23-147">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="31b23-148">Microsoft.Azure.Commands.management.storage.models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="31b23-148">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="31b23-149">Microsoft.Azure.Commands.management.storage.models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="31b23-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="31b23-150">輸出</span><span class="sxs-lookup"><span data-stu-id="31b23-150">OUTPUTS</span></span>

### <span data-ttu-id="31b23-151">Microsoft.Azure.Commands.management.storage.models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="31b23-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="31b23-152">筆記</span><span class="sxs-lookup"><span data-stu-id="31b23-152">NOTES</span></span>

## <span data-ttu-id="31b23-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="31b23-153">RELATED LINKS</span></span>
