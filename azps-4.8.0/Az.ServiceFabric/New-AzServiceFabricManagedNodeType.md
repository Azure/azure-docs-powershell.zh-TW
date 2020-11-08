---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 3e89e807acfb2507834686574931011bf398c76c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971718"
---
# <span data-ttu-id="e8511-101">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="e8511-101">New-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="e8511-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8511-102">SYNOPSIS</span></span>
<span data-ttu-id="e8511-103">建立新的節點類型資源。</span><span class="sxs-lookup"><span data-stu-id="e8511-103">Create new node type resource.</span></span>

## <span data-ttu-id="e8511-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8511-104">SYNTAX</span></span>

```
New-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -InstanceCount <Int32> [-Primary] [-DiskSize <Int32>] [-ApplicationStartPort <Int32>]
 [-ApplicationEndPort <Int32>] [-EphemeralStartPort <Int32>] [-EphemeralEndPort <Int32>] [-VmSize <String>]
 [-VmImagePublisher <String>] [-VmImageOffer <String>] [-VmImageSku <String>] [-VmImageVersion <String>]
 [-Capacity <Hashtable>] [-PlacementProperty <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8511-105">說明</span><span class="sxs-lookup"><span data-stu-id="e8511-105">DESCRIPTION</span></span>
<span data-ttu-id="e8511-106">針對特定的群集建立新的節點類型資源。</span><span class="sxs-lookup"><span data-stu-id="e8511-106">Create new node type resource for an specific cluster.</span></span>

## <span data-ttu-id="e8511-107">示例</span><span class="sxs-lookup"><span data-stu-id="e8511-107">EXAMPLES</span></span>

### <span data-ttu-id="e8511-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e8511-108">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
New-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName -Primary -InstanceCount 3
```

<span data-ttu-id="e8511-109">建立具有3個節點的主要節點類型。</span><span class="sxs-lookup"><span data-stu-id="e8511-109">Create primary node type with 3 nodes.</span></span>

### <span data-ttu-id="e8511-110">範例2</span><span class="sxs-lookup"><span data-stu-id="e8511-110">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
New-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName -InstanceCount 5 -Primary -PlacementProperty @{NodeColor="Green";SomeProperty="5";} -Capacity @{ClientConnections="65536";} -ApplicationStartPort 20575 -ApplicationEndPort 20605 -EphemeralStartPort 20606 -EphemeralEndPort 20861
```

<span data-ttu-id="e8511-111">建立具有5個節點的主要節點類型，並指定放置屬性、容量、應用程式和暫時埠。</span><span class="sxs-lookup"><span data-stu-id="e8511-111">Create primary node type with 5 nodes and specifying placement properties, capacities, application and ephemeral ports.</span></span>

## <span data-ttu-id="e8511-112">參數</span><span class="sxs-lookup"><span data-stu-id="e8511-112">PARAMETERS</span></span>

### <span data-ttu-id="e8511-113">-ApplicationEndPort</span><span class="sxs-lookup"><span data-stu-id="e8511-113">-ApplicationEndPort</span></span>
<span data-ttu-id="e8511-114">埠範圍的應用程式結束埠。</span><span class="sxs-lookup"><span data-stu-id="e8511-114">Application End port of a range of ports.</span></span>

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

### <span data-ttu-id="e8511-115">-ApplicationStartPort</span><span class="sxs-lookup"><span data-stu-id="e8511-115">-ApplicationStartPort</span></span>
<span data-ttu-id="e8511-116">埠範圍的應用程式啟動埠。</span><span class="sxs-lookup"><span data-stu-id="e8511-116">Application start port of a range of ports.</span></span>

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

### <span data-ttu-id="e8511-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e8511-117">-AsJob</span></span>
<span data-ttu-id="e8511-118">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="e8511-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e8511-119">-容量</span><span class="sxs-lookup"><span data-stu-id="e8511-119">-Capacity</span></span>
<span data-ttu-id="e8511-120">針對節點類型中的節點套用的容量標籤是鍵/值對，而 [群集資源管理器] 會使用這些標籤來瞭解節點擁有的資源數量。</span><span class="sxs-lookup"><span data-stu-id="e8511-120">Capacity tags applied to the nodes in the node type as key/value pairs, the cluster resource manager uses these tags to understand how much resource a node has.</span></span>
<span data-ttu-id="e8511-121">更新這將會覆寫目前的值。</span><span class="sxs-lookup"><span data-stu-id="e8511-121">Updating this will override the current values.</span></span>

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

### <span data-ttu-id="e8511-122">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e8511-122">-ClusterName</span></span>
<span data-ttu-id="e8511-123">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8511-123">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="e8511-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8511-124">-DefaultProfile</span></span>
<span data-ttu-id="e8511-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8511-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8511-126">-DiskSize</span><span class="sxs-lookup"><span data-stu-id="e8511-126">-DiskSize</span></span>
<span data-ttu-id="e8511-127">節點類型中每個 vm 的磁片大小（以 Gb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="e8511-127">Disk size for each vm in the node type in GBs.</span></span>
<span data-ttu-id="e8511-128">預設100。</span><span class="sxs-lookup"><span data-stu-id="e8511-128">Default 100.</span></span>

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

### <span data-ttu-id="e8511-129">-EphemeralEndPort</span><span class="sxs-lookup"><span data-stu-id="e8511-129">-EphemeralEndPort</span></span>
<span data-ttu-id="e8511-130">埠範圍的暫時結束埠。</span><span class="sxs-lookup"><span data-stu-id="e8511-130">Ephemeral end port of a range of ports.</span></span>

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

### <span data-ttu-id="e8511-131">-EphemeralStartPort</span><span class="sxs-lookup"><span data-stu-id="e8511-131">-EphemeralStartPort</span></span>
<span data-ttu-id="e8511-132">埠範圍的暫時啟動埠。</span><span class="sxs-lookup"><span data-stu-id="e8511-132">Ephemeral start port of a range of ports.</span></span>

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

### <span data-ttu-id="e8511-133">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="e8511-133">-InstanceCount</span></span>
<span data-ttu-id="e8511-134">節點類型中的節點數目。</span><span class="sxs-lookup"><span data-stu-id="e8511-134">The number of nodes in the node type.</span></span>

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

### <span data-ttu-id="e8511-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="e8511-135">-Name</span></span>
<span data-ttu-id="e8511-136">指定節點類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8511-136">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="e8511-137">-PlacementProperty</span><span class="sxs-lookup"><span data-stu-id="e8511-137">-PlacementProperty</span></span>
<span data-ttu-id="e8511-138">將位置標記套用至節點類型中的節點做為索引鍵/值組，可以用來指出特定服務 (工作負荷) 應該如何執行。</span><span class="sxs-lookup"><span data-stu-id="e8511-138">Placement tags applied to nodes in the node type as key/value pairs, which can be used to indicate where certain services (workload) should run.</span></span>
<span data-ttu-id="e8511-139">更新這將會覆寫目前的值。</span><span class="sxs-lookup"><span data-stu-id="e8511-139">Updating this will override the current values.</span></span>

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

### <span data-ttu-id="e8511-140">-主要</span><span class="sxs-lookup"><span data-stu-id="e8511-140">-Primary</span></span>
<span data-ttu-id="e8511-141">指定節點類型是否為主要節點。</span><span class="sxs-lookup"><span data-stu-id="e8511-141">Specify if the node type is primary.</span></span>
<span data-ttu-id="e8511-142">在這個節點類型上，將會執行系統服務。</span><span class="sxs-lookup"><span data-stu-id="e8511-142">On this node type will run system services.</span></span>
<span data-ttu-id="e8511-143">只能將一個節點類型標示為主要。</span><span class="sxs-lookup"><span data-stu-id="e8511-143">Only one node type should be marked as primary.</span></span>
<span data-ttu-id="e8511-144">無法刪除或變更現有群集的主要節點類型。</span><span class="sxs-lookup"><span data-stu-id="e8511-144">Primary node type cannot be deleted or changed for existing clusters.</span></span>

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

### <span data-ttu-id="e8511-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8511-145">-ResourceGroupName</span></span>
<span data-ttu-id="e8511-146">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8511-146">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="e8511-147">-VmImageOffer</span><span class="sxs-lookup"><span data-stu-id="e8511-147">-VmImageOffer</span></span>
<span data-ttu-id="e8511-148">Azure 虛擬機器 Marketplace 影像的優惠類型。</span><span class="sxs-lookup"><span data-stu-id="e8511-148">The offer type of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="e8511-149">預設值： WindowsServer。</span><span class="sxs-lookup"><span data-stu-id="e8511-149">Default: WindowsServer.</span></span>

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

### <span data-ttu-id="e8511-150">-VmImagePublisher</span><span class="sxs-lookup"><span data-stu-id="e8511-150">-VmImagePublisher</span></span>
<span data-ttu-id="e8511-151">Azure 虛擬機器 Marketplace 影像的發行者。</span><span class="sxs-lookup"><span data-stu-id="e8511-151">The publisher of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="e8511-152">預設值： MicrosoftWindowsServer。</span><span class="sxs-lookup"><span data-stu-id="e8511-152">Default: MicrosoftWindowsServer.</span></span>

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

### <span data-ttu-id="e8511-153">-VmImageSku</span><span class="sxs-lookup"><span data-stu-id="e8511-153">-VmImageSku</span></span>
<span data-ttu-id="e8511-154">Azure 虛擬機器 Marketplace 影像的 SKU。</span><span class="sxs-lookup"><span data-stu-id="e8511-154">The SKU of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="e8511-155">預設值： 2019-資料中心。</span><span class="sxs-lookup"><span data-stu-id="e8511-155">Default: 2019-Datacenter.</span></span>

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

### <span data-ttu-id="e8511-156">-VmImageVersion</span><span class="sxs-lookup"><span data-stu-id="e8511-156">-VmImageVersion</span></span>
<span data-ttu-id="e8511-157">Azure 虛擬機器 Marketplace 影像的版本。</span><span class="sxs-lookup"><span data-stu-id="e8511-157">The version of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="e8511-158">預設值：最新版本。</span><span class="sxs-lookup"><span data-stu-id="e8511-158">Default: latest.</span></span>

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

### <span data-ttu-id="e8511-159">-VmSize</span><span class="sxs-lookup"><span data-stu-id="e8511-159">-VmSize</span></span>
<span data-ttu-id="e8511-160">池中的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="e8511-160">The size of virtual machines in the pool.</span></span>
<span data-ttu-id="e8511-161">池中的所有虛擬機器都是相同的大小。</span><span class="sxs-lookup"><span data-stu-id="e8511-161">All virtual machines in a pool are the same size.</span></span>
<span data-ttu-id="e8511-162">預設： Standard_D2。</span><span class="sxs-lookup"><span data-stu-id="e8511-162">Default: Standard_D2.</span></span>

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

### <span data-ttu-id="e8511-163">-確認</span><span class="sxs-lookup"><span data-stu-id="e8511-163">-Confirm</span></span>
<span data-ttu-id="e8511-164">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e8511-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8511-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8511-165">-WhatIf</span></span>
<span data-ttu-id="e8511-166">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e8511-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8511-167">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e8511-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8511-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8511-168">CommonParameters</span></span>
<span data-ttu-id="e8511-169">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8511-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8511-170">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e8511-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8511-171">輸入</span><span class="sxs-lookup"><span data-stu-id="e8511-171">INPUTS</span></span>

### <span data-ttu-id="e8511-172">System.object</span><span class="sxs-lookup"><span data-stu-id="e8511-172">System.String</span></span>

## <span data-ttu-id="e8511-173">輸出</span><span class="sxs-lookup"><span data-stu-id="e8511-173">OUTPUTS</span></span>

### <span data-ttu-id="e8511-174">PSManagedNodeType 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="e8511-174">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="e8511-175">筆記</span><span class="sxs-lookup"><span data-stu-id="e8511-175">NOTES</span></span>

## <span data-ttu-id="e8511-176">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8511-176">RELATED LINKS</span></span>
