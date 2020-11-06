---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
ms.openlocfilehash: 4dfa855bba7318e85eb855e35227070a55d4ed73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453428"
---
# <span data-ttu-id="60862-101">Get-AzureRmMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="60862-101">Get-AzureRmMlOpClusterKey</span></span>

## <span data-ttu-id="60862-102">摘要</span><span class="sxs-lookup"><span data-stu-id="60862-102">SYNOPSIS</span></span>
<span data-ttu-id="60862-103">取得與 operationalization 群集相關聯的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="60862-103">Gets the access keys associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60862-104">句法</span><span class="sxs-lookup"><span data-stu-id="60862-104">SYNTAX</span></span>

### <span data-ttu-id="60862-105">從 Cmdlet 輸入參數取得 operationalization 群集的金鑰。</span><span class="sxs-lookup"><span data-stu-id="60862-105">Get operationalization cluster's keys from cmdlet input parameters.</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceGroupName <String> -Name <String>
```

### <span data-ttu-id="60862-106">從 OperationalizationCluster 實例定義取得 operationalization 群集的金鑰。</span><span class="sxs-lookup"><span data-stu-id="60862-106">Get operationalization cluster's keys from an OperationalizationCluster instance definition.</span></span>
```
Get-AzureRmMlOpClusterKey -Cluster <PSOperationalizationCluster>
```

### <span data-ttu-id="60862-107">從 Azure 資源識別碼取得 operationalization 群集的金鑰。</span><span class="sxs-lookup"><span data-stu-id="60862-107">Get operationalization cluster's keys from an Azure resource id.</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceId <String>
```

## <span data-ttu-id="60862-108">說明</span><span class="sxs-lookup"><span data-stu-id="60862-108">DESCRIPTION</span></span>
<span data-ttu-id="60862-109">取得群集屬性時，並不會傳回與 operationalization 群集相關聯的儲存空間帳戶、容器註冊表及其他服務的按鍵。</span><span class="sxs-lookup"><span data-stu-id="60862-109">The keys for the storage account, container registry, and other services associated with the operationalization cluster are not returned when getting the cluster properties.</span></span> <span data-ttu-id="60862-110">必須進行特定的呼叫來取得金鑰，因為它們是機密資訊。</span><span class="sxs-lookup"><span data-stu-id="60862-110">A specific call to retrieve the keys must be made since they are sensitive information.</span></span>

## <span data-ttu-id="60862-111">示例</span><span class="sxs-lookup"><span data-stu-id="60862-111">EXAMPLES</span></span>

### <span data-ttu-id="60862-112">範例1</span><span class="sxs-lookup"><span data-stu-id="60862-112">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpClusterKey -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="60862-113">傳回與 operationalization 群集相關聯之服務的機密金鑰。</span><span class="sxs-lookup"><span data-stu-id="60862-113">Returns the secret keys for the services associated with the operationalization cluster.</span></span>

## <span data-ttu-id="60862-114">參數</span><span class="sxs-lookup"><span data-stu-id="60862-114">PARAMETERS</span></span>

### <span data-ttu-id="60862-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60862-115">-InputObject</span></span>
<span data-ttu-id="60862-116">Operationalization 群集物件。</span><span class="sxs-lookup"><span data-stu-id="60862-116">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Get operationalization cluster's keys from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60862-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="60862-117">-Name</span></span>
<span data-ttu-id="60862-118">Operationalization 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="60862-118">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60862-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60862-119">-ResourceGroupName</span></span>
<span data-ttu-id="60862-120">Operationalization 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="60862-120">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60862-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60862-121">-ResourceId</span></span>
<span data-ttu-id="60862-122">Operationalization 群集的 Azure 資源 id。</span><span class="sxs-lookup"><span data-stu-id="60862-122">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="60862-123">輸入</span><span class="sxs-lookup"><span data-stu-id="60862-123">INPUTS</span></span>

### <span data-ttu-id="60862-124">PSOperationalizationCluster 中的 MachineLearningCompute。</span><span class="sxs-lookup"><span data-stu-id="60862-124">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="60862-125">System.object</span><span class="sxs-lookup"><span data-stu-id="60862-125">System.String</span></span>


## <span data-ttu-id="60862-126">輸出</span><span class="sxs-lookup"><span data-stu-id="60862-126">OUTPUTS</span></span>

### <span data-ttu-id="60862-127">PSOperationalizationClusterCredentials 中的 MachineLearningCompute。</span><span class="sxs-lookup"><span data-stu-id="60862-127">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationClusterCredentials</span></span>


## <span data-ttu-id="60862-128">筆記</span><span class="sxs-lookup"><span data-stu-id="60862-128">NOTES</span></span>

## <span data-ttu-id="60862-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="60862-129">RELATED LINKS</span></span>

