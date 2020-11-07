---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/get-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
ms.openlocfilehash: 0e9eecf16a26be5367df5d8ad8b45a40e0050da3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624086"
---
# <span data-ttu-id="f502c-101">Get-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="f502c-101">Get-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="f502c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f502c-102">SYNOPSIS</span></span>
<span data-ttu-id="f502c-103">取得 operationalization 群集物件。</span><span class="sxs-lookup"><span data-stu-id="f502c-103">Gets an operationalization cluster object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f502c-104">句法</span><span class="sxs-lookup"><span data-stu-id="f502c-104">SYNTAX</span></span>

### <span data-ttu-id="f502c-105">GetByName</span><span class="sxs-lookup"><span data-stu-id="f502c-105">GetByName</span></span>
```
Get-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f502c-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f502c-106">GetByResourceGroup</span></span>
```
Get-AzureRmMlOpCluster [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f502c-107">說明</span><span class="sxs-lookup"><span data-stu-id="f502c-107">DESCRIPTION</span></span>
<span data-ttu-id="f502c-108">依名稱、資源群組或訂閱來取得 operationalization 群集物件。</span><span class="sxs-lookup"><span data-stu-id="f502c-108">Gets an operationalization cluster object by name, or by resource group, or by subscription.</span></span>

## <span data-ttu-id="f502c-109">示例</span><span class="sxs-lookup"><span data-stu-id="f502c-109">EXAMPLES</span></span>

### <span data-ttu-id="f502c-110">範例1</span><span class="sxs-lookup"><span data-stu-id="f502c-110">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="f502c-111">依名稱取得特定的 operationalization 群集。</span><span class="sxs-lookup"><span data-stu-id="f502c-111">Gets a specific operationalization cluster by name.</span></span>

### <span data-ttu-id="f502c-112">範例2</span><span class="sxs-lookup"><span data-stu-id="f502c-112">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group
```

<span data-ttu-id="f502c-113">取得資源群組中的所有 operationalization 群集。</span><span class="sxs-lookup"><span data-stu-id="f502c-113">Gets all the operationalization clusters in a resource group.</span></span>

### <span data-ttu-id="f502c-114">範例3</span><span class="sxs-lookup"><span data-stu-id="f502c-114">Example 3</span></span>
```
PS C:\> Get-AzureRmMlOpCluster
```

<span data-ttu-id="f502c-115">取得訂閱中的所有 operationalization 群集。</span><span class="sxs-lookup"><span data-stu-id="f502c-115">Gets all the operationalization clusters in a subscription.</span></span>

## <span data-ttu-id="f502c-116">參數</span><span class="sxs-lookup"><span data-stu-id="f502c-116">PARAMETERS</span></span>

### <span data-ttu-id="f502c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f502c-117">-DefaultProfile</span></span>
<span data-ttu-id="f502c-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f502c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f502c-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="f502c-119">-Name</span></span>
<span data-ttu-id="f502c-120">Operationalization 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="f502c-120">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f502c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f502c-121">-ResourceGroupName</span></span>
<span data-ttu-id="f502c-122">Operationalization 群集之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f502c-122">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetByResourceGroup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f502c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f502c-123">CommonParameters</span></span>
<span data-ttu-id="f502c-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f502c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f502c-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f502c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f502c-126">輸入</span><span class="sxs-lookup"><span data-stu-id="f502c-126">INPUTS</span></span>

### <span data-ttu-id="f502c-127">所有</span><span class="sxs-lookup"><span data-stu-id="f502c-127">None</span></span>

## <span data-ttu-id="f502c-128">輸出</span><span class="sxs-lookup"><span data-stu-id="f502c-128">OUTPUTS</span></span>

### <span data-ttu-id="f502c-129">PSOperationalizationCluster 中的 MachineLearningCompute。</span><span class="sxs-lookup"><span data-stu-id="f502c-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="f502c-130">[System.object]。清單 ' 1 [MachineLearningCompute. PSOperationalizationCluster，MachineLearningCompute，版本 = 0.1.0.0，Culture = 中性，PublicKeyToken = null]]。）））</span><span class="sxs-lookup"><span data-stu-id="f502c-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster, Microsoft.Azure.Commands.MachineLearningCompute, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f502c-131">筆記</span><span class="sxs-lookup"><span data-stu-id="f502c-131">NOTES</span></span>

## <span data-ttu-id="f502c-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="f502c-132">RELATED LINKS</span></span>

