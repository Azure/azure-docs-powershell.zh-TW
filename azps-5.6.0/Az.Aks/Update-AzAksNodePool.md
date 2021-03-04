---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/update-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
ms.openlocfilehash: 6f16664eac63ab2bb543b2d032679d979f3c2122
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916683"
---
# <span data-ttu-id="620f8-101">Update-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="620f8-101">Update-AzAksNodePool</span></span>

## <span data-ttu-id="620f8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="620f8-102">SYNOPSIS</span></span>
<span data-ttu-id="620f8-103">更新受管理之集中的節點集區。</span><span class="sxs-lookup"><span data-stu-id="620f8-103">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="620f8-104">語法</span><span class="sxs-lookup"><span data-stu-id="620f8-104">SYNTAX</span></span>

### <span data-ttu-id="620f8-105">defaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="620f8-105">defaultParameterSet (Default)</span></span>
```
Update-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="620f8-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="620f8-106">ParentObjectParameterSet</span></span>
```
Update-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="620f8-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="620f8-107">InputObjectParameterSet</span></span>
```
Update-AzAksNodePool -InputObject <PSNodePool> [-AsJob] [-Force] [-KubernetesVersion <String>]
 [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="620f8-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="620f8-108">IdParameterSet</span></span>
```
Update-AzAksNodePool -Id <String> [-AsJob] [-Force] [-KubernetesVersion <String>] [-MinCount <Int32>]
 [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="620f8-109">描述</span><span class="sxs-lookup"><span data-stu-id="620f8-109">DESCRIPTION</span></span>
<span data-ttu-id="620f8-110">更新受管理之集中的節點集區。</span><span class="sxs-lookup"><span data-stu-id="620f8-110">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="620f8-111">例子</span><span class="sxs-lookup"><span data-stu-id="620f8-111">EXAMPLES</span></span>

### <span data-ttu-id="620f8-112">將指定的節點資料庫的迷你Mun計數變更為 5</span><span class="sxs-lookup"><span data-stu-id="620f8-112">Change minimun count to 5 for specified node pool</span></span>
```powershell
PS C:\> Update-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name linuxpool -MinCount 5
```

## <span data-ttu-id="620f8-113">參數</span><span class="sxs-lookup"><span data-stu-id="620f8-113">PARAMETERS</span></span>

### <span data-ttu-id="620f8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="620f8-114">-AsJob</span></span>
<span data-ttu-id="620f8-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="620f8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="620f8-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="620f8-116">-ClusterName</span></span>
<span data-ttu-id="620f8-117">受管理的組群資源名稱。</span><span class="sxs-lookup"><span data-stu-id="620f8-117">The name of the managed cluster resource.</span></span>

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

### <span data-ttu-id="620f8-118">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="620f8-118">-ClusterObject</span></span>
<span data-ttu-id="620f8-119">該組群物件</span><span class="sxs-lookup"><span data-stu-id="620f8-119">The cluster object</span></span>

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

### <span data-ttu-id="620f8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="620f8-120">-DefaultProfile</span></span>
<span data-ttu-id="620f8-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="620f8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="620f8-122">-EnableAutoScaling</span><span class="sxs-lookup"><span data-stu-id="620f8-122">-EnableAutoScaling</span></span>
<span data-ttu-id="620f8-123">是否要啟用自動縮放</span><span class="sxs-lookup"><span data-stu-id="620f8-123">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="620f8-124">-強制</span><span class="sxs-lookup"><span data-stu-id="620f8-124">-Force</span></span>
<span data-ttu-id="620f8-125">更新節點區，而不提示</span><span class="sxs-lookup"><span data-stu-id="620f8-125">Update node pool without prompt</span></span>

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

### <span data-ttu-id="620f8-126">-Id</span><span class="sxs-lookup"><span data-stu-id="620f8-126">-Id</span></span>
<span data-ttu-id="620f8-127">受管理的 Kubernetes 集中節點集區識別碼</span><span class="sxs-lookup"><span data-stu-id="620f8-127">Id of an node pool in managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="620f8-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="620f8-128">-InputObject</span></span>
<span data-ttu-id="620f8-129">PSAgentPool 物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="620f8-129">A PSAgentPool object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="620f8-130">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="620f8-130">-KubernetesVersion</span></span>
<span data-ttu-id="620f8-131">要用於建立該組集的 Kubernetes 版本。</span><span class="sxs-lookup"><span data-stu-id="620f8-131">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="620f8-132">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="620f8-132">-MaxCount</span></span>
<span data-ttu-id="620f8-133">自動縮放的節點數目上限</span><span class="sxs-lookup"><span data-stu-id="620f8-133">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="620f8-134">-MinCount</span><span class="sxs-lookup"><span data-stu-id="620f8-134">-MinCount</span></span>
<span data-ttu-id="620f8-135">可自動縮放的節點數目最低。</span><span class="sxs-lookup"><span data-stu-id="620f8-135">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="620f8-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="620f8-136">-Name</span></span>
<span data-ttu-id="620f8-137">節點組名。</span><span class="sxs-lookup"><span data-stu-id="620f8-137">The name of the node pool.</span></span>

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

### <span data-ttu-id="620f8-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="620f8-138">-ResourceGroupName</span></span>
<span data-ttu-id="620f8-139">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="620f8-139">The name of the resource group.</span></span>

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

### <span data-ttu-id="620f8-140">-確認</span><span class="sxs-lookup"><span data-stu-id="620f8-140">-Confirm</span></span>
<span data-ttu-id="620f8-141">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="620f8-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="620f8-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="620f8-142">-WhatIf</span></span>
<span data-ttu-id="620f8-143">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="620f8-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="620f8-144">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="620f8-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="620f8-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="620f8-145">CommonParameters</span></span>
<span data-ttu-id="620f8-146">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="620f8-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="620f8-147">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="620f8-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="620f8-148">輸入</span><span class="sxs-lookup"><span data-stu-id="620f8-148">INPUTS</span></span>

### <span data-ttu-id="620f8-149">Microsoft.Azure.Commands.Aks.models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="620f8-149">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="620f8-150">System.String</span><span class="sxs-lookup"><span data-stu-id="620f8-150">System.String</span></span>

## <span data-ttu-id="620f8-151">輸出</span><span class="sxs-lookup"><span data-stu-id="620f8-151">OUTPUTS</span></span>

### <span data-ttu-id="620f8-152">Microsoft.Azure.Commands.Aks.models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="620f8-152">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="620f8-153">筆記</span><span class="sxs-lookup"><span data-stu-id="620f8-153">NOTES</span></span>

## <span data-ttu-id="620f8-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="620f8-154">RELATED LINKS</span></span>
