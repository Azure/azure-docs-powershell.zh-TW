---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksNodePool.md
ms.openlocfilehash: 77125022002f09233154ba468f22a28228219e04
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281895"
---
# <span data-ttu-id="4bacc-101">New-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="4bacc-101">New-AzAksNodePool</span></span>

## <span data-ttu-id="4bacc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4bacc-102">SYNOPSIS</span></span>
<span data-ttu-id="4bacc-103">在指定的群集中建立新的節點池。</span><span class="sxs-lookup"><span data-stu-id="4bacc-103">Create a new node pool in specified cluster.</span></span>

## <span data-ttu-id="4bacc-104">句法</span><span class="sxs-lookup"><span data-stu-id="4bacc-104">SYNTAX</span></span>

### <span data-ttu-id="4bacc-105">defaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="4bacc-105">defaultParameterSet</span></span>
```
New-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-Count <Int32>]
 [-OsDiskSize <Int32>] [-VmSize <String>] [-VnetSubnetID <String>] [-MaxPodCount <Int32>] [-OsType <String>]
 [-ScaleSetPriority <String>] [-ScaleSetEvictionPolicy <String>] [-VmSetType <String>] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bacc-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4bacc-106">ParentObjectParameterSet</span></span>
```
New-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-Count <Int32>] [-OsDiskSize <Int32>]
 [-VmSize <String>] [-VnetSubnetID <String>] [-MaxPodCount <Int32>] [-OsType <String>]
 [-ScaleSetPriority <String>] [-ScaleSetEvictionPolicy <String>] [-VmSetType <String>] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bacc-107">說明</span><span class="sxs-lookup"><span data-stu-id="4bacc-107">DESCRIPTION</span></span>
<span data-ttu-id="4bacc-108">在指定的群集中建立新的節點池。</span><span class="sxs-lookup"><span data-stu-id="4bacc-108">Create a new node pool in specified cluster.</span></span>

## <span data-ttu-id="4bacc-109">示例</span><span class="sxs-lookup"><span data-stu-id="4bacc-109">EXAMPLES</span></span>

### <span data-ttu-id="4bacc-110">使用預設參數建立節點池</span><span class="sxs-lookup"><span data-stu-id="4bacc-110">Create node pool with default parameters</span></span>
```powershell
PS C:\> New-AzAksNodePool -ResourceGroupName myResouceGroup -ClusterName myCluster -Name mydefault
```

### <span data-ttu-id="4bacc-111">在 AKS 上建立 Windows Server 容器</span><span class="sxs-lookup"><span data-stu-id="4bacc-111">Create Windows Server container on an AKS</span></span>
```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="4bacc-112">參數</span><span class="sxs-lookup"><span data-stu-id="4bacc-112">PARAMETERS</span></span>

### <span data-ttu-id="4bacc-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4bacc-113">-ClusterName</span></span>
<span data-ttu-id="4bacc-114">受管理的群集資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="4bacc-114">The name of the managed cluster resource.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bacc-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="4bacc-115">-ClusterObject</span></span>
<span data-ttu-id="4bacc-116">指定要在其中建立節點池的群集物件。</span><span class="sxs-lookup"><span data-stu-id="4bacc-116">Specify cluster object in which to create node pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4bacc-117">-Count</span><span class="sxs-lookup"><span data-stu-id="4bacc-117">-Count</span></span>
<span data-ttu-id="4bacc-118">節點池的預設節點數。</span><span class="sxs-lookup"><span data-stu-id="4bacc-118">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="4bacc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bacc-119">-DefaultProfile</span></span>
<span data-ttu-id="4bacc-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4bacc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bacc-121">-EnableAutoScaling</span><span class="sxs-lookup"><span data-stu-id="4bacc-121">-EnableAutoScaling</span></span>
<span data-ttu-id="4bacc-122">是否要啟用自動 scaler</span><span class="sxs-lookup"><span data-stu-id="4bacc-122">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="4bacc-123">-Force</span><span class="sxs-lookup"><span data-stu-id="4bacc-123">-Force</span></span>
<span data-ttu-id="4bacc-124">建立節點池（即使已存在）</span><span class="sxs-lookup"><span data-stu-id="4bacc-124">Create node pool even if it already exists</span></span>

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

### <span data-ttu-id="4bacc-125">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="4bacc-125">-KubernetesVersion</span></span>
<span data-ttu-id="4bacc-126">要用來建立群集的 Kubernetes 版本。</span><span class="sxs-lookup"><span data-stu-id="4bacc-126">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="4bacc-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="4bacc-127">-MaxCount</span></span>
<span data-ttu-id="4bacc-128">自動調整的最大節點數</span><span class="sxs-lookup"><span data-stu-id="4bacc-128">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="4bacc-129">-MaxPodCount</span><span class="sxs-lookup"><span data-stu-id="4bacc-129">-MaxPodCount</span></span>
<span data-ttu-id="4bacc-130">可在節點上執行的箱數上限。</span><span class="sxs-lookup"><span data-stu-id="4bacc-130">Maximum number of pods that can run on node.</span></span>

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

### <span data-ttu-id="4bacc-131">-MinCount</span><span class="sxs-lookup"><span data-stu-id="4bacc-131">-MinCount</span></span>
<span data-ttu-id="4bacc-132">自動縮放的最小節點數。</span><span class="sxs-lookup"><span data-stu-id="4bacc-132">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="4bacc-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="4bacc-133">-Name</span></span>
<span data-ttu-id="4bacc-134">節點池的名稱。</span><span class="sxs-lookup"><span data-stu-id="4bacc-134">The name of the node pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bacc-135">-OsDiskSize</span><span class="sxs-lookup"><span data-stu-id="4bacc-135">-OsDiskSize</span></span>
<span data-ttu-id="4bacc-136">節點池的預設節點數。</span><span class="sxs-lookup"><span data-stu-id="4bacc-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="4bacc-137">-OsType</span><span class="sxs-lookup"><span data-stu-id="4bacc-137">-OsType</span></span>
<span data-ttu-id="4bacc-138">要用來指定 os 類型的 OsType。</span><span class="sxs-lookup"><span data-stu-id="4bacc-138">OsType to be used to specify os type.</span></span>
<span data-ttu-id="4bacc-139">選擇 [Linux] 和 [Windows]。</span><span class="sxs-lookup"><span data-stu-id="4bacc-139">Choose from Linux and Windows.</span></span>
<span data-ttu-id="4bacc-140">預設為 Linux。</span><span class="sxs-lookup"><span data-stu-id="4bacc-140">Default to Linux.</span></span>

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

### <span data-ttu-id="4bacc-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bacc-141">-ResourceGroupName</span></span>
<span data-ttu-id="4bacc-142">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4bacc-142">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bacc-143">-ScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="4bacc-143">-ScaleSetEvictionPolicy</span></span>
<span data-ttu-id="4bacc-144">ScaleSetEvictionPolicy，用於針對低優先順序的虛擬機器縮放集指定逐出原則。</span><span class="sxs-lookup"><span data-stu-id="4bacc-144">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span>
<span data-ttu-id="4bacc-145">預設為 [刪除]。</span><span class="sxs-lookup"><span data-stu-id="4bacc-145">Default to Delete.</span></span>

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

### <span data-ttu-id="4bacc-146">-ScaleSetPriority</span><span class="sxs-lookup"><span data-stu-id="4bacc-146">-ScaleSetPriority</span></span>
<span data-ttu-id="4bacc-147">要用來指定虛擬電腦比例集優先順序的 ScaleSetPriority。</span><span class="sxs-lookup"><span data-stu-id="4bacc-147">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span>
<span data-ttu-id="4bacc-148">預設為 [一般]。</span><span class="sxs-lookup"><span data-stu-id="4bacc-148">Default to regular.</span></span>

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

### <span data-ttu-id="4bacc-149">-VmSetType</span><span class="sxs-lookup"><span data-stu-id="4bacc-149">-VmSetType</span></span>
<span data-ttu-id="4bacc-150">代表節點池的類型。</span><span class="sxs-lookup"><span data-stu-id="4bacc-150">Represents types of an node pool.</span></span>
<span data-ttu-id="4bacc-151">可能的值包括： "VirtualMachineScaleSets"、"AvailabilitySet"</span><span class="sxs-lookup"><span data-stu-id="4bacc-151">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

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

### <span data-ttu-id="4bacc-152">-VmSize</span><span class="sxs-lookup"><span data-stu-id="4bacc-152">-VmSize</span></span>
<span data-ttu-id="4bacc-153">虛擬機器的大小。</span><span class="sxs-lookup"><span data-stu-id="4bacc-153">The size of the Virtual Machine.</span></span> <span data-ttu-id="4bacc-154">預設值為 [Standard_D2_v2]。</span><span class="sxs-lookup"><span data-stu-id="4bacc-154">Default value is Standard_D2_v2.</span></span>

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

### <span data-ttu-id="4bacc-155">-VnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="4bacc-155">-VnetSubnetID</span></span>
<span data-ttu-id="4bacc-156">VNet SubnetID 會指定 VNet 的子網識別碼。</span><span class="sxs-lookup"><span data-stu-id="4bacc-156">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

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

### <span data-ttu-id="4bacc-157">-確認</span><span class="sxs-lookup"><span data-stu-id="4bacc-157">-Confirm</span></span>
<span data-ttu-id="4bacc-158">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4bacc-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bacc-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bacc-159">-WhatIf</span></span>
<span data-ttu-id="4bacc-160">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4bacc-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bacc-161">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4bacc-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bacc-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bacc-162">CommonParameters</span></span>
<span data-ttu-id="4bacc-163">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4bacc-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bacc-164">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4bacc-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bacc-165">輸入</span><span class="sxs-lookup"><span data-stu-id="4bacc-165">INPUTS</span></span>

### <span data-ttu-id="4bacc-166">PSKubernetesCluster 中的 Aks。</span><span class="sxs-lookup"><span data-stu-id="4bacc-166">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="4bacc-167">輸出</span><span class="sxs-lookup"><span data-stu-id="4bacc-167">OUTPUTS</span></span>

### <span data-ttu-id="4bacc-168">PSNodePool 中的 Aks。</span><span class="sxs-lookup"><span data-stu-id="4bacc-168">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="4bacc-169">筆記</span><span class="sxs-lookup"><span data-stu-id="4bacc-169">NOTES</span></span>

## <span data-ttu-id="4bacc-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="4bacc-170">RELATED LINKS</span></span>
