---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/get-azmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentAssociation.md
ms.openlocfilehash: 9d58d8385d3f1d02e3bd823f43403d7dcdacf4a5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917158"
---
# <span data-ttu-id="280e3-101">Get-AzMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="280e3-101">Get-AzMlCommitmentAssociation</span></span>

## <span data-ttu-id="280e3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="280e3-102">SYNOPSIS</span></span>
<span data-ttu-id="280e3-103">為一或多個承諾關聯取摘要資訊。</span><span class="sxs-lookup"><span data-stu-id="280e3-103">Retrieves the summary information for one or more commitment associations.</span></span>

## <span data-ttu-id="280e3-104">語法</span><span class="sxs-lookup"><span data-stu-id="280e3-104">SYNTAX</span></span>

```
Get-AzMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="280e3-105">描述</span><span class="sxs-lookup"><span data-stu-id="280e3-105">DESCRIPTION</span></span>
<span data-ttu-id="280e3-106">會取回承諾關聯資訊。</span><span class="sxs-lookup"><span data-stu-id="280e3-106">Retrieves commitment association information.</span></span>
<span data-ttu-id="280e3-107">根據傳遞的參數，Cmdlet 會傳回指定承諾計畫的特定承諾關聯或承諾關聯集合。</span><span class="sxs-lookup"><span data-stu-id="280e3-107">Depending on the parameters passed, the cmdlet returns a specific commitment association or a collection of commitment associations for the specified commitment plan.</span></span>

## <span data-ttu-id="280e3-108">例子</span><span class="sxs-lookup"><span data-stu-id="280e3-108">EXAMPLES</span></span>

### <span data-ttu-id="280e3-109">範例 1：取得特定的承諾關聯</span><span class="sxs-lookup"><span data-stu-id="280e3-109">Example 1: Get a specific commitment association</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName" -Name "MyCommitmentAssociationName"
```

### <span data-ttu-id="280e3-110">範例 2：取得指定承諾計畫的所有承諾關聯</span><span class="sxs-lookup"><span data-stu-id="280e3-110">Example 2: Get all commitment associations for the specified commitment plan</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName"
```

## <span data-ttu-id="280e3-111">參數</span><span class="sxs-lookup"><span data-stu-id="280e3-111">PARAMETERS</span></span>

### <span data-ttu-id="280e3-112">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="280e3-112">-CommitmentPlanName</span></span>
<span data-ttu-id="280e3-113">具有一或多個承諾關聯之 Azure ML 承諾計畫的名稱。</span><span class="sxs-lookup"><span data-stu-id="280e3-113">The name of the Azure ML commitment plan which has one or more commitment associations.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="280e3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="280e3-114">-DefaultProfile</span></span>
<span data-ttu-id="280e3-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="280e3-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="280e3-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="280e3-116">-Name</span></span>
<span data-ttu-id="280e3-117">Azure ML 承諾關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="280e3-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="280e3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="280e3-118">-ResourceGroupName</span></span>
<span data-ttu-id="280e3-119">Azure ML 承諾關聯之資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="280e3-119">The name of the resource group for the Azure ML commitment association.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="280e3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="280e3-120">CommonParameters</span></span>
<span data-ttu-id="280e3-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="280e3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="280e3-122">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="280e3-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="280e3-123">輸入</span><span class="sxs-lookup"><span data-stu-id="280e3-123">INPUTS</span></span>

### <span data-ttu-id="280e3-124">沒有</span><span class="sxs-lookup"><span data-stu-id="280e3-124">None</span></span>

## <span data-ttu-id="280e3-125">輸出</span><span class="sxs-lookup"><span data-stu-id="280e3-125">OUTPUTS</span></span>

### <span data-ttu-id="280e3-126">Microsoft.Azure.management.MachineLearning.CommitmentPlans.models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="280e3-126">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="280e3-127">筆記</span><span class="sxs-lookup"><span data-stu-id="280e3-127">NOTES</span></span>
<span data-ttu-id="280e3-128">關鍵字：azure、azurerm、arm、resource、management、manager、machine、機器學習、azureml</span><span class="sxs-lookup"><span data-stu-id="280e3-128">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="280e3-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="280e3-129">RELATED LINKS</span></span>
