---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/lock-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Lock-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Lock-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 44d0f6b9717e51aec508da76a9ef9b776891d8c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912985"
---
# <span data-ttu-id="9a7d3-101">Lock-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="9a7d3-101">Lock-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="9a7d3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9a7d3-102">SYNOPSIS</span></span>
<span data-ttu-id="9a7d3-103">鎖定儲存 Blob 容器的可更新性</span><span class="sxs-lookup"><span data-stu-id="9a7d3-103">Locks ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="9a7d3-104">語法</span><span class="sxs-lookup"><span data-stu-id="9a7d3-104">SYNTAX</span></span>

### <span data-ttu-id="9a7d3-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="9a7d3-105">AccountName (Default)</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -Etag <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a7d3-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="9a7d3-106">AccountObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -Etag <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a7d3-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="9a7d3-107">ContainerObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -Etag <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a7d3-108">可移動性PolicyObject</span><span class="sxs-lookup"><span data-stu-id="9a7d3-108">ImmutabilityPolicyObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a7d3-109">描述</span><span class="sxs-lookup"><span data-stu-id="9a7d3-109">DESCRIPTION</span></span>
<span data-ttu-id="9a7d3-110">**Lock-AzRmStorageContainerImmutabilityPolidlet** 會鎖定儲存 Blob 容器的服務性。</span><span class="sxs-lookup"><span data-stu-id="9a7d3-110">The **Lock-AzRmStorageContainerImmutabilityPolicy** cmdlet locks ImmutabilityPolicy of a Storage blob containers.</span></span>

## <span data-ttu-id="9a7d3-111">例子</span><span class="sxs-lookup"><span data-stu-id="9a7d3-111">EXAMPLES</span></span>

### <span data-ttu-id="9a7d3-112">範例 1：具有儲存帳戶名稱和容器名稱的儲存 Blob 容器的 Lock 就地服務</span><span class="sxs-lookup"><span data-stu-id="9a7d3-112">Example 1: Lock ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="9a7d3-113">此命令會鎖定儲存 Blob 容器的服務性，以及儲存帳戶名稱和容器名稱。</span><span class="sxs-lookup"><span data-stu-id="9a7d3-113">This command Locks ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="9a7d3-114">範例 2：使用 Storage 帳戶物件鎖定儲存 Blob 容器的 Lock 就地服務</span><span class="sxs-lookup"><span data-stu-id="9a7d3-114">Example 2: Lock ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag -Force
```

<span data-ttu-id="9a7d3-115">此命令會鎖定儲存 Blob 容器與儲存空間帳戶物件的一項服務性。</span><span class="sxs-lookup"><span data-stu-id="9a7d3-115">This command locks ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="9a7d3-116">範例 3：使用容器物件鎖定 Storage Blob 容器的 Lock 就地服務</span><span class="sxs-lookup"><span data-stu-id="9a7d3-116">Example 3: Lock ImmutabilityPolicyof a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag -Force
```

<span data-ttu-id="9a7d3-117">此命令會鎖定儲存 Blob 容器與儲存容器物件的ObutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="9a7d3-117">This command locks ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="9a7d3-118">範例 4：鎖定 Storage Blob 容器的就地服務，與一個資料標籤物件</span><span class="sxs-lookup"><span data-stu-id="9a7d3-118">Example 4: Lock ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Lock-AzRmStorageContainerImmutabilityPolicy -Force
```

<span data-ttu-id="9a7d3-119">此命令會鎖定儲存 Blob 容器的一項服務性，以及一個使用一項服務選項的物件。</span><span class="sxs-lookup"><span data-stu-id="9a7d3-119">This command locks ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> 

## <span data-ttu-id="9a7d3-120">參數</span><span class="sxs-lookup"><span data-stu-id="9a7d3-120">PARAMETERS</span></span>

### <span data-ttu-id="9a7d3-121">-Container</span><span class="sxs-lookup"><span data-stu-id="9a7d3-121">-Container</span></span>
<span data-ttu-id="9a7d3-122">儲存容器物件</span><span class="sxs-lookup"><span data-stu-id="9a7d3-122">Storage container object</span></span>

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

### <span data-ttu-id="9a7d3-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="9a7d3-123">-ContainerName</span></span>
<span data-ttu-id="9a7d3-124">容器名稱</span><span class="sxs-lookup"><span data-stu-id="9a7d3-124">Container Name</span></span>

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

### <span data-ttu-id="9a7d3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a7d3-125">-DefaultProfile</span></span>
<span data-ttu-id="9a7d3-126">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9a7d3-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a7d3-127">-Etag</span><span class="sxs-lookup"><span data-stu-id="9a7d3-127">-Etag</span></span>
<span data-ttu-id="9a7d3-128">可移動性政策 etag。</span><span class="sxs-lookup"><span data-stu-id="9a7d3-128">Immutability policy etag.</span></span>

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

### <span data-ttu-id="9a7d3-129">-強制</span><span class="sxs-lookup"><span data-stu-id="9a7d3-129">-Force</span></span>
<span data-ttu-id="9a7d3-130">強制移除可移進性政策。</span><span class="sxs-lookup"><span data-stu-id="9a7d3-130">Force to remove the ImmutabilityPolicy.</span></span>

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

### <span data-ttu-id="9a7d3-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a7d3-131">-InputObject</span></span>
<span data-ttu-id="9a7d3-132">要移除的可移動性Policy 物件</span><span class="sxs-lookup"><span data-stu-id="9a7d3-132">ImmutabilityPolicy Object to Remove</span></span>

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

### <span data-ttu-id="9a7d3-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a7d3-133">-ResourceGroupName</span></span>
<span data-ttu-id="9a7d3-134">資源組名。</span><span class="sxs-lookup"><span data-stu-id="9a7d3-134">Resource Group Name.</span></span>

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

### <span data-ttu-id="9a7d3-135">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="9a7d3-135">-StorageAccount</span></span>
<span data-ttu-id="9a7d3-136">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="9a7d3-136">Storage account object</span></span>

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

### <span data-ttu-id="9a7d3-137">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9a7d3-137">-StorageAccountName</span></span>
<span data-ttu-id="9a7d3-138">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="9a7d3-138">Storage Account Name.</span></span>

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

### <span data-ttu-id="9a7d3-139">-確認</span><span class="sxs-lookup"><span data-stu-id="9a7d3-139">-Confirm</span></span>
<span data-ttu-id="9a7d3-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9a7d3-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a7d3-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a7d3-141">-WhatIf</span></span>
<span data-ttu-id="9a7d3-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9a7d3-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a7d3-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9a7d3-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a7d3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a7d3-144">CommonParameters</span></span>
<span data-ttu-id="9a7d3-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9a7d3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a7d3-146">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="9a7d3-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a7d3-147">輸入</span><span class="sxs-lookup"><span data-stu-id="9a7d3-147">INPUTS</span></span>

### <span data-ttu-id="9a7d3-148">System.String</span><span class="sxs-lookup"><span data-stu-id="9a7d3-148">System.String</span></span>

### <span data-ttu-id="9a7d3-149">Microsoft.Azure.Commands.management.storage.models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9a7d3-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="9a7d3-150">Microsoft.Azure.Commands.management.storage.models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="9a7d3-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="9a7d3-151">Microsoft.Azure.Commands.management.storage.models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="9a7d3-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="9a7d3-152">輸出</span><span class="sxs-lookup"><span data-stu-id="9a7d3-152">OUTPUTS</span></span>

### <span data-ttu-id="9a7d3-153">Microsoft.Azure.Commands.management.storage.models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="9a7d3-153">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="9a7d3-154">筆記</span><span class="sxs-lookup"><span data-stu-id="9a7d3-154">NOTES</span></span>

## <span data-ttu-id="9a7d3-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="9a7d3-155">RELATED LINKS</span></span>
