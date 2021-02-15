---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclusterprincipalassignmentnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
ms.openlocfilehash: 0fbffb0effff782c154e4b6c38d6eb296b89ffb9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100129230"
---
# <span data-ttu-id="0d838-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span><span class="sxs-lookup"><span data-stu-id="0d838-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span></span>

## <span data-ttu-id="0d838-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0d838-102">SYNOPSIS</span></span>
<span data-ttu-id="0d838-103">檢查原則指派名稱是否有效，且尚未使用中。</span><span class="sxs-lookup"><span data-stu-id="0d838-103">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="0d838-104">句法</span><span class="sxs-lookup"><span data-stu-id="0d838-104">SYNTAX</span></span>

### <span data-ttu-id="0d838-105">CheckExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="0d838-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -ClusterName <String> -ResourceGroupName <String>
 -Name <String> -Type <Type> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="0d838-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="0d838-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -InputObject <IKustoIdentity> -Name <String>
 -Type <Type> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0d838-107">說明</span><span class="sxs-lookup"><span data-stu-id="0d838-107">DESCRIPTION</span></span>
<span data-ttu-id="0d838-108">檢查原則指派名稱是否有效，且尚未使用中。</span><span class="sxs-lookup"><span data-stu-id="0d838-108">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="0d838-109">示例</span><span class="sxs-lookup"><span data-stu-id="0d838-109">EXAMPLES</span></span>

### <span data-ttu-id="0d838-110">範例1：檢查使用中的群集 principalassignment 名稱是否有空？</span><span class="sxs-lookup"><span data-stu-id="0d838-110">Example 1: Check the availability of a cluster principalassignment name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "myprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments" 

Message                                                                                                        Name            NameAvailable Reason
-------                                                                                                        ----            ------------- ------
PrincipalAssignment myprincipal already exists in cluster testnewkustocluster. Please select a different name. myprincipal   False
```

<span data-ttu-id="0d838-111">上述命令會傳回群集 "testnewkustocluster" 中是否存在名為 "myprincipal" 的 PrincipalAssignment。</span><span class="sxs-lookup"><span data-stu-id="0d838-111">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="0d838-112">範例2：檢查未使用的群集 principalassignment 名稱的可用性</span><span class="sxs-lookup"><span data-stu-id="0d838-112">Example 2: Check the availability of a cluster principalassignment name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "newprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments"

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="0d838-113">上述命令會傳回群集 "testnewkustocluster" 中是否存在名為 "newprincipal" 的 PrincipalAssignment。</span><span class="sxs-lookup"><span data-stu-id="0d838-113">The above command returns whether or not a PrincipalAssignment named "newprincipal" exists in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="0d838-114">參數</span><span class="sxs-lookup"><span data-stu-id="0d838-114">PARAMETERS</span></span>

### <span data-ttu-id="0d838-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="0d838-115">-ClusterName</span></span>
<span data-ttu-id="0d838-116">Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d838-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="0d838-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d838-117">-DefaultProfile</span></span>
<span data-ttu-id="0d838-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0d838-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d838-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d838-119">-InputObject</span></span>
<span data-ttu-id="0d838-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="0d838-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0d838-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="0d838-121">-Name</span></span>
<span data-ttu-id="0d838-122">主體工作分派資源名稱。</span><span class="sxs-lookup"><span data-stu-id="0d838-122">Principal Assignment resource name.</span></span>

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

### <span data-ttu-id="0d838-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d838-123">-ResourceGroupName</span></span>
<span data-ttu-id="0d838-124">包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d838-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="0d838-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0d838-125">-SubscriptionId</span></span>
<span data-ttu-id="0d838-126">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="0d838-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0d838-127">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="0d838-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0d838-128">-類型</span><span class="sxs-lookup"><span data-stu-id="0d838-128">-Type</span></span>
<span data-ttu-id="0d838-129">資源類型 Kusto/群集/principalAssignments。</span><span class="sxs-lookup"><span data-stu-id="0d838-129">The type of resource, Microsoft.Kusto/Clusters/principalAssignments.</span></span>

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

### <span data-ttu-id="0d838-130">-確認</span><span class="sxs-lookup"><span data-stu-id="0d838-130">-Confirm</span></span>
<span data-ttu-id="0d838-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0d838-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d838-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d838-132">-WhatIf</span></span>
<span data-ttu-id="0d838-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0d838-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d838-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0d838-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d838-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d838-135">CommonParameters</span></span>
<span data-ttu-id="0d838-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0d838-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d838-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0d838-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d838-138">輸入</span><span class="sxs-lookup"><span data-stu-id="0d838-138">INPUTS</span></span>

### <span data-ttu-id="0d838-139">IKustoIdentity （Kusto）的</span><span class="sxs-lookup"><span data-stu-id="0d838-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="0d838-140">輸出</span><span class="sxs-lookup"><span data-stu-id="0d838-140">OUTPUTS</span></span>

### <span data-ttu-id="0d838-141">ICheckNameResult （Kusto）。 Api20200918。</span><span class="sxs-lookup"><span data-stu-id="0d838-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span></span>

## <span data-ttu-id="0d838-142">筆記</span><span class="sxs-lookup"><span data-stu-id="0d838-142">NOTES</span></span>

<span data-ttu-id="0d838-143">別名</span><span class="sxs-lookup"><span data-stu-id="0d838-143">ALIASES</span></span>

<span data-ttu-id="0d838-144">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="0d838-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0d838-145">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="0d838-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0d838-146">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="0d838-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0d838-147">INPUTOBJECT <IKustoIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="0d838-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0d838-148">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d838-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="0d838-149">`[ClusterName <String>]`： Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d838-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="0d838-150">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d838-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="0d838-151">`[DatabaseName <String>]`： Kusto 群集中之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d838-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="0d838-152">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="0d838-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0d838-153">`[Location <String>]`： Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="0d838-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="0d838-154">`[PrincipalAssignmentName <String>]`： Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d838-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="0d838-155">`[ResourceGroupName <String>]`：包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d838-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="0d838-156">`[SubscriptionId <String>]`：取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="0d838-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="0d838-157">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="0d838-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="0d838-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="0d838-158">RELATED LINKS</span></span>

