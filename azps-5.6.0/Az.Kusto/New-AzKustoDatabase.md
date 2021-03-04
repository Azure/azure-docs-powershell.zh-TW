---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/new-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabase.md
ms.openlocfilehash: b3e6319de721d63071c730bb43e1ef7db5a46e25
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902954"
---
# <span data-ttu-id="e32a7-101">New-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="e32a7-101">New-AzKustoDatabase</span></span>

## <span data-ttu-id="e32a7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e32a7-102">SYNOPSIS</span></span>
<span data-ttu-id="e32a7-103">建立或更新資料庫。</span><span class="sxs-lookup"><span data-stu-id="e32a7-103">Creates or updates a database.</span></span>

## <span data-ttu-id="e32a7-104">語法</span><span class="sxs-lookup"><span data-stu-id="e32a7-104">SYNTAX</span></span>

```
New-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String> -Kind <Kind>
 [-SubscriptionId <String>] [-HotCachePeriod <TimeSpan>] [-Location <String>] [-SoftDeletePeriod <TimeSpan>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e32a7-105">描述</span><span class="sxs-lookup"><span data-stu-id="e32a7-105">DESCRIPTION</span></span>
<span data-ttu-id="e32a7-106">建立或更新資料庫。</span><span class="sxs-lookup"><span data-stu-id="e32a7-106">Creates or updates a database.</span></span>

## <span data-ttu-id="e32a7-107">例子</span><span class="sxs-lookup"><span data-stu-id="e32a7-107">EXAMPLES</span></span>

### <span data-ttu-id="e32a7-108">範例 1：根據名稱建立新 Kusto 資料庫</span><span class="sxs-lookup"><span data-stu-id="e32a7-108">Example 1: Create a new Kusto database by name</span></span>
```powershell
PS C:\> New-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Kind ReadWrite -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="e32a7-109">上述命令會于資源群組"testrg"找到的現有叢集「testnewkustocluster」中，建立名為"mykustodatabase"的新 Kusto 資料庫。</span><span class="sxs-lookup"><span data-stu-id="e32a7-109">The above command creates a new Kusto database named "mykustodatabase" in the existing cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="e32a7-110">參數</span><span class="sxs-lookup"><span data-stu-id="e32a7-110">PARAMETERS</span></span>

### <span data-ttu-id="e32a7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e32a7-111">-AsJob</span></span>
<span data-ttu-id="e32a7-112">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="e32a7-112">Run the command as a job</span></span>

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

### <span data-ttu-id="e32a7-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e32a7-113">-ClusterName</span></span>
<span data-ttu-id="e32a7-114">Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="e32a7-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="e32a7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e32a7-115">-DefaultProfile</span></span>
<span data-ttu-id="e32a7-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e32a7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e32a7-117">-HotCachePeriod</span><span class="sxs-lookup"><span data-stu-id="e32a7-117">-HotCachePeriod</span></span>
<span data-ttu-id="e32a7-118">資料應保留在快處理中的時間，以在時間跨時間進行快速查詢。</span><span class="sxs-lookup"><span data-stu-id="e32a7-118">The time the data should be kept in cache for fast queries in TimeSpan.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e32a7-119">-Kind</span><span class="sxs-lookup"><span data-stu-id="e32a7-119">-Kind</span></span>
<span data-ttu-id="e32a7-120">資料庫類型</span><span class="sxs-lookup"><span data-stu-id="e32a7-120">Kind of the database</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e32a7-121">-位置</span><span class="sxs-lookup"><span data-stu-id="e32a7-121">-Location</span></span>
<span data-ttu-id="e32a7-122">資源位置。</span><span class="sxs-lookup"><span data-stu-id="e32a7-122">Resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e32a7-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="e32a7-123">-Name</span></span>
<span data-ttu-id="e32a7-124">Kusto cluster 中的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="e32a7-124">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e32a7-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e32a7-125">-NoWait</span></span>
<span data-ttu-id="e32a7-126">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="e32a7-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e32a7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e32a7-127">-ResourceGroupName</span></span>
<span data-ttu-id="e32a7-128">包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="e32a7-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="e32a7-129">-SoftDeletePeriod</span><span class="sxs-lookup"><span data-stu-id="e32a7-129">-SoftDeletePeriod</span></span>
<span data-ttu-id="e32a7-130">資料在時間跨行中停止可供查詢使用之前，應該保留的時間。</span><span class="sxs-lookup"><span data-stu-id="e32a7-130">The time the data should be kept before it stops being accessible to queries in TimeSpan.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e32a7-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e32a7-131">-SubscriptionId</span></span>
<span data-ttu-id="e32a7-132">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="e32a7-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e32a7-133">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="e32a7-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e32a7-134">-確認</span><span class="sxs-lookup"><span data-stu-id="e32a7-134">-Confirm</span></span>
<span data-ttu-id="e32a7-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e32a7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e32a7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e32a7-136">-WhatIf</span></span>
<span data-ttu-id="e32a7-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e32a7-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e32a7-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e32a7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e32a7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e32a7-139">CommonParameters</span></span>
<span data-ttu-id="e32a7-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e32a7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e32a7-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e32a7-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e32a7-142">輸入</span><span class="sxs-lookup"><span data-stu-id="e32a7-142">INPUTS</span></span>

## <span data-ttu-id="e32a7-143">輸出</span><span class="sxs-lookup"><span data-stu-id="e32a7-143">OUTPUTS</span></span>

### <span data-ttu-id="e32a7-144">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span><span class="sxs-lookup"><span data-stu-id="e32a7-144">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span></span>

## <span data-ttu-id="e32a7-145">筆記</span><span class="sxs-lookup"><span data-stu-id="e32a7-145">NOTES</span></span>

<span data-ttu-id="e32a7-146">別名</span><span class="sxs-lookup"><span data-stu-id="e32a7-146">ALIASES</span></span>

## <span data-ttu-id="e32a7-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="e32a7-147">RELATED LINKS</span></span>

