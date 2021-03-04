---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/remove-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
ms.openlocfilehash: 2de3856a51ce8b55d6db7a82f6e50027b60d9d87
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917301"
---
# <span data-ttu-id="ce07b-101">Remove-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="ce07b-101">Remove-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="ce07b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ce07b-102">SYNOPSIS</span></span>
<span data-ttu-id="ce07b-103">移除儲存目標。</span><span class="sxs-lookup"><span data-stu-id="ce07b-103">Removes a Storage Target.</span></span>

## <span data-ttu-id="ce07b-104">語法</span><span class="sxs-lookup"><span data-stu-id="ce07b-104">SYNTAX</span></span>

```
Remove-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce07b-105">描述</span><span class="sxs-lookup"><span data-stu-id="ce07b-105">DESCRIPTION</span></span>
<span data-ttu-id="ce07b-106">**Remove-AzHpcCacheStorageTarget** Cmdlet 會從 Azure HPC Cache 移除儲存目標。</span><span class="sxs-lookup"><span data-stu-id="ce07b-106">The **Remove-AzHpcCacheStorageTarget** cmdlet removes a Storage Target from Azure HPC Cache.</span></span>

## <span data-ttu-id="ce07b-107">例子</span><span class="sxs-lookup"><span data-stu-id="ce07b-107">EXAMPLES</span></span>

### <span data-ttu-id="ce07b-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="ce07b-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST
```

## <span data-ttu-id="ce07b-109">參數</span><span class="sxs-lookup"><span data-stu-id="ce07b-109">PARAMETERS</span></span>

### <span data-ttu-id="ce07b-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce07b-110">-AsJob</span></span>
<span data-ttu-id="ce07b-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ce07b-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ce07b-112">-CacheName</span><span class="sxs-lookup"><span data-stu-id="ce07b-112">-CacheName</span></span>
<span data-ttu-id="ce07b-113">緩存名稱。</span><span class="sxs-lookup"><span data-stu-id="ce07b-113">Name of cache.</span></span>

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

### <span data-ttu-id="ce07b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce07b-114">-DefaultProfile</span></span>
<span data-ttu-id="ce07b-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ce07b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce07b-116">-強制</span><span class="sxs-lookup"><span data-stu-id="ce07b-116">-Force</span></span>
<span data-ttu-id="ce07b-117">表示 Cmdlet 不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ce07b-117">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="ce07b-118">根據預設，此 Cmdlet 會提示您確認要移除儲存目標。</span><span class="sxs-lookup"><span data-stu-id="ce07b-118">By default, this cmdlet prompts you to confirm that you want to remove the storage target.</span></span>

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

### <span data-ttu-id="ce07b-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="ce07b-119">-Name</span></span>
<span data-ttu-id="ce07b-120">儲存目標的名稱。</span><span class="sxs-lookup"><span data-stu-id="ce07b-120">Name of storage target.</span></span>

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

### <span data-ttu-id="ce07b-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce07b-121">-PassThru</span></span>
<span data-ttu-id="ce07b-122">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="ce07b-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ce07b-123">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="ce07b-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ce07b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce07b-124">-ResourceGroupName</span></span>
<span data-ttu-id="ce07b-125">要從緩存移除儲存目標的資源組名。</span><span class="sxs-lookup"><span data-stu-id="ce07b-125">Name of resource group under which you want to remove storage target from cache.</span></span>

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

### <span data-ttu-id="ce07b-126">-確認</span><span class="sxs-lookup"><span data-stu-id="ce07b-126">-Confirm</span></span>
<span data-ttu-id="ce07b-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ce07b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce07b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce07b-128">-WhatIf</span></span>
<span data-ttu-id="ce07b-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ce07b-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ce07b-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce07b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce07b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce07b-131">CommonParameters</span></span>
<span data-ttu-id="ce07b-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ce07b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce07b-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ce07b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce07b-134">輸入</span><span class="sxs-lookup"><span data-stu-id="ce07b-134">INPUTS</span></span>

### <span data-ttu-id="ce07b-135">System.String</span><span class="sxs-lookup"><span data-stu-id="ce07b-135">System.String</span></span>

## <span data-ttu-id="ce07b-136">輸出</span><span class="sxs-lookup"><span data-stu-id="ce07b-136">OUTPUTS</span></span>

## <span data-ttu-id="ce07b-137">筆記</span><span class="sxs-lookup"><span data-stu-id="ce07b-137">NOTES</span></span>

## <span data-ttu-id="ce07b-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="ce07b-138">RELATED LINKS</span></span>
