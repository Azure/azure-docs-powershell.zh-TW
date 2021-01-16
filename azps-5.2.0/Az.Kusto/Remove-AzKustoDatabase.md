---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabase.md
ms.openlocfilehash: cfb5eb3c65434f0f62af03bcca57174010041e58
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278907"
---
# <span data-ttu-id="d018a-101">Remove-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="d018a-101">Remove-AzKustoDatabase</span></span>

## <span data-ttu-id="d018a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d018a-102">SYNOPSIS</span></span>
<span data-ttu-id="d018a-103">刪除具有指定名稱的資料庫。</span><span class="sxs-lookup"><span data-stu-id="d018a-103">Deletes the database with the given name.</span></span>

## <span data-ttu-id="d018a-104">句法</span><span class="sxs-lookup"><span data-stu-id="d018a-104">SYNTAX</span></span>

### <span data-ttu-id="d018a-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="d018a-105">Delete (Default)</span></span>
```
Remove-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="d018a-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d018a-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDatabase -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d018a-107">說明</span><span class="sxs-lookup"><span data-stu-id="d018a-107">DESCRIPTION</span></span>
<span data-ttu-id="d018a-108">刪除具有指定名稱的資料庫。</span><span class="sxs-lookup"><span data-stu-id="d018a-108">Deletes the database with the given name.</span></span>

## <span data-ttu-id="d018a-109">示例</span><span class="sxs-lookup"><span data-stu-id="d018a-109">EXAMPLES</span></span>

### <span data-ttu-id="d018a-110">範例1：依名稱刪除現有的 Kusto 資料庫</span><span class="sxs-lookup"><span data-stu-id="d018a-110">Example 1: Delete an existing Kusto database by name</span></span>
```powershell
PS C:\> Remove-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase
```

<span data-ttu-id="d018a-111">上述命令會刪除在資源群組 "testrg" 中找到的群集 "testnewkustocluster" 中名為 "mykustodatabase" 的 Kusto 資料庫。</span><span class="sxs-lookup"><span data-stu-id="d018a-111">The above command deletes the Kusto database named "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="d018a-112">參數</span><span class="sxs-lookup"><span data-stu-id="d018a-112">PARAMETERS</span></span>

### <span data-ttu-id="d018a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d018a-113">-AsJob</span></span>
<span data-ttu-id="d018a-114">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="d018a-114">Run the command as a job</span></span>

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

### <span data-ttu-id="d018a-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d018a-115">-ClusterName</span></span>
<span data-ttu-id="d018a-116">Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="d018a-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="d018a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d018a-117">-DefaultProfile</span></span>
<span data-ttu-id="d018a-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d018a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d018a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d018a-119">-InputObject</span></span>
<span data-ttu-id="d018a-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="d018a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d018a-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="d018a-121">-Name</span></span>
<span data-ttu-id="d018a-122">Kusto 群集中之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="d018a-122">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="d018a-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d018a-123">-NoWait</span></span>
<span data-ttu-id="d018a-124">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="d018a-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d018a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d018a-125">-PassThru</span></span>
<span data-ttu-id="d018a-126">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="d018a-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d018a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d018a-127">-ResourceGroupName</span></span>
<span data-ttu-id="d018a-128">包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d018a-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="d018a-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d018a-129">-SubscriptionId</span></span>
<span data-ttu-id="d018a-130">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="d018a-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d018a-131">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="d018a-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d018a-132">-確認</span><span class="sxs-lookup"><span data-stu-id="d018a-132">-Confirm</span></span>
<span data-ttu-id="d018a-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d018a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d018a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d018a-134">-WhatIf</span></span>
<span data-ttu-id="d018a-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d018a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d018a-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d018a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d018a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d018a-137">CommonParameters</span></span>
<span data-ttu-id="d018a-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d018a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d018a-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d018a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d018a-140">輸入</span><span class="sxs-lookup"><span data-stu-id="d018a-140">INPUTS</span></span>

### <span data-ttu-id="d018a-141">IKustoIdentity （Kusto）的</span><span class="sxs-lookup"><span data-stu-id="d018a-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="d018a-142">輸出</span><span class="sxs-lookup"><span data-stu-id="d018a-142">OUTPUTS</span></span>

### <span data-ttu-id="d018a-143">System.object</span><span class="sxs-lookup"><span data-stu-id="d018a-143">System.Boolean</span></span>

## <span data-ttu-id="d018a-144">筆記</span><span class="sxs-lookup"><span data-stu-id="d018a-144">NOTES</span></span>

<span data-ttu-id="d018a-145">別名</span><span class="sxs-lookup"><span data-stu-id="d018a-145">ALIASES</span></span>

<span data-ttu-id="d018a-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="d018a-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d018a-147">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="d018a-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d018a-148">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="d018a-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d018a-149">INPUTOBJECT <IKustoIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="d018a-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d018a-150">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="d018a-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="d018a-151">`[ClusterName <String>]`： Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="d018a-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="d018a-152">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="d018a-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="d018a-153">`[DatabaseName <String>]`： Kusto 群集中之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="d018a-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="d018a-154">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="d018a-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d018a-155">`[Location <String>]`： Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="d018a-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="d018a-156">`[PrincipalAssignmentName <String>]`： Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="d018a-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="d018a-157">`[ResourceGroupName <String>]`：包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d018a-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="d018a-158">`[SubscriptionId <String>]`：取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="d018a-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d018a-159">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="d018a-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d018a-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="d018a-160">RELATED LINKS</span></span>

