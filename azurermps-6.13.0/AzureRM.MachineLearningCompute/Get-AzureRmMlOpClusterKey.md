---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/get-azurermmlopclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
ms.openlocfilehash: 6b5797d67b709e9c44756dad018a47eb416ed174
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449078"
---
# <span data-ttu-id="c969a-101">Get-AzureRmMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="c969a-101">Get-AzureRmMlOpClusterKey</span></span>

## <span data-ttu-id="c969a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c969a-102">SYNOPSIS</span></span>
<span data-ttu-id="c969a-103">取得與 operationalization 群集相關聯的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="c969a-103">Gets the access keys associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c969a-104">句法</span><span class="sxs-lookup"><span data-stu-id="c969a-104">SYNTAX</span></span>

### <span data-ttu-id="c969a-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c969a-105">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c969a-106">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="c969a-106">GetByInputObject</span></span>
```
Get-AzureRmMlOpClusterKey -InputObject <PSOperationalizationCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c969a-107">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c969a-107">GetByResourceId</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c969a-108">說明</span><span class="sxs-lookup"><span data-stu-id="c969a-108">DESCRIPTION</span></span>
<span data-ttu-id="c969a-109">取得群集屬性時，並不會傳回與 operationalization 群集相關聯的儲存空間帳戶、容器註冊表及其他服務的按鍵。</span><span class="sxs-lookup"><span data-stu-id="c969a-109">The keys for the storage account, container registry, and other services associated with the operationalization cluster are not returned when getting the cluster properties.</span></span> <span data-ttu-id="c969a-110">必須進行特定的呼叫來取得金鑰，因為它們是機密資訊。</span><span class="sxs-lookup"><span data-stu-id="c969a-110">A specific call to retrieve the keys must be made since they are sensitive information.</span></span>

## <span data-ttu-id="c969a-111">示例</span><span class="sxs-lookup"><span data-stu-id="c969a-111">EXAMPLES</span></span>

### <span data-ttu-id="c969a-112">範例1</span><span class="sxs-lookup"><span data-stu-id="c969a-112">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpClusterKey -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="c969a-113">傳回與 operationalization 群集相關聯之服務的機密金鑰。</span><span class="sxs-lookup"><span data-stu-id="c969a-113">Returns the secret keys for the services associated with the operationalization cluster.</span></span>

## <span data-ttu-id="c969a-114">參數</span><span class="sxs-lookup"><span data-stu-id="c969a-114">PARAMETERS</span></span>

### <span data-ttu-id="c969a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c969a-115">-DefaultProfile</span></span>
<span data-ttu-id="c969a-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c969a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c969a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c969a-117">-InputObject</span></span>
<span data-ttu-id="c969a-118">Operationalization 群集物件。</span><span class="sxs-lookup"><span data-stu-id="c969a-118">The operationalization cluster object.</span></span>

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

### <span data-ttu-id="c969a-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="c969a-119">-Name</span></span>
<span data-ttu-id="c969a-120">Operationalization 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="c969a-120">The name of the operationalization cluster.</span></span>

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

### <span data-ttu-id="c969a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c969a-121">-ResourceGroupName</span></span>
<span data-ttu-id="c969a-122">Operationalization 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c969a-122">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="c969a-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c969a-123">-ResourceId</span></span>
<span data-ttu-id="c969a-124">Operationalization 群集的 Azure 資源 id。</span><span class="sxs-lookup"><span data-stu-id="c969a-124">The Azure resource id for the operationalization cluster.</span></span>

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

### <span data-ttu-id="c969a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c969a-125">CommonParameters</span></span>
<span data-ttu-id="c969a-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c969a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c969a-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c969a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c969a-128">輸入</span><span class="sxs-lookup"><span data-stu-id="c969a-128">INPUTS</span></span>

### <span data-ttu-id="c969a-129">PSOperationalizationCluster 中的 MachineLearningCompute。</span><span class="sxs-lookup"><span data-stu-id="c969a-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="c969a-130">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="c969a-130">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="c969a-131">System.object</span><span class="sxs-lookup"><span data-stu-id="c969a-131">System.String</span></span>

## <span data-ttu-id="c969a-132">輸出</span><span class="sxs-lookup"><span data-stu-id="c969a-132">OUTPUTS</span></span>

### <span data-ttu-id="c969a-133">PSOperationalizationClusterCredentials 中的 MachineLearningCompute。</span><span class="sxs-lookup"><span data-stu-id="c969a-133">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationClusterCredentials</span></span>

## <span data-ttu-id="c969a-134">筆記</span><span class="sxs-lookup"><span data-stu-id="c969a-134">NOTES</span></span>

## <span data-ttu-id="c969a-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="c969a-135">RELATED LINKS</span></span>
