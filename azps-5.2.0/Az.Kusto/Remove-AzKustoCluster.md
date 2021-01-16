---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoCluster.md
ms.openlocfilehash: e9bdea3820b8b8121e0e250c99283c0ca656ca61
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98276555"
---
# <span data-ttu-id="9a9ac-101">Remove-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="9a9ac-101">Remove-AzKustoCluster</span></span>

## <span data-ttu-id="9a9ac-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9a9ac-102">SYNOPSIS</span></span>
<span data-ttu-id="9a9ac-103">刪除 Kusto 群集。</span><span class="sxs-lookup"><span data-stu-id="9a9ac-103">Deletes a Kusto cluster.</span></span>

## <span data-ttu-id="9a9ac-104">句法</span><span class="sxs-lookup"><span data-stu-id="9a9ac-104">SYNTAX</span></span>

### <span data-ttu-id="9a9ac-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="9a9ac-105">Delete (Default)</span></span>
```
Remove-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9a9ac-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9a9ac-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9a9ac-107">說明</span><span class="sxs-lookup"><span data-stu-id="9a9ac-107">DESCRIPTION</span></span>
<span data-ttu-id="9a9ac-108">刪除 Kusto 群集。</span><span class="sxs-lookup"><span data-stu-id="9a9ac-108">Deletes a Kusto cluster.</span></span>

## <span data-ttu-id="9a9ac-109">示例</span><span class="sxs-lookup"><span data-stu-id="9a9ac-109">EXAMPLES</span></span>

### <span data-ttu-id="9a9ac-110">範例1：依名稱刪除現有的 Kusto 群集</span><span class="sxs-lookup"><span data-stu-id="9a9ac-110">Example 1: Delete an existing Kusto cluster by name</span></span>
```powershell
PS C:\> Remove-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster
```

<span data-ttu-id="9a9ac-111">上述命令會刪除資源群組 "testrg" 中名為 "testnewkustocluster" 的 Kusto 群集。</span><span class="sxs-lookup"><span data-stu-id="9a9ac-111">The above command deletes the Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="9a9ac-112">參數</span><span class="sxs-lookup"><span data-stu-id="9a9ac-112">PARAMETERS</span></span>

### <span data-ttu-id="9a9ac-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a9ac-113">-AsJob</span></span>
<span data-ttu-id="9a9ac-114">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="9a9ac-114">Run the command as a job</span></span>

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

### <span data-ttu-id="9a9ac-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a9ac-115">-DefaultProfile</span></span>
<span data-ttu-id="9a9ac-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9a9ac-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a9ac-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a9ac-117">-InputObject</span></span>
<span data-ttu-id="9a9ac-118">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="9a9ac-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9a9ac-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="9a9ac-119">-Name</span></span>
<span data-ttu-id="9a9ac-120">Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="9a9ac-120">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a9ac-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9a9ac-121">-NoWait</span></span>
<span data-ttu-id="9a9ac-122">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="9a9ac-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9a9ac-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a9ac-123">-PassThru</span></span>
<span data-ttu-id="9a9ac-124">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="9a9ac-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9a9ac-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a9ac-125">-ResourceGroupName</span></span>
<span data-ttu-id="9a9ac-126">包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9a9ac-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="9a9ac-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9a9ac-127">-SubscriptionId</span></span>
<span data-ttu-id="9a9ac-128">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="9a9ac-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9a9ac-129">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="9a9ac-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9a9ac-130">-確認</span><span class="sxs-lookup"><span data-stu-id="9a9ac-130">-Confirm</span></span>
<span data-ttu-id="9a9ac-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9a9ac-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a9ac-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a9ac-132">-WhatIf</span></span>
<span data-ttu-id="9a9ac-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9a9ac-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a9ac-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9a9ac-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a9ac-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a9ac-135">CommonParameters</span></span>
<span data-ttu-id="9a9ac-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9a9ac-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a9ac-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9a9ac-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a9ac-138">輸入</span><span class="sxs-lookup"><span data-stu-id="9a9ac-138">INPUTS</span></span>

### <span data-ttu-id="9a9ac-139">IKustoIdentity （Kusto）的</span><span class="sxs-lookup"><span data-stu-id="9a9ac-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="9a9ac-140">輸出</span><span class="sxs-lookup"><span data-stu-id="9a9ac-140">OUTPUTS</span></span>

### <span data-ttu-id="9a9ac-141">System.object</span><span class="sxs-lookup"><span data-stu-id="9a9ac-141">System.Boolean</span></span>

## <span data-ttu-id="9a9ac-142">筆記</span><span class="sxs-lookup"><span data-stu-id="9a9ac-142">NOTES</span></span>

<span data-ttu-id="9a9ac-143">別名</span><span class="sxs-lookup"><span data-stu-id="9a9ac-143">ALIASES</span></span>

<span data-ttu-id="9a9ac-144">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="9a9ac-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9a9ac-145">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="9a9ac-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9a9ac-146">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="9a9ac-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9a9ac-147">INPUTOBJECT <IKustoIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="9a9ac-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9a9ac-148">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="9a9ac-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="9a9ac-149">`[ClusterName <String>]`： Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="9a9ac-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="9a9ac-150">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="9a9ac-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="9a9ac-151">`[DatabaseName <String>]`： Kusto 群集中之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="9a9ac-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="9a9ac-152">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="9a9ac-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9a9ac-153">`[Location <String>]`： Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="9a9ac-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="9a9ac-154">`[PrincipalAssignmentName <String>]`： Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="9a9ac-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="9a9ac-155">`[ResourceGroupName <String>]`：包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9a9ac-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="9a9ac-156">`[SubscriptionId <String>]`：取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="9a9ac-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9a9ac-157">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="9a9ac-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="9a9ac-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="9a9ac-158">RELATED LINKS</span></span>

