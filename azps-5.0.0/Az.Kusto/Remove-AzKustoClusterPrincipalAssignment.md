---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 92d6855753bdf56941d6f6ca85ec021228894a2d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140427"
---
# <span data-ttu-id="e7244-101">Remove-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="e7244-101">Remove-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="e7244-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e7244-102">SYNOPSIS</span></span>
<span data-ttu-id="e7244-103">刪除 Kusto 群集 principalAssignment。</span><span class="sxs-lookup"><span data-stu-id="e7244-103">Deletes a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="e7244-104">句法</span><span class="sxs-lookup"><span data-stu-id="e7244-104">SYNTAX</span></span>

### <span data-ttu-id="e7244-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="e7244-105">Delete (Default)</span></span>
```
Remove-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e7244-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e7244-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoClusterPrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e7244-107">說明</span><span class="sxs-lookup"><span data-stu-id="e7244-107">DESCRIPTION</span></span>
<span data-ttu-id="e7244-108">刪除 Kusto 群集 principalAssignment。</span><span class="sxs-lookup"><span data-stu-id="e7244-108">Deletes a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="e7244-109">示例</span><span class="sxs-lookup"><span data-stu-id="e7244-109">EXAMPLES</span></span>

### <span data-ttu-id="e7244-110">範例1：依名稱刪除現有的 Kusto 群集 PrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="e7244-110">Example 1: Delete an existing Kusto cluster PrincipalAssignment by name</span></span>
```powershell
PS C:\> Remove-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1
```

<span data-ttu-id="e7244-111">上述命令會刪除 Kusto 群集 "testnewkustocluster" 中名為 "kustoprincipal1" 的 PrincipalAssignment。</span><span class="sxs-lookup"><span data-stu-id="e7244-111">The above command deletes the PrincipalAssignment named "kustoprincipal1" in the Kusto cluster  "testnewkustocluster".</span></span>

## <span data-ttu-id="e7244-112">參數</span><span class="sxs-lookup"><span data-stu-id="e7244-112">PARAMETERS</span></span>

### <span data-ttu-id="e7244-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e7244-113">-AsJob</span></span>
<span data-ttu-id="e7244-114">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="e7244-114">Run the command as a job</span></span>

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

### <span data-ttu-id="e7244-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e7244-115">-ClusterName</span></span>
<span data-ttu-id="e7244-116">Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7244-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7244-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7244-117">-DefaultProfile</span></span>
<span data-ttu-id="e7244-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e7244-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7244-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7244-119">-InputObject</span></span>
<span data-ttu-id="e7244-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e7244-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7244-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e7244-121">-NoWait</span></span>
<span data-ttu-id="e7244-122">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="e7244-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e7244-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7244-123">-PassThru</span></span>
<span data-ttu-id="e7244-124">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="e7244-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e7244-125">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="e7244-125">-PrincipalAssignmentName</span></span>
<span data-ttu-id="e7244-126">Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7244-126">The name of the Kusto principalAssignment.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7244-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7244-127">-ResourceGroupName</span></span>
<span data-ttu-id="e7244-128">包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7244-128">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7244-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e7244-129">-SubscriptionId</span></span>
<span data-ttu-id="e7244-130">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="e7244-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e7244-131">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="e7244-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7244-132">-確認</span><span class="sxs-lookup"><span data-stu-id="e7244-132">-Confirm</span></span>
<span data-ttu-id="e7244-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e7244-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7244-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7244-134">-WhatIf</span></span>
<span data-ttu-id="e7244-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e7244-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7244-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e7244-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7244-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7244-137">CommonParameters</span></span>
<span data-ttu-id="e7244-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e7244-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7244-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e7244-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7244-140">輸入</span><span class="sxs-lookup"><span data-stu-id="e7244-140">INPUTS</span></span>

### <span data-ttu-id="e7244-141">IKustoIdentity （Kusto）的</span><span class="sxs-lookup"><span data-stu-id="e7244-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="e7244-142">輸出</span><span class="sxs-lookup"><span data-stu-id="e7244-142">OUTPUTS</span></span>

### <span data-ttu-id="e7244-143">System.object</span><span class="sxs-lookup"><span data-stu-id="e7244-143">System.Boolean</span></span>

## <span data-ttu-id="e7244-144">筆記</span><span class="sxs-lookup"><span data-stu-id="e7244-144">NOTES</span></span>

<span data-ttu-id="e7244-145">別名</span><span class="sxs-lookup"><span data-stu-id="e7244-145">ALIASES</span></span>

<span data-ttu-id="e7244-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="e7244-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e7244-147">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="e7244-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e7244-148">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="e7244-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e7244-149">INPUTOBJECT <IKustoIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="e7244-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e7244-150">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7244-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="e7244-151">`[ClusterName <String>]`： Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7244-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="e7244-152">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7244-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="e7244-153">`[DatabaseName <String>]`： Kusto 群集中之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7244-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="e7244-154">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="e7244-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e7244-155">`[Location <String>]`： Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="e7244-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="e7244-156">`[PrincipalAssignmentName <String>]`： Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7244-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="e7244-157">`[ResourceGroupName <String>]`：包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7244-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="e7244-158">`[SubscriptionId <String>]`：取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="e7244-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e7244-159">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="e7244-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e7244-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="e7244-160">RELATED LINKS</span></span>

