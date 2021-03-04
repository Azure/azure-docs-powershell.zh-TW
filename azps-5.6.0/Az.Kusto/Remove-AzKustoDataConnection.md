---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/remove-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDataConnection.md
ms.openlocfilehash: ac2eac129231f33a2f74732923652d3851debbd0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907630"
---
# <span data-ttu-id="18826-101">Remove-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="18826-101">Remove-AzKustoDataConnection</span></span>

## <span data-ttu-id="18826-102">簡介</span><span class="sxs-lookup"><span data-stu-id="18826-102">SYNOPSIS</span></span>
<span data-ttu-id="18826-103">刪除與指定名稱的資料連線。</span><span class="sxs-lookup"><span data-stu-id="18826-103">Deletes the data connection with the given name.</span></span>

## <span data-ttu-id="18826-104">語法</span><span class="sxs-lookup"><span data-stu-id="18826-104">SYNTAX</span></span>

### <span data-ttu-id="18826-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="18826-105">Delete (Default)</span></span>
```
Remove-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="18826-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="18826-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDataConnection -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="18826-107">描述</span><span class="sxs-lookup"><span data-stu-id="18826-107">DESCRIPTION</span></span>
<span data-ttu-id="18826-108">刪除與指定名稱的資料連線。</span><span class="sxs-lookup"><span data-stu-id="18826-108">Deletes the data connection with the given name.</span></span>

## <span data-ttu-id="18826-109">例子</span><span class="sxs-lookup"><span data-stu-id="18826-109">EXAMPLES</span></span>

### <span data-ttu-id="18826-110">範例 1：根據名稱刪除現有的資料連線</span><span class="sxs-lookup"><span data-stu-id="18826-110">Example 1: Delete an existing data connection by name</span></span>
```powershell
PS C:\> Remove-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "mykustodataconnection"
```

<span data-ttu-id="18826-111">上述命令會刪除資源群組 "testrg" 中現有叢集 "testnewkustocluster" 中名為 "mykustodataconnection" 之資料庫 "mykustodataconnection" 的資料連線</span><span class="sxs-lookup"><span data-stu-id="18826-111">The above command deletes the data connection named "mykustodataconnection" in database "mykustodatabase" of the existing cluster "testnewkustocluster" found in the resource group "testrg"</span></span>

## <span data-ttu-id="18826-112">參數</span><span class="sxs-lookup"><span data-stu-id="18826-112">PARAMETERS</span></span>

### <span data-ttu-id="18826-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="18826-113">-AsJob</span></span>
<span data-ttu-id="18826-114">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="18826-114">Run the command as a job</span></span>

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

### <span data-ttu-id="18826-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="18826-115">-ClusterName</span></span>
<span data-ttu-id="18826-116">Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="18826-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="18826-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="18826-117">-DatabaseName</span></span>
<span data-ttu-id="18826-118">Kusto cluster 中的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="18826-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="18826-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18826-119">-DefaultProfile</span></span>
<span data-ttu-id="18826-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="18826-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18826-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18826-121">-InputObject</span></span>
<span data-ttu-id="18826-122">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="18826-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="18826-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="18826-123">-Name</span></span>
<span data-ttu-id="18826-124">資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="18826-124">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18826-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="18826-125">-NoWait</span></span>
<span data-ttu-id="18826-126">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="18826-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="18826-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="18826-127">-PassThru</span></span>
<span data-ttu-id="18826-128">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="18826-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="18826-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18826-129">-ResourceGroupName</span></span>
<span data-ttu-id="18826-130">包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="18826-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="18826-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="18826-131">-SubscriptionId</span></span>
<span data-ttu-id="18826-132">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="18826-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="18826-133">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="18826-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="18826-134">-確認</span><span class="sxs-lookup"><span data-stu-id="18826-134">-Confirm</span></span>
<span data-ttu-id="18826-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="18826-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18826-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18826-136">-WhatIf</span></span>
<span data-ttu-id="18826-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="18826-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18826-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="18826-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18826-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18826-139">CommonParameters</span></span>
<span data-ttu-id="18826-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="18826-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18826-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="18826-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18826-142">輸入</span><span class="sxs-lookup"><span data-stu-id="18826-142">INPUTS</span></span>

### <span data-ttu-id="18826-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="18826-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="18826-144">輸出</span><span class="sxs-lookup"><span data-stu-id="18826-144">OUTPUTS</span></span>

### <span data-ttu-id="18826-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="18826-145">System.Boolean</span></span>

## <span data-ttu-id="18826-146">筆記</span><span class="sxs-lookup"><span data-stu-id="18826-146">NOTES</span></span>

<span data-ttu-id="18826-147">別名</span><span class="sxs-lookup"><span data-stu-id="18826-147">ALIASES</span></span>

<span data-ttu-id="18826-148">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="18826-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="18826-149">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="18826-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="18826-150">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="18826-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="18826-151">INPUTOBJECT： <IKustoIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="18826-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="18826-152">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫組配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="18826-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="18826-153">`[ClusterName <String>]`：Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="18826-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="18826-154">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="18826-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="18826-155">`[DatabaseName <String>]`：Kusto cluster 中的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="18826-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="18826-156">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="18826-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="18826-157">`[Location <String>]`：Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="18826-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="18826-158">`[PrincipalAssignmentName <String>]`：Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="18826-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="18826-159">`[ResourceGroupName <String>]`：包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="18826-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="18826-160">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="18826-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="18826-161">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="18826-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="18826-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="18826-162">RELATED LINKS</span></span>

