---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 9631855803b4ad16312c907c1d1c747b3aee6fdf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137228"
---
# <span data-ttu-id="d57f1-101">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d57f1-101">Set-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="d57f1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d57f1-102">SYNOPSIS</span></span>
<span data-ttu-id="d57f1-103">建立或更新儲存 blob 容器的 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d57f1-103">Creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="d57f1-104">句法</span><span class="sxs-lookup"><span data-stu-id="d57f1-104">SYNTAX</span></span>

### <span data-ttu-id="d57f1-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="d57f1-105">AccountName (Default)</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-ImmutabilityPeriod <Int32>] [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d57f1-106">ExtendAccountName</span><span class="sxs-lookup"><span data-stu-id="d57f1-106">ExtendAccountName</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d57f1-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="d57f1-107">AccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-ImmutabilityPeriod <Int32>] [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d57f1-108">ExtendAccountObject</span><span class="sxs-lookup"><span data-stu-id="d57f1-108">ExtendAccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d57f1-109">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="d57f1-109">ContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-ImmutabilityPeriod <Int32>]
 [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d57f1-110">ExtendContainerObject</span><span class="sxs-lookup"><span data-stu-id="d57f1-110">ExtendContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32> -Etag <String>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d57f1-111">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="d57f1-111">ImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> [-ImmutabilityPeriod <Int32>]
 [-AllowProtectedAppendWrite <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d57f1-112">ExtendImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="d57f1-112">ExtendImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d57f1-113">說明</span><span class="sxs-lookup"><span data-stu-id="d57f1-113">DESCRIPTION</span></span>
<span data-ttu-id="d57f1-114">**AzRmStorageContainerImmutabilityPolicy** Cmdlet 會建立或更新存儲 blob 容器的 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d57f1-114">The **Set-AzRmStorageContainerImmutabilityPolicy** cmdlet creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="d57f1-115">示例</span><span class="sxs-lookup"><span data-stu-id="d57f1-115">EXAMPLES</span></span>

### <span data-ttu-id="d57f1-116">範例1：使用儲存空間帳戶名稱和容器名稱來建立或更新儲存 blob 容器的 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d57f1-116">Example 1: Create or update ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -ImmutabilityPeriod 10
```

<span data-ttu-id="d57f1-117">這個命令會建立或更新包含儲存空間帳戶名稱和容器名稱之儲存 blob 容器的 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="d57f1-117">This command creates or updates ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="d57f1-118">範例2：使用儲存帳戶物件延伸儲存 blob 容器的 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d57f1-118">Example 2: Extend ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -ImmutabilityPeriod 20 -Etag $policy.Etag -ExtendPolicy
```

<span data-ttu-id="d57f1-119">這個命令會擴充 ImmutabilityPolicy 的儲存 blob 容器，其中包含儲存空間帳戶物件。</span><span class="sxs-lookup"><span data-stu-id="d57f1-119">This command extend ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> <span data-ttu-id="d57f1-120">只有在 ImmutabilityPolicy 鎖定之後，才能執行延伸 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="d57f1-120">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

### <span data-ttu-id="d57f1-121">範例3：更新儲存 blob 容器的 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d57f1-121">Example 3: Update ImmutabilityPolicy of a Storage blob container</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 12
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 9 -Etag $policy.Etag
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -AllowProtectedAppendWrite $true
```

<span data-ttu-id="d57f1-122">這個命令會更新存儲容器物件3次的儲存 blob 容器 ImmutabilityPolicy： First to ImmutabilityPeriod 12 天（不含 etag），然後使用 etag ImmutabilityPeriod 9 天，最後啟用 AllowProtectedAppendWrite。</span><span class="sxs-lookup"><span data-stu-id="d57f1-122">This command updates ImmutabilityPolicy of a Storage blob container with Storage container object 3 times: First to ImmutabilityPeriod 12 days without etag, then to ImmutabilityPeriod 9 days with etag, finally enabled AllowProtectedAppendWrite.</span></span>

### <span data-ttu-id="d57f1-123">範例4：使用 ImmutabilityPolicy 物件延伸儲存 blob 容器的 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d57f1-123">Example 4: Extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Set-AzRmStorageContainerImmutabilityPolicy -ImmutabilityPeriod 15 -ExtendPolicy
```

<span data-ttu-id="d57f1-124">這個命令會擴充 ImmutabilityPolicy 的儲存 blob 容器，以及 ImmutabilityPolicy 物件。</span><span class="sxs-lookup"><span data-stu-id="d57f1-124">This command extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> <span data-ttu-id="d57f1-125">只有在 ImmutabilityPolicy 鎖定之後，才能執行延伸 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="d57f1-125">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

## <span data-ttu-id="d57f1-126">參數</span><span class="sxs-lookup"><span data-stu-id="d57f1-126">PARAMETERS</span></span>

### <span data-ttu-id="d57f1-127">-AllowProtectedAppendWrite</span><span class="sxs-lookup"><span data-stu-id="d57f1-127">-AllowProtectedAppendWrite</span></span>
<span data-ttu-id="d57f1-128">這個屬性只能針對未鎖定的時間型保留原則進行變更。</span><span class="sxs-lookup"><span data-stu-id="d57f1-128">This property can only be changed for unlocked time-based retention policies.</span></span> <span data-ttu-id="d57f1-129">啟用這個屬性後，就可以將新的區塊寫入附加的 blob，同時維持不保留的保護與合規性。</span><span class="sxs-lookup"><span data-stu-id="d57f1-129">With this property enabled, new blocks can be written to an append blob while maintaining immutability protection and compliance.</span></span> <span data-ttu-id="d57f1-130">只能新增新的區塊，且無法修改或刪除任何現有區塊。</span><span class="sxs-lookup"><span data-stu-id="d57f1-130">Only new blocks can be added and any existing blocks cannot be modified or deleted.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AccountName, AccountObject, ContainerObject, ImmutabilityPolicyObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d57f1-131">-容器</span><span class="sxs-lookup"><span data-stu-id="d57f1-131">-Container</span></span>
<span data-ttu-id="d57f1-132">儲存容器物件</span><span class="sxs-lookup"><span data-stu-id="d57f1-132">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject, ExtendContainerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d57f1-133">-容器</span><span class="sxs-lookup"><span data-stu-id="d57f1-133">-ContainerName</span></span>
<span data-ttu-id="d57f1-134">容器名稱</span><span class="sxs-lookup"><span data-stu-id="d57f1-134">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, ExtendAccountName, AccountObject, ExtendAccountObject
Aliases: N

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d57f1-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d57f1-135">-DefaultProfile</span></span>
<span data-ttu-id="d57f1-136">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d57f1-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d57f1-137">-Etag</span><span class="sxs-lookup"><span data-stu-id="d57f1-137">-Etag</span></span>
<span data-ttu-id="d57f1-138">永久性原則 etag。</span><span class="sxs-lookup"><span data-stu-id="d57f1-138">Immutability policy etag.</span></span> <span data-ttu-id="d57f1-139">如果未指定-ExtendPolicy，則可選用 Etag;else Etag 是必要的。</span><span class="sxs-lookup"><span data-stu-id="d57f1-139">If -ExtendPolicy is not specified, Etag is optional; else Etag is required.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject
Aliases: IfMatch

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d57f1-140">-ExtendPolicy</span><span class="sxs-lookup"><span data-stu-id="d57f1-140">-ExtendPolicy</span></span>
<span data-ttu-id="d57f1-141">指示 ExtendPolicy 延伸現有的 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="d57f1-141">Indicate ExtendPolicy to Extend an existing ImmutabilityPolicy.</span></span>  <span data-ttu-id="d57f1-142">ImmutabilityPolicy 鎖定之後，只能延伸。</span><span class="sxs-lookup"><span data-stu-id="d57f1-142">After ImmutabilityPolicy is locked, it can only be extend.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject, ExtendImmutabilityPolicyObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d57f1-143">-ImmutabilityPeriod</span><span class="sxs-lookup"><span data-stu-id="d57f1-143">-ImmutabilityPeriod</span></span>
<span data-ttu-id="d57f1-144">在建立天數後的永久性期間。</span><span class="sxs-lookup"><span data-stu-id="d57f1-144">Immutability period since creation in days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: AccountName, AccountObject, ContainerObject, ImmutabilityPolicyObject
Aliases: ImmutabilityPeriodSinceCreationInDays

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject, ExtendImmutabilityPolicyObject
Aliases: ImmutabilityPeriodSinceCreationInDays

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d57f1-145">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d57f1-145">-InputObject</span></span>
<span data-ttu-id="d57f1-146">容器名稱</span><span class="sxs-lookup"><span data-stu-id="d57f1-146">Container Name</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject, ExtendImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d57f1-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d57f1-147">-ResourceGroupName</span></span>
<span data-ttu-id="d57f1-148">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="d57f1-148">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, ExtendAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d57f1-149">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="d57f1-149">-StorageAccount</span></span>
<span data-ttu-id="d57f1-150">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="d57f1-150">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject, ExtendAccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d57f1-151">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d57f1-151">-StorageAccountName</span></span>
<span data-ttu-id="d57f1-152">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="d57f1-152">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, ExtendAccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d57f1-153">-確認</span><span class="sxs-lookup"><span data-stu-id="d57f1-153">-Confirm</span></span>
<span data-ttu-id="d57f1-154">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d57f1-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d57f1-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d57f1-155">-WhatIf</span></span>
<span data-ttu-id="d57f1-156">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d57f1-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d57f1-157">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d57f1-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d57f1-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d57f1-158">CommonParameters</span></span>
<span data-ttu-id="d57f1-159">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d57f1-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d57f1-160">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d57f1-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d57f1-161">輸入</span><span class="sxs-lookup"><span data-stu-id="d57f1-161">INPUTS</span></span>

### <span data-ttu-id="d57f1-162">System.object</span><span class="sxs-lookup"><span data-stu-id="d57f1-162">System.String</span></span>

### <span data-ttu-id="d57f1-163">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="d57f1-163">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="d57f1-164">PSContainer 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="d57f1-164">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="d57f1-165">PSImmutabilityPolicy 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="d57f1-165">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="d57f1-166">輸出</span><span class="sxs-lookup"><span data-stu-id="d57f1-166">OUTPUTS</span></span>

### <span data-ttu-id="d57f1-167">PSImmutabilityPolicy 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="d57f1-167">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="d57f1-168">筆記</span><span class="sxs-lookup"><span data-stu-id="d57f1-168">NOTES</span></span>

## <span data-ttu-id="d57f1-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="d57f1-169">RELATED LINKS</span></span>
