---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: 9f9789d288773b16b2003e23b00674c12ca08738
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451660"
---
# <span data-ttu-id="0d4d2-101">Get-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="0d4d2-101">Get-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="0d4d2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0d4d2-102">SYNOPSIS</span></span>
<span data-ttu-id="0d4d2-103">檢索一或多個承諾方案的摘要資訊。</span><span class="sxs-lookup"><span data-stu-id="0d4d2-103">Retrieves the summary information for one or more commitment plans.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d4d2-104">句法</span><span class="sxs-lookup"><span data-stu-id="0d4d2-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d4d2-105">說明</span><span class="sxs-lookup"><span data-stu-id="0d4d2-105">DESCRIPTION</span></span>
<span data-ttu-id="0d4d2-106">檢索承諾方案資訊。</span><span class="sxs-lookup"><span data-stu-id="0d4d2-106">Retrieves commitment plan information.</span></span>
<span data-ttu-id="0d4d2-107">根據傳遞的 paramenters，Cmdlet 會傳回特定的承約方案，以及目前訂閱中指定資源群組的一組承諾方案集合，或目前訂閱中的承諾方案集合。</span><span class="sxs-lookup"><span data-stu-id="0d4d2-107">Depending on the paramenters passed, the cmdlet returns the a specific commitment plan, a collection of commitment plans for a specified resource group within the current subscription, or a collection of commitment plans within the current subscription.</span></span>

## <span data-ttu-id="0d4d2-108">示例</span><span class="sxs-lookup"><span data-stu-id="0d4d2-108">EXAMPLES</span></span>

### <span data-ttu-id="0d4d2-109">--------------------------範例1：取得特定的承約方案--------------------------</span><span class="sxs-lookup"><span data-stu-id="0d4d2-109">--------------------------  Example 1: Get a specific commitment plan  --------------------------</span></span>
<span data-ttu-id="0d4d2-110">@ {段落 = PS C： \\ \> }</span><span class="sxs-lookup"><span data-stu-id="0d4d2-110">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### <span data-ttu-id="0d4d2-111">--------------------------範例2：取得目前訂閱中的所有承諾方案資源--------------------------</span><span class="sxs-lookup"><span data-stu-id="0d4d2-111">--------------------------  Example 2: Get all commitment plan resources in current subscription  --------------------------</span></span>
<span data-ttu-id="0d4d2-112">@ {段落 = PS C： \\ \> }</span><span class="sxs-lookup"><span data-stu-id="0d4d2-112">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentPlan
```

### <span data-ttu-id="0d4d2-113">--------------------------範例3：取得目前訂閱和指定資源群組中的所有承諾方案--------------------------</span><span class="sxs-lookup"><span data-stu-id="0d4d2-113">--------------------------  Example 3: Get all commitment plans in the current subscription and given resource group  --------------------------</span></span>
<span data-ttu-id="0d4d2-114">@ {段落 = PS C： \\ \> }</span><span class="sxs-lookup"><span data-stu-id="0d4d2-114">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## <span data-ttu-id="0d4d2-115">參數</span><span class="sxs-lookup"><span data-stu-id="0d4d2-115">PARAMETERS</span></span>

### <span data-ttu-id="0d4d2-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="0d4d2-116">-Name</span></span>
<span data-ttu-id="0d4d2-117">承諾方案的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d4d2-117">The name of the commitment plan.</span></span>

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

### <span data-ttu-id="0d4d2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d4d2-118">-ResourceGroupName</span></span>
<span data-ttu-id="0d4d2-119">Azure ML 承諾方案之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d4d2-119">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="0d4d2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d4d2-120">-DefaultProfile</span></span>
<span data-ttu-id="0d4d2-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0d4d2-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d4d2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d4d2-122">CommonParameters</span></span>
<span data-ttu-id="0d4d2-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0d4d2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d4d2-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0d4d2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d4d2-125">輸入</span><span class="sxs-lookup"><span data-stu-id="0d4d2-125">INPUTS</span></span>

## <span data-ttu-id="0d4d2-126">輸出</span><span class="sxs-lookup"><span data-stu-id="0d4d2-126">OUTPUTS</span></span>

### <span data-ttu-id="0d4d2-127">MachineLearning CommitmentPlans. CommitmentPlan （）</span><span class="sxs-lookup"><span data-stu-id="0d4d2-127">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="0d4d2-128">CommitmentPlan []. MachineLearning [CommitmentPlans]</span><span class="sxs-lookup"><span data-stu-id="0d4d2-128">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan[]</span></span>

## <span data-ttu-id="0d4d2-129">筆記</span><span class="sxs-lookup"><span data-stu-id="0d4d2-129">NOTES</span></span>
<span data-ttu-id="0d4d2-130">關鍵字： azure，azurerm，arm，資源，管理，管理員，機器，機器學習，azureml</span><span class="sxs-lookup"><span data-stu-id="0d4d2-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="0d4d2-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="0d4d2-131">RELATED LINKS</span></span>

