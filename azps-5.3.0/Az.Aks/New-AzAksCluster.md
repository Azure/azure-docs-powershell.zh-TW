---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
ms.openlocfilehash: aaab86d7943072ae861acb71ec5021bb098a48ef
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98437764"
---
# <span data-ttu-id="d4668-101">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="d4668-101">New-AzAksCluster</span></span>

## <span data-ttu-id="d4668-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d4668-102">SYNOPSIS</span></span>
<span data-ttu-id="d4668-103">建立新的 managed Kubernetes 群集。</span><span class="sxs-lookup"><span data-stu-id="d4668-103">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="d4668-104">句法</span><span class="sxs-lookup"><span data-stu-id="d4668-104">SYNTAX</span></span>

```
New-AzAksCluster [-Force] [-GenerateSshKey] [-NodeVmSetType <String>] [-NodeVnetSubnetID <String>]
 [-NodeMaxPodCount <Int32>] [-NodeSetPriority <String>] [-NodePoolMode <String>]
 [-NodeScaleSetEvictionPolicy <String>] [-AddOnNameToBeEnabled <String[]>] [-WorkspaceResourceId <String>]
 [-SubnetName <String>] [-AcrNameToAttach <String>] [-EnableRbac] [-WindowsProfileAdminUserName <String>]
 [-WindowsProfileAdminUserPassword <SecureString>] [-NetworkPlugin <String>] [-LoadBalancerSku <String>]
 [-ResourceGroupName] <String> [-Name] <String> [[-ServicePrincipalIdAndSecret] <PSCredential>]
 [-Location <String>] [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>]
 [-KubernetesVersion <String>] [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>]
 [-EnableNodeAutoScaling] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>]
 [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4668-105">說明</span><span class="sxs-lookup"><span data-stu-id="d4668-105">DESCRIPTION</span></span>

<span data-ttu-id="d4668-106"> (AKS) 群集中建立新的 Azure Kubernetes Service。</span><span class="sxs-lookup"><span data-stu-id="d4668-106">Create a new Azure Kubernetes Service(AKS) cluster.</span></span>

## <span data-ttu-id="d4668-107">示例</span><span class="sxs-lookup"><span data-stu-id="d4668-107">EXAMPLES</span></span>

### <span data-ttu-id="d4668-108">使用預設的 params 來新增 AKS。</span><span class="sxs-lookup"><span data-stu-id="d4668-108">New an AKS with default params.</span></span>

```powershell
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster
```

### <span data-ttu-id="d4668-109">在 AKS 上建立 Windows Server 容器。</span><span class="sxs-lookup"><span data-stu-id="d4668-109">Create Windows Server container on an AKS.</span></span>
<span data-ttu-id="d4668-110">若要在 AKS 上建立 Windows Server 容器，在建立 AKS 時，至少必須指定四個下列參數，且必須是及的值 `NetworkPlugin` `NodeVmSetType` `azure` `VirtualMachineScaleSets` 。</span><span class="sxs-lookup"><span data-stu-id="d4668-110">To create Windows Server container on an AKS, you must specify at least four following parameters when creating the AKS, and the value for `NetworkPlugin` and `NodeVmSetType` must be `azure` and `VirtualMachineScaleSets` respectively.</span></span>
`-WindowsProfileAdminUserName *** -WindowsProfileAdminUserPassword **_ -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets`

```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="d4668-111">參數</span><span class="sxs-lookup"><span data-stu-id="d4668-111">PARAMETERS</span></span>

### <span data-ttu-id="d4668-112">-AcrNameToAttach</span><span class="sxs-lookup"><span data-stu-id="d4668-112">-AcrNameToAttach</span></span>
<span data-ttu-id="d4668-113">將指定的 ACR 的「acrpull」角色授與 AKS 服務主體（例如 myacr）。</span><span class="sxs-lookup"><span data-stu-id="d4668-113">Grant the 'acrpull' role of the specified ACR to AKS Service Principal, e.g. myacr</span></span>

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

### <span data-ttu-id="d4668-114">-AddOnNameToBeEnabled</span><span class="sxs-lookup"><span data-stu-id="d4668-114">-AddOnNameToBeEnabled</span></span>
<span data-ttu-id="d4668-115">建立群集時要啟用的附加元件名稱。</span><span class="sxs-lookup"><span data-stu-id="d4668-115">Add-on names to be enabled when cluster is created.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4668-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4668-116">-AsJob</span></span>
<span data-ttu-id="d4668-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d4668-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d4668-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4668-118">-DefaultProfile</span></span>
<span data-ttu-id="d4668-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d4668-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4668-120">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="d4668-120">-DnsNamePrefix</span></span>
<span data-ttu-id="d4668-121">群集的 DNS 名稱首碼。</span><span class="sxs-lookup"><span data-stu-id="d4668-121">The DNS name prefix for the cluster.</span></span> <span data-ttu-id="d4668-122">如果使用者計畫新增 windows 容器，長度必須 <= 9。</span><span class="sxs-lookup"><span data-stu-id="d4668-122">The length must be <= 9 if users plan to add windows container.</span></span>

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

### <span data-ttu-id="d4668-123">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="d4668-123">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="d4668-124">是否要啟用自動 scaler</span><span class="sxs-lookup"><span data-stu-id="d4668-124">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="d4668-125">-EnableRbac</span><span class="sxs-lookup"><span data-stu-id="d4668-125">-EnableRbac</span></span>
<span data-ttu-id="d4668-126">是否要啟用 Kubernetes Role-Based 存取權</span><span class="sxs-lookup"><span data-stu-id="d4668-126">Whether to enable Kubernetes Role-Based Access</span></span>

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

### <span data-ttu-id="d4668-127">-Force</span><span class="sxs-lookup"><span data-stu-id="d4668-127">-Force</span></span>
<span data-ttu-id="d4668-128">建立群集（即使已存在）</span><span class="sxs-lookup"><span data-stu-id="d4668-128">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="d4668-129">-GenerateSshKey</span><span class="sxs-lookup"><span data-stu-id="d4668-129">-GenerateSshKey</span></span>
<span data-ttu-id="d4668-130">產生 ssh 金鑰檔案至 {HOME}/.ssh/id_rsa。</span><span class="sxs-lookup"><span data-stu-id="d4668-130">Generate ssh key file to {HOME}/.ssh/id_rsa.</span></span>

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

### <span data-ttu-id="d4668-131">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="d4668-131">-KubernetesVersion</span></span>
<span data-ttu-id="d4668-132">要用來建立群集的 Kubernetes 版本。</span><span class="sxs-lookup"><span data-stu-id="d4668-132">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="d4668-133">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="d4668-133">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="d4668-134">Linux 虛擬機器的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="d4668-134">User name for the Linux Virtual Machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AdminUserName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4668-135">-LoadBalancerSku</span><span class="sxs-lookup"><span data-stu-id="d4668-135">-LoadBalancerSku</span></span>
<span data-ttu-id="d4668-136">受管理的群集的負載平衡器 sku。</span><span class="sxs-lookup"><span data-stu-id="d4668-136">The load balancer sku for the managed cluster.</span></span>

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

### <span data-ttu-id="d4668-137">-位置</span><span class="sxs-lookup"><span data-stu-id="d4668-137">-Location</span></span>
<span data-ttu-id="d4668-138">群集的 Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="d4668-138">Azure location for the cluster.</span></span>
<span data-ttu-id="d4668-139">預設為資源群組的位置。</span><span class="sxs-lookup"><span data-stu-id="d4668-139">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="d4668-140">-名稱</span><span class="sxs-lookup"><span data-stu-id="d4668-140">-Name</span></span>
<span data-ttu-id="d4668-141">Kubernetes 受管理的群集名稱。</span><span class="sxs-lookup"><span data-stu-id="d4668-141">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4668-142">-NetworkPlugin</span><span class="sxs-lookup"><span data-stu-id="d4668-142">-NetworkPlugin</span></span>
<span data-ttu-id="d4668-143">用於建立 Kubernetes 網路的網路外掛程式。</span><span class="sxs-lookup"><span data-stu-id="d4668-143">Network plugin used for building Kubernetes network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: azure
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4668-144">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="d4668-144">-NodeCount</span></span>
<span data-ttu-id="d4668-145">節點池的預設節點數。</span><span class="sxs-lookup"><span data-stu-id="d4668-145">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="d4668-146">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="d4668-146">-NodeMaxCount</span></span>
<span data-ttu-id="d4668-147">自動調整的最大節點數</span><span class="sxs-lookup"><span data-stu-id="d4668-147">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="d4668-148">-NodeMaxPodCount</span><span class="sxs-lookup"><span data-stu-id="d4668-148">-NodeMaxPodCount</span></span>
<span data-ttu-id="d4668-149">可在節點上執行的箱數上限。</span><span class="sxs-lookup"><span data-stu-id="d4668-149">Maximum number of pods that can run on node.</span></span>

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

### <span data-ttu-id="d4668-150">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="d4668-150">-NodeMinCount</span></span>
<span data-ttu-id="d4668-151">自動縮放的最小節點數。</span><span class="sxs-lookup"><span data-stu-id="d4668-151">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="d4668-152">-NodeName</span><span class="sxs-lookup"><span data-stu-id="d4668-152">-NodeName</span></span>
<span data-ttu-id="d4668-153">[訂閱與資源群組] 內容中代理池設定檔的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="d4668-153">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="d4668-154">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="d4668-154">-NodeOsDiskSize</span></span>
<span data-ttu-id="d4668-155">節點池中每個節點的 OS 磁片大小（GB）。</span><span class="sxs-lookup"><span data-stu-id="d4668-155">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="d4668-156">最低 30 GB。</span><span class="sxs-lookup"><span data-stu-id="d4668-156">Minimum 30 GB.</span></span>

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

### <span data-ttu-id="d4668-157">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="d4668-157">-NodePoolMode</span></span>
<span data-ttu-id="d4668-158">NodePoolMode 代表節點池的模式。</span><span class="sxs-lookup"><span data-stu-id="d4668-158">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="d4668-159">-NodeScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="d4668-159">-NodeScaleSetEvictionPolicy</span></span>
<span data-ttu-id="d4668-160">ScaleSetEvictionPolicy，用於針對低優先順序的虛擬機器縮放集指定逐出原則。</span><span class="sxs-lookup"><span data-stu-id="d4668-160">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span> <span data-ttu-id="d4668-161">預設為 [刪除]。</span><span class="sxs-lookup"><span data-stu-id="d4668-161">Default to Delete.</span></span>

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

### <span data-ttu-id="d4668-162">-NodeSetPriority</span><span class="sxs-lookup"><span data-stu-id="d4668-162">-NodeSetPriority</span></span>
<span data-ttu-id="d4668-163">要用來指定虛擬電腦比例集優先順序的 ScaleSetPriority。</span><span class="sxs-lookup"><span data-stu-id="d4668-163">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span> <span data-ttu-id="d4668-164">預設為 [一般]。</span><span class="sxs-lookup"><span data-stu-id="d4668-164">Default to regular.</span></span>

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

### <span data-ttu-id="d4668-165">-NodeVmSetType</span><span class="sxs-lookup"><span data-stu-id="d4668-165">-NodeVmSetType</span></span>
<span data-ttu-id="d4668-166">AgentPoolType 代表代理程式庫的類型。</span><span class="sxs-lookup"><span data-stu-id="d4668-166">AgentPoolType represents types of an agent pool.</span></span> <span data-ttu-id="d4668-167">可能的值包括： "VirtualMachineScaleSets"、"AvailabilitySet"</span><span class="sxs-lookup"><span data-stu-id="d4668-167">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: VirtualMachineScaleSets
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4668-168">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="d4668-168">-NodeVmSize</span></span>
<span data-ttu-id="d4668-169">虛擬機器的大小。</span><span class="sxs-lookup"><span data-stu-id="d4668-169">The size of the Virtual Machine.</span></span> <span data-ttu-id="d4668-170">預設值為 [Standard_D2_v2]。</span><span class="sxs-lookup"><span data-stu-id="d4668-170">Default value is Standard_D2_v2.</span></span>

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

### <span data-ttu-id="d4668-171">-NodeVnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="d4668-171">-NodeVnetSubnetID</span></span>
<span data-ttu-id="d4668-172">VNet SubnetID 會指定 VNet 的子網識別碼。</span><span class="sxs-lookup"><span data-stu-id="d4668-172">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

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

### <span data-ttu-id="d4668-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4668-173">-ResourceGroupName</span></span>
<span data-ttu-id="d4668-174">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="d4668-174">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4668-175">-ServicePrincipalIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="d4668-175">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="d4668-176">與 AAD 應用程式/服務主體相關聯的用戶端識別碼與用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="d4668-176">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4668-177">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="d4668-177">-SshKeyValue</span></span>
<span data-ttu-id="d4668-178">SSH 金鑰檔值或金鑰檔路徑。</span><span class="sxs-lookup"><span data-stu-id="d4668-178">SSH key file value or key file path.</span></span>
<span data-ttu-id="d4668-179">預設值為 {HOME}/.ssh/[id_rsa .pub]。</span><span class="sxs-lookup"><span data-stu-id="d4668-179">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SshKeyPath

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4668-180">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="d4668-180">-SubnetName</span></span>
<span data-ttu-id="d4668-181">VirtualNode 載入項的子網名稱。</span><span class="sxs-lookup"><span data-stu-id="d4668-181">Subnet name of VirtualNode addon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4668-182">-Tag</span><span class="sxs-lookup"><span data-stu-id="d4668-182">-Tag</span></span>
<span data-ttu-id="d4668-183">要套用至資源的標記</span><span class="sxs-lookup"><span data-stu-id="d4668-183">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="d4668-184">-WindowsProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="d4668-184">-WindowsProfileAdminUserName</span></span>
<span data-ttu-id="d4668-185">要用於 Windows Vm 的管理員使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="d4668-185">The administrator username to use for Windows VMs.</span></span>

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

### <span data-ttu-id="d4668-186">-WindowsProfileAdminUserPassword</span><span class="sxs-lookup"><span data-stu-id="d4668-186">-WindowsProfileAdminUserPassword</span></span>
<span data-ttu-id="d4668-187">要用於 Windows Vm 的系統管理員密碼，其長度必須至少為12個，包含至少一個小寫字元（亦即 `[a-z]` 一個 `[A-Z]` 特殊字元） `[!@#$%^&_()]` 。</span><span class="sxs-lookup"><span data-stu-id="d4668-187">The administrator password to use for Windows VMs, its length must be at least 12, containing at least one lower case character, i.e. `[a-z]`, one `[A-Z]` and one special character `[!@#$%^&_()]`.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4668-188">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="d4668-188">-WorkspaceResourceId</span></span>
<span data-ttu-id="d4668-189">監視載入項之工作區的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d4668-189">Resource Id of the workspace of Monitoring addon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4668-190">-確認</span><span class="sxs-lookup"><span data-stu-id="d4668-190">-Confirm</span></span>
<span data-ttu-id="d4668-191">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d4668-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4668-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4668-192">-WhatIf</span></span>
<span data-ttu-id="d4668-193">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d4668-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4668-194">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d4668-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4668-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4668-195">CommonParameters</span></span>
<span data-ttu-id="d4668-196">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d4668-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4668-197">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d4668-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4668-198">輸入</span><span class="sxs-lookup"><span data-stu-id="d4668-198">INPUTS</span></span>

### <span data-ttu-id="d4668-199">所有</span><span class="sxs-lookup"><span data-stu-id="d4668-199">None</span></span>

## <span data-ttu-id="d4668-200">輸出</span><span class="sxs-lookup"><span data-stu-id="d4668-200">OUTPUTS</span></span>

### <span data-ttu-id="d4668-201">PSKubernetesCluster 中的 Aks。</span><span class="sxs-lookup"><span data-stu-id="d4668-201">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="d4668-202">筆記</span><span class="sxs-lookup"><span data-stu-id="d4668-202">NOTES</span></span>

## <span data-ttu-id="d4668-203">相關連結</span><span class="sxs-lookup"><span data-stu-id="d4668-203">RELATED LINKS</span></span>
