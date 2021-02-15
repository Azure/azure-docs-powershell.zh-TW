---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 533e247ed2a0b9682e2fe87699d0a77b51ed06ee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131623"
---
# <span data-ttu-id="319ff-101">Get-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="319ff-101">Get-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="319ff-102">摘要</span><span class="sxs-lookup"><span data-stu-id="319ff-102">SYNOPSIS</span></span>
<span data-ttu-id="319ff-103">取得 Kusto 群集資料庫 principalAssignment。</span><span class="sxs-lookup"><span data-stu-id="319ff-103">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="319ff-104">句法</span><span class="sxs-lookup"><span data-stu-id="319ff-104">SYNTAX</span></span>

### <span data-ttu-id="319ff-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="319ff-105">List (Default)</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="319ff-106">獲取</span><span class="sxs-lookup"><span data-stu-id="319ff-106">Get</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="319ff-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="319ff-107">GetViaIdentity</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="319ff-108">說明</span><span class="sxs-lookup"><span data-stu-id="319ff-108">DESCRIPTION</span></span>
<span data-ttu-id="319ff-109">取得 Kusto 群集資料庫 principalAssignment。</span><span class="sxs-lookup"><span data-stu-id="319ff-109">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="319ff-110">示例</span><span class="sxs-lookup"><span data-stu-id="319ff-110">EXAMPLES</span></span>

### <span data-ttu-id="319ff-111">範例1：依名稱列出資料庫中的所有 PrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="319ff-111">Example 1: List all PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

Name                                                                     Type
----                                                                     ----
testnewkustocluster/mykustodatabase/kustoprincipal1                      Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="319ff-112">上述命令會傳回在群集 "testnewkustocluster" 中找到的資料庫 "mykustodatabase" 中的所有 PrincipalAssignment。</span><span class="sxs-lookup"><span data-stu-id="319ff-112">The above command returns all all PrincipalAssignment in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="319ff-113">範例2：依名稱在資料庫中取得特定 PrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="319ff-113">Example 2: Get a specific PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="319ff-114">上述命令會傳回在群集 "testnewkustocluster" 中找到的資料庫 "mykustodatabase" 中所有名為 "kustoprincipal1" 的所有 PrincipalAssignment。</span><span class="sxs-lookup"><span data-stu-id="319ff-114">The above command returns all all PrincipalAssignment named "kustoprincipal1" in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="319ff-115">參數</span><span class="sxs-lookup"><span data-stu-id="319ff-115">PARAMETERS</span></span>

### <span data-ttu-id="319ff-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="319ff-116">-ClusterName</span></span>
<span data-ttu-id="319ff-117">Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="319ff-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="319ff-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="319ff-118">-DatabaseName</span></span>
<span data-ttu-id="319ff-119">Kusto 群集中之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="319ff-119">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="319ff-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="319ff-120">-DefaultProfile</span></span>
<span data-ttu-id="319ff-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="319ff-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="319ff-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="319ff-122">-InputObject</span></span>
<span data-ttu-id="319ff-123">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="319ff-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="319ff-124">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="319ff-124">-PrincipalAssignmentName</span></span>
<span data-ttu-id="319ff-125">Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="319ff-125">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="319ff-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="319ff-126">-ResourceGroupName</span></span>
<span data-ttu-id="319ff-127">包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="319ff-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="319ff-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="319ff-128">-SubscriptionId</span></span>
<span data-ttu-id="319ff-129">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="319ff-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="319ff-130">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="319ff-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="319ff-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="319ff-131">CommonParameters</span></span>
<span data-ttu-id="319ff-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="319ff-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="319ff-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="319ff-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="319ff-134">輸入</span><span class="sxs-lookup"><span data-stu-id="319ff-134">INPUTS</span></span>

### <span data-ttu-id="319ff-135">IKustoIdentity （Kusto）的</span><span class="sxs-lookup"><span data-stu-id="319ff-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="319ff-136">輸出</span><span class="sxs-lookup"><span data-stu-id="319ff-136">OUTPUTS</span></span>

### <span data-ttu-id="319ff-137">IDatabasePrincipalAssignment （Kusto）。 Api20200918。</span><span class="sxs-lookup"><span data-stu-id="319ff-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="319ff-138">筆記</span><span class="sxs-lookup"><span data-stu-id="319ff-138">NOTES</span></span>

<span data-ttu-id="319ff-139">別名</span><span class="sxs-lookup"><span data-stu-id="319ff-139">ALIASES</span></span>

<span data-ttu-id="319ff-140">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="319ff-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="319ff-141">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="319ff-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="319ff-142">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="319ff-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="319ff-143">INPUTOBJECT <IKustoIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="319ff-143">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="319ff-144">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="319ff-144">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="319ff-145">`[ClusterName <String>]`： Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="319ff-145">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="319ff-146">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="319ff-146">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="319ff-147">`[DatabaseName <String>]`： Kusto 群集中之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="319ff-147">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="319ff-148">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="319ff-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="319ff-149">`[Location <String>]`： Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="319ff-149">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="319ff-150">`[PrincipalAssignmentName <String>]`： Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="319ff-150">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="319ff-151">`[ResourceGroupName <String>]`：包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="319ff-151">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="319ff-152">`[SubscriptionId <String>]`：取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="319ff-152">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="319ff-153">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="319ff-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="319ff-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="319ff-154">RELATED LINKS</span></span>

