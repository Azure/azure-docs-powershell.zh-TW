---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustodatabaseprincipalassignmentnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabasePrincipalAssignmentNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabasePrincipalAssignmentNameAvailability.md
ms.openlocfilehash: f61bbfc57017f16f9fee0c05f57aa51bd21d364d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279398"
---
# <span data-ttu-id="5af11-101">Test-AzKustoDatabasePrincipalAssignmentNameAvailability</span><span class="sxs-lookup"><span data-stu-id="5af11-101">Test-AzKustoDatabasePrincipalAssignmentNameAvailability</span></span>

## <span data-ttu-id="5af11-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5af11-102">SYNOPSIS</span></span>
<span data-ttu-id="5af11-103">檢查資料庫主體指派是否有效且尚未使用中。</span><span class="sxs-lookup"><span data-stu-id="5af11-103">Checks that the database principal assignment is valid and is not already in use.</span></span>

## <span data-ttu-id="5af11-104">句法</span><span class="sxs-lookup"><span data-stu-id="5af11-104">SYNTAX</span></span>

### <span data-ttu-id="5af11-105">CheckExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="5af11-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDatabasePrincipalAssignmentNameAvailability -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5af11-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="5af11-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDatabasePrincipalAssignmentNameAvailability -InputObject <IKustoIdentity> -Name <String>
 -Type <Type> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5af11-107">說明</span><span class="sxs-lookup"><span data-stu-id="5af11-107">DESCRIPTION</span></span>
<span data-ttu-id="5af11-108">檢查資料庫主體指派是否有效且尚未使用中。</span><span class="sxs-lookup"><span data-stu-id="5af11-108">Checks that the database principal assignment is valid and is not already in use.</span></span>

## <span data-ttu-id="5af11-109">示例</span><span class="sxs-lookup"><span data-stu-id="5af11-109">EXAMPLES</span></span>

### <span data-ttu-id="5af11-110">範例1：檢查使用中的資料庫 principalassignment 名稱是否有空</span><span class="sxs-lookup"><span data-stu-id="5af11-110">Example 1: Check the availability of a database principalassignment name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -Name "myprincipal" -Type "Microsoft.Kusto/Clusters/Database/principalAssignments" 

Message                                                                                                                                   Name            NameAvailable Reason
-------                                                                                                                                    ----            ------------- ------
Database principal assignment myprincipal already exists in database mykustodatabase. Please select a different principal assignment name. myprincipal   False
```

<span data-ttu-id="5af11-111">上述命令會傳回在群集 "testnewkustocluster" 的資料庫 "mykustodatabase" 中是否存在名為 "myprincipal" 的 PrincipalAssignment。</span><span class="sxs-lookup"><span data-stu-id="5af11-111">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the database "mykustodatabase" from cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="5af11-112">範例2：檢查是否有空使用的資料庫 principalassignment 名稱</span><span class="sxs-lookup"><span data-stu-id="5af11-112">Example 2: Check the availability of a database principalassignment name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -Name "newprincipal" -Type "Microsoft.Kusto/Clusters/Database/principalAssignments"

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="5af11-113">上述命令會傳回在群集 "testnewkustocluster" 的資料庫 "mykustodatabase" 中是否存在名為 "myprincipal" 的 PrincipalAssignment。</span><span class="sxs-lookup"><span data-stu-id="5af11-113">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the database "mykustodatabase" from cluster "testnewkustocluster" .</span></span>

## <span data-ttu-id="5af11-114">參數</span><span class="sxs-lookup"><span data-stu-id="5af11-114">PARAMETERS</span></span>

### <span data-ttu-id="5af11-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="5af11-115">-ClusterName</span></span>
<span data-ttu-id="5af11-116">Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="5af11-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="5af11-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5af11-117">-DatabaseName</span></span>
<span data-ttu-id="5af11-118">Kusto 群集中之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="5af11-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="5af11-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5af11-119">-DefaultProfile</span></span>
<span data-ttu-id="5af11-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5af11-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5af11-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5af11-121">-InputObject</span></span>
<span data-ttu-id="5af11-122">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="5af11-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5af11-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="5af11-123">-Name</span></span>
<span data-ttu-id="5af11-124">主體工作分派資源名稱。</span><span class="sxs-lookup"><span data-stu-id="5af11-124">Principal Assignment resource name.</span></span>

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

### <span data-ttu-id="5af11-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5af11-125">-ResourceGroupName</span></span>
<span data-ttu-id="5af11-126">包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5af11-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="5af11-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5af11-127">-SubscriptionId</span></span>
<span data-ttu-id="5af11-128">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="5af11-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5af11-129">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="5af11-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5af11-130">-類型</span><span class="sxs-lookup"><span data-stu-id="5af11-130">-Type</span></span>
<span data-ttu-id="5af11-131">資源類型 Kusto/群集/資料庫/principalAssignments。</span><span class="sxs-lookup"><span data-stu-id="5af11-131">The type of resource, Microsoft.Kusto/Clusters/Databases/principalAssignments.</span></span>

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

### <span data-ttu-id="5af11-132">-確認</span><span class="sxs-lookup"><span data-stu-id="5af11-132">-Confirm</span></span>
<span data-ttu-id="5af11-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5af11-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5af11-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5af11-134">-WhatIf</span></span>
<span data-ttu-id="5af11-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5af11-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5af11-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5af11-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5af11-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5af11-137">CommonParameters</span></span>
<span data-ttu-id="5af11-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5af11-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5af11-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5af11-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5af11-140">輸入</span><span class="sxs-lookup"><span data-stu-id="5af11-140">INPUTS</span></span>

### <span data-ttu-id="5af11-141">IKustoIdentity （Kusto）的</span><span class="sxs-lookup"><span data-stu-id="5af11-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="5af11-142">輸出</span><span class="sxs-lookup"><span data-stu-id="5af11-142">OUTPUTS</span></span>

### <span data-ttu-id="5af11-143">ICheckNameResult （Kusto）。 Api20200614。</span><span class="sxs-lookup"><span data-stu-id="5af11-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="5af11-144">筆記</span><span class="sxs-lookup"><span data-stu-id="5af11-144">NOTES</span></span>

<span data-ttu-id="5af11-145">別名</span><span class="sxs-lookup"><span data-stu-id="5af11-145">ALIASES</span></span>

<span data-ttu-id="5af11-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="5af11-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5af11-147">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="5af11-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5af11-148">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="5af11-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5af11-149">INPUTOBJECT <IKustoIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="5af11-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5af11-150">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="5af11-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="5af11-151">`[ClusterName <String>]`： Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="5af11-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="5af11-152">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="5af11-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="5af11-153">`[DatabaseName <String>]`： Kusto 群集中之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="5af11-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="5af11-154">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="5af11-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5af11-155">`[Location <String>]`： Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="5af11-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="5af11-156">`[PrincipalAssignmentName <String>]`： Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="5af11-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="5af11-157">`[ResourceGroupName <String>]`：包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5af11-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="5af11-158">`[SubscriptionId <String>]`：取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="5af11-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="5af11-159">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="5af11-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="5af11-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="5af11-160">RELATED LINKS</span></span>

