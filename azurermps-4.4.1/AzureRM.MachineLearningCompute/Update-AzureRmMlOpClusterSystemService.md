---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Update-AzureRmMlOpClusterSystemService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Update-AzureRmMlOpClusterSystemService.md
ms.openlocfilehash: fc89ff40c36fc444eec23089288849aa5ffe592c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456540"
---
# <span data-ttu-id="e7bd6-101">Update-AzureRmMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="e7bd6-101">Update-AzureRmMlOpClusterSystemService</span></span>

## <span data-ttu-id="e7bd6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e7bd6-102">SYNOPSIS</span></span>
<span data-ttu-id="e7bd6-103">在 operationalization 群集的系統服務上開始更新。</span><span class="sxs-lookup"><span data-stu-id="e7bd6-103">Starts an update on the operationalization cluster's system services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7bd6-104">句法</span><span class="sxs-lookup"><span data-stu-id="e7bd6-104">SYNTAX</span></span>

### <span data-ttu-id="e7bd6-105">從 Cmdlet 的輸入參數開始進行系統服務更新。</span><span class="sxs-lookup"><span data-stu-id="e7bd6-105">Start a system services update from cmdlet input parameters.</span></span>
```
Update-AzureRmMlOpClusterSystemService -ResourceGroupName <String> -Name <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="e7bd6-106">從 PSOperationalizationCluster 實例定義啟動系統服務更新。</span><span class="sxs-lookup"><span data-stu-id="e7bd6-106">Start a system services update from an PSOperationalizationCluster instance definition.</span></span>
```
Update-AzureRmMlOpClusterSystemService -InputObject <PSOperationalizationCluster> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="e7bd6-107">從 Azure 資源識別碼啟動系統服務更新。</span><span class="sxs-lookup"><span data-stu-id="e7bd6-107">Start a system services update from an Azure resouce id.</span></span>
```
Update-AzureRmMlOpClusterSystemService -ResourceId <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="e7bd6-108">說明</span><span class="sxs-lookup"><span data-stu-id="e7bd6-108">DESCRIPTION</span></span>
<span data-ttu-id="e7bd6-109">系統服務可以獨立于 operationalization 群集進行更新。</span><span class="sxs-lookup"><span data-stu-id="e7bd6-109">The system services can be updated independently from the operationalization cluster.</span></span> <span data-ttu-id="e7bd6-110">若要在系統服務上開始更新，請使用此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e7bd6-110">To start an update on the system services use this cmdlet.</span></span> <span data-ttu-id="e7bd6-111">如果沒有可用的更新，更新仍會啟動並成功返回。</span><span class="sxs-lookup"><span data-stu-id="e7bd6-111">If no update is available an update will still be started and will return successfully.</span></span> <span data-ttu-id="e7bd6-112">更新完成之後，就會報告它開始、完成及是否成功。</span><span class="sxs-lookup"><span data-stu-id="e7bd6-112">Once the update is finished it reports when it started, finished, and if it was successful.</span></span>

## <span data-ttu-id="e7bd6-113">示例</span><span class="sxs-lookup"><span data-stu-id="e7bd6-113">EXAMPLES</span></span>

### <span data-ttu-id="e7bd6-114">範例1</span><span class="sxs-lookup"><span data-stu-id="e7bd6-114">Example 1</span></span>
```
PS C:\> Update-AzureRmMlOpClusterSystemService -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="e7bd6-115">在指定的群集上啟動系統服務更新。</span><span class="sxs-lookup"><span data-stu-id="e7bd6-115">Starts a system services update on the specified cluster.</span></span> 

## <span data-ttu-id="e7bd6-116">參數</span><span class="sxs-lookup"><span data-stu-id="e7bd6-116">PARAMETERS</span></span>

### <span data-ttu-id="e7bd6-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7bd6-117">-InputObject</span></span>
<span data-ttu-id="e7bd6-118">Operationalization 群集物件。</span><span class="sxs-lookup"><span data-stu-id="e7bd6-118">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Start a system services update from an PSOperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7bd6-119">-確認</span><span class="sxs-lookup"><span data-stu-id="e7bd6-119">-Confirm</span></span>
<span data-ttu-id="e7bd6-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e7bd6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7bd6-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="e7bd6-121">-Name</span></span>
<span data-ttu-id="e7bd6-122">Operationalization 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7bd6-122">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Start a system services update from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7bd6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7bd6-123">-ResourceGroupName</span></span>
<span data-ttu-id="e7bd6-124">Operationalization 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7bd6-124">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Start a system services update from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7bd6-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7bd6-125">-ResourceId</span></span>
<span data-ttu-id="e7bd6-126">Operationalization 群集的 Azure 資源 id。</span><span class="sxs-lookup"><span data-stu-id="e7bd6-126">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Start a system services update from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7bd6-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7bd6-127">-WhatIf</span></span>
<span data-ttu-id="e7bd6-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e7bd6-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7bd6-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e7bd6-129">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="e7bd6-130">輸入</span><span class="sxs-lookup"><span data-stu-id="e7bd6-130">INPUTS</span></span>

### <span data-ttu-id="e7bd6-131">PSOperationalizationCluster 中的 MachineLearningCompute。</span><span class="sxs-lookup"><span data-stu-id="e7bd6-131">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
### <span data-ttu-id="e7bd6-132">System.object</span><span class="sxs-lookup"><span data-stu-id="e7bd6-132">System.String</span></span>


## <span data-ttu-id="e7bd6-133">輸出</span><span class="sxs-lookup"><span data-stu-id="e7bd6-133">OUTPUTS</span></span>

### <span data-ttu-id="e7bd6-134">PSUpdateSystemServicesResponse 中的 MachineLearningCompute。</span><span class="sxs-lookup"><span data-stu-id="e7bd6-134">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSUpdateSystemServicesResponse</span></span>


## <span data-ttu-id="e7bd6-135">筆記</span><span class="sxs-lookup"><span data-stu-id="e7bd6-135">NOTES</span></span>

## <span data-ttu-id="e7bd6-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="e7bd6-136">RELATED LINKS</span></span>

