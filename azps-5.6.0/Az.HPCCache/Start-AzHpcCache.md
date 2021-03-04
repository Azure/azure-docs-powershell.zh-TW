---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/start-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Start-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Start-AzHpcCache.md
ms.openlocfilehash: 29ab4c0536b64203af540f08d0a1974371812c19
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917293"
---
# <span data-ttu-id="974e1-101">Start-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="974e1-101">Start-AzHpcCache</span></span>

## <span data-ttu-id="974e1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="974e1-102">SYNOPSIS</span></span>
<span data-ttu-id="974e1-103">啟動 HPC 緩存。</span><span class="sxs-lookup"><span data-stu-id="974e1-103">Starts HPC cache.</span></span>

## <span data-ttu-id="974e1-104">語法</span><span class="sxs-lookup"><span data-stu-id="974e1-104">SYNTAX</span></span>

### <span data-ttu-id="974e1-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="974e1-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="974e1-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="974e1-106">ByResourceIdParameterSet</span></span>
```
Start-AzHpcCache -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="974e1-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="974e1-107">ByObjectParameterSet</span></span>
```
Start-AzHpcCache -InputObject <PSHPCCache> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="974e1-108">描述</span><span class="sxs-lookup"><span data-stu-id="974e1-108">DESCRIPTION</span></span>
<span data-ttu-id="974e1-109">**Start-AzHpcCache** Cmdlet 會啟動 Azure HPC Cache。</span><span class="sxs-lookup"><span data-stu-id="974e1-109">The **Start-AzHpcCache** cmdlet starts a Azure HPC Cache.</span></span>

## <span data-ttu-id="974e1-110">例子</span><span class="sxs-lookup"><span data-stu-id="974e1-110">EXAMPLES</span></span>

### <span data-ttu-id="974e1-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="974e1-111">Example 1</span></span>
```powershell
PS C:\> Start-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="974e1-112">參數</span><span class="sxs-lookup"><span data-stu-id="974e1-112">PARAMETERS</span></span>

### <span data-ttu-id="974e1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="974e1-113">-AsJob</span></span>
<span data-ttu-id="974e1-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="974e1-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="974e1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="974e1-115">-DefaultProfile</span></span>
<span data-ttu-id="974e1-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="974e1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="974e1-117">-強制</span><span class="sxs-lookup"><span data-stu-id="974e1-117">-Force</span></span>
<span data-ttu-id="974e1-118">表示 Cmdlet 不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="974e1-118">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="974e1-119">根據預設，此 Cmdlet 會提示您確認要啟動緩存。</span><span class="sxs-lookup"><span data-stu-id="974e1-119">By default, this cmdlet prompts you to confirm that you want to start the cache.</span></span>

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

### <span data-ttu-id="974e1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="974e1-120">-InputObject</span></span>
<span data-ttu-id="974e1-121">要啟動的緩存物件。</span><span class="sxs-lookup"><span data-stu-id="974e1-121">The cache object to start.</span></span>

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

### <span data-ttu-id="974e1-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="974e1-122">-Name</span></span>
<span data-ttu-id="974e1-123">緩存名稱。</span><span class="sxs-lookup"><span data-stu-id="974e1-123">Name of cache.</span></span>

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

### <span data-ttu-id="974e1-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="974e1-124">-PassThru</span></span>
<span data-ttu-id="974e1-125">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="974e1-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="974e1-126">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="974e1-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="974e1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="974e1-127">-ResourceGroupName</span></span>
<span data-ttu-id="974e1-128">這是要開始緩存的資源組名。</span><span class="sxs-lookup"><span data-stu-id="974e1-128">Name of resource group under which you want to start cache.</span></span>

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

### <span data-ttu-id="974e1-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="974e1-129">-ResourceId</span></span>
<span data-ttu-id="974e1-130">Cache 的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="974e1-130">The resource id of the Cache</span></span>

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

### <span data-ttu-id="974e1-131">-確認</span><span class="sxs-lookup"><span data-stu-id="974e1-131">-Confirm</span></span>
<span data-ttu-id="974e1-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="974e1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="974e1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="974e1-133">-WhatIf</span></span>
<span data-ttu-id="974e1-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="974e1-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="974e1-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="974e1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="974e1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="974e1-136">CommonParameters</span></span>
<span data-ttu-id="974e1-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="974e1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="974e1-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="974e1-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="974e1-139">輸入</span><span class="sxs-lookup"><span data-stu-id="974e1-139">INPUTS</span></span>

### <span data-ttu-id="974e1-140">System.String</span><span class="sxs-lookup"><span data-stu-id="974e1-140">System.String</span></span>

## <span data-ttu-id="974e1-141">輸出</span><span class="sxs-lookup"><span data-stu-id="974e1-141">OUTPUTS</span></span>

## <span data-ttu-id="974e1-142">筆記</span><span class="sxs-lookup"><span data-stu-id="974e1-142">NOTES</span></span>

## <span data-ttu-id="974e1-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="974e1-143">RELATED LINKS</span></span>
