---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/test-azkustodataconnectionnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDataConnectionNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDataConnectionNameAvailability.md
ms.openlocfilehash: b33f496845cf03a31a90203d5a4d10076d156e59
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916405"
---
# <span data-ttu-id="53371-101">Test-AzKustoDataConnectionNameAvailability</span><span class="sxs-lookup"><span data-stu-id="53371-101">Test-AzKustoDataConnectionNameAvailability</span></span>

## <span data-ttu-id="53371-102">簡介</span><span class="sxs-lookup"><span data-stu-id="53371-102">SYNOPSIS</span></span>
<span data-ttu-id="53371-103">檢查資料連線名稱是否有效，且尚未使用中。</span><span class="sxs-lookup"><span data-stu-id="53371-103">Checks that the data connection name is valid and is not already in use.</span></span>

## <span data-ttu-id="53371-104">語法</span><span class="sxs-lookup"><span data-stu-id="53371-104">SYNTAX</span></span>

### <span data-ttu-id="53371-105">CheckExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="53371-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDataConnectionNameAvailability -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="53371-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="53371-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDataConnectionNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="53371-107">描述</span><span class="sxs-lookup"><span data-stu-id="53371-107">DESCRIPTION</span></span>
<span data-ttu-id="53371-108">檢查資料連線名稱是否有效，且尚未使用中。</span><span class="sxs-lookup"><span data-stu-id="53371-108">Checks that the data connection name is valid and is not already in use.</span></span>

## <span data-ttu-id="53371-109">例子</span><span class="sxs-lookup"><span data-stu-id="53371-109">EXAMPLES</span></span>

### <span data-ttu-id="53371-110">範例 1：檢查使用中資料連線名稱的可用性</span><span class="sxs-lookup"><span data-stu-id="53371-110">Example 1: Check the availability of a Data Connection name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoDataConnectionNameAvailability -ClusterName testnewkustocluster -DatabaseName mykustodatabase -ResourceGroupName testrg -Name mykustodataconnection -Type Microsoft.Kusto/Clusters/Databases/dataConnections

Message                                                                                                                                                          Name                  NameAvailable Reason
-------                                                                                                                                                          ----                  ------------- ------
Data Connection mykustodataconnection already exists in database mykustodatabase in cluster testnewkustocluster. Please select a different data connection name. mykustodataconnection False         AlreadyExists
```

<span data-ttu-id="53371-111">上述命令會返回名為"mykustodataconnection"的資料連線是否存在於 "mykustodatabase" 資料庫中。</span><span class="sxs-lookup"><span data-stu-id="53371-111">The above command returns whether or not a Data Connection named "mykustodataconnection" exists in the "mykustodatabase" database.</span></span>

### <span data-ttu-id="53371-112">範例 2：檢查不使用的資料連線名稱是否可用</span><span class="sxs-lookup"><span data-stu-id="53371-112">Example 2: Check the availability of a Data Connection name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoDataConnectionNameAvailability -ClusterName testnewkustocluster -DatabaseName mykustodatabase -ResourceGroupName testrg -Name mydataconnection -Type Microsoft.Kusto/Clusters/Databases/dataConnections

Message Name             NameAvailable Reason
------- ----             ------------- ------
        mydataconnection True
```

<span data-ttu-id="53371-113">上述命令會返回名為「mydataconnection」的資料連線是否存在於「mykustodatabase」資料庫中。</span><span class="sxs-lookup"><span data-stu-id="53371-113">The above command returns whether or not a Data Connection named "mydataconnection" exists in the "mykustodatabase" database.</span></span>

## <span data-ttu-id="53371-114">參數</span><span class="sxs-lookup"><span data-stu-id="53371-114">PARAMETERS</span></span>

### <span data-ttu-id="53371-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="53371-115">-ClusterName</span></span>
<span data-ttu-id="53371-116">Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="53371-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="53371-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="53371-117">-DatabaseName</span></span>
<span data-ttu-id="53371-118">Kusto cluster 中的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="53371-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="53371-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53371-119">-DefaultProfile</span></span>
<span data-ttu-id="53371-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="53371-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53371-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53371-121">-InputObject</span></span>
<span data-ttu-id="53371-122">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="53371-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="53371-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="53371-123">-Name</span></span>
<span data-ttu-id="53371-124">資料連線名稱。</span><span class="sxs-lookup"><span data-stu-id="53371-124">Data Connection name.</span></span>

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

### <span data-ttu-id="53371-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53371-125">-ResourceGroupName</span></span>
<span data-ttu-id="53371-126">包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="53371-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="53371-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="53371-127">-SubscriptionId</span></span>
<span data-ttu-id="53371-128">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="53371-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="53371-129">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="53371-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="53371-130">-類型</span><span class="sxs-lookup"><span data-stu-id="53371-130">-Type</span></span>
<span data-ttu-id="53371-131">資源類型：Microsoft.Kusto/Clusters/Databases/dataConnections。</span><span class="sxs-lookup"><span data-stu-id="53371-131">The type of resource, Microsoft.Kusto/Clusters/Databases/dataConnections.</span></span>

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

### <span data-ttu-id="53371-132">-確認</span><span class="sxs-lookup"><span data-stu-id="53371-132">-Confirm</span></span>
<span data-ttu-id="53371-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="53371-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53371-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53371-134">-WhatIf</span></span>
<span data-ttu-id="53371-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="53371-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53371-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="53371-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53371-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53371-137">CommonParameters</span></span>
<span data-ttu-id="53371-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="53371-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53371-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53371-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53371-140">輸入</span><span class="sxs-lookup"><span data-stu-id="53371-140">INPUTS</span></span>

### <span data-ttu-id="53371-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="53371-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="53371-142">輸出</span><span class="sxs-lookup"><span data-stu-id="53371-142">OUTPUTS</span></span>

### <span data-ttu-id="53371-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.models.Api20200918.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="53371-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span></span>

## <span data-ttu-id="53371-144">筆記</span><span class="sxs-lookup"><span data-stu-id="53371-144">NOTES</span></span>

<span data-ttu-id="53371-145">別名</span><span class="sxs-lookup"><span data-stu-id="53371-145">ALIASES</span></span>

<span data-ttu-id="53371-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="53371-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="53371-147">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="53371-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="53371-148">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="53371-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="53371-149">INPUTOBJECT： <IKustoIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="53371-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="53371-150">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫組配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="53371-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="53371-151">`[ClusterName <String>]`：Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="53371-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="53371-152">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="53371-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="53371-153">`[DatabaseName <String>]`：Kusto cluster 中的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="53371-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="53371-154">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="53371-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="53371-155">`[Location <String>]`：Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="53371-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="53371-156">`[PrincipalAssignmentName <String>]`：Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="53371-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="53371-157">`[ResourceGroupName <String>]`：包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="53371-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="53371-158">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="53371-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="53371-159">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="53371-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="53371-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="53371-160">RELATED LINKS</span></span>

