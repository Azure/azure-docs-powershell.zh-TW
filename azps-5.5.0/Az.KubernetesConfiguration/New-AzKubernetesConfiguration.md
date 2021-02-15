---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/new-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
ms.openlocfilehash: 425a2f2fcc145b360ea981a4d78113d6053c90e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131686"
---
# <span data-ttu-id="2629c-101">New-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="2629c-101">New-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="2629c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2629c-102">SYNOPSIS</span></span>
<span data-ttu-id="2629c-103">建立新的 Kubernetes 來源控制項配置。</span><span class="sxs-lookup"><span data-stu-id="2629c-103">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="2629c-104">句法</span><span class="sxs-lookup"><span data-stu-id="2629c-104">SYNTAX</span></span>

```
New-AzKubernetesConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 -RepositoryUrl <String> [-ClusterType <String>] [-SubscriptionId <String>] [-ClusterScoped]
 [-EnableHelmOperator] [-HelmOperatorChartValues <String>] [-HelmOperatorChartVersion <String>]
 [-OperatorInstanceName <String>] [-OperatorNamespace <String>] [-OperatorParameters <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2629c-105">說明</span><span class="sxs-lookup"><span data-stu-id="2629c-105">DESCRIPTION</span></span>
<span data-ttu-id="2629c-106">建立新的 Kubernetes 來源控制項配置。</span><span class="sxs-lookup"><span data-stu-id="2629c-106">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="2629c-107">示例</span><span class="sxs-lookup"><span data-stu-id="2629c-107">EXAMPLES</span></span>

### <span data-ttu-id="2629c-108">範例1：建立 kubernetes 群集的配置</span><span class="sxs-lookup"><span data-stu-id="2629c-108">Example 1: Create a configuration for kubernetes cluster</span></span>
```powershell
PS C:\> New-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -Name k8sconfig-t01 -RepositoryUrl http://github.com/xxxx

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t01 12/21/2020 5:26:17 AM                                             12/21/2020 5:26:17 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="2629c-109">這個命令會建立 kubernetes 群集的配置。</span><span class="sxs-lookup"><span data-stu-id="2629c-109">This command creates a configuration for kubernetes cluster.</span></span>

### <span data-ttu-id="2629c-110">範例1：使用指定參數 OperatorNamespace 為 kubernetes 群集建立配置</span><span class="sxs-lookup"><span data-stu-id="2629c-110">Example 1: Create a configuration for kubernetes cluster with specify paramter OperatorNamespace</span></span>
```powershell
PS C:\> New-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -Name k8sconfig-t02 -RepositoryUrl http://github.com/xxxx -OperatorNamespace namespace-t01

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:26:17 AM                                             12/21/2020 5:26:17 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="2629c-111">這個命令會在 kubernetes 群集的新操作員命名空間中建立配置。</span><span class="sxs-lookup"><span data-stu-id="2629c-111">This command creates a configuration in the new operator namespace for kubernetes cluster.</span></span>
<span data-ttu-id="2629c-112">注意，無法在現有的操作員命名空間中建立配置。</span><span class="sxs-lookup"><span data-stu-id="2629c-112">Note, Unable to create a configuration in an existing operator namespace.</span></span>

## <span data-ttu-id="2629c-113">參數</span><span class="sxs-lookup"><span data-stu-id="2629c-113">PARAMETERS</span></span>

### <span data-ttu-id="2629c-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2629c-114">-ClusterName</span></span>
<span data-ttu-id="2629c-115">Kubernetes 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="2629c-115">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="2629c-116">-ClusterScoped</span><span class="sxs-lookup"><span data-stu-id="2629c-116">-ClusterScoped</span></span>
<span data-ttu-id="2629c-117">如果傳遞將設定的範圍設定為 [群集] (預設值為 nameSpace) 。</span><span class="sxs-lookup"><span data-stu-id="2629c-117">If passed set the scope of the Configuration to Cluster (default is nameSpace).</span></span>

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

### <span data-ttu-id="2629c-118">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="2629c-118">-ClusterType</span></span>
<span data-ttu-id="2629c-119">Kubernetes 群集資源名稱-AKS 群集的 managedClusters () 或 OnPrem K8S 群集) 的 connectedClusters (。</span><span class="sxs-lookup"><span data-stu-id="2629c-119">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="2629c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2629c-120">-DefaultProfile</span></span>
<span data-ttu-id="2629c-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2629c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2629c-122">-EnableHelmOperator</span><span class="sxs-lookup"><span data-stu-id="2629c-122">-EnableHelmOperator</span></span>
<span data-ttu-id="2629c-123">選項，以針對此 git 設定啟用 Helm 運算子。</span><span class="sxs-lookup"><span data-stu-id="2629c-123">Option to enable Helm Operator for this git configuration.</span></span>

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

### <span data-ttu-id="2629c-124">-HelmOperatorChartValues</span><span class="sxs-lookup"><span data-stu-id="2629c-124">-HelmOperatorChartValues</span></span>
<span data-ttu-id="2629c-125">運算子 Helm 圖表的值覆寫。</span><span class="sxs-lookup"><span data-stu-id="2629c-125">Values override for the operator Helm chart.</span></span>

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

### <span data-ttu-id="2629c-126">-HelmOperatorChartVersion</span><span class="sxs-lookup"><span data-stu-id="2629c-126">-HelmOperatorChartVersion</span></span>
<span data-ttu-id="2629c-127">運算子 Helm 圖表的版本。</span><span class="sxs-lookup"><span data-stu-id="2629c-127">Version of the operator Helm chart.</span></span>

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

### <span data-ttu-id="2629c-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="2629c-128">-Name</span></span>
<span data-ttu-id="2629c-129">來源控制項配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="2629c-129">Name of the Source Control Configuration.</span></span>

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

### <span data-ttu-id="2629c-130">-OperatorInstanceName</span><span class="sxs-lookup"><span data-stu-id="2629c-130">-OperatorInstanceName</span></span>
<span data-ttu-id="2629c-131">運算子的實例名稱-識別特定的設定。</span><span class="sxs-lookup"><span data-stu-id="2629c-131">Instance name of the operator - identifying the specific configuration.</span></span>

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

### <span data-ttu-id="2629c-132">-OperatorNamespace</span><span class="sxs-lookup"><span data-stu-id="2629c-132">-OperatorNamespace</span></span>
<span data-ttu-id="2629c-133">安裝此操作員的命名空間。</span><span class="sxs-lookup"><span data-stu-id="2629c-133">The namespace to which this operator is installed to.</span></span>
<span data-ttu-id="2629c-134">最多253個小寫字母數位字元、連字號及期間。</span><span class="sxs-lookup"><span data-stu-id="2629c-134">Maximum of 253 lower case alphanumeric characters, hyphen and period only.</span></span>

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

### <span data-ttu-id="2629c-135">-OperatorParameters</span><span class="sxs-lookup"><span data-stu-id="2629c-135">-OperatorParameters</span></span>
<span data-ttu-id="2629c-136">字串格式的運算子實例的任何參數。</span><span class="sxs-lookup"><span data-stu-id="2629c-136">Any Parameters for the Operator instance in string format.</span></span>

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

### <span data-ttu-id="2629c-137">-RepositoryUrl</span><span class="sxs-lookup"><span data-stu-id="2629c-137">-RepositoryUrl</span></span>
<span data-ttu-id="2629c-138">SourceControl 存放庫的 Url。</span><span class="sxs-lookup"><span data-stu-id="2629c-138">Url of the SourceControl Repository.</span></span>

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

### <span data-ttu-id="2629c-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2629c-139">-ResourceGroupName</span></span>
<span data-ttu-id="2629c-140">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2629c-140">The name of the resource group.</span></span>

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

### <span data-ttu-id="2629c-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2629c-141">-SubscriptionId</span></span>
<span data-ttu-id="2629c-142">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="2629c-142">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="2629c-143">-確認</span><span class="sxs-lookup"><span data-stu-id="2629c-143">-Confirm</span></span>
<span data-ttu-id="2629c-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2629c-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2629c-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2629c-145">-WhatIf</span></span>
<span data-ttu-id="2629c-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2629c-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2629c-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2629c-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2629c-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2629c-148">CommonParameters</span></span>
<span data-ttu-id="2629c-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2629c-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2629c-150">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2629c-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2629c-151">輸入</span><span class="sxs-lookup"><span data-stu-id="2629c-151">INPUTS</span></span>

## <span data-ttu-id="2629c-152">輸出</span><span class="sxs-lookup"><span data-stu-id="2629c-152">OUTPUTS</span></span>

### <span data-ttu-id="2629c-153">ISourceControlConfiguration （KubernetesConfiguration）。 Api20201001Preview。</span><span class="sxs-lookup"><span data-stu-id="2629c-153">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20201001Preview.ISourceControlConfiguration</span></span>

## <span data-ttu-id="2629c-154">筆記</span><span class="sxs-lookup"><span data-stu-id="2629c-154">NOTES</span></span>

<span data-ttu-id="2629c-155">別名</span><span class="sxs-lookup"><span data-stu-id="2629c-155">ALIASES</span></span>

## <span data-ttu-id="2629c-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="2629c-156">RELATED LINKS</span></span>

