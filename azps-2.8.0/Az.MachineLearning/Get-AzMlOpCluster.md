---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlOpCluster.md
ms.openlocfilehash: 24400b7a2c882cef81d818c5f5b94fca4235ec83
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611925"
---
# <span data-ttu-id="a1cb5-101">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="a1cb5-101">Get-AzMlOpCluster</span></span>

## <span data-ttu-id="a1cb5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a1cb5-102">SYNOPSIS</span></span>
<span data-ttu-id="a1cb5-103">取得 operationalization 群集物件。</span><span class="sxs-lookup"><span data-stu-id="a1cb5-103">Gets an operationalization cluster object.</span></span>

## <span data-ttu-id="a1cb5-104">句法</span><span class="sxs-lookup"><span data-stu-id="a1cb5-104">SYNTAX</span></span>

### <span data-ttu-id="a1cb5-105">GetByName</span><span class="sxs-lookup"><span data-stu-id="a1cb5-105">GetByName</span></span>
```
Get-AzMlOpCluster -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a1cb5-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a1cb5-106">GetByResourceGroup</span></span>
```
Get-AzMlOpCluster [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1cb5-107">說明</span><span class="sxs-lookup"><span data-stu-id="a1cb5-107">DESCRIPTION</span></span>
<span data-ttu-id="a1cb5-108">依名稱、資源群組或訂閱來取得 operationalization 群集物件。</span><span class="sxs-lookup"><span data-stu-id="a1cb5-108">Gets an operationalization cluster object by name, or by resource group, or by subscription.</span></span>

## <span data-ttu-id="a1cb5-109">示例</span><span class="sxs-lookup"><span data-stu-id="a1cb5-109">EXAMPLES</span></span>

### <span data-ttu-id="a1cb5-110">範例1</span><span class="sxs-lookup"><span data-stu-id="a1cb5-110">Example 1</span></span>
```
PS C:\> Get-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="a1cb5-111">依名稱取得特定的 operationalization 群集。</span><span class="sxs-lookup"><span data-stu-id="a1cb5-111">Gets a specific operationalization cluster by name.</span></span>

### <span data-ttu-id="a1cb5-112">範例2</span><span class="sxs-lookup"><span data-stu-id="a1cb5-112">Example 2</span></span>
```
PS C:\> Get-AzMlOpCluster -ResourceGroupName my-group
```

<span data-ttu-id="a1cb5-113">取得資源群組中的所有 operationalization 群集。</span><span class="sxs-lookup"><span data-stu-id="a1cb5-113">Gets all the operationalization clusters in a resource group.</span></span>

### <span data-ttu-id="a1cb5-114">範例3</span><span class="sxs-lookup"><span data-stu-id="a1cb5-114">Example 3</span></span>
```
PS C:\> Get-AzMlOpCluster
```

<span data-ttu-id="a1cb5-115">取得訂閱中的所有 operationalization 群集。</span><span class="sxs-lookup"><span data-stu-id="a1cb5-115">Gets all the operationalization clusters in a subscription.</span></span>

## <span data-ttu-id="a1cb5-116">參數</span><span class="sxs-lookup"><span data-stu-id="a1cb5-116">PARAMETERS</span></span>

### <span data-ttu-id="a1cb5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1cb5-117">-DefaultProfile</span></span>
<span data-ttu-id="a1cb5-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a1cb5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1cb5-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="a1cb5-119">-Name</span></span>
<span data-ttu-id="a1cb5-120">Operationalization 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1cb5-120">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1cb5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1cb5-121">-ResourceGroupName</span></span>
<span data-ttu-id="a1cb5-122">Operationalization 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1cb5-122">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1cb5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1cb5-123">CommonParameters</span></span>
<span data-ttu-id="a1cb5-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a1cb5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1cb5-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a1cb5-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1cb5-126">輸入</span><span class="sxs-lookup"><span data-stu-id="a1cb5-126">INPUTS</span></span>

### <span data-ttu-id="a1cb5-127">所有</span><span class="sxs-lookup"><span data-stu-id="a1cb5-127">None</span></span>

## <span data-ttu-id="a1cb5-128">輸出</span><span class="sxs-lookup"><span data-stu-id="a1cb5-128">OUTPUTS</span></span>

### <span data-ttu-id="a1cb5-129">PSOperationalizationCluster 中的 MachineLearningCompute。</span><span class="sxs-lookup"><span data-stu-id="a1cb5-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="a1cb5-130">筆記</span><span class="sxs-lookup"><span data-stu-id="a1cb5-130">NOTES</span></span>

## <span data-ttu-id="a1cb5-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="a1cb5-131">RELATED LINKS</span></span>
