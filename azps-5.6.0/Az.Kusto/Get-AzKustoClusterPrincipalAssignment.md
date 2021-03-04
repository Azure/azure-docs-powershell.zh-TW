---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/get-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: b89327f80ec5f8e0f5faf9f66e943ee07601799e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905042"
---
# <span data-ttu-id="32a15-101">Get-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="32a15-101">Get-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="32a15-102">簡介</span><span class="sxs-lookup"><span data-stu-id="32a15-102">SYNOPSIS</span></span>
<span data-ttu-id="32a15-103">獲得 Kusto cluster principalAssignment。</span><span class="sxs-lookup"><span data-stu-id="32a15-103">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="32a15-104">語法</span><span class="sxs-lookup"><span data-stu-id="32a15-104">SYNTAX</span></span>

### <span data-ttu-id="32a15-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="32a15-105">List (Default)</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="32a15-106">獲取</span><span class="sxs-lookup"><span data-stu-id="32a15-106">Get</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="32a15-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="32a15-107">GetViaIdentity</span></span>
```
Get-AzKustoClusterPrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="32a15-108">描述</span><span class="sxs-lookup"><span data-stu-id="32a15-108">DESCRIPTION</span></span>
<span data-ttu-id="32a15-109">獲得 Kusto cluster principalAssignment。</span><span class="sxs-lookup"><span data-stu-id="32a15-109">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="32a15-110">例子</span><span class="sxs-lookup"><span data-stu-id="32a15-110">EXAMPLES</span></span>

### <span data-ttu-id="32a15-111">範例 1：列出所有 Kusto cluster principalAssignment</span><span class="sxs-lookup"><span data-stu-id="32a15-111">Example 1: List all Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="32a15-112">上述命令會列出叢集中 「testnewkustocluster」中所有主體的Assignment。</span><span class="sxs-lookup"><span data-stu-id="32a15-112">The above command lists all principalAssignment in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="32a15-113">範例 2：根據名稱獲得 Kusto cluster principalAssignment</span><span class="sxs-lookup"><span data-stu-id="32a15-113">Example 2: Gets a Kusto cluster principalAssignment by name</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="32a15-114">上述命令會返回名為 "testnewkustocluster" 叢集中"kustoprincipal1" 的 Kusto 叢集主體Assignment。</span><span class="sxs-lookup"><span data-stu-id="32a15-114">The above command returns the Kusto cluster principalAssignment named "kustoprincipal1" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="32a15-115">參數</span><span class="sxs-lookup"><span data-stu-id="32a15-115">PARAMETERS</span></span>

### <span data-ttu-id="32a15-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="32a15-116">-ClusterName</span></span>
<span data-ttu-id="32a15-117">Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="32a15-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="32a15-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32a15-118">-DefaultProfile</span></span>
<span data-ttu-id="32a15-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="32a15-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32a15-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="32a15-120">-InputObject</span></span>
<span data-ttu-id="32a15-121">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="32a15-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="32a15-122">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="32a15-122">-PrincipalAssignmentName</span></span>
<span data-ttu-id="32a15-123">Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="32a15-123">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="32a15-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32a15-124">-ResourceGroupName</span></span>
<span data-ttu-id="32a15-125">包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="32a15-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="32a15-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="32a15-126">-SubscriptionId</span></span>
<span data-ttu-id="32a15-127">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="32a15-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="32a15-128">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="32a15-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="32a15-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32a15-129">CommonParameters</span></span>
<span data-ttu-id="32a15-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="32a15-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32a15-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="32a15-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32a15-132">輸入</span><span class="sxs-lookup"><span data-stu-id="32a15-132">INPUTS</span></span>

### <span data-ttu-id="32a15-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="32a15-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="32a15-134">輸出</span><span class="sxs-lookup"><span data-stu-id="32a15-134">OUTPUTS</span></span>

### <span data-ttu-id="32a15-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.models.Api20200918.IClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="32a15-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="32a15-136">筆記</span><span class="sxs-lookup"><span data-stu-id="32a15-136">NOTES</span></span>

<span data-ttu-id="32a15-137">別名</span><span class="sxs-lookup"><span data-stu-id="32a15-137">ALIASES</span></span>

<span data-ttu-id="32a15-138">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="32a15-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="32a15-139">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="32a15-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="32a15-140">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="32a15-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="32a15-141">INPUTOBJECT： <IKustoIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="32a15-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="32a15-142">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫組配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="32a15-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="32a15-143">`[ClusterName <String>]`：Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="32a15-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="32a15-144">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="32a15-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="32a15-145">`[DatabaseName <String>]`：Kusto cluster 中的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="32a15-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="32a15-146">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="32a15-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="32a15-147">`[Location <String>]`：Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="32a15-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="32a15-148">`[PrincipalAssignmentName <String>]`：Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="32a15-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="32a15-149">`[ResourceGroupName <String>]`：包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="32a15-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="32a15-150">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="32a15-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="32a15-151">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="32a15-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="32a15-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="32a15-152">RELATED LINKS</span></span>

