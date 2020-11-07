---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageContainer.md
ms.openlocfilehash: 3ece496830cf3d6b1618bd410e2352d65f6e2fad
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957436"
---
# <span data-ttu-id="2c005-101">Update-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="2c005-101">Update-AzRmStorageContainer</span></span>

## <span data-ttu-id="2c005-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2c005-102">SYNOPSIS</span></span>
<span data-ttu-id="2c005-103">修改儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="2c005-103">Modifies a Storage blob container</span></span>

## <span data-ttu-id="2c005-104">句法</span><span class="sxs-lookup"><span data-stu-id="2c005-104">SYNTAX</span></span>

### <span data-ttu-id="2c005-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="2c005-105">AccountName (Default)</span></span>
```
Update-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c005-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="2c005-106">AccountObject</span></span>
```
Update-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c005-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="2c005-107">ContainerObject</span></span>
```
Update-AzRmStorageContainer -InputObject <PSContainer> [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c005-108">說明</span><span class="sxs-lookup"><span data-stu-id="2c005-108">DESCRIPTION</span></span>
<span data-ttu-id="2c005-109">**AzRmStorageContainer** Cmdlet 會修改儲存 blob 容器</span><span class="sxs-lookup"><span data-stu-id="2c005-109">The **Update-AzRmStorageContainer** cmdlet modifies a Storage blob container</span></span>

## <span data-ttu-id="2c005-110">示例</span><span class="sxs-lookup"><span data-stu-id="2c005-110">EXAMPLES</span></span>

### <span data-ttu-id="2c005-111">範例1：使用儲存空間帳戶名稱和容器名稱來修改儲存 blob 容器的中繼資料和公用存取</span><span class="sxs-lookup"><span data-stu-id="2c005-111">Example 1: Modifies a Storage blob container's metadata and public access with Storage account name and container name</span></span>
```
PS C:\>Update-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -PublicAccess Container -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="2c005-112">這個命令會使用儲存空間帳戶名稱和容器名稱來修改儲存 blob 容器的中繼資料和公用存取。</span><span class="sxs-lookup"><span data-stu-id="2c005-112">This command modifies a Storage blob container's metadata and public access with Storage account name and container name.</span></span>

### <span data-ttu-id="2c005-113">範例2：停用儲存帳戶物件和容器名稱的儲存 blob 容器上的公用存取</span><span class="sxs-lookup"><span data-stu-id="2c005-113">Example 2: Disable public access on a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Update-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess None
```

<span data-ttu-id="2c005-114">這個命令會停用儲存帳戶物件和容器名稱的儲存 blob 容器上的公用存取。</span><span class="sxs-lookup"><span data-stu-id="2c005-114">This command disables public access on a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="2c005-115">範例3：使用管線在儲存空間帳戶中，將公用存取設為 Blob</span><span class="sxs-lookup"><span data-stu-id="2c005-115">Example 3: Set public access as Blob for all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Update-AzRmStorageContainer -PublicAccess Blob
```

<span data-ttu-id="2c005-116">這個命令會將使用管線的儲存空間帳戶中所有儲存區 blob 容器的公用存取設定為 Blob。</span><span class="sxs-lookup"><span data-stu-id="2c005-116">This command set public access as Blob for all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="2c005-117">參數</span><span class="sxs-lookup"><span data-stu-id="2c005-117">PARAMETERS</span></span>

### <span data-ttu-id="2c005-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c005-118">-DefaultProfile</span></span>
<span data-ttu-id="2c005-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2c005-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c005-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c005-120">-InputObject</span></span>
<span data-ttu-id="2c005-121">儲存容器物件</span><span class="sxs-lookup"><span data-stu-id="2c005-121">Storage container object</span></span>

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

### <span data-ttu-id="2c005-122">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="2c005-122">-Metadata</span></span>
<span data-ttu-id="2c005-123">容器中繼資料</span><span class="sxs-lookup"><span data-stu-id="2c005-123">Container Metadata</span></span>

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

### <span data-ttu-id="2c005-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="2c005-124">-Name</span></span>
<span data-ttu-id="2c005-125">容器名稱</span><span class="sxs-lookup"><span data-stu-id="2c005-125">Container Name</span></span>

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

### <span data-ttu-id="2c005-126">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="2c005-126">-PublicAccess</span></span>
<span data-ttu-id="2c005-127">容器 PublicAccess</span><span class="sxs-lookup"><span data-stu-id="2c005-127">Container PublicAccess</span></span>

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

### <span data-ttu-id="2c005-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c005-128">-ResourceGroupName</span></span>
<span data-ttu-id="2c005-129">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="2c005-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="2c005-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="2c005-130">-StorageAccount</span></span>
<span data-ttu-id="2c005-131">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="2c005-131">Storage account object</span></span>

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

### <span data-ttu-id="2c005-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2c005-132">-StorageAccountName</span></span>
<span data-ttu-id="2c005-133">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="2c005-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="2c005-134">-確認</span><span class="sxs-lookup"><span data-stu-id="2c005-134">-Confirm</span></span>
<span data-ttu-id="2c005-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2c005-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c005-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c005-136">-WhatIf</span></span>
<span data-ttu-id="2c005-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2c005-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c005-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2c005-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c005-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c005-139">CommonParameters</span></span>
<span data-ttu-id="2c005-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2c005-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c005-141">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2c005-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c005-142">輸入</span><span class="sxs-lookup"><span data-stu-id="2c005-142">INPUTS</span></span>

### <span data-ttu-id="2c005-143">System.object</span><span class="sxs-lookup"><span data-stu-id="2c005-143">System.String</span></span>

### <span data-ttu-id="2c005-144">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="2c005-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="2c005-145">PSContainer 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="2c005-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="2c005-146">輸出</span><span class="sxs-lookup"><span data-stu-id="2c005-146">OUTPUTS</span></span>

### <span data-ttu-id="2c005-147">PSContainer 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="2c005-147">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="2c005-148">筆記</span><span class="sxs-lookup"><span data-stu-id="2c005-148">NOTES</span></span>

## <span data-ttu-id="2c005-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="2c005-149">RELATED LINKS</span></span>
