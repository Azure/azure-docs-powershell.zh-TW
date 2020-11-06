---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 74963ef36a33bed6145d315f5792aa776a36bc7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450159"
---
# <span data-ttu-id="aa100-101">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="aa100-101">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="aa100-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aa100-102">SYNOPSIS</span></span>
<span data-ttu-id="aa100-103">移除儲存 blob 容器的 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="aa100-103">Removes ImmutabilityPolicy of a Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa100-104">句法</span><span class="sxs-lookup"><span data-stu-id="aa100-104">SYNTAX</span></span>

### <span data-ttu-id="aa100-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="aa100-105">AccountName (Default)</span></span>
```
Remove-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa100-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="aa100-106">AccountObject</span></span>
```
Remove-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa100-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="aa100-107">ContainerObject</span></span>
```
Remove-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa100-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="aa100-108">ImmutabilityPolicyObject</span></span>
```
Remove-AzureRmStorageContainerImmutabilityPolicy -InputObject <PSImmutabilityPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa100-109">說明</span><span class="sxs-lookup"><span data-stu-id="aa100-109">DESCRIPTION</span></span>
<span data-ttu-id="aa100-110">**AzureRmStorageContainerImmutabilityPolicy** Cmdlet 會移除存儲 blob 容器的 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="aa100-110">The **Remove-AzureRmStorageContainerImmutabilityPolicy** cmdlet removes ImmutabilityPolicy of a Storage blob containers.</span></span>

## <span data-ttu-id="aa100-111">示例</span><span class="sxs-lookup"><span data-stu-id="aa100-111">EXAMPLES</span></span>

### <span data-ttu-id="aa100-112">範例1：移除含儲存空間帳戶名稱和容器名稱的儲存 blob 容器 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="aa100-112">Example 1: Remove ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Remove-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="aa100-113">這個命令會移除含有儲存空間帳戶名稱和容器名稱的儲存 blob 容器 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="aa100-113">This command removes ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="aa100-114">範例2：移除含儲存空間帳戶物件的儲存 blob 容器 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="aa100-114">Example 2: Remove ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Remove-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="aa100-115">這個命令會以儲存空間帳戶物件移除儲存 blob 容器的 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="aa100-115">This command removes ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="aa100-116">範例3：使用容器物件移除 ImmutabilityPolicyof 儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="aa100-116">Example 3: Remove ImmutabilityPolicyof a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Remove-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag
```

<span data-ttu-id="aa100-117">這個命令會移除含儲存容器物件之儲存 blob 容器的 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="aa100-117">This command removes ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="aa100-118">範例4：移除含 ImmutabilityPolicy 物件的儲存 blob 容器 ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="aa100-118">Example 4: Remove ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Remove-AzureRmStorageContainerImmutabilityPolicy
```

<span data-ttu-id="aa100-119">這個命令會移除含 ImmutabilityPolicy 物件的儲存 blob 容器 ImmutabilityPolicy。</span><span class="sxs-lookup"><span data-stu-id="aa100-119">This command removes ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span>

## <span data-ttu-id="aa100-120">參數</span><span class="sxs-lookup"><span data-stu-id="aa100-120">PARAMETERS</span></span>

### <span data-ttu-id="aa100-121">-容器</span><span class="sxs-lookup"><span data-stu-id="aa100-121">-Container</span></span>
<span data-ttu-id="aa100-122">儲存容器物件</span><span class="sxs-lookup"><span data-stu-id="aa100-122">Storage container object</span></span>

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

### <span data-ttu-id="aa100-123">-容器</span><span class="sxs-lookup"><span data-stu-id="aa100-123">-ContainerName</span></span>
<span data-ttu-id="aa100-124">容器名稱</span><span class="sxs-lookup"><span data-stu-id="aa100-124">Container Name</span></span>

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

### <span data-ttu-id="aa100-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa100-125">-DefaultProfile</span></span>
<span data-ttu-id="aa100-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="aa100-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa100-127">-Etag</span><span class="sxs-lookup"><span data-stu-id="aa100-127">-Etag</span></span>
<span data-ttu-id="aa100-128">永久性原則 etag。</span><span class="sxs-lookup"><span data-stu-id="aa100-128">Immutability policy etag.</span></span>

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

### <span data-ttu-id="aa100-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa100-129">-InputObject</span></span>
<span data-ttu-id="aa100-130">要移除的 ImmutabilityPolicy 物件</span><span class="sxs-lookup"><span data-stu-id="aa100-130">ImmutabilityPolicy Object to Remove</span></span>

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

### <span data-ttu-id="aa100-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa100-131">-ResourceGroupName</span></span>
<span data-ttu-id="aa100-132">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="aa100-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="aa100-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="aa100-133">-StorageAccount</span></span>
<span data-ttu-id="aa100-134">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="aa100-134">Storage account object</span></span>

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

### <span data-ttu-id="aa100-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="aa100-135">-StorageAccountName</span></span>
<span data-ttu-id="aa100-136">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="aa100-136">Storage Account Name.</span></span>

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

### <span data-ttu-id="aa100-137">-確認</span><span class="sxs-lookup"><span data-stu-id="aa100-137">-Confirm</span></span>
<span data-ttu-id="aa100-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="aa100-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa100-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa100-139">-WhatIf</span></span>
<span data-ttu-id="aa100-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="aa100-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa100-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="aa100-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa100-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa100-142">CommonParameters</span></span>
<span data-ttu-id="aa100-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aa100-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa100-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="aa100-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa100-145">輸入</span><span class="sxs-lookup"><span data-stu-id="aa100-145">INPUTS</span></span>

### <span data-ttu-id="aa100-146">System.object</span><span class="sxs-lookup"><span data-stu-id="aa100-146">System.String</span></span>
<span data-ttu-id="aa100-147">PSImmutabilityPolicy 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="aa100-147">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="aa100-148">輸出</span><span class="sxs-lookup"><span data-stu-id="aa100-148">OUTPUTS</span></span>

### <span data-ttu-id="aa100-149">PSImmutabilityPolicy 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="aa100-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="aa100-150">筆記</span><span class="sxs-lookup"><span data-stu-id="aa100-150">NOTES</span></span>

## <span data-ttu-id="aa100-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="aa100-151">RELATED LINKS</span></span>

