---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDatabase.md
ms.openlocfilehash: eb4c4e8318cf091662a9348ef9e786ec25d5436f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274988"
---
# <span data-ttu-id="941b4-101">Update-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="941b4-101">Update-AzKustoDatabase</span></span>

## <span data-ttu-id="941b4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="941b4-102">SYNOPSIS</span></span>
<span data-ttu-id="941b4-103">更新資料庫。</span><span class="sxs-lookup"><span data-stu-id="941b4-103">Updates a database.</span></span>

## <span data-ttu-id="941b4-104">句法</span><span class="sxs-lookup"><span data-stu-id="941b4-104">SYNTAX</span></span>

### <span data-ttu-id="941b4-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="941b4-105">UpdateExpanded (Default)</span></span>
```
Update-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-HotCachePeriod <TimeSpan>] [-SoftDeletePeriod <TimeSpan>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="941b4-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="941b4-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzKustoDatabase -InputObject <IKustoIdentity> -Kind <Kind> -Location <String>
 [-HotCachePeriod <TimeSpan>] [-SoftDeletePeriod <TimeSpan>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="941b4-107">說明</span><span class="sxs-lookup"><span data-stu-id="941b4-107">DESCRIPTION</span></span>
<span data-ttu-id="941b4-108">更新資料庫。</span><span class="sxs-lookup"><span data-stu-id="941b4-108">Updates a database.</span></span>

## <span data-ttu-id="941b4-109">示例</span><span class="sxs-lookup"><span data-stu-id="941b4-109">EXAMPLES</span></span>

### <span data-ttu-id="941b4-110">範例1：依名稱更新現有資料庫</span><span class="sxs-lookup"><span data-stu-id="941b4-110">Example 1: Update an existing database by name</span></span>
```powershell
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> $4ds = New-TimeSpan -Days 4
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Kind ReadWrite -SoftDeletePeriod $4ds -HotCachePeriod $2ds -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="941b4-111">上述命令會更新在資源群組 "testrg" 中找到的群集 "testnewkustocluster" 中，Kusto 資料庫 "mykustodatabase" 的虛刪除期間和熱緩存期間。</span><span class="sxs-lookup"><span data-stu-id="941b4-111">The above command updates the soft deletion period and hot cache period of the Kusto database "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="941b4-112">範例2：透過身分識別來更新現有的資料庫</span><span class="sxs-lookup"><span data-stu-id="941b4-112">Example 2: Update an existing database via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> $4ds = New-TimeSpan -Days 4
PS C:\> Update-AzKustoDatabase -InputObject $database -Kind ReadWrite -SoftDeletePeriod $4ds -HotCachePeriod $2ds -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="941b4-113">上述命令會更新在資源群組 "testrg" 中找到的群集 "testnewkustocluster" 中，Kusto 資料庫 "mykustodatabase" 的虛刪除期間和熱緩存期間。</span><span class="sxs-lookup"><span data-stu-id="941b4-113">The above command updates the soft deletion period and hot cache period of the Kusto database "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="941b4-114">範例3：依名稱更新現有的 ReadOnly 資料庫</span><span class="sxs-lookup"><span data-stu-id="941b4-114">Example 3: Update an existing ReadOnly database by name</span></span>
```powershell
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName myfollowercluster -Name mykustodatabase -Kind ReadOnlyFollowing -HotCachePeriod $2ds -Location 'East US'

Kind              Location Name                                Type
----              -------- ----                                ----
ReadOnlyFollowing East US  myfollowercluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="941b4-115">上述命令會更新在資源群組 "testrg" 中找到的群集 "myfollowercluster" 中的 Kusto 資料庫 "mykustodatabase" 的熱緩存期間。</span><span class="sxs-lookup"><span data-stu-id="941b4-115">The above command updates the hot cache period of the Kusto database "mykustodatabase" in the cluster "myfollowercluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="941b4-116">範例4：透過身分識別更新現有的 ReadOnly 資料庫</span><span class="sxs-lookup"><span data-stu-id="941b4-116">Example 4: Update an existing ReadOnly database via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName myfollowercluster -Name mykustodatabase
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> Update-AzKustoDatabase -InputObject $database -Kind ReadOnlyFollowing -HotCachePeriod $2ds -Location 'East US'

Kind              Location Name                                Type
----              -------- ----                                ----
ReadOnlyFollowing East US  myfollowercluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="941b4-117">上述命令會更新在資源群組 "testrg" 中找到的群集 "myfollowercluster" 中的 Kusto 資料庫 "mykustodatabase" 的熱緩存期間。</span><span class="sxs-lookup"><span data-stu-id="941b4-117">The above command updates the hot cache period of the Kusto database "mykustodatabase" in the cluster "myfollowercluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="941b4-118">參數</span><span class="sxs-lookup"><span data-stu-id="941b4-118">PARAMETERS</span></span>

### <span data-ttu-id="941b4-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="941b4-119">-AsJob</span></span>
<span data-ttu-id="941b4-120">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="941b4-120">Run the command as a job</span></span>

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

### <span data-ttu-id="941b4-121">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="941b4-121">-ClusterName</span></span>
<span data-ttu-id="941b4-122">Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="941b4-122">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="941b4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="941b4-123">-DefaultProfile</span></span>
<span data-ttu-id="941b4-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="941b4-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="941b4-125">-HotCachePeriod</span><span class="sxs-lookup"><span data-stu-id="941b4-125">-HotCachePeriod</span></span>
<span data-ttu-id="941b4-126">資料在 cache 中應保留在快取中的時間。</span><span class="sxs-lookup"><span data-stu-id="941b4-126">The time the data should be kept in cache for fast queries in TimeSpan.</span></span>

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

### <span data-ttu-id="941b4-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="941b4-127">-InputObject</span></span>
<span data-ttu-id="941b4-128">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="941b4-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="941b4-129">類型</span><span class="sxs-lookup"><span data-stu-id="941b4-129">-Kind</span></span>
<span data-ttu-id="941b4-130">資料庫的類型</span><span class="sxs-lookup"><span data-stu-id="941b4-130">Kind of the database</span></span>

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

### <span data-ttu-id="941b4-131">-位置</span><span class="sxs-lookup"><span data-stu-id="941b4-131">-Location</span></span>
<span data-ttu-id="941b4-132">資源位置。</span><span class="sxs-lookup"><span data-stu-id="941b4-132">Resource location.</span></span>

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

### <span data-ttu-id="941b4-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="941b4-133">-Name</span></span>
<span data-ttu-id="941b4-134">Kusto 群集中之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="941b4-134">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="941b4-135">-NoWait</span><span class="sxs-lookup"><span data-stu-id="941b4-135">-NoWait</span></span>
<span data-ttu-id="941b4-136">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="941b4-136">Run the command asynchronously</span></span>

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

### <span data-ttu-id="941b4-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="941b4-137">-ResourceGroupName</span></span>
<span data-ttu-id="941b4-138">包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="941b4-138">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="941b4-139">-SoftDeletePeriod</span><span class="sxs-lookup"><span data-stu-id="941b4-139">-SoftDeletePeriod</span></span>
<span data-ttu-id="941b4-140">資料在不能在時間跨度中停止存取前，應保留資料的時間。</span><span class="sxs-lookup"><span data-stu-id="941b4-140">The time the data should be kept before it stops being accessible to queries in TimeSpan.</span></span>

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

### <span data-ttu-id="941b4-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="941b4-141">-SubscriptionId</span></span>
<span data-ttu-id="941b4-142">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="941b4-142">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="941b4-143">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="941b4-143">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="941b4-144">-確認</span><span class="sxs-lookup"><span data-stu-id="941b4-144">-Confirm</span></span>
<span data-ttu-id="941b4-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="941b4-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="941b4-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="941b4-146">-WhatIf</span></span>
<span data-ttu-id="941b4-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="941b4-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="941b4-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="941b4-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="941b4-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="941b4-149">CommonParameters</span></span>
<span data-ttu-id="941b4-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="941b4-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="941b4-151">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="941b4-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="941b4-152">輸入</span><span class="sxs-lookup"><span data-stu-id="941b4-152">INPUTS</span></span>

### <span data-ttu-id="941b4-153">IKustoIdentity （Kusto）的</span><span class="sxs-lookup"><span data-stu-id="941b4-153">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="941b4-154">輸出</span><span class="sxs-lookup"><span data-stu-id="941b4-154">OUTPUTS</span></span>

### <span data-ttu-id="941b4-155">IDatabase （Kusto）。 Api20200614。</span><span class="sxs-lookup"><span data-stu-id="941b4-155">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabase</span></span>

## <span data-ttu-id="941b4-156">筆記</span><span class="sxs-lookup"><span data-stu-id="941b4-156">NOTES</span></span>

<span data-ttu-id="941b4-157">別名</span><span class="sxs-lookup"><span data-stu-id="941b4-157">ALIASES</span></span>

<span data-ttu-id="941b4-158">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="941b4-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="941b4-159">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="941b4-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="941b4-160">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="941b4-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="941b4-161">INPUTOBJECT <IKustoIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="941b4-161">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="941b4-162">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="941b4-162">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="941b4-163">`[ClusterName <String>]`： Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="941b4-163">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="941b4-164">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="941b4-164">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="941b4-165">`[DatabaseName <String>]`： Kusto 群集中之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="941b4-165">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="941b4-166">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="941b4-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="941b4-167">`[Location <String>]`： Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="941b4-167">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="941b4-168">`[PrincipalAssignmentName <String>]`： Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="941b4-168">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="941b4-169">`[ResourceGroupName <String>]`：包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="941b4-169">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="941b4-170">`[SubscriptionId <String>]`：取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="941b4-170">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="941b4-171">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="941b4-171">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="941b4-172">相關連結</span><span class="sxs-lookup"><span data-stu-id="941b4-172">RELATED LINKS</span></span>

