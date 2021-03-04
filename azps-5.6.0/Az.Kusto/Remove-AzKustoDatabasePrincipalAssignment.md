---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/remove-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 66a5a844255f5a44000638877abf6a3ed5f908c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903802"
---
# <span data-ttu-id="06112-101">Remove-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="06112-101">Remove-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="06112-102">簡介</span><span class="sxs-lookup"><span data-stu-id="06112-102">SYNOPSIS</span></span>
<span data-ttu-id="06112-103">刪除 Kusto 主體的Assignment。</span><span class="sxs-lookup"><span data-stu-id="06112-103">Deletes a Kusto principalAssignment.</span></span>

## <span data-ttu-id="06112-104">語法</span><span class="sxs-lookup"><span data-stu-id="06112-104">SYNTAX</span></span>

### <span data-ttu-id="06112-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="06112-105">Delete (Default)</span></span>
```
Remove-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="06112-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="06112-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDatabasePrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="06112-107">描述</span><span class="sxs-lookup"><span data-stu-id="06112-107">DESCRIPTION</span></span>
<span data-ttu-id="06112-108">刪除 Kusto 主體的Assignment。</span><span class="sxs-lookup"><span data-stu-id="06112-108">Deletes a Kusto principalAssignment.</span></span>

## <span data-ttu-id="06112-109">例子</span><span class="sxs-lookup"><span data-stu-id="06112-109">EXAMPLES</span></span>

### <span data-ttu-id="06112-110">範例 1：刪除現有的 Kusto 資料庫 PrincipalAssignment by name</span><span class="sxs-lookup"><span data-stu-id="06112-110">Example 1: Delete an existing Kusto database PrincipalAssignment by name</span></span>
```powershell
PS C:\> Remove-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1
```

<span data-ttu-id="06112-111">上述命令會刪除 Kusto 資料庫中名為 "kustoprincipal1" 的 PrincipalAssignment "mykustodatabase"。</span><span class="sxs-lookup"><span data-stu-id="06112-111">The above command deletes the PrincipalAssignment named "kustoprincipal1" in the Kusto database  "mykustodatabase".</span></span>

## <span data-ttu-id="06112-112">參數</span><span class="sxs-lookup"><span data-stu-id="06112-112">PARAMETERS</span></span>

### <span data-ttu-id="06112-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06112-113">-AsJob</span></span>
<span data-ttu-id="06112-114">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="06112-114">Run the command as a job</span></span>

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

### <span data-ttu-id="06112-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="06112-115">-ClusterName</span></span>
<span data-ttu-id="06112-116">Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="06112-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="06112-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="06112-117">-DatabaseName</span></span>
<span data-ttu-id="06112-118">Kusto cluster 中的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="06112-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="06112-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06112-119">-DefaultProfile</span></span>
<span data-ttu-id="06112-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="06112-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06112-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06112-121">-InputObject</span></span>
<span data-ttu-id="06112-122">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="06112-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="06112-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="06112-123">-NoWait</span></span>
<span data-ttu-id="06112-124">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="06112-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="06112-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06112-125">-PassThru</span></span>
<span data-ttu-id="06112-126">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="06112-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="06112-127">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="06112-127">-PrincipalAssignmentName</span></span>
<span data-ttu-id="06112-128">Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="06112-128">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="06112-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06112-129">-ResourceGroupName</span></span>
<span data-ttu-id="06112-130">包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="06112-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="06112-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="06112-131">-SubscriptionId</span></span>
<span data-ttu-id="06112-132">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="06112-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="06112-133">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="06112-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="06112-134">-確認</span><span class="sxs-lookup"><span data-stu-id="06112-134">-Confirm</span></span>
<span data-ttu-id="06112-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="06112-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06112-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06112-136">-WhatIf</span></span>
<span data-ttu-id="06112-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="06112-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06112-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="06112-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06112-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06112-139">CommonParameters</span></span>
<span data-ttu-id="06112-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="06112-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06112-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06112-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06112-142">輸入</span><span class="sxs-lookup"><span data-stu-id="06112-142">INPUTS</span></span>

### <span data-ttu-id="06112-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="06112-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="06112-144">輸出</span><span class="sxs-lookup"><span data-stu-id="06112-144">OUTPUTS</span></span>

### <span data-ttu-id="06112-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="06112-145">System.Boolean</span></span>

## <span data-ttu-id="06112-146">筆記</span><span class="sxs-lookup"><span data-stu-id="06112-146">NOTES</span></span>

<span data-ttu-id="06112-147">別名</span><span class="sxs-lookup"><span data-stu-id="06112-147">ALIASES</span></span>

<span data-ttu-id="06112-148">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="06112-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="06112-149">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="06112-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="06112-150">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="06112-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="06112-151">INPUTOBJECT： <IKustoIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="06112-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="06112-152">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫組配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="06112-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="06112-153">`[ClusterName <String>]`：Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="06112-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="06112-154">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="06112-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="06112-155">`[DatabaseName <String>]`：Kusto cluster 中的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="06112-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="06112-156">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="06112-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="06112-157">`[Location <String>]`：Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="06112-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="06112-158">`[PrincipalAssignmentName <String>]`：Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="06112-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="06112-159">`[ResourceGroupName <String>]`：包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="06112-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="06112-160">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="06112-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="06112-161">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="06112-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="06112-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="06112-162">RELATED LINKS</span></span>

