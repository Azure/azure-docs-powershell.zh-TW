---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodetachclusterfollowerdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
ms.openlocfilehash: 80994e2966ccb33bfaff0e2de2c70827c491108b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449085"
---
# <span data-ttu-id="2b402-101">Invoke-AzKustoDetachClusterFollowerDatabase</span><span class="sxs-lookup"><span data-stu-id="2b402-101">Invoke-AzKustoDetachClusterFollowerDatabase</span></span>

## <span data-ttu-id="2b402-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2b402-102">SYNOPSIS</span></span>
<span data-ttu-id="2b402-103">分離這個群集擁有之資料庫的所有關注者。</span><span class="sxs-lookup"><span data-stu-id="2b402-103">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="2b402-104">句法</span><span class="sxs-lookup"><span data-stu-id="2b402-104">SYNTAX</span></span>

### <span data-ttu-id="2b402-105">DetachExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="2b402-105">DetachExpanded (Default)</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -ClusterName <String> -ResourceGroupName <String>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2b402-106">DetachViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="2b402-106">DetachViaIdentityExpanded</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -InputObject <IKustoIdentity>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2b402-107">說明</span><span class="sxs-lookup"><span data-stu-id="2b402-107">DESCRIPTION</span></span>
<span data-ttu-id="2b402-108">分離這個群集擁有之資料庫的所有關注者。</span><span class="sxs-lookup"><span data-stu-id="2b402-108">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="2b402-109">示例</span><span class="sxs-lookup"><span data-stu-id="2b402-109">EXAMPLES</span></span>

### <span data-ttu-id="2b402-110">範例1：分離從動資料庫</span><span class="sxs-lookup"><span data-stu-id="2b402-110">Example 1: Detach a follower database</span></span>
```powershell
PS C:\> Invoke-AzKustoDetachClusterFollowerDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -AttachedDatabaseConfigurationName "myfollowerconfiguration" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustoclusterf"

```

<span data-ttu-id="2b402-111">上述命令會從 [群集] testnewkustoclusterf 中，將 AttachedDatabaseConfiguration "myfollowerconfiguration" 中定義的從動資料庫分離。</span><span class="sxs-lookup"><span data-stu-id="2b402-111">The above command detaches the follower database defined in AttachedDatabaseConfiguration "myfollowerconfiguration" from cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="2b402-112">參數</span><span class="sxs-lookup"><span data-stu-id="2b402-112">PARAMETERS</span></span>

### <span data-ttu-id="2b402-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2b402-113">-AsJob</span></span>
<span data-ttu-id="2b402-114">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="2b402-114">Run the command as a job</span></span>

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

### <span data-ttu-id="2b402-115">-AttachedDatabaseConfigurationName</span><span class="sxs-lookup"><span data-stu-id="2b402-115">-AttachedDatabaseConfigurationName</span></span>
<span data-ttu-id="2b402-116">在從動機構群集中附加的資料庫配置的資源名稱。</span><span class="sxs-lookup"><span data-stu-id="2b402-116">Resource name of the attached database configuration in the follower cluster.</span></span>

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

### <span data-ttu-id="2b402-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2b402-117">-ClusterName</span></span>
<span data-ttu-id="2b402-118">Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b402-118">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DetachExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b402-119">-ClusterResourceId</span><span class="sxs-lookup"><span data-stu-id="2b402-119">-ClusterResourceId</span></span>
<span data-ttu-id="2b402-120">該群集所擁有之資料庫的群集資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2b402-120">Resource id of the cluster that follows a database owned by this cluster.</span></span>

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

### <span data-ttu-id="2b402-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b402-121">-DefaultProfile</span></span>
<span data-ttu-id="2b402-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2b402-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b402-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b402-123">-InputObject</span></span>
<span data-ttu-id="2b402-124">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="2b402-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DetachViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b402-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2b402-125">-NoWait</span></span>
<span data-ttu-id="2b402-126">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="2b402-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2b402-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b402-127">-PassThru</span></span>
<span data-ttu-id="2b402-128">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="2b402-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2b402-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b402-129">-ResourceGroupName</span></span>
<span data-ttu-id="2b402-130">包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b402-130">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DetachExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b402-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2b402-131">-SubscriptionId</span></span>
<span data-ttu-id="2b402-132">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="2b402-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2b402-133">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="2b402-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: DetachExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b402-134">-確認</span><span class="sxs-lookup"><span data-stu-id="2b402-134">-Confirm</span></span>
<span data-ttu-id="2b402-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2b402-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b402-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b402-136">-WhatIf</span></span>
<span data-ttu-id="2b402-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2b402-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b402-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2b402-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b402-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b402-139">CommonParameters</span></span>
<span data-ttu-id="2b402-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2b402-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b402-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2b402-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b402-142">輸入</span><span class="sxs-lookup"><span data-stu-id="2b402-142">INPUTS</span></span>

### <span data-ttu-id="2b402-143">IKustoIdentity （Kusto）的</span><span class="sxs-lookup"><span data-stu-id="2b402-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="2b402-144">輸出</span><span class="sxs-lookup"><span data-stu-id="2b402-144">OUTPUTS</span></span>

### <span data-ttu-id="2b402-145">System.object</span><span class="sxs-lookup"><span data-stu-id="2b402-145">System.Boolean</span></span>

## <span data-ttu-id="2b402-146">筆記</span><span class="sxs-lookup"><span data-stu-id="2b402-146">NOTES</span></span>

<span data-ttu-id="2b402-147">別名</span><span class="sxs-lookup"><span data-stu-id="2b402-147">ALIASES</span></span>

<span data-ttu-id="2b402-148">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="2b402-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2b402-149">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="2b402-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2b402-150">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="2b402-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2b402-151">INPUTOBJECT <IKustoIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="2b402-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2b402-152">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b402-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="2b402-153">`[ClusterName <String>]`： Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b402-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="2b402-154">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b402-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="2b402-155">`[DatabaseName <String>]`： Kusto 群集中之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b402-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="2b402-156">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="2b402-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2b402-157">`[Location <String>]`： Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="2b402-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="2b402-158">`[PrincipalAssignmentName <String>]`： Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b402-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="2b402-159">`[ResourceGroupName <String>]`：包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b402-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="2b402-160">`[SubscriptionId <String>]`：取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="2b402-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2b402-161">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="2b402-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="2b402-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="2b402-162">RELATED LINKS</span></span>

