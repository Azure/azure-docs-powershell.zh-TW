---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 3e89e807acfb2507834686574931011bf398c76c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448227"
---
# <span data-ttu-id="06487-101">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="06487-101">New-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="06487-102">摘要</span><span class="sxs-lookup"><span data-stu-id="06487-102">SYNOPSIS</span></span>
<span data-ttu-id="06487-103">建立新的節點類型資源。</span><span class="sxs-lookup"><span data-stu-id="06487-103">Create new node type resource.</span></span>

## <span data-ttu-id="06487-104">句法</span><span class="sxs-lookup"><span data-stu-id="06487-104">SYNTAX</span></span>

```
New-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -InstanceCount <Int32> [-Primary] [-DiskSize <Int32>] [-ApplicationStartPort <Int32>]
 [-ApplicationEndPort <Int32>] [-EphemeralStartPort <Int32>] [-EphemeralEndPort <Int32>] [-VmSize <String>]
 [-VmImagePublisher <String>] [-VmImageOffer <String>] [-VmImageSku <String>] [-VmImageVersion <String>]
 [-Capacity <Hashtable>] [-PlacementProperty <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06487-105">說明</span><span class="sxs-lookup"><span data-stu-id="06487-105">DESCRIPTION</span></span>
<span data-ttu-id="06487-106">針對特定的群集建立新的節點類型資源。</span><span class="sxs-lookup"><span data-stu-id="06487-106">Create new node type resource for an specific cluster.</span></span>

## <span data-ttu-id="06487-107">示例</span><span class="sxs-lookup"><span data-stu-id="06487-107">EXAMPLES</span></span>

### <span data-ttu-id="06487-108">範例1</span><span class="sxs-lookup"><span data-stu-id="06487-108">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
New-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName -Primary -InstanceCount 3
```

<span data-ttu-id="06487-109">建立具有3個節點的主要節點類型。</span><span class="sxs-lookup"><span data-stu-id="06487-109">Create primary node type with 3 nodes.</span></span>

### <span data-ttu-id="06487-110">範例2</span><span class="sxs-lookup"><span data-stu-id="06487-110">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
New-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName -InstanceCount 5 -Primary -PlacementProperty @{NodeColor="Green";SomeProperty="5";} -Capacity @{ClientConnections="65536";} -ApplicationStartPort 20575 -ApplicationEndPort 20605 -EphemeralStartPort 20606 -EphemeralEndPort 20861
```

<span data-ttu-id="06487-111">建立具有5個節點的主要節點類型，並指定放置屬性、容量、應用程式和暫時埠。</span><span class="sxs-lookup"><span data-stu-id="06487-111">Create primary node type with 5 nodes and specifying placement properties, capacities, application and ephemeral ports.</span></span>

## <span data-ttu-id="06487-112">參數</span><span class="sxs-lookup"><span data-stu-id="06487-112">PARAMETERS</span></span>

### <span data-ttu-id="06487-113">-ApplicationEndPort</span><span class="sxs-lookup"><span data-stu-id="06487-113">-ApplicationEndPort</span></span>
<span data-ttu-id="06487-114">埠範圍的應用程式結束埠。</span><span class="sxs-lookup"><span data-stu-id="06487-114">Application End port of a range of ports.</span></span>

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

### <span data-ttu-id="06487-115">-ApplicationStartPort</span><span class="sxs-lookup"><span data-stu-id="06487-115">-ApplicationStartPort</span></span>
<span data-ttu-id="06487-116">埠範圍的應用程式啟動埠。</span><span class="sxs-lookup"><span data-stu-id="06487-116">Application start port of a range of ports.</span></span>

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

### <span data-ttu-id="06487-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06487-117">-AsJob</span></span>
<span data-ttu-id="06487-118">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="06487-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="06487-119">-容量</span><span class="sxs-lookup"><span data-stu-id="06487-119">-Capacity</span></span>
<span data-ttu-id="06487-120">針對節點類型中的節點套用的容量標籤是鍵/值對，而 [群集資源管理器] 會使用這些標籤來瞭解節點擁有的資源數量。</span><span class="sxs-lookup"><span data-stu-id="06487-120">Capacity tags applied to the nodes in the node type as key/value pairs, the cluster resource manager uses these tags to understand how much resource a node has.</span></span>
<span data-ttu-id="06487-121">更新這將會覆寫目前的值。</span><span class="sxs-lookup"><span data-stu-id="06487-121">Updating this will override the current values.</span></span>

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

### <span data-ttu-id="06487-122">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="06487-122">-ClusterName</span></span>
<span data-ttu-id="06487-123">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="06487-123">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="06487-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06487-124">-DefaultProfile</span></span>
<span data-ttu-id="06487-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="06487-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06487-126">-DiskSize</span><span class="sxs-lookup"><span data-stu-id="06487-126">-DiskSize</span></span>
<span data-ttu-id="06487-127">節點類型中每個 vm 的磁片大小（以 Gb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="06487-127">Disk size for each vm in the node type in GBs.</span></span>
<span data-ttu-id="06487-128">預設100。</span><span class="sxs-lookup"><span data-stu-id="06487-128">Default 100.</span></span>

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

### <span data-ttu-id="06487-129">-EphemeralEndPort</span><span class="sxs-lookup"><span data-stu-id="06487-129">-EphemeralEndPort</span></span>
<span data-ttu-id="06487-130">埠範圍的暫時結束埠。</span><span class="sxs-lookup"><span data-stu-id="06487-130">Ephemeral end port of a range of ports.</span></span>

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

### <span data-ttu-id="06487-131">-EphemeralStartPort</span><span class="sxs-lookup"><span data-stu-id="06487-131">-EphemeralStartPort</span></span>
<span data-ttu-id="06487-132">埠範圍的暫時啟動埠。</span><span class="sxs-lookup"><span data-stu-id="06487-132">Ephemeral start port of a range of ports.</span></span>

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

### <span data-ttu-id="06487-133">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="06487-133">-InstanceCount</span></span>
<span data-ttu-id="06487-134">節點類型中的節點數目。</span><span class="sxs-lookup"><span data-stu-id="06487-134">The number of nodes in the node type.</span></span>

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

### <span data-ttu-id="06487-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="06487-135">-Name</span></span>
<span data-ttu-id="06487-136">指定節點類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="06487-136">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="06487-137">-PlacementProperty</span><span class="sxs-lookup"><span data-stu-id="06487-137">-PlacementProperty</span></span>
<span data-ttu-id="06487-138">將位置標記套用至節點類型中的節點做為索引鍵/值組，可以用來指出特定服務 (工作負荷) 應該如何執行。</span><span class="sxs-lookup"><span data-stu-id="06487-138">Placement tags applied to nodes in the node type as key/value pairs, which can be used to indicate where certain services (workload) should run.</span></span>
<span data-ttu-id="06487-139">更新這將會覆寫目前的值。</span><span class="sxs-lookup"><span data-stu-id="06487-139">Updating this will override the current values.</span></span>

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

### <span data-ttu-id="06487-140">-主要</span><span class="sxs-lookup"><span data-stu-id="06487-140">-Primary</span></span>
<span data-ttu-id="06487-141">指定節點類型是否為主要節點。</span><span class="sxs-lookup"><span data-stu-id="06487-141">Specify if the node type is primary.</span></span>
<span data-ttu-id="06487-142">在這個節點類型上，將會執行系統服務。</span><span class="sxs-lookup"><span data-stu-id="06487-142">On this node type will run system services.</span></span>
<span data-ttu-id="06487-143">只能將一個節點類型標示為主要。</span><span class="sxs-lookup"><span data-stu-id="06487-143">Only one node type should be marked as primary.</span></span>
<span data-ttu-id="06487-144">無法刪除或變更現有群集的主要節點類型。</span><span class="sxs-lookup"><span data-stu-id="06487-144">Primary node type cannot be deleted or changed for existing clusters.</span></span>

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

### <span data-ttu-id="06487-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06487-145">-ResourceGroupName</span></span>
<span data-ttu-id="06487-146">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="06487-146">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="06487-147">-VmImageOffer</span><span class="sxs-lookup"><span data-stu-id="06487-147">-VmImageOffer</span></span>
<span data-ttu-id="06487-148">Azure 虛擬機器 Marketplace 影像的優惠類型。</span><span class="sxs-lookup"><span data-stu-id="06487-148">The offer type of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="06487-149">預設值： WindowsServer。</span><span class="sxs-lookup"><span data-stu-id="06487-149">Default: WindowsServer.</span></span>

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

### <span data-ttu-id="06487-150">-VmImagePublisher</span><span class="sxs-lookup"><span data-stu-id="06487-150">-VmImagePublisher</span></span>
<span data-ttu-id="06487-151">Azure 虛擬機器 Marketplace 影像的發行者。</span><span class="sxs-lookup"><span data-stu-id="06487-151">The publisher of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="06487-152">預設值： MicrosoftWindowsServer。</span><span class="sxs-lookup"><span data-stu-id="06487-152">Default: MicrosoftWindowsServer.</span></span>

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

### <span data-ttu-id="06487-153">-VmImageSku</span><span class="sxs-lookup"><span data-stu-id="06487-153">-VmImageSku</span></span>
<span data-ttu-id="06487-154">Azure 虛擬機器 Marketplace 影像的 SKU。</span><span class="sxs-lookup"><span data-stu-id="06487-154">The SKU of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="06487-155">預設值： 2019-資料中心。</span><span class="sxs-lookup"><span data-stu-id="06487-155">Default: 2019-Datacenter.</span></span>

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

### <span data-ttu-id="06487-156">-VmImageVersion</span><span class="sxs-lookup"><span data-stu-id="06487-156">-VmImageVersion</span></span>
<span data-ttu-id="06487-157">Azure 虛擬機器 Marketplace 影像的版本。</span><span class="sxs-lookup"><span data-stu-id="06487-157">The version of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="06487-158">預設值：最新版本。</span><span class="sxs-lookup"><span data-stu-id="06487-158">Default: latest.</span></span>

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

### <span data-ttu-id="06487-159">-VmSize</span><span class="sxs-lookup"><span data-stu-id="06487-159">-VmSize</span></span>
<span data-ttu-id="06487-160">池中的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="06487-160">The size of virtual machines in the pool.</span></span>
<span data-ttu-id="06487-161">池中的所有虛擬機器都是相同的大小。</span><span class="sxs-lookup"><span data-stu-id="06487-161">All virtual machines in a pool are the same size.</span></span>
<span data-ttu-id="06487-162">預設： Standard_D2。</span><span class="sxs-lookup"><span data-stu-id="06487-162">Default: Standard_D2.</span></span>

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

### <span data-ttu-id="06487-163">-確認</span><span class="sxs-lookup"><span data-stu-id="06487-163">-Confirm</span></span>
<span data-ttu-id="06487-164">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="06487-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06487-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06487-165">-WhatIf</span></span>
<span data-ttu-id="06487-166">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="06487-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06487-167">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="06487-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06487-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06487-168">CommonParameters</span></span>
<span data-ttu-id="06487-169">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="06487-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06487-170">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="06487-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06487-171">輸入</span><span class="sxs-lookup"><span data-stu-id="06487-171">INPUTS</span></span>

### <span data-ttu-id="06487-172">System.object</span><span class="sxs-lookup"><span data-stu-id="06487-172">System.String</span></span>

## <span data-ttu-id="06487-173">輸出</span><span class="sxs-lookup"><span data-stu-id="06487-173">OUTPUTS</span></span>

### <span data-ttu-id="06487-174">PSManagedNodeType 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="06487-174">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="06487-175">筆記</span><span class="sxs-lookup"><span data-stu-id="06487-175">NOTES</span></span>

## <span data-ttu-id="06487-176">相關連結</span><span class="sxs-lookup"><span data-stu-id="06487-176">RELATED LINKS</span></span>
