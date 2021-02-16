---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: eedeeb3311373c240cd564534d3438b948c7a0f6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100134418"
---
# <span data-ttu-id="9caef-101">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="9caef-101">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="9caef-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9caef-102">SYNOPSIS</span></span>
<span data-ttu-id="9caef-103">移除已解除鎖定之原則的儲存 blob 容器 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="9caef-103">Removes ImmutabilityPolicy of a Storage blob container with an unlocked policy</span></span>

## <span data-ttu-id="9caef-104">句法</span><span class="sxs-lookup"><span data-stu-id="9caef-104">SYNTAX</span></span>

### <span data-ttu-id="9caef-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="9caef-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9caef-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="9caef-106">AccountObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9caef-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="9caef-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -Etag <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9caef-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="9caef-108">ImmutabilityPolicyObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9caef-109">說明</span><span class="sxs-lookup"><span data-stu-id="9caef-109">DESCRIPTION</span></span>
<span data-ttu-id="9caef-110">**AzRmStorageContainerImmutabilityPolicy** Cmdlet 會移除已解除鎖定的原則 ImmutabilityPolicy 的儲存 blob 容器。</span><span class="sxs-lookup"><span data-stu-id="9caef-110">The **Remove-AzRmStorageContainerImmutabilityPolicy** cmdlet removes ImmutabilityPolicy of a Storage blob container with an unlocked policy.</span></span>

## <span data-ttu-id="9caef-111">示例</span><span class="sxs-lookup"><span data-stu-id="9caef-111">EXAMPLES</span></span>

### <span data-ttu-id="9caef-112">範例1：使用儲存空間帳戶名稱和容器名稱移除儲存 blob 容器的未鎖定 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="9caef-112">Example 1: Remove unlocked ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="9caef-113">這個命令會以儲存空間帳戶名稱和容器名稱移除儲存 blob 容器的解除鎖定的 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="9caef-113">This command removes unlocked ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="9caef-114">範例2：使用儲存帳戶物件移除儲存 blob 容器的解除鎖定 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="9caef-114">Example 2: Remove unlocked ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="9caef-115">這個命令會以儲存帳戶物件移除儲存 blob 容器的解除鎖定的 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="9caef-115">This command removes unlocked ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="9caef-116">範例3：移除已解除鎖定的儲存 blob 容器 ImmutabilityPolicy （含容器物件）</span><span class="sxs-lookup"><span data-stu-id="9caef-116">Example 3: Remove unlocked ImmutabilityPolicy of a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag
```

<span data-ttu-id="9caef-117">這個命令會移除儲存區 blob 容器的已解除鎖定 ImmutabilityPolicy （含儲存容器物件）。</span><span class="sxs-lookup"><span data-stu-id="9caef-117">This command removes unlocked ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="9caef-118">範例4：移除已解除鎖定的儲存 blob 容器 ImmutabilityPolicy，包含 ImmutabilityPolicy 物件</span><span class="sxs-lookup"><span data-stu-id="9caef-118">Example 4: Remove unlocked ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Remove-AzRmStorageContainerImmutabilityPolicy
```

<span data-ttu-id="9caef-119">這個命令會移除已解除鎖定的儲存 blob 容器 ImmutabilityPolicy，以及 ImmutabilityPolicy 物件。</span><span class="sxs-lookup"><span data-stu-id="9caef-119">This command removes unlocked ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span>

## <span data-ttu-id="9caef-120">參數</span><span class="sxs-lookup"><span data-stu-id="9caef-120">PARAMETERS</span></span>

### <span data-ttu-id="9caef-121">-容器</span><span class="sxs-lookup"><span data-stu-id="9caef-121">-Container</span></span>
<span data-ttu-id="9caef-122">儲存容器物件</span><span class="sxs-lookup"><span data-stu-id="9caef-122">Storage container object</span></span>

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

### <span data-ttu-id="9caef-123">-容器</span><span class="sxs-lookup"><span data-stu-id="9caef-123">-ContainerName</span></span>
<span data-ttu-id="9caef-124">容器名稱</span><span class="sxs-lookup"><span data-stu-id="9caef-124">Container Name</span></span>

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

### <span data-ttu-id="9caef-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9caef-125">-DefaultProfile</span></span>
<span data-ttu-id="9caef-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9caef-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9caef-127">-Etag</span><span class="sxs-lookup"><span data-stu-id="9caef-127">-Etag</span></span>
<span data-ttu-id="9caef-128">永久性原則 etag。</span><span class="sxs-lookup"><span data-stu-id="9caef-128">Immutability policy etag.</span></span>

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

### <span data-ttu-id="9caef-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9caef-129">-InputObject</span></span>
<span data-ttu-id="9caef-130">已解除鎖定的 ImmutabilityPolicy 物件以移除</span><span class="sxs-lookup"><span data-stu-id="9caef-130">Unlocked ImmutabilityPolicy Object to Remove</span></span>

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

### <span data-ttu-id="9caef-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9caef-131">-ResourceGroupName</span></span>
<span data-ttu-id="9caef-132">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="9caef-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="9caef-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="9caef-133">-StorageAccount</span></span>
<span data-ttu-id="9caef-134">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="9caef-134">Storage account object</span></span>

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

### <span data-ttu-id="9caef-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9caef-135">-StorageAccountName</span></span>
<span data-ttu-id="9caef-136">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="9caef-136">Storage Account Name.</span></span>

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

### <span data-ttu-id="9caef-137">-確認</span><span class="sxs-lookup"><span data-stu-id="9caef-137">-Confirm</span></span>
<span data-ttu-id="9caef-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9caef-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9caef-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9caef-139">-WhatIf</span></span>
<span data-ttu-id="9caef-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9caef-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9caef-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9caef-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9caef-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9caef-142">CommonParameters</span></span>
<span data-ttu-id="9caef-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9caef-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9caef-144">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9caef-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9caef-145">輸入</span><span class="sxs-lookup"><span data-stu-id="9caef-145">INPUTS</span></span>

### <span data-ttu-id="9caef-146">System.object</span><span class="sxs-lookup"><span data-stu-id="9caef-146">System.String</span></span>

### <span data-ttu-id="9caef-147">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="9caef-147">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="9caef-148">PSContainer 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="9caef-148">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="9caef-149">PSImmutabilityPolicy 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="9caef-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="9caef-150">輸出</span><span class="sxs-lookup"><span data-stu-id="9caef-150">OUTPUTS</span></span>

### <span data-ttu-id="9caef-151">PSImmutabilityPolicy 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="9caef-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="9caef-152">筆記</span><span class="sxs-lookup"><span data-stu-id="9caef-152">NOTES</span></span>

## <span data-ttu-id="9caef-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="9caef-153">RELATED LINKS</span></span>
