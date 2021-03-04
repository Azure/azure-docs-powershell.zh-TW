---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/new-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricService.md
ms.openlocfilehash: c0572e994650347d24a6b58ca12b6d2938a182bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915853"
---
# <span data-ttu-id="f3876-101">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="f3876-101">New-AzServiceFabricService</span></span>

## <span data-ttu-id="f3876-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f3876-102">SYNOPSIS</span></span>
<span data-ttu-id="f3876-103">在指定的應用程式和組集中建立新的服務結構服務。</span><span class="sxs-lookup"><span data-stu-id="f3876-103">Create new service fabric service under the specified application and cluster.</span></span>

## <span data-ttu-id="f3876-104">語法</span><span class="sxs-lookup"><span data-stu-id="f3876-104">SYNTAX</span></span>

### <span data-ttu-id="f3876-105">Stateless-Singleton (預設) </span><span class="sxs-lookup"><span data-stu-id="f3876-105">Stateless-Singleton (Default)</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeSingleton] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f3876-106">Stateless-UniformInt64Range</span><span class="sxs-lookup"><span data-stu-id="f3876-106">Stateless-UniformInt64Range</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeUniformInt64] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f3876-107">Stateless-Named</span><span class="sxs-lookup"><span data-stu-id="f3876-107">Stateless-Named</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeNamed] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3876-108">Stateful-Singleton</span><span class="sxs-lookup"><span data-stu-id="f3876-108">Stateful-Singleton</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeSingleton]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3876-109">Stateful-UniformInt64Range</span><span class="sxs-lookup"><span data-stu-id="f3876-109">Stateful-UniformInt64Range</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeUniformInt64]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3876-110">Stateful-Named</span><span class="sxs-lookup"><span data-stu-id="f3876-110">Stateful-Named</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeNamed]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3876-111">描述</span><span class="sxs-lookup"><span data-stu-id="f3876-111">DESCRIPTION</span></span>
<span data-ttu-id="f3876-112">此 Cmdlet 允許根據指定的應用程式建立程式設計或狀態服務。</span><span class="sxs-lookup"><span data-stu-id="f3876-112">This cmdlet allows to creating  stateless or stateful services under the specified application.</span></span> <span data-ttu-id="f3876-113">服務應該會從應用程式清單中退出，而且類型應該與清單中的類型相同。</span><span class="sxs-lookup"><span data-stu-id="f3876-113">The service should exit in the application manifest and the type should be the same as the one in the manifest.</span></span> <span data-ttu-id="f3876-114">應用程式名稱應該是服務名稱的首碼。</span><span class="sxs-lookup"><span data-stu-id="f3876-114">The application name should be a prefix of the service name.</span></span>

## <span data-ttu-id="f3876-115">例子</span><span class="sxs-lookup"><span data-stu-id="f3876-115">EXAMPLES</span></span>

### <span data-ttu-id="f3876-116">範例 1</span><span class="sxs-lookup"><span data-stu-id="f3876-116">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService1"
PS C:\> $serviceTypeName = "testStateless"
PS C:\> New-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName -Type $serviceTypeName -Stateless -InstanceCount -1 -PartitionSchemaSingleton -Verbose
```

<span data-ttu-id="f3876-117">此範例將在所有節點上建立實例計數 -1 的新服務「testApp~testService1」， (節點上) 。</span><span class="sxs-lookup"><span data-stu-id="f3876-117">This example will create a new stateless service "testApp~testService1" with instance count -1 (on all the nodes).</span></span>

### <span data-ttu-id="f3876-118">範例 2</span><span class="sxs-lookup"><span data-stu-id="f3876-118">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService2"
PS C:\> $serviceTypeName = "testStatefulType"
PS C:\> New-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName -Type $serviceTypeName -Stateful -TargetReplicaSetSize 3 MinReplicaSetSize 5
```

<span data-ttu-id="f3876-119">此範例會建立一個新的狀態服務"testApp~testService2"，目標為 5 個節點。</span><span class="sxs-lookup"><span data-stu-id="f3876-119">This example will create a new stateful service "testApp~testService2" with a target of 5 nodes.</span></span>

## <span data-ttu-id="f3876-120">參數</span><span class="sxs-lookup"><span data-stu-id="f3876-120">PARAMETERS</span></span>

### <span data-ttu-id="f3876-121">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="f3876-121">-ApplicationName</span></span>
<span data-ttu-id="f3876-122">指定應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3876-122">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3876-123">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f3876-123">-ClusterName</span></span>
<span data-ttu-id="f3876-124">指定組名。</span><span class="sxs-lookup"><span data-stu-id="f3876-124">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3876-125">-DefaultMoveCost</span><span class="sxs-lookup"><span data-stu-id="f3876-125">-DefaultMoveCost</span></span>
<span data-ttu-id="f3876-126">指定移動的預設成本。</span><span class="sxs-lookup"><span data-stu-id="f3876-126">Specify the default cost for a move.</span></span>
<span data-ttu-id="f3876-127">成本越高，當嘗試在組群之間取得平衡時，組組資源管理員移動複本的可能性較小</span><span class="sxs-lookup"><span data-stu-id="f3876-127">Higher costs make it less likely that the Cluster Resource Manager will move the replica when trying to balance the cluster</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.MoveCostEnum
Parameter Sets: (All)
Aliases:
Accepted values: Zero, Low, Medium, High

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3876-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3876-128">-DefaultProfile</span></span>
<span data-ttu-id="f3876-129">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f3876-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3876-130">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="f3876-130">-InstanceCount</span></span>
<span data-ttu-id="f3876-131">指定服務的實例計數</span><span class="sxs-lookup"><span data-stu-id="f3876-131">Specify the instance count for the service</span></span>

```yaml
Type: System.Int32
Parameter Sets: Stateless-Singleton, Stateless-UniformInt64Range, Stateless-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3876-132">-MinReplicaSetSize</span><span class="sxs-lookup"><span data-stu-id="f3876-132">-MinReplicaSetSize</span></span>
<span data-ttu-id="f3876-133">指定服務的最小複本集大小</span><span class="sxs-lookup"><span data-stu-id="f3876-133">Specify the min replica set size for the service</span></span>

```yaml
Type: System.Int32
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3876-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="f3876-134">-Name</span></span>
<span data-ttu-id="f3876-135">指定服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3876-135">Specify the name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3876-136">-PartitionSchemeNamed</span><span class="sxs-lookup"><span data-stu-id="f3876-136">-PartitionSchemeNamed</span></span>
<span data-ttu-id="f3876-137">表示服務使用已命名的分區分配。</span><span class="sxs-lookup"><span data-stu-id="f3876-137">Indicates that the service uses the named partition scheme.</span></span>
<span data-ttu-id="f3876-138">使用此模型的服務通常會有一些資料可以在一組界限內進行容器處理。</span><span class="sxs-lookup"><span data-stu-id="f3876-138">Services using this model usually have data that can be bucketed, within a bounded set.</span></span>
<span data-ttu-id="f3876-139">一些常用資料欄位做為命名的分割鍵，例如區域、郵遞區號、客戶群組或其他商務邊界。</span><span class="sxs-lookup"><span data-stu-id="f3876-139">Some common examples of data fields used as named partition keys would be regions, postal codes, customer groups, or other business boundaries.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateless-Named, Stateful-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3876-140">-PartitionSchemeSingleton</span><span class="sxs-lookup"><span data-stu-id="f3876-140">-PartitionSchemeSingleton</span></span>
<span data-ttu-id="f3876-141">表示服務使用單一磁碟分割分配。</span><span class="sxs-lookup"><span data-stu-id="f3876-141">Indicates that the service uses the singleton partition scheme.</span></span>
<span data-ttu-id="f3876-142">當服務不需要任何其他路由時，通常會使用單一磁碟分割。</span><span class="sxs-lookup"><span data-stu-id="f3876-142">Singleton partitions are typically used when the service does not require any additional routing.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateless-Singleton, Stateful-Singleton
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3876-143">-PartitionSchemeUniformInt64</span><span class="sxs-lookup"><span data-stu-id="f3876-143">-PartitionSchemeUniformInt64</span></span>
<span data-ttu-id="f3876-144">表示服務使用 UniformInt64 分割方案。</span><span class="sxs-lookup"><span data-stu-id="f3876-144">Indicates that the service uses the UniformInt64 partition scheme.</span></span>
<span data-ttu-id="f3876-145">這表示每個磁碟分割區都有一系列 int64 鍵。</span><span class="sxs-lookup"><span data-stu-id="f3876-145">This means that each partition owns a range of int64 keys.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateless-UniformInt64Range, Stateful-UniformInt64Range
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3876-146">-一些圖旁白</span><span class="sxs-lookup"><span data-stu-id="f3876-146">-QuorumLossWaitDuration</span></span>
<span data-ttu-id="f3876-147">指定服務的因應值遺失等待時間</span><span class="sxs-lookup"><span data-stu-id="f3876-147">Specify the quorum loss wait duration for the service</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3876-148">-複本RestartWaitDuration</span><span class="sxs-lookup"><span data-stu-id="f3876-148">-ReplicaRestartWaitDuration</span></span>
<span data-ttu-id="f3876-149">指定服務的複本重新開機等候持續時間</span><span class="sxs-lookup"><span data-stu-id="f3876-149">Specify the replica restart wait duration for the service</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3876-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3876-150">-ResourceGroupName</span></span>
<span data-ttu-id="f3876-151">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3876-151">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3876-152">-StandByReplicaKeepDuration</span><span class="sxs-lookup"><span data-stu-id="f3876-152">-StandByReplicaKeepDuration</span></span>
<span data-ttu-id="f3876-153">指定服務的獨立複本持續時間</span><span class="sxs-lookup"><span data-stu-id="f3876-153">Specify the stand by replica duration for the service</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3876-154">-Stateful</span><span class="sxs-lookup"><span data-stu-id="f3876-154">-Stateful</span></span>
<span data-ttu-id="f3876-155">用於有狀態的服務</span><span class="sxs-lookup"><span data-stu-id="f3876-155">Use for stateful service</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3876-156">-萬能</span><span class="sxs-lookup"><span data-stu-id="f3876-156">-Stateless</span></span>
<span data-ttu-id="f3876-157">用於進位服務</span><span class="sxs-lookup"><span data-stu-id="f3876-157">Use for stateless service</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateless-Singleton, Stateless-UniformInt64Range, Stateless-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3876-158">-TargetReplicaSetSize</span><span class="sxs-lookup"><span data-stu-id="f3876-158">-TargetReplicaSetSize</span></span>
<span data-ttu-id="f3876-159">指定服務的目標複本集大小</span><span class="sxs-lookup"><span data-stu-id="f3876-159">Specify the target replica set size for the service</span></span>

```yaml
Type: System.Int32
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3876-160">-類型</span><span class="sxs-lookup"><span data-stu-id="f3876-160">-Type</span></span>
<span data-ttu-id="f3876-161">指定應用程式的服務類型名稱，應該存在於應用程式清單中。</span><span class="sxs-lookup"><span data-stu-id="f3876-161">Specify the service type name of the application, should exist in the application manifest.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceType

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3876-162">-確認</span><span class="sxs-lookup"><span data-stu-id="f3876-162">-Confirm</span></span>
<span data-ttu-id="f3876-163">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f3876-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3876-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3876-164">-WhatIf</span></span>
<span data-ttu-id="f3876-165">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f3876-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3876-166">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f3876-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3876-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3876-167">CommonParameters</span></span>
<span data-ttu-id="f3876-168">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f3876-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3876-169">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f3876-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3876-170">輸入</span><span class="sxs-lookup"><span data-stu-id="f3876-170">INPUTS</span></span>

### <span data-ttu-id="f3876-171">System.String</span><span class="sxs-lookup"><span data-stu-id="f3876-171">System.String</span></span>

## <span data-ttu-id="f3876-172">輸出</span><span class="sxs-lookup"><span data-stu-id="f3876-172">OUTPUTS</span></span>

### <span data-ttu-id="f3876-173">Microsoft.Azure.Commands.ServiceFabric.models.PSService</span><span class="sxs-lookup"><span data-stu-id="f3876-173">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="f3876-174">筆記</span><span class="sxs-lookup"><span data-stu-id="f3876-174">NOTES</span></span>

## <span data-ttu-id="f3876-175">相關連結</span><span class="sxs-lookup"><span data-stu-id="f3876-175">RELATED LINKS</span></span>
