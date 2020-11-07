---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: c216765657cc87c958cc20dd0f2014f0e1c16970
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793156"
---
# <span data-ttu-id="60505-101">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="60505-101">Set-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="60505-102">摘要</span><span class="sxs-lookup"><span data-stu-id="60505-102">SYNOPSIS</span></span>
<span data-ttu-id="60505-103">建立或更新儲存 blob 容器的 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="60505-103">Creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="60505-104">句法</span><span class="sxs-lookup"><span data-stu-id="60505-104">SYNTAX</span></span>

### <span data-ttu-id="60505-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="60505-105">AccountName (Default)</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -ImmutabilityPeriod <Int32> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60505-106">ExtendAccountName</span><span class="sxs-lookup"><span data-stu-id="60505-106">ExtendAccountName</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60505-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="60505-107">AccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="60505-108">ExtendAccountObject</span><span class="sxs-lookup"><span data-stu-id="60505-108">ExtendAccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60505-109">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="60505-109">ContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60505-110">ExtendContainerObject</span><span class="sxs-lookup"><span data-stu-id="60505-110">ExtendContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32> -Etag <String>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60505-111">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="60505-111">ImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60505-112">ExtendImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="60505-112">ExtendImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60505-113">說明</span><span class="sxs-lookup"><span data-stu-id="60505-113">DESCRIPTION</span></span>
<span data-ttu-id="60505-114">**AzRmStorageContainerImmutabilityPolicy** Cmdlet 會建立或更新存儲 blob 容器的 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="60505-114">The **Set-AzRmStorageContainerImmutabilityPolicy** cmdlet creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="60505-115">示例</span><span class="sxs-lookup"><span data-stu-id="60505-115">EXAMPLES</span></span>

### <span data-ttu-id="60505-116">範例1：使用儲存空間帳戶名稱和容器名稱來建立或更新儲存 blob 容器的 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="60505-116">Example 1: Create or update ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -ImmutabilityPeriod 10
```

<span data-ttu-id="60505-117">這個命令會建立或更新包含儲存空間帳戶名稱和容器名稱之儲存 blob 容器的 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="60505-117">This command creates or updates ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="60505-118">範例2：使用儲存帳戶物件延伸儲存 blob 容器的 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="60505-118">Example 2: Extend ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -ImmutabilityPeriod 20 -Etag $policy.Etag -ExtendPolicy
```

<span data-ttu-id="60505-119">這個命令會擴充 ImmutabilityPolicy 的儲存 blob 容器，其中包含儲存空間帳戶物件。</span><span class="sxs-lookup"><span data-stu-id="60505-119">This command extend ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> <span data-ttu-id="60505-120">只有在 ImmutabilityPolicy 鎖定之後，才能執行延伸 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="60505-120">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

### <span data-ttu-id="60505-121">範例3：更新 ImmutabilityPolicyof 儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="60505-121">Example 3: Update ImmutabilityPolicyof a Storage blob container</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 12
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 9 -Etag $policy.Etag
```

<span data-ttu-id="60505-122">這個命令會更新存儲容器物件為2次的儲存 blob 容器 ImmutabilityPolicy，第一次為 ImmutabilityPeriod 12 天（沒有 etag），然後使用 etag ImmutabilityPeriod 9 天。</span><span class="sxs-lookup"><span data-stu-id="60505-122">This command updates ImmutabilityPolicy of a Storage blob container with Storage container object 2 times, first to ImmutabilityPeriod 12 days without etag, then to ImmutabilityPeriod 9 days with etag.</span></span>

### <span data-ttu-id="60505-123">範例4：使用 ImmutabilityPolicy 物件延伸儲存 blob 容器的 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="60505-123">Example 4: Extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Set-AzRmStorageContainerImmutabilityPolicy -ImmutabilityPeriod 15 -ExtendPolicy
```

<span data-ttu-id="60505-124">這個命令會擴充 ImmutabilityPolicy 的儲存 blob 容器，以及 ImmutabilityPolicy 物件。</span><span class="sxs-lookup"><span data-stu-id="60505-124">This command extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> <span data-ttu-id="60505-125">只有在 ImmutabilityPolicy 鎖定之後，才能執行延伸 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="60505-125">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

## <span data-ttu-id="60505-126">參數</span><span class="sxs-lookup"><span data-stu-id="60505-126">PARAMETERS</span></span>

### <span data-ttu-id="60505-127">-容器</span><span class="sxs-lookup"><span data-stu-id="60505-127">-Container</span></span>
<span data-ttu-id="60505-128">儲存容器物件</span><span class="sxs-lookup"><span data-stu-id="60505-128">Storage container object</span></span>

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

### <span data-ttu-id="60505-129">-容器</span><span class="sxs-lookup"><span data-stu-id="60505-129">-ContainerName</span></span>
<span data-ttu-id="60505-130">容器名稱</span><span class="sxs-lookup"><span data-stu-id="60505-130">Container Name</span></span>

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

### <span data-ttu-id="60505-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60505-131">-DefaultProfile</span></span>
<span data-ttu-id="60505-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="60505-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60505-133">-Etag</span><span class="sxs-lookup"><span data-stu-id="60505-133">-Etag</span></span>
<span data-ttu-id="60505-134">永久性原則 etag。</span><span class="sxs-lookup"><span data-stu-id="60505-134">Immutability policy etag.</span></span> <span data-ttu-id="60505-135">如果未指定-ExtendPolicy，則可選用 Etag;else Etag 是必要的。</span><span class="sxs-lookup"><span data-stu-id="60505-135">If -ExtendPolicy is not specified, Etag is optional; else Etag is required.</span></span>

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

### <span data-ttu-id="60505-136">-ExtendPolicy</span><span class="sxs-lookup"><span data-stu-id="60505-136">-ExtendPolicy</span></span>
<span data-ttu-id="60505-137">指示 ExtendPolicy 延伸現有的 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="60505-137">Indicate ExtendPolicy to Extend an existing ImmutabilityPolicy.</span></span>  <span data-ttu-id="60505-138">ImmutabilityPolicy 鎖定之後，只能延伸。</span><span class="sxs-lookup"><span data-stu-id="60505-138">After ImmutabilityPolicy is locked, it can only be extend.</span></span> 

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

### <span data-ttu-id="60505-139">-ImmutabilityPeriod</span><span class="sxs-lookup"><span data-stu-id="60505-139">-ImmutabilityPeriod</span></span>
<span data-ttu-id="60505-140">在建立天數後的永久性期間。</span><span class="sxs-lookup"><span data-stu-id="60505-140">Immutability period since creation in days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: ImmutabilityPeriodSinceCreationInDays

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60505-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60505-141">-InputObject</span></span>
<span data-ttu-id="60505-142">容器名稱</span><span class="sxs-lookup"><span data-stu-id="60505-142">Container Name</span></span>

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

### <span data-ttu-id="60505-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60505-143">-ResourceGroupName</span></span>
<span data-ttu-id="60505-144">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="60505-144">Resource Group Name.</span></span>

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

### <span data-ttu-id="60505-145">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="60505-145">-StorageAccount</span></span>
<span data-ttu-id="60505-146">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="60505-146">Storage account object</span></span>

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

### <span data-ttu-id="60505-147">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="60505-147">-StorageAccountName</span></span>
<span data-ttu-id="60505-148">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="60505-148">Storage Account Name.</span></span>

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

### <span data-ttu-id="60505-149">-確認</span><span class="sxs-lookup"><span data-stu-id="60505-149">-Confirm</span></span>
<span data-ttu-id="60505-150">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="60505-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60505-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60505-151">-WhatIf</span></span>
<span data-ttu-id="60505-152">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="60505-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60505-153">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="60505-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60505-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60505-154">CommonParameters</span></span>
<span data-ttu-id="60505-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="60505-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60505-156">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="60505-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60505-157">輸入</span><span class="sxs-lookup"><span data-stu-id="60505-157">INPUTS</span></span>

### <span data-ttu-id="60505-158">System.object</span><span class="sxs-lookup"><span data-stu-id="60505-158">System.String</span></span>

### <span data-ttu-id="60505-159">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="60505-159">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="60505-160">PSContainer 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="60505-160">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="60505-161">PSImmutabilityPolicy 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="60505-161">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="60505-162">輸出</span><span class="sxs-lookup"><span data-stu-id="60505-162">OUTPUTS</span></span>

### <span data-ttu-id="60505-163">PSImmutabilityPolicy 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="60505-163">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="60505-164">筆記</span><span class="sxs-lookup"><span data-stu-id="60505-164">NOTES</span></span>

## <span data-ttu-id="60505-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="60505-165">RELATED LINKS</span></span>
