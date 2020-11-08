---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/new-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
ms.openlocfilehash: 70ff3c636f6c88ac89e53a5c2b1acb209aad274a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141631"
---
# <span data-ttu-id="efa82-101">New-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="efa82-101">New-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="efa82-102">摘要</span><span class="sxs-lookup"><span data-stu-id="efa82-102">SYNOPSIS</span></span>
<span data-ttu-id="efa82-103">建立新的 Kubernetes 來源控制項配置。</span><span class="sxs-lookup"><span data-stu-id="efa82-103">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="efa82-104">句法</span><span class="sxs-lookup"><span data-stu-id="efa82-104">SYNTAX</span></span>

```
New-AzKubernetesConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 -RepositoryUrl <String> [-ClusterType <String>] [-SubscriptionId <String>] [-ClusterScoped]
 [-EnableHelmOperator] [-HelmOperatorChartValues <String>] [-HelmOperatorChartVersion <String>]
 [-OperatorInstanceName <String>] [-OperatorNamespace <String>] [-OperatorParameters <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="efa82-105">說明</span><span class="sxs-lookup"><span data-stu-id="efa82-105">DESCRIPTION</span></span>
<span data-ttu-id="efa82-106">建立新的 Kubernetes 來源控制項配置。</span><span class="sxs-lookup"><span data-stu-id="efa82-106">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="efa82-107">示例</span><span class="sxs-lookup"><span data-stu-id="efa82-107">EXAMPLES</span></span>

### <span data-ttu-id="efa82-108">範例1：建立 kubernetes 群集的 configuation</span><span class="sxs-lookup"><span data-stu-id="efa82-108">Example 1: Create a configuation for kubernetes cluster</span></span>
```powershell
PS C:\> New-AzKubernetesConfiguration -Name conf-test01 -ClusterName connaks-d983yc -ResourceGroupName connaks-rg-w9vlnp -RepositoryUrl http://github.com/xxxx

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="efa82-109">這個命令會建立 kubernetes 群集的 configuation。</span><span class="sxs-lookup"><span data-stu-id="efa82-109">This command creates a configuation for kubernetes cluster.</span></span>

## <span data-ttu-id="efa82-110">參數</span><span class="sxs-lookup"><span data-stu-id="efa82-110">PARAMETERS</span></span>

### <span data-ttu-id="efa82-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="efa82-111">-ClusterName</span></span>
<span data-ttu-id="efa82-112">Kubernetes 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="efa82-112">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="efa82-113">-ClusterScoped</span><span class="sxs-lookup"><span data-stu-id="efa82-113">-ClusterScoped</span></span>
<span data-ttu-id="efa82-114">如果傳遞將設定的範圍設定為 [群集] (預設值為 nameSpace) 。</span><span class="sxs-lookup"><span data-stu-id="efa82-114">If passed set the scope of the Configuration to Cluster (default is nameSpace).</span></span>

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

### <span data-ttu-id="efa82-115">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="efa82-115">-ClusterType</span></span>
<span data-ttu-id="efa82-116">Kubernetes 群集資源名稱-AKS 群集的 managedClusters () 或 OnPrem K8S 群集) 的 connectedClusters (。</span><span class="sxs-lookup"><span data-stu-id="efa82-116">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="efa82-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efa82-117">-DefaultProfile</span></span>
<span data-ttu-id="efa82-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="efa82-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efa82-119">-EnableHelmOperator</span><span class="sxs-lookup"><span data-stu-id="efa82-119">-EnableHelmOperator</span></span>
<span data-ttu-id="efa82-120">選項，以針對此 git 設定啟用 Helm 運算子。</span><span class="sxs-lookup"><span data-stu-id="efa82-120">Option to enable Helm Operator for this git configuration.</span></span>

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

### <span data-ttu-id="efa82-121">-HelmOperatorChartValues</span><span class="sxs-lookup"><span data-stu-id="efa82-121">-HelmOperatorChartValues</span></span>
<span data-ttu-id="efa82-122">運算子 Helm 圖表的值覆寫。</span><span class="sxs-lookup"><span data-stu-id="efa82-122">Values override for the operator Helm chart.</span></span>

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

### <span data-ttu-id="efa82-123">-HelmOperatorChartVersion</span><span class="sxs-lookup"><span data-stu-id="efa82-123">-HelmOperatorChartVersion</span></span>
<span data-ttu-id="efa82-124">運算子 Helm 圖表的版本。</span><span class="sxs-lookup"><span data-stu-id="efa82-124">Version of the operator Helm chart.</span></span>

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

### <span data-ttu-id="efa82-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="efa82-125">-Name</span></span>
<span data-ttu-id="efa82-126">來源控制項配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="efa82-126">Name of the Source Control Configuration.</span></span>

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

### <span data-ttu-id="efa82-127">-OperatorInstanceName</span><span class="sxs-lookup"><span data-stu-id="efa82-127">-OperatorInstanceName</span></span>
<span data-ttu-id="efa82-128">運算子的實例名稱-識別特定的設定。</span><span class="sxs-lookup"><span data-stu-id="efa82-128">Instance name of the operator - identifying the specific configuration.</span></span>

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

### <span data-ttu-id="efa82-129">-OperatorNamespace</span><span class="sxs-lookup"><span data-stu-id="efa82-129">-OperatorNamespace</span></span>
<span data-ttu-id="efa82-130">安裝此操作員的命名空間。</span><span class="sxs-lookup"><span data-stu-id="efa82-130">The namespace to which this operator is installed to.</span></span>
<span data-ttu-id="efa82-131">最多253個小寫字母數位字元、連字號及期間。</span><span class="sxs-lookup"><span data-stu-id="efa82-131">Maximum of 253 lower case alphanumeric characters, hyphen and period only.</span></span>

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

### <span data-ttu-id="efa82-132">-OperatorParameters</span><span class="sxs-lookup"><span data-stu-id="efa82-132">-OperatorParameters</span></span>
<span data-ttu-id="efa82-133">字串格式的運算子實例的任何參數。</span><span class="sxs-lookup"><span data-stu-id="efa82-133">Any Parameters for the Operator instance in string format.</span></span>

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

### <span data-ttu-id="efa82-134">-RepositoryUrl</span><span class="sxs-lookup"><span data-stu-id="efa82-134">-RepositoryUrl</span></span>
<span data-ttu-id="efa82-135">SourceControl 存放庫的 Url。</span><span class="sxs-lookup"><span data-stu-id="efa82-135">Url of the SourceControl Repository.</span></span>

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

### <span data-ttu-id="efa82-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efa82-136">-ResourceGroupName</span></span>
<span data-ttu-id="efa82-137">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="efa82-137">The name of the resource group.</span></span>

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

### <span data-ttu-id="efa82-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="efa82-138">-SubscriptionId</span></span>
<span data-ttu-id="efa82-139">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="efa82-139">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="efa82-140">-確認</span><span class="sxs-lookup"><span data-stu-id="efa82-140">-Confirm</span></span>
<span data-ttu-id="efa82-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="efa82-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efa82-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efa82-142">-WhatIf</span></span>
<span data-ttu-id="efa82-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="efa82-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efa82-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="efa82-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efa82-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efa82-145">CommonParameters</span></span>
<span data-ttu-id="efa82-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="efa82-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efa82-147">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="efa82-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efa82-148">輸入</span><span class="sxs-lookup"><span data-stu-id="efa82-148">INPUTS</span></span>

## <span data-ttu-id="efa82-149">輸出</span><span class="sxs-lookup"><span data-stu-id="efa82-149">OUTPUTS</span></span>

### <span data-ttu-id="efa82-150">ISourceControlConfiguration （KubernetesConfiguration）。 Api20191101Preview。</span><span class="sxs-lookup"><span data-stu-id="efa82-150">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20191101Preview.ISourceControlConfiguration</span></span>

## <span data-ttu-id="efa82-151">筆記</span><span class="sxs-lookup"><span data-stu-id="efa82-151">NOTES</span></span>

<span data-ttu-id="efa82-152">別名</span><span class="sxs-lookup"><span data-stu-id="efa82-152">ALIASES</span></span>

## <span data-ttu-id="efa82-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="efa82-153">RELATED LINKS</span></span>

