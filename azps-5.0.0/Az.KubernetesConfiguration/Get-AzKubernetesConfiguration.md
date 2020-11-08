---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/get-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
ms.openlocfilehash: 3fd93e42b8f38659f61fcbeb0f49040409f635a8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140482"
---
# <span data-ttu-id="aeccc-101">Get-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="aeccc-101">Get-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="aeccc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aeccc-102">SYNOPSIS</span></span>
<span data-ttu-id="aeccc-103">取得原始程式碼管理設定的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="aeccc-103">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="aeccc-104">句法</span><span class="sxs-lookup"><span data-stu-id="aeccc-104">SYNTAX</span></span>

### <span data-ttu-id="aeccc-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="aeccc-105">List (Default)</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="aeccc-106">獲取</span><span class="sxs-lookup"><span data-stu-id="aeccc-106">Get</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="aeccc-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="aeccc-107">GetViaIdentity</span></span>
```
Get-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="aeccc-108">說明</span><span class="sxs-lookup"><span data-stu-id="aeccc-108">DESCRIPTION</span></span>
<span data-ttu-id="aeccc-109">取得原始程式碼管理設定的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="aeccc-109">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="aeccc-110">示例</span><span class="sxs-lookup"><span data-stu-id="aeccc-110">EXAMPLES</span></span>

### <span data-ttu-id="aeccc-111">範例1：取得 kubernetes 群集的所有設定</span><span class="sxs-lookup"><span data-stu-id="aeccc-111">Example 1: Get all configurations of kubernetes cluster</span></span>
```powershell
PS C:\> Get-AzKubernetesConfiguration -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t02 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="aeccc-112">這個命令會取得 kubernetes 群集的所有設定。</span><span class="sxs-lookup"><span data-stu-id="aeccc-112">This command gets all configurations of kubernetes cluster.</span></span>

### <span data-ttu-id="aeccc-113">範例2：依名稱取得 kubernetes 群集的設定</span><span class="sxs-lookup"><span data-stu-id="aeccc-113">Example 2: Get a configuration of kubernetes cluster by name</span></span>
```powershell
PS C:\> Get-AzKubernetesConfiguration -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t02 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters -Name conf-t02

Name     Type
----     ----
conf-t02 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="aeccc-114">這個命令會透過名稱取得 kubernetes 群集的設定。</span><span class="sxs-lookup"><span data-stu-id="aeccc-114">This command gets a configuration of kubernetes cluster by name.</span></span>

### <span data-ttu-id="aeccc-115">範例3：依物件取得 kubernetes 群集的設定</span><span class="sxs-lookup"><span data-stu-id="aeccc-115">Example 3: Get a configuration of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = New-AzKubernetesConfiguration -Name conf-test02 -ClusterName connaks-dkc29c -ResourceGroupName connaks-rg-w9vlnp -RepositoryUrl http://github.com/xxxx
PS C:\> Get-AzKubernetesConfiguration -InputObject $kubConf

Name     Type
----     ----
conf-t02 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="aeccc-116">這個命令會透過物件取得 kubernetes 群集的設定。</span><span class="sxs-lookup"><span data-stu-id="aeccc-116">This command gets a configuration of kubernetes cluster by object.</span></span>

### <span data-ttu-id="aeccc-117">範例4：依管道取得 kubernetes 群集的設定</span><span class="sxs-lookup"><span data-stu-id="aeccc-117">Example 4: Get a configuration of kubernetes cluster by pipeline</span></span>
```powershell
PS C:\> @{Id='/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/connaks-rg-w9vlnp/providers/Microsoft.Kubernetes/connectedClusters/connaks-d983yc/providers/Microsoft.KubernetesConfiguration/sourceControlConfigurations/conf-test01'} | Get-AzKubernetesConfiguration

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="aeccc-118">這個命令會透過管線取得 kubernetes 群集的設定。</span><span class="sxs-lookup"><span data-stu-id="aeccc-118">This command gets a configuration of kubernetes cluster by pipeline.</span></span>

## <span data-ttu-id="aeccc-119">參數</span><span class="sxs-lookup"><span data-stu-id="aeccc-119">PARAMETERS</span></span>

### <span data-ttu-id="aeccc-120">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="aeccc-120">-ClusterName</span></span>
<span data-ttu-id="aeccc-121">Kubernetes 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="aeccc-121">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="aeccc-122">-ClusterRp</span><span class="sxs-lookup"><span data-stu-id="aeccc-122">-ClusterRp</span></span>
<span data-ttu-id="aeccc-123">Kubernetes 群集 RP-AKS 群集的 ContainerService () 或 Microsoft. Kubernetes (OnPrem K8S 群集) 。</span><span class="sxs-lookup"><span data-stu-id="aeccc-123">The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="aeccc-124">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="aeccc-124">-ClusterType</span></span>
<span data-ttu-id="aeccc-125">Kubernetes 群集資源名稱-AKS 群集的 managedClusters () 或 OnPrem K8S 群集) 的 connectedClusters (。</span><span class="sxs-lookup"><span data-stu-id="aeccc-125">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="aeccc-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aeccc-126">-DefaultProfile</span></span>
<span data-ttu-id="aeccc-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="aeccc-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aeccc-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aeccc-128">-InputObject</span></span>
<span data-ttu-id="aeccc-129">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="aeccc-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="aeccc-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="aeccc-130">-Name</span></span>
<span data-ttu-id="aeccc-131">來源控制項配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="aeccc-131">Name of the Source Control Configuration.</span></span>

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

### <span data-ttu-id="aeccc-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aeccc-132">-ResourceGroupName</span></span>
<span data-ttu-id="aeccc-133">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="aeccc-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="aeccc-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aeccc-134">-SubscriptionId</span></span>
<span data-ttu-id="aeccc-135">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="aeccc-135">The Azure subscription ID.</span></span>
<span data-ttu-id="aeccc-136">這是 GUID 格式的字串 (例如 00000000-0000-0000-0000-000000000000) </span><span class="sxs-lookup"><span data-stu-id="aeccc-136">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="aeccc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeccc-137">CommonParameters</span></span>
<span data-ttu-id="aeccc-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aeccc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeccc-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="aeccc-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeccc-140">輸入</span><span class="sxs-lookup"><span data-stu-id="aeccc-140">INPUTS</span></span>

### <span data-ttu-id="aeccc-141">IKubernetesConfigurationIdentity （KubernetesConfiguration）的</span><span class="sxs-lookup"><span data-stu-id="aeccc-141">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="aeccc-142">輸出</span><span class="sxs-lookup"><span data-stu-id="aeccc-142">OUTPUTS</span></span>

### <span data-ttu-id="aeccc-143">ISourceControlConfiguration （KubernetesConfiguration）。 Api20191101Preview。</span><span class="sxs-lookup"><span data-stu-id="aeccc-143">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20191101Preview.ISourceControlConfiguration</span></span>

## <span data-ttu-id="aeccc-144">筆記</span><span class="sxs-lookup"><span data-stu-id="aeccc-144">NOTES</span></span>

<span data-ttu-id="aeccc-145">別名</span><span class="sxs-lookup"><span data-stu-id="aeccc-145">ALIASES</span></span>

<span data-ttu-id="aeccc-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="aeccc-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="aeccc-147">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="aeccc-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aeccc-148">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="aeccc-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="aeccc-149">INPUTOBJECT <IKubernetesConfigurationIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="aeccc-149">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="aeccc-150">`[ClusterName <String>]`： Kubernetes 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="aeccc-150">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="aeccc-151">`[ClusterResourceName <String>]`： Kubernetes 群集資源名稱-AKS 群集的 managedClusters () 或 OnPrem K8S 群集) 的 connectedClusters (。</span><span class="sxs-lookup"><span data-stu-id="aeccc-151">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="aeccc-152">`[ClusterRp <String>]`： Kubernetes 群集 RP-AKS 群集的 ContainerService () 或 Microsoft. Kubernetes (OnPrem K8S 群集) 。</span><span class="sxs-lookup"><span data-stu-id="aeccc-152">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="aeccc-153">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="aeccc-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="aeccc-154">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="aeccc-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="aeccc-155">`[SourceControlConfigurationName <String>]`：來源控制項配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="aeccc-155">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="aeccc-156">`[SubscriptionId <String>]`： Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="aeccc-156">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="aeccc-157">這是 GUID 格式的字串 (例如 00000000-0000-0000-0000-000000000000) </span><span class="sxs-lookup"><span data-stu-id="aeccc-157">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="aeccc-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="aeccc-158">RELATED LINKS</span></span>

