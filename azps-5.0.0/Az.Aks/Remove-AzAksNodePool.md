---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/remove-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksNodePool.md
ms.openlocfilehash: 13bc647a0b2cbbc415c12aabb9e14016e3d34149
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138552"
---
# <span data-ttu-id="1bbb2-101">Remove-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="1bbb2-101">Remove-AzAksNodePool</span></span>

## <span data-ttu-id="1bbb2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1bbb2-102">SYNOPSIS</span></span>
<span data-ttu-id="1bbb2-103">從受管理的群集刪除節點池。</span><span class="sxs-lookup"><span data-stu-id="1bbb2-103">Delete node pool from managed cluster.</span></span>

## <span data-ttu-id="1bbb2-104">句法</span><span class="sxs-lookup"><span data-stu-id="1bbb2-104">SYNTAX</span></span>

### <span data-ttu-id="1bbb2-105">GroupNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1bbb2-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAksNodePool [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bbb2-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1bbb2-106">InputObjectParameterSet</span></span>
```
Remove-AzAksNodePool -InputObject <PSNodePool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bbb2-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1bbb2-107">IdParameterSet</span></span>
```
Remove-AzAksNodePool [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bbb2-108">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1bbb2-108">ParentObjectParameterSet</span></span>
```
Remove-AzAksNodePool [-Name] <String> -ClusterObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bbb2-109">說明</span><span class="sxs-lookup"><span data-stu-id="1bbb2-109">DESCRIPTION</span></span>
<span data-ttu-id="1bbb2-110">從受管理的群集刪除節點池。</span><span class="sxs-lookup"><span data-stu-id="1bbb2-110">Delete node pool from managed cluster.</span></span>

## <span data-ttu-id="1bbb2-111">示例</span><span class="sxs-lookup"><span data-stu-id="1bbb2-111">EXAMPLES</span></span>

### <span data-ttu-id="1bbb2-112">刪除指定的節點池</span><span class="sxs-lookup"><span data-stu-id="1bbb2-112">Delete specified node pool</span></span>
```powershell
PS C:\> Remove-AzAksNodePool -ResourceGroupName myResourceGroup -CulsterName myCluster -Name winpool
```

## <span data-ttu-id="1bbb2-113">參數</span><span class="sxs-lookup"><span data-stu-id="1bbb2-113">PARAMETERS</span></span>

### <span data-ttu-id="1bbb2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1bbb2-114">-AsJob</span></span>
<span data-ttu-id="1bbb2-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1bbb2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1bbb2-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1bbb2-116">-ClusterName</span></span>
<span data-ttu-id="1bbb2-117">受管理的 Kubernetes 群集的名稱</span><span class="sxs-lookup"><span data-stu-id="1bbb2-117">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bbb2-118">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="1bbb2-118">-ClusterObject</span></span>
<span data-ttu-id="1bbb2-119">群集物件。</span><span class="sxs-lookup"><span data-stu-id="1bbb2-119">The cluster object.</span></span>

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

### <span data-ttu-id="1bbb2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bbb2-120">-DefaultProfile</span></span>
<span data-ttu-id="1bbb2-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1bbb2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bbb2-122">-Force</span><span class="sxs-lookup"><span data-stu-id="1bbb2-122">-Force</span></span>
<span data-ttu-id="1bbb2-123">移除節點池而不提示</span><span class="sxs-lookup"><span data-stu-id="1bbb2-123">Remove node pool without prompt</span></span>

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

### <span data-ttu-id="1bbb2-124">-識別碼</span><span class="sxs-lookup"><span data-stu-id="1bbb2-124">-Id</span></span>
<span data-ttu-id="1bbb2-125">受管理的 Kubernetes 群集中的節點池 Id</span><span class="sxs-lookup"><span data-stu-id="1bbb2-125">Id of an node pool in managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="1bbb2-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1bbb2-126">-InputObject</span></span>
<span data-ttu-id="1bbb2-127">PSAgentPool 物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="1bbb2-127">A PSAgentPool object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="1bbb2-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="1bbb2-128">-Name</span></span>
<span data-ttu-id="1bbb2-129">您節點池的名稱</span><span class="sxs-lookup"><span data-stu-id="1bbb2-129">Name of your node pool</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet, ParentObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bbb2-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1bbb2-130">-PassThru</span></span>
<span data-ttu-id="1bbb2-131">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="1bbb2-131">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="1bbb2-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bbb2-132">-ResourceGroupName</span></span>
<span data-ttu-id="1bbb2-133">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="1bbb2-133">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bbb2-134">-確認</span><span class="sxs-lookup"><span data-stu-id="1bbb2-134">-Confirm</span></span>
<span data-ttu-id="1bbb2-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1bbb2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bbb2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bbb2-136">-WhatIf</span></span>
<span data-ttu-id="1bbb2-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1bbb2-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bbb2-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1bbb2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bbb2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bbb2-139">CommonParameters</span></span>
<span data-ttu-id="1bbb2-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1bbb2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bbb2-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1bbb2-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bbb2-142">輸入</span><span class="sxs-lookup"><span data-stu-id="1bbb2-142">INPUTS</span></span>

### <span data-ttu-id="1bbb2-143">PSNodePool 中的 Aks。</span><span class="sxs-lookup"><span data-stu-id="1bbb2-143">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="1bbb2-144">System.object</span><span class="sxs-lookup"><span data-stu-id="1bbb2-144">System.String</span></span>

## <span data-ttu-id="1bbb2-145">輸出</span><span class="sxs-lookup"><span data-stu-id="1bbb2-145">OUTPUTS</span></span>

### <span data-ttu-id="1bbb2-146">System.object</span><span class="sxs-lookup"><span data-stu-id="1bbb2-146">System.Boolean</span></span>

## <span data-ttu-id="1bbb2-147">筆記</span><span class="sxs-lookup"><span data-stu-id="1bbb2-147">NOTES</span></span>

## <span data-ttu-id="1bbb2-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="1bbb2-148">RELATED LINKS</span></span>