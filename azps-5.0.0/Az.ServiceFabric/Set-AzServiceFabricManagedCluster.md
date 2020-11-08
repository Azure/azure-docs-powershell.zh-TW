---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedCluster.md
ms.openlocfilehash: 4636dc8f8c8efdf9dae5f7d2094fd3432528f043
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138467"
---
# <span data-ttu-id="6e8a7-101">Set-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="6e8a7-101">Set-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="6e8a7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6e8a7-102">SYNOPSIS</span></span>
<span data-ttu-id="6e8a7-103">設定群集資源屬性。</span><span class="sxs-lookup"><span data-stu-id="6e8a7-103">Set cluster resource properties.</span></span>

## <span data-ttu-id="6e8a7-104">句法</span><span class="sxs-lookup"><span data-stu-id="6e8a7-104">SYNTAX</span></span>

### <span data-ttu-id="6e8a7-105">ByObj (預設) </span><span class="sxs-lookup"><span data-stu-id="6e8a7-105">ByObj (Default)</span></span>
```
Set-AzServiceFabricManagedCluster [-InputObject] <PSManagedCluster> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e8a7-106">WithPramsByName</span><span class="sxs-lookup"><span data-stu-id="6e8a7-106">WithPramsByName</span></span>
```
Set-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-HttpGatewayConnectionPort <Int32>]
 [-ClientConnectionPort <Int32>] [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e8a7-107">ByNameById</span><span class="sxs-lookup"><span data-stu-id="6e8a7-107">ByNameById</span></span>
```
Set-AzServiceFabricManagedCluster [-ResourceId] <String> [-UpgradeMode <ClusterUpgradeMode>]
 [-CodeVersion <String>] [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>]
 [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e8a7-108">說明</span><span class="sxs-lookup"><span data-stu-id="6e8a7-108">DESCRIPTION</span></span>
<span data-ttu-id="6e8a7-109">設定群集資源屬性。</span><span class="sxs-lookup"><span data-stu-id="6e8a7-109">Set cluster resource properties.</span></span>

## <span data-ttu-id="6e8a7-110">示例</span><span class="sxs-lookup"><span data-stu-id="6e8a7-110">EXAMPLES</span></span>

### <span data-ttu-id="6e8a7-111">範例1</span><span class="sxs-lookup"><span data-stu-id="6e8a7-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Update-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName -DnsName testnewdns -ClientConnectionPort 50000 -Verbose
```

<span data-ttu-id="6e8a7-112">更新群集的 dns 名稱和用戶端連線埠。</span><span class="sxs-lookup"><span data-stu-id="6e8a7-112">Update dns name and client connection port for the cluster.</span></span>

### <span data-ttu-id="6e8a7-113">範例2</span><span class="sxs-lookup"><span data-stu-id="6e8a7-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster.DnsName = "testnewdns"
$cluster.ClientConnectionPort = 50000
$cluster | Set-AzServiceFabricManagedCluster
```

<span data-ttu-id="6e8a7-114">使用管道更新群集的 dns 名稱和用戶端連線埠。</span><span class="sxs-lookup"><span data-stu-id="6e8a7-114">Update dns name and client connection port for the cluster, with piping.</span></span>

## <span data-ttu-id="6e8a7-115">參數</span><span class="sxs-lookup"><span data-stu-id="6e8a7-115">PARAMETERS</span></span>

### <span data-ttu-id="6e8a7-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6e8a7-116">-AsJob</span></span>
<span data-ttu-id="6e8a7-117">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="6e8a7-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="6e8a7-118">-ClientConnectionPort</span><span class="sxs-lookup"><span data-stu-id="6e8a7-118">-ClientConnectionPort</span></span>
<span data-ttu-id="6e8a7-119">用於用戶端連線至群集的埠。</span><span class="sxs-lookup"><span data-stu-id="6e8a7-119">Port used for client connections to the cluster.</span></span> <span data-ttu-id="6e8a7-120">預設：19000。</span><span class="sxs-lookup"><span data-stu-id="6e8a7-120">Default: 19000.</span></span>

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

### <span data-ttu-id="6e8a7-121">-CodeVersion</span><span class="sxs-lookup"><span data-stu-id="6e8a7-121">-CodeVersion</span></span>
<span data-ttu-id="6e8a7-122">群集程式碼版本。</span><span class="sxs-lookup"><span data-stu-id="6e8a7-122">Cluster code version.</span></span> <span data-ttu-id="6e8a7-123">只有在 [升級模式] 為 [手動] 時才使用。</span><span class="sxs-lookup"><span data-stu-id="6e8a7-123">Only use if upgrade mode is Manual.</span></span>

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

### <span data-ttu-id="6e8a7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e8a7-124">-DefaultProfile</span></span>
<span data-ttu-id="6e8a7-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6e8a7-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e8a7-126">-DnsName</span><span class="sxs-lookup"><span data-stu-id="6e8a7-126">-DnsName</span></span>
<span data-ttu-id="6e8a7-127">群集的 dns 名稱。</span><span class="sxs-lookup"><span data-stu-id="6e8a7-127">Cluster's dns name.</span></span>

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

### <span data-ttu-id="6e8a7-128">-HttpGatewayConnectionPort</span><span class="sxs-lookup"><span data-stu-id="6e8a7-128">-HttpGatewayConnectionPort</span></span>
<span data-ttu-id="6e8a7-129">用於連接至群集的 HTTP 連線埠。</span><span class="sxs-lookup"><span data-stu-id="6e8a7-129">Port used for http connections to the cluster.</span></span> <span data-ttu-id="6e8a7-130">預設：19080。</span><span class="sxs-lookup"><span data-stu-id="6e8a7-130">Default: 19080.</span></span>

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

### <span data-ttu-id="6e8a7-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e8a7-131">-InputObject</span></span>
<span data-ttu-id="6e8a7-132">受管理的群集資源</span><span class="sxs-lookup"><span data-stu-id="6e8a7-132">Managed Cluster resource</span></span>

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

### <span data-ttu-id="6e8a7-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="6e8a7-133">-Name</span></span>
<span data-ttu-id="6e8a7-134">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="6e8a7-134">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="6e8a7-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e8a7-135">-ResourceGroupName</span></span>
<span data-ttu-id="6e8a7-136">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6e8a7-136">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="6e8a7-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e8a7-137">-ResourceId</span></span>
<span data-ttu-id="6e8a7-138">受管理的群集資源識別碼</span><span class="sxs-lookup"><span data-stu-id="6e8a7-138">Managed Cluster resource id</span></span>

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

### <span data-ttu-id="6e8a7-139">-ReverseProxyEndpointPort</span><span class="sxs-lookup"><span data-stu-id="6e8a7-139">-ReverseProxyEndpointPort</span></span>
<span data-ttu-id="6e8a7-140">反向 proxy 使用的端點。</span><span class="sxs-lookup"><span data-stu-id="6e8a7-140">Endpoint used by reverse proxy.</span></span>

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

### <span data-ttu-id="6e8a7-141">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="6e8a7-141">-UpgradeMode</span></span>
<span data-ttu-id="6e8a7-142">群集代碼版本升級模式。</span><span class="sxs-lookup"><span data-stu-id="6e8a7-142">Cluster code version upgrade mode.</span></span> <span data-ttu-id="6e8a7-143">[自動] 或 [手動]。</span><span class="sxs-lookup"><span data-stu-id="6e8a7-143">Automatic or Manual.</span></span>

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

### <span data-ttu-id="6e8a7-144">-確認</span><span class="sxs-lookup"><span data-stu-id="6e8a7-144">-Confirm</span></span>
<span data-ttu-id="6e8a7-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6e8a7-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e8a7-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e8a7-146">-WhatIf</span></span>
<span data-ttu-id="6e8a7-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6e8a7-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6e8a7-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6e8a7-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e8a7-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e8a7-149">CommonParameters</span></span>
<span data-ttu-id="6e8a7-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6e8a7-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e8a7-151">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6e8a7-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e8a7-152">輸入</span><span class="sxs-lookup"><span data-stu-id="6e8a7-152">INPUTS</span></span>

### <span data-ttu-id="6e8a7-153">System.object</span><span class="sxs-lookup"><span data-stu-id="6e8a7-153">System.String</span></span>

## <span data-ttu-id="6e8a7-154">輸出</span><span class="sxs-lookup"><span data-stu-id="6e8a7-154">OUTPUTS</span></span>

### <span data-ttu-id="6e8a7-155">PSManagedCluster 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="6e8a7-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="6e8a7-156">筆記</span><span class="sxs-lookup"><span data-stu-id="6e8a7-156">NOTES</span></span>

## <span data-ttu-id="6e8a7-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="6e8a7-157">RELATED LINKS</span></span>