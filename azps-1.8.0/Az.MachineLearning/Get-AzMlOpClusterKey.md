---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlopclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlOpClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlOpClusterKey.md
ms.openlocfilehash: d8b8a333b4d009ee1b40a8b4ddc6ed49850f1a11
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93786962"
---
# <span data-ttu-id="e41ba-101">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="e41ba-101">Get-AzMlOpClusterKey</span></span>

## <span data-ttu-id="e41ba-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e41ba-102">SYNOPSIS</span></span>
<span data-ttu-id="e41ba-103">取得與 operationalization 群集相關聯的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="e41ba-103">Gets the access keys associated with an operationalization cluster.</span></span>

## <span data-ttu-id="e41ba-104">句法</span><span class="sxs-lookup"><span data-stu-id="e41ba-104">SYNTAX</span></span>

### <span data-ttu-id="e41ba-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e41ba-105">GetByNameAndResourceGroup</span></span>
```
Get-AzMlOpClusterKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e41ba-106">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="e41ba-106">GetByInputObject</span></span>
```
Get-AzMlOpClusterKey -InputObject <PSOperationalizationCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e41ba-107">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e41ba-107">GetByResourceId</span></span>
```
Get-AzMlOpClusterKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e41ba-108">說明</span><span class="sxs-lookup"><span data-stu-id="e41ba-108">DESCRIPTION</span></span>
<span data-ttu-id="e41ba-109">取得群集屬性時，並不會傳回與 operationalization 群集相關聯的儲存空間帳戶、容器註冊表及其他服務的按鍵。</span><span class="sxs-lookup"><span data-stu-id="e41ba-109">The keys for the storage account, container registry, and other services associated with the operationalization cluster are not returned when getting the cluster properties.</span></span> <span data-ttu-id="e41ba-110">必須進行特定的呼叫來取得金鑰，因為它們是機密資訊。</span><span class="sxs-lookup"><span data-stu-id="e41ba-110">A specific call to retrieve the keys must be made since they are sensitive information.</span></span>

## <span data-ttu-id="e41ba-111">示例</span><span class="sxs-lookup"><span data-stu-id="e41ba-111">EXAMPLES</span></span>

### <span data-ttu-id="e41ba-112">範例1</span><span class="sxs-lookup"><span data-stu-id="e41ba-112">Example 1</span></span>
```
PS C:\> Get-AzMlOpClusterKey -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="e41ba-113">傳回與 operationalization 群集相關聯之服務的機密金鑰。</span><span class="sxs-lookup"><span data-stu-id="e41ba-113">Returns the secret keys for the services associated with the operationalization cluster.</span></span>

## <span data-ttu-id="e41ba-114">參數</span><span class="sxs-lookup"><span data-stu-id="e41ba-114">PARAMETERS</span></span>

### <span data-ttu-id="e41ba-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e41ba-115">-DefaultProfile</span></span>
<span data-ttu-id="e41ba-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e41ba-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e41ba-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e41ba-117">-InputObject</span></span>
<span data-ttu-id="e41ba-118">Operationalization 群集物件。</span><span class="sxs-lookup"><span data-stu-id="e41ba-118">The operationalization cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: GetByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e41ba-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="e41ba-119">-Name</span></span>
<span data-ttu-id="e41ba-120">Operationalization 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="e41ba-120">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e41ba-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e41ba-121">-ResourceGroupName</span></span>
<span data-ttu-id="e41ba-122">Operationalization 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e41ba-122">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e41ba-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e41ba-123">-ResourceId</span></span>
<span data-ttu-id="e41ba-124">Operationalization 群集的 Azure 資源 id。</span><span class="sxs-lookup"><span data-stu-id="e41ba-124">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e41ba-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e41ba-125">CommonParameters</span></span>
<span data-ttu-id="e41ba-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e41ba-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e41ba-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e41ba-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e41ba-128">輸入</span><span class="sxs-lookup"><span data-stu-id="e41ba-128">INPUTS</span></span>

### <span data-ttu-id="e41ba-129">PSOperationalizationCluster 中的 MachineLearningCompute。</span><span class="sxs-lookup"><span data-stu-id="e41ba-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="e41ba-130">System.object</span><span class="sxs-lookup"><span data-stu-id="e41ba-130">System.String</span></span>

## <span data-ttu-id="e41ba-131">輸出</span><span class="sxs-lookup"><span data-stu-id="e41ba-131">OUTPUTS</span></span>

### <span data-ttu-id="e41ba-132">PSOperationalizationClusterCredentials 中的 MachineLearningCompute。</span><span class="sxs-lookup"><span data-stu-id="e41ba-132">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationClusterCredentials</span></span>

## <span data-ttu-id="e41ba-133">筆記</span><span class="sxs-lookup"><span data-stu-id="e41ba-133">NOTES</span></span>

## <span data-ttu-id="e41ba-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="e41ba-134">RELATED LINKS</span></span>
