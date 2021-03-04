---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/get-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 038db26826c4f3f37dcba42e1ccd435512ecd88b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910710"
---
# <span data-ttu-id="8860e-101">Get-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="8860e-101">Get-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="8860e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8860e-102">SYNOPSIS</span></span>
<span data-ttu-id="8860e-103">獲得 Kusto cluster 資料庫主體Assignment。</span><span class="sxs-lookup"><span data-stu-id="8860e-103">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="8860e-104">語法</span><span class="sxs-lookup"><span data-stu-id="8860e-104">SYNTAX</span></span>

### <span data-ttu-id="8860e-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="8860e-105">List (Default)</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8860e-106">獲取</span><span class="sxs-lookup"><span data-stu-id="8860e-106">Get</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8860e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8860e-107">GetViaIdentity</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="8860e-108">描述</span><span class="sxs-lookup"><span data-stu-id="8860e-108">DESCRIPTION</span></span>
<span data-ttu-id="8860e-109">獲得 Kusto cluster 資料庫主體Assignment。</span><span class="sxs-lookup"><span data-stu-id="8860e-109">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="8860e-110">例子</span><span class="sxs-lookup"><span data-stu-id="8860e-110">EXAMPLES</span></span>

### <span data-ttu-id="8860e-111">範例 1：按名稱列出資料庫中的所有 PrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="8860e-111">Example 1: List all PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

Name                                                                     Type
----                                                                     ----
testnewkustocluster/mykustodatabase/kustoprincipal1                      Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="8860e-112">上述命令會以「testnewkustocluster」為叢集找到的資料庫「mykustodatabase」，來將資料庫中的所有 PrincipalAssignment 全部全部發回。</span><span class="sxs-lookup"><span data-stu-id="8860e-112">The above command returns all all PrincipalAssignment in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="8860e-113">範例 2：根據名稱在資料庫中取得特定的 PrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="8860e-113">Example 2: Get a specific PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="8860e-114">上述命令會在所有名為 "kustoprincipal1" 的「mykustodatabase」資料庫中，于「testnewkustocluster」找到的所有 PrincipalAssignment。</span><span class="sxs-lookup"><span data-stu-id="8860e-114">The above command returns all all PrincipalAssignment named "kustoprincipal1" in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="8860e-115">參數</span><span class="sxs-lookup"><span data-stu-id="8860e-115">PARAMETERS</span></span>

### <span data-ttu-id="8860e-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8860e-116">-ClusterName</span></span>
<span data-ttu-id="8860e-117">Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="8860e-117">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8860e-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8860e-118">-DatabaseName</span></span>
<span data-ttu-id="8860e-119">Kusto cluster 中的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="8860e-119">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8860e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8860e-120">-DefaultProfile</span></span>
<span data-ttu-id="8860e-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8860e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8860e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8860e-122">-InputObject</span></span>
<span data-ttu-id="8860e-123">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="8860e-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8860e-124">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="8860e-124">-PrincipalAssignmentName</span></span>
<span data-ttu-id="8860e-125">Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="8860e-125">The name of the Kusto principalAssignment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8860e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8860e-126">-ResourceGroupName</span></span>
<span data-ttu-id="8860e-127">包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="8860e-127">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8860e-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8860e-128">-SubscriptionId</span></span>
<span data-ttu-id="8860e-129">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="8860e-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8860e-130">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="8860e-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8860e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8860e-131">CommonParameters</span></span>
<span data-ttu-id="8860e-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8860e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8860e-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8860e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8860e-134">輸入</span><span class="sxs-lookup"><span data-stu-id="8860e-134">INPUTS</span></span>

### <span data-ttu-id="8860e-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="8860e-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="8860e-136">輸出</span><span class="sxs-lookup"><span data-stu-id="8860e-136">OUTPUTS</span></span>

### <span data-ttu-id="8860e-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="8860e-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="8860e-138">筆記</span><span class="sxs-lookup"><span data-stu-id="8860e-138">NOTES</span></span>

<span data-ttu-id="8860e-139">別名</span><span class="sxs-lookup"><span data-stu-id="8860e-139">ALIASES</span></span>

<span data-ttu-id="8860e-140">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="8860e-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8860e-141">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="8860e-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8860e-142">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="8860e-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8860e-143">INPUTOBJECT： <IKustoIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="8860e-143">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8860e-144">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫組配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="8860e-144">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="8860e-145">`[ClusterName <String>]`：Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="8860e-145">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="8860e-146">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="8860e-146">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="8860e-147">`[DatabaseName <String>]`：Kusto cluster 中的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="8860e-147">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="8860e-148">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="8860e-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8860e-149">`[Location <String>]`：Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="8860e-149">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="8860e-150">`[PrincipalAssignmentName <String>]`：Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="8860e-150">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="8860e-151">`[ResourceGroupName <String>]`：包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="8860e-151">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="8860e-152">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="8860e-152">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8860e-153">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="8860e-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="8860e-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="8860e-154">RELATED LINKS</span></span>

