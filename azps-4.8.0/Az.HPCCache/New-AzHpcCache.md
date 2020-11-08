---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/new-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCache.md
ms.openlocfilehash: faadb14259dd397f713480c771d2d450260d99cc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128162"
---
# <span data-ttu-id="7c52a-101">New-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="7c52a-101">New-AzHpcCache</span></span>

## <span data-ttu-id="7c52a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7c52a-102">SYNOPSIS</span></span>
<span data-ttu-id="7c52a-103">建立 HPC 快取。</span><span class="sxs-lookup"><span data-stu-id="7c52a-103">Creates a HPC Cache.</span></span>

## <span data-ttu-id="7c52a-104">句法</span><span class="sxs-lookup"><span data-stu-id="7c52a-104">SYNTAX</span></span>

```
New-AzHpcCache -ResourceGroupName <String> -Name <String> -Sku <String> -SubnetUri <String> -CacheSize <Int32>
 -Location <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7c52a-105">說明</span><span class="sxs-lookup"><span data-stu-id="7c52a-105">DESCRIPTION</span></span>
<span data-ttu-id="7c52a-106">**新的-AzHpcCache** Cmdlet 會建立 Azure HPC 緩存。</span><span class="sxs-lookup"><span data-stu-id="7c52a-106">The **New-AzHpcCache** cmdlet creates a Azure HPC Cache.</span></span>

## <span data-ttu-id="7c52a-107">示例</span><span class="sxs-lookup"><span data-stu-id="7c52a-107">EXAMPLES</span></span>

### <span data-ttu-id="7c52a-108">範例1</span><span class="sxs-lookup"><span data-stu-id="7c52a-108">Example 1</span></span>
```powershell
PS C:\> New-AzHpcCache -ResourceGroupName testRG -CacheName testCache -Sku Standard_2G -SubnetUri /subscriptions/<subid>/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/testvnet/subnets/defauly-tip1-test2 -cacheSize 3072 -Location eastus -Tag @{"tag1" = "value1"; "tag2" = "value2"}
```

## <span data-ttu-id="7c52a-109">參數</span><span class="sxs-lookup"><span data-stu-id="7c52a-109">PARAMETERS</span></span>

### <span data-ttu-id="7c52a-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c52a-110">-AsJob</span></span>
<span data-ttu-id="7c52a-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7c52a-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7c52a-112">-CacheSize</span><span class="sxs-lookup"><span data-stu-id="7c52a-112">-CacheSize</span></span>
<span data-ttu-id="7c52a-113">CacheSize.</span><span class="sxs-lookup"><span data-stu-id="7c52a-113">CacheSize.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c52a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c52a-114">-DefaultProfile</span></span>
<span data-ttu-id="7c52a-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7c52a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c52a-116">-位置</span><span class="sxs-lookup"><span data-stu-id="7c52a-116">-Location</span></span>
<span data-ttu-id="7c52a-117">位於.</span><span class="sxs-lookup"><span data-stu-id="7c52a-117">Location.</span></span>

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

### <span data-ttu-id="7c52a-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="7c52a-118">-Name</span></span>
<span data-ttu-id="7c52a-119">快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="7c52a-119">Name of cache.</span></span>

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

### <span data-ttu-id="7c52a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c52a-120">-ResourceGroupName</span></span>
<span data-ttu-id="7c52a-121">您要在其中建立快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7c52a-121">Name of resource group under which you want to create cache.</span></span>

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

### <span data-ttu-id="7c52a-122">-Sku</span><span class="sxs-lookup"><span data-stu-id="7c52a-122">-Sku</span></span>
<span data-ttu-id="7c52a-123">Sku.</span><span class="sxs-lookup"><span data-stu-id="7c52a-123">Sku.</span></span>

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

### <span data-ttu-id="7c52a-124">-SubnetUri</span><span class="sxs-lookup"><span data-stu-id="7c52a-124">-SubnetUri</span></span>
<span data-ttu-id="7c52a-125">SubnetURI.</span><span class="sxs-lookup"><span data-stu-id="7c52a-125">SubnetURI.</span></span>

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

### <span data-ttu-id="7c52a-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="7c52a-126">-Tag</span></span>
<span data-ttu-id="7c52a-127">要與 HPC 緩存關聯的標籤。</span><span class="sxs-lookup"><span data-stu-id="7c52a-127">The tags to associate with HPC Cache.</span></span>

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

### <span data-ttu-id="7c52a-128">-確認</span><span class="sxs-lookup"><span data-stu-id="7c52a-128">-Confirm</span></span>
<span data-ttu-id="7c52a-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7c52a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c52a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c52a-130">-WhatIf</span></span>
<span data-ttu-id="7c52a-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7c52a-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7c52a-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7c52a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c52a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c52a-133">CommonParameters</span></span>
<span data-ttu-id="7c52a-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7c52a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c52a-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7c52a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c52a-136">輸入</span><span class="sxs-lookup"><span data-stu-id="7c52a-136">INPUTS</span></span>

### <span data-ttu-id="7c52a-137">System.object</span><span class="sxs-lookup"><span data-stu-id="7c52a-137">System.String</span></span>

### <span data-ttu-id="7c52a-138">System.object</span><span class="sxs-lookup"><span data-stu-id="7c52a-138">System.Int32</span></span>

## <span data-ttu-id="7c52a-139">輸出</span><span class="sxs-lookup"><span data-stu-id="7c52a-139">OUTPUTS</span></span>

### <span data-ttu-id="7c52a-140">PSHPCCache （HPCCache）的</span><span class="sxs-lookup"><span data-stu-id="7c52a-140">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="7c52a-141">筆記</span><span class="sxs-lookup"><span data-stu-id="7c52a-141">NOTES</span></span>

## <span data-ttu-id="7c52a-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="7c52a-142">RELATED LINKS</span></span>