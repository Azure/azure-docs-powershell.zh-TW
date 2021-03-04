---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/set-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedCluster.md
ms.openlocfilehash: 8a3ca4ed215dccbcc3cbfb541d7e023871bf6490
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915794"
---
# <span data-ttu-id="54868-101">Set-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="54868-101">Set-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="54868-102">簡介</span><span class="sxs-lookup"><span data-stu-id="54868-102">SYNOPSIS</span></span>
<span data-ttu-id="54868-103">設定組群資源屬性。</span><span class="sxs-lookup"><span data-stu-id="54868-103">Set cluster resource properties.</span></span>

## <span data-ttu-id="54868-104">語法</span><span class="sxs-lookup"><span data-stu-id="54868-104">SYNTAX</span></span>

### <span data-ttu-id="54868-105">ByObj (預設) </span><span class="sxs-lookup"><span data-stu-id="54868-105">ByObj (Default)</span></span>
```
Set-AzServiceFabricManagedCluster [-InputObject] <PSManagedCluster> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54868-106">WithBymsByName</span><span class="sxs-lookup"><span data-stu-id="54868-106">WithPramsByName</span></span>
```
Set-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-HttpGatewayConnectionPort <Int32>]
 [-ClientConnectionPort <Int32>] [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54868-107">ByNameById</span><span class="sxs-lookup"><span data-stu-id="54868-107">ByNameById</span></span>
```
Set-AzServiceFabricManagedCluster [-ResourceId] <String> [-UpgradeMode <ClusterUpgradeMode>]
 [-CodeVersion <String>] [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>]
 [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54868-108">描述</span><span class="sxs-lookup"><span data-stu-id="54868-108">DESCRIPTION</span></span>
<span data-ttu-id="54868-109">設定組群資源屬性。</span><span class="sxs-lookup"><span data-stu-id="54868-109">Set cluster resource properties.</span></span>

## <span data-ttu-id="54868-110">例子</span><span class="sxs-lookup"><span data-stu-id="54868-110">EXAMPLES</span></span>

### <span data-ttu-id="54868-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="54868-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Update-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName -DnsName testnewdns -ClientConnectionPort 50000 -Verbose
```

<span data-ttu-id="54868-112">更新該組群的 dns 名稱和用戶端連接埠。</span><span class="sxs-lookup"><span data-stu-id="54868-112">Update dns name and client connection port for the cluster.</span></span>

### <span data-ttu-id="54868-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="54868-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster.DnsName = "testnewdns"
$cluster.ClientConnectionPort = 50000
$cluster | Set-AzServiceFabricManagedCluster
```

<span data-ttu-id="54868-114">使用管線更新組群的 dns 名稱和用戶端連接埠。</span><span class="sxs-lookup"><span data-stu-id="54868-114">Update dns name and client connection port for the cluster, with piping.</span></span>

## <span data-ttu-id="54868-115">參數</span><span class="sxs-lookup"><span data-stu-id="54868-115">PARAMETERS</span></span>

### <span data-ttu-id="54868-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54868-116">-AsJob</span></span>
<span data-ttu-id="54868-117">在背景中執行 Cmdlet 並返回工作以追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="54868-117">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54868-118">-ClientConnectionPort</span><span class="sxs-lookup"><span data-stu-id="54868-118">-ClientConnectionPort</span></span>
<span data-ttu-id="54868-119">用於用戶端連接到該組集的埠。</span><span class="sxs-lookup"><span data-stu-id="54868-119">Port used for client connections to the cluster.</span></span> <span data-ttu-id="54868-120">預設值：19000。</span><span class="sxs-lookup"><span data-stu-id="54868-120">Default: 19000.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54868-121">-CodeVersion</span><span class="sxs-lookup"><span data-stu-id="54868-121">-CodeVersion</span></span>
<span data-ttu-id="54868-122">組代碼版本。</span><span class="sxs-lookup"><span data-stu-id="54868-122">Cluster code version.</span></span> <span data-ttu-id="54868-123">只有在升級模式為手動時才能使用。</span><span class="sxs-lookup"><span data-stu-id="54868-123">Only use if upgrade mode is Manual.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54868-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54868-124">-DefaultProfile</span></span>
<span data-ttu-id="54868-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="54868-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54868-126">-DnsName</span><span class="sxs-lookup"><span data-stu-id="54868-126">-DnsName</span></span>
<span data-ttu-id="54868-127">Cluster 的 dns 名稱。</span><span class="sxs-lookup"><span data-stu-id="54868-127">Cluster's dns name.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54868-128">-HTTPGatewayConnectionPort</span><span class="sxs-lookup"><span data-stu-id="54868-128">-HttpGatewayConnectionPort</span></span>
<span data-ttu-id="54868-129">用於將 HTTP 連結至該組集的埠。</span><span class="sxs-lookup"><span data-stu-id="54868-129">Port used for http connections to the cluster.</span></span> <span data-ttu-id="54868-130">預設值：19080。</span><span class="sxs-lookup"><span data-stu-id="54868-130">Default: 19080.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54868-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54868-131">-InputObject</span></span>
<span data-ttu-id="54868-132">Managed Cluster 資源</span><span class="sxs-lookup"><span data-stu-id="54868-132">Managed Cluster resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54868-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="54868-133">-Name</span></span>
<span data-ttu-id="54868-134">指定組名。</span><span class="sxs-lookup"><span data-stu-id="54868-134">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54868-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54868-135">-ResourceGroupName</span></span>
<span data-ttu-id="54868-136">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="54868-136">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54868-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54868-137">-ResourceId</span></span>
<span data-ttu-id="54868-138">Managed Cluster 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="54868-138">Managed Cluster resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54868-139">-ReverseProxyEndpointPort</span><span class="sxs-lookup"><span data-stu-id="54868-139">-ReverseProxyEndpointPort</span></span>
<span data-ttu-id="54868-140">由反向 Proxy 使用的端點。</span><span class="sxs-lookup"><span data-stu-id="54868-140">Endpoint used by reverse proxy.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54868-141">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="54868-141">-UpgradeMode</span></span>
<span data-ttu-id="54868-142">組代碼版本升級模式。</span><span class="sxs-lookup"><span data-stu-id="54868-142">Cluster code version upgrade mode.</span></span> <span data-ttu-id="54868-143">自動或手動。</span><span class="sxs-lookup"><span data-stu-id="54868-143">Automatic or Manual.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode]
Parameter Sets: WithPramsByName, ByNameById
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54868-144">-確認</span><span class="sxs-lookup"><span data-stu-id="54868-144">-Confirm</span></span>
<span data-ttu-id="54868-145">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="54868-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54868-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54868-146">-WhatIf</span></span>
<span data-ttu-id="54868-147">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="54868-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="54868-148">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="54868-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54868-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54868-149">CommonParameters</span></span>
<span data-ttu-id="54868-150">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="54868-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54868-151">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="54868-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54868-152">輸入</span><span class="sxs-lookup"><span data-stu-id="54868-152">INPUTS</span></span>

### <span data-ttu-id="54868-153">System.String</span><span class="sxs-lookup"><span data-stu-id="54868-153">System.String</span></span>

## <span data-ttu-id="54868-154">輸出</span><span class="sxs-lookup"><span data-stu-id="54868-154">OUTPUTS</span></span>

### <span data-ttu-id="54868-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="54868-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="54868-156">筆記</span><span class="sxs-lookup"><span data-stu-id="54868-156">NOTES</span></span>

## <span data-ttu-id="54868-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="54868-157">RELATED LINKS</span></span>
