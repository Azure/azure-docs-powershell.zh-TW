---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/test-azmlopclustersystemservicesupdateavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Test-AzMlOpClusterSystemServicesUpdateAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Test-AzMlOpClusterSystemServicesUpdateAvailability.md
ms.openlocfilehash: d05f8b746dbd212c834e3554639340fa6075c216
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93786918"
---
# <span data-ttu-id="410eb-101">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="410eb-101">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>

## <span data-ttu-id="410eb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="410eb-102">SYNOPSIS</span></span>
<span data-ttu-id="410eb-103">檢查是否有適用于與 operationalization 群集相關聯之系統服務的更新。</span><span class="sxs-lookup"><span data-stu-id="410eb-103">Checks if there are updates available for the system services associated with an operationalization cluster.</span></span>

## <span data-ttu-id="410eb-104">句法</span><span class="sxs-lookup"><span data-stu-id="410eb-104">SYNTAX</span></span>

### <span data-ttu-id="410eb-105">TestByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="410eb-105">TestByNameAndResourceGroup</span></span>
```
Test-AzMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="410eb-106">TestByInputObject</span><span class="sxs-lookup"><span data-stu-id="410eb-106">TestByInputObject</span></span>
```
Test-AzMlOpClusterSystemServicesUpdateAvailability -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="410eb-107">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="410eb-107">TestByResourceId</span></span>
```
Test-AzMlOpClusterSystemServicesUpdateAvailability -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="410eb-108">說明</span><span class="sxs-lookup"><span data-stu-id="410eb-108">DESCRIPTION</span></span>
<span data-ttu-id="410eb-109">系統服務會獨立于 operationalization 群集接收更新。</span><span class="sxs-lookup"><span data-stu-id="410eb-109">System services receive updates independently from the operationalization cluster.</span></span> <span data-ttu-id="410eb-110">使用這個 Cmdlet 可以讓使用者知道 AzMlOpClusterSystemServicesUpdate 的情況。</span><span class="sxs-lookup"><span data-stu-id="410eb-110">Using this cmdlet will let the user know if Invoke-AzMlOpClusterSystemServicesUpdate.</span></span>

## <span data-ttu-id="410eb-111">示例</span><span class="sxs-lookup"><span data-stu-id="410eb-111">EXAMPLES</span></span>

### <span data-ttu-id="410eb-112">範例1</span><span class="sxs-lookup"><span data-stu-id="410eb-112">Example 1</span></span>
```
PS C:\> Test-AzMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="410eb-113">範例2</span><span class="sxs-lookup"><span data-stu-id="410eb-113">Example 2</span></span>
```
PS C:\> Get-AzMlOpCluster | Test-AzMlOpClusterSystemServicesUpdateAvailability
```

### <span data-ttu-id="410eb-114">範例3</span><span class="sxs-lookup"><span data-stu-id="410eb-114">Example 3</span></span>
```
PS C:\> Find-AzResource -ResourceType Microsoft.MachineLearningCompute/operationalizationClusters | Test-AzMlOpClusterSystemServicesUpdateAvailability
```

## <span data-ttu-id="410eb-115">參數</span><span class="sxs-lookup"><span data-stu-id="410eb-115">PARAMETERS</span></span>

### <span data-ttu-id="410eb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="410eb-116">-DefaultProfile</span></span>
<span data-ttu-id="410eb-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="410eb-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="410eb-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="410eb-118">-InputObject</span></span>
<span data-ttu-id="410eb-119">Operationalization 群集物件。</span><span class="sxs-lookup"><span data-stu-id="410eb-119">The operationalization cluster object.</span></span>

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

### <span data-ttu-id="410eb-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="410eb-120">-Name</span></span>
<span data-ttu-id="410eb-121">Operationalization 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="410eb-121">The name of the operationalization cluster.</span></span>

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

### <span data-ttu-id="410eb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="410eb-122">-ResourceGroupName</span></span>
<span data-ttu-id="410eb-123">Operationalization 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="410eb-123">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="410eb-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="410eb-124">-ResourceId</span></span>
<span data-ttu-id="410eb-125">Operationalization 群集的 Azure 資源 id。</span><span class="sxs-lookup"><span data-stu-id="410eb-125">The Azure resource id for the operationalization cluster.</span></span>

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

### <span data-ttu-id="410eb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="410eb-126">CommonParameters</span></span>
<span data-ttu-id="410eb-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="410eb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="410eb-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="410eb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="410eb-129">輸入</span><span class="sxs-lookup"><span data-stu-id="410eb-129">INPUTS</span></span>

### <span data-ttu-id="410eb-130">PSOperationalizationCluster 中的 MachineLearningCompute。</span><span class="sxs-lookup"><span data-stu-id="410eb-130">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="410eb-131">System.object</span><span class="sxs-lookup"><span data-stu-id="410eb-131">System.String</span></span>

## <span data-ttu-id="410eb-132">輸出</span><span class="sxs-lookup"><span data-stu-id="410eb-132">OUTPUTS</span></span>

### <span data-ttu-id="410eb-133">PSCheckSystemServicesUpdatesAvailableResponse 中的 MachineLearningCompute。</span><span class="sxs-lookup"><span data-stu-id="410eb-133">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSCheckSystemServicesUpdatesAvailableResponse</span></span>

## <span data-ttu-id="410eb-134">筆記</span><span class="sxs-lookup"><span data-stu-id="410eb-134">NOTES</span></span>

## <span data-ttu-id="410eb-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="410eb-135">RELATED LINKS</span></span>
