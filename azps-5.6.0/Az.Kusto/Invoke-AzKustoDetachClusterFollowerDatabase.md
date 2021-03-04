---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/invoke-azkustodetachclusterfollowerdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
ms.openlocfilehash: f410ba5dc89f29c3a928ed459be87769bf5ffca7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904101"
---
# <span data-ttu-id="f6484-101">Invoke-AzKustoDetachClusterFollowerDatabase</span><span class="sxs-lookup"><span data-stu-id="f6484-101">Invoke-AzKustoDetachClusterFollowerDatabase</span></span>

## <span data-ttu-id="f6484-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f6484-102">SYNOPSIS</span></span>
<span data-ttu-id="f6484-103">將此組所擁有之資料庫的所有關注者分開。</span><span class="sxs-lookup"><span data-stu-id="f6484-103">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="f6484-104">語法</span><span class="sxs-lookup"><span data-stu-id="f6484-104">SYNTAX</span></span>

### <span data-ttu-id="f6484-105">將Expanded (預設) </span><span class="sxs-lookup"><span data-stu-id="f6484-105">DetachExpanded (Default)</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -ClusterName <String> -ResourceGroupName <String>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f6484-106">DetachViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f6484-106">DetachViaIdentityExpanded</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -InputObject <IKustoIdentity>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f6484-107">描述</span><span class="sxs-lookup"><span data-stu-id="f6484-107">DESCRIPTION</span></span>
<span data-ttu-id="f6484-108">將此組所擁有之資料庫的所有關注者分開。</span><span class="sxs-lookup"><span data-stu-id="f6484-108">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="f6484-109">例子</span><span class="sxs-lookup"><span data-stu-id="f6484-109">EXAMPLES</span></span>

### <span data-ttu-id="f6484-110">範例 1：將追蹤者資料庫分開</span><span class="sxs-lookup"><span data-stu-id="f6484-110">Example 1: Detach a follower database</span></span>
```powershell
PS C:\> Invoke-AzKustoDetachClusterFollowerDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -AttachedDatabaseConfigurationName "myfollowerconfiguration" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustoclusterf"

```

<span data-ttu-id="f6484-111">上述命令將 AttachedDatabaseConfiguration "myfollollconfiguration" 中定義的追蹤者資料庫與叢集 "testnewkustoclusterf" 分離。</span><span class="sxs-lookup"><span data-stu-id="f6484-111">The above command detaches the follower database defined in AttachedDatabaseConfiguration "myfollowerconfiguration" from cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="f6484-112">參數</span><span class="sxs-lookup"><span data-stu-id="f6484-112">PARAMETERS</span></span>

### <span data-ttu-id="f6484-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f6484-113">-AsJob</span></span>
<span data-ttu-id="f6484-114">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="f6484-114">Run the command as a job</span></span>

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

### <span data-ttu-id="f6484-115">-AttachedDatabaseConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f6484-115">-AttachedDatabaseConfigurationName</span></span>
<span data-ttu-id="f6484-116">追蹤者集中附加資料庫組配置的資源名稱。</span><span class="sxs-lookup"><span data-stu-id="f6484-116">Resource name of the attached database configuration in the follower cluster.</span></span>

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

### <span data-ttu-id="f6484-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f6484-117">-ClusterName</span></span>
<span data-ttu-id="f6484-118">Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="f6484-118">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="f6484-119">-ClusterResourceId</span><span class="sxs-lookup"><span data-stu-id="f6484-119">-ClusterResourceId</span></span>
<span data-ttu-id="f6484-120">此組所擁有的資料庫後之該組組的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f6484-120">Resource id of the cluster that follows a database owned by this cluster.</span></span>

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

### <span data-ttu-id="f6484-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6484-121">-DefaultProfile</span></span>
<span data-ttu-id="f6484-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f6484-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6484-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6484-123">-InputObject</span></span>
<span data-ttu-id="f6484-124">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f6484-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f6484-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f6484-125">-NoWait</span></span>
<span data-ttu-id="f6484-126">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="f6484-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f6484-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f6484-127">-PassThru</span></span>
<span data-ttu-id="f6484-128">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="f6484-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f6484-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6484-129">-ResourceGroupName</span></span>
<span data-ttu-id="f6484-130">包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="f6484-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="f6484-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f6484-131">-SubscriptionId</span></span>
<span data-ttu-id="f6484-132">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="f6484-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f6484-133">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="f6484-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f6484-134">-確認</span><span class="sxs-lookup"><span data-stu-id="f6484-134">-Confirm</span></span>
<span data-ttu-id="f6484-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f6484-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6484-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6484-136">-WhatIf</span></span>
<span data-ttu-id="f6484-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f6484-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6484-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6484-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6484-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6484-139">CommonParameters</span></span>
<span data-ttu-id="f6484-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f6484-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6484-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f6484-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6484-142">輸入</span><span class="sxs-lookup"><span data-stu-id="f6484-142">INPUTS</span></span>

### <span data-ttu-id="f6484-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="f6484-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="f6484-144">輸出</span><span class="sxs-lookup"><span data-stu-id="f6484-144">OUTPUTS</span></span>

### <span data-ttu-id="f6484-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f6484-145">System.Boolean</span></span>

## <span data-ttu-id="f6484-146">筆記</span><span class="sxs-lookup"><span data-stu-id="f6484-146">NOTES</span></span>

<span data-ttu-id="f6484-147">別名</span><span class="sxs-lookup"><span data-stu-id="f6484-147">ALIASES</span></span>

<span data-ttu-id="f6484-148">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="f6484-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f6484-149">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f6484-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f6484-150">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="f6484-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f6484-151">INPUTOBJECT： <IKustoIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="f6484-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f6484-152">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫組配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6484-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="f6484-153">`[ClusterName <String>]`：Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="f6484-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="f6484-154">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6484-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="f6484-155">`[DatabaseName <String>]`：Kusto cluster 中的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="f6484-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="f6484-156">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="f6484-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f6484-157">`[Location <String>]`：Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="f6484-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="f6484-158">`[PrincipalAssignmentName <String>]`：Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6484-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="f6484-159">`[ResourceGroupName <String>]`：包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="f6484-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="f6484-160">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="f6484-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f6484-161">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="f6484-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f6484-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="f6484-162">RELATED LINKS</span></span>

