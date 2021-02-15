---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentAssociation.md
ms.openlocfilehash: 415645b1b4c1d0094b1466d833a29aa10b2b83b8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100136099"
---
# <span data-ttu-id="e8210-101">Get-AzMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="e8210-101">Get-AzMlCommitmentAssociation</span></span>

## <span data-ttu-id="e8210-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8210-102">SYNOPSIS</span></span>
<span data-ttu-id="e8210-103">檢索一或多個承諾關聯的摘要資訊。</span><span class="sxs-lookup"><span data-stu-id="e8210-103">Retrieves the summary information for one or more commitment associations.</span></span>

## <span data-ttu-id="e8210-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8210-104">SYNTAX</span></span>

```
Get-AzMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8210-105">說明</span><span class="sxs-lookup"><span data-stu-id="e8210-105">DESCRIPTION</span></span>
<span data-ttu-id="e8210-106">檢索承諾關聯資訊。</span><span class="sxs-lookup"><span data-stu-id="e8210-106">Retrieves commitment association information.</span></span>
<span data-ttu-id="e8210-107">根據傳遞的參數，此 Cmdlet 會傳回特定的承諾關聯或指定承諾方案的一組承諾關聯性。</span><span class="sxs-lookup"><span data-stu-id="e8210-107">Depending on the parameters passed, the cmdlet returns a specific commitment association or a collection of commitment associations for the specified commitment plan.</span></span>

## <span data-ttu-id="e8210-108">示例</span><span class="sxs-lookup"><span data-stu-id="e8210-108">EXAMPLES</span></span>

### <span data-ttu-id="e8210-109">範例1：取得特定的承諾關聯</span><span class="sxs-lookup"><span data-stu-id="e8210-109">Example 1: Get a specific commitment association</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName" -Name "MyCommitmentAssociationName"
```

### <span data-ttu-id="e8210-110">範例2：取得指定承諾方案的所有承諾關聯</span><span class="sxs-lookup"><span data-stu-id="e8210-110">Example 2: Get all commitment associations for the specified commitment plan</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName"
```

## <span data-ttu-id="e8210-111">參數</span><span class="sxs-lookup"><span data-stu-id="e8210-111">PARAMETERS</span></span>

### <span data-ttu-id="e8210-112">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="e8210-112">-CommitmentPlanName</span></span>
<span data-ttu-id="e8210-113">包含一或多個承諾關聯的 Azure ML 提交方案名稱。</span><span class="sxs-lookup"><span data-stu-id="e8210-113">The name of the Azure ML commitment plan which has one or more commitment associations.</span></span>

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

### <span data-ttu-id="e8210-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8210-114">-DefaultProfile</span></span>
<span data-ttu-id="e8210-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e8210-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8210-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="e8210-116">-Name</span></span>
<span data-ttu-id="e8210-117">Azure ML 承諾協會的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8210-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="e8210-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8210-118">-ResourceGroupName</span></span>
<span data-ttu-id="e8210-119">Azure ML 承諾協會之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8210-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="e8210-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8210-120">CommonParameters</span></span>
<span data-ttu-id="e8210-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8210-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8210-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e8210-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8210-123">輸入</span><span class="sxs-lookup"><span data-stu-id="e8210-123">INPUTS</span></span>

### <span data-ttu-id="e8210-124">所有</span><span class="sxs-lookup"><span data-stu-id="e8210-124">None</span></span>

## <span data-ttu-id="e8210-125">輸出</span><span class="sxs-lookup"><span data-stu-id="e8210-125">OUTPUTS</span></span>

### <span data-ttu-id="e8210-126">MachineLearning CommitmentPlans. CommitmentPlan （）</span><span class="sxs-lookup"><span data-stu-id="e8210-126">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="e8210-127">筆記</span><span class="sxs-lookup"><span data-stu-id="e8210-127">NOTES</span></span>
<span data-ttu-id="e8210-128">關鍵字： azure，azurerm，arm，資源，管理，管理員，機器，機器學習，azureml</span><span class="sxs-lookup"><span data-stu-id="e8210-128">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="e8210-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8210-129">RELATED LINKS</span></span>
