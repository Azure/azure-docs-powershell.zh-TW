---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: fd735b1d343c046f9ca2f0528bff4bf7ce8a403d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127639"
---
# <span data-ttu-id="b1a9c-101">Get-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="b1a9c-101">Get-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="b1a9c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b1a9c-102">SYNOPSIS</span></span>
<span data-ttu-id="b1a9c-103">傳回已附加的資料庫設定。</span><span class="sxs-lookup"><span data-stu-id="b1a9c-103">Returns an attached database configuration.</span></span>

## <span data-ttu-id="b1a9c-104">句法</span><span class="sxs-lookup"><span data-stu-id="b1a9c-104">SYNTAX</span></span>

### <span data-ttu-id="b1a9c-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="b1a9c-105">List (Default)</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b1a9c-106">獲取</span><span class="sxs-lookup"><span data-stu-id="b1a9c-106">Get</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b1a9c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b1a9c-107">GetViaIdentity</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b1a9c-108">說明</span><span class="sxs-lookup"><span data-stu-id="b1a9c-108">DESCRIPTION</span></span>
<span data-ttu-id="b1a9c-109">傳回已附加的資料庫設定。</span><span class="sxs-lookup"><span data-stu-id="b1a9c-109">Returns an attached database configuration.</span></span>

## <span data-ttu-id="b1a9c-110">示例</span><span class="sxs-lookup"><span data-stu-id="b1a9c-110">EXAMPLES</span></span>

### <span data-ttu-id="b1a9c-111">範例1：列出群集中的所有 AttachedDatabaseConfigurations</span><span class="sxs-lookup"><span data-stu-id="b1a9c-111">Example 1: List all the AttachedDatabaseConfigurations in a cluster</span></span>
```powershell
PS C:\> Get-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf"

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="b1a9c-112">上述命令會列出 [testnewkustoclusterf] 群集中的所有 AttachedDatabaseConfigurations。</span><span class="sxs-lookup"><span data-stu-id="b1a9c-112">The above command lists all the AttachedDatabaseConfigurations in the cluster "testnewkustoclusterf".</span></span>

### <span data-ttu-id="b1a9c-113">範例2：在群集中取得特定 AttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="b1a9c-113">Example 2: Get a specific AttachedDatabaseConfiguration in a cluster</span></span>
```powershell
PS C:\>  Get-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration" 

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="b1a9c-114">上述命令會傳回群集 "testnewkustoclusterf" 中名為 "myfollowerconfiguration" 的 AttachedDatabaseConfigurations。</span><span class="sxs-lookup"><span data-stu-id="b1a9c-114">The above command returns the AttachedDatabaseConfigurations named "myfollowerconfiguration" in the cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="b1a9c-115">參數</span><span class="sxs-lookup"><span data-stu-id="b1a9c-115">PARAMETERS</span></span>

### <span data-ttu-id="b1a9c-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b1a9c-116">-ClusterName</span></span>
<span data-ttu-id="b1a9c-117">Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1a9c-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="b1a9c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1a9c-118">-DefaultProfile</span></span>
<span data-ttu-id="b1a9c-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b1a9c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1a9c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1a9c-120">-InputObject</span></span>
<span data-ttu-id="b1a9c-121">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b1a9c-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b1a9c-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="b1a9c-122">-Name</span></span>
<span data-ttu-id="b1a9c-123">已附加資料庫配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1a9c-123">The name of the attached database configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AttachedDatabaseConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1a9c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1a9c-124">-ResourceGroupName</span></span>
<span data-ttu-id="b1a9c-125">包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1a9c-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="b1a9c-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b1a9c-126">-SubscriptionId</span></span>
<span data-ttu-id="b1a9c-127">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="b1a9c-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b1a9c-128">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="b1a9c-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b1a9c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1a9c-129">CommonParameters</span></span>
<span data-ttu-id="b1a9c-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b1a9c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1a9c-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b1a9c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1a9c-132">輸入</span><span class="sxs-lookup"><span data-stu-id="b1a9c-132">INPUTS</span></span>

### <span data-ttu-id="b1a9c-133">IKustoIdentity （Kusto）的</span><span class="sxs-lookup"><span data-stu-id="b1a9c-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="b1a9c-134">輸出</span><span class="sxs-lookup"><span data-stu-id="b1a9c-134">OUTPUTS</span></span>

### <span data-ttu-id="b1a9c-135">IAttachedDatabaseConfiguration （Kusto）。 Api20200614。</span><span class="sxs-lookup"><span data-stu-id="b1a9c-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="b1a9c-136">筆記</span><span class="sxs-lookup"><span data-stu-id="b1a9c-136">NOTES</span></span>

<span data-ttu-id="b1a9c-137">別名</span><span class="sxs-lookup"><span data-stu-id="b1a9c-137">ALIASES</span></span>

<span data-ttu-id="b1a9c-138">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="b1a9c-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b1a9c-139">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="b1a9c-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b1a9c-140">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="b1a9c-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b1a9c-141">INPUTOBJECT <IKustoIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="b1a9c-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b1a9c-142">`[AttachedDatabaseConfigurationName <String>]`：附加資料庫配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1a9c-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="b1a9c-143">`[ClusterName <String>]`： Kusto 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1a9c-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="b1a9c-144">`[DataConnectionName <String>]`：資料連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1a9c-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="b1a9c-145">`[DatabaseName <String>]`： Kusto 群集中之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1a9c-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="b1a9c-146">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="b1a9c-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b1a9c-147">`[Location <String>]`： Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="b1a9c-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="b1a9c-148">`[PrincipalAssignmentName <String>]`： Kusto principalAssignment 的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1a9c-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="b1a9c-149">`[ResourceGroupName <String>]`：包含 Kusto 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1a9c-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="b1a9c-150">`[SubscriptionId <String>]`：取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="b1a9c-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b1a9c-151">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="b1a9c-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b1a9c-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="b1a9c-152">RELATED LINKS</span></span>

