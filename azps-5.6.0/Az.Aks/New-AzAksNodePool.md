---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/new-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksNodePool.md
ms.openlocfilehash: 07944177b7c92ff4c515b6d9dcd01d11d3c5a888
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904562"
---
# <span data-ttu-id="1f085-101">New-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="1f085-101">New-AzAksNodePool</span></span>

## <span data-ttu-id="1f085-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1f085-102">SYNOPSIS</span></span>
<span data-ttu-id="1f085-103">在指定的組集中建立新節點集區。</span><span class="sxs-lookup"><span data-stu-id="1f085-103">Create a new node pool in specified cluster.</span></span>

## <span data-ttu-id="1f085-104">語法</span><span class="sxs-lookup"><span data-stu-id="1f085-104">SYNTAX</span></span>

### <span data-ttu-id="1f085-105">defaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f085-105">defaultParameterSet</span></span>
```
New-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-Count <Int32>]
 [-OsDiskSize <Int32>] [-VmSize <String>] [-VnetSubnetID <String>] [-MaxPodCount <Int32>] [-OsType <String>]
 [-ScaleSetPriority <String>] [-ScaleSetEvictionPolicy <String>] [-VmSetType <String>] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f085-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f085-106">ParentObjectParameterSet</span></span>
```
New-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-Count <Int32>] [-OsDiskSize <Int32>]
 [-VmSize <String>] [-VnetSubnetID <String>] [-MaxPodCount <Int32>] [-OsType <String>]
 [-ScaleSetPriority <String>] [-ScaleSetEvictionPolicy <String>] [-VmSetType <String>] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f085-107">描述</span><span class="sxs-lookup"><span data-stu-id="1f085-107">DESCRIPTION</span></span>
<span data-ttu-id="1f085-108">在指定的組集中建立新節點集區。</span><span class="sxs-lookup"><span data-stu-id="1f085-108">Create a new node pool in specified cluster.</span></span>

## <span data-ttu-id="1f085-109">例子</span><span class="sxs-lookup"><span data-stu-id="1f085-109">EXAMPLES</span></span>

### <span data-ttu-id="1f085-110">使用預設參數建立節點區</span><span class="sxs-lookup"><span data-stu-id="1f085-110">Create node pool with default parameters</span></span>
```powershell
PS C:\> New-AzAksNodePool -ResourceGroupName myResouceGroup -ClusterName myCluster -Name mydefault
```

### <span data-ttu-id="1f085-111">在 AKS 上建立 Windows Server 容器</span><span class="sxs-lookup"><span data-stu-id="1f085-111">Create Windows Server container on an AKS</span></span>
```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="1f085-112">參數</span><span class="sxs-lookup"><span data-stu-id="1f085-112">PARAMETERS</span></span>

### <span data-ttu-id="1f085-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1f085-113">-ClusterName</span></span>
<span data-ttu-id="1f085-114">受管理的組群資源名稱。</span><span class="sxs-lookup"><span data-stu-id="1f085-114">The name of the managed cluster resource.</span></span>

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

### <span data-ttu-id="1f085-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="1f085-115">-ClusterObject</span></span>
<span data-ttu-id="1f085-116">指定要建立節點集區之集區物件的集區物件。</span><span class="sxs-lookup"><span data-stu-id="1f085-116">Specify cluster object in which to create node pool.</span></span>

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

### <span data-ttu-id="1f085-117">-Count</span><span class="sxs-lookup"><span data-stu-id="1f085-117">-Count</span></span>
<span data-ttu-id="1f085-118">節點資料庫的預設節點數目。</span><span class="sxs-lookup"><span data-stu-id="1f085-118">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="1f085-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f085-119">-DefaultProfile</span></span>
<span data-ttu-id="1f085-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1f085-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f085-121">-EnableAutoScaling</span><span class="sxs-lookup"><span data-stu-id="1f085-121">-EnableAutoScaling</span></span>
<span data-ttu-id="1f085-122">是否要啟用自動縮放</span><span class="sxs-lookup"><span data-stu-id="1f085-122">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="1f085-123">-強制</span><span class="sxs-lookup"><span data-stu-id="1f085-123">-Force</span></span>
<span data-ttu-id="1f085-124">建立節點區，即使它已經存在</span><span class="sxs-lookup"><span data-stu-id="1f085-124">Create node pool even if it already exists</span></span>

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

### <span data-ttu-id="1f085-125">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="1f085-125">-KubernetesVersion</span></span>
<span data-ttu-id="1f085-126">要用於建立該組集的 Kubernetes 版本。</span><span class="sxs-lookup"><span data-stu-id="1f085-126">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="1f085-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="1f085-127">-MaxCount</span></span>
<span data-ttu-id="1f085-128">自動縮放的節點數目上限</span><span class="sxs-lookup"><span data-stu-id="1f085-128">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="1f085-129">-MaxPodCount</span><span class="sxs-lookup"><span data-stu-id="1f085-129">-MaxPodCount</span></span>
<span data-ttu-id="1f085-130">可在節點上執行之窗格數目上限。</span><span class="sxs-lookup"><span data-stu-id="1f085-130">Maximum number of pods that can run on node.</span></span>

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

### <span data-ttu-id="1f085-131">-MinCount</span><span class="sxs-lookup"><span data-stu-id="1f085-131">-MinCount</span></span>
<span data-ttu-id="1f085-132">可自動縮放的節點數目最低。</span><span class="sxs-lookup"><span data-stu-id="1f085-132">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="1f085-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="1f085-133">-Name</span></span>
<span data-ttu-id="1f085-134">節點組名。</span><span class="sxs-lookup"><span data-stu-id="1f085-134">The name of the node pool.</span></span>

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

### <span data-ttu-id="1f085-135">-Os前小數</span><span class="sxs-lookup"><span data-stu-id="1f085-135">-OsDiskSize</span></span>
<span data-ttu-id="1f085-136">節點資料庫的預設節點數目。</span><span class="sxs-lookup"><span data-stu-id="1f085-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="1f085-137">-OsType</span><span class="sxs-lookup"><span data-stu-id="1f085-137">-OsType</span></span>
<span data-ttu-id="1f085-138">用來指定 os 類型的 OsType。</span><span class="sxs-lookup"><span data-stu-id="1f085-138">OsType to be used to specify os type.</span></span>
<span data-ttu-id="1f085-139">從 Linux 和 Windows 中選擇。</span><span class="sxs-lookup"><span data-stu-id="1f085-139">Choose from Linux and Windows.</span></span>
<span data-ttu-id="1f085-140">預設為 Linux。</span><span class="sxs-lookup"><span data-stu-id="1f085-140">Default to Linux.</span></span>

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

### <span data-ttu-id="1f085-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f085-141">-ResourceGroupName</span></span>
<span data-ttu-id="1f085-142">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1f085-142">The name of the resource group.</span></span>

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

### <span data-ttu-id="1f085-143">-ScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="1f085-143">-ScaleSetEvictionPolicy</span></span>
<span data-ttu-id="1f085-144">要用來指定低優先順序虛擬機器縮放集的部署策略的 ScaleSetEvictionPolicy。</span><span class="sxs-lookup"><span data-stu-id="1f085-144">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span>
<span data-ttu-id="1f085-145">預設為 Delete。</span><span class="sxs-lookup"><span data-stu-id="1f085-145">Default to Delete.</span></span>

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

### <span data-ttu-id="1f085-146">-ScaleSetPriority</span><span class="sxs-lookup"><span data-stu-id="1f085-146">-ScaleSetPriority</span></span>
<span data-ttu-id="1f085-147">用來指定虛擬機器縮放比例集優先順序的 ScaleSetPriority。</span><span class="sxs-lookup"><span data-stu-id="1f085-147">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span>
<span data-ttu-id="1f085-148">預設為一般。</span><span class="sxs-lookup"><span data-stu-id="1f085-148">Default to regular.</span></span>

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

### <span data-ttu-id="1f085-149">-VmSetType</span><span class="sxs-lookup"><span data-stu-id="1f085-149">-VmSetType</span></span>
<span data-ttu-id="1f085-150">代表節點區類型。</span><span class="sxs-lookup"><span data-stu-id="1f085-150">Represents types of an node pool.</span></span>
<span data-ttu-id="1f085-151">可能的值包括：「VirtualMachineScaleSets'、'AvailabilitySet'</span><span class="sxs-lookup"><span data-stu-id="1f085-151">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

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

### <span data-ttu-id="1f085-152">-VmSize</span><span class="sxs-lookup"><span data-stu-id="1f085-152">-VmSize</span></span>
<span data-ttu-id="1f085-153">虛擬機器的大小。</span><span class="sxs-lookup"><span data-stu-id="1f085-153">The size of the Virtual Machine.</span></span> <span data-ttu-id="1f085-154">預設值會Standard_D2_v2。</span><span class="sxs-lookup"><span data-stu-id="1f085-154">Default value is Standard_D2_v2.</span></span>

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

### <span data-ttu-id="1f085-155">-VnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="1f085-155">-VnetSubnetID</span></span>
<span data-ttu-id="1f085-156">VNet 子網識別碼會指定 VNet 的子網識別碼。</span><span class="sxs-lookup"><span data-stu-id="1f085-156">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

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

### <span data-ttu-id="1f085-157">-確認</span><span class="sxs-lookup"><span data-stu-id="1f085-157">-Confirm</span></span>
<span data-ttu-id="1f085-158">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1f085-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f085-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f085-159">-WhatIf</span></span>
<span data-ttu-id="1f085-160">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1f085-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f085-161">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1f085-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f085-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f085-162">CommonParameters</span></span>
<span data-ttu-id="1f085-163">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1f085-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f085-164">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1f085-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f085-165">輸入</span><span class="sxs-lookup"><span data-stu-id="1f085-165">INPUTS</span></span>

### <span data-ttu-id="1f085-166">Microsoft.Azure.Commands.Aks.models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="1f085-166">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="1f085-167">輸出</span><span class="sxs-lookup"><span data-stu-id="1f085-167">OUTPUTS</span></span>

### <span data-ttu-id="1f085-168">Microsoft.Azure.Commands.Aks.models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="1f085-168">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="1f085-169">筆記</span><span class="sxs-lookup"><span data-stu-id="1f085-169">NOTES</span></span>

## <span data-ttu-id="1f085-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="1f085-170">RELATED LINKS</span></span>
