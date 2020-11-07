---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlcommitmentplanusagehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: e92f32dab72a4a96be03f800297194711f275d70
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "93626655"
---
# <span data-ttu-id="e3692-101">Get-AzureRmMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="e3692-101">Get-AzureRmMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="e3692-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e3692-102">SYNOPSIS</span></span>
<span data-ttu-id="e3692-103">檢索指定承諾方案的使用狀況歷程記錄資訊。</span><span class="sxs-lookup"><span data-stu-id="e3692-103">Retrieves usage history information for a specified commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3692-104">句法</span><span class="sxs-lookup"><span data-stu-id="e3692-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3692-105">說明</span><span class="sxs-lookup"><span data-stu-id="e3692-105">DESCRIPTION</span></span>
<span data-ttu-id="e3692-106">檢索指定承諾方案的使用方式歷程記錄資訊，包括所使用的資源，以及方案中剩餘的資源。</span><span class="sxs-lookup"><span data-stu-id="e3692-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="e3692-107">示例</span><span class="sxs-lookup"><span data-stu-id="e3692-107">EXAMPLES</span></span>

### <span data-ttu-id="e3692-108">--------------------------範例1：取得特定承諾方案的使用狀況歷程記錄--------------------------</span><span class="sxs-lookup"><span data-stu-id="e3692-108">--------------------------  Example 1: Get usage history for a specific commitment plan  --------------------------</span></span>
```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="e3692-109">參數</span><span class="sxs-lookup"><span data-stu-id="e3692-109">PARAMETERS</span></span>

### <span data-ttu-id="e3692-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3692-110">-DefaultProfile</span></span>
<span data-ttu-id="e3692-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e3692-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3692-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="e3692-112">-Name</span></span>
<span data-ttu-id="e3692-113">Azure ML 提交方案的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3692-113">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3692-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3692-114">-ResourceGroupName</span></span>
<span data-ttu-id="e3692-115">Azure ML 承諾方案之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3692-115">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3692-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3692-116">CommonParameters</span></span>
<span data-ttu-id="e3692-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e3692-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3692-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e3692-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3692-119">輸入</span><span class="sxs-lookup"><span data-stu-id="e3692-119">INPUTS</span></span>

### <span data-ttu-id="e3692-120">所有</span><span class="sxs-lookup"><span data-stu-id="e3692-120">None</span></span>
<span data-ttu-id="e3692-121">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="e3692-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e3692-122">輸出</span><span class="sxs-lookup"><span data-stu-id="e3692-122">OUTPUTS</span></span>

### <span data-ttu-id="e3692-123">PlanUsageHistory []. MachineLearning [CommitmentPlans]</span><span class="sxs-lookup"><span data-stu-id="e3692-123">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory[]</span></span>

## <span data-ttu-id="e3692-124">筆記</span><span class="sxs-lookup"><span data-stu-id="e3692-124">NOTES</span></span>
<span data-ttu-id="e3692-125">關鍵字： azure，azurerm，arm，資源，管理，管理員，機器，機器學習，azureml</span><span class="sxs-lookup"><span data-stu-id="e3692-125">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="e3692-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3692-126">RELATED LINKS</span></span>

