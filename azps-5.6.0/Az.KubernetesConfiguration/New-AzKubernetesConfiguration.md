---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/powershell/module/az.kubernetesconfiguration/new-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
ms.openlocfilehash: 0040ab3bc037527400ea1f3eabf3c887189fc73c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908129"
---
# <span data-ttu-id="f8545-101">New-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8545-101">New-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="f8545-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f8545-102">SYNOPSIS</span></span>
<span data-ttu-id="f8545-103">建立新的 Kubernetes 原始程式碼管理組。</span><span class="sxs-lookup"><span data-stu-id="f8545-103">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="f8545-104">語法</span><span class="sxs-lookup"><span data-stu-id="f8545-104">SYNTAX</span></span>

```
New-AzKubernetesConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 -RepositoryUrl <String> [-ClusterType <String>] [-SubscriptionId <String>] [-ClusterScoped]
 [-EnableHelmOperator] [-HelmOperatorChartValues <String>] [-HelmOperatorChartVersion <String>]
 [-OperatorInstanceName <String>] [-OperatorNamespace <String>] [-OperatorParameters <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f8545-105">描述</span><span class="sxs-lookup"><span data-stu-id="f8545-105">DESCRIPTION</span></span>
<span data-ttu-id="f8545-106">建立新的 Kubernetes 原始程式碼管理組。</span><span class="sxs-lookup"><span data-stu-id="f8545-106">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="f8545-107">例子</span><span class="sxs-lookup"><span data-stu-id="f8545-107">EXAMPLES</span></span>

### <span data-ttu-id="f8545-108">範例 1：建立 kubernetes cluster 的組式</span><span class="sxs-lookup"><span data-stu-id="f8545-108">Example 1: Create a configuration for kubernetes cluster</span></span>
```powershell
PS C:\> New-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -Name k8sconfig-t01 -RepositoryUrl http://github.com/xxxx

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t01 12/21/2020 5:26:17 AM                                             12/21/2020 5:26:17 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="f8545-109">此命令會建立 kubernetes cluster 的組式。</span><span class="sxs-lookup"><span data-stu-id="f8545-109">This command creates a configuration for kubernetes cluster.</span></span>

### <span data-ttu-id="f8545-110">範例 1：使用指定 paramter OperatorNamespace 為 kubernetes cluster 建立組式</span><span class="sxs-lookup"><span data-stu-id="f8545-110">Example 1: Create a configuration for kubernetes cluster with specify paramter OperatorNamespace</span></span>
```powershell
PS C:\> New-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -Name k8sconfig-t02 -RepositoryUrl http://github.com/xxxx -OperatorNamespace namespace-t01

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:26:17 AM                                             12/21/2020 5:26:17 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="f8545-111">此命令會針對 kubernetes cluster 的新運算子命名空間建立一個組式。</span><span class="sxs-lookup"><span data-stu-id="f8545-111">This command creates a configuration in the new operator namespace for kubernetes cluster.</span></span>
<span data-ttu-id="f8545-112">請注意，無法在現有的運算子命名空間中建立組組。</span><span class="sxs-lookup"><span data-stu-id="f8545-112">Note, Unable to create a configuration in an existing operator namespace.</span></span>

## <span data-ttu-id="f8545-113">參數</span><span class="sxs-lookup"><span data-stu-id="f8545-113">PARAMETERS</span></span>

### <span data-ttu-id="f8545-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f8545-114">-ClusterName</span></span>
<span data-ttu-id="f8545-115">kubernetes 組名。</span><span class="sxs-lookup"><span data-stu-id="f8545-115">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="f8545-116">-ClusterScoped</span><span class="sxs-lookup"><span data-stu-id="f8545-116">-ClusterScoped</span></span>
<span data-ttu-id="f8545-117">如果通過設定，設定為組 (預設值為 nameSpace) 。</span><span class="sxs-lookup"><span data-stu-id="f8545-117">If passed set the scope of the Configuration to Cluster (default is nameSpace).</span></span>

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

### <span data-ttu-id="f8545-118">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="f8545-118">-ClusterType</span></span>
<span data-ttu-id="f8545-119">Kubernetes 叢集資源名稱 -managedClusters (for AKS 叢集) 或 connectedClusters (for OnPrem K8S 叢集) 。</span><span class="sxs-lookup"><span data-stu-id="f8545-119">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="f8545-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8545-120">-DefaultProfile</span></span>
<span data-ttu-id="f8545-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f8545-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8545-122">-EnableHelmOperator</span><span class="sxs-lookup"><span data-stu-id="f8545-122">-EnableHelmOperator</span></span>
<span data-ttu-id="f8545-123">此選項可針對此 Git 組配置啟用資料標籤運算子。</span><span class="sxs-lookup"><span data-stu-id="f8545-123">Option to enable Helm Operator for this git configuration.</span></span>

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

### <span data-ttu-id="f8545-124">-讓OperatorChartValues</span><span class="sxs-lookup"><span data-stu-id="f8545-124">-HelmOperatorChartValues</span></span>
<span data-ttu-id="f8545-125">值會優先于運算子的圓形圖。</span><span class="sxs-lookup"><span data-stu-id="f8545-125">Values override for the operator Helm chart.</span></span>

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

### <span data-ttu-id="f8545-126">-一個中式圖表</span><span class="sxs-lookup"><span data-stu-id="f8545-126">-HelmOperatorChartVersion</span></span>
<span data-ttu-id="f8545-127">運算子的圖表版本。</span><span class="sxs-lookup"><span data-stu-id="f8545-127">Version of the operator Helm chart.</span></span>

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

### <span data-ttu-id="f8545-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="f8545-128">-Name</span></span>
<span data-ttu-id="f8545-129">原始程式碼管理組名。</span><span class="sxs-lookup"><span data-stu-id="f8545-129">Name of the Source Control Configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceControlConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8545-130">-OperatorInstanceName</span><span class="sxs-lookup"><span data-stu-id="f8545-130">-OperatorInstanceName</span></span>
<span data-ttu-id="f8545-131">運算子的實例名稱 - 識別特定組式。</span><span class="sxs-lookup"><span data-stu-id="f8545-131">Instance name of the operator - identifying the specific configuration.</span></span>

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

### <span data-ttu-id="f8545-132">-OperatorNamespace</span><span class="sxs-lookup"><span data-stu-id="f8545-132">-OperatorNamespace</span></span>
<span data-ttu-id="f8545-133">此運算子安裝至的命名空間。</span><span class="sxs-lookup"><span data-stu-id="f8545-133">The namespace to which this operator is installed to.</span></span>
<span data-ttu-id="f8545-134">最多 253 個小寫字母數位元、連字號和期間。</span><span class="sxs-lookup"><span data-stu-id="f8545-134">Maximum of 253 lower case alphanumeric characters, hyphen and period only.</span></span>

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

### <span data-ttu-id="f8545-135">-OperatorParameters</span><span class="sxs-lookup"><span data-stu-id="f8545-135">-OperatorParameters</span></span>
<span data-ttu-id="f8545-136">字串格式之運算子實例的任何參數。</span><span class="sxs-lookup"><span data-stu-id="f8545-136">Any Parameters for the Operator instance in string format.</span></span>

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

### <span data-ttu-id="f8545-137">-RepositoryUrl</span><span class="sxs-lookup"><span data-stu-id="f8545-137">-RepositoryUrl</span></span>
<span data-ttu-id="f8545-138">SourceControl 存放庫的 URL。</span><span class="sxs-lookup"><span data-stu-id="f8545-138">Url of the SourceControl Repository.</span></span>

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

### <span data-ttu-id="f8545-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8545-139">-ResourceGroupName</span></span>
<span data-ttu-id="f8545-140">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8545-140">The name of the resource group.</span></span>

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

### <span data-ttu-id="f8545-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f8545-141">-SubscriptionId</span></span>
<span data-ttu-id="f8545-142">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="f8545-142">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8545-143">-確認</span><span class="sxs-lookup"><span data-stu-id="f8545-143">-Confirm</span></span>
<span data-ttu-id="f8545-144">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f8545-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8545-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8545-145">-WhatIf</span></span>
<span data-ttu-id="f8545-146">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f8545-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8545-147">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f8545-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8545-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8545-148">CommonParameters</span></span>
<span data-ttu-id="f8545-149">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f8545-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8545-150">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f8545-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8545-151">輸入</span><span class="sxs-lookup"><span data-stu-id="f8545-151">INPUTS</span></span>

## <span data-ttu-id="f8545-152">輸出</span><span class="sxs-lookup"><span data-stu-id="f8545-152">OUTPUTS</span></span>

### <span data-ttu-id="f8545-153">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20210301.ISourceControlConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8545-153">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20210301.ISourceControlConfiguration</span></span>

## <span data-ttu-id="f8545-154">筆記</span><span class="sxs-lookup"><span data-stu-id="f8545-154">NOTES</span></span>

<span data-ttu-id="f8545-155">別名</span><span class="sxs-lookup"><span data-stu-id="f8545-155">ALIASES</span></span>

## <span data-ttu-id="f8545-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="f8545-156">RELATED LINKS</span></span>

