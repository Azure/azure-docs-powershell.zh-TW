---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/get-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
ms.openlocfilehash: b3ea89f2470052a0d5858da199ee5285b3d5ea18
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905378"
---
# <span data-ttu-id="360a9-101">Get-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="360a9-101">Get-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="360a9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="360a9-102">SYNOPSIS</span></span>
<span data-ttu-id="360a9-103">為一或多個承諾計畫摘要資訊。</span><span class="sxs-lookup"><span data-stu-id="360a9-103">Retrieves the summary information for one or more commitment plans.</span></span>

## <span data-ttu-id="360a9-104">語法</span><span class="sxs-lookup"><span data-stu-id="360a9-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="360a9-105">描述</span><span class="sxs-lookup"><span data-stu-id="360a9-105">DESCRIPTION</span></span>
<span data-ttu-id="360a9-106">會取回承諾計畫資訊。</span><span class="sxs-lookup"><span data-stu-id="360a9-106">Retrieves commitment plan information.</span></span>
<span data-ttu-id="360a9-107">根據傳遞的參數，Cmdlet 會傳回特定承諾計畫、目前訂閱中指定資源群組的承諾計畫集合，或目前訂閱內的承諾計畫集合。</span><span class="sxs-lookup"><span data-stu-id="360a9-107">Depending on the parameters passed, the cmdlet returns the a specific commitment plan, a collection of commitment plans for a specified resource group within the current subscription, or a collection of commitment plans within the current subscription.</span></span>

## <span data-ttu-id="360a9-108">例子</span><span class="sxs-lookup"><span data-stu-id="360a9-108">EXAMPLES</span></span>

### <span data-ttu-id="360a9-109">範例 1：取得特定的承諾計畫</span><span class="sxs-lookup"><span data-stu-id="360a9-109">Example 1: Get a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### <span data-ttu-id="360a9-110">範例 2：取得目前訂閱的所有承諾計畫資源</span><span class="sxs-lookup"><span data-stu-id="360a9-110">Example 2: Get all commitment plan resources in current subscription</span></span>
```
Get-AzMlCommitmentPlan
```

### <span data-ttu-id="360a9-111">範例 3：取得目前訂閱和給定資源群組的所有承諾計畫</span><span class="sxs-lookup"><span data-stu-id="360a9-111">Example 3: Get all commitment plans in the current subscription and given resource group</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## <span data-ttu-id="360a9-112">參數</span><span class="sxs-lookup"><span data-stu-id="360a9-112">PARAMETERS</span></span>

### <span data-ttu-id="360a9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="360a9-113">-DefaultProfile</span></span>
<span data-ttu-id="360a9-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="360a9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="360a9-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="360a9-115">-Name</span></span>
<span data-ttu-id="360a9-116">承諾計畫的名稱。</span><span class="sxs-lookup"><span data-stu-id="360a9-116">The name of the commitment plan.</span></span>

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

### <span data-ttu-id="360a9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="360a9-117">-ResourceGroupName</span></span>
<span data-ttu-id="360a9-118">Azure ML 承諾計畫的資源組名。</span><span class="sxs-lookup"><span data-stu-id="360a9-118">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="360a9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="360a9-119">CommonParameters</span></span>
<span data-ttu-id="360a9-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="360a9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="360a9-121">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="360a9-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="360a9-122">輸入</span><span class="sxs-lookup"><span data-stu-id="360a9-122">INPUTS</span></span>

### <span data-ttu-id="360a9-123">沒有</span><span class="sxs-lookup"><span data-stu-id="360a9-123">None</span></span>

## <span data-ttu-id="360a9-124">輸出</span><span class="sxs-lookup"><span data-stu-id="360a9-124">OUTPUTS</span></span>

### <span data-ttu-id="360a9-125">Microsoft.Azure.management.MachineLearning.CommitmentPlans.models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="360a9-125">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="360a9-126">筆記</span><span class="sxs-lookup"><span data-stu-id="360a9-126">NOTES</span></span>
<span data-ttu-id="360a9-127">關鍵字：azure、azurerm、arm、resource、management、manager、machine、機器學習、azureml</span><span class="sxs-lookup"><span data-stu-id="360a9-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="360a9-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="360a9-128">RELATED LINKS</span></span>
