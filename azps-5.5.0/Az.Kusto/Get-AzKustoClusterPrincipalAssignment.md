---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 9ff5021e43b9d23fc79ffca81519809ae0052558
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131650"
---
# <span data-ttu-id="b257b-101">Get-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="b257b-101">Get-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="b257b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b257b-102">SYNOPSIS</span></span>
<span data-ttu-id="b257b-103">取得 Kusto 群集 principalAssignment。</span><span class="sxs-lookup"><span data-stu-id="b257b-103">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="b257b-104">句法</span><span class="sxs-lookup"><span data-stu-id="b257b-104">SYNTAX</span></span>

### <span data-ttu-id="b257b-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="b257b-105">List (Default)</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b257b-106">獲取</span><span class="sxs-lookup"><span data-stu-id="b257b-106">Get</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b257b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b257b-107">GetViaIdentity</span></span>
```
Get-AzKustoClusterPrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b257b-108">說明</span><span class="sxs-lookup"><span data-stu-id="b257b-108">DESCRIPTION</span></span>
<span data-ttu-id="b257b-109">取得 Kusto 群集 principalAssignment。</span><span class="sxs-lookup"><span data-stu-id="b257b-109">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="b257b-110">示例</span><span class="sxs-lookup"><span data-stu-id="b257b-110">EXAMPLES</span></span>

### <span data-ttu-id="b257b-111">範例1：列出所有 Kusto 群集 principalAssignment</span><span class="sxs-lookup"><span data-stu-id="b257b-111">Example 1: List all Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="b257b-112">上述命令會列出群集 "testnewkustocluster" 中的所有 principalAssignment。</span><span class="sxs-lookup"><span data-stu-id="b257b-112">The above command lists all principalAssignment in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="b257b-113">範例2：透過名稱取得 Kusto 群集 principalAssignment</span><span class="sxs-lookup"><span data-stu-id="b257b-113">Example 2: Gets a Kusto cluster principalAssignment by name</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="b257b-114">上述命令會傳回群集 "testnewkustocluster" 中名為「kustoprincipal1」的 Kusto 群集 principalAssignment。</span><span class="sxs-lookup"><span data-stu-id="b257b-114">The above command returns the Kusto cluster principalAssignment named "kustoprincipal1" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="b257b-115">參數</span><span class="sxs-lookup"><span data-stu-id="b257b-115">PARAMETERS</span></span>

### <span data-ttu-id="b257b-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b257b-116">-ClusterName</span></span>
<span data-ttu-id="b257b-117">Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="b257b-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="b257b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b257b-118">-DefaultProfile</span></span>
<span data-ttu-id="b257b-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b257b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b257b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b257b-120">-InputObject</span></span>
<span data-ttu-id="b257b-121">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b257b-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b257b-122">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="b257b-122">-PrincipalAssignmentName</span></span>
<span data-ttu-id="b257b-123">Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="b257b-123">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="b257b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b257b-124">-ResourceGroupName</span></span>
<span data-ttu-id="b257b-125">包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b257b-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="b257b-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b257b-126">-SubscriptionId</span></span>
<span data-ttu-id="b257b-127">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="b257b-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b257b-128">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="b257b-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b257b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b257b-129">CommonParameters</span></span>
<span data-ttu-id="b257b-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b257b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b257b-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b257b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b257b-132">輸入</span><span class="sxs-lookup"><span data-stu-id="b257b-132">INPUTS</span></span>

### <span data-ttu-id="b257b-133">IKustoIdentity （Kusto）的</span><span class="sxs-lookup"><span data-stu-id="b257b-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="b257b-134">輸出</span><span class="sxs-lookup"><span data-stu-id="b257b-134">OUTPUTS</span></span>

### <span data-ttu-id="b257b-135">IClusterPrincipalAssignment （Kusto）。 Api20200918。</span><span class="sxs-lookup"><span data-stu-id="b257b-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="b257b-136">筆記</span><span class="sxs-lookup"><span data-stu-id="b257b-136">NOTES</span></span>

<span data-ttu-id="b257b-137">別名</span><span class="sxs-lookup"><span data-stu-id="b257b-137">ALIASES</span></span>

<span data-ttu-id="b257b-138">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="b257b-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b257b-139">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="b257b-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b257b-140">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="b257b-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b257b-141">INPUTOBJECT <IKustoIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="b257b-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b257b-142">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="b257b-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="b257b-143">`[ClusterName <String>]`： Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="b257b-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="b257b-144">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="b257b-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="b257b-145">`[DatabaseName <String>]`： Kusto 群集中之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="b257b-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="b257b-146">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="b257b-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b257b-147">`[Location <String>]`： Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="b257b-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="b257b-148">`[PrincipalAssignmentName <String>]`： Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="b257b-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="b257b-149">`[ResourceGroupName <String>]`：包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b257b-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="b257b-150">`[SubscriptionId <String>]`：取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="b257b-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b257b-151">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="b257b-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b257b-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="b257b-152">RELATED LINKS</span></span>

