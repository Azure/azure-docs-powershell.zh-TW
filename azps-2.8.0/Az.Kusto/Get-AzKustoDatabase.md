---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoDatabase.md
ms.openlocfilehash: 98936051ba3faa06d611fc8509faaa2b26998d29
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612051"
---
# <span data-ttu-id="636cb-101">Get-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="636cb-101">Get-AzKustoDatabase</span></span>

## <span data-ttu-id="636cb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="636cb-102">SYNOPSIS</span></span>
<span data-ttu-id="636cb-103">列出群集中的所有 Kusto 資料庫，或取得特定的 Kusto 資料庫。</span><span class="sxs-lookup"><span data-stu-id="636cb-103">List all Kusto databases in a cluster or get a specific Kusto database.</span></span>

## <span data-ttu-id="636cb-104">句法</span><span class="sxs-lookup"><span data-stu-id="636cb-104">SYNTAX</span></span>

### <span data-ttu-id="636cb-105">ByClusterOrResourceGroupOrSubscription (預設) </span><span class="sxs-lookup"><span data-stu-id="636cb-105">ByClusterOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzKustoDatabase -ResourceGroupName <String> -ClusterName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="636cb-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="636cb-106">ByResourceId</span></span>
```
Get-AzKustoDatabase [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="636cb-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="636cb-107">ByInputObject</span></span>
```
Get-AzKustoDatabase [-Name <String>] -InputObject <PSKustoCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="636cb-108">說明</span><span class="sxs-lookup"><span data-stu-id="636cb-108">DESCRIPTION</span></span>
<span data-ttu-id="636cb-109">列出群集中的所有 Kusto 資料庫，或取得特定的 Kusto 資料庫。</span><span class="sxs-lookup"><span data-stu-id="636cb-109">List all Kusto databases in a cluster or get a specific Kusto database.</span></span>

## <span data-ttu-id="636cb-110">示例</span><span class="sxs-lookup"><span data-stu-id="636cb-110">EXAMPLES</span></span>

### <span data-ttu-id="636cb-111">範例 1-依名稱列出群集中的所有 Kusto 資料庫</span><span class="sxs-lookup"><span data-stu-id="636cb-111">Example 1 - List all Kusto databases in a cluster by name</span></span>

```
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster

Name                   : mykustocluster/mykustodatabase1
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase1
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases

Name                   : mykustocluster/mykustodatabase2
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase2
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="636cb-112">上述命令會傳回在資源群組 "testrg" 中找到的 [mykustocluster] 群集中的所有 Kusto 資料庫。</span><span class="sxs-lookup"><span data-stu-id="636cb-112">The above command returns all Kusto databases in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="636cb-113">範例 2-依管道列出群集中的所有 Kusto 資料庫</span><span class="sxs-lookup"><span data-stu-id="636cb-113">Example 2 - List all Kusto databases in a cluster by piping</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Get-AzKustoDatabase
Name                   : mykustocluster/mykustodatabase1
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase1
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases

Name                   : mykustocluster/mykustodatabase2
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase2
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="636cb-114">上述命令會在使用 Cmdlet 的資源群組 "testrg" 中，找到名為 "mykustocluster" 的 Kusto 群集 `Get-AzKustoCluster` ，並將結果輸送至 `Get-AzKustoDatabase` Cmdlet，以列出該群集中的所有資料庫。</span><span class="sxs-lookup"><span data-stu-id="636cb-114">The above command will get the Kusto cluster named "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and pipe the result to the `Get-AzKustoDatabase` cmdlet to list all databases in that cluster.</span></span>

### <span data-ttu-id="636cb-115">範例 3-依名稱取得特定的 Kusto 資料庫</span><span class="sxs-lookup"><span data-stu-id="636cb-115">Example 3 - Get a specific Kusto database by name</span></span>

```
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase

Name                   : mykustocluster/mykustodatabase
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="636cb-116">上述命令會傳回在資源群組 "testrg" 中找到的群集 "mykustocluster" 中名為 "mykustodatabase" 的 Kusto 資料庫。</span><span class="sxs-lookup"><span data-stu-id="636cb-116">The above command returns the Kusto database named "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="636cb-117">參數</span><span class="sxs-lookup"><span data-stu-id="636cb-117">PARAMETERS</span></span>

### <span data-ttu-id="636cb-118">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="636cb-118">-ClusterName</span></span>
<span data-ttu-id="636cb-119">資料庫所在之群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="636cb-119">Name of cluster under which the database exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByClusterOrResourceGroupOrSubscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="636cb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="636cb-120">-DefaultProfile</span></span>
<span data-ttu-id="636cb-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="636cb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="636cb-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="636cb-122">-InputObject</span></span>
<span data-ttu-id="636cb-123">Kusto [群集物件]。</span><span class="sxs-lookup"><span data-stu-id="636cb-123">Kusto cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="636cb-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="636cb-124">-Name</span></span>
<span data-ttu-id="636cb-125">資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="636cb-125">the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="636cb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="636cb-126">-ResourceGroupName</span></span>
<span data-ttu-id="636cb-127">使用者想要在其上取得群集的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="636cb-127">Name of resource group under which the user wants to retrieve the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByClusterOrResourceGroupOrSubscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="636cb-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="636cb-128">-ResourceId</span></span>
<span data-ttu-id="636cb-129">Kusto [群集 ResourceID]。</span><span class="sxs-lookup"><span data-stu-id="636cb-129">Kusto cluster ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="636cb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="636cb-130">CommonParameters</span></span>
<span data-ttu-id="636cb-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="636cb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="636cb-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="636cb-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="636cb-133">輸入</span><span class="sxs-lookup"><span data-stu-id="636cb-133">INPUTS</span></span>

### <span data-ttu-id="636cb-134">System.object</span><span class="sxs-lookup"><span data-stu-id="636cb-134">System.String</span></span>

### <span data-ttu-id="636cb-135">PSKustoCluster 中的 Kusto。</span><span class="sxs-lookup"><span data-stu-id="636cb-135">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="636cb-136">輸出</span><span class="sxs-lookup"><span data-stu-id="636cb-136">OUTPUTS</span></span>

### <span data-ttu-id="636cb-137">PSKustoDatabase 中的 Kusto。</span><span class="sxs-lookup"><span data-stu-id="636cb-137">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="636cb-138">筆記</span><span class="sxs-lookup"><span data-stu-id="636cb-138">NOTES</span></span>

## <span data-ttu-id="636cb-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="636cb-139">RELATED LINKS</span></span>
