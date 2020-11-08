---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/set-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAksCluster.md
ms.openlocfilehash: 7853119fcc68b709c2f4963dfa60ebc93ad03351
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126624"
---
# <span data-ttu-id="2e6b9-101">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="2e6b9-101">Set-AzAksCluster</span></span>

## <span data-ttu-id="2e6b9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2e6b9-102">SYNOPSIS</span></span>
<span data-ttu-id="2e6b9-103">更新或建立受管理的 Kubernetes 群集。</span><span class="sxs-lookup"><span data-stu-id="2e6b9-103">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="2e6b9-104">句法</span><span class="sxs-lookup"><span data-stu-id="2e6b9-104">SYNTAX</span></span>

### <span data-ttu-id="2e6b9-105">defaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2e6b9-105">defaultParameterSet (Default)</span></span>
```
Set-AzAksCluster [-NodePoolMode <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-ServicePrincipalIdAndSecret] <PSCredential>] [-Location <String>] [-LinuxProfileAdminUserName <String>]
 [-DnsNamePrefix <String>] [-KubernetesVersion <String>] [-NodeName <String>] [-NodeMinCount <Int32>]
 [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>]
 [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e6b9-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e6b9-106">InputObjectParameterSet</span></span>
```
Set-AzAksCluster -InputObject <PSKubernetesCluster> [-NodePoolMode <String>] [-Location <String>]
 [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e6b9-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e6b9-107">IdParameterSet</span></span>
```
Set-AzAksCluster [-NodePoolMode <String>] [-Id] <String> [-Location <String>]
 [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e6b9-108">說明</span><span class="sxs-lookup"><span data-stu-id="2e6b9-108">DESCRIPTION</span></span>
<span data-ttu-id="2e6b9-109">更新或建立受管理的 Kubernetes 群集。</span><span class="sxs-lookup"><span data-stu-id="2e6b9-109">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="2e6b9-110">示例</span><span class="sxs-lookup"><span data-stu-id="2e6b9-110">EXAMPLES</span></span>

### <span data-ttu-id="2e6b9-111">範例1</span><span class="sxs-lookup"><span data-stu-id="2e6b9-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Set-AzAks -NodeCount 5
```

<span data-ttu-id="2e6b9-112">將 Kubernetes 群集中的節點數設定為5。</span><span class="sxs-lookup"><span data-stu-id="2e6b9-112">Set the number of nodes in the Kubernetes cluster to 5.</span></span>

## <span data-ttu-id="2e6b9-113">參數</span><span class="sxs-lookup"><span data-stu-id="2e6b9-113">PARAMETERS</span></span>

### <span data-ttu-id="2e6b9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2e6b9-114">-AsJob</span></span>
<span data-ttu-id="2e6b9-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2e6b9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2e6b9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e6b9-116">-DefaultProfile</span></span>
<span data-ttu-id="2e6b9-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2e6b9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e6b9-118">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="2e6b9-118">-DnsNamePrefix</span></span>
<span data-ttu-id="2e6b9-119">群集的 DNS 名稱首碼。</span><span class="sxs-lookup"><span data-stu-id="2e6b9-119">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="2e6b9-120">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="2e6b9-120">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="2e6b9-121">是否要啟用自動 scaler</span><span class="sxs-lookup"><span data-stu-id="2e6b9-121">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="2e6b9-122">-識別碼</span><span class="sxs-lookup"><span data-stu-id="2e6b9-122">-Id</span></span>
<span data-ttu-id="2e6b9-123">受管理的 Kubernetes 群集的 Id</span><span class="sxs-lookup"><span data-stu-id="2e6b9-123">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e6b9-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e6b9-124">-InputObject</span></span>
<span data-ttu-id="2e6b9-125">PSKubernetesCluster 物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="2e6b9-125">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e6b9-126">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="2e6b9-126">-KubernetesVersion</span></span>
<span data-ttu-id="2e6b9-127">要用來建立群集的 Kubernetes 版本。</span><span class="sxs-lookup"><span data-stu-id="2e6b9-127">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="2e6b9-128">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="2e6b9-128">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="2e6b9-129">Linux 虛擬機器的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="2e6b9-129">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="2e6b9-130">-位置</span><span class="sxs-lookup"><span data-stu-id="2e6b9-130">-Location</span></span>
<span data-ttu-id="2e6b9-131">群集的 Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="2e6b9-131">Azure location for the cluster.</span></span>
<span data-ttu-id="2e6b9-132">預設為資源群組的位置。</span><span class="sxs-lookup"><span data-stu-id="2e6b9-132">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="2e6b9-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="2e6b9-133">-Name</span></span>
<span data-ttu-id="2e6b9-134">Kubernetes 受管理的群集名稱。</span><span class="sxs-lookup"><span data-stu-id="2e6b9-134">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e6b9-135">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="2e6b9-135">-NodeCount</span></span>
<span data-ttu-id="2e6b9-136">節點池的預設節點數。</span><span class="sxs-lookup"><span data-stu-id="2e6b9-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="2e6b9-137">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="2e6b9-137">-NodeMaxCount</span></span>
<span data-ttu-id="2e6b9-138">自動調整的最大節點數</span><span class="sxs-lookup"><span data-stu-id="2e6b9-138">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="2e6b9-139">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="2e6b9-139">-NodeMinCount</span></span>
<span data-ttu-id="2e6b9-140">自動縮放的最小節點數。</span><span class="sxs-lookup"><span data-stu-id="2e6b9-140">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="2e6b9-141">-NodeName</span><span class="sxs-lookup"><span data-stu-id="2e6b9-141">-NodeName</span></span>
<span data-ttu-id="2e6b9-142">[訂閱與資源群組] 內容中代理池設定檔的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="2e6b9-142">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="2e6b9-143">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="2e6b9-143">-NodeOsDiskSize</span></span>
<span data-ttu-id="2e6b9-144">節點池的預設節點數。</span><span class="sxs-lookup"><span data-stu-id="2e6b9-144">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="2e6b9-145">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="2e6b9-145">-NodePoolMode</span></span>
<span data-ttu-id="2e6b9-146">NodePoolMode 代表節點池的模式。</span><span class="sxs-lookup"><span data-stu-id="2e6b9-146">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="2e6b9-147">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="2e6b9-147">-NodeVmSize</span></span>
<span data-ttu-id="2e6b9-148">虛擬機器的大小。</span><span class="sxs-lookup"><span data-stu-id="2e6b9-148">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="2e6b9-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e6b9-149">-ResourceGroupName</span></span>
<span data-ttu-id="2e6b9-150">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="2e6b9-150">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e6b9-151">-ServicePrincipalIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="2e6b9-151">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="2e6b9-152">與 AAD 應用程式/服務主體相關聯的用戶端識別碼與用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="2e6b9-152">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: defaultParameterSet
Aliases: ClientIdAndSecret

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e6b9-153">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="2e6b9-153">-SshKeyValue</span></span>
<span data-ttu-id="2e6b9-154">SSH 金鑰檔值或金鑰檔路徑。</span><span class="sxs-lookup"><span data-stu-id="2e6b9-154">SSH key file value or key file path.</span></span>
<span data-ttu-id="2e6b9-155">預設值為 {HOME}/.ssh/[id_rsa .pub]。</span><span class="sxs-lookup"><span data-stu-id="2e6b9-155">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="2e6b9-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="2e6b9-156">-Tag</span></span>
<span data-ttu-id="2e6b9-157">要套用至資源的標記</span><span class="sxs-lookup"><span data-stu-id="2e6b9-157">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="2e6b9-158">-確認</span><span class="sxs-lookup"><span data-stu-id="2e6b9-158">-Confirm</span></span>
<span data-ttu-id="2e6b9-159">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2e6b9-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e6b9-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e6b9-160">-WhatIf</span></span>
<span data-ttu-id="2e6b9-161">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2e6b9-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e6b9-162">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2e6b9-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e6b9-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e6b9-163">CommonParameters</span></span>
<span data-ttu-id="2e6b9-164">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2e6b9-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e6b9-165">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2e6b9-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e6b9-166">輸入</span><span class="sxs-lookup"><span data-stu-id="2e6b9-166">INPUTS</span></span>

### <span data-ttu-id="2e6b9-167">PSKubernetesCluster 中的 Aks。</span><span class="sxs-lookup"><span data-stu-id="2e6b9-167">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="2e6b9-168">System.object</span><span class="sxs-lookup"><span data-stu-id="2e6b9-168">System.String</span></span>

## <span data-ttu-id="2e6b9-169">輸出</span><span class="sxs-lookup"><span data-stu-id="2e6b9-169">OUTPUTS</span></span>

### <span data-ttu-id="2e6b9-170">PSKubernetesCluster 中的 Aks。</span><span class="sxs-lookup"><span data-stu-id="2e6b9-170">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="2e6b9-171">筆記</span><span class="sxs-lookup"><span data-stu-id="2e6b9-171">NOTES</span></span>

## <span data-ttu-id="2e6b9-172">相關連結</span><span class="sxs-lookup"><span data-stu-id="2e6b9-172">RELATED LINKS</span></span>
