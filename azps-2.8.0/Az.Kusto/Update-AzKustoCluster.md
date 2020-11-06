---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Update-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Update-AzKustoCluster.md
ms.openlocfilehash: 890ec07cecd46badaccc1c2140290fd8042d319b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612038"
---
# <span data-ttu-id="4199a-101">Update-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="4199a-101">Update-AzKustoCluster</span></span>

## <span data-ttu-id="4199a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4199a-102">SYNOPSIS</span></span>
<span data-ttu-id="4199a-103">更新現有的 Kusto 群集。</span><span class="sxs-lookup"><span data-stu-id="4199a-103">Update an existing Kusto cluster.</span></span>

## <span data-ttu-id="4199a-104">句法</span><span class="sxs-lookup"><span data-stu-id="4199a-104">SYNTAX</span></span>

### <span data-ttu-id="4199a-105">ByNameAndResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="4199a-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzKustoCluster [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>] [-Capacity <Int32>]
 [-Tier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4199a-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4199a-106">ByResourceId</span></span>
```
Update-AzKustoCluster [-SkuName <String>] [-Capacity <Int32>] [-Tier <String>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4199a-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4199a-107">ByInputObject</span></span>
```
Update-AzKustoCluster [-SkuName <String>] [-Capacity <Int32>] [-Tier <String>] [-InputObject] <PSKustoCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4199a-108">說明</span><span class="sxs-lookup"><span data-stu-id="4199a-108">DESCRIPTION</span></span>
<span data-ttu-id="4199a-109">更新現有的 Kusto 群集。</span><span class="sxs-lookup"><span data-stu-id="4199a-109">Update an existing Kusto cluster.</span></span>

## <span data-ttu-id="4199a-110">示例</span><span class="sxs-lookup"><span data-stu-id="4199a-110">EXAMPLES</span></span>

### <span data-ttu-id="4199a-111">範例 1-依名稱更新現有的群集</span><span class="sxs-lookup"><span data-stu-id="4199a-111">Example 1 - Update an existing cluster by name</span></span>

```
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster -Sku D14_v2

Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Sku               : D14_v2
Capacity          : 5
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster1.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster1.centralus.kusto.windows.net
```

<span data-ttu-id="4199a-112">上述命令會更新在資源群組 "testrg" 中找到的 Kusto 群集 "mykustocluster" 的層級。</span><span class="sxs-lookup"><span data-stu-id="4199a-112">The above command updates the tier of the Kusto cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="4199a-113">範例 2-依管道更新現有的群集</span><span class="sxs-lookup"><span data-stu-id="4199a-113">Example 2 - Update an existing cluster by piping</span></span>

```
PS C:\> PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Update-AzKustoCluster -Sku D14_v2 -Capacity 10

Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 10
Sku               : D14_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster1.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster1.centralus.kusto.windows.net
```

<span data-ttu-id="4199a-114">上述命令會取得使用 Cmdlet 在資源群組 "testrg" 中找到的 Kusto 群集 "mykustocluster" `Get-AzKustoCluster` ，然後將結果管道 `Update-AzKustoCluster` 更新為 "標準"。</span><span class="sxs-lookup"><span data-stu-id="4199a-114">The above command gets the Kusto cluster "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and then pipes the result to `Update-AzKustoCluster` to update the cluster's tier to "standard".</span></span>

## <span data-ttu-id="4199a-115">參數</span><span class="sxs-lookup"><span data-stu-id="4199a-115">PARAMETERS</span></span>

### <span data-ttu-id="4199a-116">-容量</span><span class="sxs-lookup"><span data-stu-id="4199a-116">-Capacity</span></span>
<span data-ttu-id="4199a-117">VM 的實例編號。</span><span class="sxs-lookup"><span data-stu-id="4199a-117">The instance number of the VM.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4199a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4199a-118">-DefaultProfile</span></span>
<span data-ttu-id="4199a-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4199a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4199a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4199a-120">-InputObject</span></span>
<span data-ttu-id="4199a-121">Kusto [群集物件]。</span><span class="sxs-lookup"><span data-stu-id="4199a-121">Kusto cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4199a-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="4199a-122">-Name</span></span>
<span data-ttu-id="4199a-123">要更新之群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="4199a-123">Name of cluster to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4199a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4199a-124">-ResourceGroupName</span></span>
<span data-ttu-id="4199a-125">群集存在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4199a-125">Name of resource group under which the cluster exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4199a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4199a-126">-ResourceId</span></span>
<span data-ttu-id="4199a-127">Kusto [群集 ResourceID]。</span><span class="sxs-lookup"><span data-stu-id="4199a-127">Kusto cluster ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4199a-128">-SkuName</span><span class="sxs-lookup"><span data-stu-id="4199a-128">-SkuName</span></span>
<span data-ttu-id="4199a-129">用來建立群集的 Sku 名稱</span><span class="sxs-lookup"><span data-stu-id="4199a-129">Name of the Sku used to create the cluster</span></span>

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

### <span data-ttu-id="4199a-130">層級</span><span class="sxs-lookup"><span data-stu-id="4199a-130">-Tier</span></span>
<span data-ttu-id="4199a-131">建立群集所用的層級名稱</span><span class="sxs-lookup"><span data-stu-id="4199a-131">Name of the Tier used to create the cluster</span></span>

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

### <span data-ttu-id="4199a-132">-確認</span><span class="sxs-lookup"><span data-stu-id="4199a-132">-Confirm</span></span>
<span data-ttu-id="4199a-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4199a-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4199a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4199a-134">-WhatIf</span></span>
<span data-ttu-id="4199a-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4199a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4199a-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4199a-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4199a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4199a-137">CommonParameters</span></span>
<span data-ttu-id="4199a-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4199a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4199a-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4199a-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4199a-140">輸入</span><span class="sxs-lookup"><span data-stu-id="4199a-140">INPUTS</span></span>

### <span data-ttu-id="4199a-141">System.object</span><span class="sxs-lookup"><span data-stu-id="4199a-141">System.String</span></span>

### <span data-ttu-id="4199a-142">PSKustoCluster 中的 Kusto。</span><span class="sxs-lookup"><span data-stu-id="4199a-142">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="4199a-143">輸出</span><span class="sxs-lookup"><span data-stu-id="4199a-143">OUTPUTS</span></span>

### <span data-ttu-id="4199a-144">PSKustoCluster 中的 Kusto。</span><span class="sxs-lookup"><span data-stu-id="4199a-144">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="4199a-145">筆記</span><span class="sxs-lookup"><span data-stu-id="4199a-145">NOTES</span></span>

## <span data-ttu-id="4199a-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="4199a-146">RELATED LINKS</span></span>
