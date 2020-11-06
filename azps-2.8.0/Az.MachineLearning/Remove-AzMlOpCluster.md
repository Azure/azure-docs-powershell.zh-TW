---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/remove-azmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlOpCluster.md
ms.openlocfilehash: de297c94be69773d07efedfae42ccc029fc13414
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611904"
---
# <span data-ttu-id="dd0f2-101">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="dd0f2-101">Remove-AzMlOpCluster</span></span>

## <span data-ttu-id="dd0f2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dd0f2-102">SYNOPSIS</span></span>
<span data-ttu-id="dd0f2-103">移除 operationalization 群集。</span><span class="sxs-lookup"><span data-stu-id="dd0f2-103">Removes an operationalization cluster.</span></span>

## <span data-ttu-id="dd0f2-104">句法</span><span class="sxs-lookup"><span data-stu-id="dd0f2-104">SYNTAX</span></span>

### <span data-ttu-id="dd0f2-105">RemoveByNameAndResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="dd0f2-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzMlOpCluster -ResourceGroupName <String> -Name <String> [-IncludeAllResources]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd0f2-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="dd0f2-106">RemoveByInputObject</span></span>
```
Remove-AzMlOpCluster -InputObject <PSOperationalizationCluster> [-IncludeAllResources]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd0f2-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="dd0f2-107">RemoveByResourceId</span></span>
```
Remove-AzMlOpCluster -ResourceId <String> [-IncludeAllResources] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd0f2-108">說明</span><span class="sxs-lookup"><span data-stu-id="dd0f2-108">DESCRIPTION</span></span>
<span data-ttu-id="dd0f2-109">移除 operationalization 群集。</span><span class="sxs-lookup"><span data-stu-id="dd0f2-109">Removes an operationalization cluster.</span></span> <span data-ttu-id="dd0f2-110">某些與群集相關的資源可能不會全部移除。</span><span class="sxs-lookup"><span data-stu-id="dd0f2-110">Some resources associated with the cluster might not all be removed.</span></span> <span data-ttu-id="dd0f2-111">例如，Azure 容器服務將會移除，但相關的虛擬機器則不會。</span><span class="sxs-lookup"><span data-stu-id="dd0f2-111">For example, the Azure container service will get removed, but the associated VMs do not.</span></span> <span data-ttu-id="dd0f2-112">針對診斷資訊，不會移除儲存空間帳戶、容器註冊表及 application insights。</span><span class="sxs-lookup"><span data-stu-id="dd0f2-112">The storage account, container registry, and application insights are not removed for diagnostic information.</span></span>

## <span data-ttu-id="dd0f2-113">示例</span><span class="sxs-lookup"><span data-stu-id="dd0f2-113">EXAMPLES</span></span>

### <span data-ttu-id="dd0f2-114">範例1</span><span class="sxs-lookup"><span data-stu-id="dd0f2-114">Example 1</span></span>
```
PS C:\> Remove-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="dd0f2-115">範例2</span><span class="sxs-lookup"><span data-stu-id="dd0f2-115">Example 2</span></span>
```
PS C:\> Get-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster | Remove-AzMlOpCluster
```

## <span data-ttu-id="dd0f2-116">參數</span><span class="sxs-lookup"><span data-stu-id="dd0f2-116">PARAMETERS</span></span>

### <span data-ttu-id="dd0f2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd0f2-117">-DefaultProfile</span></span>
<span data-ttu-id="dd0f2-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dd0f2-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd0f2-119">-IncludeAllResources</span><span class="sxs-lookup"><span data-stu-id="dd0f2-119">-IncludeAllResources</span></span>
<span data-ttu-id="dd0f2-120">移除所有與該群集建立的資源。</span><span class="sxs-lookup"><span data-stu-id="dd0f2-120">Removes all resources that were created with the cluster.</span></span>

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

### <span data-ttu-id="dd0f2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd0f2-121">-InputObject</span></span>
<span data-ttu-id="dd0f2-122">Operationalization 群集物件。</span><span class="sxs-lookup"><span data-stu-id="dd0f2-122">The operationalization cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: RemoveByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd0f2-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="dd0f2-123">-Name</span></span>
<span data-ttu-id="dd0f2-124">Operationalization 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd0f2-124">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd0f2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd0f2-125">-ResourceGroupName</span></span>
<span data-ttu-id="dd0f2-126">Operationalization 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd0f2-126">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd0f2-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd0f2-127">-ResourceId</span></span>
<span data-ttu-id="dd0f2-128">Operationalization 群集的 Azure 資源 id。</span><span class="sxs-lookup"><span data-stu-id="dd0f2-128">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd0f2-129">-確認</span><span class="sxs-lookup"><span data-stu-id="dd0f2-129">-Confirm</span></span>
<span data-ttu-id="dd0f2-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dd0f2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd0f2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd0f2-131">-WhatIf</span></span>
<span data-ttu-id="dd0f2-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dd0f2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd0f2-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dd0f2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd0f2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd0f2-134">CommonParameters</span></span>
<span data-ttu-id="dd0f2-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dd0f2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd0f2-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dd0f2-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd0f2-137">輸入</span><span class="sxs-lookup"><span data-stu-id="dd0f2-137">INPUTS</span></span>

### <span data-ttu-id="dd0f2-138">PSOperationalizationCluster 中的 MachineLearningCompute。</span><span class="sxs-lookup"><span data-stu-id="dd0f2-138">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="dd0f2-139">System.object</span><span class="sxs-lookup"><span data-stu-id="dd0f2-139">System.String</span></span>

## <span data-ttu-id="dd0f2-140">輸出</span><span class="sxs-lookup"><span data-stu-id="dd0f2-140">OUTPUTS</span></span>

### <span data-ttu-id="dd0f2-141">System.void</span><span class="sxs-lookup"><span data-stu-id="dd0f2-141">System.Void</span></span>

## <span data-ttu-id="dd0f2-142">筆記</span><span class="sxs-lookup"><span data-stu-id="dd0f2-142">NOTES</span></span>

## <span data-ttu-id="dd0f2-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="dd0f2-143">RELATED LINKS</span></span>
