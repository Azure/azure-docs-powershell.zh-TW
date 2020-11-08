---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
ms.openlocfilehash: 2eeaf4d4c1f0a2cf97359610d34963e32b50d1c9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141559"
---
# <span data-ttu-id="b8ab4-101">Get-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="b8ab4-101">Get-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="b8ab4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b8ab4-102">SYNOPSIS</span></span>
<span data-ttu-id="b8ab4-103">檢索一或多個承諾方案的摘要資訊。</span><span class="sxs-lookup"><span data-stu-id="b8ab4-103">Retrieves the summary information for one or more commitment plans.</span></span>

## <span data-ttu-id="b8ab4-104">句法</span><span class="sxs-lookup"><span data-stu-id="b8ab4-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8ab4-105">說明</span><span class="sxs-lookup"><span data-stu-id="b8ab4-105">DESCRIPTION</span></span>
<span data-ttu-id="b8ab4-106">檢索承諾方案資訊。</span><span class="sxs-lookup"><span data-stu-id="b8ab4-106">Retrieves commitment plan information.</span></span>
<span data-ttu-id="b8ab4-107">根據傳遞的參數，此 Cmdlet 會傳回特定的承諾計畫、目前訂閱中指定資源群組的一組承諾方案集合，或目前訂閱中的承諾方案集合。</span><span class="sxs-lookup"><span data-stu-id="b8ab4-107">Depending on the parameters passed, the cmdlet returns the a specific commitment plan, a collection of commitment plans for a specified resource group within the current subscription, or a collection of commitment plans within the current subscription.</span></span>

## <span data-ttu-id="b8ab4-108">示例</span><span class="sxs-lookup"><span data-stu-id="b8ab4-108">EXAMPLES</span></span>

### <span data-ttu-id="b8ab4-109">範例1：取得特定的承約方案</span><span class="sxs-lookup"><span data-stu-id="b8ab4-109">Example 1: Get a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### <span data-ttu-id="b8ab4-110">範例2：取得目前訂閱中的所有承諾方案資源</span><span class="sxs-lookup"><span data-stu-id="b8ab4-110">Example 2: Get all commitment plan resources in current subscription</span></span>
```
Get-AzMlCommitmentPlan
```

### <span data-ttu-id="b8ab4-111">範例3：取得目前訂閱與指定資源群組中的所有承諾方案</span><span class="sxs-lookup"><span data-stu-id="b8ab4-111">Example 3: Get all commitment plans in the current subscription and given resource group</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## <span data-ttu-id="b8ab4-112">參數</span><span class="sxs-lookup"><span data-stu-id="b8ab4-112">PARAMETERS</span></span>

### <span data-ttu-id="b8ab4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8ab4-113">-DefaultProfile</span></span>
<span data-ttu-id="b8ab4-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b8ab4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b8ab4-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="b8ab4-115">-Name</span></span>
<span data-ttu-id="b8ab4-116">承諾方案的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8ab4-116">The name of the commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8ab4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8ab4-117">-ResourceGroupName</span></span>
<span data-ttu-id="b8ab4-118">Azure ML 承諾方案之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8ab4-118">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8ab4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8ab4-119">CommonParameters</span></span>
<span data-ttu-id="b8ab4-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b8ab4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8ab4-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b8ab4-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8ab4-122">輸入</span><span class="sxs-lookup"><span data-stu-id="b8ab4-122">INPUTS</span></span>

### <span data-ttu-id="b8ab4-123">所有</span><span class="sxs-lookup"><span data-stu-id="b8ab4-123">None</span></span>

## <span data-ttu-id="b8ab4-124">輸出</span><span class="sxs-lookup"><span data-stu-id="b8ab4-124">OUTPUTS</span></span>

### <span data-ttu-id="b8ab4-125">MachineLearning CommitmentPlans. CommitmentPlan （）</span><span class="sxs-lookup"><span data-stu-id="b8ab4-125">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="b8ab4-126">筆記</span><span class="sxs-lookup"><span data-stu-id="b8ab4-126">NOTES</span></span>
<span data-ttu-id="b8ab4-127">關鍵字： azure，azurerm，arm，資源，管理，管理員，機器，機器學習，azureml</span><span class="sxs-lookup"><span data-stu-id="b8ab4-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="b8ab4-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="b8ab4-128">RELATED LINKS</span></span>
