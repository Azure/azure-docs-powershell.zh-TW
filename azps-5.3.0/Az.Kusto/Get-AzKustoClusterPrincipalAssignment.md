---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 9ff5021e43b9d23fc79ffca81519809ae0052558
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435363"
---
# <span data-ttu-id="f81ec-101">Get-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="f81ec-101">Get-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="f81ec-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f81ec-102">SYNOPSIS</span></span>
<span data-ttu-id="f81ec-103">取得 Kusto 群集 principalAssignment。</span><span class="sxs-lookup"><span data-stu-id="f81ec-103">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="f81ec-104">句法</span><span class="sxs-lookup"><span data-stu-id="f81ec-104">SYNTAX</span></span>

### <span data-ttu-id="f81ec-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="f81ec-105">List (Default)</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f81ec-106">獲取</span><span class="sxs-lookup"><span data-stu-id="f81ec-106">Get</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f81ec-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f81ec-107">GetViaIdentity</span></span>
```
Get-AzKustoClusterPrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="f81ec-108">說明</span><span class="sxs-lookup"><span data-stu-id="f81ec-108">DESCRIPTION</span></span>
<span data-ttu-id="f81ec-109">取得 Kusto 群集 principalAssignment。</span><span class="sxs-lookup"><span data-stu-id="f81ec-109">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="f81ec-110">示例</span><span class="sxs-lookup"><span data-stu-id="f81ec-110">EXAMPLES</span></span>

### <span data-ttu-id="f81ec-111">範例1：列出所有 Kusto 群集 principalAssignment</span><span class="sxs-lookup"><span data-stu-id="f81ec-111">Example 1: List all Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="f81ec-112">上述命令會列出群集 "testnewkustocluster" 中的所有 principalAssignment。</span><span class="sxs-lookup"><span data-stu-id="f81ec-112">The above command lists all principalAssignment in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="f81ec-113">範例2：透過名稱取得 Kusto 群集 principalAssignment</span><span class="sxs-lookup"><span data-stu-id="f81ec-113">Example 2: Gets a Kusto cluster principalAssignment by name</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="f81ec-114">上述命令會傳回群集 "testnewkustocluster" 中名為「kustoprincipal1」的 Kusto 群集 principalAssignment。</span><span class="sxs-lookup"><span data-stu-id="f81ec-114">The above command returns the Kusto cluster principalAssignment named "kustoprincipal1" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="f81ec-115">參數</span><span class="sxs-lookup"><span data-stu-id="f81ec-115">PARAMETERS</span></span>

### <span data-ttu-id="f81ec-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f81ec-116">-ClusterName</span></span>
<span data-ttu-id="f81ec-117">Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="f81ec-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="f81ec-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f81ec-118">-DefaultProfile</span></span>
<span data-ttu-id="f81ec-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f81ec-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f81ec-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f81ec-120">-InputObject</span></span>
<span data-ttu-id="f81ec-121">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f81ec-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f81ec-122">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="f81ec-122">-PrincipalAssignmentName</span></span>
<span data-ttu-id="f81ec-123">Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="f81ec-123">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="f81ec-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f81ec-124">-ResourceGroupName</span></span>
<span data-ttu-id="f81ec-125">包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f81ec-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="f81ec-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f81ec-126">-SubscriptionId</span></span>
<span data-ttu-id="f81ec-127">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="f81ec-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f81ec-128">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="f81ec-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f81ec-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f81ec-129">CommonParameters</span></span>
<span data-ttu-id="f81ec-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f81ec-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f81ec-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f81ec-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f81ec-132">輸入</span><span class="sxs-lookup"><span data-stu-id="f81ec-132">INPUTS</span></span>

### <span data-ttu-id="f81ec-133">IKustoIdentity （Kusto）的</span><span class="sxs-lookup"><span data-stu-id="f81ec-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="f81ec-134">輸出</span><span class="sxs-lookup"><span data-stu-id="f81ec-134">OUTPUTS</span></span>

### <span data-ttu-id="f81ec-135">IClusterPrincipalAssignment （Kusto）。 Api20200918。</span><span class="sxs-lookup"><span data-stu-id="f81ec-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="f81ec-136">筆記</span><span class="sxs-lookup"><span data-stu-id="f81ec-136">NOTES</span></span>

<span data-ttu-id="f81ec-137">別名</span><span class="sxs-lookup"><span data-stu-id="f81ec-137">ALIASES</span></span>

<span data-ttu-id="f81ec-138">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="f81ec-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f81ec-139">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="f81ec-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f81ec-140">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="f81ec-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f81ec-141">INPUTOBJECT <IKustoIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="f81ec-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f81ec-142">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="f81ec-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="f81ec-143">`[ClusterName <String>]`： Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="f81ec-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="f81ec-144">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="f81ec-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="f81ec-145">`[DatabaseName <String>]`： Kusto 群集中之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="f81ec-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="f81ec-146">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="f81ec-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f81ec-147">`[Location <String>]`： Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="f81ec-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="f81ec-148">`[PrincipalAssignmentName <String>]`： Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="f81ec-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="f81ec-149">`[ResourceGroupName <String>]`：包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f81ec-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="f81ec-150">`[SubscriptionId <String>]`：取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="f81ec-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f81ec-151">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="f81ec-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f81ec-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="f81ec-152">RELATED LINKS</span></span>

