---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/set-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAksCluster.md
ms.openlocfilehash: 0cf25018ad9cb432b739f5beeb147d20272d7f50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914961"
---
# <span data-ttu-id="7105f-101">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="7105f-101">Set-AzAksCluster</span></span>

## <span data-ttu-id="7105f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7105f-102">SYNOPSIS</span></span>
<span data-ttu-id="7105f-103">更新或建立受管理的Kubernetes 集區。</span><span class="sxs-lookup"><span data-stu-id="7105f-103">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="7105f-104">語法</span><span class="sxs-lookup"><span data-stu-id="7105f-104">SYNTAX</span></span>

### <span data-ttu-id="7105f-105">defaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7105f-105">defaultParameterSet (Default)</span></span>
```
Set-AzAksCluster [-NodePoolMode <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-ServicePrincipalIdAndSecret] <PSCredential>] [-Location <String>] [-LinuxProfileAdminUserName <String>]
 [-DnsNamePrefix <String>] [-KubernetesVersion <String>] [-NodeName <String>] [-NodeMinCount <Int32>]
 [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>]
 [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7105f-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7105f-106">InputObjectParameterSet</span></span>
```
Set-AzAksCluster -InputObject <PSKubernetesCluster> [-NodePoolMode <String>] [-Location <String>]
 [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7105f-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7105f-107">IdParameterSet</span></span>
```
Set-AzAksCluster [-NodePoolMode <String>] [-Id] <String> [-Location <String>]
 [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7105f-108">描述</span><span class="sxs-lookup"><span data-stu-id="7105f-108">DESCRIPTION</span></span>
<span data-ttu-id="7105f-109">更新或建立受管理的Kubernetes 集區。</span><span class="sxs-lookup"><span data-stu-id="7105f-109">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="7105f-110">例子</span><span class="sxs-lookup"><span data-stu-id="7105f-110">EXAMPLES</span></span>

### <span data-ttu-id="7105f-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="7105f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Set-AzAks -NodeCount 5
```

<span data-ttu-id="7105f-112">將 Kubernetes 集中的節點數目設定為 5 個。</span><span class="sxs-lookup"><span data-stu-id="7105f-112">Set the number of nodes in the Kubernetes cluster to 5.</span></span>

## <span data-ttu-id="7105f-113">參數</span><span class="sxs-lookup"><span data-stu-id="7105f-113">PARAMETERS</span></span>

### <span data-ttu-id="7105f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7105f-114">-AsJob</span></span>
<span data-ttu-id="7105f-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7105f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7105f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7105f-116">-DefaultProfile</span></span>
<span data-ttu-id="7105f-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7105f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7105f-118">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="7105f-118">-DnsNamePrefix</span></span>
<span data-ttu-id="7105f-119">該組群的 DNS 名稱首碼。</span><span class="sxs-lookup"><span data-stu-id="7105f-119">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="7105f-120">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="7105f-120">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="7105f-121">是否要啟用自動縮放</span><span class="sxs-lookup"><span data-stu-id="7105f-121">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="7105f-122">-Id</span><span class="sxs-lookup"><span data-stu-id="7105f-122">-Id</span></span>
<span data-ttu-id="7105f-123">受管理的Kubernetes 集的識別碼</span><span class="sxs-lookup"><span data-stu-id="7105f-123">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="7105f-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7105f-124">-InputObject</span></span>
<span data-ttu-id="7105f-125">PSKubernetesCluster 物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="7105f-125">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="7105f-126">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="7105f-126">-KubernetesVersion</span></span>
<span data-ttu-id="7105f-127">要用於建立該組集的 Kubernetes 版本。</span><span class="sxs-lookup"><span data-stu-id="7105f-127">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="7105f-128">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="7105f-128">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="7105f-129">Linux 虛擬機器的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="7105f-129">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="7105f-130">-位置</span><span class="sxs-lookup"><span data-stu-id="7105f-130">-Location</span></span>
<span data-ttu-id="7105f-131">該組群的 Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="7105f-131">Azure location for the cluster.</span></span>
<span data-ttu-id="7105f-132">預設為資源群組的位置。</span><span class="sxs-lookup"><span data-stu-id="7105f-132">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="7105f-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="7105f-133">-Name</span></span>
<span data-ttu-id="7105f-134">Kubernetes managed cluster Name.</span><span class="sxs-lookup"><span data-stu-id="7105f-134">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="7105f-135">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="7105f-135">-NodeCount</span></span>
<span data-ttu-id="7105f-136">節點資料庫的預設節點數目。</span><span class="sxs-lookup"><span data-stu-id="7105f-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="7105f-137">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="7105f-137">-NodeMaxCount</span></span>
<span data-ttu-id="7105f-138">自動縮放的節點數目上限</span><span class="sxs-lookup"><span data-stu-id="7105f-138">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="7105f-139">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="7105f-139">-NodeMinCount</span></span>
<span data-ttu-id="7105f-140">可自動縮放的節點數目最低。</span><span class="sxs-lookup"><span data-stu-id="7105f-140">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="7105f-141">-NodeName</span><span class="sxs-lookup"><span data-stu-id="7105f-141">-NodeName</span></span>
<span data-ttu-id="7105f-142">訂閱和資源群組中代理程式組設定檔的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="7105f-142">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="7105f-143">-NodeOs以Size</span><span class="sxs-lookup"><span data-stu-id="7105f-143">-NodeOsDiskSize</span></span>
<span data-ttu-id="7105f-144">節點資料庫的預設節點數目。</span><span class="sxs-lookup"><span data-stu-id="7105f-144">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="7105f-145">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="7105f-145">-NodePoolMode</span></span>
<span data-ttu-id="7105f-146">NodePoolMode 代表節點區模式。</span><span class="sxs-lookup"><span data-stu-id="7105f-146">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="7105f-147">-NodeEvSize</span><span class="sxs-lookup"><span data-stu-id="7105f-147">-NodeVmSize</span></span>
<span data-ttu-id="7105f-148">虛擬機器的大小。</span><span class="sxs-lookup"><span data-stu-id="7105f-148">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="7105f-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7105f-149">-ResourceGroupName</span></span>
<span data-ttu-id="7105f-150">資源組名。</span><span class="sxs-lookup"><span data-stu-id="7105f-150">Resource Group Name.</span></span>

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

### <span data-ttu-id="7105f-151">-ServicePrincipalIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="7105f-151">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="7105f-152">與 AAD 應用程式/服務主體相關聯的用戶端識別碼與用戶端金鑰。</span><span class="sxs-lookup"><span data-stu-id="7105f-152">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: defaultParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7105f-153">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="7105f-153">-SshKeyValue</span></span>
<span data-ttu-id="7105f-154">SSH 鍵檔案值或金鑰檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="7105f-154">SSH key file value or key file path.</span></span>
<span data-ttu-id="7105f-155">預設為 {HOME}/.ssh/id_rsa.pub。</span><span class="sxs-lookup"><span data-stu-id="7105f-155">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="7105f-156">-標記</span><span class="sxs-lookup"><span data-stu-id="7105f-156">-Tag</span></span>
<span data-ttu-id="7105f-157">要適用于資源的標記</span><span class="sxs-lookup"><span data-stu-id="7105f-157">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="7105f-158">-確認</span><span class="sxs-lookup"><span data-stu-id="7105f-158">-Confirm</span></span>
<span data-ttu-id="7105f-159">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7105f-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7105f-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7105f-160">-WhatIf</span></span>
<span data-ttu-id="7105f-161">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7105f-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7105f-162">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7105f-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7105f-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7105f-163">CommonParameters</span></span>
<span data-ttu-id="7105f-164">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7105f-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7105f-165">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7105f-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7105f-166">輸入</span><span class="sxs-lookup"><span data-stu-id="7105f-166">INPUTS</span></span>

### <span data-ttu-id="7105f-167">Microsoft.Azure.Commands.Aks.models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="7105f-167">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="7105f-168">System.String</span><span class="sxs-lookup"><span data-stu-id="7105f-168">System.String</span></span>

## <span data-ttu-id="7105f-169">輸出</span><span class="sxs-lookup"><span data-stu-id="7105f-169">OUTPUTS</span></span>

### <span data-ttu-id="7105f-170">Microsoft.Azure.Commands.Aks.models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="7105f-170">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="7105f-171">筆記</span><span class="sxs-lookup"><span data-stu-id="7105f-171">NOTES</span></span>

## <span data-ttu-id="7105f-172">相關連結</span><span class="sxs-lookup"><span data-stu-id="7105f-172">RELATED LINKS</span></span>
