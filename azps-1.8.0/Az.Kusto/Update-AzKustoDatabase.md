---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Update-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Update-AzKustoDatabase.md
ms.openlocfilehash: 05d01d776f03ec3bbfe4e9bf6bd438ba8f002afb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787197"
---
# <span data-ttu-id="76da4-101">Update-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="76da4-101">Update-AzKustoDatabase</span></span>

## <span data-ttu-id="76da4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="76da4-102">SYNOPSIS</span></span>
<span data-ttu-id="76da4-103">更新現有的 Kusto 資料庫。</span><span class="sxs-lookup"><span data-stu-id="76da4-103">Update an existing Kusto database.</span></span>

## <span data-ttu-id="76da4-104">句法</span><span class="sxs-lookup"><span data-stu-id="76da4-104">SYNTAX</span></span>

### <span data-ttu-id="76da4-105">ByNameAndResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="76da4-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzKustoDatabase [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-SoftDeletePeriodInDays <Int32>] [-HotCachePeriodInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76da4-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="76da4-106">ByResourceId</span></span>
```
Update-AzKustoDatabase [-SoftDeletePeriodInDays <Int32>] [-HotCachePeriodInDays <Int32>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76da4-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="76da4-107">ByInputObject</span></span>
```
Update-AzKustoDatabase [-SoftDeletePeriodInDays <Int32>] [-HotCachePeriodInDays <Int32>]
 [-InputObject] <PSKustoDatabase> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="76da4-108">說明</span><span class="sxs-lookup"><span data-stu-id="76da4-108">DESCRIPTION</span></span>
<span data-ttu-id="76da4-109">更新現有的 Kusto 資料庫。</span><span class="sxs-lookup"><span data-stu-id="76da4-109">Update an existing Kusto database.</span></span>

## <span data-ttu-id="76da4-110">示例</span><span class="sxs-lookup"><span data-stu-id="76da4-110">EXAMPLES</span></span>

### <span data-ttu-id="76da4-111">範例 1-依名稱更新現有資料庫</span><span class="sxs-lookup"><span data-stu-id="76da4-111">Example 1 - Update an existing database by name</span></span>

```
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase -SoftDeletePeriodInDays 5

Name                   : mykustocluster/mykustodatabase
SoftDeletePeriodInDays : 5
HotCachePeriodInDays   : 2
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="76da4-112">上述命令會更新在資源群組 "testrg" 中找到的群集 "mykustocluster" 中，Kusto 資料庫 "mykustodatabase" 的虛刪除週期。</span><span class="sxs-lookup"><span data-stu-id="76da4-112">The above command updates the soft deletion period of the Kusto database "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="76da4-113">範例 2-依管道更新現有的資料庫</span><span class="sxs-lookup"><span data-stu-id="76da4-113">Example 2 - Update an existing database by piping</span></span>

```
PS C:\> PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase | Update-AzKustoDatabase -SoftDeletePeriodInDays 5

Name                   : mykustocluster/mykustodatabase
SoftDeletePeriodInDays : 5
HotCachePeriodInDays   : 2
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="76da4-114">上述命令會在使用 Cmdlet 的資源群組 "testrg" 中找到 [mykustocluster] 群組中的 Kusto 資料庫 "mykustodatabase"，然後將結果指令成，以將 `Get-AzKustoDatabase` `Update-AzKustoDatabase` 資料庫的虛刪除期間更新為5天。</span><span class="sxs-lookup"><span data-stu-id="76da4-114">The above command gets the Kusto database "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoDatabase` cmdlet, and then pipes the result to `Update-AzKustoDatabase` to update the database's soft deletion period to five days.</span></span>

## <span data-ttu-id="76da4-115">參數</span><span class="sxs-lookup"><span data-stu-id="76da4-115">PARAMETERS</span></span>

### <span data-ttu-id="76da4-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="76da4-116">-ClusterName</span></span>
<span data-ttu-id="76da4-117">資料庫所在之群集的名稱</span><span class="sxs-lookup"><span data-stu-id="76da4-117">Name of cluster under which the database exists</span></span>

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

### <span data-ttu-id="76da4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76da4-118">-DefaultProfile</span></span>
<span data-ttu-id="76da4-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="76da4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76da4-120">-HotCachePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="76da4-120">-HotCachePeriodInDays</span></span>
<span data-ttu-id="76da4-121">資料在快取到快速查詢時應保留的天數</span><span class="sxs-lookup"><span data-stu-id="76da4-121">The number of days that data should be kept in cache for fast queries</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76da4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76da4-122">-InputObject</span></span>
<span data-ttu-id="76da4-123">Kusto 資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="76da4-123">Kusto database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76da4-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="76da4-124">-Name</span></span>
<span data-ttu-id="76da4-125">要更新的資料庫名稱</span><span class="sxs-lookup"><span data-stu-id="76da4-125">Name of the database to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76da4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76da4-126">-ResourceGroupName</span></span>
<span data-ttu-id="76da4-127">群集存在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="76da4-127">Name of resource group under which the cluster exists.</span></span>

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

### <span data-ttu-id="76da4-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76da4-128">-ResourceId</span></span>
<span data-ttu-id="76da4-129">Kusto 資料庫 ResourceID。</span><span class="sxs-lookup"><span data-stu-id="76da4-129">Kusto database ResourceID.</span></span>

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

### <span data-ttu-id="76da4-130">-SoftDeletePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="76da4-130">-SoftDeletePeriodInDays</span></span>
<span data-ttu-id="76da4-131">資料在停止存取查詢之前應保留的天數</span><span class="sxs-lookup"><span data-stu-id="76da4-131">The number of days that data should be kept before it stops being accessible to queries</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76da4-132">-確認</span><span class="sxs-lookup"><span data-stu-id="76da4-132">-Confirm</span></span>
<span data-ttu-id="76da4-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="76da4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76da4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76da4-134">-WhatIf</span></span>
<span data-ttu-id="76da4-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="76da4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76da4-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="76da4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76da4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76da4-137">CommonParameters</span></span>
<span data-ttu-id="76da4-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="76da4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76da4-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="76da4-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76da4-140">輸入</span><span class="sxs-lookup"><span data-stu-id="76da4-140">INPUTS</span></span>

### <span data-ttu-id="76da4-141">System.object</span><span class="sxs-lookup"><span data-stu-id="76da4-141">System.String</span></span>

### <span data-ttu-id="76da4-142">PSKustoDatabase 中的 Kusto。</span><span class="sxs-lookup"><span data-stu-id="76da4-142">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="76da4-143">輸出</span><span class="sxs-lookup"><span data-stu-id="76da4-143">OUTPUTS</span></span>

### <span data-ttu-id="76da4-144">PSKustoDatabase 中的 Kusto。</span><span class="sxs-lookup"><span data-stu-id="76da4-144">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="76da4-145">筆記</span><span class="sxs-lookup"><span data-stu-id="76da4-145">NOTES</span></span>

## <span data-ttu-id="76da4-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="76da4-146">RELATED LINKS</span></span>
