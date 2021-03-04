---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/test-azkustodatabaseprincipalassignmentnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabasePrincipalAssignmentNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabasePrincipalAssignmentNameAvailability.md
ms.openlocfilehash: 6a151119552ab4b0e42d247641248dd110af4994
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907126"
---
# <span data-ttu-id="792b1-101">Test-AzKustoDatabasePrincipalAssignmentNameAvailability</span><span class="sxs-lookup"><span data-stu-id="792b1-101">Test-AzKustoDatabasePrincipalAssignmentNameAvailability</span></span>

## <span data-ttu-id="792b1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="792b1-102">SYNOPSIS</span></span>
<span data-ttu-id="792b1-103">檢查資料庫主體指派是否有效，且尚未使用中。</span><span class="sxs-lookup"><span data-stu-id="792b1-103">Checks that the database principal assignment is valid and is not already in use.</span></span>

## <span data-ttu-id="792b1-104">語法</span><span class="sxs-lookup"><span data-stu-id="792b1-104">SYNTAX</span></span>

### <span data-ttu-id="792b1-105">CheckExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="792b1-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDatabasePrincipalAssignmentNameAvailability -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="792b1-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="792b1-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDatabasePrincipalAssignmentNameAvailability -InputObject <IKustoIdentity> -Name <String>
 -Type <Type> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="792b1-107">描述</span><span class="sxs-lookup"><span data-stu-id="792b1-107">DESCRIPTION</span></span>
<span data-ttu-id="792b1-108">檢查資料庫主體指派是否有效，且尚未使用中。</span><span class="sxs-lookup"><span data-stu-id="792b1-108">Checks that the database principal assignment is valid and is not already in use.</span></span>

## <span data-ttu-id="792b1-109">例子</span><span class="sxs-lookup"><span data-stu-id="792b1-109">EXAMPLES</span></span>

### <span data-ttu-id="792b1-110">範例 1：檢查使用中的資料庫主體指定名稱的可用性</span><span class="sxs-lookup"><span data-stu-id="792b1-110">Example 1: Check the availability of a database principalassignment name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -Name "myprincipal" -Type "Microsoft.Kusto/Clusters/Database/principalAssignments" 

Message                                                                                                                                   Name            NameAvailable Reason
-------                                                                                                                                    ----            ------------- ------
Database principal assignment myprincipal already exists in database mykustodatabase. Please select a different principal assignment name. myprincipal   False
```

<span data-ttu-id="792b1-111">上述命令會從叢集「testnewkustocluster」的「myprincipal」資料庫"mykustodatabase"中，會返回名為"myprincipal"的 PrincipalAssignment。</span><span class="sxs-lookup"><span data-stu-id="792b1-111">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the database "mykustodatabase" from cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="792b1-112">範例 2：檢查不使用的資料庫主體指定名稱的可用性</span><span class="sxs-lookup"><span data-stu-id="792b1-112">Example 2: Check the availability of a database principalassignment name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -Name "newprincipal" -Type "Microsoft.Kusto/Clusters/Database/principalAssignments"

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="792b1-113">上述命令會從叢集「testnewkustocluster」的「myprincipal」資料庫「mykustodatabase」中，會返回名為「myprincipal」的 PrincipalAssignment。</span><span class="sxs-lookup"><span data-stu-id="792b1-113">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the database "mykustodatabase" from cluster "testnewkustocluster" .</span></span>

## <span data-ttu-id="792b1-114">參數</span><span class="sxs-lookup"><span data-stu-id="792b1-114">PARAMETERS</span></span>

### <span data-ttu-id="792b1-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="792b1-115">-ClusterName</span></span>
<span data-ttu-id="792b1-116">Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="792b1-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="792b1-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="792b1-117">-DatabaseName</span></span>
<span data-ttu-id="792b1-118">Kusto cluster 中的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="792b1-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="792b1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="792b1-119">-DefaultProfile</span></span>
<span data-ttu-id="792b1-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="792b1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="792b1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="792b1-121">-InputObject</span></span>
<span data-ttu-id="792b1-122">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="792b1-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="792b1-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="792b1-123">-Name</span></span>
<span data-ttu-id="792b1-124">主要工作分派資源名稱。</span><span class="sxs-lookup"><span data-stu-id="792b1-124">Principal Assignment resource name.</span></span>

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

### <span data-ttu-id="792b1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="792b1-125">-ResourceGroupName</span></span>
<span data-ttu-id="792b1-126">包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="792b1-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="792b1-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="792b1-127">-SubscriptionId</span></span>
<span data-ttu-id="792b1-128">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="792b1-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="792b1-129">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="792b1-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="792b1-130">-類型</span><span class="sxs-lookup"><span data-stu-id="792b1-130">-Type</span></span>
<span data-ttu-id="792b1-131">資源類型：Microsoft.Kusto/Clusters/Databases/principalAssignments。</span><span class="sxs-lookup"><span data-stu-id="792b1-131">The type of resource, Microsoft.Kusto/Clusters/Databases/principalAssignments.</span></span>

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

### <span data-ttu-id="792b1-132">-確認</span><span class="sxs-lookup"><span data-stu-id="792b1-132">-Confirm</span></span>
<span data-ttu-id="792b1-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="792b1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="792b1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="792b1-134">-WhatIf</span></span>
<span data-ttu-id="792b1-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="792b1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="792b1-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="792b1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="792b1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="792b1-137">CommonParameters</span></span>
<span data-ttu-id="792b1-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="792b1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="792b1-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="792b1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="792b1-140">輸入</span><span class="sxs-lookup"><span data-stu-id="792b1-140">INPUTS</span></span>

### <span data-ttu-id="792b1-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="792b1-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="792b1-142">輸出</span><span class="sxs-lookup"><span data-stu-id="792b1-142">OUTPUTS</span></span>

### <span data-ttu-id="792b1-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.models.Api20200918.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="792b1-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span></span>

## <span data-ttu-id="792b1-144">筆記</span><span class="sxs-lookup"><span data-stu-id="792b1-144">NOTES</span></span>

<span data-ttu-id="792b1-145">別名</span><span class="sxs-lookup"><span data-stu-id="792b1-145">ALIASES</span></span>

<span data-ttu-id="792b1-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="792b1-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="792b1-147">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="792b1-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="792b1-148">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="792b1-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="792b1-149">INPUTOBJECT： <IKustoIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="792b1-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="792b1-150">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫組配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="792b1-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="792b1-151">`[ClusterName <String>]`：Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="792b1-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="792b1-152">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="792b1-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="792b1-153">`[DatabaseName <String>]`：Kusto cluster 中的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="792b1-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="792b1-154">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="792b1-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="792b1-155">`[Location <String>]`：Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="792b1-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="792b1-156">`[PrincipalAssignmentName <String>]`：Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="792b1-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="792b1-157">`[ResourceGroupName <String>]`：包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="792b1-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="792b1-158">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="792b1-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="792b1-159">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="792b1-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="792b1-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="792b1-160">RELATED LINKS</span></span>

