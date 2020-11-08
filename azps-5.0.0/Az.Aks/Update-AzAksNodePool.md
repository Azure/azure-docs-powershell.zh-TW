---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/update-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
ms.openlocfilehash: a3849a07f83cda8876acdf87015e8f2fc9fe81b5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139339"
---
# <span data-ttu-id="46bc5-101">Update-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="46bc5-101">Update-AzAksNodePool</span></span>

## <span data-ttu-id="46bc5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="46bc5-102">SYNOPSIS</span></span>
<span data-ttu-id="46bc5-103">更新受管理的群集中的節點池。</span><span class="sxs-lookup"><span data-stu-id="46bc5-103">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="46bc5-104">句法</span><span class="sxs-lookup"><span data-stu-id="46bc5-104">SYNTAX</span></span>

### <span data-ttu-id="46bc5-105">defaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="46bc5-105">defaultParameterSet (Default)</span></span>
```
Update-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46bc5-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="46bc5-106">ParentObjectParameterSet</span></span>
```
Update-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46bc5-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="46bc5-107">InputObjectParameterSet</span></span>
```
Update-AzAksNodePool -InputObject <PSNodePool> [-AsJob] [-Force] [-KubernetesVersion <String>]
 [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46bc5-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="46bc5-108">IdParameterSet</span></span>
```
Update-AzAksNodePool -Id <String> [-AsJob] [-Force] [-KubernetesVersion <String>] [-MinCount <Int32>]
 [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="46bc5-109">說明</span><span class="sxs-lookup"><span data-stu-id="46bc5-109">DESCRIPTION</span></span>
<span data-ttu-id="46bc5-110">更新受管理的群集中的節點池。</span><span class="sxs-lookup"><span data-stu-id="46bc5-110">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="46bc5-111">示例</span><span class="sxs-lookup"><span data-stu-id="46bc5-111">EXAMPLES</span></span>

### <span data-ttu-id="46bc5-112">針對指定的節點池，將 minimun 計數變更為5</span><span class="sxs-lookup"><span data-stu-id="46bc5-112">Change minimun count to 5 for specified node pool</span></span>
```powershell
PS C:\> Update-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name linuxpool -MinCount 5
```

## <span data-ttu-id="46bc5-113">參數</span><span class="sxs-lookup"><span data-stu-id="46bc5-113">PARAMETERS</span></span>

### <span data-ttu-id="46bc5-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46bc5-114">-AsJob</span></span>
<span data-ttu-id="46bc5-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46bc5-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="46bc5-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="46bc5-116">-ClusterName</span></span>
<span data-ttu-id="46bc5-117">受管理的群集資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="46bc5-117">The name of the managed cluster resource.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46bc5-118">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="46bc5-118">-ClusterObject</span></span>
<span data-ttu-id="46bc5-119">Cluster 物件</span><span class="sxs-lookup"><span data-stu-id="46bc5-119">The cluster object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46bc5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46bc5-120">-DefaultProfile</span></span>
<span data-ttu-id="46bc5-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="46bc5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46bc5-122">-EnableAutoScaling</span><span class="sxs-lookup"><span data-stu-id="46bc5-122">-EnableAutoScaling</span></span>
<span data-ttu-id="46bc5-123">是否要啟用自動 scaler</span><span class="sxs-lookup"><span data-stu-id="46bc5-123">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="46bc5-124">-Force</span><span class="sxs-lookup"><span data-stu-id="46bc5-124">-Force</span></span>
<span data-ttu-id="46bc5-125">在不提示的情況下更新節點池</span><span class="sxs-lookup"><span data-stu-id="46bc5-125">Update node pool without prompt</span></span>

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

### <span data-ttu-id="46bc5-126">-識別碼</span><span class="sxs-lookup"><span data-stu-id="46bc5-126">-Id</span></span>
<span data-ttu-id="46bc5-127">受管理的 Kubernetes 群集中的節點池 Id</span><span class="sxs-lookup"><span data-stu-id="46bc5-127">Id of an node pool in managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46bc5-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46bc5-128">-InputObject</span></span>
<span data-ttu-id="46bc5-129">PSAgentPool 物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="46bc5-129">A PSAgentPool object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSNodePool
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46bc5-130">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="46bc5-130">-KubernetesVersion</span></span>
<span data-ttu-id="46bc5-131">要用來建立群集的 Kubernetes 版本。</span><span class="sxs-lookup"><span data-stu-id="46bc5-131">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="46bc5-132">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="46bc5-132">-MaxCount</span></span>
<span data-ttu-id="46bc5-133">自動調整的最大節點數</span><span class="sxs-lookup"><span data-stu-id="46bc5-133">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="46bc5-134">-MinCount</span><span class="sxs-lookup"><span data-stu-id="46bc5-134">-MinCount</span></span>
<span data-ttu-id="46bc5-135">自動縮放的最小節點數。</span><span class="sxs-lookup"><span data-stu-id="46bc5-135">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="46bc5-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="46bc5-136">-Name</span></span>
<span data-ttu-id="46bc5-137">節點池的名稱。</span><span class="sxs-lookup"><span data-stu-id="46bc5-137">The name of the node pool.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet, ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46bc5-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46bc5-138">-ResourceGroupName</span></span>
<span data-ttu-id="46bc5-139">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="46bc5-139">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46bc5-140">-確認</span><span class="sxs-lookup"><span data-stu-id="46bc5-140">-Confirm</span></span>
<span data-ttu-id="46bc5-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="46bc5-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46bc5-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46bc5-142">-WhatIf</span></span>
<span data-ttu-id="46bc5-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="46bc5-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46bc5-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="46bc5-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46bc5-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46bc5-145">CommonParameters</span></span>
<span data-ttu-id="46bc5-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="46bc5-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46bc5-147">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="46bc5-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46bc5-148">輸入</span><span class="sxs-lookup"><span data-stu-id="46bc5-148">INPUTS</span></span>

### <span data-ttu-id="46bc5-149">PSNodePool 中的 Aks。</span><span class="sxs-lookup"><span data-stu-id="46bc5-149">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="46bc5-150">System.object</span><span class="sxs-lookup"><span data-stu-id="46bc5-150">System.String</span></span>

## <span data-ttu-id="46bc5-151">輸出</span><span class="sxs-lookup"><span data-stu-id="46bc5-151">OUTPUTS</span></span>

### <span data-ttu-id="46bc5-152">PSNodePool 中的 Aks。</span><span class="sxs-lookup"><span data-stu-id="46bc5-152">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="46bc5-153">筆記</span><span class="sxs-lookup"><span data-stu-id="46bc5-153">NOTES</span></span>

## <span data-ttu-id="46bc5-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="46bc5-154">RELATED LINKS</span></span>