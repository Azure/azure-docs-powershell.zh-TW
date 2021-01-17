---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricService.md
ms.openlocfilehash: 930d86e457bef446d282db95d4289913bdcf10b1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448220"
---
# <span data-ttu-id="301df-101">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="301df-101">New-AzServiceFabricService</span></span>

## <span data-ttu-id="301df-102">摘要</span><span class="sxs-lookup"><span data-stu-id="301df-102">SYNOPSIS</span></span>
<span data-ttu-id="301df-103">在指定的應用程式和群集下建立新的 service fabric service。</span><span class="sxs-lookup"><span data-stu-id="301df-103">Create new service fabric service under the specified application and cluster.</span></span>

## <span data-ttu-id="301df-104">句法</span><span class="sxs-lookup"><span data-stu-id="301df-104">SYNTAX</span></span>

### <span data-ttu-id="301df-105">Stateless-Singleton (預設) </span><span class="sxs-lookup"><span data-stu-id="301df-105">Stateless-Singleton (Default)</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeSingleton] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="301df-106">Stateless-UniformInt64Range</span><span class="sxs-lookup"><span data-stu-id="301df-106">Stateless-UniformInt64Range</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeUniformInt64] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="301df-107">Stateless-Named</span><span class="sxs-lookup"><span data-stu-id="301df-107">Stateless-Named</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeNamed] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="301df-108">Stateful-Singleton</span><span class="sxs-lookup"><span data-stu-id="301df-108">Stateful-Singleton</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeSingleton]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="301df-109">Stateful-UniformInt64Range</span><span class="sxs-lookup"><span data-stu-id="301df-109">Stateful-UniformInt64Range</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeUniformInt64]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="301df-110">Stateful-Named</span><span class="sxs-lookup"><span data-stu-id="301df-110">Stateful-Named</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeNamed]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="301df-111">說明</span><span class="sxs-lookup"><span data-stu-id="301df-111">DESCRIPTION</span></span>
<span data-ttu-id="301df-112">這個 Cmdlet 可讓您在指定的應用程式下建立無狀態或有狀態的服務。</span><span class="sxs-lookup"><span data-stu-id="301df-112">This cmdlet allows to creating  stateless or stateful services under the specified application.</span></span> <span data-ttu-id="301df-113">服務應該會在應用程式資訊清單中結束，且類型應該與資訊清單中的相同。</span><span class="sxs-lookup"><span data-stu-id="301df-113">The service should exit in the application manifest and the type should be the same as the one in the manifest.</span></span> <span data-ttu-id="301df-114">應用程式名稱應該是服務名稱的首碼。</span><span class="sxs-lookup"><span data-stu-id="301df-114">The application name should be a prefix of the service name.</span></span>

## <span data-ttu-id="301df-115">示例</span><span class="sxs-lookup"><span data-stu-id="301df-115">EXAMPLES</span></span>

### <span data-ttu-id="301df-116">範例1</span><span class="sxs-lookup"><span data-stu-id="301df-116">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService1"
PS C:\> $serviceTypeName = "testStateless"
PS C:\> New-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName -Type $serviceTypeName -Stateless -InstanceCount -1 -PartitionSchemaSingleton -Verbose
```

<span data-ttu-id="301df-117">這個範例會在所有節點) 上，建立一個新的無狀態服務「testApp ~ testService1」，並 (實例計數-1。</span><span class="sxs-lookup"><span data-stu-id="301df-117">This example will create a new stateless service "testApp~testService1" with instance count -1 (on all the nodes).</span></span>

### <span data-ttu-id="301df-118">範例2</span><span class="sxs-lookup"><span data-stu-id="301df-118">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService2"
PS C:\> $serviceTypeName = "testStatefulType"
PS C:\> New-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName -Type $serviceTypeName -Stateful -TargetReplicaSetSize 3 MinReplicaSetSize 5
```

<span data-ttu-id="301df-119">這個範例會使用5個節點的目標，建立新的狀態服務「testApp ~ testService2」。</span><span class="sxs-lookup"><span data-stu-id="301df-119">This example will create a new stateful service "testApp~testService2" with a target of 5 nodes.</span></span>

## <span data-ttu-id="301df-120">參數</span><span class="sxs-lookup"><span data-stu-id="301df-120">PARAMETERS</span></span>

### <span data-ttu-id="301df-121">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="301df-121">-ApplicationName</span></span>
<span data-ttu-id="301df-122">指定應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="301df-122">Specify the name of the application.</span></span>

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

### <span data-ttu-id="301df-123">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="301df-123">-ClusterName</span></span>
<span data-ttu-id="301df-124">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="301df-124">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="301df-125">-DefaultMoveCost</span><span class="sxs-lookup"><span data-stu-id="301df-125">-DefaultMoveCost</span></span>
<span data-ttu-id="301df-126">指定移動的預設成本。</span><span class="sxs-lookup"><span data-stu-id="301df-126">Specify the default cost for a move.</span></span>
<span data-ttu-id="301df-127">較高的成本可讓群集資源管理員在嘗試平衡群集時移動複製副本的可能性不大</span><span class="sxs-lookup"><span data-stu-id="301df-127">Higher costs make it less likely that the Cluster Resource Manager will move the replica when trying to balance the cluster</span></span>

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

### <span data-ttu-id="301df-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="301df-128">-DefaultProfile</span></span>
<span data-ttu-id="301df-129">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="301df-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="301df-130">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="301df-130">-InstanceCount</span></span>
<span data-ttu-id="301df-131">指定服務的實例計數</span><span class="sxs-lookup"><span data-stu-id="301df-131">Specify the instance count for the service</span></span>

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

### <span data-ttu-id="301df-132">-MinReplicaSetSize</span><span class="sxs-lookup"><span data-stu-id="301df-132">-MinReplicaSetSize</span></span>
<span data-ttu-id="301df-133">指定服務的最小複本集大小</span><span class="sxs-lookup"><span data-stu-id="301df-133">Specify the min replica set size for the service</span></span>

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

### <span data-ttu-id="301df-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="301df-134">-Name</span></span>
<span data-ttu-id="301df-135">指定服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="301df-135">Specify the name of the service.</span></span>

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

### <span data-ttu-id="301df-136">-PartitionSchemeNamed</span><span class="sxs-lookup"><span data-stu-id="301df-136">-PartitionSchemeNamed</span></span>
<span data-ttu-id="301df-137">指示服務使用命名的分區配置。</span><span class="sxs-lookup"><span data-stu-id="301df-137">Indicates that the service uses the named partition scheme.</span></span>
<span data-ttu-id="301df-138">使用此模型的服務通常會有可在限制集內 bucketed 的資料。</span><span class="sxs-lookup"><span data-stu-id="301df-138">Services using this model usually have data that can be bucketed, within a bounded set.</span></span>
<span data-ttu-id="301df-139">使用做為命名的分區鍵的一些資料欄位的常見範例是地區、郵遞區號、客戶群組或其他業務界限。</span><span class="sxs-lookup"><span data-stu-id="301df-139">Some common examples of data fields used as named partition keys would be regions, postal codes, customer groups, or other business boundaries.</span></span>

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

### <span data-ttu-id="301df-140">-PartitionSchemeSingleton</span><span class="sxs-lookup"><span data-stu-id="301df-140">-PartitionSchemeSingleton</span></span>
<span data-ttu-id="301df-141">指示服務使用單一分區配置。</span><span class="sxs-lookup"><span data-stu-id="301df-141">Indicates that the service uses the singleton partition scheme.</span></span>
<span data-ttu-id="301df-142">當服務不需要任何其他路由時，通常會使用單一分區。</span><span class="sxs-lookup"><span data-stu-id="301df-142">Singleton partitions are typically used when the service does not require any additional routing.</span></span>

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

### <span data-ttu-id="301df-143">-PartitionSchemeUniformInt64</span><span class="sxs-lookup"><span data-stu-id="301df-143">-PartitionSchemeUniformInt64</span></span>
<span data-ttu-id="301df-144">指示服務使用 UniformInt64 分區配置。</span><span class="sxs-lookup"><span data-stu-id="301df-144">Indicates that the service uses the UniformInt64 partition scheme.</span></span>
<span data-ttu-id="301df-145">這表示每個分區都擁有一個範圍的 int64 鍵。</span><span class="sxs-lookup"><span data-stu-id="301df-145">This means that each partition owns a range of int64 keys.</span></span>

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

### <span data-ttu-id="301df-146">-QuorumLossWaitDuration</span><span class="sxs-lookup"><span data-stu-id="301df-146">-QuorumLossWaitDuration</span></span>
<span data-ttu-id="301df-147">指定服務的仲裁損失等待時間</span><span class="sxs-lookup"><span data-stu-id="301df-147">Specify the quorum loss wait duration for the service</span></span>

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

### <span data-ttu-id="301df-148">-ReplicaRestartWaitDuration</span><span class="sxs-lookup"><span data-stu-id="301df-148">-ReplicaRestartWaitDuration</span></span>
<span data-ttu-id="301df-149">指定服務的複本重新開機等待持續時間</span><span class="sxs-lookup"><span data-stu-id="301df-149">Specify the replica restart wait duration for the service</span></span>

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

### <span data-ttu-id="301df-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="301df-150">-ResourceGroupName</span></span>
<span data-ttu-id="301df-151">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="301df-151">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="301df-152">-StandByReplicaKeepDuration</span><span class="sxs-lookup"><span data-stu-id="301df-152">-StandByReplicaKeepDuration</span></span>
<span data-ttu-id="301df-153">指定服務的 [備用複本] 持續時間</span><span class="sxs-lookup"><span data-stu-id="301df-153">Specify the stand by replica duration for the service</span></span>

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

### <span data-ttu-id="301df-154">-狀態</span><span class="sxs-lookup"><span data-stu-id="301df-154">-Stateful</span></span>
<span data-ttu-id="301df-155">用於狀態服務</span><span class="sxs-lookup"><span data-stu-id="301df-155">Use for stateful service</span></span>

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

### <span data-ttu-id="301df-156">-無狀態</span><span class="sxs-lookup"><span data-stu-id="301df-156">-Stateless</span></span>
<span data-ttu-id="301df-157">用於無狀態服務</span><span class="sxs-lookup"><span data-stu-id="301df-157">Use for stateless service</span></span>

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

### <span data-ttu-id="301df-158">-TargetReplicaSetSize</span><span class="sxs-lookup"><span data-stu-id="301df-158">-TargetReplicaSetSize</span></span>
<span data-ttu-id="301df-159">指定服務的目標複本集大小</span><span class="sxs-lookup"><span data-stu-id="301df-159">Specify the target replica set size for the service</span></span>

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

### <span data-ttu-id="301df-160">-類型</span><span class="sxs-lookup"><span data-stu-id="301df-160">-Type</span></span>
<span data-ttu-id="301df-161">指定應用程式的服務類型名稱，應該存在於應用程式資訊清單中。</span><span class="sxs-lookup"><span data-stu-id="301df-161">Specify the service type name of the application, should exist in the application manifest.</span></span>

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

### <span data-ttu-id="301df-162">-確認</span><span class="sxs-lookup"><span data-stu-id="301df-162">-Confirm</span></span>
<span data-ttu-id="301df-163">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="301df-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="301df-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="301df-164">-WhatIf</span></span>
<span data-ttu-id="301df-165">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="301df-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="301df-166">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="301df-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="301df-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="301df-167">CommonParameters</span></span>
<span data-ttu-id="301df-168">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="301df-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="301df-169">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="301df-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="301df-170">輸入</span><span class="sxs-lookup"><span data-stu-id="301df-170">INPUTS</span></span>

### <span data-ttu-id="301df-171">System.object</span><span class="sxs-lookup"><span data-stu-id="301df-171">System.String</span></span>

## <span data-ttu-id="301df-172">輸出</span><span class="sxs-lookup"><span data-stu-id="301df-172">OUTPUTS</span></span>

### <span data-ttu-id="301df-173">PSService 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="301df-173">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="301df-174">筆記</span><span class="sxs-lookup"><span data-stu-id="301df-174">NOTES</span></span>

## <span data-ttu-id="301df-175">相關連結</span><span class="sxs-lookup"><span data-stu-id="301df-175">RELATED LINKS</span></span>
