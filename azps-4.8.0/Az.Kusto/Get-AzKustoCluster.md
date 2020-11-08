---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: a95f8a00578ccf917a55cdfd9685dedf9a20734f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127640"
---
# <span data-ttu-id="5ce0e-101">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="5ce0e-101">Get-AzKustoCluster</span></span>

## <span data-ttu-id="5ce0e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5ce0e-102">SYNOPSIS</span></span>
<span data-ttu-id="5ce0e-103">取得 Kusto 群集。</span><span class="sxs-lookup"><span data-stu-id="5ce0e-103">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="5ce0e-104">句法</span><span class="sxs-lookup"><span data-stu-id="5ce0e-104">SYNTAX</span></span>

### <span data-ttu-id="5ce0e-105">List1 (預設) </span><span class="sxs-lookup"><span data-stu-id="5ce0e-105">List1 (Default)</span></span>
```
Get-AzKustoCluster [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5ce0e-106">獲取</span><span class="sxs-lookup"><span data-stu-id="5ce0e-106">Get</span></span>
```
Get-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5ce0e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5ce0e-107">GetViaIdentity</span></span>
```
Get-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5ce0e-108">清單</span><span class="sxs-lookup"><span data-stu-id="5ce0e-108">List</span></span>
```
Get-AzKustoCluster -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="5ce0e-109">說明</span><span class="sxs-lookup"><span data-stu-id="5ce0e-109">DESCRIPTION</span></span>
<span data-ttu-id="5ce0e-110">取得 Kusto 群集。</span><span class="sxs-lookup"><span data-stu-id="5ce0e-110">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="5ce0e-111">示例</span><span class="sxs-lookup"><span data-stu-id="5ce0e-111">EXAMPLES</span></span>

### <span data-ttu-id="5ce0e-112">範例1：列出資源群組中的所有 Kusto 群集</span><span class="sxs-lookup"><span data-stu-id="5ce0e-112">Example 1: List all Kusto clusters in a resource group</span></span>
```powershell
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg

Location Name                 Type                     Zone
-------- ----                 ----                     ----
East US  testnewkustocluster  Microsoft.Kusto/Clusters
East US  testnewkustocluster2 Microsoft.Kusto/Clusters
```

<span data-ttu-id="5ce0e-113">上述命令會列出 [資源] 群組中的所有 Kusto 群集 [testrg]。</span><span class="sxs-lookup"><span data-stu-id="5ce0e-113">The above command lists all Kusto clusters in the resource group "testrg".</span></span>

### <span data-ttu-id="5ce0e-114">範例2：依名稱取得特定的 Kusto 群集</span><span class="sxs-lookup"><span data-stu-id="5ce0e-114">Example 2: Get a specific Kusto cluster by name</span></span>
```powershell
PS C:\>  Get-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="5ce0e-115">上述命令會傳回資源群組 "testrg" 中名為 "testnewkustocluster" 的 Kusto 群集。</span><span class="sxs-lookup"><span data-stu-id="5ce0e-115">The above command returns the Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="5ce0e-116">參數</span><span class="sxs-lookup"><span data-stu-id="5ce0e-116">PARAMETERS</span></span>

### <span data-ttu-id="5ce0e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ce0e-117">-DefaultProfile</span></span>
<span data-ttu-id="5ce0e-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5ce0e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ce0e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ce0e-119">-InputObject</span></span>
<span data-ttu-id="5ce0e-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="5ce0e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5ce0e-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="5ce0e-121">-Name</span></span>
<span data-ttu-id="5ce0e-122">Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ce0e-122">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="5ce0e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ce0e-123">-ResourceGroupName</span></span>
<span data-ttu-id="5ce0e-124">包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ce0e-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="5ce0e-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5ce0e-125">-SubscriptionId</span></span>
<span data-ttu-id="5ce0e-126">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="5ce0e-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5ce0e-127">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="5ce0e-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5ce0e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ce0e-128">CommonParameters</span></span>
<span data-ttu-id="5ce0e-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5ce0e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ce0e-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5ce0e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ce0e-131">輸入</span><span class="sxs-lookup"><span data-stu-id="5ce0e-131">INPUTS</span></span>

### <span data-ttu-id="5ce0e-132">IKustoIdentity （Kusto）的</span><span class="sxs-lookup"><span data-stu-id="5ce0e-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="5ce0e-133">輸出</span><span class="sxs-lookup"><span data-stu-id="5ce0e-133">OUTPUTS</span></span>

### <span data-ttu-id="5ce0e-134">ICluster （Kusto）。 Api20200614。</span><span class="sxs-lookup"><span data-stu-id="5ce0e-134">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span></span>

## <span data-ttu-id="5ce0e-135">筆記</span><span class="sxs-lookup"><span data-stu-id="5ce0e-135">NOTES</span></span>

<span data-ttu-id="5ce0e-136">別名</span><span class="sxs-lookup"><span data-stu-id="5ce0e-136">ALIASES</span></span>

<span data-ttu-id="5ce0e-137">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="5ce0e-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5ce0e-138">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="5ce0e-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5ce0e-139">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="5ce0e-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5ce0e-140">INPUTOBJECT <IKustoIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="5ce0e-140">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5ce0e-141">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ce0e-141">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="5ce0e-142">`[ClusterName <String>]`： Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ce0e-142">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="5ce0e-143">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ce0e-143">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="5ce0e-144">`[DatabaseName <String>]`： Kusto 群集中之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ce0e-144">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="5ce0e-145">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="5ce0e-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5ce0e-146">`[Location <String>]`： Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="5ce0e-146">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="5ce0e-147">`[PrincipalAssignmentName <String>]`： Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ce0e-147">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="5ce0e-148">`[ResourceGroupName <String>]`：包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ce0e-148">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="5ce0e-149">`[SubscriptionId <String>]`：取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="5ce0e-149">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="5ce0e-150">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="5ce0e-150">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="5ce0e-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="5ce0e-151">RELATED LINKS</span></span>

