---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/set-azurermstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Set-AzureRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Set-AzureRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 7717aaa76efba736015a1cf762c95af440b28218
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450154"
---
# <span data-ttu-id="5055e-101">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="5055e-101">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="5055e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5055e-102">SYNOPSIS</span></span>
<span data-ttu-id="5055e-103">建立或更新儲存 blob 容器的 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="5055e-103">Creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5055e-104">句法</span><span class="sxs-lookup"><span data-stu-id="5055e-104">SYNTAX</span></span>

### <span data-ttu-id="5055e-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="5055e-105">AccountName (Default)</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> -ImmutabilityPeriod <Int32> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5055e-106">ExtendAccountName</span><span class="sxs-lookup"><span data-stu-id="5055e-106">ExtendAccountName</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5055e-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="5055e-107">AccountObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5055e-108">ExtendAccountObject</span><span class="sxs-lookup"><span data-stu-id="5055e-108">ExtendAccountObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5055e-109">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="5055e-109">ContainerObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5055e-110">ExtendContainerObject</span><span class="sxs-lookup"><span data-stu-id="5055e-110">ExtendContainerObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32>
 -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5055e-111">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="5055e-111">ImmutabilityPolicyObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy -InputObject <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5055e-112">ExtendImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="5055e-112">ExtendImmutabilityPolicyObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy -InputObject <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5055e-113">說明</span><span class="sxs-lookup"><span data-stu-id="5055e-113">DESCRIPTION</span></span>
<span data-ttu-id="5055e-114">**AzureRmStorageContainerImmutabilityPolicy** Cmdlet 會建立或更新存儲 blob 容器的 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="5055e-114">The **Set-AzureRmStorageContainerImmutabilityPolicy** cmdlet creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="5055e-115">示例</span><span class="sxs-lookup"><span data-stu-id="5055e-115">EXAMPLES</span></span>

### <span data-ttu-id="5055e-116">範例1：使用儲存空間帳戶名稱和容器名稱來建立或更新儲存 blob 容器的 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="5055e-116">Example 1: Create or update ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Set-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -ImmutabilityPeriod 10 
```

<span data-ttu-id="5055e-117">這個命令會建立或更新包含儲存空間帳戶名稱和容器名稱之儲存 blob 容器的 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="5055e-117">This command creates or updates ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="5055e-118">範例2：使用儲存帳戶物件延伸儲存 blob 容器的 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="5055e-118">Example 2: Extend ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Set-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -ImmutabilityPeriod 20 -Etag $policy.Etag -ExtendPolicy
```

<span data-ttu-id="5055e-119">這個命令會擴充 ImmutabilityPolicy 的儲存 blob 容器，其中包含儲存空間帳戶物件。</span><span class="sxs-lookup"><span data-stu-id="5055e-119">This command extend ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> <span data-ttu-id="5055e-120">只有在 ImmutabilityPolicy 鎖定之後，才能執行延伸 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="5055e-120">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

### <span data-ttu-id="5055e-121">範例3：更新 ImmutabilityPolicyof 儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="5055e-121">Example 3: Update ImmutabilityPolicyof a Storage blob container</span></span> 
```
PS C:\>$containerObject = Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Set-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 12
PS C:\>$policy = Set-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 9 -Etag $policy.Etag
```

<span data-ttu-id="5055e-122">這個命令會更新存儲容器物件為2次的儲存 blob 容器 ImmutabilityPolicy，第一次為 ImmutabilityPeriod 12 天（沒有 etag），然後使用 etag ImmutabilityPeriod 9 天。</span><span class="sxs-lookup"><span data-stu-id="5055e-122">This command updates ImmutabilityPolicy of a Storage blob container with Storage container object 2 times, first to ImmutabilityPeriod 12 days without etag, then to ImmutabilityPeriod 9 days with etag.</span></span>

### <span data-ttu-id="5055e-123">範例4：使用 ImmutabilityPolicy 物件延伸儲存 blob 容器的 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="5055e-123">Example 4: Extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Set-AzureRmStorageContainerImmutabilityPolicy -ImmutabilityPeriod 15 -ExtendPolicy
```

<span data-ttu-id="5055e-124">這個命令會擴充 ImmutabilityPolicy 的儲存 blob 容器，以及 ImmutabilityPolicy 物件。</span><span class="sxs-lookup"><span data-stu-id="5055e-124">This command extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> <span data-ttu-id="5055e-125">只有在 ImmutabilityPolicy 鎖定之後，才能執行延伸 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="5055e-125">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

## <span data-ttu-id="5055e-126">參數</span><span class="sxs-lookup"><span data-stu-id="5055e-126">PARAMETERS</span></span>

### <span data-ttu-id="5055e-127">-容器</span><span class="sxs-lookup"><span data-stu-id="5055e-127">-Container</span></span>
<span data-ttu-id="5055e-128">儲存容器物件</span><span class="sxs-lookup"><span data-stu-id="5055e-128">Storage container object</span></span>

```yaml
Type: PSContainer
Parameter Sets: ContainerObject, ExtendContainerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5055e-129">-容器</span><span class="sxs-lookup"><span data-stu-id="5055e-129">-ContainerName</span></span>
<span data-ttu-id="5055e-130">容器名稱</span><span class="sxs-lookup"><span data-stu-id="5055e-130">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, ExtendAccountName, AccountObject, ExtendAccountObject
Aliases: N

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5055e-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5055e-131">-DefaultProfile</span></span>
<span data-ttu-id="5055e-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5055e-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5055e-133">-Etag</span><span class="sxs-lookup"><span data-stu-id="5055e-133">-Etag</span></span>
<span data-ttu-id="5055e-134">永久性原則 etag。</span><span class="sxs-lookup"><span data-stu-id="5055e-134">Immutability policy etag.</span></span> <span data-ttu-id="5055e-135">如果未指定-ExtendPolicy，則可選用 Etag;else Etag 是必要的。</span><span class="sxs-lookup"><span data-stu-id="5055e-135">If -ExtendPolicy is not specified, Etag is optional; else Etag is required.</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject
Aliases: IfMatch

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5055e-136">-ExtendPolicy</span><span class="sxs-lookup"><span data-stu-id="5055e-136">-ExtendPolicy</span></span>
<span data-ttu-id="5055e-137">指示 ExtendPolicy 延伸現有的 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="5055e-137">Indicate ExtendPolicy to Extend an existing ImmutabilityPolicy.</span></span>  <span data-ttu-id="5055e-138">ImmutabilityPolicy 鎖定之後，只能延伸。</span><span class="sxs-lookup"><span data-stu-id="5055e-138">After ImmutabilityPolicy is locked, it can only be extend.</span></span> 

```yaml
Type: SwitchParameter
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject, ExtendImmutabilityPolicyObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5055e-139">-ImmutabilityPeriod</span><span class="sxs-lookup"><span data-stu-id="5055e-139">-ImmutabilityPeriod</span></span>
<span data-ttu-id="5055e-140">在建立天數後的永久性期間。</span><span class="sxs-lookup"><span data-stu-id="5055e-140">Immutability period since creation in days.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: ImmutabilityPeriodSinceCreationInDays

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5055e-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5055e-141">-InputObject</span></span>
<span data-ttu-id="5055e-142">容器名稱</span><span class="sxs-lookup"><span data-stu-id="5055e-142">Container Name</span></span>

```yaml
Type: PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject, ExtendImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5055e-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5055e-143">-ResourceGroupName</span></span>
<span data-ttu-id="5055e-144">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="5055e-144">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName, ExtendAccountName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5055e-145">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="5055e-145">-StorageAccount</span></span>
<span data-ttu-id="5055e-146">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="5055e-146">Storage account object</span></span>

```yaml
Type: PSStorageAccount
Parameter Sets: AccountObject, ExtendAccountObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5055e-147">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5055e-147">-StorageAccountName</span></span>
<span data-ttu-id="5055e-148">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="5055e-148">Storage Account Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName, ExtendAccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5055e-149">-確認</span><span class="sxs-lookup"><span data-stu-id="5055e-149">-Confirm</span></span>
<span data-ttu-id="5055e-150">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5055e-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5055e-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5055e-151">-WhatIf</span></span>
<span data-ttu-id="5055e-152">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5055e-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5055e-153">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5055e-153">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5055e-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5055e-154">CommonParameters</span></span>
<span data-ttu-id="5055e-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5055e-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5055e-156">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5055e-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5055e-157">輸入</span><span class="sxs-lookup"><span data-stu-id="5055e-157">INPUTS</span></span>

### <span data-ttu-id="5055e-158">System.object</span><span class="sxs-lookup"><span data-stu-id="5055e-158">System.String</span></span>
<span data-ttu-id="5055e-159">PSImmutabilityPolicy 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="5055e-159">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="5055e-160">輸出</span><span class="sxs-lookup"><span data-stu-id="5055e-160">OUTPUTS</span></span>

### <span data-ttu-id="5055e-161">PSImmutabilityPolicy 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="5055e-161">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="5055e-162">筆記</span><span class="sxs-lookup"><span data-stu-id="5055e-162">NOTES</span></span>

## <span data-ttu-id="5055e-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="5055e-163">RELATED LINKS</span></span>

