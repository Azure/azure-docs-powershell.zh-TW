---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/remove-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksNodePool.md
ms.openlocfilehash: 27de96fccf2c420bd15e4a7522fecc16fd3032fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912510"
---
# <span data-ttu-id="2c776-101">Remove-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="2c776-101">Remove-AzAksNodePool</span></span>

## <span data-ttu-id="2c776-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2c776-102">SYNOPSIS</span></span>
<span data-ttu-id="2c776-103">從受管理的集區刪除節點集區。</span><span class="sxs-lookup"><span data-stu-id="2c776-103">Delete node pool from managed cluster.</span></span>

## <span data-ttu-id="2c776-104">語法</span><span class="sxs-lookup"><span data-stu-id="2c776-104">SYNTAX</span></span>

### <span data-ttu-id="2c776-105">GroupNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2c776-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAksNodePool [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c776-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c776-106">InputObjectParameterSet</span></span>
```
Remove-AzAksNodePool -InputObject <PSNodePool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c776-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c776-107">IdParameterSet</span></span>
```
Remove-AzAksNodePool [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c776-108">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c776-108">ParentObjectParameterSet</span></span>
```
Remove-AzAksNodePool [-Name] <String> -ClusterObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c776-109">描述</span><span class="sxs-lookup"><span data-stu-id="2c776-109">DESCRIPTION</span></span>
<span data-ttu-id="2c776-110">從受管理的集區刪除節點集區。</span><span class="sxs-lookup"><span data-stu-id="2c776-110">Delete node pool from managed cluster.</span></span>

## <span data-ttu-id="2c776-111">例子</span><span class="sxs-lookup"><span data-stu-id="2c776-111">EXAMPLES</span></span>

### <span data-ttu-id="2c776-112">刪除指定的節點資料庫</span><span class="sxs-lookup"><span data-stu-id="2c776-112">Delete specified node pool</span></span>
```powershell
PS C:\> Remove-AzAksNodePool -ResourceGroupName myResourceGroup -CulsterName myCluster -Name winpool
```

## <span data-ttu-id="2c776-113">參數</span><span class="sxs-lookup"><span data-stu-id="2c776-113">PARAMETERS</span></span>

### <span data-ttu-id="2c776-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2c776-114">-AsJob</span></span>
<span data-ttu-id="2c776-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2c776-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2c776-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2c776-116">-ClusterName</span></span>
<span data-ttu-id="2c776-117">受管理的Kubernetes 組名</span><span class="sxs-lookup"><span data-stu-id="2c776-117">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="2c776-118">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="2c776-118">-ClusterObject</span></span>
<span data-ttu-id="2c776-119">該組物件。</span><span class="sxs-lookup"><span data-stu-id="2c776-119">The cluster object.</span></span>

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

### <span data-ttu-id="2c776-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c776-120">-DefaultProfile</span></span>
<span data-ttu-id="2c776-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2c776-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c776-122">-強制</span><span class="sxs-lookup"><span data-stu-id="2c776-122">-Force</span></span>
<span data-ttu-id="2c776-123">移除節點區，但不提示</span><span class="sxs-lookup"><span data-stu-id="2c776-123">Remove node pool without prompt</span></span>

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

### <span data-ttu-id="2c776-124">-Id</span><span class="sxs-lookup"><span data-stu-id="2c776-124">-Id</span></span>
<span data-ttu-id="2c776-125">受管理的 Kubernetes 集中節點集區識別碼</span><span class="sxs-lookup"><span data-stu-id="2c776-125">Id of an node pool in managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="2c776-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c776-126">-InputObject</span></span>
<span data-ttu-id="2c776-127">PSAgentPool 物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="2c776-127">A PSAgentPool object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="2c776-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="2c776-128">-Name</span></span>
<span data-ttu-id="2c776-129">節點組名</span><span class="sxs-lookup"><span data-stu-id="2c776-129">Name of your node pool</span></span>

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

### <span data-ttu-id="2c776-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c776-130">-PassThru</span></span>
<span data-ttu-id="2c776-131">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="2c776-131">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="2c776-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c776-132">-ResourceGroupName</span></span>
<span data-ttu-id="2c776-133">資源組名</span><span class="sxs-lookup"><span data-stu-id="2c776-133">Resource group name</span></span>

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

### <span data-ttu-id="2c776-134">-確認</span><span class="sxs-lookup"><span data-stu-id="2c776-134">-Confirm</span></span>
<span data-ttu-id="2c776-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2c776-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c776-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c776-136">-WhatIf</span></span>
<span data-ttu-id="2c776-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2c776-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c776-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2c776-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c776-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c776-139">CommonParameters</span></span>
<span data-ttu-id="2c776-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2c776-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c776-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2c776-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c776-142">輸入</span><span class="sxs-lookup"><span data-stu-id="2c776-142">INPUTS</span></span>

### <span data-ttu-id="2c776-143">Microsoft.Azure.Commands.Aks.models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="2c776-143">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="2c776-144">System.String</span><span class="sxs-lookup"><span data-stu-id="2c776-144">System.String</span></span>

## <span data-ttu-id="2c776-145">輸出</span><span class="sxs-lookup"><span data-stu-id="2c776-145">OUTPUTS</span></span>

### <span data-ttu-id="2c776-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2c776-146">System.Boolean</span></span>

## <span data-ttu-id="2c776-147">筆記</span><span class="sxs-lookup"><span data-stu-id="2c776-147">NOTES</span></span>

## <span data-ttu-id="2c776-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="2c776-148">RELATED LINKS</span></span>
