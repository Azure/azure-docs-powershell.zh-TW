---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: cd29af9ac8569683e6447a51f4d4f6784139f735
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98276603"
---
# <span data-ttu-id="ba0b9-101">Remove-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="ba0b9-101">Remove-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="ba0b9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ba0b9-102">SYNOPSIS</span></span>
<span data-ttu-id="ba0b9-103">刪除 Kusto principalAssignment。</span><span class="sxs-lookup"><span data-stu-id="ba0b9-103">Deletes a Kusto principalAssignment.</span></span>

## <span data-ttu-id="ba0b9-104">句法</span><span class="sxs-lookup"><span data-stu-id="ba0b9-104">SYNTAX</span></span>

### <span data-ttu-id="ba0b9-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="ba0b9-105">Delete (Default)</span></span>
```
Remove-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ba0b9-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ba0b9-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDatabasePrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ba0b9-107">說明</span><span class="sxs-lookup"><span data-stu-id="ba0b9-107">DESCRIPTION</span></span>
<span data-ttu-id="ba0b9-108">刪除 Kusto principalAssignment。</span><span class="sxs-lookup"><span data-stu-id="ba0b9-108">Deletes a Kusto principalAssignment.</span></span>

## <span data-ttu-id="ba0b9-109">示例</span><span class="sxs-lookup"><span data-stu-id="ba0b9-109">EXAMPLES</span></span>

### <span data-ttu-id="ba0b9-110">範例1：依名稱刪除現有的 Kusto 資料庫 PrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="ba0b9-110">Example 1: Delete an existing Kusto database PrincipalAssignment by name</span></span>
```powershell
PS C:\> Remove-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1
```

<span data-ttu-id="ba0b9-111">上述命令會刪除 Kusto 資料庫 "mykustodatabase" 中名為 "kustoprincipal1" 的 PrincipalAssignment。</span><span class="sxs-lookup"><span data-stu-id="ba0b9-111">The above command deletes the PrincipalAssignment named "kustoprincipal1" in the Kusto database  "mykustodatabase".</span></span>

## <span data-ttu-id="ba0b9-112">參數</span><span class="sxs-lookup"><span data-stu-id="ba0b9-112">PARAMETERS</span></span>

### <span data-ttu-id="ba0b9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ba0b9-113">-AsJob</span></span>
<span data-ttu-id="ba0b9-114">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="ba0b9-114">Run the command as a job</span></span>

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

### <span data-ttu-id="ba0b9-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ba0b9-115">-ClusterName</span></span>
<span data-ttu-id="ba0b9-116">Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="ba0b9-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="ba0b9-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ba0b9-117">-DatabaseName</span></span>
<span data-ttu-id="ba0b9-118">Kusto 群集中之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="ba0b9-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="ba0b9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba0b9-119">-DefaultProfile</span></span>
<span data-ttu-id="ba0b9-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ba0b9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba0b9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba0b9-121">-InputObject</span></span>
<span data-ttu-id="ba0b9-122">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="ba0b9-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ba0b9-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ba0b9-123">-NoWait</span></span>
<span data-ttu-id="ba0b9-124">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="ba0b9-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ba0b9-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ba0b9-125">-PassThru</span></span>
<span data-ttu-id="ba0b9-126">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="ba0b9-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ba0b9-127">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="ba0b9-127">-PrincipalAssignmentName</span></span>
<span data-ttu-id="ba0b9-128">Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="ba0b9-128">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="ba0b9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba0b9-129">-ResourceGroupName</span></span>
<span data-ttu-id="ba0b9-130">包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ba0b9-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="ba0b9-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ba0b9-131">-SubscriptionId</span></span>
<span data-ttu-id="ba0b9-132">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="ba0b9-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ba0b9-133">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="ba0b9-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ba0b9-134">-確認</span><span class="sxs-lookup"><span data-stu-id="ba0b9-134">-Confirm</span></span>
<span data-ttu-id="ba0b9-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ba0b9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba0b9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba0b9-136">-WhatIf</span></span>
<span data-ttu-id="ba0b9-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ba0b9-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba0b9-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ba0b9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba0b9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba0b9-139">CommonParameters</span></span>
<span data-ttu-id="ba0b9-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ba0b9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba0b9-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ba0b9-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba0b9-142">輸入</span><span class="sxs-lookup"><span data-stu-id="ba0b9-142">INPUTS</span></span>

### <span data-ttu-id="ba0b9-143">IKustoIdentity （Kusto）的</span><span class="sxs-lookup"><span data-stu-id="ba0b9-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="ba0b9-144">輸出</span><span class="sxs-lookup"><span data-stu-id="ba0b9-144">OUTPUTS</span></span>

### <span data-ttu-id="ba0b9-145">System.object</span><span class="sxs-lookup"><span data-stu-id="ba0b9-145">System.Boolean</span></span>

## <span data-ttu-id="ba0b9-146">筆記</span><span class="sxs-lookup"><span data-stu-id="ba0b9-146">NOTES</span></span>

<span data-ttu-id="ba0b9-147">別名</span><span class="sxs-lookup"><span data-stu-id="ba0b9-147">ALIASES</span></span>

<span data-ttu-id="ba0b9-148">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="ba0b9-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ba0b9-149">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="ba0b9-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ba0b9-150">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="ba0b9-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ba0b9-151">INPUTOBJECT <IKustoIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="ba0b9-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ba0b9-152">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="ba0b9-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="ba0b9-153">`[ClusterName <String>]`： Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="ba0b9-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="ba0b9-154">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="ba0b9-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="ba0b9-155">`[DatabaseName <String>]`： Kusto 群集中之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="ba0b9-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="ba0b9-156">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="ba0b9-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ba0b9-157">`[Location <String>]`： Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="ba0b9-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="ba0b9-158">`[PrincipalAssignmentName <String>]`： Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="ba0b9-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="ba0b9-159">`[ResourceGroupName <String>]`：包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ba0b9-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="ba0b9-160">`[SubscriptionId <String>]`：取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="ba0b9-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ba0b9-161">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="ba0b9-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ba0b9-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="ba0b9-162">RELATED LINKS</span></span>

