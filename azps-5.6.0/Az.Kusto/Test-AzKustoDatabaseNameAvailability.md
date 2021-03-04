---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/test-azkustodatabasenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabaseNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabaseNameAvailability.md
ms.openlocfilehash: 9be95744e7528a1b1eeec3a2784e7c0ccf21e8d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905390"
---
# <span data-ttu-id="51b09-101">Test-AzKustoDatabaseNameAvailability</span><span class="sxs-lookup"><span data-stu-id="51b09-101">Test-AzKustoDatabaseNameAvailability</span></span>

## <span data-ttu-id="51b09-102">簡介</span><span class="sxs-lookup"><span data-stu-id="51b09-102">SYNOPSIS</span></span>
<span data-ttu-id="51b09-103">檢查資料庫名稱是否有效，且尚未使用中。</span><span class="sxs-lookup"><span data-stu-id="51b09-103">Checks that the database name is valid and is not already in use.</span></span>

## <span data-ttu-id="51b09-104">語法</span><span class="sxs-lookup"><span data-stu-id="51b09-104">SYNTAX</span></span>

### <span data-ttu-id="51b09-105">CheckExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="51b09-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDatabaseNameAvailability -ClusterName <String> -ResourceGroupName <String> -Name <String>
 -Type <Type> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="51b09-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="51b09-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDatabaseNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="51b09-107">描述</span><span class="sxs-lookup"><span data-stu-id="51b09-107">DESCRIPTION</span></span>
<span data-ttu-id="51b09-108">檢查資料庫名稱是否有效，且尚未使用中。</span><span class="sxs-lookup"><span data-stu-id="51b09-108">Checks that the database name is valid and is not already in use.</span></span>

## <span data-ttu-id="51b09-109">例子</span><span class="sxs-lookup"><span data-stu-id="51b09-109">EXAMPLES</span></span>

### <span data-ttu-id="51b09-110">範例 1：檢查使用中的 Kusto 資料庫名稱是否可用</span><span class="sxs-lookup"><span data-stu-id="51b09-110">Example 1: Check the availability of a Kusto database name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoDatabaseNameAvailability -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Type Microsoft.Kusto/Clusters/Databases

Message                                                                                                          Name            NameAvailable Reason
-------                                                                                                          ----            ------------- ------
Database mykustodatabase already exists in cluster testnewkustocluster. Please select a different database name. mykustodatabase False
```

<span data-ttu-id="51b09-111">上述命令會返回名為 "mykustodatabase" 的 Kusto 資料庫是否存在於 "testnewkustocluster" 叢集中。</span><span class="sxs-lookup"><span data-stu-id="51b09-111">The above command returns whether or not a Kusto database named "mykustodatabase" exists in the "testnewkustocluster" cluster.</span></span>

### <span data-ttu-id="51b09-112">範例 2：檢查未使用之 Kusto 資料庫名稱的可用性</span><span class="sxs-lookup"><span data-stu-id="51b09-112">Example 2: Check the availability of a Kusto database name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoDatabaseNameAvailability -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase2 -Type Microsoft.Kusto/Clusters/Databases

Message Name             NameAvailable Reason
------- ----             ------------- ------
        mykustodatabase2 True
```

<span data-ttu-id="51b09-113">上述命令會返回名為 "mykustodatabase2" 的 Kusto 資料庫是否存在於 "testnewkustocluster" 叢集中。</span><span class="sxs-lookup"><span data-stu-id="51b09-113">The above command returns whether or not a Kusto database named "mykustodatabase2" exists in the "testnewkustocluster" cluster.</span></span>

## <span data-ttu-id="51b09-114">參數</span><span class="sxs-lookup"><span data-stu-id="51b09-114">PARAMETERS</span></span>

### <span data-ttu-id="51b09-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="51b09-115">-ClusterName</span></span>
<span data-ttu-id="51b09-116">Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="51b09-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="51b09-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51b09-117">-DefaultProfile</span></span>
<span data-ttu-id="51b09-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="51b09-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51b09-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51b09-119">-InputObject</span></span>
<span data-ttu-id="51b09-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="51b09-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="51b09-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="51b09-121">-Name</span></span>
<span data-ttu-id="51b09-122">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="51b09-122">Resource name.</span></span>

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

### <span data-ttu-id="51b09-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51b09-123">-ResourceGroupName</span></span>
<span data-ttu-id="51b09-124">包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="51b09-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="51b09-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="51b09-125">-SubscriptionId</span></span>
<span data-ttu-id="51b09-126">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="51b09-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="51b09-127">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="51b09-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="51b09-128">-類型</span><span class="sxs-lookup"><span data-stu-id="51b09-128">-Type</span></span>
<span data-ttu-id="51b09-129">資源類型，例如 Microsoft.Kusto/Clusters/databases。</span><span class="sxs-lookup"><span data-stu-id="51b09-129">The type of resource, for instance Microsoft.Kusto/Clusters/databases.</span></span>

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

### <span data-ttu-id="51b09-130">-確認</span><span class="sxs-lookup"><span data-stu-id="51b09-130">-Confirm</span></span>
<span data-ttu-id="51b09-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="51b09-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51b09-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51b09-132">-WhatIf</span></span>
<span data-ttu-id="51b09-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="51b09-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51b09-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="51b09-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51b09-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51b09-135">CommonParameters</span></span>
<span data-ttu-id="51b09-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="51b09-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51b09-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="51b09-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51b09-138">輸入</span><span class="sxs-lookup"><span data-stu-id="51b09-138">INPUTS</span></span>

### <span data-ttu-id="51b09-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="51b09-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="51b09-140">輸出</span><span class="sxs-lookup"><span data-stu-id="51b09-140">OUTPUTS</span></span>

### <span data-ttu-id="51b09-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.models.Api20200918.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="51b09-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span></span>

## <span data-ttu-id="51b09-142">筆記</span><span class="sxs-lookup"><span data-stu-id="51b09-142">NOTES</span></span>

<span data-ttu-id="51b09-143">別名</span><span class="sxs-lookup"><span data-stu-id="51b09-143">ALIASES</span></span>

<span data-ttu-id="51b09-144">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="51b09-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="51b09-145">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="51b09-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="51b09-146">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="51b09-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="51b09-147">INPUTOBJECT： <IKustoIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="51b09-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="51b09-148">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫組配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="51b09-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="51b09-149">`[ClusterName <String>]`：Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="51b09-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="51b09-150">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="51b09-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="51b09-151">`[DatabaseName <String>]`：Kusto cluster 中的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="51b09-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="51b09-152">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="51b09-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="51b09-153">`[Location <String>]`：Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="51b09-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="51b09-154">`[PrincipalAssignmentName <String>]`：Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="51b09-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="51b09-155">`[ResourceGroupName <String>]`：包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="51b09-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="51b09-156">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="51b09-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="51b09-157">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="51b09-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="51b09-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="51b09-158">RELATED LINKS</span></span>

