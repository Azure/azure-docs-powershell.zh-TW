---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/remove-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCache.md
ms.openlocfilehash: 12bf101fb404b02fc70cbec9640f5f2bd976107c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917302"
---
# <span data-ttu-id="6f92e-101">Remove-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="6f92e-101">Remove-AzHpcCache</span></span>

## <span data-ttu-id="6f92e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6f92e-102">SYNOPSIS</span></span>
<span data-ttu-id="6f92e-103">移除 HPC Cache。</span><span class="sxs-lookup"><span data-stu-id="6f92e-103">Removes a HPC Cache.</span></span>

## <span data-ttu-id="6f92e-104">語法</span><span class="sxs-lookup"><span data-stu-id="6f92e-104">SYNTAX</span></span>

```
Remove-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f92e-105">描述</span><span class="sxs-lookup"><span data-stu-id="6f92e-105">DESCRIPTION</span></span>
<span data-ttu-id="6f92e-106">**Remove-AzHpcCache** Cmdlet 會移除 Azure HPC Cache。</span><span class="sxs-lookup"><span data-stu-id="6f92e-106">The **Remove-AzHpcCache** cmdlet removes a Azure HPC Cache.</span></span>

## <span data-ttu-id="6f92e-107">例子</span><span class="sxs-lookup"><span data-stu-id="6f92e-107">EXAMPLES</span></span>

### <span data-ttu-id="6f92e-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="6f92e-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="6f92e-109">參數</span><span class="sxs-lookup"><span data-stu-id="6f92e-109">PARAMETERS</span></span>

### <span data-ttu-id="6f92e-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6f92e-110">-AsJob</span></span>
<span data-ttu-id="6f92e-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6f92e-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6f92e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f92e-112">-DefaultProfile</span></span>
<span data-ttu-id="6f92e-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6f92e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f92e-114">-強制</span><span class="sxs-lookup"><span data-stu-id="6f92e-114">-Force</span></span>
<span data-ttu-id="6f92e-115">表示 Cmdlet 不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6f92e-115">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="6f92e-116">根據預設，此 Cmdlet 會提示您確認要移除該緩存。</span><span class="sxs-lookup"><span data-stu-id="6f92e-116">By default, this cmdlet prompts you to confirm that you want to remove the cache.</span></span>

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

### <span data-ttu-id="6f92e-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="6f92e-117">-Name</span></span>
<span data-ttu-id="6f92e-118">緩存名稱。</span><span class="sxs-lookup"><span data-stu-id="6f92e-118">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CacheName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f92e-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f92e-119">-PassThru</span></span>
<span data-ttu-id="6f92e-120">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="6f92e-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6f92e-121">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="6f92e-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6f92e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f92e-122">-ResourceGroupName</span></span>
<span data-ttu-id="6f92e-123">您想要移除緩存的資源組名。</span><span class="sxs-lookup"><span data-stu-id="6f92e-123">Name of resource group under which you want to remove cache.</span></span>

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

### <span data-ttu-id="6f92e-124">-確認</span><span class="sxs-lookup"><span data-stu-id="6f92e-124">-Confirm</span></span>
<span data-ttu-id="6f92e-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6f92e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f92e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f92e-126">-WhatIf</span></span>
<span data-ttu-id="6f92e-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6f92e-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6f92e-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6f92e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f92e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f92e-129">CommonParameters</span></span>
<span data-ttu-id="6f92e-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6f92e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f92e-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6f92e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f92e-132">輸入</span><span class="sxs-lookup"><span data-stu-id="6f92e-132">INPUTS</span></span>

### <span data-ttu-id="6f92e-133">System.String</span><span class="sxs-lookup"><span data-stu-id="6f92e-133">System.String</span></span>

## <span data-ttu-id="6f92e-134">輸出</span><span class="sxs-lookup"><span data-stu-id="6f92e-134">OUTPUTS</span></span>

## <span data-ttu-id="6f92e-135">筆記</span><span class="sxs-lookup"><span data-stu-id="6f92e-135">NOTES</span></span>

## <span data-ttu-id="6f92e-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="6f92e-136">RELATED LINKS</span></span>
