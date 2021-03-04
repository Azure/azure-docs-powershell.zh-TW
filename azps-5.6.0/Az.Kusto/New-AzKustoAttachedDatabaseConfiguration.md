---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/new-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: 6b540b82ed07e42a6789a2603299508c21c7c3aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909793"
---
# <span data-ttu-id="76c32-101">New-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="76c32-101">New-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="76c32-102">簡介</span><span class="sxs-lookup"><span data-stu-id="76c32-102">SYNOPSIS</span></span>
<span data-ttu-id="76c32-103">建立或更新附加的資料庫組配置。</span><span class="sxs-lookup"><span data-stu-id="76c32-103">Creates or updates an attached database configuration.</span></span>

## <span data-ttu-id="76c32-104">語法</span><span class="sxs-lookup"><span data-stu-id="76c32-104">SYNTAX</span></span>

```
New-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterResourceId <String>] [-DatabaseName <String>]
 [-DefaultPrincipalsModificationKind <DefaultPrincipalsModificationKind>] [-Location <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="76c32-105">描述</span><span class="sxs-lookup"><span data-stu-id="76c32-105">DESCRIPTION</span></span>
<span data-ttu-id="76c32-106">建立或更新附加的資料庫組配置。</span><span class="sxs-lookup"><span data-stu-id="76c32-106">Creates or updates an attached database configuration.</span></span>

## <span data-ttu-id="76c32-107">例子</span><span class="sxs-lookup"><span data-stu-id="76c32-107">EXAMPLES</span></span>

### <span data-ttu-id="76c32-108">範例 1：建立新 AttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="76c32-108">Example 1: Create a new AttachedDatabaseConfiguration</span></span>
```powershell
PS C:\> New-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration" -Location "East US" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustocluster" -DatabaseName "mykustodatabase" -DefaultPrincipalsModificationKind "Union"

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="76c32-109">上述命令在叢集「testnewkustoclusterf」中建立 ReadOnly 資料庫"mykustodatabase"。</span><span class="sxs-lookup"><span data-stu-id="76c32-109">The above command creates a ReadOnly database "mykustodatabase" in cluster "testnewkustoclusterf".</span></span>
<span data-ttu-id="76c32-110">它遵循來自叢集"testnewkustocluster" 的資料庫"mykustodatabase"</span><span class="sxs-lookup"><span data-stu-id="76c32-110">It follows the database "mykustodatabase" from cluster "testnewkustocluster"</span></span>

## <span data-ttu-id="76c32-111">參數</span><span class="sxs-lookup"><span data-stu-id="76c32-111">PARAMETERS</span></span>

### <span data-ttu-id="76c32-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76c32-112">-AsJob</span></span>
<span data-ttu-id="76c32-113">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="76c32-113">Run the command as a job</span></span>

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

### <span data-ttu-id="76c32-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="76c32-114">-ClusterName</span></span>
<span data-ttu-id="76c32-115">Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="76c32-115">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="76c32-116">-ClusterResourceId</span><span class="sxs-lookup"><span data-stu-id="76c32-116">-ClusterResourceId</span></span>
<span data-ttu-id="76c32-117">要附加之資料庫所在的組群資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="76c32-117">The resource id of the cluster where the databases you would like to attach reside.</span></span>

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

### <span data-ttu-id="76c32-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="76c32-118">-DatabaseName</span></span>
<span data-ttu-id="76c32-119">如果您想要附加的資料庫名稱，如果您想要追蹤所有目前和未來的資料庫，請使用 \*。</span><span class="sxs-lookup"><span data-stu-id="76c32-119">The name of the database which you would like to attach, use \* if you want to follow all current and future databases.</span></span>

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

### <span data-ttu-id="76c32-120">-DefaultPrincipalsModificationKind</span><span class="sxs-lookup"><span data-stu-id="76c32-120">-DefaultPrincipalsModificationKind</span></span>
<span data-ttu-id="76c32-121">預設主體修改類型</span><span class="sxs-lookup"><span data-stu-id="76c32-121">The default principals modification kind</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.DefaultPrincipalsModificationKind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76c32-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76c32-122">-DefaultProfile</span></span>
<span data-ttu-id="76c32-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="76c32-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76c32-124">-位置</span><span class="sxs-lookup"><span data-stu-id="76c32-124">-Location</span></span>
<span data-ttu-id="76c32-125">資源位置。</span><span class="sxs-lookup"><span data-stu-id="76c32-125">Resource location.</span></span>

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

### <span data-ttu-id="76c32-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="76c32-126">-Name</span></span>
<span data-ttu-id="76c32-127">附加資料庫組配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="76c32-127">The name of the attached database configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AttachedDatabaseConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76c32-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="76c32-128">-NoWait</span></span>
<span data-ttu-id="76c32-129">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="76c32-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="76c32-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76c32-130">-ResourceGroupName</span></span>
<span data-ttu-id="76c32-131">包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="76c32-131">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="76c32-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="76c32-132">-SubscriptionId</span></span>
<span data-ttu-id="76c32-133">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="76c32-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="76c32-134">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="76c32-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="76c32-135">-確認</span><span class="sxs-lookup"><span data-stu-id="76c32-135">-Confirm</span></span>
<span data-ttu-id="76c32-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="76c32-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76c32-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76c32-137">-WhatIf</span></span>
<span data-ttu-id="76c32-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="76c32-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76c32-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="76c32-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76c32-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76c32-140">CommonParameters</span></span>
<span data-ttu-id="76c32-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="76c32-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76c32-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76c32-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76c32-143">輸入</span><span class="sxs-lookup"><span data-stu-id="76c32-143">INPUTS</span></span>

## <span data-ttu-id="76c32-144">輸出</span><span class="sxs-lookup"><span data-stu-id="76c32-144">OUTPUTS</span></span>

### <span data-ttu-id="76c32-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="76c32-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="76c32-146">筆記</span><span class="sxs-lookup"><span data-stu-id="76c32-146">NOTES</span></span>

<span data-ttu-id="76c32-147">別名</span><span class="sxs-lookup"><span data-stu-id="76c32-147">ALIASES</span></span>

## <span data-ttu-id="76c32-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="76c32-148">RELATED LINKS</span></span>

