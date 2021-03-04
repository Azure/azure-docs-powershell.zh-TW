---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/set-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCache.md
ms.openlocfilehash: 9ad46b21990e6a864408536bf56bb09c2d0b3dc3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917298"
---
# <span data-ttu-id="2f18a-101">Set-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="2f18a-101">Set-AzHpcCache</span></span>

## <span data-ttu-id="2f18a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2f18a-102">SYNOPSIS</span></span>
<span data-ttu-id="2f18a-103">更新 HPC Cache 上的標記。</span><span class="sxs-lookup"><span data-stu-id="2f18a-103">Updates tags on a HPC Cache.</span></span>

## <span data-ttu-id="2f18a-104">語法</span><span class="sxs-lookup"><span data-stu-id="2f18a-104">SYNTAX</span></span>

### <span data-ttu-id="2f18a-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2f18a-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzHpcCache -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f18a-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f18a-106">ByObjectParameterSet</span></span>
```
Set-AzHpcCache -InputObject <PSHPCCache> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f18a-107">描述</span><span class="sxs-lookup"><span data-stu-id="2f18a-107">DESCRIPTION</span></span>
<span data-ttu-id="2f18a-108">**Set-AzHpcCache** Cmdlet 會更新 Azure HPC Cache 標籤。</span><span class="sxs-lookup"><span data-stu-id="2f18a-108">The **Set-AzHpcCache** cmdlet updates an Azure HPC Cache tags.</span></span>

## <span data-ttu-id="2f18a-109">例子</span><span class="sxs-lookup"><span data-stu-id="2f18a-109">EXAMPLES</span></span>

### <span data-ttu-id="2f18a-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="2f18a-110">Example 1</span></span>
```powershell
PS C:\> Set-AzHpcCache -ResourceGroupName testRG -CacheName testCache -Tag @{"tag3" = "value1"; "tag4" = "value2"}
```

## <span data-ttu-id="2f18a-111">參數</span><span class="sxs-lookup"><span data-stu-id="2f18a-111">PARAMETERS</span></span>

### <span data-ttu-id="2f18a-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2f18a-112">-AsJob</span></span>
<span data-ttu-id="2f18a-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2f18a-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2f18a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f18a-114">-DefaultProfile</span></span>
<span data-ttu-id="2f18a-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2f18a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f18a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f18a-116">-InputObject</span></span>
<span data-ttu-id="2f18a-117">要更新的快用物件。</span><span class="sxs-lookup"><span data-stu-id="2f18a-117">The cache object to update.</span></span>

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

### <span data-ttu-id="2f18a-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="2f18a-118">-Name</span></span>
<span data-ttu-id="2f18a-119">緩存名稱。</span><span class="sxs-lookup"><span data-stu-id="2f18a-119">Name of cache.</span></span>

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

### <span data-ttu-id="2f18a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f18a-120">-ResourceGroupName</span></span>
<span data-ttu-id="2f18a-121">這是要更新快點的資源組名。</span><span class="sxs-lookup"><span data-stu-id="2f18a-121">Name of resource group under which you want to update cache.</span></span>

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

### <span data-ttu-id="2f18a-122">-標記</span><span class="sxs-lookup"><span data-stu-id="2f18a-122">-Tag</span></span>
<span data-ttu-id="2f18a-123">要與 HPC Cache 關聯的標記。</span><span class="sxs-lookup"><span data-stu-id="2f18a-123">The tags to associate with HPC Cache.</span></span> 

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f18a-124">-確認</span><span class="sxs-lookup"><span data-stu-id="2f18a-124">-Confirm</span></span>
<span data-ttu-id="2f18a-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2f18a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f18a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f18a-126">-WhatIf</span></span>
<span data-ttu-id="2f18a-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2f18a-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2f18a-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2f18a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f18a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f18a-129">CommonParameters</span></span>
<span data-ttu-id="2f18a-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2f18a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f18a-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f18a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f18a-132">輸入</span><span class="sxs-lookup"><span data-stu-id="2f18a-132">INPUTS</span></span>

### <span data-ttu-id="2f18a-133">System.String</span><span class="sxs-lookup"><span data-stu-id="2f18a-133">System.String</span></span>

### <span data-ttu-id="2f18a-134">System.Int32</span><span class="sxs-lookup"><span data-stu-id="2f18a-134">System.Int32</span></span>

## <span data-ttu-id="2f18a-135">輸出</span><span class="sxs-lookup"><span data-stu-id="2f18a-135">OUTPUTS</span></span>

### <span data-ttu-id="2f18a-136">Microsoft.Azure.PowerShell.Cmdlets.HPCache.models.PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="2f18a-136">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="2f18a-137">筆記</span><span class="sxs-lookup"><span data-stu-id="2f18a-137">NOTES</span></span>

## <span data-ttu-id="2f18a-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="2f18a-138">RELATED LINKS</span></span>
