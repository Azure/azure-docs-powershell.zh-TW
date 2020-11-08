---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/remove-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
ms.openlocfilehash: a3603a1884318f567908937ab880182e0df5ee57
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139253"
---
# <span data-ttu-id="ef744-101">Remove-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="ef744-101">Remove-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="ef744-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ef744-102">SYNOPSIS</span></span>
<span data-ttu-id="ef744-103">移除存儲目標。</span><span class="sxs-lookup"><span data-stu-id="ef744-103">Removes a Storage Target.</span></span>

## <span data-ttu-id="ef744-104">句法</span><span class="sxs-lookup"><span data-stu-id="ef744-104">SYNTAX</span></span>

```
Remove-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef744-105">說明</span><span class="sxs-lookup"><span data-stu-id="ef744-105">DESCRIPTION</span></span>
<span data-ttu-id="ef744-106">**AzHpcCacheStorageTarget** Cmdlet 會從 Azure HPC 緩存中移除存儲目標。</span><span class="sxs-lookup"><span data-stu-id="ef744-106">The **Remove-AzHpcCacheStorageTarget** cmdlet removes a Storage Target from Azure HPC Cache.</span></span>

## <span data-ttu-id="ef744-107">示例</span><span class="sxs-lookup"><span data-stu-id="ef744-107">EXAMPLES</span></span>

### <span data-ttu-id="ef744-108">範例1</span><span class="sxs-lookup"><span data-stu-id="ef744-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST
```

## <span data-ttu-id="ef744-109">參數</span><span class="sxs-lookup"><span data-stu-id="ef744-109">PARAMETERS</span></span>

### <span data-ttu-id="ef744-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ef744-110">-AsJob</span></span>
<span data-ttu-id="ef744-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ef744-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ef744-112">-CacheName</span><span class="sxs-lookup"><span data-stu-id="ef744-112">-CacheName</span></span>
<span data-ttu-id="ef744-113">快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="ef744-113">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef744-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef744-114">-DefaultProfile</span></span>
<span data-ttu-id="ef744-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ef744-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef744-116">-Force</span><span class="sxs-lookup"><span data-stu-id="ef744-116">-Force</span></span>
<span data-ttu-id="ef744-117">表示 Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ef744-117">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="ef744-118">根據預設，這個 Cmdlet 會提示您確認您要移除該儲存空間目標。</span><span class="sxs-lookup"><span data-stu-id="ef744-118">By default, this cmdlet prompts you to confirm that you want to remove the storage target.</span></span>

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

### <span data-ttu-id="ef744-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="ef744-119">-Name</span></span>
<span data-ttu-id="ef744-120">儲存目標的名稱。</span><span class="sxs-lookup"><span data-stu-id="ef744-120">Name of storage target.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageTargetName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef744-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef744-121">-PassThru</span></span>
<span data-ttu-id="ef744-122">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="ef744-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ef744-123">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="ef744-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ef744-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef744-124">-ResourceGroupName</span></span>
<span data-ttu-id="ef744-125">您要從快取中移除存儲目標的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ef744-125">Name of resource group under which you want to remove storage target from cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef744-126">-確認</span><span class="sxs-lookup"><span data-stu-id="ef744-126">-Confirm</span></span>
<span data-ttu-id="ef744-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ef744-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef744-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef744-128">-WhatIf</span></span>
<span data-ttu-id="ef744-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ef744-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef744-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ef744-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef744-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef744-131">CommonParameters</span></span>
<span data-ttu-id="ef744-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ef744-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef744-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ef744-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef744-134">輸入</span><span class="sxs-lookup"><span data-stu-id="ef744-134">INPUTS</span></span>

### <span data-ttu-id="ef744-135">System.object</span><span class="sxs-lookup"><span data-stu-id="ef744-135">System.String</span></span>

## <span data-ttu-id="ef744-136">輸出</span><span class="sxs-lookup"><span data-stu-id="ef744-136">OUTPUTS</span></span>

## <span data-ttu-id="ef744-137">筆記</span><span class="sxs-lookup"><span data-stu-id="ef744-137">NOTES</span></span>

## <span data-ttu-id="ef744-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="ef744-138">RELATED LINKS</span></span>
