---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabase.md
ms.openlocfilehash: a39578ffb7a0f3a5ecc6abc873f659b5d170aff5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131634"
---
# <span data-ttu-id="812e6-101">Get-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="812e6-101">Get-AzKustoDatabase</span></span>

## <span data-ttu-id="812e6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="812e6-102">SYNOPSIS</span></span>
<span data-ttu-id="812e6-103">傳回資料庫。</span><span class="sxs-lookup"><span data-stu-id="812e6-103">Returns a database.</span></span>

## <span data-ttu-id="812e6-104">句法</span><span class="sxs-lookup"><span data-stu-id="812e6-104">SYNTAX</span></span>

### <span data-ttu-id="812e6-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="812e6-105">List (Default)</span></span>
```
Get-AzKustoDatabase -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="812e6-106">獲取</span><span class="sxs-lookup"><span data-stu-id="812e6-106">Get</span></span>
```
Get-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="812e6-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="812e6-107">GetViaIdentity</span></span>
```
Get-AzKustoDatabase -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="812e6-108">說明</span><span class="sxs-lookup"><span data-stu-id="812e6-108">DESCRIPTION</span></span>
<span data-ttu-id="812e6-109">傳回資料庫。</span><span class="sxs-lookup"><span data-stu-id="812e6-109">Returns a database.</span></span>

## <span data-ttu-id="812e6-110">示例</span><span class="sxs-lookup"><span data-stu-id="812e6-110">EXAMPLES</span></span>

### <span data-ttu-id="812e6-111">範例1：依名稱列出群集中的所有 Kusto 資料庫</span><span class="sxs-lookup"><span data-stu-id="812e6-111">Example 1: List all Kusto databases in a cluster by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster

Kind      Location Name                                 Type
----      -------- ----                                 ----
ReadWrite East US  testnewkustocluster/mykustodatabase  Microsoft.Kusto/Clusters/Databases
ReadWrite East US  testnewkustocluster/mykustodatabase2 Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="812e6-112">上述命令會傳回在資源群組 "testrg" 中找到的 [testnewkustocluster] 群集中的所有 Kusto 資料庫。</span><span class="sxs-lookup"><span data-stu-id="812e6-112">The above command returns all Kusto databases in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="812e6-113">範例2：依名稱取得特定的 Kusto 資料庫</span><span class="sxs-lookup"><span data-stu-id="812e6-113">Example 2: Get a specific Kusto database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="812e6-114">上述命令會傳回在資源群組 "testrg" 中找到的群集 "testnewkustocluster" 中名為 "mykustodatabase" 的 Kusto 資料庫。</span><span class="sxs-lookup"><span data-stu-id="812e6-114">The above command returns the Kusto database named "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="812e6-115">參數</span><span class="sxs-lookup"><span data-stu-id="812e6-115">PARAMETERS</span></span>

### <span data-ttu-id="812e6-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="812e6-116">-ClusterName</span></span>
<span data-ttu-id="812e6-117">Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="812e6-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="812e6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="812e6-118">-DefaultProfile</span></span>
<span data-ttu-id="812e6-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="812e6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="812e6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="812e6-120">-InputObject</span></span>
<span data-ttu-id="812e6-121">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="812e6-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="812e6-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="812e6-122">-Name</span></span>
<span data-ttu-id="812e6-123">Kusto 群集中之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="812e6-123">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="812e6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="812e6-124">-ResourceGroupName</span></span>
<span data-ttu-id="812e6-125">包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="812e6-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="812e6-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="812e6-126">-SubscriptionId</span></span>
<span data-ttu-id="812e6-127">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="812e6-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="812e6-128">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="812e6-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="812e6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="812e6-129">CommonParameters</span></span>
<span data-ttu-id="812e6-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="812e6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="812e6-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="812e6-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="812e6-132">輸入</span><span class="sxs-lookup"><span data-stu-id="812e6-132">INPUTS</span></span>

### <span data-ttu-id="812e6-133">IKustoIdentity （Kusto）的</span><span class="sxs-lookup"><span data-stu-id="812e6-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="812e6-134">輸出</span><span class="sxs-lookup"><span data-stu-id="812e6-134">OUTPUTS</span></span>

### <span data-ttu-id="812e6-135">IDatabase （Kusto）。 Api20200918。</span><span class="sxs-lookup"><span data-stu-id="812e6-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span></span>

## <span data-ttu-id="812e6-136">筆記</span><span class="sxs-lookup"><span data-stu-id="812e6-136">NOTES</span></span>

<span data-ttu-id="812e6-137">別名</span><span class="sxs-lookup"><span data-stu-id="812e6-137">ALIASES</span></span>

<span data-ttu-id="812e6-138">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="812e6-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="812e6-139">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="812e6-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="812e6-140">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="812e6-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="812e6-141">INPUTOBJECT <IKustoIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="812e6-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="812e6-142">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="812e6-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="812e6-143">`[ClusterName <String>]`： Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="812e6-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="812e6-144">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="812e6-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="812e6-145">`[DatabaseName <String>]`： Kusto 群集中之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="812e6-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="812e6-146">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="812e6-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="812e6-147">`[Location <String>]`： Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="812e6-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="812e6-148">`[PrincipalAssignmentName <String>]`： Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="812e6-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="812e6-149">`[ResourceGroupName <String>]`：包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="812e6-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="812e6-150">`[SubscriptionId <String>]`：取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="812e6-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="812e6-151">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="812e6-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="812e6-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="812e6-152">RELATED LINKS</span></span>

