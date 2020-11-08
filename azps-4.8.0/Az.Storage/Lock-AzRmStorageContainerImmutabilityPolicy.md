---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/lock-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Lock-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Lock-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 0cb3a4e65d8e464dda85e18e12dc106620e3eee8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126722"
---
# <span data-ttu-id="306ae-101">Lock-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="306ae-101">Lock-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="306ae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="306ae-102">SYNOPSIS</span></span>
<span data-ttu-id="306ae-103">[鎖定 ImmutabilityPolicy] 儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="306ae-103">Locks ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="306ae-104">句法</span><span class="sxs-lookup"><span data-stu-id="306ae-104">SYNTAX</span></span>

### <span data-ttu-id="306ae-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="306ae-105">AccountName (Default)</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -Etag <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="306ae-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="306ae-106">AccountObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -Etag <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="306ae-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="306ae-107">ContainerObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -Etag <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="306ae-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="306ae-108">ImmutabilityPolicyObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="306ae-109">說明</span><span class="sxs-lookup"><span data-stu-id="306ae-109">DESCRIPTION</span></span>
<span data-ttu-id="306ae-110">**AzRmStorageContainerImmutabilityPolicy** Cmdlet 會鎖定儲存 blob 容器的 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="306ae-110">The **Lock-AzRmStorageContainerImmutabilityPolicy** cmdlet locks ImmutabilityPolicy of a Storage blob containers.</span></span>

## <span data-ttu-id="306ae-111">示例</span><span class="sxs-lookup"><span data-stu-id="306ae-111">EXAMPLES</span></span>

### <span data-ttu-id="306ae-112">範例1：使用儲存空間帳戶名稱和容器名稱來鎖定儲存 blob 容器的 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="306ae-112">Example 1: Lock ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="306ae-113">這個命令會使用儲存空間帳戶名稱和容器名稱來鎖定儲存 blob 容器的 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="306ae-113">This command Locks ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="306ae-114">範例2：使用儲存帳戶物件鎖定儲存 blob 容器的 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="306ae-114">Example 2: Lock ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag -Force
```

<span data-ttu-id="306ae-115">這個命令會以儲存帳戶物件鎖定儲存 blob 容器的 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="306ae-115">This command locks ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="306ae-116">範例3：使用容器物件鎖定 ImmutabilityPolicyof 儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="306ae-116">Example 3: Lock ImmutabilityPolicyof a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag -Force
```

<span data-ttu-id="306ae-117">這個命令會以儲存容器物件鎖定儲存 blob 容器的 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="306ae-117">This command locks ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="306ae-118">範例4：使用 ImmutabilityPolicy 物件鎖定儲存 blob 容器的 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="306ae-118">Example 4: Lock ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Lock-AzRmStorageContainerImmutabilityPolicy -Force
```

<span data-ttu-id="306ae-119">這個命令會使用 ImmutabilityPolicy 物件鎖定儲存 blob 容器的 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="306ae-119">This command locks ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> 

## <span data-ttu-id="306ae-120">參數</span><span class="sxs-lookup"><span data-stu-id="306ae-120">PARAMETERS</span></span>

### <span data-ttu-id="306ae-121">-容器</span><span class="sxs-lookup"><span data-stu-id="306ae-121">-Container</span></span>
<span data-ttu-id="306ae-122">儲存容器物件</span><span class="sxs-lookup"><span data-stu-id="306ae-122">Storage container object</span></span>

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

### <span data-ttu-id="306ae-123">-容器</span><span class="sxs-lookup"><span data-stu-id="306ae-123">-ContainerName</span></span>
<span data-ttu-id="306ae-124">容器名稱</span><span class="sxs-lookup"><span data-stu-id="306ae-124">Container Name</span></span>

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

### <span data-ttu-id="306ae-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="306ae-125">-DefaultProfile</span></span>
<span data-ttu-id="306ae-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="306ae-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="306ae-127">-Etag</span><span class="sxs-lookup"><span data-stu-id="306ae-127">-Etag</span></span>
<span data-ttu-id="306ae-128">永久性原則 etag。</span><span class="sxs-lookup"><span data-stu-id="306ae-128">Immutability policy etag.</span></span>

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

### <span data-ttu-id="306ae-129">-Force</span><span class="sxs-lookup"><span data-stu-id="306ae-129">-Force</span></span>
<span data-ttu-id="306ae-130">強制移除 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="306ae-130">Force to remove the ImmutabilityPolicy.</span></span>

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

### <span data-ttu-id="306ae-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="306ae-131">-InputObject</span></span>
<span data-ttu-id="306ae-132">要移除的 ImmutabilityPolicy 物件</span><span class="sxs-lookup"><span data-stu-id="306ae-132">ImmutabilityPolicy Object to Remove</span></span>

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

### <span data-ttu-id="306ae-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="306ae-133">-ResourceGroupName</span></span>
<span data-ttu-id="306ae-134">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="306ae-134">Resource Group Name.</span></span>

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

### <span data-ttu-id="306ae-135">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="306ae-135">-StorageAccount</span></span>
<span data-ttu-id="306ae-136">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="306ae-136">Storage account object</span></span>

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

### <span data-ttu-id="306ae-137">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="306ae-137">-StorageAccountName</span></span>
<span data-ttu-id="306ae-138">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="306ae-138">Storage Account Name.</span></span>

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

### <span data-ttu-id="306ae-139">-確認</span><span class="sxs-lookup"><span data-stu-id="306ae-139">-Confirm</span></span>
<span data-ttu-id="306ae-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="306ae-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="306ae-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="306ae-141">-WhatIf</span></span>
<span data-ttu-id="306ae-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="306ae-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="306ae-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="306ae-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="306ae-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="306ae-144">CommonParameters</span></span>
<span data-ttu-id="306ae-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="306ae-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="306ae-146">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="306ae-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="306ae-147">輸入</span><span class="sxs-lookup"><span data-stu-id="306ae-147">INPUTS</span></span>

### <span data-ttu-id="306ae-148">System.object</span><span class="sxs-lookup"><span data-stu-id="306ae-148">System.String</span></span>

### <span data-ttu-id="306ae-149">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="306ae-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="306ae-150">PSContainer 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="306ae-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="306ae-151">PSImmutabilityPolicy 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="306ae-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="306ae-152">輸出</span><span class="sxs-lookup"><span data-stu-id="306ae-152">OUTPUTS</span></span>

### <span data-ttu-id="306ae-153">PSImmutabilityPolicy 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="306ae-153">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="306ae-154">筆記</span><span class="sxs-lookup"><span data-stu-id="306ae-154">NOTES</span></span>

## <span data-ttu-id="306ae-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="306ae-155">RELATED LINKS</span></span>
