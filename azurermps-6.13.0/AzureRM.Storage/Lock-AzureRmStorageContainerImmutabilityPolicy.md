---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/lock-azurermstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Lock-AzureRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Lock-AzureRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 726dc9043c1082f97e32da46305cf81192e1806c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443692"
---
# <span data-ttu-id="ec047-101">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ec047-101">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="ec047-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ec047-102">SYNOPSIS</span></span>
<span data-ttu-id="ec047-103">[鎖定 ImmutabilityPolicy] 儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="ec047-103">Locks ImmutabilityPolicy of a Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec047-104">句法</span><span class="sxs-lookup"><span data-stu-id="ec047-104">SYNTAX</span></span>

### <span data-ttu-id="ec047-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="ec047-105">AccountName (Default)</span></span>
```
Lock-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> [-Etag] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec047-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="ec047-106">AccountObject</span></span>
```
Lock-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 [-Etag] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec047-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="ec047-107">ContainerObject</span></span>
```
Lock-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec047-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="ec047-108">ImmutabilityPolicyObject</span></span>
```
Lock-AzureRmStorageContainerImmutabilityPolicy -InputObject <PSImmutabilityPolicy> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec047-109">說明</span><span class="sxs-lookup"><span data-stu-id="ec047-109">DESCRIPTION</span></span>
<span data-ttu-id="ec047-110">**AzureRmStorageContainerImmutabilityPolicy** Cmdlet 會鎖定儲存 blob 容器的 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="ec047-110">The **Lock-AzureRmStorageContainerImmutabilityPolicy** cmdlet locks ImmutabilityPolicy of a Storage blob containers.</span></span>

## <span data-ttu-id="ec047-111">示例</span><span class="sxs-lookup"><span data-stu-id="ec047-111">EXAMPLES</span></span>

### <span data-ttu-id="ec047-112">範例1：使用儲存空間帳戶名稱和容器名稱來鎖定儲存 blob 容器的 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ec047-112">Example 1: Lock ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Lock-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="ec047-113">這個命令會使用儲存空間帳戶名稱和容器名稱來鎖定儲存 blob 容器的 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="ec047-113">This command Locks ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="ec047-114">範例2：使用儲存帳戶物件鎖定儲存 blob 容器的 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ec047-114">Example 2: Lock ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Lock-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag -Force
```

<span data-ttu-id="ec047-115">這個命令會以儲存帳戶物件鎖定儲存 blob 容器的 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="ec047-115">This command locks ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="ec047-116">範例3：使用容器物件鎖定 ImmutabilityPolicyof 儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="ec047-116">Example 3: Lock ImmutabilityPolicyof a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Lock-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag -Force
```

<span data-ttu-id="ec047-117">這個命令會以儲存容器物件鎖定儲存 blob 容器的 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="ec047-117">This command locks ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="ec047-118">範例4：使用 ImmutabilityPolicy 物件鎖定儲存 blob 容器的 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ec047-118">Example 4: Lock ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Lock-AzureRmStorageContainerImmutabilityPolicy -Force
```

<span data-ttu-id="ec047-119">這個命令會使用 ImmutabilityPolicy 物件鎖定儲存 blob 容器的 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="ec047-119">This command locks ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> 

## <span data-ttu-id="ec047-120">參數</span><span class="sxs-lookup"><span data-stu-id="ec047-120">PARAMETERS</span></span>

### <span data-ttu-id="ec047-121">-容器</span><span class="sxs-lookup"><span data-stu-id="ec047-121">-Container</span></span>
<span data-ttu-id="ec047-122">儲存容器物件</span><span class="sxs-lookup"><span data-stu-id="ec047-122">Storage container object</span></span>

```yaml
Type: PSContainer
Parameter Sets: ContainerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec047-123">-容器</span><span class="sxs-lookup"><span data-stu-id="ec047-123">-ContainerName</span></span>
<span data-ttu-id="ec047-124">容器名稱</span><span class="sxs-lookup"><span data-stu-id="ec047-124">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject
Aliases: N

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec047-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec047-125">-DefaultProfile</span></span>
<span data-ttu-id="ec047-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ec047-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec047-127">-Etag</span><span class="sxs-lookup"><span data-stu-id="ec047-127">-Etag</span></span>
<span data-ttu-id="ec047-128">永久性原則 etag。</span><span class="sxs-lookup"><span data-stu-id="ec047-128">Immutability policy etag.</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec047-129">-Force</span><span class="sxs-lookup"><span data-stu-id="ec047-129">-Force</span></span>
<span data-ttu-id="ec047-130">強制移除 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="ec047-130">Force to remove the ImmutabilityPolicy.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec047-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec047-131">-InputObject</span></span>
<span data-ttu-id="ec047-132">要移除的 ImmutabilityPolicy 物件</span><span class="sxs-lookup"><span data-stu-id="ec047-132">ImmutabilityPolicy Object to Remove</span></span>

```yaml
Type: PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec047-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec047-133">-ResourceGroupName</span></span>
<span data-ttu-id="ec047-134">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="ec047-134">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec047-135">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="ec047-135">-StorageAccount</span></span>
<span data-ttu-id="ec047-136">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="ec047-136">Storage account object</span></span>

```yaml
Type: PSStorageAccount
Parameter Sets: AccountObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec047-137">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ec047-137">-StorageAccountName</span></span>
<span data-ttu-id="ec047-138">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="ec047-138">Storage Account Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec047-139">-確認</span><span class="sxs-lookup"><span data-stu-id="ec047-139">-Confirm</span></span>
<span data-ttu-id="ec047-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ec047-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec047-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec047-141">-WhatIf</span></span>
<span data-ttu-id="ec047-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ec047-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec047-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ec047-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec047-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec047-144">CommonParameters</span></span>
<span data-ttu-id="ec047-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ec047-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec047-146">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ec047-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec047-147">輸入</span><span class="sxs-lookup"><span data-stu-id="ec047-147">INPUTS</span></span>

### <span data-ttu-id="ec047-148">System.object</span><span class="sxs-lookup"><span data-stu-id="ec047-148">System.String</span></span>
<span data-ttu-id="ec047-149">PSImmutabilityPolicy 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="ec047-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="ec047-150">輸出</span><span class="sxs-lookup"><span data-stu-id="ec047-150">OUTPUTS</span></span>

### <span data-ttu-id="ec047-151">PSImmutabilityPolicy 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="ec047-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="ec047-152">筆記</span><span class="sxs-lookup"><span data-stu-id="ec047-152">NOTES</span></span>

## <span data-ttu-id="ec047-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="ec047-153">RELATED LINKS</span></span>

