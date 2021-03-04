---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/remove-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabase.md
ms.openlocfilehash: ab6ef84d05e77711a767f35f915d53c2fe5cdb46
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907866"
---
# <span data-ttu-id="e19b5-101">Remove-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="e19b5-101">Remove-AzKustoDatabase</span></span>

## <span data-ttu-id="e19b5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e19b5-102">SYNOPSIS</span></span>
<span data-ttu-id="e19b5-103">刪除具有指定名稱的資料庫。</span><span class="sxs-lookup"><span data-stu-id="e19b5-103">Deletes the database with the given name.</span></span>

## <span data-ttu-id="e19b5-104">語法</span><span class="sxs-lookup"><span data-stu-id="e19b5-104">SYNTAX</span></span>

### <span data-ttu-id="e19b5-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="e19b5-105">Delete (Default)</span></span>
```
Remove-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="e19b5-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e19b5-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDatabase -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e19b5-107">描述</span><span class="sxs-lookup"><span data-stu-id="e19b5-107">DESCRIPTION</span></span>
<span data-ttu-id="e19b5-108">刪除具有指定名稱的資料庫。</span><span class="sxs-lookup"><span data-stu-id="e19b5-108">Deletes the database with the given name.</span></span>

## <span data-ttu-id="e19b5-109">例子</span><span class="sxs-lookup"><span data-stu-id="e19b5-109">EXAMPLES</span></span>

### <span data-ttu-id="e19b5-110">範例 1：根據名稱刪除現有的 Kusto 資料庫</span><span class="sxs-lookup"><span data-stu-id="e19b5-110">Example 1: Delete an existing Kusto database by name</span></span>
```powershell
PS C:\> Remove-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase
```

<span data-ttu-id="e19b5-111">上述命令會刪除資源群組 "testrg" 中"testnewkustocluster"中名為 "mykustodatabase" 的 Kusto 資料庫。</span><span class="sxs-lookup"><span data-stu-id="e19b5-111">The above command deletes the Kusto database named "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="e19b5-112">參數</span><span class="sxs-lookup"><span data-stu-id="e19b5-112">PARAMETERS</span></span>

### <span data-ttu-id="e19b5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e19b5-113">-AsJob</span></span>
<span data-ttu-id="e19b5-114">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="e19b5-114">Run the command as a job</span></span>

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

### <span data-ttu-id="e19b5-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e19b5-115">-ClusterName</span></span>
<span data-ttu-id="e19b5-116">Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="e19b5-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="e19b5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e19b5-117">-DefaultProfile</span></span>
<span data-ttu-id="e19b5-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e19b5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e19b5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e19b5-119">-InputObject</span></span>
<span data-ttu-id="e19b5-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e19b5-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e19b5-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="e19b5-121">-Name</span></span>
<span data-ttu-id="e19b5-122">Kusto cluster 中的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="e19b5-122">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e19b5-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e19b5-123">-NoWait</span></span>
<span data-ttu-id="e19b5-124">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="e19b5-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e19b5-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e19b5-125">-PassThru</span></span>
<span data-ttu-id="e19b5-126">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="e19b5-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e19b5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e19b5-127">-ResourceGroupName</span></span>
<span data-ttu-id="e19b5-128">包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="e19b5-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="e19b5-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e19b5-129">-SubscriptionId</span></span>
<span data-ttu-id="e19b5-130">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="e19b5-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e19b5-131">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="e19b5-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e19b5-132">-確認</span><span class="sxs-lookup"><span data-stu-id="e19b5-132">-Confirm</span></span>
<span data-ttu-id="e19b5-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e19b5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e19b5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e19b5-134">-WhatIf</span></span>
<span data-ttu-id="e19b5-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e19b5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e19b5-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e19b5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e19b5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e19b5-137">CommonParameters</span></span>
<span data-ttu-id="e19b5-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e19b5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e19b5-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e19b5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e19b5-140">輸入</span><span class="sxs-lookup"><span data-stu-id="e19b5-140">INPUTS</span></span>

### <span data-ttu-id="e19b5-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="e19b5-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="e19b5-142">輸出</span><span class="sxs-lookup"><span data-stu-id="e19b5-142">OUTPUTS</span></span>

### <span data-ttu-id="e19b5-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e19b5-143">System.Boolean</span></span>

## <span data-ttu-id="e19b5-144">筆記</span><span class="sxs-lookup"><span data-stu-id="e19b5-144">NOTES</span></span>

<span data-ttu-id="e19b5-145">別名</span><span class="sxs-lookup"><span data-stu-id="e19b5-145">ALIASES</span></span>

<span data-ttu-id="e19b5-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="e19b5-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e19b5-147">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e19b5-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e19b5-148">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="e19b5-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e19b5-149">INPUTOBJECT： <IKustoIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="e19b5-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e19b5-150">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫組配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="e19b5-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="e19b5-151">`[ClusterName <String>]`：Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="e19b5-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="e19b5-152">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="e19b5-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="e19b5-153">`[DatabaseName <String>]`：Kusto cluster 中的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="e19b5-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="e19b5-154">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="e19b5-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e19b5-155">`[Location <String>]`：Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="e19b5-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="e19b5-156">`[PrincipalAssignmentName <String>]`：Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e19b5-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="e19b5-157">`[ResourceGroupName <String>]`：包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="e19b5-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="e19b5-158">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="e19b5-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e19b5-159">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="e19b5-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e19b5-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="e19b5-160">RELATED LINKS</span></span>

