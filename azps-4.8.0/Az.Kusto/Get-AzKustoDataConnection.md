---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDataConnection.md
ms.openlocfilehash: 6cfc5cdae87512245a573ed5c7ff9c746036c815
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971413"
---
# <span data-ttu-id="8a859-101">Get-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="8a859-101">Get-AzKustoDataConnection</span></span>

## <span data-ttu-id="8a859-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8a859-102">SYNOPSIS</span></span>
<span data-ttu-id="8a859-103">傳回資料連線。</span><span class="sxs-lookup"><span data-stu-id="8a859-103">Returns a data connection.</span></span>

## <span data-ttu-id="8a859-104">句法</span><span class="sxs-lookup"><span data-stu-id="8a859-104">SYNTAX</span></span>

### <span data-ttu-id="8a859-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="8a859-105">List (Default)</span></span>
```
Get-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8a859-106">獲取</span><span class="sxs-lookup"><span data-stu-id="8a859-106">Get</span></span>
```
Get-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8a859-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8a859-107">GetViaIdentity</span></span>
```
Get-AzKustoDataConnection -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8a859-108">說明</span><span class="sxs-lookup"><span data-stu-id="8a859-108">DESCRIPTION</span></span>
<span data-ttu-id="8a859-109">傳回資料連線。</span><span class="sxs-lookup"><span data-stu-id="8a859-109">Returns a data connection.</span></span>

## <span data-ttu-id="8a859-110">示例</span><span class="sxs-lookup"><span data-stu-id="8a859-110">EXAMPLES</span></span>

### <span data-ttu-id="8a859-111">範例1：列出特定資料庫中的所有資料連線</span><span class="sxs-lookup"><span data-stu-id="8a859-111">Example 1: List all data connections in a specific database</span></span>
```powershell
PS C:\> Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase"

Kind     Location Name                                               Type
----     -------- ----                                               ----
EventHub East US  testnewkustocluster/mykustodatabase/mykustodataconnection Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="8a859-112">上述命令會傳回在資源群組 "testrg" 中找到的 [testnewkustocluster] 群集中的所有 Kusto 資料庫。</span><span class="sxs-lookup"><span data-stu-id="8a859-112">The above command returns all Kusto databases in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="8a859-113">範例2：依名稱取得特定資料連線</span><span class="sxs-lookup"><span data-stu-id="8a859-113">Example 2: Get a specific data connection by name</span></span>
```powershell
PS C:\> Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "mykustodataconnection"

Kind     Location Name                                               Type
----     -------- ----                                               ----
EventHub East US  testnewkustocluster/mykustodatabase/mykustodataconnection Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="8a859-114">上述命令會傳回在資源群組 "testrg" 中找到現有群集 "testnewkustocluster" 的 [mykustodatabase] 資料連線（名為 "mykustodataconnection"）。</span><span class="sxs-lookup"><span data-stu-id="8a859-114">The above command returns the data connection named "mykustodataconnection" in database "mykustodatabase" of the existing cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="8a859-115">參數</span><span class="sxs-lookup"><span data-stu-id="8a859-115">PARAMETERS</span></span>

### <span data-ttu-id="8a859-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8a859-116">-ClusterName</span></span>
<span data-ttu-id="8a859-117">Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="8a859-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="8a859-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8a859-118">-DatabaseName</span></span>
<span data-ttu-id="8a859-119">Kusto 群集中之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="8a859-119">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="8a859-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a859-120">-DefaultProfile</span></span>
<span data-ttu-id="8a859-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8a859-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a859-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a859-122">-InputObject</span></span>
<span data-ttu-id="8a859-123">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="8a859-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8a859-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="8a859-124">-Name</span></span>
<span data-ttu-id="8a859-125">資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="8a859-125">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a859-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a859-126">-ResourceGroupName</span></span>
<span data-ttu-id="8a859-127">包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8a859-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="8a859-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8a859-128">-SubscriptionId</span></span>
<span data-ttu-id="8a859-129">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="8a859-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8a859-130">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="8a859-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8a859-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a859-131">CommonParameters</span></span>
<span data-ttu-id="8a859-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8a859-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a859-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8a859-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a859-134">輸入</span><span class="sxs-lookup"><span data-stu-id="8a859-134">INPUTS</span></span>

### <span data-ttu-id="8a859-135">IKustoIdentity （Kusto）的</span><span class="sxs-lookup"><span data-stu-id="8a859-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="8a859-136">輸出</span><span class="sxs-lookup"><span data-stu-id="8a859-136">OUTPUTS</span></span>

### <span data-ttu-id="8a859-137">IDataConnection （Kusto）。 Api20200614。</span><span class="sxs-lookup"><span data-stu-id="8a859-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDataConnection</span></span>

## <span data-ttu-id="8a859-138">筆記</span><span class="sxs-lookup"><span data-stu-id="8a859-138">NOTES</span></span>

<span data-ttu-id="8a859-139">別名</span><span class="sxs-lookup"><span data-stu-id="8a859-139">ALIASES</span></span>

<span data-ttu-id="8a859-140">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="8a859-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8a859-141">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="8a859-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8a859-142">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="8a859-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8a859-143">INPUTOBJECT <IKustoIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="8a859-143">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8a859-144">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="8a859-144">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="8a859-145">`[ClusterName <String>]`： Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="8a859-145">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="8a859-146">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="8a859-146">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="8a859-147">`[DatabaseName <String>]`： Kusto 群集中之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="8a859-147">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="8a859-148">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="8a859-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8a859-149">`[Location <String>]`： Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="8a859-149">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="8a859-150">`[PrincipalAssignmentName <String>]`： Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="8a859-150">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="8a859-151">`[ResourceGroupName <String>]`：包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8a859-151">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="8a859-152">`[SubscriptionId <String>]`：取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="8a859-152">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8a859-153">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="8a859-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="8a859-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="8a859-154">RELATED LINKS</span></span>

