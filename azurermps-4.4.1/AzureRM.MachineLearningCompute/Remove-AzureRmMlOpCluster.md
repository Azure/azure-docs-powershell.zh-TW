---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
ms.openlocfilehash: 63e401c09a2d224b53d260855990198a409d4846
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624553"
---
# <span data-ttu-id="8fc53-101">Remove-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="8fc53-101">Remove-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="8fc53-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8fc53-102">SYNOPSIS</span></span>
<span data-ttu-id="8fc53-103">移除 operationalization 群集。</span><span class="sxs-lookup"><span data-stu-id="8fc53-103">Removes an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fc53-104">句法</span><span class="sxs-lookup"><span data-stu-id="8fc53-104">SYNTAX</span></span>

### <span data-ttu-id="8fc53-105">從 Cmdlet 輸入參數中移除 operationalization 群集。</span><span class="sxs-lookup"><span data-stu-id="8fc53-105">Remove an operationalization cluster from cmdlet input parameters.</span></span>
```
Remove-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="8fc53-106">從 OperationalizationCluster 實例定義中移除 operationalization 群集。</span><span class="sxs-lookup"><span data-stu-id="8fc53-106">Remove an operationalization cluster from an OperationalizationCluster instance definition.</span></span>
```
Remove-AzureRmMlOpCluster -InputObject <PSOperationalizationCluster> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="8fc53-107">從 Azure 資源識別碼中移除 operationalization 群集。</span><span class="sxs-lookup"><span data-stu-id="8fc53-107">Remove an operationalization cluster from an Azure resouce id.</span></span>
```
Remove-AzureRmMlOpCluster -ResourceId <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="8fc53-108">說明</span><span class="sxs-lookup"><span data-stu-id="8fc53-108">DESCRIPTION</span></span>
<span data-ttu-id="8fc53-109">移除 operationalization 群集。</span><span class="sxs-lookup"><span data-stu-id="8fc53-109">Removes an operationalization cluster.</span></span> <span data-ttu-id="8fc53-110">某些與群集相關的資源可能不會全部移除。</span><span class="sxs-lookup"><span data-stu-id="8fc53-110">Some resources associated with the cluster might not all be removed.</span></span> <span data-ttu-id="8fc53-111">例如，Azure 容器服務將會移除，但相關的虛擬機器則不會。</span><span class="sxs-lookup"><span data-stu-id="8fc53-111">For example, the Azure container service will get removed, but the associated VMs do not.</span></span> <span data-ttu-id="8fc53-112">針對診斷資訊，不會移除儲存空間帳戶、容器註冊表及 application insights。</span><span class="sxs-lookup"><span data-stu-id="8fc53-112">The storage account, container registry, and application insights are not removed for diagnostic information.</span></span>

## <span data-ttu-id="8fc53-113">示例</span><span class="sxs-lookup"><span data-stu-id="8fc53-113">EXAMPLES</span></span>

### <span data-ttu-id="8fc53-114">範例1</span><span class="sxs-lookup"><span data-stu-id="8fc53-114">Example 1</span></span>
```
PS C:\> Remove-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="8fc53-115">範例2</span><span class="sxs-lookup"><span data-stu-id="8fc53-115">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster | Remove-AzureRmMlOpCluster 
```

## <span data-ttu-id="8fc53-116">參數</span><span class="sxs-lookup"><span data-stu-id="8fc53-116">PARAMETERS</span></span>

### <span data-ttu-id="8fc53-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8fc53-117">-InputObject</span></span>
<span data-ttu-id="8fc53-118">Operationalization 群集物件。</span><span class="sxs-lookup"><span data-stu-id="8fc53-118">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Remove an operationalization cluster from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8fc53-119">-確認</span><span class="sxs-lookup"><span data-stu-id="8fc53-119">-Confirm</span></span>
<span data-ttu-id="8fc53-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8fc53-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc53-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="8fc53-121">-Name</span></span>
<span data-ttu-id="8fc53-122">Operationalization 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="8fc53-122">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Remove an operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc53-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fc53-123">-ResourceGroupName</span></span>
<span data-ttu-id="8fc53-124">Operationalization 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8fc53-124">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Remove an operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc53-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8fc53-125">-ResourceId</span></span>
<span data-ttu-id="8fc53-126">Operationalization 群集的 Azure 資源 id。</span><span class="sxs-lookup"><span data-stu-id="8fc53-126">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Remove an operationalization cluster from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fc53-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fc53-127">-WhatIf</span></span>
<span data-ttu-id="8fc53-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8fc53-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fc53-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8fc53-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="8fc53-130">輸入</span><span class="sxs-lookup"><span data-stu-id="8fc53-130">INPUTS</span></span>

### <span data-ttu-id="8fc53-131">PSOperationalizationCluster 中的 MachineLearningCompute。</span><span class="sxs-lookup"><span data-stu-id="8fc53-131">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
### <span data-ttu-id="8fc53-132">System.object</span><span class="sxs-lookup"><span data-stu-id="8fc53-132">System.String</span></span>


## <span data-ttu-id="8fc53-133">輸出</span><span class="sxs-lookup"><span data-stu-id="8fc53-133">OUTPUTS</span></span>

### <span data-ttu-id="8fc53-134">System.void</span><span class="sxs-lookup"><span data-stu-id="8fc53-134">System.Void</span></span>


## <span data-ttu-id="8fc53-135">筆記</span><span class="sxs-lookup"><span data-stu-id="8fc53-135">NOTES</span></span>

## <span data-ttu-id="8fc53-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="8fc53-136">RELATED LINKS</span></span>

