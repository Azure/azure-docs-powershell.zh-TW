---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodetachclusterfollowerdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
ms.openlocfilehash: 80994e2966ccb33bfaff0e2de2c70827c491108b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142999"
---
# <span data-ttu-id="7fc1c-101">Invoke-AzKustoDetachClusterFollowerDatabase</span><span class="sxs-lookup"><span data-stu-id="7fc1c-101">Invoke-AzKustoDetachClusterFollowerDatabase</span></span>

## <span data-ttu-id="7fc1c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7fc1c-102">SYNOPSIS</span></span>
<span data-ttu-id="7fc1c-103">分離這個群集擁有之資料庫的所有關注者。</span><span class="sxs-lookup"><span data-stu-id="7fc1c-103">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="7fc1c-104">句法</span><span class="sxs-lookup"><span data-stu-id="7fc1c-104">SYNTAX</span></span>

### <span data-ttu-id="7fc1c-105">DetachExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="7fc1c-105">DetachExpanded (Default)</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -ClusterName <String> -ResourceGroupName <String>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7fc1c-106">DetachViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="7fc1c-106">DetachViaIdentityExpanded</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -InputObject <IKustoIdentity>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7fc1c-107">說明</span><span class="sxs-lookup"><span data-stu-id="7fc1c-107">DESCRIPTION</span></span>
<span data-ttu-id="7fc1c-108">分離這個群集擁有之資料庫的所有關注者。</span><span class="sxs-lookup"><span data-stu-id="7fc1c-108">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="7fc1c-109">示例</span><span class="sxs-lookup"><span data-stu-id="7fc1c-109">EXAMPLES</span></span>

### <span data-ttu-id="7fc1c-110">範例1：分離從動資料庫</span><span class="sxs-lookup"><span data-stu-id="7fc1c-110">Example 1: Detach a follower database</span></span>
```powershell
PS C:\> Invoke-AzKustoDetachClusterFollowerDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -AttachedDatabaseConfigurationName "myfollowerconfiguration" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustoclusterf"

```

<span data-ttu-id="7fc1c-111">上述命令會從 [群集] testnewkustoclusterf 中，將 AttachedDatabaseConfiguration "myfollowerconfiguration" 中定義的從動資料庫分離。</span><span class="sxs-lookup"><span data-stu-id="7fc1c-111">The above command detaches the follower database defined in AttachedDatabaseConfiguration "myfollowerconfiguration" from cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="7fc1c-112">參數</span><span class="sxs-lookup"><span data-stu-id="7fc1c-112">PARAMETERS</span></span>

### <span data-ttu-id="7fc1c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7fc1c-113">-AsJob</span></span>
<span data-ttu-id="7fc1c-114">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="7fc1c-114">Run the command as a job</span></span>

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

### <span data-ttu-id="7fc1c-115">-AttachedDatabaseConfigurationName</span><span class="sxs-lookup"><span data-stu-id="7fc1c-115">-AttachedDatabaseConfigurationName</span></span>
<span data-ttu-id="7fc1c-116">在從動機構群集中附加的資料庫配置的資源名稱。</span><span class="sxs-lookup"><span data-stu-id="7fc1c-116">Resource name of the attached database configuration in the follower cluster.</span></span>

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

### <span data-ttu-id="7fc1c-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="7fc1c-117">-ClusterName</span></span>
<span data-ttu-id="7fc1c-118">Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="7fc1c-118">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="7fc1c-119">-ClusterResourceId</span><span class="sxs-lookup"><span data-stu-id="7fc1c-119">-ClusterResourceId</span></span>
<span data-ttu-id="7fc1c-120">該群集所擁有之資料庫的群集資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="7fc1c-120">Resource id of the cluster that follows a database owned by this cluster.</span></span>

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

### <span data-ttu-id="7fc1c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fc1c-121">-DefaultProfile</span></span>
<span data-ttu-id="7fc1c-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7fc1c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fc1c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7fc1c-123">-InputObject</span></span>
<span data-ttu-id="7fc1c-124">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="7fc1c-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7fc1c-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7fc1c-125">-NoWait</span></span>
<span data-ttu-id="7fc1c-126">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="7fc1c-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7fc1c-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7fc1c-127">-PassThru</span></span>
<span data-ttu-id="7fc1c-128">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="7fc1c-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7fc1c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fc1c-129">-ResourceGroupName</span></span>
<span data-ttu-id="7fc1c-130">包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7fc1c-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="7fc1c-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7fc1c-131">-SubscriptionId</span></span>
<span data-ttu-id="7fc1c-132">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="7fc1c-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7fc1c-133">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="7fc1c-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7fc1c-134">-確認</span><span class="sxs-lookup"><span data-stu-id="7fc1c-134">-Confirm</span></span>
<span data-ttu-id="7fc1c-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7fc1c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fc1c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fc1c-136">-WhatIf</span></span>
<span data-ttu-id="7fc1c-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7fc1c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fc1c-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7fc1c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fc1c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fc1c-139">CommonParameters</span></span>
<span data-ttu-id="7fc1c-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7fc1c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fc1c-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7fc1c-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fc1c-142">輸入</span><span class="sxs-lookup"><span data-stu-id="7fc1c-142">INPUTS</span></span>

### <span data-ttu-id="7fc1c-143">IKustoIdentity （Kusto）的</span><span class="sxs-lookup"><span data-stu-id="7fc1c-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="7fc1c-144">輸出</span><span class="sxs-lookup"><span data-stu-id="7fc1c-144">OUTPUTS</span></span>

### <span data-ttu-id="7fc1c-145">System.object</span><span class="sxs-lookup"><span data-stu-id="7fc1c-145">System.Boolean</span></span>

## <span data-ttu-id="7fc1c-146">筆記</span><span class="sxs-lookup"><span data-stu-id="7fc1c-146">NOTES</span></span>

<span data-ttu-id="7fc1c-147">別名</span><span class="sxs-lookup"><span data-stu-id="7fc1c-147">ALIASES</span></span>

<span data-ttu-id="7fc1c-148">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="7fc1c-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7fc1c-149">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="7fc1c-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7fc1c-150">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="7fc1c-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7fc1c-151">INPUTOBJECT <IKustoIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="7fc1c-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7fc1c-152">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="7fc1c-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="7fc1c-153">`[ClusterName <String>]`： Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="7fc1c-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="7fc1c-154">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="7fc1c-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="7fc1c-155">`[DatabaseName <String>]`： Kusto 群集中之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="7fc1c-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="7fc1c-156">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="7fc1c-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7fc1c-157">`[Location <String>]`： Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="7fc1c-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="7fc1c-158">`[PrincipalAssignmentName <String>]`： Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="7fc1c-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="7fc1c-159">`[ResourceGroupName <String>]`：包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7fc1c-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="7fc1c-160">`[SubscriptionId <String>]`：取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="7fc1c-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="7fc1c-161">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="7fc1c-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="7fc1c-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="7fc1c-162">RELATED LINKS</span></span>

