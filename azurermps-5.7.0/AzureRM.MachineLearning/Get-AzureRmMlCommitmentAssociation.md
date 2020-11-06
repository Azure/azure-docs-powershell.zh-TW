---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentAssociation.md
ms.openlocfilehash: 3be16cd371543848d650711241dbcb8828a5ba32
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455391"
---
# <span data-ttu-id="6ee86-101">Get-AzureRmMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="6ee86-101">Get-AzureRmMlCommitmentAssociation</span></span>

## <span data-ttu-id="6ee86-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6ee86-102">SYNOPSIS</span></span>
<span data-ttu-id="6ee86-103">檢索一或多個承諾關聯的摘要資訊。</span><span class="sxs-lookup"><span data-stu-id="6ee86-103">Retrieves the summary information for one or more commitment associations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ee86-104">句法</span><span class="sxs-lookup"><span data-stu-id="6ee86-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ee86-105">說明</span><span class="sxs-lookup"><span data-stu-id="6ee86-105">DESCRIPTION</span></span>
<span data-ttu-id="6ee86-106">檢索承諾關聯資訊。</span><span class="sxs-lookup"><span data-stu-id="6ee86-106">Retrieves commitment association information.</span></span>
<span data-ttu-id="6ee86-107">根據傳遞的 paramenters，Cmdlet 會針對指定的承諾方案傳回特定的「承諾關聯」或「承諾關聯」集合。</span><span class="sxs-lookup"><span data-stu-id="6ee86-107">Depending on the paramenters passed, the cmdlet returns a specific commitment association or a collection of commitment associations for the specified commitment plan.</span></span>

## <span data-ttu-id="6ee86-108">示例</span><span class="sxs-lookup"><span data-stu-id="6ee86-108">EXAMPLES</span></span>

### <span data-ttu-id="6ee86-109">--------------------------範例1：取得特定的承諾關聯--------------------------</span><span class="sxs-lookup"><span data-stu-id="6ee86-109">--------------------------  Example 1: Get a specific commitment association  --------------------------</span></span>
```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName" -Name "MyCommitmentAssociationName"
```

### <span data-ttu-id="6ee86-110">--------------------------範例2：取得指定承諾方案的所有承諾關聯--------------------------</span><span class="sxs-lookup"><span data-stu-id="6ee86-110">--------------------------  Example 2: Get all commitment associations for the specified commitment plan  --------------------------</span></span>
```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName"
```

## <span data-ttu-id="6ee86-111">參數</span><span class="sxs-lookup"><span data-stu-id="6ee86-111">PARAMETERS</span></span>

### <span data-ttu-id="6ee86-112">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="6ee86-112">-CommitmentPlanName</span></span>
<span data-ttu-id="6ee86-113">包含一或多個承諾關聯的 Azure ML 提交方案名稱。</span><span class="sxs-lookup"><span data-stu-id="6ee86-113">The name of the Azure ML commitment plan which has one or more commitment associations.</span></span>

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

### <span data-ttu-id="6ee86-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ee86-114">-DefaultProfile</span></span>
<span data-ttu-id="6ee86-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="6ee86-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6ee86-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="6ee86-116">-Name</span></span>
<span data-ttu-id="6ee86-117">Azure ML 承諾協會的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ee86-117">The name of the Azure ML commitment association.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ee86-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ee86-118">-ResourceGroupName</span></span>
<span data-ttu-id="6ee86-119">Azure ML 承諾協會之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ee86-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="6ee86-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ee86-120">CommonParameters</span></span>
<span data-ttu-id="6ee86-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6ee86-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ee86-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6ee86-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ee86-123">輸入</span><span class="sxs-lookup"><span data-stu-id="6ee86-123">INPUTS</span></span>

### <span data-ttu-id="6ee86-124">所有</span><span class="sxs-lookup"><span data-stu-id="6ee86-124">None</span></span>
<span data-ttu-id="6ee86-125">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="6ee86-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6ee86-126">輸出</span><span class="sxs-lookup"><span data-stu-id="6ee86-126">OUTPUTS</span></span>

### <span data-ttu-id="6ee86-127">MachineLearning CommitmentPlans. CommitmentPlan （）</span><span class="sxs-lookup"><span data-stu-id="6ee86-127">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="6ee86-128">CommitmentPlan []. MachineLearning [CommitmentPlans]</span><span class="sxs-lookup"><span data-stu-id="6ee86-128">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan[]</span></span>

## <span data-ttu-id="6ee86-129">筆記</span><span class="sxs-lookup"><span data-stu-id="6ee86-129">NOTES</span></span>
<span data-ttu-id="6ee86-130">關鍵字： azure，azurerm，arm，資源，管理，管理員，機器，機器學習，azureml</span><span class="sxs-lookup"><span data-stu-id="6ee86-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="6ee86-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="6ee86-131">RELATED LINKS</span></span>

