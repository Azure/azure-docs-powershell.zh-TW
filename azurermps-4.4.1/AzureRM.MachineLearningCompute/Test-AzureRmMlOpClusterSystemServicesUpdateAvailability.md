---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
ms.openlocfilehash: 067fdf88b7a7b29007f81ab26590ffaa542ac7e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624806"
---
# <span data-ttu-id="558a4-101">Test-AzureRmMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="558a4-101">Test-AzureRmMlOpClusterSystemServicesUpdateAvailability</span></span>

## <span data-ttu-id="558a4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="558a4-102">SYNOPSIS</span></span>
<span data-ttu-id="558a4-103">檢查是否有適用于與 operationalization 群集相關聯之系統服務的更新。</span><span class="sxs-lookup"><span data-stu-id="558a4-103">Checks if there are updates available for the system services associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="558a4-104">句法</span><span class="sxs-lookup"><span data-stu-id="558a4-104">SYNTAX</span></span>

### <span data-ttu-id="558a4-105">測試 Cmdlet 輸入參數的可用性更新。</span><span class="sxs-lookup"><span data-stu-id="558a4-105">Test for update availability from cmdlet input parameters.</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName <String> -Name <String>
```

### <span data-ttu-id="558a4-106">從 OperationalizationCluster 實例定義測試是否有可用的更新。</span><span class="sxs-lookup"><span data-stu-id="558a4-106">Test for update availability from an OperationalizationCluster instance definition.</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -InputObject <PSOperationalizationCluster>
```

### <span data-ttu-id="558a4-107">從 Azure 資源識別碼測試可用性更新。</span><span class="sxs-lookup"><span data-stu-id="558a4-107">Test for update availability from an Azure resouce id.</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceId <String>
```

## <span data-ttu-id="558a4-108">說明</span><span class="sxs-lookup"><span data-stu-id="558a4-108">DESCRIPTION</span></span>
<span data-ttu-id="558a4-109">系統服務會獨立于 operationalization 群集接收更新。</span><span class="sxs-lookup"><span data-stu-id="558a4-109">System services receive updates independently from the operationalization cluster.</span></span> <span data-ttu-id="558a4-110">使用這個 Cmdlet 可以讓使用者知道 AzureRmMlOpClusterSystemServicesUpdate 的情況。</span><span class="sxs-lookup"><span data-stu-id="558a4-110">Using this cmdlet will let the user know if Invoke-AzureRmMlOpClusterSystemServicesUpdate.</span></span>

## <span data-ttu-id="558a4-111">示例</span><span class="sxs-lookup"><span data-stu-id="558a4-111">EXAMPLES</span></span>

### <span data-ttu-id="558a4-112">範例1</span><span class="sxs-lookup"><span data-stu-id="558a4-112">Example 1</span></span>
```
PS C:\> Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="558a4-113">範例2</span><span class="sxs-lookup"><span data-stu-id="558a4-113">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

### <span data-ttu-id="558a4-114">範例3</span><span class="sxs-lookup"><span data-stu-id="558a4-114">Example 3</span></span>
```
PS C:\> Find-AzureRmResource -ResourceType Microsoft.MachineLearningCompute/operationalizationClusters | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

## <span data-ttu-id="558a4-115">參數</span><span class="sxs-lookup"><span data-stu-id="558a4-115">PARAMETERS</span></span>

### <span data-ttu-id="558a4-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="558a4-116">-InputObject</span></span>
<span data-ttu-id="558a4-117">Operationalization 群集物件。</span><span class="sxs-lookup"><span data-stu-id="558a4-117">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Test for update availability from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="558a4-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="558a4-118">-Name</span></span>
<span data-ttu-id="558a4-119">Operationalization 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="558a4-119">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Test for update availability from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="558a4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="558a4-120">-ResourceGroupName</span></span>
<span data-ttu-id="558a4-121">Operationalization 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="558a4-121">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Test for update availability from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="558a4-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="558a4-122">-ResourceId</span></span>
<span data-ttu-id="558a4-123">Operationalization 群集的 Azure 資源 id。</span><span class="sxs-lookup"><span data-stu-id="558a4-123">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Test for update availability from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="558a4-124">輸入</span><span class="sxs-lookup"><span data-stu-id="558a4-124">INPUTS</span></span>

### <span data-ttu-id="558a4-125">PSOperationalizationCluster 中的 MachineLearningCompute。</span><span class="sxs-lookup"><span data-stu-id="558a4-125">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
### <span data-ttu-id="558a4-126">System.object</span><span class="sxs-lookup"><span data-stu-id="558a4-126">System.String</span></span>


## <span data-ttu-id="558a4-127">輸出</span><span class="sxs-lookup"><span data-stu-id="558a4-127">OUTPUTS</span></span>

### <span data-ttu-id="558a4-128">PSCheckSystemServicesUpdatesAvailableResponse 中的 MachineLearningCompute。</span><span class="sxs-lookup"><span data-stu-id="558a4-128">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSCheckSystemServicesUpdatesAvailableResponse</span></span>


## <span data-ttu-id="558a4-129">筆記</span><span class="sxs-lookup"><span data-stu-id="558a4-129">NOTES</span></span>

## <span data-ttu-id="558a4-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="558a4-130">RELATED LINKS</span></span>

