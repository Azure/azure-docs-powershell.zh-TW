---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/powershell/module/az.kubernetesconfiguration/get-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
ms.openlocfilehash: 8cbf938917f26b1229b5c18d25448da4df3bb5b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908130"
---
# <span data-ttu-id="4ea66-101">Get-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ea66-101">Get-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="4ea66-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4ea66-102">SYNOPSIS</span></span>
<span data-ttu-id="4ea66-103">獲得原始程式碼管理組配置的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="4ea66-103">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="4ea66-104">語法</span><span class="sxs-lookup"><span data-stu-id="4ea66-104">SYNTAX</span></span>

### <span data-ttu-id="4ea66-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="4ea66-105">List (Default)</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4ea66-106">獲取</span><span class="sxs-lookup"><span data-stu-id="4ea66-106">Get</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4ea66-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4ea66-107">GetViaIdentity</span></span>
```
Get-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="4ea66-108">描述</span><span class="sxs-lookup"><span data-stu-id="4ea66-108">DESCRIPTION</span></span>
<span data-ttu-id="4ea66-109">獲得原始程式碼管理組配置的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="4ea66-109">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="4ea66-110">例子</span><span class="sxs-lookup"><span data-stu-id="4ea66-110">EXAMPLES</span></span>

### <span data-ttu-id="4ea66-111">範例 1：取得 kubernetes cluster 的所有組式</span><span class="sxs-lookup"><span data-stu-id="4ea66-111">Example 1: Get all configurations of kubernetes cluster</span></span>
```powershell
PS C:\> Get-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:29:33 AM                                             12/21/2020 5:29:33 AM                                                          Microsoft.KubernetesConfiguration/so…
k8sconfig-t01 12/21/2020 5:26:17 AM                                             12/21/2020 5:27:45 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="4ea66-112">此命令會獲得 kubernetes 集區的所有組式。</span><span class="sxs-lookup"><span data-stu-id="4ea66-112">This command gets all configurations of kubernetes cluster.</span></span>

### <span data-ttu-id="4ea66-113">範例 2：根據名稱取得 kubernetes cluster 的組式</span><span class="sxs-lookup"><span data-stu-id="4ea66-113">Example 2: Get a configuration of kubernetes cluster by name</span></span>
```powershell
PS C:\>  Get-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters -Name  k8sconfig-t02

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:29:33 AM                                             12/21/2020 5:29:33 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="4ea66-114">此命令會根據名稱獲得 kubernetes cluster 的組式。</span><span class="sxs-lookup"><span data-stu-id="4ea66-114">This command gets a configuration of kubernetes cluster by name.</span></span>

### <span data-ttu-id="4ea66-115">範例 3：根據物件取得 kubernetes cluster 的組式</span><span class="sxs-lookup"><span data-stu-id="4ea66-115">Example 3: Get a configuration of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = New-AzKubernetesConfiguration -Name k8sconfig-t02 -ClusterName connaks-dkc29c -ResourceGroupName connaks-rg-w9vlnp -RepositoryUrl http://github.com/xxxx
PS C:\> Get-AzKubernetesConfiguration -InputObject $kubConf

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:29:33 AM                                             12/21/2020 5:29:33 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="4ea66-116">此命令會根據物件獲得 kubernetes cluster 的組式。</span><span class="sxs-lookup"><span data-stu-id="4ea66-116">This command gets a configuration of kubernetes cluster by object.</span></span>

### <span data-ttu-id="4ea66-117">範例 4：根據管線取得 kubernetes cluster 的組式</span><span class="sxs-lookup"><span data-stu-id="4ea66-117">Example 4: Get a configuration of kubernetes cluster by pipeline</span></span>
```powershell
PS C:\> @{Id='/subscriptions/xxxxx-xxxxxxx-xxxxx-xxxxxx/resourceGroups/connaks-rg-w9vlnp/providers/Microsoft.Kubernetes/connectedClusters/connaks-d983yc/providers/Microsoft.KubernetesConfiguration/sourceControlConfigurations/k8sconfig-t02'} | Get-AzKubernetesConfiguration

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:29:33 AM                                             12/21/2020 5:29:33 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="4ea66-118">此命令會根據管線獲得 kubernetes cluster 的組式。</span><span class="sxs-lookup"><span data-stu-id="4ea66-118">This command gets a configuration of kubernetes cluster by pipeline.</span></span>

## <span data-ttu-id="4ea66-119">參數</span><span class="sxs-lookup"><span data-stu-id="4ea66-119">PARAMETERS</span></span>

### <span data-ttu-id="4ea66-120">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4ea66-120">-ClusterName</span></span>
<span data-ttu-id="4ea66-121">kubernetes 組名。</span><span class="sxs-lookup"><span data-stu-id="4ea66-121">The name of the kubernetes cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ea66-122">-ClusterRp</span><span class="sxs-lookup"><span data-stu-id="4ea66-122">-ClusterRp</span></span>
<span data-ttu-id="4ea66-123">Kubernetes cluster RP - 適用于 AKS (的 Microsoft.ContainerService) 或適用于 OnPrem K8S (的 Microsoft.Kubernetes) 。</span><span class="sxs-lookup"><span data-stu-id="4ea66-123">The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ea66-124">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="4ea66-124">-ClusterType</span></span>
<span data-ttu-id="4ea66-125">Kubernetes 叢集資源名稱 -managedClusters (for AKS 叢集) 或 connectedClusters (for OnPrem K8S 叢集) 。</span><span class="sxs-lookup"><span data-stu-id="4ea66-125">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ea66-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ea66-126">-DefaultProfile</span></span>
<span data-ttu-id="4ea66-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4ea66-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ea66-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ea66-128">-InputObject</span></span>
<span data-ttu-id="4ea66-129">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="4ea66-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ea66-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="4ea66-130">-Name</span></span>
<span data-ttu-id="4ea66-131">原始程式碼管理組名。</span><span class="sxs-lookup"><span data-stu-id="4ea66-131">Name of the Source Control Configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SourceControlConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ea66-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ea66-132">-ResourceGroupName</span></span>
<span data-ttu-id="4ea66-133">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4ea66-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ea66-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4ea66-134">-SubscriptionId</span></span>
<span data-ttu-id="4ea66-135">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="4ea66-135">The Azure subscription ID.</span></span>
<span data-ttu-id="4ea66-136">這是 GUID 格式的字串 (例如 00000000-0000-0000-0000-00000000000000000000000000000000000000000000000000000) </span><span class="sxs-lookup"><span data-stu-id="4ea66-136">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ea66-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ea66-137">CommonParameters</span></span>
<span data-ttu-id="4ea66-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4ea66-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ea66-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4ea66-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ea66-140">輸入</span><span class="sxs-lookup"><span data-stu-id="4ea66-140">INPUTS</span></span>

### <span data-ttu-id="4ea66-141">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.models.IKubernetesConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="4ea66-141">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="4ea66-142">輸出</span><span class="sxs-lookup"><span data-stu-id="4ea66-142">OUTPUTS</span></span>

### <span data-ttu-id="4ea66-143">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20210301.ISourceControlConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ea66-143">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20210301.ISourceControlConfiguration</span></span>

## <span data-ttu-id="4ea66-144">筆記</span><span class="sxs-lookup"><span data-stu-id="4ea66-144">NOTES</span></span>

<span data-ttu-id="4ea66-145">別名</span><span class="sxs-lookup"><span data-stu-id="4ea66-145">ALIASES</span></span>

<span data-ttu-id="4ea66-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="4ea66-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4ea66-147">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="4ea66-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4ea66-148">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="4ea66-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4ea66-149">INPUTOBJECT： <IKubernetesConfigurationIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="4ea66-149">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4ea66-150">`[ClusterName <String>]`：kubernetes 組名。</span><span class="sxs-lookup"><span data-stu-id="4ea66-150">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="4ea66-151">`[ClusterResourceName <String>]`：Kubernetes 叢集資源名稱 - managedClusters (for AKS 叢集) 或 connectedClusters (for OnPrem K8S 叢集) 。</span><span class="sxs-lookup"><span data-stu-id="4ea66-151">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="4ea66-152">`[ClusterRp <String>]`：Kubernetes cluster RP - 適用于 AKS (的 Microsoft.ContainerService) 或適用于 OnPrem K8S (的 Microsoft.Kubernetes) 。</span><span class="sxs-lookup"><span data-stu-id="4ea66-152">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="4ea66-153">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="4ea66-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4ea66-154">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4ea66-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="4ea66-155">`[SourceControlConfigurationName <String>]`：原始程式碼管理組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4ea66-155">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="4ea66-156">`[SubscriptionId <String>]`：Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="4ea66-156">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="4ea66-157">這是 GUID 格式的字串 (例如 00000000-0000-0000-0000-00000000000000000000000000000000000000000000000000000) </span><span class="sxs-lookup"><span data-stu-id="4ea66-157">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="4ea66-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="4ea66-158">RELATED LINKS</span></span>

