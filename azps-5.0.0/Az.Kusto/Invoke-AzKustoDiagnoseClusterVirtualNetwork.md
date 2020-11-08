---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodiagnoseclustervirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDiagnoseClusterVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDiagnoseClusterVirtualNetwork.md
ms.openlocfilehash: 682de416a4aba61e1f287661c88faee9e20d248c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140445"
---
# <span data-ttu-id="d34ed-101">Invoke-AzKustoDiagnoseClusterVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d34ed-101">Invoke-AzKustoDiagnoseClusterVirtualNetwork</span></span>

## <span data-ttu-id="d34ed-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d34ed-102">SYNOPSIS</span></span>
<span data-ttu-id="d34ed-103">診斷服務所依賴之外部資源的網路線上狀態。</span><span class="sxs-lookup"><span data-stu-id="d34ed-103">Diagnoses network connectivity status for external resources on which the service is dependent on.</span></span>

## <span data-ttu-id="d34ed-104">句法</span><span class="sxs-lookup"><span data-stu-id="d34ed-104">SYNTAX</span></span>

### <span data-ttu-id="d34ed-105">診斷 (預設) </span><span class="sxs-lookup"><span data-stu-id="d34ed-105">Diagnose (Default)</span></span>
```
Invoke-AzKustoDiagnoseClusterVirtualNetwork -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="d34ed-106">DiagnoseViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d34ed-106">DiagnoseViaIdentity</span></span>
```
Invoke-AzKustoDiagnoseClusterVirtualNetwork -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d34ed-107">說明</span><span class="sxs-lookup"><span data-stu-id="d34ed-107">DESCRIPTION</span></span>
<span data-ttu-id="d34ed-108">診斷服務所依賴之外部資源的網路線上狀態。</span><span class="sxs-lookup"><span data-stu-id="d34ed-108">Diagnoses network connectivity status for external resources on which the service is dependent on.</span></span>

## <span data-ttu-id="d34ed-109">示例</span><span class="sxs-lookup"><span data-stu-id="d34ed-109">EXAMPLES</span></span>

### <span data-ttu-id="d34ed-110">範例1：顯示外部資源的網路連線性診斷</span><span class="sxs-lookup"><span data-stu-id="d34ed-110">Example 1: Show network connectivity diagnosis for external resources</span></span> 
```powershell
PS C:\> Invoke-AzKustoDiagnoseClusterVirtualNetwork -ResourceGroupName "testrg" -ClusterName "testnewkustocluster"

```

<span data-ttu-id="d34ed-111">上述命令會診斷群集 "testnewkustocluster" 所依賴之外部資源的網路線上狀態</span><span class="sxs-lookup"><span data-stu-id="d34ed-111">The above command diagnoses network connectivity status for external resources on which the cluster "testnewkustocluster" is dependent on</span></span>

## <span data-ttu-id="d34ed-112">參數</span><span class="sxs-lookup"><span data-stu-id="d34ed-112">PARAMETERS</span></span>

### <span data-ttu-id="d34ed-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d34ed-113">-AsJob</span></span>
<span data-ttu-id="d34ed-114">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="d34ed-114">Run the command as a job</span></span>

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

### <span data-ttu-id="d34ed-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d34ed-115">-ClusterName</span></span>
<span data-ttu-id="d34ed-116">Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="d34ed-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Diagnose
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d34ed-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d34ed-117">-DefaultProfile</span></span>
<span data-ttu-id="d34ed-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d34ed-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d34ed-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d34ed-119">-InputObject</span></span>
<span data-ttu-id="d34ed-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="d34ed-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DiagnoseViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d34ed-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d34ed-121">-NoWait</span></span>
<span data-ttu-id="d34ed-122">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="d34ed-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d34ed-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d34ed-123">-ResourceGroupName</span></span>
<span data-ttu-id="d34ed-124">包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d34ed-124">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Diagnose
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d34ed-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d34ed-125">-SubscriptionId</span></span>
<span data-ttu-id="d34ed-126">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="d34ed-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d34ed-127">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="d34ed-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Diagnose
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d34ed-128">-確認</span><span class="sxs-lookup"><span data-stu-id="d34ed-128">-Confirm</span></span>
<span data-ttu-id="d34ed-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d34ed-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d34ed-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d34ed-130">-WhatIf</span></span>
<span data-ttu-id="d34ed-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d34ed-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d34ed-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d34ed-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d34ed-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d34ed-133">CommonParameters</span></span>
<span data-ttu-id="d34ed-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d34ed-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d34ed-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d34ed-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d34ed-136">輸入</span><span class="sxs-lookup"><span data-stu-id="d34ed-136">INPUTS</span></span>

### <span data-ttu-id="d34ed-137">IKustoIdentity （Kusto）的</span><span class="sxs-lookup"><span data-stu-id="d34ed-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="d34ed-138">輸出</span><span class="sxs-lookup"><span data-stu-id="d34ed-138">OUTPUTS</span></span>

### <span data-ttu-id="d34ed-139">System.object</span><span class="sxs-lookup"><span data-stu-id="d34ed-139">System.String</span></span>

## <span data-ttu-id="d34ed-140">筆記</span><span class="sxs-lookup"><span data-stu-id="d34ed-140">NOTES</span></span>

<span data-ttu-id="d34ed-141">別名</span><span class="sxs-lookup"><span data-stu-id="d34ed-141">ALIASES</span></span>

<span data-ttu-id="d34ed-142">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="d34ed-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d34ed-143">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="d34ed-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d34ed-144">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="d34ed-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d34ed-145">INPUTOBJECT <IKustoIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="d34ed-145">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d34ed-146">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="d34ed-146">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="d34ed-147">`[ClusterName <String>]`： Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="d34ed-147">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="d34ed-148">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="d34ed-148">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="d34ed-149">`[DatabaseName <String>]`： Kusto 群集中之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="d34ed-149">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="d34ed-150">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="d34ed-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d34ed-151">`[Location <String>]`： Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="d34ed-151">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="d34ed-152">`[PrincipalAssignmentName <String>]`： Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="d34ed-152">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="d34ed-153">`[ResourceGroupName <String>]`：包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d34ed-153">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="d34ed-154">`[SubscriptionId <String>]`：取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="d34ed-154">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d34ed-155">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="d34ed-155">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d34ed-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="d34ed-156">RELATED LINKS</span></span>
