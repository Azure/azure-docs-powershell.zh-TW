---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/stop-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Stop-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Stop-AzHpcCache.md
ms.openlocfilehash: 2d3fd9d44a06c8538233b1f130010e905055912e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917278"
---
# <span data-ttu-id="9ea25-101">Stop-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="9ea25-101">Stop-AzHpcCache</span></span>

## <span data-ttu-id="9ea25-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9ea25-102">SYNOPSIS</span></span>
<span data-ttu-id="9ea25-103">停止 HPC 緩存。</span><span class="sxs-lookup"><span data-stu-id="9ea25-103">Stops HPC cache.</span></span>

## <span data-ttu-id="9ea25-104">語法</span><span class="sxs-lookup"><span data-stu-id="9ea25-104">SYNTAX</span></span>

### <span data-ttu-id="9ea25-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9ea25-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ea25-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ea25-106">ByResourceIdParameterSet</span></span>
```
Stop-AzHpcCache -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ea25-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ea25-107">ByObjectParameterSet</span></span>
```
Stop-AzHpcCache -InputObject <PSHPCCache> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ea25-108">描述</span><span class="sxs-lookup"><span data-stu-id="9ea25-108">DESCRIPTION</span></span>
<span data-ttu-id="9ea25-109">**Stop-AzHpcCache** Cmdlet 會停止 Azure HPC Cache。</span><span class="sxs-lookup"><span data-stu-id="9ea25-109">The **Stop-AzHpcCache** cmdlet stops a Azure HPC Cache.</span></span>

## <span data-ttu-id="9ea25-110">例子</span><span class="sxs-lookup"><span data-stu-id="9ea25-110">EXAMPLES</span></span>

### <span data-ttu-id="9ea25-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="9ea25-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="9ea25-112">參數</span><span class="sxs-lookup"><span data-stu-id="9ea25-112">PARAMETERS</span></span>

### <span data-ttu-id="9ea25-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ea25-113">-DefaultProfile</span></span>
<span data-ttu-id="9ea25-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9ea25-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ea25-115">-強制</span><span class="sxs-lookup"><span data-stu-id="9ea25-115">-Force</span></span>
<span data-ttu-id="9ea25-116">表示 Cmdlet 不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9ea25-116">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="9ea25-117">根據預設，此 Cmdlet 會提示您確認要停止緩存。</span><span class="sxs-lookup"><span data-stu-id="9ea25-117">By default, this cmdlet prompts you to confirm that you want to stop the cache.</span></span>

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

### <span data-ttu-id="9ea25-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ea25-118">-InputObject</span></span>
<span data-ttu-id="9ea25-119">要停止的緩存物件。</span><span class="sxs-lookup"><span data-stu-id="9ea25-119">The cache object to stop.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ea25-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="9ea25-120">-Name</span></span>
<span data-ttu-id="9ea25-121">緩存名稱。</span><span class="sxs-lookup"><span data-stu-id="9ea25-121">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: CacheName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ea25-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ea25-122">-PassThru</span></span>
<span data-ttu-id="9ea25-123">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="9ea25-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9ea25-124">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="9ea25-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ea25-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ea25-125">-ResourceGroupName</span></span>
<span data-ttu-id="9ea25-126">您想要停止緩存的資源組名。</span><span class="sxs-lookup"><span data-stu-id="9ea25-126">Name of resource group under which you want to stop cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ea25-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ea25-127">-ResourceId</span></span>
<span data-ttu-id="9ea25-128">Cache 的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="9ea25-128">The resource id of the Cache</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ea25-129">-確認</span><span class="sxs-lookup"><span data-stu-id="9ea25-129">-Confirm</span></span>
<span data-ttu-id="9ea25-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9ea25-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ea25-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ea25-131">-WhatIf</span></span>
<span data-ttu-id="9ea25-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9ea25-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9ea25-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9ea25-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ea25-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ea25-134">CommonParameters</span></span>
<span data-ttu-id="9ea25-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9ea25-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ea25-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9ea25-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ea25-137">輸入</span><span class="sxs-lookup"><span data-stu-id="9ea25-137">INPUTS</span></span>

### <span data-ttu-id="9ea25-138">System.String</span><span class="sxs-lookup"><span data-stu-id="9ea25-138">System.String</span></span>

## <span data-ttu-id="9ea25-139">輸出</span><span class="sxs-lookup"><span data-stu-id="9ea25-139">OUTPUTS</span></span>

## <span data-ttu-id="9ea25-140">筆記</span><span class="sxs-lookup"><span data-stu-id="9ea25-140">NOTES</span></span>

## <span data-ttu-id="9ea25-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="9ea25-141">RELATED LINKS</span></span>
