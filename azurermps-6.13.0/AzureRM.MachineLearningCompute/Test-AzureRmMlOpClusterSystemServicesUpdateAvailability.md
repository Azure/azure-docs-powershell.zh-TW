---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/test-azurermmlopclustersystemservicesupdateavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
ms.openlocfilehash: 9832faaaaf1097f53aff841f8a455680b2a40a2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449074"
---
# <span data-ttu-id="ad5f6-101">Test-AzureRmMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="ad5f6-101">Test-AzureRmMlOpClusterSystemServicesUpdateAvailability</span></span>

## <span data-ttu-id="ad5f6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ad5f6-102">SYNOPSIS</span></span>
<span data-ttu-id="ad5f6-103">檢查是否有適用于與 operationalization 群集相關聯之系統服務的更新。</span><span class="sxs-lookup"><span data-stu-id="ad5f6-103">Checks if there are updates available for the system services associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad5f6-104">句法</span><span class="sxs-lookup"><span data-stu-id="ad5f6-104">SYNTAX</span></span>

### <span data-ttu-id="ad5f6-105">TestByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ad5f6-105">TestByNameAndResourceGroup</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad5f6-106">TestByInputObject</span><span class="sxs-lookup"><span data-stu-id="ad5f6-106">TestByInputObject</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad5f6-107">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="ad5f6-107">TestByResourceId</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad5f6-108">說明</span><span class="sxs-lookup"><span data-stu-id="ad5f6-108">DESCRIPTION</span></span>
<span data-ttu-id="ad5f6-109">系統服務會獨立于 operationalization 群集接收更新。</span><span class="sxs-lookup"><span data-stu-id="ad5f6-109">System services receive updates independently from the operationalization cluster.</span></span> <span data-ttu-id="ad5f6-110">使用這個 Cmdlet 可以讓使用者知道 AzureRmMlOpClusterSystemServicesUpdate 的情況。</span><span class="sxs-lookup"><span data-stu-id="ad5f6-110">Using this cmdlet will let the user know if Invoke-AzureRmMlOpClusterSystemServicesUpdate.</span></span>

## <span data-ttu-id="ad5f6-111">示例</span><span class="sxs-lookup"><span data-stu-id="ad5f6-111">EXAMPLES</span></span>

### <span data-ttu-id="ad5f6-112">範例1</span><span class="sxs-lookup"><span data-stu-id="ad5f6-112">Example 1</span></span>
```
PS C:\> Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="ad5f6-113">範例2</span><span class="sxs-lookup"><span data-stu-id="ad5f6-113">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

### <span data-ttu-id="ad5f6-114">範例3</span><span class="sxs-lookup"><span data-stu-id="ad5f6-114">Example 3</span></span>
```
PS C:\> Find-AzureRmResource -ResourceType Microsoft.MachineLearningCompute/operationalizationClusters | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

## <span data-ttu-id="ad5f6-115">參數</span><span class="sxs-lookup"><span data-stu-id="ad5f6-115">PARAMETERS</span></span>

### <span data-ttu-id="ad5f6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad5f6-116">-DefaultProfile</span></span>
<span data-ttu-id="ad5f6-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ad5f6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad5f6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad5f6-118">-InputObject</span></span>
<span data-ttu-id="ad5f6-119">Operationalization 群集物件。</span><span class="sxs-lookup"><span data-stu-id="ad5f6-119">The operationalization cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: TestByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad5f6-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="ad5f6-120">-Name</span></span>
<span data-ttu-id="ad5f6-121">Operationalization 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="ad5f6-121">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad5f6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad5f6-122">-ResourceGroupName</span></span>
<span data-ttu-id="ad5f6-123">Operationalization 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ad5f6-123">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad5f6-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad5f6-124">-ResourceId</span></span>
<span data-ttu-id="ad5f6-125">Operationalization 群集的 Azure 資源 id。</span><span class="sxs-lookup"><span data-stu-id="ad5f6-125">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad5f6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad5f6-126">CommonParameters</span></span>
<span data-ttu-id="ad5f6-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ad5f6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad5f6-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ad5f6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad5f6-129">輸入</span><span class="sxs-lookup"><span data-stu-id="ad5f6-129">INPUTS</span></span>

### <span data-ttu-id="ad5f6-130">PSOperationalizationCluster 中的 MachineLearningCompute。</span><span class="sxs-lookup"><span data-stu-id="ad5f6-130">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="ad5f6-131">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="ad5f6-131">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="ad5f6-132">System.object</span><span class="sxs-lookup"><span data-stu-id="ad5f6-132">System.String</span></span>

## <span data-ttu-id="ad5f6-133">輸出</span><span class="sxs-lookup"><span data-stu-id="ad5f6-133">OUTPUTS</span></span>

### <span data-ttu-id="ad5f6-134">PSCheckSystemServicesUpdatesAvailableResponse 中的 MachineLearningCompute。</span><span class="sxs-lookup"><span data-stu-id="ad5f6-134">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSCheckSystemServicesUpdatesAvailableResponse</span></span>

## <span data-ttu-id="ad5f6-135">筆記</span><span class="sxs-lookup"><span data-stu-id="ad5f6-135">NOTES</span></span>

## <span data-ttu-id="ad5f6-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="ad5f6-136">RELATED LINKS</span></span>
