---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabase.md
ms.openlocfilehash: fe976ed4e5d34e4b10fb8bba0a5e5397173417b8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100140759"
---
# <span data-ttu-id="6fc6b-101">New-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="6fc6b-101">New-AzKustoDatabase</span></span>

## <span data-ttu-id="6fc6b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6fc6b-102">SYNOPSIS</span></span>
<span data-ttu-id="6fc6b-103">建立或更新資料庫。</span><span class="sxs-lookup"><span data-stu-id="6fc6b-103">Creates or updates a database.</span></span>

## <span data-ttu-id="6fc6b-104">句法</span><span class="sxs-lookup"><span data-stu-id="6fc6b-104">SYNTAX</span></span>

```
New-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String> -Kind <Kind>
 [-SubscriptionId <String>] [-HotCachePeriod <TimeSpan>] [-Location <String>] [-SoftDeletePeriod <TimeSpan>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6fc6b-105">說明</span><span class="sxs-lookup"><span data-stu-id="6fc6b-105">DESCRIPTION</span></span>
<span data-ttu-id="6fc6b-106">建立或更新資料庫。</span><span class="sxs-lookup"><span data-stu-id="6fc6b-106">Creates or updates a database.</span></span>

## <span data-ttu-id="6fc6b-107">示例</span><span class="sxs-lookup"><span data-stu-id="6fc6b-107">EXAMPLES</span></span>

### <span data-ttu-id="6fc6b-108">範例1：依名稱建立新的 Kusto 資料庫</span><span class="sxs-lookup"><span data-stu-id="6fc6b-108">Example 1: Create a new Kusto database by name</span></span>
```powershell
PS C:\> New-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Kind ReadWrite -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="6fc6b-109">上述命令會在資源群組 "testrg" 中找到現有群集 "testnewkustocluster" 中，建立名為 "mykustodatabase" 的新 Kusto 資料庫。</span><span class="sxs-lookup"><span data-stu-id="6fc6b-109">The above command creates a new Kusto database named "mykustodatabase" in the existing cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="6fc6b-110">參數</span><span class="sxs-lookup"><span data-stu-id="6fc6b-110">PARAMETERS</span></span>

### <span data-ttu-id="6fc6b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6fc6b-111">-AsJob</span></span>
<span data-ttu-id="6fc6b-112">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="6fc6b-112">Run the command as a job</span></span>

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

### <span data-ttu-id="6fc6b-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="6fc6b-113">-ClusterName</span></span>
<span data-ttu-id="6fc6b-114">Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="6fc6b-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="6fc6b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fc6b-115">-DefaultProfile</span></span>
<span data-ttu-id="6fc6b-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6fc6b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fc6b-117">-HotCachePeriod</span><span class="sxs-lookup"><span data-stu-id="6fc6b-117">-HotCachePeriod</span></span>
<span data-ttu-id="6fc6b-118">資料在 cache 中應保留在快取中的時間。</span><span class="sxs-lookup"><span data-stu-id="6fc6b-118">The time the data should be kept in cache for fast queries in TimeSpan.</span></span>

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

### <span data-ttu-id="6fc6b-119">類型</span><span class="sxs-lookup"><span data-stu-id="6fc6b-119">-Kind</span></span>
<span data-ttu-id="6fc6b-120">資料庫的類型</span><span class="sxs-lookup"><span data-stu-id="6fc6b-120">Kind of the database</span></span>

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

### <span data-ttu-id="6fc6b-121">-位置</span><span class="sxs-lookup"><span data-stu-id="6fc6b-121">-Location</span></span>
<span data-ttu-id="6fc6b-122">資源位置。</span><span class="sxs-lookup"><span data-stu-id="6fc6b-122">Resource location.</span></span>

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

### <span data-ttu-id="6fc6b-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="6fc6b-123">-Name</span></span>
<span data-ttu-id="6fc6b-124">Kusto 群集中之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="6fc6b-124">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="6fc6b-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6fc6b-125">-NoWait</span></span>
<span data-ttu-id="6fc6b-126">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="6fc6b-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6fc6b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fc6b-127">-ResourceGroupName</span></span>
<span data-ttu-id="6fc6b-128">包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6fc6b-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="6fc6b-129">-SoftDeletePeriod</span><span class="sxs-lookup"><span data-stu-id="6fc6b-129">-SoftDeletePeriod</span></span>
<span data-ttu-id="6fc6b-130">資料在不能在時間跨度中停止存取前，應保留資料的時間。</span><span class="sxs-lookup"><span data-stu-id="6fc6b-130">The time the data should be kept before it stops being accessible to queries in TimeSpan.</span></span>

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

### <span data-ttu-id="6fc6b-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6fc6b-131">-SubscriptionId</span></span>
<span data-ttu-id="6fc6b-132">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="6fc6b-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6fc6b-133">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="6fc6b-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6fc6b-134">-確認</span><span class="sxs-lookup"><span data-stu-id="6fc6b-134">-Confirm</span></span>
<span data-ttu-id="6fc6b-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6fc6b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fc6b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fc6b-136">-WhatIf</span></span>
<span data-ttu-id="6fc6b-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6fc6b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fc6b-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6fc6b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fc6b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fc6b-139">CommonParameters</span></span>
<span data-ttu-id="6fc6b-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6fc6b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fc6b-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6fc6b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fc6b-142">輸入</span><span class="sxs-lookup"><span data-stu-id="6fc6b-142">INPUTS</span></span>

## <span data-ttu-id="6fc6b-143">輸出</span><span class="sxs-lookup"><span data-stu-id="6fc6b-143">OUTPUTS</span></span>

### <span data-ttu-id="6fc6b-144">IDatabase （Kusto）。 Api20200918。</span><span class="sxs-lookup"><span data-stu-id="6fc6b-144">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span></span>

## <span data-ttu-id="6fc6b-145">筆記</span><span class="sxs-lookup"><span data-stu-id="6fc6b-145">NOTES</span></span>

<span data-ttu-id="6fc6b-146">別名</span><span class="sxs-lookup"><span data-stu-id="6fc6b-146">ALIASES</span></span>

## <span data-ttu-id="6fc6b-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="6fc6b-147">RELATED LINKS</span></span>

