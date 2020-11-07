---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: f0b081911d1bcd2a2b195d3185eb3b36505060c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624162"
---
# <span data-ttu-id="35b2c-101">Get-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="35b2c-101">Get-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="35b2c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="35b2c-102">SYNOPSIS</span></span>
<span data-ttu-id="35b2c-103">檢索一或多個承諾方案的摘要資訊。</span><span class="sxs-lookup"><span data-stu-id="35b2c-103">Retrieves the summary information for one or more commitment plans.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35b2c-104">句法</span><span class="sxs-lookup"><span data-stu-id="35b2c-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35b2c-105">說明</span><span class="sxs-lookup"><span data-stu-id="35b2c-105">DESCRIPTION</span></span>
<span data-ttu-id="35b2c-106">檢索承諾方案資訊。</span><span class="sxs-lookup"><span data-stu-id="35b2c-106">Retrieves commitment plan information.</span></span>
<span data-ttu-id="35b2c-107">根據傳遞的 paramenters，Cmdlet 會傳回特定的承約方案，以及目前訂閱中指定資源群組的一組承諾方案集合，或目前訂閱中的承諾方案集合。</span><span class="sxs-lookup"><span data-stu-id="35b2c-107">Depending on the paramenters passed, the cmdlet returns the a specific commitment plan, a collection of commitment plans for a specified resource group within the current subscription, or a collection of commitment plans within the current subscription.</span></span>

## <span data-ttu-id="35b2c-108">示例</span><span class="sxs-lookup"><span data-stu-id="35b2c-108">EXAMPLES</span></span>

### <span data-ttu-id="35b2c-109">範例1：取得特定的承約方案</span><span class="sxs-lookup"><span data-stu-id="35b2c-109">Example 1: Get a specific commitment plan</span></span>
```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### <span data-ttu-id="35b2c-110">範例2：取得目前訂閱中的所有承諾方案資源</span><span class="sxs-lookup"><span data-stu-id="35b2c-110">Example 2: Get all commitment plan resources in current subscription</span></span>
```
Get-AzureRmMlCommitmentPlan
```

### <span data-ttu-id="35b2c-111">範例3：取得目前訂閱與指定資源群組中的所有承諾方案</span><span class="sxs-lookup"><span data-stu-id="35b2c-111">Example 3: Get all commitment plans in the current subscription and given resource group</span></span>
```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## <span data-ttu-id="35b2c-112">參數</span><span class="sxs-lookup"><span data-stu-id="35b2c-112">PARAMETERS</span></span>

### <span data-ttu-id="35b2c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35b2c-113">-DefaultProfile</span></span>
<span data-ttu-id="35b2c-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="35b2c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35b2c-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="35b2c-115">-Name</span></span>
<span data-ttu-id="35b2c-116">承諾方案的名稱。</span><span class="sxs-lookup"><span data-stu-id="35b2c-116">The name of the commitment plan.</span></span>

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

### <span data-ttu-id="35b2c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35b2c-117">-ResourceGroupName</span></span>
<span data-ttu-id="35b2c-118">Azure ML 承諾方案之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="35b2c-118">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="35b2c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35b2c-119">CommonParameters</span></span>
<span data-ttu-id="35b2c-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="35b2c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35b2c-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="35b2c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35b2c-122">輸入</span><span class="sxs-lookup"><span data-stu-id="35b2c-122">INPUTS</span></span>

### <span data-ttu-id="35b2c-123">所有</span><span class="sxs-lookup"><span data-stu-id="35b2c-123">None</span></span>

## <span data-ttu-id="35b2c-124">輸出</span><span class="sxs-lookup"><span data-stu-id="35b2c-124">OUTPUTS</span></span>

### <span data-ttu-id="35b2c-125">MachineLearning CommitmentPlans. CommitmentPlan （）</span><span class="sxs-lookup"><span data-stu-id="35b2c-125">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="35b2c-126">筆記</span><span class="sxs-lookup"><span data-stu-id="35b2c-126">NOTES</span></span>
<span data-ttu-id="35b2c-127">關鍵字： azure，azurerm，arm，資源，管理，管理員，機器，機器學習，azureml</span><span class="sxs-lookup"><span data-stu-id="35b2c-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="35b2c-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="35b2c-128">RELATED LINKS</span></span>
