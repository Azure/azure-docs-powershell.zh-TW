---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/invoke-azkustodiagnoseclustervirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDiagnoseClusterVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDiagnoseClusterVirtualNetwork.md
ms.openlocfilehash: d2530404774c3cb735dedb6eb233979fe602fe4d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916934"
---
# <span data-ttu-id="2beaf-101">Invoke-AzKustoDiagnoseClusterVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2beaf-101">Invoke-AzKustoDiagnoseClusterVirtualNetwork</span></span>

## <span data-ttu-id="2beaf-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2beaf-102">SYNOPSIS</span></span>
<span data-ttu-id="2beaf-103">診斷服務所依存之外部資源的網路連接狀態。</span><span class="sxs-lookup"><span data-stu-id="2beaf-103">Diagnoses network connectivity status for external resources on which the service is dependent on.</span></span>

## <span data-ttu-id="2beaf-104">語法</span><span class="sxs-lookup"><span data-stu-id="2beaf-104">SYNTAX</span></span>

### <span data-ttu-id="2beaf-105">診斷 (預設) </span><span class="sxs-lookup"><span data-stu-id="2beaf-105">Diagnose (Default)</span></span>
```
Invoke-AzKustoDiagnoseClusterVirtualNetwork -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="2beaf-106">診斷ViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2beaf-106">DiagnoseViaIdentity</span></span>
```
Invoke-AzKustoDiagnoseClusterVirtualNetwork -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2beaf-107">描述</span><span class="sxs-lookup"><span data-stu-id="2beaf-107">DESCRIPTION</span></span>
<span data-ttu-id="2beaf-108">診斷服務所依存之外部資源的網路連接狀態。</span><span class="sxs-lookup"><span data-stu-id="2beaf-108">Diagnoses network connectivity status for external resources on which the service is dependent on.</span></span>

## <span data-ttu-id="2beaf-109">例子</span><span class="sxs-lookup"><span data-stu-id="2beaf-109">EXAMPLES</span></span>

### <span data-ttu-id="2beaf-110">範例 1：顯示外部資源的網路連接診斷</span><span class="sxs-lookup"><span data-stu-id="2beaf-110">Example 1: Show network connectivity diagnosis for external resources</span></span> 
```powershell
PS C:\> Invoke-AzKustoDiagnoseClusterVirtualNetwork -ResourceGroupName "testrg" -ClusterName "testnewkustocluster"

```

<span data-ttu-id="2beaf-111">上述命令可診斷叢集「testnewkustocluster」所依存之外部資源的網路連接狀態</span><span class="sxs-lookup"><span data-stu-id="2beaf-111">The above command diagnoses network connectivity status for external resources on which the cluster "testnewkustocluster" is dependent on</span></span>

## <span data-ttu-id="2beaf-112">參數</span><span class="sxs-lookup"><span data-stu-id="2beaf-112">PARAMETERS</span></span>

### <span data-ttu-id="2beaf-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2beaf-113">-AsJob</span></span>
<span data-ttu-id="2beaf-114">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="2beaf-114">Run the command as a job</span></span>

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

### <span data-ttu-id="2beaf-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2beaf-115">-ClusterName</span></span>
<span data-ttu-id="2beaf-116">Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="2beaf-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="2beaf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2beaf-117">-DefaultProfile</span></span>
<span data-ttu-id="2beaf-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2beaf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2beaf-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2beaf-119">-InputObject</span></span>
<span data-ttu-id="2beaf-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="2beaf-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2beaf-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2beaf-121">-NoWait</span></span>
<span data-ttu-id="2beaf-122">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="2beaf-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2beaf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2beaf-123">-ResourceGroupName</span></span>
<span data-ttu-id="2beaf-124">包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="2beaf-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="2beaf-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2beaf-125">-SubscriptionId</span></span>
<span data-ttu-id="2beaf-126">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="2beaf-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2beaf-127">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="2beaf-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2beaf-128">-確認</span><span class="sxs-lookup"><span data-stu-id="2beaf-128">-Confirm</span></span>
<span data-ttu-id="2beaf-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2beaf-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2beaf-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2beaf-130">-WhatIf</span></span>
<span data-ttu-id="2beaf-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2beaf-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2beaf-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2beaf-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2beaf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2beaf-133">CommonParameters</span></span>
<span data-ttu-id="2beaf-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2beaf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2beaf-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2beaf-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2beaf-136">輸入</span><span class="sxs-lookup"><span data-stu-id="2beaf-136">INPUTS</span></span>

### <span data-ttu-id="2beaf-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="2beaf-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="2beaf-138">輸出</span><span class="sxs-lookup"><span data-stu-id="2beaf-138">OUTPUTS</span></span>

### <span data-ttu-id="2beaf-139">System.String</span><span class="sxs-lookup"><span data-stu-id="2beaf-139">System.String</span></span>

## <span data-ttu-id="2beaf-140">筆記</span><span class="sxs-lookup"><span data-stu-id="2beaf-140">NOTES</span></span>

<span data-ttu-id="2beaf-141">別名</span><span class="sxs-lookup"><span data-stu-id="2beaf-141">ALIASES</span></span>

<span data-ttu-id="2beaf-142">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="2beaf-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2beaf-143">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="2beaf-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2beaf-144">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="2beaf-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2beaf-145">INPUTOBJECT： <IKustoIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="2beaf-145">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2beaf-146">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫組配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="2beaf-146">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="2beaf-147">`[ClusterName <String>]`：Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="2beaf-147">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="2beaf-148">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="2beaf-148">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="2beaf-149">`[DatabaseName <String>]`：Kusto cluster 中的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="2beaf-149">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="2beaf-150">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="2beaf-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2beaf-151">`[Location <String>]`：Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="2beaf-151">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="2beaf-152">`[PrincipalAssignmentName <String>]`：Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="2beaf-152">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="2beaf-153">`[ResourceGroupName <String>]`：包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="2beaf-153">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="2beaf-154">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="2beaf-154">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2beaf-155">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="2beaf-155">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="2beaf-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="2beaf-156">RELATED LINKS</span></span>

