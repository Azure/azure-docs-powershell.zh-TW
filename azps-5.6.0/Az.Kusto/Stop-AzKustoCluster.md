---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/stop-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Stop-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Stop-AzKustoCluster.md
ms.openlocfilehash: 4f03c3fd8e36e8122a8ada001efa97475922dc91
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916407"
---
# <span data-ttu-id="4a221-101">Stop-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="4a221-101">Stop-AzKustoCluster</span></span>

## <span data-ttu-id="4a221-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4a221-102">SYNOPSIS</span></span>
<span data-ttu-id="4a221-103">停止 Kusto 集區。</span><span class="sxs-lookup"><span data-stu-id="4a221-103">Stops a Kusto cluster.</span></span>

## <span data-ttu-id="4a221-104">語法</span><span class="sxs-lookup"><span data-stu-id="4a221-104">SYNTAX</span></span>

### <span data-ttu-id="4a221-105">停止 (預設) </span><span class="sxs-lookup"><span data-stu-id="4a221-105">Stop (Default)</span></span>
```
Stop-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4a221-106">StopViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4a221-106">StopViaIdentity</span></span>
```
Stop-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4a221-107">描述</span><span class="sxs-lookup"><span data-stu-id="4a221-107">DESCRIPTION</span></span>
<span data-ttu-id="4a221-108">停止 Kusto 集區。</span><span class="sxs-lookup"><span data-stu-id="4a221-108">Stops a Kusto cluster.</span></span>

## <span data-ttu-id="4a221-109">例子</span><span class="sxs-lookup"><span data-stu-id="4a221-109">EXAMPLES</span></span>

### <span data-ttu-id="4a221-110">範例 1：停止 Kusto cluster</span><span class="sxs-lookup"><span data-stu-id="4a221-110">Example 1: Stop a Kusto cluster</span></span>
```powershell
PS C:\> Stop-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster
```

<span data-ttu-id="4a221-111">上述命令會停止 Kusto 集區</span><span class="sxs-lookup"><span data-stu-id="4a221-111">The above command stops a Kusto cluster</span></span>

## <span data-ttu-id="4a221-112">參數</span><span class="sxs-lookup"><span data-stu-id="4a221-112">PARAMETERS</span></span>

### <span data-ttu-id="4a221-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a221-113">-AsJob</span></span>
<span data-ttu-id="4a221-114">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="4a221-114">Run the command as a job</span></span>

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

### <span data-ttu-id="4a221-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a221-115">-DefaultProfile</span></span>
<span data-ttu-id="4a221-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4a221-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a221-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a221-117">-InputObject</span></span>
<span data-ttu-id="4a221-118">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="4a221-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: StopViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a221-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="4a221-119">-Name</span></span>
<span data-ttu-id="4a221-120">Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="4a221-120">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a221-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4a221-121">-NoWait</span></span>
<span data-ttu-id="4a221-122">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="4a221-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4a221-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4a221-123">-PassThru</span></span>
<span data-ttu-id="4a221-124">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="4a221-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4a221-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a221-125">-ResourceGroupName</span></span>
<span data-ttu-id="4a221-126">包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="4a221-126">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a221-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4a221-127">-SubscriptionId</span></span>
<span data-ttu-id="4a221-128">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="4a221-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4a221-129">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="4a221-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a221-130">-確認</span><span class="sxs-lookup"><span data-stu-id="4a221-130">-Confirm</span></span>
<span data-ttu-id="4a221-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4a221-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a221-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a221-132">-WhatIf</span></span>
<span data-ttu-id="4a221-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4a221-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a221-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4a221-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a221-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a221-135">CommonParameters</span></span>
<span data-ttu-id="4a221-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4a221-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a221-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4a221-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a221-138">輸入</span><span class="sxs-lookup"><span data-stu-id="4a221-138">INPUTS</span></span>

### <span data-ttu-id="4a221-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="4a221-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="4a221-140">輸出</span><span class="sxs-lookup"><span data-stu-id="4a221-140">OUTPUTS</span></span>

### <span data-ttu-id="4a221-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4a221-141">System.Boolean</span></span>

## <span data-ttu-id="4a221-142">筆記</span><span class="sxs-lookup"><span data-stu-id="4a221-142">NOTES</span></span>

<span data-ttu-id="4a221-143">別名</span><span class="sxs-lookup"><span data-stu-id="4a221-143">ALIASES</span></span>

<span data-ttu-id="4a221-144">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="4a221-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4a221-145">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="4a221-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4a221-146">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="4a221-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4a221-147">INPUTOBJECT： <IKustoIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="4a221-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4a221-148">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫組配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="4a221-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="4a221-149">`[ClusterName <String>]`：Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="4a221-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="4a221-150">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="4a221-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="4a221-151">`[DatabaseName <String>]`：Kusto cluster 中的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="4a221-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="4a221-152">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="4a221-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4a221-153">`[Location <String>]`：Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="4a221-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="4a221-154">`[PrincipalAssignmentName <String>]`：Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="4a221-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="4a221-155">`[ResourceGroupName <String>]`：包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="4a221-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="4a221-156">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="4a221-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="4a221-157">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="4a221-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="4a221-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="4a221-158">RELATED LINKS</span></span>

