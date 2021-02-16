---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: 5a5450629024dbca8433bee79bfe9d2fa7119025
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398031"
---
# <span data-ttu-id="d7d98-101">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="d7d98-101">Get-AzKustoCluster</span></span>

## <span data-ttu-id="d7d98-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d7d98-102">SYNOPSIS</span></span>
<span data-ttu-id="d7d98-103">列出資源群組中所有的 Kusto 群組，或取得特定的 Kusto 群組。</span><span class="sxs-lookup"><span data-stu-id="d7d98-103">List all Kusto clusters in a resource group or get a specific Kusto cluster.</span></span>

## <span data-ttu-id="d7d98-104">語法</span><span class="sxs-lookup"><span data-stu-id="d7d98-104">SYNTAX</span></span>

### <span data-ttu-id="d7d98-105">ByClusterOrResourceGroupOrSubscription (預設) </span><span class="sxs-lookup"><span data-stu-id="d7d98-105">ByClusterOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzKustoCluster -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d7d98-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d7d98-106">ByResourceId</span></span>
```
Get-AzKustoCluster -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7d98-107">描述</span><span class="sxs-lookup"><span data-stu-id="d7d98-107">DESCRIPTION</span></span>
<span data-ttu-id="d7d98-108">列出資源群組中所有的 Kusto 群組，或取得特定的 Kusto 群組。</span><span class="sxs-lookup"><span data-stu-id="d7d98-108">List all Kusto clusters in a resource group or get a specific Kusto cluster.</span></span>

## <span data-ttu-id="d7d98-109">例子</span><span class="sxs-lookup"><span data-stu-id="d7d98-109">EXAMPLES</span></span>

### <span data-ttu-id="d7d98-110">範例 1 - 列出資源群組中所有的 Kusto 群組</span><span class="sxs-lookup"><span data-stu-id="d7d98-110">Example 1 - List all Kusto clusters in a resource group</span></span>

<span data-ttu-id="d7d98-111">類型 ： Microsoft.Kusto/Clusters Id ： /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster1 ResourceGroup ： testrg Name ： mykustocluster1 Location ： Central US Capacity ： 3 SKU ： D13_v2 ProvisioningState ： Succeeded State ： Running Tag ： {} `https://mykustocluster1.centralus.kusto.windows.net` DataIngestionUri： `https://ingest-mykustocluster1.centralus.kusto.windows.net`</span><span class="sxs-lookup"><span data-stu-id="d7d98-111">Type              : Microsoft.Kusto/Clusters Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster1 ResourceGroup     : testrg Name              : mykustocluster1 Location          : Central US Capacity          : 3 Sku               : D13_v2 ProvisioningState : Succeeded State             : Running Tag               : {} Uri               : `https://mykustocluster1.centralus.kusto.windows.net` DataIngestionUri  : `https://ingest-mykustocluster1.centralus.kusto.windows.net`</span></span>

<span data-ttu-id="d7d98-112">類型 ： Microsoft.Kusto/Clusters Id ： /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster2 ResourceGroup ： testrg Name ： mykustocluster2 Location ： Central US Capacity ： 5 SKU ： D13_v2 ProvisioningState ： succeeded State ： Running Tag ： {} `https://mykustocluster2.centralus.kusto.windows.net` DataIngestionUri： `https://ingest-mykustocluster2.centralus.kusto.windows.net`</span><span class="sxs-lookup"><span data-stu-id="d7d98-112">Type              : Microsoft.Kusto/Clusters Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster2 ResourceGroup     : testrg Name              : mykustocluster2 Location          : Central US Capacity          : 5 Sku               : D13_v2 ProvisioningState : Succeeded State             : Running Tag               : {} Uri               : `https://mykustocluster2.centralus.kusto.windows.net` DataIngestionUri  : `https://ingest-mykustocluster2.centralus.kusto.windows.net`</span></span>


```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg
```

<span data-ttu-id="d7d98-113">上述命令會列出資源群組 "testrg" 中所有的 Kusto 群組。</span><span class="sxs-lookup"><span data-stu-id="d7d98-113">The above command lists all Kusto clusters in the resource group "testrg".</span></span>

### <span data-ttu-id="d7d98-114">範例 2 - 根據名稱取得特定的 Kusto 集區</span><span class="sxs-lookup"><span data-stu-id="d7d98-114">Example 2 - Get a specific Kusto cluster by name</span></span>

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

<span data-ttu-id="d7d98-115">上述命令會返回資源群組 "testrg" 中名為 "mykustocluster" 的 Kusto 叢集。</span><span class="sxs-lookup"><span data-stu-id="d7d98-115">The above command returns the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

### <span data-ttu-id="d7d98-116">範例 3 - 根據資源識別碼取得特定的 Kusto 組</span><span class="sxs-lookup"><span data-stu-id="d7d98-116">Example 3 - Get a specific Kusto cluster by resource id</span></span>

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

<span data-ttu-id="d7d98-117">上述命令會返回資源群組 "testrg" 中名為 "mykustocluster" 的 Kusto 叢集。</span><span class="sxs-lookup"><span data-stu-id="d7d98-117">The above command returns the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="d7d98-118">參數</span><span class="sxs-lookup"><span data-stu-id="d7d98-118">PARAMETERS</span></span>

### <span data-ttu-id="d7d98-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7d98-119">-DefaultProfile</span></span>
<span data-ttu-id="d7d98-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d7d98-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7d98-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="d7d98-121">-Name</span></span>
<span data-ttu-id="d7d98-122">特定組名。</span><span class="sxs-lookup"><span data-stu-id="d7d98-122">Name of a specific cluster.</span></span>

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

### <span data-ttu-id="d7d98-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7d98-123">-ResourceGroupName</span></span>
<span data-ttu-id="d7d98-124">使用者想要在資源群組中取回群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="d7d98-124">Name of resource group under which the user wants to retrieve the cluster.</span></span>

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

### <span data-ttu-id="d7d98-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7d98-125">-ResourceId</span></span>
<span data-ttu-id="d7d98-126">Kusto cluster ResourceID.</span><span class="sxs-lookup"><span data-stu-id="d7d98-126">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="d7d98-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7d98-127">CommonParameters</span></span>
<span data-ttu-id="d7d98-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d7d98-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7d98-129">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="d7d98-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7d98-130">輸入</span><span class="sxs-lookup"><span data-stu-id="d7d98-130">INPUTS</span></span>

### <span data-ttu-id="d7d98-131">System.String</span><span class="sxs-lookup"><span data-stu-id="d7d98-131">System.String</span></span>

## <span data-ttu-id="d7d98-132">輸出</span><span class="sxs-lookup"><span data-stu-id="d7d98-132">OUTPUTS</span></span>

### <span data-ttu-id="d7d98-133">Microsoft.Azure.Commands.Kusto.models.PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="d7d98-133">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="d7d98-134">筆記</span><span class="sxs-lookup"><span data-stu-id="d7d98-134">NOTES</span></span>

## <span data-ttu-id="d7d98-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="d7d98-135">RELATED LINKS</span></span>
