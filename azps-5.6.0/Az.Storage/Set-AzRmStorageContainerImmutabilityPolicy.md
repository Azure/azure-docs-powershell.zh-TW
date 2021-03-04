---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 81db149500ce489801a25437fbb7a50443d7426a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907465"
---
# <span data-ttu-id="a3ed4-101">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a3ed4-101">Set-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="a3ed4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a3ed4-102">SYNOPSIS</span></span>
<span data-ttu-id="a3ed4-103">建立或更新儲存 Blob 容器的可更新性</span><span class="sxs-lookup"><span data-stu-id="a3ed4-103">Creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="a3ed4-104">語法</span><span class="sxs-lookup"><span data-stu-id="a3ed4-104">SYNTAX</span></span>

### <span data-ttu-id="a3ed4-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="a3ed4-105">AccountName (Default)</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-ImmutabilityPeriod <Int32>] [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3ed4-106">ExtendAccountName</span><span class="sxs-lookup"><span data-stu-id="a3ed4-106">ExtendAccountName</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3ed4-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="a3ed4-107">AccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-ImmutabilityPeriod <Int32>] [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3ed4-108">ExtendAccountObject</span><span class="sxs-lookup"><span data-stu-id="a3ed4-108">ExtendAccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3ed4-109">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="a3ed4-109">ContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-ImmutabilityPeriod <Int32>]
 [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3ed4-110">延伸ContainerObject</span><span class="sxs-lookup"><span data-stu-id="a3ed4-110">ExtendContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32> -Etag <String>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3ed4-111">可移動性PolicyObject</span><span class="sxs-lookup"><span data-stu-id="a3ed4-111">ImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> [-ImmutabilityPeriod <Int32>]
 [-AllowProtectedAppendWrite <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a3ed4-112">ExtendImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="a3ed4-112">ExtendImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3ed4-113">描述</span><span class="sxs-lookup"><span data-stu-id="a3ed4-113">DESCRIPTION</span></span>
<span data-ttu-id="a3ed4-114">**Set-AzRmStorageContainerImmutabilityPolidlet** 會建立或更新儲存 Blob 容器的服務性</span><span class="sxs-lookup"><span data-stu-id="a3ed4-114">The **Set-AzRmStorageContainerImmutabilityPolicy** cmdlet creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="a3ed4-115">例子</span><span class="sxs-lookup"><span data-stu-id="a3ed4-115">EXAMPLES</span></span>

### <span data-ttu-id="a3ed4-116">範例 1：使用儲存帳戶名稱和容器名稱來建立或更新儲存 Blob 容器的項項</span><span class="sxs-lookup"><span data-stu-id="a3ed4-116">Example 1: Create or update ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -ImmutabilityPeriod 10
```

<span data-ttu-id="a3ed4-117">此命令會使用儲存帳戶名稱和容器名稱來建立或更新儲存 Blob 容器的一項作業。</span><span class="sxs-lookup"><span data-stu-id="a3ed4-117">This command creates or updates ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="a3ed4-118">範例 2：使用 Storage 帳戶物件擴充儲存 Blob 容器的更新更新</span><span class="sxs-lookup"><span data-stu-id="a3ed4-118">Example 2: Extend ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -ImmutabilityPeriod 20 -Etag $policy.Etag -ExtendPolicy
```

<span data-ttu-id="a3ed4-119">此命令會擴充儲存 Blob 容器的指令性，以及儲存帳戶物件。</span><span class="sxs-lookup"><span data-stu-id="a3ed4-119">This command extend ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> <span data-ttu-id="a3ed4-120">擴充的可操作性Policy 只能在鎖定了一個功能之後才能執行。</span><span class="sxs-lookup"><span data-stu-id="a3ed4-120">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

### <span data-ttu-id="a3ed4-121">範例 3：更新儲存 Blob 容器的更新服務性</span><span class="sxs-lookup"><span data-stu-id="a3ed4-121">Example 3: Update ImmutabilityPolicy of a Storage blob container</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 12
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 9 -Etag $policy.Etag
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -AllowProtectedAppendWrite $true
```

<span data-ttu-id="a3ed4-122">此命令會使用儲存容器物件更新 3 次儲存 Blob 容器的指令性：第一次更新至 12 天不含 etag 的 12 天，然後使用 etag 將 9 天更新為 9 天，最後啟用 AllowProtectedAppendWrite。</span><span class="sxs-lookup"><span data-stu-id="a3ed4-122">This command updates ImmutabilityPolicy of a Storage blob container with Storage container object 3 times: First to ImmutabilityPeriod 12 days without etag, then to ImmutabilityPeriod 9 days with etag, finally enabled AllowProtectedAppendWrite.</span></span>

### <span data-ttu-id="a3ed4-123">範例 4：擴充 Storage Blob 容器的擴充更新性Policy，使用一個可及性Policy 物件</span><span class="sxs-lookup"><span data-stu-id="a3ed4-123">Example 4: Extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Set-AzRmStorageContainerImmutabilityPolicy -ImmutabilityPeriod 15 -ExtendPolicy
```

<span data-ttu-id="a3ed4-124">此命令會擴充儲存 Blob 容器的一項服務性，並包含一個與一個資料標籤物件。</span><span class="sxs-lookup"><span data-stu-id="a3ed4-124">This command extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> <span data-ttu-id="a3ed4-125">擴充的可操作性Policy 只能在鎖定了一個功能之後才能執行。</span><span class="sxs-lookup"><span data-stu-id="a3ed4-125">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

## <span data-ttu-id="a3ed4-126">參數</span><span class="sxs-lookup"><span data-stu-id="a3ed4-126">PARAMETERS</span></span>

### <span data-ttu-id="a3ed4-127">-AllowProtectedAppendWrite</span><span class="sxs-lookup"><span data-stu-id="a3ed4-127">-AllowProtectedAppendWrite</span></span>
<span data-ttu-id="a3ed4-128">此屬性只能針對解除鎖定的時間型保留原則變更。</span><span class="sxs-lookup"><span data-stu-id="a3ed4-128">This property can only be changed for unlocked time-based retention policies.</span></span> <span data-ttu-id="a3ed4-129">啟用此屬性後，新區塊可以寫入至附加 Blob，同時維持可讀性保護與合規性。</span><span class="sxs-lookup"><span data-stu-id="a3ed4-129">With this property enabled, new blocks can be written to an append blob while maintaining immutability protection and compliance.</span></span> <span data-ttu-id="a3ed4-130">只能新增區塊，而且無法修改或刪除任何現有的區塊。</span><span class="sxs-lookup"><span data-stu-id="a3ed4-130">Only new blocks can be added and any existing blocks cannot be modified or deleted.</span></span>

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

### <span data-ttu-id="a3ed4-131">-Container</span><span class="sxs-lookup"><span data-stu-id="a3ed4-131">-Container</span></span>
<span data-ttu-id="a3ed4-132">儲存容器物件</span><span class="sxs-lookup"><span data-stu-id="a3ed4-132">Storage container object</span></span>

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

### <span data-ttu-id="a3ed4-133">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="a3ed4-133">-ContainerName</span></span>
<span data-ttu-id="a3ed4-134">容器名稱</span><span class="sxs-lookup"><span data-stu-id="a3ed4-134">Container Name</span></span>

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

### <span data-ttu-id="a3ed4-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3ed4-135">-DefaultProfile</span></span>
<span data-ttu-id="a3ed4-136">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a3ed4-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3ed4-137">-Etag</span><span class="sxs-lookup"><span data-stu-id="a3ed4-137">-Etag</span></span>
<span data-ttu-id="a3ed4-138">可移動性政策 etag。</span><span class="sxs-lookup"><span data-stu-id="a3ed4-138">Immutability policy etag.</span></span> <span data-ttu-id="a3ed4-139">如果未指定 -ExtendPolicy，則 Etag 為選擇性;否則必須輸入 Etag。</span><span class="sxs-lookup"><span data-stu-id="a3ed4-139">If -ExtendPolicy is not specified, Etag is optional; else Etag is required.</span></span>

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

### <span data-ttu-id="a3ed4-140">-ExtendPolicy</span><span class="sxs-lookup"><span data-stu-id="a3ed4-140">-ExtendPolicy</span></span>
<span data-ttu-id="a3ed4-141">表示延伸策略以延伸現有的客戶服務。</span><span class="sxs-lookup"><span data-stu-id="a3ed4-141">Indicate ExtendPolicy to Extend an existing ImmutabilityPolicy.</span></span>  <span data-ttu-id="a3ed4-142">鎖定了一個可移動策略之後，它只能延伸。</span><span class="sxs-lookup"><span data-stu-id="a3ed4-142">After ImmutabilityPolicy is locked, it can only be extend.</span></span> 

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

### <span data-ttu-id="a3ed4-143">-改善服務</span><span class="sxs-lookup"><span data-stu-id="a3ed4-143">-ImmutabilityPeriod</span></span>
<span data-ttu-id="a3ed4-144">建立後可通性期間 ，以天數表示。</span><span class="sxs-lookup"><span data-stu-id="a3ed4-144">Immutability period since creation in days.</span></span>

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

### <span data-ttu-id="a3ed4-145">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3ed4-145">-InputObject</span></span>
<span data-ttu-id="a3ed4-146">容器名稱</span><span class="sxs-lookup"><span data-stu-id="a3ed4-146">Container Name</span></span>

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

### <span data-ttu-id="a3ed4-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3ed4-147">-ResourceGroupName</span></span>
<span data-ttu-id="a3ed4-148">資源組名。</span><span class="sxs-lookup"><span data-stu-id="a3ed4-148">Resource Group Name.</span></span>

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

### <span data-ttu-id="a3ed4-149">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="a3ed4-149">-StorageAccount</span></span>
<span data-ttu-id="a3ed4-150">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="a3ed4-150">Storage account object</span></span>

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

### <span data-ttu-id="a3ed4-151">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a3ed4-151">-StorageAccountName</span></span>
<span data-ttu-id="a3ed4-152">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="a3ed4-152">Storage Account Name.</span></span>

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

### <span data-ttu-id="a3ed4-153">-確認</span><span class="sxs-lookup"><span data-stu-id="a3ed4-153">-Confirm</span></span>
<span data-ttu-id="a3ed4-154">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a3ed4-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3ed4-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3ed4-155">-WhatIf</span></span>
<span data-ttu-id="a3ed4-156">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a3ed4-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3ed4-157">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a3ed4-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3ed4-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3ed4-158">CommonParameters</span></span>
<span data-ttu-id="a3ed4-159">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a3ed4-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3ed4-160">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a3ed4-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3ed4-161">輸入</span><span class="sxs-lookup"><span data-stu-id="a3ed4-161">INPUTS</span></span>

### <span data-ttu-id="a3ed4-162">System.String</span><span class="sxs-lookup"><span data-stu-id="a3ed4-162">System.String</span></span>

### <span data-ttu-id="a3ed4-163">Microsoft.Azure.Commands.management.storage.models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a3ed4-163">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="a3ed4-164">Microsoft.Azure.Commands.management.storage.models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="a3ed4-164">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="a3ed4-165">Microsoft.Azure.Commands.management.storage.models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a3ed4-165">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="a3ed4-166">輸出</span><span class="sxs-lookup"><span data-stu-id="a3ed4-166">OUTPUTS</span></span>

### <span data-ttu-id="a3ed4-167">Microsoft.Azure.Commands.management.storage.models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a3ed4-167">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="a3ed4-168">筆記</span><span class="sxs-lookup"><span data-stu-id="a3ed4-168">NOTES</span></span>

## <span data-ttu-id="a3ed4-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="a3ed4-169">RELATED LINKS</span></span>
