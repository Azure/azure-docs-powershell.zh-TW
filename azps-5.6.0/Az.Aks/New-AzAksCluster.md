---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/new-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
ms.openlocfilehash: 806c3a17dcfc470e01801548013d0d8c6ea58ae4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916446"
---
# <span data-ttu-id="00099-101">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="00099-101">New-AzAksCluster</span></span>

## <span data-ttu-id="00099-102">簡介</span><span class="sxs-lookup"><span data-stu-id="00099-102">SYNOPSIS</span></span>
<span data-ttu-id="00099-103">建立新的受管理的Kubernetes 集區。</span><span class="sxs-lookup"><span data-stu-id="00099-103">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="00099-104">語法</span><span class="sxs-lookup"><span data-stu-id="00099-104">SYNTAX</span></span>

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

## <span data-ttu-id="00099-105">描述</span><span class="sxs-lookup"><span data-stu-id="00099-105">DESCRIPTION</span></span>

<span data-ttu-id="00099-106">在 AKS (中) Azure Kubernetes Service。</span><span class="sxs-lookup"><span data-stu-id="00099-106">Create a new Azure Kubernetes Service(AKS) cluster.</span></span>

## <span data-ttu-id="00099-107">例子</span><span class="sxs-lookup"><span data-stu-id="00099-107">EXAMPLES</span></span>

### <span data-ttu-id="00099-108">新增具有預設參數的 AKS。</span><span class="sxs-lookup"><span data-stu-id="00099-108">New an AKS with default params.</span></span>

```powershell
PS C:\> New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster
```

### <span data-ttu-id="00099-109">在 AKS 上建立 Windows Server 容器。</span><span class="sxs-lookup"><span data-stu-id="00099-109">Create Windows Server container on an AKS.</span></span>
<span data-ttu-id="00099-110">若要在 AKS 上建立 Windows Server 容器，您必須在建立 AKS 時指定至少四個下列參數，且其值必須和分別 `NetworkPlugin` `NodeVmSetType` `azure` `VirtualMachineScaleSets` 指定。</span><span class="sxs-lookup"><span data-stu-id="00099-110">To create Windows Server container on an AKS, you must specify at least four following parameters when creating the AKS, and the value for `NetworkPlugin` and `NodeVmSetType` must be `azure` and `VirtualMachineScaleSets` respectively.</span></span>
`-WindowsProfileAdminUserName *** -WindowsProfileAdminUserPassword *** -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets`

```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="00099-111">參數</span><span class="sxs-lookup"><span data-stu-id="00099-111">PARAMETERS</span></span>

### <span data-ttu-id="00099-112">-AcrNameToAttach</span><span class="sxs-lookup"><span data-stu-id="00099-112">-AcrNameToAttach</span></span>
<span data-ttu-id="00099-113">將指定 ACR 的 'acrpull' 角色授予 AKS 服務主體，例如 myacr</span><span class="sxs-lookup"><span data-stu-id="00099-113">Grant the 'acrpull' role of the specified ACR to AKS Service Principal, e.g. myacr</span></span>

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

### <span data-ttu-id="00099-114">-AddOnNameToBeEnabled</span><span class="sxs-lookup"><span data-stu-id="00099-114">-AddOnNameToBeEnabled</span></span>
<span data-ttu-id="00099-115">建立組組時要啟用的附加元件名稱。</span><span class="sxs-lookup"><span data-stu-id="00099-115">Add-on names to be enabled when cluster is created.</span></span>

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

### <span data-ttu-id="00099-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="00099-116">-AsJob</span></span>
<span data-ttu-id="00099-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="00099-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="00099-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00099-118">-DefaultProfile</span></span>
<span data-ttu-id="00099-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="00099-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00099-120">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="00099-120">-DnsNamePrefix</span></span>
<span data-ttu-id="00099-121">該組群的 DNS 名稱首碼。</span><span class="sxs-lookup"><span data-stu-id="00099-121">The DNS name prefix for the cluster.</span></span> <span data-ttu-id="00099-122">如果使用者打算新增視窗容器<長度必須等於 9。</span><span class="sxs-lookup"><span data-stu-id="00099-122">The length must be <= 9 if users plan to add windows container.</span></span>

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

### <span data-ttu-id="00099-123">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="00099-123">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="00099-124">是否要啟用自動縮放</span><span class="sxs-lookup"><span data-stu-id="00099-124">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="00099-125">-EnableRbac</span><span class="sxs-lookup"><span data-stu-id="00099-125">-EnableRbac</span></span>
<span data-ttu-id="00099-126">是否要啟用 Kubernetes Role-Based Access</span><span class="sxs-lookup"><span data-stu-id="00099-126">Whether to enable Kubernetes Role-Based Access</span></span>

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

### <span data-ttu-id="00099-127">-強制</span><span class="sxs-lookup"><span data-stu-id="00099-127">-Force</span></span>
<span data-ttu-id="00099-128">即使已存在，也建立該組</span><span class="sxs-lookup"><span data-stu-id="00099-128">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="00099-129">-GenerateSshKey</span><span class="sxs-lookup"><span data-stu-id="00099-129">-GenerateSshKey</span></span>
<span data-ttu-id="00099-130">產生 ssh 鍵檔案至 {HOME}/.ssh/id_rsa。</span><span class="sxs-lookup"><span data-stu-id="00099-130">Generate ssh key file to {HOME}/.ssh/id_rsa.</span></span>

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

### <span data-ttu-id="00099-131">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="00099-131">-KubernetesVersion</span></span>
<span data-ttu-id="00099-132">要用於建立該組集的 Kubernetes 版本。</span><span class="sxs-lookup"><span data-stu-id="00099-132">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="00099-133">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="00099-133">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="00099-134">Linux 虛擬機器的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="00099-134">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="00099-135">-LoadBalancerSku</span><span class="sxs-lookup"><span data-stu-id="00099-135">-LoadBalancerSku</span></span>
<span data-ttu-id="00099-136">受管理之組群的負載平衡器 SKU。</span><span class="sxs-lookup"><span data-stu-id="00099-136">The load balancer sku for the managed cluster.</span></span>

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

### <span data-ttu-id="00099-137">-位置</span><span class="sxs-lookup"><span data-stu-id="00099-137">-Location</span></span>
<span data-ttu-id="00099-138">該組群的 Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="00099-138">Azure location for the cluster.</span></span>
<span data-ttu-id="00099-139">預設為資源群組的位置。</span><span class="sxs-lookup"><span data-stu-id="00099-139">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="00099-140">-名稱</span><span class="sxs-lookup"><span data-stu-id="00099-140">-Name</span></span>
<span data-ttu-id="00099-141">Kubernetes managed cluster Name.</span><span class="sxs-lookup"><span data-stu-id="00099-141">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="00099-142">-NetworkPlugin</span><span class="sxs-lookup"><span data-stu-id="00099-142">-NetworkPlugin</span></span>
<span data-ttu-id="00099-143">用來建建 Kubernetes 網路的網路外掛程式。</span><span class="sxs-lookup"><span data-stu-id="00099-143">Network plugin used for building Kubernetes network.</span></span>

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

### <span data-ttu-id="00099-144">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="00099-144">-NodeCount</span></span>
<span data-ttu-id="00099-145">節點資料庫的預設節點數目。</span><span class="sxs-lookup"><span data-stu-id="00099-145">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="00099-146">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="00099-146">-NodeMaxCount</span></span>
<span data-ttu-id="00099-147">自動縮放的節點數目上限</span><span class="sxs-lookup"><span data-stu-id="00099-147">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="00099-148">-NodeMaxPodCount</span><span class="sxs-lookup"><span data-stu-id="00099-148">-NodeMaxPodCount</span></span>
<span data-ttu-id="00099-149">可在節點上執行之窗格數目上限。</span><span class="sxs-lookup"><span data-stu-id="00099-149">Maximum number of pods that can run on node.</span></span>

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

### <span data-ttu-id="00099-150">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="00099-150">-NodeMinCount</span></span>
<span data-ttu-id="00099-151">可自動縮放的節點數目最低。</span><span class="sxs-lookup"><span data-stu-id="00099-151">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="00099-152">-NodeName</span><span class="sxs-lookup"><span data-stu-id="00099-152">-NodeName</span></span>
<span data-ttu-id="00099-153">訂閱和資源群組中代理程式組設定檔的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="00099-153">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="00099-154">-NodeOs以Size</span><span class="sxs-lookup"><span data-stu-id="00099-154">-NodeOsDiskSize</span></span>
<span data-ttu-id="00099-155">節點資料庫每個節點的作業系統磁片大小 ，以 GB 為單位。</span><span class="sxs-lookup"><span data-stu-id="00099-155">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="00099-156">最低 30 GB。</span><span class="sxs-lookup"><span data-stu-id="00099-156">Minimum 30 GB.</span></span>

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

### <span data-ttu-id="00099-157">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="00099-157">-NodePoolMode</span></span>
<span data-ttu-id="00099-158">NodePoolMode 代表節點區模式。</span><span class="sxs-lookup"><span data-stu-id="00099-158">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="00099-159">-NodeScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="00099-159">-NodeScaleSetEvictionPolicy</span></span>
<span data-ttu-id="00099-160">要用來指定低優先順序虛擬機器縮放集的部署策略的 ScaleSetEvictionPolicy。</span><span class="sxs-lookup"><span data-stu-id="00099-160">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span> <span data-ttu-id="00099-161">預設為 Delete。</span><span class="sxs-lookup"><span data-stu-id="00099-161">Default to Delete.</span></span>

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

### <span data-ttu-id="00099-162">-NodeSetPriority</span><span class="sxs-lookup"><span data-stu-id="00099-162">-NodeSetPriority</span></span>
<span data-ttu-id="00099-163">用來指定虛擬機器縮放比例集優先順序的 ScaleSetPriority。</span><span class="sxs-lookup"><span data-stu-id="00099-163">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span> <span data-ttu-id="00099-164">預設為一般。</span><span class="sxs-lookup"><span data-stu-id="00099-164">Default to regular.</span></span>

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

### <span data-ttu-id="00099-165">-NodeEvSetType</span><span class="sxs-lookup"><span data-stu-id="00099-165">-NodeVmSetType</span></span>
<span data-ttu-id="00099-166">AgentPoolType 代表代理程式清單類型。</span><span class="sxs-lookup"><span data-stu-id="00099-166">AgentPoolType represents types of an agent pool.</span></span> <span data-ttu-id="00099-167">可能的值包括：「VirtualMachineScaleSets'、'AvailabilitySet'</span><span class="sxs-lookup"><span data-stu-id="00099-167">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

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

### <span data-ttu-id="00099-168">-NodeEvSize</span><span class="sxs-lookup"><span data-stu-id="00099-168">-NodeVmSize</span></span>
<span data-ttu-id="00099-169">虛擬機器的大小。</span><span class="sxs-lookup"><span data-stu-id="00099-169">The size of the Virtual Machine.</span></span> <span data-ttu-id="00099-170">預設值會Standard_D2_v2。</span><span class="sxs-lookup"><span data-stu-id="00099-170">Default value is Standard_D2_v2.</span></span>

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

### <span data-ttu-id="00099-171">-NodeVnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="00099-171">-NodeVnetSubnetID</span></span>
<span data-ttu-id="00099-172">VNet 子網識別碼會指定 VNet 的子網識別碼。</span><span class="sxs-lookup"><span data-stu-id="00099-172">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

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

### <span data-ttu-id="00099-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00099-173">-ResourceGroupName</span></span>
<span data-ttu-id="00099-174">資源組名。</span><span class="sxs-lookup"><span data-stu-id="00099-174">Resource Group Name.</span></span>

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

### <span data-ttu-id="00099-175">-ServicePrincipalIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="00099-175">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="00099-176">與 AAD 應用程式/服務主體相關聯的用戶端識別碼與用戶端金鑰。</span><span class="sxs-lookup"><span data-stu-id="00099-176">The client id and client secret associated with the AAD application / service principal.</span></span>

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

### <span data-ttu-id="00099-177">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="00099-177">-SshKeyValue</span></span>
<span data-ttu-id="00099-178">SSH 鍵檔案值或金鑰檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="00099-178">SSH key file value or key file path.</span></span>
<span data-ttu-id="00099-179">預設為 {HOME}/.ssh/id_rsa.pub。</span><span class="sxs-lookup"><span data-stu-id="00099-179">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="00099-180">-子網名稱</span><span class="sxs-lookup"><span data-stu-id="00099-180">-SubnetName</span></span>
<span data-ttu-id="00099-181">VirtualNode 外掛程式的子網名稱。</span><span class="sxs-lookup"><span data-stu-id="00099-181">Subnet name of VirtualNode addon.</span></span>

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

### <span data-ttu-id="00099-182">-標記</span><span class="sxs-lookup"><span data-stu-id="00099-182">-Tag</span></span>
<span data-ttu-id="00099-183">要適用于資源的標記</span><span class="sxs-lookup"><span data-stu-id="00099-183">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="00099-184">-WindowsProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="00099-184">-WindowsProfileAdminUserName</span></span>
<span data-ttu-id="00099-185">要用於 Windows 虛擬機器的系統管理員使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="00099-185">The administrator username to use for Windows VMs.</span></span>

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

### <span data-ttu-id="00099-186">-WindowsProfileAdminUserPassword</span><span class="sxs-lookup"><span data-stu-id="00099-186">-WindowsProfileAdminUserPassword</span></span>
<span data-ttu-id="00099-187">Windows 虛擬機器的系統管理員密碼長度必須至少為 12 個，包含至少一個小寫字元，即一個特殊 `[a-z]` `[A-Z]` 字元 `[!@#$%^&*()]` 。</span><span class="sxs-lookup"><span data-stu-id="00099-187">The administrator password to use for Windows VMs, its length must be at least 12, containing at least one lower case character, i.e. `[a-z]`, one `[A-Z]` and one special character `[!@#$%^&*()]`.</span></span>

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

### <span data-ttu-id="00099-188">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="00099-188">-WorkspaceResourceId</span></span>
<span data-ttu-id="00099-189">監控外掛程式工作區的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="00099-189">Resource Id of the workspace of Monitoring addon.</span></span>

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

### <span data-ttu-id="00099-190">-確認</span><span class="sxs-lookup"><span data-stu-id="00099-190">-Confirm</span></span>
<span data-ttu-id="00099-191">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="00099-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00099-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00099-192">-WhatIf</span></span>
<span data-ttu-id="00099-193">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="00099-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00099-194">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="00099-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00099-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00099-195">CommonParameters</span></span>
<span data-ttu-id="00099-196">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="00099-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00099-197">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="00099-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00099-198">輸入</span><span class="sxs-lookup"><span data-stu-id="00099-198">INPUTS</span></span>

### <span data-ttu-id="00099-199">沒有</span><span class="sxs-lookup"><span data-stu-id="00099-199">None</span></span>

## <span data-ttu-id="00099-200">輸出</span><span class="sxs-lookup"><span data-stu-id="00099-200">OUTPUTS</span></span>

### <span data-ttu-id="00099-201">Microsoft.Azure.Commands.Aks.models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="00099-201">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="00099-202">筆記</span><span class="sxs-lookup"><span data-stu-id="00099-202">NOTES</span></span>

## <span data-ttu-id="00099-203">相關連結</span><span class="sxs-lookup"><span data-stu-id="00099-203">RELATED LINKS</span></span>
