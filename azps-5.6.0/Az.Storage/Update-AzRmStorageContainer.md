---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/update-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageContainer.md
ms.openlocfilehash: 696070e19f1810ab352abde4ad6248f4bf42b180
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907253"
---
# <span data-ttu-id="36d50-101">Update-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="36d50-101">Update-AzRmStorageContainer</span></span>

## <span data-ttu-id="36d50-102">簡介</span><span class="sxs-lookup"><span data-stu-id="36d50-102">SYNOPSIS</span></span>
<span data-ttu-id="36d50-103">修改儲存 Blob 容器</span><span class="sxs-lookup"><span data-stu-id="36d50-103">Modifies a Storage blob container</span></span>

## <span data-ttu-id="36d50-104">語法</span><span class="sxs-lookup"><span data-stu-id="36d50-104">SYNTAX</span></span>

### <span data-ttu-id="36d50-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="36d50-105">AccountName (Default)</span></span>
```
Update-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36d50-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="36d50-106">AccountObject</span></span>
```
Update-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36d50-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="36d50-107">ContainerObject</span></span>
```
Update-AzRmStorageContainer -InputObject <PSContainer> [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36d50-108">描述</span><span class="sxs-lookup"><span data-stu-id="36d50-108">DESCRIPTION</span></span>
<span data-ttu-id="36d50-109">**Update-AzRmstorageContainer Cmdlet** 會修改儲存 Blob 容器</span><span class="sxs-lookup"><span data-stu-id="36d50-109">The **Update-AzRmStorageContainer** cmdlet modifies a Storage blob container</span></span>

## <span data-ttu-id="36d50-110">例子</span><span class="sxs-lookup"><span data-stu-id="36d50-110">EXAMPLES</span></span>

### <span data-ttu-id="36d50-111">範例 1：使用儲存空間帳戶名稱和容器名稱修改儲存 Blob 容器的中繼資料和公用存取</span><span class="sxs-lookup"><span data-stu-id="36d50-111">Example 1: Modifies a Storage blob container's metadata and public access with Storage account name and container name</span></span>
```
PS C:\>Update-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -PublicAccess Container -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="36d50-112">此命令會修改儲存 Blob 容器的中繼資料，以及儲存帳戶名稱和容器名稱的公用存取。</span><span class="sxs-lookup"><span data-stu-id="36d50-112">This command modifies a Storage blob container's metadata and public access with Storage account name and container name.</span></span>

### <span data-ttu-id="36d50-113">範例 2：停用儲存 Blob 容器上的公用存取與儲存帳戶物件和容器名稱</span><span class="sxs-lookup"><span data-stu-id="36d50-113">Example 2: Disable public access on a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Update-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess None
```

<span data-ttu-id="36d50-114">此命令會停用具有儲存帳戶物件和容器名稱的儲存 Blob 容器上的公用存取。</span><span class="sxs-lookup"><span data-stu-id="36d50-114">This command disables public access on a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="36d50-115">範例 3：將具有管線的儲存體帳戶中所有儲存 Blob 容器的公用存取設為 Blob</span><span class="sxs-lookup"><span data-stu-id="36d50-115">Example 3: Set public access as Blob for all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Update-AzRmStorageContainer -PublicAccess Blob
```

<span data-ttu-id="36d50-116">此命令將具有管線的儲存空間帳戶中所有儲存 Blob 容器的公用存取設為 Blob。</span><span class="sxs-lookup"><span data-stu-id="36d50-116">This command set public access as Blob for all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="36d50-117">參數</span><span class="sxs-lookup"><span data-stu-id="36d50-117">PARAMETERS</span></span>

### <span data-ttu-id="36d50-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36d50-118">-DefaultProfile</span></span>
<span data-ttu-id="36d50-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="36d50-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36d50-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36d50-120">-InputObject</span></span>
<span data-ttu-id="36d50-121">儲存容器物件</span><span class="sxs-lookup"><span data-stu-id="36d50-121">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36d50-122">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="36d50-122">-Metadata</span></span>
<span data-ttu-id="36d50-123">容器中繼資料</span><span class="sxs-lookup"><span data-stu-id="36d50-123">Container Metadata</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36d50-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="36d50-124">-Name</span></span>
<span data-ttu-id="36d50-125">容器名稱</span><span class="sxs-lookup"><span data-stu-id="36d50-125">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36d50-126">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="36d50-126">-PublicAccess</span></span>
<span data-ttu-id="36d50-127">Container PublicAccess</span><span class="sxs-lookup"><span data-stu-id="36d50-127">Container PublicAccess</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSPublicAccess
Parameter Sets: (All)
Aliases:
Accepted values: Container, Blob, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36d50-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36d50-128">-ResourceGroupName</span></span>
<span data-ttu-id="36d50-129">資源組名。</span><span class="sxs-lookup"><span data-stu-id="36d50-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="36d50-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="36d50-130">-StorageAccount</span></span>
<span data-ttu-id="36d50-131">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="36d50-131">Storage account object</span></span>

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

### <span data-ttu-id="36d50-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="36d50-132">-StorageAccountName</span></span>
<span data-ttu-id="36d50-133">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="36d50-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="36d50-134">-確認</span><span class="sxs-lookup"><span data-stu-id="36d50-134">-Confirm</span></span>
<span data-ttu-id="36d50-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="36d50-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36d50-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36d50-136">-WhatIf</span></span>
<span data-ttu-id="36d50-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="36d50-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36d50-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="36d50-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36d50-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36d50-139">CommonParameters</span></span>
<span data-ttu-id="36d50-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="36d50-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36d50-141">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="36d50-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36d50-142">輸入</span><span class="sxs-lookup"><span data-stu-id="36d50-142">INPUTS</span></span>

### <span data-ttu-id="36d50-143">System.String</span><span class="sxs-lookup"><span data-stu-id="36d50-143">System.String</span></span>

### <span data-ttu-id="36d50-144">Microsoft.Azure.Commands.management.storage.models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="36d50-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="36d50-145">Microsoft.Azure.Commands.management.storage.models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="36d50-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="36d50-146">輸出</span><span class="sxs-lookup"><span data-stu-id="36d50-146">OUTPUTS</span></span>

### <span data-ttu-id="36d50-147">Microsoft.Azure.Commands.management.storage.models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="36d50-147">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="36d50-148">筆記</span><span class="sxs-lookup"><span data-stu-id="36d50-148">NOTES</span></span>

## <span data-ttu-id="36d50-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="36d50-149">RELATED LINKS</span></span>
