---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: a68604e9701a6ae2c251edf3f2a0935df5ffa94f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787234"
---
# <span data-ttu-id="e3583-101">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="e3583-101">Get-AzKustoCluster</span></span>

## <span data-ttu-id="e3583-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e3583-102">SYNOPSIS</span></span>
<span data-ttu-id="e3583-103">列出資源群組中的所有 Kusto 群集，或取得特定的 Kusto 群集。</span><span class="sxs-lookup"><span data-stu-id="e3583-103">List all Kusto clusters in a resource group or get a specific Kusto cluster.</span></span>

## <span data-ttu-id="e3583-104">句法</span><span class="sxs-lookup"><span data-stu-id="e3583-104">SYNTAX</span></span>

### <span data-ttu-id="e3583-105">ByClusterOrResourceGroupOrSubscription (預設) </span><span class="sxs-lookup"><span data-stu-id="e3583-105">ByClusterOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzKustoCluster -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3583-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e3583-106">ByResourceId</span></span>
```
Get-AzKustoCluster -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3583-107">說明</span><span class="sxs-lookup"><span data-stu-id="e3583-107">DESCRIPTION</span></span>
<span data-ttu-id="e3583-108">列出資源群組中的所有 Kusto 群集，或取得特定的 Kusto 群集。</span><span class="sxs-lookup"><span data-stu-id="e3583-108">List all Kusto clusters in a resource group or get a specific Kusto cluster.</span></span>

## <span data-ttu-id="e3583-109">示例</span><span class="sxs-lookup"><span data-stu-id="e3583-109">EXAMPLES</span></span>

### <span data-ttu-id="e3583-110">範例 1-列出資源群組中的所有 Kusto 群集</span><span class="sxs-lookup"><span data-stu-id="e3583-110">Example 1 - List all Kusto clusters in a resource group</span></span>

<span data-ttu-id="e3583-111">類型： Kusto/群集 Id：/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster1 ResourceGroup： testrg 名稱： mykustocluster1 位置：中美式容量： 3 Sku： D13_v2 ProvisioningState： Succeeded 狀態：執行標記： {} Uri： https://mykustocluster1.centralus.kusto.windows.net DataIngestionUri： https://ingest-mykustocluster1.centralus.kusto.windows.net</span><span class="sxs-lookup"><span data-stu-id="e3583-111">Type              : Microsoft.Kusto/Clusters Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster1 ResourceGroup     : testrg Name              : mykustocluster1 Location          : Central US Capacity          : 3 Sku               : D13_v2 ProvisioningState : Succeeded State             : Running Tag               : {} Uri               : https://mykustocluster1.centralus.kusto.windows.net DataIngestionUri  : https://ingest-mykustocluster1.centralus.kusto.windows.net</span></span>

<span data-ttu-id="e3583-112">類型： Kusto/群集 Id：/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster2 ResourceGroup： testrg 名稱： mykustocluster2 位置：中美式容量： 5 Sku： D13_v2 ProvisioningState： Succeeded 狀態：執行標記： {} Uri： https://mykustocluster2.centralus.kusto.windows.net DataIngestionUri： https://ingest-mykustocluster2.centralus.kusto.windows.net</span><span class="sxs-lookup"><span data-stu-id="e3583-112">Type              : Microsoft.Kusto/Clusters Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster2 ResourceGroup     : testrg Name              : mykustocluster2 Location          : Central US Capacity          : 5 Sku               : D13_v2 ProvisioningState : Succeeded State             : Running Tag               : {} Uri               : https://mykustocluster2.centralus.kusto.windows.net DataIngestionUri  : https://ingest-mykustocluster2.centralus.kusto.windows.net</span></span>


```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg
```

<span data-ttu-id="e3583-113">上述命令會列出 [資源] 群組中的所有 Kusto 群集 [testrg]。</span><span class="sxs-lookup"><span data-stu-id="e3583-113">The above command lists all Kusto clusters in the resource group "testrg".</span></span>

### <span data-ttu-id="e3583-114">範例 2-依名稱取得特定的 Kusto 群集</span><span class="sxs-lookup"><span data-stu-id="e3583-114">Example 2 - Get a specific Kusto cluster by name</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster

Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 5
Sku               : D13_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster.centralus.kusto.windows.net
```

<span data-ttu-id="e3583-115">上述命令會傳回資源群組 "testrg" 中名為 "mykustocluster" 的 Kusto 群集。</span><span class="sxs-lookup"><span data-stu-id="e3583-115">The above command returns the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

### <span data-ttu-id="e3583-116">範例 3-依資源識別碼取得特定的 Kusto 群集</span><span class="sxs-lookup"><span data-stu-id="e3583-116">Example 3 - Get a specific Kusto cluster by resource id</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceId /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/clusters/mykustocluster
Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 5
Sku               : D13_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster.centralus.kusto.windows.net
```

<span data-ttu-id="e3583-117">上述命令會傳回資源群組 "testrg" 中名為 "mykustocluster" 的 Kusto 群集。</span><span class="sxs-lookup"><span data-stu-id="e3583-117">The above command returns the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="e3583-118">參數</span><span class="sxs-lookup"><span data-stu-id="e3583-118">PARAMETERS</span></span>

### <span data-ttu-id="e3583-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3583-119">-DefaultProfile</span></span>
<span data-ttu-id="e3583-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e3583-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3583-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="e3583-121">-Name</span></span>
<span data-ttu-id="e3583-122">特定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3583-122">Name of a specific cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByClusterOrResourceGroupOrSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3583-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3583-123">-ResourceGroupName</span></span>
<span data-ttu-id="e3583-124">使用者想要在其上取得群集的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3583-124">Name of resource group under which the user wants to retrieve the cluster.</span></span>

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

### <span data-ttu-id="e3583-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3583-125">-ResourceId</span></span>
<span data-ttu-id="e3583-126">Kusto [群集 ResourceID]。</span><span class="sxs-lookup"><span data-stu-id="e3583-126">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="e3583-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3583-127">CommonParameters</span></span>
<span data-ttu-id="e3583-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e3583-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3583-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e3583-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3583-130">輸入</span><span class="sxs-lookup"><span data-stu-id="e3583-130">INPUTS</span></span>

### <span data-ttu-id="e3583-131">System.object</span><span class="sxs-lookup"><span data-stu-id="e3583-131">System.String</span></span>

## <span data-ttu-id="e3583-132">輸出</span><span class="sxs-lookup"><span data-stu-id="e3583-132">OUTPUTS</span></span>

### <span data-ttu-id="e3583-133">PSKustoCluster 中的 Kusto。</span><span class="sxs-lookup"><span data-stu-id="e3583-133">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="e3583-134">筆記</span><span class="sxs-lookup"><span data-stu-id="e3583-134">NOTES</span></span>

## <span data-ttu-id="e3583-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3583-135">RELATED LINKS</span></span>
