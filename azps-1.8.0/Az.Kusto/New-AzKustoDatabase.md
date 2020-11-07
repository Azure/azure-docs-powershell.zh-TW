---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoDatabase.md
ms.openlocfilehash: 33272012d81160a055bcd5d1eb0ef617787eed1e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787230"
---
# <span data-ttu-id="340ec-101">New-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="340ec-101">New-AzKustoDatabase</span></span>

## <span data-ttu-id="340ec-102">摘要</span><span class="sxs-lookup"><span data-stu-id="340ec-102">SYNOPSIS</span></span>
<span data-ttu-id="340ec-103">在現有的群集中建立新的 Kusto 資料庫。</span><span class="sxs-lookup"><span data-stu-id="340ec-103">Creates a new Kusto database in an existing cluster.</span></span>

## <span data-ttu-id="340ec-104">句法</span><span class="sxs-lookup"><span data-stu-id="340ec-104">SYNTAX</span></span>

### <span data-ttu-id="340ec-105">ByNameAndResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="340ec-105">ByNameAndResourceGroup (Default)</span></span>
```
New-AzKustoDatabase [-ResourceGroupName] <String> [-ClusterName] <String> -Name <String>
 -SoftDeletePeriodInDays <Int32> -HotCachePeriodInDays <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="340ec-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="340ec-106">ByResourceId</span></span>
```
New-AzKustoDatabase -Name <String> -SoftDeletePeriodInDays <Int32> -HotCachePeriodInDays <Int32>
 [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="340ec-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="340ec-107">ByInputObject</span></span>
```
New-AzKustoDatabase -Name <String> -SoftDeletePeriodInDays <Int32> -HotCachePeriodInDays <Int32>
 [-InputObject] <PSKustoCluster> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="340ec-108">說明</span><span class="sxs-lookup"><span data-stu-id="340ec-108">DESCRIPTION</span></span>
<span data-ttu-id="340ec-109">在現有的群集中建立新的 Kusto 資料庫。</span><span class="sxs-lookup"><span data-stu-id="340ec-109">Creates a new Kusto database in an existing cluster.</span></span>

## <span data-ttu-id="340ec-110">示例</span><span class="sxs-lookup"><span data-stu-id="340ec-110">EXAMPLES</span></span>

### <span data-ttu-id="340ec-111">範例 1-依名稱建立新的 Kusto 資料庫</span><span class="sxs-lookup"><span data-stu-id="340ec-111">Example 1 - Create a new Kusto database by name</span></span>

```
PS C:\> New-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase -SoftDeletePeriodInDays 4 -HotCachePeriodInDays 2

Name                   : mykustocluster/mykustodatabase
SoftDeletePeriodInDays : 4
HotCachePeriodInDays   : 2
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="340ec-112">上述命令會在資源群組 "testrg" 中找到現有群集 "mykustocluster" 中，建立名為 "mykustodatabase" 的新 Kusto 資料庫。</span><span class="sxs-lookup"><span data-stu-id="340ec-112">The above command creates a new Kusto database named "mykustodatabase" in the existing cluster "mykustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="340ec-113">參數</span><span class="sxs-lookup"><span data-stu-id="340ec-113">PARAMETERS</span></span>

### <span data-ttu-id="340ec-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="340ec-114">-ClusterName</span></span>
<span data-ttu-id="340ec-115">您要在其下建立資料庫的群集名稱。</span><span class="sxs-lookup"><span data-stu-id="340ec-115">Name of cluster under which you want to create the database.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="340ec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="340ec-116">-DefaultProfile</span></span>
<span data-ttu-id="340ec-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="340ec-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="340ec-118">-HotCachePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="340ec-118">-HotCachePeriodInDays</span></span>
<span data-ttu-id="340ec-119">要保留在快取中以快速查詢的資料天數。</span><span class="sxs-lookup"><span data-stu-id="340ec-119">The number of days of data that should be kept in cache for fast queries.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="340ec-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="340ec-120">-InputObject</span></span>
<span data-ttu-id="340ec-121">Kusto [群集物件]。</span><span class="sxs-lookup"><span data-stu-id="340ec-121">Kusto cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="340ec-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="340ec-122">-Name</span></span>
<span data-ttu-id="340ec-123">要建立之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="340ec-123">Name of the database to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="340ec-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="340ec-124">-ResourceGroupName</span></span>
<span data-ttu-id="340ec-125">群集存在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="340ec-125">Name of resource group under which the cluster exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="340ec-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="340ec-126">-ResourceId</span></span>
<span data-ttu-id="340ec-127">Kusto [群集 ResourceID]。</span><span class="sxs-lookup"><span data-stu-id="340ec-127">Kusto cluster ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="340ec-128">-SoftDeletePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="340ec-128">-SoftDeletePeriodInDays</span></span>
<span data-ttu-id="340ec-129">資料在停止存取查詢之前應保留的天數。</span><span class="sxs-lookup"><span data-stu-id="340ec-129">The number of days data should be kept before it stops being accessible to queries.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="340ec-130">-確認</span><span class="sxs-lookup"><span data-stu-id="340ec-130">-Confirm</span></span>
<span data-ttu-id="340ec-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="340ec-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="340ec-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="340ec-132">-WhatIf</span></span>
<span data-ttu-id="340ec-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="340ec-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="340ec-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="340ec-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="340ec-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="340ec-135">CommonParameters</span></span>
<span data-ttu-id="340ec-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="340ec-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="340ec-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="340ec-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="340ec-138">輸入</span><span class="sxs-lookup"><span data-stu-id="340ec-138">INPUTS</span></span>

### <span data-ttu-id="340ec-139">System.object</span><span class="sxs-lookup"><span data-stu-id="340ec-139">System.String</span></span>

### <span data-ttu-id="340ec-140">PSKustoCluster 中的 Kusto。</span><span class="sxs-lookup"><span data-stu-id="340ec-140">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="340ec-141">輸出</span><span class="sxs-lookup"><span data-stu-id="340ec-141">OUTPUTS</span></span>

### <span data-ttu-id="340ec-142">PSKustoDatabase 中的 Kusto。</span><span class="sxs-lookup"><span data-stu-id="340ec-142">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="340ec-143">筆記</span><span class="sxs-lookup"><span data-stu-id="340ec-143">NOTES</span></span>

## <span data-ttu-id="340ec-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="340ec-144">RELATED LINKS</span></span>
