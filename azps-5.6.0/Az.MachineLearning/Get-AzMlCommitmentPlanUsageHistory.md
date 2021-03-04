---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/get-azmlcommitmentplanusagehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: 8baf0e2af5ebc06e51c0f8b588fe04ff3106f892
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916629"
---
# <span data-ttu-id="f7ecb-101">Get-AzMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="f7ecb-101">Get-AzMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="f7ecb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f7ecb-102">SYNOPSIS</span></span>
<span data-ttu-id="f7ecb-103">為指定的承諾計畫取回使用歷程記錄資訊。</span><span class="sxs-lookup"><span data-stu-id="f7ecb-103">Retrieves usage history information for a specified commitment plan.</span></span>

## <span data-ttu-id="f7ecb-104">語法</span><span class="sxs-lookup"><span data-stu-id="f7ecb-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7ecb-105">描述</span><span class="sxs-lookup"><span data-stu-id="f7ecb-105">DESCRIPTION</span></span>
<span data-ttu-id="f7ecb-106">為指定的承諾計畫，包括已使用的資源及計畫內的其餘資源，來取回使用歷程記錄資訊。</span><span class="sxs-lookup"><span data-stu-id="f7ecb-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="f7ecb-107">例子</span><span class="sxs-lookup"><span data-stu-id="f7ecb-107">EXAMPLES</span></span>

### <span data-ttu-id="f7ecb-108">範例 1：取得特定承諾計畫的使用歷程記錄</span><span class="sxs-lookup"><span data-stu-id="f7ecb-108">Example 1: Get usage history for a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="f7ecb-109">參數</span><span class="sxs-lookup"><span data-stu-id="f7ecb-109">PARAMETERS</span></span>

### <span data-ttu-id="f7ecb-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7ecb-110">-DefaultProfile</span></span>
<span data-ttu-id="f7ecb-111">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="f7ecb-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7ecb-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="f7ecb-112">-Name</span></span>
<span data-ttu-id="f7ecb-113">Azure ML 承諾計畫的名稱。</span><span class="sxs-lookup"><span data-stu-id="f7ecb-113">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="f7ecb-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7ecb-114">-ResourceGroupName</span></span>
<span data-ttu-id="f7ecb-115">Azure ML 承諾計畫的資源組名。</span><span class="sxs-lookup"><span data-stu-id="f7ecb-115">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="f7ecb-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7ecb-116">CommonParameters</span></span>
<span data-ttu-id="f7ecb-117">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f7ecb-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7ecb-118">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f7ecb-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7ecb-119">輸入</span><span class="sxs-lookup"><span data-stu-id="f7ecb-119">INPUTS</span></span>

### <span data-ttu-id="f7ecb-120">沒有</span><span class="sxs-lookup"><span data-stu-id="f7ecb-120">None</span></span>

## <span data-ttu-id="f7ecb-121">輸出</span><span class="sxs-lookup"><span data-stu-id="f7ecb-121">OUTPUTS</span></span>

### <span data-ttu-id="f7ecb-122">Microsoft.Azure.management.MachineLearning.CommitmentPlans.models.PlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="f7ecb-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory</span></span>

## <span data-ttu-id="f7ecb-123">筆記</span><span class="sxs-lookup"><span data-stu-id="f7ecb-123">NOTES</span></span>
<span data-ttu-id="f7ecb-124">關鍵字：azure、azurerm、arm、resource、management、manager、machine、機器學習、azureml</span><span class="sxs-lookup"><span data-stu-id="f7ecb-124">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="f7ecb-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="f7ecb-125">RELATED LINKS</span></span>
