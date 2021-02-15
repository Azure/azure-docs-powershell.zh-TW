---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/remove-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Remove-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Remove-AzKubernetesConfiguration.md
ms.openlocfilehash: 16b1e6f56cd5d324815dcf9453bc7f94e0de2480
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131678"
---
# <span data-ttu-id="4e81d-101">Remove-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="4e81d-101">Remove-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="4e81d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4e81d-102">SYNOPSIS</span></span>
<span data-ttu-id="4e81d-103">這將會刪除用來設定來源控制設定的 YAML 檔案，從而停止未來與來源存放庫的同步處理。</span><span class="sxs-lookup"><span data-stu-id="4e81d-103">This will delete the YAML file used to set up the Source control configuration, thus stopping future sync from the source repo.</span></span>

## <span data-ttu-id="4e81d-104">句法</span><span class="sxs-lookup"><span data-stu-id="4e81d-104">SYNTAX</span></span>

### <span data-ttu-id="4e81d-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="4e81d-105">Delete (Default)</span></span>
```
Remove-AzKubernetesConfiguration -ClusterName <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4e81d-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4e81d-106">DeleteViaIdentity</span></span>
```
Remove-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4e81d-107">說明</span><span class="sxs-lookup"><span data-stu-id="4e81d-107">DESCRIPTION</span></span>
<span data-ttu-id="4e81d-108">這將會刪除用來設定來源控制設定的 YAML 檔案，從而停止未來與來源存放庫的同步處理。</span><span class="sxs-lookup"><span data-stu-id="4e81d-108">This will delete the YAML file used to set up the Source control configuration, thus stopping future sync from the source repo.</span></span>

## <span data-ttu-id="4e81d-109">示例</span><span class="sxs-lookup"><span data-stu-id="4e81d-109">EXAMPLES</span></span>

### <span data-ttu-id="4e81d-110">範例1：依名稱移除 kubernetes 群集的 configuation</span><span class="sxs-lookup"><span data-stu-id="4e81d-110">Example 1: Remove a configuation of kubernetes cluster by name</span></span>
```powershell
PS C:\> Remove-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -Name  k8sconfig-t02 -ClusterType ConnectedClusters

```

<span data-ttu-id="4e81d-111">這個命令會依名稱移除 kubernetes 群集的 configuation。</span><span class="sxs-lookup"><span data-stu-id="4e81d-111">This command removes a configuation of kubernetes cluster by name.</span></span>

### <span data-ttu-id="4e81d-112">範例2：依物件移除 kubernetes 群集的 configuation</span><span class="sxs-lookup"><span data-stu-id="4e81d-112">Example 2: Remove a configuation of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = Get-AzKubernetesConfiguration -ClusterName connaks-dkc29c -ClusterType ConnectedClusters -ResourceGroupName connaks-rg-w9vlnp -Name conf-test02 -ClusterRp Microsoft.Kubernetes
PS C:\> Remove-AzKubernetesConfiguration -InputObject $kubConf

```

<span data-ttu-id="4e81d-113">這個命令會依物件移除 kubernetes 群集的 configuation。</span><span class="sxs-lookup"><span data-stu-id="4e81d-113">This command removes a configuation of kubernetes cluster by object.</span></span>

## <span data-ttu-id="4e81d-114">參數</span><span class="sxs-lookup"><span data-stu-id="4e81d-114">PARAMETERS</span></span>

### <span data-ttu-id="4e81d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e81d-115">-AsJob</span></span>
<span data-ttu-id="4e81d-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="4e81d-116">Run the command as a job</span></span>

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

### <span data-ttu-id="4e81d-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4e81d-117">-ClusterName</span></span>
<span data-ttu-id="4e81d-118">Kubernetes 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="4e81d-118">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="4e81d-119">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="4e81d-119">-ClusterType</span></span>
<span data-ttu-id="4e81d-120">Kubernetes 群集資源名稱-AKS 群集的 managedClusters () 或 OnPrem K8S 群集) 的 connectedClusters (。</span><span class="sxs-lookup"><span data-stu-id="4e81d-120">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="4e81d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e81d-121">-DefaultProfile</span></span>
<span data-ttu-id="4e81d-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4e81d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e81d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e81d-123">-InputObject</span></span>
<span data-ttu-id="4e81d-124">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="4e81d-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4e81d-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="4e81d-125">-Name</span></span>
<span data-ttu-id="4e81d-126">來源控制項配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="4e81d-126">Name of the Source Control Configuration.</span></span>

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

### <span data-ttu-id="4e81d-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4e81d-127">-NoWait</span></span>
<span data-ttu-id="4e81d-128">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="4e81d-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4e81d-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e81d-129">-PassThru</span></span>
<span data-ttu-id="4e81d-130">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="4e81d-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4e81d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e81d-131">-ResourceGroupName</span></span>
<span data-ttu-id="4e81d-132">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4e81d-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="4e81d-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4e81d-133">-SubscriptionId</span></span>
<span data-ttu-id="4e81d-134">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="4e81d-134">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="4e81d-135">-確認</span><span class="sxs-lookup"><span data-stu-id="4e81d-135">-Confirm</span></span>
<span data-ttu-id="4e81d-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4e81d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e81d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e81d-137">-WhatIf</span></span>
<span data-ttu-id="4e81d-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4e81d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e81d-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4e81d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e81d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e81d-140">CommonParameters</span></span>
<span data-ttu-id="4e81d-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4e81d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e81d-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4e81d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e81d-143">輸入</span><span class="sxs-lookup"><span data-stu-id="4e81d-143">INPUTS</span></span>

### <span data-ttu-id="4e81d-144">IKubernetesConfigurationIdentity （KubernetesConfiguration）的</span><span class="sxs-lookup"><span data-stu-id="4e81d-144">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="4e81d-145">輸出</span><span class="sxs-lookup"><span data-stu-id="4e81d-145">OUTPUTS</span></span>

### <span data-ttu-id="4e81d-146">System.object</span><span class="sxs-lookup"><span data-stu-id="4e81d-146">System.Boolean</span></span>

## <span data-ttu-id="4e81d-147">筆記</span><span class="sxs-lookup"><span data-stu-id="4e81d-147">NOTES</span></span>

<span data-ttu-id="4e81d-148">別名</span><span class="sxs-lookup"><span data-stu-id="4e81d-148">ALIASES</span></span>

<span data-ttu-id="4e81d-149">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="4e81d-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4e81d-150">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="4e81d-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4e81d-151">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="4e81d-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4e81d-152">INPUTOBJECT <IKubernetesConfigurationIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="4e81d-152">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4e81d-153">`[ClusterName <String>]`： Kubernetes 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="4e81d-153">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="4e81d-154">`[ClusterResourceName <String>]`： Kubernetes 群集資源名稱-AKS 群集的 managedClusters () 或 OnPrem K8S 群集) 的 connectedClusters (。</span><span class="sxs-lookup"><span data-stu-id="4e81d-154">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="4e81d-155">`[ClusterRp <String>]`： Kubernetes 群集 RP-AKS 群集的 ContainerService () 或 Microsoft. Kubernetes (OnPrem K8S 群集) 。</span><span class="sxs-lookup"><span data-stu-id="4e81d-155">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="4e81d-156">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="4e81d-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4e81d-157">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4e81d-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="4e81d-158">`[SourceControlConfigurationName <String>]`：來源控制項配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="4e81d-158">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="4e81d-159">`[SubscriptionId <String>]`： Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="4e81d-159">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="4e81d-160">這是 GUID 格式的字串 (例如 00000000-0000-0000-0000-000000000000) </span><span class="sxs-lookup"><span data-stu-id="4e81d-160">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="4e81d-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="4e81d-161">RELATED LINKS</span></span>

