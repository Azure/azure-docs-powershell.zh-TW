---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/powershell/module/az.kubernetesconfiguration/remove-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Remove-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Remove-AzKubernetesConfiguration.md
ms.openlocfilehash: a63a28d301b5b565a01bf1e3c22acba413ee779a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905073"
---
# <span data-ttu-id="ccf22-101">Remove-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="ccf22-101">Remove-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="ccf22-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ccf22-102">SYNOPSIS</span></span>
<span data-ttu-id="ccf22-103">這會刪除用來設定原始程式碼管理設定的 YAML 檔案，因而停止來源 Repo 未來的同步。</span><span class="sxs-lookup"><span data-stu-id="ccf22-103">This will delete the YAML file used to set up the Source control configuration, thus stopping future sync from the source repo.</span></span>

## <span data-ttu-id="ccf22-104">語法</span><span class="sxs-lookup"><span data-stu-id="ccf22-104">SYNTAX</span></span>

### <span data-ttu-id="ccf22-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="ccf22-105">Delete (Default)</span></span>
```
Remove-AzKubernetesConfiguration -ClusterName <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ccf22-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ccf22-106">DeleteViaIdentity</span></span>
```
Remove-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ccf22-107">描述</span><span class="sxs-lookup"><span data-stu-id="ccf22-107">DESCRIPTION</span></span>
<span data-ttu-id="ccf22-108">這會刪除用來設定原始程式碼管理設定的 YAML 檔案，因而停止來源 Repo 未來的同步。</span><span class="sxs-lookup"><span data-stu-id="ccf22-108">This will delete the YAML file used to set up the Source control configuration, thus stopping future sync from the source repo.</span></span>

## <span data-ttu-id="ccf22-109">例子</span><span class="sxs-lookup"><span data-stu-id="ccf22-109">EXAMPLES</span></span>

### <span data-ttu-id="ccf22-110">範例 1：根據名稱移除 kubernetes cluster 的設定檔</span><span class="sxs-lookup"><span data-stu-id="ccf22-110">Example 1: Remove a configuation of kubernetes cluster by name</span></span>
```powershell
PS C:\> Remove-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -Name  k8sconfig-t02 -ClusterType ConnectedClusters

```

<span data-ttu-id="ccf22-111">此命令會移除kubernetes 組名的設定檔。</span><span class="sxs-lookup"><span data-stu-id="ccf22-111">This command removes a configuation of kubernetes cluster by name.</span></span>

### <span data-ttu-id="ccf22-112">範例 2：根據物件移除 kubernetes cluster 的設定檔</span><span class="sxs-lookup"><span data-stu-id="ccf22-112">Example 2: Remove a configuation of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = Get-AzKubernetesConfiguration -ClusterName connaks-dkc29c -ClusterType ConnectedClusters -ResourceGroupName connaks-rg-w9vlnp -Name conf-test02 -ClusterRp Microsoft.Kubernetes
PS C:\> Remove-AzKubernetesConfiguration -InputObject $kubConf

```

<span data-ttu-id="ccf22-113">此命令會移除根據物件之 kubernetes cluster 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="ccf22-113">This command removes a configuation of kubernetes cluster by object.</span></span>

## <span data-ttu-id="ccf22-114">參數</span><span class="sxs-lookup"><span data-stu-id="ccf22-114">PARAMETERS</span></span>

### <span data-ttu-id="ccf22-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ccf22-115">-AsJob</span></span>
<span data-ttu-id="ccf22-116">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="ccf22-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ccf22-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ccf22-117">-ClusterName</span></span>
<span data-ttu-id="ccf22-118">kubernetes 組名。</span><span class="sxs-lookup"><span data-stu-id="ccf22-118">The name of the kubernetes cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf22-119">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="ccf22-119">-ClusterType</span></span>
<span data-ttu-id="ccf22-120">Kubernetes 叢集資源名稱 -managedClusters (for AKS 叢集) 或 connectedClusters (for OnPrem K8S 叢集) 。</span><span class="sxs-lookup"><span data-stu-id="ccf22-120">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf22-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccf22-121">-DefaultProfile</span></span>
<span data-ttu-id="ccf22-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ccf22-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf22-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ccf22-123">-InputObject</span></span>
<span data-ttu-id="ccf22-124">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="ccf22-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ccf22-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="ccf22-125">-Name</span></span>
<span data-ttu-id="ccf22-126">原始程式碼管理組名。</span><span class="sxs-lookup"><span data-stu-id="ccf22-126">Name of the Source Control Configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SourceControlConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf22-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ccf22-127">-NoWait</span></span>
<span data-ttu-id="ccf22-128">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="ccf22-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ccf22-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ccf22-129">-PassThru</span></span>
<span data-ttu-id="ccf22-130">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="ccf22-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ccf22-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccf22-131">-ResourceGroupName</span></span>
<span data-ttu-id="ccf22-132">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ccf22-132">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf22-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ccf22-133">-SubscriptionId</span></span>
<span data-ttu-id="ccf22-134">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="ccf22-134">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf22-135">-確認</span><span class="sxs-lookup"><span data-stu-id="ccf22-135">-Confirm</span></span>
<span data-ttu-id="ccf22-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ccf22-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccf22-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccf22-137">-WhatIf</span></span>
<span data-ttu-id="ccf22-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ccf22-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccf22-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ccf22-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccf22-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccf22-140">CommonParameters</span></span>
<span data-ttu-id="ccf22-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ccf22-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccf22-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ccf22-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccf22-143">輸入</span><span class="sxs-lookup"><span data-stu-id="ccf22-143">INPUTS</span></span>

### <span data-ttu-id="ccf22-144">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.models.IKubernetesConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="ccf22-144">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="ccf22-145">輸出</span><span class="sxs-lookup"><span data-stu-id="ccf22-145">OUTPUTS</span></span>

### <span data-ttu-id="ccf22-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ccf22-146">System.Boolean</span></span>

## <span data-ttu-id="ccf22-147">筆記</span><span class="sxs-lookup"><span data-stu-id="ccf22-147">NOTES</span></span>

<span data-ttu-id="ccf22-148">別名</span><span class="sxs-lookup"><span data-stu-id="ccf22-148">ALIASES</span></span>

<span data-ttu-id="ccf22-149">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="ccf22-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ccf22-150">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="ccf22-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ccf22-151">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="ccf22-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ccf22-152">INPUTOBJECT： <IKubernetesConfigurationIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="ccf22-152">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ccf22-153">`[ClusterName <String>]`：kubernetes 組名。</span><span class="sxs-lookup"><span data-stu-id="ccf22-153">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="ccf22-154">`[ClusterResourceName <String>]`：Kubernetes 叢集資源名稱 - managedClusters (for AKS 叢集) 或 connectedClusters (for OnPrem K8S 叢集) 。</span><span class="sxs-lookup"><span data-stu-id="ccf22-154">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="ccf22-155">`[ClusterRp <String>]`：Kubernetes cluster RP - 適用于 AKS (的 Microsoft.ContainerService) 或適用于 OnPrem K8S (的 Microsoft.Kubernetes) 。</span><span class="sxs-lookup"><span data-stu-id="ccf22-155">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="ccf22-156">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="ccf22-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ccf22-157">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ccf22-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="ccf22-158">`[SourceControlConfigurationName <String>]`：原始程式碼管理組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ccf22-158">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="ccf22-159">`[SubscriptionId <String>]`：Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="ccf22-159">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="ccf22-160">這是 GUID 格式的字串 (例如 00000000-0000-0000-0000-00000000000000000000000000000000000000000000000000000) </span><span class="sxs-lookup"><span data-stu-id="ccf22-160">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="ccf22-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="ccf22-161">RELATED LINKS</span></span>

