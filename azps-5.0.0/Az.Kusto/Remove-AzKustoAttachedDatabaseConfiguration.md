---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: 9d38b9c3297dc950cc12d46189bc940e27877d8a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140435"
---
# <span data-ttu-id="7a5cb-101">Remove-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="7a5cb-101">Remove-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="7a5cb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7a5cb-102">SYNOPSIS</span></span>
<span data-ttu-id="7a5cb-103">刪除具有指定名稱的已附加資料庫設定。</span><span class="sxs-lookup"><span data-stu-id="7a5cb-103">Deletes the attached database configuration with the given name.</span></span>

## <span data-ttu-id="7a5cb-104">句法</span><span class="sxs-lookup"><span data-stu-id="7a5cb-104">SYNTAX</span></span>

### <span data-ttu-id="7a5cb-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="7a5cb-105">Delete (Default)</span></span>
```
Remove-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="7a5cb-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7a5cb-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoAttachedDatabaseConfiguration -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7a5cb-107">說明</span><span class="sxs-lookup"><span data-stu-id="7a5cb-107">DESCRIPTION</span></span>
<span data-ttu-id="7a5cb-108">刪除具有指定名稱的已附加資料庫設定。</span><span class="sxs-lookup"><span data-stu-id="7a5cb-108">Deletes the attached database configuration with the given name.</span></span>

## <span data-ttu-id="7a5cb-109">示例</span><span class="sxs-lookup"><span data-stu-id="7a5cb-109">EXAMPLES</span></span>

### <span data-ttu-id="7a5cb-110">範例1：依名稱刪除現有的 AttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="7a5cb-110">Example 1: Delete an existing AttachedDatabaseConfiguration by name</span></span>
```powershell
PS C:\> Remove-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration"
```

<span data-ttu-id="7a5cb-111">上述命令會從 [群集] testnewkustoclusterf "刪除 AttachedDatabaseConfiguration" myfollowerconfiguration "中定義的從動資料庫。</span><span class="sxs-lookup"><span data-stu-id="7a5cb-111">The above command deletes the follower database defined in the AttachedDatabaseConfiguration "myfollowerconfiguration" from cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="7a5cb-112">參數</span><span class="sxs-lookup"><span data-stu-id="7a5cb-112">PARAMETERS</span></span>

### <span data-ttu-id="7a5cb-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a5cb-113">-AsJob</span></span>
<span data-ttu-id="7a5cb-114">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="7a5cb-114">Run the command as a job</span></span>

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

### <span data-ttu-id="7a5cb-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="7a5cb-115">-ClusterName</span></span>
<span data-ttu-id="7a5cb-116">Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="7a5cb-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="7a5cb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a5cb-117">-DefaultProfile</span></span>
<span data-ttu-id="7a5cb-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7a5cb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a5cb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a5cb-119">-InputObject</span></span>
<span data-ttu-id="7a5cb-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="7a5cb-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7a5cb-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="7a5cb-121">-Name</span></span>
<span data-ttu-id="7a5cb-122">已附加資料庫配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="7a5cb-122">The name of the attached database configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AttachedDatabaseConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a5cb-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7a5cb-123">-NoWait</span></span>
<span data-ttu-id="7a5cb-124">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="7a5cb-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7a5cb-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a5cb-125">-PassThru</span></span>
<span data-ttu-id="7a5cb-126">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="7a5cb-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7a5cb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a5cb-127">-ResourceGroupName</span></span>
<span data-ttu-id="7a5cb-128">包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7a5cb-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="7a5cb-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7a5cb-129">-SubscriptionId</span></span>
<span data-ttu-id="7a5cb-130">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="7a5cb-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7a5cb-131">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="7a5cb-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7a5cb-132">-確認</span><span class="sxs-lookup"><span data-stu-id="7a5cb-132">-Confirm</span></span>
<span data-ttu-id="7a5cb-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7a5cb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a5cb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a5cb-134">-WhatIf</span></span>
<span data-ttu-id="7a5cb-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7a5cb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a5cb-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7a5cb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a5cb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a5cb-137">CommonParameters</span></span>
<span data-ttu-id="7a5cb-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7a5cb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a5cb-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7a5cb-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a5cb-140">輸入</span><span class="sxs-lookup"><span data-stu-id="7a5cb-140">INPUTS</span></span>

### <span data-ttu-id="7a5cb-141">IKustoIdentity （Kusto）的</span><span class="sxs-lookup"><span data-stu-id="7a5cb-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="7a5cb-142">輸出</span><span class="sxs-lookup"><span data-stu-id="7a5cb-142">OUTPUTS</span></span>

### <span data-ttu-id="7a5cb-143">System.object</span><span class="sxs-lookup"><span data-stu-id="7a5cb-143">System.Boolean</span></span>

## <span data-ttu-id="7a5cb-144">筆記</span><span class="sxs-lookup"><span data-stu-id="7a5cb-144">NOTES</span></span>

<span data-ttu-id="7a5cb-145">別名</span><span class="sxs-lookup"><span data-stu-id="7a5cb-145">ALIASES</span></span>

<span data-ttu-id="7a5cb-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="7a5cb-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7a5cb-147">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="7a5cb-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7a5cb-148">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="7a5cb-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7a5cb-149">INPUTOBJECT <IKustoIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="7a5cb-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7a5cb-150">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="7a5cb-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="7a5cb-151">`[ClusterName <String>]`： Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="7a5cb-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="7a5cb-152">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="7a5cb-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="7a5cb-153">`[DatabaseName <String>]`： Kusto 群集中之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="7a5cb-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="7a5cb-154">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="7a5cb-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7a5cb-155">`[Location <String>]`： Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="7a5cb-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="7a5cb-156">`[PrincipalAssignmentName <String>]`： Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="7a5cb-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="7a5cb-157">`[ResourceGroupName <String>]`：包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7a5cb-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="7a5cb-158">`[SubscriptionId <String>]`：取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="7a5cb-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="7a5cb-159">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="7a5cb-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="7a5cb-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="7a5cb-160">RELATED LINKS</span></span>

