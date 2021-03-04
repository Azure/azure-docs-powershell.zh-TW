---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/new-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 065885f4ae8f6d2ac51cb87cb0e697f4f22245f5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913306"
---
# <span data-ttu-id="4b52a-101">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="4b52a-101">New-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="4b52a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4b52a-102">SYNOPSIS</span></span>
<span data-ttu-id="4b52a-103">建立新節點類型資源。</span><span class="sxs-lookup"><span data-stu-id="4b52a-103">Create new node type resource.</span></span>

## <span data-ttu-id="4b52a-104">語法</span><span class="sxs-lookup"><span data-stu-id="4b52a-104">SYNTAX</span></span>

```
New-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -InstanceCount <Int32> [-Primary] [-DiskSize <Int32>] [-ApplicationStartPort <Int32>]
 [-ApplicationEndPort <Int32>] [-EphemeralStartPort <Int32>] [-EphemeralEndPort <Int32>] [-VmSize <String>]
 [-VmImagePublisher <String>] [-VmImageOffer <String>] [-VmImageSku <String>] [-VmImageVersion <String>]
 [-Capacity <Hashtable>] [-PlacementProperty <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b52a-105">描述</span><span class="sxs-lookup"><span data-stu-id="4b52a-105">DESCRIPTION</span></span>
<span data-ttu-id="4b52a-106">為特定組群建立新節點類型資源。</span><span class="sxs-lookup"><span data-stu-id="4b52a-106">Create new node type resource for an specific cluster.</span></span>

## <span data-ttu-id="4b52a-107">例子</span><span class="sxs-lookup"><span data-stu-id="4b52a-107">EXAMPLES</span></span>

### <span data-ttu-id="4b52a-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="4b52a-108">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
New-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName -Primary -InstanceCount 3
```

<span data-ttu-id="4b52a-109">使用 3 個節點建立主節點類型。</span><span class="sxs-lookup"><span data-stu-id="4b52a-109">Create primary node type with 3 nodes.</span></span>

### <span data-ttu-id="4b52a-110">範例 2</span><span class="sxs-lookup"><span data-stu-id="4b52a-110">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
New-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName -InstanceCount 5 -Primary -PlacementProperty @{NodeColor="Green";SomeProperty="5";} -Capacity @{ClientConnections="65536";} -ApplicationStartPort 20575 -ApplicationEndPort 20605 -EphemeralStartPort 20606 -EphemeralEndPort 20861
```

<span data-ttu-id="4b52a-111">使用 5 個節點建立主節點類型，並指定位置屬性、容量、應用程式和暫時埠。</span><span class="sxs-lookup"><span data-stu-id="4b52a-111">Create primary node type with 5 nodes and specifying placement properties, capacities, application and ephemeral ports.</span></span>

## <span data-ttu-id="4b52a-112">參數</span><span class="sxs-lookup"><span data-stu-id="4b52a-112">PARAMETERS</span></span>

### <span data-ttu-id="4b52a-113">-ApplicationEndPort</span><span class="sxs-lookup"><span data-stu-id="4b52a-113">-ApplicationEndPort</span></span>
<span data-ttu-id="4b52a-114">埠範圍的應用程式結束埠。</span><span class="sxs-lookup"><span data-stu-id="4b52a-114">Application End port of a range of ports.</span></span>

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

### <span data-ttu-id="4b52a-115">-ApplicationStartPort</span><span class="sxs-lookup"><span data-stu-id="4b52a-115">-ApplicationStartPort</span></span>
<span data-ttu-id="4b52a-116">一系列埠的應用程式啟動埠。</span><span class="sxs-lookup"><span data-stu-id="4b52a-116">Application start port of a range of ports.</span></span>

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

### <span data-ttu-id="4b52a-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4b52a-117">-AsJob</span></span>
<span data-ttu-id="4b52a-118">在背景中執行 Cmdlet 並返回工作以追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="4b52a-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="4b52a-119">-容量</span><span class="sxs-lookup"><span data-stu-id="4b52a-119">-Capacity</span></span>
<span data-ttu-id="4b52a-120">將節點類型中的節點所使用容量標記當做金鑰/值組時，集區資源管理員會使用這些標記來瞭解節點有多少資源。</span><span class="sxs-lookup"><span data-stu-id="4b52a-120">Capacity tags applied to the nodes in the node type as key/value pairs, the cluster resource manager uses these tags to understand how much resource a node has.</span></span>
<span data-ttu-id="4b52a-121">更新此選項會優先于目前的值。</span><span class="sxs-lookup"><span data-stu-id="4b52a-121">Updating this will override the current values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b52a-122">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4b52a-122">-ClusterName</span></span>
<span data-ttu-id="4b52a-123">指定組名。</span><span class="sxs-lookup"><span data-stu-id="4b52a-123">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="4b52a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b52a-124">-DefaultProfile</span></span>
<span data-ttu-id="4b52a-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4b52a-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b52a-126">-DiskSize</span><span class="sxs-lookup"><span data-stu-id="4b52a-126">-DiskSize</span></span>
<span data-ttu-id="4b52a-127">GBs 中節點類型中每個 vm 的磁片大小。</span><span class="sxs-lookup"><span data-stu-id="4b52a-127">Disk size for each vm in the node type in GBs.</span></span>
<span data-ttu-id="4b52a-128">預設 100。</span><span class="sxs-lookup"><span data-stu-id="4b52a-128">Default 100.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b52a-129">-EphemeralEndPort</span><span class="sxs-lookup"><span data-stu-id="4b52a-129">-EphemeralEndPort</span></span>
<span data-ttu-id="4b52a-130">一系列埠的暫時結束埠。</span><span class="sxs-lookup"><span data-stu-id="4b52a-130">Ephemeral end port of a range of ports.</span></span>

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

### <span data-ttu-id="4b52a-131">-EphemeralStartPort</span><span class="sxs-lookup"><span data-stu-id="4b52a-131">-EphemeralStartPort</span></span>
<span data-ttu-id="4b52a-132">一系列埠的暫時啟動埠。</span><span class="sxs-lookup"><span data-stu-id="4b52a-132">Ephemeral start port of a range of ports.</span></span>

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

### <span data-ttu-id="4b52a-133">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="4b52a-133">-InstanceCount</span></span>
<span data-ttu-id="4b52a-134">節點類型的節點數目。</span><span class="sxs-lookup"><span data-stu-id="4b52a-134">The number of nodes in the node type.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b52a-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="4b52a-135">-Name</span></span>
<span data-ttu-id="4b52a-136">指定節點類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="4b52a-136">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NodeTypeName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b52a-137">-PlacementProperty</span><span class="sxs-lookup"><span data-stu-id="4b52a-137">-PlacementProperty</span></span>
<span data-ttu-id="4b52a-138">在節點類型中，將節點所使用的位置標記當做金鑰/值組，可用來指出應在何處執行特定服務 (工作負載) 位置。</span><span class="sxs-lookup"><span data-stu-id="4b52a-138">Placement tags applied to nodes in the node type as key/value pairs, which can be used to indicate where certain services (workload) should run.</span></span>
<span data-ttu-id="4b52a-139">更新此選項會優先于目前的值。</span><span class="sxs-lookup"><span data-stu-id="4b52a-139">Updating this will override the current values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b52a-140">-主要</span><span class="sxs-lookup"><span data-stu-id="4b52a-140">-Primary</span></span>
<span data-ttu-id="4b52a-141">指定節點類型是否為主要。</span><span class="sxs-lookup"><span data-stu-id="4b52a-141">Specify if the node type is primary.</span></span>
<span data-ttu-id="4b52a-142">在此節點類型上，將會執行系統服務。</span><span class="sxs-lookup"><span data-stu-id="4b52a-142">On this node type will run system services.</span></span>
<span data-ttu-id="4b52a-143">只有一個節點類型應標示為主要。</span><span class="sxs-lookup"><span data-stu-id="4b52a-143">Only one node type should be marked as primary.</span></span>
<span data-ttu-id="4b52a-144">無法針對現有組群刪除或變更主要節點類型。</span><span class="sxs-lookup"><span data-stu-id="4b52a-144">Primary node type cannot be deleted or changed for existing clusters.</span></span>

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

### <span data-ttu-id="4b52a-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b52a-145">-ResourceGroupName</span></span>
<span data-ttu-id="4b52a-146">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4b52a-146">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="4b52a-147">-VmImageOffer</span><span class="sxs-lookup"><span data-stu-id="4b52a-147">-VmImageOffer</span></span>
<span data-ttu-id="4b52a-148">Azure 虛擬機器 Marketplace 映射的優惠類型。</span><span class="sxs-lookup"><span data-stu-id="4b52a-148">The offer type of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="4b52a-149">預設值：WindowsServer。</span><span class="sxs-lookup"><span data-stu-id="4b52a-149">Default: WindowsServer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "WindowsServer"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b52a-150">-VmImagePublisher</span><span class="sxs-lookup"><span data-stu-id="4b52a-150">-VmImagePublisher</span></span>
<span data-ttu-id="4b52a-151">Azure 虛擬機器 Marketplace 映射的發行者。</span><span class="sxs-lookup"><span data-stu-id="4b52a-151">The publisher of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="4b52a-152">預設值：MicrosoftWindowsServer。</span><span class="sxs-lookup"><span data-stu-id="4b52a-152">Default: MicrosoftWindowsServer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "MicrosoftWindowsServer"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b52a-153">-VmImageSku</span><span class="sxs-lookup"><span data-stu-id="4b52a-153">-VmImageSku</span></span>
<span data-ttu-id="4b52a-154">Azure 虛擬機器 Marketplace 映射的 SKU。</span><span class="sxs-lookup"><span data-stu-id="4b52a-154">The SKU of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="4b52a-155">預設值：2019-資料中心。</span><span class="sxs-lookup"><span data-stu-id="4b52a-155">Default: 2019-Datacenter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "2019-Datacenter"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b52a-156">-VmImageVersion</span><span class="sxs-lookup"><span data-stu-id="4b52a-156">-VmImageVersion</span></span>
<span data-ttu-id="4b52a-157">Azure 虛擬機器 Marketplace 映射的版本。</span><span class="sxs-lookup"><span data-stu-id="4b52a-157">The version of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="4b52a-158">預設：最新。</span><span class="sxs-lookup"><span data-stu-id="4b52a-158">Default: latest.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "latest"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b52a-159">-VmSize</span><span class="sxs-lookup"><span data-stu-id="4b52a-159">-VmSize</span></span>
<span data-ttu-id="4b52a-160">位於資料庫的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="4b52a-160">The size of virtual machines in the pool.</span></span>
<span data-ttu-id="4b52a-161">同一個資料庫內的所有虛擬機器大小都相同。</span><span class="sxs-lookup"><span data-stu-id="4b52a-161">All virtual machines in a pool are the same size.</span></span>
<span data-ttu-id="4b52a-162">預設：Standard_D2。</span><span class="sxs-lookup"><span data-stu-id="4b52a-162">Default: Standard_D2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "Standard_D2"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b52a-163">-確認</span><span class="sxs-lookup"><span data-stu-id="4b52a-163">-Confirm</span></span>
<span data-ttu-id="4b52a-164">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4b52a-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b52a-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b52a-165">-WhatIf</span></span>
<span data-ttu-id="4b52a-166">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4b52a-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b52a-167">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4b52a-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b52a-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b52a-168">CommonParameters</span></span>
<span data-ttu-id="4b52a-169">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4b52a-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b52a-170">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4b52a-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b52a-171">輸入</span><span class="sxs-lookup"><span data-stu-id="4b52a-171">INPUTS</span></span>

### <span data-ttu-id="4b52a-172">System.String</span><span class="sxs-lookup"><span data-stu-id="4b52a-172">System.String</span></span>

## <span data-ttu-id="4b52a-173">輸出</span><span class="sxs-lookup"><span data-stu-id="4b52a-173">OUTPUTS</span></span>

### <span data-ttu-id="4b52a-174">Microsoft.Azure.Commands.ServiceFabric.models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="4b52a-174">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="4b52a-175">筆記</span><span class="sxs-lookup"><span data-stu-id="4b52a-175">NOTES</span></span>

## <span data-ttu-id="4b52a-176">相關連結</span><span class="sxs-lookup"><span data-stu-id="4b52a-176">RELATED LINKS</span></span>
