---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: 753f2e4f2a1e2b60a12570307b518a5f2a78887b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905057"
---
# <span data-ttu-id="4b921-101">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="4b921-101">Get-AzKustoCluster</span></span>

## <span data-ttu-id="4b921-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4b921-102">SYNOPSIS</span></span>
<span data-ttu-id="4b921-103">獲得 Kusto 集區。</span><span class="sxs-lookup"><span data-stu-id="4b921-103">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="4b921-104">語法</span><span class="sxs-lookup"><span data-stu-id="4b921-104">SYNTAX</span></span>

### <span data-ttu-id="4b921-105">清單1 (預設) </span><span class="sxs-lookup"><span data-stu-id="4b921-105">List1 (Default)</span></span>
```
Get-AzKustoCluster [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4b921-106">獲取</span><span class="sxs-lookup"><span data-stu-id="4b921-106">Get</span></span>
```
Get-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4b921-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4b921-107">GetViaIdentity</span></span>
```
Get-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4b921-108">清單</span><span class="sxs-lookup"><span data-stu-id="4b921-108">List</span></span>
```
Get-AzKustoCluster -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="4b921-109">描述</span><span class="sxs-lookup"><span data-stu-id="4b921-109">DESCRIPTION</span></span>
<span data-ttu-id="4b921-110">獲得 Kusto 集區。</span><span class="sxs-lookup"><span data-stu-id="4b921-110">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="4b921-111">例子</span><span class="sxs-lookup"><span data-stu-id="4b921-111">EXAMPLES</span></span>

### <span data-ttu-id="4b921-112">範例 1：列出資源群組中所有的 Kusto 群組</span><span class="sxs-lookup"><span data-stu-id="4b921-112">Example 1: List all Kusto clusters in a resource group</span></span>
```powershell
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg

Location Name                 Type                     Zone
-------- ----                 ----                     ----
East US  testnewkustocluster  Microsoft.Kusto/Clusters
East US  testnewkustocluster2 Microsoft.Kusto/Clusters
```

<span data-ttu-id="4b921-113">上述命令會列出資源群組 "testrg" 中所有的 Kusto 群組。</span><span class="sxs-lookup"><span data-stu-id="4b921-113">The above command lists all Kusto clusters in the resource group "testrg".</span></span>

### <span data-ttu-id="4b921-114">範例 2：根據名稱取得特定的 Kusto cluster</span><span class="sxs-lookup"><span data-stu-id="4b921-114">Example 2: Get a specific Kusto cluster by name</span></span>
```powershell
PS C:\>  Get-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="4b921-115">上述命令會返回資源群組"testrg"中名為"testnewkustocluster"的 Kusto 叢集。</span><span class="sxs-lookup"><span data-stu-id="4b921-115">The above command returns the Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="4b921-116">參數</span><span class="sxs-lookup"><span data-stu-id="4b921-116">PARAMETERS</span></span>

### <span data-ttu-id="4b921-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b921-117">-DefaultProfile</span></span>
<span data-ttu-id="4b921-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4b921-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b921-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b921-119">-InputObject</span></span>
<span data-ttu-id="4b921-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="4b921-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4b921-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="4b921-121">-Name</span></span>
<span data-ttu-id="4b921-122">Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="4b921-122">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b921-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b921-123">-ResourceGroupName</span></span>
<span data-ttu-id="4b921-124">包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="4b921-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="4b921-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4b921-125">-SubscriptionId</span></span>
<span data-ttu-id="4b921-126">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="4b921-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4b921-127">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="4b921-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b921-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b921-128">CommonParameters</span></span>
<span data-ttu-id="4b921-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4b921-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b921-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4b921-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b921-131">輸入</span><span class="sxs-lookup"><span data-stu-id="4b921-131">INPUTS</span></span>

### <span data-ttu-id="4b921-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="4b921-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="4b921-133">輸出</span><span class="sxs-lookup"><span data-stu-id="4b921-133">OUTPUTS</span></span>

### <span data-ttu-id="4b921-134">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span><span class="sxs-lookup"><span data-stu-id="4b921-134">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span></span>

## <span data-ttu-id="4b921-135">筆記</span><span class="sxs-lookup"><span data-stu-id="4b921-135">NOTES</span></span>

<span data-ttu-id="4b921-136">別名</span><span class="sxs-lookup"><span data-stu-id="4b921-136">ALIASES</span></span>

<span data-ttu-id="4b921-137">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="4b921-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4b921-138">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="4b921-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4b921-139">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="4b921-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4b921-140">INPUTOBJECT： <IKustoIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="4b921-140">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4b921-141">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫組配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="4b921-141">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="4b921-142">`[ClusterName <String>]`：Kusto 組名。</span><span class="sxs-lookup"><span data-stu-id="4b921-142">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="4b921-143">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="4b921-143">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="4b921-144">`[DatabaseName <String>]`：Kusto cluster 中的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="4b921-144">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="4b921-145">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="4b921-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4b921-146">`[Location <String>]`：Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="4b921-146">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="4b921-147">`[PrincipalAssignmentName <String>]`：Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="4b921-147">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="4b921-148">`[ResourceGroupName <String>]`：包含 Kusto 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="4b921-148">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="4b921-149">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="4b921-149">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="4b921-150">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="4b921-150">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="4b921-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="4b921-151">RELATED LINKS</span></span>

