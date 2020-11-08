---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/stop-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Stop-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Stop-AzHpcCache.md
ms.openlocfilehash: 22813d762fe575f7f34b6c8eb81f1b5c1c167047
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94136795"
---
# <span data-ttu-id="e8f6f-101">Stop-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="e8f6f-101">Stop-AzHpcCache</span></span>

## <span data-ttu-id="e8f6f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8f6f-102">SYNOPSIS</span></span>
<span data-ttu-id="e8f6f-103">停止 HPC 快取。</span><span class="sxs-lookup"><span data-stu-id="e8f6f-103">Stops HPC cache.</span></span>

## <span data-ttu-id="e8f6f-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8f6f-104">SYNTAX</span></span>

### <span data-ttu-id="e8f6f-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e8f6f-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8f6f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8f6f-106">ByResourceIdParameterSet</span></span>
```
Stop-AzHpcCache -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8f6f-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8f6f-107">ByObjectParameterSet</span></span>
```
Stop-AzHpcCache -InputObject <PSHPCCache> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8f6f-108">說明</span><span class="sxs-lookup"><span data-stu-id="e8f6f-108">DESCRIPTION</span></span>
<span data-ttu-id="e8f6f-109">**AzHpcCache** Cmdlet 會停止 Azure HPC 緩存。</span><span class="sxs-lookup"><span data-stu-id="e8f6f-109">The **Stop-AzHpcCache** cmdlet stops a Azure HPC Cache.</span></span>

## <span data-ttu-id="e8f6f-110">示例</span><span class="sxs-lookup"><span data-stu-id="e8f6f-110">EXAMPLES</span></span>

### <span data-ttu-id="e8f6f-111">範例1</span><span class="sxs-lookup"><span data-stu-id="e8f6f-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="e8f6f-112">參數</span><span class="sxs-lookup"><span data-stu-id="e8f6f-112">PARAMETERS</span></span>

### <span data-ttu-id="e8f6f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8f6f-113">-DefaultProfile</span></span>
<span data-ttu-id="e8f6f-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8f6f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8f6f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e8f6f-115">-Force</span></span>
<span data-ttu-id="e8f6f-116">表示 Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e8f6f-116">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="e8f6f-117">根據預設，這個 Cmdlet 會提示您確認是否要停止快取。</span><span class="sxs-lookup"><span data-stu-id="e8f6f-117">By default, this cmdlet prompts you to confirm that you want to stop the cache.</span></span>

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

### <span data-ttu-id="e8f6f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8f6f-118">-InputObject</span></span>
<span data-ttu-id="e8f6f-119">要停止的快取物件。</span><span class="sxs-lookup"><span data-stu-id="e8f6f-119">The cache object to stop.</span></span>

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

### <span data-ttu-id="e8f6f-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="e8f6f-120">-Name</span></span>
<span data-ttu-id="e8f6f-121">快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8f6f-121">Name of cache.</span></span>

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

### <span data-ttu-id="e8f6f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8f6f-122">-PassThru</span></span>
<span data-ttu-id="e8f6f-123">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="e8f6f-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e8f6f-124">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="e8f6f-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e8f6f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8f6f-125">-ResourceGroupName</span></span>
<span data-ttu-id="e8f6f-126">您想要停止快取之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8f6f-126">Name of resource group under which you want to stop cache.</span></span>

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

### <span data-ttu-id="e8f6f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8f6f-127">-ResourceId</span></span>
<span data-ttu-id="e8f6f-128">快取的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="e8f6f-128">The resource id of the Cache</span></span>

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

### <span data-ttu-id="e8f6f-129">-確認</span><span class="sxs-lookup"><span data-stu-id="e8f6f-129">-Confirm</span></span>
<span data-ttu-id="e8f6f-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e8f6f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8f6f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8f6f-131">-WhatIf</span></span>
<span data-ttu-id="e8f6f-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e8f6f-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e8f6f-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e8f6f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8f6f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8f6f-134">CommonParameters</span></span>
<span data-ttu-id="e8f6f-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8f6f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8f6f-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e8f6f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8f6f-137">輸入</span><span class="sxs-lookup"><span data-stu-id="e8f6f-137">INPUTS</span></span>

### <span data-ttu-id="e8f6f-138">System.object</span><span class="sxs-lookup"><span data-stu-id="e8f6f-138">System.String</span></span>

## <span data-ttu-id="e8f6f-139">輸出</span><span class="sxs-lookup"><span data-stu-id="e8f6f-139">OUTPUTS</span></span>

## <span data-ttu-id="e8f6f-140">筆記</span><span class="sxs-lookup"><span data-stu-id="e8f6f-140">NOTES</span></span>

## <span data-ttu-id="e8f6f-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8f6f-141">RELATED LINKS</span></span>