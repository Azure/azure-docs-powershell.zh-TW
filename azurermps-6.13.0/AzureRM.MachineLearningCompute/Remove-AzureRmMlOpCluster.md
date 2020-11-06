---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/remove-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
ms.openlocfilehash: 5619b9ca4e7f5593a20baf04951d0d5594b31215
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446978"
---
# <span data-ttu-id="59b43-101">Remove-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="59b43-101">Remove-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="59b43-102">摘要</span><span class="sxs-lookup"><span data-stu-id="59b43-102">SYNOPSIS</span></span>
<span data-ttu-id="59b43-103">移除 operationalization 群集。</span><span class="sxs-lookup"><span data-stu-id="59b43-103">Removes an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59b43-104">句法</span><span class="sxs-lookup"><span data-stu-id="59b43-104">SYNTAX</span></span>

### <span data-ttu-id="59b43-105">RemoveByNameAndResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="59b43-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-IncludeAllResources]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59b43-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="59b43-106">RemoveByInputObject</span></span>
```
Remove-AzureRmMlOpCluster -InputObject <PSOperationalizationCluster> [-IncludeAllResources]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59b43-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="59b43-107">RemoveByResourceId</span></span>
```
Remove-AzureRmMlOpCluster -ResourceId <String> [-IncludeAllResources]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59b43-108">說明</span><span class="sxs-lookup"><span data-stu-id="59b43-108">DESCRIPTION</span></span>
<span data-ttu-id="59b43-109">移除 operationalization 群集。</span><span class="sxs-lookup"><span data-stu-id="59b43-109">Removes an operationalization cluster.</span></span> <span data-ttu-id="59b43-110">某些與群集相關的資源可能不會全部移除。</span><span class="sxs-lookup"><span data-stu-id="59b43-110">Some resources associated with the cluster might not all be removed.</span></span> <span data-ttu-id="59b43-111">例如，Azure 容器服務將會移除，但相關的虛擬機器則不會。</span><span class="sxs-lookup"><span data-stu-id="59b43-111">For example, the Azure container service will get removed, but the associated VMs do not.</span></span> <span data-ttu-id="59b43-112">針對診斷資訊，不會移除儲存空間帳戶、容器註冊表及 application insights。</span><span class="sxs-lookup"><span data-stu-id="59b43-112">The storage account, container registry, and application insights are not removed for diagnostic information.</span></span>

## <span data-ttu-id="59b43-113">示例</span><span class="sxs-lookup"><span data-stu-id="59b43-113">EXAMPLES</span></span>

### <span data-ttu-id="59b43-114">範例1</span><span class="sxs-lookup"><span data-stu-id="59b43-114">Example 1</span></span>
```
PS C:\> Remove-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="59b43-115">範例2</span><span class="sxs-lookup"><span data-stu-id="59b43-115">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster | Remove-AzureRmMlOpCluster
```

## <span data-ttu-id="59b43-116">參數</span><span class="sxs-lookup"><span data-stu-id="59b43-116">PARAMETERS</span></span>

### <span data-ttu-id="59b43-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59b43-117">-DefaultProfile</span></span>
<span data-ttu-id="59b43-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="59b43-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59b43-119">-IncludeAllResources</span><span class="sxs-lookup"><span data-stu-id="59b43-119">-IncludeAllResources</span></span>
<span data-ttu-id="59b43-120">移除所有與該群集建立的資源。</span><span class="sxs-lookup"><span data-stu-id="59b43-120">Removes all resources that were created with the cluster.</span></span>

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

### <span data-ttu-id="59b43-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59b43-121">-InputObject</span></span>
<span data-ttu-id="59b43-122">Operationalization 群集物件。</span><span class="sxs-lookup"><span data-stu-id="59b43-122">The operationalization cluster object.</span></span>

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

### <span data-ttu-id="59b43-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="59b43-123">-Name</span></span>
<span data-ttu-id="59b43-124">Operationalization 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="59b43-124">The name of the operationalization cluster.</span></span>

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

### <span data-ttu-id="59b43-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59b43-125">-ResourceGroupName</span></span>
<span data-ttu-id="59b43-126">Operationalization 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="59b43-126">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="59b43-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59b43-127">-ResourceId</span></span>
<span data-ttu-id="59b43-128">Operationalization 群集的 Azure 資源 id。</span><span class="sxs-lookup"><span data-stu-id="59b43-128">The Azure resource id for the operationalization cluster.</span></span>

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

### <span data-ttu-id="59b43-129">-確認</span><span class="sxs-lookup"><span data-stu-id="59b43-129">-Confirm</span></span>
<span data-ttu-id="59b43-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="59b43-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59b43-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59b43-131">-WhatIf</span></span>
<span data-ttu-id="59b43-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="59b43-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59b43-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="59b43-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59b43-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59b43-134">CommonParameters</span></span>
<span data-ttu-id="59b43-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="59b43-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59b43-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="59b43-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59b43-137">輸入</span><span class="sxs-lookup"><span data-stu-id="59b43-137">INPUTS</span></span>

### <span data-ttu-id="59b43-138">PSOperationalizationCluster 中的 MachineLearningCompute。</span><span class="sxs-lookup"><span data-stu-id="59b43-138">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="59b43-139">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="59b43-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="59b43-140">System.object</span><span class="sxs-lookup"><span data-stu-id="59b43-140">System.String</span></span>

## <span data-ttu-id="59b43-141">輸出</span><span class="sxs-lookup"><span data-stu-id="59b43-141">OUTPUTS</span></span>

### <span data-ttu-id="59b43-142">System.void</span><span class="sxs-lookup"><span data-stu-id="59b43-142">System.Void</span></span>

## <span data-ttu-id="59b43-143">筆記</span><span class="sxs-lookup"><span data-stu-id="59b43-143">NOTES</span></span>

## <span data-ttu-id="59b43-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="59b43-144">RELATED LINKS</span></span>
