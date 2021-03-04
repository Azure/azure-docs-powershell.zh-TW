---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/test-azkustoclusterprincipalassignmentnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
ms.openlocfilehash: f1c96909421dcc21d2b1f318a923ef7f9b804bf8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917705"
---
# <span data-ttu-id="cd35e-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span><span class="sxs-lookup"><span data-stu-id="cd35e-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span></span>

## <span data-ttu-id="cd35e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cd35e-102">SYNOPSIS</span></span>
<span data-ttu-id="cd35e-103">檢查主要工作分派名稱是否有效，且尚未使用中。</span><span class="sxs-lookup"><span data-stu-id="cd35e-103">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="cd35e-104">語法</span><span class="sxs-lookup"><span data-stu-id="cd35e-104">SYNTAX</span></span>

### <span data-ttu-id="cd35e-105">CheckExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="cd35e-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -ClusterName <String> -ResourceGroupName <String>
 -Name <String> -Type <Type> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="cd35e-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="cd35e-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -InputObject <IKustoIdentity> -Name <String>
 -Type <Type> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cd35e-107">描述</span><span class="sxs-lookup"><span data-stu-id="cd35e-107">DESCRIPTION</span></span>
<span data-ttu-id="cd35e-108">檢查主要工作分派名稱是否有效，且尚未使用中。</span><span class="sxs-lookup"><span data-stu-id="cd35e-108">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="cd35e-109">例子</span><span class="sxs-lookup"><span data-stu-id="cd35e-109">EXAMPLES</span></span>

### <span data-ttu-id="cd35e-110">範例 1：檢查使用中的組群主體指定名稱的可用性</span><span class="sxs-lookup"><span data-stu-id="cd35e-110">Example 1: Check the availability of a cluster principalassignment name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "myprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments" 

Message                                                                                                        Name            NameAvailable Reason
-------                                                                                                        ----            ------------- ------
PrincipalAssignment myprincipal already exists in cluster testnewkustocluster. Please select a different name. myprincipal   False
```

<span data-ttu-id="cd35e-111">上述命令會返回名為"myprincipal"的 PrincipalAssignment 是否存在於叢集"testnewkustocluster"中。</span><span class="sxs-lookup"><span data-stu-id="cd35e-111">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="cd35e-112">範例 2：檢查不使用的組群主體指定名稱的可用性</span><span class="sxs-lookup"><span data-stu-id="cd35e-112">Example 2: Check the availability of a cluster principalassignment name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "newprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments"

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="cd35e-113">上述命令會返回名為"newprincipal"的 PrincipalAssignment 是否存在於叢集"testnewkustocluster"中。</span><span class="sxs-lookup"><span data-stu-id="cd35e-113">The above command returns whether or not a PrincipalAssignment named "newprincipal" exists in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="cd35e-114">參數</span><span class="sxs-lookup"><span data-stu-id="cd35e-114">PARAMETERS</span></span>

### <span data-ttu-id="cd35e-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="cd35e-115">-ClusterName</span></span>
<span data-ttu-id="cd35e-116">Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="cd35e-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd35e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd35e-117">-DefaultProfile</span></span>
<span data-ttu-id="cd35e-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cd35e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd35e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd35e-119">-InputObject</span></span>
<span data-ttu-id="cd35e-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="cd35e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd35e-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="cd35e-121">-Name</span></span>
<span data-ttu-id="cd35e-122">主要工作分派資源名稱。</span><span class="sxs-lookup"><span data-stu-id="cd35e-122">Principal Assignment resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd35e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd35e-123">-ResourceGroupName</span></span>
<span data-ttu-id="cd35e-124">包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="cd35e-124">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd35e-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cd35e-125">-SubscriptionId</span></span>
<span data-ttu-id="cd35e-126">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="cd35e-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cd35e-127">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="cd35e-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd35e-128">-類型</span><span class="sxs-lookup"><span data-stu-id="cd35e-128">-Type</span></span>
<span data-ttu-id="cd35e-129">資源類型：Microsoft.Kusto/Clusters/principalAssignments。</span><span class="sxs-lookup"><span data-stu-id="cd35e-129">The type of resource, Microsoft.Kusto/Clusters/principalAssignments.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Type
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd35e-130">-確認</span><span class="sxs-lookup"><span data-stu-id="cd35e-130">-Confirm</span></span>
<span data-ttu-id="cd35e-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="cd35e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd35e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd35e-132">-WhatIf</span></span>
<span data-ttu-id="cd35e-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cd35e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd35e-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd35e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd35e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd35e-135">CommonParameters</span></span>
<span data-ttu-id="cd35e-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cd35e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd35e-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd35e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd35e-138">輸入</span><span class="sxs-lookup"><span data-stu-id="cd35e-138">INPUTS</span></span>

### <span data-ttu-id="cd35e-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="cd35e-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="cd35e-140">輸出</span><span class="sxs-lookup"><span data-stu-id="cd35e-140">OUTPUTS</span></span>

### <span data-ttu-id="cd35e-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.models.Api20200918.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="cd35e-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span></span>

## <span data-ttu-id="cd35e-142">筆記</span><span class="sxs-lookup"><span data-stu-id="cd35e-142">NOTES</span></span>

<span data-ttu-id="cd35e-143">別名</span><span class="sxs-lookup"><span data-stu-id="cd35e-143">ALIASES</span></span>

<span data-ttu-id="cd35e-144">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="cd35e-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cd35e-145">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="cd35e-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cd35e-146">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="cd35e-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cd35e-147">INPUTOBJECT： <IKustoIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="cd35e-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cd35e-148">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫組配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="cd35e-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="cd35e-149">`[ClusterName <String>]`：Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="cd35e-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="cd35e-150">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="cd35e-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="cd35e-151">`[DatabaseName <String>]`：Kusto cluster 中的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="cd35e-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="cd35e-152">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="cd35e-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cd35e-153">`[Location <String>]`：Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="cd35e-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="cd35e-154">`[PrincipalAssignmentName <String>]`：Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="cd35e-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="cd35e-155">`[ResourceGroupName <String>]`：包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="cd35e-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="cd35e-156">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="cd35e-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="cd35e-157">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="cd35e-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="cd35e-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="cd35e-158">RELATED LINKS</span></span>

