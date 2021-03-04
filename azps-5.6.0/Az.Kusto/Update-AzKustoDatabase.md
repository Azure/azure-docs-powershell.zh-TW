---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/update-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDatabase.md
ms.openlocfilehash: 76e712a881c88490a71933056f82fe1959df2948
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902882"
---
# <span data-ttu-id="3f97e-101">Update-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="3f97e-101">Update-AzKustoDatabase</span></span>

## <span data-ttu-id="3f97e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3f97e-102">SYNOPSIS</span></span>
<span data-ttu-id="3f97e-103">更新資料庫。</span><span class="sxs-lookup"><span data-stu-id="3f97e-103">Updates a database.</span></span>

## <span data-ttu-id="3f97e-104">語法</span><span class="sxs-lookup"><span data-stu-id="3f97e-104">SYNTAX</span></span>

### <span data-ttu-id="3f97e-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="3f97e-105">UpdateExpanded (Default)</span></span>
```
Update-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-HotCachePeriod <TimeSpan>] [-SoftDeletePeriod <TimeSpan>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3f97e-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3f97e-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzKustoDatabase -InputObject <IKustoIdentity> -Kind <Kind> -Location <String>
 [-HotCachePeriod <TimeSpan>] [-SoftDeletePeriod <TimeSpan>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3f97e-107">描述</span><span class="sxs-lookup"><span data-stu-id="3f97e-107">DESCRIPTION</span></span>
<span data-ttu-id="3f97e-108">更新資料庫。</span><span class="sxs-lookup"><span data-stu-id="3f97e-108">Updates a database.</span></span>

## <span data-ttu-id="3f97e-109">例子</span><span class="sxs-lookup"><span data-stu-id="3f97e-109">EXAMPLES</span></span>

### <span data-ttu-id="3f97e-110">範例 1：根據名稱更新現有資料庫</span><span class="sxs-lookup"><span data-stu-id="3f97e-110">Example 1: Update an existing database by name</span></span>
```powershell
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> $4ds = New-TimeSpan -Days 4
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Kind ReadWrite -SoftDeletePeriod $4ds -HotCachePeriod $2ds -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="3f97e-111">上述命令會更新在資源群組"testrg"找到的群組"testnewkustocluster"中，Kusto 資料庫 "mykustodatabase" 的柔刪除期間和快快時段。</span><span class="sxs-lookup"><span data-stu-id="3f97e-111">The above command updates the soft deletion period and hot cache period of the Kusto database "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="3f97e-112">範例 2：透過身分識別更新現有資料庫</span><span class="sxs-lookup"><span data-stu-id="3f97e-112">Example 2: Update an existing database via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> $4ds = New-TimeSpan -Days 4
PS C:\> Update-AzKustoDatabase -InputObject $database -Kind ReadWrite -SoftDeletePeriod $4ds -HotCachePeriod $2ds -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="3f97e-113">上述命令會更新在資源群組"testrg"找到的群組"testnewkustocluster"中，Kusto 資料庫 "mykustodatabase" 的柔刪除期間和快快時段。</span><span class="sxs-lookup"><span data-stu-id="3f97e-113">The above command updates the soft deletion period and hot cache period of the Kusto database "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="3f97e-114">範例 3：根據名稱更新現有的 ReadOnly 資料庫</span><span class="sxs-lookup"><span data-stu-id="3f97e-114">Example 3: Update an existing ReadOnly database by name</span></span>
```powershell
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName myfollowercluster -Name mykustodatabase -Kind ReadOnlyFollowing -HotCachePeriod $2ds -Location 'East US'

Kind              Location Name                                Type
----              -------- ----                                ----
ReadOnlyFollowing East US  myfollowercluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="3f97e-115">上述命令會更新在資源群組"testrg"找到的群組"myfollollcluster"中，Kusto 資料庫「mykustodatabase」的熱門緩存期間。</span><span class="sxs-lookup"><span data-stu-id="3f97e-115">The above command updates the hot cache period of the Kusto database "mykustodatabase" in the cluster "myfollowercluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="3f97e-116">範例 4：透過身分識別更新現有的 ReadOnly 資料庫</span><span class="sxs-lookup"><span data-stu-id="3f97e-116">Example 4: Update an existing ReadOnly database via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName myfollowercluster -Name mykustodatabase
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> Update-AzKustoDatabase -InputObject $database -Kind ReadOnlyFollowing -HotCachePeriod $2ds -Location 'East US'

Kind              Location Name                                Type
----              -------- ----                                ----
ReadOnlyFollowing East US  myfollowercluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="3f97e-117">上述命令會更新在資源群組"testrg"找到的群組"myfollollcluster"中，Kusto 資料庫「mykustodatabase」的熱門緩存期間。</span><span class="sxs-lookup"><span data-stu-id="3f97e-117">The above command updates the hot cache period of the Kusto database "mykustodatabase" in the cluster "myfollowercluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="3f97e-118">參數</span><span class="sxs-lookup"><span data-stu-id="3f97e-118">PARAMETERS</span></span>

### <span data-ttu-id="3f97e-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f97e-119">-AsJob</span></span>
<span data-ttu-id="3f97e-120">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="3f97e-120">Run the command as a job</span></span>

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

### <span data-ttu-id="3f97e-121">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="3f97e-121">-ClusterName</span></span>
<span data-ttu-id="3f97e-122">Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="3f97e-122">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="3f97e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f97e-123">-DefaultProfile</span></span>
<span data-ttu-id="3f97e-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3f97e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f97e-125">-HotCachePeriod</span><span class="sxs-lookup"><span data-stu-id="3f97e-125">-HotCachePeriod</span></span>
<span data-ttu-id="3f97e-126">資料應保留在快處理中的時間，以在時間跨時間進行快速查詢。</span><span class="sxs-lookup"><span data-stu-id="3f97e-126">The time the data should be kept in cache for fast queries in TimeSpan.</span></span>

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

### <span data-ttu-id="3f97e-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f97e-127">-InputObject</span></span>
<span data-ttu-id="3f97e-128">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="3f97e-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3f97e-129">-Kind</span><span class="sxs-lookup"><span data-stu-id="3f97e-129">-Kind</span></span>
<span data-ttu-id="3f97e-130">資料庫類型</span><span class="sxs-lookup"><span data-stu-id="3f97e-130">Kind of the database</span></span>

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

### <span data-ttu-id="3f97e-131">-位置</span><span class="sxs-lookup"><span data-stu-id="3f97e-131">-Location</span></span>
<span data-ttu-id="3f97e-132">資源位置。</span><span class="sxs-lookup"><span data-stu-id="3f97e-132">Resource location.</span></span>

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

### <span data-ttu-id="3f97e-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="3f97e-133">-Name</span></span>
<span data-ttu-id="3f97e-134">Kusto cluster 中的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="3f97e-134">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="3f97e-135">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3f97e-135">-NoWait</span></span>
<span data-ttu-id="3f97e-136">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="3f97e-136">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3f97e-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f97e-137">-ResourceGroupName</span></span>
<span data-ttu-id="3f97e-138">包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="3f97e-138">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="3f97e-139">-SoftDeletePeriod</span><span class="sxs-lookup"><span data-stu-id="3f97e-139">-SoftDeletePeriod</span></span>
<span data-ttu-id="3f97e-140">資料在時間跨行中停止可供查詢使用之前，應該保留的時間。</span><span class="sxs-lookup"><span data-stu-id="3f97e-140">The time the data should be kept before it stops being accessible to queries in TimeSpan.</span></span>

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

### <span data-ttu-id="3f97e-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3f97e-141">-SubscriptionId</span></span>
<span data-ttu-id="3f97e-142">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="3f97e-142">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3f97e-143">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="3f97e-143">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3f97e-144">-確認</span><span class="sxs-lookup"><span data-stu-id="3f97e-144">-Confirm</span></span>
<span data-ttu-id="3f97e-145">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3f97e-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f97e-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f97e-146">-WhatIf</span></span>
<span data-ttu-id="3f97e-147">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3f97e-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f97e-148">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3f97e-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f97e-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f97e-149">CommonParameters</span></span>
<span data-ttu-id="3f97e-150">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3f97e-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f97e-151">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3f97e-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f97e-152">輸入</span><span class="sxs-lookup"><span data-stu-id="3f97e-152">INPUTS</span></span>

### <span data-ttu-id="3f97e-153">Microsoft.Azure.PowerShell.Cmdlets.Kusto.models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="3f97e-153">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="3f97e-154">輸出</span><span class="sxs-lookup"><span data-stu-id="3f97e-154">OUTPUTS</span></span>

### <span data-ttu-id="3f97e-155">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span><span class="sxs-lookup"><span data-stu-id="3f97e-155">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span></span>

## <span data-ttu-id="3f97e-156">筆記</span><span class="sxs-lookup"><span data-stu-id="3f97e-156">NOTES</span></span>

<span data-ttu-id="3f97e-157">別名</span><span class="sxs-lookup"><span data-stu-id="3f97e-157">ALIASES</span></span>

<span data-ttu-id="3f97e-158">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="3f97e-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3f97e-159">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="3f97e-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3f97e-160">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="3f97e-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3f97e-161">INPUTOBJECT： <IKustoIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="3f97e-161">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3f97e-162">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫組配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="3f97e-162">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="3f97e-163">`[ClusterName <String>]`：Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="3f97e-163">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="3f97e-164">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="3f97e-164">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="3f97e-165">`[DatabaseName <String>]`：Kusto cluster 中的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="3f97e-165">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="3f97e-166">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="3f97e-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3f97e-167">`[Location <String>]`：Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="3f97e-167">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="3f97e-168">`[PrincipalAssignmentName <String>]`：Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="3f97e-168">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="3f97e-169">`[ResourceGroupName <String>]`：包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="3f97e-169">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="3f97e-170">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="3f97e-170">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3f97e-171">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="3f97e-171">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="3f97e-172">相關連結</span><span class="sxs-lookup"><span data-stu-id="3f97e-172">RELATED LINKS</span></span>

